# DRIFT (PML Tech House) — as 8 faixas dissecadas

> Fonte: Production Music Live — "Tech House - Drift" / `PML - Tech House - Project Files/` (pack da Production Music Live)
> 8 músicas × 2 versões (Serum 1 e Serum 2) = 16 `.als`. **Toda a análise abaixo usa as versões Serum 2.**
> Método: leitura do XML do `.als` (pistas, devices, parâmetros, EQ, automação, notas, samples).
> Data: 25/10/2026. Nada foi ouvido — os valores são exatos, o resultado sonoro é `NÃO VERIFICADO`.

---

## 1. Ficha das 8 faixas

| Faixa | BPM | Pistas (sem returns) | Grupos | Notas MIDI | Compassos | Sends ativos | Devices | Lanes de automação |
|---|---|---|---|---|---|---|---|---|
| Arson | 130 | 32 | 4 | 502 | 124 | 0 | 91 | 17 |
| Brain | 128 | 26 | 4 | 517 | 152 | 0 | 82 | 13 |
| Chaos | 126 | 32 | 5 | 1.189 | 188 | 2 | 73 | 17 |
| Ether | 128 | 34 | 6 | 764 | 146 | 1 | 109 | 26 |
| Far | 122 | 19 | 3 | 96 | 144 | 1 | 55 | 5 |
| Greed | 132 | 28 | 5 | 289 | 128 | 0 | 80 | 15 |
| Ring | 128 | 38 | 5 | 713 | 137 | 0 | 116 | 11 |
| Work | 131 | 32 | 6 | 417 | 176 | 0 | 90 | 6 |

`VERIFICADO` — contagem direta do `.als`.
`INFERÊNCIA` — o pack é feito para vender sample pack: as faixas são curtas (124–188 compassos ≈ 3,8–6,0 min a 128 BPM), densas em pistas e **pobres em notas** (96 a 1.189). Quase tudo é loop de áudio ou loop MIDI de 4 compassos repetido.

---

## 2. Arquitetura de sessão

### 2.1 Grupos por função, sempre
Os grupos são nomeados pela função, não pelo instrumento:
`Drums` · `Cymbals` · `Bass`/`Bassline` · `Instruments` · `Fx` · `Vocals` · `Bridge Loop`.
`VERIFICADO` em todas as 8.

### 2.2 Densidade de FX
**2,88 devices por pista em média** (55 a 116 devices em 19 a 38 pistas; faixa 2,28–3,21). A mediana de um corpus de 55 projetos medidos nesta pesquisa também é **2,88** — o Drift é a definição da régua, não um outlier.

### 2.3 Returns: um template fixo de 2
Em **7 das 8** faixas o par é idêntico:

| Return | Cadeia | Ajuste medido |
|---|---|---|
| `A-Hall` | Reverb → Eq8 | **Decay 7,00 s** · PreDelay 2,5 ms · BandLow 2,3 kHz largura 6,0 · ShelfHigh 3 kHz +0,45 dB · ShelfLow 100 Hz +0,20 dB · Chorus interno ON |
| `B-Echo` | Delay → Eq8 | Sync ON · PingPong ON · tempo esquerdo/direito iguais · **Feedback 0,21** |

Exceção: **Chaos** troca por `A-Echo` (Delay fb 0,50) + `B-Reversed Delay` (Echo → Eq8 → Ducking → AutoPan → 2 Utilities).

### 2.4 Os sends estão desligados
**5 das 8 faixas têm ZERO send ativo** (Arson, Brain, Greed, Ring, Work). As outras usam 1 ou 2 pistas.
O valor mínimo de send no Live é `0,000316` (−70 dB): todas as pistas estão nesse valor.

`INFERÊNCIA` — o espaço deste pack **não vem do send**: vem de reverb em insert, por pista. É o oposto do Tim Engelhardt (ver doc da trajetória dele). Quem escuta o pack e tenta reproduzir "com sends" está copiando a parte que não faz som.

---

## 3. Os racks que se repetem em toda faixa

Três racks salvos são usados como peças de Lego. Todos são `AudioEffectGroupDevice` com nome próprio:

| Rack | Conteúdo real | Macros | Uso |
|---|---|---|---|
| **Mix Control** | `StereoGain` (Utility) | `Trim`, `Phase Flip` | em **quase toda pista** — é o controle de ganho fino e fase |
| **Clipper** | rack interno → `Saturator` (Type 5) + `StereoGain` | `Clip`, `Gain` | no master, no bass bus, no kick, no drums bus |
| **Ducking** | `MxDeviceAudioEffect` (Max for Live) + `StereoGain` 0,912 | — | nas pistas de baixo (sidechain/volume shaping) |

`VERIFICADO` — estrutura lida do XML.
`INFERÊNCIA` — a existência de um rack "Mix Control" em 20+ pistas seguidas mostra que o produtor **não mixa no fader**: mixa no Trim do rack (o fader fica em 0 dB na maioria).

---

## 4. Master: a receita do volume

Cadeia mais comum (6 das 8 faixas): **Compressor2 → Clipper → Limiter → Limiter**.
Variações: Arson e Greed põem um Clipper antes do compressor (`Clipper → Comp → Clipper → Lim → Lim`); Chaos usa Saturator no lugar do Clipper; Far e Ring inserem Multiband.

Ajustes medidos:

| Device | Parâmetro | Valor |
|---|---|---|
| Compressor2 | Threshold | **−6,0 dB** (−8 dB em Far) |
| Compressor2 | Ratio | 4,0 |
| Compressor2 | Attack | **0,01 ms** (mínimo) |
| Compressor2 | Release | 15 ms |
| Compressor2 | Knee | 0 |
| Clipper | macro `Clip` | **68,8 a 84,7** (0–127) |
| Clipper | macro `Gain` | 63,5 (centro) |
| Limiter 1 | Release | 1 ms / 100 ms / 300 ms (varia) |
| Limiter 2 | Release | 100 ms |

`VERIFICADO`.
`INFERÊNCIA` — attack de 0,01 ms não é glue: é **prensagem de transiente**. O compressor do master aqui funciona como um clipper lento; o Clipper (saturator) faz o corte de pico e os dois limiters seguram.

---

## 5. Baixo: duas arquiteturas, e nenhuma é "um patch"

### 5.1 Separação por camada de timbre (Arson)
Um único loop de 4 compassos (`PML_TH3_Bass_Loop_004_Layer1..Layer5`) foi **fatiado em 5 pistas**, cada uma com seu Serum e sua cadeia:

| Pista | Notas | Registro | Cadeia |
|---|---|---|---|
| Bassline | 272 | 63–66 | Serum → Mix Control → EQ ×3 → Ducking → Comp (thr −27 dB) |
| Bass Dist 1 | 48 | 63–66 | Serum → Mix Control → EQ ×2 → Ducking |
| Bass Pluck | 10 | 63–66 | Serum → Mix Control → EQ |
| Bass Dist 2 | 10 | 63–64 | Serum → Mix Control → EQ → Ducking → EQ |
| Bass Dist 3 | 22 | 63 | Serum → Mix Control → EQ → Ducking → rack |
| Bass Stab | 2 | 64 | Serum → Mix Control → EQ |
| Subdrop | 2 | 61 | Serum → Mix Control |

### 5.2 Separação por registro (Brain, Ether, Ring, Work, Greed, Chaos)
Ex.: **Brain** — `Bass Sub` (43 notas, 49–61) + `Bass Mid 1` (128, 49–61) + `Bass Mid 2` (64, 49–61).
**Ether** — `Sub 1` (145), `Reese 1` (35), `Sub 2` (11), `Bass Saw` (29), `Bass Fm` (9), `Reese 2` (3), todos 52–61.
**Ring** — `Bass Pluck` (86, 65–78) + `Bass Sub` (40, 65–68) + `Bass Saw` (60, 65–68).

### 5.3 Os números que se repetem no baixo
- Compressores de camada: **threshold −20 a −28 dB, ratio 4, attack 0,01 ms, release 30 a 120 ms**
- Compressor do **bus** de baixo: **threshold −20/−28/−35 dB**, ratio 4, release 30–49 ms
- O bus `Bass` sempre tem **Clipper** ou **GlueCompressor** depois do compressor
- O `Ducking` (M4L) aparece em **6 das 8** faixas (Arson 4 pistas · Brain 3 · Ether 3 · Greed 2 · Chaos 1 · Work 1) — o "pump" do baixo é por device dedicado, não por sidechain do compressor

`VERIFICADO` — valores lidos.
`INFERÊNCIA` — o baixo nunca é um patch só: é **2 a 7 pistas** com o mesmo conteúdo dividido por caráter (sub / corpo / pluck / distorção).

---

## 6. Kick: sempre um one-shot, nunca um sintetizador

**8 de 8** usam `OriginalSimpler` com um único sample (`PML_TH3_Kick_004_F#_Arson`, `PML_DPV*`, etc.) tocado em **C4 (MIDI 60) fixo** — 1 a 2 notas por clip, sem variação de altura.

### 6.1 Curvas de EQ medidas (Eq8)

| Faixa | Low cut | Corte principal | Boost principal | Extras |
|---|---|---|---|---|
| Arson | 102 Hz | **278 Hz −3,1 dB Q1,9** | **3.997 Hz +3,1** | 1.467 Hz +1,6 |
| Chaos | 160 Hz | 174 Hz −3,8 Q1,9 | **163 Hz +5,8 Q3,0** | 958 Hz +3,6; 44 Hz +1,1 |
| Ether | 109 Hz | **202 Hz −1,6 dB Q18** | — | Clipper no insert |
| Far | — | **464 Hz −15,0 dB Q4,8** | — | 206 Hz −1,9 Q5,0 |
| Greed | **215 Hz** | — | — | Ducking + Clipper no kick |
| Ring | 109 Hz | 153 Hz −6,1 Q6,4 | 182 Hz +3,6 | 1.564 Hz +4,6 Q0,37 |
| Work | — | 303 Hz −2,1 Q2,9 | — | |
| Brain | 111 Hz | — | — | só corte de baixo e de agudo |

Regras que aparecem no conjunto:
1. **High cut em 12 kHz** — **8 de 8**, e sempre em duas bandas duplicadas (banda 6A e 6B).
2. **Corte entre 150 e 464 Hz** (a "caixa" do kick) — **6 de 8** (Arson, Chaos, Ether, Far, Ring, Work), de −1,6 a −15 dB. Brain e Greed não cortam o médio.
3. **Low cut entre 100 e 215 Hz** — **6 de 8** (Far e Work não têm). O kick deste pack é curto, sem sub.
4. Quando precisa de peso, o boost é **na faixa de 163–182 Hz**, não abaixo de 60 Hz.

### 6.2 Cadeia de insert
`OriginalSimpler → Mix Control → Eq8 ×1–3 → [Clipper] → [Ducking] → [Compressor2 thr −1 a −6 dB ratio 4 attack 0,01 release 30]`

---

## 7. Automação: o arranjo é feito ligando e desligando devices

Contagem total por faixa: **5 a 26 lanes**. O que elas controlam:

| Tipo de alvo | Onde aparece | Contagem típica |
|---|---|---|
| `On` de um device (Eq8, Compressor2, AutoFilter, Delay) | todas | 3 a 126 pontos |
| `ParameterValue` de plugin (Serum 2 / Diva) | todas | 5 a 76 pontos |
| `MacroControls.N` de rack | Chaos, Ether, Arson | 4 a 69 pontos |
| `Cutoff` de AutoFilter (risers, pads, snare build) | 6 das 8 | 3 a 27 pontos |
| `DryWet` de Delay (vocal) | **2 das 8** (Arson, Brain) | 4 a 8 pontos |
| `Freq`/`Gain` de Eq8 | Arson, Ether, Ring | 2 a 5 pontos |

Casos extremos medidos: `Compressor2 On` com **126 pontos** (Arson/Bassline) e `Eq8 On` com 18 pontos — ou seja, o compressor do baixo é ligado e desligado compasso a compasso para criar dinâmica de arranjo.

`INFERÊNCIA` — é a diferença de método em relação ao Tim Engelhardt: aqui a automação **não varre parâmetros**, ela **troca o estado do device**. Isso é mais barato de desenhar e mais difícil de mixar, porque cada troca muda o timbre de forma discreta.

---

## 8. Estrutura de arranjo: quanto tempo o kick fica fora

Medido por interseção dos clips da pista de kick:

| Faixa | Compassos | Kick presente | Buracos ≥ 2 compassos |
|---|---|---|---|
| Greed | 129 | **99%** | nenhum |
| Brain | 153 | 98% | 31–32 (2) |
| Chaos | 189 | 97% | 185–189 (5) |
| Arson | 125 | 86% | 31–32 (2), **57–68 (12)**, 83–84 (2) |
| Ether | 147 | 80% | 37–40, 56–58, 74–78, **83–93 (11)**, 111–114 |
| Ring | 137 | 75% | 15–16, 25–31 (7), **61–79 (19)**, 133–137 |
| Far | 145 | 74% | 15–16, **33–48 (16)**, **81–96 (16)** |

`VERIFICADO`.
`INFERÊNCIA` — o padrão é: **faixa que precisa de hipnose mantém o kick 97–99% do tempo**; faixa que precisa de contraste tira o kick por **11 a 19 compassos** (uma seção inteira), não por 2–4.

Para contraste: um set de psytech em construção, medido no mesmo dia, manteve o kick em **70%** de 241 compassos, com buracos de 16, 8, 16, 8 e 25 compassos — mais perto do Far/Ring (74–75%) do que do miolo do pack (97–99%), e com um buraco final de 25 compassos, maior que qualquer buraco destas 8 faixas.

---

## 9. MIDI: o dialeto do pack

95 arquivos `.mid` com nota, **3.344 notas**, PPQ 96 em todos.

- Notas por arquivo: mínimo 1 · **mediana 32** · máximo 144
- Registro: 38 a 84 (D2 a C6)
- Classe de altura dominante: **F# (703)**, depois F (369), G (330), D (328), E (323), D# (315)
- Intervalos mais comuns: **0 (1.766 — nota repetida!)**, −1 (165), +1 (158), +7 (145), +3 (138)
- Velocity: mínimo 11 · **mediana 99** · máximo 127

`INFERÊNCIA` — o centro é **F# (ou D# menor/F# maior)** e o vocabulário é de **semitom e quinta**, não de escala. Metade dos intervalos é zero: são loops de baixo em nota pedal, típico de tech house.

Comparação com os outros packs (mesma medição):

| Pack | Arquivos | Notas | Notas/arquivo (mediana) | Centro | Intervalos dominantes |
|---|---|---|---|---|---|
| **Drift** | 95 | 3.344 | 32 | **F#** | 0, ±1, +7 |
| Tim Engelhardt | 37 | 1.183 | 23 | C/F/G/D | 0, **+2**, +4, +7 |
| Cercle Vol.4 | 100 | 1.648 | **8** | F | 0, +5, +3, ±19 |
| Giants (assets) | 1.034 | 34.001 | 26 | C/G/F | 0, ±2, +12 |

---

## 10. Presets e samples

- **152 `.SerumPreset`** (Serum 2) nomeados por faixa e função: `17 - Arson - Bass Pluck`, `26 - Arson - Lead Alarm`, `27 - Arson - Arp High`, `29 - Arson - Noise Uplifter`… Prefixos reutilizáveis: `BS` 22 (bass), `LD` 16 (lead), `PL` 11 (pluck), `PD` 6 (pad), `STB` 2 (stab).
- **122 `.fxp`** — presets de **Serum 1**. Mortos sem o Serum 1 instalado (não carregam); é por isso que a versão "(Live 11.1 and Serum)" de cada projeto fica inutilizável nesse cenário.
- **527 WAV**, em 4 pastas: Sample Pack (333), Project Files (116), Serum Presets (57), Bonus Vocal (21). Por nome: HAT 66, VOCAL 63, **KICK 53**, CLAP 47, PERC 44, TOP 33, SNARE 28, LOOP 24, BASS 20.

`VERIFICADO` — contagem de arquivos e nomes.

---

## 11. O que aplicar (por ordem de impacto)

1. **Mix Control em toda pista** — criar um rack `Trim` (Utility) + `Phase Flip` e inserir nas pistas; isso deixa o fader no centro e o ajuste fino num lugar só.
2. **Clipper como rack de bus** — para quem já tem compressão de bus, o estágio que costuma faltar é a saturação/clip antes do limiter. O rack do Drift é `Saturator Type 5` + `Utility`, com macro de drive. Aplicar no bus de graves e no master, e só depois de um gate de true peak.
3. **Kick: dois Eq8 em série, high cut 12 kHz nas duas bandas 6A/6B** — é literalmente o que 8 de 8 fazem. Se o kick já tem EQ, verificar se tem o corte de agudo duplicado.
4. **Corte de 150–460 Hz no kick** — o intervalo medido nos 8 é −1,6 a −15 dB. Se o kick tiver corpo sobrando, é ali.
5. **Baixo em camadas** — o padrão do pack é dividir **sub / corpo / pluck / distorção** com o mesmo MIDI, cada um com seu filtro. Não é mais conteúdo: é o mesmo conteúdo separado.
6. **Ducking por device** — o pack usa um M4L `Ducking`; quem já usa sidechain ducking por device cumpre o mesmo papel. Não é gap.
7. **Automação de `On` de device** como ferramenta de arranjo — o pack usa 126 pontos de `On` no compressor do baixo; poucos pontos de `On` são espaço não explorado.

## 12. O que NÃO copiar

- **O master com 2 limiters e compressor a 0,01 ms** — é receita de loudness de pack; para quem tem gate de true peak e masterização separada, não serve.
- **Low cut de 215 Hz no kick (Greed)** — é um kick sem corpo, escolha da faixa, não regra.
- **7 s de decay no hall como padrão** — o Tim Engelhardt usa 2,2 s (hall) + 9,8 s (cauda). 7 s é o meio-termo do template, não uma decisão estética.
- **Sends zerados** — funciona neste pack porque o espaço é insert; em um projeto em que o espaço é decisão estética de produto, o send ganha função.

## 13. Limites

- Nada foi ouvido. Nenhum preset foi carregado no Live.
- Os `.fxp` (122) não foram lidos — formato Serum 1, sem aplicação prática nesse cenário.
- O rack `Ducking` é um device Max for Live: o XML mostra o wrapper, não os parâmetros internos. O que ele faz é `INFERÊNCIA`.
- Os 527 WAV foram classificados por **nome de arquivo**, não por áudio.
