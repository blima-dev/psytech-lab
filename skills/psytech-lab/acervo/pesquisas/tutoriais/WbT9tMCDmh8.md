# How I make bubbly Psytrance FM Plucks

**Canal:** Scionaugh (apresentador "Sino" na transcrição, transmitindo do Vietnã) · **ID:** `WbT9tMCDmh8` · **Duração:** 2:55 (175 s, publicado 20/07/2026)
**Fonte:** transcrição completa do vídeo (via web reader; sem timestamps — o download da legenda via yt-dlp ficou bloqueado). **Método:** transcrição SEM timestamps — provas são citações literais na ordem do vídeo; **áudio não escutado.**

## Técnica ensinada

Plucks "borbulhantes" de psytrance **no Operator (Live nativo)**: duas senoides — **carrier em frequência alta + osc B uma oitava abaixo como modulador** ("the trick with these bubbly sounds or anything bubbly really is to start with a carrier wave with a high frequency and a modulating wave… with a lower one"); subir o nível de B revela o efeito bolha, e mover a relação de oitavas muda o caráter das bolhas. Em seguida, **Expression Control (Max for Live) com 4 moduladores Random** mapeados em: **decay do envelope de volume, release, decay do FM e coarse pitch**. Afinar os amounts (menos release tira o ring residual). O groove nasce disso: ele toca **uma nota longa** ("I'll grab my rhythmizer… I can just play one long note") e as bolhas ritmadas emergem da variação aleatória de envelopes — não de MIDI programado. Cadeia final leve: **compressão (consistência), phaser, reverb e echo**, com ajuste de release para matar o ring.

## Ferramenta usada no vídeo

**Ableton Operator + Expression Control (M4L stock)** + compressor/phaser/reverb/echo nativos. **Arsenal literal — zero tradução** (Operator é o motor do sub no material de referência).

## Tradução para um arsenal compatível

Direta. É a mesma lei do "bubbly FM" do vídeo longo (`LVv74akK58c`: carrier agudo + modulador grave), agora em Operator e aplicada a **pluck/resposta**. A sacada canônica é o **groove sem onsets programados**: uma nota longa + envelopes randomizados = eventos percussivos que respiram — hipnose por microvariação, irmã do call-and-response por chop de takes (`MgWlvH3n4EU`) e da randomização sutil (`ejNHFdtYrw0`).

## Aplicação concreta em um arranjo minimal de referência

Pista de resposta/stab: Operator com 2 senoides (carrier C#4–C#5, B −1/−2 oitavas), Random M4L em decay/release/FM-decay (pitch random **desligado ou ≤2 st** — ver conflitos), nota longa sobre 2 compassos nos slots deslocados **.27/.77** do groove, **HP ≥250 Hz na saída**, compressor leve para consistência, reverb/echo em retorno filtrado. Nunca no sub/baixo.

## Conflitos com o material de referência

- **Random no coarse pitch** (o vídeo usa): o teto de randomização de pitch é ±2 st e só em textura (recomendação do uso do Serum no material); em resposta na tônica C# frígio, prefira random **sem pitch** (só envelopes) na primeira versão.
- Random de envelope por nota é o mesmo mecanismo que outra análise do gênero desaconselha **no grave** — aqui liberado porque é resposta ≥250 Hz, não baixo.
- Phaser/reverb/echo: retorno filtrado, dry predominante — sem serial 100% wet em elemento de transiente.

## Trechos de prova (transcrição, sem timestamp — ordem literal)

1. "the trick with these bubbly sounds or anything bubbly really is to start with a carrier wave with a high frequency and a modulating wave so that oscillator B with a lower one"
2. "grab an expression control. Now, this is a Max for Live plugin… we're just going to modulate it with random all of the things that we think sounds quite interesting… on the volume envelope I'm going to do a bit of decay… Release as well… map that to my release… map that to the decay here of the FM… put this on the course pitch"
3. "I'll grab my rhythmizer. So I can just play one long note… give it a bit of compression… maybe a bit of phaser… a bit of reverb. And a bit of echo"

## Limites

Transcrição via web reader **sem timestamps** (a legenda via yt-dlp seguiu indisponível); nenhum valor numérico de amount/level na fala ("tune these babies" é de ouvido); áudio não escutado; "rhythmizer" não é nome de device stock — provavelmente apelido/ferramenta própria, `NÃO VERIFICADO`.
