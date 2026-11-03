# Layering Bass Like a Pro!

> **Fonte:** legenda automática em inglês do vídeo (VTT, 86,19 KiB; 2.104 linhas; vídeo ~11:00).
> Canal: Sonic Academy · Frente: pressao-grave · Prioridade: P1.
> A legenda automática tem erros de reconhecimento: "Anna" = ANA 2, "webs" = waves, "baseline(s)" = bassline(s), "highp pass" = high-pass, "Qbase" = Cubase. O vídeo **não dá nenhum valor** de frequência, dB, ratio ou decay — a demo é inteiramente por escuta.

## Técnica ensinada (2-4 frases)

O vídeo separa o baixo em **camadas com funções distintas**: uma base estável no fundo — *"I can pick a stable sound which is easy to control in the bottom end"* `[00:00:18.960]` — e, por cima dela, ideias que seriam arriscadas num som único. Ele monta **quatro instâncias de ANA roteadas para um group bus**, com ShaperBox no grupo só para duckar sob o kick `[00:00:47.680–00:01:01.189]`. A camada 1 é **sine + saw** (saw em volume menor, só pelos harmônicos), com **re-trigger** para o ataque ficar estável; essa camada é filtrada para isolar o sub, e as notas que caem no kick são apagadas `[00:01:17.920–00:02:20.470]`. A camada 2 é **dois saws, um deles uma oitava abaixo**, com o saw grave re-triggerado e o agudo **sem** re-trigger — o "bunching" de formas de onda no início da nota rende largura estéreo — para preencher o médio acima do sub `[00:02:38.879–00:03:15.670]`. O fecho é o que ele chama de mais importante: **fazer espaço com EQ**, isolar o sub, monoar com width zero, saturar só o médio e comprimir o grupo `[00:03:56.400–00:09:17.750]`.

## Ferramenta usada no vídeo (plugin/stock)

- **ANA 2 × 4 instâncias** — a legenda escreve "Anna": *"I've just got four instances of Anna playing here"* `[00:00:47.680–00:00:49.440]`; *"another one that I just quickly put together in Anna"* `[00:02:30.879–00:02:32.710]`.
- **Group bus** — *"they are all been rooted into a group bus"* `[00:00:51.920–00:00:55.350]`.
- **ShaperBox** (legenda: "shaper box") no grupo, só para ducking: *"there's an instance of shaper box on this as well just to duck things under the kick here"* `[00:00:55.360–00:01:01.189]`.
- **DAW = Bitwig** — *"in Bitwig, you can do this"* `[00:05:31.039]`; *"bring in a step mod inside of Bitwig"* `[00:08:07.199]`.
- **EQ (sem modelo/nome na legenda):** *"grab an EQ here and use the highp pass filter"* `[00:01:53.040–00:01:58.320]`.
- **Step mod do Bitwig** → *"assign that to our filter master frequency"* `[00:08:13.120–00:08:18.390]`, *"set this up to be 16th notes"* `[00:08:18.720]`.
- **Saturator (sem modelo):** *"Perhaps something like a little bit of a saturator on the mid-range stuff"* `[00:08:51.040–00:08:57.910]`.
- **Compressor (sem modelo):** *"So, let's just use the compressor here"* `[00:09:09.279–00:09:17.750]`.
- **Ferramenta de width / mid-side (não nomeada: "our tool")**: *"bring in our tool... We'll set the width to zero"* `[00:07:18.240–00:07:27.110]`; *"We can also use um midside processing again"* `[00:07:30.000–00:07:33.670]`.
- **Terceira camada:** *"Just a filter with a filter envelope being triggered"* `[00:02:34.560–00:02:38.869]`.
- **Quarta camada:** *"another sound in here which has got a lot of reverb on it"* `[00:05:47.840–00:05:52.950]`.
- O vídeo **não nomeia** EQ, saturator, compressor nem reverb, e **não cita** crossover, HP/LP em Hz, ratio ou decay.

## Tradução para ferramentas comuns: Serum 2, Diva, Vital, Massive X, Surge XT, Kontakt 8, Live 12 nativo

**Arquitetura antes do timbre — 4 pistas separadas, não 4 osciladores num patch só.** O vídeo usa quatro instâncias porque cada camada recebe processamento diferente: uma é filtrada para isolar o sub `[00:01:45.990–00:02:02.389]`, outra é aberta em estéreo `[00:03:03.760–00:03:15.670]`, a de acento leva ressonância `[00:04:44.320–00:04:48.230]` e a de highlight leva reverb `[00:05:47.840]`. O mapeamento: **SUB** = sub isolado mono; **BASE** = camada principal sine+saw; **MÉDIO** = dois saws; **ACENTO/HIGHLIGHT** = spots/highlights. Todas para um grupo, com o compressor de grupo no fim `[00:09:07.519–00:09:17.750]`.

**ANA 2 → Serum 2 (rota principal).**
- Camada principal: OSC A em sine (ou o Sub do Serum, slot 4) + OSC B em saw com volume menor, exatamente o gesto `"Just a sine oscillator and a saw wave... Just a little bit lower volume for the saw wave. Just providing a little bit of extra harmonics"` `[00:01:18.720–00:01:25.040]`. Ligar **Retrig** do OSC no painel do oscilador — é o equivalente do *"set this to re-trigger just to keep the attacks of the bass really stable"* `[00:01:32.000–00:01:35.439]`.
- Camada média: OSC A saw + OSC B saw **−12 semitons**. Retrig ligado só no grave — *"The low one, that's one octave down, is re-triggered again"* `[00:02:43.920–00:02:45.280]` — e o agudo **sem** Retrig — *"the top one I've left not re-triggered"* `[00:02:50.319–00:02:52.790]` — para reproduzir o *"slight bunching up of the waveforms at the beginning of the of the note"* que ele associa a largura `[00:02:55.280–00:03:03.750]`. Filtro LP com envelope de filtro: *"Just a filter with a filter envelope being triggered"* `[00:02:34.560–00:02:38.869]`. Largura extra: pan/unison leve no OSC agudo; o "bunching" é comportamento de fase, não um knob chamado width — **INFERÊNCIA de tradução**, validar por escuta.
- Step mod do Bitwig → **LFO 1 do Serum 2**: Beat Sync em **1/16**, Mode **Retrig**, destino **filter cutoff**, com amount baixo. É o mesmo gesto de *"assign that to our filter master frequency... 16th notes"* `[00:08:13.120–00:08:20.720]`.
- **GranularOsc não tem papel neste vídeo.** As camadas mostradas são síntese (sine/saw/filtro), não granular; usar granular aqui seria invenção, não tradução.

**Vital / Massive X / Surge XT (alternativas ao ANA).** Vital é a mais direta: dois osciladores (sine + saw), reset/re-trigger por oscilador, largura estéreo e LFO sync. Massive X: dois osciladores com restart por oscilador e unison para a largura. Surge XT: oscilador sub + dois saws, retrigger e LFO sincronizado. Em todos, o alvo é o mesmo: **sine estável embaixo, saws no corpo, ataque re-disparado, agudo livre para a largura** `[00:01:18.720–00:03:03.750]`. *(Mapeamento de parâmetros por plugin = INFERÊNCIA; o vídeo só mostra ANA 2.)*

**Diva.** Entrega o timbre analógico dos dois saws e o corpo da camada média, mas o truque de fase por oscilador não é tão direto quanto no Serum/Vital; o ataque estável se aproxima pelo retrigger de envelope e unison. Usar Diva se o objetivo for calor analógico, não se o objetivo for o "bunching" exato. *(INFERÊNCIA.)*

**Live 12 nativo — o vídeo inteiro sem ANA/Bitwig:**
- **EQ Eight** por camada: *"you really do want to make space with EQ"* `[00:03:56.400–00:03:59.750]`.
- **Utility** com **Width = 0** e **Bass Mono** no SUB: *"bring it completely mono... We'll set the width to zero"* `[00:07:18.240–00:07:27.110]`. Prática padrão: low-end rigorosamente mono.
- **Compressor com sidechain do kick** no lugar do ShaperBox: mesma função de *"duck things under the kick"* `[00:00:57.280–00:01:01.189]`. ShaperBox desenha a curva; o Compressor segue o kick — o resultado musical é o mesmo, o controle é outro.
- **Saturator** só na pista MÉDIO: *"a little bit of a saturator on the mid-range stuff... And you're still keeping the sub clean of any extra harmonics there"* `[00:08:51.040–00:09:03.646]`.
- **Glue Compressor** no grupo: *"compress all of this as well"* `[00:09:07.519–00:09:09.269]`.
- **Hybrid Reverb** só na pista de highlight: *"a lot of reverb on it"* `[00:05:47.840–00:05:52.950]`.
- **Echo** só na camada de acento, nunca no sub: *"if I'm delaying a sound in a baseline, it's usually in a separate layer isolated in the mids... you're not going to get subs rolling into each other"* `[00:10:24.399–00:10:36.079]`.
- **Operator** para o sub sine puro (uma única parcial, sem filtro ressonante); **Simpler/Sampler** para tocar as camadas como one-shots se preferir; **Grain** só se a camada de highlight pedir textura — não é o que o vídeo faz. **AutoPan** não é a ferramenta de largura aqui (o vídeo usa mid/side estático, `[00:07:30.000–00:07:38.495]`). **Shifter** desloca pitch/frequência, não largura — não traduz o gesto.
- **LFO do Live** em 1/16 no cutoff é o equivalente mais próximo do step mod; o Bitwig tem um modulador de passos, o Live não tem 1:1 — alternativa é automação desenhada. *(INFERÊNCIA de mapeamento.)*

**Kontakt 8 (Rubber Bridge Guitar, LOOP GARDEN, Ethereal Earth, Vintage Organs).** Nenhuma dessas bibliotecas é o baixo do vídeo; as camadas 1 e 2 são síntese. Elas só cabem na **camada de highlight/acento** ("spot sounds" `[00:04:18.560–00:04:23.510]`): Rubber Bridge Guitar para plucks curtos, LOOP GARDEN para textura, Ethereal Earth para a cauda, Vintage Organs para corpo — sempre com HP acima do sub e reverb isolada. *(INFERÊNCIA de adaptação, não é fala do vídeo.)*

**Substituições:** ANA 2 → Serum 2/Vital/Massive X/Surge XT; ShaperBox → Compressor com sidechain do kick; Bitwig (step mod, saturator, compressor; a ferramenta de width nem é nomeada) → Live 12 nativo. **VELA, SideKick e Kick 3 não aparecem neste vídeo** — não há nada a traduzir deles aqui.

## Aplicação por função (kick, sub, baixo/rolling, hats/shaker, percussão de resposta, madeira, stab, subida, atmosfera)

**O que a técnica ataca:** as camadas de dois saws preenchem o corpo de médio `[00:03:08.879–00:03:15.670]` e o mid/side empurra as laterais `[00:07:34.080–00:07:38.495]` — exatamente os dois pontos fracos típicos de um mix psytech (falta de corpo no médio e meio estreito), atacados **sem tocar no sub**.

| Função | O que aplicar | Por quê / limite |
|---|---|---|
| **Kick** | Não processar. Aplicar a **subtração**: apagar da camada de baixo as notas cujo onset coincide com o kick — *"though we are ducking it, we can probably remove the ones that are on the kick"* `[00:02:15.040–00:02:20.470]`. | Abre o espaço do kick sem EQ nem sidechain mais agressivo. O kick continua a âncora; a regra é tirar nota, não mexer no kick. |
| **Sub** | Uma camada só de sine, Retrig ligado, **Width 0 / Bass Mono**, **sem saturação**, LP deixando só a fundamental. | *"isolate the sub even more"* `[00:01:46.000–00:01:47.670]`; *"set the width to zero"* `[00:07:24.160–00:07:27.110]`; *"keeping the sub clean of any extra harmonics"* `[00:09:01.200]`. Prática padrão: low-end mono, sem desfasamento estéreo no sub/kick. |
| **Baixo / rolling** | Sine + saw (saw em volume menor), Retrig no ataque; **HP ~100–120 Hz** para dividir com o SUB; **não quantizar** nem mover onsets do groove. A camada de dois saws entra só no corpo (300–1.200 Hz). **Não** transpor o sub uma oitava para buscar o médio: ele diz que isso deixa o sub instável e pode mudar o groove `[00:03:15.680–00:03:28.710]` — as notas altas vão na segunda camada. | Timbre `[00:01:18.720–00:01:25.040]`, ataque `[00:01:32.000–00:01:40.710]`, corpo `[00:03:08.879–00:03:15.670]`. O vídeo edita **notas**, não timing `[00:02:22.080–00:02:29.430]` — logo o groove sobrevive. *Números de HP = proposta (INFERÊNCIA).* |
| **Hats / shaker** | **Não é tratado no vídeo.** Único princípio aproveitável: manter a camada de saw com LP (proposta: 2,5–3,5 kHz) para ela não subir no topo. | Evita que o corpo novo vire brilho metálico em 3–4 kHz. *LP = proposta (INFERÊNCIA).* |
| **Percussão de resposta** | Melhor candidato: criar uma pista **"spot sound"** separada — copiar o padrão, apagar a maioria das notas e deixar poucos acentos com som próprio e reverb dedicada. | É literalmente o processo *"these little spot sounds within these uh layered patterns"* `[00:04:18.560–00:04:23.510]` e *"I'm just looking for sort of places that I like these little highlights in"* `[00:05:06.950–00:05:09.120]`. Função de resposta = poucas notas, não camada contínua. |
| **Madeira** | Usar a pista de highlight com reverb isolada, HP ≥ 300 Hz, só nos pontos de resposta; nunca como cama contínua. | Camada 4: *"another sound in here which has got a lot of reverb on it"* `[00:05:47.840–00:05:52.950]`. HP = proposta (INFERÊNCIA). |
| **Stab** | Molde = camada 3: filtro com envelope + **ressonância controlada**, LP para não gerar fizz; acento curto, não sustentado. | *"Just a filter with a filter envelope being triggered"* `[00:02:34.560–00:02:38.869]`; *"quite a bit of resonance in the filter as well"* `[00:04:44.320–00:04:48.230]`. |
| **Subida** | **Não é tratado no vídeo.** Não usar este esquema para riser: o vídeo é sobre baixo sustentado, não transição. | Sem tradução possível sem inventar. |
| **Atmosfera** | A única camada com reverb é a de highlight, não uma cama; manter atmosfera fora do sub, com HP e retorno isolado. | *"a lot of reverb on it"* `[00:05:47.840]`; o princípio de delay em camada separada no médio `[00:10:24.399–00:10:36.079]` vale igual para reverb. |

**Nota de fidelidade (direção do filtro do sub):** a legenda diz *"grab an EQ here and use the highp pass filter"* `[00:01:53.040–00:01:58.320]`, mas depois ele fala em *"where the the high cut was for the sub elements"* `[00:04:03.120–00:04:07.519]`. A legenda automática **não permite confirmar** se o filtro é high-pass ou low-pass; o objetivo declarado é *"isolate the sub even more"* `[00:01:46.000–00:01:47.670]`. Na tradução proposta, o SUB leva LP e a camada principal leva HP — a direção exata é decisão por escuta, não está no vídeo.

**Três regras para não engordar o sub nem criar brilho metálico:**
1. **Sub não se duplica.** O vídeo isola o sub e faz o resto começar acima dele — *"make sure that the sub element is uh by itself"* `[00:07:04.800–00:07:14.070]` — no ponto onde o corte do sub termina: *"We can go down to kind of where the the high cut was for the sub elements"* `[00:04:03.120–00:04:07.519]`, com apenas um leve overlap: *"and we can overlap them slightly"* `[00:04:11.760–00:04:12.879]`. Tradução: HP na camada principal e LP no SUB no mesmo ponto; **não** copiar a sine para a camada média.
2. **Brilho vem de saturação e ressonância, não de volume de saw.** O saw entra em volume menor `[00:01:22.640–00:01:25.040]`; a saturação é **só no médio** e o sub fica limpo `[00:08:51.040–00:09:03.646]`; a ressonância fica só na camada de acento `[00:04:44.320]`. Para presença em 1.200–4.000 Hz, prefira o acento esparso a abrir o LP dos saws.
3. **Groove intocado.** As edições do vídeo são subtractivas (`"copying things down and down and down and then subtracting elements from them"` `[00:02:22.080–00:02:27.280]`); nenhuma nota é movida. Se uma nota cair perto do kick, o ducking resolve — só apague a coincidência real de onset. *(INFERÊNCIA.)*

## Prioridade e esforço

- **Prioridade: alta.** É a arquitetura central da frente pressao-grave: separa sub, corpo e acento em canais independentes, o que permite atacar o corpo de médio e a largura do meio sem tocar no sub.
- **Esforço: médio.** Quatro pistas + grupo, EQ Eight por camada, Utility no sub, Compressor sidechain, Saturator no médio, Glue no grupo e uma reverb na pista de acento. Tudo nativo e reversível; o custo real é a curadoria de notas (copiar/apagar), não a instalação.
- **Risco: médio.** O risco é a camada de saws comer o topo ou o sub ficar duplicado. Mitigação: LP no saw, saturação só no médio, SUB com Width 0 e checagem de mono antes de fechar.

## Trechos de prova

1. `[00:00:18.320–00:00:30.720]` **"I can pick a stable sound which is easy to control in the bottom end. uh that doesn't move, that has consistent frequencies and provides the weight and grounding for a track."**
2. `[00:03:54.720–00:03:59.750]` **"when it comes to layering bass like this, you really do want to make space with EQ."**
3. `[00:07:00.479–00:07:07.520]` **"the EQ is probably the most important when layering bass here. You really want to make sure that the sub element is uh by itself."**
