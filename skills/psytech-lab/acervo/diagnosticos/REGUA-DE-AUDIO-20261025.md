# Régua de áudio — set de referência × 15 referências da família (25/10/2026)

> Estudo do acervo psytech-lab, anonimizado. Método: medição em **taxa nativa e estéreo** via ffmpeg, sem
> reamostrar e sem somar em mono (regra de método do projeto: proibido medir topo (>8 kHz) ou estéreo após
> reamostrar para 22,050 kHz ou somar em mono). Mede: LUFS integrado e true peak (ebur128) e, na **janela de
> 60 s de maior RMS** (o clímax): 6 bandas de energia, side/mid total e side/mid do grave, crest.
> **Nada foi ouvido** — os números são objetivos; o julgamento estético é do produtor.
>
> **CORREÇÃO do baseline (25/10):** os números de "ar 0,5% / low-mid 13,7%" da seção 2 vêm de um render
> anterior (24/10, motor antes de uma revisão grande), na janela de maior RMS. O baseline novo do estado
> atual mede, no **Drop 1**, **air 1,0% · low-mid 23,9% · bass 22,6%** e, no **Drop 2**, **air 1,7% ·
> low-mid 30,5% · bass 15,5%**. O gap real do estado atual é **low-mid/bass**, não ar.

---

## 1. As 15 referências

Acervo de 15 faixas completas (> 150 s) da família: Slippery Slope (Luis M), Luis M, Desert Nomads,
Farhy/Orion/Kaled Nasser, Fox (Artemis), Gazolla/Petrix, ISMAIL.M, AlpaKa, Petrix, Rollfree, Lady Rave.

| Métrica (mediana) | Valor | Faixa (min–max) |
|---|---|---|
| LUFS integrado | **−8,7** | −11,7 a −6,9 |
| True peak | **+2,3 dBTP** | +0,6 a +6,3 |
| Crest | 11,1 dB | 9,2 a 15,7 |
| Sub (20–60 Hz) | **47,5%** | 13,5 a 59,0 |
| Bass (60–120 Hz) | **37,1%** | 22,8 a 52,7 |
| Low-mid (120–400) | 9,4% | 4,9 a 22,3 |
| Mid (400–1,5k) | 2,7% | 0,9 a 7,9 |
| Presence (1,5–6k) | 1,2% | 0,4 a 8,3 |
| **Air (6–16k)** | **1,6%** | 0,3 a 6,9 |
| Side/mid | −14,8 dB | −24,6 a −10,9 |
| Side/mid do grave (<120 Hz) | −32,7 dB | −48,6 a −12,9 |

`VERIFICADO`.
Observação de leitura: as referências estão **masterizadas e clipando** (+2,3 dBTP de mediana). Comparar
LUFS/TP com um render cru não mede qualidade de mix — mede estágio de masterização. As bandas e o estéreo
são a parte comparável.

---

## 2. O set de referência contra a família

Render completo (20:15), janela analisada 80–140 s.

| Métrica | Referências | Set | Delta |
|---|---|---|---|
| LUFS | −8,7 | **−10,9** | −2,2 LU mais baixo (esperado: não masterizado) |
| True peak | +2,3 dBTP | **−0,6** | −2,9 dB (headroom; elas clipam) |
| Crest | 11,1 | **10,5** | −0,6 (mesma família) |
| Sub | 47,5% | **43,6%** | −3,9 pp |
| Bass | 37,1% | **36,9%** | **−0,2 pp — idêntico** |
| Low-mid | 9,4% | **13,7%** | **+4,3 pp** |
| Mid | 2,7% | **3,7%** | +1,0 pp |
| Presence | 1,2% | **1,5%** | +0,3 pp |
| **Air** | 1,6% | **0,5%** | **−1,1 pp (≈3× menos)** |
| Side/mid | −14,8 | **−14,1** | +0,7 dB (levemente mais largo) |
| Side/mid grave | −32,7 | **−41,8** | −9,1 dB (grave mais mono) |

`VERIFICADO` nas medições; a leitura abaixo é `INFERÊNCIA`.

**O que estava certo:** o grave na régua (bass idêntico, sub 4 pp abaixo), o estéreo na régua (0,7 dB mais
largo), o grave **9 dB mais mono** que a mediana — o desejado quando o cânon é low-end mono — e o crest na
família.

**O que estava fora:** o set é **mais escuro e mais grosso**. +4,3 pp de 120–400 Hz e **3× menos ar
(6–16 kHz)**. Não é problema de topo de mix (presence 1,5% contra 1,2%) — é de **ar**: falta a camada de
8–16 kHz que as referências têm. Um A/B de high shelf que estava pendente reabre com número — e diz onde
agir: **acima de 6 kHz**, não em 1,5–6 kHz. (⚠️ ver a correção do baseline no topo: num render mais novo o
gap passou a ser low-mid/bass.)

---

## 3. As quatro escolas de sessão (medidas com a mesma ferramenta)

| | **Let You Go** | **Giants** | **Drift** | **Tim Engelhardt** | **Set de referência** |
|---|---|---|---|---|---|
| BPM | 125 | 122 | 122–132 | 123–124 | 128 |
| Pistas | 22 | 71 | 19–40 | 24–32 | **81** |
| Notas | 1.334 | 21.127 | 96–1.189 | 730–3.659 | **70.645** |
| Compassos | 209 | 220 | 124–188 | 192–208 | 241 |
| **FX por pista** | 2,7 | **5,1** | 2,9 | 2,8–3,5 | **5,07** |
| Returns | **1** | 5 | 2 | 3–4 | 2 |
| Sends ativos | 5 | **28** | 0–2 | 19–32 | 9 |
| Master | **só Utility −3,33 dB** | rack + EQ + Utility +8,33 + master chain | comp 0,01 ms + Clipper + **2 limiters** | EQ + **Glue paralelo 4,8–7,9%** + 1 limiter | EQ + Glue + Utility + Limiter + M4L |

`VERIFICADO`.

**O que a tabela prova:** não existe "o master do gênero". Existe **um continuum** — do Let You Go
(master = um trim de −3,3 dB, nada mais) ao Drift (dois limiters em série). O que três das quatro escolas
compartilham é **FX por pista entre 2,7 e 3,5**; o Giants (5,1) e o set (5,07) estão no extremo maximalista
— mesma densidade por pista, por motivos diferentes (o Giants por ser curso com 71 pistas; o set por ter
~20 trilhas de FX por família).

O set está **acima** da régua de FX por pista (5,07 contra mediana 2,88) e no meio do continuum de master.
Maximalista em duas dimensões: densidade por pista (igual ao Giants) e tamanho (2,5× a mediana de pistas,
129× as notas).

---

## 4. Racks `.adg` — amostra de 125

| Tipo | Quantidade | Conteúdo |
|---|---|---|
| Cadeias de efeito (sem instrumento) | **48** | Eq8 63 · Delay 39 · Limiter 37 · AutoFilter 30 · StereoGain 29 · Reverb 29 · Saturator 26 · Multiband 21 · Compressor2 19 |
| Racks de bateria | **1** | rack de hats |
| Racks com plugin | 0 | — |

Distribuição: 90 em um mega pack de psytrance, 20 + 13 em packs de peak-time techno, 2 avulsos.
`VERIFICADO`.
`INFERÊNCIA` — são cadeias de efeito reutilizáveis (EQ, delay, limiter, filtro, reverb, saturação) e **um**
rack de bateria. Não são "presets de som": são peças de mix. O valor está em reusar as cadeias, não em
procurar instrumento.

---

## 5. O que aplicar num set com este perfil (a partir do áudio)

| # | Ação | Prova numérica |
|---|---|---|
| 1 | **A/B de high shelf em 8–12 kHz** (+1,5 a +2 dB) no master ou no bus de madeiras/orquestra | ar 0,5% × mediana 1,6% |
| 1b | **Sala curta (0,7–1,0 s) para bateria**: nenhuma pista de bateria tinha reverb — as reverbs do set estavam em leads, madeiras e vozes | a escola Tim mede 0,71 / 1,04 / 0,78 s de drum room nas 3 faixas |
| 2 | **Cortar 120–400 Hz** (−1 a −2 dB) em uma faixa larga do master ou nos buses que acumulam low-mid | low-mid 13,7% × mediana 9,4% |
| 3 | **Não mexer no grave nem no estéreo** | bass idêntico, S/M +0,7 dB, grave 9 dB mais mono |
| 4 | Se for masterizar: mirar **−9 a −8 LUFS e true peak −0,3**, não os +2,3 dBTP das referências | mediana −8,7 / +2,3 |

## 6. Limites

- **Nada foi ouvido.** Bandas de energia são mapa, não julgamento.
- O render analisado é de uma data específica — pode não ser o estado final do set.
- As 15 referências são masters de lançamento; as diferenças de LUFS/TP medem masterização, não mix.
- A janela de 60 s de maior RMS é uma escolha: mede o clímax, não a média da faixa.
- Ferramentas antigas de comparação que carregam a 22,050 Hz e somam em mono **não servem** para esta régua:
  cortam o ar e perdem o estéreo.

---

## 7. Afinação e cauda do kick (medido)

### 7.1 Os 53 kicks do pack Drift (referência externa)

| Medida | Valor |
|---|---|
| Fundamental (pico 25–150 Hz) | mediana **49,1 Hz** · mín 25,6 · máx 68,0 |
| Classes mais comuns | **G1 (15)** · G#1 (11) · A1 (6) · F#1 (5) · E1 (5) |
| Decay −20 dB | mediana **0,19 s** · mín 0,08 · máx 0,39 |
| Duração do arquivo | mediana **0,48 s** |

`VERIFICADO`. O nome do arquivo carrega a nota e a medição confere: `PML_TH3_Kick_004_F#_Arson` → 45,1 Hz
(F#1) · `…_G_Brain` → 47,8 (G1) · `…_F_Greed` → 42,4 (F1) · `…_A#_Far` → 53,8 (~A#1).
`INFERÊNCIA` — o pack **afina o kick na nota**, mas não necessariamente na tônica: o loop de baixo citado é
D#min e o kick é F# (terça menor). O que importa é ser **grau consonante da tonalidade**.

### 7.2 Os dois kicks do set de referência

| Papel | Sample | Fundamental medida | Intervalo sobre C# |
|---|---|---|---|
| kick principal | `01. Punchy Kick - Outerverse.wav` | **52,5 Hz** | ≈ **G#1 (+20 cents) = 5ª justa** |
| kick alternativo | `TPS - Oasis - Kick 15.wav` | **46,4 Hz** | ≈ **F#1 (+81 cents) = 4ª justa** |

`VERIFICADO` por FFT nos dois arquivos.
**Os dois são consonantes com C#** (quinta e quarta). Não há problema de afinação.
No save medido **só o principal toca**; o alternativo está desligado — sem um segundo kick somando na
fundamental.

⚠️ **O nome mente:** o rack do kick principal se intitulava "Organic **48Hz**" e a fundamental medida é
**52,5 Hz**. Qualquer ajuste futuro feito "pelos 48 Hz do nome" erraria ~90 cents. Auditar o áudio, não o
nome.

### 7.3 Correção de leitura importante (semântica do .als)

No `.als`, `Mixer/Speaker` **não é mute**: `Speaker/Manual = true` significa **pista ATIVA**. Uma ferramenta
de auditoria antiga rotulava esse campo como `mute` — estava **invertida em 186 sets auditados**. Corrigido
em 25/10: o JSON de auditoria passou a trazer `active` e `mute` separados, com mute = inverso de Speaker.
