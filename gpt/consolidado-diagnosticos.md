# Consolidado diagnosticos
Psytech Lab v0.1.1 · 03/11/2026

## AUDITORIA-GRUPO-EFEITOS-20261016.md

# Auditoria de um grupo de efeitos de transição (FX) — estudo de caso, 14 canais (16/10/2026)

> Estudo do acervo psytech-lab, anonimizado de um set de referência. Régua de referência externa usada:
> biblioteca de transições com DNA medido em 1168 transições de referências e medição arquivo-a-arquivo
> das fontes candidatas. Nomes de canal do set substituídos por função; packs de biblioteca citados pelo nome.

## 1. O mapa (14 canais, 361 clipes de áudio, 41 fontes únicas)

| função do canal | cadeia | lanes (automação) | clipes | fontes principais | fader | sends A/B |
|---|---|---|---|---|---|---|
| uplifter sintético | Serum 2 FX + EQ + AutoFilter | **nenhuma** | 1 | uplifter de biblioteca (6,5 kHz) | −18,7 | 0/0 |
| escape de ar (exhaust) | **Serum 2 (patch próprio)** + AF HP 140 + Utility 156% | Volume (−3..0) · **Send0 (−9)** | 52 (MIDI) | patch | −3,0* | lane/0 |
| tape-stop | 2 AutoFilter (1 off) | Volume (−3..0) | 22 | **bow_scratch_chuff** (3,8 kHz/40% >4k) | −3,0* | −16/−18 |
| raspagem (scrape) | AF + Utility | Volume · Send0 (−10,2) | 72 | **bow_scratch_chuff 66×** + FX_01_SUCTION | −3,0* | lane/0 |
| rugido (roar) | **Roar** + AF + Utility | Volume · Send0 (−8,7) | 18 | organic_reverse_tail (245 Hz) + reverse snare (morto) | −3,0* | lane/0 |
| cauda reversa (reverse) | 3 AF (HP180 + LP12k + 1 off) | Volume (−3..0) | 90 | White_Noise_Breath (1,7 kHz) 37× + organic_reverse_tail 32× | −3,0* | −15,2/0 |
| puxada de caixa (insnare) | EQ + Utility (**sem filtro, sem automação**) | só Speaker | 42 | AN_Inhale_Reverse 37× (1,6 kHz) + galope de cascos 5× | 0,0 | 0/−16 |
| echoroll (throw 1–16) | Delay 39% + AF BPF + Pan + EQ + Utility + Serum 2 FX | Volume (**−39,5..−10,5**) | 39 | AN_Exhale_Throw 28× (1,6 kHz) | −11,0* | 0/0 |
| downer (descida de exaustão) | AF + Saturator + Reverb + **Ducker (kick)** + Utility + Serum FX | Volume · Send0 (−8,7) · **6 lanes de On** | 47 | fx_transition_splash 22× + downlifter 9× + **fonte morta 4×** | −4..−7,9* | lane/0 |
| último sopro (last breath) | Simpler (braam) + EQ + Utility + Serum FX | Volume (−18,7..−9) · Send0 (−6,9) | 18 (MIDI) | sample braam | −10,5* | lane/0 |
| riser | EQ + AutoFilter | Pan + **filtro 250→10k** | 19 | risers reversos (15,5 s) + trailer boom | 0,0* | 0/0 |
| stutter filtrado | AutoFilter | **Volume 413 ev** + Pan + **filtro 800→3.200** | 6 | tape rewind (3,1 kHz/21%) | −4,5 | −14/−16 |
| whoosh flyby | AutoFilter | Volume (−60..−9) + Pan + filtro 400→3.200 | 3 | elemento de biblioteca (3,7 kHz) | −9,0* | 0/0 |
| riser orgânico | AF + Serum 2 FX | Volume (−40..−9) + Pan + filtro 300→900 | 2 | rise orgânico (4,4 kHz/55%) | −9,0* | 0/0 |

`*` fader cosmético: a lane de Volume é quem manda no som final — lição geral do set (vale para o grupo todo).

## 2. Achados (verificados no arquivo)

1. **Duas fontes mortas — 5 clipes mudos no grupo.** Um sweep de 8 beats do pack Music4Aliens Stems
   (`music4aliens_moog_sweep_8beat.wav`) tinha 3,75 s de **silêncio digital** (máx −91,0 dB) e tocava **4×
   no downer** — incluindo a virada para o compasso 49. Um reverse snare 16th (`in_snare_16th_reverse.wav`)
   media máx **−58,9 dB** (inaudível) e tocava 1× no roar. Lição: **auditar o áudio real da fonte, não o nome
   do arquivo**.
2. **Material duplicado entre canais:** `bow_scratch_chuff.wav` era fonte de **74 clipes** em dois papéis
   diferentes — 66× no scrape e 8× no tape-stop (+14× da variante `_pitch_drop_bar56`): "raspagem" e
   "trava fita" eram **o mesmo som**. Já `organic_reverse_tail.wav` (centroide **245 Hz**, 0% >4k) alimentava
   **50 clipes** em 3 canais (reverse 32×, roar 17×, scrape 1×).
3. **O grupo era escuro; o DNA das referências é brilhante.** Refs (1168 transições): `sweep-longo` 53%,
   centroide **~3,0–3,5 kHz**, **~30–34% da energia acima de 4 kHz**. Fontes do set: organic_reverse_tail
   245 Hz/0% · fx_transition_splash 1,1 kHz/1,7% · downlifter 744 Hz/0% · uplifter 913 Hz/0,4% ·
   inhale/exhale 1,6 kHz/~5% · White_Noise_Breath 1,7 kHz/3,8%. Fontes brilhantes e alinhadas:
   bow_scratch_chuff 3,8 kHz/40% · tape rewind 3,1 kHz/21% · whoosh 3,7 kHz/11% · rise orgânico 4,4 kHz/55%
   (7,7 s) · uplifter 6,5 kHz/67% (6 s) · crash 7,7 kHz/**95%** (fino demais).
4. **Desenho real (síntese/plugin) × biblioteca:** com cadeia própria — exhaust (patch Serum), downer
   (cadeia completa com ducker), riser orgânico/echoroll/uplifter (Serum FX). **Sample + filtro:** tape-stop,
   scrape, reverse, roar, stutter, insnare (6 canais) — candidatos naturais a camada sintética própria.
5. **O insnare era o canal mais fraco:** 42 clipes, sem lane de volume, sem filtro, cadeia só EQ+Utility.
6. **O retorno de eco pontual estava em zero nos 14 canais** (o retorno de cauda só em 5, por lane). Ajuste
   aplicado: stutter −14/−16, tape-stop −16/−18, reverse −15,2, insnare −16.
7. **Cobertura de fronteiras (7 seções):** 7/7 — tape-stop, scrape, reverse, insnare · 6/7 — downer ·
   5/7 — echoroll, last breath · 4/7 — roar · 3/7 — riser, stutter · 2/7 — orgânico · 0/7 — whoosh
   (flybys no meio de seção, por desenho).

## 3. Plano de desenho (executado por fatias)

1. **Consertar o que está mudo** (prioridade): trocar a fonte dos 4 clipes do downer (sweep morto) por um
   corte vivo de 3,75 s (**8 beats**) da última rajada do stem original, gain 0,4, mapeamento 1:1 — refs
   mortas = 0 na verificação; e trocar/remover o reverse snare inaudível do roar.
2. **Diferenciar scrape × tape-stop** (mesma fonte): dar ao scrape uma camada própria (fricção com corpo —
   Corpus, timbre de marimba afinada, ~495 ms, Material 20% · Brightness 15% · 50% wet) ou trocar a fonte de
   um dos dois; no tape-stop, LP 2,5 kHz · Res 40% · Drive 25%.
3. **Subir o brilho do grupo rumo ao DNA** (centro 3–3,5 kHz, ~1/3 >4k): camada de ar (ruído HP 2 kHz + shelf)
   nos gestos escuros — reverse, roar, insnare, downer, uplifters.
4. **Insnare:** cadeia de verdade (AF + saturação + send) + lane de volume.
5. **Camada sintética própria** nos 6 canais "sample+filtro": 2–3 elementos por gesto (corpo + ar + cauda),
   no padrão dos selos de referência.
6. **Automação de seção** onde falta: o uplifter sem nenhuma lane e o nível do insnare por seção.
7. Curadoria das 41 fontes (361 clipes; sobreposição de papel entre canais) — decisão de escuta.

## 4. Lições desta auditoria

- **A checagem original olhou só Auto Filter** — três canais já tinham High Pass 48 dB dentro do EQ Eight
  (121 / 221 / 121 Hz). O item "dar HPF aos três" **não existia**: a limpeza de grave ali já estava feita.
  Sempre conferir **todos** os devices da cadeia antes de propor o conserto.
- **Ressonância no caminho do kick:** Filter Resonance do downer estava em 0.85 e o pico caía na zona do
  kick → reduzido a 0.25 (verificado por read-back).
- **Ferramenta de diff cega:** o comparador de devices não enxergava parâmetro de device de topo (fora de
  rack) — bug silencioso que faria qualquer revisão futura declarar "nada mudou". Corrigido e revalidado
  (o diff da rodada é a própria prova: 9 diffs em 3 canais).
- **Fader cosmético × lane:** medir a lane de volume, não o fader.
- Pendência de medição: o resultado no **render** (as lanes mudam o nível final de cada gesto; a régua de
  brilho acima é da fonte, não do canal somado).


---

## AUDITORIA-GRUPO-SYNTHS-20261016.md

# Auditoria de um grupo de synths e madeiras — estudo de caso, 18 canais (16/10/2026)

> Estudo do acervo psytech-lab, anonimizado de um set de referência (arquivo .als lido offline + estado vivo).
> Nomes de canal substituídos por função; patches de biblioteca citados pelo nome. Nenhum trecho depende de
> estado pessoal do autor.

## 1. O que o grupo é (mapa completo — 18 canais, 502 clipes)

**Portadores em potencial (têm sustain):**

| canal (função) | fonte real (medida) | característica | clipes |
|---|---|---|---|
| braam | Serum `BA - Vision Blurred` | braam **estrangulado** por LP 171 Hz/res 49% — virou rumor | 34 |
| cello staccato | Simpler (sample de cello) + Serum FX `BR - Slow Synth Brass Aberto C#` | cello staccato + brass aberto (2 camadas) | 44 |
| brass lento | Serum `BR - Slow Synth Brass` | brass lento lush (sustain 0.63) — avaliado de escuta como demais para o papel | 22 |
| groove de madeira | loop de 16 beats de pack (Music4Aliens) ×23 + perc | groove de 15 s repetido — quase sem topo (centroide 391 Hz) | 27 |
| sequência analógica | Serum `ST - Stab 2 Trust Me` + fills brilhantes | stabs/fills | 22 |

**Família madeira (percussiva por natureza):**

| canal (função) | fonte | nota |
|---|---|---|
| madeira 3D | Simpler `Perc Wood.wav` + Serum `GREENWOLVE_WOOD_LEAD` | Corpus OFF (afinado em C#4 via Tune C4 + Transpose +1 st — **não é defeito**) |
| madeira ressonante | Simpler `Perc Wood.wav` | Corpus OFF idem; 13 clipes |
| perc orgânica | Simpler `[FREAKAUDIO] PERC SHOT - 001.wav` | 31% >4k, centroide 3,5k |
| madeira clique seco | Simpler `Perc Wood.wav` | o canal mais denso (107 clipes) |

**Família glitch (nove canais, patches Serum):**

| canal (caráter) | patch carregado | caráter medido do patch |
|---|---|---|
| glitch seco | `[DRY GLITCH] BUSH MODULAR GLITCH` | comb 38%, pan aleatório, percussivo |
| formante | `ST - Million Pieces` | LP24 moog res 56% + HyperD — blip falante |
| granulador | `[SQUELCH BODY] BUSH VELVET FRICTION` | **pink noise** em bandpass (leito de ruído por projeto) |
| FM | `LD - UH HUH` | FM curto |
| resposta | `[GAP ACCENT] BORRATCHA TENEBROSA` (.fxp) | gap accent + Redux2 com lanes até beat 352 |
| espaço | `[GLITCH DELAY] BUSH MODULAR SPACE GLITCH` | eco filtrado — **desligado** |
| shimmer | `PL - Whispers` (.fxp) | LP **11,9 kHz** (o topo mais aberto do grupo) — suspeito nº 1 do chiado |
| squelch | `[SQUELCH BODY] SQUELCHY` | **sustain 1.00, bandpass 150–1100 Hz — CAPAZ DE SEGURAR, só recebia gestos** |
| tickler | `LD - ACID` | HP 105 res 52% + LP 1742 res 48% (assobio) — **desligado** |

**Mídia:** 9 fontes verificadas no disco — **nenhuma faltando** (o loop de madeira resolve no pack
Music4Aliens Stems). Nenhum clipe mudo (ao contrário do grupo de efeitos).

## 2. Estado ligado/desligado — a semântica que estava errada

Lição geral de auditoria offline de `.als` (Live 12):

- Neste set o arquivo **não tem tag Mute/Solo no mixer**; o `track.mute` da LOM reflete o liga/desliga
  (`Mixer/Speaker`), e **a lane de Speaker vence o Manual** (canal com Manual false + lane true = LIGADO).
- Ler save antigo engana: "o grupo está mudo pela lane de Speaker" era leitura de save desatualizado — a lane
  era `true,true` (não mudo nada). A arqueologia de saves mostrou canais alternados entre datas — **auditar
  sempre o estado atual, não o histórico**.
- Estado efetivo medido: 3 canais desligados (brass, espaço, tickler), 15 ligados, grupo ligado (lane all-true).

## 3. O chiado ("tá chiado ruim") — medido, sem chute

| fonte | centroide | >4 kHz | natureza |
|---|---|---|---|
| `Perc Wood.wav` | 3.270 Hz | **28,7%** | madeira brilhante (percussiva) |
| perc shot de pack | 3.492 Hz | 31,4% | idem |
| fill longo brilhante | 3.959 Hz | **52,1%** | fill |
| granulador | — | — | **pink noise contínuo por projeto** |
| shimmer (whispers) | — | LP 11,9k | patch de sussurro, topo mais aberto |
| tickler (acid) | — | — | ressonâncias gêmeas (desligado) |

Soma: o topo do grupo = madeira brilhante + dois patches de ruído/sussurro + fills — **textura, não defeito**.
O desenho certo é curar papéis (evento × leito) e diferenciar, não procurar "o bug".

## 4. Execução registrada (com prova) e a regra da ponte Serum

Ação aplicada no braam: patch novo `BR - Braam Aberto Peak Time C#` gerado sob medida e carregado; LP do canal
aberto de **171 Hz/49% → 15,0 kHz/15%**; Auto Filter High-pass **90,0 Hz / 10%** inserido no fim da cadeia.
Verificação: diff de devices mostrou **10 diffs em 2 canais**; `als_audit` do arquivo ok (72 tracks, 49.531 notas).

**Regra da ponte (corrigida e medida):** ao carregar patch por Bank/Program no Serum 2,
- **Bank = nº da PASTA** (User raiz = 46; medido — carregou);
- **Program = posição do preset na lista viva do plugin, em ordem alfabética, incluindo arquivos novos**
  (medido em dois pontos);
- o `presets.db` **não** é reescrito — a lista vive na memória do plugin, atualizada sem gravar o DB;
- ⚠️ os números deslocam se arquivos entrarem/saírem da pasta — **recalcular sempre** (mapa bank/PC por nome).

## 5. Pendências de curadoria (decisão de escuta)

- Trocar o brass ("o serum dele é demais") por um patch de resposta peak-time já gerado — não aplicado; fica
  a critério da escuta (mute/ouvir antes de trocar).
- Curadoria de mute (quem fica/sai) = decisão de ouvido — o grupo fica no ar para isso.
- Kit anti-chiado (params exatos para fechar o topo de shimmer/FM/glitch seco) e material de "portador"
  sustentado (notas longas no squelch/brass) — no doc de desenho, não aplicados.


---

## AUDITORIA-SET-KUNI-P0.md

# Auditoria read-only: um set contra o framework KUNI-P0 (12 camadas)

> Estudo do acervo psytech-lab, anonimizado. Data: 05/09/2026 · BPM 132,00 · tonalidade C#m.
> Alvo de referência: Fox Artemis / AlpaKa / Yao Ofosu + Tech House BR 2018.
> O framework KUNI-P0 são as 12 camadas de checagem (transiente do kick, low-end mono, saturação de
> harmônicos etc.). Nomes de pista do set substituídos por função.

| Elemento | Status | Checagem contra as 12 camadas | Evidência técnica |
|---|---|---|---|
| **KICK** | **ALIGNED** | Repetibilidade de transiente, envelope seco (232 ms), bate solteiro na cabeça (0.0) deixando espaço para o baixo. | Simpler + Drum Buss. RMS e pico 100% consistentes. |
| **SUB BASS [C#1]** | **ALIGNED** | Sub 100% mono (<120 Hz), phase retrigger estável no Serum 2, zero reverb/delay no sub, notas curtas no pocket (0.5/0.75). | Bass Mono 120 Hz ativo. Volume −2 dB. |
| **MID BASS [TEXTURE]** | **ALIGNED** | Saturação analógica nos harmônicos (150–300 Hz), corte estrito em 345 Hz, decaimento suave no break (velocity 85→20). | Auto Filter + EQ Eight LP 345 Hz + Saturator Soft Sine. |
| **PSY SYNTH [STABS]** | **ALIGNED** | Atonalidade e esparsidade (estilo Yao Ofosu). Zero arpejos de Goa Trance. Stabs secos percussivos em C#3/D3 com Ping-Pong delay. | 5 a 7 stabs por bloco de 4 compassos. High-Pass em 250 Hz. |
| **GLITCH CONVERSA** | **ALIGNED** | Micro-sound design estéreo, call-and-response nos buracos vazios, sem disputar médios. | 8 micro-glitches de pack, High-Pass 448 Hz, Delay Ping-Pong 35% wet. |
| **TOP + PERC GROOVE** | **ALIGNED** | Condução 909 + congas ativas no break. Evita corte brusco e mantém o balanço de quadril. | Congas de pack + perc swing, High-Pass 317 Hz, volume −16 dB. |
| **ATMO [drone C#m]** | **ALIGNED** | Minimal pitch motion (drone estático), alta tensão atmosférica, baixa atenção rítmica. | Drone dark contínuo sem revelar acordes/melodias. |
| **TRANSIÇÕES & RESPIRO** | **ALIGNED** | Antecipação por subtração (1,5 tempos de vácuo) + fill de conga chamando o drop. Zero risers EDM. | — |
| **AGRUPAMENTO NO DAW** | **DIVERGENT** | Organização visual: baixos e synth criados fora do grupo esperado. | Áudio ok; painel vertical desorganizado (observação de organização, não de som). |
| **VOCAL COM MALÍCIA** | **UNKNOWN** | Oportunidade estagiada: vocal chop curto e malandro no break ainda não inserido. | Trecho vazio no break aguardando escolha de sample. |

---

## Síntese da auditoria read-only

- **8 elementos ALIGNED:** a base técnica, o low-end, os stabs no estilo do artista de referência (Yao Ofosu),
  a conversa em 3D e as congas do break cumpriam rigorosamente as 12 camadas do framework.
- **1 divergência de organização visual (não sonora):** agrupamento de pistas no DAW.
- **1 oportunidade pendente (UNKNOWN):** vocal falado/chop com malícia no break — decidir por escuta.


---

## AVALIACAO-SINFONIA-20260924.md

# Avaliação estrutural de um arranjo sinfônico — 240 compassos, 128 BPM (24/09/2026)

> Estudo do acervo psytech-lab, anonimizado de um set de referência. O original trazia as tabelas completas
> de clipes por canal do set (estado da obra, com nomes de canal e clipe); essa parte é estado puro e foi
> condensada. Esta versão conserva o **método de auditoria**, as **categorias de defeito**, as **contagens**
> e a **medição de ar por bloco** — que são transferíveis.

Método: parse do XML gzipado do `.als` (clipes de arranjo, notas, keys) + medição ffmpeg por bloco no export
MP3 do projeto (465 s / 7:45, 320 kbps). Marcas: VERIFICADO (lido/medido) · INFERÊNCIA · NÃO VERIFICADO.

## 1. Método de auditoria (replicável)

- Ler cada clipe de arranjo dos canais melódicos (no caso auditado: 6 solistas + pad + acid + braam,
  ~150 clipes entre bars 1 e 232) e medir por clipe: nº de notas, notas/beat, duração média, registro
  (nota MIDI mín–máx) e classes de pitch.
- Verificar **notas coladas no fim do clipe** (a nota ultrapassa o fim do clip → som cortado no arranjo).
- Verificar **registros fora da faixa** do estilo (no caso: notas MIDI 73–85 = oitavas 5/6, acima da
  faixa-sombra frígia definida pelo projeto).
- Verificar **densidade "sem ar"** (notas/beat absurdas: 18, 4,5 e até 61,7 n/beat em um clip de 1 compasso —
  uma fanfarra de guerra e um interlink de flauta).
- Marcar clips **vazios** (existem, sem notas) e clips cujo **nome não bate** com o conteúdo.

## 2. Resultado agregado do caso (VERIFICADO)

- **46 apontamentos** de estrutura, concentrados em 5 famílias: trombeta de pico, kanun dedilhado, flauta
  líder (duduk), pad sinfônico e vozes/acid/braam.
- Categorias: **CORTADO** (notas coladas no fim do clip — o tipo mais comum, inclusive nos drops),
  **OITAVA 5/6** (notas MIDI 73–85 fora da faixa do projeto), **SEM AR** (densidade alta sem respiro),
  **VAZIO** (2 clips de pad sem nota nenhuma).
- Padrão útil: os clipes com nome de "fanfarra/clímax" eram exatamente os que concentravam nota colada +
  densidade sem ar — o pico de energia escondia o pior corte (ex.: um clip de fanfarra do drop 2 com 18
  notas/beat e 34 notas coladas).
- Solistas ativos por bloco (matriz de "monofonia teatral"): intro com 6 solistas simultâneos e a marcha
  com 9; dos blocos 73–144 ao outro, a matriz marcava **0** solistas — o motor melódico parou nos blocos
  centrais do arranjo.

## 3. Ar por bloco (medido no export) — 5–12 kHz vs faixa cheia

| bloco | AR (5–12k) | cheio | AR−cheio | ar vazio? |
|---|---|---|---|---|
| intro | 17,1 | 37,2 | −20,1 | não |
| 9–32 | 12,0 | 46,3 | −34,3 | SIM |
| 33–48 | 24,4 | 50,9 | −26,5 | SIM |
| 49–56 | 17,1 | 50,0 | −32,8 | SIM |
| marcha 57–72 | 21,4 | 52,9 | −31,4 | SIM |
| 73–88 | 21,2 | 52,9 | −31,7 | SIM |
| 89–104 | 22,1 | 52,7 | −30,6 | SIM |
| falso break 105–120 | 19,5 | 48,8 | −29,2 | SIM |
| 121–144 | 22,7 | 54,7 | −32,0 | SIM |
| breakdown 145–168 | 18,2 | 51,0 | −32,7 | SIM |
| DROP 2 169–200 | 25,8 | 54,3 | −28,4 | SIM |
| outro 201–241 | 19,1 | 51,2 | −32,1 | SIM |

Leitura (INFERÊNCIA): 10 dos 12 blocos tinham o ar (5–12 kHz) 26–34 dB abaixo da faixa cheia — o arranjo
não tinha camada de ar própria; só a intro (com pad de abertura) escapava. Métrica replicável para arranjos
do gênero: quando AR−cheio cai abaixo de ~−25 dB num bloco, o bloco está sem camada de ar.


---

## DOSSIE-HOMOLOGADO-CERTIFICACAO-CANONICA-SET-REF.md

# Dossiê técnico homologado — obra de referência de 240 compassos (extended DJ cut, 128 BPM)

> Estudo do acervo psytech-lab, anonimizado. O original é o dossiê de homologação da obra do autor;
> a cerimônia de homologação e o nome da obra foram neutralizados. A técnica dos 4 pilares, o cronograma de
> timeline e o gate de masterização são o conteúdo de estudo — o molde técnico consolidado do projeto.
> Escolas de referência declaradas pela obra: AlpaKa MuziK, Zenon Records, KUNI SOUND, Ismail.M.

**Tonalidade:** **C# frígio canônico** (notas: C#, D, E, F#, G#, A, B)
**Assinatura de estilo:** Minimal Psytech Hipnótico / Dark Zenon / Bush Tech Australiano

---

## 1. Arquitetura acústica — os 4 pilares

```
┌─────────────────────────────────────────────────────────────────────────────────────────┐
│ 1. MOTOR DE GRAVES: Kick 150ms + Slingshot 1.75 (35% de Energia) + Sub Ground 34.6Hz    │
├─────────────────────────────────────────────────────────────────────────────────────────┤
│ 2. FRICÇÃO FRÍGIA: C# (Tônica 34.6Hz) ↔ D (2ª Menor 36.7Hz) + G# (5ª Imperial 51.9Hz)   │
├─────────────────────────────────────────────────────────────────────────────────────────┤
│ 3. ESPAÇO 3D & PLANO Z: Mono Rígido <120Hz (Corr +1.0000) + Órbita 360° em Agudos (>6kHz)│
├─────────────────────────────────────────────────────────────────────────────────────────┤
│ 4. SUB DEPRIVATION: Vácuos de 2 Tempos + Exhaust Downer Estéreo (Width 140%)            │
└─────────────────────────────────────────────────────────────────────────────────────────┘
```

### 🥁 PILAR 1: o motor de graves e a gangorra slingshot 1.75
- **O kick "vapt-vupt" (decay 150 ms):** o bumbo atinge o pico em 48,0 Hz (C#1) e desliga em curva V aos
  **150,0 ms**. O envelope ultracurto abre uma **janela de silêncio absoluto de ~90 ms** antes do ataque do
  baixo, eliminando qualquer colisão de fase ou lama de sub-grave no PA.
- **A gangorra slingshot 1.75** — distribuição de energia em 4 semicolcheias, conforme as medições de
  laboratório do gênero:
  - **Beat 1.00 (head):** `Velocity 0` no baixo (mudo para liberar o transiente de ataque do kick);
  - **Beat 1.25 (ghost):** `Velocity 65–75` (toque sutil para o cone do alto-falante recuar);
  - **Beat 1.50 (offbeat):** `Velocity 80–90` (contratempo suave e contido, ~15% de energia);
  - **Beat 1.75 (slingshot):** **`Velocity 122–124`** (ataque de massa máxima concentrando 30–37% da energia
    de grave), a mola propulsora que arremessa o ouvinte para o tempo seguinte.
- **Sub ground monolítico:** ancoragem contínua em C#1 (34,65 Hz) em onda senoidal pura saturada, com
  *Phase Retrigger* travado em **0° lock**.

### 🎻 PILAR 2: a fricção modal C# frígio
- **Atrito em vez de escalas:** a tensão dramática é regida estritamente pela disputa entre a tônica
  **C# (I / 34,65 Hz)** e a segunda menor frígia **D (bII / 36,70 Hz)**.
- **Instrumentos solistas ancestrais:**
  - **Kamancheh:** glissandos de crina de cavalo no semitom (D4→C#4) com *Glide* de 45 ms e notch
    anti-nasal em 740 Hz (−3,5 dB) — no lugar do violino ocidental clássico;
  - **Flauta duduk:** sopro de madeira contemplativo com melismas frígios e LPF em 5,38 kHz, mantendo a
    sonoridade mística sem invadir a faixa de brilho dos pratos;
  - **Kanun & oud 3D:** rajadas sincopadas em 32nd notes no flanco direito (**35R**), com a nota E4
    (terça menor) substituindo qualquer terça maior indevida;
  - **Dark brass & braam:** uníssono imperial em C#2+G#2+C#3 nas aberturas e sinais de guerra pré-drop,
    com HPF em 90 Hz.

### 🌌 PILAR 3: imagem estéreo, centro de concreto & plano Z
- **Centro de concreto (<120 Hz):** correlação de fase estritamente cravada em **+1.0000 (mono puro)**
  abaixo de 120 Hz. Zero energia dissipada nas laterais do subwoofer.
- **Abertura de ar (>6 kHz):** condução de hats e shakers operando a **−32,0 a −27,0 dBFS**, presença
  cristalina e limpa sem fadiga auditiva.
- **Bush swing (track delay):** shakers e percussões de madeira operam com **+13,5 a +18,0 ms de atraso
  positivo**, gerando o "puxão de quadril" elástico fora da grade rígida.
- **Profundidade Z:** o retorno de reverb (3,09 s) aplica *self-ducking orquestral*: o som direto bate seco
  na frente (0–1 m) e a cauda do reverb expande nos vácuos de silêncio, projetando o horizonte acústico a
  ~20 metros de distância.

### 💥 PILAR 4: transições subtrativas & sub deprivation
- **Zero clichês EDM:** ausência total de *white noise risers*, *snare rolls* ou subidas comerciais.
- **Sub deprivation (despressurização de 2 tempos):** nos compassos pré-drop (bars 28, 44, 56, 88, 120, 144
  e 168), o bumbo é silenciado e o baixo sofre corte de passa-altas saltando de 32 Hz para **350 Hz**.
- **O vácuo do beat 4.4:** silêncio absoluto nos últimos 234 ms pré-drop, com a puxada de um reverse snare
  16th.
- **Exhaust downer no downbeat 1.0:** no momento do impacto dos drops (bars 57 e 169), dispara-se um ruído
  pneumático estéreo com HPF em **220 Hz** e *Utility Width* em **140%**, fazendo o espaço acústico explodir
  nas laterais enquanto o bumbo e o sub esmagam o centro mono.

---

## 2. Cronograma de impacto da timeline (240 compassos)

| Bloco | Compassos | Narrativa rítmica, espacial e dinâmica |
|---|---|---|
| **INTRO TEMPLO** | Bars 1–32 (0:00–1:00) | • Bars 1–8: invocação do kamancheh (D4→C#4) + bronze lur no fundo · • Bars 9–16: wood clicks em G#4 (+13,5 ms swing) + cello pedal em C#2 · • Bars 17–24: despertar do sub ground C#1 (34,6 Hz). Zero kick. · • Bars 25–32: daf em rolo de argolas. Bar 28.4: sub deprivation |
| **APROXIMAÇÃO DE DROPS** | Bars 33–48 (1:00–1:30) | • SUPER VÁCUO (15 s sem kick/sub). Solo de duduk e aulos fatiado pelo grain delay. Suspensão no estilo Gazolla no bar 44 (4 tempos de silêncio) |
| **DROP 1 & MARCHAS** | Bars 49–64 (1:30–2:00) | • DROP 1 (bar 49): kick slingshot + sub ground 40 Hz + exhaust downer · • Bar 56.4: carnyx urra na 4ª semicolcheia preparando a marcha |
| **MARCHA HIPNÓTICA** | Bars 65–104 (2:00–3:15) | • Duelo de barks: low bark (10L / '1','2e') vs resposta rasgada (35R) · • Acid 303 modular rasga cutoff (600 Hz→2,5 kHz) com legato slide |
| **FALSO BREAK EM 2 ATOS** | Bars 105–120 (3:15–3:45) | • Ato 1 (105–112): flutuação sem kick; kamancheh abre os portões · • Ato 2 (113–120): kick meio-tempo cardíaco; acid 303 acelera para 3,5 kHz |
| **DROP 03:45 & DESCIDA** | Bars 121–144 (3:45–4:30) | • Breakbeat e retorno de tração: trombetas frontais no bar 121 · • Bars 141–144: arquitetura de descida subtrativa (escurecimento) |
| **GRANDE BREAKDOWN** | Bars 145–168 (4:30–5:15) | • 24 compassos sem graves. Solo soberano de duduk → cello → tutti orquestral em rampa LPF (1,2k→8,5 kHz). BAR 168.3-4: VÁCUO BRUTAL |
| **DROP 2 "PAU TORA"** | Bars 169–192 (5:15–6:00) | • BEAT 169.1.1: CLÍMAX MONUMENTAL. Kick punch + sub ground · • Dark brass braam + bronze lur + double kicks nos turnarounds |
| **OUTRO DJ** | Bars 193–240 (6:00–7:30) | • Descompressão subtrativa progressiva para saída limpa em 3 decks, afunilando em volume e filtro LPF até o silêncio final |

---

## 3. Gate de masterização e checklist de homologação

Para a exportação do render final em **48 kHz / 24-bit PCM WAV**:

1. [x] **True Peak & teto de streaming:** true peak cravado em **≤ −0,5 dBFS** (medido **−0,71 dBFS** no
       master limiter com lookahead de 1,5–3,0 ms e true peak ON).
2. [x] **Loudness & dinâmica:** loudness integrada nos blocos de drop cravada em **−9,6 LUFS-I / −8,0 RMS**,
       preservando o crest factor em **10,5–11,3 dB** para o soco frontal sem esmagar transientes.
3. [x] **Rigidez monofônica de baixa frequência:** correlação de fase estrita abaixo de 120 Hz em
       **+1.0000 mono puro**.
4. [x] **Higiene de médios (mid-range pocket):** região de 400 Hz a 2,5 kHz mantida em depressão suave
       relativa ao RMS, garantindo a ilusão de bateria pesada e espaço negativo.
5. [x] **Integridade da timeline:** zero clipes com notas perdidas, zero mutes involuntários em canais
       ativos e 100% de conformidade modal em C# frígio.


---

## FOX-PSY-DIFERENCAS-ATUAIS.md

# Fox × projeto de referência — diferenças e correções da escuta (07/09/2026)

> Estudo do acervo psytech-lab, anonimizado. Referência externa: **Fox (Artemis AR Remix)**. O lado pessoal
> do original (quem acompanhou, decisões de captura canceladas) foi neutralizado; a técnica fica.

| Elemento | Evidência | Correção aplicada | Limite / próximo teste |
|---|---|---|---|
| Stabs | EQ Eight passava ~137–345 Hz, cortes de 48 dB/oitava. | Corte superior aberto para 2,80 kHz. | A/B: faixa de ataque ganhou ~18,7 dB relativo ao corpo; mudança perceptível confirmada por escuta. Não é medição de qualidade. |
| Kick: ataque | Drum Buss Damping 971 Hz. | Damping 3,99 kHz. | A/B: grave 30–120 Hz praticamente igual; ataque 1,5–6 kHz +12,46 dB relativo, pico menor. |
| Kick: corpo | Cru desce de ~178 a 50 Hz; capturado ~128 a 61,5 Hz. Não há oitava dobrada. Nota MIDI .24 beat, release ~50 ms. | Teste .36 beat nos clips 192 e 208; boom preservado. | Hipótese: o gate curto corta parte da cauda grave. Escuta atual, sem nova gravação. |
| Subgrave | Três notas por beat; ouvido como acelerado. | 47 clips passaram a notas em .5 do beat, duração .30 e velocidades 87/90; pausas anteriores preservadas. | Contratempo é decisão candidata para o projeto, não transcrição exata do stem Fox. |
| Hats | Sustain integral, decay 600 ms nos dois Simplers; rejeitados por escuta. | Aberto decay 120/release 20 ms; fechado 55/12 ms; sustain −inf em ambos. | Mudança de envelope; os samples continuam os mesmos. A escuta decide se trocar timbre. |
| Atmosfera | Grupo desligado e relatado "menos melodia". | Atmosferas permanece mutado. | Não reativar automaticamente; o projeto conserva o material até decidir a remoção. |
| Frase curta | Clip em 416 usa sequência 61/64/68/71/73, notas ~.28–.34 beat. | Teste com duas notas 61/64 e duração .14 no clip 416. | Teste local; demais frases ainda podem soar melódicas. |
| Retorno | Kick ausente em 387 na leitura anterior. | Kick 387 inserido, 16 notas em 384–400. | Nova leitura com 16 notas é resultado da correção; não erro do relatório anterior. |
| Construção | Riser terminava 336, drop 384; hats 4 notas por 16 beats. | Riser 374–382; hat fechado 352 = 8 notas, 368 = 18 notas. | Pausa final preservada; posições serão remapeadas no molde Fox. |

## Estrutura

Grade candidata da referência (mapa reverso): **132 BPM**. Intro 1–16; drop 1 17–72; preparação 73–80;
break 81–112; drop 2 113–192; saída 193–216. No projeto anterior o segundo drop começava no compasso 97:
alterar apenas locators não atende ao pedido — clips e automações precisam mudar juntos. Aplicação do molde
ainda pendente.

## Fontes e limitações (regras de método)

- Comparação kick/baixo e A/Bs (stabs, damping) documentados em arquivos de medição do projeto (stems Demucs
  e JSONs de A/B).
- Capturas existentes em `/tmp` são temporárias e anteriores a ajustes mais recentes.
- Fox drums/bass/other são **separações Demucs do edit de 3 min**, não os canais originais e não a timeline
  integral.
- **Não equiparar picos/níveis absolutos do MP3 masterizado aos sinais isolados pre-limiter do set.**

Principal ainda em desenvolvimento: avaliação integral, caudas, mono e aplicação da estrutura pendentes.
Não há variantes concluídas.


---

## FOX-PSY-V3-MAPA.md

# Fox → projeto de referência: mapa de continuidade (07/09/2026)

> Estudo do acervo psytech-lab, anonimizado. O original trazia o inventário completo de 36 pistas/grupos do
> set (cadeias por pista, nomes de canal) e a infraestrutura de automação do autor — essa parte é
> estado/infra pessoal e foi removida. Ficam as referências Fox (externas), as medições, o mapa por função,
> o contrato de trabalho e as limitações metodológicas do uso de stems Demucs.

**DECISÃO registrada:** Fox (Artemis (AR) Remix) é a referência; manter o método de separação por elemento
para aprender de ouvido.

**VERIFICADO (leitura do Live):** 132 BPM, 36 pistas/grupos (30 pistas + 6 grupos) e 3 retornos; nenhuma
alteração no set nesta rodada. Inventário das cadeias no nível principal; parâmetros internos, automações e
presets não foram auditados.
**NÃO VERIFICADO:** correspondência auditiva, qualidade dos timbres, BPM/tom da referência e alinhamento do
edit à faixa integral. Nomes de clips indicam intenção; não provam resultado sonoro.

## 1. Referências Fox disponíveis (tabela de estudo)

| Arquivo | Duração medida | Uso |
|---|---:|---|
| `Fox (Artemis (AR) Remix).mp3` | 393,744 s | Referência integral: arco, densidade e balanço geral |
| `Fox (Artemis (AR) Remix) - Instrumental 3min ref.mp3` | 180,036 s | Apoio para ouvir instrumentação |
| `Fox - Bass oitava-acima ref.mp3` | 180,016 s | Apoio para perceber ritmo/notas; NÃO usar como régua de subgrave |
| `Fox (Artemis (AR) Remix) - Edit Drop Maior 3min.mp3` | 180,000 s | Edit curto: comparação de energia; não presumir timestamps da integral |
| `htdemucs/…/other.mp3` | 180,036 s | Restante extraído: synths, atmosfera e efeitos possivelmente misturados |
| `htdemucs/…/bass.mp3` | 180,036 s | Baixo extraído do edit: ritmo, duração e movimento |
| `htdemucs/…/drums.mp3` | 180,036 s | Bateria extraída do edit: groove e ataques |
| `htdemucs/…/vocals.mp3` | 180,036 s | Vozes/resíduos extraídos; presença do arquivo não exige adicionar vocal |

Medição (ffmpeg volumedetect; **não é LUFS**): média no arquivo inteiro −8,7 dB na integral, −15,8 dB em
bass, −12,9 dB em drums, −18,6 dB em other e −30,3 dB em vocals. **Não comparar esses números diretamente
com o volume das pistas do set.** Métricas antigas em trechos não substituem esta medição integral.

## 2. Limitações dos stems Demucs (regra de leitura)

- Os quatro stems são **separações do edit de 3 min**, não pistas originais de produção, e não a timeline
  integral.
- **Não há kick, hat e clap isolados** nesses quatro arquivos.
- O bass "oitava acima" é uma referência **alterada** — nunca régua de sub.
- Samples de outros packs na mesma pasta não são elementos de Fox.
- **Não equiparar picos/níveis absolutos do MP3 masterizado aos sinais isolados pre-limiter do set.**

## 3. Mapa por função — onde ouvir e onde trabalhar

As correspondências abaixo são **INFERÊNCIAS funcionais** pelos stems. A coluna de escuta define perguntas,
não defeitos já diagnosticados.

| Elemento em linguagem simples | Referência Fox | O que comparar / intervenção mínima possível |
|---|---|---|
| Kick / bumbo: batida que dá o impacto | drums + integral | Ataque e duração; avaliar Simpler/Drum Buss existentes antes de trocar instrumento |
| Hi-hat aberto: abertura entre batidas | drums | Cauda e espaço; envelope do Simpler e EQ existentes |
| Hi-hat fechado: pequenos impulsos do groove | drums | Pausas e intensidade; distinguir ritmo de problema de timbre |
| Clap / palma e percussão: balanço | drums | Resposta ao kick; Simpler no clap e áudio já pronto na percussão |
| Ride / prato: brilho sustentado | drums | Entrada e duração; Drum Rack 909 existente |
| Subgrave: peso mais profundo | bass + integral | Relação com kick e cauda; Serum 2, filtro e Utility existentes |
| Baixo médio: parte do baixo que "fala" | bass; other como apoio | Movimento e presença; Serum 2, filtro, EQ, Saturator e Chorus existentes |
| Acordes curtos: ataques de synth | other + integral | Timbre, pausa e resposta; cada variante já pode receber tratamento próprio |
| Melodias e respostas: conversa entre synths | other + integral | Escolher uma voz por vez; não preencher todas as pistas com novos VSTs |
| Atmosfera: som de fundo sustentado | other + integral | Profundidade e espaço; áudio com Serum 2 FX e filtro — não falta instrumento gerador |
| Transições e cortes: anunciam ou interrompem a volta | other, drums e integral | Contraste na entrada/saída; distinguir efeitos em áudio de notas do Serum |
| Voz | vocals + integral | Adicionar só se houver intenção musical e necessidade auditiva |

## 4. Forma de trabalho preservada (contrato por rodada)

O produtor define intenção e aprova pelo ouvido → escolhe-se uma pergunta → coleta só os fatos ausentes →
1–2 análises apenas quando existir decisão material → um executor escreve no Live → leitura real confirma →
áudio A/B → manter ou desfazer.

Contrato por rodada: **TARGET / REGION / CHANGE / DO-NOT-CHANGE / ACCEPTANCE**. Uma hipótese e uma mudança
material. Nomes claros, variantes em linhas próprias e subgrupos. Não adicionar camadas ou trocar VSTs em
massa. **Não copiar melodia, hook ou composição da referência.**

## 5. Próxima rodada concreta (método do caso)

1. Comparar **other + integral de Fox** com um canal de stabs já separado (região existente de 4 compassos,
   beats 192–208). É um candidato curto por já estar separado e usar Serum; não é diagnóstico de que seja o
   maior defeito.
2. Ouvir e identificar UMA diferença material (por exemplo duração ou movimento), em volume percebido
   comparável. Localizar um trecho correspondente em Fox por função musical; não alinhar automaticamente os
   tempos do edit e da integral.
3. Só então escolher um parâmetro/efeito ou mudança de preset que teste essa diferença. Priorizar controle já
   disponível se suficiente; se exigir interior do Serum, validar a ligação real do host nesse elemento antes
   de substituir a instância atual.
4. Guardar A/B curto, confirmar estado final e obter decisão estética do produtor. A seleção definitiva da
   intervenção depende da escuta — métricas e consenso de agentes não aprovam música.

## 6. Evidência e limites

- Snapshot do Live (pistas, grupos, cadeias e posições) e inventário dos oito arquivos de referência
  (duração, canais, sample rate, volume integral) registrados no projeto.
- Nenhuma audição simulada: esta rodada entrega mapeamento operacional, não análise estética concluída.
- Nenhuma mutação no Ableton, preset, áudio ou configuração global nesta rodada.


---

## MAPA-GRUPOS-ARTISTAS-x-SET-REF-20261030.md

# Mapa por grupo — artistas dissecados × set de referência (30/10/2026)

> Estudo do acervo psytech-lab, anonimizado. Fonte dos artistas: compilação (somente leitura) sobre as
> dissecações de Scionaugh, PML, MERAKKI, Dowden, KUNI, urklang, Vision Serpent, Tom Cosm e Sadowick.
> **Todos os números dos artistas vêm de legenda/fala dos vídeos, não de áudio medido.** A coluna do set foi
> lida no Live, com faders e cadeias.

| Grupo | Artistas (faixa · corte · nível) | Set de referência (medido) | Leitura |
|---|---|---|---|
| KICK+SUB | 20–200 Hz, 100% mono até ~178 Hz; kick = 0 dB de referência (KUNI). Scionaugh: sub **+5,1 dB acima** do punch | kick −6 dB, grupo −2 dB; sub 20–60 = 24% e 60–120 = 55% (pico em 69 Hz) | Invertido: o punch está muito acima do sub |
| SUBS | Fundamental em **uma camada só** (urklang, Tom Cosm); senoide ~50 Hz; sem reverb e sem width abaixo de 120 Hz | SUB único (34,6 Hz) a −8 dB; sub extra mudo | Agora bate com a regra |
| BAIXO | Corpo 210–1.000 Hz; mono abaixo de 150–178 Hz; LP de 12–24 dB | C#1 a 69 Hz; LP 1,2 kHz; corte de 69 Hz em −6 dB | O fundamental do baixo disputa com o sub |
| TOPO E HATS | Hats **≈ −18 dB** do kick (KUNI); HP 150; hat sobre o click do kick | HAT −7,3 dB | ~10 dB mais alto que a régua KUNI |
| PERCUSSÃO | Shaker abaixo do hat, "quase inaudível"; HP 100–160 | OPEN MALANDRO −9,5 · PERC SYNTH −14 | Sem número nos artistas |
| MADEIRAS | Corpo **300–1.200 Hz**; HP 150–300; "bem baixo" | −8 a −10,8 dB, sem HP sistemático | Faltam os HP |
| MEIO atmos | Pad 300–4k; reverb com HP 300–500 / LP 5–6k, wet 10–15% | pad C#3 sustentado, −12,2 dB | Falta conferir os HP e o reverb |
| MEIO pluck | Clique ~600 Hz; HP ≥250; par wide+mono | FM pluck C#5, HP 280, −12 dB | Já bate na faixa |
| SYNTHS | Stabs/mid-bass **−5 a −8 dB** do kick (KUNI); uníssono ímpar | STAB 0 dB · TICKLER −1,5 dB | ~5 dB mais alto que a régua KUNI |
| ORQUESTRA | NÃO ENCONTRADO | HORN −9 · CORNETA −8 | Sem régua de artista |
| IMPACTOS/FX | Camada própria, "shave the bottom" | SUB IMPACT −14,7 dB | Sem número |
| REVERSE/GLITCH | O volume para na fronteira da seção | — | Sem número |
| Master | Scionaugh: 10 dB de headroom, picos pré-limiter ≈ −4 dBFS, ~2 dB GR | true peak −0,7 dBTP | Sem headroom |

**Convergências entre artistas:** grave mono, fundamental numa camada só, largura só acima de 150–210 Hz,
corpo em 300–1.200 Hz.
**Lacunas:** orquestra, fader por grupo (só a KUNI dá números) e LUFS.


---

## PSY-V3-MAPA-ATUAL.md

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


---

## RAIO-X-360-SET-REF-20260924.md

# Raio-X 360 de um set de referência (24/09/2026)

> Estudo do acervo psytech-lab, anonimizado. O original (grande) trazia fader por canal (51 pistas), clipe a
> clipe por bloco e a auditoria completa de nomes do set — essa parte é estado puro e foi condensada. Ficam:
> o método, a hierarquia de mix por família, a dinâmica de velocity por bloco, o perfil tonal por bloco, a
> régua de referências do detector de firmeza do kick e as lições de auditoria de nomes.

Fontes: `.als` salvo (693 clipes de arranjo, 57 pistas) + export do projeto (8:00, 48k/24-bit).
Método de áudio: ffmpeg → mono 48k → FFT Hann; bandas LOW 20–120 · CORPO 120–500 · SINF 500–2500 ·
PRES 2500–5000 · AR 5–12k. Marcas: VERIFICADO (medido), INFERÊNCIA, HIPÓTESE, NÃO VERIFICADO.

## 1. Faders — hierarquia de mix medida (linear→dB, VERIFICADO no .als)

Faixas por papel (o original lista canal a canal):

| papel | fader (dB) | observação |
|---|---|---|
| kicks (3 variantes ativas + testes mortos) | −2,8 a +6,0 | kick principal como referência |
| open hat / shaker / closed hat | −5,7 / −5,7 / −4,0 | topo percussivo |
| trigger sidechain | −70,0 | canal de gatilho, fora do mix |
| subs (ground + rolling) | −2,0 / +1,6 | sub rolling acima do ground |
| solistas sinfônicos (trombeta, cello, kamancheh, kanun, flauta) | −6,4 a −11,4 | núcleo melódico |
| pad sinfônico / voz de garganta / acid / braam | −13,2 a −16,0 | apoio e acento |
| madeiras (3 canais) | −13,9 a −18,9 | percussiva |
| glitches (8 canais) | −15,0 a −18,9 | textura |
| pads/ambient/drone/forest | −13,8 a −28,8 | fundo em degradê |
| vozes processed (4 canais) | −22,0 a −28,8 | fundo |
| FX/impactos/transições (12 canais) | −14,0 a −20,0 | acentos |

## 2. Velocity do kick por bloco (a dependência que mais muda o bloco)

| bloco (beats) | compassos | notas | velocity média | notas/beat |
|---|---|---|---|---|
| 128–160 | 33–40 | 66 | 99,1 | 2,06 |
| 192–222 | 49–56 | 62 | 58,5 | 2,03 |
| 224–254 | 57–64 | 61 | 56,7 | 2,00 |
| 256–286 | 65–72 | 61 | 45,7 | 2,03 |
| 288–352 | 73–88 | 59 | 110,7 | 0,92 |
| 352–384 | 89–96 | 29 | 112,4 | 0,91 |
| 384–432 | 97–108 | 45 | 107,9 | 0,94 |
| 480–512 | 121–128 | 29 | 112,6 | 0,91 |
| 512–574 | 129–144 | 61 | 82,0 | 0,98 |
| 672–736 | 169–184 | 59 | 122,9 | 0,92 |
| 736–800 | 185–200 | 59 | 122,9 | 0,92 |
| 800–864 | 201–216 | 59 | 122,9 | 0,92 |

Leitura: a velocity média do kick é o knob narrativo do arranjo — queda (45–58) na abertura da marcha,
sobe (108–113) na tensão, teto (122,9) no clímax. Métrica replicável: velocity média por clipe × bloco.

## 3. Clipes por bloco (condensado nesta versão)

O original lista clipe a clipe (notas, n/beat, velocity, pitch) para 10 blocos. Achados que sobrevivem:

- Clipes de "hold antigo" com densidade absurda (**9.182 notas/beat**) — lixo detectável pela métrica n/beat.
- Canal de trigger sidechain com velocity fixa **127** em todo o arranjo (gatilho constante por desenho).
- Registros dos subs em C#2/C#3 (69/139 Hz) e o descer para C#1 (35 Hz) só no clímax.
- Madeiras/pérc com padrão de resposta (clips curtos de 1–5 notas) entre os blocos de kick.

## 4. Bandas por bloco (VERIFICADO no export)

| bloco | LOW | CORPO | SINF | PRES | AR | CORPO−LOW | pico LOW |
|---|---|---|---|---|---|---|---|
| intro 1-8 | 36,8 | 47,5 | 35,1 | 14,1 | −8,5 | 10,7 | 104,1 Hz |
| 9-32 | 40,4 | 60,7 | 50,8 | 29,8 | 12,0 | 20,3 | 104,1 Hz |
| 33-48 | 73,7 | 60,2 | 48,0 | 39,1 | 23,5 | −13,5 | 68,4 Hz |
| 49-56 | 72,7 | 59,3 | 42,0 | 28,9 | 16,4 | −13,4 | 51,2 Hz |
| marcha 57-104 | 79,7 | 67,1 | 52,8 | 41,0 | 26,2 | −12,6 | 51,2 Hz |
| falso break 105-120 | 70,6 | 56,4 | 51,3 | 38,1 | 17,4 | −14,2 | 51,2 Hz |
| 121-144 | 75,3 | 63,6 | 54,9 | 35,9 | 23,2 | −11,7 | 51,2 Hz |
| breakdown 145-168 | 37,5 | 55,0 | 59,4 | 40,3 | 18,8 | 17,5 | 104,1 Hz |
| DROP 2 169-200 | 75,6 | 64,2 | 56,7 | 45,1 | 26,5 | −11,4 | 51,2 Hz |
| outro 201-241 | 74,0 | 61,6 | 49,3 | 33,9 | 18,7 | −12,5 | 51,2 Hz |

Leitura (INFERÊNCIA): nos blocos com kick o pico de LOW cai para a tônica do kick (51,2 Hz) e CORPO fica
11–14 dB ABAIXO de LOW (hierarquia grave-cêntrica); na intro e no breakdown (sem kick) o pico de LOW sobe
para 104 Hz e CORPO vira +10 a +17 dB ACIMA — o arranjo troca a hierarquia grave↔corpo entre seções com e
sem bateria.

## 5. Firmeza do primeiro kick por corte (VERIFICADO, mesmo detector)

No set: Δ entre o primeiro kick e a mediana dos kicks do corte oscilou de **−4,5 a +2,3 dB** (sem padrão de
"primeiro mais firme") e o rise do primeiro variou **34–199 ms** contra 65–76 ms típicos — nas fronteiras o
kick de entrada não era nem mais firme nem mais rápido de forma consistente.

### Referências (mesmo detector) — RÉGUA EXTERNA

| faixa | cortes | primeiro−mediana | primeiro mais firme | rise típico | rise 1º |
|---|---|---|---|---|---|
| ISMAIL.M Ortahisar | 10 | +0,03 dB | 6/10 | 79 ms | 71 ms |
| Kaled Bush | 11 | +0,24 dB | 8/11 | 80 ms | 41 ms |
| DN Lost Dinasty | 18 | −0,04 dB | 8/18 | 72 ms | 71 ms |
| DN Quartzo | 12 | +0,09 dB | 9/12 | 71 ms | 68 ms |
| DN Tiger Eyes | 8 | −0,14 dB | 3/8 | 70 ms | 65 ms |
| Gazolla Oziris | 10 | −0,01 dB | 4/10 | 64 ms | 46 ms |
| Akari Slippery | 8 | +0,65 dB | 6/8 | 54 ms | 68 ms |

Nas referências o primeiro kick do corte é essencialmente igual à mediana (Δ ≈ 0) — firmeza de entrada não é
o recurso narrativo do gênero; o rise típico fica em 64–80 ms.

## 6. Auditoria de nomes (lição de gate)

- **121 apontamentos** no set: clips cujo nome promete "(Bars A-B)" divergente da posição real (ex.: nome
  "Drop 2 (Bars 169-184)" tocando em 185–200) e devices com Hz no nome divergentes do valor real.
- Lição geral: **o nome do clipe/device mente** — auditar posição e parâmetro reais; renomear pela posição
  medida, nunca o contrário.
- Correções de renome aplicadas no caso: canal de sub renomeado pelo registro real (notas movidas de C#3
  para C#1 → nome atualizado), kick renomeado pelo corte real (boom em 0% → nome atualizado), Auto Filters
  renomeados pela média de corte real (164 Hz e 182 Hz → 100 Hz).


---

## RASTREIO-SERUM-PRESET-DIRETO-20260915.md

# Rastreio — aplicar preset no Serum 2 direto (frente "preset direto")

> Estudo operacional do acervo psytech-lab, anonimizado (data original: 15–16/09/2026, Live 12.4.5/12.4.6,
> Serum 2 VST3 + AU). Objetivo: trocar/carregar preset nas instâncias de Serum **sem clique humano**, com
> rastreio de evidência. Nomes de pistas/patches do set de referência foram anonimizados; nomes de presets
> de fábrica do Serum foram mantidos porque são referência externa.

## 1. O que era verdade no começo (estado herdado)

| Fato | Evidência |
|---|---|
| Geração de `.SerumPreset` e leitura do patch de cada canal já existiam | inventário de patches por canal (arquivo do projeto) |
| `Device.parameters` de cada Serum = **1** ("Device On") | medido em 24 devices, código dentro do Live (15/09) |
| Escrever estado de plug-in no `.als` → crash do Live | log de crash do sistema: thread principal dentro de `Serum2.vst3` |
| Browser interno do Serum carrega preset (busca + duplo clique) | funcionou 1×; abrir a janela por coordenada falhou depois |

## 2. Medições desta rodada

### 2.1 LOM nativo (hipótese "PluginDevice.presets") → REFUTADO
- `Device.presets` existe (StringVector) e `selected_preset_index` existe (int, com listener).
- **Medido nas 24 instâncias** (VST3 `PluginDevice` e AU `AuPluginDevice`, instrumentos e FX):
  `presets = ["Default"]` (1 entrada; IndexError no índice 1), `selected_preset_index = 0`.
- Leitura: o Serum **não publica** a lista de presets para o host → trocar por índice via LOM não tem para
  onde ir. Consequência: `selected_preset_index` não serve como fundação.

### 2.2 Estado de plug-in por arquivo (`.adv` / `.aupreset`) → RECEITA VALIDADA OFFLINE, sem teste no Live
- Formato do estado: `XferJson\0` + (len,flags) + JSON meta + (len,flags=2) + zstd → CBOR.
- **Achado que explica o crash**: o AU **descarta em silêncio** estado em que `processor` e `controller` usam
  o MESMO corpo (o corpo do `.SerumPreset`). Ele aceita e aplica quando:
  - `processor` = estado COMPLETO (162 chaves) com os valores do patch sobrescritos;
  - `controller` = corpo de controller (~59 chaves) com `presetName/presetAuthor/presetDescription/selectedPresetPath` do alvo;
  - o blob `data` é **regerado pelo próprio plug-in** (sem risco de dado velho).
- Verificação offline (instanciando o AU fora do Live, round-trip de `kAudioUnitProperty_ClassInfo`):
  estado devolvido = alvo; **som mudou** (default −18,8 dBFS/4334 Hz · patch antigo −30,1/3194 · artefato
  −37,1/2108; correlação ≤0,21).
- **NÃO VERIFICADO**: carregar esses artefatos DENTRO do Live (o teste exige set descartável e aceitar o
  risco de crash).
- Observação: o Live **não registra** `.aupreset` no `Info.plist`; e não há `.adv` de plug-in na máquina
  (o molde foi construído a partir do `PluginDevice` do próprio `.als`).

### 2.3 Program Change (VST3) por clip MIDI → CAMINHO MAIS PROMISSOR
- Fontes (VERIFICADO por leitura): Live 12.2+ suporta PC em VST3 (release notes oficiais); KB do Ableton
  sobre Bank/Sub-Bank/Program em clips (banco = CC0, sub-banco = CC32); **staff da Xfer confirma que o
  Serum 2 aceita PC** ("not documented in the manual"; Live adicionou suporte em 12.2).
- Local: todo `<MidiClip>` do `.als` tem `<BankSelectCoarse>/<BankSelectFine>/<ProgramChange>` (default −1)
  e o LOM **não** expõe esses campos → edição offline, cirúrgica.
- **⚠️ Armadilha de teste:** set descartável só salva se for **pasta de projeto completa** (`Samples/` +
  `Ableton Project Info/`) — cópia solta fora de pasta de projeto é recusada pelo save; e o transporte via
  API pode entrar em stall na cópia.

### 2.4 Preferência do próprio Serum (`Enable CCForRockers`) → plano B, exige backup
- Manual instalado do Serum 2, Apêndice D: `Enable CCForRockers: 1` (CC) ou `2` (notas) +
  `CCForRocker Preset +/-`; setas ‹ › navegam a pasta atual; ↑/↓ no browser.
- `Serum2Prefs.json` existe com essas chaves; risco: é **global** (todos os projetos), passo relativo (±1) e
  histórico de "preset skips" ao tocar nota. Só com backup do prefs.

## 3. Conclusão (parecer da época)

1. **LOM nativo está fechado** pelo próprio plug-in: medido em 24/24 instâncias. Não insistir.
2. **Cirurgia de estado no `.als` continua proibida** (crash documentado). A receita coerente existe e
   funciona fora do Live, mas o carregamento dentro do Live **não foi testado**.
3. **O caminho mais barato e correto é o Program Change por clip MIDI** (menor mecanismo que resolve, nativo
   do Live, sem infra nova). Falta o teste com set descartável — e o resultado já é útil musicalmente
   (troca de patch dentro do arranjo).
4. **Fallback documentado**: `.adv` coerente → carga nativa pelo Live; e por último automação da janela do
   Serum (1× provado, frágil) — nunca como arquitetura.
5. Para poucos canais com patch fora de papel: os 2 cliques continuam sendo o caminho mais rápido; a
   automação é para escala.

## 4. Regras que ficam (lições de método)

- **Nativo primeiro**: testar o que já existe no Live/LOM antes de construir ponte.
- **Menor mecanismo correto**: só criar registry/PC/loader quando houver lacuna comprovada.
- **Nada de state surgery no `.als`/VST3** (risco alto, evidência de crash).
- **Set descartável só vale se for pasta de projeto completa** (`Samples/` + `Ableton Project Info/`) —
  cópia solta não salva.
- **Set auto-contido**: `File > Collect All and Save` + gate de mídia (todas as referências dentro da pasta).
- Evidência crua sempre: caminho + medição + comando.

## 5. Teste P1 (Program Change) — primeira rodada: NÃO CONCLUÍDO (armadilha de verificação nomeada)

1. Grade de sondagem offline: 6 pistas, bancos 0/1 × programas 0..2 — edição verificada (6 clips alterados,
   404 intactos, audit ok).
2. Playback cruzou **todos os 6 clips** — confirmado pelo playhead.
3. Save da cópia ok (pasta de projeto completa).
4. **Read-back: patches IGUAIS ao baseline nos 6 canais.**

**Por que isso NÃO fecha o veredito:** o read-back depende do estado que o Live grava no `.als`, e já havia
sido medido que **o Live salva o estado em cache do plug-in sem consultá-lo** (teste de sentinela). Se a
troca aconteceu *dentro* do Serum, o save pode persistir o estado antigo → **falso negativo possível**.

**Tentativa de read-back independente (áudio A/B):** captura de 8 s de uma pista em solo na cópia = OK; a
captura equivalente no set de trabalho **falhou** (diálogo de save bloqueando a troca de documento e o
`start_playing` pela LOM não engatando de forma consistente). Sem o "antes", o A/B não fecha.

**Receita para fechar (determinística):** (a) criar um clip de SESSÃO com 3-4 notas numa pista de Serum via
LOM, salvar; (b) fechar e editar o `.als` para pôr `BankSelectCoarse/Fine/ProgramChange` nesse clip de sessão
(o manual do Ableton é explícito: o PC sai **ao dar launch no clip** — mais determinístico que depender do
playhead cruzar clip de arranjo); (c) reabrir e dar launch; (d) verificar por áudio **e** por janela do Serum.

## 6. Cruzamento com pesquisa externa e o que muda

- Confirmação pelas fontes oficiais: o manual do Live autoriza Bank/Sub-Bank/Program para plug-ins (até 128³
  combinações); o Live 12.2 trouxe PC para VST3 (com correções em 12.2.5/12.3).
- **Nuance de verificação importante**: no Serum 2, **Module Locks sobrevivem à troca de preset** (manual
  oficial) → "preset X selecionado" não prova que o som inteiro é X; o read-back ideal é áudio e/ou janela do
  Serum, não só o nome.
- Fonte `github.com/Serum-2` descartada (aparência de SEO/repack); autoridade = `xferrecords.com`.
- **Melhoria real no fallback**: desde o **Live 12.4.3**, um device Max for Live consegue abrir/fechar a
  janela de editor do plug-in via LOM → o clique frágil por coordenada sai da equação.
- Repos de referência citados (não instalar ainda): gerador de `.SerumPreset` (não carrega), mapa CC,
  fork com "128 params curados", host VST em Max `vst~` (mudança arquitetural grande).

**Sequência final:** LOM nativo (❌ medido: lista vazia em 24/24) → P1 PC por clip de sessão (pendente) →
P2 `.adv` de estado coerente (receita validada offline) → P3 M4L abre editor + automação interna do Serum
(último recurso, mais barato desde o 12.4.3).

---

## 7. ATUALIZAÇÃO 16/09 — spike executado: PC **não** validado (negativo com read-back duplo)

Set descartável completo (cópia do set de referência + `Samples/` + `Ableton Project Info/`), Live **12.4.6**.
Ferramenta nova: injetor de `ProgramChange`/`BankSelectCoarse` por faixa, por bytes, com dry-run + validação
XML; `als_audit` ok nas duas sondas.

| Teste | Configuração | Resultado |
|---|---|---|
| A — clip de ARRANJO | PC=0/1/2 em 3 pistas de sonda (open hat / sub bass / motif), 44 clips alterados, playhead 20→262 | **nenhum preset mudou** |
| B — clip de SESSÃO (`ClipSlot.fire()`) | clips de sessão das 3 pistas patchados, disparados e tocando | **nenhum preset mudou** |
| C — banco + programa | `BankSelectCoarse=0` + PC 0/1/2 (43 clips) | **nenhum preset mudou** |

**Read-back duplo, dois métodos independentes concordando:** (i) leitura do `presetName` no `.als` salvo;
(ii) **janela do Serum aberta por código** (`Device.is_editor_open = True` — capacidade verificada) +
captura de tela → a pista-sonda mantinha o patch original.

**Outros fatos medidos:**
- `PluginDevice.presets = ["Default"]` nas **26** instâncias (re-confirmado).
- **O browser do Live não indexa `.SerumPreset`** → o hot-swap de preset do Serum pelo browser **não tem
  item para carregar**.
- O Live **detecta** o parâmetro de PC do Serum: `VST3: Found 1 program change parameters for plugin Serum 2`
  (26× no load).
- `Serum2Prefs.json`: `CCForRockers = 0`, todos os CCs em `-1`; **não existe switch de Program Change** nas
  preferências.
- **`open "<outro>.als"` troca o Set sem `Cmd+Q`** (com o doc limpo, sem prompt) — reload mais barato.
- O `.als` salvo guarda o `presetName` de cada Serum na meta do `ControllerState` → **read-back de preset por
  arquivo, sem UI**.

**Conclusão:** com **3 configurações e 0 mudanças** (e read-back duplo), a rota do Program Change **não
estava validada** — e a observação anterior ("PC=1 injetado num clip de sessão → Init Preset") **não se
reproduziu**. **Discriminador:** setar o PC **pela UI** (painel de propriedades do clip) na sonda e ver se o
preset muda — se mudar pela UI e não pelo XML, o problema é o campo/leitura do campo; se não mudar nem pela
UI, o Live não está entregando PC ao Serum na versão testada.

### 7.1 SPIKE S2 — **O PC FUNCIONA: era BANCO, não suporte**

Sonda com 3 pistas com clips de sessão patchados:

| pista | `BankSelectCoarse` | `ProgramChange` | resultado |
|---|---|---|---|
| sonda 1 | 15 | 0 | sem mudança |
| sonda 2 | 16 | 0 | sem mudança (**PC=0 = no-op**) |
| **sonda 3** | **16** | **1** | **MUDOU: patch original → `CH - Beach Club`** (preset de fábrica) |

Disparo = `ClipSlot.fire()` (o PC sai no **launch**; playhead cruzando clip de arranjo **não** dispara).
Leitura = `presetName` no `.als` salvo. A troca **foi persistida pelo save** (no arquivo).

**⚠️ CRASH — 2× no mesmo dia, assinatura IDÊNTICA:** logs de crash do sistema no instante da troca de set e
~20 s depois do save, transporte tocando: `EXC_BAD_ACCESS KERN_INVALID_ADDRESS` · **MainThread** · 5 frames
idênticos dentro do `Serum2` chamados de `__CFRunLoopDoTimer` → é o **timer do Serum na thread principal**.
**Correlação — HIPÓTESE (não provada):** burn de ~1 core e crash podem compartilhar um loop/timer interno;
o que está provado é só que **o timer que caiu é do Serum** (medição com `sample` mostrou os frames do
burn em outra faixa de endereços; discriminador: novo `sample` pós-upgrade × este baseline).
**Procedência dos binários (verificada com `codesign -dv`):** o **VST3 era `adhoc` / sem Team ID (build
modificado, não assinado pela Xfer)**; o **AU era genuíno** (`Developer ID: Steve Duda`). Os pacotes vinham
de distribuição não oficial e **os crashes + o burn estavam no VST3** → "bug da versão" concorre com "build
não oficial" como causa. Baseline limpo = instalar build **assinado pela Xfer** e repetir o gate.
**Mistura VST3 × AU (contagem lida do `.als`):** **19 VST3 + 7 AU** — o PC vale para os 19 VST3.

### 7.2 A REGRA DO PC FOI RESOLVIDA (16/09) — agora dá para escolher preset **POR NOME**

- **bank** = posição **1-based** da PASTA do preset na lista alfabética **case-sensitive** de todos os
  diretórios de `…/Serum 2 Presets/Presets`;
- **program** = índice **0-based** na lista do **`presets.db`** daquela location, em ordem de nome
  **case-insensitive**.
- **Validado no Live (10 pontos sem erro):** bancos 13–17 → `BA - Bubba`/`BL - Kinderjoy`/`BR - Brass Wall`/
  `CH - Beach Club`/`DR - Clap Machine` (presets de fábrica); e 4 presets de User/alvo do projeto validados
  no mesmo ciclo.
- **Ferramenta:** um mapa bank/PC por nome de preset, que imprime **fingerprint** a cada chamada (versão do
  Serum + hash/mtime do `presets.db` + hash/contagem da árvore de Presets).
- **Limites:** `ProgramChange=0` é **no-op** (preset no índice 0 não é selecionável assim); pastas privadas
  do projeto não resolvem → usar as cópias em `User/`.
- **Persistência pós-reload PROVADA:** sonda salva com presets trocados, **fechada, reaberta** e, ao forçar
  um save, os nomes continuavam os trocados ✓ (fecha o critério "save → fechar → reabrir").
- **A regra é do CORPUS ATUAL, não do Serum em abstrato:** a lista viva muda com a pasta; o fingerprint do db
  (neste ciclo: 659 KB, 72 locations / 2.162 presets; 91 dirs; 1.624 arquivos) faz parte da prova.
  **Recalcular sempre — o par (bank, PC) não é para memorizar.**
- **Consequência:** a varredura cega de bancos **morreu** — o par (bank, PC) de qualquer preset em
  `Factory/`/`User/` é **calculável**. O gargalo de "trocar preset sem clique" está fechado por cálculo.


---

## REGUA-DE-AUDIO-20261025.md

# Régua de áudio — set de referência × 15 referências da família (25/10/2026)

> Estudo do acervo psytech-lab, anonimizado. Método: medição em **taxa nativa e estéreo** via ffmpeg, sem
> reamostrar e sem somar em mono (regra de método do projeto: proibido medir topo (>8 kHz) ou estéreo após
> reamostrar para 22,050 kHz ou somar em mono). Mede: LUFS integrado e true peak (ebur128) e, na **janela de
> 60 s de maior RMS** (o clímax): 6 bandas de energia, side/mid total e side/mid do grave, crest.
> **Nada foi ouvido** — os números são objetivos; o julgamento estético é do produtor.
>
> **CORREÇÃO do baseline (25/10):** os números de "ar 0,5% / low-mid 13,7%" da seção 2 vêm de um render
> anterior (24/10, motor antes de uma revisão grande), na janela de maior RMS. O baseline novo do estado
> atual mede, no **Drop 1**, **air 1,0% · low-mid 23,9% · bass 22,6%** e, no **Drop 2**, **air 1,7% ·
> low-mid 30,5% · bass 15,5%**. O gap real do estado atual é **low-mid/bass**, não ar.

---

## 1. As 15 referências

Acervo de 15 faixas completas (> 150 s) da família: Slippery Slope (Luis M), Luis M, Desert Nomads,
Farhy/Orion/Kaled Nasser, Fox (Artemis), Gazolla/Petrix, ISMAIL.M, AlpaKa, Petrix, Rollfree, Lady Rave.

| Métrica (mediana) | Valor | Faixa (min–max) |
|---|---|---|
| LUFS integrado | **−8,7** | −11,7 a −6,9 |
| True peak | **+2,3 dBTP** | +0,6 a +6,3 |
| Crest | 11,1 dB | 9,2 a 15,7 |
| Sub (20–60 Hz) | **47,5%** | 13,5 a 59,0 |
| Bass (60–120 Hz) | **37,1%** | 22,8 a 52,7 |
| Low-mid (120–400) | 9,4% | 4,9 a 22,3 |
| Mid (400–1,5k) | 2,7% | 0,9 a 7,9 |
| Presence (1,5–6k) | 1,2% | 0,4 a 8,3 |
| **Air (6–16k)** | **1,6%** | 0,3 a 6,9 |
| Side/mid | −14,8 dB | −24,6 a −10,9 |
| Side/mid do grave (<120 Hz) | −32,7 dB | −48,6 a −12,9 |

`VERIFICADO`.
Observação de leitura: as referências estão **masterizadas e clipando** (+2,3 dBTP de mediana). Comparar
LUFS/TP com um render cru não mede qualidade de mix — mede estágio de masterização. As bandas e o estéreo
são a parte comparável.

---

## 2. O set de referência contra a família

Render completo (20:15), janela analisada 80–140 s.

| Métrica | Referências | Set | Delta |
|---|---|---|---|
| LUFS | −8,7 | **−10,9** | −2,2 LU mais baixo (esperado: não masterizado) |
| True peak | +2,3 dBTP | **−0,6** | −2,9 dB (headroom; elas clipam) |
| Crest | 11,1 | **10,5** | −0,6 (mesma família) |
| Sub | 47,5% | **43,6%** | −3,9 pp |
| Bass | 37,1% | **36,9%** | **−0,2 pp — idêntico** |
| Low-mid | 9,4% | **13,7%** | **+4,3 pp** |
| Mid | 2,7% | **3,7%** | +1,0 pp |
| Presence | 1,2% | **1,5%** | +0,3 pp |
| **Air** | 1,6% | **0,5%** | **−1,1 pp (≈3× menos)** |
| Side/mid | −14,8 | **−14,1** | +0,7 dB (levemente mais largo) |
| Side/mid grave | −32,7 | **−41,8** | −9,1 dB (grave mais mono) |

`VERIFICADO` nas medições; a leitura abaixo é `INFERÊNCIA`.

**O que estava certo:** o grave na régua (bass idêntico, sub 4 pp abaixo), o estéreo na régua (0,7 dB mais
largo), o grave **9 dB mais mono** que a mediana — o desejado quando o cânon é low-end mono — e o crest na
família.

**O que estava fora:** o set é **mais escuro e mais grosso**. +4,3 pp de 120–400 Hz e **3× menos ar
(6–16 kHz)**. Não é problema de topo de mix (presence 1,5% contra 1,2%) — é de **ar**: falta a camada de
8–16 kHz que as referências têm. Um A/B de high shelf que estava pendente reabre com número — e diz onde
agir: **acima de 6 kHz**, não em 1,5–6 kHz. (⚠️ ver a correção do baseline no topo: num render mais novo o
gap passou a ser low-mid/bass.)

---

## 3. As quatro escolas de sessão (medidas com a mesma ferramenta)

| | **Let You Go** | **Giants** | **Drift** | **Tim Engelhardt** | **Set de referência** |
|---|---|---|---|---|---|
| BPM | 125 | 122 | 122–132 | 123–124 | 128 |
| Pistas | 22 | 71 | 19–40 | 24–32 | **81** |
| Notas | 1.334 | 21.127 | 96–1.189 | 730–3.659 | **70.645** |
| Compassos | 209 | 220 | 124–188 | 192–208 | 241 |
| **FX por pista** | 2,7 | **5,1** | 2,9 | 2,8–3,5 | **5,07** |
| Returns | **1** | 5 | 2 | 3–4 | 2 |
| Sends ativos | 5 | **28** | 0–2 | 19–32 | 9 |
| Master | **só Utility −3,33 dB** | rack + EQ + Utility +8,33 + master chain | comp 0,01 ms + Clipper + **2 limiters** | EQ + **Glue paralelo 4,8–7,9%** + 1 limiter | EQ + Glue + Utility + Limiter + M4L |

`VERIFICADO`.

**O que a tabela prova:** não existe "o master do gênero". Existe **um continuum** — do Let You Go
(master = um trim de −3,3 dB, nada mais) ao Drift (dois limiters em série). O que três das quatro escolas
compartilham é **FX por pista entre 2,7 e 3,5**; o Giants (5,1) e o set (5,07) estão no extremo maximalista
— mesma densidade por pista, por motivos diferentes (o Giants por ser curso com 71 pistas; o set por ter
~20 trilhas de FX por família).

O set está **acima** da régua de FX por pista (5,07 contra mediana 2,88) e no meio do continuum de master.
Maximalista em duas dimensões: densidade por pista (igual ao Giants) e tamanho (2,5× a mediana de pistas,
129× as notas).

---

## 4. Racks `.adg` — amostra de 125

| Tipo | Quantidade | Conteúdo |
|---|---|---|
| Cadeias de efeito (sem instrumento) | **48** | Eq8 63 · Delay 39 · Limiter 37 · AutoFilter 30 · StereoGain 29 · Reverb 29 · Saturator 26 · Multiband 21 · Compressor2 19 |
| Racks de bateria | **1** | rack de hats |
| Racks com plugin | 0 | — |

Distribuição: 90 em um mega pack de psytrance, 20 + 13 em packs de peak-time techno, 2 avulsos.
`VERIFICADO`.
`INFERÊNCIA` — são cadeias de efeito reutilizáveis (EQ, delay, limiter, filtro, reverb, saturação) e **um**
rack de bateria. Não são "presets de som": são peças de mix. O valor está em reusar as cadeias, não em
procurar instrumento.

---

## 5. O que aplicar num set com este perfil (a partir do áudio)

| # | Ação | Prova numérica |
|---|---|---|
| 1 | **A/B de high shelf em 8–12 kHz** (+1,5 a +2 dB) no master ou no bus de madeiras/orquestra | ar 0,5% × mediana 1,6% |
| 1b | **Sala curta (0,7–1,0 s) para bateria**: nenhuma pista de bateria tinha reverb — as reverbs do set estavam em leads, madeiras e vozes | a escola Tim mede 0,71 / 1,04 / 0,78 s de drum room nas 3 faixas |
| 2 | **Cortar 120–400 Hz** (−1 a −2 dB) em uma faixa larga do master ou nos buses que acumulam low-mid | low-mid 13,7% × mediana 9,4% |
| 3 | **Não mexer no grave nem no estéreo** | bass idêntico, S/M +0,7 dB, grave 9 dB mais mono |
| 4 | Se for masterizar: mirar **−9 a −8 LUFS e true peak −0,3**, não os +2,3 dBTP das referências | mediana −8,7 / +2,3 |

## 6. Limites

- **Nada foi ouvido.** Bandas de energia são mapa, não julgamento.
- O render analisado é de uma data específica — pode não ser o estado final do set.
- As 15 referências são masters de lançamento; as diferenças de LUFS/TP medem masterização, não mix.
- A janela de 60 s de maior RMS é uma escolha: mede o clímax, não a média da faixa.
- Ferramentas antigas de comparação que carregam a 22,050 Hz e somam em mono **não servem** para esta régua:
  cortam o ar e perdem o estéreo.

---

## 7. Afinação e cauda do kick (medido)

### 7.1 Os 53 kicks do pack Drift (referência externa)

| Medida | Valor |
|---|---|
| Fundamental (pico 25–150 Hz) | mediana **49,1 Hz** · mín 25,6 · máx 68,0 |
| Classes mais comuns | **G1 (15)** · G#1 (11) · A1 (6) · F#1 (5) · E1 (5) |
| Decay −20 dB | mediana **0,19 s** · mín 0,08 · máx 0,39 |
| Duração do arquivo | mediana **0,48 s** |

`VERIFICADO`. O nome do arquivo carrega a nota e a medição confere: `PML_TH3_Kick_004_F#_Arson` → 45,1 Hz
(F#1) · `…_G_Brain` → 47,8 (G1) · `…_F_Greed` → 42,4 (F1) · `…_A#_Far` → 53,8 (~A#1).
`INFERÊNCIA` — o pack **afina o kick na nota**, mas não necessariamente na tônica: o loop de baixo citado é
D#min e o kick é F# (terça menor). O que importa é ser **grau consonante da tonalidade**.

### 7.2 Os dois kicks do set de referência

| Papel | Sample | Fundamental medida | Intervalo sobre C# |
|---|---|---|---|
| kick principal | `01. Punchy Kick - Outerverse.wav` | **52,5 Hz** | ≈ **G#1 (+20 cents) = 5ª justa** |
| kick alternativo | `TPS - Oasis - Kick 15.wav` | **46,4 Hz** | ≈ **F#1 (+81 cents) = 4ª justa** |

`VERIFICADO` por FFT nos dois arquivos.
**Os dois são consonantes com C#** (quinta e quarta). Não há problema de afinação.
No save medido **só o principal toca**; o alternativo está desligado — sem um segundo kick somando na
fundamental.

⚠️ **O nome mente:** o rack do kick principal se intitulava "Organic **48Hz**" e a fundamental medida é
**52,5 Hz**. Qualquer ajuste futuro feito "pelos 48 Hz do nome" erraria ~90 cents. Auditar o áudio, não o
nome.

### 7.3 Correção de leitura importante (semântica do .als)

No `.als`, `Mixer/Speaker` **não é mute**: `Speaker/Manual = true` significa **pista ATIVA**. Uma ferramenta
de auditoria antiga rotulava esse campo como `mute` — estava **invertida em 186 sets auditados**. Corrigido
em 25/10: o JSON de auditoria passou a trazer `active` e `mute` separados, com mute = inverso de Speaker.


---

## REVISAO-AUTOMACAO-CORTES-KICK-20261016.md

# REVISÃO — AUTOMAÇÃO LANE A LANE · CORTES · CAUDA · KICK NO VERMELHO (16/10/2026)

> Diagnóstico de leitura pura sobre um projeto de referência (minimal psytech, 128 BPM). Três perguntas originaram
> a revisão: (1) revisar a automação do Arrangement lane a lane; (2) conferir se algum corte de nota deixa cauda
> vazando (reverb/delay e afins); (3) o kick encostando no vermelho do master é problema?
>
> **Método:** auditoria offline do arquivo do projeto com scripts de leitura (clipes MIDI/notas, lanes de automação
> e cruzamento com devices de cauda), comprovando o modelo do arquivo contra a API do Live (LOM); e medição sobre o
> export de áudio de referência (466,9 s).

---

## 1. CORTES — 91 notas cortadas, e onde a cauda realmente vaza

**Modelo do `.als` provado contra a API do Live (LOM)** (fonte de erro comum na primeira tentativa): `Time` = origem
do conteúdo do clipe; `CurrentStart`/`CurrentEnd` = **janela de arranjo** (batem com `start_time`/`end_time` do LOM);
`MidiNoteEvent.Time` é relativo ao `Time`. Nota **fora** da janela é normal — o clipe vizinho do split toca aquela
parte. **Defeito é a nota que atravessa a borda**: começa dentro e termina depois.

**Resultado: 907 clipes MIDI · 91 notas cortadas · 16 canais.**

**Leitura cruzada — notas cortadas × devices de cauda ligados por canal:**

- **11 dos 16 canais não têm nenhum device de cauda ligado** — neles o corte é limpo por construção (o que sobra é
  só o release do instrumento). **Os três canais mais cortados (21, 21 e 8 notas, com passes de 66 beats,
  30,9 beats = 14,5 s e 12,0 beats = 5,6 s) estão entre os limpos.**
- **O vazamento real está em 5 canais**, todos com cauda ligada:
  - um bed atmosférico: Corpus 50 %, Echo 37 %, Reverb + send de 0,1999 (passe de 2,5 beats);
  - duas fontes com **Reverb de decay 3,09 s** (uma com Delay 25 %/FB 30 %, outra com Delay 12 %) — **o pior
    vazamento: a cauda continua soando até 6 compassos depois do corte**;
  - uma fonte com Reverb de decay 1,75 s e Delay 14 % (FB 27 %);
  - um lead com Delay 20 % (FB 38 %) e Reverb de decay 786 ms.
- Cortes percussivos menores (passes ≤ 0,2–0,9 beat) são irrelevantes; um Delay de 8 % com feedback 0 é inofensivo.

**Exemplo de corte correto:** um clipe reduzido de 4 para 2 beats com a nota terminando **exatamente na borda** da
janela — nenhuma nota passa; zero notas cortadas nesse canal.

**Armadilha que NÃO é defeito:** `FadeOutLength = 0` em **609 dos 611 clipes de áudio**. É o estado normal do Live
(ele aplica micro-fade automático na borda) — não entra no relatório como problema.

---

## 2. AUTOMAÇÃO — 166 lanes em 68 canais

**68 GRAVE · 54 MÉDIO · 44 limpas.** Tipos de GRAVE: 49 degrau duro · 25 duplicatas · 4 salto no beat 0 · 2 sem eventos.

### 2a. O padrão de "dip" — DESENHO, e medido como inaudível

**~370 pontos** de mute curto espalhados em 8 canais (36–42 pontos cada: hats, shaker, rolls, glitch, sub e kick) +
a lane de Volume do grupo da bateria desenhando o breakdown. Cada dip é `X.998: 0,3162` → `X.000: 0,000316` →
`Y.998: 0,000316` → `Y.000: 0,3162` = **60 dB em 0,9 ms**. É o recurso de arranjo de **ausência deliberada do kick**
— não é defeito.

**Medição no áudio em vez de teoria:** detector de descontinuidade (|Δamostra| / RMS local de 20 ms) nas **38
fronteiras de dip**: todas deram **0,002 a 0,19**, contra **mediana global 0,021 e p99,9 = 1,50**. **Não estalam** —
a chave cai em cima do onset da nota, não corta cauda. As 8 descontinuidades reais do arquivo (ratio 3,5–7,1) estão
em beats `X.28/.51/.79` que **não** são de dip (são ataques percussivos e o flick de Pan de 7 ms de um device de
stutter).

⇒ **CORREÇÃO DE RUMO (erro da primeira leitura, declarado):** o "sub saltado" foi lido como estalo causado pelo
degrau da lane. O estalo **não existe** (medido). O que se ouve é o **próprio degrau de nível** — o sub sai 60 dB
por 2 beats, 19 vezes. Dar forma ao dip (rampa de 15–30 ms em vez de 0,9 ms) é **decisão musical**, não conserto de
bug.

### 2b. Duplicatas — escadinhas e gates, também não é defeito

As 25 lanes com dois eventos no mesmo beat são **degraus de propósito**: escada de reverb (`RoomSize` e `PreDelay`
em passos de ~2 dB ao longo de ~22 beats — o reverb crescendo em degraus), Volume em saltos de 0,0–1,6 dB, gate de
EQ (−inf → +3,97 → −inf), Eq8 do grupo da bateria (−3 → −4,5). **Consequência prática:** uma ferramenta de escrita
offline de automação **recusa** lane com tempo duplicado — essas 25 lanes não são editáveis enquanto tiverem o par.

### 2c. O que É lixo de verdade (pouco, e barato)

- **4 lanes de filtro INERTES** (automatizam device desligado, sem lane de `On` que o justifique; filtros entre
  180–641 Hz e 450–1900 Hz). Ficaram de uma varredura anterior que desligou os devices. **Lane morta** — ou volta o
  device ou sai a lane.
- **2 cascos vazios:** `TimeSignature` e `Tempo` do master (sem evento nenhum).
- **2 lanes com ponto em beat 9600** (compasso 2400, muito além do fim do projeto). Inofensivo, mas é ponto órfão.
- **11 lanes automatizam o `On` de device** — **não** são órfãs: a lane É quem liga/desliga o device por seção.
  Legítimo.

---

## 3. KICK NO VERMELHO — medido

- **O render NÃO clipa:** pico global do export = **−0,71 dBFS** e **zero amostras no teto** (0 em 22,4 M).
- **O Limiter do master tem `Ceiling = −0,712 dB`** (`Maximize = false`) e o pico do arquivo é exatamente o teto ⇒
  **o limiter está clampando a soma.** Antes dele, o Glue está a −1 dB de threshold, 100 % wet.
- **A banda 30–90 Hz (kick + sub) bate em +0,09 a +0,21 dBFS** na mix — acima do fundo de escala nessa banda antes
  do master. Por seção: intro **+0,21** · drop 1 **+0,21** · 1:15 **−0,47** · marcha **+0,09** · drop 2 **+0,09** ·
  breakdown −3,96 · outro −2,57.
- O master toca o teto **~10,5 vezes por segundo** (4.928 rajadas, mediana de 0,1 ms), e **só 526 delas estão no
  grid do kick** — ou seja, não é só o kick: a mix inteira está encostada no teto.
- **RESSALVA:** a medição é de um export renderizado **antes** de o Bell de 48 Hz do canal do kick ir de
  **+3,50 → 0,00 dB**. O estado pós-ajuste está ~3,5 dB mais baixo em 48 Hz do que o medido.

**Resposta à pergunta:** é ruim **não** porque suja o arquivo (não clipa), mas porque o **limiter faz o trabalho no
lugar do kick** — ele achata a ponta de cada batida, que é onde mora o soco. A correção proposta (mexe no equilíbrio
da mix, logo é decisão do produtor): **Utility no canal do kick com ~−3 dB**, para a ponta do kick ficar em
~−3 dBFS no canal e o limiter parar de segurar toda batida.

---

## 4. ESTUDO DE CASO — CAMADA DE INVOCAÇÃO CURTA NOS VAZIOS

Técnica: camada de "invocação" (motivo curto de duas notas) inserida apenas em **vazios de ≥ 16 beats** de distância
de qualquer clipe existente. Gesto base: **G#3 (MIDI 56) por 0,5 beat → C#4 (61) por 1,5 beat** — a quinta ancestral.
Variações: inversão descendente (**61→56**), tensão pela b2 (**56→62**) e abertura ascendente (**61→68**, G#4).
Todas as entradas de **2 beats**, distribuídas por seções de energia diferente (logo após um drop, marcha, descida,
segundo drop, outro).

**Resultado do caso:** a camada passou de 8 para 16 entradas e de ~28 para ~44 beats de presença — quase o dobro de
presença, com cada entrada **mais curta** e o **vazio preservado** entre elas.

**Verificação:** cada entrada conferida nota por nota (pitch, tempo, duração e velocity) por leitura de volta da API
(`get_notes_extended`); nenhuma entrada sobrescreveu clipe existente (as bordas dos clipes vizinhos permaneceram
intactas).

---

## 5. Ideias de automação que pedem edição offline (exemplos)

1. **Dar forma aos dips do sub** (rampa de 15–30 ms em vez de 0,9 ms) — a lane já existe; item mais seguro.
2. **Onda de filtro num braam por seção** (ex.: 1250 → 800 Hz ao longo de ~16 beats, reabre para 1650, reset a 700,
   sobe a 2100 Hz e corta pouco depois) — exige **criar o casco da lane** (o canal só tinha `AutoFilter2/On` e
   `Send`).
3. **Drive por seção num braam** (22 → 40 → 42 %) — mesmo caso: casco.
4. **Automatizar filtros que hoje estão estáticos** (ex.: LP de 850 Hz num canal étnico; filtro de 12,3 kHz num
   lead).
5. **Filtro de horn** (900 → 3200 Hz nos picos de frase — spec de um tutorial do Miles From Mars).
6. **Outro com o master apagando o TOPO primeiro** (desenho de slope invertido ainda não explorado).
7. **Saneamento barato:** as 4 lanes de filtro inertes, os 2 cascos vazios do master e os 2 pontos em beat 9600 (§2c).

Criar casco de lane exige patch no `.als` **com o Live fechado** (com ele aberto, o Live sobrescreve do RAM ao
salvar).


---

## SET-REF_CROSSING_REVIEW.md

# Cruzamento: o set de referência montado × o que as referências fazem (12/09/2026)

> Estudo do acervo psytech-lab, anonimizado. Estado medido após faxina (62 pistas); fontes comparadas:
> perfil de groove das 29 referências, medições Fox, bibliotecas de groove e estudo forense comparativo da
> Rolling Music. Os números das referências são externos e permanecem íntegros; o lado do set é tratado como
> "set de referência".

## 1. O que estava montado (verificado no Live)

- **Motor:** kick único ligado (a versão anterior foi removida, preservada em backup) · sub: **3 engines de
  sub simultâneas** · cama 4× (3 versões iguais + 1 em Serum, diferente de verdade).
- **Topo novo:** hat em Serum + closed hat em Gatelab + **acid FREAKAUDIO ACID** (Serum FX) + FX PACK 73 +
  tape rewind + 2× Serum FX (uma mutada).
- **Movimento:** wood editado (26 clipes), swells reeditada (16 clipes, vol 0.27), shaker de teste reciclado
  (26 clipes 96–495, cadeia Serum+Filter+Delay).
- Personagem 4× (B/E/D/C), glitch 5×, wood ~6 no ar.

## 2. O que ainda estava duplicado igual — para mexer

| Prioridade | Família | O que é | Overlap medido |
|---|---|---|---|
| **P0** | **Glitch 5×** | 5 pistas com os MESMOS 22 clipes + mesmo device | 407–408 beats (100% do tempo) |
| **P0** | **Sub A×D×C** | 3 engines de sub simultâneas | 287–333 beats — risco de fase/embolação no low-end (regra de método: sub mono e único) |
| P1 | **Swells** | 3× mesmos 7 clipes (a 4ª já reeditada) | 137 beats |
| P1 | **Yao A×B** | 2× mesmos 10 clipes (C/D/E já mudos) | 283 beats |
| P2 | **Personagem** | 4 simultâneas, clipes diferentes mas sobrepostos | 329–393 beats |
| P2 | **Cama** | 4 simultâneas (1 em Serum, diferente de verdade) | 236–411 beats |
| P2 | **Wood** | 4 + 2 de teste somando | 61–394 beats |

**Nota:** as somas múltiplas são parte da "profundidade cruda" aprovada de ouvido — a decisão
cruda × organizada fica em aberto. O que é objetivo: **glitch 5× e sub 3× são os dois pontos onde a soma
idêntica pesa mais** (glitch = 5× o mesmo evento; sub = risco de cancelamento de fase no grave).

## 3. Cruzamento com as referências — onde estava perto e onde faltava

### O que já estava parecido (os acertos de ouvido)
| O que o set fazia | A referência que isso imita |
|---|---|
| Ácido FREAKAUDIO + FX packs + tape rewind | **acelero narrativo Akari/Artemis** (eventos rápidos no midrange, transições marcadas) |
| Wood editado denso (26 clipes) + ticklers ×.772 | **Greenwolve/Rolling** (madeiras respondendo, micro-pocket) |
| Sub staccato + Desert Nomads | movimento de bass psy (Zenon/Desert Nomads são da linhagem certa) |
| Hat em Serum + Gatelab closed hat | topo aéreo da Fox (começado — faltava ganho) |
| Ghost notes nos canais de teste (vel 48/72) | **Petrix Allert 30/32 ghosts** — a técnica do selo |

### O que as referências têm e o set ainda não tinha (lacunas medidas)
1. **Topo aéreo com ganho real** — Fox: 4–10 kHz a −20 dBFS; o set: −47. Os hats existiam, mas o master
   continuava escuro no ar. Medir de novo no master após a mix.
2. **Rolling bass que "pega o bastão" a ~180 ms** — a referência Fox (60–120 Hz a −12) e os 29 GROOVE_BASS
   extraídos mostram o desenho; o sub do set ainda era 3 engines somadas, não um rolling único com
   harmônicos em 120–250 Hz.
3. **Pull sensual distribuído** — na Rolling é contínuo (offset 0.61 no breakdown); no set só nos canais de
   teste. Sugestão: 1 percussão lateral com o pull em todos os blocos, não só 192–304.
4. **Um elemento por função** — nenhuma ref soma 5 cópias do mesmo evento; elas variam timbre/pitch por
   bloco. É o desvio estrutural mais visível.

## 4. Plano mínimo sugerido (sem executar)

1. **Glitch 5× → 1×** (manter uma, mutar as outras 4) — ganho imediato de clareza no midrange, zero risco
   musical (são idênticas).
2. **Sub 3× → 1× + verificar fase** — testar cada um sozinho contra o kick antes de escolher.
3. Swells: manter só a reeditada.
4. Personagem/cama: testar a versão Serum vs as iguais, depois 1×.
5. Wood: decidir a duplicata parcial (apagar ou virar variação).
6. Depois da faxina: medir master vs Fox (4–10 kHz) para calibrar ganho do topo.

## 5. Camada 2 — presets dos Serums comparados (state binário do arquivo)

Todos os devices estavam **LIGADOS** (único device OFF = trem ghost pump, igual nos 3 subs). Hashes do
ProcessorState:

| Família | Pist. | Veredito |
|---|---|---|
| **Sub** (3 engines) | 3 | **MESMO PRESET EXATO** (hash 2a3764702c4e ×3) — os nomes são diferentes, o SOM é 3× idêntico. Duplicata real mais grave do set. |
| **Glitch** | 5 | 3 sons distintos: 2 próprios + **trio idêntico** (03f4291733cd). Redução correta: manter os 2 e 1 do trio. |
| **Personagem** | 4 | 1 próprio; **trio idêntico**. Redução: 1 + 1 do trio. |
| **Swells** | 4 | **4 presets DIFERENTES** — não são duplicatas sonoras; são 4 timbres somados (decisão artística, não faxina). |
| Cama em Serum | 1 | state único de 1,95 MB (com samples embutidos no Serum). |

**Correção ao mapa da seção 2:** sub ×3 é duplicata total (mesmo preset). Glitch/Personagem: redução segura =
manter as variações A/B e UMA cópia do trio idêntico. Swells: ouvir antes de cortar — são timbres diferentes
somados no mesmo tempo.

**Método (replicável):** comparar o hash do ProcessorState do Serum entre pistas "iguais" — hash idêntico =
mesmo som (faxina); hash diferente = timbres somados (decisão artística, ouvir antes de cortar).

## 6. Medição pós-faxina (janela mais energética da captura) — base da receita do bass

| Banda | Set | Fox (drop) | Gap |
|---|---|---|---|
| 20–60 | −16,7 | −10,0 | −6,7 |
| 60–120 | −17,6 | **−7,1** | **−10,5** |
| 120–300 | −18,9 | −14,4 | −4,5 |
| 300–1 k | −25,8 | −19,4 | −6,4 |
| 1–4 k | −35,9 | −19,9 | −16,1 |
| 4–10 k | −42,6 | −20,5 | −22,2 |

Faxina + elementos novos fecharam: 60–120 **+5,6 dB**, 120–300 **+9,3**, 1–4 k **+7,1**, 4–10 k **+4,6**
(direcional: kick/trecho diferentes entre as duas medições). Peak da janela: −0,7 dBFS (limiter no teto).

**Receita do bass novo derivada dos números:**
1. **60–120 Hz é o maior gap musical (−10,5)** — na Fox essa é a banda MAIS ALTA de todas (rolling bass
   domina). No set o grave ainda era sub-centrado (20–60 acima de 60–120).
2. **Arquitetura:** sub puro em C#1 (34,65 Hz, mono) + camada rolling cujos HARMÔNICOS 2º/3º (69,3 / 103,9 Hz)
   entregam o 60–120 — é assim que a Fox domina a banda sem subir o sub.
3. **Nível alvo:** 60–120 de −17,6 → ~−11 (fechar 6–7 dB com o rolling; limites: não subir 20–60 mais que
   ~1–2 dB; 120–300 já está a −4,5, harmônicos acima disso estragam).
4. **O resto do gap (1–4 k −16, 4–10 k −22) é GANHO DO TOPO**, não bass — por isso 120–300 deve parar em
   −4,5: mais mordida aí vira congestionamento, o ar vem dos hats.


---

## SET-REF_SESSION_MAP.md

# Mapa de sessão de um set de referência — material de estudo extraído (12/09/2026)

> Estudo do acervo psytech-lab, anonimizado. O original é um mapa de sessão do set (tabelas de mutes por
> canal, backups, rollbacks, estado não salvo) — essa parte é estado puro e foi removida. Fica o material
> transferível: hipóteses de teste, o design system de resposta, o tratamento medido de transições, o mapa
> espacial da profundidade e as lições operacionais do Live.

Contexto: set a 128 BPM, C# frígio, loop de trabalho no drop 1 (beats 192–304), retornos A-Reverb (0.85) e
B-Delay (0.85).

## 1. Hipóteses de teste (canais de teste, todos mutados por padrão, clipes 192–304)

| Hipótese | Pergunta que responde | Implementação |
|---|---|---|
| **Micro-hats 16th sintopado** — velocidade no topo | O 16th sintopado deixa a faixa mais rápida sem virar metralhadora? | 16ths com pocket no 4º beat (silêncio .75); Serum 2 |
| **Ear ticklers 3D órbita** — movimento ao redor da cabeça | Os micro-ticks ×.772 orbitando dão profundidade sem Auto Pan em tudo? | Simpler wood + Delay + AutoPan |
| **Perc orgânica sincopada** — corpo no centro | A perc sincopada dá malandragem sem encher o groove? | perc de pack (BLACKBOX) sincopada, sem AutoPan |
| **Wood click resposta** — conversa | O wood respondendo nos gaps cria diálogo ou fica espalhado? | wood só responde nos gaps dos bars pares |
| **Shaker swing malandro** — atraso sensual | O shaker com +0.02 beat traz o swing do tech house antigo ou fica datado? | 8ths com +0.02 beat no contratempo; Operator |

Volumes 0,75–0,9; densidade crescente (ghost notes nos blocos finais). **Padrão ×.772** (atraso ~10 ms no
micro) = linguagem de swing já usada no material original.

## 2. Design system de resposta (duelo de personagens)

- **Resposta em duelo (−1 oitava):** duplicar o personagem A com patch/FX intactos; a resposta espelha TODAS
  as frases do A −1 oitava (ex.: 61→49, 62→50, 56→44, 68→56), shift +2.0/1.5/2.5 beats onde couber sem
  colisão, velocity −10~14, fecho na quinta (44). Anti-colisão: resposta nunca toca junto com o A.
- **Tema nos cortes:** célula malandra que entra nos cortes REAIS do kick (espera o kick e não vem — a
  surpresa). Vocabulário descendente 68→62→56→50 com "mordida" no bII (a nota frígia) + ghosts vel 52.
  Auto Pan-Tremolo em modo Panning (Sine, 68%, synced 1 bar, Phase 180°) = varredura 3D de um lado pro outro
  (linguagem Greenwolve/Ear Ticklers).
- **Regra anti-colisão:** cada célula nunca sobrepõe A, B ou outra C — a varredura pula posições ocupadas.
- **Regra de dono:** 1 dono por corte (janela de FX exclui célula melódica, e vice-versa).

**O sistema da conversa:** A pergunta → B responde grave no vácuo → kick corta → C entra inesperado rasgando
em 3D → subs complementam. Papéis por artista de referência: **Akari** = chão quase reto; **Gazolla** = corte
seco e PUSH; **Desert Nomads / Tiger Eyes** = retorno deslizante; **Greenwolve** = malandragem lateral;
**Rolling** = PULL sensual.

## 3. Tratamento medido de transições (FX pack e tape rewind)

- Auto Filter HP no canal de FX (**111 Hz**) e no tape rewind (**151 Hz**) — calibrado por bissecção no display.
- Sends medidos: FX pack A-Reverb 0,25 / B-Delay 0,15; tape rewind A-Reverb 0,40 / B-Delay 0,30 (cauda do
  corte seco Oziris).
- Base: dicionário de 232 FX das referências — a transição das refs vive no **topo** (centro 3–3,5 kHz,
  ~1/3 >4 kHz) e **NUNCA no grave**; o FX pack medido tinha **37% da energia <100 Hz** → HPF obrigatório.

## 4. Mapa espacial da profundidade (molde de organização)

- **Centro/chão:** kick + sub ground (senoidal + saturador) + camas de médio (150–400 Hz no centro).
- **Frente:** personagem melódico (synth + delay + filtro, sends de reverb/delay).
- **Laterais:** madeiras (delay ping-pong + auto pan), glitches, ear ticklers.
- **Fundo/altura:** camas atmosféricas com filtro fechado, drones, chants, swells, caudas reversas.
- **Movimento ao redor da cabeça:** auto pan-tremolo das madeiras (binaural), micro-hats.
- **Silêncio:** vácuos programados (bars 24/32), corte seco no estilo da referência, caudas reversas.

## 5. Lições operacionais (Live 12, verificadas na sessão)

- `set_notes` legacy via bridge **ADICIONA**, não reconstrói — sempre `remove_notes` antes, ou usar
  `add_notes clear=true` pela ponte.
- `get_notes_extended` retorna tempos **RELATIVOS ao clip** — misturar com absolutos dobra as posições.
- Popups de permissão do script aparecem na GUI do Live e travam a chamada até alguém aceitar.
- Filtro de pistas por nome: buscar "kick" (não "ick", que pega Wood Click).
- `AudioClip.file_path` EXISTE no Live 12 — dá para medir o WAV real de cada clipe.
- Um corte de kick no meio do arranjo pode ser intencional (duelo de personagens sem kick) — checar o desenho
  antes de "consertar".
- Clipes de transição de biblioteca têm o tratamento certo no topo (HPF + sends) e errado no grave — medir
  a energia <100 Hz antes de mandar o FX para a frente.


---

## SET-REF_TEST_MENU.md

# Menu de testes de escuta — método e design system (12/09/2026)

> Estudo do acervo psytech-lab, anonimizado. O original é um menu de A/B para escuta no set (números de
> canal, comandos de script e estado de mutes) — essa parte é estado puro e foi removida. Fica o **método do
> menu de teste** e o **design system da conversa**, que são transferíveis.

## 1. O método do menu (replicável)

- Cada teste nasce **mutado por padrão**; ouve-se UM por vez (desmute → ouvir → voltar ao estado).
- Cada teste registra: **sensação** (o que promete), **pergunta que responde**, **como ouvir** e **como voltar**.
- Loop de trabalho fixo (o mesmo trecho sempre) para comparar testes entre si.
- **Teste conjunto declarado:** combinar dois testes que competem no mesmo papel para ouvir a hipótese em
  pares ("topo corre veloz + órbita" → hipótese "acelero Akari + elasticidade Greenwolve").
- **Alternador** para famílias com múltiplas versões (ex.: kicks): um candidato por vez, com pergunta final
  registrada ("versão sem transposição vs transposta +0,65 st").

## 2. As perguntas do menu (o caso)

| Teste — sensação | Pergunta que responde |
|---|---|
| **Micro-hats 16th sintopado** — velocidade no topo | O 16th sintopado deixa a faixa mais rápida sem virar metralhadora? |
| **Ear ticklers 3D órbita** — movimento ao redor da cabeça | Os micro-ticks ×.772 orbitando dão profundidade sem Auto Pan em tudo? |
| **Wood click resposta** — conversa | O wood respondendo nos gaps cria diálogo ou fica espalhado? |
| **Perc orgânica sincopada** — corpo no centro | A perc sincopada dá malandragem sem encher o groove? |
| **Shaker swing malandro** — atraso sensual | O shaker com +0.02 beat traz o swing do tech house antigo ou fica datado? |
| **Personagem B resposta (duelo −1 oit)** — diálogo bass/lead | O duelo −1 oitava funciona em toda a música? (B responde TODAS as frases do A) |
| **Personagem C tema (enters nos cortes)** — o inesperado | O tema malandro entrando nos cortes de kick (espera o kick e não vem) vira surpresa boa? |

## 3. Design system da conversa (A pergunta → B responde → C entra)

- **A pergunta** (personagem principal) → **B responde** grave no vácuo, espelhado −1 oitava
  (61→49, 62→50, 56→44, 68→56), shift +2.0/1.5/2.5 sem colisão, velocity −10~14, fecho na quinta (44).
- **Kick corta** → **C entra inesperado** rasgando em 3D (células malandras nos cortes reais do kick;
  vocabulário 68→62→56→50 com mordida no bII frígio + ghosts vel 52).
- **Auto Pan-Tremolo em Panning** (Sine, 68%, synced 1 bar, Phase 180°) = o rasgo 3D de um lado pro outro
  (linguagem Greenwolve/Ear Ticklers).
- Anti-colisão: resposta nunca toca junto com o A; célula nunca sobrepõe A, B ou outra C — a varredura pula
  posições ocupadas.

**Papéis por artista de referência:** Akari = chão quase reto; Gazolla = corte seco e PUSH;
Desert Nomads/Tiger Eyes = retorno deslizante; Greenwolve = malandragem lateral; Rolling = PULL sensual.

## 4. A decisão de profundidade (pergunta de curadoria)

| Opção | O que é |
|---|---|
| **Profundidade cruda** | famílias ×5 somadas (cama/drone/chant/glitch/swells/reverse) — o que estava no ar |
| **Profundidade organizada** | 1 versão por família (mantém uma, muta as outras 4) |

O objetivo do teste: decidir se a soma quíntupla é **assinatura** ou **vazamento**. (No caso original a
decisão ficou em aberto — é decisão de escuta.)

## 5. Limitações registradas

- Os canais de teste tinham devices herdados de outro material (delay ping-pong) — parte do caráter vem da
  herança; isolar o caráter novo exige limpar a cadeia herdada.
- Duas camadas de kick estavam dobradas em uma seção da intro e foram reduzidas a uma (estado registrado para
  não "consertar" duas vezes).
- Estado de sessão não salvo no momento dos testes — o estado de mutes era volátil (lição: registrar o estado
  antes de ouvir).
