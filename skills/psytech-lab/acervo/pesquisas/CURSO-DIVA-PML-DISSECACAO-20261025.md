# CURSO PML — u-he Diva Sound Design (dissecação completa)

**Fonte:** curso "u-he Diva Sound Design Course" da Production Music Live.
**Data da análise:** 25/10/2026 · **Método:** `ffprobe` nos 38 vídeos, leitura do zip de presets, parse dos 14 `.h2p` (metadados + parâmetros internos). **Nenhum vídeo foi assistido** — a leitura de conteúdo é estrutural e técnica.
**Autoria do curso:** "Bound to Divide" (construtor dos presets) · **Ano:** 2020

---

## 1. Ficha técnica

| Item | Medida |
|---|---|
| Vídeos reais | **38** (mais 38 arquivos `._` do macOS, que são lixo) |
| Presets | **14** `.h2p` no zip `PML BTD Diva Course Presets.zip` |
| Tamanho | 1,9 GB |
| Duração total | **5h42min** |
| Resolução | 1080p, exceto `02 Bodzin Bass` que é **4K** |
| Projeto Ableton do curso | **não vem** — o zip traz só os presets |

---

## 2. Mapa das 4 partes

| Parte | Conteúdo | Vídeos | Duração |
|---|---|---|---|
| **1 — Introdução** | boas-vindas + demo do Diva + onde baixar os arquivos | 2 | 3min16 |
| **2 — Main Part: Sound Design Sessions** | 13 construções de som, do zero ao complexo | 13 | **1h56min** |
| **3 — Bonus 1: Every Knob Explained** | o Diva inteiro, módulo por módulo | 20 | **2h43min** |
| **4 — Bonus 2: Sessions** | 3 produções longas (techno melódico, baixo Bodzin, percussão) | 3 | 58min |

### Parte 2 em detalhe — é o núcleo

| # | Aula | Tempo | O que constrói |
|---|---|---|---|
| 01 | Simple Saw Wave Pluck | 7:30 | pluck básico (ponto de partida) |
| 02 | Sustained Bass | 4:02 | baixo sustentado |
| 03 | Basic Pad | 13:15 | pad simples |
| 04 | Basic Sustained Lead With Vibrato | 7:46 | lead com vibrato |
| 05 | **Clean Punchy Sub** | 7:40 | **sub com punch** |
| 06 | Dusty Noise Pluck | 9:20 | pluck ruidoso para arpejo |
| 07 | Gritty FM Lead | 11:07 | lead FM áspero |
| 08 | Epic Supersaw Chord Stabs | 7:38 | stabs de supersaw |
| 09 | Warm Crunchy Perfect 5th Bass Sweep | 7:24 | baixo em quinta com sweep |
| 10 | Lane 8 — March Of The Forest Cat (whip pluck) | 7:47 | automação de lane |
| 11 | Ben Böhmer — After Earth (lead) | 10:34 | modulação avançada |
| 12 | Arpeggiator + modulação avançada | 9:44 | arp interno do Diva |
| 13 | Complex Lush Evolving Pad | 13:02 | pad grande e evolutivo |

### Parte 3 — o que cada vídeo cobre (2h43 no total)

`Control Panel` (4:25) · `Triple VCO` (16:27) · `Dual VCO` (13:43) · `DCO` (6:03) · `Dual VCO Eco` (6:02) · `Digital Oscillator` (11:58) · `Highpass Filters & Feedback` (4:53) · `Main Filters` (13:06) · `Envelopes` (6:25) · `LFOs` (14:25) · `Tuning` (5:31) · `Amplifier & Pan` (3:17) · `Voice` (6:17) · `Clock & Arpeggiator` (6:08) · `Chorus` (1:43) · `Phaser` (3:07) · `Plate & Delay` (5:10) · `Rotary` (6:22) · `Modifications` (11:26) · `Trimmers & Scope` (17:24)

---

## 3. Os 14 presets — leitura técnica parágrafo por parágrafo

Todos os presets são compatíveis com **Diva 1.4.8** (`#Vers=10001`).

`Model` de oscilador e filtro: códigos lidos do arquivo. A correspondência com os nomes é `INFERÊNCIA` pela ordem do manual (Triple VCO, Dual VCO, DCO, Dual VCO Eco, Digital · Ladder, Cascade, Multimode, Bite, Uhbie) — não foi confirmada abrindo o plugin.

| Preset | Oscilador | VCF | HPF | ENV1 A/D/S/R | ENV2 A/D/S/R | Voz/Modo | FX | Descrição do autor |
|---|---|---|---|---|---|---|---|---|
| After_Earth_Lead | Dual VCO | Multimode | BITE | 5 / 54 / 0 / 30 | 1 / 54 / 27 / 30 | 5 / 0 | Plate | "inspired by Ben Böhmer – After Earth" |
| Arp_Example | Dual VCO | Multimode | BITE | 5 / 50 / 50 / 30 | 23,8 / 47,6 / 0 / 30 | 5 / 0 | Delay | mudanças sutis de modulação |
| Basic_Lead_With_Vibrato | Triple VCO | Ladder | POST | 0 / 30 / 100 / 20 | 0 / 75,5 / 0 / 50 | 4 / 1 | Plate | saw/square com vibrato |
| Basic_Pad | Triple VCO | Ladder | POST | 39,5 / 39 / 100 / 20 | 52 / 57,5 / 11,5 / 50 | 7 / 0 | Plate | pad simples |
| Basic_Saw_Pluck | Triple VCO | Ladder | POST | 1 / 20 / 100 / 20 | 1 / 50 / 0 / 50 | 4 / 0 | Delay | pluck de saw |
| Basic_Sustained_Bass | Triple VCO | Ladder | POST | 1 / 50 / 100 / 20 | 0 / 48,5 / 8 / 50 | 4 / 2 | Chorus | baixo saw com punch de filtro |
| **Clean_Punchy_Sub** | Triple VCO | Ladder | POST | 0 / 15,5 / 0 / 20 | 0 / 65 / 0 / 50 | 4 / 1 | Chorus | **sub limpo e sustentado com punch** |
| Complex_Lush_Evolving_Pad | Dual VCO | Multimode | BITE | 52 / 70 / 100 / 58 | 60 / 50 / 70 / 56 | 5 / 0 | Delay | muita modulação = pad grande |
| Dusty_Noise_Pluck | Dual VCO | Multimode | BITE | 5 / 31 / 0 / 30 | 1 / 53 / 0 / 30 | 5 / 0 | Delay | pluck brilhante e ruidoso para arps |
| ForestCat_Lead | Triple VCO | Ladder | POST | 1 / 20 / 100 / 20 | 27,5 / 43 / 0 / 50 | 4 / 1 | Delay | "inspired by Lane 8 – March Of The Forest Cat" |
| Gritty_FM_Lead | Triple VCO | Ladder | POST | 15 / 33,5 / 80 / 35 | 15 / 55,5 / 54 / 37 | 4 / 0 | Chorus | lead áspero com cutoff + FM do oscilador |
| Supersaw_Chord_Stab | **Digital** | **Uhbie** | PRE | 1 / 36 / 0 / 30 | 0 / 58 / 0 / 37 | 6 / 0 | Plate | stabs épicos |
| Supersaw_Chord_Stab_2 | **Digital** | **Uhbie** | PRE | 1 / 50 / 100 / 30 | 0 / 57 / 0 / 37 | 5 / 0 | Plate | variação do anterior |
| Warm_Crunchy_Perfect_5th_Bass | Triple VCO | Ladder | POST | 1 / 9,5 / 0 / 20 | 25 / 50 / 0 / 50 | 4 / 1 | Chorus | baixo em 5ª com sweep |

### O que os números revelam

1. **Só 3 combinações de oscilador × filtro em 14 presets:** Triple VCO+Ladder (8), Dual VCO+Multimode (4), Digital+Uhbie (2). **DCO, Dual VCO Eco, Cascade e Bite não são usados nenhuma vez.** São justamente os módulos com caráter mais "sujo"/analógico.
2. **Um único módulo de FX por preset** (Chorus, Plate ou Delay). Nada de cadeia. É Diva 2020 cru.
3. **O arp interno é usado em 1 preset só.** A Parte 3 dedica 6 minutos ao Clock & Arpeggiator — subaproveitado no material.
4. **ENV1 é o envelope de amplitude** (ataques de 0–5 para percussivo, 39,5–52 para pads; sustain 0 ou 100, nunca meio). **ENV2 é o modulador de filtro**, com ataques mais longos.
5. `Clean_Punchy_Sub` resolve o sub com **Triple VCO + Ladder + HPF POST em 30 Hz + ENV1 de decay 15,5 sem sustain** — ou seja, o "punch" vem do envelope, não de compressão.

---

## 4. O que o curso não vai (gap para um projeto psytech)

O curso é **techno melódico / progressive house** de 2020: Lane 8, Ben Böhmer, Bodzin. Não é psytech, não é forest, não é Zenon. Faltam exatamente as coisas que sustentam uma faixa psytech:

- **Nada de sequência/groove psy** — nenhuma aula sobre rolling bass de 16 avos, ausência de kick ou jogo de contratempo.
- **Nada de espacialidade binaural** — reverb e delay apenas dentro do Diva.
- **Nada de madeira orgânica** — sem comb filter como textura, sem kamancheh/kanun.
- **Nada de modulação pesada por LFO em textura** — o máximo é o pad evolutivo da aula 13.
- **Cascade e Bite ficam de fora** — que são os filtros com mais condição de dar o "sujo" psy.

---

## 5. Onde vale gastar tempo (ordem de prioridade para um projeto psytech)

1. **`3 - DCO Module` (6:03)** e **`3 - Main Filters` (13:06)** — o DCO é o módulo mais indicado a sub e é o único que o curso não usa nos presets. Aqui se aprende o que o material não aplicou.
2. **`2 - 05 Clean Punchy Sub` (7:40)** — é o som mais próximo de um sub rolling limpo. Comparar o envelope com o sub do seu projeto.
3. **`3 - Highpass Filters & Feedback` (4:53)** — o feedback do Diva não existe no Serum; é o tempero que falta ao baixo.
4. **`2 - 02 Sustained Bass` (4:02)** + **`2 - 09 Perfect 5th Bass Sweep` (7:24)** — os dois baixos "com corpo".
5. **`3 - Voice` (6:17)** + **`3 - Tuning` (5:31)** — drift e desafinação: o que separa Diva de plugin digital.
6. Só se sobrar tempo: a Parte 4 (`Bodzin Bass`, 4K) — é referência de techno melódico, não de psytech.

**Pode pular sem culpa:** as aulas 01–04 e 06–08 da Parte 2 (pluck, pad e lead genéricos) e as de efeitos do Diva (Chorus, Phaser, Plate, Rotary — 15 minutos no total), se o projeto não usar os FX internos do Diva.

---

## 6. Limites desta análise

- **Nada foi assistido.** A ordenação de prioridade acima vem do assunto declarado no título, da duração e do que os presets revelam — não do conteúdo falado.
- Os presets foram lidos em parâmetro, **não ouvidos**.
- O mapeamento código→nome de modelo (oscilador/filtro) é inferência do manual.
- O zip **não traz o projeto Ableton** citado na introdução; se o curso promete um projeto, ele não veio neste pacote.
