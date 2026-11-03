# Minimal Psy-tech Elements Serum 2 Sound Design Breakdown

- **Canal:** MERAKKI
- **URL:** https://www.youtube.com/watch?v=jjnsu2lnf98
- **Duração:** ~22:00
- **Tema:** pressão de grave / bateria-percussão / sound design Serum 2 · gênero: psytech
- **Legenda:** transcrição completa normalizada (legenda automática), lida integralmente. Sem escuta do áudio (limites ao final).
- **Contexto:** dissecção de todos os elementos do loop do vídeo FM Donks (`Q9WCC0Ylxic`) — kick+bass, snare/knock, offbeat hat, 16th shakers, accents, rides, reverse, lead, FM layer, glitches, atmosferas. É o mapa completo do "kit psytech" em Serum 2.

## Técnica ensinada

**KICK:** sample de kick feito no Serum + **camada de mini-hat comprimida como GATE** — compressor com
threshold no chão e ratio altíssimo: o **attack time define quanto do hat passa** (*"just bringing that back
until it's literally just a tiny little tick"*). Tick de ataque/brilho sobre o kick.

**BASS (sliding, tudo DENTRO do Serum — "no processing outside of Serum"):**
- Quarter notes com **a última nota deslocada** ("slight change in groove"); automação de cutoff com ênfase no
  offbeat + swell no fim; 2ª frase = pitch bend por portamento + abertura de cutoff ("rich harmonics from the
  saw").
- **Variação por repetição:** 1ª passada tem double kick SEM nota de baixo; 2ª passada kick mais curto/quieto e
  a ÚLTIMA nota de baixo removida.
- **Phase-distorted saw** = "all the harmonics from a saw wave, but phases altered = rubbery quality"; como:
  frequency splitters (phase shift por banda) ou disperser/diffuser do Serum 2.
- Camada estéreo = cópia com **HP filter** (sem graves) + pan por oscilador em **audio rate** + FM de A "in
  very select moments" (efeito de quebra). O grave mais baixo foi REMOVIDO da onda principal para o sub ter
  controle independente.
- **Envelope 1 = o groove:** curva íngreme = pulse; suave = glued; *"I like to have a little bit of a pulse, so
  I'll have it somewhere in between"*. E o **ponto de pico**: *"just after the offbeat gets quite a nice groove
  going"*. Envelope 2 (sub) entra um pouco DEPOIS ("dispersed character"); envelope 3 abre o cutoff no offbeat.
- **EQ+LFO corta o mid-range da CAUDA** → *"it kind of becomes a bit deeper and also creates more space for
  other elements"*; a forma do LFO dita quando as frequências existem.
- **LFO final de volume corta ANTES do próximo kick** — *"a nice clean baseline that doesn't have any
  overlapping tails"*.

**PERC/KNOCK (snare):** 3 camadas de knocks feitos no Serum (principal + caráter + ruído de suporte "right
behind everything"); processamento: frequency shifter ("I love using frequency shifters for percussion"),
EQ, waveshaper ("thickness and glue"), reverb curto.

**HATS — a regra de hierarquia:** *"in your drums, especially with high hats, you want to make sure that one
of the sounds is the dominant sound and therefore has more harmonics and more volume. And then the other
sound has to be contrasting from that… Otherwise everything can sort of become just a harsh mess."*

**16TH SHAKERS:** mesma cadeia do hat mas **focada mais baixa no espectro** = *"a push-pull between the two
high-end elements"*; patch = ruído num filtro; LFO controla volume + abre o filtro no começo (mais low end no
ataque); **shapes morfados por note-on random** ("alive feeling… not static at all"); LFO2 controla o
SMOOTHING do LFO1 ("another level of dynamism").

**Detalhes do topo:** accent hats sutis; rides com sidechain leve (ênfase no offbeat); **mini-reverse antes de
cada segundo offbeat hat com reverb 100% wet** — *"you're not actually really hearing the reverse… just the
after effects"*; pre-delay/decay dão o groove: *"the amount of time that it takes for the reverb to kick in
dictates the groove"*. Crash a cada 8 compassos.

**LEAD:** saw com 16 unison + detune/shaper/cutoff→env; fora do Serum só **low-cut EQ** ("don't want any low
frequencies to clash with our bass") + reverb; cadeia: boost de mids, soft saturation, multiband, distorção
**atrelada ao envelope principal** (reforça o movimento), cleanup EQ no mesmo movimento ("not as bright
throughout the whole thing"), LFO2 abre cutoff+resonance no fim ("direction"). Roteado ao sidechain.

**FM LAYER (a assinatura):** saw + unison, phase-distorted por saw uma oitava acima, FM'd por sine uma oitava
e 7 semitons acima; LFO1→cutoff (menos plucky no fim), rate modulada; LFO3 abre cutoff + **detune spread
(mais dissonante no fim)** + remove phase distortion; comb filter com **mix caindo ao longo de 2 compassos
enquanto a ressonância sobe**; HP abre no fim; fade-in curtinho; **LFO de 8 compassos** = 2ª passada com
smoothing diferente (*"a smidge of variation"*); macro na forma do slowdown do rate.
- ⭐ Comb filter **afinado na tônica**: *"the frequency is set to 38 hertz, which is the frequency of the
  sharp, which is the key of this track"* — ressonância harmônica no C#.
- **Warp macro = caráter FM:** ramp up + sine = *"nice bubbles"*; curva menos logarítmica = *"gritty"* (mais
  harmônicos complexos); um dos sons começa gritty e desce ("just wanted it for the initial").

**GLITCHES/ATMOS:** arquivo longo de glitches generativos do Serum (*"set up a bunch of random modulations…
basically trying to break the synth"*), bounce, escolher pedaços como accents; tonal delay 0,1 s; swell de
reverb REVERSO; glassy atmosphere; riser final. **Reverb automatizado:** wet sobe no 1º ciclo e no 2º começa
alto→seca — *"gives the impression that the sound is coming closer towards you… alternation"*.

## Tradução para ambiente comum: Serum 2, Live 12 nativo

- **Gate de mini-hat no kick** (attack time = quanto passa) = rota para dar tick/brilho de ataque ao kick com
  controle fino de quanto entra.
- **Pico do envelope logo APÓS o offbeat** = afinação de groove do baixo com shape (curva intermediária =
  pulse com glue).
- **Corte de mids na cauda (EQ+LFO)** + **corte de volume antes do próximo kick** = as duas camadas que limpam
  a cauda do baixo e evitam sobreposição com o kick.
- **Hierarquia dos hats (um dominante, outro contrastante)** = a regra para topo percussivo denso: a saída é
  hierarquia, não corte cego.
- **Push-pull hat/shaker por banda** (um mais alto, outro mais baixo) = desenho para duas camadas de topo que
  não brigam.
- **Comb afinado na tônica (38 Hz = C#)** = assinatura harmônica para layers/leads — ressonância que acompanha
  a faixa em vez de zumbir fora do tom.
- **Mini-reverse com reverb 100% wet** + **pre-delay como groove** = variação do topo sem nova camada de
  evento.
- **Reverb que alterna wet alto/wet baixo** = proximidade/distância 3D com automação simples.
- **Glitch bank generativo** = biblioteca de accents sem importar sample novo (gerar, renderizar e curar
  pedaços).

## Aplicação sugerida (checklist de teste, **proposta**)

1. **KICK:** camada de tick via compressor-gate (A/B em camada de teste, nível baixo).
2. **BAIXO:** conferir pico de envelope (depois do offbeat?) e cauda cortada antes do kick.
3. **HATS/SHAKER:** definir dominante/contrastante e bandas separadas.
4. **CAMADA DE RESPOSTA:** comb afinado na tônica da faixa como teste de assinatura.

## Contrastes/cautelas

- Lead com 16 unison: se a house rule preferir uníssono menor (3/5/7), tratar a camada dele como lead pluck
  pontual e testar em camada separada. **Low-cut no lead** coincide com prática comum do estilo.
- Nenhum conflito com sub limpo: o sub fica fora do oscilador principal e sem saturação.

## Trechos de prova (transcrição)

1. "the amount of time that it takes for the reverb to kick in dictates the groove so much."
2. "one of the sounds is the dominant sound and therefore has more harmonics and more volume. And then the
   other sound has to be contrasting… Otherwise everything can sort of become just a harsh mess."
3. "the frequency is set to 38 hertz, which is the frequency of the sharp, which is the key of this track."
4. "this little final LFO controlling the volume at the very end… making sure that the volume is cutting
   right before the next kick."

## Limites do estudo

Sem timestamps por frase; valores citados: 38 Hz, 0,1 s de delay, 16 unison. Áudio não escutado. Plugins
pagos dele (Valhalla) são de mercado; disperser/diffuser = dispositivos equivalentes do Serum 2/Live.
