# Full Psytech Breakdown Pt 2: Leads, Oneshots, and Glitches

**Canal:** MERAKKI · **ID:** `cAxR-CRSe_c` · **Duração:** ~25:00 · **Fonte:** transcrição completa normalizada via yt-dlp. **Não ouvi o áudio.**
**Contexto:** parte 2 do breakdown `jomEtF3s_E0` — sweeps, FM reverse, squelch, plucks, lead com modulação
audio-rate, glitch bank, e as regras de ARRANJO do drop.

## Técnica ensinada

**Regras de arranjo (o ouro da parte 2):**
- ⭐ **O gap de 1 compasso antes do drop:** *"it is very very important not to just build up straight into a
  drop. It's very important to release that tension, then just wait a moment because you'll get much much
  greater contrast and therefore a much more powerful drop."*
- ⭐ **O motor respira por HP no GRUPO kick+bass:** *"the kick and bass have this filter modulation where the
  filter gets mixed in when I'm going to do the filtering… I can just remove some of the low end. And make
  sure that when it comes back in on the next section, it's nice and deep again."* — algumas seções filtram
  por mais tempo (antes do arp; antes do breakdown).
- **Movimento tem limite:** no lead, ele mesmo critica — *"probably slightly too much movement because it's
  ending up actually taking away from the solidity and the focus"*.
- Snare rise: automações de envelope/cutoff/frequency shift subindo — *"as long as it feels like it's
  building towards something, you're pretty much in the clear"*.
- White noise swells com UM patch (macro de volume/cutoff/reverb) automatizado em tamanhos diferentes —
  *"brought in a little bit of noise where I thought needed a little bit more density"*.
- Intro usa pedaços da melodia exportada com mais reverb/delay: *"same sound palette… in a different
  fashion… introduces a bit of the flavor of the track without spoiling too much."*

**Sound design:**
- **FM reverse tonal:** 2 sines FM com movimento RISENTE (não pluck); o modulador tem forma flat→sine
  morfada pela posição da wavetable — *"a cleaner way to alter the amount of FM… the sound can just get very
  messy if you try and modulate the FM [amount] directly"*. Reverb alto = "FM tonal throw"; volume automatizado
  para o reverb PARAR na fronteira de seção (corte limpo).
- **Squelch:** saw (2 unison, random phase off, oitava baixa) com LFO de 1 bar no coarse pitch + **modulação
  OPOSTA no band-pass** = squelch imediato; diffuser ("liquidy") + flanger sweep (camada extra de movimento).
  Regra dele para SYNTH: mesmo seco de propósito, *"it's still nice if they have at least a little bit of
  reverb on them"* (send leve).
- **Plucks:** saw + sine fold, modulados por PD de outro saw, **random phase ZERO nos dois** (*"same every
  time we play it"* — determinismo); LFO ramp-down em volume+cutoff; **Utility com ganho modulado funciona de
  sidechain para esconder os stutters do início do MIDI** ("that's where the kick is going to be playing — we
  don't want to muddy that up").
- **Dotted plucks:** saw com 2 distorções (diode + "sim") = *"pseudo square-ifying… hollow square vibe"*;
  envelope de volume com release + envelope curto SÓ no filtro; distorção modulada pelo MESMO envelope do
  filtro.
- **Lead:** FM com random phase 0; **modulação de filtro em AUDIO RATE (sub oscilador controla o cutoff)** —
  *"because it's audio rate modulation, it is actually introducing a bit of tonality into the sound"*; a taxa
  do filtro muda ao mudar o pitch do sub modulador (variação de caráter); HP trazendo o lead devagar; OTT no
  fim ("quieter details much closer").
- **Sci-fi sweep:** 2 saws FM; a **RATE do LFO de cutoff modulada por outro LFO** — *"the rhythm of this sound
  is purely based on what shape this is… fine-tune the shape while working in context"*; comb afinado na
  tônica (38 Hz no demo dele).
- **Glitch bank:** *"make yourself a bunch of massive glitch pie… the hardest part isn't finding something
  good, it's just actually deciding on what you're going to go with."*
- Neuro fill: *"these sounds are different every time you make them… keep making them to refine your
  selection"*; A/B em contextos; 2ª vez uma oitava acima = variação barata.

## Ferramenta usada no vídeo
Serum 2 (tudo), diffuser, flanger, OTT, tonal delay, comb, Hyperdimension, Fruity Balance (volume de ponta).

## Leituras e traduções

- **Gap de 1 bar antes do drop** é regra de arranjo independente de projeto: nunca build direto no downbeat —
  soltar a tensão, esperar um momento, e o drop ganha contraste.
- **HP automatizado no grupo kick+bass como respiração de arranjo:** alternativa a tirar camadas por
  mute/nota — o mesmo contraste com o motor voltando "nice and deep" na seção seguinte. Cuidado técnico:
  automatizar o **MIX** do filtro (em paralelo), nunca HP fixo em série perto da fundamental.
- **Morph de forma no modulador para controlar FM amount** = o caminho limpo para variar FM sem sujar —
  convergente com o que se vê no vídeo `2YgKSex63Wg` (Scionaugh): dois artistas chegando ao mesmo gesto.
- **Random phase 0 nos plucks** = determinismo para camadas que precisam bater juntas.
- **Squelch = pitch sobe + band-pass desce (opostos)** = o "momento psy" por desenho de opostos, com receita
  exata.
- **Comb afinado na tônica** aparece 2× no canal (38 Hz) — convergência com `jjnsu2lnf98`.
- **Utility-gain como sidechain local** para esconder stutters onde o kick toca = micro-limpeza sem compressor.

## Aplicações sugeridas (genéricas)

1. Testar HP automatizado (mix paralelo) no grupo kick+bass nas fronteiras de seção, em cópia/pista de teste.
2. Subida: FM reverse tonal (2 sines, morph por wavetable position) como substituto de **textura** para quem
   evita riser tonal — não é um riser no sentido clássico.
3. Stab/resposta: random phase 0 + squelch de opostos como alternativa de timbre.

## Ressalvas

- "Todo synth merece um pouco de reverb" é regra para SYNTH. Em solistas acústicos/orgânicos (madeira, voz),
  prática conservadora preserva o dry e mantém wet baixo (≤ ~25%) ou paralelo.
- Movimento extremo no lead: o próprio autor reprova em excesso — melodia sóbria e focada fica intacta.

## Trechos de prova (transcrição)

1. "it is very very important not to just build up straight into a drop… release that tension, then just
   wait a moment because you'll get much much greater contrast and therefore a much more powerful drop."
2. "the kick and bass have this filter modulation… I can just remove some of the low end. And make sure that
   when it comes back in on the next section, it's nice and deep again."
3. "it's ending up actually taking away from the solidity and the focus in the lead." (autocrítica de
   movimento demais)

## Limites
Sem timestamps; demo em D# (comb 38 Hz) — adaptar à tônica do projeto. Plugins dele (Fruity Balance,
Hyperdimension) têm equivalentes em Utility/width no Live. Áudio não escutado; CPU crackles no vídeo são do
ambiente dele, não da técnica.
