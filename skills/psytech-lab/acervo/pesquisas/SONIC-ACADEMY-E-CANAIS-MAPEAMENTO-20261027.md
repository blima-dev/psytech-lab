# Sonic Academy e canais — mapeamento para o motor dos 2 minutos

**Data:** 27/10/2026 · **fontes:** 62 mapas de vídeo (um `.md` por vídeo, com ID de YouTube) · **régua declarada:** um comparativo espectral prévio contra 6 faixas de referência externas (26/10/2026).

**Natureza:** pesquisa. Nada foi aplicado em nenhum DAW nem em nenhum arquivo; nenhum áudio dos vídeos foi escutado como fonte musical — os 62 mapas são leitura de legenda automática, ASR local ou descrição, e isso está marcado caso a caso. Todo número de aplicação abaixo é **ponto de partida de design (`HIPÓTESE`/`INFERÊNCIA`)**; só vira afirmação de som depois de A/B.

**Como ler os rótulos:** `VERIFICADO` = está na legenda/descrição/arquivo citado; `INFERÊNCIA` = leitura para o arsenal do estilo; `HIPÓTESE` = valor de partida não testado; `NÃO VERIFICADO` = não foi possível confirmar.

**Termos do set de referência usados abaixo** (características do projeto de origem, não valores universais): pocket off-grid `.27/.77` (adiantamentos de ~0,27/0,77 do beat, ≈9,4 ms); SUB em C# (Operator) e BAIXO (Serum 2) como canais de grave; "MEIO/RUIDO/CHINELADA" = canais utilitários/de diagnóstico do set de referência.

---

## 0. A régua numérica (não re-medida nesta pesquisa)

Fonte: comparativo espectral de 26/10 contra 6 faixas de referência externas, seção "Frequências — dB relativos a 60–120 Hz".

| Banda | Média 6 refs | Set de referência | Diferença |
|---|---:|---:|---:|
| 20–60 Hz | +1,34 | +0,27 | −1,07 |
| 120–300 Hz | −5,36 | −5,89 | −0,53 |
| 300–1.200 Hz | −7,22 | −12,05 | **−4,83** |
| 1.200–4.000 Hz | −13,39 | −19,15 | **−5,76** |
| 5.000–12.000 Hz | −14,67 | −23,53 | −8,86 |

- Grave 30–120 Hz: side/mid **−59,52 dB**, correlação sub/bass **1,00** (mono, sem cancelamento relevante). Meio 400 Hz–2 kHz: side/mid **−21,90 dB** contra média **−3,52 dB** — o meio está baixo **e** muito fechado.
- O set de referência tem **mais agudo relativo que as faixas Demons e Limbo** (−24,79/−25,71 dB na mesma banda de 5–12 kHz). Subir shaker para perseguir a média contraria o alvo (mesmo relatório).
- Restrições do set de referência: SUB = Operator + Saturator, MIDI 25, ataque em **.27** de cada tempo, notas de **.68 beat** (.46 no quarto), release **27,1 ms**; BAIXO = Serum 2 + EQ Eight, notas 37/38/44/49/50, alternando **.50/.77**. Groove de referência aprovado: trecho 1:30–3:00 de "Shadows"; não aplicar grade reta por cima. Low-end mono é lei; 2:00 é o início do compasso 65 (bars 1–64 dentro dos dois minutos).
- Um aviso que vale para todo o dossiê: o EQ estático já foi testado. O bell de 300 Hz do BAIXO foi de −6 para −2,5 dB e rendeu **+0,38 dB** em 300–1.200 Hz ("alterações reais" do comparativo). O que os 62 vídeos oferecem, quando se sustentam, é **conteúdo e movimento**, não mais gain.
- **Tensão de régua, declarada e não resolvida:** a régua homologada do projeto fixa "Higiene de Médios: 400 Hz–2,5 kHz mantida em depressão suave relativo ao RMS", enquanto o comparativo mede **déficit** de 300–1.200 e 1.200–4.000 Hz contra 6 referências. As duas réguas não se contradizem automaticamente, mas não foram conciliadas em documento. Neste dossiê, "preencher" = adicionar conteúdo articulado e **medir o RMS do meio**; se o RMS subir acima do que a régua de depressão permite, a decisão é do produtor. Nenhuma aplicação abaixo autoriza boost estático no master.

---

## 1. Sumário executivo

1. **O buraco não se fecha com EQ nem com volume.** Os mapas que tratam do gap convergem para três rotas que atacam 300–4.000 Hz sem tocar no sub: cama/resposta **granular acima de 250 Hz**; **camada média do baixo com a fundamental em uma camada só**; e **duplicação +12 de resposta/madeira** com HP/LP.
2. **A rota de menor custo aparente e mais alinhada ao estilo é a duplicata +12** (ttYFldHqLWk): mesma frase, mesmos offsets, HP 200–250 Hz, LP 4–5 kHz, velocity abaixo do original. O vídeo diz **duas oitavas (+24)**; **+12 é downgrade conservador do mapa**, não do autor. Não cria ataque novo nem mexe no `.27/.77`.
3. **A rota mais direta no grave é separar fundamental e harmônicos** (kGfIx2d4oEI): Sub uma oitava abaixo carrega a fundamental; o saw tem o 1º harmônico cortado e, com o LFO abrindo o filtro, gera harmônicos de 2ª a 8ª ordem em **69–277 Hz** — não "300–1.200 Hz" por si. O corpo em 300–1.200 vem do LFO, do shelf de ~600 Hz e do transiente, não do fundamental do saw. **Nunca somar** as duas fundamentais.
4. **Pressão sem volume tem três mecanismos descritos nos vídeos:** kick+baixo como grupo com drive **band-limited 150 Hz–1,8 kHz** e clipper antes do limiter (I__tWZTk5-Q); rumble em **retorno** HP 120/LP 300–500, sidechainado e mono (xuHSPaCHjvo); rampas de **8 compassos** em poucos parâmetros (bOEc9c3pGi8).
5. **O que não muda:** SUB C# mono em `.27`, BAIXO em `.50/.77`, low-end mono abaixo de 120–150 Hz, shaker em −28 dB, canais utilitários mudos, sem kick 4/4 reto além de 32 compassos, nada depois de 2:00.
6. **Textura não é cama permanente.** Todos os mapas de textura que mediram o vício do projeto apontam o mesmo erro: preencher o tempo todo. As "3–4 camadas" do li-Oed1DWck são **camadas de uma única cama**, não três camas independentes; a cama precisa de buracos e automação por seção (QLPV1Wk5hoE, lHGfb5Hlmuc, sTizY7Qln78).
7. **Granular e rolling não têm canal no set atual.** O arquivo lido em 27/10 tem 16 MIDI + 2 returns, **nenhum canal granular e nenhum canal de rolling dedicado**; "rolling" é o BAIXO (Serum 2). Os canais de granulador citados por dois vídeos vêm de um estudo anterior e **não estão no arquivo atual** — a camada precisa nascer em canal novo ou reaproveitar madeira/percussão de madeira.
8. **P0 = 19 vídeos, P1 = 35, P2 = 8.** A ordem de A/B recomendada está no fim do §3.8: segurança/mono → fundamental do baixo → resposta/meio → textura → tensão/arranjo → transições → melodia, sempre 8–16 compassos por vez e em volume casado. **Nenhum A/B foi executado nesta pesquisa**; as receitas são hipóteses de design, não resultados.

---

## 2. Tabela de prioridade

Legenda de canal: **SA** = Sonic Academy · **AR** = Audioreakt · **SG** = SINEE Global · **VS** = Vision Serpent · **HTP** = Hypnotic Techno Production · **AV** = avulso.

**Nota de contagem:** o plano de pesquisa escrevia "P0 (16)" mas lista 19 IDs; a curva machine-readable também tem **19 P0**. Adota-se 19 — a contagem escrita do plano está errada; a lista e o JSON não.

### P0 — núcleo (19)

| ID | Canal | Frente | Técnica (uma linha) | Aplicação no motor 2min |
|---|---|---|---|---|
| JNAyJa_Dcx0 | SA | textura-atmosfera | Granular = sobrepor dezenas de grãos com pitch/posição/direção/volume próprios; o motor granular vira o oscilador de um synth subtrativo | Cama e resposta granular ≥180–250 Hz; nunca kick/sub/baixo; usar Serum 2 GranularOsc |
| li-Oed1DWck | SA | textura-atmosfera | 3–4 playheads deslocados, grão longo/densidade alta, pan/pitch/random por voz | 3 camadas na GUI ou 2–3 instâncias (o SCAN/playhead não está exposto no gerador): grão 80–200 ms, offset 30–50%, pan 35–50%, HP 250–300, sem −1 oitava |
| vREN7ACIcFc | SA | textura-atmosfera | Drone granular com pitch travado, reverse ~50/50, LFOs pequenos e HP antes do reverb | Drone 150–300 ms, random pitch 0, HP 120–150, LP 3–5 kHz, −18 a −24 dB |
| QLPV1Wk5hoE | SA | textura-atmosfera | Cama granular de fonte orgânica, até 8 vozes, loop fwd/back, usada como ferramenta de arranjo | Uma cama, corpo 1,2–4 kHz, HP 250–300 depois do granular, com silêncios e automação por seção |
| iWOPUHKbJjI | SA | groove | Síncope macro (3/16, tercinas) e LFO fora do beat, sem adicionar camada | Grade 3/16 só em madeira/resposta; LFO 1/8D/1/8T em via HP ≥300 do baixo; `.27/.77` intacto |
| bOEc9c3pGi8 | SA | pressao-grave | Curvas de 8/16/32 compassos em poucos parâmetros, unipolares e com reset | Rampa de 8 no low-cut paralelo do kick, no cutoff 300 Hz–1,2 kHz do rolling e no send da atmosfera; pontuar 9/17/25/33/41/49 |
| dSXz_MFS5ks | SA | meio-espaco | Reverb 100% wet somada em mono, posicionada como fonte contra o dry no centro | Retorno MONO ROOM: Hybrid 100% wet → HP 280–320/LP 4–5 kHz → Width 0 → pan oposto; só resposta/madeira |
| w1WsSkRLyrU | SA | pressao-grave | Mono na fonte ou low-cut só no Side, deixando o Mid intacto | Width 0 em kick/sub; EQ8 M/S com low-cut 120 Hz só no S no bus de bateria e no master |
| Mix6rW9AHgE | AR | pressao-grave | O grave sai do baixo psy; ele é reconstruído como articulação de médio | Camada psy em C#2/C#3, Env2 sustain 0, saturação/multibanda/EQ 1 kHz; HP 50–60 Hz em C#2 ou 100–120 Hz em C#3 (não 80–100, que come o C#2); não somar sub |
| xuHSPaCHjvo | AR | groove | Peso por rumble filtrado + baixo square médio, não por volume | Camada média Env2 0,08–0,12 s (a parte segura); rumble em retorno HP 120/LP 300–500 é **opcional** — o mapa lembra que rumble é base hard techno e o motor do set é rolling |
| ttYFldHqLWk | SG | meio-espaco | Preencher médio por arranjo: duplicata duas oitavas acima, camadas, saturação/OTT; EQ só para domar picos | Duplicar resposta/madeira **+12** (o vídeo diz **+24**; +12 é downgrade do mapa), HP 200–250/LP 4–5 kHz, velocity menor; +24 só se 1,2–4 kHz continuar vazio |
| I__tWZTk5-Q | SG | pressao-grave | Kick+baixo como grupo único com cadeia fixa e clipper antes do limiter | Bus kick+baixo: EQ → drive paralelo 150 Hz–1,8 kHz → EQ → Glue → clipper 1–3 dB → limiter; sem low extender |
| h39gdHGGo-c | SG | pressao-grave | Noise sem grave deslocado para baixo com Shifter e envelope espelhado ao kick | Eventos mono 60–200 Hz nos `.27/.77`, HP 45–60/LP 200–300, sem Echo no núcleo; só resposta, não cama |
| _W_mwJVDhqA | SG | pressao-grave | Rolling em 16º com o 1º 16º de cada tempo vazio, saw mono LP ~200 Hz, Env2 sustain 0 decay 1/16 | Decay **117 ms** a 128 BPM, preservar `.27/.77`, duck pelo kick; **não** copiar o corte de 300–4 kHz |
| iteUJHS5YNE | HTP | pressao-grave | Meta-análise: fonte vence processamento; kick curto + sine sequenciado e LFO em rates ímpares | Kick ≤130 ms, sub sine mono C#, LFO só como modulação (sem onsets novos), glue + compressor de retorno |
| NCY0r4q-QcM | HTP | pressao-grave | Tensão por subtração; o retorno do groove é a resolução | Kick fora 53–56 com duck do sub congelado, hats caem em 49, resolve em 57; sem delay no shaker/rolling |
| f4tdX3LsKj0 | HTP | textura-atmosfera | Granular percussivo em loop, disparado em 16avos, nos buracos como pergunta-resposta | Camada ≥250 Hz: grão 60–120 ms na resposta e 100–160 ms na madeira; 1 pergunta + 1 resposta a cada 2 compassos nos buracos `.27/.77` |
| CixBgwVAAYg | HTP | meio-espaco | Designar cada elemento ao campo mono/mid ou ao estéreo; largura só onde é decoração | Centro: kick/sub/rolling/hat principal; largura: ghost notes, resposta e atmosfera; auditar returns |
| kGfIx2d4oEI | AV | pressao-grave | Sub carrega a fundamental; saw sem 1º harmônico; LFO envelope no corte | Serum 2 em `.27/.77`, sub **substitui** (não soma), release curto; splitter 210 Hz e random phase 0 são ajuste de UI — **NÃO VERIFICADOS** no gerador |

### P1 — expansão (35)

| ID | Canal | Frente | Técnica | Aplicação no motor 2min |
|---|---|---|---|---|
| nS7CHBL-Bzs | SA | pressao-grave | Alinhamento de fase automático no SideKick | Sem SideKick: Utility `Ph` A/B + `Phase` do oscilador, sem mover tempo |
| R6xwYFH5SSY | SA | pressao-grave | Clipper corta pico e gera HF; soft clip para corpo, hard clip para transiente | Clip só no ramo de click/resposta, HP antes e LP depois; sub vai de limiter |
| yZ-q1H6KaME | SA | pressao-grave | 4 camadas de baixo com funções separadas; apagar notas que caem no kick | Sub mono, corpo sine+saw, dois saws no médio, acentos com reverb; HP na camada média |
| Kt22wEkGx-Y | SA | meio-espaco | OTT é upward compression e desfaz EQ anterior; entra cedo e em paralelo | Só resposta/madeira: Multiband Dynamics em paralelo, crossovers 300 Hz/4 kHz, Below só no meio, release ≥150 ms |
| ZSvJlc3LRqo | SA | textura-atmosfera | Warp Texture/Tones vira sustain; estiramento extremo, grain e clip envelope | Grain ~65, flux baixo, clip envelope de 16 compassos no grain size, HP 120–300 |
| ejNHFdtYrw0 | SA | groove | Micro-delays e randomização sutil de posição/velocity/pitch/round robin | Só hats/shaker/resposta/madeira: 1–8 ms, velocity ±10–15, pitch sutil; kick/sub/rolling fora |
| qvJqxGrAtCc | SA | transicoes | Grupo portátil de FX reequilibrado no destino | Grupo de FX de transição sem snare roll duplicado, só nos respiros 0:44–0:45 e 0:59,5–1:00 |
| OJ3Fxk4E0gU | SA | meio-espaco | Semicírculo de pan com +6 dB temporário para achar espaço | Pans pequenos e opostos: madeira 8–12 L, resposta 16–20 L, hats 4–8 R, stab 14–18 R |
| 4q6GrRSEfhI | SA | textura-atmosfera | Warp Texture grain 226, esticar, resamplear e empilhar cópias transpostas | Cama 300–1.200 Hz com HP 180–300/LP ~6 kHz, fora de kick/sub/baixo |
| nU3udPVlJGg | SA | textura-atmosfera | Drone 7(b5) sem a nota de baixo, HP, duck lento e dois panners | Oitava 4 (C#4–B4), HP 280–320, sidechain 2–4 dB do kick, sem sub |
| 90VpsmIaPuk | AR | textura-atmosfera | Operator parallel em ratios inteiros, macros escalonadas e feedback ~50% | Cama C# em 1×/2×/3×/4×, HP (160 Hz no parecer de FX; 90 Hz na trilha 33 — divergência a decidir), largura só acima do corte |
| S0DRqIEXW_4 | AR | motor-completo | Template peak time 100% stock: kick com transiente, baixo em 3 camadas, 4 hats, stab FM | Transiente ~1 kHz, mono <130; um dono de sub; mid do baixo 200–800; stab 400–900; sem Shimmer |
| TdNE8oEb2Lk | AR | arranjo-mix | Camadas com automação de filtro/volume/sends, sidechain e master mono <120 | Build 49–57 com low-cut no kick, filtro, riser, stop e reverse; Drop em 57 com rolling −10→0 dB |
| v-mjY-Vlgv0 | AR | textura-atmosfera | Wavetable mono POS 100, filtro MS-20 pluck, chorus/flanger/Echo/Shimmer | Stab-resposta em C# frígio, 2–3 eventos/compasso nos `.27/.77`, shimmer só em retorno filtrado |
| C3x8o9Krfc0 | AR | groove | Stab band-pass OSR com drive e Env2 curto | Centro do band pass em 250–400 Hz, res ~50, Env2 25, release 600 ms, Bass Mono 120 |
| lHGfb5Hlmuc | SG | textura-atmosfera | Duas camadas, noise + drone, LFOs de rates diferentes | Bus HP 280–300/LP 4–5 kHz; LFOs ~0,045/0,071 Hz; entrar em 17 e subir até 57 |
| sTizY7Qln78 | SG | textura-atmosfera | Atmosfera só no retorno, alimentada por pulsos de send; LFO lento + reverb 100% + AutoPan | Throw nas respostas/fim de seção; sem enviar kick/sub/baixo; cauda em 1,2–4 kHz |
| oO2gdXg1-nE | SG | melodia | Três ganchos por repetição + microvariação: granular gated, FM 2-op, 5 pads | FM como stab curto e os 5 pads na resposta, HP 180–300, sem swing extra |
| VqPpTk3gp78 | SG | melodia | 2ª menor, 7ª maior e trítono como tensão; podar 2ªs empilhadas | Célula C#–D e trítono D–G# como acentos, C# repetido como centro, tudo acima de ~200 Hz |
| A6XjjwGUkA8 | SG | groove | Frações mínimas de ruído viram hat/resposta; Corpus tube devolve corpo | HP ≥1 kHz, pico ressonante 700–900 Hz, LFO no attack só na resposta; **substituir** eventos |
| G4Tsj5or6A8 | SG | groove | Kick em 3 camadas, ghost/rumble, hats por velocity/swing/LFO | Kick 3 camadas, ghost filtrado, resposta em `.27/.77`, hats com velocity+swing; saturação em vez de agudo |
| xZW3lTHRCxs | SG | pressao-grave | Cinco passos de encaixe do kick: tuning, cauda, EQ antes da distorção, Roar multibanda, compressão | Confirmar G#0 52,41 Hz e cauda ~0,5 s; Roar low clean + tube no mid do rolling; sem click de filtro |
| GyhA92cfQgE | VS | motor-completo | Sine segura a fundamental, saw sem fundamental dá harmônicos; fase fixa no sub | Testar no BAIXO em A/B de 8–16 compassos; sub intocado; hat-transiente no kick só se 8k+ subir sem 2–4k |
| TwZk8Gcyl1E | VS | motor-completo | Low end em 4 camadas; kick afinado; fase testada; sidechain só nos graves | SUB como camada low e BAIXO como high; cortar graves do BAIXO; duck só <150 Hz |
| Wmr4dnvhVkc | VS | textura-atmosfera | Saw + camada de caráter, dois filtros em série, Env2 plucky, sync no filtro | Molde para madeira/stab em 300–1.200 Hz; guardar sync + abertura para as subidas |
| Fx3jM4xdw4M | VS | motor-completo | Kick mono + EQ + transiente; baixo saw FM leve, mono, duck 20–200 Hz | Cadeia do kick, patch de baixo Serum 2 e bus GRAVES com Bass Mono 178 Hz; presença no baixo em 300–1,2 kHz |
| 5XUULOEJ2tI | HTP | arranjo-mix | Curva de energia em degraus por camadas; base constante | 4 cenas de 16 compassos: hats/echo/16tos sobem a energia; kick/sub/baixo constantes; reset em 1:45 |
| VSYCY__WVQ8 | HTP | groove | Hipnose por troca/omissão de UM elemento por fronteira de 8; 6–8 FX curtos | Portas em c33/c41/c49: sair com open hat, voltar trocado, acento em `.27/.77`; falso release c33–c40 |
| Dcs7r1b6RwI | HTP | pressao-grave | Três basslines stock: saw transient no sine, LFO→wavetable, pitch envelope em loop | Sub mono; BAIXO-MID com LFO→WT e HPF; loop de 3 tempos só na resposta/madeira |
| Hzszjbt_c9I | HTP | textura-atmosfera | Pad dark com dois osciladores a +6 st, ataque longo, LFOs e shimmer | Cama 1–56, HP 180–220/LP 5–6 kHz; recuar/duckar no Drop 1 |
| BjDkkB8ElnY | HTP | textura-atmosfera | Dobra do baixo com grave cortado + saturação e LFO; cama de field/vinil; splashes | Dobra em bar 17 com HP 250/LP 5–6 kHz, sem gate; resposta 1 a cada 2 compassos |
| cVtnGIFGYss | HTP | groove | Groove Pool: swing de 8ª/16ª, timing e velocity separados, Random pequeno | Só hats/shaker/resposta, Amount 10–20%, printar 2–3 variações; kick/sub/rolling fora |
| NXWjMYYYHGw | HTP | pressao-grave | Operator parallel + detune + Shifter ring + LFO → lead/sino inarmônico | Usar como resposta/stab de meio (HP 200–300), loop 5/16 ou 7/16; não é técnica de grave |
| ORj8Vgu2vNs | AV | motor-completo | Repetição em camadas (1/4 + 8/16/32/64); célula de 1 beat; colocação de sample | Célula de 1 beat com `.27/.77` intacto; intro filtrada em 17; side cut ~300 só em atmos/hats |
| n2rdb-8fQ9c | AV | motor-completo | Kick curto/afinado, sub + camada estéreo HPF, LFO envelope, Q&A de dois patches | HPF antes/depois do drive no SUB/BAIXO, pluck por LFO, sidechain por colisão, resposta call/response |

### P2 — banco de ideias (8)

| ID | Canal | Frente | Técnica | Aplicação no motor 2min |
|---|---|---|---|---|
| 44m_K42KtX8 | SA | transicoes | Sweep de ruído com EQ ressonante automatizado; riser tonal de 2→24 st em 8 compassos | Riser 1:30–1:45 terminando seco em 57; sweep de 1 compasso em 0:30 e 1:00; HP ≥120 |
| rSorLiUr6xI | SA | melodia | Ritmo antes das notas; pergunta-resposta; rests como parte da frase | Lead C#4–C#5, 3–4 acentos do shaker, 2 compassos sobe/2 desce/1 cala; sem sub nem detune |
| 4TOQ-5mGpUY | SA | textura-atmosfera | Resample → sample osc → loop curto → LFO no loop start/end (granular falso) | Conceito já resolvido pelo GranularOsc; usar só como cauda/atmosfera, +1 oitava antes do scan |
| IbeXMrvWAew | AR | pressao-grave | Kick 909 com LP24 ressonante aberto por envelope, duas saturações fora do rack, reverb curto paralelo | Só no kick existente: LP24 varrendo 380–550 Hz, res 40–55, duas saturações, reverb curto com HPF |
| DeRUOw8T98Y | SG | arranjo-mix | Pré-mixar, mapear stems em faders com teto = premix e gravar o arranjo em um take | 8 faders + 2 sends + 3 botões via Utility Output; gravar bars 1–64; só ganho/filtro/send |
| ed5ODapIIBc | VS | motor-completo | Camadas por banda com cadeias paralelas: topo do kick, reverb mid-only, sub, rolling, sample 70–240 | Ghost kick só de médio (300 Hz–2 kHz) como resposta; reverb só no médio; sem camada nova de sub |
| 6x1_XZDcI8I | HTP | arranjo-mix | Arranjar trocando fonte/sequência sobre a mesma grade; contraste do drop por subtração do agudo | Fade de 1–2 compassos na entrada; mutar topo/hats 1–2 compassos antes do drop; sem camada nova |
| aK2tKYe8yCI | HTP | groove | Camadas curtas afinadas em Q&A, ghost notes, 5 semicolcheias, LFO/scan e automação | Ghost notes e 5/16 no hat fechado; resposta/madeira em C#; rolling de uma nota por pitch envelope |

---

## 3. Receitas por frente

> **Regra comum a todas as frentes:** nenhuma receita abaixo escreve abaixo de 120–150 Hz, mexe em `.27/.77`, sobe o shaker ou religa os canais utilitários do set. "Preservar" é parte da receita, não aviso de rodapé.

### 3.1 pressao-grave (16 vídeos)

**O que os mapas sustentam.** O grave do set de referência já tem pressão: `sub−kick` dentro do envelope e correlação 1,00 (estudo de 17/10). O que falta é **corpo harmônico no meio** e **encaixe**, não mais sub. As receitas úteis são as que separam a fundamental dos harmônicos, ou que criam pressão por camada filtrada.

| ID | Receita concreta | Onde / valor de partida |
|---|---|---|
| kGfIx2d4oEI | Serum 2 com **Sub uma oitava abaixo** + saw com 1º harmônico removido (`custom_harmonics` índice 0 = 0); LFO1 em modo envelope no cutoff; release do Env 1 curto | Tocar nas subdivisões `.27/.77`; o saw filtrado fica quase inaudível sozinho — é o LFO que o traz. Sub **substitui** o existente, nunca soma. Splitter 210 Hz, Hyper Dimension e random phase 0: **NÃO VERIFICADOS** no gerador; ajustar na UI |
| _W_mwJVDhqA | Wavetable/Serum 2 mono, saw, LP ~200 Hz, Env2 +55% sustain 0, **decay 117 ms** (=1/16 a 128 BPM), release 10 ms; Saturator ~40%; compressor paralelo; Auto Filter; duck pelo kick | Preservar `.27/.77`; **não** cortar 300–4 kHz (já −4,83/−5,76 no set); cortar só acima de 6–8 kHz se necessário |
| Mix6rW9AHgE | Uma camada de articulação psy em C#2/C#3 com Env2 sustain 0; cadeia saw → LPF → Saturator → Multibanda (só médios) → EQ 1 kHz → soft clip → reverb curto | **Decidir a nota antes do HP:** em C#2 (69,3 Hz), HP **50–60 Hz** remove o C#1 (34,65) e preserva o fundamental; HP 80–100 comeria o C#2. Em C#3 (138,6), HP 100–120. Não somar o "add a bit of sub"; máximo **dois** estágios de cor |
| I__tWZTk5-Q | Grupo KICK+BAIXO: EQ8 corretivo → **drive paralelo HP 150 Hz/LP 1,8 kHz** (20–35% wet) → EQ8 pós-drive → Glue 1–2 dB → clipper 1–3 dB → limiter | Hats, resposta, madeira, stab, subida e atmosfera **fora** do bus; **não** usar Bass Low Extender; medir 55–75 Hz antes/depois |
| iteUJHS5YNE | Kick curto (≤117–130 ms de corpo), afinado em C#; sub sine mono em C#1/C#2, fora do beat 1; LFO só como modulação de amplitude/posição; glue de ataque longo/release curto + compressor de pico no retorno | O LFO **não** pode criar onsets novos; sem reverb no sub; "pouco processamento" é a tese do vídeo |
| bOEc9c3pGi8 | Rampas de **8 compassos**: low-cut de um ramo paralelo do kick (150–300 Hz); cutoff do rolling **300 Hz–1,2 kHz**; send da atmosfera subindo em 16–32 compassos | Pontuar a cada 8 nos pontos 9/17/25/33/41/49; não descer o cutoff abaixo de 250 Hz; não modular o fundamental do sub. O **±1–2 dB é adaptação [I]**, não valor demonstrado; o Shepard/Falcon/ANA 2 do vídeo fica fora (§4) |
| NCY0r4q-QcM | Kick fora em **53–56** (rampa de 1/16, não mute seco); congelar o duck do sub nesse trecho; hats caem em 49–52; nota sustentada na 5ª/6ª resolve em C# no 57 | Nada de delay no shaker/rolling; nada de ganho de compensação no retorno do kick; o vazio é o efeito |
| h39gdHGGo-c | Noise loop sem grave → **Shifter para baixo** → HP 45–60/LP 200–300 → envelope espelhado ao kick → sidechain; eventos curtos, mono | Só nos `.27/.77`, não em cama; **fora** do canal de sub; sem Echo no núcleo seco; não usar ring mod |
| xuHSPaCHjvo | **Parte segura:** camada média de baixo (Env2 0,08–0,12 s, valor do estudo interno, não do vídeo). **Opcional:** rumble em retorno: send do kick → Hybrid Reverb 100% wet (decay 150–300 ms) → HP 120 → LP 300–500 Q≤1,2 → Compressor sidechain → −18/−24 dB | Retorno mono <150 Hz; delay 3/16 feedback 50% **não** entra (cai 9,4 ms antes do BAIXO). **Cautela de gênero:** o próprio mapa cita que rumble é base de hard techno e o motor do set é rolling; se o A/B fizer o motor soar tech house, descartar o rumble e manter só a camada média |
| Dcs7r1b6RwI | SUB: Operator sine + segunda oscilação saw com sustain 0/decay curtíssimo; harmônicos só 2ª–4ª; drive 140–250 Hz com compensação. BAIXO-MID: LFO→WT Pos e Env2→cutoff | SUB e camada média separados; Echo/reverb só no médio; loop de 3 tempos só na resposta/madeira |
| xZW3lTHRCxs | No kick: EQ subtrativo **antes** da distorção; Roar com low "soft and clean"; compressor 4:1/attack 100 ms/release mínimo | Confirmar G#0 52,41 Hz e cauda ~0,5 s; **tube só no mid**; evitar click de filtro e boost 55–75 Hz; a novidade é usar o mesmo Roar no **mid do rolling** |
| yZ-q1H6KaME | Quatro camadas: SUB sine mono sem saturação; corpo sine+saw; dois saws no médio com LP 2,5–3,5 kHz; acentos esparsos com reverb | Width 0 no sub; HP ~100–120 na camada principal; apagar da camada as notas cujo onset coincide com o kick |
| IbeXMrvWAew | Só no kick existente: LP24 com envelope rápido varrendo **380–550 Hz**, ressonância 40–55%; duas saturações **fora** do instrumento; reverb curtíssimo em paralelo com HPF | Sem camada de rumble nova; ressonância larga (Q baixo) para não brigar com o formante da madeira; pico em 485 Hz ≈ B4, não briga com C# |
| nS7CHBL-Bzs | Protocolo: kick sozinho → kick+sub com Utility `Ph` e depois `Phase` do oscilador em passos de 45–90° → kick+sub+baixo por nota | Sem SideKick: não há detecção automática; **não mover tempo**; nivelar para baixo se o alinhamento aumentar o grave; nos trechos sem kick não há fase a resolver |
| NXWjMYYYHGw | Operator parallel com osciladores na mesma nota e detune curto; Shifter em ring mod baixo; LFO no filtro; loops 5/16 ou 7/16 | É **resposta/stab de meio**, não grave: HP 200–300; decay curto; ring mod baixo para não virar sino |

**Preservar nesta frente**
- SUB em C#, mono, `.27`, durações `.68/.46`, release 27,1 ms — não trocar a fonte nem alongar para "sustentar".
- BAIXO alternando `.50/.77`, com D no quarto tempo; nada de quantizar para 16º reto.
- Um único dono da fundamental. Toda receita que adiciona sub (kGf, yZ, Mix6, TwZk8Gcyl1E) só entra **substituindo** uma camada existente.
- 55–75 Hz não pode subir: já está +4,0 dB acima de 40–55 Hz contra −1,2…+1,4 dB das referências (estudo de 17/10).

### 3.2 meio-espaco (5 vídeos)

**O que os mapas sustentam.** Quatro dessas técnicas **desmascaram** o meio e devolvem clareza ao centro; elas não sobem a banda sozinhas. A quinta (ttYFldHqLWk) é a exceção: **adiciona conteúdo** e pode subir 300–1.200/1.200–4.000. O erro a evitar é tratar pan/largura como correção de déficit espectral.

| ID | Receita concreta | Onde / valor de partida |
|---|---|---|
| dSXz_MFS5ks | Retorno **MONO ROOM**: Hybrid Reverb 100% wet → EQ8 HP 280–320/LP 4–5 kHz → Utility Width 0% → pan oposto ao dry | Melhor candidato: percussão de resposta (send −12/−18 dB); madeira (send médio); kick/sub/rolling **zero** |
| CixBgwVAAYg | Designar campo: kick/sub/rolling/hat principal em **Width 0%**; ghost notes e resposta com pan L/R; atmosfera larga | A largura vem de ghost notes e camadas de HF, não de widener no bus; auditar returns que recebem kick |
| OJ3Fxk4E0gU | Varredura de pan com Utility +6 dB temporário, ouvindo a música inteira, até achar espaço próprio; devolver o gain a 0 | Madeira 8–12 L; resposta 16–20 L; hats 4–8 R; stab 14–18 R; **pan estático, sem Haas** |
| w1WsSkRLyrU | Mono na fonte (kick/sub) + EQ8 em M/S com low-cut **só no Side a 120 Hz** no bus de bateria e no master | Auditar subindo até 150 Hz; se soar diferente, voltar; **não** cortar o Mid nem usar 200 Hz como meta |
| ttYFldHqLWk | Preencher por conteúdo: duplicar a resposta/madeira com **+24** (o vídeo diz "two octaves higher"); o mapa propõe **+12 primeiro** como downgrade para não invadir 1,2–4 kHz. HP 200–250/LP 4–5 kHz, velocity abaixo; EQ só para domar picos | Hats protegidos; nada de boost estático no master; OTT só na camada de médio e em mix baixo; o vídeo resolve densidade, **não** a largura do meio (side/mid −21,90). **+12 é decisão do mapa, não do autor do vídeo** |

**Preservar nesta frente**
- Nada abaixo de 120 Hz sai do centro; correlação ≥0,98 abaixo de 120 Hz continua gate.
- Pan estático não muda ataque: `.27/.77` ficam intactos por construção. Widener/chorus/Haas no bus é caminho de brilho metálico.
- O meio 400 Hz–2 kHz está **muito fechado** (−21,90 dB side/mid). Pan não abre conteúdo lateral; abrir L/R só acima de ~150–250 Hz, e com fonte real, não com Utility Width.

### 3.3 textura-atmosfera (16 vídeos)

**O que os mapas sustentam.** Granular e drone são as rotas mais diretas ao vale de 300–4.000 Hz **desde que** entrem high-passed, com pitch estável, densidade não percussiva e buracos. A fonte escura (madeira, voz, foley, guitarra) vence fonte brilhante. Textura não substitui o motor.

| ID | Receita concreta | Onde / valor de partida |
|---|---|---|
| JNAyJa_Dcx0 | Fundamento: grão = fatia curta com pitch/velocidade/direção/volume próprios; sobrepor dezenas/centenas; passar por filtro/envelope/LFO | Cama/resposta ≥180–250 Hz; nunca kick/sub/baixo; o granular pode ser o oscilador, não o motor rítmico |
| li-Oed1DWck | **Uma** cama com 3 camadas (não três camas): A corpo (grão 120–200 ms, density 12–18, offset 15–30%, pan centro); B/C (80–150 ms, offset 30–50%, pan 35–50%); D +1 oitava (60–100 ms, HP 400–500). O offset por playhead exige **GUI ou 2–3 instâncias** — o gerador não escreve o SCAN | HP 250–300 em todas; LP 7–9 kHz; random pitch ≤0,5 st; **sem** camada −1 oitava; sem LFO tempo-sync. Arranjo: 1–16 só A; 17–32 entra B; 33–48 entra C; 49–56 entra D e abre o reverb; buracos e automação por seção |
| vREN7ACIcFc | Drone granular: fonte afinada em C#, grão 150–300 ms, density alta, `random_pitch = 0`; duas camadas normal + reverse (~50/50); LFO lento no LP | HP 120–150 antes do reverb; LP 3–5 kHz; −18/−24 dB; nada de gate/retrigger em 1/16 |
| QLPV1Wk5hoE | Uma cama granular de fonte orgânica; até 8 vozes com entradas/spreads diferentes; automação de filtro por seção | Corpo em **1,2–4 kHz** (primário) e 300–800 secundário; HP 250–300 **depois** do granular; silêncios, não colchão |
| f4tdX3LsKj0 | Granular percussivo num **canal percussivo de madeira (sampler)** ou no canal de madeira (sintetizador): printar 1–2 compassos, loop on, grão **60–120 ms na resposta** e **100–160 ms na madeira**, offset 20–40%, pitch ±1–2, pan ±20%, max grains 8–16; 16avos com gate curto | **1 pergunta + 1 resposta a cada 2 compassos**, só nos buracos `.27/.77`; um hit por buraco, **sem sobrepor as duas camadas** (o mapa não manda substituir evento; a regra de densidade é do projeto, §3.4). HP ~276; nível 3–6 dB abaixo dos hats; 2–3 samples |
| 4q6GrRSEfhI | Uma nota longa de madeira/guitarra → warp Texture, flux 0, grain 226, esticar ao máximo, resamplear; empilhar cópias −5/−8 st e lavar com delay/reverb | Cama 300–1.200 Hz; HP 180–300/LP ~6 kHz; reafinar as cópias ao C#; dry na frente se precisar soar madeira |
| ZSvJlc3LRqo | Warp **Texture/Tones** em sample de 1–4 s com sustain; estirar 2–4×; grain ~65, flux baixo; clip envelope de 16 compassos no grain size | HP 120–300; L/R só acima de 150–250 Hz; **não** usar o gate 1/8 do vídeo em quem carrega `.27/.77`; preservar os vazios de 0:44–0:45 e 0:59,5–1:00 |
| 4TOQ-5mGpUY | Resample de uma nota → SampleOsc → loop curto → LFO lento no loop start/end (granular falso); subir +1 oitava antes do scan | Conceito **já resolvido** pelo GranularOsc; se usar, só cauda/atmosfera, grão longo, HP 180–250; nunca em kick/sub/baixo |
| nU3udPVlJGg | Drone 7(b5) sem a nota de baixo; fonte madeira/loop orgânico; HP; sidechain 2–4 dB do kick; dois AutoPan em rates diferentes | Oitava 4 (C#4–B4); HP 280–320; Bass Mono; LP 5,5–6 kHz; sem Sub osc; −12 a −18 dB sob o elemento principal |
| 90VpsmIaPuk | Operator parallel, 3–4 osciladores em ratios 1×/2×/3×/4× sobre C#; macros de shape/detune/volume; feedback ~50% com LFO lento; filtro + delay/reverb em send | Largura só acima do HP; detune pequeno (3–8, não 26/34); notch 320 Hz/1,2 kHz se colidir com madeira; decidir a divergência 90 vs 160 Hz |
| v-mjY-Vlgv0 | Wavetable mono POS 100, filtro MS-20 com Env2 (A0, D~200 ms, amount ~68), chorus Classic, flanger lento, Echo HP 1,5/LP 11 kHz, Shimmer em retorno | Stab-resposta em C# frígio, 2–3 eventos/compasso nos `.27/.77`; HP 200–250; BassMono no retorno; +6 do vídeo trocar por +7 (G#) ou +1 (D) |
| lHGfb5Hlmuc | **Um** bus com **duas** camadas: NOISE (HP 300/LP 4,5 kHz) e DRONE (madeira granular em C#/D/G#), LFOs ~0,045 e 0,071 Hz; reverb/delay no retorno | Entrar em 17 (só noise) e 25 (drone); 49–57 desligar LFO e subir o noise por volume; depois de 57 manter só o drone baixo; EQ em 300–1.200 |
| sTizY7Qln78 | Atmosfera só no **retorno**: LFO muito lento + reverb 100% wet de decay longo + Drum Buss/Overdrive leve + duas AutoPan (uma polimétrica); send em pulsos | Throw nas respostas e no fim de seção; não enviar kick/sub/baixo; HPF do bus de atmosfera ≤40 Hz; a cauda substitui o corte seco (vício de 1,33 gaps/min medido no set) |
| Hzszjbt_c9I | Pad dark: dois osciladores a **+6 st (trítono)**, ataque longo, LFO2→pitch, LFO1→filtro, FM/warp e unison; echo de feedback longo + reverb longo | Cama bars 1–56; HP 180–220/LP 5–6 kHz; trítono só acima do grave; recuar/duckar em 57 |
| BjDkkB8ElnY | Duplicar o clip do baixo com HP ~250/LP 5–6 kHz, saturação leve e LFO lento (a dobra herda `.27/.77`); cama de field recording/vinil; splashes de 1/16 em Q&A | Nível bem abaixo do original; sem gate/sidechain na cópia; splash só substituindo evento; pre-delay 20–40 ms nos retornos |
| Wmr4dnvhVkc | Saw rica + camada de caráter, Filter 1→Filter 2 em série, Env 2 plucky, macro no decay; sync + abertura de filtro | Molde para madeira/stab em 300–1.200 Hz; sem LPF ressonante de trance; sync só nas subidas; nada de pan no que toca o grave |

**Preservar nesta frente**
- HP obrigatório em toda camada (120–300 Hz conforme a fonte), **antes** do reverb; retorno também com HP.
- `random_pitch` ≤0,5–2 st e `random_pitch = 0` em drone; a variação vem de posição/offset, não de afinação.
- Nada de LFO tempo-sync, gate 1/16 ou retrigger na camada que carrega o groove; os vazios de 0:44–0:45, 0:59,5–1:00, 1:29,5, 1:44,1–1:45 e 1:59,5 continuam vazios.
- Uma cama com camadas, não três camas independentes; a textura precisa de buracos e automação por seção.

### 3.4 groove (9 vídeos)

**O que os mapas sustentam.** A hipnose vem de **troca, omissão, microtiming e modulação**, não de mais eventos. A densidade de transientes já está em 7,57 picos/s contra teto interno de 6,99 (estudo de 17/10). Portanto: toda receita aqui **substitui** eventos ou varia timbre; nada soma camada contínua.

| ID | Receita concreta | Onde / valor de partida |
|---|---|---|
| iWOPUHKbJjI | Grade macro só nas respostas: madeira/percussão em 3/16 ou tercina; LFO 1/8D/1/8T no filtro de uma via **paralela HP ≥300** do baixo; polimetria 7/16 ou 13/16 no shaker | Não mover kick, não sincopar o SUB; shaker sem subir nível; testar em 8 compassos |
| xuHSPaCHjvo | Camada média de baixo com Env2 0,08–0,12 s; rumble filtrado em retorno só como opção | Ver §3.1; o "heavy" vem do mid, não do sub; rumble é base hard techno no próprio mapa — descartar se virar tech house |
| ejNHFdtYrw0 | Micro-delay de claps (+15/−10 ms), random position 1–8 ms, velocity ±10–15, pitch sutil, round robin de 3; fatiar loop de madeira no Simpler | Só hats/shaker/resposta/madeira; kick/sub/rolling intactos; uma direção por bloco (nunca atrasado e adiantado juntos) |
| C3x8o9Krfc0 | Stab band-pass OSR, drive 5–6 dB, centro **250–400 Hz**, res ~50, Env2 amount 25, amp sem sustain, release 600 ms; Bass Mono 120; LP para domar | No riff 3/16; se o centro ficar em 100 Hz vira baixo, não resposta; sem high shelf amplo |
| A6XjjwGUkA8 | One-shots de ruído: clique do início = hat fechado; Corpus tube ~800 Hz para corpo; LFO no attack/decay só na resposta; HP ≥1 kHz, LP 7–8 kHz | **Substituir** um evento existente; pico ressonante 700–900 Hz, não 2–4 kHz; ataque idêntico onde há `.27/.77` |
| G4Tsj5or6A8 | Kick em 3 camadas (transiente/corpo/cauda), ghost kick encurtado, rumble filtrado; hats com velocity+swing+LFO lento em volume/pan; saturação em vez de agudo | Bump na fundamental de C#, não em 55 Hz; corte de low-mid; bus com tone escurecido e level match |
| VSYCY__WVQ8 | Portas de 8: sair com open hat em c33; voltar **trocado** em c41; acento de open hat em `.27/.77` em c49; falso release c33–c40; 4–6 eventos de transição band-limited 300 Hz–6 kHz | Não copiar 16avos contínuos; não subir shaker; o release real fica em 57 |
| cVtnGIFGYss | Groove Pool: swing de 16ª, Amount 10–20%, Random pequeno, timing e velocity separados; printar 2–3 variações | Só hats/shaker/resposta; kick/sub/rolling fora; nada de EQ/saturação "para combinar" |
| aK2tKYe8yCI | Ghost notes, hat em 5 semicolcheias com curva de dinâmica, Q&A entre samples, madeira em loops de 2–4 compassos, Shifter/notch lento | Resposta afinada em C#, nos buracos; hat não preenche 1,2–4 kHz (isso é madeira/shaker com corpo); sem stab/subida (não cobertos) |

**Preservar nesta frente**
- O pocket `.27/.77` é microtiming (+0,02 beat ≈ 9,4 ms), não grade macro. Nada de swing extra de 15% por cima (o projeto já corrigiu flam).
- Kick 4x4 com os vácuos já escritos; sem ghost kick novo que crie colisão com SUB `.27` e BAIXO `.50/.77`.
- Teto de densidade: trocar, não somar.

### 3.5 transicoes (2 vídeos)

**O que os mapas sustentam.** O projeto tem **excesso de corte seco** (1,33 gaps/min contra máximo 0,80 da família) e não falta reverb. A tradução é substituir o corte por cauda/transformação, com **um dono por fronteira**.

| ID | Receita concreta | Onde / valor de partida |
|---|---|---|
| qvJqxGrAtCc | Grupo de **FX de transição** com crash, reverse-crash, noise-up, noise-down; dois clipes-âncora em 0:44 e 0:59,5; HP em cada pista; sidechain do crash só no noise do grupo | Terminar no downbeat de 0:45 e 1:00; sem snare roll duplicado; reequilibrar no destino (−4 dB → 0 é exemplo, não meta); um evento por respiro |
| 44m_K42KtX8 | Riser tonal: fonte em C# → pitch 2→24 st em **8 compassos**; unison crescendo; LP; reverb **100→0** exponencial; terminar seco. Sweep: noise + banda de EQ ressonante automatizada de baixo para cima | Riser de **1:30 (49) a 1:45 (57)**, aterrissando no Drop 1; sweep de 1 compasso em 0:30 e 1:00; HP ≥120, pink/brown, LP ~8 kHz, Q moderado |

**Preservar nesta frente**
- Nada de sub no FX de transição; retorno com HP 200–300.
- Não repetir o salto agudo do compasso 32, já rejeitado no plano do motor.
- Um dono por fronteira: se já existe reverse/riser, **substituir**, não somar.

### 3.6 melodia (3 vídeos)

**O que os mapas sustentam.** A melodia do estilo é sóbria e curta. O que falta não é nota: é **ritmo, silêncio e uma dissonância por frase**. As três receitas cabem sem tocar no grave.

| ID | Receita concreta | Onde / valor de partida |
|---|---|---|
| rSorLiUr6xI | Ritmo antes da nota: 3–4 acentos por compasso tirados do shaker; 2 compassos de pergunta ascendente, 2 de resposta descendente, 1 de silêncio em que a resposta percussiva fala | Lead em **C#4–C#5** (277–554 Hz), HP 180–220; unison 1, detune 0; sem camada de sub; sem FM/comb/ressonância alta |
| oO2gdXg1-nE | Três ganchos: granular gated + EQ desenhado; FM 2-op com LFO minúsculo; 5 pads do mesmo sample com ataque/pitch diferentes | FM como **stab curto**; pads na resposta; HP 180–300; não copiar swing 15%; não cortar 700 Hz–1 kHz largo |
| VqPpTk3gp78 | Célula C#–D (2ª menor), G#–A (2ª menor), trítono D–G#; usar **uma** dissonância por frase; acento agudo G#–A em 49–56 e retirar uma nota em 57 | Tudo acima de ~200 Hz; +6 só em D/G#; +13 só em C#/G#; nada de sino/prato/exciter; não mover posição/duração/velocity |

**Preservar nesta frente**
- C# como centro; frígio estrito C#–D–E–F#–G#–A–B; notas fora liberadas **em teste**, não como nova tonalidade.
- Nada abaixo de 200 Hz na camada melódica; sem camada de sub no patch.
- A conversa é sobreposição, não espera: a resposta atrasada é minoria nas referências (estudo de arranjo/FX de 25/10, §3).

### 3.7 arranjo-mix (4 vídeos)

**O que os mapas sustentam.** O segundo minuto precisa de **história**, não de mais camadas. As receitas são de curva, troca e performance; nenhuma corrige espectro.

| ID | Receita concreta | Onde / valor de partida |
|---|---|---|
| 5XUULOEJ2tI | Quatro cenas de 16 compassos: A=L1, B=L2, C=L3, D=L4→L1. Hats escuros com echo/16tos/open-hat sobem a energia; kick/sub/baixo **constantes**; reset em 1:45 | 0:00–0:30 base; 0:30–1:00 hat "t-t"+echo; 1:00–1:30 16 hats; 1:30–2:00 pico e reset; LPF 10–12 kHz nos hats |
| TdNE8oEb2Lk | Build 1:30–1:45: reintroduzir o kick com low-cut, abrir filtro, riser, parar tudo, deixar o lead sozinho e um silêncio, resample-reverse e cortar o último kick | Drop em 57 com rolling **−10→0 dB**, sem lead; **não** copiar o corte global de 200–500 Hz nem o boost de 3 kHz no master |
| DeRUOw8T98Y | Mapear 8 faders + 2 sends + 3 botões; Utility `Output` com teto = premix; gravar bars 1–64 em um take | F1 kick, F2 sub, F3 rolling, F4 hats, F5 resposta, F6 madeira, F7 stab, F8 atmosfera; K1 lowpass na madeira; B1 HP no mid/high; B2 mute bateria; B3 mute graves |
| 6x1_XZDcI8I | Arranjar trocando a fonte/sequência sobre a **mesma** grade; entrada com fade de 1–2 compassos; contraste do drop por **subtração** do agudo | Mutar topo/hats 1–2 compassos antes do drop; mesma sequência em outro device; sem camada nova |

**Preservar nesta frente**
- A performance/automação só escreve ganho, filtro e send; nada de Beat Repeat, delay 100% wet ou granular que mova `.27/.77`.
- O teto do take é o premix: nenhum fader acima dele; o drop é retorno ao teto, não boost.
- Correção de 300–4.000 Hz é estática, feita antes, no premix.

### 3.8 motor-completo (7 vídeos)

**O que os mapas sustentam.** Os walkthroughs confirmam a arquitetura: **um dono de sub**, camada média separada, sidechain por banda, kick curto e afinado, hats por camada. O que varia é o timbre; o princípio é estável.

| ID | Receita concreta | Onde / valor de partida |
|---|---|---|
| S0DRqIEXW_4 | Kick: Overdrive/transiente ~1 kHz, mono <130; baixo em 3 camadas; hats em 4; stab FM+band-pass+Env | Um dono de sub; camada mid 200–800 mono <200; stab 400–900; sem Shimmer; sem EQ em 2–4 kHz |
| GyhA92cfQgE | Sine + saw **sem fundamental** (fundamental em uma camada só); phase randomization **off** no sub; camada estéreo duplicada acima do crossover; pump de filtro | Testar no BAIXO em A/B de 8–16 compassos; sub Operator intocado; hat-transiente dentro do kick só se 8k+ subir sem 2–4k e sem evento novo |
| TwZk8Gcyl1E | Low end em 4 camadas: kick 2×, baixo low impresso + high MIDI; kick afinado na escala; A/B de polaridade; sidechain só nos graves | SUB = low, BAIXO = high; cortar graves do BAIXO; duck <150 Hz; não duplicar sub |
| Fx3jM4xdw4M | Kick Utility mono, EQ cortando as duas pontas, +4 dB de transiente, limiter; baixo saw FM leve, LP12, drive, legato ~25%, duck 20–200 Hz | Bus de graves com Glue + Bass Mono **178 Hz** + rack que ducka 20–200; reforço de presença no próprio baixo em 300–1,2 kHz; sem Boom |
| ed5ODapIIBc | Kick com cadeia paralela de topo e reverb **só no médio**; sub sine; rolling com mais médio e stereo acima de 150; rhythm kick filtrado como resposta | Ghost kick 300 Hz–2 kHz nos `.27/.77`; sub sem reverb/width/Redux; sem camada nova de grave |
| ORj8Vgu2vNs | Repetição em camadas: loops de 1/4 compassos para o corpo + 8/16/32/64 para a mente; célula kick+baixo de 1 beat; colocação de sample; reverse+fade antes do acento | Intro filtrada em 17; side cut ~300 Hz só em atmos/hats/retornos; resposta rara (1 por 8 compassos); `.27/.77` intacto |
| n2rdb-8fQ9c | Kick sample curto/afinado, compressor após 50 ms; sub + camada estéreo HPF; LFO envelope no cutoff; Q&A de dois patches; hats complementares | HPF **antes e depois** do drive no SUB/BAIXO; pluck por LFO; sidechain por colisão de frequência; cortar 6 kHz nos hats |

**Preservar nesta frente**
- Kick: fonte e afinação homologadas (G#0 52,41 Hz, cauda ~0,5 s), sem click de filtro, sem boost 55–75 Hz.
- Sub: um dono, mono, sem saturação/width/reverb; sidechain só <150 Hz.
- BAIXO: `.50/.77`, sem 16º reto por cima, sem camada nova de sub; harmônicos no médio, não no fundamental.

### Onde cada aplicação costuma morar no set de referência (16 MIDI + 2 returns; não há canal granular nem de rolling dedicado)

| Aplicação | Canal/return típico | Observação |
|---|---|---|
| Cama granular (li-O, vREN, QLPV, 4q6, ZSv) | **Canal novo** ou canal de madeira; return próprio com HP | Não existe canal granular no arquivo; os antigos canais de granulador citados por dois vídeos não estão no arquivo. Se usar Granulator, Max for Live/Suite **NÃO VERIFICADO** |
| Resposta granular (f4td) | Canal percussivo de madeira (sampler) ou canal de madeira (sintetizador) | Printar o próprio material do canal; um hit por buraco |
| Duplicata +12 (ttYF) | Mesmo canal da resposta/madeira, como **layer separado** | Não é canal novo obrigatório; precisa de filtro e nível próprios |
| Fundamental + harmônicos (kGf) | **BAIXO** (Serum 2 + EQ Eight); **SUB** (Operator + Saturator) fica como dono do C#1 | O Sub do patch substitui o SUB ou fica mudo; nunca soma |
| Camada média psy / rolling (Mix6, _W, Dcs) | **BAIXO** (Serum 2) | Não existe canal de rolling dedicado; se precisar de outra instância, criar canal novo e nomear |
| Rumble (xuH, opcional) | **Return novo** (não há return de rumble; existem retorno de reverb e retorno de delay) | Retorno mono <150 Hz; sidechain do KICK |
| Rampas de 8 (bOE) | Ramo paralelo dentro do **KICK** ou return novo; cutoff no **BAIXO**; send no retorno de reverb | A rampa de low-cut no kick inteiro é o que o mapa proíbe |
| Mono/width (w1W, Cix) | Master e bus de bateria (EQ8 M/S); Utility nos canais de kick/sub | Não há grupo de graves nomeado no arquivo compacto; confirmar antes de inserir |
| OTT (Kt22) | Insert no canal de resposta ou madeira, **antes** do EQ subtrativo | Nunca no master, nunca depois do reverb |

### Ordem de A/B recomendada (8–16 compassos por vez, volume casado)

1. **Segurança/mono:** w1WsSkRLyrU + CixBgwVAAYg + retorno mono de dSXz_MFS5ks. Medir 20–120 Hz e correlação antes/depois; nada deve mudar abaixo de 120.
2. **Fundamental e corpo do baixo:** kGfIx2d4oEI (A/B de 8–16 compassos), _W_mwJVDhqA (decay 117 ms), TwZk8Gcyl1E (HPF antes/depois do drive). Medir 55–75 Hz, 300–1.200 e mono.
3. **Resposta e meio:** f4tdX3LsKj0 (granular nos buracos), ttYFldHqLWk (duplicata +24, com +12 como primeiro teste), camada média de xuHSPaCHjvo. Medir 300–1.200/1.200–4.000, 5–12 kHz e o **RMS do meio** (régua de depressão).
4. **Textura:** li-Oed1DWck/QLPV1Wk5hoE (cama) e vREN7ACIcFc (drone). Mute A/B; conferir 20–120 Hz idêntico e 5–10 kHz sem salto.
5. **Tensão/arranjo:** bOEc9c3pGi8 (rampas de 8), NCY0r4q-QcM (kick fora 53–56), 5XUULOEJ2tI (4 cenas), VSYCY__WVQ8 (portas de 8).
6. **Transições:** qvJqxGrAtCc nos respiros e 44m_K42KtX8 em 49→57. Um dono por fronteira.
7. **Melodia:** VqPpTk3gp78 (célula), oO2gdXg1-nE (ganchos), rSorLiUr6xI (ritmo/silêncio).

**Critério de parada:** se o A/B não mostrar ganho em 300–1.200/1.200–4.000 **sem** subir 5–12 kHz, **sem** mexer em 20–120 Hz e **sem** apagar `.27/.77`, a receita é descartada — não se compensa com EQ.

### Top 8 para a primeira rodada (revisado, na ordem de A/B)

| # | ID | Aplicação | Gate de aceitação |
|---|---|---|---|
| 1 | w1WsSkRLyrU | Width 0 em kick/sub + EQ8 M/S com low-cut 120 Hz só no Side, no bus de bateria e no master | 20–120 Hz idêntico; correlação ≥0,98; nada acima de 150 Hz muda |
| 2 | CixBgwVAAYg | Centro para kick/sub/rolling/hat principal; largura só em ghost notes, resposta e atmosfera; auditar returns | Soma mono não perde elemento; 300–1.200/1.200–4.000 não caem |
| 3 | kGfIx2d4oEI | BAIXO com Sub uma oitava abaixo + saw sem 1º harmônico; sub **substitui**; splitter/phase na UI | 20–60 Hz não sobe; 69–277 Hz ganha corpo; `.27/.77` intacto |
| 4 | _W_mwJVDhqA | Rolling no BAIXO com Env2 sustain 0, decay 117 ms, LP ~200 Hz, duck pelo kick | 55–75 Hz não sobe; 300–4 kHz não é cortado; onsets `.50/.77` idênticos |
| 5 | ttYFldHqLWk | Duplicata da resposta/madeira **+24** (teste inicial +12), HP 200–250/LP 4–5 kHz, velocity menor | 300–1.200/1.200–4.000 sobem; 5–12 kHz não salta; ataque original preservado |
| 6 | Mix6rW9AHgE | Camada média psy no BAIXO, C#3 com HP 100–120 (ou C#2 com HP 50–60), Env2 sustain 0 | Fundamental preservada; 120–300 não engorda; 300–1.200 sobe |
| 7 | bOEc9c3pGi8 | Rampas de 8 compassos no low-cut paralelo do kick, cutoff do rolling 300 Hz–1,2 kHz e send da atmosfera | 20–120 Hz igual; movimento espectral sem novo onset; pontuação em 9/17/25/33/41/49 |
| 8 | f4tdX3LsKj0 | Resposta granular no canal de madeira, grão 60–120/100–160 ms, HP ~276, um hit por buraco | 1 pergunta + 1 resposta a cada 2 compassos; sem sobreposição; 20–120 Hz igual |

---

## 4. O que não é traduzível

Nenhum dos 62 vídeos depende de plugin pago fora do arsenal do estilo; as dependências reais e as rotas possíveis:

| Vídeo | Dependência ausente | Por que não é literal | Rota possível | Limite declarado |
|---|---|---|---|---|
| nS7CHBL-Bzs | **SideKick** (detecção/alinhamento de fase) + Bitwig | A detecção automática e a rotação de fase por correlação são o núcleo do plugin | Utility `Ph` para A/B de polaridade + `Phase` do oscilador em passos de 45–90°; `Rand=0`/retrigger no sub | Sem detecção automática; a escolha do ponto é de ouvido/medidor, não do plugin |
| yZ-q1H6KaME | **4× ANA 2** + Bitwig step modulator | As quatro camadas e o step mod são o instrumento do vídeo | 4 camadas em Serum 2/tracks separadas; MIDI lanes no lugar do step mod | Sem step modulator nativo; a arquitetura de camadas sobrevive, o timbre não é copiável |
| 4TOQ-5mGpUY | **ANA 2** (sem oscilador granular) | O vídeo existe para **burlar** a ausência de granular; Serum 2 tem GranularOsc | Serum 2 GranularOsc direto; o "fake granular" só como cauda | Prioridade P2: o problema que o vídeo resolve não é o deste estilo |
| bOEc9c3pGi8 | **Bitwig global modulators + script Shepherd do UVI Falcon + patches de rise da ANA 2** | O mapa lista as três dependências: modulação global, Shepard pronto e rises prontos | Automação de clip/envelope por lane; Macro de Rack para mover vários alvos; Shepard construído em Vital/Serum 2 e resampleado | Sem modulador global; sem Shepard pronto; sem os patches ANA 2 — o desenho sobrevive, o custo sobe |
| dSXz_MFS5ks | **Bitwig Reverb** + effects bus | O retorno mono e o width são o mecanismo; o device é intercambiável | Hybrid Reverb no retorno + EQ8 + Utility Width 0 | O algoritmo não é o mesmo; o conceito de cauda mono é |
| li-Oed1DWck | **Bitwig Fragments** (device granular) | O empilhamento de vozes/playheads é do device | Serum 2 GranularOsc com 3–4 instâncias/camadas | O SCAN/playhead do GranularOsc real não está todo exposto no gerador de presets; ajuste na GUI |
| QLPV1Wk5hoE | **Bitwig sampler** (modos granulares) | O gesto é sample → grãos → vozes → FX | Serum 2 GranularOsc ou Granulator (Max for Live) | Max for Live/Suite não foi verificado nesta pesquisa |
| Kt22wEkGx-Y | **Bitwig Dynamics** (só demo visual) + clone "VOTT" | O Bitwig é usado para visualizar a curva; o clone substitui o OTT | Multiband Dynamics do Live em paralelo (Below só no meio) | Não é o mesmo algoritmo do OTT; a regra de ordem (antes do EQ) é o que vale |
| I__tWZTk5-Q | **Weiss EQ, Virtual Mix Rack, Soothe 2, Bass Low Extender** | Quatro dos nove estágios não existem no arsenal nativo; Soothe 2 não tem equivalente exato | EQ8 + Multiband Dynamics + Glue + Saturator/clipper; **não** usar low extender | A ordem dos capítulos não prova a ordem do sinal; a cadeia é proposta, não transcrição |
| ed5ODapIIBc | **OTT** de terceiro | O OTT é citado duas vezes; não é plugin nativo | Multiband Dynamics em paralelo, se necessário | Sem upward compression idêntica; o vídeo é P2 e o OTT não é o núcleo |
| n2rdb-8fQ9c | RComp, Hyperdimension e outros avulsos | Plugins de terceiros citados de passagem; o núcleo é Serum + Live | Compressor/EQ8/Utility/Serum 2 | O timbre dos plugins avulsos não é reproduzível; a arquitetura é |
| G4Tsj5or6A8 | **Cableguys Sidechain** | O ducking da percussão grave é feito por plugin | Compressor do Live com sidechain externo | Sem a curva do plugin; a função é a mesma |
| 6x1_XZDcI8I | **u-he Frequency Shifter** | O shift de frequência é do plugin | Shifter do Live (modo Frequency Shifter, desvio pequeno) | Sidebands diferentes; manter LP e wet baixo |
| ejNHFdtYrw0 | **ANA 2** | Aparece só como fonte do acorde de preenchimento | Qualquer pad do Serum 2/Kontakt | A técnica de bateria não depende do ANA 2 |
| kGfIx2d4oEI | **Splitter de 3 bandas, Hyper Dimension e random phase 0** no gerador de presets | O patch depende desses ajustes; o mapa confirma o parâmetro `kParamRandomPhase`, mas não há campo amigável no `OscillatorSpec` | Ajustar na UI do Serum 2; splitter pode ser reproduzido com Rack + EQ Eight (≈210 Hz/≈1 kHz) | **NÃO VERIFICADO** no gerador; sem a UI, o patch não fica fiel |
| ORj8Vgu2vNs | **Bitwig** como DAW de costume | O autor usa Bitwig, mas o método é de colocação/loop | Live 12 + Simpler/Sampler | Nada do método depende do Bitwig |

**Fora de escopo por decisão de projeto, não por falta de plugin:** `Kickstart 2` (demo/licença) e qualquer sample criado sob demanda ou recorte das referências.

---

## 5. Vídeos sem legenda / NÃO VERIFICADOS

| ID | Estado da legenda | O que foi usado | O que fica NÃO VERIFICADO |
|---|---|---|---|
| I__tWZTk5-Q | **Sem legenda** — `yt-dlp` confirma "no automatic captions"; só `live_chat` | Descrição oficial + capítulos/metadados | Todos os valores de parâmetro e a **ordem do sinal**: a cadeia é a ordem dos capítulos, não uma demonstração; não há fala transcrita |
| VSYCY__WVQ8 | **Legenda bloqueada** — HTTP 429 em 4 tentativas; faixa `en` existe, entrega bloqueada | ASR local (`whisper-cli`, `ggml-small.bin`) sobre o áudio; 269 linhas | Grafia exata de termos; posições/nomes de camada são reconstrução de quem mapeou, não dados do projeto de Rene Wise; o próprio mapeador diz que fez o mapa de ouvido |
| iteUJHS5YNE | **Legenda bloqueada** — HTTP 429 em 5 tentativas; faixa `en` listada | ASR local (`whisper-cli`, `ggml-small.en.bin`); 719 linhas, 21:02 de fala | Palavras técnicas corrompidas pelo ASR ("roar"=Roar, "9-on-nine"=909, "one six"=1/16); números citados são da fala, não de demonstração |
| 5XUULOEJ2tI | **Legenda bloqueada** — HTTP 429 em 6 tentativas | ASR local (`whisper.cpp`, `ggml-small.bin`); VTT com 374 linhas | Citações são da transcrição ASR, com erros preservados; a análise é de uma track de Valentino Mora, não demonstração de parâmetros |

**Limites herdados que valem para o dossiê inteiro**
- **Nenhum áudio de vídeo foi ouvido como fonte musical** na produção dos 62 mapas; todos são leitura de legenda/ASR/descrição. Nos três vídeos transcritos por ASR (VSYCY__WVQ8, iteUJHS5YNE, 5XUULOEJ2tI), o áudio foi transcrito localmente, não escutado; em I__tWZTk5-Q não há fala transcrita. "O vídeo diz" não é "o som funciona".
- **Nenhuma medição nova** foi feita nesta pesquisa; os números de 300–4.000 Hz vêm do comparativo de 26/10 e foram apenas citados.
- Valores marcados como `HIPÓTESE` nos mapas (ex.: tempo "7" do Echo em v-mjY-Vlgv0; ressonância 80% do kick em IbeXMrvWAew; arquitetura do kick em TwZk8Gcyl1E não inspecionada) continuam não verificados.
- O arquivo do set lido em 27/10 não tem canal granular; os canais de granulador citados por dois vídeos vêm de estudo de 25/10 — **conflito declarado, não resolvido**.
- 90VpsmIaPuk registra **divergência real** entre HPF 160 Hz (parecer de FX/Atmos) e 90 Hz (trilha 33); decidir no set.

---

## 6. Perguntas prováveis do produtor

Respostas curtas com o material disponível; o que não tem base está marcado `NÃO VERIFICADO`. Não são decisões de produto.

1. **Isso vira tech house?** O próprio mapa do xuH cita a fonte de gênero: "tiraram o Rumble base do hard techno e colocaram um rolling base" (opinião transcrita de fonte externa, não medição). Por isso o rumble **saiu do top-8** e ficou opcional no §3.1: a parte segura é a camada média; o rolling já é o BAIXO. Se o A/B com rumble fizer o motor soar hard techno, descarta. **NÃO VERIFICADO** no áudio.
2. **Engorda o sub?** Nenhum A/B foi rodado; **NÃO VERIFICADO**. As receitas têm gate escrito: 20–120 Hz idêntico (±0,2 dB), correlação 1,00, retorno mono <150 Hz. A camada do kGf troca a fundamental de camada; a do Mix6 decide o HP pela nota; o rumble opcional do xuH tem HP 120. Nenhuma prova até render.
3. **A camada em C#2 com HP "acima do sub" sobrevive?** Não com HP 80–100: C#2 = 69,3 Hz, e o mapa do `_W` diz que 80–100 "comeria o fundamental". Duas saídas: tocar em **C#3 (138,6 Hz)** com HP 100–120, ou tocar em **C#2** com HP **50–60 Hz** (remove o C#1 de 34,65 e preserva o C#2). A segunda não é "acima do sub", é "acima do C#1". Qual soa melhor: **NÃO VERIFICADO**.
4. **Qual canal?** Não existe canal de rolling dedicado no arquivo; BAIXO = Serum 2 com notas 37/38/44/49/50 (C#2–C#3); SUB = Operator MIDI 25 (C#1). Uma "camada psy em C#2" dentro do BAIXO duplica as notas existentes; tem de ser layer interno ou canal novo, com A/B contra o BAIXO. O mapa não resolve; **NÃO VERIFICADO**.
5. **O Sub do kGf cai no C#1 do Operator. Substituo, deixo mudo ou somo?** O mapa é explícito: "nunca somar o Sub do patch ao sub que já existe" — ou o Sub do Serum vira o sub da faixa, ou fica mudo e o Operator carrega. Qual preserva o sub aprovado: **NÃO VERIFICADO**. O `random phase = 0` existe como `kParamRandomPhase`, mas não tem campo amigável no `OscillatorSpec`; ajustar na UI.
6. **3–4 camadas contra "uma cama, não três"?** São camadas de **uma** cama, não três camas independentes. O arranjo está no §3.3: 1–16 só A; 17–32 entra B; 33–48 entra C; 49–56 entra D e abre o reverb; com buracos e automação. O playhead deslocado — coração do vídeo — só sai na GUI ou em 2–3 instâncias; o gerador não escreve o SCAN. **NÃO VERIFICADO** no gerador.
7. **Qual régua vale: perfil contra 6 refs ou higiene de médios?** As duas estão declaradas e **não foram conciliadas**: o comparativo mede déficit de −4,83/−5,76 dB; a régua homologada fixa 400 Hz–2,5 kHz em depressão relativa ao RMS. Se o RMS do meio subir acima do que a segunda permite, a decisão é do produtor. As 8 aplicações são hipóteses; nenhum A/B.
8. **+24 ou +12?** O vídeo diz "two octaves higher" (+24); +12 é downgrade do mapa, para não invadir 1,2–4 kHz. O primeiro A/B deve ser a **segurança/mono** (w1W), com tolerância de 20–120 Hz ±0,2 dB e correlação 1,00; só depois a duplicata. **NÃO VERIFICADO**.

---

## 7. Fontes consultadas

**Mapas (62, lidos integralmente nesta consolidação):** um mapa por ID listado no §2; legendas e curva machine-readable (62 vídeos, `canal`, `frente`, `prioridade`, `porque`) ficaram no acervo de origem. Os estudos internos citados pelos mapas (estudo de bateria/baixo de 17/10; comparativo de motor de 26/10; gates e réguas do projeto; dossiê homologado) pertencem ao projeto original e não são reproduzidos aqui — os números citados destes estudos estão embutidos no texto acima com a marcação de origem.

**O que não foi consultado nesta consolidação:** os áudios dos vídeos; o DAW aberto; nenhum render; nenhuma nova medição de áudio. **Nenhum A/B foi executado.**
