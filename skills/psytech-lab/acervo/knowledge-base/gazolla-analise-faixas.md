# André Gazolla — análise técnica de 2 faixas (gingado e estrutura de drops)

Data: 2026-09-08 · Método: ffmpeg (decode f32le 22050 Hz mono, primeiros 300 s) + numpy (STFT 1024 pts, hop 256 ≈ 11,6 ms). Energia por banda 20-120 / 120-300 / 300-1k / 1-5k / 5-12k Hz; onsets por fluxo espectral por banda; kick detectado por pico do envelope 30-120 Hz (máx. local > baseline+6 dB, ataque = cruzamento -6 dB); grid de batida por varredura de concentração circular (R) dos picos de kick; pausas do kick = envelope LF < baseline-7 dB por ≥ 0,3 s sem pico de kick no interior.

Faixas analisadas:

| # | Arquivo | Duração real | Janela analisada |
|---|---|---|---|
| 1 | `Andre Gazolla - Mayuri.mp3` | 385,5 s (320 kbps) | 0–300 s (78%) |
| 2 | `Andre Gazolla, Petrix - Breakdown [Intro Mix].mp3` | 390,3 s (~130 kbps) | 0–300 s (77%) |

**Premissa testada e refutada:** as faixas NÃO estão a 132 BPM.

- Mayuri: **127,0 BPM** (beat 472,5 ms, compasso 1,89 s). VERIFICADO: R do grid @127 = 0,733 vs R@132 = 0,039; IOI mediana do kick = 476 ms; 89% dos kicks dentro de ±40 ms do grid; drift 180–300 s = 127,05 BPM (estável).
- Breakdown: **123,0 BPM** (beat 487,7 ms, compasso 1,951 s). VERIFICADO: R@123 = 0,308 vs ≤0,049 em todos os outros BPM testados (124–140); drift 123,01 → 123,57 BPM (aceleração de +0,56 na janela — grid menos estável, R global 0,31).

Todos os mapas abaixo usam beats no BPM medido (1 beat = 472,5 ms em Mayuri; 487,7 ms em Breakdown).

---

## 1. Mapa temporal

### Mayuri (127 BPM) — t(s) / beat / compasso / evento

| t (s) | beat | compasso | Evento medido |
|---|---|---|---|
| 0–30,4 | 0–64 | 0–16 | Intro: pulso de grave 1× por compasso — furos de LF de 0,80 s espaçados exatamente 1,9 s (= 1 compasso de 1,89 s), 16 furos seguidos |
| 30,4–59,6 | 64–126 | 16–32 | **Kick sai** (0,0–0,2 kicks/s por 30 s). Topo denso: HF 8,2–8,3 onsets/s (máximo da faixa). 120-300 Hz sobe 27,6→31,9 dB: groove de percussão + bass sem kick |
| 59,6–60,5 | 126–128 | 31–32 | Furo de LF de 0,94 s com tudo caindo (1-5k −53 dB, 300-1k −23 dB vs baseline) |
| **60,5** | **128** | **32** | **Drop 1**: kick volta (2,1/s), salto +57 dB no envelope LF; topo continua denso (7,2–8,1 HF/s); bass 32,4 dB |
| 60,5–119 | 128–252 | 32–63 | 4×4 cheio (1,7–2,1 kicks/s) com percussão densa por cima (7,2–8,2 HF/s) |
| ~120 | ~254 | ~63–64 | **Kick sai de novo** (0,0–0,3 kicks/s por ~30 s); bass sobe para 34,1 dB (máx. até então); HF se mantém 6,1–8,1/s |
| 149,3–150,1 | 316–318 | 79 | Cut de 1,55 beat caindo no downbeat (posição no compasso = 0,06 beat), 300-1k −21 dB; retorno fraco (+3 dB) |
| 150,7–151,2 | 319–320 | 79–80 | Re-cut de 1,08 beat |
| **151,2** | **320** | **80** | **Drop 2**: +60 dB; daqui pra frente o topo seca (HF cai 8,1→4,5/s) e o grave sobe (34,2→35,3 dB) |
| 151,2–203 | 320–430 | 80–107 | 4×4 com menos topo (4,5 HF/s) e mais grave (35 dB) |
| 203,7–211,2 | 431–447 | 108–111 | **Build de 8 compassos com micro-cuts a cada ~2 compassos**: cut 0,84 beat @203,7 (retorno com roll de kick 3,5/s); cut 0,66 beat @207,6 (roll 3,5/s + riser 5-12k +23 dB/s dentro do furo); cut 1,13 beat @211,2 |
| **211,7** | **448** | **112** | **Drop principal**: +52 dB, kick 2,0/s, topo seco (1,7–2,3 HF/s nos primeiros 20 s) |
| 253,9–257,0 | 537–544 | 134–136 | **Cut triplo**: 253,9 cut 1,67 beat (+3 dB, só tira o grave); 255,9 cut 1,15 beat com riser 1-5k +24 dB/s; 256,6 cut 0,88 beat com colapso total (1-5k −129 dB/s → silêncio de ~0,4 s) |
| **257,0** | **544** | **136** | **Drop 3**: +61 dB |
| 271,5–272,2 | 574–576 | 144 | Cut de 1,5 beat, retorno +62 dB; topo re-anima (HF 3,4→6,5/s) |
| 286,1–287,3 | 605–608 | 152 | Cut de 2,51 beat (o mais longo da faixa), retorno +57 dB (último evento dentro da janela) |

VERIFICADO: todos os 7 pontos de estrutura (beats 64, 128, 320, 448, 544, 576, 608) caem em múltiplos de 32 beats (8 compassos) com erro ≤0,2 beat — estrutura quantizada em blocos de 8 compassos.

### Breakdown w/ Petrix (123 BPM) — t(s) / beat / compasso / evento

| t (s) | beat | compasso | Evento medido |
|---|---|---|---|
| 0–30 | 0–61 | 0–15 | Intro em nível baixo (120-300 Hz: 17–18 dB vs 30+ depois) com padrão de kick denso e sincopado: 2,9–3,5 eventos LF/s (≈1,7 por beat) e 10 furos de LF de 0,3–0,8 s espaçados de 1 a 2 compassos, com retorno de +8 a +47 dB |
| 30–60 | 61–123 | 15–31 | **Breakdown do título**: kick cai para 0,9–1,3/s, topo quase mudo (0,6–1,2 HF/s), 120-300 Hz sobe 30,7→36,2 dB — só grave e pouco mais |
| 60,5–60,9 | 124 | 31 | Furo de 0,4 s com **riser brutal: 5-12k +104,8 dB/s e 1-5k +30,4 dB/s** dentro do furo |
| **60,9** | **125** | 31 | **Drop 1**: +22 dB, kick retorna (2,1/s no bloco seguinte), HF dispara 4,7→7,8/s ao longo da seção (pico de percussão da faixa em 80–90 s) |
| 77,1–78,1 | 158–160 | 39–40 | **Cut de 1 compasso inteiro** (1,95 beat), retorno +24 dB |
| ~120 | ~246 | ~61–62 | Kick continua (1,7/s) mas o topo morre (1,1→0,3 HF/s) e o grave vai ao máximo até então (37,3→38,6 dB) — segunda seção de grave puro |
| 140–200 | 287–410 | 72–102 | Groove de volta (kick 1,8–2,3/s, HF 4,1–6,0/s) |
| 233,2–240,8 | 478–494 | 119–123 | **4 cortes em 7,6 s (a cada ~1 compasso)**: 233,2 (0,64 beat, posição 2,0 no compasso = beat 3), 236,2 (1,14 beat, com riser 1-5k +20,7 dB/s), 237,1 (1,12 beat, riser +18,8 dB/s), 240,5 (0,71 beat). Diferença chave vs Mayuri: estes cortes caem em beats 2–3 do compasso, não no downbeat |
| 250–280 | 513–574 | 128–143 | **Terceira seção de grave puro, a mais grave da faixa** (120-300 Hz 37,4–38,9 dB), kick 1,3/s, topo 0–1,2 HF/s |
| **280,6–281,0** | **575–576** | **143–144** | Cut de 0,74 beat, retorno +26 dB: kick volta (2,1/s) com topo (4,3–4,9 HF/s) |

INFERÊNCIA: a quantização de 8 compassos é clara nos extremos (beats 513 ≈ bar 128, 576 ≈ bar 144), mas os cortes do meio (beats 124, 158, 478) caem fora de múltiplos de 32 — consistente com o drift de +0,56 BPM e o R mais baixo do grid (0,31): a estrutura é menos "militar" que a de Mayuri.

---

## 2. O gingado (números)

Distribuição de onsets por 16 avos de beat (slot 0 = cabeça do beat; slot 4 = "e"; slot 8 = "&" contratempo; slot 12 = "a"):

| Camada | Maiores concentrações (% dos onsets) |
|---|---|
| **Mayuri kick** | slot 0: 44% + slot 15: 43,6% → 4×4 reto, sem fantasma no contratempo (só 11% dos kicks fora do grid) |
| **Mayuri hats (1-8k)** | slot 7: 25,3% + slot 15: 24,4% + slot 3: 12,6% + slot 11: 9,5% → **quase tudo acumulado JUSTO ANTES das linhas do grid** |
| **Mayuri 5-12k** | slot 7: 24,4% + slot 15: 21,9% + slot 3: 15,5% |
| **Breakdown kick** | slot 0: 24,9% + slot 15: 25,2%, mas com 5–6% espalhado em quase todos os slots → 48% dos eventos LF (294/606) FORA do grid |
| **Breakdown hats (1-8k)** | slot 15: 18,8% + slot 7: 15,5% + slot 6: 13,8% + slot 14: 13,8% |

Desvio medido vs grid perfeito (negativo = adiantado):

| Camada | Offbeat "&" (slot 8) | "e" (slot 4) | "a" (slot 12) |
|---|---|---|---|
| **Mayuri hats 1-8k** | **−13,3 ms** (IQR −19,4 a −7,3; n=456) | −4,4 ms (n=300) | −1,4 ms (n=279) |
| **Mayuri 5-12k** | **−13,8 ms** (IQR −20,0 a −8,0; n=441) | −5,3 ms | +1,0 ms |
| **Mayuri 300-1k** | −7,8 ms | −2,9 ms | −5,5 ms |
| Mayuri kick fora do grid | −0,6 ms (n=14) | **−17,2 ms** (n=16) | — |
| **Breakdown hats 1-8k** | **−12,7 ms** (IQR −21,0 a −3,9; n=208) | **−16,0 ms** (n=72) | −3,0 ms |
| **Breakdown 300-1k** | −11,6 ms | −14,6 ms | −10,1 ms |
| **Breakdown kick fora do grid** | +1,6 ms (n=45) | **+9,8 ms** (n=46) | −8,9 ms (n=31) |

Leitura do gingado (VERIFICADO nos números acima):

1. **O swing do Gazolla é ADIANTADO, não atrasado.** Os contratempos de hats brilho vêm 12–14 ms antes da linha em ambas as faixas (IQR consistente, centenas de eventos). É groove "empurrado" — a track corre pra frente em vez de arrastar.
2. **A antecipação é seletiva por subdivisão**: no "&" os hats adiantam ~13 ms; nos 16ths ("e"/"a") eles ficam quase mortos no grid (−1 a −5 ms em Mayuri). O resultado é um shuffle invertido: só o contratempo corre.
3. **No Breakdown há micro-groove entre kick e topo**: os kicks fora do grid atrasam +9,8 ms no "e" enquanto os hats adiantam −16,0 ms na mesma subdivisão — ~26 ms de estiramento entre grave e brilho que dá a sensação de "dobradiça".
4. **Mayuri é a faixa do kick cirúrgico; Breakdown é a faixa do LF sincopado.** Mayuri: 89% dos kicks no grid, 4×4 seco. Breakdown: 48% dos eventos LF fora do grid, espalhados nos 16ths (slots 4–13, picos de 11–13%) — kick fantasma/bassline dobrado contra o 4×4.

---

## 3. Anatomia das transições (4–8 compassos antes de cada drop)

Padrão medido, não há riser longo de 8 compassos em nenhuma das faixas. O que existe é **cut cirúrgico + furo curto + re-cut**, com estes recursos recorrentes:

1. **Micro-cuts de 0,6–1,7 beat** (0,3–0,8 s de furo de LF), espaçados ~2 compassos no build (Mayuri 203,7 / 207,6 / 211,2) ou a cada ~1 compasso (Breakdown 233–240: 4 cortes em 7,6 s).
2. **Roll de kick dentro/na saída do furo**: 3,5 kicks/s medidos nos 2 s após os cuts de 203,7 e 207,6 (vs 2,0–2,2/s do 4×4 normal) — o kick duplica momentaneamente antes do drop.
3. **Riser curto dentro do furo**, não antes dele: pentes 1-5k/5-12k subindo +18 a +105 dB/s em janelas de 0,3–0,5 s (Mayuri @207,6: 5-12k +23,3 dB/s; Mayuri @255,9: 1-5k +24,1 dB/s; Breakdown @60,5: 5-12k +104,8 dB/s; Breakdown @236,2/237,1: 1-5k +20,7/+18,8 dB/s).
4. **Cut duplo ou triplo antes do drop principal**: Mayuri @149,3+150,7 (dois cuts em 1,4 s, caindo o primeiro no downbeat exato, posição 0,06 do compasso) e @253,9+255,9+256,6 (triplo, terminando em silêncio quase absoluto — colapso de −129 dB/s em 1-5k e 0,4 s de furo).
5. **Retorno com salto medido de +22 a +62 dB no envelope LF** (drops principais de Mayuri: +57, +60, +52, +61, +62, +57 dB). O drop nunca "cresce": ele entra com degrau.
6. **Posição do cut no compasso**: Mayuri corta em downbeat ou quase (posições 0,06–3,3, majoritariamente 0–1); Breakdown corta de propósito em beats 2–3 do compasso nas transições de 233–240 (posições 2,0 / 0,1 / 2,1 / 1,0) — deslocamento rítmico que gera antecipação no ouvinte.

Casos-notáveis: cut de 1 compasso INTEIRO no Breakdown @77,1 (1,95 beat) e cut de 2,51 beat na Mayuri @286,1 — os dois maiores furos, ambos com retorno full (+24 / +57 dB).

---

## 4. A "história" — o que muda entre as metades (da janela de 300 s)

**Mayuri** — do topo para o grave:
- Kick: 1,16/s na 1ª metade → **1,99/s na 2ª** (+72%; a 1ª metade carrega intro e duas seções sem kick de 30 s cada).
- Topo: HF 7,16 → 4,29 onsets/s (−40%): a percussão densa do início seca depois do drop 2.
- Espectro: 120-300 Hz +2,5 dB (31,8→34,3), 300-1k +1,4 dB, 1-5k +4,0 dB (20,1→24,1), mas **5-12k −4,4 dB (16,6→12,2)** — a faixa perde ar e ganha corpo; o brilho restante vira transe, não percussionismo.
- Pausas do kick: 19 na 1ª metade vs 9 na 2ª — depois do bar 80 a track quase não respira fora dos cuts planejados.
- Arco: intro por pulsos (16c) → groove percussivo sem kick (16c) → drop 1 denso (32c) → seção grave sem kick (16c) → daí em diante é tudo low-end com cuts (drops nos bars 112, 136, 144, 152). No fim da janela o topo re-anima (HF 3,4→7,9/s entre 250–290 s) preparando o último trecho.

**Breakdown (w/ Petrix)** — a faixa afunda:
- Low-end: 20-120 Hz **30,9 → 37,6 dB (+6,7 dB)** da 1ª para a 2ª metade; topo estável (1-5k 28,4→28,0; 5-12k 27,7→27,8). Todo o desenvolvimento é no grave.
- Cada seção de "grave puro" é mais grave que a anterior (120-300 Hz: 30,7–36,2 → 37,3–38,6 → 37,4–38,9 dB nas seções de breakdown 1, 2 e 3).
- Pausas: 14 → 6. A 2ª metade flui contínua; os cortes se concentram na passagem 233–240 s.
- Arco: intro sincopada em nível baixo (15c) → breakdown de título só-grave (16c) → drop 1 com pico de percussão (HF 7,8/s @80–90 s) → grave puro 2 → groove → série de cuts → grave puro 3 (o mais fundo) → drop final no bar 144.

---

## 5. Síntese da assinatura (para reproduzir o estilo)

1. Grid em 123–127 BPM (não 132), kick 4×4 cirúrgico (89% no grid em Mayuri) OU dobleado com LF sincopado de 16ths (48% fora do grid em Breakdown).
2. Swing por antecipação: contratempos de hats 12–14 ms adiantados; 16ths no grid; no Breakdown, kick +10 ms atrás dos hats no "e" (~26 ms de estiramento grave-vs-topo).
3. Drops por degrau (+52 a +62 dB de salto LF medido), nunca por fade.
4. Pré-drop = 2–4 micro-cuts de 0,6–1,7 beat espaçados ~2 compassos, roll de kick na saída (3,5/s) e riser de prato curto DENTRO do furo (+20 a +105 dB/s em 0,3–0,5 s).
5. Recursos de assinatura: cut duplo/triplo com silêncio total de 0,4 s antes do drop; cut de 1 compasso inteiro; cortes fora do downbeat (beat 2–3) no Breakdown.
6. Estrutura quantizada a 8 compassos (todos os marcos da Mayuri em múltiplos de 32 beats, erro ≤0,3 beat).
7. Narrativa espectral: da percussão densa para o low-end — o topo seca e o grave cresce ao longo da track (+6,7 dB de 20-120 Hz no Breakdown; −4,4 dB de 5-12k na Mayuri).

## Verificação e limites

- VERIFICADO: todos os números acima saem da análise ffmpeg+numpy dos primeiros 300 s.
- NÃO VERIFICADO: trechos após 300 s (Mayuri tem 85,5 s e Breakdown 90,3 s não analisados — possíveis seções finais não mapeadas).
- Limitação registrada: pausas detectadas por baseline adaptativo de 3 s não capturam seções sem kick longas (>3 s) como "pausa" — elas aparecem no mapa via taxa de kick por bloco de 10 s (0,0–0,3/s), que é a evidência usada.
- BPM da premissa (132) testado e refutado: R(grid) = 0,039 (Mayuri) e 0,024 (Breakdown) @132 vs 0,733 e 0,308 nos BPM medidos.
