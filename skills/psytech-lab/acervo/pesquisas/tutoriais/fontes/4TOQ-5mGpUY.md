# ANA 2 Resampling and Granular Hack

**Canal:** Sonic Academy (Tech Tips Vol. 68, Protoculture) · **Vídeo:** https://www.youtube.com/watch?v=4TOQ-5mGpUY · **Duração:** 7:26 · **Publicado:** 2021-12-17
**Fonte:** legenda automática EN (capítulo único: Fake Granular FX in ANA2).

## Técnicas-chave

- **Granular falso (a ANA 2 não tem oscilador granular)** — toca UMA nota só (C3) do patch, faz bounce/resample, normaliza o WAV logo abaixo de 0 dB (−0,3) e carrega no sample oscillator do synth.
- **Loop mínimo + LFO1 lento em loop start/end** — encolhe o loop a um trecho mínimo e modula start e end com o LFO1 em taxa bem baixa: o ponto de leitura rasteja pelo áudio, imitando o scan de um granular real. Limite declarado: um loop por vez.
- **Variações demonstradas** — reverse do sample inteiro; +1 oitava antes do scan (acelera a leitura e tira o conteúdo do low-mid); LFO ainda mais lento muda a textura por completo; alongar o material até virar pad com shimmer.
- **Bônus do resample** — gravar um patch inteiro numa nota e recarregá-lo permite empilhar uma versão "congelada" de qualquer som sobre outros sons e transformá-lo por completo.
- **Tradução nativa** — o gesto (loop curto varrido) é o que o GranularOsc do Serum 2 e o Grain do Live 12 fazem de fábrica; a parte transferível universal é o resample como fonte.

## Notas de aplicação

- Subir +1 oitava ANTES de granularizar move a textura do low-mid para o vale de médios — e um HP 180–250 Hz fecha a porta do grave.
- Random só de posição/offset; manter pitch estável (±2 st no máximo) para não desafinar a fonte; LFO livre, sem tempo-sync, para a textura não espelhar o groove.
- Loop curto + grão curto + pitch instável é a receita de brilho metálico: grão longo e fonte escura evitam.
