# PESQUISA NOTEBOOKLM — DINÂMICA, FX E ABERTURA

**Data:** 24/09/2026 · **Fontes:** cadernos **Building a PSYTECH Track** (69 fontes), **PME Experts** (297 fontes), **Generative Forest Psytrance Atmosphere Techniques** (20 fontes).
**Lacunas medidas no set de referência que a pesquisa ataca:** atividade 42% (refs 46–59%) · onsets 4,8/s (refs 8–9/s) · ar 5–12 kHz −27 dB (refs −14 a −17) · miolo "parado".

---

## 1. BUILDING A PSYTECH TRACK — ROTAÇÃO DO MIOLO E ABERTURA

### 1.1 Rotação por bloco (bar por bar)
| compassos | entra | sai / automação |
|---|---|---|
| 57–64 | Kick 48 Hz, Sub Bounce C#1, **voz grave tipo bark** (pan 10% L, bandpass 514 Hz c/ dip 480) | Auto Filter do kick abre 1,8 k → 12 kHz |
| 65–72 | **Cello Spiccato** (35% L) + **Kanun 32nds** (35% R, width 125–130%) em D | Voz bark recua −4 dB |
| 73–88 | **Voz de resposta rasgada** (35% R) | Redux2: sample rate **40 k → 8,8 k** e dry/wet **25% → 80%** entre 81 e 88 |
| 89–104 (Ato 1) | Violino solo **D5→C#5→G#4** | **Mute total de kick e sub** (−50 dB <120 Hz) |
| 105–120 (Ato 2) | Kick em meio-tempo acelerando p/ 4/4 no 113 + **Acid 303** (glide 35–40 ms) | Cutoff do 303: **450 Hz → 2,2 kHz** |
| 121–140 | Marcha 4/4 | mutes cirúrgicos de 2–4 tempos no topo a cada 4 compassos |
| 141–144 | Downlifter contínuo | 143: corte de open hat + sub offbeat; 144: corte do kick (beat 574) |

### 1.2 Transição sem riser (fronteiras 56/88/120/144/168)
1. **Sub Deprivation:** no baixo, HPF 48 dB/oct salta **30 Hz → 350 Hz** no tempo 3.1 (o ataque de médios fica, o peso some).
2. **Micro-silêncio:** Utility do grupo Drums+Bass → mute/`-inf` nas posições **4.3 e 4.4**, fade de 4 ms (evita pop).
3. **Sucção:** congelar o último transiente + Reverb 100% wet (cauda 3–4 s), inverter e posicionar crescendo no tempo 4, ápice no 1.1.1 seguinte + **In-Snare invertido em 4.4**.

### 1.3 Espectro-alvo do drop (Zenon)
`<70 Hz` mono rígido · `70–150` mono · `150–400` **escavado −13 dB** · `400–2,5k` **escavado −17 dB** · `>5–6k` **aerado −27 dBFS**.

### 1.4 Agudos — o que fazer
- **Open Hat:** HPF **380–420 Hz** (18 dB/oct), decay **140 ms**, fader **−18 a −22 dBFS**.
- **Shaker 16ths:** HPF **350 Hz**, velocity oscilante **65-80-115-75**.
- **BUSH SWING (chave da velocidade):** `Track Delay` de **+12 a +18 ms** em Open Hat, Closed Hat, Shaker e Wood Clicks. O kick fica em **0,00 ms**. Cria o arrasto temporal e a sensação de velocidade.
- **EAR TICKLERS:** Operator FM (Osc A sine modulado por Osc B square, ratio **3,5 ou 7,0**), attack 0, decay **28–35 ms**, sustain −inf, release 10 ms, HPF **2,8 kHz**, chance **45–65%**, Auto Pan sine 1/4 ou 1/8, **phase 180°**, amount **20–35%**. Alvo: **11,5 picos/s**.
- **Downer de exaustão pré-drop no 1.1.1:** HPF **200–220 Hz** (24 dB/oct), width **140%**, decay **280–350 ms**.

### 1.5 Call-and-response (as 3 regras)
1. **Proibido ataque na cabeça de tempo** (1.1.1, 2.1.1, 3.1.1, 4.1.1) — reservadas ao kick/fundação.
2. **Responder em 3.3, 3.4, 4.2 e 4.4.**
3. **Ducking do midbass:** −3 a −5 dB em **300–800 Hz** durante o ataque do solista/FX.

**Exemplo pronto (1 compasso):** chamada Duduk `C#4 (vel 112) → D4 (vel 118)`, gate 115 ms, nas 16avos 3 e 4 do tempo 1; resposta `D3 (vel 70) → C#3 (glide 35 ms, vel 118) → G#3 (vel 124)` em 3.3.4 / 3.4.2 / 3.4.4.

---

## 2. PME EXPERTS — RULE OF 32, DHARANA E MASTERING

### 2.1 Rotação por blocos (200 compassos)
- **1–16** Atmos + R · **17–32** R + Acid (S calado)
- **33–48** S + R · **49–64** Acid + R (S só respostas curtas)
- **65–80** R + S (Acid calado) · **81–96** Acid + R (S calado) · **97–112** S + Acid **sem kick/bass** · **113–128** R + Acid (kick cardíaco) · **129–144** S+R+Acid (micro-respostas a cada 4/8)
- **145–160** S (orquestra) · **161–168** Acid + S crescendo
- **169–184** **Tutti (S+R+Acid)** — o clímax monumental · **185–200** R + Atmos (desconstrução)

### 2.2 Dharana — automação em ondas (não rampa)
- LP cutoff oscilando **250 Hz ↔ 3,5–4,5 kHz** em ciclos de **8 ou 16 compassos**.
- HPF fixo **150–200 Hz** (12 dB/oct) nos FX.
- Volume: cama **−21 a −18 dB**, pico **−12 a −9 dB**.
- Reverb decay **1,8 → 4,5 s**; pre-delay **20–45 ms**; dry/wet **15% → 40%**.

### 2.3 Pré-Drop 2 (168 → 169) — 3 obrigatórios
1. **Vácuo de low-end:** mute de kick e sub em 168.3–168.4.
2. **Reverse throw** de cauda (orquestra/vocal) ou tonal sweep cobrindo 168.2–168.4.
3. **Stutter 1/16** filtrado ou 1 nota seca (Throat Bark/Ney) + **1/4 de silêncio absoluto** em 168.4.4.

### 2.4 Mastering (free download)
- Ceiling **−0,5 dBTP** (ou −1,0). · LUFS integrado **−8 a −9,5** no Drop 2.
- HPF 12 dB/oct em **20 Hz** no master. · Side abaixo de **120–150 Hz** cortado (sub 100% mono).
- Headroom pré-master **−3 a −6 dB**. · Exportar **WAV 24-bit/44,1 kHz** + **MP3 320**.

---

## 3. GENERATIVE FOREST — ATMOSFERA QUE NUNCA PARA

### 3.1 Camadas de atmosfera/FX
- **Fontes generativas:** Feedback Network → Operator → Vocoder (pitch tracking) → Limiter ceiling −20 dB; Granulator/Sampler com start/grain size aleatórios; **Beat Repeaters** em 1/16 com LFO no grid.
- **Frequência:** HPF **abaixo de 200 Hz** em TODA atmosfera/FX; high-cut suave em ~9 kHz antes das reverbs longas.
- **Estéreo:** `Note On Random Discrete`/LFO no pan de cada gatilho; o centro fica mono p/ kick e sub.
- **Nível:** bus de atmosfera/FX entre **−18 e −24 dB** + **sidechain pelo kick** (a atmosfera encolhe no batimento e expande nos intervalos).

### 3.2 Molho dub (Tetra Hydro)
- Stab offbeat após o 1º ou 3º kick (tempos 2 e 4).
- Delay: **1/8d** ou **1/16**; feedback **60–75%**; HP interno **300–400 Hz** + LP **4–6 kHz**.
- **Send throw** só nas pontas de frase/vãos, entre **−6 e −12 dB**; reverb 100% wet em série depois do delay, com sidechain na cauda.

### 3.3 Abrir o agudo sem estridente
- **OTT suave (20–40%)** em vez de EQ estático no topo.
- **Vocoder noise carrier + Enhance** ou **Erosion** para sizzle.
- **De-harsh:** entalhe cirúrgico em **2,5–4,5 kHz** ANTES de subir o topo.
- **High shelf a partir de 6–8 kHz: +3 a +6 dB** nos busses de percussão/FX/atmosfera.
- Alvo: sair de **−27** e chegar em **−14 a −17 dB**.

---

## 4. Fila de execução (aplicação das recomendações)
1. **AR:** shelf 6–8 kHz +3…+6 nos busses de percussão/FX/atmosfera + de-harsh 2,5–4,5 kHz no master.
2. **Bush Swing:** Track Delay +12…+18 ms nas hats/shaker/woodclicks.
3. **Open Hat:** HPF 380–420 Hz + decay 140 ms.
4. **Ear Ticklers:** camada FM 16th com chance e Auto Pan 180°.
5. **Dharana:** LFO de cutoff nos atmos (8/16 compassos).
6. **Sub Deprivation** nas fronteiras + os 3 cortes pré-Drop 2.
7. **Mastering:** ceiling −0,5 dBTP, HPF 20 Hz, mono <120 Hz, LUFS −8…−9,5.
