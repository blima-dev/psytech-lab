# Full Psytech Breakdown Pt 1: Kick, Bass, Drums

- **Canal:** MERAKKI
- **URL:** https://www.youtube.com/watch?v=jomEtF3s_E0
- **Duração:** ~20:00
- **Tema:** bateria-percussão / pressão de grave / sound design Serum 2 · gênero: psytech
- **Legenda:** transcrição completa normalizada (legenda automática), lida integralmente. Sem escuta do áudio (limites ao final).
- **Contexto:** parte 1 do breakdown de faixa psytech completa em Serum 2 — kick sintetizado, bass com sub
  separado, offbeat hat, clap de ruído custom, shakers rolling, ghost hits e knock. Parte 2 = vídeo `cAxR-CRSe_c`.

## Técnica ensinada

**KICK (sintetizado no Serum):**
- Sine com **pitch bend em glide consistente** — *"the shape of your pitch bend and your amplitude envelopes
  are everything when it comes to kicks… a nice consistent glide [gives] a nice representation of the whole
  spectrum in one nice pulse"*.
- **Segundo envelope de pitch no 16avo, sliver minúsculo** = potência extra do transiente inicial.
- Envelope de volume esculpe o kick com **osciloscópio aberto** (arrastar o ponto = sub incha na cauda; quantos
  mids entram). Fade curtinho doma o click; a quantidade de click = quanto high-end a track tem.
- FX: **frequency splitting** sutil = "rubberiness" — com o alerta: *"with kicks, especially for psy music,
  it's all about making them super clean. Every time you add a little bit of processing, you are battling
  against that cleanliness"*.
- EQ: corte de low-mids @128 + shelf @500 com **automação de ganho** que reduz highs/mids rápido após o hit
  (kick mais fundo, espaço no médio).
- ⭐ **Cleanup LFO:** Utility com ganho modulado por LFO em fadeout que **desliga tudo no 1/8 exato** —
  *"any kind of smearing or extension to the kick that would be happening from these EQs is mitigated… it
  shuts off at 1/8 perfectly to keep the bassline nice and clean"*. O processamento nunca vaza para o tempo
  do baixo.
- Reverb a **1% de mix** — *"when a kick plays hundreds of times in a track, making it just that slight bit
  softer can make it way more pleasing for a longer duration"*.

**BASS (saw com fase dispersa, sub separado):**
- Envelope de volume DESLIZANTE por quarter: **volume baixo quando o kick entra, sobe no offbeat, some antes
  do próximo kick** (fade out antes da chegada). O SUB tem envelope próprio, separado do oscilador principal
  (*"I've got the sub removed out of our main oscillator so that I can control the main oscillator and the
  sub separately"*), entrando depois do principal. Um terceiro envelope modula levemente o cutoff do LP.
- **Camada estéreo mono-safe:** cópia do osc principal com harmônicos graves rolados para fora, panning por
  outro oscilador **em audio rate** ("very quickly panning from left to right… a nice wide version… that
  doesn't have as many low frequencies"); ganho baixo — *"you just need enough to add a little bit more
  information on the sides"*.
- EQ de escurecimento com LFO pluck (cauda com menos highs) + **cleanup LFO de quarter** depois de EQ move
  ("because I've done an EQ move, I want to make sure everything is clean").
- Movimento do cutoff em **MACRO com clip de automação** ("a few different expressions for the cutoff… most
  expression at the end").

**OFFBEAT HAT (Serum):** FM do ruído + blend; EQ + frequency shifter para posicionar; reverb leve ("organic")
+ waveshaper para harmônicos.

**CLAP (ruído custom — receita completa):**
- Saw → sine shaper (complexidade harmônica) → **FM do ruído** = *"this is how you can make endless custom
  noises… using extreme FM. Eventually, it just becomes noise"*; o pitch do ruído muda o caráter.
- Panning em audio rate (osc B → pan de A, 59% bipolar) alarga o ruído.
- LFO em modo envelope com **picos** = o caráter do hit inicial — *"these spikes… is emulating multiple people
  clapping in quick succession"*; rate: lento = stutter, rápido = burst sem graça; *"8.1 hertz sounded really
  nice"*.
- Burst de energia no ataque (EQ boost ~1100 + shelf 3k + lows + distorção), diffuser mixado FORA (faz de
  phaser), phaser estático com polos no talo mixado fora ("adds flavor, less uniform"), **par HP+LP** que
  afina highs/lows conforme o som corre ("contained… more like a real clap"), distorção, compressão snappy;
  depois: Saturn 2, hard clip, reverb 2,9%, transient processor. *"You're basically just trying to EQ white
  noise until it sounds good."*

**SHAKERS ROLLING (o padrão dos 3 hits):**
- Notas MIDI de quarter + **envelope de quarter com 3 hits**: primeiro hit BAIXO no 2º 16avo, **sem hit no
  1º tempo** (*"we already have a nice transient layer on our kick, so I don't want to be interfering"*),
  offbeat pronunciado, último 16avo mais baixo — *"this is the kind of pattern that you'd see on the
  velocities of a rolling bass in most psytrance… a really satisfying up and down groove"*.
- Random de velocity ("note on random discrete", os 3 randomizam por quarter) + modulação da curva (mais
  aberto/fechado) + envelopes abrindo ao longo de 2 compassos + smoothing = menos rígido, elemento de FUNDO
  (*"the function of these 16ths is not to take too much of the focus, but to add a bit of energy… harmonic
  tempo"*).
- **A tese:** *"these three elements [open hat, shakers, snare/clap] are going to be in pretty much every
  psytech/psytrance track… if you can get your bassline and drums locked in, writing the rest of the track
  becomes considerably easier."*

**Ghost hits / knock / reverb sidechain:**
- Ghost percussões **pequenas e silenciosas nos slots sincopados** (nem offbeat nem downbeat) — *"they kind
  of help things keep grooving"*.
- Knock one-shot: saw + FM do ruído + 2 envelopes + reverb — *"really nice for when a track first drops in
  because you have all of this open space"*.
- **Reverb com sidechain interno:** peak controller vendo o sinal — *"every time a percussive hits, the
  reverb is ducking out the way"* → orgânico e maior sem lama.
- **Frequency shifter é o melhor amigo para variações** — *"bounce different versions of it at different
  pitches… a ridiculous amount of material"*.

## Ferramenta usada no vídeo (plugin/stock)

Serum 2 (kick/bass/hat/clap/shakers todos no Serum), Utility+LFO (cleanup), EQ Eight, Saturn 2, Newfangled
Saturate, Valhalla Room, transient processor, frequency shifter, peak controller.

## Tradução para ambiente comum: Serum 2, Live 12 nativo

- **Cleanup LFO no 1/8** = fecho de cauda exato para kick com EQ/splitting: receita exata para matar o smear
  no tempo exato — casa com a célula de cauda curta de kick (~117 ms ≈ 1/16 a 128 BPM).
- **Envelope deslizante do bass (kick in → offbeat up → fade antes do próximo kick)** = o desenho clássico do
  rolling bass psy: terminar/liberar antes do próximo evento.
- **Sub separado do oscilador principal** = confirma a arquitetura comum do estilo (sub cama + corpo camada).
- **Largura por audio-rate pan com graves rolados e ganho baixo** = largura sem violar o low-end mono.
- **Shaker em 3 hits/quarter com velocity do rolling bass e SEM hit no 1º tempo** = desenho de esteira de topo
  que não interfere no transiente do kick — resolve o embolado de topo.
- **Reverb com duck por peak controller** = resposta orgânica nos sends, sem lama.
- **"Os 3 elementos (open hat, shaker, clap) trancados entre si + bassline"** = critério de progressão:
  perfeccionar a RELAÇÃO antes de adicionar família nova.

## Aplicação sugerida (checklist de teste, **proposta**)

1. **KICK:** cleanup LFO (Utility+LFO fadeout no 1/8) como camada de teste A/B; conferir smear pós-EQ.
2. **SHAKER/HATS:** redesenhar como 3 hits/quarter (baixo no 2º 16, zero no 1º tempo, offbeat pronunciado,
   último 16 mais baixo) + random discrete — A/B em camada de teste.
3. **BAIXO:** conferir se o envelope atual faz o fade ANTES do próximo kick (cauda invadindo o kick é causa
   comum de grave gordo entre 55–75 Hz).
4. **Ghost hits:** slots sincopados silenciosos com nível "pequeno e silencioso".

## Contrastes/cautelas

- Saturação/clips no clap (Saturn, hard clip): válidos em percussão de topo; **nunca no sub**.
- Frequency splitting no kick: se já existe cadeia de kick aprovada, experimentar em camada separada, nunca
  por cima do aprovado.
- Reverb em kick 1%: é kick (não solista acústico) e 1% é processamento mínimo — não fere a cautela usual de
  preservar dry em fonte com transiente.

## Trechos de prova (transcrição)

1. "any kind of smearing or extension to the kick that would be happening from these EQs is mitigated and
   cleaned up by this LFO, which makes sure that it shuts off at 1/8 perfectly to keep the bassline nice and
   clean."
2. "the volume low for when the kick is in, and then it comes in for the offbeat, and then it disappears
   again to make sure we've got a nice little bit of a fade out before the next kick comes in."
3. "I don't really want to be interfering with that [transient layer of the kick]… a really satisfying up
   and down groove… this is the kind of pattern that you'd see on the velocities of a rolling bass."
4. "if you can get your bassline and drums locked in, writing the rest of the track becomes considerably
   easier."

## Limites do estudo

Transcrição sem timestamps por frase; valores citados: 128 Hz, ~500 shelf, 8,1 Hz (rate do clap), 1% e 2,9%
de reverb, 59% de pan, 1100/3k. Plugins pagos dele (Saturn 2, Newfangled) traduzem para Saturator/clip do
Live. Áudio não escutado.
