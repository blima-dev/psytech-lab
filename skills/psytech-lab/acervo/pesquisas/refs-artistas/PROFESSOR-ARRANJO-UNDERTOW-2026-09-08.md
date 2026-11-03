# PROFESSOR DE ARRANJO — UNDERTOW (Artefakt): a gramática de arranjo de uma referência

Data: 2026-09-08 · Fonte: extração do Set de referência "Artefakt - Undertow" (somente leitura): **702 clipes, 22 tracks, 233 compassos, 120 BPM**. Saída estruturada: DNA de arranjo em JSON.

Método: tabulação direta dos clipes do arrangement (cada clipe = `{track, start, end, name}` em beats). Nada aqui é conselho genérico: toda regra tem contagem ou posição medida. Automation, mix, conteúdo de áudio e estrutura interna dos clipes NÃO foram capturados pela extração (limitação registrada).

Descoberta que organiza tudo: **VERIFICADO** que o conteúdo musical inteiro de 233 compassos vem de ~6 gravações-fonte recicladas — família "Wood hits" (15 clipes em 5 tracks), família "Twig shaker" (9 clipes em 4 tracks), "Wind in trees" (3), pad "18-LABS 2" (13 em 3 tracks), "Air Pump" (418) e o kick processado. O Undertow não compõe seções novas: **recicla os mesmos materiais em versões novas**.

---

## 1. Tabela canônica (blocos de 4 compassos)

Colunas: `act` = clipes ativos no bloco · `tr` = tracks ativas · `ent` = clipes que ENTRAM · `sai` = clipes que SAEM · `entra-nova` = track que estreia no bloco.

| Blk | Bars | act | tr | ent | sai | entra-nova | Função do bloco de 16 (VERIFICADO dos dados) |
|---|---|---|---|---|---|---|---|
| 0 | 0–4 | 24 | 9 | 24 | 10 | 5 tracks (fundação+texturas) | **0–16 INTRO/FUNDAÇÃO**: kick processado (return), top kick, stem pre-master, Wood hits cru, vento, Edged, Air Pump |
| 1 | 4–8 | 22 | 9 | 8 | 9 | — | idem |
| 2 | 8–12 | 21 | 9 | 8 | 8 | — | idem |
| 3 | 12–16 | 22 | 9 | 9 | 11 | — | idem |
| 4 | 16–20 | 20 | 10 | 10 | 9 | **Round (16)** | **16–32 GROOVE I**: baixo/pulso grave entra, fundação intacta |
| 5 | 20–24 | 20 | 10 | 8 | 9 | — | idem |
| 6 | 24–28 | 18 | 9 | 8 | 9 | — | idem |
| 7 | 28–32 | 18 | 9 | 8 | 8 | — | idem |
| 8 | 32–36 | 20 | 11 | 10 | 8 | **Mod shaker + 8th shaker (32)** | **32–48 GROOVE II**: mesmo Twig Shaker dobrado em 2 tracks |
| 9 | 36–40 | 20 | 11 | 8 | 8 | — | idem |
| 10 | 40–44 | 21 | 12 | 9 | 8 | **Round, Vox Pathfinder Ret (40)** | idem — entrada FORA do múltiplo de 8 |
| 11 | 44–48 | 21 | 12 | 8 | 8 | — | idem |
| 12 | 48–52 | 21 | 12 | 8 | 8 | — | **48–64 DESENV. SUSTENTADO**: zero tracks novas, clipes correndo |
| 13 | 52–56 | 21 | 12 | 8 | 8 | — | idem |
| 14 | 56–60 | 22 | 12 | 9 | 9 | — | idem |
| 15 | 60–64 | 23 | 12 | 10 | 10 | — | **refresh 1 @63.5**: Shifting Perc + Field Rec trocam de versão com stitch de 0,5 bar |
| 16 | 64–68 | 29 | 14 | 17 | 15 | **RE201 + Shaper Mid (64)** | **64–80 DESENV. I**: liga a engine de chops no return de delay |
| 17 | 68–72 | 30 | 14 | 15 | 15 | — | idem |
| 18 | 72–76 | 30 | 14 | 16 | 16 | — | idem |
| 19 | 76–80 | 29 | 14 | 14 | 14 | — | idem |
| 20 | 80–84 | 31 | 15 | 17 | 16 | **Perc Tension (80)** | **80–96 DESENV. II** |
| 21 | 84–88 | 32 | 15 | 16 | 16 | — | idem |
| 22 | 88–92 | 36 | 15 | 21 | 21 | — | pico local de chops |
| 23 | 92–96 | 32 | 17 | 16 | 14 | **Pads Ret (92), Pad 3 (94.44)** | preview harmônico — pads entram ANTES do breakdown, Pad 3 fora do grid |
| 24 | 96–100 | 31 | 17 | 14 | 16 | — | **96–112 PRÉ-BREAKDOWN** |
| 25 | 100–104 | 31 | 16 | 15 | 15 | — | Air Pump morre no bar 103.7 (gap de 50 beats) |
| 26 | 104–108 | 23 | 15 | 8 | 8 | — | só chops RE201 sustentam |
| 27 | 108–112 | 23 | 15 | 7 | 7 | — | clipes dos shakers/Shaper/RE201 terminam exatamente em 112 |
| 28 | 112–116 | 13 | 12 | 1 | 4 | **Pad 1 (112)** | **112–128 BREAKDOWN→REFRESH**: mínimo da track (13 clipes ativos); Pad 1 anuncia |
| 29 | 116–120 | 21 | 13 | 8 | 8 | — | Air Pump volta @116.23 |
| 30 | 120–124 | 22 | 14 | 10 | 10 | **Corpus metal (120)** | stitch Round @125.12 (3,5 beats) |
| 31 | 124–128 | 29 | 17 | 21 | 17 | **Pad 2 (126)** | **REFRESH 2 @126**: 10 tracks reentrancam em ≤1,5 bar |
| 32 | 128–132 | 31 | 17 | 14 | 16 | — | **128–144 CLÍMAX I** |
| 33 | 132–136 | 31 | 16 | 16 | 15 | — | idem |
| 34 | 136–140 | 32 | 17 | 16 | 16 | — | idem — Perc Tension volta @139 |
| 35 | 140–144 | 32 | 18 | 17 | 15 | — | idem |
| 36 | 144–148 | 32 | 18 | 14 | 16 | — | **144–160 CLÍMAX II** |
| 37 | 148–152 | 32 | 17 | 16 | 15 | — | idem |
| 38 | 152–156 | 33 | 17 | 16 | 17 | — | idem |
| 39 | 156–160 | 35 | 19 | 19 | 15 | **808 hat (158)** | entra o topo; 19 tracks = máximo da música |
| 40 | 160–164 | 35 | 19 | 15 | 17 | — | **160–176 TOPO**: pads em ciclos 4-on/4-off |
| 41 | 164–168 | 33 | 17 | 15 | 15 | — | idem |
| 42 | 168–172 | 32 | 17 | 15 | 15 | — | idem |
| 43 | 172–176 | 33 | 18 | 15 | 14 | — | Pad 3 volta (12 bars) @174 |
| 44 | 176–180 | 34 | 18 | 16 | 16 | — | **176–192 SAÍDA I** |
| 45 | 180–184 | 35 | 18 | 16 | 16 | — | idem |
| 46 | 184–188 | 37 | 19 | 18 | 22 | — | **REFRESH 3 @185.5/186** (Edged, Round, Pad 1) = ÚLTIMA entrada nova da música |
| 47 | 188–192 | 30 | 15 | 15 | 16 | — | **192–208 SAÍDA II**: sem entradas |
| 48 | 192–196 | 29 | 14 | 15 | 15 | — | idem |
| 49 | 196–200 | 28 | 14 | 15 | 15 | — | idem |
| 50 | 200–204 | 27 | 13 | 14 | 15 | — | RE201 termina @204 |
| 51 | 204–208 | 19 | 11 | 8 | 12 | — | 808 hat termina @206 |
| 52 | 208–212 | 17 | 10 | 8 | 8 | — | **208–233 CAUDA**: cascata de fins |
| 53 | 212–216 | 17 | 10 | 8 | 8 | — | idem |
| 54 | 216–220 | 17 | 10 | 8 | 8 | — | idem |
| 55 | 220–224 | 13 | 10 | 4 | 7 | — | Field Rec e Air Pump terminam @222 |
| 56 | 224–228 | 6 | 6 | 0 | 1 | — | zero entradas; Round termina @228 |
| 57 | 228–232 | 4 | 4 | 0 | 1 | — | só returns + Round Vox |
| 58 | 232–233 | 1 | 1 | 0 | 4 | — | último som: Round, Vox Pathfinder (termina @232.8) |

Leituras diretas da tabela (**VERIFICADO**): densidade média de 25 clipes ativos por bloco; mínimo 13 no breakdown (112–116); máximo 37 no refresh 3 (184–188); a mesma contagem de clipes ativos **nunca** se repete por mais de 4 blocos consecutivos (= 16 bars; máximo observado: 21 clipes em 48–64 e 32 clipes em 136–152).

---

## 2. Os 11 padrões de microvariação (com contagem exata)

Contado sobre os 702 clipes. Ordem de frequência.

| # | Padrão | Ocorrências | Evidência medida |
|---|---|---|---|
| P1 | **Re-trigger de pulso respiratório (Air Pump)** | **418** re-triggers | 418 clipes de exatamente 1 beat, a cada 2 beats, fase fixa 0.906, dos bars 0.23 a 222. Só 2 gaps: 50 beats (bar 103.7→116.2 = pré-breakdown) e 6 beats (123.7→125.2 = colado no refresh). |
| P2 | **Chop de loops no return de delay (RE201)** | **223** clipes | 151 "Short Loop" (97× 2 beats, 14× 4, 9× 6, 8× 1.125, 6× 1.5, 6× 3.105…) + 63 "Long Loop" (17× 4, 15× 2, 14× 2.5, 9× 1.375, 8× 0.895) + 9 takes "Audio" (2–71 beats), bars 64–204. 16 sobreposições consecutivas; 53 loops contidos dentro de takes "Audio" longos. Ritmo de ~27 chops por bloco de 16 bars (bloco 112–126: só 4 = breakdown). |
| P3 | **Commit longo ("entra e fica")** | **51** commits ≥4 bars; 28 ≥40 bars | Mediana de duração dos commits: **48 bars**. Ex.: Round 108 bars (16–124), Twig Shaker 80 bars ×2 tracks, Round Vox 192.8 bars (40–232.8), Field Rec 158 bars (64–222). Não existe mute intercalado de elemento. |
| P4 | **Camada cruzada do mesmo material (cross-track layering)** | **37** clipes reciclados | Wood hits em 5 tracks (Source, Edged, Round, Perc Tension, Corpus metal) = 15 clipes; Twig shaker em 4 tracks = 9; 18-LABS em Pad 1/2/3 = 13. O mesmo arquivo é o conteúdo de "baixo" (Round), "percussão" (Perc Tension) e "efeito" (Corpus metal). |
| P5 | **Entradas fora do grid humano, fase travada** | **463** clipes fora do beat inteiro; **565/702** fora da linha de compasso; 68 durações não-inteiras | O Air Pump inteiro vive na fase 0.906 (constante, não aleatória); entradas de tracks em 0.23, 92, 94.44, 126, 158 (fora do múltiplo de 8); stitches em 63.5, 125.12, 185.5. Macro desalinhado + micro phase-locked. |
| P6 | **Refresh em massa (troca de versão, não de material)** | **3** eventos (63.5, 126, 185.5/186) | @126: **10 tracks** reentrancam em ≤1,5 bar (Round, Mod shaker, 8th shaker, Shaper Mid, RE201, Edged, Edged Vox, Pad 1, Pad 2, Shifting Perc@126.5) com clipe novo do MESMO arquivo. Espaçamento dos refreshes: 62.5 e 59.5 bars. |
| P7 | **Reentrada após gap (subtração por fim de clipe)** | **11** eventos | 4 tracks terminam exatamente no bar 112 e voltam juntas no 126 (gap 14 bars): Mod shaker, 8th shaker, Shaper Mid, RE201. Perc Tension 124→139 (15). Pad 2 2× (12). Pad 1 162→186 (24). Pad 3 98.4→174 (75.6). Air Pump 104→116.2 (12.2). Edged Vox 0.8→59.4 (58.6). |
| P8 | **Pads cíclicos 4-on/4-off** | **13** clipes de pads | Pad 1: 112–120 (8 bars), 120–124, depois 4 bars a cada 8 (126, 134, 142, 150, 158) = respiração 4-on/4-off, reentrada final 186. Pad 2: 3× a cada 16 bars (126, 142, 158). Pad 3: 4 bars @94.44 + 12 bars @174. |
| P9 | **Correntes de mesmo nome colados (segmentação de material)** | **53** correntes, 91 enlaces, run máx. 4 | Mesmo clipe re-segmentado em pedaços adjacentes (ex.: Field Rec "Wind in trees" 0.5 bar + 158 bars; Perc Tension 44 + 19 + 28). O material continua, o contorno muda. |
| P10 | **Stitch de transição (clipe-ponte)** | **3** | Clipe-ponte de 0.5–3.5 beats colando versão antiga→nova: Field Rec 0.5 bar @63.5; Round 3.5 beats @125.12; Edged 0.5 bar @185.5. |
| P11 | **Freeze/stack de versões renderizadas** | **8** grupos de stack; 6 clipes "(Freeze)" | 5 pares "normal + (Freeze)" no mesmo start (Source@0, Edged@0/126/185.5, 808 hat@158); Edged Vox Ret@0 com 6 takes empilhados; RE201 com loops sobre o take Audio. "(Freeze)" + timestamp no nome = versão renderizada/resampleada do mesmo material (HIPÓTESE sobre a semântica exata do comando; o padrão de nome é VERIFICADO). |

---

## 3. GRAMÁTICA TEMPORAL do Undertow (10 regras derivadas dos dados)

G1. **A fundação é imortal.** Kick processado (2 returns) + stem pre-master = 3 clipes únicos de 232 bars, do bar 0 ao fim, sem uma única interrupção no nível de clipe. VERIFICADO (conteúdo de áudio interno NÃO VERIFICADO). A energia é administrada removendo camadas de cima, nunca a base.

G2. **Elemento entra e fica.** 51 commits ≥4 bars, mediana 48 bars; nenhum elemento é mutado e religado dentro do próprio clipe. Saída de elemento = fim de clipe natural, desenhado para terminar no ponto certo (4 tracks terminam exatamente no 112).

G3. **1 track nova a cada ~16 bars.** 14 tracks novas ao longo de 233 bars; intervalos: mediana 16, média 12 (mín. 2.4, máx. 32). O arrangement cresce por adição lenta e constante.

G4. **Densidade nunca fica estática por mais de 16 bars.** Máximo de 4 blocos de 4 bars consecutivos com a mesma contagem de clipes ativos. Não existe "groove igual por 32 bars" — sempre há um clipe entrando ou saindo a cada bloco de 4.

G5. **Refresh de versão a cada ~60 bars, com stitch.** Nos bars 63.5, 126 e 186 (espaçamento 62.5 / 59.5) os mesmos materiais voltam com clipe novo — às vezes nome novo (Twigs Shaker→Twigs, Wind→0109, Wood hits→0106) — e um clipe-ponte de 0.5–3.5 beats costura a troca. Nada de material inédito no refresh: é nova versão do DNA.

G6. **Breakdown = subtração, e é único.** Em 233 bars existe UM breakdown (112–126, 14 bars): os clipes foram desenhados para acabar juntos no 112 e os elementos voltam juntos no 126. Densidade mínima da música: 13 clipes ativos. Os pads entram ANTES (92/94.44/112) para anunciar.

G7. **Engine de microvariação contínua em escala sub-beat.** Duas tracks trabalham o tempo todo: o pulso respiratório (Air Pump: 1 beat a cada 2, fase fixa, 222 bars) e o chop de delay (RE201: 223 fatias de 0.9–6 beats reorganizadas à mão, ~27 por 16 bars). A hipnose do Undertow é esta camada, não as seções.

G8. **Pads respiram em ciclos.** 4-on/4-off (Pad 1), a cada 16 bars (Pad 2), soltos fora do grid (Pad 3 @94.44). A camada harmônica pulsa em compassos, em vez de drone contínuo.

G9. **Macro humano, micro travado.** 5/14 tracks novas entram fora do múltiplo de 8 (0.23, 92, 94.44, 126, 158); 11/58 entradas de conteúdo fora da linha de compasso; o refresh principal cai no bar 126 (2 bars antes do múltiplo de 8). Mas a fase do pulso constante nunca muda (0.906 fixo). O groove é um metrônomo; a forma, um humano.

G10. **Saída em cascata, sem seção nova.** Última entrada nova: bar 186. A partir daí só fins: RE201 @204, 808 hat @206, Field Rec/Air Pump @222, Round @228, Round Vox @232.8. Cauda de ~47 bars encolhendo de 37 para 1 clipe ativo.

---

## 4. RECEITA DE MICROVARIÇÃO derivada da gramática (padrões → operações concretas)

Princípio geral extraído: **manter o material, multiplicar as versões.** Cada grupo abaixo converte os padrões P1–P11 em operação concreta sobre clipes de 8–32 bars.

### Subgrave / baixo contínuo
- **P3 (commit) + P9 (segmentação):** tornar o canal contínuo — um clipe longo por seção (32–64 bars), sem furos internos (o Undertow não tem nenhum gap na base).
- **P5 (versão A/A′):** duplicar o clipe e deslocar `loop_start` (ex.: começar no 2º beat do material) alternando A/A′ a cada 16 bars — variação sem material novo.
- **P10 (stitch):** na troca de seção, clipe-ponte de 0,5 bar antes da versão nova.
- LOM: `Clip.loop_start/loop_end/start/end` e `Clip.name` settable; `Track.duplicate_clip_to_arrangement` para clonar (API padrão do Live Object Model — NÃO VERIFICADO contra a doc de cada versão).

### Baixo médio / grooves médios
- **P4 (cross-track layering):** duplicar o clipe para uma track-gêmea processada (amp/sat) e tocar juntas só nos blocos de clímax — modelo exato: Twig Shaker em Mod shaker + 8th shaker (bars 32–112).
- **P6 (refresh):** reentrar com clipe novo do mesmo arquivo no marco de seção (~60 bars), nunca trocar o sample.
- **P11 (freeze):** renderizar uma versão e empilhar com a original no mesmo start nas transições.

### Hi-hat fechado / topo contínuo
- **P1 (modelo Air Pump — prioridade máxima):** substituir o clipe repetitivo de 8–32 bars por re-triggers de 1–2 beats com **fase fixa** deslocada (o Undertow usa +0.906 beat, constante por 222 bars). Fase fixa ≠ humanização aleatória — timing aleatório espalha a energia do hat e mata o groove empurrado das refs (hats adiantados −13 a −27 ms, concentrados num slot).
- **P8 (ciclo):** camada secundária de hat em ciclos 4-on/4-off (clipe de 4 bars a cada 8) como respiração do topo.

### Lead / melodia
- **P7 (anunciar):** entrar primeiro no breakdown/vácuo (modelo Pads Ret @92 e Pad 1 @112 — a camada que anuncia a seção seguinte), em ciclos 8-on/4-off, e só ficar contínuo no clímax.
- **P6 (versões nomeadas):** a cada refresh, clipe novo nomeado (Lead A, Lead A2) com contorno diferente (loop deslocado ou transposição via propriedades do clipe) em vez de material novo.

### Topo melódico / efeitos
- **P2 (modelo RE201):** gravar/bounce um take longo pelo return de delay/tape e fatiar loops de 2 e 4 beats ("Short/Long Loop"), reorganizando manualmente sobre o take — ~27 fatias por bloco de 16 bars na zona de desenvolvimento.
- **P11 (stack):** par "normal + (Freeze)" no mesmo start na virada das seções.
- **P5 (off-grid):** permitir entradas fora do múltiplo de 8 (o Undertow coloca o efeito novo em 94.44 e o topo em 158) mantendo a fase interna travada.

---

## 5. Verificação e limites

- VERIFICADO: todas as contagens, posições e durações saem de leitura direta do DNA extraído (702 clipes) por script python3; tabela completa e eventos macro no JSON de arranjo.
- VERIFICADO: kick/top-kick returns e stem pre-master como clipes únicos de 232 bars no nível de arrangement. O conteúdo de áudio interno (se o kick soa em todos os bars) é NÃO VERIFICADO — a extração não captura áudio/automation.
- HIPÓTESE: semântica do sufixo "(Freeze)" = versão renderizada (freeze/flatten) do mesmo material; suportada pelo padrão de nome com timestamp, não confirmada no Set.
- HIPÓTESE: playback de clipes sobrepostos na mesma track (RE201: 16 sobreposições) — o comportamento de mixagem interna é do Live, não dedutível do JSON.
- NÃO VERIFICADO: disponibilidade exata das operações LOM citadas na versão do Live em uso (`duplicate_clip_to_arrangement`, propriedades de clipe) — checar a doc do LOM instalada antes de implementar.
- Nenhum arquivo do Set de referência foi modificado.
