# How to Use Clipping for Louder, Punchier Mixes

**Fonte:** YouTube `R6xwYFH5SSY` · Sonic Academy · Larry Holcombe · ~12m31s
**Legenda:** automática EN do vídeo, obtida e lida → `temLegenda=true`
**Contexto:** material de referência minimal psytech hipnótico · 128 BPM · tônica C# · arranjo de referência dos 2 primeiros minutos
**Aviso de escopo:** o vídeo não cita Serum 2, Diva, Vital, Massive X, Surge XT, Kontakt 8, Live 12, ANA 2, VELA, SideKick, Kick 3 nem Bitwig. Toda ponte para o arsenal compatível abaixo é mapeamento deste estudo (`INFERÊNCIA`), não conteúdo do vídeo.

## Técnica ensinada (2-4 frases)

O clipper fixa um teto (ceiling) e corta a forma de onda que passa dele; diferente do limiter, não tem attack/release e não desenha envelope de volume — "It just chops the top of the waveform" (00:02:37–00:02:45). O corte gera distorção harmônica, normalmente um burst de alta frequência que, em drums, soma punch e informação de transiente, e em fonte musical soa fora de lugar (00:02:44–00:03:14). Hard clip (teto em ângulo reto) soa agressivo, crocante e brilhante; soft clip (curva arredondada) soa mais quente, espesso e musical (00:03:41–00:04:39). Serve para loudness, tone/punch e controle de transientes em buses, instrumentos individuais e master — e quando não se quer distorcer a fonte (baixo, vocal), o vídeo manda usar limiter (00:05:03–00:05:26; 00:08:58–00:09:09).

## Ferramenta usada no vídeo (plugin/stock)

- **StandardCLIP, da SIR Audio Tools** — a legenda automática transcreve "standard clip from Sir Audio Tools". O próprio vídeo libera a substituição: "you can replace that with any clipper you have at your disposal" (00:00:14–00:00:19).
- Controles demonstrados: **teto/ceiling** ("I'm setting a ceiling essentially", 00:01:43–00:01:47), modo **Hard Clip** ("let's put it on to the hard clip mode", 00:01:37–00:01:38; "hard clipping has a very sharp threshold here", 00:03:41–00:03:46) e modo **Soft Clip Pro** com um controle de "soft clip saturator" que arredonda a curva ("we need to move this soft clip saturator. And you'll see this becomes more rounded", 00:03:55–00:04:07).
- Não é plugin stock de DAW. Não há menção a Bitwig, Live, ANA 2, VELA, SideKick ou Kick 3 neste vídeo.

## Tradução para um arsenal compatível: Serum 2, Diva, Vital, Massive X, Surge XT, Kontakt 8, Live 12 nativo — sem ANA 2, VELA, SideKick, Kick 3, Bitwig

> Tudo nesta seção é `INFERÊNCIA` de engenharia: o vídeo só ensina o conceito de clipper (teto, curvas hard/soft, clipper vs. limiter); ele não nomeia nenhum desses instrumentos.

**Princípio de substituição:** o vídeo diz que qualquer clipper serve. O que precisa ser preservado é (a) teto fixo, (b) curva dura vs. curva suave, (c) ausência de envelope de volume. Qualquer waveshaper com essas três propriedades cumpre o papel.

- **Live 12 nativo — Saturator (o substituto direto).** Usar a seção Waveshaper: curva **Digital Clip** como equivalente do hard clip e **Soft Sine / Medium Curve** como equivalente do soft clip. `Drive` empurra o sinal contra o teto; `Output` compensa o ganho; `Dry/Wet` permite o uso paralelo; `Oversampling` (2x/4x) reduz o aliasing gerado pelos harmônicos de alta frequência descritos no vídeo. Obs.: Saturator, Limiter e Drum Buss são dispositivos nativos do Live 12 fora da lista curta de devices (Simpler/Sampler/Grain, Operator, Echo, Hybrid Reverb, AutoPan, Shifter) — citados porque são os nativos que cumprem a função de clipper; se a instalação não os tiver, usar qualquer waveshaper com curva de clip.
- **Live 12 nativo — Limiter (o papel oposto, não o clipper).** O vídeo define limiter como "an infinite ratio compressor" com attack/release que "will cut a volume envelope to turn down that peak" (00:02:09–00:02:20). No Live, é o dispositivo para o caso em que o vídeo manda **não** distorcer: baixo e vocal (00:08:58–00:09:09).
- **Serum 2.** Dois usos, ambos de sound design (o sintetizador só processa a própria saída, não é bus): (1) os modos de warp por oscilador **`hard_clip`** e **`soft_clip`** (presentes no vocabulário de warp do Serum 2) para desenhar click de kick, stab e transientes; (2) o **FXDistortion** na cadeia de FX do patch, escolhendo a curva dura ou suave — útil para o stab/baixo saírem do synth já com a saturação que o vídeo descreve, antes de qualquer processamento de bus.
- **Vital.** Módulo **Distortion** com curvas de clip duro/suave no patch — mesmo uso de sound design do Serum 2; não substitui um clipper de bus no Live.
- **Massive X.** Módulo de distorção do insert FX, com curva dura ou suave — sound design do patch, não processamento de áudio externo.
- **Surge XT.** **Waveshaper** com curvas duras/suaves. Se a instalação tiver o **Surge XT Effects** (versão só de efeitos), ele pode entrar como insert no canal e fazer o papel de clipper de bus; caso contrário, fica no sound design do patch.
- **Kontakt 8 (Rubber Bridge Guitar, LOOP GARDEN, Ethereal Earth, Vintage Organs).** São instrumentos de sample, não processadores. A regra do vídeo para fonte musical se aplica: "you're not going to clip a a a felt piano necessarily unless that's the sound you're going for because it will be out of keeping with the the source sound" (00:11:03–00:11:16). Ou seja: **não clipar** essas bibliotecas; no máximo limiter se o pico atrapalhar.
- **Sem ANA 2, VELA, SideKick, Kick 3 e Bitwig:** nada a substituir, porque nenhum deles aparece no vídeo. O StandardCLIP do vídeo também não está na lista do arsenal; a tradução é o Saturator do Live (ou qualquer waveshaper com teto e curva dura/suave).

## Aplicação concreta em um motor minimal de 2 minutos: por função

**Restrições medidas do set de referência:** o meio 300–1.200 Hz está **−4,83 dB** e 1.200–4.000 Hz **−5,76 dB** contra a média de 6 referências externas; low-end é **mono**; o groove usa subdivisões deslocadas **.27/.77**.

**Regras que saem do vídeo e valem para todas as funções:**
1. O clipper **não move o tempo**: não tem attack/release e "just goes bang, decapitates the transients" (00:10:24–00:10:35). Por isso ele preserva melhor as subdivisões .27/.77 do que um limiter com attack/release, que amolece transientes e pode borrar o deslocamento percebido.
2. Clipping **reduz o pico e aumenta a loudness percebida**: no demo, o drum bus clipado pica em −16.9 dB contra −13.3 dB do bypass — "about 3 dB quieter in peak level" — e ainda assim "in perceived volume, we're a little bit louder" (00:00:54–00:01:15).
3. Hard clip **adiciona elementos de alta frequência**; soft clip é mais quente (00:10:45–00:10:51). Para não criar brilho metálico, preferir soft clip no corpo e reservar hard clip para transientes curtíssimos.
4. **Nunca clipar o ramo que contém o sub.** O vídeo só autoriza clipping em drums/percussão e master; para baixo sem distorção, limiter (00:08:58–00:09:09). Como o low-end do material é mono, todo ramo clipado deve ser **high-passed** antes do clipper, para que os harmônicos gerados não caiam na faixa mono do sub.
5. Pós-clipper, **low-pass** no ramo clipado (corta o "white noise" que o vídeo descreve em 00:02:58–00:03:04) e medição A/B de 300–1.200 Hz e 1.200–4.000 Hz antes de manter.

**Por função:**

- **Kick:** separar em dois ramos. O ramo **sub (< ~120–150 Hz)** fica limpo, mono, sem clipper (limiter só se o pico pedir). O ramo de **click/ataque** recebe soft clip (corpo) ou hard clip (só se quiser agressão), com high-pass em ~150–250 Hz antes e low-pass em ~6–8 kHz depois; misturar em paralelo (~10–25% de partida) e devolver o ataque com **transient shaper** — é exatamente a receita do vídeo para o clap: "combine some clipping with some transient shaping" (00:06:37–00:06:43) para recuperar o transiente perdido (00:06:28–00:06:30; 00:07:14–00:07:22). Oversampling ligado.
- **Sub:** **sem clipping.** O vídeo é explícito: se não quer distorcer o baixo, "you'd probably reach for a limiter" (00:08:58–00:09:01). Clipping aqui geraria harmônicos que engordam o low-end e borram o mono. Se precisar de controle de pico, limiter no ramo de sub, com o cuidado de não usar attack/release longo (borra o .27/.77).
- **Baixo/rolling:** o vídeo escolhe **limiter** para transparência ("limiting's a little bit more transparent", 00:08:50–00:08:58). Para atacar o déficit de 300–1.200 Hz sem engordar o sub, usar um **ramo paralelo de exciter**: high-pass em ~300 Hz → soft clip (Saturator, curva Soft Sine/Medium Curve) → low-pass em ~4–5 kHz → mix ~8–15%. O fundamental e o sub do baixo ficam intocados e mono; o ramo clipado é só o que preenche o meio. Não usar hard clip no baixo inteiro: o vídeo associa hard clip a "punchy, crunchy… very aggressive" (00:04:25–00:04:39), o que viraria aspereza no rolling. Preservar o .27/.77 mantendo o clipper sem envelope e evitando limiter com release longo no canal do baixo.
- **Hats/shaker:** **não usar hard clip.** São fonte já rica em alta; o hard clip "is going to introduce more high-frequency elements" (00:10:45–00:10:48) e o vídeo avisa que o resultado pode ser "harsh sounding" (00:03:19–00:03:21). Se o pico atrapalhar, limiter; no máximo um soft clip bem leve, com low-pass em ~10–12 kHz depois. Não usar este canal para "resolver" o déficit de 1.200–4.000 Hz — o brilho metálico nasce aqui.
- **Percussão de resposta (clap, rim, woodblock, toms):** **melhor ponto de aplicação do vídeo.** É o clap do demo: "let's take this onto the clap… Let's try and give it thickness to this clap" (00:05:44–00:05:57), com o resultado "how much thicker that sounds" (00:06:18–00:06:19) e a perda de transiente corrigida com transient shaper (00:06:28–00:06:55). Usar **soft clip** para claps/toms (espessura) e **hard clip** só em rim/woodblock curtos (snap), sempre em paralelo, high-pass antes (~200 Hz) e low-pass depois (~6–8 kHz). O posicionamento deslocado .27/.77 é preservado porque o clipper não tem envelope.
- **Madeira (Kontakt: Rubber Bridge Guitar, LOOP GARDEN, Ethereal Earth, Vintage Organs):** **não clipar.** O vídeo trata fonte musical como outro caso: clipping "will be out of keeping with the the source sound" (00:11:03–00:11:16). Se o pico incomodar, limiter; se faltar corpo, EQ/soft saturation leve, não clipper.
- **Stab:** tratar como percussão curta: **soft clip em paralelo** (10–20%) para dar corpo e presença de meio, low-pass em ~6–8 kHz depois para não metalizar. Pode ser feito dentro do próprio Serum 2 (warp `soft_clip` ou FXDistortion) ou no Saturator do canal.
- **Subida (riser):** **não coberto pelo vídeo.** `NÃO VERIFICADO` como receita. Por lógica do que foi dito (clipping cresce a distorção conforme o sinal sobe e adiciona alta frequência), o risco de aspereza no clímax é alto; se precisar conter pico, limiter. Não usar clipper como "cola" de riser.
- **Atmosfera:** **não clipar.** Mesma lógica da fonte musical (00:11:03–00:11:16); o burst de alta frequência descrito em 00:02:52–00:03:04 arruinaria o tecido atmosférico. Limiter só se houver pico isolado.
- **Bus/master (opcional, fora do motor de 2 min):** o vídeo usa clipping em **todo** master, "often two clippers, sometimes three clippers" (00:11:46–00:11:53), e recomenda hard clip sutil no master porque a saturação já foi feita no mix (00:09:13–00:09:24): "a little bit of hard clipping subtly is often pretty much inaudible, but you're just managing your transients" (00:09:27–00:09:37). Se for aplicado, entrar **antes** do limiter (para o limiter trabalhar menos) e conferir o gate de true peak — clipping deixa de ser inaudível quando começa a distorcer os picos de verdade.

## Prioridade e esforço

- **Prioridade: alta.** Dentro da frente `pressao-grave` é uma das respostas mais diretas à dor registrada "punch sem esmagar com Limiter". O vídeo dá o mecanismo exato: clipper corta o pico antes do limiter, o limiter reduz menos e o punch sobrevive; no master ele chega a empilhar dois ou três clippers (00:11:46–00:11:53). Bônus: os harmônicos gerados podem ajudar a preencher o meio medido (−4,83 dB em 300–1.200 Hz e −5,76 dB em 1.200–4.000 Hz), desde que controlados.
- **Esforço: médio.** Não é plug-and-play: exige separar ramos (sub vs. ataque), high-pass/low-pass em volta do clipper, ganho de entrada/saída, oversampling, blend paralelo, transient shaper no caso do clap/kick e A/B medido. O risco de exagero é alto — hard clip em hats, baixo inteiro ou atmosfera cria exatamente o brilho metálico e o "engorda sub" que o material evita. Vale fazer primeiro em **percussão de resposta + ramo de click do kick**, que é onde o vídeo mostra o maior retorno com o menor risco.

## Trechos de prova: citações literais da legenda com timestamp

1. **00:01:30.760–00:01:35.430** — "Okay, so what's clipping all about? Well, what clipping does is it basically cuts off the peak of a signal."
2. **00:02:37.280–00:02:45.190** — "Now, clipping doesn't do that. It doesn't work on a volume envelope. It just chops the top of the waveform."
3. **00:03:06.910–00:03:14.959** — "But, when we're using clipping on things like drums, that white noise can actually add to the punch of the drum sound. It can add to the transient information."
4. **00:03:41.590–00:03:46.622** — "So, hard clipping has a very sharp threshold here."
5. **00:04:25.800–00:04:39.190** — "hard clipping we generally associate with, as I said, punchy, crunchy sounds, very aggressive sounding. Whereas a soft clipping, bit more gradual saturation, sounds a bit warmer, a bit thicker sounding."
6. **00:06:37.520–00:06:43.470** — "You can actually do something like this where you combine some clipping with some transient shaping."
7. **00:08:58.710–00:09:01.750** — "So, say the bass, we didn't want to distort the bass, you'd probably reach for a limiter."
8. **00:09:27.120–00:09:37.720** — "But a little bit of hard clipping subtly is often pretty much inaudible, but you're just you're just managing your transients a little bit."
9. **00:10:45.080–00:10:54.440** — hard clipping adiciona conteúdo agudo; soft saturation soa mais "warm"; ambos tornam o tom mais agressivo (Sonic Academy).
10. **00:11:03.720–00:11:16.520** — "Whereas, for musical elements like, you know, you're not going to clip a a a felt piano necessarily unless that's the sound you're going for because it will be out of keeping with the the source sound."

## Limites e o que não foi verificado

- **O áudio do vídeo não foi ouvido.** A dissecação é só da legenda automática EN; os julgamentos de "mais quente", "mais grosso" e "mais agressivo" são os do apresentador, não medição própria.
- **O motor do set de referência não foi re-medido.** Os valores −4,83 dB (300–1.200 Hz) e −5,76 dB (1.200–4.000 Hz), o low-end mono e as subdivisões .27/.77 vêm de um diagnóstico prévio do set de referência, não de nova medição.
- **O vídeo não cobre** baixo rolling minimal, riser, atmosfera, tônica frígia em C#, 128 BPM nem nenhum dos plugins listados. As aplicações nessas funções são `INFERÊNCIA` a partir do princípio (clipper sem envelope; hard clip brilha; limiter quando não se quer distorcer), não receita demonstrada.
- **Faixas de blend, high-pass e low-pass** sugeridas acima são pontos de partida de engenharia (`INFERÊNCIA`), não números do vídeo. O vídeo só quantifica a comparação de pico: −16.9 dB clipado vs. −13.3 dB bypass (00:00:54–00:01:03).
