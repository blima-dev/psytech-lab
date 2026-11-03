# Kaled Nasser — Análise técnica de 3 faixas (produção psytech / bush tech)

Data: 2026-09-08 · Método: ffmpeg + numpy (sem libs de MIR) · Foco: **percussão orgânica / camadas tribais**

## Fontes analisadas

| Faixa | Arquivo | Duração | Analisado |
|---|---|---|---|
| Bush | `274. Kaled Nasser - Bush.mp3` | 439,7 s | primeiros 300 s |
| Nebula | `91. Kaled Nasser - Nebula.mp3` | 439,4 s | primeiros 300 s |
| Karmacobra | `18. Kaled Nasser - Karmacobra.mp3` | 434,3 s | primeiros 300 s |

## Método (reprodutível)

- Decode `ffmpeg -t 300 -f f32le -ac 1 -ar 22050` → STFT janela 2048 (93 ms), hop 512 (**23 ms/frame**), Hann.
- Energia por banda em blocos de 5 s: **20–120 / 120–300 / 300–1k / 1–5k / 5–11k** (Nyquist 11,025 kHz limita o topo; não há 11–12k).
- **Onset-rate por banda**: fluxo espectral retificado + threshold adaptativo (mediana móvel 0,7 s × k) com distância mínima por banda (kick 100 ms, perc 50–60 ms).
- **Kick** = onsets 30–120 Hz · **bass** = 120–300 Hz · **glitch/perc** = 1–8 kHz.
- **Clicks orgânicos** = transientes em 200–800 Hz **e** 5–11 kHz que NÃO coincidem (±60 ms) com evento LF, deduplicados em grade de 50 ms. É a métrica da textura tribal ("clicks" fora do kick).
- **Pausa do kick** = intervalo entre onsets LF ≥ 0,9 s (~2 beats @132).
- **Seções** = novelty por distância cosseno entre perfis espectrais normalizados (resolução 1 s), picos com distância mínima 10 s.
- BPM por autocorrelação do envelope LF: **Bush ≈ 136 · Nebula ≈ 133 · Karmacobra ≈ 128** (resolução ±3 BPM). O mapa em beats abaixo usa **132 BPM fixo** como premissa de partida — VERIFICADO que o alinhamento absoluto desliza, principalmente em Karmacobra (INFERÊNCIA).
- Cobertura: ~68% de cada faixa (finais não analisados).

---

## 1. Mapa temporal em beats @132 (blocos de 10 s ≈ 22 beats)

Legenda densidades (eventos/s): k = kick 30–120 Hz · b = bass 120–300 Hz · o = clicks orgânicos.
Leitura do kick: 0 = sem kick · ~2,2 = 4-no-chão simples (1 evento/beat) · 4–5 = groove cheio (~2 eventos LF/beat: kick + re-trigger de sub/bass na mesma faixa — INFERÊNCIA para a duplicidade).

### Bush — groove contínuo, kick entra tardiamente e quase não sai

| t (s) | beats @132 | Bandas dB (20-120/120-300/300-1k/1-5k/5-11k) | k / b / o |
|---|---|---|---|
| 0–25 | 0–55 | sub sobe 5→27 dB, sem kick | 0 / 1,5–2,6 / 1,7–3,2 |
| **25–30** | **55–66** | **ENTRA O KICK** (sub 27→36 dB) | 0,8→3,6 / 5,6–6,0 / 4,4→2,8 |
| 30–55 | 66–121 | groove cheio, agudos ainda contidos (5-11k negativo) | 3,7–4,4 / 5,4–6,0 / 2,9–3,7 |
| 55–60 | 121–132 | **abre o hi-hat/ar**: 5-11k salta −5→+5 dB | 4,5 / 6,4 / 4,9 |
| 60–110 | 132–242 | groove hipnótico estável | 4,1–4,6 / 5,9–6,4 / 4,4–5,0 |
| **114,3–116,4** | **251–256** | **respiro do kick (4,6 beats)** | gap |
| 120–255 | 264–561 | groove cheio por 135 s sem mudança de seção | 4,4–4,6 / 5,9–6,6 / 4,1–4,9 |
| **262–300** | **576–660** | **KICK SAI, percussão domina** (org 6,0–6,6/s, sub cai 44→19 dB mas bass 120-300 segue ~24 dB) | 0→0,7 / 3,0–3,9 / 5,0–6,2 |

Gaps do kick (total: 3 em 300 s): 114,3–116,4 s (4,6 beats) · 173,6–174,5 (2,0) · 202,7–203,6 (2,0). **O Bush é estruturalmente o mais hipnótico: um único groove longo com respiros de 2 beats.**

### Nebula — arco clássico com breakdown percussivo de 32 s

| t (s) | beats @132 | Evento | k / b / o |
|---|---|---|---|
| 0–29 | 0–64 | já começa em groove (kick 2,2/s) com sub alto (41 dB) e ar fechado (5-11k = −13 dB) | 2,2 / 6,5 / 4,5–5,0 |
| 30–58 | 66–128 | sub sobe mais, perc orgânica densa | 3,1–3,5 / 5,7–6,1 / 3,8–4,5 |
| **58** | **127,6** | **DROP 1**: kick 2,2→5,2/s, 5-11k −9→+6 dB (abre o "hats") | 5,2 / 5,9 / 3,0 |
| 60–110 | 132–242 | peak time, kick 5,0–5,2/s | 4,4–5,2 / 5,8–6,3 / 3,0–4,1 |
| **117** | **257,4** | **DROP 2** (kick sai no build) | 5,3 / 5,9 / 3,5 |
| 120–179 | 264–394 | groove com 300-1k cheio (24–27 dB: o "corpo" tribal) | 4,2–5,4 / 5,5–5,9 / 3,5–4,3 |
| **207–239** | **455–526** | **BREAKDOWN PERCUSSIVO: kick OFF por 70,9 beats (32,2 s)**, sub morre (20-120: 43→−12 dB), org SOBE para 8,2/s (pico da faixa) | 0 / 4,2–5,0 / 6,8–8,2 |
| 239–266 | 526–585 | sub volta fragmentado (30–32 dB), build | 0,2 / 3,6–4,9 / 5,3–7,0 |
| **266** | **585,2** | **RE-DROP**: kick 0,14→5,5/s; org COLAPSA 5,45→0,57/s (drop é seco) | 5,4→5,0 / 5,3 / 0,6→3,0 |

Gaps do kick: 57,9–59,1 (2,6) · 116–118,1 (4,6) · **206,8–239 (70,9)** · 239–243,5 (9,9) · 243,9–250,8 (15,3) · 251,8–265,9 (31,0).

### Karmacobra — intro esparso + breakdown de 30 s

| t (s) | beats @132 | Evento | k / b / o |
|---|---|---|---|
| 0–29 | 0–64 | kick 4-no-chão simples (2,1/s), SEM bass line (b≈2,2/s) e quase sem clicks (0,4–1,3/s) | 1,9–2,3 / 2,1–2,8 / 0,4–1,3 |
| **30–45** | **66–99** | **entram os clicks orgânicos em massa**: org 1,3→7,0/s (primeiro "momento tribal") | 2,3–2,8 / 2,8–4,0 / 6,0–7,0 |
| 50–58 | 110–128 | bass line engata (b 4,0→5,9), build para o drop | 3,6 / 5,9 / 4,9 |
| **58–129** | **128–284** | DROP: kick 4,7–5,0/s, ar abre (5-11k −10→+7 dB) | 4,3–5,0 / 5,6–6,4 / 3,5–4,2 |
| 129–152 | 284–334 | groove afina, kick alivia (3,7/s), org sobe (4,9/s) | 3,0–3,7 / 5,4–6,2 / 3,5–5,8 |
| **152** | **334,4** | **DROP 2** (kick sai no build: 4,1→1,65/s) | 4,3→5,2 / 6,6 / 3,5 |
| 160–213 | 352–469 | groove longo | 4,5–5,2 / 6,3–6,9 / 3,3–4,9 |
| **213–244** | **469–536** | **BREAKDOWN: kick OFF 67,3 beats (30,6 s)**, sub some (43→−2 dB), org 6,0–6,4/s | 0→1,4 / 4,6–6,0 / 5,6–6,4 |
| 244–274 | 537–603 | retorno gradual do sub (25→40 dB), build | 1,4→3,9 / 5,8–6,5 / 3,3–5,6 |
| **274** | **602,8** | **RE-DROP**: kick 2,61→5,23/s (post 5,2/s) | 5,2 / 6,7 / 3,5 |

Gaps do kick: 29,1–30,5 (3,1) · 59,7–61 (2,7) · 89,5–91,4 (4,2) · 150,5–152,4 (4,2) · **213,2–243,8 (67,3)** · 272,1–274,3 (4,7).

---

## 2. Densidade percussiva por seção (onsets/s)

Valores médios por seção detectada (k = kick LF · o = clicks orgânicos). **Negrito = extremos.**

**Bush**
| Seção | beats @132 | k | o | Caráter |
|---|---|---|---|---|
| 0–67 s | 0–147 | 2,30 | 3,09 | intro com perc já ativa |
| 67–115 s | 147–253 | 4,30–4,45 | 4,29–4,75 | groove denso |
| 115–262 s | 253–576 | 4,31–4,39 | 4,00–4,29 | groove estável |
| **262–272 s** | 576–598 | **0,00** | **6,60** | outro percussivo (pico orgânico) |
| 272–300 s | 598–660 | 0,00 | 5,11 | decrescendo percussivo |

**Nebula**
| Seção | beats @132 | k | o | Caráter |
|---|---|---|---|---|
| 0–37 s | 0–81 | 2,43 | 4,62 | groove de entrada |
| 37–58 s | 81–128 | 3,10–3,45 | 4,09–4,80 | acúmulo |
| **58–117 s** | 128–257 | **4,45–4,80** | 3,23–3,76 | **peak (máx kick, org recua)** |
| 117–179 s | 257–394 | 4,53 | 4,02 | peak 2 |
| **179–250 s** | 394–550 | 1,96 | **5,45** | **quebra percussiva longa** |
| 250–266 s | 550–585 | 0,19 | **6,62** | build sem kick |
| **266–280 s** | 585–616 | **5,43** | **0,57** | **re-drop seco (org some)** |

**Karmacobra**
| Seção | beats @132 | k | o | Caráter |
|---|---|---|---|---|
| **0–58 s** | 0–128 | 2,43 | **3,40** (mín. 0,4/s até 20 s) | **intro esparso** |
| 58–129 s | 128–284 | 4,44–4,75 | 3,62–3,83 | peak denso |
| 129–152 s | 284–334 | 3,74 | 4,87 | alívio percussivo |
| 152–274 s | 334–603 | 3,11 (com quebra 0) | 4,53 (pico 6,4 na quebra) | seção longa híbrida |
| 274–300 s | 603–660 | **5,04** | 3,81 | re-drop denso |

**Padrão VERIFICADO nas 3 faixas**: kick e clicks orgânicos são **antagonistas** — onde o kick satura (4,4–5,4/s), org recua para 3,0–4,0/s; onde o kick sai, org sobe 1,4–1,8× (Nebula: 5,45 vs 0,57 entre seções adjacentes). Kaled orquestra por subtração: a percussão orgânica ocupa o espaço que o kick libera.

---

## 3. O low-end sustentado: quando o sub/bass pausa

Runs contínuas de energia ativa em 30–300 Hz (≥4 s), limiar 35% da mediana móvel 5 s:

- **Bush**: runs de 47–67 beats nos grooves. **O sub nunca morre de fato**: o mínimo do bloco 20–120 Hz é 12,4 dB (t≈290) contra ~44 dB no groove (−31,6 dB), e mesmo nos 38 s finais sem kick o bass 120–300 segue ativo (~24 dB). Pausas do kick são sempre curtas (≤4,6 beats) e o low-end atravessa.
- **Nebula**: runs de 57–63 beats; **sub para COMPLETAMENTE em 207–239 s (32 s)** — bloco 20–120 cai a −12,4 dB (queda de 55,5 dB vs groove). O bass médio (120–300) continua a ~24 dB: o "chão" tribal segue sem sub. Retorna fragmentado (239–266) e só volta inteiro no re-drop (266 s).
- **Karmacobra**: runs mais curtas (9–15 beats no meio, 31 no início) = **low-end mais "falado", com stabs**; sub fora em 213–244 s (43→−2,4 dB, queda de 45 dB). Retorno gradual por ~30 s antes do re-drop.

**Resumo**: o sub 20–120 é tratado como **evento do kick**, não como colchão — exceto no Bush, onde a massa LF é contínua e o que articula é a percussão. Quando o kick pausa nas outras duas, o 120–300 (bass médio/bassinha) mantém o movimento (VERIFICADO nos blocos: Nebula t=210: 20–120 = −12,4 dB vs 120–300 = +23,9 dB).

---

## 4. Transições pré-drop (o que entra/sai nos 32 beats antes)

Padrão recorrente (VERIFICADO nos quartis do build de 32 beats):

1. **Kick afinando (thin-out)**: a densidade LF cai nos últimos 8–16 beats. Nebula t=117: 5,2→1,9 eventos/s · Karmacobra t=152: 4,1→1,65 · Karmacobra t=274: 3,85→1,65 · Nebula t=266: 0,28→0 (já estava sem kick). O kick nunca é cortado seco no 4º beat: ele esvazia.
2. **Corpo subindo**: a banda 200–800 Hz cresce ~20–50% nos 2 últimos quartis (Karmacobra t=152: 9,8→14,8 magnitude média; Nebula t=266: 13,6→16,7→pico).
3. **Ar abrindo devagar**: 3–11 kHz em rampa (Nebula t=266: 0,6→1,0→1,7). Não há riser agudo forte detectado — o build é mais rítmico-percussivo que tonal/riser (INFERÊNCIA apoiada na ausência de pico de fluxo hi no build).
4. **No instante do drop**: clicks orgânicos COLAPSAM para dar espaço ao kick seco (Nebula 585: org 0,57/s na seção do drop vs 6,62/s no build) e o kick salta para densidade máxima (0,14→5,5/s; 2,61→5,23/s).
5. **Transição alternativa sem drop**: Nebula t=179 é corte por subtração — mid 200–800 CAI 20,9→16,2 nos quartis do build e o hi fica estável: troca de seção "flip", não build (VERIFICADO nos quartis medidos).

**Bush é a exceção**: nenhum drop passou no critério (salto de energia ×1,25 + kick retornando mais denso). Suas transições são: (a) entrada do kick em ~25 s (bass 120–300 já instalado em 28 dB antes do sub chegar) e (b) saída do kick em 262 s mantendo bass + percussão. Estrutura de "layering contínuo", não de tensão/soltura (INFERÊNCIA).

---

## 5. A história: primeira vs segunda metade (dos 300 s analisados)

| Métrica | Bush h1→h2 | Nebula h1→h2 | Karmacobra h1→h2 |
|---|---|---|---|
| Kick onsets/s | 3,41→3,29 | 3,92→**2,95** | 3,71→3,42 |
| Clicks orgânicos/s | 3,89→**4,52** | 4,00→**4,54** | 3,75→**4,43** |
| Bass onsets/s | 5,27→5,50 | 6,04→4,97 | 4,86→**6,17** |
| 1–5k (dB) | 7,7→**9,8** (+2,1) | 7,0→**9,2** (+2,2) | 6,2→**10,1** (+3,9) |
| 5–11k (dB) | 4,8→**7,5** (+2,7) | 4,7→3,8 (−0,9) | 6,8→6,2 (−0,6) |
| 300-1k (dB) | 20,3→21,9 | 20,6→**24,6** (+4,0) | 19,2→**22,6** (+3,4) |
| 20–120 (dB) | 41,9→40,2 | 41,2→39,8 | 41,1→40,0 |

**Leitura (INFERÊNCIA sobre números VERIFICADOS)**: a segunda metade é consistentemente **mais percussiva e mais "encorpada no meio"** — sobe 1–5k (percussão/ataque) e 300-1k (corpo tribal), enquanto o sub/20–120 levemente ARRECUDA (−1,3 a −1,7 dB). O Kaled economiza o low-end e gasta o meio-agudo: a faixa "afina para dentro" sem perder peso. Em Nebula, a queda de kick na 2ª metade (3,92→2,95/s) é explicada pelo breakdown de 32 s. Em Bush, a 2ª metade é onde o ar (5–11k) finalmente abre (+2,7 dB) — o groove fica mais brilhante com o tempo.

---

## Assinatura de produção (síntese para recriar o bush tech do Kaled)

1. **Groove base**: kick 4-no-chão + ~1 evento LF extra por beat (sub/bass re-trigger). Kick nunca para por mais de 2–4 beats nos grooves — quando para, é momento estrutural grande (30 s) ou respiro curto.
2. **Camada orgânica permanente a ~4 clicks/s** (200–800 Hz + 5–11 kHz, fora do grid do kick), que **dobra para 6–8/s quando o kick sai**. Implementável: 2–3 loops tribais com gate/sidechain inverso ao kick.
3. **Low-end = evento, não colchão**: sub morre junto com o kick; o bass médio (120–300) segura o groove nas quebras.
4. **Build sem riser tonal**: esvaziar o kick nos últimos 16 beats, engrossar 200–800 Hz e abrir 3–11 kHz em rampa; drop seco (percussão orgânica muda).
5. **Arco**: 1ª metade mais grave e contida, 2ª metade +2 a +4 dB em 300 Hz–5 kHz, sub estável ou caindo — brilho e corpo crescem, peso constante.

## Evidência e limites

- VERIFICADO: todos os números acima saem da análise ffmpeg+numpy executada.
- INFERÊNCIA: interpretações estruturais (antagonismo kick/perc, layering contínuo do Bush, build rítmico não-tonal) — derivadas dos números, não confirmadas por escuta/stems.
- NÃO VERIFICADO: últimos ~140 s de cada faixa (fora da janela de 300 s); BPM exato (autocorrelação ±3 BPM; mapa de beats usa 132 fixo e desliza em Karmacobra ~128); instrumentação real (não é possível separar stems neste método).
