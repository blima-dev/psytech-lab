# Akari System — análise técnica de produção (psytech)

**Faixas analisadas (arquivos locais, decodificação ffmpeg f32le / 22050 Hz / mono + numpy):**

1. `Akari System - Segments.mp3` — 339,4 s (5:39), ~320 kbps, 181 compassos
2. `Akari System - Slippery Slope (Luis M Re.mp3` — 420,0 s (7:00), ~320 kbps, 224 compassos

**Método:** FFT em blocos de 5 s para energia por banda (20–120 / 120–300 / 300–1k / 1–5k / 5–12k Hz); detector de onset por banda (flux positivo, threshold relativo 0.3, refratário 40–95 ms) sobre envelopes filtrados (kick 30–120 Hz, bass 120–300 Hz, glitch 1–8k Hz, hats 5–12k Hz); autocorrelação do envelope LF para BPM e fase; mudança espectral (distância entre vetores de banda normalizados, janela 1 s) para mapa de seções. Energias em dB por banda são uma escala relativa interna — no relatório uso deltas, que são comparáveis entre compassos.

**Nota de método:** a duração completa (339 s / 420 s) foi decodificada em vez de cortar em 300 s, para que a comparação "1ª vs 2ª metade" cubra a faixa inteira. Todos os demais parâmetros foram mantidos. Dados por compasso foram exportados em CSV (180 e 223 linhas).

---

## 0. Correção de BPM: as faixas estão a 128,00 BPM, não 132

A hipótese de trabalho (132 BPM, beat = 0,4545 s) foi **refutada pela medição**:

| Métrica | Segments | Slippery Slope |
|---|---|---|
| BPM medido (autocorr. envelope LF) | **128,00** (lag 468,7 ms) | **128,00** (lag 468,8 ms) |
| autocorr @ 128 BPM | **0,947** | **0,692** |
| autocorr @ 130 BPM | 0,451 | 0,512 |
| autocorr @ 132 BPM | **0,168** | **0,372** |
| autocorr no 16th (117,2 ms) | 0,457 | 0,218 |
| autocorr no compasso (4 beats) | 0,829 | 0,621 |

**VERIFICADO adicional:** com o grid de 128 BPM (beat = 0,4688 s; compasso = 1,875 s; 8 compassos = 15 s exatos), **todas as fronteiras de seção fortes caem em múltiplos de 8 compassos**: Segments em 30/60/90/120/149/165/180/240/300 s = compassos 16/32/48/64/80/88/96/128/160; Slippery em 30/105/141/171/188/217/276/291/319/351/409 s = compassos 16/56/76/92/101/116/124/148/156/171/188/219. A 132 BPM esse alinhamento se degradaria ~1 compasso a cada 4 (drift de ~0,6 s por minuto). Grade usada em todo o relatório: **1 beat = 0,4688 s; fase do grid: 0,100 s (Segments) / 0,110 s (Slippery)**.

---

## 1. Mapa temporal por compassos (beats @128 BPM)

Formas de onda medidas: kick = presença de onset 30–120 Hz em cada beat do grid (janela ±70 ms); bass = onsets 120–300 Hz por compasso; glitch = onsets 1–8k; hats = onsets 5–12k. Energias = dB relativo por banda.

### 1.1 Segments (181 compassos; compasso N começa em 0,100 + (N−1)×1,875 s)

| Compassos | Beats | t (s) | Kick | Bass rolling | Hats 5–12k | Glitch 1–8k | O que muda (medido) |
|---|---|---|---|---|---|---|---|
| 1–8 | 1–32 | 0,1–15,0 | 4/4 desde o beat 1 | 16–19/comp. | 26–33/comp. | 25–34/comp. | Abertura a frio: kick + rolling cheios no beat 1 (LF 54,5 dB), sem intro ambiente |
| 8 | 29–32 | 13,2–15,0 | 1111 | 16 | 28 | 27 | Corte parcial de graves: LF 54,5 → 39,2 (−15 dB), 1 compasso |
| 9–16 | 33–64 | 15,0–30,0 | 1111 | 19–20 | 29–32 | 28–32 | Seção A; no compasso 16 outro dip de graves (LF 41,1) com hats subindo 32 |
| 17–32 | 65–128 | 30,0–60,0 | 1111 | 19–20 | 27–43 (cresce) | 28–32 | Camadas agudas entram: 300–1k 32→37, 1–5k 26→28, 5–12k 22,3→24,4 |
| 33–48 | 129–192 | 60,0–90,0 | 1111 | 19–20 | 28–45 (cresce) | 28–32 | **Sweep de 15 compassos**: LF 42,8→26,7 (graves saem aos poucos) enquanto 1–5k sobe 29,8→32,4 (melodia/ácido cresce) |
| 48 | 189–192 | 89,1–90,9 | 1111 (ticks abafados) | 20 | 44 (máx.) | 4 indep. | **Corte total de graves 1 compasso**: LF −1,8 dB (−59), bass 120–300 cai 45→28; hats e glitch continuam no máximo |
| 49–63 | 193–252 | 90,9–117,5 | 1111 | 19–20 | 28–38 | 28–32 | **Drop**: LF volta a 57,2; seção mais brilhante que a 1ª (300–1k 36–39, 1–5k 29–31, 5–12k 24,8–26,7) |
| 63–64 | 249–256 | 117,5–120,0 | 1111 | 19 | 33→43 | 0→4 | Antecipação curta: 2 compassos de dip (LF 42,6, 36,7) + hats +10 |
| 65–79 | 257–316 | 120,9–148,1 | 1111 | 19–20 | 31–43 | 28–32 | Full-on; glitch sobe p/ 292–297 por 8 comp. |
| 80–88 | 317–352 | 148,4–165,0 | 1111 | 19–20 | 44→17 (sai) | 28→24 | **Seção escura**: 5–12k despencam 25→12,6 dB (hats filtrados para fora); compasso 88 = corte (LF 34,3) |
| 89–95 | 353–380 | 165,0–177,5 | 1111 | 19–20 | 39→19 | 32→25 | Volta com hats leves (h17–25); glitch burst g4 no compasso 89 |
| 96–111 | 381–444 | 179,1–208,3 | 1111 | 19–20 | 19–42 | 28–29 | Full-on; 2 dips de 1 compasso (96: LF 41,7; 111: 38,2) |
| 112–127 | 445–508 | 208,4–236,2 | 1111 até 119; **kick some 120–127** | 19–20 (nunca para) | 44–45 o tempo todo | 28–33 | **Breakdown principal**: 5–12k caem p/ 6,3–13,7 dB; 1–5k sobe a 30,1–33,6 (máx. da faixa = solo de mids); LF escorre 57,9→10,5 (beats 477–508) |
| 128 | 509–512 | 238,1–240,0 | **1110** (sem beat 4) | 20 | 37 | 1 | Último corte: LF 17,5 dB |
| 129–144 | 513–576 | 240,3–269,1 | 1111 | 19–20 | 36–45 | 30–40 | **Drop "seco"**: volta cheia (LF 57,4) mas com hats abafados (5–12k = 18,2 dB vs 26 antes), abrindo gradualmente até ~24–26 |
| 145–159 | 577–636 | 270,0–298,1 | 1111 | 19–20 | 31–44 | 30–40 | Pico de glitch da faixa: 310–318 onsets/8 compassos |
| 160 | 637–640 | 298,1–300,0 | **1100** (sem beats 3–4) | 19 | 42 | 5 | Corte de 2 beats antes da última seção |
| 161–176 | 641–704 | 300,0–330,0 | 1111 | 19–20 | 31–42 | 30–33 | Último bloco full-on |
| 177–181 | 705–724 | 330,9–339,4 | 1111 | 19–20 | 42→0 | 30→0 | **Outro em corte de graves**: LF 23,3 → −28 → −33,5; fade em ~3 compassos |

### 1.2 Slippery Slope (224 compassos; compasso N começa em 0,110 + (N−1)×1,875 s)

| Compassos | Beats | t (s) | Kick | Bass rolling | Hats 5–12k | Glitch 1–8k | O que muda (medido) |
|---|---|---|---|---|---|---|---|
| 1–16 | 1–64 | 0,1–30,0 | **abafado** (1111, mas LF 42–43 dB vs 55,8 do full) | 19–20 | **13 → 40** (build contínuo) | 31–40 | Intro de 16 compassos com rolling + percussão e kick filtrado; melodia sobe (1–5k 15,5→22,5) |
| 16 | 61–64 | 28,2–30,0 | **1110** (fill: cai beat 4) | 20 | 40 | 39 | Fill de fechamento da intro |
| 17 | 65 | 30,1 | 1111 | 19 | **32→22 (caem)** | 27 | **Drop de abertura**: LF 41,9→55,8 (+14 dB); detalhe: os hats da intro SAEM no drop (h40→22) |
| 18–52 | 69–208 | 31,9–97,0 | 1111 | 19–20 | 20–34 | 26–32 | Full-on estável (LF 60,1; 1–5k sobe 19,4→26,0 entre 20–25 s) |
| 53–56 | 209–224 | 98,9–104,9 | 1111 (abafado) | 19–20 | 34→41 | 28–41 | Antecipação: LF 55,8→27,9→7,9→6,9 (kick some em 4 compassos), hats sobem; 1 s de corte total em 100–101 s (LF 13,8) |
| 57–60 | 225–240 | 105,1–111,1 | 1111 | 19–20 | 42–44 (máx.) | 27–30 | Drop (LF 55,9) com hats no pico; fill 1110 no compasso 60 |
| 61–75 | 241–300 | 113,0–140,2 | 1111 | 19–20 | 24–41 | 27–32 | Full-on |
| 76 | 301–304 | 141,4–143,2 | **0111 — SEM beat 1** | 19 | 36 | 0 | **Corte de 1 beat no downbeat da fronteira**: LF 55,8→13,3; kick volta abafado nos beats 2–4 |
| 77–91 | 305–364 | 143,3–169,4 | 1111 | 19–20 | 30–45 | 27–41 | Nova seção; glitch burst g4 no compasso 77 |
| 92 | 365–368 | 171,4–173,2 | **0111 — SEM beat 1** | 20 | 43 | 0 | Mesmo dispositivo: LF 27,3, corte no beat 1 |
| 93–100 | 369–400 | 173,3–186,3 | 1111 | 19–20 | 44→20 (esfria) | 27–31 | Glitch burst g7 no compasso 93 (máx. da faixa) |
| 101–107 | 401–428 | 187,9–199,8 | 1111 (abafando) | 19–20 | 37→45 | 28–31 | Início do trecho longo de low-out: LF 39,9→6,5 |
| 105–115 | 417–460 | 194,5–214,3 | **kick-fantasma** (4/4 como tick, LF 5,6–12 dB, −45 a −50) | 19–20 (segue cheio, 120–300 ≈ 42–45) | 43–46 (máx.) | 28–33 | **Breakdown assinatura**: sub do kick fora, rolling continua, hats saturados; 300–1k sobe a 40,9–44,1 e 1–5k a 32,4 (solo de mids em 210–215 s) |
| 116 | 461–464 | 216,2–218,1 | 1111 | 20 | 41 | 0 | **Corte total**: LF −0,2 dB, bass 45→25,8 |
| 117–124 | 465–496 | 218,2–231,1 | 1111 | 19–20 | 38→19 (sai) | 27–30 | Drop: LF 55,8; hats saem logo após a entrada (h44→19) |
| 125–147 | 497–588 | 232,1–275,0 | 1111 | 19–20 | 19–43 | 26–32 | Full-on longo; glitch sobe (312–318/8 comp. nos compassos 105–112) |
| 148 | 589–592 | 275,0–276,9 | 1111 (abafado) | 19 | 37 | 3 | Corte de 1 compasso (LF 21,4) |
| 149–155 | 593–620 | 276,9–290,0 | 1111 (mais suave, LF 52,3, −8) | 19–20 | 26–42 | 26–34 | Variação de groove com kick um degrau abaixo |
| 156 | 621–624 | 290,0–291,9 | abafado | 20 | 28 | 2 | Corte de 1 compasso (LF 25,6) |
| 157–170 | 625–680 | 291,9–318,3 | 1111 | 19–20 | 25–46 (cresce) | 27–41 | Build de 14 compassos: hats 25→46, glitch g4 em 158 e 167 |
| 171 | 681–684 | 319,2–321,1 | **0111 — SEM beat 1** | 19 | 45 | 0 | Corte no downbeat (LF 16,5) |
| 172–179 | 685–716 | 321,1–334,4 | 1111 | 19–20 | 43–46 | 27–42 | Seção mais brilhante da faixa (300–1k 43,6–43,9; 1–5k 30,0–31,8); glitch burst g4 no compasso 172 |
| 180 | 717–720 | 334,4–336,3 | **1110** (fill) | 19 | 29 | 1 | Fill |
| 181–188 | 721–752 | 336,3–351,4 | 1111 | 19–20 | 26–38 | 26–32 | Transição |
| 188 | 749–752 | 351,4–353,2 | **0111 — SEM beat 1** | 19 | 38 | 3 | Corte no downbeat (LF 29,3) |
| 189–218 | 753–872 | 353,2–408,1 | 1111 | 19–20 | 20–41 | 26–32 | Seção final enxuta: 1–5k cai 25→19–21, 5–12k 20–21 (textura seca) |
| 219–223 | 873–892 | 409,0–420,0 | 1111 (abafado) | 18–20 | 37→0 | 30→0 | **Encerramento em corte**: LF 5,7 → −24,2 → −35,9 → −47,0; fade de 2 compassos |

**Resposta à hipótese "o kick corta o 1º tempo de compassos alternados": NÃO como padrão periódico.** Kick 4/4 em 178/180 compassos (Segments) e 216/223 (Slippery). Cortes de kick existem apenas como **evento de fronteira**, nunca alternados: beat 1 removido em 4 compassos de drop (Slippery 76, 92, 171, 188 — todos com mudança espectral tvd 0,88–0,91), e beats finais removidos como fill (Segments 128 e 160; Slippery 16, 60, 180). Nos breakdowns, o kick não some: vira um "tick" abafado mantendo o 4/4 (LF média −45 a −50 dB, ex.: Slippery compassos 105–115).

---

## 2. O padrão EXATO do bass rolling (120–300 Hz)

**VERIFICADO: rolling contínuo de semicolcheias (16ths), em todos os 16 slots do compasso, sem pausas em nenhuma das duas faixas.**

- Histograma de onsets de bass nos 16 slots do compasso (16ths), faixa inteira:
  - Segments: `[219, 232, 214, 202, 215, 201, 237, 173, 226, 243, 216, 232, 204, 216, 221, 220]` — todos os slots populados, variação ±15% em torno de ~215 (slot 7, o "a" do beat 2, é o único recesso: 173, −20%).
  - Slippery: `[275, 264, 264, 275, 273, 272, 260, 283, 265, 265, 280, 262, 275, 284, 253, 261]` — variação de apenas ±4% em torno de ~270: rolling perfeitamente plano, **sem acento de offbeat e sem esquema K‑B‑B‑B**.
- Inter-onset modal: 0,09–0,10 s (3019 ocorrências em Segments; 3799 em Slippery). O 16th real a 128 BPM é 117 ms; o excesso de pares a ~95 ms é o refratário do detector fatiando o ripple do envelope de cada nota (pitch do bass ~85–110 Hz) — a densidade real é de 1 nota por 16th, com 19–20 onsets detectados por compasso contra os 16 teóricos.
- **O rolling nunca para**: 0 compassos com bass ≤ 4 onsets nas duas faixas (contra 180/224 compassos analisados). Nem no breakdown (Slippery comp. 105–115: b19–20 com LF total em 6–12 dB), nem no corte total (Slippery comp. 116: b20 com bass a −19 dB = rolando abafado/filtrado), nem no fade final (Segments comp. 179–180: b20).
- Relação com o kick: não há permuta kick↔bass (estilo techno). Kick 4/4 e rolling 16ths **coexistem** o tempo todo; o arranjo dina apenas por filtros/volume (120–300 oscila só entre ~45–50 dB full e ~25–44 dB nas fronteiras), nunca por remoção de notas.
- 16ths de 117,2 ms confirmados no domínio da frequência: autocorrelação do envelope de bass @117 ms = 0,457 (Segments).

---

## 3. Como o Akari faz a ANTECIPAÇÃO antes dos drops

Três dispositivos recorrentes, sempre alinhados à grade de 8 compassos (15 s):

**A. Fade/sweep de graves + 1 compasso de corte total + drop (drops grandes, a cada 32–64 compassos)**
- Segments → drop no comp. 49 (beat 193, 90,9 s): LF desce gradualmente durante 15 compassos (42,8 → 26,7 dB nos comp. 33–47, sweep, não gate), o comp. 48 é corte quase total de graves (LF −1,8 dB, −59; bass 120–300 −17 dB) **com hats no máximo (h44) e glitch ativo**, e o comp. 49 volta a 57,2 dB.
- Slippery → drop no comp. 117 (beat 465, 218,2 s): 8 compassos de low-out (LF 39,9 → 5,6–11,9 nos comp. 101–115, com o kick reduzido a tick fantasma e o rolling tocando inteiro), 1 compasso de corte total (comp. 116: LF −0,2 dB, bass 45→25,8), drop no 117 (LF 55,8).
- Slippery → drop no comp. 57 (105,1 s): 4 compassos fora (LF 27,9→7,9→6,9→23,5), hats subindo 34→41, drop com h42–44.

**B. Corte de 1 beat no downbeat da fronteira (fronteiras de 8 compassos em Slippery)**
- Compasso de fronteira com beat 1 removido e kick abafado nos beats 2–4: comp. 76 (LF 13,3), 92 (27,3), 171 (16,5), 188 (29,3) — sempre −30 a −45 dB em relação ao full — com o novo material entrando cheio no compasso seguinte (LF 55,8–55,9) e **glitch burst imediato** (g4 no comp. 77, g7 no 93, g4 no 172).
- Variação de 2 beats: Segments comp. 160 perde os beats 3–4 (1100) antes da última seção.

**C. Antecipação por percussão/textura, sem tirar o grave (fronteiras suaves)**
- Os hats 5–12k **sempre aumentam** na aproximação: Segments h28→41→43→45 nos comp. 40–47; Slippery h25→46 nos comp. 157–170 (build de 14 compassos); intro da Slippery build de 16 compassos h13→40.
- Dips de 1–2 compassos de graves sem cortar o beat (Segments comp. 8: LF −15; comp. 16: −16; comp. 63–64: −15/−21) marcam fronteiras menores mantendo o groove.
- O que NÃO entra na antecipação: o bass rolling. Ele permanece 19–20 onsets/compasso em 100% dos compassos de antecipação — a tensão é feita filtrando (dreno de LF e de 5–12k), não removendo camadas.

Regra prática medida: **hats sobem primeiro (8–14 compassos antes), graves são drenados por sweep (4–15 compassos antes), corte total dura 1 compasso (às vezes só 1 beat), e o drop entra cheio no downbeat seguinte — frequentemente com uma camada a menos (hats), que reabre nos 8–16 compassos seguintes** (Segments pós-comp. 129: 5–12k = 18,2 dB por ~8 compassos, abrindo para 24–26; Slippery pós-comp. 117: h44→19).

---

## 4. ONDE o glitch aparece (1–8 kHz)

- **97% do conteúdo transiente 1–8k está travado no grid de 16ths do kick+bass**: em Segments, 6.457 onsets no total e apenas 199 "independentes" (sem kick nem bass em ±40 ms); em Slippery, 7.914 → 202. Taxa média ~4 onsets/beat = textura contínua em semicolcheias (o click/attack do rolling e do kick domina a banda média).
- **Glitch independente (fills, ruídos, cortes)**: ~1,1/compasso em Segments (199/180) e ~0,9/compasso em Slippery (202/223); em grupos de 8 compassos varia de 1 a 17, sem periodicidade — é ornamento, não loop.
- **Posição rítmica dos independentes**: caem nos 16ths fracos. Segments: picos nos slots 9 ("e" do beat 3: 34 ocorrências), 3 ("a" do beat 1: 23), 6–7 ("e"/"a" do beat 2: 19/20), zero no slot 14. Slippery: mais distribuído, pico no slot 11 ("e" do beat 3: 20). **Nunca se acumulam no downbeat** (slot 0: 15 e 8).
- **Bursts de entrada de seção**: 4–7 onsets independentes no compasso 1 da nova seção (Segments comp. 46/48: g4; comp. 89: g4; Slippery comp. 77: g4; 93: g7 — máximo da faixa; 172: g4), funcionando como "impact" do drop.
- **Densidade ao longo da faixa (onsets 1–8k por grupo de 8 compassos)**: Segments sobe de 220 (comp. 1–8) → 284–305 (miolo) → **311–318 no clímax pós-breakdown (comp. 129–152)** → 280 no fim. Slippery: 272–304 na abertura, vale de 220–251 (comp. 17–48), pico **318 (comp. 105–112, o breakdown)** e 312–313 nas seções 172–187, queda para 248–271 na reta final.
- Faixa de frequência: a "sujeira" hábil vive em 1–8k; os hats propriamente ditos (5–12k) têm acentos medidos nos 16ths "&" e "a" (Segments: slots 2, 7, 8, 10, 13 = 550–585; Slippery: cluster característico nos slots 5–6, o "e"/"a" do beat 2, com 786/748 ocorrências — quase o dobro dos demais).

---

## 5. O que MUDA entre a primeira e a segunda metade ("a história")

**Segments (metade = comp. ~90, 165–169 s) — arqueto "sobe, quebra, volta mais pesado":**
- 1ª metade: textura cresce em camadas — 300–1k de 32,3→39,6 dB, 1–5k de 26,0→31,5, 5–12k de 22,3→26,7 (blocos 5 s, 0→135 s); glitch/8 comp. de 220→298. O centro dramático é o sweep de 15 compassos drenando graves (60–90 s) com as melodias subindo em contraponto.
- 2ª metade: começa com a **seção escura** (comp. 80–88: 5–12k caem a 12,6 dB e 1–5k a 21,4 — hats e brilho removidos), passa pelo **breakdown de mids** (comp. 112–127: 1–5k atinge 33,6 dB, máximo da faixa, enquanto 5–12k caem a 6,3), e o drop do comp. 129 volta **intencionalmente incompleto** (hats abafados em 18,2 dB, reabrindo só a partir do comp. ~141). O clímax de densidade de glitch (311–318/8 comp.) vem depois do breakdown, não antes. Fim: corte de graves em 3 compassos (LF 23,3→−33,5).
- Constantes nas duas metades: kick 4/4 (exceto comp. 128/160), rolling 19–20/compasso em 100% dos compassos.

**Slippery Slope (metade = comp. ~112, 209–217 s) — arqueto "intro longa, dois drops, quebra central, reta final seca":**
- 1ª metade: intro de 16 compassos com kick abafado (LF 42–43 vs 55,8) e hats em build (13→40), drop que **tira** os hats (h40→22) em vez de acrescentar; dois cortes de downbeat (comp. 76, 92); hats oscilam 20–45 sem zona morta.
- 2ª metade: concentra o **breakdown assinatura de 16 compassos** (comp. 101–116): único trecho com 5–12k abaixo de 0 dB (−9,1 em 200–205 s), solo de mids (300–1k 44,1; 1–5k 32,4 — máximos da faixa) e kick-fantasma; depois disso a faixa muda de caráter: groove com kick um degrau abaixo (LF 52,3 nos comp. 149–155), dois cortes de downbeat (comp. 171, 188), pico de brilho nos comp. 172–179 (300–1k 43,6) e **reta final enxuta** (1–5k cai de ~25 para 19–21 dB; hats 20–27), encerrando em corte de 2 compassos (LF −47).
- Constantes: rolling 19–20/compasso em 224/224 compassos; kick 4/4 salvo os 7 compassos de evento.

**Em comum (assinatura Akari System medida):** graves e groove nunca param — a "história" é contada por **filtros e subtração de camadas agudas**, não por quebras de bateria; 97% do transitório médio é o próprio groove; os drops grandes são precedidos de dreno progressivo de LF (4–15 compassos) + 1 compasso de vácuo + reentrada cheia **sem uma camada** (hats), que reabre depois; e a densidade de glitch só atinge o máximo **depois** do maior breakdown.

---

## Síntese como "receita" (para reproduzir o estilo)

1. 128 BPM exatos, fraseado de 8/16 compassos (fronteiras sempre em múltiplos de 8).
2. Kick 4/4 ininterrupto + rolling bass em 16ths planos (sem acento) dos primeiros ao últimos segundos; tensão = filtro, não mudo.
3. Hats em 16ths com acentos em "&"/"a" (no Slippery, cluster no beat 2.5); densidade de hats é o termômetro da build (h13→46).
4. Drop grande = sweep de LF por 4–15 compassos + 1 compasso de vácuo (às vezes só o beat 1) + reentrada cheia sem hats, com glitch burst (4–7 hits) no compasso 1.
5. Glitch melódico independente em 16ths fracos ("e"/"a"), 1–2 por compasso, crescendo ao longo da faixa e explodindo após o breakdown.
6. Estrutura energética: 2ª metade mais densa que a 1ª (glitch +7 a +15%), com um breakdown de mids como clímax emocional e final enxuto/corte.

---

## Evidência e limitações

- VERIFICADO: todos os números acima saem da execução do script sobre os arquivos indicados (FFT/autocorrelação/onsets conforme método; exit code 0 nas duas execuções).
- INFERÊNCIA: identificação "kick abafado/tick fantasma" (máscara 1111 com LF −45 dB) e "rolling abafado" nos cortes — o detector vê onsets acima do piso com energia bandpass muito reduzida; a leitura como "filtro" (e não outra fonte) decorre da continuidade da máscara rítmica.
- NÃO VERIFICADO: afinação/tônica do rolling (requer análise de pitch além do escopo), identidade do remix "(Luis M Re…)" (nome truncado no arquivo), e percepção subjetiva de "drop" além dos critérios espectrais adotados.
- Limite conhecido: energias em dB por banda são relativas (média por bin), válidas para deltas dentro e entre compassos das mesmas faixas; onsets têm resolução limitada pelo refratário (95 ms no bass), o que fatia notas longas em 2 eventos — os histogramas por slot e as contagens por compasso absorvem esse viés de forma consistente entre as duas faixas.
