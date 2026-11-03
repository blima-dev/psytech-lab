# Yao Ofosu — Análise de densidade Limbo + Demons (2026-09-08)

> Método: ffmpeg (f32le 22050 mono) + onsets por banda (env LF 30–120 = kick · 120–300 = bass · 300–1k = synth · 1–8k = glitch; threshold 0,35). Blocos de 20 s, 0–300 s.

## Yao — Limbo (391 s) — densidade de onsets/s por 20 s

| t (s) | kick | bass | synth | glitch |
|---|---:|---:|---:|---:|
| 0–20 | 2,2 | 3,1 | 3,6 | 4,3 |
| 20–40 | 6,0 | 8,7 | 9,8 | 8,8 |
| 40–60 | 9,7 | 11,0 | 8,9 | 8,6 |
| 60–80 | 9,7 | 10,9 | 9,9 | 8,2 |
| 80–100 | 8,0 | 10,8 | 10,4 | 9,0 |
| 100–120 | 8,3 | 10,7 | 9,9 | 7,0 |
| 120–140 | 9,8 | 10,8 | 9,2 | 7,8 |
| 140–160 | 9,2 | 10,8 | 9,7 | 8,6 |
| 160–180 | 8,3 | 10,3 | 9,8 | 6,5 |
| 180–200 | 10,4 | 10,6 | 10,2 | 9,6 |
| 200–220 | **3,5** | 11,7 | **12,5** | 8,0 |
| 220–240 | **1,9** | 10,9 | **11,7** | **10,7** |
| 240–260 | 9,6 | 9,8 | 9,6 | 8,7 |
| 260–300 | 9,1 | 10,8 | 9,9 | 7,3 |

## Yao — Demons (376 s) — idem

| t (s) | kick | bass | synth | glitch |
|---|---:|---:|---:|---:|
| 0–20 | 11,4 | 10,2 | 7,9 | 3,4 |
| 20–40 | 11,0 | 10,4 | 6,6 | 3,3 |
| 40–60 | 10,5 | 11,1 | 8,5 | 4,5 |
| 60–80 | 9,0 | 10,6 | 9,1 | 6,1 |
| 80–100 | 4,7 | 10,4 | 9,2 | 7,5 |
| 100–120 | 10,1 | 10,7 | 9,1 | 8,1 |
| 120–140 | 9,4 | 11,1 | 9,7 | 7,8 |
| 140–160 | 10,1 | 11,7 | 8,5 | 7,6 |
| 160–180 | 9,6 | 10,8 | 8,8 | 5,2 |
| 180–200 | 10,2 | 10,5 | 9,3 | 5,5 |
| 200–220 | **1,4** | 3,9 | 6,2 | 5,8 |
| 220–240 | 5,8 | 10,2 | **12,1** | 7,5 |
| 240–300 | 9,5–10,6 | 10,1–11,4 | 6,9–12,1 | 5,5–9,8 |

## A RECEITA MEDIDA (o segredo do Yao)

1. **Densidade total do pleno: TODAS as camadas a 9–12 onsets/s SIMULTÂNEAS** (kick 4/4 + bass 16ths + synth 16ths + glitch 16ths somando ~40 eventos/s). Não é um elemento carregando — são TODOS correndo.
2. **Breakdown = inversão**: o kick DESAPARECE (Limbo 200–240: 9,8→1,9/s) e o synth GLITCH SOBE (8,6→10,7/s) — a energia transfere de camada em vez de sumir.
3. **Limbo abre com tensão inversa**: glitch 4,3/s antes de qualquer kick (a "conversa" começa nos agudos, o grave entra depois).
4. **Demons abre direto no pleno** (kick 11,4/s desde o 0) — intro sem build.
5. **Corpo da track: 180–300 s contínuo denso sem pausas** — a "história" do Yao é um mergulho: entra, afunda, e não sai até o fim.

## Fontes

Faixas Limbo (391 s) e Demons (376 s) de Yao Ofosu; análise ffmpeg+numpy.
