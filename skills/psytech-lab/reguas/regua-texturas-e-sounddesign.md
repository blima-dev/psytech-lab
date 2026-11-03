# RÉGUA — TEXTURAS E SOUND DESIGN (Serum · madeira orgânica · atmosferas · FX)

v0.1.0 · 03/11/2026

> Destilada do acervo limpo `plugins/psytech-lab/skills/psytech-lab/acervo/` (01/11/2026) + mapa de conflitos `MAPA-DE-LACUNAS-E-CONFLITOS-20261030.md` (30/10; arquivo completo fora do pacote).
> Régua descreve referência externa ou teoria; contraste com o set do projeto aparece como **CASO** (§I). Conflito aberto no mapa → **EM DISPUTA** (§H).

## Fontes (15)

Acervo, base `acervo/`: `PSYTECH-LAB/04-SINTESE-SONORA-E-RECEITAS-POR-FUNCAO.md` (30/10) · `pesquisas/tutoriais/TEXTURA-ATMOSFERA.md` (27/10) · `pesquisas/Estudo Synth e Atmos e FX.md` (17/10) · `pesquisas/ESTUDO-ARRANJO-FX-DESENHO-20261025.md` (25/10) · `pesquisas/AUDITORIA-PACKS-ORGANICOS-20261029.md` (29/10) · `pesquisas/cursos/PRESETS-SERUM-20261025.md` (25/10) · `pesquisas/cursos/OMAR-MEHO-SOUND-DESIGN-20261025.md` (25/10) · `knowledge-base/BASS_MONSTER_Supreme_Serum2_Processing.md`, `Leads_from_Forest_Dark_Serum2.md`, `FOREST_AMBIENCES_Aula_Completa.md`, `MODO_ALIEN_Dark_Psytrance_Serum2.md`, `KUNI-SOUND-MANUAL-DEFINITIVO.md` (knowledge-base 11–15/10, conforme MAPA §2) · `knowledge-base/KUNI-SOUND-GUIAS-COMPLEMENTARES.md` (06/09) · `genre-dna/psytech-dark-prog.md` (14/10, origem: biblioteca de conhecimento do projeto original, fora do pacote).

## A. Arquitetura do sound design

1. Montar a cadeia como híbrido amostra+sintetizador — fonte humana/acústica → transformação digital → retenção de vestígio físico; prioridade máxima da cena (Estudo Synth e Atmos e FX, 17/10).
2. Fazer o sound design ganhar escassez, parentesco e consequência narrativa: madeira/voz/foley geram a matéria, Serum/granular/FM/spectral a deformam, tails e atmosferas ocupam as bordas (Estudo Synth, 17/10).
3. Toda camada nova substitui ou enriquece uma função existente, em vez de criar mais uma camada simultânea — troca, não soma (Estudo Synth, 17/10).
4. Reciclar o mesmo patch/material entre leads, plucks e pads para DNA coerente (KUNI-SOUND-GUIAS, 06/09); resamplear o mesmo gesto orgânico por vias diferentes faz timbres "parentes" (Estudo Synth, 17/10).
5. Escolher um instrumento para conduzir e centralizar o resto em volta; padrão complexo pede os outros simples (OMAR-MEHO cheat sheet, 25/10).
6. Partir de Serum 2 + Live 12 nativos — cobrem wavetable, sample, granular, spectral, FM/PD/RM antes de comprar plugin novo (Estudo Synth, 17/10).

## B. Serum 2

7. Seguir a economia por função medida no pack Drift (152 presets): baixo 2 camadas/2 FX · lead e pluck 3 camadas/5 FX · pad 2 camadas; mediana de rotas de modulação 3 no baixo e 7 no lead (PRESETS-SERUM, 25/10).
8. Resolver o timbre dentro do patch — EQ interno em 105/152 presets do pack; o ajuste no DAW é fino, não estrutural (PRESETS-SERUM, 25/10).
9. Usar phase distortion (`kPD_OSC`) como via de sujeira controlada: warp mais comum do pack, 28 de 152 (PRESETS-SERUM, 25/10).
10. Envelope ENV1 de referência do pack: attack 0,5 ms · decay 1,0 s · sustain 0,79 · release 76 ms · cutoff mediana 43,4/100 (PRESETS-SERUM, 25/10).
11. Encorpar com distorção idêntica antes e depois do filtro (soft clip ou tube); tipos diferentes afetam harmônicos distintos e estragam a fase (Leads_from_Forest_Dark, kb 11–15/10).
12. Engordar com face shifting (Diffuser no filtro 2 em série; splitter low/mid/high), mantendo o fluxo filtro 1 → filtro 2 (BASS_MONSTER, kb 11–15/10).
13. Adicionar bus paralelo de distorção agressiva saindo do filtro 2 (overdrive + EQ + filtro pós) com macro no mix — zero plugin externo (BASS_MONSTER, kb 11–15/10).
14. Desenhar MIDI dentro do clip do Serum (salva no preset; note expression para bends/glides); glide exige sustain no amp envelope (BASS_MONSTER, kb 11–15/10).
15. Construir conversas de síntese com chains no Instrument Rack: troca de timbre a cada nota tocada (arpejador/nota antes do chain selector), até 127 chains; automação no gate deixa o resultado psicodélico (MODO_ALIEN + Leads_from_Forest_Dark, kb 11–15/10).
16. Travar o warp handle para o timbre ficar consistente em vez de randomizar (Leads_from_Forest_Dark, kb 11–15/10).
17. Fazer stab metálico com FM a partir de sine básica + Spectral Morph para extrair timbre "seco" (KUNI-SOUND-MANUAL, kb 11–15/10).

## C. Percussão orgânica de madeira

18. Distribuir o material orgânico por função: acento/resposta no espaço negativo (one-shots 0,2–1,0 s) · topo percussivo contínuo (loops) · madeira melódica (marimba/woodwinds) · cama granular (texturas ~1,5 s por grão-fonte) (AUDITORIA-PACKS-ORGANICOS, 29/10).
19. Reafinar material de pack para a tônica do projeto: marimba vem rotulada "121 BPM – Gmin" e os MIDI dos packs pedem conferência de tonalidade (AUDITORIA-PACKS, 29/10).
20. Tratar percussão como direção rítmica: microvariação com LFO aleatório no pan e no Auto Filter impede o som robótico (KUNI-SOUND-MANUAL, kb 11–15/10).
21. Dosar a madeira como lado secundário — o valor do estilo mora no baixo/sub (AUDITORIA-PACKS, 29/10).
22. Tirar acentos dos one-shots de perc (Tulum Percs 120 · Essentials Shaker/Percussion/Stick Shots) e topo contínuo dos loops de acoustic/subtle percussion (AUDITORIA-PACKS, 29/10).

## D. Atmosferas, granular e camas

23. Dar buracos à textura: cama entra e sai por seção, o silêncio faz parte, e os acentos `.27/.77` ficam livres de hit (TEXTURA-ATMOSFERA, 27/10).
24. Nascer a cama de fonte acústica (madeira, voz, campo) — grão é fatia de sample, fonte escura vence filtro corretivo; granular aplica-se em cama/resposta acima do HP, não no motor de grave (TEXTURA-ATMOSFERA, 27/10).
25. Travar o pitch: `random_pitch` 0 no drone e ±2 st no máximo na textura; a variação vem de posição, comprimento de grão e pan (TEXTURA-ATMOSFERA, 27/10).
26. Ajustar grão por função: drone 150–300 ms · resposta percussiva 60–120 ms · madeira 100–160 ms · cama lisa = grão longo + densidade alta (TEXTURA-ATMOSFERA, 27/10).
27. Construir cama orgânica em 8 vozes/uníssono com start point diferente por voz, loop fwd/back e filtro automatizado por seção (TEXTURA-ATMOSFERA, 27/10).
28. Construir as 3–4 camadas como camadas de UMA cama (mesma fonte, offsets deslocados), não pads independentes (TEXTURA-ATMOSFERA, 27/10).
29. Manter cauda em return 100% wet alimentado por pulsos curtos de send, com kick/sub/baixo em send zero (TEXTURA-ATMOSFERA, 27/10 — diretriz provisória do projeto de referência).
30. Derivar atmosfera do próprio lead: Grain Delay → delay paralelo (dry 100% + wet com feedback, controle por volume) → Gated Stretch → Beat Repeat ~1/4 antes → triple LFO random smooth em macros; cauda de fundo em −5 a −8 dB (FOREST_AMBIENCES, kb 11–15/10).
31. Congelar e capturar cauda de reverb (freeze & capture) de elemento da própria track para criar pad/wash coerente (KUNI-SOUND-MANUAL, kb 11–15/10; KUNI-SOUND-GUIAS, 06/09).
32. Ancorar drone no intervalo de quinta justa da tônica — tensão estável que puxa para a tônica (KUNI-SOUND-MANUAL, kb 11–15/10).
33. Construir pad dark com ataque longo, ratios 1×/2×/3× sobre a tônica (0/+12/+19 st) e unison shimmer, com LP abrindo por seção em vez de estático (TEXTURA-ATMOSFERA, 27/10).
34. Engrossar o motivo/baixo com dobra filtrada: duplicar o clip, cortar todo o grave, LP ~5–6 kHz, Roar leve e nível abaixo do original — sem criar ataque novo (TEXTURA-ATMOSFERA, 27/10).
35. Partir de filtros de entrada por função: cama HP 250–300 · atmosfera/pad HP 180–300 · resposta granular HP ~276 (TEXTURA-ATMOSFERA, 27/10).

## E. FX e transições

36. Guardar o silêncio total para 1–3 momentos por faixa, quase sempre no último terço; nas demais fronteiras transformar (sweep/wash/riser) em vez de desligar (ESTUDO-ARRANJO-FX-DESENHO, 25/10).
37. Usar riser e downlifter em pares (sobe antes da fronteira, desce depois) e manter impact/roll raros — 0–0,3/min na família (ESTUDO-ARRANJO-FX, 25/10).
38. Concentrar FX no último terço da faixa, como faz a família de referências (ESTUDO-ARRANJO-FX, 25/10).
39. Fazer transições de material próprio: cauda de reverb/delay throw + Low-Pass fechando na cabeça de break; cabeça de drop com impact sub-grave + downlifter + micro-vácuo antes da pancada (genre-dna psytech-dark-prog, 14/10).
40. Marcar fronteira com sucção — remover o 4º kick antes da transição gera antecipação física (KUNI-SOUND-GUIAS, 06/09; KUNI-SOUND-MANUAL, kb 11–15/10).
41. Montar build dobrando velocidade por ÷2 (1/4 → 1/8 → 1/16 → 1/32) com volume descendo e filtro fechando — a ilusão de drop maior vem do contraste (OMAR-MEHO, 25/10).
42. Preparar drop com bridge de 2–4 compassos: crash com reverb+delay+sidechain entrando baixo, riser de ruído (Noise + band-pass ressonante + sweep + Auto Pan) e reverse crash/kick imediatamente antes (OMAR-MEHO, 25/10).
43. Deixar o FX crescer de volume ao longo do tempo — soa como saltar para fora (OMAR-MEHO, 25/10).
44. Combinar técnicas de transição (tirar antes de entrar + fill + upbeat antecipado + silêncio de 1–2 compassos + reverb grande na frente do drop) — a combinação é a versão profissional (OMAR-MEHO cheat sheet, 25/10).
45. Fazer o "simmer" com ruído branco + band-pass de sweep descendente, caráter de poeira/vapor (KUNI-SOUND-GUIAS, 06/09).

## F. Espaço, largura e grave

46. Criar Side real acima de ~150–250 Hz com conteúdo L/R genuinamente diferente (granular com posições independentes, delays/reverbs decorrelacionados, modulação distinta por canal); pan e Utility manipulam largura existente, não criam Side (Estudo Synth, 17/10).
47. Manter mono ≤120 Hz: motor de grave focado, texturas nas bordas (Estudo Synth, 17/10).
48. Usar o fader como profundidade — abaixar o nível assenta o elemento mais fundo na mix (OMAR-MEHO, 25/10).
49. Conferir a mistura em mono antes de abrir em estéreo (OMAR-MEHO, 25/10).

## G. Régua numérica do corpus de referência (externa)

50. Medidas do corpus de referências do gênero (10 faixas dissecatas, sendo 1 a faixa do projeto — régua técnica do estilo, não standard da indústria; Estudo Synth, 17/10): 8 kHz+ −22,1 a −20,1 dB · "ar" −17,2 a −16,1 dB · centroide 266–287 · presença ≈0,51 · correlação média L/R 0,32–0,44 · densidade ≤6,99 picos/s.
51. Faixas operacionais de partida por família (Estudo Synth, 17/10): stab HP 120–180 Hz · glitch HP >150 Hz · voz HP 100–250 Hz · atmos HP 120–300 Hz conforme a fonte · FX de transição HP 150–250 Hz quando não deve ocupar o motor de grave.

## H. EM DISPUTA

52. **EM DISPUTA — topo percussivo contínuo.** Leitura A (cânon): Pilar 3 pede topo percussivo contínuo, régua provisória citada na auditoria dos packs (AUDITORIA-PACKS, 29/10). Leitura B: G16/G17/G18 estão PROVISÓRIAS e não substituem o Pilar 3 sem homologação auditiva (MAPA 30/10 §3.8). Decide o ouvido do produtor.
53. **EM DISPUTA — HPF do drone em seções abertas.** Leitura A: 90 Hz. Leitura B: 160 Hz. As fontes divergem; decisão no projeto de destino (TEXTURA-ATMOSFERA, 27/10).
54. **EM DISPUTA — BPM/tom do transporte.** Leitura A (cânon): 128 BPM + C# frígio. Leitura B (estado): arquivo atual em 130 BPM, tratado como estado e não lei nova (MAPA 30/10 §3.3). Afeta reafinação/estica de loops de pack (120/121 BPM) e MIDIs.
55. **EM DISPUTA — stems de IA (Demucs/M4A) como fonte.** Leitura A: separação útil como material. Leitura B: resultado é estimativa; leitura de instrumento isolado exige etiqueta `ESTIMATIVA` (MAPA 30/10 §3.7).

## I. Casos (contraste com o set do projeto — não régua)

56. Bass do set construída como "lead do pack" — 3 camadas/5 FX/8 rotas/release 0,20 s contra 2/2/3/0,076 s do pack: mais sobreposição e cauda no grave; redução a 2 camadas é teste proposto (PRESETS-SERUM, 25/10).
57. Render do projeto fora do corpus: 8 kHz+ −25,6 dB · ar −20,1 dB · centroide 217 · presença 0,64 · correlação 0,80 · densidade 7,57 picos/s; +3 dB de shelf nas fontes entregou só ~+0,8 dB em 8–16 kHz (Estudo Synth, 17/10).
58. Gap de silêncio do projeto = 1,33/min, 3–12× o máximo da família — o corte total perdeu o valor dramático (ESTUDO-ARRANJO-FX, 25/10).

## J. Limites declarados

59. Nenhum A/B da frente textura foi executado; os critérios são protocolo, não resultado (TEXTURA-ATMOSFERA, 27/10).
60. Granulator 3/Max for Live não verificados no ambiente; o gerador de presets não escreve o SCAN/playhead do GranularOsc; `granular_reverse` é booleano; "Grain Size 226" é unidade do Live, não ms; preset granular depende do WAV junto; LFOs não travam fase entre renders (TEXTURA-ATMOSFERA, 27/10).
61. Síntese sistemática pendente (SYN-01…SYN-10): fase fixa vs random, unison no grave, razões de FM, pitch-env de kick, distorção pré/pós-filtro sem experimento (04-SINTESE-SONORA, 30/10; MAPA §4).
62. Timbre dos packs orgânicos NÃO VERIFICADO — triagem auditiva pendente (AUDITORIA-PACKS, 29/10); leitura de presets foi de estrutura, sem escuta (PRESETS-SERUM, 25/10).
