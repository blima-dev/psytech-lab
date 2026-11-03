# Raw / Hypnotic Techno - Fill Up Your Mids! (Mix Translation On Every Soundsystem)

**Canal:** SINEE Global · **Vídeo:** `ttYFldHqLWk` · **Duração:** 9:36
**Fonte:** legenda automática faixa `en-orig` (English Original, auto), baixada inteira (63.685 bytes; 1.528 linhas). **Tem legenda.** (A faixa `en` traduzida falhou por rate-limit; a `en-orig` cobriu.) A descrição é só confirmatória, não fonte da técnica: *"Today it`s all about the midrange! This area is crucial for your mixes to translate and sound full on other systems and is often overlooked."*

## Técnica ensinada (2-4 frases)

O vídeo trata o vale de médios como **problema de arranjo e balanço**, não de boost de EQ: parte de uma track só com kick/baixo/hats, mostra que o analisador tem apenas *"these two spikes here and the rest of the spectrum is still missing"* `[00:03:16.920–00:03:23.640]` e vai preenchendo o espectro com camadas de synth extras, saturação, OTT e uma duplicata com notas duas oitavas acima, até a curva encostar na média de tracks de clube do Tonal Balance Control. O EQ entra cirúrgico e em modo **dinâmico** somente em 468 Hz e 740 Hz *"just to tame the spikes"* `[00:03:30.799–00:03:46.070]`, nunca para levantar o vale. Depois ele **estreita o espectro dos synths**, cortando o topo para não mascarar kick, baixo, pratos, hats e shakers `[00:06:44.480–00:07:05.150]`. Ele aceita que sozinho o som pareça *"a little bit muffled"* e julga só em contexto `[00:07:13.919–00:07:18.080]`; o alvo é tradução em qualquer sistema, e o erro a evitar é a *"smiley curve"* / *"bathtub"* — grave e agudo exagerados com um buraco no meio `[00:01:40.840–00:01:53.910]`.

## Ferramentas usadas no vídeo (plugin/stock)

- **iZotope Tonal Balance Control** (a legenda só diz o nome): alimentado por *"tracks that I know work well in a club"* `[00:02:32.319–00:02:40.910]`; a meta é *"this is where we want to land roughly"* `[00:05:44.520–00:05:54.909]`.
- **FabFilter Pro-Q 3 em modo dynamic EQ** (a legenda diz "pro Q3"): *"an instance of pro Q3 so you can see at 468 and 740 HZ this is where I engaged the dynamic AQ just to tame the spikes a little bit"* `[00:03:30.799–00:03:46.070]`. É o único EQ citado com números.
- **OTT embutido** (a legenda automaticamente grafou *"a button built-in Ott"*): *"first thing I did was put some Ott on there"* `[00:06:26.199–00:06:30.710]` e *"also of course use the a button built-in Ott same"* `[00:06:30.720–00:06:34.910]`.
- **Saturação**: *"then I introduced some saturation and this really does something to the high..."* `[00:04:31.800–00:04:45.270]` (a legenda quebra a palavra seguinte; não dá para saber se é "highs" ou "high mids").
- **Duplicar a track + notas duas oitavas acima**: *"least I duplicated my track and added some notes two octaves [Music] higher"* `[00:05:09.800–00:05:26.950]`.
- **Delay**: *"also let's engage some delay"* `[00:03:47.599–00:03:51.519]`.
- **Granulator 2 + "Max for Live snake sequencer"**: *"the next sequence is made with granulator 2 and I sequenced this with the max for Life snake sequencer"* `[00:06:00.039–00:06:06.950]`.
- **Analisador de espectro**: *"you can a see the dip in the Spectrum analyzer here"* [sic] `[00:08:23.120–00:08:28.589]`.
- **Camadas de synth nomeadas "Operator" / "Operator C"**: *"the next thing I did was I introduced another operator"* `[00:04:05.000–00:04:11.910]` e *"introduce operator c as well"* `[00:04:48.320–00:04:54.790]`. A legenda **não confirma** se é o instrumento Operator do Live ou só o nome das tracks; ele apenas diz *"The Operators are quite crude because that's how I like my sound"* `[00:04:54.799–00:05:00.310]`.
- **"amp" e "sech"**: *"engaged an amp but the amp is really really low in the mix we are roughly at 9%"* `[00:07:46.759–00:07:57.070]` e *"a little bit of sech and compression to our kick"* `[00:07:57.080–00:08:02.240]`. **NÃO VERIFICADO** — a legenda automática não decifra o que é "amp" nem "sech"; não há base para traduzir isso.
- **ANA 2, VELA, SideKick, Kick 3 e Bitwig não aparecem na legenda** (contagem 0 no `.vtt`). O vídeo **não depende** deles; não há conceito a substituir.

## Equivalentes em ferramentas comuns

O conceito sobrevive inteiro: o que ele faz é **densidade espectral por conteúdo**, medida contra uma curva de referência e protegida por filtro — nada disso exige os plugins do canal.

| No vídeo | Equivalente | Como fazer |
|---|---|---|
| Tonal Balance Control (curva de 6 refs de clube) | **Live 12 nativo: Spectrum** (stock) + a média medida das próprias referências do projeto | Comparar as bandas 300–1.200 e 1.200–4.000 Hz do render com o perfil de referência medido. A curva é **alvo de chegada**, não medidor de pico. |
| Pro-Q 3 dynamic EQ | **EQ Eight** (estático) + **Multiband Dynamics** ou **Compressor** com sidechain filtrado | O **EQ Eight é estático**; para ação dinâmica no Live, o caminho é Multiband Dynamics (bandas largas) ou Compressor com sidechain filtrado. Para um pico fixo, um bell estreito estático já resolve; o modo dinâmico só é necessário se o pico variar de nível. **Não copiar 468/740 Hz** — são os picos da demo dele; medir os próprios. |
| OTT | **Live 12 Multiband Dynamics → preset OTT** (stock) | Só em camada de médio. O vídeo mostra OTT no material de synth. |
| Saturação | **Serum 2** (Distortion/Fold), **Vital** (Distortion), **Surge XT**, ou **Live Saturator/Drive** | Paralelo ou drive baixo; o alvo é densidade de médio, não aspereza. Ver aviso de brilho metálico abaixo. |
| Duplicar track + 2 oitavas | **Duplicar a resposta percussiva / madeira / stab** e transpor +12 (ou +24) | Precisa ser **voz separada**, com filtro e nível próprios — camada, não truque de ganho (elevar volume por transposição de oitava não é a técnica; é abuso dela). |
| Granulator 2 | **Serum 2 GranularOsc**, **Live Grain**, **Sampler em modo granular** | Serve para atmosfera/textura, não para o corpo rítmico do motor. |
| Sequencer "snake" (Max for Live) | passo/arp nativo do Live | Irrelevante para o motor de grave — não criar dependência. |
| Delay | **Echo** (nativo) | Nas respostas (stab/madeira), nunca no kick/sub; HP no delay. |
| Synth layers ("Operator") | **Diva**, **Vital**, **Surge XT**, **Serum 2**, **Massive X**, ou o **Operator** do Live | Um só timbre por função — não empilhar três synths com a mesma função. |
| Madeira / texturas / atmosfera | **Kontakt 8**: Rubber Bridge Guitar (madeira/corda), LOOP GARDEN (orgânico), Ethereal Earth (atmosfera), Vintage Organs (corpo) | Rubber Bridge e LOOP GARDEN são os candidatos naturais a 300–1.200 Hz; Ethereal Earth entra como atmosfera, não como corpo. |
| Amp / "sech" | — | **NÃO VERIFICADO**: sem decifrar a legenda, não traduzir. |

**Custo de plugin:** só dois itens do vídeo são pagos e externos (Tonal Balance Control e Pro-Q 3); ambos têm equivalente nativo.

**O que fica de fora:** **Hybrid Reverb**, **AutoPan** e **Shifter** não têm papel nesta técnica — o vídeo não usa reverb, pan nem modulação; forçá-los seria inventar. **Vintage Organs** só entra se o corpo 200–500 Hz estiver vazio sem competir com o baixo; é o candidato mais arriscado para este gap.

## Notas de aplicação (por função)

**Contexto do projeto de referência (para leitura das notas):** 300–1.200 Hz está **−4,83 dB** e 1.200–4.000 Hz **−5,76 dB** contra a média de 6 referências; low-end mono. Princípio do vídeo, traduzido: *"every move you make that fills the Spectrum more is really helpful"* `[00:05:00.880–00:05:09.790]` — fechar o gap **adicionando conteúdo tocado**, não girando um gain de EQ. Evidência do mesmo projeto: o sino de 300 Hz no baixo foi de −6 para −2,5 dB e rendeu só **+0,38 dB em 300–1.200 Hz** — o limite do EQ estático é real.

| Função | O que fazer | Por quê / limite |
|---|---|---|
| **Kick** | **Nenhum preenchimento novo.** Não boostar 300–800 Hz no kick. | A regra do vídeo é proteger a área do kick do mascaramento dos synths `[00:06:51.919–00:07:05.150]`. Enfiar médio no kick engorda o bumbo e briga com o groove. |
| **Sub** | **Zero.** Nenhuma camada nova abaixo de ~200–250 Hz; sub segue mono. | O vídeo nunca sugere acrescentar grave — ao contrário, ele diz que ainda poderia *"work on the base and take out some"* `[00:05:52.680–00:05:57.199]`. |
| **Baixo / rolling** | Manter o timbre aprovado; **não duplicar o baixo uma oitava acima** como "fill". Filtrar as camadas novas para não invadirem 200–400 Hz. | O médio que falta começa em 300 Hz; duplicar baixo em +12 só cria lama em 200–400 e mascara o próprio rolling. O ganho de EQ já se mostrou pequeno; a alavanca é conteúdo. |
| **Hats / shaker** | **Proteger.** Low-pass/high-shelf de ~4–5 kHz nas camadas de médio novas; não subir shaker para "fechar" a média. | O vídeo é explícito: pratos, hats e shakers *"should live in this area right here and I don't want it to be masked"* `[00:06:59.160–00:07:08.309]`. |
| **Percussão de resposta** | **Principal candidato.** Duplicar a resposta e transpor **+12** (só +24 se 1.200–4.000 continuar vazio), com HP ~200–250 Hz, LP ~4–5 kHz e velocity abaixo do original. Manter os mesmos offsets do groove. | É o gesto literal do vídeo: *"I duplicated my track and added some notes two octaves [Music] higher"* `[00:05:09.800–00:05:26.950]`, e depois *"now we can see that the mid to high mid spectrum is really nice nicely filled out"* `[00:05:25.680–00:05:31.390]`. A duplicata não pode mudar o ataque que faz o pocket. |
| **Madeira** | **Carregador principal de 300–1.200 Hz.** Camada de madeira (biblioteca orgânica) ou segunda voz, filtrada, decay curto. Sinal seco preservado. | O vídeo usa *"noises or atmospheres in the background more textures"* como opção de preenchimento `[00:02:20.840–00:02:26.630]`. Em solista acústico, filtro serial 100% wet é anti-prática; EQ estático pode, modulação serial não. |
| **Stab** | Stab curto em 500–1.500 Hz, LP ~4–5 kHz, entrando entre kicks. | É exatamente o papel da segunda camada de synth do vídeo. |
| **Subida** | Se precisar de médio temporário, noise/riser **band-pass 1.200–4.000 Hz**, curto, no fim de frase. Não usar como preenchimento permanente. | Um riser largo demais vira parede de ruído. |
| **Atmosfera** | Textura atmosférica em 1–3 kHz, baixo nível, filtrada. **Não** usar reverb como "preenchedor". | O vídeo cita atmosferas/texturas como preenchimento espectral, mas diz *"let's keep it simple"* `[00:02:23.959–00:02:29.190]`. Inferência: reverb adiciona espalhamento, não articulação de médio — não fecha um gap de densidade. |

### Como preencher sem engordar o sub nem criar brilho metálico

1. **HP 200–250 Hz (12 dB/oct) em toda camada nova de médio.** Abaixo disso fica o território de sub/baixo; nada novo entra. *(Proposta — inferência; o vídeo não dá valores.)*
2. **LP ou high-shelf 4–5 kHz nas camadas novas.** O topo 5–12 kHz fica com hats/shaker; é a tradução do *"cut off of the high frequencies"* `[00:07:27.520–00:07:36.550]` e do *"narrowed down our frequency spectrum"* `[00:06:44.480–00:06:49.469]`.
3. **Saturação só na camada de médio, em paralelo ou drive baixo.** O próprio vídeo diz que a saturação *"really does something to the high..."* `[00:04:31.800–00:04:45.270]` — é exatamente o risco de aspereza; nunca saturar o master nem o bus de hats para "abrir" o meio.
4. **OTT só na camada de médio, mix baixo; A/B em 2–5 kHz.** OTT densifica high-mid e pode ler como metálico se aplicado no master ou no kick/sub.
5. **Nada de boost estático no master para fechar o vale.** O vídeo também não usa EQ para levantar o vale.
6. **Julgar em contexto, não em solo:** *"you might think that sounds a little bit muffled but let's hear it in context"* `[00:07:13.919–00:07:18.080]`.
7. **A/B com tudo bypassado para ver o vale:** *"if I now disengage all my plugins you can a see the dip"* `[00:08:14.080–00:08:26.710]`.
8. **Não confundir preencher com alargar.** O vídeo não fala de largura estéreo. Este vídeo resolve densidade espectral, **não** resolve estreiteza estéreo do meio; registrar como frente separada.
9. Dado de referência externa útil: medição de stems de referências de psytech mostra o sequenciador concentrando ~90% da energia entre 300 Hz e 5 kHz (0% em sub, ~2% acima de 5 kHz) — preencher com conteúdo articulado, com o bus de médio sem ganho extra.

## Prioridade e esforço

- **Prioridade: alta.** Ataca direto o gap 300–4k medido — o "buraco mais útil para investigar" é corpo médio/presença. Sem tocar em sub, groove ou topo.
- **Esforço: médio.** Não é um plugin: são 2–3 camadas novas (resposta, madeira, talvez stab), cada uma com filtro e nível próprios, mais medição contra as referências. Tudo nativo e reversível; nada de plugin pago.
- **Risco: baixo a médio.** Baixo no sub (HP protege) e no groove (mesmos offsets); médio no brilho metálico se a saturação/OTT for aplicada no lugar errado. Mitigação: LP 4–5 kHz, saturação só na camada, A/B bypassado e escuta em contexto.

## Trechos de prova

1. `[00:03:30.799–00:03:46.070]` **"and for this I'm going to use an instance of pro Q3 so you can see at 468 and 740 HZ this is where I engaged the dynamic AQ just to tame the spikes a little bit"**
2. `[00:06:51.919–00:07:05.150]` **"because I don't really want it to shine in the areas where the kick base and the highights are located so everything that is symbols wres hiatts and shakers should live in this area right here and I don't want it to be masked by my sense"** [legenda automática; "sense" = synths]
3. `[00:05:00.880–00:05:09.790]` **"but even if you do melodic stuff you can apply the same concept so every move you make that fills the Spectrum more is really helpful"**
4. `[00:05:09.800–00:05:26.950]` **"least I duplicated my track and added some notes two octaves [Music] higher ... and now we can see that the mid"**
5. `[00:01:40.840–00:01:53.910]` **"lost in uh what some people call the smiley curve so you have a huge over pronounced low end and chances are very over pronounced highs as well and there's a big dip in the middle looks a little bit like a bathtub"**

**Verificação da fonte (estudo original):** a faixa `en` traduzida falhou com HTTP 429 (rate-limit) e `--write-subs` não encontrou legendas humanas; a faixa `en-orig` baixou inteira via `--sub-langs "en.*"` (62,19 KiB, 1.528 linhas, confirmada por listagem). Contagem de "ANA/VELA/SideKick/Kick 3/Bitwig" no VTT: 0 ocorrências relevantes.

**O que o vídeo NÃO diz (lacunas, para não inventar):** não dá Q, ganho, threshold, ratio, attack/release do EQ dinâmico; não dá as frequências do corte dos synths (só "cut off of the high frequencies"); não fala de sidechain, mono, largura estéreo, BPM ou groove; não decifra "amp" nem "sech"; não mostra a curva-alvo em números; "two spikes" é a demo dele, não uma regra.
