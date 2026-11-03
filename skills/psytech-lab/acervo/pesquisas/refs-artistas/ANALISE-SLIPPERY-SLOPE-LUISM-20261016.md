# ANÁLISE — `Slippery Slope (Luis M Remix)` · Akari System (16/10/2026)

> Fonte: master em MP3 322 kbps · 44,1 kHz estéreo · **7:00** (últimos ~7 s em silêncio).
> Método: ffmpeg para separar bandas + envelope/onset em Python (janela de 10 ms; blocos de 4 compassos).
> **LIMITE DECLARADO: não houve escuta** — tudo abaixo é medição, não parecer estético. As bandas são
> filtradas (lowpass 80 Hz / highpass 4 kHz) e "onset" aqui soma kick + baixo quando olha o grave.
> Escala dos números: `dBFS = valor − 90,3` (RMS de int16), arredondado.

## 1. Essência (medido)

- **127,6 BPM ≈ 128** (autocorrelação do envelope: lag de 0,47 s dominante) — o andamento típico do estilo.
- **Sub ausente na intro**: 0:00–0:30 com a banda ≤80 Hz a ~−27 dBFS (contra −11,5 dBFS na marcha) = **+14,4 dB de
  sub de uma vez** no primeiro drop.
- **Marchas com RMS −9 dBFS** (mix de peak time, alto) e o sub respondendo por metade da energia do corpo.
- **O topo (>4 kHz) nunca desliga**: entre −39 e −33 dBFS na marcha, e **é a única coisa que fica viva nos breaks**.
- O brilho **não é estado, é rampa**: na intro o topo sobe +8,4 dB em 22 s (2.º por cento em 4 blocos seguidos)
  antes de qualquer kick.

## 2. Mapa de seções (blocos de 4 compassos · compasso = 1,881 s)

| tempo | comp. | sub ≤80 | topo >4k | full | dens. | leitura |
|---|---|---|---|---|---|---|
| 0:00 | 1 | −27,5 | −48,2 | −17,4 | 2,1 | abertura só com ar/foley |
| 0:07 | 5 | −26,9 | −46,7 | −15,2 | 3,2 | tensão subindo |
| 0:15 | 9 | −26,9 | −43,1 | −15,0 | 2,7 | **rampa de topo** |
| 0:22 | 13 | −25,9 | −39,8 | −14,4 | 2,1 | pico do brilho pré-kick |
| **0:30** | **17** | **−11,5** | −47,6 | −9,2 | **6,0** | **DROP 1** (sub +14 dB, densidade ×3) |
| 0:37–1:30 | 21–49 | −11,5 | −46…−38 | −9,1 | 5–6,5 | marcha; topo enriquecendo devagar |
| 1:37 | 53 | **−31,9** | −36,5 | −17,9 | **0,3** | **BREAK 1** (sub fora, topo MAIOR que na marcha, quase zero transiente) |
| **1:45** | **57** | −11,7 | −46,4 | −9,5 | 6,0 | **DROP 2** |
| 1:52–3:00 | 61–97 | −11,4 | −39…−34 | −9,0 | 5–6,8 | marcha longa (topo no máximo do trecho) |
| 3:08 | 101 | **−32,7** | −35,6 | −16,9 | 1,9 | **BREAK 2** (entrando fundo) |
| 3:15–3:30 | 105–113 | −36 a −29 | −40…−33 | −16 a −15 | **0,0** | **O VÁCUO**: 15 s **sem nenhum transiente** — só textura/topo |
| 3:38 | 117 | −29,6 | −33,5 | −15,2 | 0,5 | rebuild (poucos eventos voltando) |
| **3:45** | **121** | −11,5 | −37,2 | −8,9 | 6,0 | **DROP 3** |
| 4:30–4:53 | 145–157 | −14,5 → −17,3 | −39…−36,8 | −12,4 → −13,7 | 4,4→3,9 | **meia-tensão**: sub cai ~6 dB e a densidade cai 25%, topo fica |
| **5:15** | **169** | **−17,4** | **−33,4** | −11,1 | 2,9 | **respiração com topo no máximo** (sub −6 dB, densidade 2,9) |
| 5:23–6:16 | 173–201 | −11,5 | −36…−41 | −8,9 | 6,2 | marcha final |
| 6:16–6:46 | 205–217 | −11,5 | −47…−47,6 | −9,1 | 5,4–6,2 | **outro: o TOPO sai primeiro**, o sub fica |
| 6:46 | 217 | −20,3 | −45,1 | −15,4 | 2,4 | último bloco |
| 6:53–7:00 | 221 | −85,8 | −73,6 | −51,6 | 0,0 | silêncio |

## 3. A BATERIA (o foco do estudo) — medido

1. **O corpo é um fluxo de 16 avos.** Nos trechos densos (3:00–4:00, 0:30–1:30) os onsets fortes caem a
   **0,11–0,13 s um do outro** — a semicolcheia a 127,6 BPM é 0,118 s → é **fluxo de 16 avos contínuo**, com
   densidade de **6,0–6,8 eventos/s** (8,5/s seria o 16 avos cheio; ~4,25/s seria só 8 avos).
2. **Onde o kick "não" toca:** há trechos em que o forte do grave fica **1 vez por compasso**, e não no
   4-no-chão — em trechos esparsos (0:30–1:30 e 5:00–6:00) o histograma de fase do grave dá ~**1 evento por
   compasso, no 1.º tempo**. (INFERÊNCIA: é o desenho "menos bateria" da referência.)
3. **A assinatura "1 … a":** nos trechos esparsos os onsets fortes se dividem em **dois polos — o 1.º tempo e o
   último 16 avo antes do próximo tempo** (contagem [39, 1, 0, 31] num dos trechos). Ou seja: peso na cabeça e
   um **pickup no fim do tempo**, quase nada no meio.
4. **Os breaks não são silêncio de bateria — são REMOÇÃO + TOPO.** No break 1 (1:37) a banda ≤80 Hz cai 20 dB
   mas o topo sobe **2,3 dB acima da marcha**; no vácuo de 3:15–3:30 a densidade é **0,0** (nenhum transiente) e o
   topo segue a −40…−33 dBFS. O contraste é orçado: **sub sai, ar fica**.
5. **O outro faz o inverso da intro:** o topo cai ~14 dB de 5:23 (207) a 6:31 (221) **enquanto o sub não se
   mexe** — a faixa "apaga a luz" antes de apagar o peso.
6. **Microtiming (medido, com ressalva):** desvio mediano dos eventos de topo em relação à grade de 16 avos ficou
   em **16–21 ms** — leitura de resolução grossa (envelope de 10 ms); **não** é swing nem "mpc feel".

## 4. Kick × baixo (o "grave violento" deles) — medido com ressalva

- A banda ≤80 Hz tem **eventos a cada ~0,20 s (1/8)** nos trechos densos = **o grave é um fluxo de 8 avos**, com a
  cabeça mais forte — kick e baixo **colados**, não kick isolado com baixo em cima. (Ressalva: nesta medição os dois
  somam na mesma banda.)
- A marcha fica com o sub **14,4 dB acima** do que a intro — o drop da referência é, antes de tudo, **entrada de
  sub**.
- Onde o kick "não" aparece, o grave continua (marcha com densidade 6/s e sub cheio) — quer dizer: **a
  continuidade do grave não depende do padrão de kick**.

## 5. O que ensina para um desenho minimal psytech (INFERÊNCIA — não é ordem)

- **A macro forma da referência tem 3 drops + 2 breaks + 1 vácuo real + 1 meia-tensão + respiração com topo**,
  nas barras **17 / 53 / 57 / 101 / 105-113 / 121 / 145-157 / 169** (127,6 BPM). Num cânon de 2 drops + breakdown
  longo, a diferença que salta: **eles picotam a tensão em blocos menores** (breaks curtos de 4-8 compassos e uma
  meia-tensão que só tira 6 dB de sub), em vez de um breakdown longo.
- **O brilho é rampa, não estado** (a intro sobe 8 dB de topo antes de existir kick) — coerente com a regra
  "topo é evento".
- **O vácuo de verdade existe e é curto** (15 s sem nenhum transiente) — coerente com a estética de menos bateria.
- **O outro apaga o topo primeiro, o sub depois** — ideia de desenho raramente explorada.
