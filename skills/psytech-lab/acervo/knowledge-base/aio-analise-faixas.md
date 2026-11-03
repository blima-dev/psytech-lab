# AIO — análise técnica de 2 faixas (groove contínuo, synths e cornetas)

Data: 2026-09-08 · Método: ffmpeg (decode f32le 22050 Hz mono, primeiros 300 s, sem reprodução audível) + numpy (STFT 1024 pts, hop 256 ≈ 11,6 ms). Energia por banda 20-120 / 120-300 / 300-1k / 1-5k / 5-12k Hz; onsets por fluxo espectral por banda; kick por pico do envelope 30-120 Hz; grid por varredura de concentração circular (R). Extras desta análise: (a) rate10 de onsets por banda em janelas de 10 s; (b) detector de sweeps = ajuste linear da energia da banda em janelas deslizantes de 3-8 s (critério: slope ≥ +4 dB/s, subida líquida ≥ 10 dB, R² ≥ 0,60); (c) detector de janelas sustentadas (mediana da banda ≥ mediana da faixa +3 dB com < 1,2 onsets/s = nota segurada); (d) varredura de periodicidade de onsets em períodos P/2, 2P/3, P, 4P/3 e 2P.

Faixas analisadas:

| # | Arquivo | Duração real | Janela analisada |
|---|---|---|---|
| 1 | `AIO - Illusion.mp3` | 427,5 s (320 kbps) | 0–300 s (70%) |
| 2 | `aio - Shifting Reality.mp3` | 425,6 s (320 kbps) | 0–300 s (70%) |

NÃO ENCONTRADO: nenhuma outra faixa do AIO além destas duas na fonte analisada (pasta única com estes 2 arquivos; a duplicata em outra biblioteca é byte-idêntica da faixa 1 — mesmo tamanho 17.213.336 bytes, mesma duração 427,5 s).

**Premissa de referência (132 BPM) refutada: as faixas do AIO estão a 128,0 BPM.**

- Illusion: **128,0 BPM** (beat 468,8 ms, compasso 1,875 s). VERIFICADO: R do grid @128 = 0,916 vs R@132 = 0,021 (e ≤ 0,104 em todos os outros BPM testados); drift 127,98 → 128,03 BPM (estável); 92,3% dos kicks dentro de ±40 ms do grid.
- Shifting Reality: **128,0 BPM** (beat 468,7 ms). VERIFICADO: R @128 = 0,844 vs R@132 = 0,063; drift 128,01 → 128,06 (estável); 65,5% no grid — o restante é o baixo sincopado (ver §2).

Todos os mapas abaixo usam beats no BPM medido (1 beat = 468,8 ms; 1 compasso = 1,875 s; bar N = beat 4N).

---

## 1. Mapa temporal

### Illusion (128 BPM) — t(s) / beat / compasso / evento

| t (s) | beat | bar | Evento medido |
|---|---|---|---|
| 0–15 | 0–32 | 0–16 | Intro JÁ em 4×4 (kick 2,2/s desde o beat 1) mas com o topo escuro: 1-5k a 1,6–2,1 dB e 5-12k a 2,3 dB (vs 20–27 dB depois). Percussão rolando no escuro (onsets 5-12k já 4,4–6,4/s) |
| 15–25 | 32–53 | 16–28 | Filtro abre: 1-5k salta 2,1 → 22,7 dB e 5-12k 2,3 → 15,8 dB em ~10 s. HF onsets sobem para 8,4–8,6/s |
| 24–30 | 51–64 | 16 | Sweep de 6 s na banda 1-5k (+4,2 dB/s, +25,3 dB líquidos, R² 0,77) terminando EXATAMENTE no beat 64 (bar 16, erro 0,05 beat) |
| 30–95 | 64–203 | 16–50 | Groove contínuo: kick 2,1–2,2/s sem nenhuma parada; HF onsets 5,5–8,5/s; 300-1k sobe 22 → 35 dB gradualmente |
| 95–115 | 203–245 | 50–61 | **Clímax de synth**: 300-1k sobe 35,2 → 39,2 dB (máximo da faixa) e 1-5k 25,9 → 32,9 dB com onsets DESPENCANDO (4,2 → 2,4/s) — lead sustentado, não percussivo. Janela sustentada medida 114,8–120,8 s (1-5k, +5,5 dB acima da mediana, < 1,2 onsets/s) |
| 115–120 | 245–256 | 61–64 | Kick praticamente sai (0,4/s no bloco; 20-120 Hz cai 32 → 27 dB) — o lead toca sozinho. Resolução no beat 256 (bar 64) |
| 120–209,7 | 256–447 | 64–112 | **64 compassos de 4×4 contínuo** (kick 2,0–2,2/s, HF 4,4–8,3/s), ZERO pausas de kick detectadas em todo o trecho |
| 209,7–210,0 | 447,3–447,9 | 112 | Única pausa da 1ª metade: furo de 0,67 beat caindo no beat 448 = bar 112 (erro 0,07 beat), retorno fraco (+11,0 dB) |
| 210–233 | 448–497 | 112–124 | Groove retoma; sweep 5-12k de 6 s em 233,7–239,7 s (+5,0 dB/s, R² 0,82) |
| ~240–265 | ~512–565 | ~128–141 | **Vácuo filtrado pré-drop**: o low-end COLAPSA — mediana de 20-120 Hz cai de 40–42 dB para 2,5 / −6,2 / 0,8 dB nos blocos de 240–265 s (−40 dB) e o topo some junto (5-12k: 16 → −37 dB @240, reabrindo até 13,6 dB @270). O kick continua pulsando fraco (1,0–2,4/s) e os mids ficam por conta do synth: 300-1k 27,9–37,9 dB |
| 243,7–247,6 | 520–528 | 130–132 | Riser 1-5k +10,5 dB/s (+42,1 dB líquidos) terminando no beat 528 (bar 132) |
| 251,1–255,1 | 536–544 | 134–136 | Riser 1-5k +8,7 dB/s terminando no beat 544 (bar 136) |
| 258,1–264,1 | 551–563 | 138–141 | Riser longo de 6 s em 300-1k E 1-5k (+4,3 / +5,2 dB/s) |
| 261,0–261,7 | 557–558 | 139,5 | Pausa de 1,44 beat (barpos 0,69) FORA do grid de 16 bars, retorno +11,1 dB — única pausa fora de múltiplo de 16 bars |
| 265,1–270,1 | 566–576 | 141,5–144 | Riser final 1-5k +4,8 dB/s (R² 0,84) com pausa de 1,16 beat dentro dele (269,4–270,0) |
| **270,0** | **576** | **144** | **Drop principal: +50,2 dB de salto no envelope LF** (o maior da faixa) — o low-end volta inteiro (20-120: 0,8 → 40,2 dB num bloco) e o topo fica PRA FORA (HF onsets 7,8 → 2,2/s; drop de low-end) |
| 270–290 | 576–619 | 144–155 | 4×4 seco com mids altos (300-1k 36 dB) e topo mínimo (1,9–2,2 HF/s) |
| 287,6–299,6 | 613–639 | 153–160 | Pad de synth sustentado no fim da janela (1-5k +7,4 dB acima da mediana, 12 s contínuos, onsets < 1,2/s) |

VERIFICADO: pausas detectadas terminando em beats 447,9 (≈448), 558,2 (fora do grid) e 575,9 (≈576) — dois dos três marcos em múltiplos de 128 beats (32 bars) com erro ≤ 0,1 beat.

### Shifting Reality (128 BPM) — t(s) / beat / compasso / evento

| t (s) | beat | bar | Evento medido |
|---|---|---|---|
| 0–15 | 0–32 | 0–16 | Intro em 4×4 COM baixo sincopado desde o beat 1: eventos LF 3,3–3,4/s (kick 2,13/s do 4×4 + fantasma), 120-300 Hz a 16,5 onsets/s. Topo escuro (1-5k 6,3 dB, 5-12k 5,2 dB) |
| 15–25 | 32–53 | 16–28 | Filtro abre (1-5k 6,5 → 21,0 dB); kick+bass seguem 3,2–3,4/s |
| 26–30 | 55–64 | 14–16 | Sweep 300-1k de 4 s (+5,0 dB/s, R² 0,84) terminando no beat 64 (bar 16) |
| 30–95 | 64–203 | 16–50 | Groove contínuo kick+bass (2,8–3,5 LF/s), HF onsets 7,0–8,5/s, sem pausas |
| 95–115 | 203–245 | 50–61 | **Clímax de synth**: 300-1k 32 → 37,2 dB e 1-5k 26,6 → 32,2 dB com HF onsets caindo 8,4 → 0,4/s — lead sustentado sobre groove meio-time (kick 1,8–2,2/s). Janelas sustentadas medidas: 109,9–119,8 s (300-1k, +7,5 dB) e 111,9–115,9 s (1-5k, +9,6 dB) |
| 119,6–120,0 | 255,1–256,0 | 64 | **Pausa de 0,92 beat caindo EXATAMENTE no beat 256 (bar 64, erro 0,05 beat), retorno +32,4 dB** — entra groove cheio (kick 3,4–3,8/s nos blocos seguintes, pico da faixa) |
| 120–209 | 256–446 | 64–111 | Groove denso contínuo (LF 2,8–3,8/s, HF 7,1–8,5/s), sem pausas |
| 209,4–210,0 | 446,8–448,1 | 112 | Pausa de 1,24 beat no beat 448 = bar 112 (erro 0,07), retorno +12,2 dB |
| 230,7–233,7 | 492–499 | 123–125 | Sweep 300-1k +4,0 dB/s |
| 240–265 | 512–565 | 128–141 | **Vácuo filtrado pré-drop**: 5-12k desaba de 21,3 dB (@235) para 0,2 / −8,2 / −0,3 dB (240–265) — o topo some e SOBRAM percussão escura (HF onsets 9,4–11,8/s, as mais altas da janela) e mids oscilantes (300-1k 19,6–33,6 dB); low-end enfraquece (20-120: 40 → 4,8 dB @245, pulsos a 19,6–24 dB depois); kick cai para 1,2–2,8/s |
| 246,1–249,1 | 525–532 | 131–133 | **Riser triplo (300-1k +15,4 / 1-5k +15,2 / 5-12k +18,0 dB/s — o mais forte das duas faixas)** terminando na pausa do beat 528 |
| 246,9–247,5 | 527–528 | 132 | Pausa de 1,26 beat no beat 528 = bar 132 (erro 0,08), retorno +41,6 dB |
| 253,6–256,6 | 541–548 | 135–137 | Riser 1-5k +12,0 / 5-12k +14,2 dB/s → pausa 254,1–255,1 (beat 544 = bar 136, erro 0,31), retorno +24,9 dB |
| 261,1–264,1 | 557–564 | 139–141 | Riser 300-1k +15,5 / 1-5k +14,0 / 5-12k +14,7 dB/s → pausa 261,5–262,6 (beat 560 = bar 140, erro 0,23), retorno +35,1 dB |
| 268,6–271,6 | 573–579 | 143–145 | Riser 5-12k +10,0 dB/s → pausa 269,6–270,0 (0,89 beat, barpos 3,06) |
| **270,0** | **576** | **144** | **Drop principal: +39,7 dB de salto LF** — low-end volta (20-120: 16 → 38,8 dB) e o topo continua mudo (HF 6,4 → 0,2/s): drop de low-end como em Illusion |
| 270–295 | 576–630 | 144–159 | Outro de synth: kick 2,0–2,3/s, HF quase mudo (0,4–1,6/s), 300-1k 33,4–35,5 dB sustentado. Janelas sustentadas: 266,6–271,6 / 277,6–287,6 / 292,6–299,6 s (300-1k +4,0 a +6,8 dB); padrão rítmico de horn detectado em 276–284 s: onsets de 300-1k periódicos em 4P/3 (1 evento a cada 1⅓ beat = galopa pontuado, R 0,70+) |

VERIFICADO: as 6 pausas terminam em beats 256,05 / 448,07 / 528,08 / 544,31 / 560,23 / 576,04 — **todas as seis em múltiplos de 16 beats (4 bars) com erro ≤ 0,31 beat**: bars 64, 112, 132, 136, 140, 144. Os três cortes finais são exatamente espaçados de 4 compassos (132 → 136 → 140 → 144), cada um com riser multi-banda de +12 a +18 dB/s desaguando nele.

---

## 2. O gingado (números)

Distribuição de onsets por 16 avos de beat (slot 0 = cabeça; slot 4 = "e"; slot 8 = "&"; slot 12 = "a"):

| Camada | Maiores concentrações (% dos onsets) |
|---|---|
| **Illusion kick** | slot 0: 46,4% + slot 15: 45,7%; só 47/608 eventos (7,7%) fora do grid; NENHUM kick fraco (weak_n = 0) — 4×4 cirúrgico |
| **Illusion fantasma LF** | os 47 fora do grid concentram 42,6% no slot 6 (baixo antecipando o "&" em 1/16) |
| **Illusion HF (1-8k)** | slot 14: 27,8% + slot 6: 27,3% + slot 2: 11,3% + slot 10: 6,4% + slot 3: 8,7% + slot 7: 5,8% → rolagem de 16avos ocupando 2-3 / 6-7 / 10-11 / 14-15 |
| **Shifting kick+bass** | slot 15: 40,2% + slot 0: 25,2% + **slot 2: 24,0%**; 296/858 eventos LF (34,5%) FORA do grid, deles 69,6% no slot 2 = nota de baixo ~70 ms DEPOIS de cada kick (galope psy grave) |
| **Shifting HF (1-8k)** | slot 6: 19,7% + slot 14: 19,4% + slot 2: 14,1% + slot 3: 9,1% + slot 10: 9,9% + slot 11: 11,0% |

Desvio medido vs grid perfeito (negativo = adiantado; 1/16 = 29,3 ms @128):

| Camada | Offbeat "&" (slot 8) | "e" (slot 4) | "a" (slot 12) |
|---|---|---|---|
| **Illusion HF 1-8k** | **−26,8 ms** (IQR −28,2 a −25,1; n=95) | **−23,3 ms** (n=143) | **−22,2 ms** (n=121) |
| **Illusion 5-12k** | **−26,4 ms** (IQR −28,0 a −24,4; n=100) | −23,8 ms | −21,5 ms |
| **Illusion 300-1k** | −20,9 ms | −18,3 ms | −20,8 ms |
| **Shifting HF 1-8k** | **−21,4 ms** (IQR −26,5 a −14,3; n=150) | −22,4 ms (n=206) | −21,7 ms (n=227) |
| **Shifting 5-12k** | −23,3 ms | −23,0 ms | −21,4 ms |
| **Shifting kick fora do grid** | −16,4 ms (n=25) | **−26,5 ms** (n=23) | −12,2 ms (n=20) |

Leitura do gingado (VERIFICADO nos números acima):

1. **O swing do AIO é o dobro do do Gazolla e vale para TODAS as subdivisões**: contratempos e 16avos do topo vêm 21–27 ms adiantados com IQR apertado (±4 ms em Illusion) — não é humanização, é o padrão inteiro empurrado ~1/16 de beat (29,3 ms) contra a linha do grid. Gazolla adiantava só o "&" (−13 ms) e deixava os 16avos no grid.
2. **O topo do AIO é uma rolagem de 16avos contínua** (massa nos slots 2-3/6-7/10-11/14-15, "enchendo" a batida por trás) — por isso o HF onsets fica em 7–10/s mesmo nas seções calmas: é a esteira psicodélica que não para.
3. **Illusion = kick cirúrgico sem fantasma (7,7% fora, nenhum fraco). Shifting = kick dobleado com baixo**: um terço dos eventos LF cai 1/16 depois do kick (slot 2, 69,6%), o galope clássico de psy bass dobrando o 4×4 — daí os 2,8–3,8 eventos LF/s contra 2,0–2,2 de Illusion.
4. Os kicks fora do grid do Shifting adiantam −26,5 ms no "e" — o próprio grave participa do empurrão.

## 3. Como o AIO usa synths e cornetas (foco sound design)

**a. Onde 1-5k / 5-12k explodem vs onde é só groove (rate10 de onsets por banda, VERIFICADO):**

| Seção | 1-5k onsets/s | 5-12k onsets/s | 300-1k onsets/s | Leitura |
|---|---|---|---|---|
| Intro 0–20 s (ambas) | 6,7–8,6 | 4,4–8,6 | 7,2–11,5 | percussão rolando no escuro (dB baixo, onsets altos = filtro fechado) |
| Groove 30–95 s | 5,9–8,4 | 6,4–8,5 | 5,0–9,7 | groove cheio; pico de percussão em 30–45 s (Illusion 8,4–8,5/s) e 0–20 s (Shifting 8,5–8,6/s) |
| **Clímax 100–120 s** | **2,0–4,5** | **0,4–8,1** | **2,9–5,6** | onsets caem e o dB SOAR (300-1k até 39,2 dB em Illusion) = **synth lead sustentado** |
| Vácuo 240–265 s | 5,7–9,7 (Shifting) | 5,4–10,3 (Shifting) | 3,2–7,8 | percussão escura com 5-12k a −8 a 0 dB = topo filtrado |
| Pós-drop 270–290 s | 0,4–2,1 | 0,0–2,2 | 3,2–7,8 | topo fora de propósito — o drop é de low-end + mids |

**b. O lead sustentado (VERIFICADO pelo detector de janelas sustentadas):** em ambas as faixas o momento melódico principal acontece nos mesmos bars ~52–64 (t ≈ 100–120 s): a banda 300-1k atinge o máximo da faixa (39,2 dB Illusion / 37,2 dB Shifting) com onsets em queda — notas seguradas de synth, não stabs. Duração medida: 10–12 s contínuos (Illusion 114,8–120,8 s em 1-5k; Shifting 109,9–119,8 s em 300-1k). No fim da janela os dois repisam: pad sustentado de 12 s em Illusion (287,6–299,6 s) e três janelas de horn no outro de Shifting (266,6–299,6 s). INFERÊNCIA: o AIO constrói o "tema" como pad/lead longo de mids (300 Hz–5 kHz) e o usa como recompensa da seção, enquanto a percussão recua.

**c. Cornetas/sweeps psicodélicos (detector de subida linear, VERIFICADO — 20 sweeps em Illusion, 18 em Shifting):**

- **Risers gigantes multi-banda só existem na reta final (t 243–272 s = bars 130–144)**: em Shifting, três risers SIMULTÂNEOS em 300-1k + 1-5k + 5-12k a **+12 a +18 dB/s** (246,1–249,1 / 253,6–256,6 / 261,1–264,1 s), cada um terminando numa pausa; em Illusion, risers de 1-5k a +8,7 a +10,5 dB/s nos mesmos bars (243,7 / 251,1 / 258,1–264,1 / 265,1–270,1 s).
- **Sweeps de textura espalhados pelo resto**: mais curtos e suaves (+4 a +6 dB/s, 3–6 s) em 300-1k/1-5k: 24–30 s (ambas, terminando no bar 16), 54,9–65,4 s e 129,3–133,3 s (Illusion), 146,3–150,3 s (Shifting, R² 0,84). Taxa típica +4 a +6 dB/s — são texturas de 10–25 dB líquidos, não os canhões de +45 dB do final.
- **Padrão rítmico de alarme (periodicidade)**: o detector R≥0,72 em 2 beats não disparou em nenhuma faixa — a "corneta" do AIO NÃO é 1 evento por 2 beats. O que existe, medido: (i) pulso de 1-5k a cada ½ beat (P/2) por 72 s seguidos em Illusion (80–152 s) — o pluck/horn em offbeat de 8avos constante; (ii) horn de Shifting no outro (276–284 s) em padrão pontuado de 1 evento a cada 1⅓ beat (4P/3, R 0,70–0,75) — galope de corneta de 8 s; (iii) janelas pontuais em P (1/beat) nas seções de clímax.
- **O filtro é o instrumento**: o "vácuo" 240–265 s derruba 5-12k a −37 dB (Illusion @240–245) e 20-120 Hz a −6 dB, e tudo reabre em ~30 s junto com os risers — a psicodelia vem do movimento de filtro em massa, com o mid (300-1k) segurando 28–38 dB o tempo todo.

**d. Densidade LF por seção — o AIO NÃO dosa o baixo por pausas (VERIFICADO):** Illusion mantém 2,0–2,4 kicks/s em TODOS os blocos de 10 s exceto dois (115–120 s: 0,4–1,3/s no clímax do synth; 240–270 s: 1,0–2,4/s no vácuo filtrado, kick presente mas abafado). Shifting: 2,8–3,8 LF/s em todo o groove, caindo para 1,2–2,5 só no vácuo e no outro. A dinâmica vem de FILTRO e de camadas, não de furar o kick.

## 4. Anatomia das transições e pausas do kick

- **Quantidade (o contraste mais forte do projeto): Illusion tem 3 pausas e Shifting 6 nos primeiros 300 s** — contra 28 (Mayuri) e 20 (Breakdown) do Gazolla e 46 de um set de referência. A 1ª pausa só aparece em 209,7 s (Illusion, bar 112) e 119,6 s (Shifting, bar 64); até lá, ZERO furos de LF ≥ 0,3 s em 64–112 compassos contínuos.
- **Duração e forma**: pausas de 0,67–2,38 beat (média 1,09 em Illusion, 1,48 em Shifting), a maioria caindo em barpos 1,8–3,2 (final do compasso), retornos de +11 a +41,6 dB. Nenhum roll de kick dentro dos furos (kick_rolls = 0) — o furo é limpo, diferente dos micro-cuts com roll do Gazolla.
- **A reta final é uma cadeia de cortes a cada 4 bars**: Shifting corta nos bars 132 → 136 → 140 → 144 (pausas de 1,26 / 2,08 / 2,38 / 0,89 beat, cada uma precedida por riser multi-banda de +12 a +18 dB/s); Illusion faz a mesma caminhada com risers de 1-5k terminando nos mesmos bars (132/136/141/144) mas corta o kick só 2 vezes (261,0 e 269,4 s) — os risers rolam POR CIMA do groove filtrado.
- **O drop final cai no MESMO ponto nas duas faixas: beat 576 = bar 144 = t 270,0 s**, erro ≤ 0,1 beat, com o maior salto LF da faixa (+50,2 dB Illusion / +39,7 dB Shifting). VERIFICADO. HIPÓTESE: template estrutural de ~7 min com drop principal fixo no bar 144.
- **O drop é de low-end**: após o beat 576 o topo fica de fora de propósito (HF onsets 2,2 → 0,2/s), os mids seguem altos (300-1k 36 dB) e o grave volta inteiro. Nenhum dos dois drops "cresce": entram por degrau, igual ao Gazolla, mas com o topo entregue DEPOIS.

## 5. A "história" — o que muda entre as metades (janela de 300 s)

**Illusion** — do brilho para o meio:
- Kick: 2,08 → 1,97/s (estável; a 1ª metade não tem pausas, a 2ª concentra as 3).
- Topo: HF 5,9 → 5,11 onsets/s; **5-12k −4,4 dB (19,1 → 14,7)** e **300-1k +3,2 dB (29,1 → 32,3)** — mesma conversão brilho→corpo da Mayuri, mas dirigida pelo clímax de synth e pelo vácuo filtrado.
- 1-5k −1,0 dB; 20-120 −1,7 dB. Low-end quase constante a tela inteira.

**Shifting Reality** — do galope para o horn:
- Kick+bass: 2,98 → 2,74 LF/s; as 6 pausas: 1 na 1ª metade, 5 na 2ª.
- **1-5k +3,1 dB (22,5 → 25,6)** e 300-1k +1,7 dB — a faixa ganha MID (os horns do outro); 5-12k −1,4 dB.
- Arco: intro galopada no escuro (16 bars) → filtro abre (bar 16) → groove duplo kick+bass → clímax de lead sustentado nos bars 50–64 com pausa no bar 64 → groove denso → pausa bar 112 → vácuo filtrado com 3 cortes de 4 bars e risers triplos → drop de low-end no bar 144 → outro de horn pontuado (4P/3).

## 6. Síntese da assinatura do AIO (para reproduzir o estilo)

1. **128,0 BPM cravado, grid de ferro** (R 0,84–0,92; drift ≤ 0,05 BPM na janela) — kick 4×4 desde o beat 1, sem intro sem batida.
2. **Groove contínuo extremo: 3 pausas de kick em Illusion e 6 em Shifting em 300 s** (Gazolla 28/20; set de referência 46). A primeira pausa só chega no bar 64 (Shifting) ou 112 (Illusion) — dezenas de compassos de 4×4 sem um único furo.
3. **Dinâmica por FILTRO, não por pausa**: intro com o topo no escuro (1-5k a 2–6 dB) abrindo no bar 16; e o "vácuo filtrado" de bars ~128–141 antes do drop final (20-120 Hz a −40 dB, 5-12k a −37 dB, kick pulsando abafado) no lugar do breakdown com kick parado.
4. **Swing empurrado ~1/16 de beat (−21 a −27 ms) em TODAS as subdivisões do topo**, IQR de ±4–6 ms — a esteira de 16avos de hats/percussão corre atrás do grid (7–10 onsets/s) sem parar.
5. **Baixo em duas escolas na mesma dupla**: Illusion = 4×4 cirúrgico sem fantasma (7,7% fora do grid); Shifting = galope psy com nota de baixo 1/16 após cada kick (slot 2 = 69,6% dos eventos fora do grid, LF total 2,8–3,8/s).
6. **Synth lead = notas SUSTENTADAS de mid (300 Hz–5 kHz)** no clímax dos bars 50–64 (300-1k até 39,2 dB com onsets caindo), e não stabs rítmicos; reprise em pad no fim.
7. **Corneta/sweep**: texturas de +4 a +6 dB/s espalhadas (sempre terminando em bar múltiplo de 16) e, na reta final, risers-canhão multi-banda de +10 a +18 dB/s em cadeia de 4 bars (132/136/140/144); padrão rítmico de horn em galope pontuado (1 evento por 1⅓ beat) — a "corneta" do AIO é fraseado em mids + filtro, não alarme de 2 em 2 beats.
8. **Estrutura quantizada**: cortes em bars 64 / 112 / 132 / 136 / 140 / 144 (todos múltiplos de 4 bars, erro ≤ 0,31 beat) e **drop principal no beat 576 (bar 144) nas duas faixas**, com salto LF de +40 a +50 dB e topo entregue depois (drop de low-end).

## Verificação e limites

- VERIFICADO: todos os números saem da análise ffmpeg+numpy dos primeiros 300 s (script padrão + extensões; resultados crus e onsets salvos em JSON/NPZ).
- NÃO VERIFICADO: trechos após 300 s (sobram 127,5 s de Illusion e 125,6 s de Shifting — possíveis seções finais e o encerramento real do drop do bar 144 não mapeados).
- Limitação registrada: o detector de pausas usa baseline adaptativo de 3 s e subestima o "vácuo filtrado" de 240–265 s (o low-end some mas o kick abafado continua picando) — a evidência do vácuo são as medianas de 20-120 Hz por bloco de 5 s (2,5 / −6,2 / 0,8 dB), não a lista de pausas.
- Limitação registrada: sweeps detectados por ajuste linear de energia de banda em mix completo — um riser pode estar mascarado por bateria; os +4 a +6 dB/s das texturas são piso conservador.
- NÃO VERIFICADO: tonalidade (a faixa de referência em uso é C#m; nenhuma medição de pitch foi feita nesta análise).
- BPM da referência (132) testado e refutado para o AIO: R(grid) = 0,021 (Illusion) e 0,063 (Shifting) @132 vs 0,916 e 0,844 @128.
