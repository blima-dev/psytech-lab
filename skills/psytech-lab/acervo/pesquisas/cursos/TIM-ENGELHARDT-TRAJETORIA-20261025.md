# TIM ENGELHARDT (PML) — a trajetória de construção de 3 faixas

> Fonte: Production Music Live — "Tim Engelhardt Production Pack - Melodic Techno" / `Templates/` (pack da Production Music Live)
> **97 `.als` no total: 3 projetos finalizados + 94 autosaves com timestamp** (03 a 10/10/2026).
> Os autosaves não são versões jogadas fora: são a **linha do tempo de como ele construiu** — o dado mais raro deste acervo.
> Método: leitura do XML dos `.als` (pistas, devices, notas, lanes). Nada foi ouvido.

---

## 1. O que existe

| Projeto | Autosaves | Período | Estado final |
|---|---|---|---|
| **Projekt A (Climb)** | 28 | 05/10 15:10 → 10/10 17:30 | 24 pistas · 1.546 notas · 208 compassos · 4 returns · 84 devices |
| **Projekt B (Ash)** | 38 | 03/10 10:13 → 10/10 17:33 | 32 pistas · 3.659 notas · 204 compassos · 4 returns · 88 devices |
| **Project C (Ivory)** | 31 | 06/10 17:38 → 10/10 17:42 | 26 pistas · 730 notas · 192 compassos · 3 returns · 78 devices |

BPM: A e C = **123**, B = **124**.
`VERIFICADO` — nome do arquivo contém o timestamp do autosave.

Também no pacote: **95 presets Diva `.h2p`**, 37 MIDI, 163 WAV.

---

## 2. A ordem de construção (o que os autosaves mostram)

### 2.1 Pista crua primeiro, grupo por último
Em **todos os três projetos**, as pistas nascem soltas e só viram grupo no fim:

| Projeto | DRUMS / BASS / MUSIC aparecem | LOW END aparece |
|---|---|---|
| B (Ash) | 03/10 13:38 (mesmo dia, ~3h depois do início) | **09/10 18:23** (6 dias depois, no penúltimo dia) |
| A (Climb) | 09/10 15:33 | **09/10 19:02** |
| C (Ivory) | 09/10 14:46 | **09/10 18:23** |

`INFERÊNCIA` — ele **não começa pela arquitetura**: começa empilhando pistas e só agrupa quando o material já existe. Um projeto que define os grupos antes de empilhar faz o oposto. Os dois métodos funcionam, mas o do Tim explica por que as sessões dele têm 24–32 pistas com nomes numéricos (`13-Diva`, `14-Diva`, `15-Diva`) — são tentativas versionadas, não camadas.

### 2.2 FX entra em conta-gotas
| Projeto | Devices no 1º save | Devices no final | Dias |
|---|---|---|---|
| C | 19 | 78 | 4 |
| A | 51 | 84 | 5 |
| B | 51 | 88 | 7 |

Crescimento típico: **+1 a +4 devices por save**. Nunca um "mutirão de mixagem" no fim — a mixagem é contemporânea à composição.
`VERIFICADO` — contagem por arquivo.

### 2.3 Notas sobem e depois descem
- B: 1.875 → **3.659** em 09/10 13:04 (o salto de +1.784 é a construção da segunda metade/drop).
- C: 331 → 473 → 708 → **380** → 436 → 497 → 804 → **851** → **730** (o último dia é **corte**: −121 notas).
- A: 1.786 → **1.972** no último autosave (09/10 22:29) — e o **arquivo final entregue tem 1.546**, ou seja, 22% menos que o pico. O entregue é mais enxuto que o último estado salvo.

`INFERÊNCIA` — o padrão é **encher e podar**. No C, o penúltimo dia tem 851 notas e o entregue tem 730: 14% do material foi removido. Isso é o oposto de "ir adicionando até o fim".

### 2.4 A sessão é de vários dias, com blocos de 3–5 h
Ex.: 03/10 10:13–13:59 (3h46) · 06/10 17:20–21:30 (4h10) · 09/10 12:43–22:30 (9h47 com pausas).
`VERIFICADO` pelos timestamps dos autosaves.

---

## 3. Arquitetura final: 3–4 sends, cada um com uma função

### 3.1 Os returns medidos

| Projeto | A | B | C | D |
|---|---|---|---|---|
| **A (Climb)** | `A-Hall` — Reverb **2,30 s** · pre 2,5 ms · shelf hi 4,5 kHz +0,70 · lo 141 Hz | `B-Drum Room` — Bright Room **0,71 s** · pre 5 ms · hi 16 kHz +1,0 · lo 717 Hz | `C-Longer Reverb` — **9,81 s** · lo 90 Hz | `D-Echo` — Echo **fb 0,131** · tempos 0,201 / 0,375 s (Sync OFF) |
| **B (Ash)** | `A-Medium Reverb` — **2,20 s** · pre 2,5 · hi 4,5 kHz | `B-Drums Room` — **1,04 s** · pre 8 ms · hi 3,3 kHz | `C-Echo` — **fb 0,655** · tempos 0,051 / 0,141 s | `D-Huge Reverb` — **11,24 s** · lo 82,6 Hz |
| **C (Ivory)** | `A-Hall` — Dark Hall **2,89 s** · pre 36,5 ms · hi 976 Hz +0,35 | `B-Drum Room` — Ambience **0,78 s** · pre 15 ms · hi 7,1 kHz +0,73 | `C-TripleDelay \| Reverb` — **4,33 s** · pre 2,5 · hi 4,5 kHz +0,70 | — |

`VERIFICADO` — DecayTime lido no `.als` (unidade do arquivo = ms → convertido para s).

**A assinatura é esta: três tamanhos de cauda convivendo.**
Curta (0,7–1,0 s) para bateria · média (2,2–2,9 s) para música · longa (9,8–11,2 s) para cauda/ambiente.
O Drift (tech house) usa **uma** reverb de 7 s como template. O Tim usa **três**, cada uma com um papel.

### 3.2 Quem manda em quem (sends por função)

Medido no Project C (valores em dB, só as pistas ativas):

| Família | Send principal | Faixa de nível |
|---|---|---|
| Kick, Toms, Percs, Hihats, Shaker, Clap | **B-Drum Room** | −23 a −36 dB |
| Rhodes, Pads, Diva, Lead, Seq, Background | **A-Hall** | −9,4 a −26,5 dB |
| Diva/Lead (cauda extra) | **C-Triple** | −12,2 a −19,0 dB |
| Nada | — | kick não vai em hall; baixo não vai em nada |

No Project B a lógica se repete com `D-Huge`: pads e noise vão em −4,4 a −20,3 dB, bateria em −25 a −35 dB.
`INFERÊNCIA` — o send não é "mais um efeito": é **roteamento funcional**. O kick só recebe sala curta; o pad só recebe cauda longa.

### 3.3 Grupos com compressor
Todos os grupos têm um compressor de bus:

| Projeto | LOW END | BASS | DRUMS | MUSIC |
|---|---|---|---|---|
| A | Eq8 → **Glue** | — | Saturator → Eq8 → **Parallel** → **Glue** | Excite → Eq8 → **Glue** |
| B | Eq8 → **Glue** | StereoGain → **Glue** | Saturator → Eq8 → **Glue → Glue** | **Glue** |
| C | Eq8 → **Glue** → Limiter | Saturator → **Glue** | rack `FINISH` | Eq8 → **Glue** |

`VERIFICADO`.
`INFERÊNCIA` — a mixagem dele é **por família**, não por pista: o grupo carrega o caráter (saturação + glue), a pista carrega o timbre.

### 3.4 Master: suave, ao contrário do Drift

| Projeto | Cadeia | Ajustes |
|---|---|---|
| A | Eq8 → **Glue** → Limiter | Glue thr −2,54 · ratio 1,0 · attack 3 · release 6 · makeup 0,79 · **Limiter ceiling −0,3 dB** |
| B | **Rack** (Eq8 → Glue → Glue) → Limiter | Glue 1: thr −28,6 · ratio 2 · attack 2 · release 3 · **DryWet 0,048 (paralelo 4,8%)** · Glue 2: thr −1,27 · ratio 1 · attack 3 · release 6 · Limiter −0,3 dB |
| C | Eq8 → **Glue** → Limiter | Glue thr −28,6 · ratio 2 · release 3 · **DryWet 0,079** · Limiter −0,3 dB |

Comparação: o Drift usa **compressor a 0,01 ms + Clipper + 2 limiters**. O Tim usa **um glue em paralelo (4,8–7,9% wet) + 1 limiter a −0,3 dB**.
`INFERÊNCIA` — são duas filosofias opostas: Drift prensa para loudness de pack; Tim preserva transiente e deixa a masterização final para fora.

### 3.5 Os faders são a mixagem
Project C: kick **−1,4 dB**, sub **0 dB**, baixo −4,2, leads −2,5 a −3,7, pads **−12,6 a −17,2**, percussão −7 a −12,4, hats −0,6 a −9,1.
`VERIFICADO`.
`INFERÊNCIA` — aqui o fader faz o trabalho que no Drift o `Mix Control` faz. Não copiar os dois métodos ao mesmo tempo.

---

## 4. Automação: varredura de parâmetro, não troca de estado

Total por projeto: **A 31 lanes · B 59 · C 51** (contra 5–26 no Drift).

O que é automatizado, em ordem de frequência:

| Alvo | Exemplos medidos |
|---|---|
| **Volume de pista** | A: 4–11 pts · B: 3–8 pts · C: 4–6 pts |
| **Send de pista** | A: `Perc II Send` **46 pts** · B: `27-PHAETON Send` **356 pts** · C: `Diva Send` 4 pts |
| **Macro/param de plugin** | C: `Seq/Diva` 38 + 21 + 18 + 15 + 12 + 3 pts · B: `2nd Layer/Diva` **240 pts** |
| **Cutoff de AutoFilter** | A: `String Section` **27 pts** · B: `Bass I` 11 · C: `Noise` |
| **`On` de device** | B: `Redux On` **106 pts** · `Overdrive On` **106** · `Amp On` **92** · `Delay On` **44** |
| **Casos extremos** | B: `NOISE TOOLS MacroControls.0` **4.758 pts** · `26-PHAETON Arp FreeRate` **1.025 pts** · `27-PHAETON Arp FreeRate` 677 pts |

`VERIFICADO` — contagem de eventos por lane.
`INFERÊNCIA` — 4.758 pontos de macro e 1.025 de rate de arp não são automação de arranjo: são **desenho de som** (LFOs e aleatoriedade desenhados à mão). O arranjo é feito de volume + send + cutoff.

---

## 5. O som: presets e MIDI

### 5.1 Os 95 presets de Diva

| Dimensão | Tim Engelhardt | Cercle Vol.4 (comparação) |
|---|---|---|
| Oscilador | **Digital 31** · TripleVCO 21 · DCO 18 · DualVCO 17 · Eco 8 | **TripleVCO 38** · DualVCO 28 · Eco 12 · DCO 12 · Digital 10 |
| Filtro | **Ladder 46 (48%)** · Multimode 24 · Uhbie 11 · Bite 9 · **Cascade 5** | **Cascade 42 (42%)** · Ladder 32 · Multimode 11 · Bite 10 · Uhbie 5 |
| HPF | **POST 37** · PRE 24 · BITE 19 | modelo 3: 32 · POST 28 · BITE 24 · PRE 16 |
| Voices (mediana) | 5 | 4 |
| Portamento (mediana) | **10** | **0** |
| VCF Freq / Res / KeyScl | 70,5 / 18 / **44** | 78,4 / 9 / **0** |
| Famílias | KEYS 25 · BASS 25 · LEAD 20 · PAD 20 · FX 5 | ARP, ATM, BASS, … |

`VERIFICADO` — parse dos `.h2p`.
`INFERÊNCIA` — o Tim é **Ladder + portamento + key tracking**: som analógico com glide e filtro que abre no agudo. O Cercle é **Cascade + sem glide + sem key tracking**: mais estático, mais Roland.

### 5.2 MIDI
37 arquivos, **1.183 notas**, PPQ 96.
- Mediana **23 notas/arquivo** (Drift 32 · Cercle 8)
- Centro: C, F, G, D (não tem uma tônica única)
- Intervalos: 0 (101), **+2 (100)**, +4 (70), +7 (68), +5 (64) → **escala maior/pentatônica**
- Velocity mediana 92

`INFERÊNCIA` — o vocabulário melódico do Tim é **grau conjunto e pentatônica maior**. O Drift é semitom e pedal; o Cercle é salto de 19 semitons (oitava + quarta). São três dialetos distintos; um dialeto frígio de 2–3 notas, comum em psytech, não é nenhum dos três.

---

## 6. O que aplicar

1. **Três reverbs de tamanhos diferentes, com função** — um set de psytech medido tinha **1** return de reverb (2,19 s) e 1 delay. O padrão do Tim é curta (0,7–1,0 s) + média (2,2–2,9 s) + longa (9,8–11,2 s). Custo: 2 returns novos.
2. **Roteamento por família** — kick/perc só na curta, elementos melódicos na média, pads/caudas na longa. Sets que mandam muitas pistas para a mesma cauda perdem essa função.
3. **Glue em paralelo no master (5–8% wet)** — antes de qualquer limiter, em vez do hábito comum de rodar Glue a 100% wet.
4. **Compressor de grupo em toda família** — 6 grupos, 6 compressores. Em muitos sets só parte dos grupos tem tratamento de bus.
5. **Podar no fim** — o projeto C removeu 14% das notas no último dia. O hábito comum é só adicionar.
6. **Portamento 10 + key tracking 44 nos leads** — é a assinatura do Tim e não é hábito comum em psytech. Testar em uma pista de lead.

## 7. O que NÃO copiar

- **Nomes numéricos de pista** (`13-Diva`, `14-Diva`) — é rascunho, não organização.
- **Começar sem grupos** — funciona para ele, mas em um projeto que organiza por família desde o início, começar sem grupos é retrabalho.
- **A cauda de 11,24 s** — em 128 BPM isso atravessa 4 compassos; só funciona com o roteamento por família. Copiar o número sem o roteamento vira lama.
- **4.758 pontos de automação de macro** — é desenho de som manual; em muitos fluxos, o equivalente é desenhar dentro do próprio synth (LFO/modulação no patch).

## 8. Limites

- Nada foi ouvido. Nenhum preset carregado.
- Os 94 autosaves foram lidos por estrutura (pistas, devices, notas, lanes), não por áudio.
- O `GlueCompressor` tem escala de attack/release própria; os valores 2/3/6 estão **crus**, sem conversão para ms.
- O rack `FINISH` (DRUMS do Project C) é um rack de rack — a leitura para no segundo nível.
