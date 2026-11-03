# How to Make Hypnotic Techno Synth

> **Vídeo:** `v-mjY-Vlgv0` · **Canal:** Audioreakt · **Duração:** 8:20
> Legenda automática em inglês, lida integralmente (63,58 KiB). **Tem legenda.**
> Descrição oficial lida: *"How to make an hypnotic techno synth sound in Ableton Live using Ableton Wavetable."* Timeline da descrição: 00:00 Intro · 00:33 Synth Sound · 02:32 Effect Chain · 07:37 Midi Pattern.
>
> **Escopo real do vídeo:** uma única voz de synth (stab/pluck) construída do zero e a cadeia de FX que a
> transforma. O vídeo **não** monta kick, sub, baixo, hats ou arranjo, e não fala de mix. O que não estiver
> ancorado em timestamp abaixo é tradução, marcada `INFERÊNCIA` ou `HIPÓTESE`.

## Técnica ensinada (2-4 frases)

A fonte é um **wavetable em mono** com forma complexa (00:35.440), **posição em 100** (00:41.920) e dois
ajustes de efeito de oscilador — 100% (00:48.480) e "around 20" (00:57.039) — que "add really some bites to
some of the wave" (00:53.199). O ataque percussivo **não** vem do amp envelope: o amp fica com attack zero e
"sustain almost to the maximum" (01:27.439–01:28.320), enquanto um **segundo envelope no filtro low-pass estilo
MS-20** (01:12.479) com amount "around 68" (01:38.960), attack "zero millisecond" (01:45.759) e decay
"around 200 milliseconds" (01:52.479) produz "something very very sharp" (01:53.680). O movimento — miolo do
estudo textura-atmosfera — vem de **Chorus-Ensemble** Classic com width 50 e rate ~2 Hz (03:35–03:56),
**flanger lento** a 1,18 Hz com amount 78, feedback, polaridade invertida "to make it a bit more nasal" e dry/wet
final ~30% (04:10–05:48), um **segundo LFO muito lento** sobre o flanger (04:54–05:13), **Echo** em sync/link com
HP ~1,5 kHz, ressonância ~26 e LP 11 kHz (06:01–06:43) e **Hybrid Reverb** em Shimmer com decay reduzido,
size/damping 50, shimmer 100 e diffusion 90 (06:58–07:28). No fim, o **padrão de MIDI** salta entre 0 e
+6 semitons e repete notas ("once two times up one times down one times up two times down", 07:50.319), e ele
afirma que "obviously the midi pattern does a lot" (07:38.960) — a hipnose é repetição com deslocamento de
altura, não um riff novo.

## Ferramentas usadas no vídeo (plugin/stock)

A descrição é explícita: **Ableton Live + Ableton Wavetable**. Todos os FX identificados são **stock do Live**;
o vídeo não nomeia os devices de FX um por um, então a identificação abaixo é por parâmetros + descrição
(`INFERÊNCIA`), não por fala literal do apresentador.

| Device | Papel no vídeo | Prova (legenda) |
|---|---|---|
| **Wavetable** (Live) | Fonte: mono, wavetable complexo, posição 100, dois ajustes de efeito de oscilador (`INFERÊNCIA`: Effect 1/Effect 2); matriz de modulação; dois LFOs; envelopes (o vídeo usa amp + filtro) | "you need to set in mono and we're going to select a complex waveform" (00:35.440); "bring the position to 100" (00:41.920); "apply some effects" (00:46.320) … "wrap it at 100" (00:48.480); "then default we're going to put around 20" (00:57.039); "it appears in the matrix" (01:35.280) |
| **Filtro low-pass "MS-20"** | Filtro principal, fechado para abrir rápido com envelope | "we're gonna choose the ms20 style" (01:12.479); "bring the filter down because we want to open it fast" (01:14.880) |
| **Amp** (Live) | "Boost mode", saída estéreo, dry/wet 100%; gain/bass/mid/treble a gosto | "use amp that we're gonna use in boost" (02:38.319); "set the output in stereo" (02:40.400); "leave the dry weight at 100 percent" (02:42.640); "adjust gain bass mid triple to my taste" (02:48.160) |
| **Saturator** (Live) | Modo **Hard Clip**; output −5 dB | "grab saturated and put in hard code mode" (03:16.480); "reduce the output to -5" (03:22.640). O binário do Live 12 contém a string **"Hard Clip"** e o script do Saturator expõe `Post Clip Mode` / `Hard` (verificado na sessão original) |
| **Chorus-Ensemble** (Live) | Modo Classic, width 50, rate ~2 Hz, amount alto; feedback/polaridade default | "start with a chorus ensemble" (03:35.519); "live in classic" (03:38.879); "bring up the weeds" / "draw it at 50" (03:40.319–03:44.799); "around two hairs" (03:56.560) |
| **Phaser-Flanger** (Live, modo Flanger) | Rate 1,18 Hz, amount 78, feedback, polaridade invertida, dry/wet 30–50%, LFO2 lento | "add some flanger" (04:10.720); "a very slow flanger movement" (04:12.959); "set the rate in earth at" (04:22.079) … "one point eighteen" (04:26.080); "bring down the amount 78" (04:31.199); "switch the polarity to make it a bit more nasal" (04:35.680); "the dry weight is at 50 percent" (04:47.040); "access to the second lfo" (04:55.840); "around 30" (05:48.320) |
| **Echo** (Live) | Sync + link, time "7", offset R pequeno, dry/wet menor, filtro HP ~1,5 kHz (res ~26) e LP 11 kHz | "use echo … live in sync and link" (06:02.880–06:04.319); "time at" (06:08.240) … "seven" (06:08.240); "shift a little bit the right" (06:12.080); "a bit less dry wet" (06:16.400); "hypothetical around one kilohertz and half" (06:26.800); "around 26" (06:40.080); "filter runs 11" (06:43.919) … "kilohertz" (06:43.919) |
| **Hybrid Reverb** (Live) | Modo Algorithm → Shimmer; decay reduzido, size/damping 50, shimmer 100, diffusion 90 | "add a bit of hybrid reverb" (06:58.960); "just with the algorithm mode" (07:01.280); "put in shimmer" (07:03.599); "reduce gyrate around 30 percent" (07:10.639); "leave size and dumping around 50" (07:12.400); "we do want the shimmer at 100" (07:19.919–07:22.080); "we also want the diffusion" (07:23.520) … "somewhat at 90 percent" (07:27.360) |

**Nenhum plugin de terceiros.** O vídeo **não menciona** ANA 2, VELA, SideKick, Kick 3 nem Bitwig. O banco
"Wavetable Techno Bank 3" da descrição é um pacote de **wavetables para o Wavetable do Live**, não um synth
externo.

### Ressalvas de legenda automática (não inventar a partir do erro)

- **"wrap"/"wall"** (00:46.320, 00:51.600): o contexto é "add really some bites to some of the wave"
  (00:53.199); no Wavetable isso corresponde a um dos **estágios de Effect do oscilador**
  (`Voice_Oscillator1_Effects_Effect1/2` no preset default do device). O nome exato do parâmetro na tela
  **não é dito** → `NÃO IDENTIFICADO`.
- **"octa face"** (00:40.480): nome do wavetable do banco pago. **Não identificado**; não é um wavetable de
  fábrica necessariamente.
- **"fdb"** (01:10.799): provavelmente "filter"; **não identificado** com certeza.
- **"gk"/"dk"** (01:31.119, 01:51.759): **decay** (o próprio vídeo já disse "decay" antes).
- **"break down the system"** (01:48.000): pelo contexto ("you want something plucky"), é **bring down the
  decay** — `INFERÊNCIA`.
- **"earth"** (02:17.920, 04:22.079): **Hz**.
- **"hairs"** (03:56.560): **Hz** (rate ~2 Hz).
- **"weeds"** (03:40.319): **width**.
- **"hypothetical"** (06:26.800): **high-pass filter** (HPF).
- **"gyrate" / "dumping"** (07:10.639, 07:13.120): **decay / damping**.
- **"driver at one percent"** (04:17.680): o Phaser-Flanger do Live 12 **não tem "Drive"** (tem Rate, Amount,
  Feedback, Invert Wet, Spread, Warmth, Dry/Wet). O parâmetro exato **não identificado** → `NÃO VERIFICADO`.
- **"drywall"** (05:40.880): **dry/wet**.
- **"hard code mode"** (03:18.560): **Hard Clip** (modo real do Saturator do Live 12, verificado).
- **"triple"** (02:49.440): **treble**.
- **"nsync mode"** (02:13.920): **sync mode** — mas o vídeo também manda "rate around eight earth"
  (02:16.800), o que é taxa em Hz, não divisão sincronizada. **A legenda se contradiz**; ver Limites.
- **"zero plus six"** (07:47.039): alturas **0 e +6 semitons**; **"balls"** (07:49.280) provavelmente "notes" ou
  "octaves" — `NÃO IDENTIFICADO`.

## Equivalentes e verificação de dispositivos

**O vídeo não depende de nada além do Live 12 Suite.** A rota inteira é stock: Wavetable + Amp +
Saturator + Chorus-Ensemble + Phaser-Flanger + Echo + Hybrid Reverb — devices confirmados presentes no Live 12
Suite na sessão original. **Não é caso de "equivalente"**; é caso de usar os mesmos devices. O preset do vídeo
é oferecido para **Live 11** (link na descrição) e um ambiente atual é **Live 12** — os devices existem, mas
alguns nomes/faixas de parâmetro podem diferir. Parâmetros confirmados lendo presets `.adv` do app:

- **Hybrid Reverb:** `Algorithm_Shimmer`, `Algorithm_Diffusion`, `Algorithm_Decay`, `Algorithm_Size`,
  `Algorithm_Damping` existem; o device também tem `BassMono` e `StereoWidth`.
- **Echo:** `Filter_HighPassFrequency`, `Filter_HighPassResonance`, `Filter_LowPassFrequency`,
  `Filter_LowPassResonance`, `Delay_TimeLink`, `DryWet`.
- **Chorus-Ensemble:** `Mode`, `Width`, `Rate`, `Amount`, `Feedback`, `InvertFeedback`, `DryWet`.
- **Phaser-Flanger:** `Mode`, `Modulation_Frequency`, `Modulation_Frequency2`, `Modulation_LfoBlend`,
  `Feedback`, `InvertWet`, `DryWet`.
- **Wavetable:** `Voice_Oscillator1_Effects_Effect1/2`, `Voice_Modulators_Lfo1_Time_Sync`,
  `Voice_Modulators_Lfo1_Retrigger`, `Voice_Filter1_Type`.

### Se a camada nascer no Serum 2 (mapeamento conceitual)

O vídeo **não usa granular**; `GranularOsc` não é necessário aqui. Mapeamento aproximado:

| Vídeo (Wavetable) | Serum 2 (aproximação) | Observação |
|---|---|---|
| Mono | `global.mono: true`, `poly_count: 1` | Mesma função: sem unison, uma voz |
| Wavetable position 100 | `oscillators[0].table_position: 1.0` | — |
| Effect 1 a 100% | `warp_amount: 1.0` + `warp_mode` a escolher | O "Effect" do Wavetable não é o "Warp" do Serum; é o estágio equivalente |
| Segundo estágio "around 20" | `warp_mode2` + `warp_amount2: 0.2` | `INFERÊNCIA`: o vídeo não diz que é o segundo Effect; é a leitura mais provável |
| Filtro LP MS-20 | `filters[0]: lowpass_24` (ou moog_lowpass_24) com `resonance`/`drive` | O Serum 2 **não tem modelo MS-20**; é aproximação, não o mesmo circuito |
| Envelope de filtro amount 68 | `mod_routes: env1 → filter0.cutoff, amount 68` | — |
| Attack 0 / decay 200 ms | `envelopes[1]: attack 0.0005, decay 0.2, sustain 0` | Envelope 2 como filtro |
| Sustain "almost max" | `envelopes[0].sustain: 0.95` | Amp envelope |
| LFO sine 8 Hz, retrigger | `lfos[0]: shape sine, rate 8, beat_sync false, mode Retrig` | — |
| LFO → pitch ±2 semitons, depois reduz amount | `lfo0 → oscillator0.pitch`, amount pequeno | A unidade de `amount` para pitch **não está documentada** → ajustar de ouvido; `NÃO VERIFICADO` |

## Notas de aplicação (por função)

**Contexto do projeto de referência:** médio 300–1.200 Hz em −4,83 dB e 1.200–4.000 Hz em −5,76 dB contra a média de 6 referências; low-end mono; groove deslocado .27/.77 a preservar. (Veio do projeto, não de medição nova.) Regras de referência adotadas na tradução: stab com HP 120–180 Hz, identidade em 300 Hz–4 kHz, brilho seletivo 6–12 kHz; atmosfera com HP 120–300 Hz e obrigação de "respirar"; veto a resolver brilho adicionando transientes.

| Função | Aplicar? | Como | Guarda-corpo |
|---|---|---|---|
| **Kick** | **Não** | O vídeo não trata de kick; não há transplante | Não passar Hard Clip/Saturator no bus de bateria; o drive do vídeo é no stab |
| **Sub** | **Não** | Manter o sub como está, mono e seco | Nenhum chorus/flanger/echo no sub; o HP do stab em 200–250 Hz é a proteção |
| **Baixo/rolling** | **Não** (no máximo a articulação) | Se quiser o "pluck", copiar **só** o envelope de filtro (0 ms / 200 ms) numa cópia mono do baixo | Sem FX estéreo, sem salto de oitava, sem tirar o low-end do mono; não usar 0/+6 no baixo |
| **Hats/shaker** | **Baixa** | Só a ideia de decay curto + HP; nada de chorus/flanger | Não adicionar eventos: a densidade de transientes do projeto pode estar no teto |
| **Percussão de resposta** | **Sim — alvo 1** | O stab curto como resposta, encaixado nos deslocamentos do groove; 2–3 eventos por compasso no máximo; o delay/reverb criam a densidade | Não quantizar em 1/16 reto; não dobrar o kick; não colocar no downbeat |
| **Madeira** | **Média** | Usar só o envelope de filtro (0 ms / 200 ms) + wavetable orgânico; sem Hard Clip, sem shimmer, sem flanger; banda ~400 Hz–2 kHz | Evita o caráter metálico; é adaptação, não o timbre do vídeo |
| **Stab** | **Sim — alvo principal** | Cadeia completa do vídeo, com os ajustes da receita abaixo | HP 200–250 Hz, LP 10–11 kHz, fonte mono, dry/wet do flanger 30% |
| **Subida** | **Baixa/média** | Usar o LFO lento no amount do flanger e automatizar o send de shimmer em 4–8 compassos; **não** é um riser | Sem pitch rise; não criar um sweep novo; a subida é textura, não evento |
| **Atmosfera** | **Sim — alvo 2** | Hybrid Reverb Shimmer 100% wet num **retorno**, HP 300–600 Hz, BassMono on, + Echo; automação lenta para respirar | Não virar cama contínua; retorno baixo (−12 a −18 dB, `HIPÓTESE`) |

### Receita de adaptação (vídeo → ajuste de projeto)

1. **Canal novo de stab hipnótico**, fonte **mono**. Wavetable: forma complexa, Position 100%, Effect 1 a
   100%, Effect 2 ~20% (o vídeo não nomeia os dois Effects; `INFERÊNCIA`; ou Serum 2:
   `table_position 1.0`, `warp_amount 1.0`, `warp_amount2 0.2`). `VIDEO` 00:35–00:57.
2. **Filtro** low-pass "MS-20" fechado, envelope amount ~68%, attack 0, decay ~200 ms, sustain 0; amp com
   attack 0 e sustain ~0.95. `VIDEO` 01:12–01:53.
3. **Vibrato** discreto: LFO1 sine, retrigger, ~8 Hz, profundidade **menor que 2 semitons** (o vídeo reduz o
   amount depois de mirar 2). `VIDEO` 02:05–02:20; a taxa é `HIPÓTESE` (ver Limites).
4. **Amp** (Boost) → **Saturator Hard Clip**, output −5 dB. `VIDEO` 02:38–03:26. `AJUSTE`: drive baixo,
   A/B contra o dry; se ficar metálico, Soft Clip/Hard Curve; **nunca** no bus.
5. **Chorus-Ensemble** Classic, Width 50, Rate ~2 Hz, Amount alto, Feedback/polaridade default.
   `VIDEO` 03:35–04:07.
6. **Phaser-Flanger** em Flanger: Rate 1,18 Hz, Amount 78, Feedback moderado, Invert Wet (nasal), Dry/Wet 30%;
   LFO2 lento (0,1–0,3 Hz) no blend/amount, ~50%. `VIDEO` 04:10–05:50; o rate do LFO2 é `HIPÓTESE` porque a
   legenda diz "around 11 hertz" para um movimento "very slow" (contradição).
7. **Echo**: Sync + Link, Time "7" (`NÃO IDENTIFICADO`; se for 7/16, combina com deslocamentos de groove — testar), offset R
   pequeno, Dry/Wet baixo, HP 1,5 kHz com ressonância ~26, LP 11 kHz. `VIDEO` 06:01–06:56.
8. **Hybrid Reverb num retorno**: Algorithm/Shimmer, Decay reduzido (o vídeo diz "30 percent"; no
   device o parâmetro é tempo, então **não converter para segundos sem escuta**), Size/Damping 50, Shimmer 100,
   Diffusion 90, **BassMono on**, HP 300 Hz, retorno −12 a −18 dB. `VIDEO` 06:58–07:28 + `AJUSTE`.
9. **MIDI**: manter a lógica de repetição com salto de altura, mas **trocar o +6** (trítono G, fora do C#
   frígio) por **+7 (G#)** ou **+1 (D)**; saltos de oitava só no stab, nunca no sub/baixo. `VIDEO`
   07:38–08:02 + `AJUSTE`.
10. **Colocação sugerida** (`HIPÓTESE`): entrada em bar 17 (00:30 num projeto a 128 BPM), 2–3 eventos por
    compasso nos deslocamentos do groove; automação de 8 compassos no amount do flanger/send de shimmer;
    nenhuma mudança no groove existente.

### Como não engordar o sub

- HP de 200–250 Hz no stab seco (mais alto que o HP 120–180 Hz genérico de referência, porque aqui o sub é a prioridade); HP 1,5 kHz **só no delay**; HP 300 Hz no retorno de reverb.
- Fonte mono; o estéreo nasce **acima de 200 Hz**, no chorus/flanger/echo. Conferir a soma mono.
- Hybrid Reverb com **BassMono** ligado e StereoWidth moderado.
- Não rotear o stab para o bus de graves; não usar sidechain no kick; não aplicar o padrão 0/+6 no baixo.

### Como não criar brilho metálico

- Hard Clip com drive baixo e A/B; o Hard Clip com output −5 dB é o ponto que mais pede A/B (`HIPÓTESE`: o vídeo não isola o que causa aspereza).
- LP 10–11 kHz no sinal seco; o Echo já tem LP 11 kHz no vídeo.
- Flanger em **30% wet** (valor final do vídeo), não 50%; feedback baixo; Invert Wet opcional.
- Shimmer só no retorno, com HP ~1,5 kHz e LP ~8 kHz (ajuste), retorno baixo.
- Checar 3–6 kHz depois de ligar chorus+flanger+clip; se a soma ficar nasal, cortar 1–2 dB com Q estreito (`HIPÓTESE`).
- Densidade: no máximo 2–3 eventos de stab por compasso; a "densidade" do vídeo vem das caudas, não de mais notas.

## Prioridade e esforço

**Prioridade: alta.** A técnica ataca exatamente as duas bandas que costumam estar abaixo da média (300–1.200 Hz e 1.200–4.000 Hz), é 100% stock do Live 12 — já instalado — e entrega a frente textura-atmosfera pelo movimento (chorus + flanger + LFO lento + echo + shimmer), não por mais camadas.

**Esforço: médio.** Um canal novo + 5 devices + 1 retorno + 1 automação; nenhum plugin, sample ou preset pago necessário. O custo real é a afinação: três estágios de modulação (chorus, flanger e LFO2) e a checagem mono/metálica exigem A/B. Não é baixo porque a cadeia tem muitas variáveis; não é alto porque não mexe em arranjo, kick, sub ou baixo.

## Trechos de prova: citações literais da legenda com timestamp

**1. Fonte mono + wavetable complexo (00:35.440):**

> 00:35.440 you need to set in mono and we're going to select a complex waveform

**2. O pluck vem do envelope do filtro, com attack zero (01:42.880–01:45.759):**

> 01:42.880 now you need to shape this envelope and you want a very fast attack
> 01:45.759 so zero millisecond

**3. O núcleo textural é um flanger muito lento (04:12.959):**

> 04:12.959 basically what we want it's a very slow flanger movement

## Limites e o que NÃO foi verificado

- **Nenhum áudio foi renderizado, escutado ou medido** na sessão original; não há A/B. O mapa é leitura de legenda + descrição + verificação de devices/parâmetros no app instalado.
- O vídeo **não dá** o nome do wavetable ("octa face"), o modelo exato do filtro no Wavetable 12, o BPM, a tonalidade, o HP do sinal seco, o Q do filtro, o valor exato de "time at" / "seven" no Echo, o que é "driver at one percent", nem o rate real do LFO2 ("around 11 hertz" contradiz "very slow"). Nada disso foi inventado; onde há número sugerido, está `HIPÓTESE`.
- "11 hertz" para um LFO "muito lento" é **contraditório**; pode ser 0,11 Hz ou uma divisão sincronizada. Não usar esse número como verdade.
- O LFO de pitch: o vídeo diz "trigger and nsync mode" e também "rate around eight earth" (Hz); as duas coisas não fecham. A tradução usa 8 Hz livre com retrigger como `HIPÓTESE`.
- A unidade de `amount` do Serum 2 para `oscillator0.pitch` não está documentada → ajuste por ouvido, `NÃO VERIFICADO`.
- O mapeamento "Effect 1/Effect 2" do Wavetable para "Warp/warp2" do Serum 2 é conceitual, não idêntico.
- O padrão de MIDI do vídeo usa **0 e +6 semitons** (trítono). Em C# frígio, +6 cai em **G natural**, fora da escala; a troca por +7/+1 é decisão de projeto, não do vídeo.
- O preset do vídeo é oferecido para **Live 11** (link da descrição); ambientes Live 12 podem diferir em nomes/faixas.
