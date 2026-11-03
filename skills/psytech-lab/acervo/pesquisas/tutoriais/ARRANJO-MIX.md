# Arranjo e mix — tutoriais traduzidos

**Frente:** arranjo-mix · **mapas:** `TdNE8oEb2Lk` (Audioreakt, stock), `DeRUOw8T98Y` (SINEE, take ao vivo), `5XUULOEJ2tI` (HTP, curva de energia), `6x1_XZDcI8I` (HTP, camadas frase a frase) · **data do levantamento:** 27/10/2026.

Triagem contra as diretrizes do projeto de referência: 2 alinhados (`DeRUOw8T98Y`, `6x1_XZDcI8I`), 1 conflito (`TdNE8oEb2Lk`), 1 neutro condicionado a uma decisão estética em aberto (`5XUULOEJ2tI`). Nada daqui foi executado num projeto real.

## Use quando

Use quando for decidir a curva dos dois minutos, montar o take de arranjo, escolher o que entra e sai por cena, ou encaminhar o build final (8 compassos) e o drop sem riser e sem boost de volume. Não serve para sound design (patch, filtro, saturação): esses gestos ficam nas frentes de grave, meio, textura e groove.

## Regras

1. **Teto de premix** — a automação do arranjo só subtrai: o fader chega no máximo ao nível que o stem já tinha no premix, e o drop é o retorno a esse teto, nunca um ganho acima dele (`DeRUOw8T98Y` 00:05:36–00:06:24).
2. **Curva em degraus** — a energia sobe e desce por camadas discretas que entram e saem, enquanto kick, sub e baixo ficam no mesmo nível entre as cenas; o retorno ao nível 1 é o gesto hipnótico (`5XUULOEJ2tI` 00:00:59, 00:03:47).
3. **Mesma grade, outra fonte** — variação é trocar device ou sequência sobre o groove aprovado, com fade de 1–2 compassos na entrada; nada re-quantiza os offsets de microtiming do bolso de referência (`6x1_XZDcI8I` 00:09:07–00:09:33, 00:18:35).
4. **Contraste por subtração** — o impacto antes do drop se constrói tirando agudo e energia 1–2 compassos antes, não somando riser nem camada nova (`6x1` 00:16:43; `TdNE` 00:16:21).
5. **Um dono por função** — ordem drums → baixo → elementos e sidechain contra o kick (`TdNE`, seção Técnica; 00:28:18), com um único responsável por fronteira e menos camadas em vez de mais (`6x1` 00:22:25).

## Receitas traduzidas

| Tutorial (timestamp) | Gesto traduzido | Aplicação de referência | Cautela |
|---|---|---|---|
| `DeRUOw8T98Y` 00:05:36–00:06:24 | Utility `Output` no fim de cada stem com `Max` = 0 dB; o fader do grupo fica no valor do premix | os faders das oito camadas do motor de referência (do kick à atmosfera); o take cobre os compassos 1–64 | Só subtrai; nada acima do premix; sem controlador, desenhar a automação no Arrangement |
| `DeRUOw8T98Y` 00:06:42–00:07:00 | Mute da bateria como botão de ausência; o mute do grupo de graves é adaptação do projeto de referência, não do vídeo | ausência de kick com sub vivo a meio do arranjo de referência; retirada opcional nos 2 compassos antes do drop | Conferir a composição real dos grupos no projeto de destino antes de mapear; preservar os offsets do bolso de referência |
| `DeRUOw8T98Y` 00:06:25–00:06:34 | Lowpass na madeira: fechado no compasso 32, abre em 8 compassos, aberto no timbre do premix | compassos 32–40 | Não deixar meio-fechado como timbre; ressonância só com notch estreito |
| `5XUULOEJ2tI` 00:00:46–00:04:05 | Escada L1→L4 por camadas; grave, drone e toms ficam "fairly at the same level" | cenas 1–16, 17–32, 33–48 do arranjo de referência; pico só até o compasso 56 | Camada de hats contínua condicionada a decisão estética em aberto; o reset não pode ocupar o drop |
| `TdNE8oEb2Lk` 00:05:42–00:05:54 | Preencher o terceiro 16º com SFX/stab, não com peça de bateria | buracos de resposta, 0:15–1:30 | Não acrescentar evento de bateria; um dono por buraco |
| `TdNE8oEb2Lk` 00:14:56–00:19:53 | Build de 8 compassos: kick reintroduzido com low-cut só no trecho, filtro abrindo, stop, lead sozinho e silêncio, resample-reverse e corte do último kick | aterrissando no drop | Low-cut não vai no kick inteiro; sem riser tonal; HP em todo retorno |
| `TdNE8oEb2Lk` 00:18:10–00:18:55 | Drop sem lead, com o baixo voltando do nível de retirada ao teto e rolling forte | no drop | O topo é o teto do premix, não boost; true peak sob controle no export |
| `6x1_XZDcI8I` 00:09:07–00:09:33 | Entrada de camada com curva de volume de 1–2 compassos, em vez de nota "no tempo" | entradas de madeira, resposta e stab | O fade não desloca ataque existente; uma entrada por fronteira |
| `6x1_XZDcI8I` 00:13:45, 00:18:35 | Trocar o device na mesma sequência e abaixar a camada antiga quando a nova já carrega o movimento | viradas de frase (c17, c33, c49) | Manter os offsets do bolso de referência; uma variação de sequência por bloco |
| `6x1_XZDcI8I` 00:16:43–00:16:45 | Tirar o agudo (mute/HP em hats e percussão) 1–2 compassos antes do drop | os 2 compassos anteriores ao drop | Não estender o corte; não é riser |
| `TdNE8oEb2Lk` 00:25:51–00:30:54 | Ordem de mix drums → baixo → elementos, sidechain contra o kick, Utility para automação de volume | premix e revisão de mix | Não copiar o corte global de 200–500 Hz nem o boost de 3 kHz do master |

## Conflitos e cautelas

| Tutorial | O que o vídeo faz | Como adaptar |
|---|---|---|
| `TdNE8oEb2Lk` 00:16:06 — riser no build | Riser tonal é o gesto que o projeto de referência aposentou | Não copiar o riser tonal; usar reverse tail do próprio elemento ou sucção + gota; se mantiver sweep, 1–2 compassos, ruído filtrado, sem pitch tonal |
| `TdNE8oEb2Lk` 00:10:14, 00:22:12 — washout no mix inteiro | Cauda mantém o impacto "presente" antes do drop | Send a zero no downbeat; cauda só em return dedicado; provar a extinção antes do drop; rumble/washout mudo nos respiros escritos do arranjo de referência |
| `TdNE8oEb2Lk` 00:33:41, 00:34:16, 00:34:35 — corte 200–500 Hz, boost 3 kHz, dois saturators + Color Limiter + limiter | Cadeia de master agressiva | Presença por elemento, não no master; nenhum corte global de 200–500 Hz; true peak sob controle no export |
| `5XUULOEJ2tI` 00:02:20 — 16 hats; reset em 1:45 | Depende de diretrizes em aberto no projeto de referência (topo contínuo × corte uníssono de 8 compassos) | A escada de grave é segura; a camada de hats fica condicionada à decisão; o reset em 1:45 colide com o drop — não transplantar sem resolver |
| `6x1_XZDcI8I` 00:11:50 — subida por cutoff + ruído | Subida que funciona como riser | Trocar a subida por reverse tail; manter o contraste por subtração de agudo |
| `6x1_XZDcI8I` 00:15:48 — ride 909 + Frequency Shifter | FM metálica é o timbre a eliminar no projeto de referência | Tempero curto, shift pequeno, wet baixo e LP depois; uma vez por frase; não é camada nem cama |
| `6x1_XZDcI8I` 00:07:30 — notas extras G, D#, D, G# | Notas fora da escala de referência (C# frígio) | Usar D/G#/A acima de ~200 Hz; D# e G ficam fora; uma dissonância por frase |
| `ORj8Vgu2vNs` — "drop no compasso 17" | O vídeo coloca o drop no compasso 17 | 0:30 numa grade de 128 BPM é o compasso 17, mas o drop depende do macro-arranjo de cada projeto; manter a arquitetura de loops curtos/longos e reescrever o encaixe |

**Duas decisões estéticas do projeto de referência seguem em aberto** (shaker/hats contínuos em 16avos; régua do médio). Este documento não as decide: a primeira condiciona a camada de hats da escada de energia; a segunda condiciona qualquer decisão de presença ou corte de médio.

## A/B

1. **Teto do take.** A: take/automação com todos os faders no topo. B: premix sem take. Critério: as bandas de sub e de corpo do grave do projeto de referência ficam idênticas ao premix dentro do erro de medição; correlação L/R unitária abaixo de 125 Hz; onsets `.27/.77` do bolso de referência na mesma posição. Se qualquer banda de grave subir, o mapeamento está acima do premix e o take volta para a mesa.
2. **Subtração vs. riser nos 2 compassos antes do drop.** A: mute/HP do topo 1–2 compassos antes. B: riser/sweep no mesmo trecho. Critério: medir as bandas de presença e de ar nas janelas 53–54, 55–56 e no downbeat do drop. A passa se o ataque do kick no beat 0.0 do drop permanece intacto e a banda de ar não sobe antes do drop; B é descartado se subir a banda de ar ou atrasar/suavizar o impacto. Escuta com volume casado; true peak sob controle no export.

## Evidência

Os mapas completos por vídeo (um por ID, com timestamps e trechos de prova) não acompanham este pacote; os IDs listados no cabeçalho identificam cada fonte. Proveniência: leitura de legenda, descrição ou ASR — em `5XUULOEJ2tI`, a legenda oficial falhou (HTTP 429) e o texto é ASR local: literal ao VTT, não ao áudio palavra por palavra.

## NÃO VERIFICADO / pendências

- **Nenhum áudio de vídeo foi escutado como fonte musical.** Os quatro mapas são leitura de legenda, descrição ou ASR.
- **Nenhum A/B foi executado e nenhum render foi feito nesta sessão.** As receitas são hipóteses de design até medição num projeto real.
- **Controlador MIDI não verificado.** `DeRUOw8T98Y` depende de um para o take único; sem ele, a automação desenhada preserva o teto, mas perde o gesto de um take.
- **Teto do premix não medido.** Os valores de teto citados no vídeo são dele e não se copiam; medir no projeto de destino.
- **`TdNE8oEb2Lk`:** o device "First Look at" (00:13:00) não é identificável na legenda; o fallback do Color Limiter é inferência.
- **`5XUULOEJ2tI`:** o quinto nível de energia não é nomeado na transcrição e não foi inventado. Onde o reset em 1:45 cabe (fim dos 2 min ou seção posterior) é decisão do produtor.
- **Decisões estéticas em aberto no projeto de referência** condicionam a camada de hats da escada de energia e a régua do médio (ver seção de conflitos).
