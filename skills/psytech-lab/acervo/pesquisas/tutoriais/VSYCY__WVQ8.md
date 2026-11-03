# How Rene Wise Makes His Tracks So Hypnotic

**Canal:** Hypnotic Techno Production · Frente: groove
**Duração real:** 13:08 (ffprobe do áudio baixado: `duration=787.876313`)
**Legenda:** `temLegenda=false` — **a legenda oficial do YouTube NÃO foi obtida.** Quatro tentativas terminaram em `HTTP Error 429: Too Many Requests` (auto-subs EN, write-subs, variações de idioma, curl direto na URL `timedtext` nos formatos `json3/srv1/ttml/vtt`); uma quinta variação por cliente (`--extractor-args "youtube:player_client=…"`) falhou antes da legenda. `--list-subs` confirma que existe faixa automática `en`, e `yt-dlp -J` devolve as URLs — o bloqueio é só na entrega do arquivo.
**Fonte de fala usada:** transcrição ASR local sobre o áudio do próprio vídeo — `whisper-cli` (whisper.cpp) com `ggml-small.bin`, WAV 16 kHz mono. **As citações abaixo são fala literal do vídeo transcrita por ASR, não a legenda oficial**; onde o ASR corrompeu palavra técnica, está marcado. Convenção: o texto falado é **VERIFICADO no áudio** e a grafia exata das palavras é **NÃO VERIFICADA**.
**Limite epistêmico central:** o próprio autor diz que fez um mapa de ouvido, não que abriu o projeto — "I've made some of the MIDI tracks here and just marked what's happening on every layer I could hear" [00:00:50–00:01:08], "I would have to see the project to properly analyze it but this is a rough overview of the arrangement" [00:01:08–00:01:15]. Logo: **posições, nomes de camada e contagens são reconstrução do autor do vídeo, não dados do projeto de Rene Wise.** O que o vídeo ensina com segurança é o *método de leitura e de arranjo*, não a receita exata da faixa.

---

## Técnica ensinada (2-4 frases)

O vídeo não ensina sound design: ensina **arranjo hipnótico por mapeamento e por gotejamento de variações**. O autor desmonta "Blackhawk" de Rene Wise em camadas (kick + 16 avos de hat + percussão + um "tomish lead" que também carrega o grave + synth principal + texturas + voz sussurrada) e mostra que a faixa funciona com pouquíssimos elementos porque **um elemento-gancho segura a atenção** — "why he can get away with having such a minimal arrangement right now because there is sound that like hooks us in" [00:06:33–00:06:46]. A hipnose vem de **micro-variações colocadas em fronteiras de frase**: um layer que "appears after four bars" para colar as duas metades da frase [00:02:07–00:02:24], um layer extra de open hat que faz "the energy of the track goes up" [00:03:16–00:03:23], a **troca** do open hat em vez de somar outro [00:04:45–00:05:00], um "additional percussive thing" que empurra a energia "a touch" [00:05:04–00:05:16], o lead que fica "more dense… more notes in the sequence" [00:07:13–00:07:21]. E o salto que ele chama de maior diferença entre iniciante e pro é a **quantidade de efeitos de transição**: "beginners just have one noise or something pro producers have like as you can see six eight different effects to help with transitions" [00:08:28–00:08:59]. O clímax é construído por **quebra de estrutura**, não por mais elementos: "here is the moment when the whole tension gets to another level because of the modulations breaking down the structure there is some like un-synced delays or something" [00:09:48–00:10:02], "some phasers maybe on this" [00:10:03–00:10:19], e só então "this moment released all the tension that was created with that synth" [00:10:19–00:10:26].

### Mecanismos observados (o que fazer, com prova)

| Mecanismo | O que o vídeo mostra | Prova |
|---|---|---|
| Camadas mínimas | "kick, 16 hi-hats, some percussion and we have this tomish lead which gives us in my opinion the low end and the main synth as well as some texture" | [00:01:15–00:01:41] |
| Elemento-gancho | o synth de tensão "whoo whoo whoo" é o que prende; é o que autoriza o arranjo mínimo | [00:06:22–00:06:39] |
| Layer de cola na 2ª metade da frase | "the synth wah which as you can see here appears after four bars so it helps like gels those two parts of the phrase" | [00:02:07–00:02:24] |
| Energia por troca, não por soma | "or maybe the swap maybe he she swapped the open hi-hats why is that just to maybe raise energy a bit" (ASR: "he she" = provável "he's") | [00:04:45–00:05:00] |
| Energia por 1 elemento novo | "there is additional percussive thing percussive bit that also changes helps with the pushing the energy up a touch and some lead variations" | [00:05:04–00:05:16] |
| Densidade como variação | "the lead is more dense so it's like more… more notes in the sequence" | [00:07:13–00:07:21] |
| Falso release | "here's like a mini breakdown we would think that the tension will release but it's not we are keep going nothing changes in my opinion in percussive" | [00:06:59–00:07:11] |
| Retirada de energia antes do breakdown | "our wall oh open hat change so kind of energy" … "energy went down a bit so we kind of like approaching the breakdown" (ASR: "wall" = provável "wah") | [00:09:11–00:09:25] |
| Banco de efeitos de transição | 6–8 efeitos curtos, inclusive voz sussurrada e grains, "just to keep things going" | [00:08:16–00:08:28], [00:08:28–00:08:59], [00:07:44] |
| Quebra por delay não sincronizado + phaser | tensão sobe "because of the modulations breaking down the structure" | [00:09:48–00:10:19] |
| Outro por subtração | "the outro just kick and perc thumps and detect main texture" (ASR: "detect" = provável "that's the") | [00:11:35–00:11:44] |
| Método de estudo | mapear percussion / low end / textures / leads / effects / motifs, "then you can erase this track and have this as a map for your own production" | [00:11:52–00:12:32] |

---

## Ferramenta usada no vídeo (plugin/stock)

**É Ableton Live**, não Bitwig: leitura de quadro do próprio vídeo em 00:01:01 e 00:01:03 (trecho baixado com `yt-dlp --download-sections "*60-64"` e extraído com `ffmpeg`). A barra de menus mostra `Live File Edit Create Playback View Navigate Options Help`; a cadeia de devices do canal selecionado mostra **Drum Rack, Utility, EQ Eight, Compressor, Echo**; o browser mostra Drum Rack; o transporte marca **134,00 BPM, 4/4**.

| Ferramenta | Papel no vídeo | Prova |
|---|---|---|
| **Ableton Live — Arrangement + Locators** | é o próprio método: trilhas separadas por camada + marcadores nomeados por função (`energy up`, `tension`, `…tension release`, `rel`, `outro`) | quadro 00:01:03; fala [00:00:50–00:01:15] |
| **Trilhas/clipes-rótulo (MIDI)** | "mapa de ouvido" com nomes por evento (`kick, 16th hats extra perc`, `OH Layer + extra perc`, `TOMan lead`, `lead variations`, `grain txtr`, `grain fx`) | quadro 00:01:01–00:01:03 + fala [00:00:50–00:01:08] |
| **Drum Rack** | motor de bateria/percussão do canal de bateria | quadro (device visível) |
| **Utility (Mono + Bass Mono 120 Hz)** | garante grave mono no canal — o canal está em "Mono" com corte em 120 Hz | quadro, ambos os frames |
| **EQ Eight** | EQ do canal; curva quase plana no quadro (não inferir valores) | quadro |
| **Compressor** | dinâmica do canal | quadro |
| **Echo** | delay do canal; nos returns aparecem `A Verb`, `C Reverb`, `D Delay` | quadro |
| **Grains / texturas** | camada "grain txtr" e "grain fx" (origem do grain não é nomeada na fala) | quadro + fala [00:05:23], [00:07:44], [00:09:04] |

**Nenhum plugin de terceiros é nomeado na fala**, e nenhum aparece legível nos quadros. **ANA 2, VELA, SideKick, Kick 3 e Bitwig não aparecem** — não há nada a substituir. Como a técnica é de arranjo, o parque de ferramentas do vídeo é exatamente o de um arsenal Live 12: **tudo o que está visível é stock do Live**.

**Cuidado de leitura:** o áudio que toca é a faixa de referência; o que o autor construiu é a *anotação*. O Drum Rack/Utility/EQ/Compressor/Echo visíveis são a cadeia do canal de anotação dele, não necessariamente a cadeia usada por Rene Wise.

---

## Tradução para um arsenal compatível: Serum 2 (com GranularOsc), Diva, Vital, Massive X, Surge XT, Kontakt 8, Live 12 nativo

**Veredito: traduzível integralmente, sem perda de conceito.** O vídeo é 100% Live e 100% arranjo; não depende de nenhum plugin fora do arsenal.

| No vídeo | Conceito | Equivalente |
|---|---|---|
| Arrangement + Locators do Live | mapa do arranjo por camada e por função | **Live 12 Arrangement + Locators** (idêntico); nomear os 8 blocos de 8 compassos do motor |
| Clipes-rótulo por evento | registrar "o que entra quando", não só o MIDI | **Live 12**: nome de clipe/cena padronizado (`ENTRA OH`, `SAI OH`, `GRAIN 2c`); mesma disciplina, custo zero |
| Drum Rack | kick + percussão + hats num rack | **Live 12 Drum Rack** (idêntico) |
| Utility `Mono` + `Bass Mono 120 Hz` | grave mono | **Live 12 Utility** (idêntico) — já é regra do material de referência (low-end mono) |
| EQ Eight | correção cirúrgica do canal | **Live 12 EQ Eight** (idêntico) |
| Compressor | dinâmica | **Live 12 Compressor** (idêntico) |
| Echo (sync ligado) | delay musical | **Live 12 Echo** (idêntico) |
| Delay dessincronizado no breakdown | quebra de grade para gerar tensão | **Live 12 Echo com `Sync` desligado** (tempo livre em ms) — é literalmente o mesmo device |
| Phaser no breakdown | movimento sem nota nova | **Live 12 Phaser-Flanger** (nativo); **Shifter** como alternativa de movimento |
| Returns `A Verb`, `C Reverb`, `D Delay` | espaço sem sujar o seco | **Live 12 Hybrid Reverb + Echo** em returns, com HPF no retorno (regra do material: não mandar kick/sub para cauda grave) |
| `grain txtr` / `grain fx` | textura granular de cola | **Live 12 Grain** (nativo, sample) ou **Serum 2 GranularOsc** (granular com afinação, bom quando a textura precisa estar na tônica). Preferir **Grain** para textura de fundo e **GranularOsc** quando se quiser grão tonal |
| Voz sussurrada / "voices" | efeito de transição e hipnose | Não há biblioteca de voz dedicada na lista do arsenal; usar **Kontakt 8 — Ethereal Earth / LOOP GARDEN** (vozes/texturas) ou um sample vocal de terceiros **já existente no set de referência**. Presença dos títulos **VERIFICADA**; som e licença **NÃO VERIFICADOS** |
| `tomish lead` que "gives us the low end" | camada de tom carregando corpo | **Serum 2** (ou Diva/Surge XT) — mas **com HPF**, porque no motor de referência o grave é do sub/baixo (ver aplicação) |
| Synth wah / synth de tensão (gancho) | motivo curto que hipnotiza | **stab (Kontakt 8)** e **Serum 2** já disponíveis; **Vital/Massive X/Surge XT** só se faltar caráter |
| Lead mais denso | variação por quantidade de notas | **Serum 2 / Diva** no material existente; aplicado à *resposta*, não ao baixo |

**O que não importar:** o projeto do vídeo corre a **134,00 BPM em 4/4** (leitura de quadro) e a camada de topo é anotada como "16th hats" — subdivisão de 16 avos, **sem informação sobre deslocamento** (o mapa não mostra micro-timing). O motor de referência corre a 128 BPM com subdivisões deslocadas **.27/.77** — adotar a densidade de 16 avos por cima do groove aprovado tenderia a mascarar o deslocamento. Toda a tradução abaixo preserva o deslocamento.

---

## Aplicação concreta em um motor minimal de 2 minutos: por função

**Contexto medido do set de referência (diagnóstico de 26/10, não re-medido aqui):** 300–1.200 Hz **−4,83 dB** e 1.200–4.000 Hz **−5,76 dB** contra a média de 6 referências externas; low-end mono; groove com subdivisões deslocadas **.27/.77** a preservar. Do diagnóstico do motor: 2:00 = 64 compassos, fronteiras em **0:15 (c9) · 0:30 (c17) · 0:45 (c25) · 1:00 (c33) · 1:15 (c41) · 1:30 (c49) · 1:45 (c57) · 2:00 (c65)**; o sub começa em **.27** a cada tempo, notas de **.68** beat (exceto **.46** no 4º tempo); o baixo alterna **.50/.77**; madeira e subida ativos; clap, horn e percussões diversas mudos; o shaker já foi reduzido para −28 dB; um salto agudo no c32 foi rejeitado; uma serra no meio foi rejeitada como metálica; vazios de kick em **0:44–0:45** e **0:59,5–1:00** a preservar.

**Regra de ouro traduzida:** o vídeo sobe energia **trocando, omitindo e estreando UM elemento por fronteira de 8 compassos** — nunca ligando uma camada contínua nova. É exatamente o que o motor de referência precisa para o 2º minuto não virar repetição e para não engordar o sub nem abrir brilho.
**Critério de segurança explícito:** nenhuma aplicação abaixo escreve abaixo de 120 Hz (kick e sub ficam intactos) nem boosta 2–5 kHz; o preenchimento de 300–1.200 Hz vem de madeira e percussão de corpo, e o de 1.200–4.000 Hz vem de textura/voz **band-limited**, não de hats.

### Kick
O vídeo trata o kick como esqueleto da "very minimal percussive flow" [00:01:15–00:01:23] e usa camadas de evento por cima dele, não troca de kick. **Aplicação:** manter fonte e afinação atuais; não tocar em EQ nem em decay. Se o A/B de peso pedir, a única intervenção compatível com o vocabulário do vídeo é **um kick-fantasma extra** na subdivisão deslocada (lado .27) dentro de 1:30–2:00 (c49–c64) — nunca um segundo kick sample; o quadro 00:01:03 mostra um rótulo de clipe que parece incluir "extra kick", mas a leitura é parcial. Risco: mascarar o sub; medir antes.

### Sub
O vídeo deixa o "tomish lead" carregar o grave [00:01:23–00:01:30]. **Não copiar:** no motor de referência o sub é Operator mono e o baixo é Serum 2; somar um tom no grave é exatamente a "sobreposição de semitom no grave" que o diagnóstico desaconselha. **Aplicação:** sub intocado (início .27, durações .68/.46). Se se quiser o *caráter* de tom, ele entra **acima de 120–150 Hz** (HPF), como corpo, não como sub. Não alongar notas para "sustentar" — o vídeo não faz isso e o diagnóstico já registrou que sub sustentado sob o D encavala.

### Baixo / rolling
Duas técnicas literais do vídeo servem: **densidade como variação** ("the lead is more dense… more notes in the sequence" [00:07:13–00:07:21]) e **articulação/automação de efeito** ("some effect automation or something just to add some variation" [00:04:20–00:04:28]). **Aplicação:** patch Serum 2 preservado. Em **1:15–1:30 (c41–c48)**, variar **comprimento/velocidade** de uma nota (ex.: encurtar .68→.50 num tempo) ou trocar a ordem **.50/.77** por **.77/.50** em 4 compassos, e reverter. Em **1:30–2:00**, uma única nota extra de 16 avos por compasso, só nos compassos ímpares, com retirada em c56. Isso dá "mais denso" sem nota nova permanente e sem mexer no desenho do sub. **Não** usar o baixo para preencher 300–1.200 Hz — o corpo vem de madeira/percussão.

### Hats / shaker
É a função com tradução mais direta e mais perigosa. O vídeo: camada extra de open hat sobe a energia [00:03:16–00:03:23]; depois **troca** o open hat para subir mais um toque [00:04:45–00:05:00]; e antes do breakdown **muda o open hat para a energia cair** [00:09:11–00:09:25]. **Aplicação:** manter nível atual (o shaker do motor de referência está em −28 dB; o diagnóstico diz explicitamente para **não** subir o shaker perseguindo o agudo médio). Usar o vocabulário do vídeo como **portas de 8 compassos**:
- **c33 (1:00):** *sair* com o open hat (equivale ao "energy went down a bit") — cria o falso release antes do clímax;
- **c41 (1:15):** voltar com o open hat **trocado** (outro sample do mesmo padrão), não somado;
- **c49 (1:30):** entrar com uma **camada de acento de open hat** (não um shaker contínuo) nas posições **.27/.77**, ganho baixo, subindo 2–3 dB ao longo de 8 compassos — a camada de shaker existente fica intocada em −28 dB;
- **c57 (1:45):** trocar de novo, ou omitir 1 tempo a cada 2 compassos.
Nunca uma camada contínua de 16 avos por cima do groove; nunca boost de 2–5 kHz para "trazer presença" — é o caminho do brilho metálico que o material já rejeitou.

### Percussão de resposta
O vídeo é explícito: "additional percussive thing… helps with the pushing the energy up a touch" [00:05:04–00:05:16], e os rótulos de clipe mostram combinações (`PER + OH`, `OH PER`). **Aplicação:** é aqui que se ataca o buraco de **300–1.200 Hz** sem subir o topo. **c17–c24:** uma resposta de bongo/madeira curta, ciclo de 2 compassos (2 de fala, 2 de pausa), HPF 250 Hz, LPF ~6 kHz, ganho baixo (−20 a −24 dB) para somar corpo sem hiss. **c41–c48:** alternar quem pergunta e quem responde entre madeira/bongo/stab (previsto no diagnóstico do arranjo) — é a versão local do "additional percussive thing" atuando como energia, não como groove novo. **c57–c64:** manter só uma célula, para o ouvinte sentir a subtração.

### Madeira
Não existe "madeira" no vídeo, mas existe a **função de cola**: um layer que "appears after four bars so it helps like gels those two parts of the phrase" [00:02:18–00:02:24]. **Aplicação:** a madeira não entra no compasso 1 da frase — entra no **compasso 5 de cada bloco de 8** e é ela que costura as duas metades. Em **c9–c16** e **c25–c32**, manter exatamente essa defasagem de 4 compassos; em **c33–c40**, deslocar para o compasso 3 (quebra a expectativa sem trocar o timbre). Corpo dela vive em 300–1.200 Hz — é o enchimento correto do vale medido, e é madeira, não serra.

### Stab
O synth de tensão é o **gancho** que autoriza o minimalismo [00:06:22–00:06:39]. **Aplicação:** o stab (Kontakt 8) assume esse papel: 2 notas frígias, 1 ataque a cada 2 compassos, no .77 (o lado deslocado), nível discreto. É o "whoo whoo whoo" do motor de referência — e é o que permite os outros elementos serem poucos. A variação "mais denso" [00:07:13–00:07:21] entra **só em c49–c56** (uma nota extra por compasso), nunca nos primeiros 8 compassos.

### Subida
O vídeo constrói o clímax com **modulação e quebra de grade**, não com mais volume: "un-synced delays" [00:09:48–00:10:02], "some phasers maybe" [00:10:03–00:10:19], e a tensão só se resolve depois [00:10:19–00:10:26]. **Aplicação:** a subida mantém o papel atual; em **c31–c32** e **c55–c56** acrescentar **Echo com `Sync` desligado** (tempo livre, ~330–350 ms) num envio curto do stab ou da madeira, com feedback moderado, e **Phaser-Flanger** em paralelo de 1 compasso. **Não** repetir o salto agudo do c32 já rejeitado: a tensão vem do tempo e da fase, não da oitava. A entrada e a saída do efeito são cortadas em 1 compasso — é efeito de transição, não camada.

### Atmosfera
O vídeo nomeia o mecanismo central: **6–8 efeitos curtos**, sendo os principais **voz sussurrada** e **grains**, todos com função de transição ("these effects are helping with the transition… it just helps to gel those sections together" [00:01:41–00:02:04]; contagem em [00:08:16–00:08:28]; "our voices going very hypnotic" [00:07:44]). **Aplicação:** montar um **banco de 4–6 eventos** (whisper chop, grain, textura reversa, ruído filtrado) e usá-los **um por fronteira** — 0:14–0:15, 0:29–0:30, 0:44–0:45, 0:59–1:00, 1:14–1:15, 1:29–1:30, 1:44–1:45, 1:59–2:00. Cada evento dura **2–4 compassos e é mutado depois**; nada fica ligado. Band-limit **300 Hz–6 kHz** (HPF para não engordar o sub, LPF para não abrir brilho metálico) — assim os eventos ocupam justamente as duas bandas que estão −4,83 e −5,76 dB. Os vazios de kick em 0:44–0:45 e 0:59,5–1:00 são o melhor lugar para a voz/whisper: o buraco já existe, o efeito só o preenche. **INFERÊNCIA**, não medição: a banda exata de cada textura tem que ser conferida em análise espectral antes de fixar.

### Falso release (mecanismo transversal, o mais valioso para "hipnose via groove")
"we would think that the tension will release but it's not we are keep going nothing changes in my opinion in percussive" [00:06:59–00:07:11]. **Aplicação:** em **c33–c40**, retirar **só** o open hat e o stab, mantendo kick, sub, baixo, hats fechados e percussão **idênticos**. O ouvinte espera alívio, o chão não muda. O release real fica para **c57** (1:45), já com a subida no diálogo. Isso atende diretamente o problema declarado do 2º minuto ("reto, sem repovo") sem acrescentar material.

### O método como entregável (o que o vídeo realmente ensina)
Antes de escrever, montar o **mapa de 64 compassos** com uma linha por função (bateria / sub / baixo / hats / resposta / madeira / stab / subida / atmos) e uma coluna por bloco de 8, marcando **entra / sai / troca / densifica** — e nomear os marcadores com função, como o autor faz (`energy up`, `tension`, `…tension release`, `rel`, `outro`). O próprio autor recomenda o exercício: "take a track that you really like and try to break it down… then you can erase this track and have this as a map for your own production" [00:11:59–00:12:26]. Custo zero, e é o que evita o 2º minuto ser cópia do 1º.

### Onde NÃO aplicar
- **Não** copiar a densidade de 16 avos dos hats, o tempo do vídeo (134,00 BPM, leitura de quadro) nem a instrumentação (tom + synth) — a referência é outra escola.
- **Não** usar os "6–8 efeitos" como 6–8 camadas sempre ligadas; no vídeo eles são **eventos**.
- **Não** preencher 1.200–4.000 Hz com shaker/hats (o diagnóstico registrou que o candidato tem mais agudo relativo que as referências).
- **Não** reviver os canais mudos do motor de referência (clap, horn e percussões avulsas) para "subir energia" — o vídeo sobe energia com troca de open hat e uma percussão.

---

## Prioridade e esforço

**Prioridade: alta.**
- **Por quê:** resolve o problema estrutural do 2º minuto (repetição) com **zero plugin novo** e sem tocar em timbre aprovado; é uma das poucas fontes da pesquisa que atacam *arranjo de hipnose por groove* em vez de sound design.
- **Nota:** não adiciona fonte sonora nem corrige banda por si só; o 1º minuto já está aprovado e o valor está na disciplina de variação do 2º. Sem A/B, o ganho é de método, não de som.

**Esforço: baixo para 70% das ações, médio para o banco de efeitos.**
- **Baixo:** trocar/omitir open hat em c33/c41 (é mute e troca de sample no mesmo padrão); defasar a madeira em 4 compassos; retirar o stab no falso release; mapear os 64 compassos em marcadores.
- **Médio:** construir e **roteirizar** o banco de 4–6 eventos de atmosfera com entrada/saída em 2–4 compassos e band-limit — exige decisão de fonte (Grain vs GranularOsc vs Kontakt), roteamento de return e disciplina de mute. É a parte que o vídeo chama de maior salto, e é a que dá mais trabalho.
- **Alto:** nenhum. Não há síntese nova, nem re-automação de grave, nem mudança de kick/sub.

**Ordem de execução sugerida (sem mutar nada de início):** (1) mapa de 64 compassos; (2) portas de open hat c33/c41/c49; (3) falso release c33–c40; (4) resposta de percussão c17–c24; (5) banco de atmosfera; (6) subida com delay dessincronizado c31–c32/c55–c56.

---

## Trechos de prova: 3 citações literais

> **1) O salto iniciante→pro é a quantidade de efeitos de transição** — [00:08:23.280 → 00:08:59.600]
> "and this is what I see like the biggest leap from beginners to pro or intermediate like the amount of effects yeah beginners just have one noise or something pro producers have like as you can see six eight different effects to help with transitions we have variations some basic thing"

> **2) O arranjo mínimo só se sustenta porque há um gancho** — [00:06:33.840 → 00:06:46.000]
> "why he can get away with having such a minimal arrangement right now because there is sound that like hooks us in and some small variations again I believe in here"

> **3) O falso release: a tensão não alivia, a percussão não muda** — [00:06:59.520 → 00:07:11.440]
> "yeah so here's like a mini breakdown we would think that the tension will release but it's not we are keep going nothing changes in my opinion in percussive"

**Nota de fidelidade:** as três citações vêm da transcrição ASR local, não da legenda automática do YouTube, que ficou bloqueada por HTTP 429. Pontuação e palavras de apoio ("yeah", "like") são do transcritor; nenhuma palavra de conteúdo foi editada. Trechos com provável erro de ASR estão marcados no corpo do mapa (`he she`, `wall`, `tummy slit`, `detect`); `16 hi-hats` é ASR para `16th hats` — os rótulos de clipe legíveis no quadro 00:01:01 dizem `kick, 16th hats extra perc`, o que confirma o conteúdo e expõe o erro do transcritor.

---

## Fontes

- Áudio do vídeo `VSYCY__WVQ8` (`yt-dlp -f bestaudio`, 12.742.743 bytes, 787,876 s) e transcrição ASR local (whisper.cpp, ggml-small.bin) — lidos na sessão de estudo.
- Quadros de 00:01:01 e 00:01:03 extraídos de trecho baixado (`--download-sections "*60-64"`) — lidos na sessão de estudo para identificar o DAW e os devices.
- Descrição oficial: "Learn hypnotic techno arrangement techniques from Rene Wise's track breakdown. You'll learn how to structure a minimal techno arrangement using very few elements that work well together." (`yt-dlp --print "%(description)s"`).
- Diagnóstico do motor de referência de 26/10 — estado do motor, fronteiras de compasso, offsets .27/.50/.68/.77, mutes, bandas medidas e restrições (lido integralmente na sessão de estudo).
- Mapa irmão do mesmo canal (`Dcs7r1b6RwI`, incluído no acervo) — usado só como referência de estrutura.

**NÃO VERIFICADO:** som real de qualquer uma das propostas; banda espectral exata de voz/grain; disponibilidade/licença de Ethereal Earth e LOOP GARDEN; se o Drum Rack/Utility/EQ/Compressor/Echo visíveis são a cadeia de Rene Wise ou só a do canal de anotação do autor. Nenhuma mutação foi feita em nenhum set durante o estudo.
