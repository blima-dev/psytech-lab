# INTERAÇÃO KANUN × KICK × BAIXO — 24/10/2026

Status: **PESQUISA CONCLUÍDA** (a aplicação no projeto de origem está registrada à parte; aqui fica o estudo).

**Sintoma-tipo:** *"a melodia parece que navega sozinha, não segue a história da música, os drops não são aproveitados, ela não conversa com baixo e kick."*

---

## 1. Método

- **Referência:** stems Demucs do *Slippery Slope (Luis M Remix)* — `drums`, `bass`, `other` (44,1 kHz, estéreo, 420,05 s). 128 BPM; 1 compasso = 1,875 s; 16 avos = 0,1172 s.
- **Onsets:** kick = banda 40–120 Hz do stem drums; baixo = 40–250 Hz do stem bass; lead = 300–3.000 Hz do stem other. Grade de 16 avos alinhada ao compasso (bar 1 = 0,0 s; conferida com a quebra do compasso 53 = 97,5 s).
- **Faixa com o problema (kanun):** notas reais lidas do Set — kick, sub de fundamento, baixo médio, rolling, cama de sub, kanun, open hat, closed hat, perc, bongo — mesma grade.
- **Janelas de referência:** D1 = compassos 57–100 (105–187,5 s), breakdown 101–116 (187,5–217,5 s), D2 = 117–192 (217,5–360 s), outro 193–217 (360–406,9 s).
- **Limites:** o stem `other` mistura lead + pads; onset não separa timbre. A busca web não abriu nesta sessão — nenhuma fonte externa nova foi lida; a evidência é a medição + os estudos internos do projeto.

---

## 2. Evidência 1 — a gramática do lead da referência

| Métrica | D1 (comp 57–100) | D2 (comp 117–192) | Outro |
|---|---|---|---|
| Onsets do lead / compasso | 3,0 | 2,9 | 5,6 |
| Compassos com gesto | 82% | 82% | 92% |
| Posições de 16 avos mais usadas | **7 (18%)**, **13 (14%)**, 10 (9%), 0/8 (7%) | **13 (14%)**, **7 (11%)**, 10 (9%), 0 (9%) | 7 (20%), 13 (13%), 0/10 (12%) |
| Onsets em vazio do low end (sem onset de kick/baixo a ±70 ms) | **67%** | **69%** | 62% |
| Onsets 0–0,5 beat antes do próximo kick | **53%** | 41,5% | 53% |
| Gestos por compasso (máscaras) | quase sempre **1 nota** (7, 13, 10, 0) | idem | idem |
| Baixo: onsets / compasso | 2,9 | 2,4 | 5,0 |
| Kick | 4x4 (posições 0/4/8/12) | 4x4 | 4x4 |

**Leitura:** o lead da referência não é uma linha contínua. É **um gesto curto por compasso**, preferencialmente no **"a" do tempo 2 e do tempo 4** (posições 7 e 13 = 0,25 beat antes do próximo kick), e **67–69% das notas caem em lugares onde kick e baixo não atacam**. A conversa existe porque o lead **antecipa** o próximo tempo e **não dobra** o baixo.

---

## 3. Evidência 2 — o caso com o problema (faixa de referência com esse defeito)

| Seção | Kanun / beat (trecho ativo) | % notas no onset do baixo | % no kick | % em vazio | Posições do kanun |
|---|---|---|---|---|---|
| Drop 1 | 2,0 | **97%** | 48% | **3%** | 0/2/4/6/8/10/12/14 |
| Marcha (ativos) | 2,3 | 86% | 45% | 12% | 0/2/4/6… (+1/3/5… raros) |
| Breakbeat | 4,0 | 55% | 20% | 44% | **todos os 16** |
| Clímax | 3,4 | 78% | 29% | 18% | todos os 16 |
| Drop 2 | 2,25 | 88% | 44% | 8% | 0/2/4/6… |

**Densidade do low end no caso:**

| Camada | Notas / compasso (Drop 1 → Drop 2) | Duração mediana |
|---|---|---|
| Sub de fundamento | 4,4 → 3,8 | **0,8 beat** (cobre 80% de cada tempo) |
| Rolling | 7,5 → 8,0 | 0,16–0,22 beat |
| Baixo médio | 0 (Drop 1) → 12,3 (clímax) | 0,2 beat |
| Cama de sub | nota longa de 44–124 beats | — |

**Cobertura do low end (kick + sub + baixo) por 16 avos:**

- Drop 1: **100% em 15 das 16 posições** (94% na última).
- Marcha: 81–100%.
- Breakbeat: 71–100%.
- Clímax: 62–100%.
- Drop 2: 88–100%.

**Mapa de ocupação do compasso no Drop 1 (quem toca em cada 16 avos):**

| Posição | 0 | 1 | 2 | 3 | 4 | 5 | 6 | 7 | 8 | 9 | 10 | 11 | 12 | 13 | 14 | 15 |
|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|---|
| Kick | X |  |  |  | X |  |  |  | X |  |  |  | X |  |  |  |
| Sub | X | X | X | X | X | X | X | X | X | X | X | X | X | X | X | X |
| Rolling | X |  | X | X | X |  | X | X | X |  | X | X | X |  | X | X |
| OpenHat |  |  | X |  |  |  | X |  |  |  | X |  |  |  | X |  |
| Perc madeira |  |  |  | X |  |  | X | X |  |  | X | X |  |  | X |  |
| Bongo |  |  |  |  |  | X |  |  |  |  |  | X |  | X |  |  |
| ClosedHat | X | X | X | X | X | X | X | X | X | X | X | X | X | X | X | X |
| **Kanun atual** | X |  | X |  | X |  | X |  | X |  | X |  | X |  | X |  |

**Posições realmente livres:** **1 e 9** (o "e" do tempo 1 e do tempo 3), e mesmo assim com o ClosedHat de fundo. O "a" 7/13 da referência está ocupado por perc madeira e baixo (7) e bongo (13).

---

## 4. Diagnóstico

1. **O kanun dobra o baixo.** 86–97% das notas do kanun coincidem com um onset do baixo. Não é conversa: é a mesma linha uma oitava acima.
2. **Densidade 2,7–5,3× a referência.** Kanun 2–4 onsets/beat vs lead da referência 0,75–1,0. Sem pausa, a frase não tem onde respirar.
3. **Falta a antecipação.** A referência usa o "a" (7/13), 0,25 beat **antes** do próximo kick. O kanun usa o "&" (0,5 antes) ou o próprio tempo (1,0 antes) — chega cedo demais ou junto.
4. **O low end não cede.** Cobertura de 100% no Drop 1 e ~12 notas/compasso de baixo contra 2,9 da referência. Sem vazio, qualquer nota do kanun é mais uma camada em cima do muro.
5. **Falta dramaturgia por seção.** O kanun mantém a mesma densidade em todos os blocos. A referência é ~0,5 onset/compasso no breakdown e ~3 nos drops. O drop não é "aproveitado" porque o kanun continua falando por cima dele.

**Causa-raiz:** não é a escolha das notas; é **o bolso ocupado + a densidade**. A melodia não conversa porque não existe espaço para a resposta — e porque ela responde na mesma grade do baixo.

---

## 5. Regras de desenho para o solista dedilhado (proposta)

- **Densidade:** 0,5–1,0 onset/beat nos drops; 1,5–2,0 no intro (protagonista); 0,3–0,5 no breakdown.
- **Célula:** 1–2 notas staccato (0,2–0,35 beat) + 1–2 beats de silêncio. Nada de linha contínua.
- **Vocabulário rítmico disponível:** **0/4/8/12** (com o kick — declaração) e **1/9** (o "e" livre — resposta). O **7/13** (o "a" da referência) só entra quando o perc/baixo ceder esse bolso.
- **Frase:** chamada de 1 compasso + resposta de 1 compasso; ou 2 compassos ligados + 2 de silêncio.
- **Cascata descendente:** só a cada 8 compassos e no fim do breakdown.
- **Dramaturgia por seção:**
  - Intro: dedilhado, protagonista, 1 gesto/compasso.
  - Abertura: 2 gestos, oitava 5, chamada.
  - Suspensão: 1 cascata e silêncio.
  - **Drop 1: solista MUDO nos 8 primeiros compassos** (o drop aterrissa no kick+sub); depois 1 gesto a cada 2 compassos.
  - Marcha: 1 gesto/2 compassos, chamada no tempo 3 (posição 8) e resposta no "e" do tempo 4 (13).
  - Breakbeat: diálogo com o open hat (hat em 2/6/10/14; solista em 1/9), 1 gesto/compasso.
  - **Clímax: solista MUDO na primeira metade**; depois 1 gesto/2 compassos.
  - Breakdown: solo de notas longas (0,3–0,5/beat), cascata no fim.
  - **Drop 2: solista MUDO na primeira metade**; depois 1 gesto/compasso, oitava 5.
  - Outro: 1 nota/compasso, desconstruindo.

---

## 6. A/B proposto

**A — só o solista (mínimo, reversível):** nova partitura esparsa em 0/4/8/12 + 1/9, sem tocar nas outras pistas. Métricas de aceitação: ≤1 onset/beat, ≥50% em vazio do low end, ≤30% no onset do baixo, Drop 1 mudo nos 8 primeiros compassos.

**B — solista + bolso (se A ainda mascarar):** abrir o "a" (7/13) da referência com subtração:
- tirar a **perc madeira** de 7/11 nos compassos em que o solista responde (perc é madeira como o kanun — mascara timbre e ataque);
- **encurtar o sub de fundamento de 0,8 → 0,4 beat** (ou mutar o rolling em 1 compasso de cada 4), criando o vazio que a referência tem.

**Critério de escuta:** no Drop 1, o primeiro gesto depois do drop tem de ser ouvido como **resposta** ao kick, não como continuação do baixo. No breakdown, o solista tem de ser o único protagonista.

---

## 7. Fontes e limites

**Estudos do projeto de origem citados no corpo (conteúdo, sem caminho):**
- "kick solteiro na cabeça; baixo nos bolsos de contratempo; 1 gesto curto a cada 4 compassos; sem melodias de Goa" (DNA psytech/dark-prog).
- Dosagem de LF por seção; pausas grandes; corte fora do downbeat (estudo de artistas).
- Kanun e oud dialogam com o chimbal nos contratempos; breakdown como solo acústico (dossiê de partitura).

**Material de medição:** stems Demucs da referência + JSON de medição da interação (do projeto de origem).

**NÃO VERIFICADO:** fonte externa nova (web indisponível nesta sessão); separação fina lead/pads no stem `other`; duração real das notas da referência (só onsets).
