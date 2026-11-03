# Ableton Live Beginners Course: Lesson 5 - FM Synthesis

**Canal:** Scionaugh · **Vídeo:** `tfncDL3iIeI` · **Duração:** ~2:11:00
**Fonte:** transcrição completa normalizada do curso via legenda. **O áudio não foi escutado.**
**Contexto:** aula do Sektion Sound Course — additive + FM no Operator, sub FM, percussão FM sintonizável, Corpus e a fórmula completa do neuro rack. É o complemento direto dos vídeos `LVv74akK58c` (FM lead) e `2YgKSex63Wg` (bass rip) do mesmo canal.

## Técnica ensinada

**Sub FM (o coração da aula):**
- Sub = sine pura não se ouve em sistema pequeno → precisa de harmônicos com a **ilusão** de sine. NÃO usar
  saw + filtro fechado: *"if the filter's super close to the fundamental, then you'll get a bit of pitch
  shift… having the whole sub that's changing pitch, everything else we're putting on top is going to sound
  out of key"*. Acima do 2º harmônico o desvio diminui; *"our bass rips… we actually cut out the first two
  harmonics anyway"* (por isso o problema é só no sub).
- **Additive:** desenhar harmônicos no display do Operator (modo 16 para focar os baixos) — esculpe o tom
  sem filtro.
- **FM no Operator** (configuração default: cada osc modula o anterior): a taxa do modulador = a própria
  nota (D ≈ 38 Hz modulando a 38 Hz) gera harmônicos harmoniosos. **Cuidado nº 1: o sub some** —
  *"as we increase this frequency modulation, there's a point here where the sub starts to drop away… if
  we're designing this as a sub, we don't want to lose too much of that sub energy… choose somewhere around
  here where the sub's still nice and strong, but we've got these higher frequencies"*. EQ aberto o tempo
  todo como analyzer. Método: primeiro osc até aparecer "a couple of these", depois engatar o segundo
  (*"add some more frequencies without the sub dropping away"*).
- **Wobble com pitch estável:** envelope POR OSCILADOR do Operator (no lugar do filtro) — *"deep wobbing
  sound, but our pitch is pretty much completely steady"*. Notas 16avo + release para não sobrepor.
- **Macro de faixa estreita:** knobs de FM são supersensíveis → macro com range mínimo (ex.: −18 a −22) e
  a lane inteira de automação para micro-variação.
- **Sidechain split 3-bandas (Multiband Dynamics):** lows duckam fundo com release longo (sub sai da frente
  do kick); mids com menos compressão; highs com release curtíssimo (crossover 2,5 k→800). Resultado:
  *"your brain just thinks the bass is playing over the kick"* — ilusão de bass-over-kick com sub limpo.
  **Segundo ganho: saturar os MIDS pesado** (*"the subs aren't being distorted at all but we can distort a
  lot of the mids"*). Rack salvável uma vez.
- **Sidechain por Utility, não compressor:** *"I don't even use a compressor. I literally use a utility —
  just draw in the shape of my side chain"* (volume automation preservando o fader do mixer livre).

**FM orgânico × metálico (o mapa de timbres):**
- Coarse em **oitavas inteiras** mantém in-tune (múltiplo perfeito); fine detune = wobble instável
  ("unsettled").
- Osciladores perto (0–2 oitavas) = tonal; **6–9 oitavas de distância = "really bubbly sounds… you start to
  hear it more in forest"**; carrier AGUDO modulado por frequência muitas oitavas abaixo = "ripples" (a
  regra do modulador 5 oitavas abaixo do vídeo `LVv74akK58c` estendida).
- Sine×sine = orgânico; *"if you're FMing complex waveforms together… they start to sound very metallic quite
  quickly"* (saw×saw = metálico de propósito). *"A sawtooth… doesn't really exist in nature"* — por que FM
  sine soa instrumental.

**Percussão FM sintonizável:** FM só no ataque (envelope do modulador pluck) → bell/mallet/xylophone:
*"when you hit a xylophone… it vibrates in a chaotic way where there's lots of higher harmonics, but very
quickly it ends up resonating at the frequency that it wants"*. Como é sintetizado, **a percussão pode ter
melodia** (controle total de pitch). **Corpus** (instrumento do Live "overlooked"): MIDI from same channel,
`Frequency last` → a membrana ressoa NA MESMA frequência; 7 modos (beam, marimba, string, membrane, plate,
pipe, tube); radius/decay automatizáveis; Auto Pan 5/16 com amount subindo = *"swapping ears and getting
wider as it gets louder"*.

**Neuro sound design (a fórmula completa):**
1. Sine limpa baixa → **clipar pesado com Glue Compressor (Clipping ON)** — *"nothing does it better than
   Ableton's Glue Compressor"*; duplicar/empilhar até o sine virar quase quadrada (limiter = digital demais).
2. Ciclo repetido: **notch → distortion → OTT** (Multiband Dynamics preset "Over The Top"; os 3 knobs
   hi/mid/low funcionam como equalizador de volta do tom) — *"notch and then distort, notch and then
   distort"*. Distortion livre: Overdrive, Saturator (−10 de partida), Raw, ou clip Glue. Overdrive tem
   faixa de frequência igual à do filtro → copiar/colar a automação do notch na distorção **preenche o
   buraco que o notch abriu**.
3. **Erosion** (noise) = a faixa de white noise no topo dos rips de D&B — *"it sounds kind of like the
   speaker is ripping… but somehow it's clean"*.
4. **Auto Filter no FIM da cadeia** = movimento principal; dentro da cadeia já há automações caóticas, então
   cada snippet tem movimento próprio.
5. **Gravar LFO mapeado (MIDI controller) por minutos** em take lanes, depois escolher pedaços
   (Ctrl+Alt+Shift navega takes; Ctrl+L pula) — *"you're focusing on the groove you want to make rather than
   tediously doing the automation for each hit"*. Rips "fora do tempo" vêm daí de propósito.
6. **Spread (width) do Operator** no processo neuro: *"really going to make these sound absolutely huge"*
   (conferir em M/S).
7. Reverb tail em notas pontuais via **send** (não no canal), com lows fora.
8. Contrast final: *"we have really nice smooth organic sounds which are sine waves and then heavily
   distorted sine wave sounds — that's going to add really nice contrast"*. Track pode começar só kick+bass.

## Ferramentas usadas no vídeo

Ableton nativo: Operator, Corpus, Glue Compressor (Clipping), Multiband Dynamics/OTT, Erosion, Overdrive,
Saturator, Auto Filter, Utility, EQ Eight (analyzer), Oculus Scope (grátis). Nada pago além do Live.

## Notas de tradução (o que cada técnica vira num projeto)

- **Sub FM com guarda de sub** = rota nova para baixo sintetizado (FM amount moderado conferido no EQ/spectrum — mesma regra: *"the sub's still nice and strong"*). Corolário de segurança: nunca filtrar perto da fundamental do sub.
- **Sidechain split 3-bandas** = o molde para quando o sidechain simples não bastar: duck por banda com sub limpo e mids saturados; também valida saturação só no meio com sub intacto.
- **Wobble por envelope de oscilador (pitch estável)** = movimento de tom grave sem desafinar (o desvio de pitch por filtro fechado perto da fundamental é a causa típica de afinação instável).
- **Corpus Frequency-last** = instrumento orgânico nativo (membrana/madeira afinada na tônica) — ressonador, não reverb: mantém o sinal seco.
- **Fórmula neuro (clip Glue → notch→distort→OTT → Auto Filter → take lanes)** = receita para stabs/rips; traduz direto para Serum 2 (Distortion + EQ notch + multiband + LFO gravado).
- **Macro de range estreito** = padrão para qualquer knob sensível de FM (percentuais curtos evitam a lane inútil).
- **Percussão FM melódica** = oneshots sintonizados na tônica — percussão com melodia dentro.

## Notas de aplicação (experimentos sugeridos)

1. **Baixo:** A/B em pista muda — sine+FM amount baixo com conferência de sub no EQ/spectrum vs. o patch atual. Critério: sub não pode cair (regra do próprio vídeo).
2. **Tom grave/timbre de golpe:** testar envelope-de-oscilador no lugar de movimento por filtro (pitch estável).
3. **Corpus** em pista nova muda: membrana marimba/beam afinada (Frequency last) para madeiras orgânicas — A/B antes de adotar.
4. **Stab/resposta:** neuro rack em versão Live (clip→notch→distort→OTT→Auto Filter) como alternativa ao patch atual — nunca por cima do aprovado.
5. **Oneshots percussivos FM** (cruza com o vídeo `Q9WCC0Ylxic` do canal MERAKKI) sintonizados na tônica do projeto (ex.: C# frígio).

## Cuidados (conflitos possíveis)

- Clipar com Glue: funciona em canal/rack de **instrumento**; aplicar clipping pesado no master é outra decisão, de mix final — não usar esta receita como justificativa.
- Saturar mids pesado no bass: conferir o grave (55–75 Hz) com medidor antes de somar energia no médio-grave. Experimento em pista muda, não no baixo vivo.
- Spread/stereo no bass: **só acima do low-end mono** (prática comum: mono até ~120 Hz) — o "huge" do neuro vale para camadas de médio/agudo.

## Trechos de prova (transcrição)

1. "there's a point here where the sub starts to drop away. And then it comes back, and then it pretty much
   disappears completely. So, if we're designing this as a sub, we probably want to think about that, cuz we
   don't want to lose too much of that sub energy."
2. "if the filter's super close to the fundamental, then you'll get a bit of pitch shift… if we have a sub
   that's not consistent on the same note, then everything else we're putting on top of it's going to sound
   sort of out of key with the sub."
3. "I don't even use a compressor. I literally use a utility. I'll just draw in the shape of my side chain."
4. "the subs aren't being distorted at all but we can distort a lot of the mids."
5. "the kind of formula with creating neuro sounds is we start with something really simple. We add a lot of
   harmonics through clipping or distortion and then we want to start shaving some of those frequencies
   away… notch and then distort, notch and then distort."
6. "if we now take this one step further… they're nine octaves apart. And you start to get these like really
   bubbly sounds that you start to hear it like more, I guess, in forest."

## Limites

Sem timestamps por frase; valores citados só os do texto (38 Hz, −18/−22, 2,5 k→800, −10 Saturator, 9
oitavas). A demo do curso é em D (aula) — todos os alvos traduzem para a tônica do projeto próprio. Áudio não
escutado; a "sensibilidade" dos knobs FM varia por preset/versão do Live.
