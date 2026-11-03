# PML Mixing A Track — curso completo e o A/B de projeto (Before/After)

**Data:** 26/10/2026 · **Fonte:** Production Music Live — "Mixing A Track From Start To Finish" (curso)
**Projetos:** course files do curso (2 `.als` + `.cfg`, 764 KB)
**Método:** contagem de arquivos + `ffprobe` + leitura do XML dos dois `.als`. **Nenhum vídeo foi assistido e nenhum áudio foi ouvido.**

---

## 1. Conteúdo do curso, medido

| Medida | Valor medido |
|---|---|
| Vídeos completos | **42 MP4 (4h32) + 4 FLV (50 min) = 5h23** |
| Fragmentos `.fdmdownload` | **0** |
| Projeto | **`Before MIX.als` + `After MIX.als`** (dentro do zip de projeto, 33 MB) |
| Extras | slides do curso em PDF (zip 17 MB) + samples do projeto (no zip) |

As aulas do ponto cego do projeto (as que mais valem): `Low Bass Layer`, `Grouping Bass Layers`, `Bass-Buss`, `New York Compression - Return Channel`, `Vocals`, `DeEsser`, `Dynamic EQ for the Subbass`, `Subtractive vs Additive EQ`, `Frequency Masking`, os 4 `How The Compressor Works` e a cadeia de export/master.

---

## 2. O A/B de projeto, medido

Antes e depois são o **mesmo arranjo** (119 BPM · 128 compassos · 718 → 766 notas; a diferença de notas é edição de clipes, não música nova).

| Medida | Before MIX | After MIX |
|---|---:|---:|
| Pistas | 25 | **31** |
| Returns | 2 | **5** |
| Devices no total | 78 | **183** |
| Master | `StereoGain` Gain 7 dB | `StereoGain` Gain 8 dB + **rack `Eq8 > GlueCompressor > Compressor2 > Compressor2 > Eq8 > Limiter > Limiter`** |

### 2.1 O que entra no After

| Alvo | Mudança medida |
|---|---|
| **Returns novos** | `C-Bass New York` (`Eq8` + `Compressor2`) · `D-Overtones` (`Redux` + `Eq8` + `Reverb` + `Utility` + `Compressor2`) · `E-Drums Reverb` (`Reverb`) |
| **Sends** | todas as pistas passam de 2 para 5 sends |
| **Kick** | ganha **2 `Eq8`** em série depois do rack `Simpler > AutoFilter` (volume intacto 0,2512) |
| **Bass Group** | `AutoFilter` → `Compressor2 > GlueCompressor > GlueCompressor > Eq8 > AutoFilter > StereoGain`; volume **+5,5 dB**; send para o `C-Bass New York` em **0,724** |
| **Massive Bass (15)** | `Plugin + Saturator` → 8 devices (`Eq8 > Eq8 > StereoGain > Eq8 > Chorus > Reverb > Eq8`); volume **+5,7 dB** |
| **Massive Bass (16)** | `Plugin` → 7 devices (`Eq8 > Compressor2 > Saturator > Eq8 > Chorus > Eq8`); volume **+8,2 dB** |
| **SubBass** | ganha `Compressor2` + `Eq8` |
| **Shaker** | ganha `Eq8`; volume **−8,1 dB** |
| **HH** | ganha `Eq8` + rack (`Vinyl > Eq8 > CrossDelay`); volume **−7,8 dB** |
| **Clap** | `Eq8` + `GlueCompressor`; volume **−1,6 dB** |
| **Instrumentos** | 7 pistas viram 10: entra `17 Low Buss`; `Violin Pizzi` é separado em `Pizzi Marimba` + `Violin Pizzi L` + `Violin Pizzi R` |

### 2.2 Leitura estrutural (o que o After faz)

1. **O baixo é o centro do mix.** O grupo inteiro sobe +5,5 dB, os dois baixos individuais sobem +5,7 e +8,2 dB, e o grupo ganha um send dedicado de **compressão New York** — compressão paralela enviada por return, o mesmo princípio que o curso explica na aula `New York Compression - Return Channel`.
2. **A bateria desce para abrir espaço.** Shaker −8,1 dB, HH −7,8 dB e clap −1,6 dB, cada um com EQ próprio. É o oposto de "mais bateria": menos percussão, mais grave.
3. **Cada elemento ganha EQ e compressão próprios**, não só o bus: 78 → 183 devices. O kick recebe **dois** `Eq8` em série.
4. **O master vira uma cadeia de 7 estágios** dentro de um rack: EQ → glue → dois compressores → EQ → dois limiters. É master de curso, não master de streaming.
5. **O "After" cria três caudas**: `C-Bass New York` (baixo), `D-Overtones` (Redux/EQ/verb para harmônicos) e `E-Drums Reverb` (bateria). Antes havia só reverb e delay genéricos.

---

## 3. O que serve para o estudo

- **A/B de mix pronto**: dá para abrir os dois `.als` lado a lado e comparar decisão por decisão — New York compression, baixo em camadas, kick com EQ em série.
- **Receita de baixo em 5 camadas**: `Low Buss` + `Massive SubBass` + três `Massive Bass` com funções diferentes; o grupo com dois glue compressors e send para compressão paralela.
- **Relação nível × função**: o After não "sobe tudo"; sobe o grave e desce o topo percussivo. É a hierarquia grave > topo típica do gênero — aqui medida em dB, não em opinião.

**O que NÃO serve:** o master de 7 estágios e o `Redux` de overtones são de outro gênero (house orgânico); copiar a cadeia inteira não é a lição. Usar como referência de decisão, não como template.

---

## 4. Limites

- **Não ouvi** nenhum dos dois mixes. A comparação é estrutural (devices, volumes, sends), não auditiva.
- **Gate de carregamento:** os dois `.als` reprovam validação estrutural offline com `NextPointeeId 0 <= maior ID` (Before 243.668 / After 259.508) — marca de projeto salvo em **Live 9 (2014–2016)**. O Live 12 pode reconstruir o campo ao abrir, mas **não foi testado**. Se for abrir, abrir uma cópia e conferir; não é o mesmo problema de grupos corrigível por renumeração.
- **Mídia:** sem os WAV do projeto, os `.als` abrem com mídia faltante. Os samples estão no zip `PML Mixing Course - Project File (Instrumental).zip` (33 MB); para abrir completo, extrair esse zip ao lado.
- Os 4 FLV (`27`, `28`, `42`, `45`) são vídeo antigo; o curso tem 46 aulas somando ~5h23.
- A reconfirmação é por leitura de XML (gzip) dos dois `.als`.
