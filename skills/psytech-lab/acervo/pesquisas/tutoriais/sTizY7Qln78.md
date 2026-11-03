# Create Techno Atmos And FX Sounds With Sends

**Canal:** SINEE Global · **Vídeo:** `sTizY7Qln78` · **Duração:** 429 s (7:09)
**Fonte:** legenda automática em inglês, lida integralmente (35,4 KiB, 960 linhas). **Tem legenda.** Todos os timestamps abaixo vêm desse arquivo. Descrição também lida (`yt-dlp --print "%(description)s"` no estudo original).
**Aviso de transcrição:** a legenda automática é de um falante não-nativo de inglês e erra palavras ("red" por *wet*, "Auto pens" por *Auto Pan*, "scent" por *send*, "right" por provável *ride*). Ela também repete cada frase 2–3× (janela móvel) e insere marcadores **[Music]** no meio de algumas falas. Cada leitura duvidosa está marcada no texto — nenhuma foi promovida a fato.

## Técnica ensinada (2-4 frases)

A atmosfera **não é feita no canal seco**: ela mora num canal de retorno, alimentado por um lead de ruído vindo do modular (00:00:42.160–00:00:44.399) e processado em cadeia — **Shifter** com LFO "really really slow" (00:01:03.199; 00:01:19.159), **Reverb 100% wet** de decay muito longo (00:01:22.920), **Drum Buss** com compressão "really hard" mais Crunch/Damp/Drive (00:01:28.840; 00:01:39.720), **Overdrive** (00:01:51.640), um passo para reduzir o "sharpness" (00:01:57.200), um estágio 8-bit / sample rate baixo em dry/wet parcial (00:02:03.960; 00:02:15.360) e **duas Auto Pan** — uma funcionando "more like a side chain... it's not to make left and right pannings" (00:02:22.200–00:02:33.040), outra "polymetric one six" (00:02:34.560–00:02:51.840).

O ponto central declarado é o **envio não-estático**: "I can't send everything statically in this chain because then you always have this for me this is too much" (00:03:29.120–00:03:40.830). Ele manda **pulsos curtos** de send para o retorno ("sent it really really short into this Channel", 00:04:10.560–00:04:16.040) — o efeito floresce só no instante escolhido.

Todos os retornos passam por **um send bus comum** ("I always use a send bus um where all my return channels going through", 00:04:24.160–00:04:31.720) onde ele tira as frequências de lama, põe um LFO no filtro para movimento e consegue filtrar/cortar **todas as atmosferas num ponto só** (00:04:34.320–00:04:53.240), com "cut it off or automate the volume" (00:04:53.240–00:04:59.400).

No fim de seção ele **automatiza o send** para produzir um "outro" — a cauda que atravessa a virada em vez de um corte seco (00:05:11.390–00:05:36.240; capítulo de descrição "05:02 FX Splashes").

## Ferramentas usadas no vídeo (plugin/stock)

**DAW: Ableton Live — confirmado literalmente pela descrição do vídeo:** "a great approach to create atmospheres, textures and big FX splashes **with sends in Ableton Live**". A legenda não nomeia o DAW; quem nomeia é a descrição.

| Elemento | Trecho literal da legenda | Timestamp | Confiança |
|---|---|---|---|
| Canal de retorno (conceito) | "let's take a look in one of my return channels take this noise lead it's just a from the modular" | 00:00:38.800–00:00:45.790 | literal |
| **Shifter** (+ LFO lento) | "I have a shifter here he's modulated by the LFO just the cross frequence so you have always a little movement" · "the LFO is really really slow" | 00:01:03.199–00:01:09.920 · 00:01:19.159–00:01:22.000 | literal (device nomeado); **"cross frequence" é ilegível** — não se sabe se é o deslocamento ou o crossfade |
| **Reverb** 100% wet, decay longo | "then there's a Reverb 100% red really long Decay" ("red" = *wet*, erro de transcrição) | 00:01:22.920–00:01:27.670 | literal, com 1 palavra corrigida por contexto |
| **Drum Buss** com compressão dura | "a drum bus … use the compressor in the drum bus it's a really hard compression" | 00:01:28.840–00:01:39.069 | literal |
| Crunch / Damp / Drive | "Crunch and damp drive" | 00:01:39.720–00:01:42.320 | **INFERÊNCIA**: são os nomes dos knobs do Drum Buss; a legenda não diz o device nessa frase |
| **Overdrive** | "yeah pulls up the Reverb then overdrive" | 00:01:51.640–00:01:57.200 | literal |
| Redutor de "sharpness" | "I use a Suzie to reduce the sharpness of this sound" | 00:01:57.200–00:02:01.840 | **HIPÓTESE**: "Suzie" é provavelmente *Soothe* (oeksound), plugin de terceiro. Não confirmado. **Não é essencial ao método** |
| Crusher 8-bit | "then the D mod to get this grainy sound because it's 8bit and really lows um sample frequence" · "I use dry red because that's too heavy" | 00:02:03.960–00:02:20.239 | **INFERÊNCIA**: descreve bit-depth 8 + sample rate baixo + dry/wet = **Redux**. O nome do device não é dito |
| **Auto Pan ×2** | "then I have two Auto pens the first one as Auto pan I'm using here is more like a side chain it's not uh to to make left and right pannings it's just a side chain" · "a four to the four side chain and another one with a polymetric one six" | 00:02:20.920–00:02:51.840 | literal ("Auto pens" = Auto Pan); a divisão exata do "polymetric" não é dita |
| Filtro modulado por LFO no send bus | "have a LFO here with a filter so more movement" | 00:04:38.720–00:04:44.710 | literal (device não nomeado) |
| EQ de lama no send bus | "here I can reduce those muddy frequencies again" | 00:04:31.720–00:04:40.230 | literal (device não nomeado) |

**O vídeo NÃO depende de ANA 2, VELA, SideKick, Kick 3 nem Bitwig.** A cadeia inteira é stock do Live, com uma única exceção possível (o "Suzie"/Soothe, passo de acabamento). A descrição anuncia "Chop Suey Kick Drum Designer" e "Kikzilla Rumble Generator" — são **links de propaganda do canal** e **não são citados na legenda** (o vídeo não trata de kick).

## Cadeia equivalente no Live 12 (sem nada de terceiros, exceto o passo opcional de de-sharpening)

| Gesto no vídeo | Equivalente | Fidelidade |
|---|---|---|
| Lead de ruído do modular | **Serum 2**: oscilador Noise (`White`/`Pink`/`Brown`) somado a **GranularOsc** sobre um one-shot próprio; ou **Grain** sobre room tone/foley; ou pad/textura de biblioteca | direta em função; a **fonte** muda |
| **Shifter** com LFO lento | **Live 12 → Shifter**, modo Frequency Shift, LFO interno lento (ou LFO do Live mapeado só no deslocamento) | direta (mesmo device) |
| **Reverb 100% wet**, decay longo | **Live 12 → Hybrid Reverb** 100% wet, decay longo (referência de mixing psytrance: ~6 s com damping no topo) | direta |
| **Drum Buss** com compressão dura + Crunch/Damp/Drive | **Live 12 → Drum Buss** (nativo) | direta |
| **Overdrive** | **Live 12 → Overdrive** (ou Saturator) | direta |
| "Suzie" (de-sharpening) | **EQ Eight** com shelf/cut estático na frequência que arde + damping da reverb. É estático, não dinâmico | **parcial** — declarar a diferença |
| Redux 8-bit / SR baixo | **Live 12 → Redux**, blend baixo. **Recomendado não usar** (ver freios) | direta tecnicamente, indesejável esteticamente |
| **Auto Pan** "como sidechain" | **Live 12 → AutoPan**, Phase 0 e sem largura (modulação de amplitude nos dois canais juntos) | direta |
| Auto Pan polimétrica | **Live 12 → AutoPan** com divisão diferente da primeira (ex.: uma em 1/4, outra em 6) | direta |
| Send bus dos retornos | Um bus de atmosferas comum (EQ Eight com HPF baixo) | direta |
| Envio em pulsos curtos | **Automação da alça de send** no Arrangement, em rampas curtas; ou `Utility` no retorno com gain automatizado | direta |

### Cadeia de partida (proposta — o vídeo não dá números)

O vídeo só dá qualitativos: LFO "really really slow", reverb "100% wet" e "really long decay", compressão "really hard", crusher "8bit" com sample rate baixo e blend parcial, send "really really short". **Nenhum valor numérico é falado.** Abaixo, valores de partida marcados como proposta:

1. **Fonte** → textura de ruído (Serum 2 Noise + GranularOsc; ou Grain sobre one-shot).
2. **Shifter** → Frequency Shift pequeno; LFO livre muito lento (proposta: **0,05–0,15 Hz**). Ele diz que o LFO modula "just the cross frequence" — a legenda não permite saber qual parâmetro é; mapeie só **um** e mantenha o resto estático.
3. **Hybrid Reverb** → 100% wet, decay longo (proposta: **~6 s**), damping no topo.
4. **Drum Buss** → Comp alto (o vídeo diz "really hard"); Crunch/Damp/Drive começando baixo (é o passo que mais engorda a cauda).
5. **Overdrive** → leve.
6. **(Soothe ausente)** → EQ Eight, shelf suave onde arde.
7. **Redux** → **desligado** por padrão; se ligar, blend ≤10–20% (ele mesmo recua: "I use dry red because that's too heavy").
8. **AutoPan ×2** → uma em divisão quaternária, outra polimétrica (6), ambas **no retorno**, nunca no sinal seco.
9. **Bus comum dos retornos** → EQ de lama, HP baixo (proteção de sub), LFO no filtro, automação de volume.
10. **Automação da alça de send** → pulsos curtos; zero entre eles.

## Notas de aplicação (por função)

**Leitura crítica antes da receita.** Em projeto com vale medido em 1,2–4 kHz (referência: médio 300–1.200 Hz −4,83 dB e 1.200–4.000 Hz −5,76 dB contra a média de 6 referências; low-end mono; groove deslocado .27/.77):

- **A atmosfera é uma das poucas coisas que legitimamente ocupa 1,2–4 kHz sem competir com o grave.** É a oportunidade real aqui — desde que entre em **pulsos**, não em cama.
- **O vício típico não é falta de reverb, é excesso de silêncio:** em um estudo de arranjo de referência, o corte seco em fronteiras foi o problema medido (gap de silêncio acima do padrão da família, com reverb-wash já em nível normal). **O valor do vídeo é substituir o corte seco pela cauda automatizada**, não somar mais uma camada.

| Função | O que fazer | Onde / banda | Freio |
|---|---|---|---|
| **kick** | **Não enviar.** Se quiser um respingo, que seja numa cópia própria, nunca na alça do kick | — | HP baixo no bus de atmosferas existe justamente para não degolar o sub; não "limpar" o bus subindo o HPF |
| **sub** | **Nunca.** Zero send | — | O Shifter e o Redux do vídeo criam bandas laterais e hash; no sub isso quebra mono/fase. 25–40 Hz não pode se mover (A/B) |
| **baixo/rolling** | **Não enviar.** Se precisar de "longe", faz cópia paralela com HP em ~250 Hz e throw curto — declarado como exceção | 250 Hz+ só na cópia | O rolling é a articulação; reverb no baixo tira definição |
| **hats/shaker** | **Melhor uso da Auto Pan polimétrica** — mas **só na cauda do retorno**. Enviar em pulsos nos hits "abertos", não em cama | Cauda em 5–12 kHz | Nunca pôr AutoPan no sinal seco: a modulação brigaria com os deslocamentos do groove. Rate polimétrico para o movimento **não** cair na grade |
| **percussão de resposta** | **Alvo principal.** Throw curto em cada resposta: o hit seco dispara, a cauda floresce no escuro logo depois | Retorno com HP de fonte em ~300 Hz; cauda 1,2–4 kHz | Um pulso por resposta; fechar em zero entre elas |
| **madeira** | **Dry preservado.** Só throw na última nota da frase, nunca envio contínuo | Cauda curta-média | Reverb escura/dampada; madeira molhada perde o orgânico |
| **stab** | Throw no stab, com Shifter lento para a cauda não ficar estática | 1,2–4 kHz | Em projetos que exigem vácuo antes do drop, **a cauda também** tem de estar extinta nos compassos anteriores. Automação de volume do bus resolve (00:04:53.240) |
| **subida** | **Uso nobre do capítulo "FX Splashes":** automatizar a alça do send no fim da seção; a cauda vira o "outro" e atravessa a virada | Send abrindo no último compasso, fechando no downbeat | Não usar como riser melódico; é cauda, não novo elemento. Em vácuo de 8 compassos, a cauda fica sozinha — é o momento certo |
| **atmosfera** | O próprio retorno: uma camada só, send bus comum, EQ de lama, LFO no filtro, automação de volume | Bus de atmosferas, HP baixo | Não deixar a cama tocar sem pulso |

### Freios para não engordar o sub nem criar brilho metálico

- **Sub:** não enviar nada de grave. A proteção é **disciplina de send**, não HPF no bus — não cortar genericamente 80–120 Hz nos barramentos.
- **Mono:** se qualquer tremolo encostar no low-end, **Phase = 0.0°** e `Utility` com Bass Mono (ex.: 120 Hz). No retorno de atmosfera puro isso não se aplica, mas vale se duplicar o truque para o grave.
- **Metálico:** o Redux do vídeo é a maior fonte de risco — 8-bit + sample rate baixo gera **hash inarmônico**, que não é "ar" nem presença. Deixe desligado; se ligar, blend ≤10–20% (ele próprio diz "that's too heavy", 00:02:19.239). Nada de ring mod. Frequency shift pequeno.
- **Não resolver o metal com LP estático muito baixo fechando o canal inteiro:** corte pontual/shelf é diferente de fechar o canal.
- **Densidade:** o Drum Buss em compressão dura sobre uma reverb longa é o passo que mais "engorda". Comece com ele baixo e só suba se a cauda sumir no contexto.
- **Caixa 300–1.200 Hz:** a reverb longa tende a acumular lama aqui. É o que o EQ do send bus do vídeo existe para resolver (00:04:34.320) — mas corte **no retorno**, não no bus principal.
- **Ar (5–16 kHz):** se for usar a atmosfera para abrir ar, prefira cauda limpa a aliasing.

### Como provar (A/B)

1. Mute A/B por seção (ex.: bars 1–32 e 33–64).
2. **25–40 Hz e 40–55 Hz:** têm de ficar **iguais** com a atmosfera ligada (teste do "engordou o sub").
3. **1,2–4 kHz:** pode subir — é o objetivo. Se subir em 5–10 kHz junto com aspereza, o Redux/Overdrive está alto.
4. **Correlação L/R abaixo de ~120 Hz:** não pode haver conteúdo estéreo novo.
5. **Contagem de gaps de silêncio:** a ideia é **cair** (substituir corte por cauda), não subir o wash de reverb.

## Prioridade e esforço

| Dimensão | Valor | Justificativa |
|---|---|---|
| **Prioridade** | **alta** | Ataca de frente dois problemas comuns no gênero: o déficit de 1,2–4 kHz e o excesso de silêncio nas fronteiras. Valida por fora o gesto de cauda pontual em retorno dedicado, sem custo de compra |
| **Esforço** | **médio** | Montar a cadeia é rápido (tudo stock, ~15 min). O custo real está na **automação de pulsos frase a frase** e na prova A/B. Não é plug-and-play, mas não bloqueia uma primeira versão |

## Trechos de prova: citações literais da legenda com timestamp

1. **"of course I can't send everything statically in this chain because then you always have this for me this is too much"** — 00:03:29.120–00:03:40.830
   *Prova do princípio central: o envio **não** é estático; mandar a faixa inteira para o retorno é o erro que ele nomeia.*

2. **"sent it really really short into this Channel and you got this"** — 00:04:10.560–00:04:16.040
   *Prova do mecanismo: o disparo é um **pulso curto** de send.*

3. **"this I always use a send bus um where all my return channels going through"** — 00:04:24.160–00:04:31.720
   *Prova da arquitetura: todos os retornos somados num bus único para EQ de lama, filtro modulado e automação de volume.*

## Fontes e limites

**Legenda (fonte primária):** automática em inglês, lida integralmente (960 linhas); as citações foram conferidas contra ela. Duração confirmada em 429 s; última marcação é 00:07:10.800 — legenda **completa**.

**Descrição do vídeo:** usada para (a) confirmar Ableton Live ("with sends in Ableton Live"), (b) os capítulos (`00:36 FX Chain · 03:54 Backing Noise Triggers · 05:02 FX Splashes · 06:35 Outro`) e (c) separar os plugins de propaganda da técnica.

**O que NÃO foi feito / não verificado:**
- Nenhuma verificação de runtime; nada foi renderizado ou medido.
- Não assistido ao vídeo em imagem: **nenhum valor que aparece na tela** (rate do LFO, decay, knobs do Drum Buss, divisão das Auto Pans) foi lido. Tudo que é número aqui é **proposta**, declarada.
- "Suzie" → *Soothe* é **HIPÓTESE**; o device não é nomeado de forma legível na legenda.
- O Redux é **INFERÊNCIA** a partir de "8bit and really lows sample frequence" + contexto Ableton; o nome não é dito.
- A referência de ~6 s de reverb com damping no topo vem de método de mixing psytrance (estudo externo), não do vídeo.
