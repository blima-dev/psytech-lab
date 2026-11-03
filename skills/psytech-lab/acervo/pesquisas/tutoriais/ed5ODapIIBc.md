# HOW TO MAKE TECHNO By Michael Nox & Robin Mind [Project Walkthrough]

> **id:** ed5ODapIIBc · **canal:** Vision Serpent · **publicado:** 2026-09-03 · **duração:** 16:10 · **tema:** motor-completo (walkthrough).
>
> **Fonte:** legenda automática EN obtida via yt-dlp (284 cues após limpeza de cabeçalho, tags `<c>`, cues de
> rolagem duplicados e linhas vazias). As citações mantêm o texto literal da ASR, inclusive disfluências
> ("um", "uh") e erros de transcrição; quando o erro muda o sentido técnico, ele é apontado. A descrição do
> vídeo confirma `#ableton`, `#psytech` e o walkthrough da faixa "Neon Pulse". **Áudio não escutado.**
>
> **Fontes consultadas:** o vídeo (legenda integral) + contexto de auditoria do set de referência (déficits de
> banda, low-end mono, largura do médio) + conhecimentos gerais de tônica/saturação citados no corpo.
>
> **Marcadores:** `[V]` literal da legenda com timestamp · `[C]` contexto de auditoria do set de referência · `[I]` tradução ou inferência, não afirmada no vídeo.

## Técnica ensinada (2-4 frases)

O vídeo ensina uma arquitetura de **camadas por banda com cadeias paralelas**: em vez de esculpir um único kick/baixo, cada região ganha uma via própria de processamento. O kick tem uma cadeia paralela só para o topo e outra só de reverb no médio [V 03:34–04:04]; o grave é dividido em low-end senoidal (~50 Hz) [V 05:16–05:42], um rolling de saw+square no médio, estereofônico e com sidechain [V 05:51–06:24], e um sample limitado a 70–240 Hz [V 07:48–07:51]. A regra que amarra tudo: sidechain no kick nas camadas de baixo que competem com ele e reverb sempre com low-end cortado [V 06:23; 07:07–07:14; 07:59–08:04], com filtro/automação para o material de topo entrar aos poucos na track [V 11:07–11:24].

## Ferramenta usada no vídeo (plugin/stock)

O processamento é **Ableton Live stock** [I, com base em `#ableton` na descrição e em "from Ableton" 10:33/10:44], com uma exceção: **OTT**, citado duas vezes [V 10:08; 15:17] — plugin de terceiros. A tabela abaixo usa o nome literal da legenda.

| Ferramenta (como a legenda diz) | Para quê no vídeo | Timestamp |
|---|---|---|
| Sample + cadeias paralelas + reverb + EQ | Kick: topo em paralelo, reverb só no médio, corte de topo/médio no seco | 03:23; 03:34–04:04; 04:16–04:29 |
| **Redux** | "sparkle"/harmônico digital no topo do mid bass; topo digital do sample de apoio | 06:39; 12:07; 14:18 |
| **Saturator** | Pós-processamento do sample; saturação do sample de apoio | 12:07; 14:28 |
| **Echo** | Stab, sample, laser e Reese | 10:50; 12:31; 13:31; 15:36 |
| **Auto Filter** | Automação para o stab "entrar"/evoluir na track | 11:07–11:24 |
| **Auto Pan** | Drop synth e laser | 09:43; 13:28 |
| **Pedal** | Topo do stab | 10:48 |
| **Resonator** ("res- resonator from Ableton") | Stab | 10:44 |
| **Phaser** + **Flanger** | Drop synth: centro do phaser movido por LFO + flanger | 09:34–09:46 |
| **Roar** (provável) | Drop synth ("a raw" 09:50) e Reese ("the roar" 15:21) | 09:50; 15:21 |
| **Multiband saturation** | Stab e laser | 10:58; 13:22 |
| **OTT** | Drop synth ("a big amount") e Reese | 10:05; 15:17 |
| **Wavetable / preset** | Stab ("Cyrus res preset from Ableton") e laser (posição da wavetable muda com a nota) | 10:33–10:39; 13:00–13:14 |
| **Reverb** (device não nomeado) | "Room" do kick/mid bass; espaço do build-up no laser | 03:59–04:04; 06:55–07:04; 13:40–13:51 |
| **Formant filter** (grafado "format filter") | Sample reverso, com automação para cada hit não soar igual | 12:15–12:27 |
| **Sample reverso** | Camada de transição/variação | 11:58–12:02 |

**Artefatos de ASR que importam para a técnica:**

- "re-space" [V 07:42; 08:55; 09:10] = **Reese**, confirmado pela própria legenda em "another Reese bass" [V 14:56].
- "Cyrus res preset from Ableton" [V 10:33] — não dá para afirmar o nome do preset; o que sobrevive é "é um preset de wavetable". Provável "Serum preset", mas **NÃO VERIFICADO**.
- "queuing" [V 04:16; 11:03] = **EQing**.
- "step" [V 10:22] = **stab**.
- "format filter" [V 12:15] = provável **formant filter**; a legenda não fecha o nome.
- "a raw" [V 09:50] / "the roar" [V 15:21] = provável **Roar**; a legenda não garante o device.

**O que o vídeo não cobre:** hats, shaker, clap, madeira, pad/atmosfera dedicado, master/mix bus e arranjo por seções. A legenda cobre kick, camadas de baixo, drop synth/Reese, stab, sample, laser e track de apoio. Há um "rhythm kick" filtrado, mas o vídeo o usa como camada de tensão, não como percussão de resposta — essa adaptação é inferência e está marcada. Não há base para traduzir hats, shaker, madeira ou pad deste vídeo.

## Tradução para ferramentas Live 12 / Serum 2

### Direto no Live 12

| No vídeo | Equivalente | Observação |
|---|---|---|
| Redux, Saturator, Echo, Auto Filter, AutoPan, Pedal, Resonator, Roar, Phaser/Flanger, Reverb | **Live 12 stock** (Redux, Saturator, Echo, Auto Filter, AutoPan, Pedal, Resonator, Roar, Phaser-Flanger, Hybrid Reverb) | Mesmos devices ou equivalentes diretos. |
| Wavetable do stab e do laser | **Serum 2** (também Vital, Massive X, Surge XT) | O laser depende de **modular a posição da wavetable enquanto a nota toca** [V 13:11–13:14]; no Serum 2, LFO/envelope → WT position. |
| Sample do kick, sample de apoio, sample reverso, camada 70–240 Hz | **Simpler / Sampler** | Reverse no Simpler; filtro/banda no Sampler para a camada 70–240 Hz. |
| Reverb de sala | **Hybrid Reverb** | Com HPF no retorno; o vídeo corta o low-end do reverb [V 07:07–07:14]. |
| Delay/eco | **Echo** | Nativo. |
| Largura/auto-pan | **AutoPan** e edição mid/side | O vídeo "adjusted the mid sides" [V 06:26–06:31] e "made it wider" [V 08:06–08:08]. |

### OTT — a única ferramenta fora do stock

**OTT** é um plugin de terceiros. Conceito: compressão multibanda agressiva que soma compressão **downward** (o que passa do threshold) e **upward** (o que fica abaixo do threshold), usada com mix alto (wet) para deixar o som "denso e presente" — o vídeo diz "a big amount of OTT" [V 10:05] e "with this OTT" [V 15:17]. Equivalente no Live 12: **Multiband Dynamics** (Above/Below por banda) ou um Audio Effect Rack de 3 bandas com Compressor; **não é idêntico**, mas reproduz o conceito de nivelar bandas separadamente. Não é necessário para um motor básico.

### O que o vídeo não usa

- **GranularOsc do Serum 2:** não há nenhum momento granular no vídeo. Não forçar uso.
- **Diva, Vital, Massive X, Surge XT:** podem gerar o saw+square do rolling, mas o vídeo não depende deles; o que importa é o processamento por banda, não o synth.
- **Grain, Operator e Shifter (Live 12):** o vídeo não usa granular, FM nem frequency shifter; o laser é wavetable [V 13:00–13:14] e o movimento vem da posição da wavetable, não de síntese granular/FM. Sem papel aqui.
- **Kontakt 8 (Rubber Bridge Guitar, LOOP GARDEN, Ethereal Earth, Vintage Organs):** nenhum instrumento acústico/orgânico aparece na legenda. Sem papel neste vídeo.
- **ANA 2, VELA, SideKick, Kick 3, Bitwig:** nenhum é citado ou necessário. O processamento é Ableton stock + OTT; as fontes são samples e presets de wavetable.

## Aplicação por função

**Contexto medido [C]:** num motor de referência a 128 BPM, o low-end é mono e o groove usa subdivisões deslocadas fora do grid, a preservar. A auditoria contra 6 referências mediu **300–1.200 Hz em −4,83 dB** e **1.200–4.000 Hz em −5,76 dB**; o mesmo estudo mediu o meio 400 Hz–2 kHz com **side/mid de −21,90 dB** contra **−3,52 dB** das referências — ou seja, o médio está baixo **e** muito mais fechado. A leitura desse estudo é que o buraco útil é corpo médio/presença, **não adicionar sub indiscriminadamente** [C]. Consequência: a tradução deste vídeo **não é "adicionar mais camadas de grave"**; é aplicar o processamento por banda nas camadas que já existem e abrir espaço antes de somar qualquer coisa.

### kick

**O vídeo faz:** sample; cadeia paralela só para o topo [V 03:34–03:39], outra cadeia paralela só de reverb no médio "to put it in a room" [V 03:59–04:04]; no seco, corta um pouco de topo e de médio [V 04:24–04:29].

**Como aplicar [I]:** no kick existente, criar dois returns em paralelo. (a) Topo: HPF acima do corpo (começar em ~2 kHz) e processar transiente/saturação só nessa faixa. (b) Médio: enviar para o Hybrid Reverb com HPF ~300–500 Hz e LPF ~5–6 kHz, retorno baixo, 100% wet no return. No kick seco, cortes pequenos de topo e médio. O grave direto fica intocado e mono.

**Por que não engorda o sub:** o reverb recebe só o médio, exatamente como no vídeo; o topo paralelo não devolve energia abaixo do HPF. Os valores de crossover **não estão no vídeo** — ele só diz "top end / low end" e "mid part". São ponto de partida [I], não receita do autor.

### sub

**O vídeo faz:** um rolling "only the low frequency and more or less a sine wave" [V 05:16–05:20], com "50 hertz. Maybe." [V 05:42–05:43].

**Como aplicar [I]:** não criar uma segunda camada de sine por cima do sub existente. Manter o sub puro: sem reverb, sem Redux, sem width, mono abaixo de ~120 Hz; e sidechain no kick, como o vídeo faz nas camadas de baixo [V 06:23]. O "50 Hz" do vídeo **não é um alvo universal**: a fundamental de sub depende da tônica (se a tônica for C#, cai por volta de 69 Hz, com corpo em ~138 Hz [I]). O que se copia é o princípio "sine, só low-end", não a frequência literal.

### baixo/rolling

**O vídeo faz:** um "classic rolling bass" com "more notes", "more in the mid part of the bass" [V 05:51–06:01], "more in the stereo field" [V 06:05], feito de "saw wave" + "square" [V 06:15–06:17]; sidechain no kick [V 06:23]; mid/side ajustado [V 06:26–06:31]; topo fechado [V 06:34]; Redux para "sparkle"/"digital harmonic feeling" [V 06:39–06:49]; reverb de sala com low-end removido [V 06:51–07:14]; automação de volume [V 07:19]. Há ainda um sample de "upper bass region" limitado a "70 hertz to 240 hertz" [V 07:26–07:51], alargado [V 08:06–08:08] e sidechained para não competir com o kick [V 07:59–08:04].

**Como aplicar [I]:** antes de somar um rolling novo, medir a densidade do baixo existente. Usar as partes do vídeo que corrigem o que está medido:

- **Mid/side e largura:** alargar somente acima de ~150 Hz, mantendo mono abaixo disso. Quando o side/mid do médio está muito abaixo das referências [C], há espaço — mas o sub não pode ser a fonte da largura.
- **Sidechain e automação:** sidechain no kick e automação de volume nos bolsos que já existem, preservando as subdivisões deslocadas do groove — não re-quantizar para 16 avos retos.
- **Reverb:** send com HPF ~300–400 Hz e LPF ~4–6 kHz [I], exatamente pelo motivo que o vídeo dá: "in the reverb we removed of course the low end ... so it don't ... get gets too muddy" [V 07:07–07:14].
- **Redux:** **não usar no baixo principal.** Medições de referências do estilo (Fox, AlpaKa, Zenon) mostram pouca energia de baixo acima de 300–400 Hz [C]; Redux gera harmônicos digitais/alias acima do conteúdo original, justamente onde o baixo deve ficar limpo, e produz o brilho metálico que o estilo rejeita. Se for usado, só em paralelo, numa banda de topo (>~1,5 kHz) e com mix baixo.
- **Camada 70–240 Hz:** mapeia o "corpo" da tônica (ex.: em C#, ~138–207 Hz [I]). Se o low end do projeto já estiver bem coberto, usar essa camada como **substituição** de uma camada existente, nunca como soma por cima.

**Onde o vídeo conflita com o que costuma ser medido:** ele pede "more notes" no rolling; em referências do estilo a densidade de baixo costuma ser menor, e sets minimalistas já rodam rolling denso (7–8 notas/compasso) [C]. Copiar a densidade do vídeo agravaria o mascaramento. Copiar a **separação de bandas, o mid/side e o sidechain**, não a quantidade de notas.

**Drop synth / Reese (fora das funções de um motor básico):** o vídeo trata o drop synth como um Reese em duas camadas, com phaser movido por LFO, flanger, provável Roar, OTT e corte de low-end para não brigar com kick/baixo [V 08:55; 09:31–10:19]. O que se aproveita é a regra de cortar o low-end de qualquer camada de topo [V 10:10–10:19] e a de não competir com kick/baixo.

### hats/shaker

**O vídeo não aborda.** A legenda não menciona hats, shaker, pratos ou percussão de topo. Sem base para traduzir deste vídeo; não inventar receita. O único princípio adjacente é o processamento de topo do kick, que não se aplica a hats.

### percussão de resposta

**O vídeo faz:** um "rhythm kick", "in general the same sample, but filtered. We removed a little bit of the lower end and ... a good amount of the high end" [V 04:34–04:45], tocado junto com o kick normal [V 04:48–04:51] para "increase the ... tension of the ... bass part of the second part" [V 04:58–05:05].

**Como aplicar [I]:** é o elemento mais transferível. Construir um **ghost kick só de médio** a partir do mesmo sample do kick: band-pass aproximadamente 300 Hz–2 kHz, sem low end, sem sub. Colocar apenas nos slots de resposta, seguindo as posições deslocadas do groove. Ele preenche 300–1.200 Hz sem dobrar o sub e sem competir com o fundamental do kick. O vídeo usa o rhythm kick para tensão na segunda parte; usá-lo como percussão de resposta é adaptação, não instrução dele.

**Cuidado:** não colocar em todos os 16 avos. Se o low end do projeto já cobre todas as posições [C], a camada tem de ser chamada/resposta, não cama.

### madeira

**O vídeo não aborda.** Nenhum instrumento de madeira, orgânico ou acústico aparece na legenda. Sem base para traduzir deste vídeo. O Kontakt 8 não tem papel aqui.

### stab

**O vídeo faz:** preset de wavetable [V 10:22–10:39], Resonator [V 10:44], Pedal no topo [V 10:48–10:50], Echo e reverb [V 10:50–10:53], multiband saturation [V 10:58], EQ [V 11:03] e Auto Filter com automação "to blend the ... sound into the track", para não ter "the full ... presence in the beginning" e "evolves ... in the track" [V 11:07–11:24].

**Como aplicar [I]:** Serum 2 (ou Vital/Massive X) com patch de wavetable; Live 12 Resonator + Pedal + Echo + Hybrid Reverb; saturação multibanda em rack (Saturator/Roar por banda); Auto Filter com automação abrindo ao longo dos compassos. É o candidato natural para 1.200–4.000 Hz, mas **não corrigir o déficit com boost de EQ**: usar a abertura do Auto Filter e saturação modesta acima de ~1,2 kHz. Nada de Redux no stab. HPF no stab para não somar sub.

**Ressalva de ASR:** "Cyrus res preset from Ableton" [V 10:33] não identifica o preset; provável "Serum preset", **NÃO VERIFICADO**. A técnica sobrevive sem o preset: wavetable + os processamentos listados.

### subida

**O vídeo faz:** laser de wavetable em que "position of the wave table is changing" enquanto a nota toca [V 13:00–13:14], com multiband saturator, AutoPan, Echo e reverb [V 13:22–13:33]; o reverb "Fill the space in the build-up" [V 13:40–13:51]. Há também um sample reverso com Saturator, Redux no topo digital, provável formant filter automatizado para "don't sounds every hit the same" e Echo [V 11:58–12:35]. Há ainda um track de apoio que só toca na última nota do laser: um sample de baixo com Redux, saturação/EQ repetidos e widening [V 13:56–14:45].

**Como aplicar [I]:** no Serum 2, LFO/envelope → posição da wavetable; AutoPan + Echo + Hybrid Reverb com wet automatizado só nos últimos compassos antes do drop. Para a variação, reverter um sample no Simpler, automatizar um filtro formântico (a legenda diz "format filter", sem nomear o device) e mandar Echo. HPF em tudo para a subida não engordar o sub. Redux aqui é menos arriscado que no baixo, porque o material é de transição — mas ainda é opcional.

### atmosfera

**O vídeo não tem faixa de atmosfera dedicada.** O "room" vem do reverb mid-only no kick [V 04:04] e do reverb no mid bass [V 06:55–07:04], ambos com low-end removido; o laser usa reverb para preencher o build-up [V 13:51].

**Como aplicar [I]:** implementar atmosfera como **send/return**, não como nova camada de grave. Hybrid Reverb no return com HPF ~300–400 Hz e LPF ~5–6 kHz, alimentado pelo médio do kick, pelo médio do baixo e pelo stab; automatizar o wet nas transições. Se o motor precisar de pad, este vídeo não dá receita — está fora do material dele.

### Guardrails de tradução

| Risco | Regra |
|---|---|
| Engordar o sub | Nenhuma camada nova de sine por cima do sub existente. Nada de reverb, width ou Redux abaixo de ~120 Hz. |
| Brilho metálico | Redux fora do baixo principal; se usar, só paralelo, banda >~1,5 kHz, mix baixo. Preferir Auto Filter e saturação de banda para 1.200–4.000 Hz. |
| Mascarar o groove | Nada em grade reta; respeitar as posições deslocadas do groove. Sidechain no kick nas camadas que competem com ele. Não encher os 16 avos. |
| Embolar o médio | Todo reverb com HPF; LPF no retorno; um dono por banda (sub, corpo, médio, topo). |

## Prioridade e esforço

**Prioridade: média · Esforço: médio.**

Não traz um conceito novo de motor, mas traz **exatamente** o tipo de processamento que a auditoria pede — separar topo/médio do kick, limitar banda do baixo, alargar o médio e usar sidechain. O valor maior não está em recriar o stack inteiro de baixo do vídeo (que conflita com a densidade medida), e sim em aplicar as cadeias paralelas nas camadas existentes.

| Item | Prioridade | Esforço | Justificativa |
|---|---|---|---|
| Kick: topo paralelo + reverb mid-only | **alta** | **baixo** | Duas cadeias, nenhum low end novo; ataca sala e topo sem tocar no sub. |
| Rhythm kick só de médio | **alta** | **baixo** | Preenche 300–1.200 Hz e cria resposta sem dobrar sub; preserva o groove deslocado. |
| Mid/side no rolling acima de ~150 Hz | **alta** | **médio** | Quando o side/mid do médio está muito abaixo das referências [C], é o maior ganho de largura. |
| Camada 70–240 Hz | **média** | **médio** | Mapeia o corpo da tônica (ex.: C# ~138–207 Hz [I]), mas se o low end já está coberto, só como substituição. |
| Stab com Resonator + Auto Filter | **média** | **alto** | Ataca 1.200–4.000 Hz, mas exige cadeia longa e automação; risco de brilho se exagerar. |
| Redux/OTT como polimento | **baixa** | **médio** | O vídeo usa para "digital top"/densidade; no baixo do estilo o Redux é contraindicado e o OTT não é nativo. |
| Hats/shaker/madeira/atmosfera-pad | **sem base** | — | O vídeo não aborda; não traduzir deste material. |

## Trechos de prova

1. **00:03:34.800 → 00:03:47.120** — *"I added a parallel chain to / um process the the top end separately / from the / low end."* (cues consecutivos, concatenados; "um" é disfluência literal).
2. **00:03:59.680 → 00:04:04.720** — *"um reverb on the mid part of the kick to / put it in a room."*
3. **00:05:16.160 → 00:05:20.080** — *"it's only the low frequency / and more or less a sine wave."*
