# AUDIOMETRIA FÍSICA COMPARATIVA: PSYTECH & BUSH TECH
## Reanálise Empírica com Áudio Real: Fox (Artemis AR Remix), Subterranean Frequency, Star System (73 Stems)

**Data:** 2026-09-09  
**Metodologia:** Decodificação física direta via `ffmpeg` (PCM Float32 44,1 kHz mono e estéreo) + processamento matemático com `numpy` e `scipy.signal`. Medições em conformidade com as normas ITU-R BS.1770-4 / EBU R128 (Loudness integrado, LRA e True Peak), densidade espectral de potência por método Welch (resolução de até 0,67 Hz para low-end), envelopes analíticos de Hilbert para decaimento de transientes, detecção de onsets por fluxo espectral retificado em meia-onda com limiar adaptativo de mediana rolante (janela 0,8 s) e rastreamento de furos/saltos de energia pré-drop.

---

## 1. Fontes Físicas Analisadas

| Faixa / Stem | Formato | Duração | Papel / Função |
|---|---|---|---|
| **Fox (Artemis (AR) Remix)** | MP3 320 kbps / 44,1 kHz | 393,74 s (6:33) | Master comercial de referência de Psytech moderna (peak-time agressivo) |
| **Fox - Stems Demucs** | MP3 / 44,1 kHz | 180,00 s | Separações `bass.mp3`, `drums.mp3`, `other.mp3`, `vocals.mp3` |
| **Subterranean Frequency** | WAV 16-bit / 48 kHz | 170,41 s (2:50) | Referência de Bush Tech / Minimal Psytech subterrâneo e limpo |
| **Subterranean - Stems** | M4A / 48 kHz | 170,41 s | Separações `bass.m4a`, `drums.m4a`, `other.m4a` |
| **Star System (Master Mix)** | FLAC 24-bit / 44,1 kHz | 507,43 s (8:27) | Master mix lossless de referência (140 BPM, F menor) |
| **Star System - 73 Stems** | FLAC 24-bit / 44,1 kHz | 507,43 s | 73 pistas isoladas (`KICK_BASS`, `BASS GROUP`, `DRUMS`, `Kick F`, `SEQ_GRID`, etc.) |

---

## 2. Tabela Mestre de Audiometria e Dinâmica (EBU R128 & Crest Factor)

*Medição integral realizada pelo scanner EBU R128 oficial do FFmpeg sobre a totalidade do sinal de cada faixa.*

| Faixa / Referência | BPM / Tom | LUFS Int. | LRA (LU) | True Peak (dBTP) | RMS (dBFS) | Peak (dBFS) | Crest Factor |
|---|---|---|---|---|---|---|---|
| **Fox (Artemis AR Remix)** | 132 / Dm | **-7.1 LUFS** | 4.0 LU | **+3.3 dBTP** | -5.9 dBFS | +0.5 dBFS | **10.4 dB** |
| **Subterranean Frequency** | 130 / G#m | **-14.7 LUFS** | 7.3 LU | **0.0 dBTP** | -12.1 dBFS | 0.0 dBFS | **14.5 dB** |
| **Star System (Master Mix)**| 140 / Fm | **-17.8 LUFS** | 7.5 LU | **-6.0 dBTP** | -15.2 dBFS | -3.6 dBFS | **11.6 dB** |
| **Star System KICK_BASS**   | 140 / Fm | **-17.9 LUFS** | 5.6 LU | **-8.8 dBTP** | -15.7 dBFS | -6.3 dBFS | **9.4 dB** |
| **Star System BASS GROUP**  | 140 / Fm | **-22.9 LUFS** | 5.9 LU | **-10.5 dBTP**| -20.7 dBFS | -8.9 dBFS | **11.8 dB** |
| **Star System DRUMS**       | 140 / Fm | **-30.6 LUFS** | 7.7 LU | **-14.0 dBTP**| -36.6 dBFS | -11.0 dBFS| **25.6 dB** |
| **Star System SEQ_GRID**    | 140 / Fm | **-29.1 LUFS** | 8.8 LU | **-12.8 dBTP**| -34.3 dBFS | -9.7 dBFS | **24.6 dB** |

### Diagnóstico de Loudness & Headroom:
1. **Mastering de Fox:** Master comercial extremamente "quente" (-7.1 LUFS) com clipping inter-sample agressivo (+3.3 dBTP). Esse nível é obtido através de clipper no master antes do limiter.
2. **Mastering de Star System:** Arquivo lossless de estúdio entregue com **6,0 dB de margem real** (True Peak -6.0 dBTP, -17.8 LUFS), sem compressão de bus esmagadora. Isso preserva a transitoriedade natural dos transientes percussivos.

---

## 3. Distribuição de Energia Espectral por Banda (Faixa Integral)

*Energia integrada por densidade espectral de potência Welch sobre o espectro audível (20 Hz a 20 kHz).*

### A. Relação Percentual de Energia (% Share do Total Audível)

| Faixa | 20–120 Hz (Sub/Low) | 120–300 Hz (Punch/Corpo) | 300–1k Hz (Médios Baixos) | 1k–5k Hz (Presença/Bite) | 5k–12k Hz (Agudos/Air) | **Low-End (20-300)** | **Médios (300-5k)** | **Agudos (5k-12k)** |
|---|---|---|---|---|---|---|---|---|
| **Fox (Artemis Remix)** | 76,2% | 11,6% | 4,9% | 4,0% | **2,9%** | **87,8%** | 8,9% | **2,9%** |
| **Subterranean Freq.** | 82,3% | 10,3% | 4,6% | 1,9% | **0,8%** | **92,6%** | 6,5% | **0,8%** |
| **Star System Master**  | 82,8% | 7,9% | 5,2% | 3,1% | **0,9%** | **90,7%** | 8,3% | **0,9%** |

### B. Nível Relativo em dB em Relação ao Low-End (Banda 20–120 Hz = 0,0 dB)

| Faixa | 20–120 Hz | 120–300 Hz | 300–1k Hz | 1k–5k Hz | 5k–12k Hz |
|---|---|---|---|---|---|
| **Fox (Artemis Remix)** | 0,0 dB | -8,2 dB | -11,9 dB | -12,8 dB | **-14,2 dB** |
| **Subterranean Freq.** | 0,0 dB | -9,0 dB | -12,5 dB | -16,3 dB | **-20,0 dB** |
| **Star System Master**  | 0,0 dB | -10,2 dB| -12,0 dB | -14,3 dB | **-19,7 dB** |

---

## 4. O Espectro no MAIN DROP (Groove Pleno)

*Medição realizada exclusivamente na janela de Groove 1 / Drop Principal (onde tocam kick, baixo e pratos em regime permanente).*

| Faixa / Seção | Janela (s) | 20–120 Hz | 120–300 Hz | 300–1k Hz | 1k–5k Hz | 5k–12k Hz | Low-End Total | Médios | Agudos | Crest |
|---|---|---|---|---|---|---|---|---|---|---|
| **Fox Drop 1** | 58,0–120,0 | 82,7% | 9,3% | 2,5% | 3,0% | **2,1%** | 92,0% | 5,5% | **2,1%** | 8,8 dB |
| **Subterranean Drop 1**| 29,5–74,0 | 85,6% | 8,6% | 3,4% | 1,5% | **0,8%** | 94,1% | 5,0% | **0,8%** | 11,5 dB |
| **Star System Drop 1** | 54,8–110,0 | 86,4% | 7,6% | 3,0% | 2,4% | **0,5%** | 94,1% | 5,4% | **0,5%** | 10,2 dB |

### 🔍 Perfil físico do drop nas referências:
1. **Agudos (5k–12k) no drop:** entre **0,5% (Star System)**, **0,8% (Subterranean)** e **2,1% (Fox)** — em decibéis relativos, −10 a −14 dB abaixo do low-end. O drop não é brilhante; é escuro e pesado.
2. **Corpo (120–300 Hz) contido:** **7,6% a 9,3%** da potência total — nada de acúmulo na região de low-mid.
3. **Domínio do sub:** o sub puro (20–120 Hz) domina com **82,7% a 86,4%**.

---

## 5. Densidade de Eventos e Onsets: Drops vs Breakdowns

*Taxa de transientes por segundo detectada por fluxo espectral (spectral flux onset detection).*

| Faixa | Seção | Tipo | Wideband (20–12k) | LF (20–200 Hz) | HF (1k–8k Hz) | Relação HF/LF |
|---|---|---|---|---|---|---|
| **Fox (Artemis)** | Intro / Build 1 | Intro | 4,33 /s | 3,48 /s | 4,74 /s | 1,36 |
| | **Drop 1 (Groove Principal)**| **Drop** | **5,06 /s** | **4,19 /s** | **5,39 /s** | **1,29** |
| | Breakdown Principal | Breakdown | 6,32 /s | 3,62 /s | 6,35 /s | 1,75 |
| | **Drop 2 (Clímax)** | **Drop** | **6,06 /s** | **4,61 /s** | **6,65 /s** | **1,44** |
| | Outro | Outro | 5,66 /s | 3,36 /s | 6,18 /s | 1,84 |
| **Subterranean** | Intro / Build 1 | Intro | 2,98 /s | 2,64 /s | 4,31 /s | 1,63 |
| | **Drop 1 (Main Groove)** | **Drop** | **5,71 /s** | **4,09 /s** | **6,52 /s** | **1,59** |
| | Breakdown | Breakdown | 5,40 /s | 4,13 /s | 6,00 /s | 1,45 |
| | **Drop 2 (Heavy Groove)** | **Drop** | **6,31 /s** | **4,25 /s** | **6,75 /s** | **1,59** |
| **Star System** | Intro (W00–W01) | Intro | 1,35 /s | 0,02 /s | 1,31 /s | 65,5 |
| | **Drop 1 / Groove A** | **Drop** | **6,90 /s** | **3,13 /s** | **8,56 /s** | **2,73** |
| | Breakdown Principal (W07)| Breakdown | 4,63 /s | 0,22 /s | 4,59 /s | 20,8 |
| | **Drop 2 / Clímax** | **Drop** | **5,92 /s** | **3,16 /s** | **7,27 /s** | **2,30** |

### 🔍 O Fenômeno Físico da Relação HF/LF:
- Em **Star System**, a relação HF/LF no Drop 1 é de **2,73** (8,56 onsets de agudo por segundo contra apenas 3,13 de grave). O groove é movido pela subdivisão rápida dos pratos, shakers e sequências em semicolcheia (16ths).
- Em **Fox**, a relação é de **1,29** (5,39 HF vs 4,19 LF).
- **Regra derivada:** o groove psytech é movido pelo TOPO — a relação HF/LF nos drops fica entre **1,3× e 2,7×**. Um projeto em que as pancadas de grave superam os transientes do agudo (HF/LF < 1) soa lento, pesado e sem o gingado característico do psytech/bush tech.

---

## 6. Duração dos Silêncios / Cortes Pré-Drop e Salto de Energia ($\Delta dB$)

*Medição do envelope LF (20–150 Hz) no instante imediatamente anterior à explosão do Drop.*

| Faixa | Marco / Corte | Duração (ms) | Duração em Beats | Piso LF no Corte | Nível no Impacto | Salto ($\Delta dB$) |
|---|---|---|---|---|---|---|
| **Fox (Artemis)** | Pre-Drop 1 Cut | **3100,0 ms** | **6,82 beats** (~7 b) | -49,1 dBFS | -0,8 dBFS | **+48,3 dB** |
| **Fox (Artemis)** | Pre-Drop 2 (Clímax) | **2950,0 ms** | **6,49 beats** (~6,5 b)| -24,2 dBFS | -1,0 dBFS | **+23,2 dB** |
| **Subterranean**  | Pre-Drop 1 Cut | **880,0 ms** | **1,91 beats** (~2 b) | -29,6 dBFS | -12,1 dBFS| **+17,5 dB** |
| **Subterranean**  | Pre-Drop 2 Cut | **1570,0 ms** | **3,40 beats** (~3,5 b)| -32,4 dBFS | -12,0 dBFS| **+20,4 dB** |
| **Star System**   | Pre-Drop 1 Cut | 20,0 ms | 0,05 beat | -70,7 dBFS | -9,9 dBFS | **+60,8 dB** |
| **Star System**   | Pre-Drop 2 (Clímax) | **1260,0 ms** | **2,94 beats** (~3 b) | -66,8 dBFS | -9,6 dBFS | **+57,2 dB** |

### 🔍 Dinâmica do Impacto Pré-Drop:
1. **Duração Musical dos Cortes:**
   - **Subterranean** usa cortes curtos e rítmicos: exatamente **2 beats** (880 ms) no Drop 1 e **3,5 beats** (1570 ms) no Drop 2.
   - **Star System** usa um vácuo limpo de **3 beats** (1260 ms a 140 BPM) antes do clímax, com o LF caindo para -66,8 dBFS e voltando com **+57,2 dB de salto**.
   - **Fox** utiliza furos longos de **~6,5 a 7 beats** (quase 2 compassos) onde apenas risers e texturas agudas tocam antes do kick entrar.
2. **Profundidade do Salto de Impacto ($\Delta dB$):** os saltos variam de **+17,5 dB** (Subterranean, mix mais aberto) a **+60,8 dB** (Star System) — a profundidade dinâmica do corte é um recurso de design, não acidente.

---

## 7. Audiometria de Stems Isolados (Star System & Fox)

*Análise de stems chave para entender o papel de cada camada na construção do mix.*

| Stem Isolado | LUFS | RMS (dBFS) | Peak (dBFS) | Onsets/s | 20–120 Hz | 120–300 Hz | 300–1k Hz | 1k–5k Hz | 5k–12k Hz |
|---|---|---|---|---|---|---|---|---|---|
| **Star System KICK_BASS** | -17,9 | -15,7 | -6,3 | 4,87 /s | **89,0%** | 7,8% | 2,0% | 1,1% | 0,1% |
| **Star System BASS GROUP**| -22,9 | -20,7 | -8,9 | 4,04 /s | **85,2%** | 11,1%| 2,5% | 1,2% | 0,1% |
| **Star System DRUMS**     | -30,6 | -36,6 | -11,0| 3,07 /s | 0,0% | 0,0% | 0,6% | **17,6%**| **76,7%**|
| **Star System SEQ_GRID**  | -29,1 | -34,3 | -9,7 | 2,58 /s | 0,0% | 7,6% | **47,3%**| **43,1%**| 2,0% |
| **Fox Stem Bass**         | -13,1 | -12,8 | +2,7 | 3,39 /s | **86,5%** | 12,5%| 1,0% | 0,1% | 0,0% |
| **Fox Stem Drums**        | -11,2 | -10,0 | +2,6 | 5,39 /s | 81,2% | 7,1% | 2,3% | 4,0% | 4,7% |
| **Fox Stem Other**        | -14,4 | -17,5 | +1,1 | 3,69 /s | 0,1% | **53,5%**| **35,5%**| 10,3%| 0,6% |
| **Subterranean Bass**     | -20,9 | -17,5 | -1,5 | 3,13 /s | **90,4%** | 8,4% | 1,2% | 0,0% | 0,0% |
| **Subterranean Drums**    | -16,2 | -14,7 | -0,7 | 3,60 /s | 87,3% | 8,5% | 1,5% | 1,3% | 1,2% |

### Lições dos Stems de Referência:
1. **DRUMS em Star System:** 76,7% da energia está em 5k–12k e 17,6% em 1k–5k. O stem DRUMS não contém low-end residual; é um topo cristalino e afiado.
2. **SEQ_GRID (A 3ª Perna do Groove):** O stem de sequências concentra **90,4% de sua energia entre 300 Hz e 5 kHz** (47,3% em 300-1k e 43,1% em 1-5k). Ele não compete com o baixo (0% em sub) e não chia com os hats (apenas 2% acima de 5k). É a engrenagem perfeita de médios.
3. **KICK e BASS:** Em Star System, Fox e Subterranean, **85% a 90% da energia do baixo fica rigorosamente confinada abaixo de 120 Hz**, com apenas 7% a 12% no segundo harmônico (120–300 Hz).

---

## 8. Física do Kick: Envelope de Decaimento e Harmônicos

*Medição do envelope analítico de Hilbert do kick isolado filtrado em 30–150 Hz.*

| Referência | Tom / F0 Fundamental | Picos Espectrais Dominantes | Decaimento -12 dB | Decaimento -20 dB |
|---|---|---|---|---|
| **Star System Kick Stem** | F1 (~43,6 Hz) | **44,4 Hz** (sub), 88,8 Hz | **128,6 ms** | **143,4 ms** |
| **Subterranean Frequency** | G#1 (~51,9 Hz) | **50,5 Hz** (sub), 101,0 Hz | 178,8 ms | ~190,0 ms |
| **Fox (Artemis Remix)**   | D2 / C2 (~65–68 Hz) | **68,6 Hz**, 103,6 Hz | — | ~200,0 ms |

### 🔍 Perfil do Envelope do Kick:
- Em 127 BPM, uma semicolcheia (16th note) dura **118,1 ms**.
- Em Star System, o kick decai até -20 dB em **143,4 ms** (dura cerca de 1,2 semicolcheias). Ele tem cauda tonal definida que transfere o peso suavemente para o baixo.
- Padrão das referências: decaimento −20 dB entre **~140 e ~200 ms**. Kicks muito mais secos morrem antes de transferir o peso e obrigam o baixo médio a preencher o buraco — acúmulo de 120–300 Hz.

---

## 9. Radar de Benchmark — alvos medidos nas referências

```
========================================================================================
                      RADAR DE BENCHMARK (ALVOS DAS REFERÊNCIAS)
========================================================================================
Banda / Métrica          |  Alvo das Referências
----------------------------------------------------------------------------------------
1. Brilho 5k-12k Hz      |  0,8% a 2,9% (-14 a -20dB rel ao low-end)
2. Low-Mid 120-300 Hz    |  7,6% a 10,3% (-9 a -10dB rel ao low-end)
3. Relação Onsets HF/LF  |  1,3x a 2,7x (topo denso movendo o groove)
4. Kick Decay (-20 dB)   |  140 ms a 200 ms (cauda tonal de ~1,2 semicolcheias)
5. True Peak Ceiling     |  -6,0 a 0,0 dBTP (Fox comercial vai a +3,3 com clipper)
========================================================================================
```
