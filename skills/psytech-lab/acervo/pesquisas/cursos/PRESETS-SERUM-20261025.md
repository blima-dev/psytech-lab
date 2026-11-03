# OS 152 PRESETS DE SERUM DO DRIFT — e um contraste com patches de referência

> Método: parser de `.SerumPreset` (leitura da estrutura de cada arquivo — osciladores, wavetables, warp, filtros, envelopes, LFOs, matriz de modulação, cadeia de FX).
> Fonte: os 152 presets do pack Drift. Para contraste, foram lidos com o mesmo método **25 patches em uso num set de referência psytech** (32 nomes de patch em uso; desses, 25 têm arquivo `.SerumPreset` legível e 7 só existem em `.fxp`).
> Nada foi ouvido. As leituras são de estrutura.

---

## 1. Como o pack é construído (152 presets)

| Dimensão | Distribuição |
|---|---|
| **Camadas por patch** | 2 (58) · 1 (46) · 3 (27) · 4 (20) · 5 (1) |
| **Wavetables** | **Basic Shapes 133** · default 100 · ICanHasKick 25 · analog_basic 8 · analog_mini 8 · Analog_BD_Sin 6 · Jno 4 · acid 4 · FM_Freak 3 |
| **Warp** | **kPD_OSC 28** (phase distortion) · kFM_SUB 7 · kFM_NOISE 3 · kBendPosNeg 2 · fm 2 · sync 2 |
| **Filtros** | **moog_lowpass_24 53** · MgL18 33 · moog_lowpass_12 28 · bandpass_24 5 · lowpass_24 5 · highpass_12 4 |
| **Cadeia de FX** | **FXEQ 105** · FXReverb 69 · FXDistortion 57 · **FXHyperD 54** · FXDelay 50 · FXFilter 33 · FXComp 26 · FXChorus 22 · FXBode 12 · FXPhaser 6 |
| **Unison** | 258 osciladores em 1 (sem unison) · 8 vozes (15) · 7 (12) · 3 (11) |
| **Arp** | **0 de 152** — nenhum preset usa arpejador |
| **Matriz de modulação** | mediana **2,5 rotas** · fontes: env1 61 · macro0 53 · lfo0 49 · macro3 49 · macro1 46 · macro2 42 · mod_wheel 30 |
| **Destinos de modulação** | **filter0.cutoff 108** · oscillator3.volume 27 · oscillator0.warp_amount 26 · fx4.wet 25 · fx0.wet 23 |
| **ENV1 (mediana)** | attack **0,5 ms** · decay 1,0 s · sustain 0,79 · release **76 ms** |
| **Cutoff (0–100, mediana)** | **43,4** (mín 0 · máx 97,2) |

`VERIFICADO`.

### 1.1 Por função

| Categoria | n | Camadas (med) | FX (med) | Mod (med) | Usa unison |
|---|---|---|---|---|---|
| **BASS** | 51 | **2** | **2** | 3 | 9 |
| **LEAD** | 23 | 3 | **5** | **7** | 12 |
| **PLUCK** | 17 | 3 | 5 | 6 | 5 |
| **PAD** | 12 | 2 | 2 | 2 | 11 |
| FX/Riser | 11 | 1 | 2 | 1 | 2 |

`INFERÊNCIA` — o pack tem uma **economia por função**: baixo é 2 camadas e 2 FX; lead e pluck são 3 camadas e 5 FX. E o **EQ interno em 105 de 152** significa que o som já sai equalizado do plugin — o ajuste no DAW é fino, não estrutural.

---

## 2. Os 25 patches de referência (set psytech)

| Patch | Osc | FX | Mod | Filtro |
|---|---|---|---|---|
| PML BS Basalt Punch Organica | 1 | 6 | 12 | moog LP24 |
| [SLINGSHOT] GLIDE BASS 03 | 2 | 1 | 2 | moog LP24 |
| [SLINGSHOT] GAZOLLA DARK TALK BASS | 2 | 1 | 1 | moog LP24 |
| BS Golden | 4 | 4 | 11 | BP12 + moog LP24 |
| BS Fruity | 4 | 5 | 10 | moog LP12/LP24 |
| BS Gravel | 3 | 4 | 18 | moog LP24 |
| BS Crown | 3 | 10 | 8 | MgL18 |
| ARYTMO_ODYSSEY_Bass_Ares | 3 | 14 | 12 | LadderMg |
| LD - Intenso | 5 | 5 | 7 | FlangeHL6P |
| [LEAD] DISTRO | 3 | 7 | 17 | bandpass_24 |
| GREENWOLVE_WOOD_LEAD | 2 | 0 | 1 | lowpass_24 |
| PML LD Flute Arctic | 2 | 4 | 2 | bandpass_24 |
| GTR - 100 Nights in Marocco | 5 | 9 | 25 | CombP + moog LP12 |
| GTR - Acoustic Modelled String Pluck | 5 | 6 | 23 | CombH6N + moog LP24 |
| ARP - Bell Arperium | 4 | 5 | 15 | moog LP12 |
| [DIMENSIONS 1] CHRONOS | 3 | 7 | 13 | MgL18 |
| 25 - Galactic - Pad 2 | 2 | 5 | 3 | moog LP12 |
| ST - Million Pieces | 2 | 5 | 7 | moog LP24 |
| ST - Stab 2 Trust Me | 2 | 3 | 5 | moog LP12 |
| [RISER 8BAR] ALIEN INFECTION | 3 | 9 | 6 | RM + moog LP12 |
| [RISER 8BAR] UPLIFTER | 4 | 5 | 19 | moog LP12 |
| [ATMOSPHERE] Epic | 3 | 7 | 6 | Reverb1 |
| INTERSTELLAR C | 4 | 5 | 12 | moog LP12 |
| AN - Sopro Cerimonial C3 | 1 | 0 | 0 | — |
| LD - Violins Motor 2H3 | 1 | 0 | 0 | — |

### 2.1 O set de referência contra o pack

| Medida | **Set de referência (25)** | Pack (global) | Pack (BASS) |
|---|---|---|---|
| Camadas (mediana) | **3** | 2 | **2** |
| FX por patch (mediana) | **5** | 2 | **2** |
| Rotas de modulação (mediana) | **8** | 2,5 | 3 |
| ENV1 release (mediana) | **0,20 s** | 0,076 s | — |
| Wavetable nomeado | 4 usam Basic Shapes | **133 usam Basic Shapes** | — |

`VERIFICADO` nos 25 presets lidos.

`INFERÊNCIA` — **os baixos do set de referência estão construídos como leads do pack**: 3 camadas, 5 FX internos e 8 rotas de modulação, contra 2/2/3 no baixo do Drift. Isso tem consequência prática: mais camadas e mais release (0,20 s contra 0,076 s) significa **mais sobreposição e mais cauda no grave**. É consistente com o diagnóstico de áudio do set (low-mid +4,3 pp contra a família de referências).

**Não é erro de gosto** — é densidade. Mas explica por que o grave desse set precisa de mais espaço do que o de uma referência: ele carrega mais informação.

---

## 3. Risco operacional: 7 patches são `.fxp` órfãos

Dos 32 nomes de patch em uso, **7 não existem como `.SerumPreset`** — só como `.fxp` (Serum 1):

`[TONAL DRONE] - Cinematic Drone` · `LD - SATOSHI` · `[RISER 8BAR] - Forestlifter` · `PL - Whispers` · `[RISER 8BAR] - Moonshine` · `LD - ACID` · `Pluck - Powers of Ten [PML]`

`VERIFICADO` — busca em `/Library/Audio/Presets/Xfer Records` e nos packs: só há `.fxp`.
`INFERÊNCIA` — o som **está preservado no estado do plugin dentro do `.als` do set**, então toca. Mas não existe preset reutilizável: se a pista for recriada ou o estado perdido, **não há de onde recarregar**. Vale exportar o estado como `.SerumPreset` numa sessão com o Live aberto.

---

## 4. O que aplicar

1. **Camadas de baixo: 2, não 3.** O pack usa 2 no baixo e reserva 3 para lead/pluck. Testar remover uma camada do grave em um bloco e comparar.
2. **Release do ENV1 do baixo: 0,08–0,10 s** em vez de 0,20. Menos sobreposição, mais definição de nota.
3. **EQ interno no patch** (o pack tem em 69%): antes de abrir EQ no DAW, resolver dentro do Serum. Menos devices na pista.
4. **Phase distortion (`kPD_OSC`)** é o warp mais usado do pack (28) e não aparece em nenhum patch de referência lido. É uma via de sujeira controlada não explorada.
5. **Exportar os 7 `.fxp` como `.SerumPreset`** para eliminar o risco de perda.

## 5. Limites

- Os 25 patches de referência vêm de 8 packs diferentes (Odd Frequency, SAKYAMUNI, Electric Himalaya, PML e patches próprios do set), não de um pack desenhado com um propósito. A comparação BASS é a mais justa; a global é indicativa.
- 7 dos 32 nomes não puderam ser lidos (`.fxp`) — as médias do set de referência excluem esses 7. As 39 instâncias VST3 apontam para 32 nomes porque há repetição (o `Cinematic Drone` aparece em 4 pistas, o `GLIDE BASS 03` em 2, o `ARYTMO_ODYSSEY` em 2).
- Nada foi ouvido. "Densidade de patch" é contagem de estrutura, não julgamento de timbre.
