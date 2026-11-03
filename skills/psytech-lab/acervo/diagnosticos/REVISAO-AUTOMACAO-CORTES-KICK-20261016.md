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
