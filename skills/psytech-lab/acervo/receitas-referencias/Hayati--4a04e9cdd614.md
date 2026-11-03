# Receita — Hayati.mp3

Medição automática de 2026-10-26 (análise por script), sem escuta humana.

## 1. Identidade (medido)

| Campo | Valor |
|---|---|
| Duração | 233.22 s |
| Taxa / canais | 48000 Hz / medido em mono para análise |
| BPM (regressão) | 90.08 |
| BPM (estimativa librosa) | 90.73 |
| Batidas detectadas | 332 |
| Densidade de onsets | 2.82/s |
| Pico | -0.2 dBFS |

## 2. Tom (candidatos)

| Correlação | Tom |
|---|---:|
| 0.71 | C# maior |
| 0.51 | F menor |
| 0.49 | A# menor |

Classe de altura no grave (CQT 40–200 Hz): **F** 0.097 · **A#** 0.095 · **F#** 0.092 · **B** 0.091

## 3. Arco de energia (RMS por 8 compassos)

| Compassos | RMS dB |
|---|---:|
| 1–8 | -25.0 |
| 9–16 | -19.0 |
| 17–24 | -17.2 |
| 25–32 | -17.3 |
| 33–40 | -17.5 |
| 41–48 | -17.0 |
| 49–56 | -17.5 |
| 57–64 | -17.2 |
| 65–72 | -16.8 |
| 73–80 | -16.9 |
| 81–88 | -25.6 |

## 4. Grade de 16avos no pico

Compasso de pico: **64** · swing do hat medido: **10.5%** (valor suspeito se negativo/extremo — conferir antes de usar)

```
       1...2...3...4...
  kick  9355523190038251
  corpo 6060719470445380
  clap  6190213240522251
  hat   8291737252544180
```

Forças relativas 0–9 por banda (kick 40–120 · corpo 200–900 · clap 1,5–4k · hat 7–16k). Não é MIDI. `corpo` mistura baixo.

## 5. Receita musical

> **A PREENCHER NA ESCUTA.** O script não lê estética. O executor deve ouvir 3 trechos (início / pico / saída) e escrever aqui: (a) traço que interessa — peso, rebote, acelero, timbre, ambiente, dramaturgia; (b) mecanismo provável; (c) o que **não** se copia (melodia/hook/composição); (d) adaptação ao tom e ao BPM-alvo do projeto receptor; (e) limite da medição.

## 6. Pendências desta faixa

- [ ] Stems Demucs (drums/bass/other/vocals), quando houver motor disponível.

- [ ] Escuta A/B com trecho de função equivalente do projeto em produção.

- [ ] Preencher §5 após a escuta.

