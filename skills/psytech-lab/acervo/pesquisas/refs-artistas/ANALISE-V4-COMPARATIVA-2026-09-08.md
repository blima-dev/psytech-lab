# RÉGUA PADRÃO PSYTECH — Mayuri (Gazolla) × AIO "Illusion" × Akari "Segments": valores de referência

Data: 2026-09-08 · **Método (régua padrão):** ffmpeg decode f32le 22050 Hz mono + numpy (STFT 1024 pts, hop 256 ≈ 11,6 ms). Energia por banda 20-120 / 120-300 / 300-1k / 1-5k / 5-12k Hz; onsets por fluxo espectral; kick por pico do envelope 30-120 Hz (> baseline+6 dB); grid por varredura de concentração circular (R); swing = desvio dos contratempos vs fase do grid; pausas = envelope LF < baseline−7 dB por ≥0,3 s sem kick no interior.

As três referências foram medidas com a mesma régua, número a número. O que segue são os **valores de referência** — a régua contra a qual qualquer faixa do estilo pode ser auditada.

---

## 1. BPM e grid

| Métrica | Mayuri | AIO Illusion | Akari Segments |
|---|---|---|---|
| BPM medido | 126,98 | 127,99 | 127,99 |
| Beat / compasso | 472,5 ms / 1,890 s | 468,8 ms / 1,875 s | 468,8 ms / 1,875 s |
| R do grid @ BPM medido | 0,733 | 0,916 | 0,895 |
| % kicks dentro de ±40 ms | 89,0% | 92,3% | 89,1% |
| IOI mediana do kick | 476 ms | 464 ms | 464 ms |
| Eventos LF fora do grid | 52/473 = 11% | 47/608 = 8% | 21/193 = 11% |
| Drift 60-180 / 180-300 | 127,05 (R 0,751; 1ª janela c/ amostra insuf.) | 127,98 / 128,03 (R 0,989 / 0,830) | 127,98 / 127,87 (R 0,954 / 0,778) |
| R @127 vs R @128 | 0,733 vs 0,325 → 127 ✓ | 0,104 vs 0,918 → 128 ✓ | 0,206 vs 0,895 → 128 ✓ |

- VERIFICADO: sem drift em nenhuma (BPM estável nas duas janelas).
- Padrão de precisão: **89–92%** dos kicks dentro de ±40 ms; eventos LF fora do grid **8–11%**.

## 2. Kick rate por bloco de 20 s (kicks/s)

| t (s) | Mayuri | AIO | Akari |
|---|---|---|---|
| 0–20 | 1,75 (pulsos intro) | 2,15 (4×4 desde o 1º bar) | 1,65 |
| 20–40 | 0,90 | 2,15 | 0,25 |
| 40–60 | 0,10 (kick sai) | 2,10 | 0,05 |
| 60–80 | 1,95 | 2,15 | 2,10 |
| 80–100 | 1,95 | 2,15 | 0,90 |
| 100–120 | 1,80 | 1,70 | 0,30 |
| 120–140 | 0,10 (kick sai) | 2,15 | 0,05 |
| 140–160 | 1,15 | 2,15 | 0,65 |
| 160–180 | 2,00 | 2,10 | 0,90 |
| 180–200 | 1,80 | 2,15 | 0,05 |
| 200–220 | 2,05 | 2,10 | 0,70 |
| 220–240 | 2,10 | 2,15 | 1,50 |
| 240–260 | 2,00 | 1,70 | 0,05 |
| 260–280 | 2,05 | 1,80 | 0,10 |
| 280–300 | 1,95 | 1,70 | 0,40 |

- Padrão: nos grooves, Mayuri sustenta **1,8–2,1/s** e AIO **2,1/s constante**; Akari é variável (0,05–2,1 — o padrão variável em si tem precedente). Vácuos declarados: o kick **sai por bloco inteiro** nos builds/breakdowns (40–60 s e 120–140 s na Mayuri).

## 3. HF rate — ondas de topo (onsets 1–8k /s)

| t (s) | Mayuri | AIO | Akari |
|---|---|---|---|
| 0–20 | 3,90 | 5,95 | 8,50 |
| 20–40 | 8,00 | 7,70 | 7,75 |
| 40–60 | 7,70 | 7,20 | 7,10 |
| 60–80 | 7,65 | 7,70 | 8,10 |
| 80–100 | 7,85 | 5,00 | 6,45 |
| 100–120 | 8,05 | 2,85 | 7,55 |
| 120–140 | 7,50 | 5,20 | 6,20 |
| 140–160 | 5,30 | 6,70 | 4,00 |
| 160–180 | 4,50 | 7,60 | 5,20 |
| 180–200 | 4,30 | 7,35 | 7,65 |
| 200–220 | 1,90 | 4,00 | 3,75 |
| 220–240 | 3,05 | 3,30 | 2,95 |
| 240–260 | 4,40 | 6,45 | 6,00 |
| 260–280 | 5,45 | 4,60 | 4,30 |
| 280–300 | 6,35 | 0,95 | 4,50 |
| Metades (h1→h2) | 7,16 → 4,29 | 5,90 → 5,11 | 7,18 → 4,82 |

- Padrão: as três fazem **ondas** de topo (vales e picos alternando). Nos grooves da 1ª metade o patamar é **6–8/s** e a intro abre **3,9–8,5 onsets/s**. Mayuri/Akari secam o topo na 2ª metade (7,2→4,3 / 7,2→4,8).

## 4. 120–300 Hz — o "corpo"

| Visão | Mayuri | AIO | Akari |
|---|---|---|---|
| Corpo nos grooves (blocos 20 s) | 30,9–35,0 dB | 36,1–37,1 dB | 27,4–32,7 dB |
| Mínimo da faixa | 27,5 (intro) | 30,5 | 19,4 (intro) |
| Metades h1→h2 | 31,8 → 34,3 (+2,5) | 36,5 → 36,1 (−0,4) | 30,7 → 31,7 (+1,0) |
| Corpo relativo ao kick (h1, dB vs 20-120) | −13,1 | −5,5 | −15,5 |

- Padrão: **o corpo nunca desliga dentro de um 4×4** (mínimo 27,5–30,5 dB nos grooves); dentro do groove ele anda entre −5,5 e −15,5 dB relativo ao kick.

## 5. Pausas do kick — quantas e onde

| Métrica | Mayuri | AIO | Akari |
|---|---|---|---|
| Total de pausas detectadas (janela 300 s) | 28 | 3 | 7 |
| Pausas estruturais | furos 0,84–2,51 beat nos builds/drops (203,7/207,6/211,2/253,9–256,6/271,5/286,1) | 3 furos curtos (209,7/261,0/269,4) | 7 furos 0,67–3,27 beat |
| Micro-furos no corpo | 0 | 0 | 0 |
| Pausas na 1ª/2ª metade | 19 / 9 | 0 / 3 | 2 / 5 |

- Padrão: **POUCAS pausas no corpo (3–28 em 300 s) e nenhuma micro-textura de gate no low-end** — os furos (0,67–2,5 beat) são reservados a builds/drops.

## 6. Swing — desvio do contratempo (negativo = adiantado)

| Camada / slot | Mayuri (Gazolla) | AIO | Akari |
|---|---|---|---|
| Kick, e16 | −17,2 ms (n=16) | — | — |
| **Hats 1-8k, off8** | **−13,3 ms adiantado (n=456)** | **−26,8 ms (n=95)** | **−24,8 ms (n=155)** |
| Hats 1-8k, e16 | −4,4 ms (n=300) | −23,3 ms (n=143) | −16,3 ms (n=226) |
| Hats 1-8k, a16 | −1,4 ms (n=279) | −22,2 ms (n=121) | −18,8 ms (n=229) |
| Brilho 5-12k, off8 | −13,8 ms (n=441) | −26,4 ms (n=100) | −25,7 ms (n=126) |
| Slots de hat (concentração) | 1 slot: 7 (25%) + 15 (24%) | 1 slot: 6 (27%) + 14 (28%) | 1 slot: 6 (21%) + 14 (26%) |

- Padrão: nos três, os hats são **ADIANTADOS (−13 a −27 ms)** e a energia se concentra **num único slot** (≥21%) — a assinatura "groove empurrado" é carregada pelos hats.

## 7. Narrativa espectral (1ª → 2ª metade)

| Banda | Mayuri | AIO | Akari |
|---|---|---|---|
| 5-12k | 16,6 → 12,2 (−4,4) | 19,1 → 14,7 (−4,4) | 24,0 → 20,3 (−3,7) |
| 120-300 | 31,8 → 34,3 (+2,5) | 36,5 → 36,1 (−0,4) | 30,7 → 31,7 (+1,0) |
| 300-1k | 29,9 → 31,3 (+1,4) | 29,1 → 32,3 (+3,2) | 27,3 → 28,5 (+1,2) |
| 1-5k | 20,1 → 24,1 | 24,4 → 23,4 | 27,1 → 27,2 |
| 5-12k relativo ao kick | −28,3 dB rel | −22,9 dB rel | −22,2 dB rel |
| 1-5k relativo ao kick | −24,8 dB rel | −17,6 dB rel | −19,1 dB rel |
| 300-1k relativo ao kick | −15,0 dB rel | −12,9 dB rel | −18,9 dB rel |

- Padrão: grave/corpo crescem ao longo; **o topo seca na 2ª metade (−3,7 a −4,4 dB)** — o arco "topo recua, transe assume". Nos grooves, o brilho fica em **1-5k ≈ −18 a −25 dB rel ao kick** e **5-12k ≈ −22 a −28 dB rel**.

## 8. Estrutura quantizada em múltiplos de 32 beats

- Mayuri: todos os marcos em múltiplos de 32 com **erro ≤0,2 beat** (intro fecha em 64; volta do groove em 128; drops em blocos cheios; 2º drop em 448).
- AIO/Akari: drops também em blocos cheios de 32.
- **Cortes estruturais caem no fim do bloco de 8 bars (mod32 28–31)**: Mayuri 30,1/29,5/30,9; AIO 31,2/30,7; Akari 28,7–31,3.

---

## O que o padrão das referências exige (síntese da régua)

1. **Topo presente nos grooves:** brilho 1-5k ≈ −18 a −25 dB rel ao kick e 5-12k ≈ −22 a −28 dB rel durante o groove inteiro; a narrativa "topo seca" (−3,7 a −4,4 dB na 2ª metade) só existe onde há topo para secar.
2. **Swing do topo adiantado e concentrado:** hats −13 a −27 ms adiantados, energia num slot único (≥21%) — o gingado é carregado pelos hats; o Gazolla antecipa −13 ms no contratempo.
3. **Grid preciso e low-end contínuo:** 89–92% dos kicks no grid (±40 ms); 8–11% de eventos LF fora; **zero micro-furos de gate no low-end entre kicks**.
4. **Densidade de groove:** kick 1,8–2,1/s nos grooves (AIO 2,1 constante); HF 6–8/s nos grooves da 1ª metade; intro com 3,9–8,5 onsets/s. O 4×4 só sai em **breakdowns declarados** (bloco inteiro sem kick).
5. **Corpo sempre presente:** dentro de qualquer 4×4, 120–300 Hz nunca desliga (mínimo 27,5–30,5 dB na régua interna).
6. **Estrutura ancorada no lattice de 8 compassos:** marcos em múltiplos de 32 beats e cortes estruturais em mod32 28–31.
7. **Master:** alvo −7 a −6 LUFS integrado com clipper antes do limiter (consenso da cena).

## Verificação e limites

- Régua aplicada identicamente às três referências (ffmpeg/numpy, STFT 1024/256 @22,05 kHz mono).
- Limitações: janelas de drift e de fase usam 60–300 s; o detector de pausas não captura vácuos >3 s como "pausa"; "kick rate" conta eventos LF (kick + re-trigger de bass na mesma banda); níveis são internos a cada faixa (não comparar absolutos entre masters diferentes).
