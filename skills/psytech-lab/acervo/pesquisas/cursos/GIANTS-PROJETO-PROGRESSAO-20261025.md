# MELODIC TECHNO GIANTS (PML) — o projeto por dentro, estágio por estágio

**Fonte:** course files do curso PML Melodic Techno Giants (zip de 227 MB)
**Análise:** 25/10/2026 · **Método:** parse dos 5 `.als` (gzip/XML, leitura pura). Nada foi aberto no Live, nada foi ouvido.

Este é o único material do acervo inteiro que mostra **a mesma faixa em 5 estágios**, do template vazio ao master. Os números abaixo são medidos arquivo por arquivo.

---

## 1. A progressão em números

| Estágio | BPM | Pistas | MIDI / Áudio | Notas | Devices | Massive | Simpler | Returns | Fim (compasso) |
|---|---|---|---|---|---|---|---|---|---|
| **01 START 9.2** | 120 | 8 | 0 / 0 | 0 | 23 | 0 | 0 | 2 | 0 |
| **02 START 9.7** | 120 | 8 | 0 / 0 | 0 | 23 | 0 | 0 | 2 | 0 |
| **03 APOS VIDEO 09 BASS** | 122 | 35 | 14 / 12 | 81 | 118 | 1 | 13 | 4 | 32 |
| **04 FINAL** | 122 | 71 | 228 / 204 | 21,127 | 343 | 12 | 24 | 5 | 220 |
| **05 FINAL EDITADO** | 122 | 67 | 207 / 204 | 20,152 | 308 | 11 | 22 | 5 | 220 |

**Leitura direta:** a faixa cresce de **8 para 71 pistas**, de **0 para 21.127 notas** e de **23 para 343 devices**. O BPM sai de 120 (template) e fixa em **122**. O arranjo fecha em **220 compassos** — 7min13s a 122 BPM.

> `START 9.2` e `START 9.7` são **o mesmo arquivo**: mesmas 8 pistas, mesmos 23 devices, mesmos 30 envelopes. O 9.7 é só uma regravação de compatibilidade. Não há conteúdo novo entre eles.

---

## 2. Estágio 1 — o template (8 pistas)

O curso não começa do zero absoluto: começa de um template com **três canais MIDI idênticos, já processados**. A cadeia de cada um:

`EQ Eight → Chorus → Compressor → Compressor → Auto Filter → Utility`

Mais: `4 Doubler` (rack de áudio), `5 Reverb Tora`, `6 PML Pipe` (rack de instrumento) e **dois sends**: `A-Reverb` e `B-Delay`.

**O que isso ensina:** o curso parte de um canal *pronto para receber som* — EQ, dois compressores em série, filtro e ganho. Não é "insira um instrumento e toque"; é "o canal já está preparado".

---

## 3. Estágio 3 — depois do vídeo 09 (Bass): 35 pistas

Com 14 clips MIDI e 12 de áudio, **81 notas** e o arranjo até o **compasso 32** (8 compassos de música). É a fundação: bateria + primeiros graves.

O que aparece nesse estágio:

- **Bateria em pistas separadas, cada uma com um `Simpler`** — 13 Simplers. Não existe Drum Rack: kick, claps, hats, toms, rides e percussão têm **canal próprio**. Isso permite processar cada peça individualmente (em oposição ao costume de montar tudo num Drum Rack único).
- **Pista de sidechain (`1-SCKICK`)** com Simpler + cadeia completa — o kick que dispara o ducking.
- **11 pistas de FX/reverso** já no primeiro estágio: `FX Sound 1` ×2, `Reverse Clap`, `FX Ugh`, `Rev Cym`, `Fx Ahhh`, `Tok`…
- **Primeiro Massive** em `26 Massive Bass`, mais um segundo baixo em Simpler (`27 Massive Bass`).
- Os sends crescem de 2 para **4**: `A-Reverb | EQ Eight`, `B-Reverb - Torastyle`, `C-Delay`, `D-Ping Pong Delay`.

---

## 4. Estágio 4 — o Final: 71 pistas, 21.127 notas

**228 clips MIDI + 204 clips de áudio**, **21,127 notas**, **12 instâncias de Massive**, **24 Simplers**, **2 grupos** e **5 returns**. Arranjo até o compasso **220**.

### 4.1 A cadeia de master (o achado mais copiável)

O master tem **dois racks em série**, mais EQ e Utility:

1. **Rack 1** — `Ping Pong Delay + Reverb + Auto Filter` (espaço no master)
2. `EQ Eight`
3. `Utility`
4. **Rack 2 (mastering)** — `EQ Eight → Chorus → Glue Compressor → EQ Eight → Multiband Dynamics → Compressor → Compressor → EQ Eight → Limiter → Limiter`

São **10 devices de masterização** dentro de um rack, com **dois limiters em série**. O master não é "um Limiter no fim": é uma cadeia montada.

### 4.2 Os 5 sends e a função de cada um

| Send | Cadeia | Função |
|---|---|---|
| **A-Reverb** | Reverb → Compressor → Auto Filter | reverb principal, comprimida e filtrada |
| **B-Torastyle** | **Toraverb** (plugin de terceiro) + Reverb | reverb de caráter, com plugin externo |
| **C-Subtile** | **Chorus** | o send mais estranho: um chorus como ambiente sutil |
| **D-Delay** | Cross Delay + Ping Pong Delay | delay duplo em série |
| **E-Ping Pong** | Ping Pong Delay | delay rítmico isolado |

Compare com o Tim Engelhardt: lá eram 4 sends com duas reverbs de tamanhos diferentes; aqui são 5, com **delay duplo**, **reverb de plugin** e **chorus como ambiente**. Duas escolas, mesma lógica: espaço vem de send, não de device no canal.

### 4.3 As 71 pistas do Final

| # | Pista | Tipo | Devices (cadeia) | MIDI | Áudio |
|---|---|---|---|---|---|
| 1 | SC | MIDI | OriginalSimpler | 3 |  |
| 2 | 2 Kick | Áudio | Eq8 |  | 21 |
| 3 | 3 High Kick | Áudio | StereoGain, Eq8, AutoFilter, StereoGain |  | 18 |
| 4 | 4 Drums | Grupo | Reverb |  |  |
| 5 | 5 Perc Clap | MIDI | OriginalSimpler, Compressor2, AutoFilter, Eq8, StereoGain | 13 |  |
| 6 | 6 Clap | MIDI | OriginalSimpler, Compressor2, AutoFilter, StereoGain | 10 |  |
| 7 | 7 High Clap | MIDI | OriginalSimpler, Compressor2, AutoFilter, StereoGain | 10 |  |
| 8 | 8 Clap Dark | MIDI | OriginalSimpler, Compressor2, Compressor2, RACK[2](FilterDelay+Chorus+StereoGain+FilterDelay+Chorus+StereoGain | 11 |  |
| 9 | 9 Closed | MIDI | RACK[1](OriginalSimpler+Compressor2+Vinyl+AutoFilter+Reverb+Eq8+Eq8+Chorus) | 9 |  |
| 10 | 10 OHH | MIDI | OriginalSimpler, Compressor2, Chorus, AutoFilter, Eq8 | 12 |  |
| 11 | 11 Loop Cut | Áudio | Compressor2, Vinyl, Eq8 |  | 6 |
| 12 | 12 FXTOMS | MIDI | OriginalSimpler, Compressor2, Eq8, Eq8, Chorus, AutoFilter | 4 |  |
| 13 | 13 Perc FX | MIDI | OriginalSimpler, Vinyl, Erosion, AutoFilter | 3 |  |
| 14 | 14 Ride end | MIDI | OriginalSimpler, Eq8 | 3 |  |
| 15 | 15 Audio Perc | Áudio | Eq8 |  | 23 |
| 16 | 16 Cymb Short | MIDI | OriginalSimpler, Compressor2, Eq8, AutoFilter, RACK[2](FilterDelay+Chorus+StereoGain+FilterDelay+Chorus+Stereo | 1 |  |
| 17 | 17 Ride short | MIDI | OriginalSimpler, Compressor2, AutoFilter, Reverb, Eq8, CrossDelay | 2 |  |
| 18 | 18 FX RVCym | Áudio | Vinyl, Eq8, Reverb |  | 10 |
| 19 | 19 FXCAH | Áudio | AutoFilter, Reverb |  | 13 |
| 20 | 20 REV CLAP | Áudio | RACK[2](FilterDelay+Chorus+StereoGain+FilterDelay+Chorus+StereoGain), Eq8 |  | 35 |
| 21 | 21 FX09 | Áudio | Erosion, Eq8 |  | 16 |
| 22 | 22 FX07 | Áudio | Eq8 |  | 7 |
| 23 | 23 FX03 | Áudio | Reverb, Eq8 |  | 3 |
| 24 | 24 Tok | Áudio | Reverb, AutoFilter, Eq8 |  | 7 |
| 25 | 25 Massive White | MIDI | Massive, Eq8, AutoFilter, StereoGain, Compressor2 | 19 |  |
| 26 | 26 Massive White 2 | MIDI | Massive, Compressor2, Eq8, AutoFilter, StereoGain | 9 |  |
| 27 | 27 ZZZZT | Áudio | Eq8 |  | 8 |
| 28 | 28 REV CL | Áudio | Eq8 |  | 4 |
| 29 | 29 BASS Deep | MIDI | OriginalSimpler, Eq8, AutoFilter, AutoFilter | 1 |  |
| 30 | 30 FXImpact | Áudio | AutoFilter |  | 2 |
| 31 | 31 Clap FX | Áudio | AutoFilter, AutoPan, Eq8 |  | 5 |
| 32 | 32 Reverse Scratch | Áudio | AutoFilter, Eq8 |  | 1 |
| 33 | 33 Clap FX | Áudio | AutoFilter, AutoPan, Eq8 |  | 6 |
| 34 | 34 Clap FX | Áudio | AutoFilter |  | 1 |
| 35 | 35 PING | Áudio | Reverb, Eq8 |  | 2 |
| 36 | 36 Open Hihat | MIDI | OriginalSimpler, Compressor2, AutoFilter, Reverb, Eq8, StereoGain, StereoGain | 2 |  |
| 37 | 37 Fast Hat | MIDI | OriginalSimpler, Eq8, Compressor2, AutoFilter, CrossDelay | 2 |  |
| 38 | 38 Ride | MIDI | OriginalSimpler, AutoFilter, Eq8, Reverb, CrossDelay, StereoGain | 6 |  |
| 39 | 39 FXTOMS2 | MIDI | OriginalSimpler, Compressor2, AutoFilter, Eq8, StereoGain | 1 |  |
| 40 | 40 REV BLOP | Áudio | Compressor2, Eq8, StereoGain |  | 1 |
| 41 | 41 REV WUUT | Áudio | StereoGain, Eq8, Compressor2 |  | 8 |
| 42 | 42 Bass Preda Sub alt1 | MIDI | Massive, Compressor2, Compressor2, Eq8, Eq8, StereoGain, StereoGain, StereoGain, Eq8 | 4 |  |
| 43 | 43 Bass Preda click | MIDI | OriginalSimpler, Compressor2, StereoGain, StereoGain, StereoGain, Eq8 | 5 |  |
| 44 | 44 Track Group | Grupo |  |  |  |
| 45 | 45 Massive Delay FX | MIDI | Massive, Compressor2, AutoFilter, Eq8, StereoGain | 3 |  |
| 46 | 46 Stabs | MIDI | OriginalSimpler, Eq8, AutoFilter, Reverb, PingPongDelay, StereoGain, StereoGain, Compressor2 | 7 |  |
| 47 | 47 Stabs Support | MIDI | OriginalSimpler, Eq8, Compressor2, AutoFilter, Eq8, StereoGain, StereoGain | 2 |  |
| 48 | 48 Main Stab | MIDI | OriginalSimpler, Compressor2, RACK[2](FilterDelay+Chorus+StereoGain+FilterDelay+Chorus+StereoGain), FrequencyS | 6 |  |
| 49 | 49 Main Stab copy | MIDI | RACK[15](OriginalSimpler+OriginalSimpler+OriginalSimpler+OriginalSimpler+OriginalSimpler+OriginalSimpler+Origi | 6 |  |
| 50 | 50 Chordstab | MIDI | OriginalSimpler, RACK[2](FilterDelay+Chorus+StereoGain+FilterDelay+Chorus+StereoGain), FrequencyShifter, AutoF | 3 |  |
| 51 | 51 Chordstab copy | MIDI | RACK[15](OriginalSimpler+OriginalSimpler+OriginalSimpler+OriginalSimpler+OriginalSimpler+OriginalSimpler+Origi | 3 |  |
| 52 | 52 Massive Pad Bass | MIDI | Massive, Compressor2, Compressor2, RACK[1](AutoFilter+AutoFilter+Eq8), StereoGain, StereoGain, StereoGain | 6 |  |
| 53 | 53 Massive Arp | MIDI | Massive, Compressor2, Compressor2, Reverb, FrequencyShifter, Eq8, Eq8, Eq8, AutoFilter, PingPongDelay, StereoG | 11 |  |
| 54 | 54-Massive | MIDI | Massive, Redux, Overdrive, Eq8, StereoGain, CrossDelay, Chorus, Compressor2, Compressor2, AutoFilter, StereoGa | 1 |  |
| 55 | 55 Massive Arp Support | MIDI | Massive, Compressor2, RACK[2](FilterDelay+Chorus+StereoGain+FilterDelay+Chorus+StereoGain), Compressor2, Frequ | 1 |  |
| 56 | 56 Reversed | MIDI | OriginalSimpler, FrequencyShifter, Saturator, Vinyl, Eq8, StereoGain, StereoGain | 2 |  |
| 57 | 57 ABS Pipe 1 FX | MIDI | OriginalSimpler, Compressor2, RACK[2](FilterDelay+Chorus+StereoGain+FilterDelay+Chorus+StereoGain), AutoFilter | 7 |  |
| 58 | 58 ABS Pipe 1 FX copy | MIDI | RACK[15](OriginalSimpler+OriginalSimpler+OriginalSimpler+OriginalSimpler+OriginalSimpler+OriginalSimpler+Origi | 7 |  |
| 59 | 59-Balafon-1 | MIDI | OriginalSimpler, RACK[2](FilterDelay+Chorus+StereoGain+FilterDelay+Chorus+StereoGain), FrequencyShifter, Erosi | 1 |  |
| 60 | 60 Massive BG Pads | MIDI | Massive, Eq8, AutoFilter, AutoFilter, RACK[2](FilterDelay+Chorus+StereoGain+FilterDelay+Chorus+StereoGain), Re | 12 |  |
| 61 | 61 Massive BG Pads | MIDI | Massive, Eq8, Chorus, AutoFilter, AutoFilter, AutoFilter, RACK[2](FilterDelay+Chorus+StereoGain+FilterDelay+Ch | 1 |  |
| 62 | 62 Massive FX Bass | MIDI | MidiPitcher, Massive, Eq8, Chorus, Compressor2, Compressor2, AutoFilter, StereoGain | 3 |  |
| 63 | 63 Massive Tonal FX | MIDI | Massive, GlueCompressor, AutoFilter, AutoPan, Eq8, Reverb, Compressor2, StereoGain, StereoGain | 16 |  |
| 64 | 64 LFO Audio FX | Áudio | Eq8, StereoGain, StereoGain, Compressor2 |  | 2 |
| 65 | 65 LFO RecNausia 2 | Áudio | Eq8, StereoGain |  | 5 |
| 66 | 66 Space | Áudio | Eq8, Compressor2, Compressor2, StereoGain |  |  |
| 67 | A-Reverb | Compressor | Auto Filter | Return | Reverb, Compressor2, AutoFilter |  |  |
| 68 | B-Torastyle | Reverb - Torastyle | Return | Toraverb, Reverb |  |  |
| 69 | C-Subtile | Return | Chorus |  |  |
| 70 | D-Delay | Ping Pong Delay | Return | CrossDelay, PingPongDelay |  |  |
| 71 | E-Ping Pong Delay | Return | PingPongDelay |  |  |

### 4.4 Onde está o peso (clips por pista)

| Pista | Clips | Notas | Por quê |
|---|---|---|---|
| 20 REV CLAP | 35 | 0 | reversos de clap — a pista mais carregada do projeto, e é **só áudio** |
| 15 Audio Perc | 23 | 0 | percussão renderizada |
| 2 Kick | 21 | 0 | o kick é áudio, não Simpler — já renderizado |
| 25 Massive White | 19 | 199 | o baixo principal em Massive |
| 3 High Kick | 18 | 0 | cópia de kick com filtro |
| 21 FX09 | 16 | 0 | FX com Erosion |
| 63 Massive Tonal FX | 16 | 37 | FX tonal em Massive |
| 5 Perc Clap | 13 | 1,534 | 1.534 notas de percussão |

**O dado que mais impressiona:** `20 REV CLAP` tem **35 clips de áudio** — mais que qualquer instrumento. O reverso de clap é usado como **peça estrutural de transição**, não como enfeite.

---

## 5. Estágio 5 — o Final Editado (o que sai)

| | Final | Final Editado | Diferença |
|---|---|---|---|
| Pistas | 71 | 67 | −4 |
| Clips MIDI | 228 | 207 | −21 |
| Notas | 21,127 | 20,152 | −975 |
| Devices | 343 | 308 | −35 |
| Massive | 12 | 11 | −1 |
| Envelopes | 137 | 135 | −2 |

O "Work Course Edits" é a versão usada em aula: **4 pistas menos e 975 notas menos**. As pistas removidas são duplicatas de suporte (`49 Main Stab copy`, `58 ABS Pipe 1 FX copy`, `28 REV CL`, `30 FXImpact`) — exatamente o tipo de camada que existe na produção mas não se explica em vídeo.

---

## 6. Os 7 padrões que o projeto revela

### 6.1 Bateria em pistas separadas, nunca em Drum Rack
24 Simplers, um por peça: kick, high kick, três claps, dois hats fechados, open hat, fast hat, ride, ride curto, três toms, cymbal, perc 1 e 2, tomtom. Cada um com cadeia própria. **Você processa a peça, não o kit.**

### 6.2 Kick em áudio, não em instrumento
`2 Kick` e `3 High Kick` são **AudioTracks** com EQ Eight e Auto Filter. O kick foi renderizado e depois esculpido — não é Simpler tocando sample. É a diferença entre "ajustar o sample" e "esculpir o áudio".

### 6.3 Reversos como estrutura
`20 REV CLAP` (35 clips), `22 FX07`, `28 REV CL`, `40 REV BLOP`, `41 REV WUUT`, `32 Reverse Scratch`, `18 FX RVCym`. O projeto usa **reverso de áudio** como sinal de transição em quase toda fronteira de seção.

### 6.4 Stabs em seis camadas para uma ideia
`46 Stabs` · `47 Stabs Support` · `48 Main Stab` · `49 Main Stab copy` · `50 Chordstab` · `51 Chordstab copy` — seis pistas com `Frequency Shifter` em quase todas. O stab não é um som: é um **empilhamento com deslocamento de frequência**.

### 6.5 Massive para tudo que é sintético
12 instâncias: `Massive White` (×2), `Massive Delay FX`, `Bass Preda Sub alt1`, `Massive Pad Bass`, `Massive Arp`, `Massive Arp Support`, `Massive BG Pads` (×2), `Massive FX Bass`, `Massive Tonal FX`, `54-Massive`. Contra 24 Simplers para material amostrado — a divisão é clara: **síntese no Massive, percussão em sample**.

### 6.6 Grupos mínimos
Só **2 grupos** em 71 pistas (`4 Drums` e `44 Track Group`). O projeto não organiza por pasta; organiza por **nome numerado**. O número na frente da pista é a ordem de criação.

### 6.7 Sends com processamento, não só reverb
Nenhum send é reverb puro. **A** tem compressor e filtro; **B** tem plugin de terceiro; **C** é chorus; **D** é delay duplo. O send é tratado como **canal de efeito**, não como "molho".

---

## 7. O que o Giants ensina, por padrão

| Padrão do Giants | Ganho estimado |
|---|---|
| Kick e percussão em pista própria com cadeia | já é prática comum (kick, hats separados) — |
| Reversos de áudio como transição | **alto** — o curso usa 7 pistas para isso |
| 5 sends com processamento | **alto** — espaço vem do send, não de FX dentro do synth |
| Rack de masterização com 2 limiters | médio — pendente de verificação em cada projeto |
| Stab em 6 camadas com Frequency Shifter | médio (depende do arranjo) |
| Massive para síntese | baixo (Serum cobre) |

**A conclusão honesta:** o que o Giants ensina de mais valioso não é timbre nem plugin — é **arquitetura de sessão**. 71 pistas para uma faixa de 7 minutos, com pista dedicada para cada peça, cada reverso e cada camada de stab.

---

## 8. Limites

- Nada foi aberto no Live; nenhuma pista foi ouvida. Tudo é leitura de XML.
- Os `.als` são de **Live 9.2/9.7** (2016). Abrir no Live 12 pode gerar aviso de versão; a mídia está no zip, então não deve faltar sample.
- O curso usa **Massive 1**; sem ele instalado (só o Massive X), as 12 instâncias vão abrir vazias ou como device ausente.
- `Toraverb` (send B) é plugin de terceiro; sem ele instalado, esse send abre sem o efeito.
- A contagem de devices inclui os que estão desligados.
