# PML — TIM ENGELHARDT PRODUCTION PACK (Melodic Techno) — dissecação

**Fonte:** Production Music Live — "Tim Engelhardt Production Pack - Melodic Techno" (pack da Production Music Live)
**Análise:** 25/10/2026 · **Método:** parse dos `.als` (gzip/XML, leitura), parse dos 95 `.h2p`, contagem de amostras. **Nada foi ouvido.**
**Tamanho:** 0,56 GB · **412 arquivos**

Este é o material **mais valioso em projeto** da coletânea: são três músicas completas de verdade, com sessão, automação, sends e amostras — não são presets soltos.

---

## 1. Conteúdo medido

| Material | Quanto |
|---|---|
| Projetos Ableton principais | **3** (Climb, Ash, Ivory) |
| Backups `.als` | **94** (versões datadas do próprio produtor) |
| Presets Diva `.h2p` | **95** |
| MIDI `.mid` | **37** |
| Amostras WAV | **163** (+17 AIF) |
| Loops | Hihat, Musical, Perc, Top |
| One-shots | Claps, Hats, Kicks, Perc, Shaker, Snares |

Os 94 backups não são lixo: são o histórico de decisão do produtor, com data e hora no nome (`[2020-10-09 214552]`). Servem para ver **o que mudou entre versões**.

---

## 2. Os três projetos — raio-x

| | **A — Climb** | **B — Ash** | **C — Ivory** |
|---|---|---|---|
| Pistas | 24 | **32** | 26 |
| Clips MIDI | **93** | 89 | 62 |
| Clips de áudio | 16 | 25 | **39** |
| Instâncias de Diva | 6 | 5 (+1 VST3) | 6 |
| Operator | 5 | **15** | 0 |
| Instrument Racks | 4 | 7 | 0 |
| Sends | A-Hall · B-Drum Room · C-Longer Reverb · D-Echo | A-Medium Reverb · B-Drums Room · C-Echo · D-Huge Reverb | A-Hall · B-Drum Room · C-TripleDelay \| Reverb |

### O achado que importa — arquitetura de 4 sends

Os três projetos usam a **mesma convenção de espaço**, com nomes diferentes:

- **A** = reverb de cauda longa (Hall / Medium Reverb / Hall)
- **B** = reverb curto de sala de bateria (Drum Room nos três)
- **C** = delay ou delay+reverb
- **D** = eco amplo / reverb enorme

Ou seja: o espaço não vem de reverb no canal, vem de **duas reverbs de tamanhos diferentes + delay + eco**, endereçadas por send. É o tipo de arranjo que um projeto de espacialidade (caudas diferenciadas por função) pede; um set que trata o espaço dentro do próprio synth deixa essa camada fora.

### Outra observação estrutural

- **Climb** tem **camadas de piano por dinâmica** (`p`, `mf`, `f`, `ff`, cada uma com Lower/Upper) — é multisample organizado para tocar dinâmica real, não velocity de plugin.
- **Ash** é o mais denso em Operator (15) e tem racks de processamento por camada.
- **Ivory** não tem nenhum instrumento nativo: **39 clips de áudio** e 6 Diva. É a prova de que o produtor renderiza e trabalha em áudio.

---

## 3. Os 95 presets de Diva — distribuição real

`Model` lido do arquivo; nome do modelo é `INFERÊNCIA` pela ordem do manual.

| Oscilador | Qtd | | Filtro | Qtd |
|---|---|---|---|---|
| Digital | **31** | | Ladder | **46** |
| Triple VCO | 21 | | Multimode | 24 |
| DCO | 18 | | Uhbie | 11 |
| Dual VCO | 17 | | Bite | 9 |
| Dual VCO Eco | 8 | | Cascade | 5 |

Nomenclatura: `PML_ENGELHARDT_BASS_01` a `_20+`, e equivalentes por função. Ao contrário do Cercle (Cascade dominante), aqui o **Ladder** manda — é um som mais redondo e menos agressivo, coerente com melodic techno.

---

## 4. Comparação dos quatro packs (o mesmo instrumento, quatro escolas)

| | Curso Diva (2020) | Cercle Vol.4 | Tim Engelhardt | Drift (Serum) |
|---|---|---|---|---|
| Osciladores usados | 3 de 5 | **5 de 5** | **5 de 5** | — |
| Filtro dominante | Ladder | **Cascade** | **Ladder** | — |
| FX por preset | 1 módulo | 2 módulos | — | — |
| Formato | curso em vídeo | pack de presets | **3 projetos completos** | 8 projetos + presets |
| Valor para psytech | conceito | timbres | **arquitetura de mix e espaço** | timbres Serum |

**Leitura:** não são concorrentes. O curso ensina o instrumento, o Cercle dá timbres modernos, o Tim Engelhardt entrega **estrutura de música**, e o Drift trabalha no Serum.

---

## 5. Como usar

1. **Copiar a arquitetura de sends** (não o conteúdo): duas reverbs de tamanhos diferentes + delay + eco, em sends A–D. É a mudança de maior impacto em espacialidade e não exige plugin novo.
2. **Estudar um projeto inteiro** — sugestão: `Project C (Ivory)`, por ser o mais enxuto (26 pistas, áudio renderizado).
3. **Usar os 95 presets de Diva** para o A/B de baixo, junto com os do Cercle.
4. **Ignorar os 94 backups** na escuta; usar só para consultar decisão pontual.

## 6. Limites

- Nada foi ouvido; nada foi aberto no Live.
- Os `.als` são de 2020 (era Live 10). Podem abrir com avisos de versão e mídia faltante.
- A contagem de plugins vem do XML; se um device estiver desativado, ele ainda é contado.
