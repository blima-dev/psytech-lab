# Syncopation and Grooves

- **Canal:** Sonic Academy
- **URL:** https://www.youtube.com/watch?v=iWOPUHKbJjI
- **Tema:** groove / síncope
- **Legenda:** automática em inglês, lida integralmente — citações literais com timestamp
- **Natureza do vídeo:** aula de síncope aplicada no piano roll e em moduladores; toda afirmação técnica abaixo tem trecho literal da transcrição; o que é proposta do estudo está marcado como **proposta**.

## Técnica ensinada (2-4 frases)

A técnica é criar síncope mudando a **grade interna** do material, não a quantidade de elementos: o vídeo define síncope como "it essentially means to highlight notes that fall outside of the standard beat that you're working in" (00:32.920–00:39.110) e demonstra a mesma frase em 4/4 com semínima pontuada, colcheia pontuada e tercinas — "Let's change that to a quarter dotted" (04:23.040–04:28.130), "eighth dotted" (04:31.040–04:40.110), "triplets" (04:40.120–04:47.750) — concluindo que "there's no reason to stay within one time signature for an entire bar of music" (04:55.360–05:03.750). O mesmo resultado aparece sem nota nova: uma nota sustentada com o filtro modulado por LFO sincronizado a tercina ou colcheia pontuada (06:49.200–06:56.160) já soa sincopada (06:59.400–07:07.870), e encurtar o loop do clipe gera polimetria, "constantly shifting out of time" (07:39.160–07:53.790). O fecho é explícito: o groove vem de "mixing and matching all these different time signatures, start points, phase points" (14:30.760–14:36.870) e de "shift and bend off the axis of the standard boring beat" (14:36.880–14:41.870).

## Ferramenta usada no vídeo (plugin/stock)

Bitwig Studio, com o som de teste no Polymer — "I'll take just the default sound from polymer" (02:04.520–02:05.750) — e os moduladores nativos do Bitwig (Phase, Random), além do piano roll, do comprimento de loop do clipe e do fatiamento de áudio. O vídeo nomeia o DAW duas vezes: "in Bitwig it's really easy to do this" (07:31.240–07:32.630) e "of course with Bitwig, this kind of thing is great" (13:04.280–13:06.150). Não usa plugin de terceiros; a legenda também capta "polymorph aperture" (11:27.560) como nome de preset, não confirmado.

## Tradução para ambiente comum: Serum 2, Diva, Vital, Massive X, Surge XT, Kontakt, Live 12 nativo

O vídeo não depende de plugin específico: as operações são grade, loop, LFO, fase e fatiamento. O pré-requisito real é o conceito; tudo tem equivalente no Live 12 ou em qualquer synth com LFO sincronizado.

| Operação no vídeo | Equivalente em ambiente comum | Limite/observação |
|---|---|---|
| **Grade pontuada / tercinas** | Live 12: piano roll com grade de tercinas e posicionamento manual em múltiplos de 3/16 para a colcheia pontuada (1 colcheia pontuada = 3/16 = 0,75 beat). O vídeo mostra o resultado: "the fourth 16th here for example third 16th second 16th and then back onto the beat there again" (03:03.600–03:10.630). | Não é preciso plugin. A grade resolve tercinas; a pontuada é aritmética de 3/16. |
| **Loop mais curto que o compasso (polimetria)** | Live 12: `Loop Start` / `Loop Length` do clipe, em beats, não em compassos. Um loop de 7/16 ou 13/16 dentro do projeto 4/4 reproduz o "shifting out of time" (07:39.160–07:53.790). Vale para MIDI e áudio; para textura, o loop do Simpler/Sampler. | Não muda o tempo do projeto; é o loop do clipe. O vídeo chama de "polyrhythm effect", mas antes corrige o termo para polymeter (07:09.680–07:16.390). |
| **LFO sincronizado a tercina / colcheia pontuada** | Serum 2: LFO com Rate sincronizado e valores pontuados/tercina. Vital, Massive X e Surge XT têm LFO com sync; Diva usa o LFO sync do patch. No Live 12, o LFO do Auto Filter com Rate sincronizado. | O alvo é o **filtro**, não o volume. Não usar no sub. |
| **Fase de 45°** | Não há um "Phase" universal: deslocar a nota/start do clipe pelo equivalente (45° = 1/8 do ciclo), desenhar a curva do LFO deslocada, usar `LFO Delay` ou, em áudio, o offset do sample. O vídeo mostra o filtro mais brilhante saindo do tempo principal (12:13.480–12:19.950; 12:26.640–12:37.630). | O resultado é o mesmo deslocamento; "45°" é o que ele diz, não uma unidade que exista em todo plugin. |
| **Random modifier** | Live 12: MIDI Tools (Generate/Transform) para gerar variações, ou escrever 2–3 variantes de 1 compasso e alternar. O próprio vídeo admite que as últimas ficaram "a little bit extreme" (14:26.240–14:28.990). | Random total raramente serve ao hipnotismo do gênero; curar manualmente. |
| **Fatiar e atrasar seções** | Live 12: Split no Arrangement + nudge de cada fatia; ou Simpler em Slice, cortando e deslocando a fatia. | Funciona melhor com material próprio; recortar referência de artista não é o escopo deste estudo. |
| **Kick deslocado** | O vídeo usa o kick como exemplo (01:25.600–01:29.430; 01:48.680–01:53.990), mas em psy o kick 4x4 é âncora. Aqui o princípio vira **omissão** nos vácuos, não deslocamento do kick. | Mover o kick em psy cria colisão com sub/baixo rolling e destrói o pocket. |

**Conclusão:** traduzível. As três peças sem knob direto (Phase, Random, slice) têm equivalentes por offset de nota, curva de LFO deslocada/MIDI Tools e edição de Arrangement.

## Aplicação por função (guardrails gerais, **proposta**)

O vídeo opera em duas escalas que não podem ser confundidas: **(a) grade macro** de 3/16 (colcheia pontuada) e tercinas, que muda onde a nota cai; **(b) microtiming** do pocket (deslocamentos de poucos milissegundos sobre o 16º já existente). A síncope do vídeo é macro; microtiming de groove é outra camada. Regra proposta: **não mexer no pocket de sub/baixo; aplicar a grade macro só nas camadas de resposta e em modulação.**

Nota acústica (**proposta**): a síncope **não cria energia de médio por si só** — ela redistribui os eventos que já têm médio (madeira, percussão, clique do kick). Não usar hat/shaker mais alto nem serra metálica para "aparecer" no meio.

| Função | Como aplicar | Guardrail |
|---|---|---|
| **Kick** | Não deslocar o 4x4. Aplicar a ideia do vídeo como **omissão**: manter os vácuos já escritos e deixar madeira/percussão preencher; se precisar de um respiro novo, 1 tempo isolado, nunca um ghost kick. | Sem ghost kick novo; mover o kick em psy colide com sub/baixo. |
| **Sub** | **Não aplicar síncope.** Manter a tônica, curto, mono. A síncope do vídeo fica acima dele. | LFO/amplitude no sub = beating e "tapete"; o vídeo não fala de sub. |
| **Baixo / rolling** | (a) LFO 1/8D ou 1/8T no filtro de uma **via paralela HP ≥300 Hz** do próprio synth, com uma nota sustentada bem baixa e o padrão rítmico intacto — "playing a single note" / "filter modulate outside of the regular beat" (06:59.400–07:07.870). LFO em modo mono (instância única, sem retrigger por nota). (b) Opcional: em **um** compasso de resposta por frase, trocar a grade para 3/16 ou tercina. | Fundamental intacta; LFO só na via de médios. Nunca no sub. A opção (b) mexe no groove → só com A/B de 8 compassos. |
| **Hats / shaker** | Polimetria no loop do clipe: 7/16, 13/16 ou 3/8 — testar o que rotaciona sem criar buracos — mantendo a grade de 16avos e os acentos. Alternativa: deslocar 2–3 acentos para o 4º/3º 16º (03:03.600–03:10.630). | Não subir nível, não trocar sample por um mais brilhante, não aumentar densidade. O ganho é rítmico. |
| **Percussão de resposta** | 2–3 hits por frase em 3/16 (colcheia pontuada), criando a rotação 4º→3º→2º 16º que o vídeo mostra. É o melhor lugar para a grade macro. | Não encher; deixar o resto respirar. Evitar colidir com os eventos do sub/baixo. Transiente de percussão ataca 1,2–4 kHz sem synth metálico — não confundir com "mais brilho". |
| **Madeira** | Mover **uma** resposta por frase para colcheia pontuada ou tercina, com o mesmo timbre e as mesmas notas. Nos vácuos de kick, a madeira sincopada preenche sem competir. | Sem camada nova, sem reverb longo, sem EQ de brilho. Evitar cair no mesmo 16º dos eventos de sub/baixo. |
| **Stab** | Deslocar **um** stab curto para o 4º 16º antes do tempo ou para uma tercina, como puxão de resposta. Manter decay curto. | Não empilhar acorde nem abrir topo; stab é resposta, não preenchimento. Sem delay/reverb que esmague o grave. |
| **Subida** | Manter a trajetória de pitch monotônica; aplicar a ideia de fase/tercina no **LFO do filtro** nos últimos 2 compassos, ou atrasar o início do movimento em 1/16. | Nada de troca aleatória de time signature (perde direção). Intensidade por movimento, não por brilho. |
| **Atmosfera** | Polimetria em textura: loop de 7/8, 13/16 ou 15/16 num pad/drone escuro, high-passed, para derivar contra o 4/4. Em motor granular, o offset/scan de grão é a ponte possível para "start points" — **inferência**, não é o que o vídeo ensina. | Nada de conteúdo novo abaixo de 300 Hz; a atmosfera não pode virar cama de sub. Sem brilho metálico. |

**Roteiro de teste sugerido (A/B, 8 compassos por vez, em volume casado):**

1. Madeira + percussão em 3/16 nos primeiros compassos de frase. Comparar com o atual e conferir que o pocket de sub/baixo não mudou.
2. LFO 1/8T e 1/8D na via HP ≥300 Hz do baixo, nota única, 8 compassos. Medir 300–1.200 Hz e 1.200–4.000 Hz; conferir 30–120 Hz e correlação mono intactas.
3. Stab deslocado; shaker em polimetria 7/16 só se 1–2 passarem.
4. Atmosfera por último; não tocar na assinatura de abertura da faixa.

**O que não fazer:** mover o kick principal; sincopar o sub; subir o shaker ou trocar por sample mais brilhante; preencher todos os compassos com a grade nova; tratar síncope como conserto de EQ — ela não substitui fonte de médio.

## Trechos de prova

1. `00:32.920–00:39.110` — "it essentially means to highlight notes that fall outside of the standard beat that you're working in." (definição de síncope; base de tudo)
2. `06:59.400–07:07.870` — "playing a single note but you're still achieving that syncopated groove by having the filter modulate outside of the regular beat that you're using." (o truque que cabe no groove sem nota nova)
3. `07:39.160–07:53.790` — "change the length of our loop to something shorter. So that when we continue to loop this we're getting this polyrhythm effect and it's constantly shifting out of time now." (polimetria; base do shaker/atmosfera. Ele chama de "polyrhythm effect" aqui; antes havia corrigido o termo para polymeter, 07:09.680–07:16.390)

## Limites do estudo

- Estudo baseado na transcrição (legenda automática); sem escuta do áudio.
- Os rótulos exatos das divisões pontuadas/tercinas no Auto Filter do Live 12 não foram confirmados — se não existirem como sync, usar Hz equivalentes (a 128 BPM: 1/8D ≈ 2,84 Hz; 1/8T ≈ 6,4 Hz; 1/4T ≈ 3,2 Hz, aritmética).
- O vídeo não mostra a tela na transcrição, então "phase 45°" é o que ele diz, não necessariamente 45° de um ciclo do LFO.
- A tradução granular em atmosfera é inferência, não conteúdo do vídeo.
