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
