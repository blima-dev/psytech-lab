# Regua: texturas e sound design (Serum · madeira organica · atmosferas · FX)

> Destilada do acervo limpo `plugins/psytech-lab/skills/psytech-lab/acervo/` + do mapa de conflitos.
> Regua descreve referencia externa ou teoria; contraste com o set do projeto aparece como **CASO** (§I). Conflito aberto no mapa → **EM DISPUTA** (§H).

## Fontes (15)

Acervo, base `acervo/`: `PSYTECH-LAB/04-SINTESE-SONORA-E-RECEITAS-POR-FUNCAO.md` · `pesquisas/tutoriais/TEXTURA-ATMOSFERA.md` · `pesquisas/Estudo Synth e Atmos e FX.md` · `pesquisas/ESTUDO-ARRANJO-FX-DESENHO-20261025.md` · `pesquisas/AUDITORIA-PACKS-ORGANICOS-20261029.md` · `pesquisas/cursos/PRESETS-SERUM-20261025.md` · `pesquisas/cursos/OMAR-MEHO-SOUND-DESIGN-20261025.md` · `knowledge-base/BASS_MONSTER_Supreme_Serum2_Processing.md`, `Leads_from_Forest_Dark_Serum2.md`, `FOREST_AMBIENCES_Aula_Completa.md`, `MODO_ALIEN_Dark_Psytrance_Serum2.md`, `KUNI-SOUND-MANUAL-DEFINITIVO.md`, `KUNI-SOUND-GUIAS-COMPLEMENTARES.md` · `genre-dna/psytech-dark-prog.md` (origem: biblioteca de conhecimento do projeto original, fora do pacote).
Mapa de conflitos: `MAPA-DE-LACUNAS-E-CONFLITOS-20261030.md` (arquivo completo fora do pacote).

## A. Arquitetura do sound design

1. Montar a cadeia como hibrido amostra+sintetizador: fonte humana/acustica → transformacao digital → retencao de vestigio fisico; prioridade maxima da cena.
2. Fazer o sound design ganhar escassez, parentesco e consequencia narrativa: madeira/voz/foley geram a materia, Serum/granular/FM/spectral a deformam, tails e atmosferas ocupam as bordas.
3. Toda camada nova substitui ou enriquece uma funcao existente, em vez de criar mais uma camada simultanea; troca, nao soma.
4. Reciclar o mesmo patch/material entre leads, plucks e pads para DNA coerente; resamplear o mesmo gesto organico por vias diferentes faz timbres "parentes".
5. Escolher um instrumento para conduzir e centralizar o resto em volta; padrao complexo pede os outros simples.
6. Partir de Serum 2 + Live 12 nativos, que cobrem wavetable, sample, granular, spectral, FM/PD/RM antes de comprar plugin novo.

## B. Serum 2

7. Seguir a economia por funcao medida no pack Drift (152 presets): baixo 2 camadas/2 FX · lead e pluck 3 camadas/5 FX · pad 2 camadas; mediana de rotas de modulacao 3 no baixo e 7 no lead.
8. Resolver o timbre dentro do patch: EQ interno em 105/152 presets do pack; o ajuste no DAW e fino, nao estrutural.
9. Usar phase distortion (`kPD_OSC`) como via de sujeira controlada: warp mais comum do pack, 28 de 152.
10. Envelope ENV1 de referencia do pack: attack 0,5 ms · decay 1,0 s · sustain 0,79 · release 76 ms · cutoff mediana 43,4/100.
11. Encorpar com distorcao identica antes e depois do filtro (soft clip ou tube); tipos diferentes afetam harmonicos distintos e estragam a fase.
12. Engordar com face shifting (Diffuser no filtro 2 em serie; splitter low/mid/high), mantendo o fluxo filtro 1 → filtro 2.
13. Adicionar bus paralelo de distorcao agressiva saindo do filtro 2 (overdrive + EQ + filtro pos) com macro no mix, sem plugin externo.
14. Desenhar MIDI dentro do clip do Serum (salva no preset; note expression para bends/glides); glide exige sustain no amp envelope.
15. Construir conversas de sintese com chains no Instrument Rack: troca de timbre a cada nota tocada (arpejador/nota antes do chain selector), ate 127 chains; automacao no gate deixa o resultado psicodelico.
16. Travar o warp handle para o timbre ficar consistente em vez de randomizar.
17. Fazer stab metalico com FM a partir de sine basica + Spectral Morph para extrair timbre "seco".

## C. Percussao organica de madeira

18. Distribuir o material organico por funcao: acento/resposta no espaco negativo (one-shots 0,2–1,0 s) · topo percussivo continuo (loops) · madeira melodica (marimba/woodwinds) · cama granular (texturas ~1,5 s por grao-fonte).
19. Reafinar material de pack para a tonica do projeto: marimba vem rotulada "121 BPM – Gmin" e os MIDI dos packs pedem conferencia de tonalidade.
20. Tratar percussao como direcao ritmica: microvariacao com LFO aleatorio no pan e no Auto Filter impede o som robotico.
21. Dosar a madeira como lado secundario; o valor do estilo mora no baixo/sub.
22. Tirar acentos dos one-shots de perc (Tulum Percs 120 · Essentials Shaker/Percussion/Stick Shots) e topo continuo dos loops de acoustic/subtle percussion.

## D. Atmosferas, granular e camas

23. Dar buracos a textura: cama entra e sai por secao, o silencio faz parte, e os acentos `.27/.77` ficam livres de hit.
24. Nascer a cama de fonte acustica (madeira, voz, campo): grao e fatia de sample, fonte escura vence filtro corretivo; granular aplica-se em cama/resposta acima do HP, nao no motor de grave.
25. Travar o pitch: `random_pitch` 0 no drone e ±2 st no maximo na textura; a variacao vem de posicao, comprimento de grao e pan.
26. Ajustar grao por funcao: drone 150–300 ms · resposta percussiva 60–120 ms · madeira 100–160 ms · cama lisa = grao longo + densidade alta.
27. Construir cama organica em 8 vozes/unissono com start point diferente por voz, loop fwd/back e filtro automatizado por secao.
28. Construir as 3–4 camadas como camadas de UMA cama (mesma fonte, offsets deslocados), nao pads independentes.
29. Manter cauda em return 100% wet alimentado por pulsos curtos de send, com kick/sub/baixo em send zero (diretriz provisoria do projeto de referencia).
30. Derivar atmosfera do proprio lead: Grain Delay → delay paralelo (dry 100% + wet com feedback, controle por volume) → Gated Stretch → Beat Repeat ~1/4 antes → triple LFO random smooth em macros; cauda de fundo em −5 a −8 dB.
31. Congelar e capturar cauda de reverb (freeze & capture) de elemento da propria track para criar pad/wash coerente.
32. Ancorar drone no intervalo de quinta justa da tonica: tensao estavel que puxa para a tonica.
33. Construir pad dark com ataque longo, ratios 1×/2×/3× sobre a tonica (0/+12/+19 st) e unison shimmer, com LP abrindo por secao em vez de estatico.
34. Engrossar o motivo/baixo com dobra filtrada: duplicar o clip, cortar todo o grave, LP ~5–6 kHz, Roar leve e nivel abaixo do original, sem criar ataque novo.
35. Partir de filtros de entrada por funcao: cama HP 250–300 · atmosfera/pad HP 180–300 · resposta granular HP ~276.

## E. FX e transicoes

36. Guardar o silencio total para 1–3 momentos por faixa, quase sempre no ultimo terco; nas demais fronteiras transformar (sweep/wash/riser) em vez de desligar.
37. Usar riser e downlifter em pares (sobe antes da fronteira, desce depois) e manter impact/roll raros: 0–0,3/min na familia.
38. Concentrar FX no ultimo terco da faixa, como faz a familia de referencias.
39. Fazer transicoes de material proprio: cauda de reverb/delay throw + Low-Pass fechando na cabeca de break; cabeca de drop com impact sub-grave + downlifter + micro-vacuo antes da pancada.
40. Marcar fronteira com succao: remover o 4º kick antes da transicao gera antecipacao fisica.
41. Montar build dobrando velocidade por ÷2 (1/4 → 1/8 → 1/16 → 1/32) com volume descendo e filtro fechando; a ilusao de drop maior vem do contraste.
42. Preparar drop com bridge de 2–4 compassos: crash com reverb+delay+sidechain entrando baixo, riser de ruido (Noise + band-pass ressonante + sweep + Auto Pan) e reverse crash/kick imediatamente antes.
43. Deixar o FX crescer de volume ao longo do tempo, que soa como saltar para fora.
44. Combinar tecnicas de transicao (tirar antes de entrar + fill + upbeat antecipado + silencio de 1–2 compassos + reverb grande na frente do drop); a combinacao e a versao profissional.
45. Fazer o "simmer" com ruido branco + band-pass de sweep descendente, carater de poeira/vapor.

## F. Espaco, largura e grave

46. Criar Side real acima de ~150–250 Hz com conteudo L/R genuinamente diferente (granular com posicoes independentes, delays/reverbs decorrelacionados, modulacao distinta por canal); pan e Utility manipulam largura existente, nao criam Side.
47. Manter mono ≤120 Hz: motor de grave focado, texturas nas bordas.
48. Usar o fader como profundidade: abaixar o nivel assenta o elemento mais fundo na mix.
49. Conferir a mistura em mono antes de abrir em estereo.

## G. Regua numerica do corpus de referencia (externa)

50. Medidas do corpus de referencias do genero (10 faixas dissecatas, sendo 1 a faixa do projeto; regua tecnica do estilo, nao standard da industria): 8 kHz+ −22,1 a −20,1 dB · "ar" −17,2 a −16,1 dB · centroide 266–287 · presenca ≈0,51 · correlacao media L/R 0,32–0,44 · densidade ≤6,99 picos/s.
51. Faixas operacionais de partida por familia: stab HP 120–180 Hz · glitch HP >150 Hz · voz HP 100–250 Hz conforme a fonte · atmos HP 120–300 Hz conforme a fonte · FX de transicao HP 150–250 Hz quando nao deve ocupar o motor de grave.

## H. EM DISPUTA

52. **EM DISPUTA: topo percussivo continuo.** Leitura A (canon): Pilar 3 pede topo percussivo continuo, regua provisoria citada na auditoria dos packs. Leitura B: G16/G17/G18 estao PROVISORIAS e nao substituem o Pilar 3 sem homologacao auditiva (§3.8 do mapa). Decide o ouvido do produtor.
53. **EM DISPUTA: HPF do drone em secoes abertas.** Leitura A: 90 Hz. Leitura B: 160 Hz. As fontes divergem; decisao no projeto de destino.
54. **EM DISPUTA: BPM/tom do transporte.** Leitura A (canon): 128 BPM + C# frigio. Leitura B (estado): arquivo atual em 130 BPM, tratado como estado e nao lei nova (§3.3 do mapa). Afeta reafinacao/estica de loops de pack (120/121 BPM) e MIDIs.
55. **EM DISPUTA: stems de IA (Demucs/M4A) como fonte.** Leitura A: separacao util como material. Leitura B: resultado e estimativa; leitura de instrumento isolado exige etiqueta `ESTIMATIVA` (§3.7 do mapa).

## I. Casos (contraste com o set do projeto, nao regua)

56. Bass do set construida como "lead do pack" (3 camadas/5 FX/8 rotas/release 0,20 s contra 2/2/3/0,076 s do pack): mais sobreposicao e cauda no grave; reducao a 2 camadas e teste proposto.
57. Render do projeto fora do corpus: 8 kHz+ −25,6 dB · ar −20,1 dB · centroide 217 · presenca 0,64 · correlacao 0,80 · densidade 7,57 picos/s; +3 dB de shelf nas fontes entregou so ~+0,8 dB em 8–16 kHz.
58. Gap de silencio do projeto = 1,33/min, 3–12× o maximo da familia; o corte total perdeu o valor dramatico.

## J. Limites declarados

59. Nenhum A/B da frente textura foi executado; os criterios sao protocolo, nao resultado.
60. Granulator 3/Max for Live nao verificados no ambiente; o gerador de presets nao escreve o SCAN/playhead do GranularOsc; `granular_reverse` e booleano; "Grain Size 226" e unidade do Live, nao ms; preset granular depende do WAV junto; LFOs nao travam fase entre renders.
61. Sintese sistematica pendente (SYN-01…SYN-10): fase fixa vs random, unison no grave, razoes de FM, pitch-env de kick, distorcao pre/pos-filtro sem experimento.
62. Timbre dos packs organicos NAO VERIFICADO (triagem auditiva pendente); a leitura de presets foi de estrutura, sem escuta.
