# Cronocops (Klipsun + Marco Element) — workshop e racks

Fontes coletadas em 2026-09-08: https://pmeexperts.com.br/cronocops/ · https://www.youtube.com/watch?v=lFkMz4s-LwU · resumo de notebook (Part I/II). Trata-se da escola do workshop CRONOCOPS (track "Time Keepers"). Uso: guia de decisão em projeto 132 BPM / C#m. Material de terceiros — não é medição da própria track.

## Filosofia e workflow

- **Menos é mais**: de 170–180 canais para **25–63 canais ativos** por track; deadline de 2 dias por track.
- **Reaproveitamento tonal (Lead de DNA)**: o synth principal reaparece em outros papéis (pad, pluck percussivo, FX de transição). O ouvinte memoriza fonte única; timbre novo que toca uma vez não gruda.
- **Low-end limpo**: baixo no Risor (Reaktor, wavetable, Pulse / Saw+Pulse) ou Wavetable nativo. **Poucos plugins no baixo** — cadeia longa bagunça polaridade/fase com o kick e obriga corretor de fase. A onda deve nascer pronta do synth. Preferir FX internos do próprio synth.
- **Tensão do silêncio (Time Keepers)**: no break, remover TODA pressão de graves (kick+baixo) e manter só tic-tac de relógio + badalos de sino em reverb longo (+ chorus). Pode rodar 1 min; a pista espera o drop — e o drop simples entra avassalador pelo alívio.

## Hacks de rack (RACKS CRONOCOPS)

1. **LFO Tool "orelhinha"**: fade-in rápido (µs/ms) em todo elemento que bate NA CABEÇA DO TEMPO junto com kick/snare — impede o transiente alheio de engolir o transiente do kick. APLICÁVEL DIRETO: elementos on-beat que dividem a cabeça do tempo com o kick.
2. **Marco's Soft Clip Hack**: Utility (+12 dB) → Glue Compressor (Soft Clip ON, threshold raspando 0 dB) → Utility (−12 dB). Dá o soft clip nativo do Glue sem enganar o ouvido com volume. APLICÁVEL: acid/synths caóticos.
3. **Ozone Imager no grupo de hats**: FECHAR estéreo dos agudos percussivos para liberar o lateral para leads/psych FX.
4. **Utility com inversão de fase** em canal de synth conflitante — anula cancelamento instantâneo quando dois timbres de espectro igual tocam juntos.
5. **Zap picotado**: em vez de zap pronto, sample comum no **Grain Delay** com picotes — textura espacial com microvariações.
6. **Rack de baixo Operator + Kick sample**: híbrido sample de kick + Operator (FM nativo) → 300+ timbres de baixo sem caçar pack novo.

## Aplicações propostas (plano de teste)

1. Break: versão "Time Keepers" — tirar sub/bombo restantes e deixar UM marcador rítmico seco (ride/tick) + reverb longo; drop volta por degrau. (Se o break atual tiver perc conversando, testar a versão silêncio.)
2. Acid → Marco's Soft Clip Hack.
3. Elementos on-beat (bombo/clicks) → "orelhinha" de fade-in de ~2–5 ms alinhada ao transiente do kick.
4. Simplificação: 3 protagonistas (cama harmônica, pluck de conversa, lead) — o audit "cadê o lead" usa esse princípio: escolher 1 lead de DNA e reciclar em pad/pluck/FX nos outros blocos.

## Premissas a validar por escuta

- HIPÓTESE (não medida): um bombo (BM) sem "orelhinha" pode ter o transiente competindo com o kick.
- A conta +12/−12 dB do Soft Clip Hack assume headroom do canal; conferir antes no fader do canal alvo.
