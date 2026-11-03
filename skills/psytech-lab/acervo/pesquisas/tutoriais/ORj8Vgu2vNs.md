# Pspiralife Tutorial - Zenonesque Sensient-Style Part 1

**Ficha:** YouTube `ORj8Vgu2vNs` · canal **Pspiralife Music & Education** · 1:11:25 · publicado 2024-09-17.
**temLegenda:** `true` — legenda automática em inglês obtida com `yt-dlp --write-auto-subs --sub-langs en --convert-subs vtt` (7.344 linhas). Todos os timestamps abaixo são da legenda automática (início do bloco); a caixa é única e as citações são literais, inclusive erros de transcrição marcados com `[sic]`. Ruídos de legenda (`[music]`, `[clears throat]`, `[snorts]`) foram removidos das citações e estão indicados onde mudam o sentido.

**O que este vídeo NÃO é:** é uma sessão de composição ao vivo (ele mesmo diz que é "unscripted" na descrição), não uma aula de síntese. Ele **não** desenha kick, sub ou baixo do zero — trabalha com samples de packs. Portanto este mapa extrai **arquitetura de arranjo e colocação**, não receita de timbre. Isso está declarado de novo na seção de prioridade.

---

## Técnica ensinada (2-4 frases)

A técnica central é **arquitetura de repetição em camadas**: montar o track combinando loops curtos (1 compasso / 4 compassos) com loops longos (8/16/32 e às vezes 64 compassos) — "the short loops are more engaging for the body and the long loops are more engaging for the mind" [00:02:42–00:02:51]. Por baixo disso, ele trata kick+baixo como **uma única célula de 1 beat** ("it's actually a one beat loop" [01:06:21]) e replica essa célula, variando pelas bordas (encurtar o 1º e o 3º bloco de um loop de 4 compassos dentro do de 8 [00:13:00–00:13:19]).

O resto é **colocação, não timbre**: "I'm not too worried about specific sounds. It's more about placement" [00:25:48–00:25:51]. Ele sustenta isso com três gestos concretos: cortar graves do **side** até ~300 Hz para o sample não disputar com kick/baixo [00:20:17–00:20:19]; inverter + fade antes do acento para o som "já soar familiar" quando o acento chega [00:28:40–00:29:32]; e entrar com hat offbeat/percussão só quando a seção precisa progredir [00:46:55–00:47:03] e [00:54:12–00:54:16].

---

## Ferramenta usada no vídeo (plugin/stock)

- **DAW: Ableton Live.** Ele declara: "But I'm using Ableton because I'm thinking of you guys and most of you use Ableton" [00:09:01–00:09:06]. A versão exata não é dita na legenda — **NÃO VERIFICADO**.
- **Bitwig aparece só como DAW de costume dele**, não como dependência do método: "In Bitwig, you can just search for any function and it comes up" [00:08:45–00:08:47]. Ele está reclamando da diferença entre as duas, não ensinando Bitwig.
- **Nenhum plugin de terceiros é nomeado na legenda.** O que se vê descrito é stock: fades de clip e split (`E`) [00:09:34], `consolidate` [00:06:13], warp/estiramento com o BPM original declarado — "Maybe I need to set it to what it's written at" [00:53:44–00:53:46] —, EQ [00:22:38] com corte de graves no side [00:20:17], Compressor com sidechain [00:43:41–00:44:20], Reverb com automação de wet/dry — "with automation of the wet dry" [00:15:44].
- **Fonte do material: sample packs.** Ele cita "a different pack from March 2020" [00:26:02–00:26:04] e um baixo já pronto "additive sign base in C" [00:03:33] (`sign` = `sine` na legenda automática). Os samples vêm normalizados e ele corrige no master: "they're all playing at full volume, which is not good practice" [00:27:38–00:27:41].
- **Não há ANA 2, VELA, SideKick, Kick 3 nem Bitwig no fluxo.** A dependência real é Ableton Live + samples.

---

## Tradução para ambiente comum: Serum 2 (tem GranularOsc nativo), Diva, Vital, Massive X, Surge XT, Kontakt 8 (bibliotecas acústicas/orgânicas), Live 12 nativo (Simpler/Sampler/Grain, Operator, Echo, Hybrid Reverb, AutoPan, Shifter)

**Conclusão: traduzível a 100%, e sem fricção — o vídeo já é Ableton.** Nenhum plugin ausente é usado. Onde ele usa sample, o substituto é uma escolha do material, não uma limitação:

| O que o vídeo faz | Equivalente real |
|---|---|
| Loop de sample em áudio, split/fade/consolidate, warp | **Live 12** — timeline de Arrangement, clip fades, warp modes, `Consolidate`. Idêntico. |
| Amostra atmosférica longa, com corte de graves | **Live 12 Simpler/Sampler** ou **Serum 2** (playback de sample, mantém o caráter do one-shot) ou **Kontakt 8 / Ethereal Earth / LOOP GARDEN** para textura contínua. |
| Reverse + fade antes do acento | **Live 12**: inverter o clip (ou Simpler em reverse) + fade in. Em **Serum 2**, inverter o áudio antes de carregar no playback de sample — verificar se o modo granular expõe reverse. Mesmo gesto. |
| Corte de graves no side até ~300 Hz | **Live 12 EQ Eight em modo M/S**, high-pass no canal **Side** a ~300 Hz; alternativa de mesmo conceito: **Utility → Bass Mono** (mono abaixo de uma frequência). |
| Sidechain suave | **Live 12 Compressor** com sidechain do kick: "just a slower release and a higher threshold and a gentler ratio" [00:44:43–00:44:51]. |
| Intro filtrada até o drop do compasso 17 | **Live 12 Auto Filter** (ou filtro do **Serum 2/Diva**) automatizado no grupo de graves. |
| Percussão orgânica de resposta | **Rubber Bridge Guitar** / one-shots de madeira no **Simpler**; **Surge XT** ou **Diva** para stab filtrado. |

**O que o vídeo não cobre e não deve ser inventado a partir dele:** síntese de kick, desenho de sub, e o rolling de baixo. Nesses pontos o vídeo só entrega o **pareamento** ("there should be a kick in there that is designed to go with that" [00:04:20–00:04:26]) e a **unidade de 1 beat** — o timbre continua sendo decisão do material.

---

## Aplicação por função

Contexto de contraste citado no levantamento original: low-end mono, groove com subdivisões deslocadas do grid a preservar, meio 300–1.200 Hz em −4,83 dB e 1.200–4.000 Hz em −5,76 dB contra a média de 6 referências (set de referência). **O vídeo está em 132 BPM** e em **C** [00:03:33] — e ele chega a testar 128 e rejeita: "That's 128. I don't want to go that slow. I want to be in the sort of mid30s" [00:03:48–00:03:52]. Não copiar BPM nem tônica; o que se importa é a arquitetura. A divergência de andamento fica registrada como gosto do autor do vídeo, não como recomendação de mudança de BPM.

| Função | O que o vídeo entrega (com timestamp) | Como aplicar |
|---|---|---|
| **Kick** | Não sintetiza. Dá o pareamento kick↔baixo [00:04:20–00:04:26] e remove o fade automático para preservar o clique [00:05:26–00:05:41]. | Tratar kick+sub+baixo como **uma célula de 1 beat fechada** [01:06:21]. O clique do kick é o evento que não se mexe ao replicar: variação só na borda do bloco, nunca dentro da célula. **Inf.** — o vídeo não dá receita de clique. |
| **Sub** | Só indiretamente: o corte de side até 300 Hz existe para o material lateral não competir com "low end of the kick and bass" [00:19:26–00:19:41]. | Manter o sub no **Mid** (mono, convenção do gênero) e aplicar o corte de side apenas em atmosferas/retornos/hats. Não usar o corte de 300 Hz como desculpa para mexer no miolo 300–1.200 Hz, que já está carente no exemplo medido. **Inf.** |
| **Baixo / rolling** | "Additive sign base in C" [00:03:33] + o par kick/baixo como loop de 1 beat [01:06:21]; cria um loop de 4 compassos **dentro** do de 8 e encurta o 1º e o 3º [00:12:30–00:13:19]. | Preservar o groove deslocado dentro da célula de 1 beat. A "variação" é de **bloco**, não de nota: replica-se o compasso e encurta-se/abre-se o bloco nas bordas, do jeito que ele faz no loop de 4 dentro do de 8. Não adicionar nota para "variar" — isso quebraria o groove. |
| **Hats / shaker** | "a high hat can come in or percussion just for the progressions sake" [00:46:55–00:47:03]; hat **offbeat** para criar movimento: "I'll do an offbeat eye hat. Something more repetitive" [00:54:12–00:54:16] (`eye hat` = `hi-hat`). | Entrada de hat como **marcador de seção**, não como camada de brilho. Escolher amostra escura/curta: a faixa 1.200–4.000 Hz já está carente no exemplo medido, e um hat metálico piora o diagnóstico em vez de corrigi-lo. **Inf.** O vídeo só fala de colocação. |
| **Percussão de resposta** | O conceito aparece como "column response" [00:59:05–00:59:12] (`call and response` na legenda) e é descrito como loop de **8 compassos**: "This little column response, if you could call it that" [01:06:05–01:06:09]. | A resposta é **rara e longa** (1 evento a cada 8 compassos), não um ping-pong a cada compasso. Isso é exatamente o que preenche o meio 300–1.200 Hz sem empilhar camadas: um único evento de madeira por bloco de 8. Não duplicar a resposta junto com o kick. |
| **Madeira** | Não nomeia instrumento; usa percussão sampleada e diz que "It's more about placement" [00:25:48–00:25:51]. | Usar **Rubber Bridge Guitar** ou one-shot de madeira no **Simpler** no papel de resposta de 8 compassos. Aplicar o mesmo critério de colocação (fora do tempo forte do kick) e nada de reverb longo — o vídeo usa reverb com automação de wet/dry [00:15:40–00:15:44], não reverb fixo. |
| **Stab** | "it's going to be a wobb like a ace wob stab" [00:59:22–00:59:27], colocado depois do acento [00:59:27–00:59:37]. | Stab curto e filtrado **depois** do acento, no fim da frase. Em **Diva/Surge XT/Serum 2** com filtro fechado; evitar abrir brilho em 1.2–4k porque esse é o buraco medido. **Inf.** |
| **Subida** | Reverse + fade **do próprio som que vai entrar**, não de um riser separado: "created like a reverse into that just to make it smoother and cooler" [00:28:40–00:28:45]; "makes it already sound familiar by the time that the accent happens" [00:29:20–00:29:32]. | Inverter o clip do elemento alvo (madeira, stab, atmosfera) e alinhar o fim do reverse no acento. Em **Live 12**: reverse de clip + fade in. Em **Serum 2**: inverter o áudio antes de carregar no playback de sample (verificar reverse no modo granular). Isso introduz o som "mais cedo" sem criar um elemento novo. |
| **Atmosfera** | Low cut no sample [00:19:26–00:19:41] **e** corte dos graves do side até ~300 Hz [00:20:17–00:20:19]; reverb com automação de wet/dry [00:15:40–00:15:44]. | Atmosfera entra **sem graves** e com wet automatizado (entra/sai por seção). É o único parâmetro de EQ com número no vídeo: ~300 Hz no side. Aplicar em **EQ Eight M/S** ou **Utility/Bass Mono** na atmosfera, nunca no bus de graves. |
| **Intro / drop no compasso 17** | "I want to make a simple intro so that it motivates me and gets me excited for the drop at bar 17" [00:06:24–00:06:31]; "filter time" [00:06:35]; "a simple intro is better than no intro" [00:06:47–00:06:55]. | A 128 BPM, 00:30 cai no compasso 17 (aritmética do grid: 1 compasso = 1,875 s) — o alvo coincide com o marco de 30 s. Intro = só filtro no motor (Auto Filter automatizado), sem elemento novo. Isso sustenta os 2 primeiros minutos sem engordar o sub. |

---

## Prioridade e esforço

**Prioridade: alta. Esforço: baixo-médio.**

Justificativa curta: não exige plugin novo, nem sound design, nem sample novo — é uma passada de **edição e estrutura** sobre material que já existe, e o alvo do vídeo (drop no compasso 17) é literalmente o marco de 00:30 a 128 BPM. O esforço é baixo porque as operações são todas nativas do Live 12; é médio (não baixo) porque exige disciplina de replicação célula-a-célula e conferência auditiva do groove deslocado depois de cada corte. **Limite honesto:** o vídeo não ensina o timbre do kick/sub/rolling, então ele **não** resolve o núcleo sonoro do motor — resolve a arquitetura dele. Para timbre, este vídeo não é fonte.

---

## Trechos de prova: 3 citações literais da legenda com timestamp

1. **[00:02:42–00:02:51]** — "the short loops are more engaging for the body and the long loops are more engaging for the mind."
2. **[00:20:17–00:20:19]** — "low frequencies from the side information up to about 300."
3. **[01:06:21]** — "it's actually a one beat loop." (contexto imediato: "we've obviously got a one bar loop with the kick and bass" [01:06:10–01:06:12])

*Citações adicionais usadas no corpo, todas literais da mesma legenda: [00:04:20] "there should be a kick in there that is designed to go with that"; [00:25:48] "I'm not too worried about specific sounds. It's more about placement."; [00:28:40] "created like a reverse into that just to make it smoother and cooler"; [00:44:43] "just a slower release"; [00:44:47] "and a higher threshold"; [00:44:51] "and a gentler ratio."; [00:54:12] "I'll do an offbeat eye hat. Something more repetitive."*
