# Como os artistas fazem — Akari × Yao × Kaled × Gazolla (régua única)

2026-09-08. **Mesma régua de análise para todos** (ffmpeg→numpy, STFT 1024/256 @22.05 kHz, grid por R-scan no envelope LF 30–120 Hz, onsets por banda, pausas de LF ≥0,3 s, janela 0–300 s). Refs: Akari *Segments*, Yao *Limbo*, Kaled *Bush*, Gazolla *Mayuri*.

## Tabela-mestra (VERIFICADO)

| Métrica | Akari | Yao | Kaled | Gazolla |
|---|---|---|---|---|
| BPM medido | 128,0 | 130,0 | 132,0 | 127,0 |
| R do grid (0–1) | 0,90 | 0,54 | **0,96** | 0,73 |
| % kick no grid | 89,1% | 58,7% | **92,3%** | 89,0% |
| Pausas de LF (nº) | 7 | 13 | 8 | 28 |
| Duração média da pausa | 1,7 beat | 1,2 | 1,3 | 1,6 |
| Salto médio no retorno | +33 dB | +37 | +25 | +35 |
| Kick rate 1ª/2ª metade (evt/s) | 0,8 / 0,5 | 0,7 / 0,5 | 1,4 / 1,7 | 1,2 / 2,0 |
| HF rate 1ª/2ª metade (evt/s) | 7,2 / 4,8 | 7,5 / 5,6 | 4,5 / 6,0 | 7,2 / 4,3 |

Leitura do detector: "kick rate" conta eventos LF (kick + re-trigger de bass na mesma faixa de frequência); "pausa" = furo de LF; "riser" do Gazolla/Kaled aparece dentro dos furos (Gazolla @6,8 s e @14,3 s: +11/+12 dB/s; Kaled @86,4 s: +9,8 dB/s em 5–12k).

## As 5 diferenças que definem o som deles (e o que aplicar)

1. **Dosagem do low-end por seção (a maior diferença).** O LF deles acelera com a faixa: Akari/Yao andam a 0,7–0,8 evt/s nas construções e chegam a 1,7–2,0 nos drops; Kaled 1,4→1,7; Gazolla 1,2→2,0. Um groove que corre no talo o tempo todo (sub em 16ths + baixo médio + kick sempre densos) perde o contraste entre seções — e é isso que "trava" a história. **Aplicar:** sub/baixo menos densos na intro/prep/build (offbeat em 8ths, sem 16ths), 16ths só nos drops e no clímax.
2. **Poucas pausas, mas pausas GRANDES com retorno em degrau.** Akari/Kaled: 7–8 pausas em 300 s, durando 1,3–1,7 beat, voltando com +25/+33 dB de degrau. Mini-furos constantes (curtos, retorno fraco) picotam o groove e os retornos não marcam. **Aplicar:** consolidar mini-furos em 2–4 chegadas grandes por bloco, retorno seco e forte.
3. **Corte FORA do downbeat.** Kaled corta sistematicamente em beat 2–3 do compasso (barpos 2,0–2,2 nos 3 maiores furos); Gazolla corta em 1,5–2,4. Isso gera a antecipação "parada no ar". **Aplicar:** nos próximos cortes, puxar o furo para beats 2–3.
4. **Arco de topo (HF): eles FECHAM.** Gazolla 7,2→4,3 e Akari 7,2→4,8 evt/s — o topo seca e o transe assume. Terminar a faixa com MAIS topo do que se começou inverte o arco do gênero. **Aplicar:** secar HF na 2ª metade (menos camadas de glitch/perc aguda simultâneas pós-clímax).
5. **Grid.** Kaled é cirúrgico (92% no grid, R 0,96) e Akari 89%; Yao fica em 58,7% (pocket deliberado). Manter swing perceptual (o Gazolla antecipa −13 ms no contratempo) mas revisar elementos que atrasam de verdade.

## Limites

Detector LF não separa kick de sub (conta eventos); MP3s das refs (masters diferentes); janela 0–300 s (finais não analisados); pausas detectadas podem incluir seções de construção com kicks esparsos. A comparação de níveis de dB é interna a cada faixa.
