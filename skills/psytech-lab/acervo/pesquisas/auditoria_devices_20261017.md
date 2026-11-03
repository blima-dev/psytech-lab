# Catálogo de armadilhas — auditoria de devices, plugins, samples e lanes em um Set de Live 12.4.6 (17/10/2026)

Auditoria completa de um set real de minimal psytech: **73 canais** (70 pistas [5 grupos, 41 MIDI, 24 áudio] + 2 retornos + master), **406 devices**, **37 instâncias de Serum 2 / Serum 2 FX** (32 VST3 + 5 AU), **28 devices Max for Live** e **198 envelopes/lanes de automação** — tudo medido no XML do `.als`. O diagnóstico pista a pista e o plano de conserto do set auditado ficaram de fora deste acervo (estado específico de projeto); o que entra é o catálogo de padrões de defeito verificados, o que a prática externa recomenda e como provar cada conserto.

## 1. Padrões de defeito verificados (como detectar)

1. **Canal `Speaker/Manual = false` reativado por envelope `Mixer.Speaker = true`** — 8 canais no caso auditado. Ao carregar o `.als`, o Live segue a automação do arranjo e **liga o canal**, somando camadas escondidas (no caso: 6 linhas de baixo simultâneas no grupo de graves e um reverb de 11,76 s de cauda de atmosfera). Detectar: varrer lanes `Mixer.Speaker` contra o `Manual` de cada pista.
2. **Device renomeado com configuração diferente** — filtros batizados "HP 90Hz" que na verdade eram **Notch** em 740,8 Hz com ressonância 100% (2 canais), e "HP 180Hz" com cutoff real em 23,2 Hz e 50,6 Hz. Nunca confiar no nome do device — ler o parâmetro real.
3. **Cascata de filtros ressonantes** — até 3 Auto Filters + EQ em série num canal só, com ressonâncias de 73–89%.
4. **Auto Filter com Dry/Wet < 100%** — 9 canais com wet 35%: mistura 65% do sinal sem filtro (com rotação de fase IIR) ao sinal filtrado → *comb filtering* na banda média. Em filtro de correção, usar 100% wet.
5. **Saturadores fantasma** — `On = true`, `Drive = −36 dB`, `DryWet = 0%` (3 casos): consomem CPU sem produzir efeito.
6. **Ducker órfão de conceito** — sidechain apontando para uma pista individual quando o conceito era um grupo que não existe; em um canal, o ducker órfão tinha **substituído** o sidechain do kick (canal sem duck de kick).
7. **Plugin de synth carregado como efeito de áudio** — 12 instâncias ativas de Serum 2 FX (VST3/AU) como insert de áudio em pistas de áudio/samplers, aplicando distorção/multibanda/filtros de presets de synth no fim da cadeia (voz, uplifter, sub-roll etc.).
8. **Ponteira bank/program desalinhada e preset errado** — 4 canais de sopro/metais carregavam o mesmo preset de drone; 2 canais de sub carregavam um mid-bass FM falante em vez de subgrave; 2 canais colidiam na mesma ponteira bank/program com conteúdos diferentes.
9. **Envelope sobrescrevendo fader** — lanes de `Mixer.Volume` travando fader de kick em +1,6 dB o tempo todo, subindo grupos inteiros a +3/+4 dB, e forçando faders de −14 dB para −2,4 dB (+11,4 a +11,8 dB acima do manual). Com 37 pistas com envelope de volume preso ao `Mixer.Volume`, mexer no fader manual não tem efeito.
10. **Pontos fantasma e lanes inertes** — 2 lanes com último ponto no beat 9600 (compasso 2401, fora da música); 39 envelopes inertes (valor único), incluindo conflitos diretos onde a lane desliga o Reverb de uns canais (manual=true vs. env=false) e liga o de outro (5,96 s).
11. **Samples fora da pasta do projeto** — 18 pistas referenciando packs/referências externos (Simplers e AudioClips) → preciso de *Collect All and Save*.
12. **Boosts extremos de EQ e mono forçado** — boosts de +9 a +15,6 dB em 37–464 Hz em 5 canais fora de grupo; cascata de 4 crossovers de Bass Mono (canais 120–140 Hz, grupos 120–144 Hz, master 121 Hz); `Utility Mono=true`/`Width 0%` **depois** de delays/reverbs estéreo fechando a imagem do canal inteiro.
13. **Device Max for Live pós-limiter no master** — risco documentado de instabilidade/crash de JS e de processamento depois do teto; remover antes de qualquer render.
14. **Reverbs de insert > 3 s** (3,09–11,76 s) em canais que deveriam ser secos; caudas vazando nos cortes e conflitando com lanes de ligar/desligar.
15. **Automação pesada em device desligado** — 232 e 175 pontos de automação de cutoff em Auto Filters com `On = false` (inócua, mas máscara de estado e custo de arquivo).

## 2. O que a prática externa recomenda (fontes verificadas)

* **Ordem limpa de cadeia e economia de filtros IIR:** guias de produção/mixagem ([Mastering The Mix, 2025](https://www.masteringthemix.com/blogs/learn/how-to-use-mid-side-eq-to-elevate-your-masters); [iZotope, 2025](https://www.izotope.com/community/blog/what-is-midside-processing)) recomendam **um único EQ por canal** para passa-altas e escultura, evitando empilhar Auto Filters e EQs com cortes graves em série — cada filtro IIR adiciona rotação de fase e borra transientes.
* **Ganho de trim no `Utility` vs. automação no fader:** a boa prática em sessões grandes ([MixMaster Pro, 2025](https://www.mixmasterpro.io/articles/stereowidth); [Hyperbits, 2026](https://hyperbits.com/blog/sidechain-compression/)) é fazer **toda a automação de volume no `Gain` de um Utility no fim da cadeia**, deixando o fader do mixer livre para balanço manual. No set auditado, 37 pistas tinham envelopes presos ao `Mixer.Volume`.
* **Sidechain dedicado nos graves:** como destaca a [Hyperbits (Mar 2026)](https://hyperbits.com/blog/sidechain-compression/):
  > "Both your kick and your bass occupy the low end of your mix, and because they are both so huge, we don't want them playing at the same time... For sidechaining, we recommend using the classic compressor plugin and not the glue compressor."

  No set auditado, o grupo de graves não tinha nenhum compressor de sidechain e o ducker da pista principal de rolling 16ths estava desligado.

## 3. Como provar cada conserto (verificações)

| Verificação | Como |
|---|---|
| Canais escondidos desligados de verdade | Abrir o `.als` e confirmar que os canais com `Manual=false` permanecem mudos no play; densidade de picos deve cair |
| Master termina no limiter | Inspecionar XML/Live: nada de device Max depois do limiter |
| Headroom recuperado | Medir True Peak e gain reduction no Glue/Limiter antes/depois |
| Sub fundado | FFT pós-render na banda 20–40 Hz antes/depois |
| Transiente do kick limpo | Escuta A/B nos drops + medição de correlação na banda média |
| Sem picos ressonantes de EQ | Varredura espectral 150–200 Hz e 700–750 Hz |
| Caudas de reverb sob controle | Escutar o silêncio nos cortes secos (ex.: fim de seções) |
| Lanes limpas | Script de auditoria de lanes: nenhum evento além do fim musical (`max_time` dentro do arranjo), nenhum envelope com valor único |
| Samples dentro do projeto | Auditar `<SampleRef>` confirmando 100% dos caminhos em `Samples/` após Collect All and Save |

## 4. O que não deu para verificar no caso auditado

* **Existência física no disco dos 18 samples externos:** apenas o `.als` foi inspecionado — caminhos verificados no XML (`Path`, `RelativePath`, `OriginalFileSize > 0`), sem testar o SSD local.
* **Parâmetros internos pós-header binário do Serum 2:** os cabeçalhos JSON (`XferJson`) foram 100% decodificados (`presetName`, `presetAuthor`, `presetDescription`, `hash`), mas os knobs de DSP dentro do blob binário só são acessíveis com o engine do plugin carregado no host.
