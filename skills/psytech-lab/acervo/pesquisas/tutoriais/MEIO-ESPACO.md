# Meio e espaço — tutoriais traduzidos

**Use quando** a tarefa mexer em médio (300–4.000 Hz), largura ou estreitamento, centro × lateral, reverb/return, panning, dry/wet, OTT ou duplicata de oitava. Frente de **5 mapas**: 4 alinhados e 1 em conflito (`ttYFldHqLWk`). Não é a frente de grave/punch (`PRESSAO-GRAVE.md`) nem de cama granular (`TEXTURA-ATMOSFERA.md`). As medições de referência (déficit de médio, fechamento do meio, low-end mono) ficam no projeto que usa este estudo — este documento não repete os números.

**Aviso de escopo:** quatro das cinco técnicas **desmascaram** o centro (pan, mid/side, retorno mono, guardrail do OTT); só `ttYFldHqLWk` **adiciona conteúdo**. Tratar pan ou largura como correção do déficit espectral é erro de alvo.

## Regras

- **largura por contraste** — a mix parece larga porque *poucos* elementos são largos; o centro precisa estar ocupado (`dSXz [00:01:50.480–00:01:53.480]`). Tudo largo, com delay e reverb em cada canal, produz mix sem punch (`Cix 00:28.640–00:40.389`). Estreitar é ferramenta de clareza, não perda.
- **centro é regra; lateral é decoração** — kick, sub, rolling e hat principal em Width 0%; a largura vai para ghost notes, percussão de resposta e atmosfera (`Cix 04:24.560–04:36.150`; `OJ3 00:01:01.830–00:01:09.270`). Low-end <150 Hz rigorosamente mono e sem desfasamento estéreo no sub/kick. Diretriz do projeto de referência: a banda mais larga da mix é o **MÉDIO**; médio mono = mix fechada.
- **cauda em return mono, dry sagrado** — reverb 100% wet no return, somada mono, com HP/LP e pan oposto ao dry; o canal solista continua seco (`dSXz [00:01:34.760–00:01:37.440]`). O dry da madeira/acústico passa intacto; a cauda pontual em return dedicado é diretriz provisória do projeto de referência.
- **densidade sem volume** — fechar o médio é adicionar conteúdo tocado (duplicata +12, camada, resposta), nunca boost de EQ nem OTT (`ttYF [00:05:00.880–00:05:09.790]`). O OTT levanta o que é quieto e **desfaz o EQ anterior** (`Kt22 06:43.816–06:50.237`); empilhado em canais, engorda o master sem subir a banda.
- **pan estático, sem Haas** — posicionar com pan pequeno e estático, ouvindo a música inteira, sem Solo, e devolver o gain de escuta (`OJ3 00:02:41.430–00:02:46.870`). Microdelay/Haas cria comb filtering — é a receita do brilho metálico, não de largura (`Cix 04:24.560–04:36.150` usa posição, não atraso).

## Receitas traduzidas

Valores sem marca vêm da legenda do mapa; `(H)` = proposta do estudo, não testada. Todas as receitas preservam os offsets `.27/.77` do bolso de referência e nada abaixo de 120 Hz sai do centro.

| técnica | fonte/ID | device | parâmetros | limite |
|---|---|---|---|---|
| Retorno **MONO ROOM** | `dSXz_MFS5ks` `[00:01:34.760–00:01:37.440]` | Hybrid Reverb → EQ8 → Utility, em **return** | Reverb 100% wet; HP 280–320 Hz; LP 4–5 kHz; Width 0%; pan do retorno oposto ao dry; send −12/−18 dB na resposta, médio na madeira `(H)` | zero em kick/sub/rolling; subida e atmosfera podem continuar largas; monoar cauda sem LP vira aspereza; **não** é preenchedor de banda; diretriz provisória no projeto de referência |
| Campo mid/side por elemento | `CixBgwVAAYg` `00:28.640–00:40.389` | Utility (Width) + pan de chain no Drum Rack + Echo | Width 0% em kick/sub/rolling/hat principal; largura em ghost/resposta/atmosfera; baixar o "stereo input" do echo que veio 100% estéreo (`01:39.350–01:48.710`) | não sobe 300–4.000; auditar returns que recebem kick; "Width 0 em tudo" é ler o vídeo ao contrário |
| Pan estático de relógio | `OJ3Fxk4E0gU` `00:00:47.110–00:00:56.270` | Utility Gain +6 dB (só escuta) + pan do canal | música inteira, sem Solo; posições pequenas; devolver Gain a 0 (`00:02:41.430`); duas passadas; Bass Mono/HP antes | pan é *balance* no Live: fonte estéreo só perde um lado, não rotaciona; nada <120 Hz fora do centro; sem AutoPan/microdelay |
| Encurtar largura na fonte | `CixBgwVAAYg` `01:39.350–01:48.710`; `02:51.440–02:57.270` | Echo (stereo input) / largura do instrumento / Utility | clap e snare "fairly mono"; echo estéreo estreitado na própria fonte; Utility só quando a fonte não tem controle | não empilhar segundo delay; não usar widener no bus de hats; não "consertar" largura com EQ depois |
| Duplicata **+12** de resposta/madeira | `ttYFldHqLWk` `00:05:09.800–00:05:26.950` | layer no canal da resposta (ou canal próprio) + EQ8 | +12 no primeiro teste; HP 200–250 Hz; LP 4–5 kHz; velocity abaixo do original; mesmos offsets `.27/.77` | camada com filtro e nível próprios, nunca ganho; LP só na camada, nunca no canal vivo; +24 cai em outro conflito; **aceite depende da régua do médio do projeto** |
| OTT pontual (guardrail) | `Kt22wEkGx-Y` `02:06.173–02:09.990`; `12:13.833–12:18.681` | Multiband Dynamics em paralelo | crossovers ~300 Hz / 4 kHz `(H)`; Below só na banda do meio; Amount baixo; release ≥150 ms `(H)`; ordem OTT → EQ subtrativo → sends | nunca master/kick/sub/hats; não fecha o vale; desfaz EQ feito antes; reverb/send sempre depois dele |

**Encaixe:** return dedicado para o MONO ROOM (confirmar os returns existentes do projeto de destino antes de criar um novo). Duplicata e OTT são insert/layer, sem canal novo obrigatório. No projeto de referência o baixo é Serum 2 e não há canal de rolling dedicado — confirmar no projeto de destino.

## Conflitos e cautelas

| tutorial | o que o vídeo faz | como adaptar |
|---|---|---|
| `ttYF`: duplicata "two octaves" (+24) | Duplicata duas oitavas acima | Primeiro teste em **+12**; +24 só se a fonte for oitava 2 e o resultado ≤4; camada, nunca ganho. Na referência, oitavas agudas de euforia ficam fora do registro. |
| `ttYF`: duplicar a mesma frase | Segunda melodia na mesma oitava | Duplicar só resposta/madeira, nunca solista; +12 garante outra oitava; dobra na mesma oitava é bug. |
| `ttYF`: OTT + saturação para fechar o vale | Compressão upward como preenchimento | OTT só na camada de médio, em paralelo e baixo; saturação paralela; nada no master; preencher com conteúdo. |
| `Cix`: ghost notes com Auto Pan | Largura por AutoPan | Posicionar ghost com pan estático por chain; AutoPan só como orbitador dedicado, nunca como widener. |
| `dSXz`: monoar a cauda de todo mundo | Return mono universal | (INFERÊNCIA) usar o return mono só em elemento que deve sentar no centro (resposta/madeira); a largura real do médio vem de ghost notes e camadas estéreo acima de ~150–250 Hz, não do return. Medir side/mid de 400 Hz–2 kHz antes/depois. |

## A/B

Medir sempre em estéreo, na taxa original, volume casado. Não comparar bandas medidas em escalas diferentes.

**A/B 1 — centro defendido + cauda mono (`Cix` + `dSXz`).**
Trecho: **8 compassos de motor já estabelecido com resposta de madeira (ex.: compassos 9–16, 0:15–0:30)**; repetir em 25–32 se quiser um segundo bloco, sem atravessar fronteira de cena.
A: estado atual. B: return MONO ROOM só em resposta/madeira (send −12/−18 dB) + Width 0% onde houver largura em kick/sub/rolling/hat principal.
Critério:
- 20–120 Hz idêntico dentro da tolerância declarada no projeto; correlação <120 Hz ≥0,98.
- 300–1.200 e 1.200–4.000 **não caem** na soma mono; se caírem, o send retirou o portador do centro.
- 5–12 kHz não sobe (proteção contra a aspereza do phasing mono).
- Side/mid de **400 Hz–2 kHz não piora**. Se piorar, o retorno mono está sendo usado como preenchedor e o meio fecha ainda mais: largura tem de vir de ghost/resposta/atmosfera, não do return.
- Posições de onset `.27/.77` idênticas (pan e width não deslocam tempo).

**A/B 2 — duplicata +12 (`ttYF`).**
Trecho: **16 compassos de cena de resposta (ex.: compassos 17–32, 0:30–0:45)**.
A: bypass. B: layer +12 na resposta/madeira com HP 200–250, LP 4–5 kHz, velocity abaixo, mesmos offsets.
Critério:
- 300–1.200 e 1.200–4.000 **sobem** (direção; a magnitude é decisão da régua do médio do projeto).
- 5–12 kHz sem salto; 20–120 Hz idêntico; nenhum conteúdo novo abaixo de 200 Hz.
- Nenhuma nota nova e nenhum onset novo: só a mesma frase uma oitava acima, nos mesmos offsets.
- Se o RMS do médio subir acima do que a régua do projeto permite, é decisão do produtor.

## Evidência

Os mapas completos por vídeo (um por ID, com timestamps) não acompanham este pacote; os IDs listados identificam cada fonte. Proveniência: leitura de legenda automática.

## NÃO VERIFICADO / pendências

**Condicionam esta frente:**
- **Régua do médio em aberto no projeto de referência.** Sem ela, o A/B 2 mede direção, não aprova a duplicata; nenhuma receita de densidade tem critério de aceite.
- **Cauda em return é diretriz provisória** no projeto de referência; não substitui a regra anterior até homologação.

**NÃO VERIFICADO:**
- Nenhum A/B executado e nenhum render desta frente; documento de leitura, sem medição nova.
- Estado do projeto de destino não lido nesta redação — confirmar returns e composição antes de criar return.
- Não há prova de slot livre para um return adicional; criar o MONO ROOM pode exigir realocar — decisão do produtor.
- Larguras atuais por canal não medidas; o "Width 0" pode já estar aplicado, e o teste viraria no-op.
- Reverb/FX interno do Serum 2 no baixo não inspecionado; se ativo, o return não cobre essa cauda (INFERÊNCIA de arquitetura).
- Escala do Utility do Live não é linear: só 0% é seguro ler como mono; 50% não significa metade.
- Mono fold-down do motor não testado: elemento paneado pode **desaparecer** por cancelamento, não por posição.
- Crossovers ~300/4 kHz do OTT e release ≥150 ms são proposta do estudo `(H)`, não fala do vídeo.
- O algoritmo de reverb do vídeo é Bitwig; só o conceito (return mono, cauda posicionável) transfere — o timbre não.
