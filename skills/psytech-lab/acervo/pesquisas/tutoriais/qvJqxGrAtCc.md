# Transition FX Hack

> **Vídeo:** `qvJqxGrAtCc` · **Canal:** Sonic Academy
> **Legenda:** automática `en-orig`, lida integralmente. Tem legenda.
> **Limite de leitura:** a dissecção abaixo usa a legenda, não os frames. Não se afirma parâmetro de tela que a fala não descreve.

## Técnica ensinada (2-4 frases)

O autor parte de um projeto antigo de minimal tech house e mostra que já tem um grupo de efeitos com pistas separadas — snare roll, crash, reverse crash, noise down e noise up (00:00:40.080; 00:01:26.320–00:01:32.240). Ele pega o grupo inteiro, não arquivos soltos, e arrasta do Browser para o projeto aberto; o Ableton repõe todos os canais e os clipes "exactly where I had them" (00:01:37.320–00:01:48.350). O grupo leva junto EQs, efeitos e até o roteamento do compressor que é sidechainado pelo crash (00:03:30.880–00:03:43.830; 00:04:47.560–00:04:53.350). No destino, ele ancora o primeiro clipe no "one", apaga o snare roll que duplicaria o que já fez, reequilibra volumes e corta sobreposições (00:01:56.320–00:02:07.390; 00:03:06.000–00:03:07.959; 00:05:01.720–00:05:08.790); a técnica é uma biblioteca portátil de transições, não um preset de plugin.

## Ferramentas usadas no vídeo (plugin/stock)

- **Ableton Live — Browser + Group Track.** O contêiner é um grupo de pistas do próprio Ableton, arrastado para a área "drag or drop files and devices" (00:01:37.320–00:01:42.150). O vídeo fala em "effects group", "side chain compressor", "EQs" e, uma vez, em "drum rack" (00:01:22.480–00:01:24.990; 00:03:29.800; 00:03:40.080–00:03:43.830; 00:04:47.560).
- **Nenhum plugin de terceiro é nomeado na legenda.** O que está provado é o uso do grupo/Browser do Ableton.
- **Não há dependência de ANA 2, VELA, SideKick, Kick 3 ou Bitwig.** Esses nomes não aparecem na legenda; o "hack" é de organização de projeto, não de um instrumento específico.

## Como recriar no Live 12

A tradução é direta: o grupo é o contêiner portátil; os sintetizadores são apenas fontes dentro das pistas. Não transformar a biblioteca de transições em preset de synth — o que se reutiliza é o grupo com clipes e devices.

| Ferramenta | Papel nesta técnica |
|---|---|
| **Live 12 nativo** | Browser + Group Track para o grupo de FX de transição (crash, reverse crash, noise up, noise down). Simpler/Sampler para crash/reverse; Grain para cauda granular; EQ Eight para o HPF; Compressor com sidechain para o roteamento crash → noise; Echo/Hybrid Reverb para cauda; AutoPan/Shifter para movimento. É o veículo 1:1 do vídeo. |
| **Serum 2 (GranularOsc)** | Pode gerar a fonte do gesto — ruído filtrado, textura granular de um crash, sweep — mas entra como uma pista dentro do grupo. O GranularOsc não substitui o contêiner de grupo. |
| **Diva / Vital / Massive X / Surge XT** | Fontes opcionais para um sweep tonal ou ruído; não são necessários. O vídeo não depende de nenhum deles. |
| **Bibliotecas sampleadas** | Se um gesto pedir camada orgânica, pode ser uma pista do grupo; a lógica de reuso continua a mesma. |

**Cuidados de tradução**

- A legenda não menciona automação. A prova que ela dá é de clipes, EQs, efeitos e sidechain; não presumir que a automação de volume do grupo antigo viaja. Refazer fades/automação no destino.
- O sidechain do crash só funciona se a pista que alimenta o compressor também vier. No vídeo o roteamento "still remembering that routing" (00:04:47.560–00:04:53.350); se apagar o crash, o compressor pode ficar sem fonte.
- O primeiro clipe é a âncora do grupo. No vídeo ele arrasta o primeiro clipe para o "one" (00:01:56.320–00:02:00.590); os demais vêm na posição relativa.
- O vídeo apaga o snare roll importado porque já tinha feito o dele (00:02:01.480–00:02:07.390). Não importar uma pista que duplique a percussão de resposta própria.

## Notas de aplicação (gerais)

- O grupo é um recurso de borda: não é um novo instrumento do groove. Ele só acorda nos respiros da faixa (fim de frase/virada), e os gestos devem morrer no downbeat seguinte.
- Montar o grupo uma vez, com pistas separadas (`CRASH`, `REV-CRASH`, `NOISE-UP`, `NOISE-DOWN`; `SNARE-ROLL` só se não houver percussão de resposta própria), ancorar o primeiro clipe no downbeat do respiro e manter a posição relativa dos demais.
- HPF em todo o grupo; se usar a receita do vídeo, rotear o **crash** para o sidechain do **noise**, não para o kick, o sub ou o baixo.
- Um gesto por respiro: apagar duplicatas, cortar overlaps e nivelar antes de julgar. O vídeo mostra que o grupo não é "set and forget": ele chega 4 dB abaixo e volta a zero; depois um efeito vai a −18 dB (00:03:06.000–00:03:07.959; 00:05:14.520–00:05:17.670) — reequilibrar no destino, não copiar o valor.
- Ruído de transição: gesto curto, com fade, cortado antes do próximo evento percussivo; conteúdo preferencialmente no topo, sem preencher o miolo com ruído contínuo nem mandar energia nova para o sub.
- Madeira/orgânico seco fica fora do grupo; se precisar de espaço, mandar só o FX para o reverb em paralelo.

## Prioridade e esforço

- **Prioridade: alta.** O vídeo oferece um método barato para povoar os respiros de uma faixa sem redesenhar o motor.
- **Esforço: baixo.** É trabalho de organização no Live — montar o grupo uma vez, ancorar os clipes, apagar duplicatas, corrigir overlaps e nivelar. Não exige plugin novo nem sound design de zero.
- **Risco:** baixo a médio; o perigo é mascarar o groove ou engordar o sub. Controlar com HPF, sidechain restrito ao grupo, um gesto por respiro e conferência em loop com o groove deslocado.

## Trechos de prova: citações literais da legenda com timestamp

> "…to take this whole effects group and I can drag it into my project where it says drag or drop files and devices here and it'll place all of those in. It'll place all the tracks in with all the clips placed exactly where I had them." — **00:01:37.320–00:01:48.350**
>
> Em português: "…pegar este grupo de efeitos inteiro e arrastá-lo para o meu projeto, onde diz 'arraste ou solte arquivos e devices aqui', e ele colocará tudo isso dentro. Ele coloca todas as pistas com todos os clipes exatamente onde eu os tinha."

> "And this had a side chain compressor on it. It's getting side chained from the crash cymbal and it's still remembering that routing, so that's pretty cool, too." — **00:04:47.560–00:04:53.350**
>
> Em português: "E isto tinha um compressor com sidechain. Ele está sendo sidechainado pelo crash e ainda se lembra desse roteamento, o que é bem legal também."

> "If you've done it once and you like the way it sounded, just grab it from another project and pull it right into your existing one." — **00:06:11.440–00:06:16.470**
>
> Em português: "Se você já fez uma vez e gostou de como soou, basta pegá-lo de outro projeto e puxá-lo direto para o seu projeto atual."
