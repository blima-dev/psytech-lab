# Essential Noises - Create A Raw / Hypnotic Techno Groove With Noise Samples

> id `A6XjjwGUkA8` · SINEE Global · 6:01 (361 s) · frente da curva **groove** · prioridade de curva **P1**.
> Legenda automática EN obtida e lida na sessão original (176 cues). **temLegenda=true**. Automação de fala com
> vários erros de ASR — as correções estão listadas no fim e nenhuma afirmação abaixo depende de palavra
> corrigida. Descrição oficial lida (usada só para identificar o pack e a cadeia de origem):
> *"Today we`re gonna look at a track structure that was entirely created with our newly released sample pack -
> Essential Noises!"* · *"Eurorack: Noise Plethora, Rossum Electro-Music Evolution, ADDAC 603 VC Triple Bandpass
> Filter, ... Basimilus Iteritas Alter"* · *"Outboard: Culture Vulture, Mackie1604, Tegeler Creme, SSL Fusion,
> Dangerous Music Bax Eq, Dangerous Music Convert AD"* · *"Pack contains 359 One Shots & Loops"*.
>
> **Escopo real do vídeo:** é um **demo de pack**, não uma aula de groove. Ele abre um projeto pronto e passa por
> **6 trilhas** uma a uma, dando ~1 frase de decisão por trilha. O projeto inteiro usa **só amostras do pack +
> efeitos do Ableton**, com duas exceções declaradas: *"except the kick drum and Rumble which is just a regular good
> old 909 kick"* (00:48.480–00:54.359) e *"this track is made only with samples from the pack and some a button
> effects"* (00:42.480–00:48.470; "a button" = *Ableton* na legenda automática). Não há valores numéricos além de
> **1K** e **800 HZ**; taxa/profundidade de LFO, Q, ratio, tempo de delay e rate do phaser **não são ditos**.

## Técnica ensinada (2-4 frases)

O groove é montado com **frações mínimas de amostras de ruído**, não com texturas inteiras: a trilha de textura usa
"a small snippet" e é mantida **sem EQ**, porque ele queria "the complete frequency spectrum of this one"
(01:24.600–01:43.749); e o hi-hat fechado é literalmente "just a little click from the very beginning of the sample"
(04:29.680–04:35.479). Onde a amostra traz grave indesejado, ele **corta tudo até 1 kHz** e devolve corpo com
**Corpus em modo tube** — o grave sai, a ressonância volta no médio (02:46.599–02:58.750). A variação que impede o
loop de soar copiado vem de **LFO mapeado no attack (e no decay) do sampler**: "the LFO really gives us a nice variety
on the attack phase" (04:15.639–04:21.880). O resto do caráter é stock e barato — **Auto Filter com pico ressonante
em ~800 Hz**, Echo, Amp e Phaser (03:47.159–04:15.639), delay com **corte de graves** (04:40.440–04:47.550) e
**Glue Compressor mapeado no kick** (02:19.640–02:26.250) para o ruído ceder lugar ao bumbo.

## Ferramenta usada no vídeo (plugin/stock)

| Device | Papel no vídeo | Prova (legenda literal) |
|---|---|---|
| **Sampler da track** (device **não nomeado** no vídeo) | Toca um recorte curto da amostra; **Attack e Decay mapeados num LFO**; "hidden menu" com a *attack phase* | "I m the attack and Decay to this LFO here this is the Decay and then in this little hidden menu the attack phase" (02:06.759–02:19.630) |
| **Corpus** (resonador do Live) — `INFERÊNCIA` pelo ASR "corpus" + "tube mode" | Depois de cortar tudo até 1 kHz, devolve ressonância física; mudança "subtle" que ele manteve | "I filtered everything out up until 1K and then I put a corpus on the track in tube mode" (02:49.360–02:58.760) |
| **Auto Filter** (ASR "autof filter") | Pico ressonante **em torno de 800 Hz** na percussão | "an autof filter with the frequency around 800 HZ and quite a resonant Peak" (03:47.159–03:54.200) |
| **Echo** | Espaço na percussão | "some Echo" (03:54.200–03:56.639) |
| **Amp** | "bite" — saturação/drive de amp no sampler | "an amp and of course a a phaser" (03:56.640–04:00.159); "just to give a little bit more bite" (02:30.640–02:32.640) |
| **Phaser** | "extra ear candy" na percussão | "a phaser for extra ear candy" (03:59.200–04:15.639) |
| **Delay** | Só no hi-hat aberto, **com corte de graves** | "just routed it to a little bit of delay and acute out the low end" (04:40.440–04:47.550) |
| **Glue Compressor** | **Mapeado no kick** — ducking do ruído contra o bumbo | "of course a glue compressor mapped to the kick" (02:19.640–02:22.360) |
| **Essential Noises** (sample pack, 359 one-shots/loops) | Fonte de todas as amostras; nasce de Noise Plethora + Rossum Evolution + ADDAC 603 + Desmodus Versio + Basimilus Iteritas Alter, processado em Culture Vulture / Mackie 1604 / Tegeler Creme / SSL Fusion / Dangerous Bax / Convert AD | Descrição oficial lida; **não** aparece na fala |

**Nenhum plugin de terceiros é mencionado.** O vídeo **não cita** ANA 2, VELA, SideKick, Kick 3 nem Bitwig — não há
dependência dessas ferramentas e nada precisa de equivalente. A dependência real é de **conteúdo**: o pack pago.
Isso não sobrevive à tradução e precisa ser substituído (ver seção seguinte).

## Rotas equivalentes sem o pack: Serum 2, Diva, Vital, Massive X, Surge XT, Kontakt 8 e Live 12 nativo

O vídeo depende de **dois** insumos: amostras de ruído e devices stock do Live. Sem o pack, a técnica sobrevive
porque ela é sobre **cortar, filtrar e modular ruído**, não sobre as amostras específicas. Rota: gerar/renderizar
um banco próprio de one-shots de ruído e processá-los com o que já existe.

| Etapa no vídeo (timestamp) | Rota exata | Alternativa | Observação |
|---|---|---|---|
| Recorte curto de uma amostra de ruído (01:24.600; 03:30.799) | **Simpler**: importar o one-shot, `Slicing/Trim` no primeiro 5–20 ms para o clique de hat; recorte maior (100–400 ms) para percussão | **Serum 2**: slot **Noise** (índice 3, `noise_type` White/Pink/Brown/Geiger) renderizado a áudio e reimportado; ou `sample_playback_source` (SampleOsc) com `sample_loop='off'` para one-shot | Fonte de ruído crua não falta: Serum 2, Vital e Surge XT têm oscilador de ruído; o custo é **curar** os recortes |
| LFO → **Attack/Decay** do envelope (02:06.759–02:19.630; 03:34.640–03:39.000) | **Serum 2**: `mod_routes` com `source='lfo0'` e `destination='env0.attack'` / `'env0.decay'` — o schema do gerador lista *envelope attack/decay/sustain/release* como destinos válidos de modulação | **Sampler** do Live (LFO com destino em envelope auxiliar — **confirmar o destino na UI, NÃO VERIFICADO na sessão original**); ou gerar 3–4 takes com ataques diferentes e alternar por velocity | É a operação mais importante do vídeo e a única que **não** é automação de clip: a variação acontece **por nota**, sem desenhar nada |
| Cortar tudo até 1 kHz (02:49.360) | **Auto Filter** high-pass em ~1 kHz, ou **EQ Eight** HP; no Serum 2: `filters` `highpass_24` com `cutoff` equivalente, ou `warp_mode='filter_hpf'` | Vital/Surge XT/Massive X: HP interno; Kontakt 8: filtro do instrumento | O vídeo diz **1K** para uma fonte que tinha muito sub. Referência de piso em psytech minimal: **≥300 Hz** (textura) e **≥1 kHz** (hats/percussão) |
| Corpus **tube mode** (02:53.400–02:58.760) | **Corpus** (Live, stock) em modo Tube, ressonador afinado na tônica/graça da track (ex.: C#/G#/F#) | **Serum 2**: `filter type='comb'` com `var` ajustado (ressonância física), ou `warp_mode='filter_lpf'` com ressonância alta; **Surge XT**: comb filter | Corpus aparece em receitas de "pad metálico de madeira". Afinar a ressonância evita que o pico caia entre notas |
| Auto Filter com pico ~800 Hz e Q alto (03:47.159–03:54.200) | **Auto Filter** band-pass, Frequency ~800 Hz, Resonance moderada | **Serum 2** `bandpass_12/24` + `resonance`; **Vital** band-pass | 800 Hz cai dentro do vale típico de médios (300–1.200 Hz) que o set de referência mede carente |
| Echo + Amp + Phaser (03:54.200–04:15.639) | **Echo** (delay com filtro), **Amp** ou **Drive** do Auto Filter / `warp_mode='soft_clip'` no Serum 2, **Phaser** do Live | Vital/Surge XT phaser; Shifter do Live (mais extremo) | Phaser é o device de maior risco de brilho metálico — usar raso e lento |
| Delay com corte de graves (04:40.440–04:47.550) | **Delay** do Live com **Low Cut** alto, ou **Echo** com filtro HP no retorno | Qualquer delay com filtro no feedback | O corte de graves no delay é o gesto que impede o eco de engordar o sub |
| Glue Compressor **mapeado no kick** (02:19.640–02:22.360) | **Compressor** do Live com **sidechain** recebendo o canal do kick (o Glue Compressor do Live **não** tem entrada de sidechain externa — `INFERÊNCIA`, não verificado na UI na sessão original) | Ducking por envelope/volume shaper disparado pelo kick; no Serum 2 não há sidechain externo | O que importa é a **função**: o ruído abaixa quando o bumbo bate. É o que protege a pressão do sub |
| "Click" do início da amostra como hat fechado (04:29.680–04:35.479) | **Simpler** com início no primeiro sample e `Length`/`Sustain` em ~5–15 ms; sem loop | **Serum 2** SampleOsc com envelope `decay` de 10–30 ms | É o truque mais barato do vídeo: um clique já existe dentro de qualquer amostra de ruído |
| Trilha "FX / four bar thing" mais molhada que o original (04:47.560–05:01.590) | **Echo/Hybrid Reverb** em retorno, disparado a cada 4 compassos (16 beats @128 = 7,5 s) | Qualquer reverb/delay em send | O vídeo não diz qual efeito nem o wet; sabe-se só que o original era "a lot more more dry than this" |

**Ressalva de honestidade sobre os devices:** Corpus, Auto Filter, Phaser, Glue Compressor, Compressor, Delay e Amp
são **stock do Live 12** (Suite), mas não estavam na lista explícita de arsenal do levantamento original.
**NÃO VERIFICADO na sessão original.**

**Ressalva sobre o sampler:** o vídeo **nunca nomeia** o device que toca as amostras. Ele só diz "the track" e
"this little hidden menu". Toda atribuição a Simpler/Sampler é do estudo, marcada `INFERÊNCIA`.

## Aplicação por função (kick, sub, baixo/rolling, hats/shaker, percussão de resposta, madeira, stab, subida, atmosfera)

Contexto de referência citado no levantamento original: um set de trabalho medido mostrou o meio carente
(300–1.200 Hz e 1.200–4.000 Hz abaixo da média de 6 referências externas), low-end **mono**, groove com
subdivisões deslocadas (~+9,4 ms de deslocamento intencional) e **densidade de onsets já acima do teto interno**
(7,57 contra 6,99 picos/s). Consequência dura: **o ruído entra substituindo eventos, não somando**.

Aritmética útil do grid (a 128 BPM um beat = 468,75 ms; um deslocamento de 0,25→0,27 é +9,4 ms) — dentro da faixa
segura de 5–20 ms e **abaixo** do limiar de percepção típico para hats (~19–24 ms). Qualquer ataque mais lento
que isso empurra o onset percebido para perto do limiar e **desmancha a intenção** do groove.

| Função | Usar? | Como aplicar | Cuidado |
|---|---|---|---|
| **Kick** | Não | O kick continua sendo o 909 + filtro do projeto; nada de ruído nele. Só a **função** do "glue compressor mapped to the kick" se aproveita: as trilhas de ruído são **duckadas pelo kick** | Não colocar o pico ressonante de 800 Hz no kick — ele já carrega o corpo |
| **Sub** | **Nunca** | Todo one-shot de ruído entra com **HP ≥120 Hz** (ideal 1 kHz em hats/perc); nenhum ruído vai para o canal de sub | O vídeo mostra o risco na prática: a amostra "tonal high" tinha *"a lot of sub stuff going on I didn't want that"* (02:43.879–02:49.350). O pack é processado por Culture Vulture/SSL — pode trazer grave escondido. Auditar cada recorte antes de entrar |
| **Baixo/rolling** | Não | Não somar ruído ao rolling; se precisar de "tick", ele é camada separada, HP ≥1 kHz, ducked pelo kick | Ruído de banda larga mascara o groove deslocado do rolling, que é a assinatura do motor |
| **Hats/shaker** | **Sim — uso primário** | (a) Clique do início da amostra = hat fechado; (b) outra fração = hat aberto; (c) delay **com low cut** só no aberto; (d) Auto Filter ~800 Hz + Q moderado para o hat soar **oco/madeira**, não metálico | Limitar o topo: **LP ~7–8 kHz** no hat de ruído. Se o set de referência já está acima da régua de presença (2–4 kHz), o buraco é de **ar** (8 kHz+), não de 2–4 kHz; subir 2–4 kHz piora o índice |
| **Percussão de resposta** | **Sim — o melhor encaixe** | Recorte de 100–400 ms + **LFO no attack/decay** para cada resposta entrar diferente. Posicionar no **último 16º antes do pulso** e nos vácuos de sub | A variação de attack **não pode** cair na camada que carrega o microdeslocamento do groove — ali o ataque deve ser idêntico nota a nota. Densidade: **substituir** um evento existente, nunca somar |
| **Madeira** | Parcial | Corpus tube afinado na tônica por baixo de uma madeira já existente, para "resina" no médio | A madeira vem do Kontakt 8; o ruído é **verniz**, não substituto. HP ≥300 Hz |
| **Stab** | Não | O stab mantém o ataque e a afinação; phaser nele borra o fundamental | Phaser é efeito de **percussão de ruído**, não de stab |
| **Subida** | Não ensinado | O vídeo não tem riser nem build; o LFO-no-attack poderia fazer uma textura "respirar", mas isso é extensão do estudo | Não atribuir ao vídeo |
| **Atmosfera** | Parcial, com correção obrigatória | A trilha "texture" é a única que ele deixa **sem EQ** — e é o gesto certo **só acima do piso**: HP 120–300 Hz e o resto intacto | Não copiar o "sem EQ" literalmente: boa prática manda HP 120–300 Hz em atmosfera. O que se preserva é o **espectro completo acima de 300 Hz**, não o grave |

### Onde encaixar

- **Hats**: manter os eventos do groove existente e apenas **trocar o timbre** pelo clique de ruído. Não
  acrescentar um hat novo no mesmo 16º — a densidade já está no teto.
- **Percussão de resposta**: último 16º do compasso e nos vácuos de sub — uma resposta seca por vácuo.
- **Textura**: contínua, mas entra em pontos de arranjo (fim de frases/fronteiras); não precisa de grid, precisa
  de HP.
- **Ruído "four bar"**: a cada 4 compassos = **7,5 s** a 128 BPM; um evento por ciclo, em send, para não sujar o
  groove.

### Regras para não engordar o sub nem criar brilho metálico

1. **HP antes de qualquer coisa.** O primeiro gesto do vídeo é cortar o grave até 1 kHz. Todo one-shot de ruído
   passa por HP (120 Hz mínimo; 300 Hz textura; 1 kHz hats/percussão) **antes** de entrar no motor.
2. **Nada de ruído branco no topo.** White noise + Q alto + phaser é a receita clássica de brilho metálico. Para
   perfil escuro: **pink/brown**, Q moderado, **LP 7–8 kHz**, phaser raso e lento.
3. **Mirar o vale certo:** o pico ressonante deve morar em **700–900 Hz** (dentro do vale de 300–1.200 Hz). Não
   estacionar em 2–4 kHz, que já tende a estar acima da régua de presença.
4. **Deixar o 1,2–4 kHz vir do timbre, não do nível.** A ressonância em 800 Hz e o Corpus tube geram harmônicos
   que preenchem a banda sem subir fader — e sem criar pico metálico.
5. **Mono abaixo de 120 Hz.** Ruído é estéreo por natureza: width só acima de ~300 Hz; conferir a soma mono. O
   low-end não se negocia.
6. **Ataque idêntico onde há microdeslocamento.** LFO no attack só na resposta e no hat; nunca na camada que
   define o deslocamento do groove. O deslocamento de ~9,4 ms é a assinatura; um ataque mais lento o apaga.
7. **Substituir, não somar.** Se a densidade de transientes já estiver no teto, cada ruído novo remove um evento
   velho.

## Prioridade e esforço

**Prioridade: média** (a curva marca **P1**; a leitura abaixo explica por que não sobe para alta). O conceito é
diretamente reaproveitável — o canal de ruído costuma estar mudo no motor e o vídeo ataca exatamente as duas
bandas que faltam (300–1.200 e 1.200–4.000) sem tocar no sub —, mas o material é um **demo de pack**: 6 minutos,
6 trilhas, uma frase de decisão cada, e **dois únicos números** em toda a legenda (1K e 800 Hz). Ele entrega
vocabulário e um gesto, não um método fechado.

**Esforço: médio.** O processamento é barato (devices stock, nada exótico) e o desenho de LFO→attack já é
possível no schema do Serum 2. O que consome tempo é o insumo: **não há o pack**, então é preciso montar um
pequeno banco de one-shots de ruído (render do oscilador de ruído do Serum 2/Vital/Surge XT, foley, vinyl) e
**auditar grave** em cada um. Riscos: brilho metálico (white + Q + phaser), sub engordado (amostra de pack
processada com grave escondido) e densidade estourada (somar em vez de substituir).

## Trechos de prova (legenda literal, timestamps do VTT)

**1. A textura fica sem EQ de propósito — espectro completo (00:01:35.320–00:01:43.749):**

> 00:01:35.320 and there isn't even any EQ nothing I
> 00:01:38.600 wanted the complete frequency spectrum
> 00:01:41.320 of this one next up we have this tonal

**2. O grave sai, a ressonância volta: corta até 1 kHz e põe Corpus em modo tube (00:02:46.599–00:02:58.760):**

> 00:02:46.599 sub stuff going on I didn't want that so
> 00:02:49.360 I filtered everything out up until 1K
> 00:02:53.400 and then I put a corpus on the track in
> 00:02:56.519 tube
> 00:02:58.760 mode here is without it's a subtle

**3. O núcleo percussivo: recorte minúsculo + LFO no attack + pico ressonante em ~800 Hz (00:03:30.799–00:04:15.639):**

> 00:03:30.799 took a really really small portion of
> 00:03:33.519 the
> 00:03:34.640 sample and then an LFO mapped to the
> 00:03:39.000 attack so we have a bit of variation
> 00:03:41.200 going
> 00:03:47.159 on after that an autof filter with the
> 00:03:51.239 frequency around 800 HZ and quite a
> 00:03:54.200 resonant Peak some Echo an amp and of
> 00:03:59.200 course a a phaser for extra ear
> 00:04:07.690 [Applause]
> 00:04:15.639 candy and you can hear the LFO really

*(O `[Applause]` entre "ear" e "candy" é ruído de legenda automática, não fala. "autof filter" = Auto Filter.)*

## Limites: o que o vídeo NÃO diz

- **Não dá valores** de LFO (rate/depth/forma), Q do filtro, ratio/attack do compressor, tempo/feedback do delay,
  rate do phaser nem wet de nada. Só 1 kHz e 800 Hz.
- **Não nomeia o sampler** nem explica como o LFO é roteado no attack/decay; "hidden menu" fica sem explicação.
- **Não explica a programação rítmica**: só *"I just placed some notes where I found them fitting"* (03:25.280–03:30.799).
  Não há grade, swing nem deslocamento declarado.
- **Não fala de mono, ganho, fase ou soma** — nada de gestão de low-end. A parte de mono é boa prática do estudo,
  não do vídeo.
- **Não ensina a fabricar as amostras**: a cadeia de hardware está só na descrição, não na fala.
- O vídeo é **promoção de pack pago**; o que ele entrega de técnica é o que se extrai das 6 passagens.

## Correções de ASR (para não inventar a partir do erro)

"a button effects" = *Ableton effects* (00:42.480) · "autof filter" = *Auto Filter* (03:47.159) · "corpus" = *Corpus*
(02:53.400) · "acute out the low end" = *a cut out the low end* (04:43.680) · "Hiatt" = *hi-hat* (04:33.880) ·
"perks" = *percs* (03:16.720) · "closed higher track" = *closed hi-hat track* (04:21.880) · "99 hats" = *909 hats*
(05:19.720) · "CE oon" = nome de pessoa que a legenda não resolve (00:15.200) — **não identificado**.

## Fontes

- Legenda automática EN do vídeo e descrição oficial do canal.
- Números do set de referência (densidade de onsets 7,57/6,99, microtiming 5–20 ms, JND de drums ~19–24 ms,
  régua de topo 8k+, groove deslocado, vale 300–4.000 Hz): dados do levantamento original que contratou a
  dissecação, não do vídeo e não re-medidos.
