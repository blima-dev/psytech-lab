# Ableton Live — FM Lead Sound Design and Arrangement — Psytech Call and Response Tutorial

**Canal:** Scionaugh · **ID:** `LVv74akK58c` · **Duração:** 51:48 (3108 s) · **Tema:** melodia / motor-completo
**Fonte:** legenda automática em inglês. **Método:** leitura por janelas da legenda comprimida (2.148 linhas limpas; janelas 1–110, 540–840, 1125–1230, 1880–1950, 2090–2148) — **não é leitura linha a linha**; trechos fora das janelas são `NÃO VERIFICADO`. **Não ouvi o áudio.**

## Técnica ensinada

Walkthrough de sessão contínua: a sessão anterior criou o "ambient atmos lead" que "set the tone"; agora ele adiciona elementos de groove — e decide por **subtração** (desliga elementos rising/atmosféricos antes de escolher o que entra). O núcleo é **síntese FM de lead psytech no Serum 2**: osc B com volume 0 como fonte FM pura ("FM from B" no osc A), random 0 nos dois para sincronizar, e a lição central — **o timbre muda drasticamente com as oitavas RELATIVAS entre carrier e modulador**; carrier agudo + FM grave (~5 oitavas de distância) dá o "classic bubbly FM sound". Depois: band-pass (testar 24 vs 12 dB), uníssono **só números ímpares (3/5/7 — ele prefere 3)** + distorção; automação de cutoff com range mapeado no máximo útil ("se no máximo fica fino demais, o máximo desce"); drive subindo junto com a frequência; e o truque do **squelch: LFO no pitch (coarse, unipolar) na direção OPOSTA à do filtro** — "filter's going up in the positive direction, so I want my coarse pitch to actually go down". Para coerência, os 16avos de acento no início usam **o mesmo som** do squelch ("since this squelch is made from essentially the same sound as this, it's just like seamless the transition"). No arranjo: consistência = repetir o motivo do início, "and then it sort of changes off of that"; oitavas puladas com Shift+Up/Down no MIDI.

## Ferramenta usada no vídeo

**Serum 2** (FM from B, wavetable basic shapes, band-pass, uníssono, distorção) + Ableton Live (automação de cutoff, MIDI overdub, LFO/shaper no pitch). Zero tradução de ferramenta.

## Como adaptar

Direta. Pontos de encaixe:
- **FM bubbly** = candidato direto ao stab/resposta de meio (outro vídeo do mesmo censo, `v-mjY-Vlgv0`, já pedia stab-resposta; `C3x8o9Krfc0` trata de stab com band-pass). Carrier agudo + modulador grave; relative octaves é o knob de timbre.
- **Squelch (filtro ↑ / pitch ↓)** é movimento de LEAD/resposta — proibido migrar para o BAIXO (o groove deslocado é a assinatura rítmica; LFO no pitch do grave não entra).
- **Uníssono 3 ímpar + distorção** no lead respeita o low-end mono se a largura ficar acima do corte do grave (~150–250 Hz).
- **Range de automação mapeado** ("máximo que eu usaria") é prática saudável: evita automação que entra em zona inaudível/fina.
- **Mesmo som no acento e no squelch** = coerência de família — conversa com `A6XjjwGUkA8` (frações mínimas de ruído virando família) e com o princípio de camada por família.

## Aplicação (referência)

1. Patch FM-from-B em Serum 2 para stab/resposta (2–3 eventos/compasso), carrier na região média-aguda, modulador 3–5 oitavas abaixo, random 0, band-pass 24 dB — posicionado nos vãos do groove, acima de ~200 Hz.
2. A/B do "squelch" (LFO pitch ↓ contra filtro ↑) num lead de entrada de seção — nunca no grave.
3. Range de cutoff pré-mapeado antes de automatizar.

## Conflitos e cautelas

- LFO de pitch/filtro só em lead/resposta acima do corte do low-end; o grave e sua assinatura rítmica ficam intocáveis.
- 16avos de acento com o mesmo som do lead: ok como resposta percussiva; não vira rolling de baixo.
- Nenhuma escala/tônica citada nas janelas lidas — `NÃO VERIFICADO` se o vídeo usa alguma tônica específica; a tonalidade fica a critério do material.

## Trechos de prova (legenda)

1. FM "bubbly" clássico: portadora aguda + moduladora ~5 oitavas abaixo (Scionaugh) — janela 730–780.
2. "Now, when you're doing unison on these sorts of sounds, I recommend have using only the odd numbers, so three, five, or seven." — janela 660–670
3. Coarse pitch na direção oposta do filtro = o que faz o som "squelch" (Scionaugh) — janela 1893–1907.

## Limites

Leitura por janelas (declarada acima) — o meio do vídeo (mix, sidechain, master, ~linhas 1300–1880) não foi lido; sem valores numéricos de Hz/dB na legenda; timestamps do VTT não acompanharam as janelas (prova por texto limpo, não por tempo exato). Áudio não escutado. Apresentador é o Scionaugh (mesmo canal dos vídeos curtos).
