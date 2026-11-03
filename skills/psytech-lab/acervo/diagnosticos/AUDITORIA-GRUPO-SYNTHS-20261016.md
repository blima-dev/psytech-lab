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
