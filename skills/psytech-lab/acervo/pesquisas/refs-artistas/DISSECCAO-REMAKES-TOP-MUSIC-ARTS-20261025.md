# DISSECÇÃO — TOP MUSIC ARTS: ARTBAT "Atlas" + Boris Brejcha "Never Look Back"

**Data:** 25/10/2026 · **Fonte:** pacote de remakes de fã (projetos `.als` + presets + MIDI)  
**Método:** parse direto do `.als` (gzip+XML) + leitura das posições de clipe no arranjo. **Nenhum áudio foi renderizado nem ouvido.**

---

## 1. O que veio

| Remake | Estado | Conteúdo |
|---|---|---|
| **ARTBAT — Atlas** | **completo** | `.als` + backup + 3 samples + cfg. **5 refs de amostra, 3 presentes.** 74 presets de device referenciados (a biblioteca do Live resolve) |
| **Boris Brejcha — Never Look Back** | **completo, mas com mídia faltando** | `.als` + 13 samples. **140 refs de amostra, só 13 presentes (127 faltam)** — os caminhos apontam para pastas originais do autor do remake |
| Adriatique — Mystery | incompleto | **64 MIDI** (nenhum `.als`, nenhum preset) |
| Boris Brejcha feat. Laura Korinth — Gravity | incompleto | **48 MIDI** |
| Monolink — Return To Oz (ARTBAT Remix) | incompleto | 23 `.fxp` (Serum 1, mortos) — **0 MIDI, 0 `.als`** |
| The Producer School — Pressure | incompleto | **52 MIDI** (de 1.380 fragmentos `.fdmdownload`) |
| **Purple Disco Machine — Hypnotized** (novo 26/10) | **completo** | `.als` + **12 `.fxp`** (Serum 1) + cfg + aulas em `.txt` (sem os WAV/AIF — abre com mídia faltante) → §8 |
| **Sofi Tukker & John Summit — Sun Came Up** (novo 26/10) | **completo** | `.als` + **8 `.fxp`** + cfg + MP3 de referência (7,9 MB; sem os WAV) → §8 |

---

## 2. O MINIMAL DO BORIS — "Never Look Back"

`VERIFICADO` por leitura do `.als`. **125 BPM · 250 compassos (7:40) · 28 pistas · 802 notas.**

### 2.1 A densidade

| Medida | Valor |
|---|---|
| Notas por compasso (track inteira) | **3,2** |
| Percussão + bateria (somas) | 76 kick + 76 ataque + 69 snare + 50 claps + 64 close + 80 open + 12 shaker + 15 crash = **442 notas** |
| Melodia/harmonia | **360 notas** |
| Elementos que tocam a track toda | **1** (o `Lead`) |

É uma track de 7m40 com **802 notas** — o conteúdo melódico de um loop de 8 compassos repetido com variação cirúrgica.

### 2.2 A linha do tempo real (compasso de entrada + duração)

| Elemento | Onde entra (bars) |
|---|---|
| **Kick + Atack Kick** (2 camadas, sempre juntas) | 0 → 250, com respiro em **35–36** |
| **Lead** | **0 + 156** e **158 + 92** → toca praticamente a track inteira |
| Sub | 16 · 32 · 40 · 76 · 132 · 140 · 158 · 182 · 198 |
| Clap 1 | 16 · 64 · 88 · 140 · 158 |
| Close | 0 + 100 · 132 · 140 · 168 + 82 |
| HH Open | 52 · 75 · 132 · 140 · 168 + 76 |
| **PLUCK** | 52 · 55 · 58 (fills curtos) · 76 + 12 · 88 + 12 · 124/126/128 · 140 + 16 · **158 + 60** |
| PAD | 20 · 60 · 108 · 124 · 128 · 132 · **174 + 22** |
| **PAD Monster** | 28 · 44 · 100 · 214 · 225 — **4 compassos cada, 5 vezes = 20 de 250** |
| Arp1 / Arp2 | 40 · 44 · 56 · 156 · 218 |
| **Noise Snare** (rolo) | 60–67 e 158–173, em clipes de **0,38 compasso** |
| Crash | 15 clipes de **0,5 compasso** |
| Shaker | 67 · 88 · 190 |

**Leitura:** as seções mudam em **8 e 16 compassos** (0 · 16 · 32 · 36 · 52 · 60 · 76 · 88 · 108 · 124 · 132 · 140 · 158 · 174 · 198 · 218 · 250). O bloco final (**158–250, 92 compassos**) é o mais longo e o mais estável: o PLUCK toca **60 compassos seguidos**.

### 2.3 O que faz o "minimal" dele funcionar

1. **Duas camadas de kick sempre em uníssono** — `Kick` (Simpler + 2× Eq8 + StereoGain, vol 0,33) e `Atack Kick` (Simpler + StereoGain, vol 0,20). Mesmas 76 notas, mesma grade. O peso vem do corpo, o clique vem da segunda.
2. **Uma melodia que não para.** O `Lead` fica 156 compassos ligado. Não é "menos elementos", é **um elemento contínuo** com os outros entrando e saindo em volta.
3. **Harmonia de 2 notas.** O `Lead Saw` tem **2 notas** na track inteira (pitch 41). O `Main BS fow` tem **2** (pitch 65). O `Tone` tem 4. A variação não vem de nota nova — vem de **timbre e filtro**.
4. **Volume como hierarquia, não como mix.** Os pads estão em 0,07 e 0,06; o PLUCK em 0,42 — o elemento melódico é 6× mais alto que o pad. No Boris, pad é **textura**, não é camada de acorde.
5. **Sidechain em tudo que respira.** 19 das 28 pistas têm `Kickstart` no fim da cadeia (VST externo).
6. **Ponto de nota a cada 4–8 compassos.** Crash de 0,5 compasso, 15 vezes. Bate com a regra do cheat sheet do Omar Meho ("ponto de nota a cada 4 ou 8 compassos").

### 2.4 A cadeia de master dele (é uma receita inteira)

```
GlueCompressor (thr −12,0 · ratio 2 · attack 0)
→ Eq8 (35 / 200 / 1k / 5k / 18k, ganhos 0 = só HP/LP)
→ RACK Mid/Side:  Side = StereoGain (separação 2 = largura total)
                   Mid  = StereoGain (separação 0 = mono)
→ Eq8 #2 (shelf +3,6 dB @ 2.947 Hz)
→ RACK Multibanda: High Gain +5,0 · Mid Gain +6,0 · Low Gain +6,5
                   (split em 120 Hz e 2.500 Hz, ratio ±0,3)
→ GlueCompressor #2 (thr −12,4 · makeup 0,95 · attack 6)
→ Limiter (Gain +8,5 dB · ceiling −0,3)
```

`INFERÊNCIA` — o ganho de +5 a +6,5 dB **por banda** antes do segundo glue é o que dá o "alto e denso sem distorcer" do gênero: ele levanta cada banda separadamente em vez de subir o master.

---

## 3. ARTBAT "Atlas" — o material de SYNTH e ATMOS

`VERIFICADO`. **122 BPM · 227,5 compassos (7:18) · 25 pistas · 1.010 notas.**

### 3.1 A assinatura: 5 leads empilhados na MESMA nota

| Pista | Motor | Notas | Vol | Cadeia |
|---|---|---|---|---|
| Lead 1 | **Operator** | 176 @ pitch 51 | 1,00 | Reverb → Flanger (OFF) → Eq8 → Glue (thr −11,7, ratio 1) → Kickstart |
| Lead 2 | **Wavetable** | 176 @ 51 | 1,00 | idem |
| Lead 3 | **Operator** | 176 @ 51 | 0,67 | idem |
| Lead 4 | **Wavetable** | 176 @ 51 | 0,76 | idem |
| Lead 5 | **Wavetable** | 24 @ 51 | 0,79 | Reverb → **A Bit Warmer** (wet 0,62) → Eq8 |

Os quatro primeiros têm **o mesmo MIDI, 176 notas, pitch 51** — 51 = **D#3**. É a tônica da track (o Reese está em 27 = D#1, as strings em 63/66/70 = **D#4/F#4/A#4** = tríade menor de D#).

**Mecanismo:** as camadas não fazem harmonia — fazem **espessura**. Dois motores diferentes (FM do Operator + wavetable) na mesma nota, com volumes decrescentes (1,00 · 1,00 · 0,67 · 0,76 · 0,79) para não somar em bloco.

A cadeia é **literalmente a mesma** nos quatro (mesmo PreDelay 2,5 ms, mesmo BandFreq 1.481,8 Hz de reverb, mesmo Glue em −11,7). Ele copiou a pista e trocou só o instrumento.

### 3.2 As cordas: 4 camadas de 12 notas

| Pista | Motor | Notas | Vol |
|---|---|---|---|
| String 1 | Wavetable | 4+4+4 @ 63/66/70 | 0,34 |
| String 2 | **Brass Wave** (rack: Wavetable → Compressor2 → DrumBuss → StereoGain → Chorus) | idem | 0,34 |
| String 3 | Wavetable | idem | 0,34 |
| String 4 | **Strings6 Ensemble** | 5 @ 63 | 0,24 |

Eq8 de todas: **high-pass em 426 Hz + low-pass em 19.776 Hz** — a faixa útil das cordas é 426 Hz–19,8 kHz. Reverb com BandFreq 1.620 Hz.

Para projetos que medem pouco ar em 6–16 kHz: aqui o ar vem de **4 camadas de cordas com HP em 426 Hz**, não de EQ no master.

### 3.3 Pluck e baixo — o uso de OTT

| Pista | Cadeia | Destaque |
|---|---|---|
| **Pluck** | Wavetable (**Sub OSC ligado, gain 1,0**) → Reverb (decay 975 ms, pre 2,5 ms) → **Overdrive (drive 50%, wet 50%, mid 1.250 Hz)** → **OTT (amount 0,2; ganhos low +10,3 / mid +5,7 / high +10,3)** → Eq8 (HP 73 Hz) | O OTT dá o "fino e brilhante" típico do prog/melodic |
| **Mid Bass 1** | Wavetable (2 osc) → Reverb → Eq8 (HP 240) → **A Bit Warmer (wet 0,33)** → **OTT Niles (amount 0,44; low +4,6 / mid +5,7 / high +4,2)** → 2 Delays (um com feedback 0,25) | O baixo **também** passa por OTT — não é só o lead |
| Sub | Waveform (1 osc) → Overdrive → Kickstart | 40 notas, grade 0/4/8/12 |
| Mid Bass 1/2/3 | 3 camadas, **mesmas 30 notas, pitch 51** | Espessura por camada, igual aos leads |

**Padrão que se repete:** ARTBAT empilha **3–5 pistas com o mesmo MIDI** e varia motor + volume. Boris faz o oposto: **1 pista por função**, harmonia de 2 notas.

---

## 4. Boris × ARTBAT — dois jeitos de chegar no mesmo lugar

| Dimensão | Boris (Never Look Back) | ARTBAT (Atlas) |
|---|---|---|
| Notas / compasso | **3,2** | 4,4 |
| Melodia | 1 lead contínuo, 2 notas de pitch | 5 camadas na mesma nota (D#3) |
| Harmonia | F–G–C (2–3 classes) | Tríade menor de D# |
| Kick | **2 camadas** (corpo + ataque) | 2 pistas (intro + principal) |
| Baixo | Sub (Serum) + Sub Groove | Sub + 3 Mid Bass empilhados |
| Atmosfera | **Pad em 0,06–0,07 de volume** = textura | 4 camadas de cordas em 0,34 |
| Dinâmica | entra/sai por clipe, seções de 8–16 | entra/sai por clipe, seções de 8–16 |
| Cor do topo | ruído (Noise Snare, Crash, Static) | sinceros + OTT no pluck |

---

## 5. Tradução para o estúdio (o que dá para pegar)

| Traço desejado | Mecanismo medido na referência | Como transplantar |
|---|---|---|
| **Minimal do Boris** = menos elementos, mais tempo | 802 notas em 250 compassos; 1 lead contínuo; harmonia de 2 notas | Pegar o **princípio**, não a track: **1 elemento contínuo** por seção + os outros entrando. Teste: isolar 1 faixa e deixá-la sozinha com kick/baixo por 16 compassos |
| **Peso do kick** | 2 camadas em uníssono (corpo 0,33 + ataque 0,20) | **Somar** camada de ataque em vez de trocar o kick; A/B kick atual × kick + camada de ataque |
| **Espessura de lead** | 4–5 camadas no MESMO MIDI, motores diferentes (Operator/Wavetable), volumes decrescentes | Duplicar o lead com segundo motor em −3 a −6 dB |
| **Ar (6–16 kHz)** | 4 camadas de cordas com HP 426 Hz + LP 19,8 kHz | Obter ar por camada de cordas, não por EQ no master; medir antes/depois |
| **Textura de pad** | pad em 0,06–0,07 de volume | Pad como **cor**, não como camada de acorde; abaixar e medir o low-mid de novo |
| **Master denso** | 2 glue + M/S + multibanda com +5 a +6,5 dB por banda + limiter +8,5 | Comparar com o master do projeto por medição de LUFS/true peak |

**Limite declarado:** nada aqui foi ouvido. Tudo é leitura de estrutura. As duas tracks são **remakes de fã**, não os projetos originais dos artistas — o nome do arquivo é a única prova de identidade da música, e nome não é prova. O que é `VERIFICADO` é a **estrutura do projeto**, não que ele soa igual ao disco.

---

## 6. O que NÃO serve

- **Monolink**: só `.fxp` (Serum 1) e um esqueleto de pastas. Sem projeto, sem MIDI.
- **Adriatique / Gravity**: só MIDI, sem `.als` e sem preset. Copiado como MIDI (112 arquivos) porque padrão rítmico ainda serve de referência.
- **Pressure**: 26 MIDI reais em 1.380 fragmentos; o resto nunca baixou.
- **`Kickstart` — lição de versão:** o projeto do Boris pede `Kickstart` (v1) e não aceita o `Kickstart 2` no lugar: são `BranchDeviceId`s diferentes (`device:vst:audiofx:1129204563` vs `1129204530`) — o Live não substitui sozinho, as instâncias abrem offline e ele oferece trocar o plugin. `VERIFICADO` por comparação de id contra o `<BranchDeviceId>` do `.als`.

---

## 7. Dois remakes novos (26/10)

Fonte: mesmo pacote de remakes (`.als` + presets + cfg + imagens; **sem os WAV/AIF** — abrem com mídia faltante). Nenhum áudio ouvido.

### 7.1 Purple Disco Machine & Sophie and the Giants — *Hypnotized*

**108 BPM · 40 pistas · 3.562 notas · 88,8 compassos.** 12 `.fxp` (Serum 1).

| Camada | Cadeia medida |
|---|---|
| Kick | `OriginalSimpler` (seco, sem EQ na pista) |
| Kick Intro | `OriginalSimpler` |
| Hat 1 / Hat 2 | `Simpler > Reverb > Eq8 > Compressor2` (Hat 2 acrescenta `Delay`) |
| Pre-Clap / Clap / Clap 2 | `Simpler > Reverb > Eq8` (+ `Delay` no Clap 2) |
| Snare / Snare Fill | `Simpler > Reverb > Eq8 > Delay` |
| Mid Bass | `Plugin > Eq8 > StereoGain > Compressor2` |
| Sub | `Plugin > Eq8 > Compressor2` |
| Chords / Note Add / Chords Filter | `Plugin > (Delay/Reverb) > Eq8 > Compressor2` |
| Arp | `Plugin > Reverb > Eq8 > Delay` |
| Guitars 1–4 | `Plugin` + `Eq8`; duas versões "Sampled" em `Simpler` com reverb/delay |
| Lead 1 / Lead 2 | `Plugin > Echo > Reverb > Eq8 > Compressor2` |
| Master | 2 racks: `GrainDelay > AutoFilter > Reverb > Eq8 > FilterDelay > Compressor2` e `Eq8 > Saturator > MultibandDynamics > GlueCompressor > Tube > Limiter` |
| Returns | `A-Reverb` (Reverb) · `B-Delay` (Delay) |

**Leitura:** é uma produção de disco house com **quase tudo sampleado e processado por pista** (hats com reverb próprio, claps com delay próprio), master com dois racks pesados e **zero returns de compressão**. Serve pelo desenho de guitarra/lead e pelo master em 2 racks — não pelo arranjo.

### 7.2 Sofi Tukker & John Summit — *Sun Came Up*

**124 BPM · 31 pistas · 2.084 notas · 107 compassos.** 8 `.fxp`.

| Camada | Cadeia medida |
|---|---|
| Kick | `OriginalSimpler` (seco) |
| Clap BUS | rack com **4 `OriginalSimpler` e 3 `Reverb`** |
| Clap / Snare / Hat / Hat Soft / Open Hat | `Simpler > Reverb/Eq8/StereoGain/Compressor2` |
| Guitar | `Plugin > Eq8 > Compressor2 > Saturator > Reverb > Plugin` |
| Lead | `Plugin > Compressor2 > Eq8 > Reverb > AutoFilter` |
| Piano | rack (`MidiVelocity > InstrumentGroup > StereoGain > Eq8 > GlueCompressor > Reverb`) + 2 `Eq8` + `Reverb` |
| Sub Bass | `Plugin > StereoGain > Compressor2 > Plugin` (dois plugins em série) |
| Whistle / Pluck / Pad | `Plugin > Compressor2/Reverb > Eq8` |
| Master | `Reverb` + rack `GlueCompressor > Saturator > MultibandDynamics > Limiter` |
| Returns | **nenhum** (tudo em insert) |

**Leitura:** é o oposto do Hypnotized — **sem returns, tudo por insert**, com `Clap BUS` empilhando quatro samplers. Serve como referência de "camada por insert" e de sub com dois plugins, não como arquitetura de mix.

**Relevância declarada:** as duas são house melódica/disco, **fora do gênero psytech**. O valor é o desenho de synth (guitarras, leads, plucks) e o A/B de cadeias — não o arranjo nem o groove. Nenhuma das duas serve como referência de arranjo.

**Limite:** mídia faltante e **nada foi ouvido**. O que é `VERIFICADO` é a estrutura do `.als`, não o som.
