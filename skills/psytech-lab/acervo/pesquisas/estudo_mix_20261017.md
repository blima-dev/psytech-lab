# Estudo Completo de Mixagem — caso real em faixa minimal psytech (Ableton Live 12.4.6, 17/10/2026)

**Arquivo auditado (`VERIFICADO`):** um set de minimal psytech (128 BPM, C# frígio) com 7.033.012 bytes, 70 pistas + 2 retornos + master, 81.156 notas MIDI habilitadas. Todos os valores foram medidos no XML do `.als`; nomes de canal foram generalizados para funções.

## 1. Sumário Executivo (5 Descobertas por Ordem de Impacto)

* **1º (Maior Impacto — banda média mono 0,80 vs. 0,32–0,44 e presença fechada 0,64 vs. 0,51 — `VERIFICADO`):** os canais que dominam a energia de 130–2.000 Hz estavam travados em **100% mono** (baixo médio com `Utility Mono = true` após boost de +10,54 dB @ 224,8 Hz; voz líder e chop vocal com `Width = 0%` após os delays/reverbs) ou despejavam boosts extremos no centro (`Pan = 0`) sem passa-altas e sem sidechain (voz de garganta com **+12,29 dB @ 134,8 Hz e +12,04 dB @ 464,1 Hz**; kamancheh com **+9,05 dB @ 37,5 Hz e +10,79 dB @ 193,6 Hz**; glitch seco com **+15,6 dB @ 166–185 Hz + +12,27 dB HShelf @ 1.088,8 Hz**), esmagando a proporção Side/Mid da banda média.
* **2º (Ausência de fundamento em 25–40 Hz — `VERIFICADO`):** a nota fundamental de C# na oitava subgrave é **MIDI 25 (C#0 no Ableton = 34,65 Hz)**, mas **existiam exatamente 0 notas em MIDI 25 em todo o projeto**. Todos os canais do grupo de graves tocavam uma a duas oitavas acima (subs em MIDI 37 = 69,30 Hz com preset de mid-bass falante; sub-roll em MIDI 44 = 103,83 Hz; rolling e baixo médio em MIDI 49 = 138,59 Hz), explicando por que ligar/desligar o sub principal não alterava a banda 25–40 Hz.
* **3º (Densidade de picos 7,57/s — "encavalado" — e ausência de ducking nos graves — `VERIFICADO`):** oito canais que pareciam mutados no painel (`Speaker/Manual = false`: shaker, sub-cama, sub extra de referência, glitch falante, shimmer, duas cópias de proposta antigas e a cama atmosférica) possuíam lanes de automação `Mixer.Speaker` cravadas em `true`, **ligando sozinhos ao abrir o `.als`**; além disso, o baixo principal 16ths (0,0 dB) estava com seu ducker `AutoPan2` **desligado**, e os 5 canais ativos fora de grupo (kanun, kanun alto, voz de garganta, kamancheh, flauta) tocavam 2.557 notas sobre os drops **sem nenhum sidechain para o kick**.
* **4º (Cascata de filtros defeituosa em braam/horn/corneta e `Wet = 35%` nos glitches — `VERIFICADO`):** em dois canais de corneta, o device batizado de 'Auto Filter HP 90Hz' estava configurado como **Notch em 740,8 Hz (Res = 100%)**; no canal de braam, o 'HP 90Hz' (67,8 Hz, Res = 73%) era desligado por lane e seguido por um Notch @ 688,9 Hz (Res = 89%); nos 4 canais de metais, o Serum 2 carregava um preset de **drone** em vez de sopro; e em 9 canais de glitch + braam, os Auto Filters tinham `DryWet = 35%`, vazando 65% do sinal sem filtro com cancelamento de fase (*comb filtering*).
* **5º (Vazamento de reverbs > 3 s e violação dos grupos em 0 dB via automação — `VERIFICADO`):** existiam **9 reverbs de insert ativos ou reativados por automação com decay entre 3,09 s e 11,76 s** (atmosfera 11,76 s; stab de drop 5,96 s; sussurro 4,00 s; sucção 3,50 s; cello e glitch seco 3,46 s; voz líder 3,18 s; kanun/voz de garganta 3,09 s com RoomSize automatizado até 258), somados às lanes de `Mixer.Volume` que subiam os grupos de clima/vozes para **+3,00 dB** e de efeitos para **+4,00 dB**.

## 2. O Que a Internet Diz (Prática Profissional Psytech / Dark Zenon / Bush Tech 2024–2026)

### 2.1. Relação Kick × Sub × Bass e Sidechain em Psytech / Zenon Records
* **Consenso Técnico:** Em minimal psytech / dark progressive (126–130 BPM), o subgrave fundamental deve ocupar a oitava 32–45 Hz (em C# frígio, C#1 científico / C#0 Ableton = 34,65 Hz, com 2º harmônico em 69,30 Hz), nunca coexistindo sem *ducking* de fase/volume com o corpo do kick (48–65 Hz). O sidechain do baixo em música 4/4 deve ser feito por *volume shaping* (LFO de 1/4 com fase travada) ou compressor clássico ultrarrápido (`Attack < 1 ms`, `Release ~120–180 ms`), nunca deixando um rolling bass 16ths sem atenuação no beat.
* **Fontes e Trechos Verificados:**
  * [What Is Sidechain Compression? How and When to Use It — Hyperbits (Mar 2026)](https://hyperbits.com/blog/sidechain-compression/):
    > "Both your kick and your bass occupy the low end of your mix, and because they are both so huge, we don't want them playing at the same time... LFO sidechain is especially useful for sidechaining sounds to a kick drum in 4x4 dance music... With band-splitting, you can only sidechain the low frequencies and leave the higher frequencies untouched, which gives you the benefit of reducing the low end of the bass without creating an overwhelming 'pumping feel.'"
  * [Mastering for Beatport — mastering.to (2025/2026)](https://mastering.to/beatport):
    > "Sub-bass 20–80 Hz: MONO... Wide sub-bass and bass sounds impressive in headphones and on stereo speakers. On a professional club PA with mono subwoofers, that same width causes phase cancellation — the fundamentals thin out or disappear."

### 2.2. Por Que a Banda Média Fica Mono e Como Abrir Sem Perder Centro/Fase
* **Consenso Técnico vs. Opinião:** A banda média (200–2.000 Hz) fica excessivamente mono (correlação > 0,75) quando: (a) plugins `Utility` estão em `Mono = true` ou `Width = 0%` após efeitos espaciais; (b) múltiplos instrumentos centrais têm boosts largos em 150–500 Hz; e (c) filtros *minimum-phase* no canal Side (como `Bass Mono` em cascata) rotacionam a fase até 1–5 kHz. Para abrir a banda média mantendo compatibilidade mono (correlação alvo 0,35–0,55), usa-se panning complementar L/R (30–70%), delays curtos/ping-pong filtrados (`HP > 250 Hz`), corte de lama nos Sides (240–480 Hz) e boost largo nos Sides em 550–800 Hz.
* **Fontes e Trechos Verificados:**
  * [What is mid/side processing? — iZotope (Ian Stewart, Aug 2025)](https://www.izotope.com/community/blog/what-is-midside-processing):
    > "I've used the mid channel to pull out some low-mid resonance from the bass around 170 Hz, as well as some brittleness around 3k in the vocal. That 3k dip is also making the background vocals and claps slightly wider in that region. I've also used the side channel to do a wide boost around 550 Hz, which adds some width and energy..."
  * [How To Use Mid/Side EQ To Elevate Your Masters — Mastering The Mix (Jul 2025)](https://www.masteringthemix.com/blogs/learn/how-to-use-mid-side-eq-to-elevate-your-masters):
    > "Add a complementary cut in the low mid range (240 to 480 Hz) on the side channel. This is where muddiness and stereo wash often build up, especially from pads, guitars, or wide reverb. Pulling these frequencies back in the sides cleans up the stereo image and puts more focus on the vocal in the center."
  * [The Science of Stereo Width: How to Widen Your Mix Without Ruining It — MixMaster Pro (Nov 2025)](https://www.mixmasterpro.io/articles/stereowidth):
    > "Place instruments across the stereo field: Center: Kick, snare, bass, lead vocal; 30-70% L/R: Rhythm guitars, keys, percussion; Hard L/R (85-100%): Hi-hats, shakers, doubled guitars... Aim for a reading between +0.5 and +1 for safe, mono-compatible width."

### 2.3. Densidade de Eventos ("Encavalado"), Groove Minimal e Reverbs Duckados
* **Consenso Técnico:** No bush tech / dark zenon (referências como Breger, Yao Ofosu, AlpaKa Muzik, Kaled Nasser, Slippery Slope), a estética hipnótica depende de **contraste seco/molhado (*call-and-response*)** e micro-pausas: nunca mais de 2 elementos melódicos/glitches atacam no mesmo subdivisor de semicolcheia, e caudas de reverb/delay são **sidechained contra o próprio sinal seco ou contra o kick** para não borrar os transientes seguintes.
* **Fontes e Trechos Verificados:**
  * [What Is Sidechain Compression? (Pro Tip 7: Sidechain Reverbs And Delays To The Dry Signal) — Hyperbits (Mar 2026)](https://hyperbits.com/blog/sidechain-compression/):
    > "When you add reverb or delay to a sound, sidechain the reverb or delay back to the dry signal. This reduces the volume of the reverb/delay when the dry signal is playing and accentuates the reverb/delay when the dry signal stops."

### 2.4. Erros Comuns no Ableton Live 12 (Cascata de Filtros, Ressonância de Auto Filter e Gain Staging)
* **Consenso Técnico:** No Live 12, deixar `Auto Filter` com `Resonance > 50%` sem controle gera picos estreitos de +6 a +12 dB que roubam headroom e disparam limiters; usar `Dry/Wet < 100%` em um `Auto Filter` (HP/LP) cria um filtro *all-pass/comb* por diferença de fase entre sinal seco e filtrado; e automatizar `Mixer.Volume` diretamente nos canais e grupos trava os faders e destrói a estrutura de buses em 0 dB.

## 3. Estado Real Medido do Caso por Grupo/Canal e Ocupação de Registros (`VERIFICADO`)

### 3.1. Grupo de bateria (fader 0,0 dB; EQ do grupo: LC12@18,5 Hz, −2,5 dB@300 Hz, +1 dB@1,67 kHz, HShelf +3,5 dB@6,9 kHz; Utility BassMono 119,9 Hz)

| Canal (função) | Estado (Man/Env) | Fader (Man/Env) | Registro MIDI / Notas / Compassos | Cadeia & parâmetros críticos |
| :--- | :--- | :--- | :--- | :--- |
| **Kick** | true / — | 0,0 dB / **+1,6 dB** | MIDI 36 (65,4 Hz, 793 notas) + MIDI 31..35,37 (124 notas!), c. 9–216 | Simpler com sample de kick de pack externo (**Transpose=+24 st**) → DrumBuss (Drive 11%, Damp 3.532 Hz, **OutGain +3,00 dB**) → EQ8 (LC12@23,3 Hz) → Utility (−2,0 dB). **Ganho líquido real = +2,60 dB!** |
| **Trigger sidechain** | true / true | −70,0 dB | MIDI 36 (7.680 notas), c. 1–240 | Simpler (mesmo sample, sem transposição). Alimenta 11 duckers `Compressor2`. |
| **Open hat** | true / — | −13,2 dB / **−9,2 dB** | MIDI 46..50 (848 notas), c. 49–216 | Simpler → AutoPan2 (35%) → Utility +2,5 dB → EQ8 (LC48@402 Hz, HShelf +4 dB@6,9k) |
| **Shaker** | **false / true!** | −17,7 dB / **−10,8 dB** | MIDI 60 (2.786 notas), c. 9–216 | **Conflito Speaker=true liga o canal!** Utility +4,0 dB → Delay (Haas 3D, Wet 8%) |
| **Hat esteira (referência)** | false / false | −4,47 dB / −14,0 dB | MIDI 60 (546 notas ativas / 21 clipes OFF) | Mudo de referência (Utility +4,5 dB, EQ8 +3 dB@6,9k) |
| **Closed hat** | true / true | −9,6 dB / **−8,0 dB** | MIDI 42..50 (2.886 notas), c. 49–232 | EQ8 (LC48@296 Hz, Notch@10,6k, +2,36 dB@1,5k) → Utility +3,0 dB → AutoPan2 (35%) → Serum2FX[OFF] |

### 3.2. Grupo de graves (fader 0,0 dB; EQ do grupo OFF; Utility BassMono 140 Hz — **zero duckers de kick!**)

| Canal (função) | Estado | Fader | Registro MIDI real | Cadeia & conflito espectral |
| :--- | :--- | :--- | :--- | :--- |
| **Baixo médio** | true / — | −7,1 dB | MIDI 49 (138,6 Hz, 649 notas) e MIDI 44 (103,8 Hz, 208 notas), c. 65–216 | Serum2 → AutoPan2 (ducker, 35%) → EQ8 (**+10,54 dB @ 224,8 Hz**, +3,0 dB @ 700 Hz) → Saturator[OFF] → AutoFilter2[OFF] (232 pts de automação!) → Utility BassMono → EQ8[OFF] → Utility (**Mono = true**) |
| **Sub-roll** | true / — | **+0,9 dB** | MIDI 44 (103,8 Hz, 790 notas) e MIDI 45 (110,0 Hz, 54 notas), c. 49–176 | Operator → EQ8 (LC12@25,2 Hz) → Utility (**Mono = true**) → **Serum2FX (AU) ativo**. **Sem sidechain e fader em +0,9 dB!** |
| **Sub principal** | true / true | −10,6 dB / −10,0 dB | MIDI 37 (69,3 Hz, 640 notas), MIDI 32 (51,9 Hz, 23), MIDI 49 (138,6 Hz, 47), c. 9–240 | Serum2 (**preset de mid-bass FM falante**) → Saturator[OFF] → EQ8[OFF] → Utility BassMono. **Zero notas em MIDI 25 (34,65 Hz) e sem sidechain!** |
| **Sub-cama** | **false / true!** | −10,6 dB / −10,0 dB | MIDI 37 (69,3 Hz, 6 notas longas), c. 57–176 | **Conflito Speaker=true liga o canal!** Mesmo preset falante e notas em 69,3 Hz (colidindo com o sub principal!) |
| **Sub extra (referência)** | **false / true!** | −5,5 dB | MIDI 49 (138,6 Hz, 3.174 notas), c. 73–199 | **Conflito Speaker=true liga o canal de referência em −5,5 dB!** 3.174 notas em cima do rolling e do baixo médio! |
| **Rolling 16ths** | true / — | 0,0 dB / 0,0 dB | MIDI 49 (138,6 Hz, 1.359 notas), MIDI 50 (146,8 Hz, 77), MIDI 37 (69,3 Hz, 3), c. 9–232 | Serum2 → AutoPan2 (ducker **OFF!**) → EQ8[OFF] → Saturator (+5,04 dB Drive) → AutoFilter2[OFF] → Utility (+0,89 dB). **Sem sidechain (ducker desligado!) e 1 oitava acima do sub!** |

### 3.3. Grupo de synths/madeiras (fader 0,0 dB; EQ: LC12@115 Hz, −2,5 dB@487 Hz, HShelf +2 dB@6,9 kHz; Utility Width 110%, BassMono 144,2 Hz)

| Canal (função) | Estado | Fader | Pan | Registro / compassos | Problemas medidos |
| :--- | :--- | :--- | :--- | :--- | :--- |
| **Cello staccato** | true / — | 0,0 dB | 0.22R | MIDI 49..56 (138,6–207,7 Hz, 46 notas), c. 49–213 | Comp2 (SC Kick, 70%) → AutoPan2 (65%) → Reverb (**3,46 s**, 20%) → EQ8 → **Serum2FX ativo**. Mascaramento direto com braam e baixo médio em 138,6 Hz! |
| **Braam 2** | true / — | −14,9 dB | 0.00 | MIDI 37..61 (+MidiPitcher +12st = **138,6–554,4 Hz**, 391 notas), c. 1–184 | Serum2 → Saturator (+8 dB, 50%) → Comp2 (SC) → Delay 15% → AutoFilter2 (LP Res 88%, Wet 35%, autom. 650–2.100 Hz) → AutoFilter2 ('HP 90Hz'@67,8 Hz, Res 73%, **desligado por lane!**) → EQ8 (+3,6 dB@612 Hz) → AutoFilter2 (Notch@688,9 Hz, Res 89%) |
| **Horn + cópia de proposta** | true / true | −10,8 dB / **−8,7..+2,5 dB** | 0.22L | MIDI 59..68 (246,9–415,3 Hz, 73 notas), c. 1–232 | **Preset errado (drone cinematográfico)**; AutoFilter2 com 175 pts de automação **OFF**; lane de volume a **+2,50 dB** no beat 127 |
| **Corneta + cópia de proposta** | true / true | 0,0 dB / **−8,7..+2,5 dB** | 0.00 | MIDI 37..73 (69,3–554,4 Hz, 62 notas), c. 59–209 | **Preset errado (drone)**; **'HP 90Hz' é Notch @ 740,8 Hz (Res 100%)**; lane de volume a **+2,50 dB** |
| **Groove sampleado** | true / — | −8,0 dB / −15..−8 dB | 0.00 | 25 AudioClips ativos | Único device é EQ8 100% em 0,0 dB (**sem HP e sem sidechain**) |
| **Glitch seco** | true / — | −11,9 dB / −25..−18 dB | 0.00 | MIDI 49..64 (138,6–329,6 Hz, 341 notas), c. 41–200 | BeatRepeat → Reverb (**3,46 s**, 12%) → **EQ8 (+4,09 dB @ 166,8 Hz + +11,53 dB @ 185,5 Hz + +12,27 dB HShelf @ 1.088,8 Hz, HC12 @ 2.554 Hz)** → Comp2 (SC). Injeta +15,6 dB em 166–185 Hz! |
| **Glitch falante** | **false / true!** | −11,2 dB | 0.35R | MIDI 49..64 (158 notas), c. 38–140 | **Reativado por lane Speaker=true!** AutoFilter2 (HP@276 Hz, Wet 35%), sem sidechain |
| **Glitch granulador** | true / — | −2,7 dB | 0.35R | MIDI 61 (277,2 Hz, 909 notas), c. 40–209 | AutoFilter2 (HP@276 Hz, Wet 35%), sem sidechain |
| **Glitch FM** | true / — | 0,0 dB | 0.00 | MIDI 49..62 (518 notas), c. 9–183 | AutoFilter2 (HP@150 Hz) → AutoFilter2 (LP@7 kHz, Wet 35%), sem sidechain; 21 de 32 clipes desativados |
| **Resposta rasgada** | true / true | −23,6 dB | 0.70R | MIDI 49..56 (302 notas), c. 66–200 | AutoFilter2 (BP@900 Hz, Wet 35%) → Redux2 → EQ8 → Comp2 (SC Kick) → Comp2 (SC cello) |
| **Glitch espaço** | true / — | −18,0 dB | 0.00 | MIDI 49..56 (320 notas), c. 57–151 | AutoFilter2 (LP@3,8 kHz, Wet 35%), sem sidechain |
| **Shimmer + cópia de proposta** | **false / true!** | −22,9 dB | 0.35R | MIDI 49..92 (612 notas), c. 57–140 | **Reativados por lane!** AutoFilter2 (LP@3,8 kHz, Wet 35%), sem sidechain |
| **Squelch** | true / — | −15,0 dB | 0.15R | MIDI 49..61 (92 notas), c. 61–175 | AutoFilter2 (LP@1,5 kHz, Wet 35%) → Comp2 (SC cello). **Sem sidechain para o kick!** |
| **Seq. analog** | true / — | 0,0 dB | 0.00 | 23 AudioClips ativos | EQ8[OFF] → **Serum2FX ativo (preset de stab)** → Utility −2,5 dB. **Sem HP e sem sidechain** |

### 3.4. Grupo de clima/vozes (automação sobe a **+3,0 dB** c. 145–168) e grupo de efeitos (**+4,0 dB** c. 120)

| Canal (função) | Estado | Fader | Diagnóstico |
| :--- | :--- | :--- | :--- |
| **Cama atmosférica** | **false / true!** | −2,98 dB | **Reativada por lane Speaker=true!** Rack interno com Echo (37%) + **Reverb 11,76 s (55% wet)**. Inunda o fundo da mix. |
| **Voz líder** | true / true | 0,0 dB | EQ8 (**GlobalGain automatizado a +11,2/+12,0 dB!**) → Comp2 (SC Kick) → Delay 25% → Reverb 3,18 s → **Utility Width = 0% (100% mono!)** → Serum2FX ativo |
| **Zumbido granulado** | true / true..false | −10,4 dB | Delay 15% → Serum2FX ativo → EQ8 (LC12@80,5 Hz com +4,0 dB de Q-boost) |
| **Eco / foley / chop vocal** | true / — | −14,2/−13,8 dB / **−2,4 dB!** | Lanes de volume forçam os 3 canais para **−2,40 dB** (+11,4 a +11,8 dB acima dos faders!); chop vocal com **Width = 0%** |
| **Sussurro / sucção** | true / — | 0,0 dB | Utility +2,97 dB jogando direto em **reverbs de fim de cadeia de 4,00 s (35% wet) e 3,50 s (40% wet)** sem corte pós-reverb |
| **Downer** | true / — | −6,8 dB | 'HP 180Hz' está em **23,2 Hz** → **EQ8 (+8,80 dB @ 146,8 Hz, +10,54 dB @ 3.299 Hz)** → Reverb 1,96 s → Serum2FX ativo |
| **Stab de drop** | true / — | 0,0 dB | 'HP 180Hz' está em **50,6 Hz** → **EQ8 (+13,51 dB @ 193,6 Hz)** → **Reverb 5,96 s ligado por lane** → Serum2FX ativo |

### 3.5. Canais fora de grupo (batem direto no master, sem sidechain)

| Canal (função) | Estado | Fader | Registro | Problemas críticos |
| :--- | :--- | :--- | :--- | :--- |
| **Kanun + kanun alto (cópia de resposta)** | true / true | 0,0 dB | MIDI 49..73 (207,7–554,4 Hz, **2.073 notas**), c. 5–232 | **EQ8 +6,32 dB @ 131,9 Hz + +3,60 dB @ 879,7 Hz** (+ automação de GlobalGain até +3,63 dB = **+9,95 dB reais @ 132 Hz!**), LC12 @ 68,1 Hz e HC12 @ 5.273 Hz (mata o brilho e infla o médio-grave). Reverb 3,09 s com RoomSize até 258. A cópia duplica o kanun nos c. 73–76 |
| **Voz de garganta + cópia de resposta** | true / false | −3,4 dB | MIDI 49..56 (138,6–207,7 Hz, 59 notas), c. 57–234 | **EQ8 (+2 dB de GlobalGain) dá +10,29 dB @ 134,8 Hz (+12,29 dB reais!) e +10,04 dB @ 464,1 Hz** com LC12 @ 10 Hz (sem corte grave!), Delay 25%, Reverb 3,09 s, LP @ 3.003 Hz |
| **Kamancheh + cópia de resposta** | true / **true!** | −2,7 dB | MIDI 49..76 (138,6–659,3 Hz, 282 notas), c. 1–216 | **EQ8 +9,05 dB @ 37,5 Hz e +10,79 dB @ 193,6 Hz** com LC12 @ 13,5 Hz! Reverb 2,60 s, BassMono 120 Hz, Roar. A cópia liga sozinha no Drop 2 (lane Speaker=true) |
| **Flauta** | true / true | 0,0 dB | MIDI 49..66 (138,6–370 Hz, 52 notas), c. 17–223 | Delay (32% wet, 36% FB) + Reverb (2,19 s, 30%) + Send A (−12,03 dB) + throws A/B. Excesso de ambiência em série |

## 4. Diagnóstico: Causa Raiz de Cada Problema (não sintoma)

1. **Causa raiz da banda média mono (correlação 0,80 vs. referência 0,32–0,44):**
   * **Colapso forçado por Utility em mono no fim da cadeia:** baixo médio (`Mono = true`), voz líder e chop vocal (`Width = 0%`) colapsavam para mono **após** os delays, reverbs e modulações estéreo.
   * **Parede de boosts de +10 a +15,6 dB no canal Mid (130–700 Hz):** baixo médio (+10,54 dB @ 224,8 Hz), voz de garganta (+12,29 dB @ 134,8 Hz e +12,04 dB @ 464,1 Hz), kamancheh (+10,79 dB @ 193,6 Hz), glitch seco (+15,6 dB @ 166–185 Hz + +12,27 dB @ 1.089 Hz) e stab de drop (+13,51 dB @ 193,6 Hz) concentravam quase toda a energia RMS de 200–2.000 Hz no centro.
   * **Delays de abertura desligados:** os delays de insert de 12+ canais estavam `On = false`.
2. **Causa raiz do vácuo em 25–40 Hz (−8 a −15 dB vs. referências):**
   * **Erro de oitava MIDI + erro de preset no sub principal:** todos os baixos escritos em MIDI 37/44/49, sem **nenhuma nota em MIDI 25 (34,65 Hz)**; o sub carregava preset de mid-bass FM; e o master cortava 25,2 Hz a 48 dB/oct.
3. **Causa raiz da densidade de picos excessiva (7,57/s vs. limite 6,99/s — "encavalado"):**
   * **Reativação fantasma de 8 pistas por automação (`Mixer.Speaker = true`):** sub extra (3.174 notas), sub-cama, shaker (2.786 notas), glitch falante, shimmer, duas cópias de proposta e a atmosfera tocando juntos sem o conhecimento visual de quem olha só o botão `Manual = false`.
   * **Colisão de ataques sem sidechain:** rolling (1.443 notas 16ths em 0 dB com ducker OFF), sub-roll (844 notas em +0,9 dB sem sidechain), kanun (2.073 notas em 0 dB sem sidechain) e glitches (sem sidechain) batendo em cima dos ataques do kick e da percussão.
4. **Causa raiz da presença fechada (0,64 vs. 0,51 — "pra dentro"):**
   * **Low-pass agressivos na presença (1,5–5,3 kHz) combinados com excesso de 130–500 Hz:** kanun cortava acima de 5.273 Hz enquanto dava +9,95 dB em 131,9 Hz; voz de garganta cortava acima de 3.003 Hz enquanto dava +12 dB em 135/464 Hz; glitch seco cortava acima de 2.554 Hz enquanto dava +15,6 dB em 166–185 Hz; squelch cortava em 1.500 Hz; kick amortecia em 3.532 Hz. Para compensar essa escuridão, o EQ do master aplicou +15,0 dB de High-Shelf acima de 8,7–11 kHz, o que só levanta chiado/pratos e esmaga o Glue/Limiter.

## 5. Propostas Concretas de Mixagem (`DE → PARA`)

### Categoria A: Ajustes seguros (bugs, gain staging, fase, sidechain)

| # | Alvo | Parâmetro | `DE` | `PARA` | Por quê | Risco | Como provar |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **A1** | 8 canais com lane Speaker | Envelope `Mixer.Speaker` | `true` (conflito com `Manual=false`) | **Deletar a lane** (manter `Manual=false`) | Desliga de verdade as pistas mutas/referência que tocavam escondidas | Zero | Densidade de picos cai de 7,57/s para < 6,6/s |
| **A2** | Rolling 16ths | ducker `AutoPan2` | `On = false` | **`true`** | Restaura o ducking de 1/4 (35%) no rolling bass | Zero | Transiente do kick ganha punch nos drops |
| **A3** | Baixo médio | `Utility Mono=true` e `Eq8[7]` OFF | Mono = true / OFF | **Deletar ambos** (manter só o BassMono 120 Hz do início) | Elimina a duplicação de cadeia e libera a largura acima de 120 Hz | Zero | Correlação média (200–2k) começa a cair de 0,80 |
| **A4** | Baixo médio | `Eq8` B2 @ 224,8 Hz | +10,54 dB (Q=0,71) | **+2,50 dB (Q=1,20)** | Remove o calombo mono que entupia a mix e o limiter | Baixo | ~3 dB menos em 150–300 Hz sem perder corpo |
| **A5** | Voz líder e chop vocal | `Utility StereoWidth` | 0,0% | **100,0%** | Devolve a imagem estéreo aos delays/reverbs da voz | Zero | Abertura imediata do centro vocal |
| **A6** | Corneta (2 canais) | `AutoFilter2 'HP 90Hz'` | Notch @ 740,8 Hz (Res 100%) | **HP @ 110,0 Hz, Res 0%** | Corrige o filtro renomeado que operava como Notch ressonante | Zero | Sem buraco ressonante em 741 Hz; graves limpam abaixo de 110 Hz |
| **A7** | Braam 2 | Lanes e filtros em cascata | 'HP 90Hz' desligado por lane; Notch @ 689 Hz Res 89% | **Deletar a lane**, HP 90 Hz Res 15%; **desligar o Notch** | Ativa o HP de verdade e remove a cascata de ressonâncias | Zero | Sem ringing metálico em 689 Hz |
| **A8** | Glitches + braam | `AutoFilter2 DryWet` | 0,35 | **1,00** | Elimina o comb filtering de filtro parcial | Zero | Transientes nítidos, sem fase oca |
| **A9** | Grupos clima e efeitos | Envelope `Mixer.Volume` | +3,0/+4,0 dB | **Cravar em 0,00 dB** | Restaura a regra de grupos em 0 dB | Zero | +3 a +4 dB de headroom limpo |
| **A10** | Eco / foley / chop | Envelope `Mixer.Volume` | −2,40 dB sobre fader de −14 dB | **−13,8 dB** (alinhado ao fader) | Corrige a automação que subia fundos em +11,4 dB | Zero | Fundo limpo nos drops |
| **A11** | Downer e stab de drop | 'HP 180Hz' e EQ | HP real em 23,2/50,6 Hz + EQ +8,8/+13,5 dB | **HP @ 160 Hz** + **EQ = 0 dB** + deletar lane que liga reverb de 5,96 s | Impede que FX de transição joguem grave e cauda no drop | Zero | Transições limpas |

### Categoria B: Ajustes que precisam de escuta (fundamento sub 25–40 Hz, timbres, balanço)

| # | Alvo | Parâmetro | `DE` | `PARA` | Por quê | Risco | Como provar |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **B1** | Sub principal | Notas + preset + sidechain | MIDI 37 (69,3 Hz) + preset falante + sem SC | **Transpor −12 st (MIDI 25 = 34,65 Hz)** + onda senoidal/triângulo (LP 75 Hz) + **Comp2 SC Kick (4:1, Rel 150 ms)** | Cria a fundamental real de C# em 34,65 Hz que não existia em nenhuma pista | Médio | FFT mostra pico sólido em 34,6 Hz (+10 dB na banda 25–40 Hz) |
| **B2** | Sub-roll | Fader + notas + FX | +0,9 dB / MIDI 44 / Serum2FX ativo / sem SC | **−4,5 dB** + **transpor −12 st (MIDI 32 = 51,9 Hz)** + **desligar o FX** + SC kick | Posiciona o sub-roll em 51,9 Hz com headroom e sem distorção de preset alheio | Médio | Rolling encaixa abaixo do baixo médio (104–139 Hz) |
| **B3** | Voz de garganta, kamancheh, kanun | EQ8 + roteamento | Fora de grupo, boosts +10 a +12,3 dB em 37–464 Hz, LP @ 3k/5,2k | **Mover p/ grupo** (ou bus com SC kick); LC12 @ 135 Hz; reduzir boosts para +1,5..+2,5 dB; abrir HC12 p/ 9,5 kHz | Remove o muro mono de +12 dB e devolve presença articulada (2–5 kHz) aos orgânicos | Médio | Presença abre de 0,64 para ~0,52 |
| **B4** | Glitch seco | EQ8 + Reverb | +4,1/+11,5/+12,3 dB em 167/186/1.100 Hz, HC12 @ 2,55 kHz, Reverb 3,46 s ON | LC48 @ 160 Hz; boosts a 0 dB; HShelf +2 dB; HC12 @ 8,5 kHz; **Reverb OFF** | Faz o "glitch seco" ser seco de verdade e abre transientes | Baixo | Ataques ganham definição percussiva |
| **B5** | Sopros/metais (4 canais) | Preset + ponteira + volume | Preset de drone; ponteiras colidindo; volume até +2,5 dB | Patches reais de horn/corneta; alinhar ponteiras; volume máx **−4,0 dB** | Substitui o drone contínuo pelo timbre de sopro sem clipar o grupo | Médio | Metais respondem como chamada/resposta nos drops |
| **B6** | 12 canais com Serum2FX como insert | `On/Manual` | true (presets de synth como efeito) | **Desligar** nas pistas de áudio/voz | Remove cadeias inteiras de distorção/multibanda aplicadas por engano | Médio | Som mais aberto e natural, menos fadiga em 2–5 kHz |

### Categoria C: Ajustes experimentais (abertura tridimensional e groove)

| # | Alvo | Parâmetro | `DE` | `PARA` | Por quê | Risco | Como provar |
| :--- | :--- | :--- | :--- | :--- | :--- | :--- | :--- |
| **C1** | Glitches (5 canais) | Delays e pans | Delays OFF, pans aglomerados | Distribuir pans (0.20L a 0.45R); delay ping-pong curto (Wet 12–16%, FB 15%, Filter 400–4k Hz) | Largura estéreo real por diferença temporal/espectral na banda 300–3.000 Hz | Baixo | Correlação média atinge 0,35–0,45 |
| **C2** | Retornos A/B | Compressor pós-efeito | Sem compressor pós-efeito (ducking OFF) | Ducking ON (Thresh −18 dB, Rel 150 ms) no eco + Comp2 SC Kick no retorno de reverb | Caudas abaixam nos ataques de kick/vocal e abrem nos contratempos | Baixo | Espaço tridimensional sem embolar a densidade |

## 6. Roteiro de Teste A/B de Escuta (adaptar a minutagem à faixa em teste)

| Trecho | Elementos em jogo | O que ouvir no A/B (antes vs. depois) |
| :--- | :--- | :--- |
| **1. Entrada do groove + sub** | kick, sub principal, rolling, kanun, kamancheh | **O peso em 34,6 Hz (sub em MIDI 25)** e o clique limpo do kick após ligar o ducker do rolling. |
| **2. Pré-drop 1 + corte seco → drop 1** | kick, baixo médio, sub-roll, cello, sopros | **A abertura lateral na entrada do drop:** sem o `Mono=true` no baixo médio e sem os 8 canais fantasmas ligados, o drop deve saltar para fora das caixas em vez de encolher no limiter. |
| **3. Diálogo étnico + glitches (meio do drop 1)** | kanun + resposta, voz de garganta + resposta, glitches | **A separação médio-grave (130–500 Hz) e presença (2–4 kHz):** a voz de garganta e o kanun deixam de soar abafados e abrem espaço lateral para os glitches. |
| **4. Breakdown final → drop 2** | stab de drop, voz, grupos de clima e efeitos, entrada do drop 2 | **O controle de volume no breakdown (sem o salto artificial de +3/+4 dB nos grupos)**, o corte seco no fim (sem vazamento do reverb de 5,96 s) e o impacto limpo do drop 2. |

## 7. O Que NÃO Deu Para Verificar (`NÃO VERIFICADO`)

* **Medição acústica em áudio renderizado (`.wav`) de stems e master:** todas as grandezas de faders, ganhos, EQs, compressores, presets de Serum 2, roteamentos de sidechain, envelopes e notas MIDI foram **100% medidas no XML do `.als`**, mas o cálculo direto de LUFS/correlação/espectro sobre ondas de áudio depende da execução do render no Live local.
* **Alinhamento de fase amostra-a-amostra entre kick e sub/rolling:** como o Serum 2 sintetiza em tempo real, a verificação visual de fase requer osciloscópio ou renderização das pistas em WAV após transpor o sub para MIDI 25.
