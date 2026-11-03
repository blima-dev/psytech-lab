# HOW TO MAKE PSYTECH By Wachter & Böhm [Project Walkthrough]

> id `TwZk8Gcyl1E` · canal **Vision Serpent** · apresentadores **Wachter & Böhm** · faixa **"Mothership"** · **16:29**
> · descrição: teaser do walkthrough completo ("Watch full-length (1,5hour) on Patreon").
> Legenda automática EN do vídeo obtida e lida (102,28 KiB; 3.136 linhas; **689 blocos úteis** após remover
> cabeçalhos, tags `<c>`, timestamps isolados e duplicatas consecutivas). **temLegenda=true.**
> Duração conferida com `yt-dlp --print "%(duration_string)s"`: **16:29**; a última entrada da legenda é
> `00:16:24.531` — o corte público está transcrito por inteiro.
>
> **Escopo real do vídeo.** O YouTube publica só o começo do walkthrough; a versão de 1,5 h está no Patreon
> (descrição). Nos 16 minutos eles abrem **apenas o grupo de graves**: grupo de kick (duas camadas), grupo de baixo
> (camada low impressa em áudio + camada high em MIDI), processamento de grupo e as checagens de afinação e fase.
> Aos 16:17 dizem *"and then we get into the next group"* e o vídeo acaba. **Não há hats/shaker, percussão de
> resposta, madeira, stab, subida, atmosfera, arranjo dos dois minutos nem BPM declarado** (grep por "bpm", "128",
> "tempo": zero ocorrências). Todo uso de um princípio do vídeo nessas funções está marcado `INFERÊNCIA`.
>
> **Convenção de evidência:** trecho entre aspas + timestamp = legenda literal (`VERIFICADO` na legenda). Aplicação
> ao material de referência = `INFERÊNCIA`. O vídeo não conhece a tônica C#, o frígio nem o groove deslocado
> (.27/.77) do material de referência.

## Técnica ensinada (2-4 frases)

O low end nasce de **quatro camadas em dois subgrupos**: kick com duas camadas ("main side kick" + "punch layer",
02:48–03:01) e baixo com uma camada **low impressa em áudio** e uma camada **high em MIDI** (04:57–05:09;
08:55–08:59). Antes de montar, eles acham a **fundamental do kick** com boost de EQ + analisador e escolhem a
tonalidade que contém aquela nota — kick em **A**, faixa em **E menor ou E frígio** ("not sure", 03:52–04:16) —
porque mesmo um grave muito baixo "always has like a a note that it's playing" (04:27–04:31). Como as duas camadas
de baixo tocam a mesma nota, eles **invertem a fase de uma no Utility** e escolhem de ouvido a que soma mais
pressão (06:52–07:51), confirmando no analisador que a energia do fundamental e dos overtones não cai
(07:55–08:20). O kick não abre espaço no baixo inteiro: um **Track Spacer** faz o duck **só nas frequências
baixas**, deixando a camada high "fresher" e "not such an obvious side chain" (12:23–13:17); a camada low leva um
duck básico (08:28–08:44) e o grupo fecha com drum bus + compressor de ataque lento para não perder o punch do kick
(13:59–14:26).

## Ferramenta usada no vídeo (plugin/stock)

| Ferramenta | Papel no vídeo | Prova literal (timestamp) |
|---|---|---|
| **Ableton Live** (DAW) | DAW do projeto; o nome aparece uma vez na fala e nas hashtags da descrição (`#ableton`) | "this is the low extender preset from Ableton" (00:14:16.720–00:14:19.070) |
| **EQ** (stock; `INFERÊNCIA`: EQ Eight) | Boost de agudos no grupo do kick; checagem da nota fundamental; limpeza do grupo de baixo; corte de graves na camada high; escuta só do grave para balancear kick×baixo | "on the group, we have an EQ to boost the highs a little bit" (00:03:14.040–00:03:16.030); "an EQ to check uh our root note" (00:03:41.320–00:03:50.552); "we have an EQ and we filter out all the high frequencies" (00:15:17.720–00:15:20.070) |
| **Utility** (stock) | Inversão de fase de uma das camadas de baixo | "with the utility is we flipped the phase of uh this track" (00:06:54–00:07:04); "if this utility is turned off, you're losing um some pressure" (00:07:17–00:07:24) |
| **Saturator** (stock) | Camada low "bigger and warmer"; camada high "a bit more character"; segundo estágio para "crunchy" | "we have a saturator. Make it a little bit bigger and warmer" (00:06:42–00:06:48); "in the first uh step, put on a saturator ... give it a bit more character" (00:10:04–00:10:13); "then we put on a saturator again ... to really make it like crunchy" (00:10:38–00:10:45) |
| **Multiband compressor** (stock; `INFERÊNCIA`: Multiband Dynamics) | Punch da camada high | "we have this multiband compressor on here. Make sure it has a lot of punch" (00:10:13.280–00:10:22) |
| **Redux** (stock) | Bitcrush/"psychedelic" na camada high | "stronger than the crunch happens with the Redux. Kind of adds a bit more of this psychedelic feeling" (00:10:48.160–00:10:57) |
| **Delay** (stock) | "subtle delay" para dar groove | "then we have a subtle delay ... It's really subtle ... it just gives it a bit more groove" (00:11:00.080–00:11:15) |
| **Drum bus** (nome dito; device não confirmado) | Engordar e colar o grupo | "the final step would be the drum bus. So, just make it fat ... and glue everything together" (00:11:16.600–00:11:25); "We have a drumbus. Make it a bit fatter again" (00:13:59–00:14:04) |
| **Compressor** (stock; device não nomeado) | Cola do grupo com ataque lento, sem perder o punch | "this is the low extender preset from Ableton. Just uh make sure that you use a slow attack so the kick can cut through" (00:14:16.720–00:14:26); "you don't put too much of the threshold cuz you'll lose the punch" (00:14:31–00:14:44) |
| **Auto Pan** (stock) | Citado como o sidechain do grupo | "this final step is a sidechain. So, we we just use the auto pan plugin" (00:11:25–00:11:31); "for chaining, if you align the phase" (00:11:33–00:11:38) |
| **SPAN** (analisador de terceiros; só o nome é dito) | Ver cancelamento de fase no fundamental e nos overtones | "a frequency analyzer like span ... This is the root note. And then if I turn this off ... we're losing power in this specific frequency" (00:07:55–00:08:20) |
| **Track Spacer** (plugin de terceiros; só o nome é dito) | Sidechain **limitado em frequência**: duck só nos graves | "here we have plug-in called Track Spacer ... basically another side chain ... only down here" (00:12:23–00:12:49); "not the entire bass gets ducked when the kick hits" (00:12:52–00:12:56) |

**Não nomeados no vídeo — não inventar:** a fonte do kick (nenhum sample ou sintetizador é nomeado; só "main side
kick" e "punch layer"), o sintetizador do baixo ("So we have a basic bass sound like this. Saw wave in this case",
00:05:30.840–00:05:32.990 — o nome nunca é dito), o modelo exato do EQ e do compressor, e o conteúdo do preset
"low extender" (nome citado, device não). A legenda automática escreve "main side kick" (00:02:52.800) e "still
bass" (00:09:56.600) — nenhuma das duas expressões é técnica o suficiente para virar instrução. Nenhuma menção a
Serum, Diva, Vital, Kick 3, SideKick, VELA, ANA 2 ou Bitwig (grep: zero).

## Tradução para um arsenal compatível: Serum 2 (tem GranularOsc nativo), Diva, Vital, Massive X, Surge XT, Kontakt 8 (Rubber Bridge Guitar, LOOP GARDEN, Ethereal Earth, Vintage Organs), Live 12 nativo (Simpler/Sampler/Grain, Operator, Echo, Hybrid Reverb, AutoPan, Shifter). Sem ANA 2, VELA, SideKick, Kick 3, Bitwig — se o vídeo depende deles, explique o conceito equivalente.

A rota do vídeo é **quase toda stock do Live**. Só dois itens não fazem parte do stock do Live 12 — o analisador
**SPAN** e o **Track Spacer** — e **nenhum dos dois é obrigatório**: o conceito de cada um sobrevive em device
nativo. O vídeo **não depende** de ANA 2, VELA, SideKick, Kick 3 nem Bitwig; essas ferramentas não aparecem em
nenhum momento. Tudo nesta seção é `INFERÊNCIA` de aplicação; o vídeo só nomeia o que está na tabela anterior.

| Do vídeo | Equivalente no arsenal | O que preservar |
|---|---|---|
| EQ genérico | **EQ Eight** | boost estreito no grupo do kick; corte de graves na camada high; análise de espectro |
| Utility (fase) | **Utility** | inversão de fase L/R no canal; é A/B, não regra |
| Saturator | **Saturator** | "bigger and warmer" na camada low, sempre seguido de corte de agudos |
| Multiband compressor | **Multiband Dynamics** | punch da camada high (`INFERÊNCIA` de que seja esse o device) |
| Redux | **Redux** | bitcrush; é o device que mais ameaça brilho metálico |
| Delay | **Echo** ou **Delay** | delay discreto só na camada high |
| Drum bus | **Drum Buss** | engordar/colar o grupo (`INFERÊNCIA` pelo nome e pelo contexto Ableton) |
| Compressor de cola | **Compressor** ou **Glue Compressor** | ataque lento; não há garantia de que o preset "low extender" exista na instalação de destino — recriar por ouvido |
| Auto Pan | **AutoPan** | ver ressalva abaixo: não usar para duck de banda que precisa ficar mono |
| SPAN | **Spectrum** (nativo) ou analisador do EQ Eight | ler fundamental e overtones antes/depois do flip |
| Track Spacer | **Audio Effect Rack divisor de banda + Compressor com sidechain** | duck dinâmico **só abaixo de ~150 Hz** |

### Rota nativa para o "Track Spacer" (o conceito que importa)

`INFERÊNCIA` de implementação, com devices nativos:

1. Na pista do **baixo**, criar um **Audio Effect Rack** com duas chains: **LOW** (Low-pass 24 dB em ~150 Hz) e
   **HIGH** (High-pass 24 dB em ~150 Hz).
2. Na chain **LOW**, inserir **Compressor** com **sidechain = KICK** (de preferência pré-fader), ataque curto e
   release curto o bastante para terminar antes da nota deslocada (ver "Onde exatamente no grid").
3. A chain **HIGH** fica seca. É isso que o vídeo chama de "not such an obvious side chain" (00:13:15).
4. A/B: com o rack ligado, o nível de 300 Hz–4 kHz do baixo **não deve mudar**; só a região <150 Hz deve bombear.

`NÃO VERIFICADO`: se o Compressor do Live 12 tem seção de EQ no sidechain, dá para fazer numa instância só.
Não testado. A rota do rack não depende disso e é a recomendada.

### Onde cada synth entra — e onde não entra

- **Serum 2 (o baixo de referência é Serum 2 + EQ Eight):** o vídeo descreve a camada high como "literally just a saw wave with
  this filter envelope" (00:09:39–00:09:50). Em Serum 2 isso é Osc A em saw, filtro LP24, um envelope rápido no
  cutoff, **unison 1** e mono. Não precisa de wavetable exótica nem do **GranularOsc** — o vídeo não tem conteúdo
  granular.
- **Diva:** alternativa para o pluck se o saw do Serum soar duro demais; o papel é o mesmo (saw + envelope de filtro
  curto, monofônico).
- **Vital / Massive X / Surge XT:** alternativas equivalentes. No Surge XT, **se o build tiver o efeito
  bitcrusher**, dá para fazer o papel do Redux dentro do synth em vez de na cadeia (`NÃO VERIFICADO` no
  ambiente de destino).
- **Kontakt 8 (Rubber Bridge Guitar, LOOP GARDEN, Ethereal Earth, Vintage Organs):** **sem papel neste vídeo.** Não há
  conteúdo acústico, orgânico ou de órgão nos 16 minutos.
- **Grain / Simpler / Sampler:** entram só na etapa de **imprimir o sub em áudio** (Freeze & Flatten ou uma pista em
  Resample gravando o loop), que é o equivalente nativo do "we recorded this from synth ... Press record ... you
  could also just bounce it to a new track" (00:05:11–00:05:47).
- **Hybrid Reverb / Shifter:** sem uso no vídeo. Não forçar.

## Aplicação concreta em um motor minimal de 2 minutos: por função

**Contexto medido do set de referência (fonte e alcance).** Um comparativo de 6 referências externas mediu o motor
**−4,83 dB em 300–1.200 Hz** e **−5,76 dB em 1.200–4.000 Hz**. Esses números são **relativos à energia de 60–120 Hz de
cada faixa**, medidos em estéreo, com Butterworth de 6ª ordem e fase zero, **sem soma mono**. Não são um déficit
absoluto de médio: são o médio baixo em relação ao próprio grave. O próprio diagnóstico conclui que *"o buraco mais
útil para investigar é corpo médio/presença, não adicionar sub indiscriminadamente"*. O low-end é mono por regra do
material de referência. O groove usa subdivisões deslocadas **.27/.77** e está aprovado no diagnóstico do motor.

**Estado registrado do motor de referência (diagnóstico de 26/10, não re-lido no Live):** sub = **Operator +
Saturator**, nota MIDI 25 (~34,65 Hz), ataca em .27, notas de .68 beat (.46 no quarto tempo); baixo = **Serum 2 +
EQ Eight**, notas 37/38/44/49/50, alterna .50/.77. A arquitetura do **kick** não foi inspecionada — `NÃO
VERIFICADO`.

### kick

- **O que o vídeo faz:** duas camadas ("main side kick" + "punch layer", 02:48–03:01), EQ **no grupo** para
  "boost the highs a little bit" e "make it cut through the rest of the sounds" (03:14–03:35), processamento mínimo
  na fonte (03:38).
- **No motor de referência:** o passo 1 é a checagem de afinação, não o EQ. Medir a fundamental com boost estreito no EQ
  Eight + Spectrum e comparar com as notas que o motor já usa: **C#** (34,65 / 69,30 Hz), **D** (36,71 / 73,42) e
  **G#** (51,91 / 103,83). Se cair em C#, está na tônica; em D ou G#, está na escala; fora disso (ex.: G≈49,00;
  F≈43,65, que está fora do frígio mas liberado em teste pela direção atual do material), retunar o kick ou
  aceitar a tensão de propósito. O vídeo escolheu a escala *por causa* da nota do kick,
  não o contrário (03:55–04:16) — e eles mesmos dizem "not sure" sobre ser E menor ou E frígio.
- **Por que isso importa aqui:** um registro do material de referência descreve o kick como "sample nominal 48 Hz".
  48 Hz fica ~64 cents acima de F#1 (46,25) e ~36 cents abaixo de G1 (49,00) — é rótulo, não medição. Medir antes de qualquer decisão.
- **EQ de grupo:** lift **estreito em 2–4 kHz**, não shelf acima de 6 kHz. `INFERÊNCIA`: "boost the highs" do vídeo
  não traz frequência nem dB; 2–4 kHz é a banda onde o set de referência está −5,76 dB, e um shelf alto é o caminho
  mais curto para o brilho metálico que o material rejeita.
- **Não fazer:** copiar as duas camadas do vídeo como se fossem obrigatórias. Se o kick for uma pista só, isso é
  mudança **estrutural**, não preset — decidir antes.

### sub

- **O que o vídeo faz na camada low:** imprime o synth em áudio ("we recorded this from synth", 00:05:11.880–00:05:17.470) para
  ter "the same exact same sound with every repetition" (06:18–06:26); passa Saturator para "bigger and warmer" e
  **corta os agudos** (06:42–06:49); inverte a fase no Utility contra a outra camada (06:54–07:04); e faz um duck
  básico (08:28–08:44). Ele chama o resultado de "kind of like manual side chaining" (06:12–06:15).
- **No motor de referência:** a camada low do vídeo **é o sub existente**, não um sub novo. Não criar segunda camada de sub —
  isso engorda o grave e contraria a conclusão do diagnóstico (não adicionar sub indiscriminadamente).
- **Aplicar:** (1) imprimir o sub em áudio com Freeze & Flatten/Resample para repetição idêntica; (2) Saturator →
  corte de agudos, nessa ordem; (3) A/B de polaridade com Utility **contra o kick e contra o baixo**. A condição do
  vídeo existe no material: "these two tracks, they play the same note" (00:07:31) — sub e baixo compartilham a
  região de 69,3 Hz e harmônicos.
- **Ressalva medida, importante:** o render de referência **não mostrou cancelamento relevante no grave** — correlação de
  sub/baixo **1,00** e side/mid **−59,52 dB** em 30–120 Hz no diagnóstico de áudio. Ou seja: o flip de fase é um
  método para guardar no bolso, não um ganho esperado agora. Testar quando a camada mudar (sub impresso, punch layer
  novo, saturação nova), não por hábito.
- **Gate objetivo:** critério do material de referência: investigar perda **>3 dB ao somar em mono** ou cancelamento
  consistente em 25–120 Hz. Usar essa medida, não só o ouvido.
- **Cuidado de método:** o diagnóstico avisa que "o silêncio MIDI não prova ausência de cauda acústica nem fase correta".
  O A/B de fase é sobre áudio renderizado, não sobre o clipe MIDI.

### baixo/rolling

- **O que o vídeo faz:** clipe MIDI de 16º com **só três notas** — "We skip the first one just to make sure it
  doesn't collide with the kick" (00:09:02–00:09:08) — e uma delas com "a bit less velocity just to give it this
  galloping kind of feel" (00:09:10–00:09:16). O som é "literally just a saw wave with this filter envelope", short
  e plucky, **sem unison**, mono (00:09:39–00:09:58). Cadeia: Saturator → multiband (punch) → EQ que **corta os
  graves** para não clashar com a camada low (00:10:31–00:10:38) → Saturator (crunch) → Redux → delay sutil
  (00:10:38–00:11:15).
- **No motor de referência:** manter as notas 37/38/44/49/50 e a alternância **.50/.77**; não endireitar a grade.
  O "skip the first one" do vídeo já está resolvido de outro jeito no groove de referência: o sub só ataca em .27,
  então o **primeiro slot do tempo já está vazio**. Não preencher esse slot.
- **O que traduzir:** o corte de graves no baixo para não clashar com o sub ("we did cut the lows ... not clash with
  the low layer", 00:10:31–00:10:38). É a transferência mais importante para **não engordar o sub**. O baixo de
  referência já tem EQ Eight — é ali que o corte entra, antes de qualquer saturação.
- **Velocity:** o acento de velocity do vídeo é traduzível como **dinâmica**, não como timing. Aplicar nas notas
  deslocadas que já existem; nunca mover .50/.77.
- **Redux:** só no baixo, com A/B e banda limitada. É o device do vídeo que mais pode criar brilho metálico
  justamente na faixa onde o material está −5,76 dB. Se a faixa 1,2–4 kHz ficar áspera, rejeitar — o material de
  referência já rejeitou uma serra metálica.
- **Delay:** curto e discreto, **só na camada high**, com low-cut no retorno. O vídeo não diz tempo, feedback nem
  mix; não inventar valores.

### hats/shaker

- **O vídeo não trata.** Zero menção a hats ou shaker nos 16 minutos.
- **Único princípio transferível (citado):** tirar do baixo em vez de empurrar o outro som — "we want to take these
  out of the bass in order to make space for other frequencies" (00:12:16–00:12:21). Se o hat precisa de espaço,
  **corte a banda no baixo**; não suba o hat.
- **Guardrail medido:** o comparativo registra −8,86 dB em 5–12 kHz, mas diz explicitamente que **aumentar shaker
  para acertar a média contrariaria o alvo e o feedback de ouvido**. Não usar o vídeo como desculpa para
  subir topo.

### percussão de resposta

- **O vídeo não trata.** Nenhuma menção a percussão de resposta, clap, conga ou similar.
- **Único princípio transferível:** o mesmo "abrir espaço no baixo" acima. Nada rítmico é ensinado.

### madeira

- **O vídeo não trata.** Nenhum conteúdo acústico, orgânico ou de madeira. Kontakt 8 não é implicado.

### stab

- **O vídeo não trata.** Nenhum stab, chord ou hit harmônico é mostrado.

### subida

- **O que o vídeo oferece (pouco, mas citado):** os filtros do grupo existem para a automação de arranjo — "These
  filters are for the automation in the track" (00:14:45–00:14:49). Ou seja: a automação de filtro mora **no grupo
  de graves**, não em cada camada.
- **No motor de referência:** se houver varredura para a virada dos 2:00, automatizar um low-pass no **bus de graves**
  (kick+baixo juntos) mantém o motor coerente; o vídeo **não mostra curva, valor nem tempo**. Não usar isso como
  licença para um riser brilhante: o material de referência rejeitou um salto agudo no compasso 32.

### atmosfera

- **O vídeo não trata.** A única menção "psicodélica" é o Redux no baixo (00:10:48–00:10:57) — é caráter de baixo,
  não atmosfera. Não traduzir isso em pad/reverb.

### Onde exatamente no grid

- 128 BPM: **1 beat = 468,75 ms**; **1/16 = 117,19 ms**; 1 compasso = 1,875 s.
- Sub ataca em **.27 beat = 126,6 ms** depois de cada tempo; .46 = 215,6 ms; .68 = 318,8 ms.
- Baixo alterna **.50 = 234,4 ms** e **.77 = 360,9 ms**.
- **Consequência para o sidechain (`INFERÊNCIA` derivada, não valor do vídeo):** o duck na banda baixa precisa
  estar praticamente terminado por volta de **120 ms** se não quiser engolir o ataque do próprio sub em .27. O vídeo
  nunca declara attack/release — não citar número dele.
- O slot vazio do vídeo (primeiro 16º) já corresponde, no groove de referência, ao tempo sem sub. Preservar.
- Os vazios de kick em **0:44–0:45** e **0:59,5–1:00** são os melhores lugares para A/B de polaridade e de
  sidechain, porque ali o baixo aparece sem kick em cima.

### Regras para não engordar o sub nem criar brilho metálico

1. **Não duplicar sub.** As duas camadas do vídeo são low + high; no set de referência, low = sub e high = baixo.
2. **Saturator sempre seguido de corte de agudos** na camada low, na ordem do vídeo (00:06:42–00:06:49). Saturação
   gera harmônicos; o corte decide quais sobrevivem.
3. **Sidechain só abaixo de ~150 Hz** — nunca no baixo inteiro (00:12:52–00:13:03).
4. **Redux só no baixo**, com A/B e banda limitada; rejeitar se a faixa 1,2–4 kHz ficar áspera.
5. **Boost de agudos do kick é estreito e no grupo do kick**, não shelf no master.
6. **Polaridade é A/B, não regra:** o vídeo diz "see if it sounds better or worse" (00:07:45–00:07:48).
7. **Grave mono:** "No unison because we want to have it mono" (00:09:55–00:09:58). Isso também significa **não
   usar AutoPan no grave** — ele mexe em imagem estéreo, e o low-end de referência é mono por regra.
8. **Não usar delay no sub**; só na camada high, com low-cut.

### Ordem de teste sugerida (do mais barato ao mais caro)

1. Medir a fundamental do kick (EQ Eight + Spectrum). Só ouvir depois de medir.
2. Imprimir o sub e comparar polaridade contra kick e baixo; medir mono-sum em 25–120 Hz.
3. Montar o rack divisor de banda no baixo e comparar com o duck atual.
4. Só então testar Redux e delay na camada high.

## Prioridade e esforço

- **Prioridade: alta.** É exatamente a frente do motor (kick/sub/baixo), todos os devices são nativos e o vídeo
  entrega duas coisas que o outro walkthrough do mesmo selo (`GyhA92cfQgE`, Verschallt) não entrega: a **checagem de
  afinação do kick** e o **sidechain limitado em frequência** com A/B de fase documentado. Custo zero de plugin.
- **Esforço: médio.** Nada de compra, mas exige (a) imprimir o sub, (b) montar o rack de banda, (c) A/B de
  polaridade em material já aprovado e (d) eventualmente separar o kick em duas camadas — isso é mudança
  **estrutural**. O trabalho de dispositivo é curto; o custo real é o A/B e a aprovação de ouvido.
- **Risco de regressão: médio.** Fase e sidechain mexem em algo aprovado; por isso a regra de não tocar em .27/.77
  e de medir antes/depois. O próprio vídeo trata a fase como tentativa ("see if it sounds better or worse").
- **O que não fazer de uma vez:** aplicar Redux e delay junto com o sidechain na mesma passada. Um movimento por A/B, senão
  não se sabe o que causou o quê.

## Trechos de prova (3 citações literais da legenda)

1. `[00:04:16.920–00:04:20.030]` — *"Phrygian, not sure. Just make sure that your kick is in key"* — a checagem de
   afinação do kick como pré-requisito da tonalidade (não como regra de mix).
2. `[00:06:18.320–00:06:26.030]` — *"have the same exact same sound with every repetition because yeah, that's
   something that you want in the low end."* — a razão declarada para imprimir a camada low em áudio.
3. `[00:12:52.160–00:13:03.150]` — *"it just sounds cleaner because it not the entire bass gets ducked when the kick
   hits, but um only the the low frequencies or the frequencies where we we wanted it."* — o sidechain limitado em
   frequência, que é a técnica central deste vídeo para o caso.

Demais citações usadas neste mapa estão ancoradas por timestamp nas seções acima.

## Limites e o que NÃO foi verificado

- **O corte público cobre só o grupo de graves.** O walkthrough completo (1,5 h) está no Patreon (descrição). Hats,
  percussão, madeira, stab, subida e atmosfera **não são ensinados** neste vídeo.
- **A arquitetura atual do kick no set de referência não foi inspecionada.** Se hoje é uma
  pista só, a proposta de duas camadas é estrutural.
- **O preset "low extender" do Ableton não foi localizado** na instalação de destino; o device que o hospeda também não é
  nomeado na legenda. A instrução verificável é só "ataque lento" + "não exagerar no threshold".
- **O Auto Pan como sidechain não está detalhado** na legenda: eles citam o plugin, "align the phase" e "volume
  automation", sem taxa, forma de LFO ou profundidade. Nenhum valor foi inventado.
- **A rota do gate por mono-sum (>3 dB) não foi executada**; é o critério do material de referência, não uma
  medição nova.
- **Os números de referência vêm do render da versão de 26/10.** O próprio diagnóstico avisa que não se deve declarar o
  estado atual por captura antiga sem novo render.
