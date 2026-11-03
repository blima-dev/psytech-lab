# How to Make POWERFUL Techno Stab (free preset)

**Canal:** Audioreakt · **ID:** `C3x8o9Krfc0` · **Duração:** 5:55 · **Tema:** stab "growling" de techno no Wavetable (Ableton Live stock).
**Fonte de estudo:** legenda automática em inglês do vídeo (`yt-dlp --write-auto-subs`), lida integralmente. A legenda é ASR e erra palavras técnicas ("Soto's" = sawtooth, "band pass heater" = bandpass filter, "GK" = provável decay). As citações mantêm o texto literal; os erros de ASR ficam anotados fora das aspas.

## Técnica ensinada (2-4 frases)

O vídeo constrói um stab "growling" do zero no Wavetable: oscilador em dente-de-serra, posição 0% ("go to basic and sold you all and make sure we are at zero percent", 00:44.219) e nota muito baixa — "play with d0" (00:37.320) — porque é a nota baixa que gera o "log rolling" (00:39.960; ASR: growling). O filtro é Band Pass de 24 dB no circuito OSR, com drive de "5 6 GB" [sic, 5–6 dB], centro em "around 100 Hertz" (01:09.900) e ressonância "around 50" (01:19.200); o Env 2 modula o corte com apenas "25" de intensidade e sobe rápido para voltar devagar — "quickly going up just to cut some higher frequency and then going back slowly" (02:17.459) — e é isso que gera o "scrolling effect" (00:49.920). O amp envelope fica "with no sustain" e release "around 600 millisecond"; a cadeia fecha com Unison clássico de 3 vozes a ~40%, Amp em Clean/Dual, EQ com low shelf em 300 Hz (+3–4 dB), delay ping-pong com feedback baixo, Hybrid Reverb em convolução (~5 s) e Drum Buss no fim para comprimir e compactar.

## Ferramenta usada no vídeo (plugin/stock)

Cadeia **100% stock do Ableton Live**; nenhum plugin de terceiros é citado. O sintetizador é o **Wavetable** — a legenda diz "load up wave table" (00:28.080), e os três detalhes que fecham a identificação são o circuito de filtro **OSR** (01:03.899), o **Unison "classic"** (02:30.060) e o **Matrix** (01:46.079), todos da UI do Wavetable [INFERÊNCIA a partir dessas três pistas]. O preset divulgado é do autor do vídeo: "this present was part of my wave table techno bang 4" (05:47.340) — ASR: "present" = preset, "bang" = bank.

- **Wavetable** — "go to basic and sold you all and make sure we are at zero percent and playing low node" (00:44.219; ASR: "sold you all" = Saw, "low node" = low note); band pass 24 dB "and we're gonna use the osr" (01:00.960–01:03.899); "classic Unison with three voice and a bit more dry wet we're gonna go around 40 percent" (02:30.060; "dry wet" = provável knob Amount do Unison).
- **Amp** (simulador de amplificador de guitarra) — "we're gonna go to amp we're gonna set the clean mode I'm gonna put it in dual because we still want our stereo" (02:59.940–03:05.570); "if you want more High you bring up the treble" (03:12.360).
- **EQ** (EQ Eight) — "we can use the low shelf you can go around 300 Hertz and just kind of boost everything by 3 4 DB" (03:36.120–03:42.710); mais tarde "boost maybe around one kilo have a high shaft" (04:55.500; ASR: "shaft" = shelf); e um low-pass no fim, "I like to use a low pass filter just up and chill" (03:42.720).
- **Delay** (ping-pong) — "add a bit of ping pong delay to make things move a little bit" (03:53.159); "put one in two and three and crank down the feedback" (03:58.500); filtro do delay "around one kilohertz" (04:12.420) e wet "around 30" (04:19.440).
- **Hybrid Reverb** — "we're gonna use the hybrid Reverb and we're gonna use the convolution" (04:25.620); decay "around 5 Seconds" (04:47.100); IR citado como "Monarch Church" (04:35.820–04:38.930, ASR; escolher um IR de igreja/ambiente) [interpretação].
- **Drum Buss** — "the trick I like to use is to use drumbass at the end of the chain because you can use the compressor to kind of compress everything" (05:18.360–05:24.650); "I will crank up the drive" (05:29.280); "I will use transient negativity to kind of reduce the tail of the Reverb" (05:36.180; termo ASR ambíguo) — o objetivo declarado é encurtar a cauda, não alargar o ataque.
- **Mono do corpo grave** — "make sure the base is in mono" (05:05.699) e "reduce the dry weight around 30 as well" (05:07.380; ASR: "dry weight" = dry/wet). Não fica claro se é Utility, mono de pista ou o botão do plugin; o alvo é o grave em mono, não um device específico.

## Rotas de tradução para outros synths

O vídeo **não depende** de plugins específicos — é uma sessão Ableton com devices stock (Wavetable, Amp, EQ, Delay, Hybrid Reverb, Drum Buss). A tradução para outros instrumentos é quase 1:1; o único ponto sem equivalente literal é o circuito **OSR** do filtro do Wavetable.

| Elemento | Equivalente / o que fazer |
|---|---|
| **Wavetable (Live)** | É o próprio device do vídeo: Basic → Saw, `Position 0%`, filtro Band Pass 24 dB com `Circuit = OSR`, `Drive` 5–6 dB, `Freq` ~100 Hz (no vídeo) e `Res` ~50; Env 2 → Filter com amount 25; amp env sem sustain e release 600 ms; Unison `Classic`, 3 vozes, ~40%. |
| **Amp (Live)** | Modo `Clean`, `Dual` ligado (mantém o estéreo do vídeo). Ganho/treble dosados. |
| **EQ Eight (Live)** | Low shelf em 300 Hz, +3–4 dB (03:36.120–03:42.710); high shelf em ~1 kHz é opcional e dosado (04:55.500); low-pass no fim (03:42.720). |
| **Delay (Live)** | Ping-pong, feedback baixo, filtro em ~1 kHz, wet ~30%. |
| **Hybrid Reverb (Live)** | Seção Convolution, IR de igreja/ambiente, decay ~5 s, wet ~30%; retorno com high-pass para não criar sub estéreo. |
| **Drum Buss (Live)** | Último insert: compressor para compactar + drive leve. `Transients` negativo se a cauda do reverb estiver longa (05:36.180). |
| **Utility (Live)** | `Bass Mono` a ~120 Hz na pista do stab — o próprio vídeo manda o grave em mono (05:05.699). |
| **Serum 2** | Osc A com Basic Shapes/Saw e posição 0%; Filter 1 Band Pass 24 dB com drive, ressonância ~50; Env 2 → `filter1.cutoff` com amount 25 (valor do vídeo no Wavetable; usar como ponto de partida e conferir de ouvido) [adaptação]; amp env sustain 0 / release 600 ms; Unison 3 vozes ~40%. O Serum não tem o circuito OSR: aproximar com saturação leve antes ou com o drive do filtro [adaptação]. |
| **Diva** | Oscilador saw, filtro multimodo em Band Pass, Env 2 → cutoff, 3 vozes/detune. O "OSR" e o Unison "Classic" são do Wavetable; o que importa é o band pass + envelope rápido [adaptação]. |
| **Vital / Massive X / Surge XT** | Mesmo conceito: wavetable/saw na posição 0, filtro Band Pass 24, filter env → cutoff com amount ~25, unison 3 vozes ~40% [adaptação]. |
| **Instruments sampleados (Kontakt etc.)** | Não se aplica: o vídeo é síntese (wavetable + filtro + envelopes), não instrumento amostrado. |

## Notas de aplicação em produção psytech/techno (por função)

**Leitura geral:** o vídeo entrega um stab de **resposta**, não uma camada de peso. O centro de band pass em "around 100 Hertz" (01:09.900) serve para depois modular com o Env 2 — "because the idea is to obviously modulate it with an envelope" (01:12.240–01:15.770). Se a faixa do sub já está ocupada pelo baixo do projeto, a adaptação típica é **mover o centro do band pass para ~250–400 Hz**: assim o sweep do Env 2 cai no miolo 300–1.200 Hz em vez de disputar o sub (num set de referência medido contra faixas de artista, esse miolo tende a ser a região mais fraca). Se o centro ficar em 100 Hz, o som vira camada de baixo — aí tem de ser tratado como baixo (mono, A/B contra o baixo existente), não como stab de resposta. [adaptação]

| Função | O que fazer | Limite / por quê |
|---|---|---|
| **Kick** | **Não aplicar.** O vídeo não trata de kick; não passar o kick pelo band pass + Env growl. | A cadeia do vídeo é de stab; nada aqui melhora o kick. |
| **Sub** | **Não aplicar.** Manter o stab com centro em 250–400 Hz e o sub intocado. | 100 Hz + nota D0 gera energia exatamente na zona do sub; somar isso engorda o grave. |
| **Baixo/rolling** | **Aplicação forte, como camada alternativa:** a mesma receita (nota baixa + band pass + envelope rápido) é uma máquina de rolling/growl. Testar em A/B contra o baixo atual, em mono <120 Hz, na tônica do projeto. | Não empilhar com o rolling existente — escolher um. Dois growls graves simultâneos viram lama e comem o espaço do kick. |
| **Hats/shaker** | **Não aplicar timbre.** A lição útil é de cauda: reduzir o feedback do delay ("crank down the feedback", 03:58.500) e o transient do Drum Buss para encurtar cauda (05:36.180). | Cauda longa de delay/reverb borra a leitura rítmica dos eventos deslocados do groove. |
| **Percussão de resposta** | **Aplicar aqui — é a casa natural do stab.** Posições de resposta do groove, release ~600 ms, delay/reverb curtos. | A cauda não pode cobrir os eventos de resposta nem o contratempo do open hat; o próprio vídeo diz que cauda longa "it's just gonna mess up with the rest of your mix" (04:05.990–04:08.220). |
| **Madeira** | **Não aplicar.** Madeira pede transiente e corpo acústico; band pass ressonante + Env rápido transforma em voz/metálico. | O vídeo não usa instrumento orgânico; a receita é para síntese. [adaptação] |
| **Stab** | **Aplicação principal.** Wavetable Basic/Saw, pos 0%, nota baixa na tônica do projeto → Band Pass 24 OSR, drive 5–6 dB, freq 250–400 Hz (adaptação), res ~50 → Env 2 no filtro com amount 25, ataque curto e volta lenta → amp env sem sustain, release 600 ms → Unison Classic 3 vozes ~40% → Amp Clean/Dual → EQ low shelf 300 Hz +3–4 dB → delay ping-pong feedback baixo → Hybrid Reverb convolução ~30% → Drum Buss no fim. [adaptação: nota e centro de freq] | É o alvo do vídeo e o que preenche o miolo 300–1.200 Hz sem tocar no sub. O topo é o risco: dosar. |
| **Subida** | **Aplicação parcial/experimental:** o mesmo Env de filtro (rápido na subida, lento na volta) pode automatizar um band pass de 300 Hz a 4 kHz como riser. | O vídeo **não ensina riser** — extrapolação. Usar em send e conferir que o sweep não passa pelo sub. |
| **Atmosfera** | **Aplicação parcial:** o Hybrid Reverb em convolução (~5 s) é a ferramenta de atmosfera do vídeo; usar como send, wet ~30%, retorno com high-pass (~300 Hz). | High-pass no retorno evita sub estéreo e mantém o low-end mono [adaptação]. O vídeo já manda "make sure the base is in mono" (05:05.699). |

**Como não engordar o sub**

1. Centro do band pass em **250–400 Hz** e sweep do Env 2 sem descer abaixo de ~120 Hz [adaptação].
2. **Utility `Bass Mono` a ~120 Hz** na pista do stab — o vídeo manda o grave em mono (05:05.699).
3. High-pass nos retornos de delay e reverb (~300 Hz) [adaptação].
4. Não usar o low shelf de 300 Hz para "compensar" o sub: ele é para o miolo, não para o grave.
5. Não duplicar o stab uma oitava abaixo para "dar peso" — o peso é do sub.

**Como não criar brilho metálico**

1. O vídeo levanta o topo em dois lugares: treble do Amp ("if you want more High you bring up the treble", 03:12.360) e high shelf em ~1 kHz ("have a high shaft", 04:55.500). Se o miolo 1,2–4 kHz estiver deficitário no próprio set, um pouco é bem-vindo — mas começar em **+1–2 dB, Q baixo**, e conferir se o band pass com res ~50 assobia.
2. Manter o Amp em **Clean** (03:00.599–03:02.030) e não subir gain/crunch; drive alto em sinal band passado vira metal.
3. Se o sweep "assobiar", **baixar a ressonância antes de subir EQ** — 50 é o valor do vídeo, não uma lei.
4. Usar o low-pass do fim do EQ (03:42.720) para domar o topo em vez de boostar.

**Ordem prática (uma pista, sem plugin novo)**

1. Wavetable: Basic/Saw, posição 0%, nota baixa na tônica do projeto.
2. Filtro Band Pass 24 dB, circuito OSR, drive 5–6 dB, freq 250–400 Hz, res ~50.
3. Env 2 → filtro, amount 25; ataque curto, decay longo ("the GK around one second and half", 02:10.020–02:15.949) e release 600 ms.
4. Amp env: sustain 0, release 600 ms.
5. Unison Classic, 3 vozes, ~40%.
6. Amp Clean/Dual → EQ Eight low shelf 300 Hz +3–4 dB → (opcional high shelf ~1 kHz +1–2 dB) → low-pass.
7. Delay ping-pong, feedback baixo, filtro ~1 kHz, wet ~30%.
8. Hybrid Reverb convolução ~5 s, wet ~30%, retorno com high-pass.
9. Drum Buss no fim: compressor + drive leve.
10. Utility Bass Mono ~120 Hz e A/B contra o sub e o baixo.

## Avaliação

- **Prioridade: alta** para quem quer preencher o miolo 300–1.200 Hz com um timbre novo sobre uma grade rítmica já fechada: o low shelf de 300 Hz mais o band pass deslocado atacam exatamente essa faixa sem tocar no sub.
- **Esforço: médio.** São várias etapas (synth → filtro/env → unison → Amp → EQ → delay → reverb → Drum Buss → Utility), mas todas stock e com valores dados pelo vídeo; o trabalho real é o A/B do centro do band pass (100 Hz do vídeo × 250–400 Hz do contexto), o controle de mono abaixo de 120 Hz e a dose de topo.

## Trechos de prova da legenda com timestamp

> Segunda dica do Audioreakt: bandpass + envelope rápido no filtro cria o efeito "scrolling" — **00:47.820–00:58.860** *(ASR: "band pass heater" = bandpass filter)*

> "the Soto's waveform that we're gonna play at a lower note so here we're gonna play with d0 and that's gonna give this log rolling not already" — **00:34.320–00:39.960** *(ASR: "Soto's" = sawtooth; "log rolling" = growling)*

> "final setting is to use the resonance to accentuate the scrolling effect so we're gonna go around 50 for the resonance" — **01:15.780–01:21.530**

---

**Fonte:** legenda automática EN do vídeo (ASR), obtida com `yt-dlp --skip-download --write-auto-subs --sub-langs en --convert-subs vtt`; citações com timestamps das cues. Nenhuma informação tirada da descrição do YouTube.
