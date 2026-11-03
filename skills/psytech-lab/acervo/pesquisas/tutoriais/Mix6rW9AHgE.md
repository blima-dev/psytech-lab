# Psytrance Bassline for Techno (free project)

> id `Mix6rW9AHgE` · canal **Audioreakt** · ~18:27 · legenda automática EN obtida e lida
> (444 linhas úteis após remover cabeçalhos, tags e duplicatas consecutivas). **temLegenda=true**.
> Descrição oficial (lida): *"Today we are making Psytrance Bassline for techno. Taking that classic psytrance
> bassline sound and giving it a techno twist. This tutorial was influenced by the track "Enrico Sangiuliano -
> Future Dust"."* Ferramentas citadas na descrição: *"Solid Techno Kick Sample Pack"*, *"Wavetable Techno Bank"*
> (ambos do próprio canal), *"Kickverb Rack"*. Capítulos: 00:00 Intro · 00:42 Kick & Rumble · 03:47 Offbeat Bass · 05:15 Psytrance Bass ·
> 16:45 More techno bass · 17:55 Final Tips.
>
> **Escopo real do vídeo:** é uma aula de *sound design* de baixo — kick + rumble, baixo offbeat e baixo psytrance
> processado para techno. O vídeo **não** trata de hats/shaker, percussão de resposta audível (o clap 909 é só
> gatilho de sidechain), madeira, stab, subida, atmosfera ou arranjo; o "mix" aparece só como processamento do
> kick e do baixo. Tudo que não estiver ancorado em timestamp abaixo é tradução do estudo, marcada como
> `INFERÊNCIA` ou `HIPÓTESE`.
>
> **Ressalvas de legenda automática (não inventar a partir do erro):** "sidetrans"/"situation's" = *psytrance*;
> "everton"/"aberton" = *Ableton*; "river" = *reverb*; "fit"/"fitter" = *filter*; "truck" = *track*;
> "slow information" (00:05:25) = provavelmente *low information*; "the dkn" = *the decay*; "queue" = *Q*;
> "five liter saturn" = *FabFilter Saturn*; "crunch" (00:15:32) = o knob **Crunch** do Drum Bus do Live
> (`INFERÊNCIA` pelo contexto, não há nome de device na fala); "locket" (00:11:44) não é identificável com
> segurança — pelo contexto é uma banda de EQ com Q alto antes de um harmônico.

## Técnica ensinada (2-4 frases)

Resumo abaixo; as provas literais de cada device/valor estão na tabela da seção seguinte e nos `Trechos de prova`.

O vídeo monta o low end em três camadas: um **kick com rumble de reverb filtrado no grave** (00:00:52–00:01:54),
um **baixo offbeat de onda quadrada em G0** que "support the rumble" (00:03:47–00:05:15) e um **baixo psytrance
rolando em semicolcheias**, feito com sawtooth + low-pass com envelope rápido (00:05:15–00:08:29). O truque central
é **tirar o grave do baixo psy** — ele diz que, como já há "a lot of low information", o baixo psy não precisa
carregar a informação de grave (00:05:18–00:05:26) — e reconstruir o som como **articulação de médio**: saturação,
multibanda, EQ ressonante em 1 kHz/3 kHz, Redux e reverb curto (00:09:14–00:14:06). A articulação nasce do **Env 2
no filtro com sustain zero**, ataque zero e decay/release curtos, o que dá o transiente "clicky and mid"
(00:07:26–00:08:18). No fim ele acrescenta um **baixo estéreo detunado** com bandpass, reverb e Haas e confere
mono/fase (00:16:45–00:18:09).

## Ferramenta usada no vídeo (plugin/stock)

A rota é toda **Ableton Live**: devices stock (declarado em 00:00:27–00:00:30: "from scratch just using everton
stock plugin"), mais um rack gratuito do próprio canal (**Kickverb Rack**) e um preset privado do autor do vídeo. Nenhum
ANA 2, VELA, SideKick, Kick 3 ou Bitwig aparece.

| Device / ferramenta | Papel no vídeo | Prova literal (timestamp) |
|---|---|---|
| **909 clap** (sample) | Trigger de sidechain — não é percussão de resposta audível | "just a side chain truck it's just a 909 clap and that i'm going to use as a trigger for my sidechain compression" (00:00:36–00:00:42) |
| **Kick sample** (Solid Techno Kick Sample Pack) | Fonte do kick | "a kick from uh my three techno kick sample pack it sounds like this" (00:00:44–00:00:49); descrição: "Solid Techno Kick Sample Pack" |
| **Kickverb Rack** (rack free do Audioreakt; devices internos não detalhados no vídeo) | Rumble por reverb; macro = pre-delay | "i'm gonna use my kick verb to uh rack" (00:00:54–00:00:56); "it's just a rack ... easily rumble using reverb or delay today we're gonna use reverb only by default" (00:00:59–00:01:06); "the idea is to use this river rumble macro which is basically the pre-delay of your reverb" (00:01:18–00:01:21) |
| **EQ / "frequency"** (Live) | Filtra o rumble para sobrar só low end; reduz Q | "we're gonna filter that because there is too many information we just want the low end so we're gonna use our frequency and bring it down until we have something we like" (00:01:40–00:01:47); "maybe reduce the queue" (00:01:54) |
| **Sub** (device não nomeado) | Camada de sub no rumble | "now we're going to add a bit of sub" (00:02:02) |
| **Compressor / Sidechain** (Live) | Duck do rumble e do baixo | "and finally we're gonna use a bit of sidechain" (00:02:17); "i usually leave a ratio around four and bring down the attack because you want your compressor to react fast" (00:04:37–00:04:40) |
| **Reverb** (Live) + **Limiter** | Reverb curto no kick, só mid/top; limiter depois | "a bit of reverb a very gentle amount just to add a little extra mid top end to your kick drum" (00:02:30–00:02:36); "bring the pre-delay to zero" (00:03:05); "reduce the diffuse" (00:03:16); "add the limiters" (00:03:43) |
| **Operator** | Baixo offbeat em onda quadrada | "we're gonna use operator ... we just need a square waveform because they are usually the one richer and very nice for bass or sub bass" (00:04:08–00:04:16) |
| **Wavetable** | Baixo psy: sawtooth + LPF + Env 2 | "we're going to use a wavetable and we need a sawtooth" (00:05:28–00:05:33); "you take a sawtooth you put it through a low pass filter and modulate the fitter very fast" (00:06:56–00:07:04) |
| **Saturator** | Medium curve, dry/wet ~60; segundo estágio soft clip | "add a saturator and i'm just going to put a medium curve ... i'm gonna reduce the dry wet around 60" (00:09:14–00:09:22); "change the medium curve and we're going to put soft sign" (00:12:47–00:12:50) |
| **Multiband Dynamics / "multiband compression"** (Live) / **FabFilter Saturn** (recomendado, não usado) | Split de bandas; EQ por banda + output, sem compressão | "using multi-band compression or even multiband distortion i recommend to use multi-band distortion" (00:09:35–00:09:46) — Live não tem multiband distortion; com Saturn fica melhor; "i'm not gonna use the compression side of the tool i'm just gonna use the frequency cuts ... and the output" (00:10:04–00:10:12) |
| **EQ** (Live) | Boost ~1 kHz e ~3 kHz; banda ressonante antes de um harmônico | "the first one i will usually boost around one kilo ... maybe another band around three kilo just to boost the top end" (00:11:20–00:11:42); "use the locket ... cut right before one of the harmonics ... crank up the resonance" (00:11:44–00:12:01) |
| **Redux** (Live) | Downsampling, click/resonância de alta | "use down sampling so we're going to use redux from a button" (00:13:08–00:13:12) |
| **Reverb** (Live) | Espaço curto, sem diffuse, input filtrado | "not to have like a big room reverb it's just to have like something tight just to give a little bit of the base a space just don't be too dry" (00:13:51–00:13:57); "short decay ... no diffuse filter the input" (00:14:01–00:14:06) |
| **Drum Bus** (Live) | Crunch + caráter | "we're gonna use a drum bus ... even with the drawer there a person is going to add some character" (00:15:14–00:15:19); "we're gonna use crunch to really make things louder" (00:15:32–00:15:37) |
| **Compressor** (Live) | "put everything in your face" | "i'm gonna use compressor to put everything in your face" (00:15:28–00:15:29) |
| **Utility** (Live) | Checagem mono e troca de fase L/R | "if you bring everything in mono you still have something pretty decent" (00:17:44–00:17:50); "if you use utility and you swap the phase of left and right it's actually kind of changed a tone" (00:18:04–00:18:09) |
| **Preset de baixo estéreo do autor do vídeo** | 2º oscilador detunado, bandpass, reverb, Haas | "i had the kind of a stereo base so i used a preset of mine ... the second oscillator is detuned and then after about the filter i use the band pass ... some reverb and some hass effect" (00:16:45–00:17:25) |

## Tradução para ambiente comum: Live 12 nativo + Serum 2 / Diva / Vital / Massive X / Surge XT / Kontakt 8 — sem ANA 2, VELA, SideKick, Kick 3 nem Bitwig

### Live 12 nativo — rota 1:1 (principal)

O vídeo **não depende de nenhum plugin pago**: a rota principal é stock do Live, o Kickverb Rack é
um rack gratuito que se reconstrói e o FabFilter Saturn é opcional. A tradução é direta:

- **Wavetable** → Wavetable do Live 12 (fonte do baixo psy; sawtooth, filtro interno LP, Env 2 na matriz).
- **Operator** → Operator do Live 12 (baixo offbeat quadrado).
- **Saturator** → Saturator (medium curve, dry/wet ~60; segundo estágio soft clip).
- **Multiband compression** → no Live 12 o device equivalente é **Multiband Dynamics** (o vídeo chama de
  "multiband compression"); usar só os cortes de banda e os outputs, sem compressão, como ele faz
  (00:10:04–00:10:12).
- **EQ** → EQ Eight (boost ~1 kHz e ~3 kHz; banda com Q alto antes de um harmônico).
- **Redux** → Redux (downsampling).
- **Reverb** → Reverb (curto, diffuse baixo, input filtrado) ou **Hybrid Reverb** no modo Room, com as mesmas
  decisões: decay curto, pre-delay zero, diffusion baixa, wet baixo.
- **Drum Bus** → Drum Bus (knob Crunch).
- **Compressor** → Compressor (ratio ~4, attack rápido, release maior).
- **Utility** → Utility (mono e troca de fase L/R).
- **Limiter** → Limiter.

**Kickverb Rack:** não é plugin proprietário; é uma montagem reproduzível. O vídeo não detalha os devices
internos; o conceito é: **Reverb/Hybrid Reverb + EQ + Utility**, com um macro no **pre-delay** do
reverb para deslocar o rumble do kick e criar groove (00:01:18–00:01:23).

### Serum 2 — o baixo psy como patch + cadeia no Live

O Serum 2 cobre a parte de síntese e a maior parte da coloração; o que ele não substitui bem é a cirurgia de EQ
ressonante e o Drum Bus — isso fica no Live.

- **Osc A:** wavetable de sawtooth (no vídeo, a Sawtooth do Wavetable; candidatas de tabela/frame: `analog_basic`,
  `analog_warm`; `custom_harmonics` com série 1/n também resolve). O
  vídeo usa "sawtooth" e diz que, em G0, ela dá "this nice juicy fatty sound" (00:05:39–00:05:44).
- **Sub osc:** ligar só se o patch precisar do fundamental; se o motor já tem sub em outra camada,
  **não empilhar** (ver guardas).
- **Filter 1:** lowpass 24; cutoff baixo; **Env 2 → filter1.cutoff** com amount positivo. Env 2: attack 0,
  decay curto, **sustain 0**, release curto. É o sustain a zero que ele chama de trick (00:08:02–00:08:05).
- **Env 1 (amp):** attack 0; decay 335 e release 600 como ponto de partida (valores que ele cita para o Wavetable
  em 00:07:42–00:07:52; a legenda não diz a unidade — conferir na interface do Wavetable; são referência, não
  promessa de som idêntico no Serum 2); sustain em −10 (como ele diz em 00:07:48; no Wavetable isso é dB, ≈0,32
  no Serum 2).
- **Ressonância:** um pouco, "not too crazy" (00:07:30–00:07:38), para o caráter ácido sem virar hit.
- **Slope:** testar 12 vs 24 dB — ele diz que o slope muda entre "super tight" e "a bit more round"
  (00:08:31–00:08:46).
- **FX no Serum 2:** distorção (medium/soft) e EQ da cadeia de FX; o restante (Multiband Dynamics, Redux,
  Reverb, Drum Bus, Compressor) no Live, na ordem do vídeo.
- **Limite:** um gerador de presets cria o patch estático (oscilador/filtro/envelopes/roteamento).
  A parte "surgical" — varredura do EQ ressonante, automação do cutoff e A/B — é manual. Não prometer preset
  pronto que substitua a aula.

### Diva, Vital, Massive X, Surge XT — fontes alternativas

- **Diva:** saw + filtro ladder + Env 2 no cutoff; boa para a versão "more round" que o vídeo mostra no slope
  (00:08:43–00:08:46). O filtro analógico tende a arredondar o click; usar quando o objetivo for corpo, não
  mordida.
- **Vital:** saw + LPF + envelope; distorção embutida. Bom para a camada mid-forward; o timbre é mais limpo,
  então a saturação do vídeo (00:09:14) tende a ser mais necessária.
- **Massive X:** wavetable saw + insert FX; roteamento mais complexo, útil para um baixo mais duro/digital.
  O caminho é o mesmo: Env no cutoff, sustain 0, saturação, EQ no Live.
- **Surge XT:** saw + LPF + Env; tem distorção interna. Serve como fonte; a parte multibanda/ressonante continua
  melhor no Live.
- Em todos: o **caráter** vem da articulação (Env 2 com sustain 0) e do pós-processamento, não do synth escolhido.

### Kontakt 8 — sem papel nesta técnica

Bibliotecas orgânicas/acústicas não têm papel aqui; o vídeo faz um baixo **sintético** (sawtooth + LPF + saturação), sem nenhuma camada acústica. Não há tradução direta para Kontakt 8 — forçar uma corda ou órgão seria outro desenho, não esta técnica. Um dobramento orgânico do baixo é decisão de arranjo separada e não está no vídeo.

### O que não é necessário

- **ANA 2, VELA, SideKick, Kick 3, Bitwig:** não são usados no vídeo. Não há dependência; nada precisa de equivalente.
- **FabFilter Saturn:** é citado como opção de **multiband distortion** ("if you have the five liter saturn it's
  really nice", 00:09:41–00:09:44). O próprio autor dá o fallback: "you can do with the classic
  multiband compression" (00:09:44–00:09:46). No ambiente Live: **Multiband Dynamics + Saturator**, ou três cadeias
  de Saturator em paralelo separadas por EQ.
- **Kickverb Rack:** rack gratuito, não plugin; reconstruível com Hybrid Reverb + EQ + Utility.

## Aplicação por função (kick, sub, baixo/rolling, hats/shaker, percussão de resposta, madeira, stab, subida, atmosfera)

Tudo nesta seção que não estiver entre aspas é `INFERÊNCIA` do estudo; o vídeo não fala de arranjo específico, de groove deslocado nem de low-end mono.

**Contexto de contraste citado no levantamento original:** num set de referência medido, o meio (300–1.200 Hz) estava **−4,83 dB** e o agudo-médio (1.200–4.000 Hz) **−5,76 dB** contra a média de 6 referências externas; o low-end é **mono**; o groove usa subdivisões deslocadas do grid e deve ser preservado. O vídeo não fala desses números; a ponte abaixo é do estudo.

| Função | O que o vídeo oferece | Como aplicar | Guarda-corpo |
|---|---|---|---|
| **Kick** | Kick sample + reverb "very gentle" de sala pequena para ganhar mid/top e cortar no mix (00:02:27–00:02:38); pre-delay 0, decay curto, diffusion baixa, input filtrado, limiter depois (00:03:01–00:03:46) | Usar o reverb do kick como **envio paralelo high-passed** (~250–300 Hz) com Hybrid Reverb/Reverb em sala pequena: pre-delay 0, decay curto, diffusion baixa, wet baixo. Isso ataca o buraco de 300–4.000 Hz sem mexer no sub. | O reverb é "very gentle"; não usar como ambiência. O envio tem que ser high-passed para o sub do kick continuar seco e mono. Não copiar o rumble + sub do vídeo por cima de um sub existente. |
| **Sub** | "Add a bit of sub" no rumble (00:02:02); onda quadrada "nice for bass or sub bass" (00:04:12–00:04:16) | **Não adicionar outra camada de sub.** Se o motor já tem sub, a técnica do vídeo entra como *substituição* (se o rumble for refeito), nunca como soma. O baixo psy fica **sem a função de grave**: high-pass/band-limit acima da faixa do sub. | Se o patch psy tocar a oitava fundamental, o high-pass come o fundamental; tocar a articulação uma oitava acima e deixar o fundamental para o sub. Medir em mono. |
| **Baixo / rolling** | Duas camadas: offbeat quadrado em G0 que "support the rumble" (00:03:47–00:04:16) + psy rolling em semicolcheias com saw/LPF/Env 2 (00:05:15–00:08:29) | Montar **uma** camada de articulação psy (Serum 2 ou Wavetable) na região de médio, com o Env 2 no filtro. O offbeat quadrado do vídeo é opcional: só entra se o groove precisar de apoio entre kicks, e sem duplicar o sub. Sidechain **leve** (ratio ~4, attack rápido, release maior) se o baixo brigar com o kick — o vídeo diz que, tocando offbeat, o sidechain "is not going to work a lot but it's just going to add a little bit of movement" (00:04:24–00:04:31). | **Preservar o groove deslocado.** O roll do vídeo é 1/16 reto; se copiado reto, ele mascara o deslocamento. Usar a articulação psy **nas subdivisões deslocadas** (ou como ghost layer com furos), e aplicar o recurso dele de "remove this knot in the center" (legenda: *knot* = nota) + nota de velocity mais baixa (00:06:07–00:06:14) para o roll não ficar mecânico. |
| **Hats / shaker** | **O vídeo não trata de hats nem shaker.** A única menção a agudo é sobre o reverb do kick: "we don't really want have too much high frequency because that created the mess" (00:03:01–00:03:05) | Não há técnica para aplicar. Não clarear hats para compensar o buraco de 1,2–4 kHz. | Sem base no vídeo. Qualquer mudança em hats por esta fonte seria invenção. |
| **Percussão de resposta** | O 909 clap existe **só como trigger de sidechain** (00:00:36–00:00:42); não é uma resposta audível | Conceito aproveitável: usar um **trigger mudo** (clap/click) como chave do sidechain, sem som audível, quando precisar de ducking sem adicionar elemento. Para a percussão de resposta em si, o vídeo não dá receita. | Não transformar o clap em percussão de resposta: no vídeo ele é gatilho, não camada. |
| **Madeira** | **O vídeo não trata de madeira.** | Nenhuma aplicação direta. `INFERÊNCIA` do estudo: a madeira é um lugar mais seguro para preencher 300–1.200 Hz do que empurrar 3 kHz no baixo; mas isso é decisão de arranjo, não do vídeo. | Não citar o vídeo como fonte de EQ de madeira. |
| **Stab** | **O vídeo não trata de stab.** | Nenhuma aplicação. | Sem base. |
| **Subida** | **O vídeo não trata de subida/riser.** O reverb é sala curta de baixo, não riser. | Nenhuma aplicação. | Sem base. |
| **Atmosfera** | **O vídeo não trata de atmosfera/pad.** O reverb é "tight" e "just to give a little bit of the base a space" (00:13:51–00:13:57). | Nenhuma aplicação como pad/atmosfera. Se muito, o conceito de sala curta, diffusion baixa e input filtrado pode informar um reverb de percussão — mas é extrapolação. | Sem base direta. |
| **Articulação** | O núcleo: saw → LPF → Env 2 com **sustain 0**, attack 0, decay/release curtos; ressonância opcional; slope "tight" ou "round"; o transiente "clicky and mid" (00:07:26–00:08:18) | É a parte que se copia quase 1:1 no patch psy. Env 1 amp: attack 0, decay 335, release 600, sustain −10 (valores do vídeo; unidade não dita na legenda — ver a interface do Wavetable; ponto de partida). Env 2: sustain 0, attack 0, decay/release curtos. | O filtro não pode ficar tão fechado que o baixo vire só click; A/B com a nota real do material. |

### Guardas específicas: não engordar o sub, não criar brilho metálico

1. **O baixo psy não carrega o grave.** É a tese do vídeo (00:05:18–00:05:26) e a maior proteção contra
   engordar o sub: high-pass/band-limit a camada psy acima da faixa do sub; deixar o fundamental para o sub/rumble.
2. **Não somar o "add a bit of sub" (00:02:02) ao sub que já existe.** Se o rumble for adotado, ele **substitui**
   a camada de sub existente; nunca empilha.
3. **Multibanda só nos médios.** No Multiband Dynamics, deixar a banda de grave em unity/bypass e usar os cortes/
   outputs das bandas de 300–4.000 Hz para gerar harmônicos. É o que preenche o buraco medido sem mexer no low-end.
4. **Brilho metálico é o risco real da cadeia.** O vídeo empilha high shelf em 3 kHz + Redux + soft clip + Drum Bus
   Crunch (00:11:37–00:13:17, 00:15:32). Escolher **no máximo dois** desses estágios: preferir o EQ
   ressonante em 1 kHz e a saturação com limite de banda; se usar Redux, em paralelo e em nível baixo; não somar
   high shelf amplo em 3 kHz com Redux no mesmo caminho.
5. **A checagem de mono é gate, não sugestão.** O vídeo confere mono e fase (00:17:44–00:18:09); o gênero pede low-end
   mono. Se a camada estéreo detunada (00:16:45–00:17:25) colapsar ou mudar de timbre ao somar em mono,
   ela sai ou é high-passed acima de ~300 Hz.
6. **O groove deslocado manda.** A articulação psy entra nas subdivisões deslocadas; o roll 1/16 do vídeo, se usado,
   é ghost layer com furos e acentos de velocity — não substitui o groove existente.

### Ordem de cadeia sugerida (adaptada do vídeo)

`Saw (Serum 2/Wavetable) → LPF com Env 2 (sustain 0) → Saturator medium ~60% → Multiband Dynamics (só bandas
médias, sem compressão) → EQ Eight (1 kHz + banda ressonante no harmônico) → Saturator soft clip → [Redux em
paralelo, opcional] → Reverb curto (diffusion baixa, input filtrado) → Drum Bus (Crunch) → Compressor → Utility
(mono/fase) → Limiter se necessário`.

O vídeo não usa sidechain no baixo psy no exemplo original: "you don't really need side chain compression you can
add if you want but in the original example there was no" (00:16:16–00:16:24). Se a camada psy ficar só no médio,
pode-se seguir sem sidechain; o ducking pesado fica no sub/kick.

## Prioridade e esforço

**Prioridade: alta.** É o cruzamento exato da frente de pressão-grave — baixo psytrance em contexto
techno — e a técnica ataca diretamente o buraco medido de 300–4.000 Hz com uma camada que, por construção, **não
carrega o sub**. É uma receita diretamente alinhada ao problema de médio do estilo.

**Esforço: médio.** Todos os devices são stock (Live 12) ou existem no Serum 2; não há plugin faltante. O custo
está na cirurgia: são ~6 estágios de cadeia, valores de envelope e EQ que o próprio autor chama de "very surgical"
(00:06:37–00:06:53), e o A/B contra o groove deslocado e contra o brilho metálico. Estimativa: uma sessão de sound
design + uma de A/B; não é um preset de 10 minutos.

## Trechos de prova

1. **[00:00:36–00:00:42]** "just a side chain truck it's just a 909 clap and that i'm going to use as a trigger for
   my sidechain compression" — o clap não é percussão de resposta; é gatilho de ducking.
2. **[00:05:20–00:05:26]** "because we have a lot of low information we're not going to especially need for the
   situation's baseline to have the slow information that's going to be the first twist to the classic situation
   baseline" — a tese central: o baixo psy perde a função de grave para caber no techno (legenda diz "slow", o
   contexto é *low*).
3. **[00:08:02–00:08:05]** "bring down the sustain to zero because we want something very sharp and pluckier" —
   a articulação que dá o caráter do baixo.
