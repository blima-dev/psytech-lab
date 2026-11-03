# Mixing Techno Kick and Bass - Your Guide to the Perfect Low-End

> ID `I__tWZTk5-Q` · canal **SINEE Global** · apresentador **Björn Torwellen** (creditado na descrição) · 16:03
> (963 s) · publicado 21/11/2024 · 10.812 views na leitura desta sessão.
>
> **temLegenda=false.** Não existe nenhuma faixa de legenda neste vídeo — nem automática, nem manual.
> Comandos executados e saídas literais:
> - `yt-dlp --skip-download --write-auto-subs --sub-langs en --convert-subs vtt …` →
>   `[info] There are no subtitles for the requested languages`
> - `yt-dlp --skip-download --write-subs --sub-langs en --convert-subs vtt …` → mesma mensagem
> - `yt-dlp --skip-download --list-subs …` → `I__tWZTk5-Q has no automatic captions` e
>   `Available subtitles for I__tWZTk5-Q: Language Formats / live_chat json`
>
> Portanto **toda a técnica abaixo vem da descrição oficial e dos capítulos/metadados do próprio vídeo**,
> não de fala transcrita. Onde se completa com engenharia, está marcado `INFERÊNCIA` ou `HIPÓTESE`.
> Tags do vídeo (metadados): `Kickbass Chain`, `Lowend Chain`, `Techno Lowend Chain`, `Kick Drum Bass Chain`.

## Técnica ensinada (2-4 frases)

O vídeo trata kick e baixo como **um único grupo** — a descrição diz literalmente *"having a well-functioning
kick and bass group is absolutely essential"* — e ensina uma **cadeia fixa de processamento** nesse grupo para
*"effortlessly glue kick and bass"* e entregar impacto no clube. A cadeia, na ordem em que os capítulos aparecem,
é: **EQ → Transformer → Roar → Weiss EQ → Bass Low Extender → Virtual Mix Rack → Soothe 2 → Clipper → Limiter**,
com o **Roar** ocupando a maior fatia (05:27–08:01, 2min34s), seguido do **Limiter** (2min26s) e do **EQ** (2min19s).
O conceito declarado é o *"concept behind his mixing approach"* de Björn Torwellen, e a promessa é *"glue kick and
bass in your future sessions"*. `INFERÊNCIA`: a ordem acima é a ordem **dos capítulos**; a descrição não afirma que
é a ordem do sinal, nem em qual estágio cada processador está no bus do grupo ou nos canais individuais.

## Ferramenta usada no vídeo (plugin/stock)

Tudo o que se sabe é o **nome do capítulo** e a **duração**. O vídeo não tem legenda, então **não há nenhum valor
de parâmetro, frequência, ratio, drive ou redução de ganho verificável** — nada disso é inventado aqui.

| # | Capítulo (start–end) | Duração | O que o nome diz | O que NÃO está dito |
|---|---|---|---|---|
| 1 | `EQing` (02:54–05:13) | 2:19 | uma etapa de EQ no grupo kick+baixo | qual EQ, quais frequências, corte ou boost |
| 2 | `Transformer` (05:13–05:27) | 0:14 | saturação por transformador, citada de passagem | qual plugin, quanto drive |
| 3 | `Roar` (05:27–08:01) | **2:34** | o núcleo do vídeo: saturação/distorção | qual "Roar" (nativo do Live 12 ou plugin homônimo), modo, drive, filtro, dry/wet |
| 4 | `Weiss EQ` (08:01–09:04) | 1:03 | um segundo EQ, de precisão | modelo exato (EQ1?) e ajustes |
| 5 | `Bass Low Extender` (09:04–09:59) | 0:55 | extensão de graves do baixo | qual plugin e quanto de sub-oitava |
| 6 | `Virtual Mix Rack` (09:59–10:25) | 0:26 | channel strip (console/comp/EQ) | qual módulo do rack |
| 7 | `Soothe 2` (10:25–10:55) | 0:30 | supressão dinâmica de ressonâncias | bandas, depth, seletividade |
| 8 | `Clipper` (10:55–12:29) | 1:34 | ceifamento de picos antes do limiter | quanto de clipping, algoritmo |
| 9 | `Limiter` (12:29–14:55) | 2:26 | limitação final do grupo | ceiling, release, redução |
| 10 | `Summary` (14:55–16:03) | 1:08 | recapitulação do conceito | — |

| Ferramenta | Natureza | Status |
|---|---|---|
| EQ (sem nome) | EQ corretivo | equivalente nativo (EQ Eight) |
| **Transformer** | saturação | sem emulação de transformador nativa; conceito = saturação harmônica |
| **Roar** | saturação/distorção (2min34s = coração do vídeo) | **se for o Roar do Live 12, é nativo**; se for outro produto, o conceito é o mesmo |
| **Weiss EQ** | EQ de alta precisão | EQ Eight cobre o gesto |
| **Bass Low Extender** | extensão de sub | Serum 2 Sub / Operator sine cobrem |
| **Virtual Mix Rack** | channel strip | Glue Compressor + EQ Eight + Saturator cobrem |
| **Soothe 2** | supressão dinâmica de ressonância | **não tem equivalente nativo exato** (ver tradução) |
| **Clipper** | ceifador | sem device "clipper" nativo; Saturator em modo de clip cobre |
| **Limiter** | limitador | nativo (Limiter) |

## Tradução para Live stock + synths comuns (Serum 2, Diva, Vital, Massive X, Surge XT, Kontakt 8)

**Nada no vídeo depende de ANA 2, VELA, SideKick, Kick 3 ou Bitwig** — a descrição e os capítulos não citam nenhum
deles. O que falta são os **processadores de mixagem de terceiros** (Weiss EQ, Virtual Mix Rack, Soothe 2,
Bass Low Extender) e, possivelmente, o Roar (se não for o nativo do Live 12). O conceito sobrevive inteiro: é uma
**cadeia de bus** — corrigir, saturar, corrigir de novo, estender grave, colar, domar ressonância, ceifar, limitar.

| Etapa do vídeo | Conceito real | Rota exata | Limite / ressalva |
|---|---|---|---|
| **EQing** (02:54) | EQ corretivo antes de saturar: tirar o que atrapalha antes de gerar harmônicos | **Live 12 EQ Eight** no bus kick+baixo; HP em ~25–30 Hz, corte estreito onde o kick "caixa" (varrer 180–450 Hz) | é o mesmo gesto, não o mesmo EQ; `INFERÊNCIA` |
| **Transformer** (05:13) | saturação de transformador: harmônicos de baixa ordem, densidade, "cola" | **Saturator** em `Soft Sine` ou `Medium Curve`, drive baixo, com **Color/Freq** mirando 300–800 Hz | Live não tem emulação de transformador; `INFERÊNCIA` |
| **Roar** (05:27, 2min34s) | saturação/distorção com filtro e mistura — o núcleo do som | **Live 12 Roar**: filtro **BP/HP+LP** cobrindo ~150 Hz–2 kHz, drive moderado, dry/wet parcial. Alternativas: **Saturator** com EQ antes/depois; **Serum 2** com warp `soft_clip`/`fold`/`hard_clip` num layer; **Diva** drive do filtro; **Vital/Massive X/Surge XT** distorção de insert | **não se sabe qual Roar é**; se for o nativo, é literalmente o mesmo device |
| **Weiss EQ** (08:01) | segundo EQ, depois da saturação: limpar o que a distorção sujou, com precisão | **EQ Eight #2** pós-drive, só cortes estreitos de Q alto nas ressonâncias que a saturação criou | a precisão do Weiss não é replicável; o gesto é |
| **Bass Low Extender** (09:04) | reforço de sub/baixa oitava do baixo | **Serum 2 Sub** (slot 4, sine/triangle, uma oitava abaixo, mono) ou **Operator** sine; low-pass ≤120 Hz | **etapa perigosa se o grave do próprio projeto já tem excesso medido** — ver aplicação |
| **Virtual Mix Rack** (09:59) | channel strip: compressão + tom + cola | **Glue Compressor** (attack lento, release auto, 1–2 dB de redução) + **EQ Eight** + **Saturator** | a "cola" é a compressão de bus, não o rack |
| **Soothe 2** (10:25) | supressão **dinâmica** de ressonância (só quando a ressonância aparece) | **não existe nativo equivalente.** Rota: **Multiband Dynamics** como compressão descendente estreita + **EQ Eight** com cortes estáticos varridos; ou automação manual de banda | declarar a lacuna: sem Soothe, o resultado é menos automático e mais estático |
| **Clipper** (10:55) | ceifar os picos do grupo **antes** do limiter, para o limiter não bombear | **Saturator** em `Hard Curve`/`Digital Clip` com drive alto e output compensado, ou `hard_clip` do Serum 2 num layer | Live não tem device "Clipper" dedicado; o Saturator faz o mesmo corte |
| **Limiter** (12:29) | limitar o grupo para entregar nível estável ao master | **Live 12 Limiter** no fim do bus do grupo | ceiling/release são de quem aplica, não do vídeo |

**O que não tem tradução e precisa ser dito:** Soothe 2 é o único estágio sem equivalente nativo honesto. Se a
ressonância for **estática**, EQ Eight resolve. Se for **dependente de nível** (só grita quando o baixo entra),
Multiband Dynamics resolve parcialmente porque suas bandas são largas (Low/Mid/High com crossovers), não por
frequência. `INFERÊNCIA` de catálogo de devices, não do vídeo.

**Regra de ouro da tradução:** a cadeia do vídeo é **serial no bus**, mas o ganho de "cola" vem de
**saturação + compressão + clipper**, não de mais EQ. O risco não é falta de processamento — é excesso de
processamento no grave quando o peso já está resolvido.

## Notas de aplicação por função (motor de ~2 min)

**Leitura de estado típica (medida em sets de referência, não do vídeo):** quando um motor psytech já tem
`sub−kick` dentro do envelope das referências, **falta de sub não é o problema**; os riscos reais costumam ser
excesso na banda 55–75 Hz, presença 2–4 kHz alta e **limiter virando envelope rítmico involuntário** (redução
reaparecendo a cada kick). Com o miolo 300–1.200 Hz deficitário, a parte do vídeo que serve é **a saturação
controlada em 150 Hz–2 kHz** (gera harmônicos justamente no miolo) e **o clipper antes do limiter** (tira o
trabalho rítmico do limiter). A parte que **não** serve é o **Bass Low Extender**: reforçar sub num sistema que já
tem excesso em 55–75 Hz engorda o grave e come headroom sem resolver o vale do meio.

| Função | Aplicar? | Como | Limite |
|---|---|---|---|
| **Kick** | **Sim, a etapa de saturação + clipper** | No canal do kick: EQ Eight (HP 25–30 Hz; corte estreito 180–450 Hz só se houver caixa) → Saturator `Soft Sine`/`Medium Curve` com Color em 300–800 Hz, drive baixo → clipper só nos picos. **Não** passar o fundamental por drive alto | O fundamental do kick é onde a relação sub−kick foi conquistada; saturar demais adiciona 2ª/3ª harmônica em 100–250 Hz e **agrava** o problema de 55–75 Hz, não o resolve |
| **Sub** | **Não — e nunca o Bass Low Extender** | Manter sine mono, sem drive, sem clipper, sem Soothe. Se precisar de definição em sistema pequeno, camada paralela de harmônicos com **HP 120 Hz** e nível baixo | Low-end mono, sub−kick já resolvido; adicionar oitava abaixo só come headroom |
| **Baixo/rolling** | **Sim — é o maior ganho** | Bus do baixo: EQ Eight (HP ~40 Hz, corte estreito em 55–75 Hz se o rolling estiver inflando essa banda) → drive **band-limited** (HP 150 Hz / LP ~1,8 kHz) → EQ Eight #2 pós-drive (só ressonância) → Glue Compressor leve | O drive no fundamental **engorda**; o drive filtrado preenche 300–1,2 kHz sem tocar no sub. Preservar o groove: compressor com attack ≥30 ms e redução ≤2 dB para os ghost notes não sumirem |
| **Hats/shaker** | **Não — fora do bus** | Continuam secos, no canal deles, com o groove intacto. Nada de clipper/limiter de grupo neles | Se entrarem no bus, o clipper sobe o nível relativo deles e o limiter comprime junto — cria hiss e destrói a hierarquia |
| **Percussão de resposta** | **Não no bus; benefício indireto** | Fica fora do bus kick+baixo. O clipper no grupo libera headroom e mantém o limiter estável, então a resposta não é "engolida" por pumping | Não usar o limiter do grupo como sidechain; isso criaria o envelope rítmico involuntário |
| **Madeira** | **Sim, como gesto — não como bus** | No canal de madeira: Saturator leve + EQ Eight cirúrgico depois, exatamente o par "Transformer → Weiss EQ". Não passa pelo limiter do grupo | Madeira é fonte acústica: dry sagrado, wet ≤25% ou paralelo |
| **Stab** | **Parcial** | Mesmo gesto saturação→EQ cirúrgico no canal do stab, para ganhar corpo em 300–1,2 kHz | Stab não entra no bus de grave; não herda o limiter do grupo |
| **Subida** | **Não** | Subida vai direto ao master; nunca pelo clipper/limiter do kick+baixo | Um riser dentro de um limiter de grupo modula o grave inteiro e achata a subida |
| **Atmosfera** | **Não** | Nada da cadeia se aplica; manter HP ≥120–200 Hz no retorno de reverb | Não passar atmosfera por clipper nem por Soothe-substituto no bus de grave |

### Onde inserir, na prática (bus do motor)

1. **Criar o grupo KICK+BAIXO** (kick, sub, rolling, bassmédio) — a descrição do vídeo fala de um
   *"kick and bass group"*; é a mesma ideia.
2. **EQ Eight #1** — corretivo: HP 25–30 Hz; corte estreito em 180–450 Hz (só se boxy); **checar 55–75 Hz** e
   cortar o excesso ali em vez de adicionar grave.
3. **Estágio de drive paralelo** (o "Roar"): rack com **EQ Eight HP 150 Hz + LP ~1,8 kHz → Saturator/Roar**
   e dry/wet ~20–35%. É o que preenche 300–1.200 Hz sem sujar o sub nem o topo.
4. **EQ Eight #2** — pós-drive, só cortes estreitos de ressonância.
5. **Glue Compressor** — 1–2 dB de redução, attack lento, release auto (a "cola" do Virtual Mix Rack).
6. **Clipper** (Saturator `Hard Curve`/`Digital Clip`) — só os 1–3 dB de pico.
7. **Limiter** — último do bus, conservador; o master continua sendo quem define o ceiling final.
8. **Fora do bus:** hats, shaker, percussão de resposta, madeira, stab, subida, atmosfera.

### Como não engordar o sub

- **Não usar o Bass Low Extender** como o vídeo usa: se o próprio grave já tem excesso medido (ex.: +4 dB em
  55–75 Hz), qualquer reforço piora. Se houver reforço, que seja **de fundamental existente** (60–90 Hz), nunca
  oitava abaixo da tônica do sub.
- Todo drive em caminho paralelo deve ter **HP ≥120–150 Hz**; o fundamental fica intocado.
- Medir a banda do grupo antes/depois: **55–75 Hz não pode subir**; se subir, o drive está entrando no fundamental
  e a resposta é reduzir o drive, não compensar com EQ.

### Como não criar brilho metálico

- **LP ~1,8–2 kHz em todo estágio de drive**. O Roar/Saturator sem filtro gera harmônicos altos que leem como
  "metálico" — e a presença 2–4 kHz já costuma estar acima do corpus em sets de referência.
- **Drive baixo e dry/wet parcial**; feedback alto (se usar Roar) é a receita do brilho metálico.
- O **clipper** só ceifa picos: acima de ~3 dB de clipping ele começa a gerar buzz em 400–800 Hz — que é justamente
  o vale de 300–1.200 Hz virando "cartolina", não corpo.
- **Guarda de fase/mono:** depois da cadeia, conferir correlação abaixo de 120 Hz. Saturação pode gerar
  diferença lateral; se gerar, o bus precisa de Utility `Bass Mono`/Width 0 abaixo de 120 Hz.
- **Não tocar o groove:** nenhuma etapa desta cadeia muda posição de nota. O risco ao groove é **dinâmico** —
  compressor/limiter achatando os ghost notes. Se depois da cadeia os eventos deslocados ficarem menos audíveis, o
  problema é redução de ganho, não timing.

## Prioridade e esforço

**Prioridade: alta (P0) para quem tem o diagnóstico certo.** O vídeo ataca o coração do motor (kick+baixo como
grupo) e a parte reaproveitável (drive band-limited + clipper antes do limiter) ataca o vale de 300–1.200 Hz.

**Esforço: médio.** O desenho do bus é simples, mas quatro dos nove estágios do vídeo são plugins de terceiros
(Weiss EQ, Virtual Mix Rack, Soothe 2, Bass Low Extender) e um deles (Soothe) **não tem equivalente nativo exato**.
O trabalho real é: (a) montar o rack de drive paralelo com HP/LP; (b) substituir o Soothe por EQ estático +
Multiband Dynamics; (c) **medir** 55–75 Hz, 300–1.200 Hz e redução do limiter antes/depois. Sem medição, a cadeia
pode "soar melhor no fone" e piorar o grave no PA.

## Trechos de prova

**sem legenda.** O vídeo não possui faixa de legenda automática nem manual (saídas do `yt-dlp` no topo deste
arquivo). Não existe nenhum timestamp de fala para citar — citar qualquer um seria invenção.

Como prova documental, seguem **três trechos literais da descrição oficial** (não são legenda), com o timestamp do
capítulo correspondente:

**1. O objeto do vídeo é o grupo kick+baixo (descrição; capítulo `EQing`, 02:54):**

> "If you want to produce techno at a high level, having a well-functioning kick and bass group is absolutely
> essential."

**2. O objetivo declarado é colar os dois (descrição; capítulos 02:54–14:55):**

> "To help you effortlessly glue kick and bass in your future sessions, Björn Torwellen has compiled his tricks for
> you in a video!"

**3. É uma cadeia de processamento, não um preset (descrição; capítulos 02:54–14:55):**

> "Take your time exploring his processing chain and let Björn guide you through the concept behind his mixing
> approach."

**Ordem da cadeia (metadado `chapters`, verbatim):** `EQing` 174 s · `Transformer` 313 s · `Roar` 327 s ·
`Weiss EQ` 481 s · `Bass Low Extender` 544 s · `Virtual Mix Rack` 599 s · `Soothe 2` 625 s · `Clipper` 655 s ·
`Limiter` 749 s · `Summary` 895 s.

## Limites e o que NÃO foi verificado

- **Não há fala transcrita.** Nenhum valor de parâmetro, frequência de corte, ordem de sinal, quantidade de drive,
  ceiling ou redução de limiter foi ouvido/lido. Todo número neste mapa é `HIPÓTESE` de engenharia, marcada como
  ponto de partida — não é do vídeo.
- **Não se sabe qual "Roar"**: pode ser o device nativo do Live 12 ou um plugin homônimo. A tradução cobre os dois.
- **Não se sabe se a cadeia é toda no bus do grupo** ou se parte dela está nos canais de kick e baixo
  separadamente. A descrição fala de "kick and bass group", o que sustenta a leitura de bus — mas é `INFERÊNCIA`.
- **Soothe 2 não tem equivalente nativo exato**; a substituição proposta (EQ estático + Multiband Dynamics) é
  aproximação, não paridade.
- **Não houve render, escuta, A/B nem medição de áudio na elaboração deste estudo.**
- As metas de "não subir 55–75 Hz" e "correlação ≥0,98 abaixo de 120 Hz" são metas de engenharia do contexto
  psytech, não resultados medidos aqui.
