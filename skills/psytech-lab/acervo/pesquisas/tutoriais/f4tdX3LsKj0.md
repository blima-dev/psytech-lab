# Granulator 3: The Game-Changer for Hypnotic Groove

> id `f4tdX3LsKj0` · canal **Hypnotic Techno Production** · ~10:25 · legenda automática EN obtida e lida via
> yt-dlp (cue final 00:10:24.720). **temLegenda=true**. A descrição do vídeo não foi consultada — não foi
> necessária, porque a legenda existiu. **Áudio não escutado.**
>
> **Escopo real do vídeo:** é uma aula de *sound design de percussão*. Ele parte de um groove que já funciona
> e diz que "for me the groove is just high heads" (00:00:43.840), quer acrescentar "some short percussion hits"
> que não sejam "not so obvious" (00:01:08.080 / 00:01:13.520) e usa o Granulator 3 para isso. O vídeo **não**
> trata de kick, sub, baixo, hats (ele não processa os hats: eles são o groove de base), madeira, stab, subida,
> atmosfera, mix (ele só ajusta o nível de uma camada) ou arranjo macro. Tudo que não estiver ancorado em timestamp
> é tradução, marcada `INFERÊNCIA`.
>
> **Ressalvas de legenda automática (não inventar a partir do erro):** "high heads" = *hi-hats*; "hypnotic techno
> rocks pack" (00:00:57.199) é a grafia da legenda para o nome do pack — não sei o nome correto, não corrijo;
> "Byron Matkov" (00:02:31.920) é a grafia da legenda (provável *Byron Metcalf* — `INFERÊNCIA`, o vídeo não
> confirma); "16 stacato" (00:06:33.680) = 16 avos *staccato*.

## Técnica ensinada (2-4 frases)

O vídeo reforça um groove hipnótico que já existe usando **granular como percussão de resposta**: carrega um
sample percussivo longo/meditativo (ou um synth printado, ou gravação própria de voz/foley) no **Granulator 3**,
que é "a granular synth that needs an audio file to work" (00:01:21.759), e põe o device em **modo loop** para
obter "percussive loopy textures" (00:03:21.680) — segundo ele, ao clicar, o granulator vai
"automatically find those loops" (00:03:31.680). O ajuste fino é
**grain size + scan** ("So, grain size is is good to tweak scan, which will be like adding a bit of uh movement
throughout the sample", 00:04:00.480) e um **LFO no grain size** para o tamanho variar ("So every time like it's
going to change the grain size a bit", 00:04:16.959); a performance é uma linha MIDI de **16 avos staccato**
(00:06:33.680) para "enhance the timing a bit" (00:06:37.120). Os hits são gravados em áudio e colocados **nos
buracos** do groove, com um som "asking another one answering" (00:10:04.240), um pouco de echo e o evento a cada
dois compassos (00:08:13.599) — e o próprio autor avisa "Try to not overdo it, not to have so too many samples"
(00:09:57.839).

## Ferramenta usada no vídeo (plugin/stock)

A rota é **Ableton Live 12 + Granulator 3** (device de Max for Live que, segundo o vídeo, "comes with uh live 12",
00:00:14.960). Nenhum ANA 2, VELA, SideKick, Kick 3 ou Bitwig aparece. O "echo" é citado de ouvido, sem nome de
device (00:08:18.150) — não vou afirmar que é o Echo do Live.

| Ferramenta | Papel no vídeo | Prova literal (timestamp) |
|---|---|---|
| **Granulator 3** (Max for Live) | Sintetizador granular que gera as texturas | "We will be using the granulator 3 which comes with uh live 12" (00:00:14.960); "granulator is a granular synth that needs an audio file to work" (00:01:21.759) |
| **Rack MIDI vazio** | Contêiner do instrumento | "you need a empty MIDI rack and you can find it in the in the instruments here" (00:01:27.920) |
| **Track de áudio + roteamento** | Gravar os hits que saem do granulator | "I will create another uh audio track" (00:05:25.199); "the granulator output comes into this input" (00:05:34.070) |
| **MIDI 16 avos staccato** | Articulação/performance dos hits | "from complex pro I went to beats and added a bit of like a 16 stacato and kind of like um enhance the timing a bit" (00:06:26.240–00:06:40.319) |
| **Echo** (device não nomeado) | Cauda curta no evento de 2 compassos | "every two bars I added yeah some some moment and a bit of echo" (00:08:13.599 / 00:08:18.150) |
| **Samples** | Fonte do granulador | pack do canal: "those sounds were created with the hypnotic techno rocks pack" (00:00:57.199); faixa longa de percussão: "It's basically 25 minutes drumming uh with some different percussion instruments and creating this kind of like a meditative atmosphere" (00:02:55.190); synth printado: "I just bounced one of the uh synths" (00:04:34.479); voz/foley próprio: "me doing some random um sounds to the microphone" (00:05:00.560) |

## Tradução para ferramentas Live 12 / Serum 2

### O vídeo usa o que o Live 12 Suite já dá (rota 1:1)

- **Granulator 3** é device de Max for Live e o vídeo diz que ele vem com o Live 12 (00:00:14.960); o Granulator
  III vem incluído no Live 12 Suite. Antes de prometer a rota, conferir no browser do Live que o device está na
  biblioteca da instalação (`NÃO VERIFICADO` nesta sessão).
- **Nada no vídeo depende de plugin pago.** A única ferramenta além de sample/MIDI é o próprio Granulator 3,
  que é stock de Max for Live; o resto é sample, MIDI e echo.

### Serum 2 — o substituto 1:1 do Granulator (GranularOsc)

O **GranularOsc** do Serum 2 cobre o núcleo do vídeo com controles equivalentes: source (o arquivo),
grain length (ms — "grain size"), density, loop (o modo loop do vídeo), random offset, random pitch, random pan
e max grains. O **scan** do Granulator ("adding a bit of uh movement throughout the sample", 00:04:03.920)
equivale à posição/scan do GranularOsc modulada por LFO; o **LFO no grain size** (00:04:14.319) equivale a
`LFO → grain length`.

- Faixa útil de textura típica de grão: **20–120 ms**, com random offset 30–80% para stutter sustentável
  (recomendação geral de uso granular em psytech).
- Para tonalidade estrita (uma tônica fixa no projeto): granular com `random_pitch` **no máximo ±2 st** — acima
  disso a afinação flutua e quebra a tonalidade — e granular **nunca como fonte melódica principal**, só
  textura/atmos.
- Nota de ferramenta: algum gerador automático de presets pode não expor o scan/posição do GranularOsc — o
  movimento por scan/LFO é ajuste manual na UI do Serum.

### Diva, Vital, Massive X, Surge XT — fonte, não motor granular

Nenhum deles é o caminho principal: são **geradores da matéria-prima** que o vídeo também usa quando printa um
synth ("I just bounced one of the uh synths", 00:04:34.479). O fluxo é: tocar uma nota curta com textura →
**printar em áudio** → jogar no GranularOsc/Granulator 3.

- **Diva:** corpo analógico, bom para a nota que vira grão de madeira/metal amadeirado.
- **Vital / Massive X:** wavetable, mais brilho e movimento — cuidado redobrado com o "brilho metálico" depois.
- **Surge XT:** híbrido; serve como fonte, mas o caráter final vem do sample e dos ajustes de grão, não do synth
  ("choosing the right sample is really a key", 00:04:26.800).

### Kontakt 8 — fonte de material orgânico para printar

As bibliotecas citadas (Rubber Bridge Guitar, LOOP GARDEN, Ethereal Earth, Vintage Organs) são **sample
playback**, não motores granulares: entram como matéria-prima, nunca como o granulador.

- **Rubber Bridge Guitar:** nota dedilhada/muted com ruído de corda — bom para grão curto de "madeira".
- **LOOP GARDEN:** loops prontos — o candidato mais direto para recortar e granular, já que o vídeo trabalha com
  loops percussivos.
- **Ethereal Earth:** atmosferas — melhor para a camada de fundo (grão longo), não para a resposta rítmica.
- **Vintage Organs:** tom sustentado — bom para o "splash" granulado, não para o pulso.

### Live 12 nativo

- **Simpler / Sampler:** **não têm síntese granular.** Cobrem só a metade "loop curto + disparo" (One-Shot com
  loop, ou Slice para isolar hits) — úteis para *printar* e para percussão de resposta em sample, não para a
  nuvem de grãos. O granular real vem do Granulator 3 ou do GranularOsc.
- **Grain Delay:** é efeito de delay granular sobre o sinal ao vivo, não resíntese de um arquivo com grain
  size/scan. Serve como *smear* de envio depois do hit, não como o instrumento do vídeo.
- **Operator:** pode gerar o click/madeira que será printado.
- **Echo / Delay:** é a tradução literal do "a bit of echo" (00:08:18.150) — curto, filtrado, feedback baixo.
- **AutoPan:** o vídeo observa que a versão em loop ficou "more stereo" (00:03:47.280); AutoPan dá esse movimento
  sem alargar o grave.
- **Hybrid Reverb:** cauda/espaço da camada granular (o vídeo **não** usa reverb; isto é `INFERÊNCIA`).
- **Shifter:** deslocamento de pitch do grão para deixar o hit menos óbvio (também `INFERÊNCIA`).

### O que não existe no vídeo

**ANA 2, VELA, SideKick, Kick 3 e Bitwig não são usados no vídeo.** Não há dependência e nada precisa de
equivalente. **traduzivel = true.**

## Aplicação por função (kick, sub, baixo/rolling, hats/shaker, percussão de resposta, madeira, stab, subida, atmosfera)

**Contexto de auditoria (set de referência contra a média de 6 referências do estilo):** 300–1.200 Hz estava
**−4,83 dB** e 1.200–4.000 Hz **−5,76 dB**; o low-end é **mono**; o groove usa subdivisões deslocadas fora do
grid e deve ser preservado. Num set minimalista típico os canais de percussão de resposta/madeira/stab já
existem em forma de sample ou synth — o granular entra como **nova camada de resposta** sobre esse material.

| Função | O que o vídeo oferece | Onde/como aplicar | Guarda-corpo |
|---|---|---|---|
| **Kick** | **Nada.** O vídeo não toca no kick; o groove é só de hats (00:00:43.840) | Não aplicar. Manter a cadeia do kick como está | Não rotear kick para granular: grão randomiza fase/pitch e destrói o transiente e o mono |
| **Sub** | **Nada** | Não aplicar. Sub intacto | Granular nunca no sub; a camada granular entra high-passed (ver guardas) |
| **Baixo / rolling** | **Nada** | Não aplicar. O desenho deslocado do rolling fica intocado | Grão randomiza pitch/fase e borra a definição do rolling; se um dia houver camada média, ela é separada, HP ≥300 Hz e com ducking — nunca o baixo em si |
| **Hats / shaker** | Os hats **são** o groove de base; ele não os processa (00:00:43.840) | Não granular os hats. Eles seguem como grade | Fonte metálica + grão curto = brilho metálico, exatamente o que o estilo pede para evitar |
| **Percussão de resposta** | **Núcleo do vídeo**: hits curtos, "not so obvious" (00:01:13.520), granulados, gravados em áudio e postos nos buracos com Q&A (00:10:04.240) a cada 2 compassos (00:08:13.599) | Printar 1–2 compassos da percussão de resposta existente (ou de fonte orgânica), granular, e colocar **uma pergunta e uma resposta por ciclo de 2 compassos**, alternando dois samples. Entrar **no buraco** entre as posições deslocadas do groove, nunca em cima delas | Um hit por buraco; não deixar as duas camadas se sobreporem ("Maybe they overlap [music] a bit too much", 00:07:43.280) |
| **Madeira** | Não é o foco, mas a fonte "percussive" e orgânica é o que ele escolhe ("percussive loopy textures", 00:03:21.680) | Printar uma nota curta de madeira (synth ou sample) e granular com grão **longo (100–160 ms)**, densidade baixa, 1 hit por compasso ou a cada 2. É a camada que pode devolver corpo em **700–1.200 Hz** | `random_pitch` ≤ ±2 st (tonalidade estrita); não deixar a madeira granular ocupar 300–700 Hz junto com o baixo |
| **Stab** | O "splash": ele adiciona a segunda textura ("Let's add the second one", 00:07:16.560) e a chama de "more like a splash or effect" (00:07:33.199) | Granular o stab printado com grão médio e envelope curto; entra **a cada 4–8 compassos**, como acento | Não virar camada contínua; é evento, não pad |
| **Subida** | **O vídeo não trata de subida** | `INFERÊNCIA`: automatizar o **scan** para cima + densidade + wet de Hybrid Reverb nos últimos 4–8 compassos do bloco, ou granular o print da subida | Não usar o granular como riser tonal: random pitch ≤ ±2 st e filtro de topo para não assobiar |
| **Atmosfera** | **O vídeo não trata de atmosfera/pad**; o máximo é a qualidade "meditative" do sample (00:03:01.520) | `INFERÊNCIA`: grão longo (300–800 ms), densidade muito baixa, fonte atmosférica printada, HP ~300 Hz, estéreo largo e nível baixo — cama do bloco, não evento | Sem transiente e sem brilho; não é o que o vídeo ensina |

### Articulação (o que copiar quase 1:1)

O hit granular precisa de **envelope curto** por fora: o vídeo dispara "16 stacato" (00:06:33.680) para "enhance
the timing a bit" (00:06:37.120). Sem isso, a cauda do grão apaga o desenho rítmico. `INFERÊNCIA`: gate de
20–40 ms no MIDI e envelope de amp curto no patch.

### Receita em números (`INFERÊNCIA` a partir dos parâmetros do vídeo)

- **Fonte:** 1–2 compassos printados da percussão de resposta (ou da madeira) na taxa do projeto. O vídeo
  insiste que a escolha do sample é o ponto ("choosing the right sample is really a key", 00:04:26.800) e que o
  loop mode é o que gera a textura percussiva (00:03:21.680).
- **Grão:** 60–120 ms; densidade baixa-média; loop **on**; random offset 20–40%; random pitch ±1–2 st; random pan
  ±20%; max grains ~8–16.
- **Movimento:** LFO 1 a cada 1/2 ou 1 compasso → **grain length** (±20–30%), como no vídeo (00:04:14.319); LFO 2
  lento → posição/scan (00:04:00.480).
- **MIDI:** 16 avos, gate curto, notas **só nos buracos**; padrão A/B alternando a cada 2 compassos
  (00:08:13.599). O evento de voz/echo a cada 2 compassos do vídeo é o molde do ciclo (00:08:20.080).
- **Cadeia:** Granulator 3 / GranularOsc → **HP 24 dB em ~250–300 Hz** → EQ (sem boost acima de 8 kHz; corte de
  300–500 Hz só se empaçar) → **echo curto** (1/8 ou 3/16, feedback 15–25%, HP 400 Hz, LP 5 kHz) → **AutoPan**
  sutil → **Utility** para conferir mono → send baixo para um reverb curto.
- **Nível:** 3–6 dB abaixo dos hats. O próprio autor abaixa uma camada ("maybe that's one a bit too loud",
  00:08:32.959).

### Guardas específicas: não engordar o sub, não criar brilho metálico, preservar o groove

1. **Nada de granular no kick/sub/baixo.** O low-end é mono e o grão randomiza fase e pitch. A camada granular
   começa acima de ~250–300 Hz.
2. **O HP de ~250–300 Hz é ponto de partida típico** para camada granular de resposta (precedente de uso no
   estilo: high-pass 24 dB/oct em ~276 Hz).
3. **Brilho metálico** nasce de grão muito curto, densidade alta e fonte metálica. Evitar grão <20–30 ms, não
   granular hats/pratos, não usar AutoFilter ressonante com Q alto depois do grão, e manter um low-pass/High
   Shelf suave (corte em 8–10 kHz ou −2 dB) no topo da camada. Random pitch/pan transforma o ringing tonal em
   textura — é o que permite preencher 1,2–4 kHz **sem** soar metálico.
4. **Faixa por dono:** a camada granular pode devolver corpo em 700–1.200 Hz (madeira) e textura em 1,2–4 kHz;
   não deixar ela também ocupar 300–700 Hz, que é onde o baixo e a madeira se encontram.
5. **O desenho deslocado do groove manda.** A resposta entra **depois** do primeiro offset e **antes** do
   segundo, no buraco; não se cria um novo deslocamento nem se quantiza a resposta em cima das posições do
   groove.
6. **Mono é gate:** Utility em mono na camada de resposta; se o random pan colapsar mal, reduzir para ±15%.
7. **Não exagerar:** 2–3 samples no máximo — "Try to not overdo it, not to have so too many samples"
   (00:09:57.839) — e preservar os gaps: é o mesmo princípio do "espaço negativo" do motor.

## Prioridade e esforço

**Prioridade: alta.** A técnica produz **percussão de resposta** a partir do material percussivo orgânico que o
estilo já usa e ataca o buraco medido de 300–4.000 Hz com uma camada que, por construção (HP ~250–300 Hz), **não
carrega sub**. Cruza textura + groove + percussão orgânica de madeira.

**Esforço: médio.** Não falta plugin (Granulator 3 é stock do Live 12 Suite; Serum 2 GranularOsc cobre o resto),
mas o trabalho é manual: printar 1–2 fontes, achar o sample certo (o vídeo diz que "choosing the right sample is
really a key", 00:04:26.800), ajustar grão/scan/LFO de ouvido ("it's up to you to experiment and find the mode
that works best", 00:03:52.879) e colocar os hits nos buracos em ciclo de 2 compassos. Se o projeto não tiver
canal granular, a camada nasce em canal novo (ou reaproveitando um existente). Estimativa: uma sessão de sound
design + uma de A/B; não é preset de 10 minutos.

## Trechos de prova

1. **[00:00:14.960]** "We will be using the granulator 3 which comes with uh live 12." — a ferramenta é o
   Granulator 3, stock do Live 12; não há plugin pago no caminho.
2. **[00:03:21.680]** "percussive loopy textures would be to set the mode of the granulator to loop" — o modo loop
   é o que transforma o sample em textura percussiva; é o ajuste que ele chama de um dos importantes.
3. **[00:10:04.240]** "remember about gaps, about uh having one sound asking another one answering" — o princípio
   de arranjo: os hits granulados vivem nos buracos e se respondem, não empilham.
