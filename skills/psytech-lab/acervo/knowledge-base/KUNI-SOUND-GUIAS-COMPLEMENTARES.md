# Guias Complementares de Produção Psytech (compilados em 2026-09-06)

> Complemento de KUNI-SOUND-MANUAL-DEFINITIVO.md. Números são baseline comparável, não lei. Master final/-8 LUFS fora do escopo deste guia.

## Especificação Operacional: Agente de Coprodução (resumo executivo)
- Princípio central: intenção sonora antes de plugin; espaço negativo é moldura; fase estática 0% em bass é inegociável.
- Reciclagem funcional: mesmo patch/planeta para leads, plucks e pads (DNA coerente).
- Sidechain como motor rítmico: Strong (100%) para sub/bass; Weak (~60%) para plucks/leads.
- Convenção de cores: Roxo (musical/leads/pads), Laranja (drums), Rosa (midbases/drones).
- Returns: reverb 100% wet + High-pass/Low-pass + sidechain pós-reverb.
- Milking: no Simmer remover sub (<80Hz); reintrodução no drop = impacto 3x.
- Suction: remover o 4º kick antes de transição.
- Automação de volume via LFO Tool em vez de velocity manual.
- FX chain padrão: Trash 2 (Multiband) → EQ Eight (limpeza) → Loudmax/BX Limiter.
- Master: BX Digital V3 (Mono Maker <80Hz, width ≤20-25%) → MJUC (Loud & Clean, GR <1dB, agulha volta a zero antes de cada kick) → BX Limiter (34% saturation).
- 80/20: estrutura sólida primeiro; polimento por último.
- Princípio estético soberano: se soar bem, está certo (ouvido > técnica).

## Hierarquia de volumes no Drop (referência do método)
| Elemento | Peak relativo | Estéreo |
|---|---|---|
| Kick & Sub | 0 dB (referência) | 100% mono |
| Mid-bases / Stabs | -5 a -8 dB | wide/stereo |
| Hats / percussão | ~ -18 dB | panned |
| Master | -8 a -7.6 RMS | Mono Maker ~20% |

## Low-end (kick)
- Sine + pitch envelope C8 → D1 (~37Hz); notch no 1º quarto do envelope; duração 1/8 (~231ms a 130 BPM) terminando antes do bass offbeat; amp envelope em "V" no início; sloped tail; afinar na tônica ou 5ª.
- Bass: saw/square fase 0%; notch filters (~140Hz) modulados ("donky"); FM do sub para o mid-bass; pitch bend do bass seguindo o sub.

## Transições (guia mestre)
- Manter fluxo: "esvaziar" sem quebrar pressão; reciclar timbres; nunca riser EDM.
- Simmer: ruído branco + band-pass com sweep descendente (poeira/vapor), não brilho sintético.
- Reverb freeze: capturar cauda 5s+ de elemento da própria track, congelar, resamplear = wash de fundo coerente.
- Vocoder layer: carrier = midbase, modulator = foley (madeira, coiote) → estética "bush".
- Haas/widener < 30ms para laterais no break; centro limpo para o sub no drop.
- 500Hz: dip 2-3 dB (woody/mud). HPF 100-160Hz em toda bateria. Corte 20Hz em todos os canais.

## Arranjo (blueprint)
- Blocos de 4/8/16/32 bars; track 6-7 min: Intro 32-64 → Drop 1 32-64 → Simmer/Break 16-32 → Drop Final 32-64 → Outro 32.
- Drop final concentra a densidade (call-and-response entre neuro bass, plucks metálicos, glitch).
- Outro: desconstrução até o esqueleto rítmico; loop points 8-16 bars para DJ.

## Diagnóstico de escuta → técnico (translator)
- "Videogame/Trance": reduzir ressonância, escala menor/cromática, fechar LPF.
- "Parado/Sem conversa": automação de filtros/LFO nos midbases; variar wavetable position.
- "Grave fraco/Embolado": fase 0%, HPF 20Hz, mono <80Hz.
- "Clean demais": Erosion/bitcrush/saturação multibanda suave.
- "Sons brigando": sidechain Weak no secundário.
- "Pontiagudo": dip 500Hz, presence shift negativo, de-esser.

## Técnicas top (principais do ranking das 50)
1. Pitch bend no bass seguindo o sub. 2. Vocoder layering em graves. 3. Spectral morph (Vital). 4. V-shape kick. 5. Freeze & flatten de reverb tails. 6. 5ª nota p/ tensão. 7. LFO Tool 1-bar nos hats. 8. Notch 140Hz no bass. 9. Sidechain no reverb send. 10. Mono sub (M/S). 21. Suction (4º kick). 22. Fase 0%. 46. Simmer pós-break. 47. Stolen structure de referência.
