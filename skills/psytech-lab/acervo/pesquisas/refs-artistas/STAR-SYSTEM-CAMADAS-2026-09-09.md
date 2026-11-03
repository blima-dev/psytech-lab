# STAR SYSTEM 140 F — densidade de eventos por stem e tabela de camadas do psy progressivo

Data: 2026-09-09 · Método: adaptação de análise espectral anterior — ffmpeg decode f32le mono 22050 Hz + numpy (STFT 1024 pts, hop 256 ≈ 11,6 ms). Bandas 20-120 / 120-300 / 300-1k / 1-5k / 5-12k Hz; onsets por fluxo espectral com limiar adaptativo (mediana rolante 0,8 s × 2,5, piso 10% do p95); pausas = envelope LF 30-120 Hz < mediana 3 s − 7 dB por ≥ 0,3 s (merge gap < 0,15 s). Energia por banda = média RMS (10·log10 da média — a mediana subestimava stems esparsos como kick/hats). Janela de 16 compassos @140 BPM = 27,43 s; 13 janelas cobrindo 0–360 s.

Notas de leitura: `rate` = onsets banda-larga por segundo (densidade de transientes, NÃO nº de kicks). `bb` = energia média banda-larga em dB. `win` = janelas ativas de 13. Ativa = energia da janela ≤ 25 dB abaixo do pico do stem (com piso −60 dBFS) OU taxa ≥ 0,5/s. Stems `Freeze` com energia baixa mas taxa alta são camadas quietas reais (conferido via volumedetect/ffmpeg: ex. F0 mean −25 dB, PHASE −33 dB, DRUMS −40 dB — audíveis, não placeholder). F0/PHASE/OFFBEAT têm dom 20-120: são camadas de sub/groove LF, não leads.

## 1. Tabela por stem (73 stems, 0–360 s)

| # | Stem | rate /s | bb dB | 20-120 | 120-300 | 300-1k | 1-5k | 5-12k | dom | pausas | win | presença W00–W12 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|
| 1 | KICK_BASS | 6.88 | 37.4 | 36.9 | 26.3 | 20.5 | 17.8 | 5.8 | 20-120 | 8 | 12 | `0111111111111` |
| 2 | 2-01_Kick F [2023-05-30 105302] (Freeze) | 6.54 | 35.7 | 35.3 | 23.2 | 18.3 | 16.3 | 4.6 | 20-120 | 2 | 10 | `0011111011111` |
| 3 | BASS GROUP | 6.33 | 32.3 | 31.7 | 22.4 | 16.2 | 12.6 | 0.1 | 20-120 | 0 | 12 | `0111111111111` |
| 4 | STAR SYSTEM 140 F | 6.16 | 37.7 | 36.9 | 26.6 | 25.1 | 22.5 | 16.5 | 20-120 | 17 | 13 | `1111111111111` |
| 5 | 13-CHH_05 (Freeze) | 4.67 | 1.5 | -89.0 | -53.7 | -34.5 | -11.3 | 1.3 | 5-12k | 7 | 7 | `0001111001110` |
| 6 | DRUMS | 4.19 | 15.5 | -44.7 | -19.1 | -5.9 | 8.7 | 14.4 | 5-12k | 1 | 9 | `0011111011110` |
| 7 | F0 | 3.92 | 30.8 | 30.1 | 21.1 | 15.2 | 11.8 | -0.7 | 20-120 | 8 | 10 | `0011111011111` |
| 8 | SEQ_GRID | 3.48 | 19.7 | -8.3 | 8.1 | 17.1 | 15.2 | 1.2 | 300-1k | 64 | 8 | `0001111011110` |
| 9 | MELOS | 3.15 | 21.0 | -12.4 | 11.3 | 19.4 | 13.7 | 1.9 | 300-1k | 26 | 9 | `1100001111111` |
| 10 | PHASE | 2.93 | 22.7 | 22.1 | 13.1 | 5.0 | -0.4 | -13.0 | 20-120 | 0 | 10 | `0011111011111` |
| 11 | 16-21 (Freeze) | 2.67 | -0.3 | -99.2 | -78.8 | -51.6 | -17.0 | -0.4 | 5-12k | 0 | 4 | `0000011000110` |
| 12 | melo 1 | 2.02 | 12.3 | -62.8 | -10.5 | 11.2 | 5.7 | -22.2 | 300-1k | 19 | 3 | `1100000000001` |
| 13 | 17-22 (Freeze) | 2.01 | -1.5 | -50.2 | -29.9 | -24.6 | -10.6 | -2.1 | 5-12k | 15 | 3 | `0000001000110` |
| 14 | VOCAL | 1.66 | 17.7 | -49.6 | 6.2 | 15.9 | 12.0 | -7.1 | 300-1k | 37 | 8 | `0101010111110` |
| 15 | SYNTH | 1.53 | 12.3 | -26.8 | -0.7 | 10.5 | 6.6 | -4.4 | 300-1k | 14 | 12 | `0111111111111` |
| 16 | 34-140 - F- Top Driver (Freeze) (Freeze) (Freeze) | 1.42 | 0.6 | -42.9 | -10.5 | -3.6 | -2.3 | -15.3 | 1-5k | 0 | 2 | `0000000000110` |
| 17 | 12-APTS - 006 - Closed Hi-Hat  [2023-05-30 113240] (Freeze) (Freeze) | 1.26 | 10.0 | -55.2 | -41.7 | -37.6 | -6.0 | 9.9 | 5-12k | 0 | 8 | `0011111001110` |
| 18 | 66-BPI - Vox F 140Bpm (Freeze) (Freeze) (Freeze) | 1.17 | -1.7 | -66.4 | -14.0 | -4.4 | -5.7 | -23.1 | 300-1k | 0 | 3 | `0000000001110` |
| 19 | SNARE ROLL | 1.08 | 11.6 | -21.7 | -12.0 | 6.4 | 8.3 | 4.9 | 1-5k | 14 | 8 | `0001111101110` |
| 20 | TRANS-X | 0.99 | 15.7 | -21.5 | -5.7 | 10.0 | 12.3 | 10.1 | 1-5k | 34 | 12 | `0111111111111` |
| 21 | 28-FX _ Reborn _ Trippy Seq_138_F (Freeze) (Freeze) | 0.93 | 13.0 | -39.4 | -1.0 | 12.4 | 1.6 | -11.6 | 300-1k | 8 | 3 | `0000000001110` |
| 22 | 43-09_VOCS_F_140 (Freeze) (Freeze) (Freeze) (Freeze) | 0.92 | 7.7 | -70.5 | -28.6 | 4.8 | 4.4 | -15.3 | 300-1k | 16 | 3 | `0001000110000` |
| 23 | 15-OHH_03 (Freeze) | 0.83 | 11.7 | -47.2 | -18.9 | -7.8 | 6.3 | 10.2 | 5-12k | 0 | 5 | `0000111000110` |
| 24 | 33-33_Grids & Sequences_F#_140 (Freeze) (Freeze) | 0.78 | 11.1 | -35.7 | 3.2 | 6.9 | 7.4 | -5.3 | 1-5k | 33 | 3 | `0000111000000` |
| 25 | 61-BPI - Shifter F 140Bpm (Freeze) (Freeze) | 0.73 | 8.5 | -63.1 | -5.8 | 7.6 | 0.4 | -27.4 | 300-1k | 0 | 12 | `0111111111111` |
| 26 | melo 2 | 0.72 | 19.1 | -12.4 | 11.3 | 16.9 | 12.6 | -4.3 | 300-1k | 1 | 4 | `0000001111000` |
| 27 | 36-03_Grids & Sequences_F_140 (Freeze) (Freeze) (Freeze) | 0.68 | 11.9 | -45.3 | -6.1 | 8.2 | 9.3 | -6.0 | 1-5k | 17 | 2 | `0000000011000` |
| 28 | 42-06_VOCS_F (Freeze) (Freeze) | 0.63 | 9.6 | -55.6 | -8.8 | 8.0 | 4.3 | -18.8 | 300-1k | 12 | 3 | `0101000100000` |
| 29 | 14-APTS - 004 - Snare  (Freeze) | 0.62 | 8.9 | -86.8 | -37.3 | -10.4 | 4.4 | 6.9 | 5-12k | 0 | 8 | `0001111011110` |
| 30 | 32-20_Grids & Sequences_F_140 (Freeze) (Freeze) | 0.61 | 8.0 | -48.1 | -9.0 | 6.3 | 2.8 | -13.8 | 300-1k | 12 | 2 | `0001100000000` |
| 31 | melo 4 | 0.56 | 3.6 | -85.4 | -50.1 | -19.5 | 0.5 | 0.7 | 5-12k | 0 | 2 | `0000000000110` |
| 32 | OFFBEAT | 0.51 | 22.7 | 22.3 | 11.2 | 4.0 | -0.4 | -12.7 | 20-120 | 28 | 2 | `0000000011000` |
| 33 | 65-SFX _ Shark Attack_V2_142_F (Freeze) (Freeze) (Freeze) | 0.37 | -1.6 | -72.1 | -18.2 | -2.5 | -9.5 | -76.8 | 300-1k | 1 | 4 | `0000100000111` |
| 34 | 62-BPI - Acidmain F# 140Bpm (Freeze) (Freeze) | 0.35 | -1.1 | -64.2 | -5.3 | -4.6 | -8.7 | -20.3 | 300-1k | 0 | 4 | `0001111000000` |
| 35 | 35-29_Grids & Sequences_F_140 (Freeze) (Freeze) | 0.28 | 12.7 | -66.3 | -9.1 | 6.7 | 11.3 | -2.8 | 1-5k | 7 | 2 | `0000011000000` |
| 36 | 67-BPI - Zap F# 140Bpm (Freeze) | 0.24 | -2.4 | -43.3 | -13.0 | -4.9 | -7.3 | -18.3 | 300-1k | 0 | 1 | `0000000000001` |
| 37 | 44-06_VOCS_F#_140 (Freeze) (Freeze) (Freeze) | 0.22 | 2.9 | -65.1 | -15.2 | 1.2 | -2.3 | -22.7 | 300-1k | 4 | 1 | `0000010000000` |
| 38 | REVERSE | 0.21 | 16.8 | 16.4 | 6.2 | -6.0 | -29.7 | -60.3 | 20-120 | 0 | 8 | `0111110111000` |
| 39 | UPLIFTER 1-1 | 0.17 | 3.8 | -67.5 | -58.6 | 2.6 | -2.3 | -19.9 | 300-1k | 12 | 4 | `0000101010001` |
| 40 | 60-21_SYNTH_F_140 (Freeze) (Freeze) | 0.16 | 0.5 | -67.1 | -19.4 | -3.4 | -1.9 | -21.3 | 1-5k | 0 | 6 | `0111111000000` |
| 41 | GRID-1 | 0.14 | 9.0 | -26.0 | 0.3 | 7.4 | 1.6 | -19.1 | 300-1k | 0 | 3 | `0000110000010` |
| 42 | 57-08_SYNTH_F_140 (Freeze) (Freeze) | 0.13 | 1.9 | -56.1 | -19.4 | -5.2 | 0.9 | -20.9 | 1-5k | 0 | 1 | `0100000000000` |
| 43 | D# | 0.10 | 15.9 | 15.3 | 5.3 | -0.2 | -3.2 | -16.0 | 20-120 | 0 | 3 | `0000111000000` |
| 44 | F# | 0.10 | 15.2 | 14.5 | 5.3 | -0.5 | -3.9 | -16.5 | 20-120 | 0 | 3 | `0000111000000` |
| 45 | F1 | 0.07 | 12.1 | 10.9 | 4.5 | -1.4 | -6.2 | -19.0 | 20-120 | 0 | 2 | `0000000000110` |
| 46 | 37-BPI - Stabs F 140Bpm (Freeze) (Freeze) | 0.06 | 5.6 | -31.1 | 0.7 | 3.5 | -6.5 | -16.1 | 300-1k | 0 | 1 | `0000000001000` |
| 47 | A-Reverb | 0.06 | 3.4 | -45.8 | -8.7 | -0.0 | -0.1 | -11.2 | 300-1k | 19 | 11 | `0101111111111` |
| 48 | GRID | 0.06 | 7.4 | -38.6 | -7.7 | 7.0 | -5.9 | -37.2 | 300-1k | 0 | 3 | `0000011000010` |
| 49 | melo 3 | 0.05 | 14.2 | -65.8 | -26.4 | 14.2 | -6.5 | -38.4 | 300-1k | 8 | 3 | `0000000001110` |
| 50 | 41-VOCAL STAR SYSTEM | 0.04 | 2.2 | -57.3 | -5.2 | 0.9 | -10.1 | -17.7 | 300-1k | 0 | 0 | `0000000000000` |
| 51 | DOWN REVERSE | 0.04 | -6.0 | -39.7 | -16.6 | -8.2 | -11.7 | -19.5 | 300-1k | 0 | 1 | `0000000000010` |
| 52 | Diva | 0.04 | 0.8 | -8.4 | -3.1 | -3.5 | -9.5 | -22.8 | 120-300 | 0 | 2 | `0000000000110` |
| 53 | 19-pad 1 (Freeze) | 0.03 | 9.6 | -22.4 | 2.1 | 7.6 | 2.2 | -40.8 | 300-1k | 28 | 10 | `1100111101111` |
| 54 | 27-LASER (Freeze) | 0.03 | -10.0 | -99.9 | -99.8 | -33.7 | -14.7 | -11.8 | 5-12k | 0 | 1 | `0001000000000` |
| 55 | 40-VOX _ Another Planet_142 (Freeze) | 0.03 | 1.8 | -62.1 | -5.9 | -0.1 | -6.4 | -13.4 | 300-1k | 1 | 2 | `0000000000110` |
| 56 | 51-02_Crash (Freeze) | 0.03 | 5.3 | -99.1 | -88.3 | -23.8 | -1.9 | 4.4 | 5-12k | 0 | 8 | `0001111101110` |
| 57 | 52-SH_Reverse Crash (Freeze) | 0.03 | 5.8 | -66.1 | -30.7 | -14.3 | 2.5 | 2.9 | 5-12k | 0 | 12 | `0111111111111` |
| 58 | 69-CSD _ Cinematic SD_13_142_F (Freeze) | 0.03 | 13.7 | 13.7 | -7.8 | -22.2 | -48.6 | -65.9 | 20-120 | 0 | 1 | `0000000000010` |
| 59 | SUB_PERCS | 0.03 | 13.7 | 13.7 | -7.8 | -22.2 | -48.6 | -65.9 | 20-120 | 0 | 1 | `0000000000010` |
| 60 | 39-VOX _ Another Planet_142 (Freeze) | 0.02 | 5.6 | -52.2 | -1.2 | 3.7 | -2.8 | -18.0 | 300-1k | 4 | 2 | `0000000001010` |
| 61 | 58-13_SYNTH_F_140 (Freeze) (Freeze) | 0.02 | 3.9 | -65.0 | -23.8 | 3.1 | -6.4 | -7.7 | 300-1k | 0 | 6 | `0111111000000` |
| 62 | ATMOS,PADS | 0.02 | 15.9 | -15.5 | 6.7 | 12.8 | 11.8 | -35.2 | 300-1k | 38 | 12 | `1111111101111` |
| 63 | DOWNLIFTER | 0.02 | 5.0 | -36.6 | -10.6 | 0.0 | 2.3 | -4.6 | 1-5k | 0 | 7 | `0100010101111` |
| 64 | UPLIFTER 1 | 0.02 | 9.7 | -52.7 | -10.2 | 4.0 | 6.8 | 2.7 | 1-5k | 0 | 6 | `0101010101010` |
| 65 | 20-pad 2 (Freeze) | 0.01 | 7.9 | -75.0 | -32.3 | 1.7 | 6.8 | -41.2 | 1-5k | 1 | 3 | `0011000000001` |
| 66 | 46-04_Downlifters_140 (Freeze) (Freeze) | 0.01 | -1.4 | -97.9 | -51.7 | -13.3 | -2.4 | -9.7 | 1-5k | 0 | 2 | `0000000000110` |
| 67 | 47-VOX _ Power_142 (Freeze) (Freeze) (Freeze) | 0.01 | -16.4 | -64.2 | -41.0 | -18.7 | -22.0 | -25.1 | 300-1k | 0 | 1 | `0000000000001` |
| 68 | 59-09_SYNTH_F#_140 (Freeze) | 0.01 | -2.6 | -48.1 | -13.2 | -4.4 | -8.7 | -28.7 | 300-1k | 0 | 2 | `0000101000000` |
| 69 | 63-BPI - Zap F 140Bpm (Freeze) | 0.01 | -6.4 | -27.2 | -11.5 | -13.4 | -14.9 | -11.1 | 5-12k | 0 | 2 | `0000000000011` |
| 70 | 64-FP_FG By the Seat of Your Pants (Freeze) (Freeze) (Freeze) | 0.01 | 0.6 | -40.6 | -14.7 | -2.8 | -2.5 | -15.7 | 1-5k | 0 | 1 | `0000000100000` |
| 71 | 70-MOD_TS23_Percussions - 144 (Freeze) | 0.00 | -93.7 | -99.9 | -99.8 | -99.1 | -96.4 | -95.7 | 5-12k | 0 | 0 | `0000000000000` |
| 72 | B-Delay | 0.00 | -93.7 | -99.9 | -99.8 | -99.1 | -96.4 | -95.7 | 5-12k | 0 | 0 | `0000000000000` |
| 73 | Chimes Finger Down | 0.00 | -13.6 | -75.6 | -58.6 | -48.8 | -28.8 | -13.8 | 5-12k | 0 | 2 | `0000000000011` |

## 2. Matriz presença stem × janela (1 = ativo)

Janelas: W0 0.0–27.4s · W1 27.4–54.9s · W2 54.9–82.3s · W3 82.3–109.7s · W4 109.7–137.2s · W5 137.2–164.6s · W6 164.6–192.0s · W7 192.0–219.4s · W8 219.4–246.9s · W9 246.9–274.3s · W10 274.3–301.7s · W11 301.7–329.2s · W12 329.2–356.6s

- `0111111111111` KICK_BASS
- `0011111011111` 2-01_Kick F [2023-05-30 105302] (Freeze)
- `0111111111111` BASS GROUP
- `1111111111111` STAR SYSTEM 140 F
- `0001111001110` 13-CHH_05 (Freeze)
- `0011111011110` DRUMS
- `0011111011111` F0
- `0001111011110` SEQ_GRID
- `1100001111111` MELOS
- `0011111011111` PHASE
- `0000011000110` 16-21 (Freeze)
- `1100000000001` melo 1
- `0000001000110` 17-22 (Freeze)
- `0101010111110` VOCAL
- `0111111111111` SYNTH
- `0000000000110` 34-140 - F- Top Driver (Freeze) (Freeze) (Freeze)
- `0011111001110` 12-APTS - 006 - Closed Hi-Hat  [2023-05-30 113240] (Freeze) (Freeze)
- `0000000001110` 66-BPI - Vox F 140Bpm (Freeze) (Freeze) (Freeze)
- `0001111101110` SNARE ROLL
- `0111111111111` TRANS-X
- `0000000001110` 28-FX _ Reborn _ Trippy Seq_138_F (Freeze) (Freeze)
- `0001000110000` 43-09_VOCS_F_140 (Freeze) (Freeze) (Freeze) (Freeze)
- `0000111000110` 15-OHH_03 (Freeze)
- `0000111000000` 33-33_Grids & Sequences_F#_140 (Freeze) (Freeze)
- `0111111111111` 61-BPI - Shifter F 140Bpm (Freeze) (Freeze)
- `0000001111000` melo 2
- `0000000011000` 36-03_Grids & Sequences_F_140 (Freeze) (Freeze) (Freeze)
- `0101000100000` 42-06_VOCS_F (Freeze) (Freeze)
- `0001111011110` 14-APTS - 004 - Snare  (Freeze)
- `0001100000000` 32-20_Grids & Sequences_F_140 (Freeze) (Freeze)
- `0000000000110` melo 4
- `0000000011000` OFFBEAT
- `0000100000111` 65-SFX _ Shark Attack_V2_142_F (Freeze) (Freeze) (Freeze)
- `0001111000000` 62-BPI - Acidmain F# 140Bpm (Freeze) (Freeze)
- `0000011000000` 35-29_Grids & Sequences_F_140 (Freeze) (Freeze)
- `0000000000001` 67-BPI - Zap F# 140Bpm (Freeze)
- `0000010000000` 44-06_VOCS_F#_140 (Freeze) (Freeze) (Freeze)
- `0111110111000` REVERSE
- `0000101010001` UPLIFTER 1-1
- `0111111000000` 60-21_SYNTH_F_140 (Freeze) (Freeze)
- `0000110000010` GRID-1
- `0100000000000` 57-08_SYNTH_F_140 (Freeze) (Freeze)
- `0000111000000` D#
- `0000111000000` F#
- `0000000000110` F1
- `0000000001000` 37-BPI - Stabs F 140Bpm (Freeze) (Freeze)
- `0101111111111` A-Reverb
- `0000011000010` GRID
- `0000000001110` melo 3
- `0000000000000` 41-VOCAL STAR SYSTEM
- `0000000000010` DOWN REVERSE
- `0000000000110` Diva
- `1100111101111` 19-pad 1 (Freeze)
- `0001000000000` 27-LASER (Freeze)
- `0000000000110` 40-VOX _ Another Planet_142 (Freeze)
- `0001111101110` 51-02_Crash (Freeze)
- `0111111111111` 52-SH_Reverse Crash (Freeze)
- `0000000000010` 69-CSD _ Cinematic SD_13_142_F (Freeze)
- `0000000000010` SUB_PERCS
- `0000000001010` 39-VOX _ Another Planet_142 (Freeze)
- `0111111000000` 58-13_SYNTH_F_140 (Freeze) (Freeze)
- `1111111101111` ATMOS,PADS
- `0100010101111` DOWNLIFTER
- `0101010101010` UPLIFTER 1
- `0011000000001` 20-pad 2 (Freeze)
- `0000000000110` 46-04_Downlifters_140 (Freeze) (Freeze)
- `0000000000001` 47-VOX _ Power_142 (Freeze) (Freeze) (Freeze)
- `0000101000000` 59-09_SYNTH_F#_140 (Freeze)
- `0000000000011` 63-BPI - Zap F 140Bpm (Freeze)
- `0000000100000` 64-FP_FG By the Seat of Your Pants (Freeze) (Freeze) (Freeze)
- `0000000000000` 70-MOD_TS23_Percussions - 144 (Freeze)
- `0000000000000` B-Delay
- `0000000000011` Chimes Finger Down

Nº de stems ativos por janela: W00=5, W01=20, W02=17, W03=30, W04=33, W05=36, W06=35, W07=21, W08=22, W09=33, W10=36, W11=45, W12=23.

## 3. Tabela de camadas do psy progressivo (quem toca junto, quando)

Seções lidas da matriz (corte/retorno da fundação kick+bass como divisor principal):

| Seção | Janelas / tempo | Fundação (kick+bass) | Topo/hats+snare | Seqs/grids | Melodia/voz | Cama/FX | Leitura |
|---|---|---|---|---|---|---|
| INTRO | W00 0–27 s (5 stems) | — (sem kick) | — | — | MELOS 8,3/s + melo 1 8,6/s | 19-pad 1 + ATMOS,PADS | intro melódica pura, zero percussão |
| BUILD | W01 27–55 s (20) | KICK_BASS+BASS GROUP entram ralos (0,1/s) | — | — | MELOS+melo 1 seguem + VOCAL entra 2,7/s | REVERSE + risers (UPLIFTER/DOWNLIFTER) + crash reverso | kick entra filtrado/ralo, melodia da intro continua por cima |
| GROOVE 1 | W02 55–82 s (17) | kick+bass cheios 9,3/s + Kick-Freeze | DRUMS 1,2/s + CHH fechado + F0/PHASE (sub-groove LF 4,5–6,8/s) | — | MELOS/melo 1 SAEM, SYNTH fica | TRANS-X + REVERSE | troca: sai melodia, entra bateria; F0+PHASE = segunda camada LF junto do kick |
| GROOVE 2 | W03–W06 82–192 s (30→36) | kick+bass 8,9–9,3/s contínuos | CHH_05 8,8–9,3/s + DRUMS 6–8,6/s + SNARE ROLL + 14-Snare | SEQ_GRID 0,9→8,0/s + 33-33 + 62-Acidmain + 35-29 | VOCAL alterna (W03✓ W04· W05✓ W06·) + 61-Shifter base + SYNTH | TRANS-X + crashes + GRID/D#/F# (W04–W06) | groove completo: o 16ths SEQ_GRID entra em W04; voz em janelas alternadas, nunca contínua |
| BREAK | W07 192–219 s (21) | Kick seco + F0 + PHASE saem (0,0/s); KICK_BASS + BASS GROUP seguem ralos como cama (0,11/s, ~14–15 dB) | DRUMS· hats· fora | SEQ_GRID· (0,0/s) | MELOS volta 3,1/s + VOCAL 5,4/s + melo 2 3,1/s + SYNTH | SNARE ROLL 3,0/s + TRANS-X 2,3/s + REVERSE | break = topo fora + fundação magra; ficam melodia+voz+roll+FX |
| REBUILD | W08 219–247 s (22) | kick+bass voltam 9,1/s (BASS GROUP meia-força 6,0/s) | DRUMS 0,6/s, hats ainda fora | SEQ_GRID 0,6/s | MELOS+VOCAL+melo 2 + OFFBEAT entra (3,3/s, só aqui e W09) | SNARE some, UPLIFTER | groove magro: kick sem hats, OFFBEAT como teaser |
| CLÍMAX | W09–W11 247–329 s (33→45) | kick+bass cheios | CHH+DRUMS+SNARE de volta 7–9/s | SEQ_GRID 8/s + 36-03 + 28-Trippy + 66-Vox | SYNTH explode (4,4–5,4/s em W09–W10, 3,8/s em W11) + 34-Top Driver + melo 2/3/4 + Diva | crashes + DOWNLIFTER/UPLIFTER contínuos | pico de densidade: 45 stems em W11; SYNTH vira protagonista |
| OUTRO | W12 329–357 s (23) | kick+bass seguem 8,7/s | hats/DRUMS/SEQ saem | grids saem | MELOS volta forte 6,6/s + melo 1 retorna (bookend da intro) | 19-pad + ATMOS + risers finos | cooldown: sai topo, volta a melodia da intro |

Camadas funcionais (resumo):

- **Fundação (kick seco sai, cama grave fica):** 2-01_Kick + F0 + PHASE saem no break W07 (0,0/s); KICK_BASS + BASS GROUP seguem como cama magra (0,11/s, ~14–15 dB) e voltam cheios em W08. Correção 2026-09-09: o break NÃO é mute total — o texto anterior dizia 100%, o JSON mostra os dois bounces de grupo ativos em nível baixo.
- **Sub-groove LF:** F0 + PHASE + OFFBEAT (dom 20-120) — segunda onda de graves sincopada, presente só nos grooves (W02–W06, W08–W12). OFFBEAT é one-section (só W08–W09).
- **Topo contínuo:** DRUMS + 13-CHH_05 (8–9 eventos/s nos grooves) + 12-APTS Closed HH + 14-Snare + 15-OHH — o prato/hat é UMA camada separada que entra em W02/W03 e sai no break e no outro.
- **Seq 16ths:** SEQ_GRID + família Grids&Sequences (32/33/35/36) + 62-Acidmain — entram em W03–W04, calam no break, voltam no clímax. É a 3ª perna do groove (kick+bass / hats / seq).
- **Melodia bookend:** MELOS + melo 1 abrem (W00–W01) e fecham (W12); somem no groove 1–2 e voltam no break. melo 2/3/4 são seccionais (W06–W11).
- **Voz em alternância:** VOCAL principal alterna janelas (W01✓ W02· W03✓ W04· W05✓ W06· W07✓) — voz como evento, nunca cama contínua. Vozes secundárias (42/43/44/66) são pontuais de clímax.
- **FX bed permanente:** TRANS-X + ATMOS,PADS + REVERSE + risers/downed uplifters presentes em 10–13 janelas — há SEMPRE um leito de FX sob tudo, inclusive no break.
- **One-shots de seção:** 27-LASER (só W03), D#/F# (só W04–W06), 69-CSD+SUB_PERCS (só W11), 67-Zap (só W12), crashes 51/52 marcando viradas.

## Verificação e limites

- VERIFICADO: 73/73 stems decodificados e analisados (0–360 s cada), 0 falhas. Nenhum arquivo de áudio tocado (análise somente leitura).
- VERIFICADO: kick/bass entram em W01; no break W07 o kick seco, F0 e PHASE saem (0,0/s) mas KICK_BASS+BASS GROUP seguem como cama magra (0,11/s) — correção 2026-09-09, antes constava "saem 100%"; voltam cheios em W08; hats 8–9/s nos grooves; clímax W11 com 45 stems (39 individuais); intro W00 com 5 stems sem percussão.
- INFERÊNCIA: nomes 'Freeze' com energia baixa porém taxa alta (ex. 16-21, 17-22) são camadas quietas reais — volumedetect confirma conteúdo audível (mean −40 a −53 dB, picos −15 a −23 dB).
- NÃO VERIFICADO: fase/swing dos hats do Star (requer R-scan por stem — fora do escopo de densidade); causa dos 64 'pausas' do SEQ_GRID (provável gate rítmico intencional, dado que o stem volta a 8/s no clímax).
- Limite: taxa de eventos conta transientes banda-larga (não é contagem de kicks); comparação de dB entre stems usa energia média 0–360 s incluindo trechos mudos — ver matriz de presença para leitura por seção.
