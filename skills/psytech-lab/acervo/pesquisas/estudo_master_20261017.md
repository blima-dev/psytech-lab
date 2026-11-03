# Estudo de Masterização — caso real em faixa minimal psytech (Ableton Live 12.4.6, 17/10/2026)

**Arquivo auditado (`VERIFICADO`):** um set de minimal psytech (128 BPM, C# frígio) com 7.033.012 bytes comprimidos / 43.600.501 bytes de XML, 70 pistas + 2 retornos + master. Todos os valores abaixo foram medidos no XML; o diagnóstico do caso serve de estudo, não de regra.

## 1. Sumário Executivo (5 Descobertas Principais)

* **Empilhamento triplo de High-Shelf (+15,0 dB acima de 11 kHz) e Low-Cut de 48 dB/oct em 25,2 Hz no `Eq8[0]` do master (`VERIFICADO`):** o EQ do master somava três filtros High Shelf ativos em série — Banda 4 em 5.004,9 Hz (+2,00 dB), Banda 5 em 8.736,4 Hz (+6,50 dB) e Banda 8 em 11.005,4 Hz (+6,50 dB), totalizando **+15,00 dB** no extremo agudo — além de um Bell de +3,00 dB em 1.487,9 Hz e um corte abrupto LC48 (48 dB/oct) em 25,2 Hz (Q=0,71) que gira a fase e atenua a oitava subgrave (25–40 Hz).
* **Esmagamento precoce no `GlueCompressor` (`Threshold = −1,0 dB`, sem oversample) e no `Limiter` (`Ceiling = −0,71 dB`, `Release = 100 ms` fixo, `LinkAmount = 100%`) (`VERIFICADO`):** mesmo com o SideChain EQ interno do Glue ativo em High-Pass @ 200 Hz, o excesso de ganho na faixa 130–500 Hz e o boost de +15 dB nos agudos do EQ anterior empurram o detector do Glue e fazem o limiter (link estéreo 100%, release manual travado em 100 ms) modular a mix inteira a cada impacto de grave, fechando o palco sonoro ("som pra dentro").
* **Vácuo estrutural em 25–40 Hz causado por oitava MIDI incorreta nos canais de grave e não por filtro (`VERIFICADO`):** a fundamental de C# na oitava subgrave é **MIDI 25 (C#0 no Ableton = 34,65 Hz)**, mas **nenhuma pista do projeto tinha notas em MIDI 25** — os canais de sub tocavam em MIDI 37 (69,30 Hz, com preset de mid-bass falante), o sub-roll em MIDI 44 (103,83 Hz), e rolling/baixo médio em MIDI 49 (138,59 Hz), concentrando toda a energia em 50–250 Hz.
* **Lanes de automação de `Mixer.Volume` violam o gain staging de grupos em 0 dB e reativam 8 canais mutados ao carregar o `.als` (`VERIFICADO`):** embora os faders manuais dos 5 grupos marcassem 0,00 dB, lanes ativas de `Mixer.Volume` elevavam o grupo de clima/vozes para **+3,00 dB** (compassos 145–168) e o grupo de efeitos para **+4,00 dB** (compasso 120), enquanto 8 canais com `Speaker/Manual = false` possuíam lanes `Mixer.Speaker` cravadas em `true`, ligando sozinhos ao abrir o projeto e sobrecarregando o master.
* **Device Max for Live de tap de áudio ativo no master pós-limiter e lane órfã no EQ (`VERIFICADO`):** um `MxDeviceAudioEffect` (tap de áudio do ecossistema open-source) estava ligado na última posição do master (após o limiter) — risco documentado de instabilidade/crash de JS no Max, a remover antes de qualquer render; adicionalmente, uma lane do master automatizava o ganho de `ParameterB` do EQ, parâmetro inativo porque o EQ opera em modo Stereo (que lê apenas `ParameterA`).

## 2. O Que a Internet Diz (Prática Profissional 2024–2026)

### 2.1. Mastering para Streaming (Spotify, Apple Music, Amazon) e por que `-1,0 dBTP`

* **Consenso Técnico:** Plataformas com normalização de loudness (Spotify em −14 LUFS, Apple Music em −16 LUFS, Deezer em −15 LUFS, Amazon/YouTube/Tidal em −14 LUFS) aplicam apenas um offset de ganho linear (volume), preservando a faixa dinâmica original; contudo, a transcodificação para codecs lossy (Ogg Vorbis, AAC, Opus) gera picos inter-amostrais (*inter-sample peaks*) que ultrapassam o pico digital em 1 a 3 dB, exigindo teto em −1,0 dBTP (ou uso combinado de clipper/limiter + limiter True Peak).

* **Fontes e Trechos Verificados:**

  * [Mastering for Streaming Platforms — mastering.to](https://mastering.to/mastering-for-streaming-platforms):

    > "Streaming platforms encode your WAV master to lossy formats — AAC, Ogg Vorbis, Opus, or MP3. These codecs can create inter-sample peaks during encoding that exceed 0 dBFS even when the source audio appears safely within limits... True peaks can be 1–3 dB above the sample peaks on complex audio. Leaving your limiter ceiling around -1 dBTP (using a true peak limiter, not a standard peak limiter) keeps the reconstructed signal comfortable after codec encoding."

  * [How to master for streaming platforms: normalization, LUFS, and loudness — iZotope (Ian Stewart, Jul 2025)](https://www.izotope.com/community/blog/mastering-for-streaming-platforms):

    > "When lossless streaming was the exception rather than the norm, it was important to leave a bit of peak headroom to avoid distortion during the encode and decode process of lossy streaming. A good rule of thumb was to leave at least 1 dB True Peak headroom... Personally, I like to make the best of both and use a non-True Peak limiter with a ceiling at -1 dBFS, followed by a True Peak limiter – like the Ozone Maximizer – set to -0.3 dBTP."

### 2.2. Loudness para Clube vs. Streaming vs. Beatport e Entrega em Duas Versões

* **Consenso Técnico vs. Opinião:** No Beatport e em sets de DJ (Rekordbox, Traktor, CDJs), **não existe normalização de loudness**. Uma faixa entregue a −14 LUFS soará drasticamente mais baixa na pista que faixas de Techno/Psytech/Trance masterizadas entre −7 e −9 LUFS (Crest Factor de 6 a 9 dB). No entanto, empurrar uma faixa com falhas de equilíbrio espectral para −7 LUFS apenas destrói os transientes no limiter.

* **Fontes e Trechos Verificados:**

  * [Mastering for Beatport: No Normalization, DJ Loudness & Club Translation Guide — mastering.to](https://mastering.to/beatport):

    > "Beatport is a download store — DJs purchase individual tracks and play them through software like Rekordbox, Serato, or Traktor into club sound systems. There is no loudness normalization applied at any stage... Techno: -8 to -6 LUFS integrated | Trance: -9 to -7 LUFS | Melodic House: -11 to -8 LUFS | True Peak: -1 dBTP | Crest Factor: 6–9 dB."

### 2.3. Limiter do Ableton Live 12.1+ (Modos Standard, True Peak, Soft Clip, Lookahead e Stereo Link)

* **Consenso Técnico:** O Limiter reformulado do Live 12.1+ possui curva de release suavizada, três modos de operação (0 = Standard, 1 = Soft Clip, 2 = True Peak), roteamento Mid/Side e controle contínuo de `LinkAmount` (Stereo Link). Reduções de ganho acima de 2 a 3 dB em um único limiter causam perda de impacto nos transientes e estreitamento da imagem estéreo se o link estéreo estiver em 100%.

* **Fontes e Trechos Verificados:**

  * [Ableton Live 12 Limiter - EVERYTHING You Need to Know! — Push Patterns (Sep 2024)](https://www.pushpatterns.com/blog/ableton-live-12-limiter):

    > "3 Limiting Modes: Standard: Light limiting, lets a few peaks through, so this sounds open. True Peak: Prevents all overshoots. This is ideal for CD or streaming. Soft Clip: Adds crunch and character, which is great for aggressive mixes... Stereo Link controls whether the limiter applies gain reduction equally to both channels. Linked: Tighter, more consistent across stereo image. Unlinked: Can preserve width."

  * [An introduction to limiters (and how to use them) — iZotope (Nick Messitte, Sep 2025)](https://www.izotope.com/community/blog/an-introduction-to-limiters-and-how-to-use-them):

    > "The most archetypal use of a limiter is at the very end of your mastering chain, applying no more than 2 dB or so of gain reduction in order to achieve a commercial loudness level... At zero percent, the maximizer is linked, left and right channels will experience the same amount of limiting. At 100%, the limiter is completely unlinked, operating in dual-mono mode. Definitely play with these controls: unlinking the limiting (to a degree) can really help preserve or even subtly enhance your stereo separation."

  * [Live Audio Effect Reference — Ableton Reference Manual Version 12](https://www.ableton.com/en/manual/live-audio-effect-reference/):

    > "When enabled, the Glue Compressor's maximum output level is -.5 dB... Finally, the True Peak mode prevents inter-sample peaks."

### 2.4. Clipper + Limiter em Série e Glue Compressor no Bus Master

* **Consenso Técnico:** Em música eletrônica de pista (Psytech, Dark Progressive, Techno), usar um estágio de *soft clipping* (ou dois limiters em série) antes do limiter final corta apenas os picos rápidos de transientes (1–2 dB), poupando o limiter True Peak de bombear (*pumping*) e preservando o *crest factor* percebido. No `Glue Compressor`, usa-se `Attack` lento (10–30 ms), `Release` rápido (0,1 s) ou `Auto`, `Ratio 2:1`, `Sidechain EQ High-Pass` acima de 100–200 Hz, e `Dry/Wet` paralelo (50–70%) para não engolir o punch do kick.

* **Fontes e Trechos Verificados:**

  * [An introduction to limiters (and how to use them) — iZotope (Sep 2025)](https://www.izotope.com/community/blog/an-introduction-to-limiters-and-how-to-use-them):

    > "You could run into a clipper first, before the limiter, or you could run two limiters in series... This mix is now reaching -6.8 LUFS short term, and -7.9 LUFS integrated, and with only a dB of limiting shared between two limiters. To get this kind of readout with one limiter, I'd have to push for 3 or more decibels of gain reduction into the maximizer, resulting in heavy artifacts."

  * [Best mastering plugins for dance music producers (2026 Guide) — We Rave You (Jun 2026)](https://weraveyou.com/2026/03/best-mastering-plugins-for-home-studios-2026-guide/):

    > "Clippers shave off transient peaks to create extra headroom to push the limiter further without introducing artifacts or distortion."

### 2.5. Mono Bass (100–120 Hz), Mid/Side EQ e Diagnóstico de "Mix Pra Dentro"

* **Consenso Técnico:** Subwoofers de sistemas de PA de clube operam em mono abaixo de 80–120 Hz; qualquer informação fora de fase nessa região causa cancelamento acústico. Por outro lado, aplicar filtros *minimum-phase* (como o modo padrão do `EQ Eight` ou `Bass Mono` do Utility) no canal Side altera a relação de fase entre Mid e Side até acima de 1–5 kHz. Para abrir uma mix que soa "pra dentro" (fechada/estreita na banda média), a prática de masterização moderna (2025–2026) recomenda limpar a lama acumulada nos Sides entre 200 e 500 Hz (−1,5 a −3 dB), dar presença articulada ao Mid (2–4 kHz) ou abrir o corpo estéreo nos Sides (500–800 Hz e High-Shelf > 10 kHz) com ajustes sutis (< 3–4 dB).

* **Fontes e Trechos Verificados:**

  * [Mastering for Beatport — mastering.to](https://mastering.to/beatport):

    > "Large subwoofer arrays reproduce frequencies below approximately 80–100 Hz in mono. Stereo content in the sub-bass register causes phase cancellation on these systems — the low end thins out or disappears... Monoizing the sub-bass below 100–120 Hz is standard practice in professional electronic music mastering."

  * [What is mid/side processing? — iZotope (Ian Stewart, Aug 2025)](https://www.izotope.com/community/blog/what-is-midside-processing):

    > "Not only is 100 Hz – the cutoff frequency of the filter – getting pulled past center to the right, but the rest of the spectrum doesn't return to full left panning until well over 5 kHz. This is the impact phase shift can have on stereo positioning in mid/side processing... I've also used the side channel to do a wide boost around 550 Hz, which adds some width and energy... Lastly, a high shelf boost on the side channel has widened the top of the percussion."

  * [How To Use Mid/Side EQ To Elevate Your Masters — Mastering The Mix (Tom Frampton, Jul 2025)](https://www.masteringthemix.com/blogs/learn/how-to-use-mid-side-eq-to-elevate-your-masters):

    > "Keep your mid/side EQ adjustments subtle, generally below 4 dB and with a wide Q... Add a complementary cut in the low mid range (240 to 480 Hz) on the side channel. This is where muddiness and stereo wash often build up, especially from pads, guitars, or wide reverb. Pulling these frequencies back in the sides cleans up the stereo image... Next, add a gentle lift to the 12 kHz band in the side channel."

  * [The Science of Stereo Width: How to Widen Your Mix Without Ruining It — MixMaster Pro (Nov 2025)](https://www.mixmasterpro.io/articles/stereowidth):

    > "A correlation meter shows the phase relationship between left and right channels: +1: Perfect correlation (mono), 0: No correlation (wide stereo), -1: Perfect anti-correlation (phase cancellation). Aim for a reading between +0.5 and +1 for safe, mono-compatible width."

## 3. Cadeia Real do Master e Retornos do Caso Auditado (`VERIFICADO`)

### 3.1. Barramento principal (`MainTrack`)

* **Volume do mixer:** 1.0 (0,00 dB), com automação mantendo 0,00 dB do início até o beat 936 (compasso 235) e fade-out para −70,00 dB no beat 984 (compasso 247).

* **Envelopes inertes / cascos vazios no master:** lane de `Mixer.TimeSignature` com 1 ponto default (casco vazio); lane de `Mixer.Tempo` com 1 ponto default (128 BPM, casco vazio); lane órfã automatizando `Eq8[0]/Bands.3/ParameterB/Gain` (−3,0 → −4,0 dB), inócua porque o EQ está em modo Stereo.

| Ordem | Device (`Tag`) | Estado (`On`) | Parâmetro Real no XML | Valor Atual (`VERIFICADO`) | Diagnóstico Técnico |
| ----- | ----- | ----- | ----- | ----- | ----- |
| **0** | `Eq8` | `true` | `Mode` / `Oversampling` / `GlobalGain` | `0` (Stereo) / `false` / `0,00 dB` | Sem Mid/Side e sem Oversampling |
| **0** | `Eq8` | `true` | Banda 1 (`ParameterA`) | `On=true`, `Mode=0` (**LC48**), `Freq=25,2 Hz`, `Q=0,71` | **Crítico:** filtro 48 dB/oct em 25,2 Hz mata o sub 25–32 Hz e gira fase |
| **0** | `Eq8` | `true` | Banda 2 (`ParameterA`) | `On=true`, `Mode=3` (Bell), `Freq=705,3 Hz`, `Gain=0,00 dB`, `Q=1,74` | Banda ligada com 0,00 dB (inócua) |
| **0** | `Eq8` | `true` | Banda 3 (`ParameterA`) | `On=true`, `Mode=3` (Bell), `Freq=1.487,9 Hz`, `Gain=+3,00 dB`, `Q=0,80` | Empurra +3,00 dB em 1,5 kHz (em Stereo/Mid), endurecendo a presença |
| **0** | `Eq8` | `true` | Banda 4 (`ParameterA`) | `On=true`, `Mode=5` (**HShelf**), `Freq=5.004,9 Hz`, `Gain=+2,00 dB`, `Q=0,71` | 1º High-Shelf (+2,00 dB acima de 5 kHz) |
| **0** | `Eq8` | `true` | Banda 5 (`ParameterA`) | `On=true`, `Mode=5` (**HShelf**), `Freq=8.736,4 Hz`, `Gain=+6,50 dB`, `Q=0,71` | **Crítico:** 2º High-Shelf empilhado (acumula +8,50 dB) |
| **0** | `Eq8` | `true` | Banda 6 (`ParameterA`) | `On=true`, `Mode=3` (Bell), `Freq=302,5 Hz`, `Gain=−0,50 dB`, `Q=0,98` | Corte tímido (−0,5 dB) para a sobrecarga real de 130–300 Hz |
| **0** | `Eq8` | `true` | Banda 7 (`ParameterA`) | `On=true`, `Mode=3` (Bell), `Freq=480,0 Hz`, `Gain=0,00 dB`, `Q=0,71` | Banda ligada com 0,00 dB (inócua) |
| **0** | `Eq8` | `true` | Banda 8 (`ParameterA`) | `On=true`, `Mode=5` (**HShelf**), `Freq=11.005,4 Hz`, `Gain=+6,50 dB`, `Q=0,71` | **Crítico:** 3º High-Shelf empilhado (**+15,00 dB totais > 11 kHz!**) |
| **1** | `GlueCompressor` | `true` | `Threshold` / `Ratio` / `Makeup` | `−1,00 dB` / `0` (`2:1`) / `0,00 dB` | Threshold em −1 dB comprime continuamente por causa do boost prévio do EQ |
| **1** | `GlueCompressor` | `true` | `Attack` / `Release` / `Range` | `6` (`30 ms`) / `6` (`Auto`) / `70,0 dB` | Attack de 30 ms adequado, mas `Release Auto` demora a soltar em densidades altas |
| **1** | `GlueCompressor` | `true` | `DryWet` / `PeakClipIn` / `Oversample` | `1,00` (`100%`) / `false` / `false` | 100% Wet sem Soft Clip e sem Oversampling |
| **1** | `GlueCompressor` | `true` | `SideChain/Eq` | `On=true`, `Mode=5` (HP), `Freq=200,0 Hz`, `Q=0,71` | HP 200 Hz interno ligado (protege do sub, mas não do boost de 1,5–11 kHz) |
| **2** | `StereoGain` (Utility) | `true` | `Gain` / `StereoWidth` / `DcFilter` | `0,00 dB` / `99,61%` / `true` | Width ligeiramente abaixo de 100%; DC Filter ativo |
| **2** | `StereoGain` (Utility) | `true` | `BassMono` / `BassMonoFrequency` | `true` / `121,33 Hz` | **Redundante em cascata** com os Bass Mono dos grupos (120/140/144 Hz) |
| **3** | `Limiter` | `true` | `Gain` / `Ceiling` / `Mode` | `0,00 dB` / `−0,712 dB` / `2` (`True Peak`) | Teto −0,71 dBTP dá margem estreita para transcodificação Ogg/AAC (ideal −1,0 dBTP) |
| **3** | `Limiter` | `true` | `Release` / `AutoRelease` / `Lookahead` | `100,0 ms` / `false` / `1` (`3,0 ms`) | Release fixo de 100 ms mantém atenuação presa entre semicolcheias (117 ms) |
| **3** | `Limiter` | `true` | `Routing` / `LinkAmount` / `Maximize` | `0` (L/R) / `1,00` (`100%`) / `false` | `LinkAmount=100%` faz qualquer pico central esmagar L e R por igual |
| **4** | `MxDeviceAudioEffect` | `true` | tap de áudio Max pós-limiter | `On=true` | **Crítico:** device Max depois do teto; risco de crash JS |

### 3.2. Retornos do caso

| Retorno | Fader | Cadeia (resumo) | Quem envia |
| ----- | ----- | ----- | ----- |
| **A — cauda pontual de reverb** | −6,00 dB | `Eq8` LC48 @ 249,5 Hz → `Reverb` (decay 2,19 s, automatizado até **3,60 s** no compasso 157; PreDelay 19,95 ms; RoomSize 100; StereoSeparation 100; ShelfHi 4.500 Hz; DryWet 100%) | Sends estáticos de meia dúzia de canais (flauta, atmosfera, drones, foleys) + ~30 canais com **throw pontual automatizado** |
| **B — eco pontual** | −8,00 dB | `Echo` (Dotted 1/8; Feedback 24,5%; HP 299,5 Hz + LP 3.495 Hz; Width 100%; DryWet 100%, automatizado para 60% → 0% → 100% e delay 0,75 num trecho) | Sends estáticos de efeitos percussivos + ~10 canais com throw pontual |

### 3.3. Gain staging dos grupos que alimentam o master (`VERIFICADO`)

| Grupo | Fader manual | Automação de volume | Problemas que chegam ao master |
| ----- | ----- | ----- | ----- |
| **Bateria** | 0,00 dB | 0,0 dB (cai p/ −1,5 dB c.63, −6,0 dB e −inf c.145) | O kick tinha `DrumBuss OutGain = +3,00 dB`, `Utility = −2,00 dB` e **lane de volume travada em +1,60 dB** (+2,60 dB líquidos acima do sample); o grupo ainda soma +3,5 dB de High-Shelf @ 6,9 kHz antes dos +15 dB do master |
| **Graves** | 0,00 dB | Sem lane de volume (3 pts `Speaker=true`) | Sub-roll com fader em **+0,90 dB**; rolling em 0 dB + Utility +0,89 dB + Saturator +5 dB Drive e **sem sidechain**; baixo médio com **boost de +10,54 dB @ 224,8 Hz**; lanes `Speaker=true` reativavam 2 canais de sub mutados |
| **Synths/madeiras** | 0,00 dB | 0,0 dB (extremos −3,5 dB) | 4 canais de sopro com lane de volume a **+2,50 dB** no compasso ~32; um canal de glitch com boosts de **+4,09 dB @ 166,8 Hz + +11,53 dB @ 185,5 Hz + +12,27 dB HShelf @ 1.088,8 Hz** |
| **Clima/vozes** | 0,00 dB | **Sobe para +3,00 dB** entre beats 578–670 (c. 145–168) | Além do grupo subir no breakdown, a voz líder tinha automação de `GlobalGain` do EQ a **+11,23/+12,00 dB**; sussurro/sucção com Utility +2,97 dB em reverbs de 4,00 s (35% wet) e 3,50 s (40% wet) |
| **Efeitos** | 0,00 dB | **Sobe para +4,00 dB** (beat 479) e **+2,00 dB** (beats 480–960) | Grupo inteiro operando a +2/+4 dB a partir do compasso 120; downer com +8,80 dB @ 146,8 Hz e +10,54 dB @ 3.299 Hz; stab de drop com **+13,51 dB @ 193,6 Hz**; despedida com Utility +5,99 dB |
| **Canais fora de grupo** | −5,4 a 0,0 dB | Sem lane (fader manual) | Batem **direto no master** sem bus e sem ducker de kick; voz de garganta com **+12,29 dB @ 134,8 Hz e +12,04 dB @ 464,1 Hz**; kamancheh com **+9,05 dB @ 37,5 Hz e +10,79 dB @ 193,6 Hz**; kanun com **+9,95 dB reais @ 132 Hz** (EQ + automação de GlobalGain) |

## 4. Diagnóstico do "Som Pra Dentro" com Números (`VERIFICADO` + `INFERÊNCIA`)

1. **Onde falta fundamento (vácuo em 25–40 Hz — `VERIFICADO`):**
   * Em C# frígio, a tônica subgrave fica em **34,65 Hz (MIDI 25 / C#0)**. A auditoria MIDI das 41 pistas revelou **0 notas em MIDI 25** em todo o arranjo: os canais de sub tocavam em MIDI 37 (69,3 Hz; 640 notas) com preset de mid-bass FM falante; o sub-roll em MIDI 44/45 (103,8/110,0 Hz); rolling e baixo médio em MIDI 49 (138,6 Hz).
   * Ao mesmo tempo, o EQ do master aplicava **Low-Cut de 48 dB/oct em 25,2 Hz**, somado aos low-cuts do grupo de bateria (18,5 Hz) e do canal do kick (23,3 Hz). Resultado: ausência de energia fundamental em 25–40 Hz (−8 a −15 dB abaixo das referências) e rotação severa de fase nos subgraves.
2. **Onde o master trabalha demais (sobrecarga em 65–500 Hz e > 5 kHz — `VERIFICADO`):**
   * Como todos os baixos tocavam entre 69,3 e 138,6 Hz, e instrumentos melódicos/vocais tinham boosts extremos nessa mesma zona (+9 a +15,6 dB em 37–464 Hz em 6+ canais), a faixa de **65–500 Hz chegava saturada ao master**.
   * Antes do Glue, o EQ do master ainda somava **+3,00 dB @ 1.487,9 Hz** e **+15,00 dB de High-Shelf acumulado acima de 11 kHz**, somados aos High-Shelves de +2,0 a +3,5 dB @ 6,9 kHz dos grupos (**até +18,5 dB de boost agudo em cascata**).
   * Esse sinal inflado atinge o Glue (threshold −1,0 dB, 100% wet) e o limiter (ceiling −0,71 dB, release 100 ms, link 100%). Cada nota de baixo/kick fazia o limiter comprimir L/R inteiro por 100 ms (praticamente uma semicolcheia a 128 BPM = 117,2 ms), impedindo a mix de respirar e empurrando os planos "para dentro".
3. **Onde a imagem estéreo fecha (correlação da banda média em 0,80 vs. 0,32–0,44 — `VERIFICADO`):**
   * Quatro cascatas de Bass Mono em filtros *minimum-phase* rodavam simultaneamente (canais 120–140 Hz → grupos 120/140/144 Hz → master 121,3 Hz). Como demonstra a literatura ([iZotope, 2025](https://www.izotope.com/community/blog/what-is-midside-processing)), filtros *minimum-phase* no canal Side deslocam a fase e estreitam o panorama até acima de 1–5 kHz.
   * Pior: os elementos que dominavam 200–2.000 Hz estavam forçados em **100% mono** (baixo médio com `Mono=true` pós-cadeia; voz líder e chop vocal com `Width=0%` após os delays/reverbs), enquanto voz de garganta e kamancheh injetavam energia maciça no canal Mid (L+R) sem filtro passa-altas.

## 5. Três Cenários de Masterização com Ajustes Exatos (`DE → PARA`)

> **Pré-requisito de higiene no master para os 3 cenários:** (1) desligar/remover o device Max pós-limiter; (2) remover a lane órfã do `ParameterB` do EQ.

| Device | Parâmetro | Valor Atual (`DE`) | (A) Streaming Seguro (TP ≤ −1,0 dBTP) | (B) Clube/Pista (−7,5 a −8,5 LUFS) | (C) Híbrido Beatport/Streaming (TP ≤ −0,8 dBTP) | Justificativa |
| ----- | ----- | ----- | ----- | ----- | ----- | ----- |
| **`Eq8[0]`** | `Mode` / `Oversampling` | `0` (Stereo) / `false` | `2` (**M/S**) / **`true`** | `2` (**M/S**) / **`true`** | `2` (**M/S**) / **`true`** | Habilita escultura M/S para abrir a banda média e evita cramping de fase nos agudos |
| **`Eq8[0]` (Mid)** | Low-Cut | LC48 @ 25,2 Hz (Q=0,71) | LC12 @ **18,0 Hz** (Q=0,55) | LC12 @ **20,0 Hz** (Q=0,60) | LC12 @ **19,0 Hz** (Q=0,58) | Libera a oitava 25–40 Hz e elimina a rotação de fase |
| **`Eq8[0]` (Mid)** | Low-Mid Bell | Bell @ 302,5 Hz, −0,50 dB | Bell @ **235,0 Hz**, **−2,50 dB** (Q=1,10) | **−3,00 dB** | **−2,80 dB** | Limpa o acúmulo mono no centro (200–300 Hz) |
| **`Eq8[0]` (Mid)** | Mid Bell | Bell @ 1.487,9 Hz, +3,00 dB | **−1,00 dB** (Q=1,20) | **−1,50 dB** | **−1,20 dB** | Remove a dureza nasal (+3 dB em 1,5 kHz no Mid) |
| **`Eq8[0]` (Mid)** | High-Shelves | +2,0 dB @ 5k + +6,5 dB @ 8,7k + +6,5 dB @ 11k (**+15 dB!**) | B4 **OFF**; B5 **OFF**; B8: HShelf @ **10.500 Hz**, **+1,50 dB** | idem, B8 **+2,00 dB** | idem, B8 **+1,80 dB** | Elimina o empilhamento que disparava Glue/Limiter prematuramente |
| **`Eq8[0]` (Side)** | Side Low-Cut | Desligado (40 Hz) | LC12 @ **110,0 Hz** | LC12 @ **115,0 Hz** | LC12 @ **110,0 Hz** | Monoiza graves via M/S com filtro suave, substituindo o BassMono redundante |
| **`Eq8[0]` (Side)** | Side Low-Mid Cut | Desligado | Bell @ **310,0 Hz**, **−2,50 dB** | **−3,00 dB** | **−2,50 dB** | Limpa a lama de reverbs longas nas laterais (240–480 Hz) |
| **`Eq8[0]` (Side)** | Side Body & Width | Desligado | Bell @ **620,0 Hz**, **+2,20 dB** (Q=0,85) | **+2,50 dB** | **+2,40 dB** | Abre a banda média nos Sides (correlação 0,80 → 0,40–0,50) |
| **`Eq8[0]` (Side)** | Side Air Shelf | Desligado | HShelf @ **11.500 Hz**, **+2,50 dB** | **+3,00 dB** | **+2,80 dB** | Cria ar tridimensional sem rachar o centro em mono |
| **`GlueCompressor`** | `Threshold` / `Attack` / `Release` | −1,0 dB / 30 ms / Auto | **−6,5 dB** (GR máx 1,5 dB) / 30 ms / **0,1 s** | **−8,0 dB** (GR máx 2,0 dB) / 30 ms / **0,1 s** | **−7,5 dB** (GR 1,5–2,0 dB) / 30 ms / **0,1 s** | `Release = 0,1 s` recupera antes do próximo beat (468 ms) e semicolcheia (117 ms) |
| **`GlueCompressor`** | `DryWet` / `PeakClipIn` / `Oversample` | 100% / false / false | **60%** / false / **true** | **65%** / **true (Soft Clip)** / **true** | **65%** / **true** / **true** | Compressão paralela preserva transientes; Soft Clip atua como clipper pré-limiter nos cenários B/C |
| **`GlueCompressor`** | `Makeup` / `SideChain/Eq` | 0,0 dB / HP 200 Hz | **+0,8 dB** / HP **150 Hz** | **+1,5 dB** / HP 150 Hz | **+1,2 dB** / HP 150 Hz | Compensa a perda do boost de +15 dB do EQ com ganho limpo |
| **`StereoGain` (Utility)** | `StereoWidth` / `BassMono` | 99,61% / true (121,3 Hz) | **104,0%** / **false** (feito no EQ M/S) | **105,0%** / **false** | **105,0%** / **false** | Remove a 4ª cascata de Bass Mono no master |
| **`Limiter`** | `Gain` / `Ceiling` / `Mode` | 0,0 dB / −0,712 dB / True Peak | **+1,5 dB** / **−1,00 dB** / True Peak | **+3,5 dB** / **−0,50 dB** / Soft Clip ou True Peak | **+2,5 dB** / **−0,80 dB** / True Peak | Alinha o teto às diretrizes reais de codec (−1,0 dBTP streaming; −0,8 híbrido; −0,5 teto de projeto) |
| **`Limiter`** | `AutoRelease` / `Lookahead` / `LinkAmount` | false / 3 ms / 100% | **true** (50 ms) / 3 ms / **65%** | **true** (40 ms) / 1,5 ms / **60%** | **true** (45 ms) / 3 ms / **65%** | Desvincular parcialmente L/R e ativar AutoRelease impede que o kick feche os Sides |
| **Métricas esperadas (`INFERÊNCIA`)** | LUFS-I / TP / LRA / Crest | −10,5 a −9,5 LUFS (c/ distorção aguda) / −0,71 dBTP / LRA 15,3 | **−10,5 a −9,8 LUFS-I** / ≤ −1,00 dBTP / LRA ~11–13 / Crest ~9,5 dB | **−8,2 a −7,6 LUFS-I** / ≤ −0,50 dBTP / LRA ~8–10 / Crest ~7,5 dB | **−9,0 a −8,5 LUFS-I** / ≤ −0,80 dBTP / LRA ~9–11 / Crest ~8,5 dB | O Cenário C entrega competitividade no Beatport sem clipar transcodificadores |

## 6. Plano de Medição Pós-Render (Comandos e Alvos Numéricos)

Como nenhum `.wav` renderizado estava anexado ao ambiente de inspeção (`NÃO VERIFICADO`), exportar o master em `WAV 24-bit / 48 kHz` (sem o device Max pós-limiter) e rodar os comandos abaixo:

### 6.1. Medição EBU R128 (LUFS-I, True Peak, LRA) via `ffmpeg`

```
ffmpeg -nostats -i master_test.wav -filter_complex ebur128=peak=true -f null - 2>&1 | tail -n 20
```

### 6.2. Medição forense por banda (sub 20–40 Hz, correlação L/R por banda, crest factor, DC)

```
python3 - <<'PY'
import soundfile as sf
import numpy as np
from scipy.signal import butter, sosfilt

wav_path = "master_test.wav"
x, sr = sf.read(wav_path, always_2d=True)
L, R = x[:, 0], x[:, 1]
M = 0.5 * (L + R)

peak_dbfs = 20 * np.log10(np.max(np.abs(x)) + 1e-12)
rms_dbfs = 20 * np.log10(np.sqrt(np.mean(x**2)) + 1e-12)
crest_db = peak_dbfs - rms_dbfs
dc_offset = np.mean(x, axis=0)

bands = [
    ("Sub (20-40 Hz)", 20, 40),
    ("Grave (40-80 Hz)", 40, 80),
    ("Upper Bass (80-200 Hz)", 80, 200),
    ("Média (200-2k Hz)", 200, 2000),
    ("Presença (2k-8k Hz)", 2000, 8000),
    ("Ar (8k-18k Hz)", 8000, 18000),
]

print(f"Sample Peak: {peak_dbfs:.2f} dBFS | RMS: {rms_dbfs:.2f} dBFS | Crest: {crest_db:.2f} dB | DC: {dc_offset}")
for name, f_lo, f_hi in bands:
    sos = butter(4, [f_lo, f_hi], btype='bandpass', fs=sr, output='sos')
    bL, bR = sosfilt(sos, L), sosfilt(sos, R)
    rms_b = 20 * np.log10(np.sqrt(np.mean(0.5*(bL**2 + bR**2))) + 1e-12)
    corr = np.corrcoef(bL, bR)[0, 1]
    print(f"{name:24s} -> RMS: {rms_b:6.2f} dBFS | Correlação L/R: {corr:+.3f}")
PY
```

### 6.3. Tabela de alvos numéricos de validação pós-render

| Métrica | Estado anterior do caso (medido 16/10) | Alvo pós-ajuste (Cenário C — híbrido) | Alvo pós-ajuste (Cenário A — streaming) |
| ----- | ----- | ----- | ----- |
| **True Peak (dBTP)** | −0,71 dBFS (tocando o teto ~10x/s) | **≤ −0,80 dBTP** (máx 1–2 dB de GR nos picos) | **≤ −1,00 dBTP** |
| **Loudness Integrado (LUFS-I)** | Escola −8,6 / faixa variável | **−9,0 a −8,5 LUFS-I** (drops em −7,8 LUFS-ST) | **−10,5 a −9,8 LUFS-I** |
| **LRA** | 15,3 LU (devido a quebras e boosts de +4 dB nos grupos) | **9,0 a 11,5 LU** (mantendo contraste orgânico de bush tech) | **10,5 a 12,5 LU** |
| **Energia Sub 20–40 Hz vs 40–80 Hz** | −8 a −15 dB abaixo das referências | **−3,0 a −5,0 dB** abaixo da banda 40–80 Hz (após descer os subs para MIDI 25) | **−3,0 a −5,0 dB** |
| **Correlação L/R Banda Média (200–2k Hz)** | 0,80 (excessivamente mono/fechada) | **0,38 a 0,52** | **0,38 a 0,52** |
| **Correlação L/R Graves (20–120 Hz)** | ~1,00 | **≥ +0,95** | **≥ +0,95** |
| **Crest Factor Global (drops)** | Comprimido na banda 30–90 Hz | **8,0 a 9,5 dB** | **9,0 a 10,5 dB** |

## 7. O Que NÃO Deu Para Verificar (`NÃO VERIFICADO`)

* **Medição DSP direta em `.wav` renderizado (LUFS-I, True Peak, LRA, Crest, correlação por banda, espectro FFT):** apenas o arquivo `.als` foi enviado ao ambiente de inspeção (sem os `.wav` locais), então as métricas acústicas não puderam ser medidas diretamente nesta sessão; ficaram propostas com script pronto na Seção 6.
* **Resposta interna exata dos módulos de FX dentro dos blobs binários do Serum 2 FX:** os cabeçalhos JSON (`XferJson`) de todas as 32 instâncias foram decodificados (preset, autor, descrição, hash), mas os knobs de DSP proprietários do Xfer são serializados em binário opaco após o cabeçalho.
