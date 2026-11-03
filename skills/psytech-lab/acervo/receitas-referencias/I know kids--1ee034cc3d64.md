# Receita — I know kids.mp3

Medição automática de 2026-10-26 (análise por script), sem escuta humana.

## 1. Identidade (medido)

| Campo | Valor |
|---|---|
| Duração | 396.23 s |
| Taxa / canais | 44100 Hz / medido em mono para análise |
| BPM (regressão) | 126.0 |
| BPM (estimativa librosa) | 126.05 |
| Batidas detectadas | 832 |
| Densidade de onsets | 5.55/s |
| Pico | 1.1 dBFS |

## 2. Tom (candidatos)

| Correlação | Tom |
|---|---:|
| 0.34 | C menor |
| 0.21 | C maior |
| 0.14 | C# menor |

Classe de altura no grave (CQT 40–200 Hz): **C** 0.123 · **G#** 0.111 · **A** 0.111 · **G** 0.104

## 3. Arco de energia (RMS por 8 compassos)

| Compassos | RMS dB |
|---|---:|
| 1–8 | -12.1 |
| 9–16 | -11.7 |
| 17–24 | -8.0 |
| 25–32 | -9.2 |
| 33–40 | -8.8 |
| 41–48 | -8.3 |
| 49–56 | -12.4 |
| 57–64 | -18.0 |
| 65–72 | -8.2 |
| 73–80 | -9.2 |
| 81–88 | -9.2 |
| 89–96 | -8.5 |
| 97–104 | -8.0 |
| 105–112 | -17.9 |
| 113–120 | -13.7 |
| 121–128 | -11.3 |
| 129–136 | -8.6 |
| 137–144 | -9.7 |
| 145–152 | -8.3 |
| 153–160 | -12.1 |
| 161–168 | -8.2 |
| 169–176 | -9.4 |
| 177–184 | -8.2 |
| 185–192 | -8.6 |
| 193–200 | -8.2 |
| 201–208 | -8.3 |
| 209–216 | -17.4 |

## 4. Grade de 16avos no pico

Compasso de pico: **89** · swing do hat medido: **-8.5%** (valor suspeito se negativo/extremo — conferir antes de usar)

```
       1...2...3...4...
  kick  9541844083318440
  corpo 6141616081905180
  clap  8071809092817090
  hat   8022903180218031
```

Forças relativas 0–9 por banda (kick 40–120 · corpo 200–900 · clap 1,5–4k · hat 7–16k). Não é MIDI. `corpo` mistura baixo.

## 5. Receita musical

> **A PREENCHER NA ESCUTA.** O script não lê estética. O executor deve ouvir 3 trechos (início / pico / saída) e escrever aqui: (a) traço que interessa — peso, rebote, acelero, timbre, ambiente, dramaturgia; (b) mecanismo provável; (c) o que **não** se copia (melodia/hook/composição); (d) adaptação ao tom e ao BPM-alvo do projeto receptor; (e) limite da medição.

## 6. Pendências desta faixa

- [ ] Stems Demucs (drums/bass/other/vocals), quando houver motor disponível.

- [ ] Escuta A/B com trecho de função equivalente do projeto em produção.

- [ ] Preencher §5 após a escuta.

