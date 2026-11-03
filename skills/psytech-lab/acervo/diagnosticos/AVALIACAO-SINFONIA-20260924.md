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
