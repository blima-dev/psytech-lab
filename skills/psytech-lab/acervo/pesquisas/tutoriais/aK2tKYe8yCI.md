# Hypnotic Techno Drums from Scratch (Stock Ableton Effects Only)

> **Ficha:** canal *Hypnotic Techno Production* · id `aK2tKYe8yCI` · legenda automática EN obtida e lida
> (652 falas úteis) · duração ≈ 43:19 · **BPM declarado no vídeo: 135** (00:00:52) · tema: groove de bateria.
> Toda afirmação técnica abaixo tem timestamp da legenda. O que a legenda não diz está marcado como
> `NÃO VERIFICADO` ou `NÃO COBERTO`. Áudio não escutado — análise só da legenda.

## Técnica ensinada (2-4 frases)

O groove é construído empilhando **camadas curtas e afinadas entre si** — kick curto afinado em F#/G
(00:00:40, 00:02:53), tom afinado no mesmo G1 do kick (00:08:46) — e cada camada é pensada como
**pergunta-resposta** com a anterior (00:06:41, 00:14:06, 00:42:28). O momentum vem dos hats: variação de
**velocity** e ghost notes deliberadamente baixas (00:15:01, 00:15:48) mais um hat fechado em **polimetria de 5
semicolcheias** com curva de dinâmica desenhada (00:16:54, 00:17:03). Movimento é criado por **modulação lenta**
— LFO no *scan* do granulado (00:05:31), LFO no feedback (00:28:55), notch lento (00:25:45), Auto Pan + Phaser
(00:17:38) — e não por mais camadas; tudo é **impresso em áudio** quando o padrão aleatório agrada (00:13:05). O
critério final declarado é corporal, não métrico: "Groove has to engage the body" (00:42:56).

## Ferramenta usada no vídeo (plugin/stock)

| Ferramenta | Para quê no vídeo | Timestamp |
|---|---|---|
| Drum Rack + **Simpler** (One-Shot → **Classic**) | kick, toms, hats; Classic + release/sustain baixos = só a parte "clicky" | 00:00:29, 00:01:00, 00:17:24 |
| **Limiter** (stock) | aparar o clique pontudo do kick sem perder peso ("so I don't lose the weight") | 00:02:00–00:02:19 |
| **Operator** | baixo de **uma nota** com *pitch envelope em loop* | 00:03:18–00:03:26 |
| **Granulator III** (+ LFO no *scan*, randomness, grain size, shape) | textura/crackle de fundo com movimento | 00:04:27–00:06:01 |
| **Compressor** (stock) | "a bit of pumping" na textura | 00:06:05–00:06:19 |
| **Echo** (e Echo + reverb) | tom (00:08:48), hat só a cada 2 compassos (00:20:10); desligado em 00:13:53 | 00:08:48, 00:20:10 |
| **MDD snake** | sequenciador MIDI que ele randomiza e depois **grava em áudio** ("printing the sound already") | 00:12:14–00:13:16 |
| **Auto Pan** + **Phaser** (lentos) | movimento do hat fechado; automação gravada em áudio | 00:17:38–00:18:38 |
| **Shifter** | deixar o wood block "more techno" | 00:24:39 |
| **Notch** (lento) | efeito psicodélico "learned from Rose the techno producer" | 00:25:37–00:25:53 |
| **Chance** por nota | percussão aparecer "every here and there" | 00:28:29–00:28:47 |
| **LFO** (M4L) no **feedback** | cauda longa de snare criando *phasing* | 00:28:55–00:29:11 |
| **Grain Delay** (+ feedback) e **Echo** com pitch modulado | tratamento de sample gravado | 00:31:11–00:31:46 |
| **Warp** Beats / **Transient** + clip gain | usar o warp como *gate* de loop barulhento | 00:33:02–00:33:11 |
| **Reverb** | espaço no loop | 00:33:57 |
| **G Voc** (nome literal da legenda) | vocal granular, gravado em takes; LFO → transposição | 00:35:37, 00:36:25, 00:37:31 |
| **Warp** em 16th + *Length 3* | textura de topo em polimetria | 00:38:53–00:39:28 |

**Ressalvas de fidelidade:**
- O título diz "Stock Ableton Effects Only", mas a legenda cita **"MDD snake"** (00:12:16) e **"G Voc"**
  (00:35:37) sem dizer que são stock. Se são stock ou M4L de terceiros: `NÃO VERIFICADO` — o vídeo não afirma.
- **"8 decibels"** como "good reference point for a kick" (00:01:48) aparece **sem unidade de referência** (não
  diz se é pico, LUFS ou diferença). Não traduzir como meta de loudness: `NÃO VERIFICADO`.
- "media rack / media track" (00:04:17) é ambíguo na legenda automática; o que dá para afirmar é que ele carrega
  **Granulator III** num rack/track novo (00:04:27).
- Nenhuma menção no vídeo a ANA 2, VELA, SideKick, Kick 3, Bitwig, Serum, Diva, Vital ou Massive (busca na
  legenda = 0 para todos). O vídeo não depende de plugin pago além dos citados na tabela.

## Tradução para ferramentas Live 12 / Serum 2

| Do vídeo | Conceito | Equivalente (Live 12 / Serum 2) | Observação |
|---|---|---|---|
| Simpler One-Shot → **Classic** + release/sustain baixos | cortar a cauda para sobrar só o transiente | **Simpler** (Live 12) | direto, sem plugin novo |
| **Limiter** no kick | segurar pico do clique sem EQ que engorda | **Limiter** do Live | com low-end mono (prática comum no estilo), o limiter não abre grave, só contém pico |
| Kick afinado em F#/G | afinar o kick na tônica e checar a frequência na tela | Simpler (display) afinado **na tônica do projeto** | 00:02:53 avisa: grave demais "will sound very muddy" |
| Bass = 1 nota Operator + **pitch envelope em loop** | rolling sem escrever mais notas | **Operator** (Live nativo) ou **Serum 2** (ENV/LFO → pitch, envelope em loop) | achado mais útil do vídeo para baixo rolling |
| **Granulator III** + LFO no scan | textura com movimento interno | **Serum 2 GranularOsc** (density/grain length/random pitch-pan) ou **Sampler/Simpler + LFO**; Granulator III é M4L que vem com o Live 12 Suite | mesmo conceito, outro motor |
| **MDD snake** (randomiza MIDI) | gerar padrão que você não escreveria e **congelar em áudio** | escrever/randomizar com as **MIDI Tools do Live 12** ou à mão, depois *freeze/flatten* | o que importa é o fluxo "gerar → imprimir" |
| **Chance** por nota | percussão esporádica, não repetitiva | **Chance** da nota no clip do Live 12 | direto |
| **LFO (M4L) → feedback** | cauda que faseia sozinha | **LFO** (M4L) no feedback do Echo/Delay; no Serum 2, mod route LFO → FX | cria movimento sem subir nível |
| **Notch** lento | psicodelia por subtração | **Auto Filter (notch)** com LFO lento, ou EQ Eight automatizado | subtrai, não engorda |
| **Shifter** | tirar o wood block do "sample cru" | **Shifter** (Live nativo) | direto |
| **Grain Delay**, Echo com pitch modulado | textura e desafinação lenta | **Grain Delay** + **Echo** (stock) | direto |
| **Warp** Beats/Transient como gate | cortar excesso de ruído sem fader | warp do clip no Live 12 | direto |
| **G Voc** no vocal | granular/vocoder em sample de voz | **Serum 2 GranularOsc** com sample vocal, ou Simpler granular + Shifter | nome do device `NÃO VERIFICADO`; conceito é granular |
| Reverb / Compressor | espaço e pumping | **Hybrid Reverb** / Compressor | direto |

Conclusão de tradução: **traduzível = true**. O núcleo (kick curto, hats com velocity/ghost/polimetria, chance,
notch, granular, warp-gate) não depende de plugin pago; só o "MDD snake" e o "G Voc" precisam de substituto
conceitual.

## Aplicação por função (princípios)

**Contexto de auditoria (set de referência medido contra a média de 6 referências do estilo):** 300–1.200 Hz
estava **−4,83 dB** e 1.200–4.000 Hz **−5,76 dB**; low-end **mono**; groove com subdivisões deslocadas fora do
grid, a preservar. A 128 BPM um compasso = 1.875 s e uma semicolcheia = **117,2 ms** (o vídeo, a 135 BPM, tem
111,1 ms — 5,5% mais apertado).

**Onde o vídeo NÃO serve de receita literal:** o alvo tonal dele é F#/G (00:02:53) — traduzir a *regra* (afinar
na tônica do próprio projeto), não os valores; o BPM é 135 (00:00:52) — ajustar os comprimentos de cauda ao BPM
do projeto.

- **Kick.** Simpler em **Classic** com release/sustain baixos (00:17:24–00:17:33), cauda curta porque "kicks
  shouldn't be that long" a tempos rápidos (00:00:40–00:00:49), afinado **na tônica** (o vídeo usa o display de
  frequência em 00:08:36). Usar **Limiter** para aparar o clique em vez de EQ (00:02:00–00:02:19) — EQ aqui é
  o caminho que engorda o sub. A 128 BPM há ~24 ms mais por batida que no vídeo, então a cauda pode ser um fio
  mais longa; ainda assim curta, porque com low-end mono e pressão de sub como princípio do estilo, cauda longa
  vira lama.
- **Sub.** **Não tocar.** O vídeo não tem camada de sub separada — o sub mora no próprio kick (00:01:54 "a bit
  more sub"). Qualquer ideia desta página entra acima do sub; nada de boost abaixo de ~120 Hz.
- **Baixo/rolling.** O achado mais útil: **uma nota só** em Operator com *pitch envelope em loop* (00:03:18–
  00:03:26). Manter a nota na tônica e deixar o loop do envelope criar o movimento, sem acrescentar notas —
  assim o rolling não compete com as subdivisões deslocadas do groove nem engrossa o grave. Em Serum 2, o mesmo
  com ENV/LFO → pitch em modo loop.
- **Hats/shaker.** Maior retorno quando o mix mostra déficit em 1,2–4 kHz. Copiar: variação de **velocity**
  (00:15:01) e **ghost notes realmente baixas** — o vídeo chama de "splashing" e diz que elas "add the groove,
  emphasize this part of the bar" (00:15:48–00:15:54); hat fechado em **5 semicolcheias** (00:16:54) com curva
  de dinâmica desenhada (00:17:03), no Simpler Classic só com a parte "clicky" (00:17:24); Auto Pan + Phaser
  lentos (00:17:38); Echo + reverb **só a cada 2 compassos** para não saturar (00:20:10–00:20:22). **Limite:**
  não resolver o déficit de 1,2–4 kHz subindo o fader do hat — energia de hat é majoritariamente mais alta e vira
  brilho metálico. Usar a camada de hat para ritmo/velocity e deixar o preenchimento de 1,2–4 kHz para
  madeira/shaker com corpo (ver abaixo).
- **Percussão de resposta.** É a espinha do método: "question-answer" no grave (00:06:41) e entre samples de
  hat (00:14:06). Copiar a receita: drum rack com **muitos** candidatos carregados para escolher rápido
  (00:06:52–00:07:10), resposta em **semicolcheias sincopadas** (00:07:18), **levemente fora do grid**
  (00:07:37) e **afinada no kick** (00:08:46) + echo (00:08:48). A resposta entra nos buracos das subdivisões
  deslocadas do groove, afinada na tônica e com corpo em 300–1.200 Hz (onde costuma faltar corpo). **Não**
  deslocar os anchors do groove — o fora-do-grid do vídeo vale só para a camada de resposta.
- **Madeira.** O vídeo procura wood block explicitamente (00:23:01–00:23:06), usa **loops de 2 ou 4 compassos**
  com pequenas variações (00:23:56–00:24:13), passa **Shifter** para "make it more techno" (00:24:39) e um
  **notch lento** para psicodelia (00:25:45). É o encaixe mais direto no corpo de 300–1.200 Hz: madeira
  com corpo, sem brilho. Aplicar variação a cada 2 compassos para não virar loop morto.
- **Stab.** `NÃO COBERTO` — ele diz que está "missing some lead, missing… some second character" e que isso
  "will be the video number two" (00:41:05–00:41:18). Não inventar receita de stab a partir daqui.
- **Subida.** `NÃO COBERTO` — nenhuma menção a riser, sweep ou transição na legenda.
- **Atmosfera.** Granulator III com LFO no scan + randomness + grain size (00:04:27–00:06:01) e compressor para
  "pumping" (00:06:05–00:06:19); warp Beats/Transient usado como **gate** para domar ruído (00:33:02–00:33:11);
  Grain Delay com feedback e Echo com pitch modulado (00:31:11–00:31:46). Usar como camada **fina** de
  preenchimento em 1,2–4 kHz, com high-pass para não encostar no sub e nível baixo — é cola, não é camada de
  destaque. Alternativa: Serum 2 GranularOsc com o mesmo sample.

## Prioridade e esforço

**Prioridade: média** · **Esforço: médio.**

- **Por que média e não alta:** o vídeo é um exercício longo (43 min, 135 BPM, tonalidade F#/G) e não trata do
  gargalo típico do estilo (sub mono + meio 1,2–4 kHz carente); ele entrega *método de empilhamento*, não
  presets. Boa parte da técnica (kick curto, ghost notes, pergunta-resposta) é conhecimento consolidado do
  estilo.
- **Por que não baixa:** duas ideias são diretamente acionáveis e baratas — **Chance** nas respostas
  (00:28:29) e **hat fechado em 5 semicolcheias** (00:16:54) — e a camada de **madeira** é justamente onde
  costuma faltar corpo (300–1.200 Hz).

| Sub-técnica | Prioridade | Esforço | Motivo curto |
|---|---|---|---|
| Ghost notes + velocity nos hats | alta | baixo | ataca o meio 1,2–4k por dinâmica, sem EQ |
| Polimetria 5 semicolcheias no hat fechado | alta | baixo | hipnose com 1 clip; 16 e 5 são coprimos → realinha a cada 5 compassos |
| Baixo de 1 nota com pitch envelope em loop | alta | baixo | rolling sem mais notas, preserva o groove |
| Chance nas percussões de resposta | média | baixo | variação sem reescrever padrão |
| Madeira com Shifter + notch lento | média | médio | preenche 300–1.2k, mas exige escolher sample e automatizar |
| Granulator/textura granular | média | médio | camada fina; risco de mascarar o médio |
| Loop de hat a cada 2 compassos com Echo+Reverb | baixa | médio | ganho pequeno num motor curto |
| G Voc / vocal granular | baixa | alto | fora do escopo de um motor básico |
| Stab / subida | — | — | `NÃO COBERTO` pelo vídeo |

## Trechos de prova

1. **[00:00:40]** "So the the good rule of the thumb for hypnotic techno kick is that it shouldn't be that
   long." — regra do kick curto (a repetição "the the" é da legenda automática).
2. **[00:02:53]** "This one is in G. G is really a good frequency for a kick. Don't go too low cuz it will
   sound very muddy on most of the speakers." — alvo de afinação e limite de graves.
3. **[00:15:48]** "They're like splashing. They're really … low in volume. This way they kind of like add the
   groove, emphasize this part of the bar." — ghost notes baixas como ferramenta de groove. (A elisão cobre um
   "uh" que a legenda rolante repete na quebra de cue; o resto é literal.)
4. **[00:16:54]** "Simple thing, let's do 5 16th. Yeah, so a bit of poly meter going. This works really well in
   the hypnotic techno." — polimetria de 5 semicolcheias no hat fechado.
5. **[00:25:41]** "thing I've learned from Rose the techno producer. So, he's using a lot of notch filters." —
   notch lento como movimento psicodélico.
6. **[00:42:56]** "Groove has to engage the body. That's the basics of dance music. That's the basics of
   techno." — critério final declarado.
