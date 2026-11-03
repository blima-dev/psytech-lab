# Projeto de referência — mapa do estado e ajustes técnicos (07/09/2026)

> Estudo do acervo psytech-lab, anonimizado. O original é o mapa de estado do set (caminhos locais, mutes,
> pontos de escuta do render, decisões pendentes) — essa parte é estado puro e foi removida. Fica a
> estrutura, os ajustes técnicos medidos e as referências externas.

132 BPM, C# menor, 224 compassos. 18 pistas musicais em cinco grupos, três retornos.

## 1. Estrutura por grupo (VERIFICADO)

| Grupo | Elemento | Clips | Cadeia |
|---|---|---:|---|
| Bateria | Kick | 49 | kick_08__ARYTMO_ODYSSEY_Kick_040 → Drum Buss |
| Bateria | Hi-hat aberto | 56 | OH - 01_1 → EQ Eight |
| Bateria | Hi-hat fechado | 59 | CH - 02_1 → EQ Eight |
| Bateria | Clap | 52 | CLAP - 01_1 → EQ Eight |
| Bateria | Percussão | 24 | EQ Eight |
| Bateria | Ride | 38 | 909 Core Kit → EQ Eight |
| Baixos | Subgrave | 48 | Serum 2 → Auto Filter → Utility |
| Baixos | Baixo médio | 51 | Serum 2 → Auto Filter → EQ Eight → Saturator → Chorus-Ensemble |
| Synths | Stabs | 17 | Serum 2 → Serum 2 FX → Auto Filter → EQ Eight → Saturator → Delay |
| Synths | Frase curta | 18 | Serum 2 → EQ Eight → Utility → Auto Filter |
| Synths | Acid — Groove | 15 | Serum 2 → Echo → Auto Filter |
| Synths | Acid — Tensão | 6 | Serum 2 → Echo → Auto Filter |
| Synths | Resposta FM | 17 | Serum 2 → Delay |
| Atmosferas | Drone | 7 | Serum 2 FX → Auto Filter |
| Transições | FX — Subidas | 6 | EQ Eight → Saturator |
| Transições | FX — Quedas | 5 | EQ Eight → Saturator |
| Transições | FX — Quebras | 5 | Serum 2 → Auto Filter |
| Transições | FX — Cortes | 26 | Auto Filter → Delay → Serum 2 FX |

Mudanças estruturais registradas: acid e FX separados por função; 29 clips de frases sobrepostas removidos,
mais cinco clips melódicos/FX da preparação final; drones interrompidos antes dos retornos; nove respostas de
percussão e nove cortes adicionais distribuídos pelo segundo desenvolvimento/clímax; duas quedas curtas
reaproveitam material local; preparação final com pulsos de 6 → 14 notas, filtro em movimento, Echo contido e
pausa do acid em 639–640 beats.

## 2. Ajustes técnicos medidos nesta rodada

- **Sub** reduzido a offbeat em 47 clips.
- **Hats** com envelopes curtos; teste local nos compassos 49–56: aberto 8 / fechado 16 notas por 4 compassos,
  sem ataques simultâneos.
- **Acid** no clip 208 em C# único.
- **Stabs** LP 2,8 kHz e **kick** Drum Buss damping 3,99 kHz abriram o timbre, com melhora percebida por escuta.
- **Frase** do clip 416 com 7 notas em duas alturas.
- Escolha de arranjo consolidada: intro (compasso 1–16) somente stabs/resposta FM em diálogo (8 clips, 11
  notas sem sobreposição MIDI); bateria e baixos entram no compasso 17; atmosferas desligadas.

## 3. O que o VERIFICADO não prova (lição de limites)

- VERIFICADO: estrutura Live, notas das construções, pausa/retorno do acid por leitura real, samples
  existentes e arquivo gzip/XML válido.
- Instrumentos internos de racks não auditados individualmente.
- Master com Limiter True Peak, teto −1,0 dB: **configuração não equivale a áudio medido**. Medidores
  pontuais em 12 trechos não provam qualidade, ausência de clipping integral, comportamento em mono ou
  ausência de notas presas.

## 4. Referências externas consultadas

- Estudo do artista **Vision Serpent** (energia).
- Biblioteca de fontes **KUNI**: 41 fontes listadas, 39 disponíveis, 2 com erro.
- **Tetra Hydro, Michael Nox/Robin Mind e SLUG** conferidos na origem — sem fingir audição de vídeo.
