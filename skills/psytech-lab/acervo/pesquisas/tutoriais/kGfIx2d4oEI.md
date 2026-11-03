# Serum 2 Bass Patch (PsyTech, DarkProg, Zenon, Forest, PsyBass)

- **Canal:** avulso · apresentador **Fabian Urklang / Urklang Academy**, identificado na própria fala:
  *"I'm Fabian Uklang [sic: Urklang], the founder of the Ulang [sic] Academy"* (00:12:17.200–00:12:23.190)
- **URL:** https://www.youtube.com/watch?v=kGfIx2d4oEI
- **Legenda:** automática EN, lida integralmente (~20:07; o título promete "10 minutes"; ele mesmo diz que será
  *"a huge challenge for me to show you this in 10 minutes"*, 00:04:13.920–00:04:19.670).
- **Descrição oficial (lida):** *"In just 10 minutes, we'll create a versatile Bass Patch from scratch – one that
  works perfectly for styles like PsyTech, DarkProg, Forest, PsyBass, Zenonesque, Techno and beyond."*
- **Ferramentas declaradas na descrição:** **"DAW: Ableton Live 12 / VST: Serum 2"**.
- **Escopo real do vídeo:** construção de **um patch de baixo do zero dentro do Serum 2** (osciladores,
  editor de wavetable, filtro, envelopes, LFO, matriz de modulação, macros) mais a cadeia de FX **interna do
  Serum 2** (equalizador, compressor, splitter, Hyper Dimension, delay). O vídeo **não** desenha kick, hats,
  shaker, madeira, stab, subida nem atmosfera, e não fala de arranjo nem de mix fora do patch. Tudo que não
  estiver ancorado em timestamp abaixo é tradução do estudo, marcada como inferência ou hipótese.

> **Ressalvas de legenda automática (não inventar a partir do erro):** "shores"/"sitecrock"/"dark brock"/
> "senones" = *styles / PsyTech / DarkProg / Zenonesque* (a descrição oficial confirma a lista);
> "pluggy"/"plugy"/"plugginess" = *plucky / pluckiness*; "med"/"medi" note = *MIDI note*; "high cut release"
> (00:05:53.680) = release curto/abrupto (inferência pelo contexto: logo depois ele diz "do at least a little
> bit of release"); "bolar"/"bipolar"/"uni polar" = *bipolar / unipolar*; "ox source"/"oxour" = *aux source*;
> "htz" = *Hz*; "subostcillator" = *suboscillator*.

## Técnica ensinada (2-4 frases)

O baixo é montado em **duas camadas que dividem o espectro**: um **Sub uma oitava abaixo** carrega o
fundamental e um **saw (Osc A) também uma oitava abaixo** tem o **1º harmônico cortado no editor de wavetable**
exatamente porque *"that one will be covered by the suboscillator"* (00:04:51.919–00:04:56.000) — ou seja, o
fundamental existe uma vez só. O saw passa por um **low-pass de 24 dB/oitava com drive**, com o corte parado
entre **20–30 Hz** e mapeado no macro 2; a articulação ("plugginess") vem de um **LFO1 em modo envelope** — não
de um envelope — *"because here I can draw in a different shape which I can't do with an envelope"*
(00:07:26.639–00:07:36.150), em modo unipolar, rate 1/4, com o comprimento da abertura/fechamento no macro 7 e a
**curva X** no macro 8 (inferência: ele mostra duas direções de abertura/fechamento — *"they are open and
closing opposite way"* × *"it's opening and closing in the same way"*, 00:08:40.560–00:08:48.870 — e chama o
resultado de squelchy, 00:08:10.720–00:08:28.309).
Duas camadas de clique fecham o som: uma **EQ com high shelf em ~600 Hz** (macro 1, bipolar, posição ~50% para
baixo) e o **oscilador de ruído tocando um sample de kick/percussão**, com **Env 2 e Env 3 em formatos
diferentes** somadas no nível desse oscilador e liberadas só pelo **macro 4 via aux source**
(00:09:11.920–00:10:59.320). Por cima: **velocity → corte do filtro** em vez de → amp (00:11:28.079–00:11:40.790),
**compressor 6:1 com attack rápido e makeup gain** (00:12:56.160–00:13:16.240) e o **splitter low/mid/high**
(210 Hz e 1k–7k) que deixa o grave seco, joga **Hyper Dimension só nos médios** e um **delay de 3–15 ms em um
lado só nos agudos** — o "house effect" (00:14:09.829–00:15:53.350), com um truque de **curva de modulação que
salta o mix para 100% no primeiro toque do macro** (00:16:41.990–00:17:11.270).

## Ferramenta usada no vídeo (plugin/stock)

| Módulo | Papel no vídeo | Prova |
|---|---|---|
| **Serum 2 — Sub osc** | Sub uma oitava abaixo; volume reduzido; compensa no volume geral do plugin | "Let's open up here sub oscillator one octave down. You can lower the volume here and increase the volume of serum 2." (00:04:39.749–00:04:46.870) |
| **Serum 2 — Osc A (wavetable)** | Saw uma oitava abaixo; **1º harmônico removido** no editor de wavetable | "Oscillator A will be a sawtooth wave also one octave down." (00:04:47.520–00:04:51.909); "Cut out the first harmonic because that one will be covered by the suboscillator." (00:04:51.919–00:04:56.000) |
| **Serum 2 — random phase** | Zerado, para todo note-on começar na mesma posição de fase | "super important is that we go with random phasing all the way down to zero because of course we want to have every bass hit every medi [MIDI] note starting at the same phasing position" (00:05:04.080–00:05:15.270); "it comes to kick and bass phase alignment" (00:05:19.120) |
| **Serum 2 — Voice Filter** | Low-pass **24 dB/oitava**, drive leve, ressonância a gosto | "four basic high cut or lowest [sic] filters 6 12 18 and 24 dB per octave. I like to go with the 24 dB" (00:05:24.790–00:05:31.919); "increase a little bit the drive, a little bit of fatness" (00:05:32.320–00:05:38.150) |
| **Serum 2 — Env 1 (amp)** | Release com sobra para uma nota afetar a seguinte | "What we don't want to do is a high cut release because then we have this subtle click at the end of the med [MIDI] note" (00:05:53.680–00:06:03.749); "one MIDI note and one bass note can affect the other note and change the sound and the shape of the baseline" (00:06:11.759–00:06:21.830) |
| **Serum 2 — LFO 1** | LFO em **modo envelope**, unipolar, rate **1/4**, curva desenhada → filter cutoff | "let's do LFO1 as an envelope. Map this here to the filter cutoff in uni polar mode" (00:07:40.000–00:07:46.319); "You can keep the rate on one over four because the length of this opening and closing we will control with macro 7" (00:07:50.880–00:08:01.510) |
| **Serum 2 — matriz / macros (8)** | macro 2 = cutoffs; 7 = abertura/tempo; 8 = curva X (squelch); 1 = clickiness; 4 = camada de ruído; 5 = house effect; 6 = largura dos médios; 3 = camadas | "macro one for example is for the clickiness of the baseline" (00:02:33.120–00:02:35.280); "Macro 2 is controlling the filter" (00:02:49.200–00:02:50.800); "with macro 5 we can create the super nice psychedelic house effect" (00:03:06.400–00:03:11.760); "with macro six, we can create out of the baseline a dimensional 3D stereo baseline" (00:03:16.879–00:03:22.480); "with macro 7, we can also control the filter and control the pluggginess and ... the shape of the baseline" (00:03:30.400–00:03:36.640); "with macro 8, we can do out of a plugy [plucky] baseline a squelchure [squelchy] baseline" (00:03:42.319–00:03:47.120) |
| **Serum 2 — EQ (FX)** | High shelf ~600 Hz como controle de loudness do clique, macro 1 bipolar | "We add a equalizer. We map here macro one to the high shelf volume in bolar [bipolar] mode ... Let's put this down like so 50%. Let's go with the frequency around 600 htz." (00:09:11.920–00:09:38.310) |
| **Serum 2 — Noise osc (sample)** | Sample de kick (nº 12) ou percussão (bongo, conga, clicky) como transiente; Env 2 e Env 3 em formatos diferentes no nível | "open noise oscillator. You can go here with one of this kick samples. I like to go with kick number 12 ... bongo hits, high head samples, uh conga hits, clicky sounds, whatever" (00:09:47.440–00:10:10.630); "Map this to the level of the noise oscillator. Go to envelope three. Do a slightly different shape than envelope two. And map this also to the level of the noise oscillator." (00:10:26.320–00:10:38.550) |
| **Serum 2 — matriz (aux source)** | Macro 1 e macro 4 como *aux* das rotas (o efeito só existe quando o macro é tocado) | "we say as an ox [aux] source only when we tweak macro one" (00:08:56.560–00:09:02.480); "as an oxour [aux source] only when we tweak macro 4 ... we don't want to have this effect all the time. We want to control the loudness." (00:10:44.720–00:10:53.509) |
| **Serum 2 — matriz (velocity)** | Velocity → filter cutoff, com curva | "what I like to do is I like to map velocity to the filter cutoff. Do a shape like so. Which now means the higher the velocity, the more the filter is opening." (00:11:28.079–00:11:40.790) |
| **Serum 2 — Compressor (FX)** | Controle de faixa dinâmica, makeup, attack rápido, ratio 6:1 | "compressor. And we want to control the dynamic range. Add a little bit of makeup gain. Let's go with a fast attack, a ratio like 6:1 for example." (00:12:56.160–00:13:16.240) |
| **Serum 2 — Splitter (FX)** | Low/Mid/High; crossovers **210 Hz** e **1k–7k**; só um splitter por vez | "Here we have splitters low high low mid high and midside splitter. Sadly we can only put on one splitter." (00:13:38.000–00:13:48.550); "210 Hz, from lows to mids is okay ... from mids to highs, we go from 1k to 7k, 7,000 htz." (00:14:09.829–00:14:18.550) |
| **Serum 2 — Hyper Dimension (FX)** | Só na banda de médios, mix via macro 6: mono → estéreo 3D | "we go into the mids and add a hyper dimension… map it to the mix… out of a mono baseline a 3D stereo baseline" (00:14:18.560–00:14:40.389); "Super nice only for the mids." (00:14:40.399–00:14:42.710) |
| **Serum 2 — Delay (FX)** | "House effect": um lado atrasado 3–15 ms, feedback 0, mix 100% | "What is a house effect? We split the signal into the left and right channel. And one of these channels will add a little bit of delay." (00:14:58.880–00:15:07.910); "Something between 3 to 15 milliseconds ... I go with 10 milliseconds ... feedback all the way down to zero ... a kind of a slapback, a one-time delay ... mix all the way up to 100%." (00:15:22.959–00:15:53.350) |
| **Ableton Live 12** | Só a DAW (declarada na descrição); nenhum device do Live é demonstrado na fala | Descrição: *"DAW: Ableton Live 12 @Ableton / VST: Serum 2 @XferRecords"* |

**Nenhum plugin de terceiros é usado.**

## Tradução para ambiente comum

**A rota do vídeo é 100% Serum 2.** Não há nada a "traduzir" de plugin — todo o patch cabe no Serum 2 (osciladores, editor de wavetable, filtro, envelopes, 10 LFOs com curva desenhável, modo Envelope do LFO, matriz de modulação com `aux source`, macros e cadeia de FX interna).

Se for preciso refazer a parte de FX **fora** do Serum: um Audio Effect Rack do Live com três chains + EQ Eight como crossover (≈210 Hz e ≈1 kHz) reproduz o conceito do splitter; Chorus-Ensemble/Chorus pode fazer o papel do Hyper Dimension; Delay com feedback 0 e mix 100% faz o slapback de um lado. Inferência — o vídeo não usa nada disso. Bibliotecas sampled (instrumentos amostrados) não têm papel aqui: este é um patch de sintetizador com matriz de modulação.

Os outros synths (Diva, Vital, Massive X, Surge XT): a técnica sobrevive pela *ideia* — dois osciladores
(sub + saw), fundamental em uma camada só, LFO one-shot desenhável no corte do filtro, macros — mas os detalhes
que fazem este patch (edição de harmônicos na wavetable, splitter de 3 bandas, Hyper Dimension, curva de
modulação) são específicos do Serum 2. Inferência; não testado em nenhum deles nesta ficha.

## Aplicação por função (guardrails gerais, **proposta**)

Tudo nesta seção que não estiver entre aspas é inferência do estudo para uma faixa psytech; o vídeo não fala de arranjo, groove nem low-end mono.

| Função | O que o vídeo oferece | Como aplicar | Guarda-corpo |
|---|---|---|---|
| **Kick** | **Não desenha kick.** Só afirma que fase importa: *"it comes to kick and bass phase alignment"* (00:05:19.120) e que random phasing zero faz todo note-on começar na mesma posição (00:05:04.080–00:05:15.270) | O kick não muda. O baixo é que se adapta: **random phase em 0** no patch de baixo garante que cada nota comece sempre na mesma fase, então o alinhamento com o kick é repetível — não muda de nota para nota. | Não usar random phase zero como receita de timbre; é ferramenta de fase. |
| **Sub** | Sub osc uma oitava abaixo, volume reduzido, e o fundamental do saw **removido** porque o sub já o cobre (00:04:39.749–00:04:56.000) | **É a técnica mais valiosa**: o fundamental existe em **uma camada só**. Duas opções, excludentes: (a) o Sub do patch vira o sub da faixa (substitui o atual) ou (b) o Sub fica mudo e o sub já existente carrega o fundamental, com o saw sem fundamental por cima. | **Nunca somar** o Sub do patch a um sub que já existe. Se as duas camadas tocarem o fundamental, o low-end engorda e perde definição. Medir em mono antes/depois. |
| **Baixo / rolling** | O corpo do vídeo: saw 1 oitava abaixo + LPF 24 dB + drive, corte parado em 20–30 Hz (00:06:57.280–00:07:02.080), LFO1 em modo envelope unipolar no cutoff (00:07:40.000–00:07:46.319), macro 7 no comprimento da abertura, macro 8 na curva X (00:08:10.720–00:08:28.309), Env 1 com release para uma nota afetar a seguinte (00:06:11.759–00:06:21.830), velocity → cutoff (00:11:28.079–00:11:40.790), compressor 6:1 (00:12:56.160–00:13:16.240) | Montar **uma** camada de articulação com esse desenho e tocá-la nas subdivisões do groove da faixa — não no 1/16 reto da demo. O LFO em modo envelope é o que dá o "pluck" sem depender de envelope: a nota abre e fecha o filtro numa curva desenhada. O release com sobra cria variação nota-a-nota (movimento hipnótico determinístico, não aleatório). | O corte parado em 20–30 Hz é para o som *não* ter corpo em repouso; o saw filtrado assim fica quase inaudível sozinho — é o LFO que o traz. Release longo demais borra o pocket: o próximo ataque tem que continuar distinto. |
| **Hats / shaker** | **O vídeo não trata de hats nem shaker.** O único material agudo é a banda alta do splitter (1k–7k) com o delay de um lado (00:14:09.829–00:15:53.350), que pertence ao baixo | Nenhuma técnica para aplicar. Não levar o Haas/atraso de 10 ms para hats: o efeito do vídeo é *dentro* do patch de baixo. | Sem base no vídeo. Qualquer mudança em hats por esta fonte seria invenção. |
| **Percussão de resposta** | O oscilador de ruído toca **bongo / conga / clicky** como *transiente do baixo*, com Env 2 e Env 3 de formatos diferentes e macro 4 como aux (00:09:47.440–00:10:59.320) | O vídeo **não** faz um canal de resposta: a percussão é uma camada do baixo, disparada pela mesma nota. O que transfere é o *molde*: one-shot curto + duas envelopes de formatos diferentes + macro que libera a camada. Pode informar um enriquecimento de camada de resposta (Simpler com dois envelopes ou Sampler), mas isso é inferência, não receita do vídeo. | Não transformar a camada em percussão independente: no vídeo ela não tem tempo próprio. O macro 4 em repouso deve ficar em zero — a graça é ele só entrar quando acionado. |
| **Madeira** | **O vídeo não trata de madeira.** | Nenhuma aplicação direta. Inferência: preferir madeira/percussão orgânica para ocupar 300–1.200 Hz em vez de empurrar o shelf de 600 Hz do baixo. | Não citar o vídeo como fonte de EQ de madeira. |
| **Stab** | O macro 3 é anunciado como *"add different layers"* (00:02:57.040–00:03:06.390), mas a fala **para em "Also"** e não descreve quais camadas são (a legenda volta ao som) | Nenhuma aplicação. O macro 3 fica como espaço reservado no patch, não como receita. | Não inventar o que seriam as "different layers". |
| **Subida** | **O vídeo não trata de subida/riser.** | Nenhuma aplicação. | Sem base. |
| **Atmosfera** | A única espacialidade é o **Hyper Dimension só nos médios**, criando estéreo 3D a partir de mono (00:14:18.560–00:14:42.710) | Nenhuma receita de atmosfera. O conceito aproveitável é **largura só acima do crossover** (nada abaixo de 210 Hz): para alargar uma atmosfera, o splitter é o modelo. | Low-end mono é boa prática. Hyper Dimension nunca na banda baixa. |

### Guardas específicas (**proposta**)

1. **O fundamental mora em uma camada só.** É a tese do patch (00:04:51.919–00:04:56.000) e a maior proteção
   contra engordar o sub. Se o saw mantém o 1º harmônico e o Sub também toca, há dois fundamentais
   somando — some em fase ou engorda. Cortar o harmônico no editor de wavetable resolve.
2. **O splitter é a prova de que o grave fica seco.** No vídeo, lows (<210 Hz) não recebem Hyper Dimension nem
   delay; só mids (210 Hz–1 kHz) e highs (1k–7k) são processados (00:14:09.829–00:14:40.389). Isso espelha a
   prática de low-end mono: qualquer largura/atraso entra **acima** do crossover, nunca abaixo.
3. **Brilho metálico é o risco real.** O vídeo empilha *três* estágios separados: high shelf em 600 Hz (macro 1),
   Hyper Dimension nos médios (macro 6) e delay de 10 ms/100% wet nos agudos (macro 5). Ele mesmo trata cada um
   como um "sabor" diferente, não como camadas simultâneas. Recomendação: **no máximo dois**, e o delay de um
   lado só entra se o A/B em mono não colapsar. Não somar o shelf de 600 Hz com o Haas no mesmo caminho sem
   conferir fase. O shelf de 600 Hz é **médio**, não agudo — não é ele que cria o brilho metálico; o risco vem do
   Hyper Dimension + delay nos 1k–7k.
4. **O clique do vídeo (shelf ~600 Hz + transiente de kick/bongo) ataca 300–1.200 Hz sem tocar no sub** — é onde
   faixas psytech costumam ter carência de corpo. Já a faixa 1.200–4.000 Hz **não** deve ser preenchida com a
   high band deste patch: o 1k–7k do vídeo é efeito de largura, não corpo. Preencher com madeira/percussão, não
   com Haas.
5. **O groove manda.** O patch é motor de **timbre e articulação**; o ritmo continua da faixa. A demo do vídeo é um
   rolling reto (ele chama de *"rolling baseline"*, 00:11:40.800–00:11:43.040); copiar o 1/16 reto mascara o
   groove da faixa. Tocar a articulação nas subdivisões escolhidas e conferir que o release do Env 1 não apaga a
   distinção entre os hits.
6. **Random phase 0 é gate de fase, não de timbre.** Serve para o baixo começar sempre igual e alinhar com o
   kick; não faz sentido aplicado a pads/atmosfera (lá a variação de fase é o que dá vida). Inferência.

## Valor e custo

- **Valor: alto.** O vídeo é declaradamente do estilo (PsyTech/Zenonesque, na descrição e na fala) e constrói um
  baixo com a divisão que o psytech pede — sub separado do corpo — e com a articulação no médio. Não é "mais um
  patch": é um molde de baixo para o motor de grave sem tocar no sub existente.
- **Custo: médio.** O núcleo (Sub + saw com fundamental cortado + LPF 24 dB + LFO1 em modo envelope + macro 2)
  é uma construção curta na UI do Serum 2. O trabalho real está na escuta — A/B em mono e contra o kick — que é
  onde o patch ganha ou perde.
- **Caminho mínimo recomendado (1ª volta):** só o núcleo + o clique de 600 Hz, com o Sub **substituindo** o sub
  existente (nunca somando). Splitter/Hyper Dimension/Haas ficam para uma segunda volta, e só se a faixa precisar
  de largura.

## Trechos de prova

1. **00:04:51.919–00:04:56.000** — *"Open the wave table editor. Cut out the first harmonic because that one will
   be covered by the subostcillator [sic: suboscillator]."*
2. **00:05:04.080–00:05:15.270** — *"super important is that we go with random phasing all the way down to zero
   because of course we want to have every bass hit every medi [sic: MIDI] note starting at the same phasing
   position."*
3. **00:07:26.639–00:07:36.150** — *"But I like to use an LFO. Therefore, why? Because here I can draw in a
   different shape which I can't do with an envelope."*
4. **00:09:11.920–00:09:38.310** — *"We add a equalizer. We map here macro one to the high shelf volume in bolar
   [sic: bipolar] mode ... Let's put this down like so 50%. Let's go with the frequency around 600 htz."*
5. **00:17:02.560–00:17:11.270** — *"Look at what's going on here. So, as soon as I tweak it, it jumps to
   100%."*

## Limites do estudo

- Estudo baseado na legenda automática; sem escuta do áudio. A legenda erra termos técnicos (ressalvas listadas no topo).
- Escopo do vídeo é só o patch: nada de arranjo, mix fora do plugin, nem os outros elementos da faixa.
- A equivalência dos FX do Serum 2 com devices do Live (splitter via rack + EQ Eight, Hyper Dimension via Chorus-Ensemble, slapback via Delay) é inferência, não testada nesta ficha.
