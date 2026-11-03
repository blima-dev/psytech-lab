# How to Make Peak Time Techno Part 2 (Arrangement, Mixing & Mastering)

> id `TdNE8oEb2Lk` · canal **Audioreakt** · 36:48 · peak time techno · template **100% Ableton Live stock**
> (descrição oficial). Capítulos da descrição: 00:00 Intro · 00:28 Track Playback · 01:14 Track origin ·
> 02:38 Arrangement idea · 04:59 Intro / Chorus 1 · 07:36 Break 1 · 11:23 Chorus 2 · 12:58 Break 2 ·
> 18:07 Chorus 3 · 21:01 Final break / outro · 21:52 Variations / Automations · 26:57 Mixing · 30:37 Mastering.
> Legenda automática EN do vídeo obtida e lida (6.464 linhas; 271,46 KiB). **temLegenda=true**.
> Descrição oficial (lida): *"In this template we only have used Ableton Live Stock Plugins, from the creation
> of the song, to the mixing stage, and finally the mastering!"*
>
> **Escopo real do vídeo:** é a **parte 2** — arranjo, automação, mixagem e masterização. O sound design foi a
> parte 1 (link na descrição) e **não é reensinado aqui**; este mapa não atribui ao vídeo o que ele não diz nesta
> parte. Tudo que não estiver ancorado em timestamp é tradução deste estudo, marcada como `INFERÊNCIA` ou `HIPÓTESE`.

## Técnica ensinada (2-4 frases)

O vídeo mostra a montagem de um peak-time techno inteiro **só com devices stock do Ableton**: o arranjo entra em
camadas (kick + clap + percussão + rolling bass filtrado + pad), os stabs e SFX preenchem os buracos sem
densificar a bateria, e as transições são feitas por **automação** — filtro, volume, send para um retorno de washout
e resample do master invertido. Na mixagem, a ordem é **drums → bass → elementos**, com sidechain "mandatory" para
abrir espaço ao kick, `Utility` para não sujar a automação de fader, pan antes do reverb para preservar o stereo e
seleção de sample antes de qualquer processamento. No master, ele mede o trecho mais alto, põe o baixo em **mono
abaixo de 120 Hz**, comprime com ataque de **~30 ms** e EQ na entrada para o kick não disparar o compressor, corta
**<30 Hz** e uma banda suja de **200–500 Hz**, dá clareza em **3 kHz**, satura em dois estágios (**Analog Clip +
Digital Clip**), passa no **Color Limiter** e fecha num limiter final.

## Ferramenta usada no vídeo (plugin/stock)

O autor afirma na descrição que o template usa **apenas plugins stock do Ableton Live**, da criação ao master.
Os devices nominalmente citados/visíveis na legenda:

| Device | Papel no vídeo | Prova |
|---|---|---|
| **EQ Eight** (a legenda diz "eq8") | EQ de canal e de master | "so is this eq8 you can see it's different" (00:08:50.580); "the main lead I have the EQ which is here" (00:22:40.919) |
| **Saturator** | Loudness de canal; saturação do master em dois estágios, **Analog Clip** e **Digital Clip** | "saturator for loudness" (00:27:18.360); "just one saturator this one with analog clip" (00:34:35.820); "use another one in digital clip" (00:34:45.240) |
| **Drum Bus** | Harmônicos e volume no bus de bateria | "drum bus as well a lot just to add some harmonics makes things a bit more louder" (00:27:22.549) |
| **EQ** (de canal, nome genérico) | Corte de graves, boost de presença, redução de aspereza com lowcut/band shelf | "EQ it's usually very subtle ... cut the low frequency ... boost a certain frequency to help a certain element cut through ... reduce the harshness of the high with a locket or a band shelf" (00:27:26.159–00:27:40.549) |
| **Delay** | Groove / sound design, não "mixagem" | "delay is more sound design because it's mainly to add Groove" (00:27:40.559) |
| **Reverb** | Cor, não espaço; ele diz "50 or let's say 80 is like sound design" (sem unidade dita) | "Reverb for me in techno there are 50 or let's say 80 is like sound design ... give color ... not because you wanna put it into a space" (00:27:49.799–00:28:02.750) |
| **Sidechain compression** (device não nomeado) | Ducking "mandatory" contra o kick; automação de threshold entre leads | "sidechain compression ... mandatory just to have leave space to the kick" (00:28:18.600–00:28:25.250); "this compressor is ducking the sound of my lead one" (00:23:51.900) |
| **Utility** | Automação de volume sem mexer no fader; pan preservando o stereo do reverb | "I rather use utility ... I don't mess up with my automation" (00:26:13.860–00:26:28.130); "I need to put a utility to pan because you want the dry signal to depend on the left ... keep the stereo of the Jill and the Reverb" (00:29:37.740–00:29:45.830) |
| **Color Limiter** (a legenda cita "creative extension" logo depois; o vínculo com um pacote específico é `INFERÊNCIA`) | Harmônicos, loudness, largura e calor no master | "color limiter ... great to add harmonics makes things louder as well" (00:35:18.290–00:35:26.690); "making it wider warmer" (00:35:33.119–00:35:42.710) |
| **Limiter** | Limiter final, "squash" do transiente | "one final limiter to kind of squash a little bit the final transient" (00:36:10.500–00:36:23.930) |
| **Retorno de washout** (device não nomeado) | Retorno com reverb/ruído que recebe hats, clap e o mix inteiro | "the return is a washout effect" (00:09:28.920–00:09:35.040); "you send your hats to the return which is kind of creating this noise" (00:22:12.360–00:22:18.049) |
| **"First Look at"** (nome não identificável na legenda) | Recurso no mixdown usado por 8 compassos para tirar kick e baixo na entrada do break | "I use First Look at uh which is on the mix down which is here and then I will place for eight bar this time and then get rid of the kick and bass" (00:13:00.600–00:13:11.509) — **NÃO IDENTIFICADO**: a legenda automática não permite afirmar qual device é; não atribuir Auto Filter nem outro nome sem confirmação |

**Nenhum plugin de terceiros é usado** — nem ANA 2, VELA, SideKick, Kick 3 ou Bitwig. O vídeo não depende de nenhum
plugin fora de um arsenal Live 12 (o Color Limiter tem fallback).

## Tradução para um arsenal compatível

Como a rota é 100% stock, a tradução é quase 1:1 no **Live 12 nativo**: EQ Eight, Saturator, Drum Bus, Compressor
(sidechain), Utility, Delay, Reverb/Hybrid Reverb, Limiter. O único item que pode exigir instalação é o
**Color Limiter** — a legenda cita "creative extension" logo depois (00:35:29.040), mas o vínculo com um pacote
específico é `INFERÊNCIA`; se não estiver instalado, o fallback é Saturator leve + Limiter, também `INFERÊNCIA`
(o vídeo não oferece fallback). Serum 2 (que tem **GranularOsc nativo**), Diva, Vital, Massive X, Surge XT e
Kontakt 8 **não são necessários para esta parte**: o vídeo ensina arranjo, automação, mix e master, não o patch.
Se a subida/atmosfera pedir textura granular, o GranularOsc do Serum 2 é uma rota extra — extensão, não conteúdo
do vídeo. Onde o som é mencionado de passagem, a tradução é só de papel timbrístico:

| Etapa no vídeo | Rota exata no Live 12 | Alternativa / synth | Observação |
|---|---|---|---|
| Camadas do intro: kick + clap + percussão + rolling bass filtrado + pad (00:05:00–00:05:22) | Mesma estrutura no Arrangement; bass com **Auto Filter** ou **EQ Eight** em low-pass; pad sustentado em qualquer synth | Pad: **Diva**, **Serum 2** ou **Operator**; bass: **Serum 2**/Diva com `lowpass_24` | O vídeo não dá patch nem cutoff; só diz que o bass "won't hear it like the proper one" no intro (00:05:13.620) |
| Stab "FM perky sound" (00:02:06.899–00:02:08.039) | **Operator** em FM ou **Serum 2** com warp `fm` | Vital/Massive X/Surge XT em FM | É menção de passagem; a parte 1 é que ensina o som. Não há parâmetros aqui |
| Preencher o terceiro 16º com SFX/stab em vez de drums (00:05:42.360–00:05:54.790) | Clipes curtos de SFX/stab no Arrangement; **não** acrescentar peças de bateria | Samples de madeira/percussão seca do Kontakt 8 (Rubber Bridge Guitar, LOOP GARDEN) para o papel de "resposta" | Princípio de arranjo, não de timbre |
| Transição por filtro de 8 compassos no mixdown (00:13:00.600–00:13:11.509) | **Auto Filter** ou **EQ Eight** automatizado no bus de mixdown; remover kick e bass no trecho | Qualquer filtro nativo | Device do vídeo não identificado; a função é clara, o nome não |
| Retorno de washout com hats/clap/mix (00:09:28.920–00:09:35.040; 00:22:12.360–00:22:18.049) | **Return track** com **Hybrid Reverb** + **Auto Filter** (HP) + **Echo** opcional; automatizar o send | Reverb nativo | O vídeo não nomeia o device do retorno; "washout effect" é a função |
| Resample do master + reverse (00:19:31.980–00:19:40.669) | **Ctrl+T** → input **Resample** → gravar o master → inverter o clipe; cortar o último kick do compasso (00:19:47.690–00:19:53.090) | Nenhuma | Receita nativa exata; não precisa de plugin |
| Automação de volume sem fader (00:25:51.059–00:26:18.890) | **Utility** → Gain automatizado | Fader do track só se não houver automação nele | O vídeo explica o porquê: preservar a automação existente |
| Sidechain contra o kick (00:28:18.600–00:28:31.310) | **Compressor** com sidechain do kick; ou **Shaper/Envelope Follower** em paralelo | Kick 3/SideKick não são usados nem necessários | O vídeo não nomeia o compressor; o conceito é ducking |
| Master: mono <120 Hz, compressão 30 ms, EQ, saturação, Color Limiter, limiter (00:30:37–00:36:23) | Cadeia no Master: **Utility** (mono <120), **Compressor**, **EQ Eight**, **Saturator** ×2, **Color Limiter**, **Limiter** | Se não houver Color Limiter: Saturator leve + Limiter | Ver "Limites" abaixo: é uma cadeia de **loudness**, não um preset para o motor dos 2 min |

**O que falta — e o que isso muda:** nada além do **Color Limiter** (com fallback). O vídeo não usa ANA 2, VELA,
SideKick, Kick 3 nem Bitwig. A única tradução de conceito real é o **Color Limiter** e o device de filtro do mixdown
que a legenda não nomeia. O resto é Live 12 nativo.

## Aplicação concreta em um motor minimal de 2 minutos: por função

Contexto medido do set de referência: **300–1.200 Hz a −4,83 dB** e **1.200–4.000 Hz a −5,76 dB** contra a média de 6
referências externas; **low-end mono**; groove com subdivisões deslocadas **.27/.77**, que não pode ser mexido. O vídeo não
conhece essas medições; ele oferece o **método** (automação, sidechain, mono <120, seleção de sample). A tradução
abaixo escolhe onde o método ajuda e onde ele **pioraria** o quadro — por exemplo, cortar 200–500 Hz no master
como ele faz (00:33:41.820) aprofundaria o vale de 300–1.200 Hz.

| Função | Usar? | Como aplicar (timestamp do vídeo) | Cuidado com o contexto do set de referência |
|---|---|---|---|
| **Kick** | **Sim**, como automação de transição e de compressor — não como timbre | (a) Reintroduzir devagar com low-cut para "you don't hear the boominess just hear the transient" (00:14:56.689–00:14:59.810); (b) automação de gain para tirar/voltar o kick no break: "gain is just for the brake like to kind of get rid of the key code [sic] to introduce the kick" (00:21:56.280–00:22:01.320); (c) no compressor de bus, EQ na entrada ou ataque de 30 ms para o kick não disparar (00:31:27.299–00:31:38.000; 00:32:01.799–00:32:13.080) | O low-cut é **só no trecho de build**, não no kick inteiro; não cortar o sub do kick. A/B obrigatório, porque o kick é a âncora do groove .27/.77 |
| **Sub** | **Não processar; preservar** | O vídeo manda "bass in mono and under 120 years" (00:30:49.220–00:30:54.169) [sic: 120 Hz]. O low-end de referência já é mono: manter. Nada de width, reverb, saturação ou camada nova no sub | O corte de "30 Hertz" do master (00:33:28.919) é **perigoso** se o sub estiver em C#0 (~17,3 Hz); em C#1 (~34,6 Hz) ele passa. Medir antes de aplicar. Não usar o corte para "limpar" o sub |
| **Baixo/rolling** | **Sim** | (a) Filtro/abafamento no intro: "the side trans type of bass line is kind of look at so you won't hear it like a the proper one" (00:05:11.689–00:05:16.310; a legenda diz "look at", o sentido é filtro — `INFERÊNCIA`); (b) automação de volume no drop: "the Baseline is playing at -10 DB and then he's playing at zero DB" (00:18:31.260–00:18:35.510); (c) sidechain "mandatory" (00:28:18.600–00:28:31.310); (d) drop com "strong rolling bass line" (00:18:51.539–00:18:55.610) | **Preservar .27/.77** — automação de ganho não muda o timing; não quantizar nem "endireitar" o groove. O vídeo usa **volume**, não boost de EQ, para o bass ficar maior: seguir isso evita engordar o sub |
| **Hats/shaker** | **Sim, por send e subtração** | (a) Enviar os hats para o retorno: "you send your hats to the return which is kind of creating this noise" (00:22:12.360–00:22:18.049); (b) tirar o ride no break: "I get rid of the ride" (00:07:45.900); (c) no chorus, juntar closed + open + driving hats: "introduced to closed open huts and driving hats all together" (00:20:07.860–00:20:15.120) | **Não** copiar o boost de 3 kHz do master (00:34:16.010) para os hats — é a receita de brilho metálico. O send para o retorno é o lugar do brilho; o retorno deve ter HP para não voltar sujeira ao meio |
| **Percussão de resposta** | **Sim** | (a) Elementos curtos "here and there": "this little stop playing here and there this short element" (00:02:13.080–00:02:17.690); (b) preencher o "third 16th" com SFX/stab, não com drums: "nothing is happening in the third 16th bar you see you have no drums or nothing really added" (00:05:46.800–00:05:54.790); (c) ducking de um elemento contra o outro: "you can sidechain one with the other ... it leaves space for the other" (00:28:49.970–00:28:56.630) | Manter a resposta **fora** das subdivisões principais; ela deve dialogar com .27/.77, não substituí-las. Nada de 16 avos retos |
| **Madeira** | **Sim, no papel do pad/lead** (adaptação) | O vídeo não tem madeira; o papel equivalente é o pad/lead: filtro abrindo para tensão (00:15:57.000–00:16:00.710), pitch bend modulation no pad (a legenda diz "Pitch band"; `INFERÊNCIA`) (00:25:09.059–00:25:12.350), reverb como cor (00:27:49.799–00:28:02.750) | A madeira é **corpo** para o vale de 300–1.200 Hz: não cortar 200–500 Hz globalmente como no master dele (00:33:40.980–00:33:49.549); só notch estreito se houver ressonância. Em fonte acústica, vale a regra do material de referência: dry sagrado, wet ≤25% ou paralelo |
| **Stab** | **Sim** | (a) Stabs como lead, não filler: "consider them like a lead ... not just like to fill out the blank ... adding this excitement and this constant interest" (00:02:23.869–00:02:35.570); (b) ducking do lead 1 quando o lead 2 entra, com automação de threshold: "ducking the sound of my lead one" (00:23:51.900–00:23:55.250) e "automate the threshold ... ducking it even more" (00:24:01.080–00:24:10.370); (c) presença em 3 kHz **no elemento** (00:34:16.010) | O 3 kHz do stab de madeira pode ficar metálico; usar bell estreito e A/B. Preferir **ducking** a cortar EQ: o vale de 1.200–4.000 Hz pede presença, não remoção |
| **Subida** | **Sim** | (a) "Riser knob which is going up and up ... more and more filtered and more and more into Reverb" (00:16:06.170–00:16:14.930); (b) "build everything up ... brutally stop everything" (00:16:21.600–00:16:26.399); (c) stop, lead sozinho, "little silence before to drop" (00:16:56.100–00:17:02.040); (d) resample do master + reverse (00:19:31.980–00:19:40.669) e cortar o último kick do compasso (00:19:47.690–00:19:53.090) | Encaixar em **1:30–1:45**, aterrissando no primeiro drop do set de referência. HP no retorno/riser para não engordar o sub; o silêncio antes do drop é parte da técnica, não um erro |
| **Atmosfera** | **Sim, secundário** | (a) Washout no mix inteiro: "this is a washout effect it's gonna bring all of your sound into a lot of ... Reverb" (00:10:14.820–00:10:20.220); "you just send everything to this return" (00:22:27.539–00:22:31.789); (b) pad sustentado no intro: "steady PAD ... playing this sustained knot" (00:05:16.320–00:05:22.010) | Não deixar cama contínua: automatizar o send e retornar com HP (200–300 Hz é ponto de partida, `INFERÊNCIA`). Atmosfera não pode ocupar o meio que a madeira precisa |

### Onde no grid (0:00–2:00)

Encaixe derivado do método do vídeo para um arranjo minimal de referência de 2 minutos (128 BPM) — **`INFERÊNCIA` de
aplicação**, não uma cópia dos tempos do track dele (o track do vídeo tem outra duração e outras seções):

- **0:00–0:30 — intro cheio, não vazio.** A receita do vídeo é explícita: "this is to avoid to have an
  intro which is too empty" (00:05:05.090–00:05:08.810). Kick + clap + percussão + rolling bass low-passed + pad;
  hats entram no fim ("another hat", 00:05:27.180–00:05:35.039).
- **0:30–1:00 — abrir o filtro do bass e entrar com hats.** No "third 16th" (00:05:46.800), preencher
  com SFX/stab, **não** com mais drums; a automação de pan pode começar aqui (00:24:38.460–00:24:42.419).
- **1:00–1:30 — stab/madeira como lead e washout.** Mandar o mix (ou hats/clap) para o retorno
  (00:22:12.360); se precisar de transição, o filtro de 8 compassos no mixdown (00:13:00.600–00:13:11.509).
- **1:30–1:45 — build.** Reintroduzir o kick com low-cut (00:14:56.689), abrir o filtro do lead
  (00:15:57.000), subir o riser (00:16:06.170), parar tudo (00:16:21.600), deixar o lead sozinho e um silêncio
  (00:16:56.100); no último compasso, resample-reverse (00:19:31.980–00:19:40.669) e cortar o último kick
  (00:19:47.690–00:19:53.090).
- **1:45–2:00 — primeiro drop contido.** Bass de −10 dB para 0 dB (00:18:31.260); "Don't drop with the lead
  one or the lead two" (00:18:10.679–00:18:14.450); manter hats/percussão; **nenhum breakdown longo nos primeiros
  2 min** — o vídeo diz que a ideia era "just one long breakdown later on in the track" (00:03:51.900–00:03:57.170).

### Como aplicar sem engordar o sub nem criar brilho metálico

1. **Sub:** nenhuma camada nova, nenhum saturator, nenhum reverb. O vídeo só autoriza mono <120 Hz (00:30:49.220).
   Se usar o corte de 30 Hz do master (00:33:28.919), medir a fundamental antes: C#1 (~34,6 Hz) passa; C#0 (~17,3 Hz)
   seria comido. Todo retorno de FX precisa de HP — escolha deste estudo (`INFERÊNCIA`): a legenda não menciona HP no retorno.
2. **Meio (300–1.200 Hz):** usar a madeira/stab como corpo, não o sub. **Não** copiar o corte global de 200–500 Hz
   (00:33:41.820): ele é um notch contra "a band that it's a bit messy" (00:33:46.970), não um corte de mix. Se houver
   ressonância, notch estreito e cirúrgico — do contrário, aprofunda o −4,83 dB medido.
3. **Presença (1.200–4.000 Hz):** o boost de 3 kHz do master (00:34:16.010) é a pista para o vale de −5,76 dB,
   mas aplicado **por elemento** (stab, madeira, percussão de resposta), com bell estreito e A/B. **Não** aplicar nos
   hats/cymbals: é aí que nasce o brilho metálico.
4. **Espaço em vez de corte:** o vídeo prefere **ducking** a EQ para dois elementos disputarem o meio ("sidechain one
   with the other so it leaves space for the other", 00:28:49.970). Para o vale medido, ducking preserva os dois corpos;
   corte de EQ elimina justamente o que falta.
5. **Master:** a cadeia do vídeo é de **loudness de peak time** (dois clippers + Color Limiter + limiter final,
   00:34:35–00:36:23). No motor dos 2 min, não aplicar "brutal saturation" (00:34:49.440) no mix inteiro sem A/B;
   renderizar e medir antes/depois. O que vale copiar já: mono <120, ataque ~30 ms, EQ de entrada do
   compressor e limiter final conservador.

## Prioridade e esforço

**Prioridade: alta.** É um dos vídeos da pesquisa que cobre **arranjo + mix + master** de ponta a ponta, e tudo é
stock do Live — quase toda técnica é executável hoje, sem plugin novo. Ele também preenche a lacuna entre o motor dos
2 min e o **primeiro drop**: o build de 8 compassos, o corte de kick/baixo, o resample-reverse e o drop sem lead
são exatamente o que falta para o primeiro drop ser "contido" sem ser vazio.

**Esforço: médio.** Não exige synth; a única instalação possível é o Color Limiter, com fallback. Exige várias
passadas de automação (filtro, gain, sends), um print de resample-reverse, um compressor de bus com sidechain e uma
sessão separada de master. Fazer em etapas — arranjo primeiro, mix depois, master por último — e medir cada etapa.

## Limites e ressalvas de legenda

A legenda automática erra palavras de forma sistemática. Normalizações usadas neste mapa (o erro literal está entre
parênteses): **base** = bass; **truck** = track; **brake** = break; **heart/hut/hearts** = hat/hats; **clubs** =
claps; **precarious / rear Cruise** = pre-chorus; **side trans** = sidechain; **vest** = verse; **120 years** = 120 Hz;
**weeds** = widths (`INFERÊNCIA`); **GK** = decay (`INFERÊNCIA`); **Lavita** = low-pass filter (`INFERÊNCIA`);
**scent** = shaker/percussão de ride (`HIPÓTESE`, não usado como prova). **"First Look at"** (00:13:00.600) não é
identificável: a legenda não permite afirmar o device, e o mapa não inventa. **"colloids"** e **"access of clipping"**
ficaram ininteligíveis e não foram usados. O vídeo não dá valores numéricos de cutoff, Q, ratio ou make-up — só os pontos
citados (30 Hz, 120 Hz, 200–500 Hz, 3 kHz, 16–18 kHz, 30 ms, −10/0 dB) e "a bit of saturation around 0.04 0.06"
(00:35:46.859–00:35:49.079, unidade não dita).

## Trechos de prova: 3 citações literais da legenda com timestamp

1. **00:28:18.600–00:28:31.310** — "finally one thing I forget some sidechain compression as well obviously I will
   use but this is like kind of mandatory just to have leave space to the kick and have this pumping effect I use
   pretty much on on everything it's important for the groove as well"
2. **00:30:49.220–00:30:54.169** — "I will put the bass in mono and under 120 years then you have the weeds which"
   [sic: a legenda diz "years"; o contexto é 120 Hz]
3. **00:32:01.799–00:32:15.289** — "then the attack release this is where attack I will usually always keep like
   30 milliseconds because you don't want to be too aggressive you don't want to turn it off your kick to be cut by
   the compressor or to be reduced by the compressor so 30 millisecond is usually a great time"

> Fonte das três citações: legenda automática EN do vídeo (baixada do YouTube com `yt-dlp --skip-download --write-auto-subs --sub-langs en --convert-subs vtt`).
> Vídeo correlato da mesma fonte para a parte de subida/riser: `44m_K42KtX8` (Sweeps and Risers, Sonic Academy,
> incluído no acervo) — usado só como rota de síntese; a técnica de arranjo/mix acima é toda deste vídeo.
