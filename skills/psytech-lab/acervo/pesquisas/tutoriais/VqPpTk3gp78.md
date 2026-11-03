# Dissonance and Tension for hypnotic Techno Sequences - intervals & music theory

> id `VqPpTk3gp78` · canal **SINEE Global** · duração ≈18:23 (último cue 00:18:22.080).
> Legenda automática EN do vídeo obtida e lida (108.460 bytes; 657 cues). **temLegenda=true**.
> O vídeo é 100% MIDI/teoria: *"I'll be talking exclusively about the notes and the midi information that is generated"*
> (00:02:19.280–00:02:25.670). Tudo que não estiver ancorado em timestamp abaixo é tradução deste estudo, marcada
> `INFERÊNCIA` ou `HIPÓTESE`.
> **Ressalvas de legenda automática:** "trone" = **tritone**; "disent" = **dissonant**; "qu generator" = **chord
> generator**; "flat n"/"minor 9" = **♭9/9ª menor**; "nodes" = **notes**.

## Técnica ensinada (2-4 frases)

O vídeo parte de uma sequência de passos, randomiza as alturas (*"I'm just going to randomize the sequence here"*,
00:03:42.760), duplica o sequencer e desativa uma cópia para enxergar os pitches (*"you can just duplicate your
sequencer and deactivate to see where your pitches"*, 00:05:00.080–00:05:09.749) e comprime tudo numa oitava
(*"squeeze everything back into one octave because then if you have them much closer next to each other you can much
better see what is really going on"*, 00:05:12.960–00:05:30.600). Define como dissonâncias úteis a **2ª menor** (1
semitom), a **7ª maior** (11 semitons = 1 semitom abaixo) e o **trítono** (±6 semitons), *"the most dissonant of them
all because it doesn't really fit anywhere"* (00:03:16.560–00:03:39.400). Lê os intervalos como números (+9, +3, +6…),
constata que sem o "zero" não há centro tonal (*"we don't have the zero here"*, 00:05:41.680–00:05:48.639) e elege
como tônica a nota que mais aparece, porque *"we hear them the most often and we get primed on them"*
(00:06:37.350–00:06:52.240). Poda as 2ªs menores empilhadas — *"+3 +4 +5 and the plus six in there those are all uh
minor second steps and that is quite the recipe to become too disent"* (00:07:21.280–00:07:40.510) — e mantém a
tensão como **acento intencional**; opcionalmente soma um chord tool com **+5** (4ª justa, *"becomes invisible"*,
00:15:29.560–00:15:45.700) e **+6/+13** (trítono/9ª menor, 00:12:13.920–00:12:51.629).

## Ferramenta usada no vídeo (plugin/stock)

| Device / ferramenta | Papel no vídeo | Prova literal (timestamp) |
|---|---|---|
| **ML-185** (step sequencer) | Gera a sequência; os valores são **offsets em semitons** (+2, +3, +4, +5, +6, +9…), não graus de escala | *"we have our ml 185 sequencer"* (00:02:28.120–00:02:31.910); *"as you can see we have + 9 + 3 + 6 + 3 + 2 + 2 + 4 and plus five"* (00:05:30.960–00:05:39.199) |
| **Chord tool / chord generator** | Acrescenta **duas notas fixas acima de cada nota gerada**: +5 e +13 | *"I added a chord tool"* (00:02:31.920–00:02:36.190); *"this one adds two notes on top of every generated note and that is the plus five and the plus 13"* (00:12:13.920–00:12:25.230) |
| **Operator** | Fonte sonora "super basic"; o som não é o assunto | *"our sound is coming from operator which is a super basic sound"* (00:02:36.200–00:02:42.070) |
| **Filtro** (não nomeado) | Usado só como A/B: desligar para ouvir a tensão que o filtro estava mascarando | *"and I deactivate the filter see how much eriness and tension that brings in there"* (00:13:05.120–00:13:18.910) |

**Nenhum plugin de terceiros é citado.** Busca na legenda inteira por `ana 2`, `vela`, `sidekick`, `kick 3`,
`bitwig`, `serum`, `diva`, `vital`, `massive`, `surge`, `kontakt`, `ableton` e `max for live`: **0 ocorrências**.
As únicas ferramentas nomeadas são "ml 185", "chord tool", "operator" e "filter". O vídeo **não diz** Ableton nem
Max for Live; "Operator" é o instrumento stock do Live e "ML-185" é citado apenas como "ml 185 sequencer" — a
equivalência com M4L é `INFERÊNCIA`, não fala do vídeo.

## Tradução para um arsenal compatível: Serum 2 (GranularOsc nativo), Diva, Vital, Massive X, Surge XT, Kontakt 8 e Live 12 nativo — sem ANA 2, VELA, SideKick, Kick 3 ou Bitwig

A técnica é **puramente MIDI**: nenhum dos plugins acima aparece, e o próprio autor diz que falará
*"exclusively about the notes and the midi information"* (00:02:19.280–00:02:25.670). Portanto a tradução não é de
plugin, é de **roteamento de notas**.

| No vídeo | Equivalente | Observação |
|---|---|---|
| **ML-185** (step sequencer) | **Clipe MIDI de 16 passos** no Arrangement do Live 12, ou qualquer step sequencer; a sequência pode viver na pista de madeira ou de stab do material de referência | Os números do ML-185 são **semitons acima da nota-base**, não graus da escala. No material de referência a base é C# e o intervalo é escrito como offset (+0, +1, +3, +5, +7, +8, +10). Se a sequência precisar viajar dentro do preset, o **Arp do Serum 2 em modo Pattern** aceita `note_offset` por passo — mas o motor toca MIDI no Arrangement, então o clipe é a rota direta |
| **Chord tool** (+5/+13 fixos por nota) | **Chord** (efeito MIDI do Live 12): adiciona intervalos fixos acima de cada nota; alternativa é escrever as notas extras à mão no clipe | O chord tool do vídeo não é "scale-aware": ele soma o mesmo intervalo a **toda** nota. Em C# frígio isso gera notas fora da escala em vários passos (ver a aritmética abaixo) |
| **Operator** | **Serum 2, Diva, Vital, Massive X, Surge XT, Kontakt 8** (Rubber Bridge Guitar, LOOP GARDEN, Ethereal Earth, Vintage Organs) ou qualquer nativo do Live 12 | O som é "super basic" e não é o tema; o carrier natural no material de referência é **madeira/stab**, não um synth novo e brilhante |
| **Filtro** (A/B) | **Auto Filter**, **EQ Eight** ou o filtro do próprio synth | Não faz parte da composição; serve para ouvir o que a tensão faz sem o filtro mascarar |

### Receita operacional no Live 12 (a versão deste estudo)

1. Abrir um clipe MIDI de **16 passos** na pista que vai carregar a ideia (madeira ou stab), na tônica **C#** do material de referência.
2. Duplicar o clipe/canal e **desativar** a cópia para enxergar as alturas — o truque do vídeo
   (00:05:00.080–00:05:09.749).
3. Limitar a janela a **uma oitava** (C#3–C#4, dentro da direção do material: melodia em oitavas 3–4) — o mesmo gesto de
   "squeeze everything back into one octave" (00:05:12.960–00:05:20.309).
4. Escrever **2–3 notas** (direção estética do material de referência) usando a escala **C# frígio = {C#, D, E, F#, G#, A, B}**.
5. Listar os intervalos em semitons e identificar onde estão as 2ªs menores; **não empilhar** três passos
   consecutivos de semitom (o vídeo chama isso de *"the recipe to become too disent"*, 00:07:31.759).
6. Eleger **C# como centro tonal** repetindo-o nos passos fortes; se a sequência não tiver centro, criar um
   (00:06:37.350–00:06:52.240; 00:08:35.240–00:08:45.590).
7. Se quiser o chord layer, usar o **Chord** do Live com **+5** (recheio), e **+6/+13** só em passos escolhidos —
   nunca em todas as notas e nunca no grave.
8. Fazer A/B com a camada muda; conferir sub mono, correlação e o balanço 300–1.200/1.200–4.000 Hz antes de manter.

## Aplicação concreta em um motor minimal de 2 minutos: por função (kick, sub, baixo/rolling, hats/shaker, percussão de resposta, madeira, stab, subida, atmosfera)

**Contexto medido do set de referência:** o meio **300–1.200 Hz está −4,83 dB** e **1.200–4.000 Hz −5,76 dB** contra a
média de 6 referências externas; o low-end é **mono**; o groove usa subdivisões deslocadas **.27/.77** e
deve ser preservado. O vídeo não fala de mix, bateria nem grave — a aplicação abaixo é deste estudo, marcada como
`INFERÊNCIA`, e a regra de ouro é: **a técnica vive acima do baixo, no MIDI, sem tocar no groove**.

### A célula de tensão em C# frígio (aritmética de semitons)

C# frígio estrito = **C#, D, E, F#, G#, A, B**; um registro do material de referência inclui a cadência
**♭II (D maior) → C#m** no 4º compasso do ciclo.

| Intervalo do vídeo | Como aparece em C# frígio | Uso no material de referência |
|---|---|---|
| **2ª menor** (1 st) | **C#–D** (1–♭2) e **G#–A** (5–♭6) | É a tensão nativa do frígio; usar **uma** das duas por frase, não as duas juntas |
| **7ª maior** (11 st) | É a inversão da 2ª menor: **D→C#** e **A→G#** na oitava acima | Mesma dissonância da 2ª menor; não precisa de nota nova |
| **Trítono** (±6 st) | **D–G#** é o único trítono **dentro** da escala | Acento mais forte, sem sair do frígio |
| **+5** (4ª justa) | C#→F#, E→A, F#→B, G#→C#, A→D, B→E; **só D→G** cai fora | Recheio quase invisível, como o vídeo descreve (00:15:29.560–00:15:45.700) |
| **+6** (trítono fixo) | Fica **na escala só quando a base é D ou G#** (D–G#); nas outras bases gera nota cromática | Usar só nos passos com base D/G# se quiser frígio estrito |
| **+13** (9ª menor) | Fica **na escala só quando a base é C# ou G#** (C#→D, G#→A na oitava acima) | Tensão forte; nunca no grave |
| **+18/+19** (par mais agudo, 1 st entre si) | Equivale, na escala, a **G#–A** (não G–G#, que exigiria G natural) | O "acento mais alto" do vídeo (00:09:12.720–00:09:35.269) traduzido para o frígio |

> Aritmética de escala é `INFERÊNCIA` deste estudo; o vídeo só afirma que 2ª menor = 1 semitom, 7ª maior = 11 semitons e
> trítono = ±6 semitons (00:03:16.560–00:03:39.400).

**O vídeo aceita a atonalidade como sistema.** Ele observa que, uma vez em loop, a sequência passa a fazer sentido
*"no matter how dissonant once you follow their own logic"* (00:14:04.120–00:14:19.509), e que *"that sequence is your
key is your scale"* (00:14:41.320–00:14:44.870). No material de referência isso não revoga o frígio: a célula pode ser
tratada como um sistema próprio **dentro** de C# frígio; notas fora da escala continuam liberadas **em teste**, não
como nova tonalidade (direção provisória em vigor no material de origem).

### Por função

| Função | Usar a técnica? | Como aplicar | Cuidado |
|---|---|---|---|
| **Kick** | **Não** | O vídeo não trata de kick; deixar o kick atual intacto, sem retunar para "criar intervalo" | Nenhum chord tool, nenhuma 2ª menor no kick |
| **Sub** | **Não** | Manter um só **C#** (Operator + Saturator), mono, como está no motor de referência | 2ª menor em 30–70 Hz bate lento e pode cancelar na soma mono — `HIPÓTESE` acústica; o vídeo não fala de sub |
| **Baixo/rolling** | **Não como alvo** | Preservar as notas e o .27/.77; o baixo do motor usa 37/38/44/49/50 (C#, D, G#, C#, D), então a relação **C#–D já está no vocabulário do grave** | Não somar outra camada de semitom embaixo; o diagnóstico do motor manda "evitar nova sobreposição de semitom no grave". A técnica deve viver **acima de ~200 Hz** |
| **Hats/shaker** | **Não** | Manter como estão; o vídeo não ensina percussão | Nada de metal afinado nem sino; é a rota curta para o brilho metálico vetado |
| **Percussão de resposta** | **Extensão** | Célula de 2 notas na madeira/bongo: **C#–D** como pergunta e **D–G#** (trítono) como resposta, nos slots rítmicos já aprovados | Não criar ataques novos no .27/.77; manter curto e seco |
| **Madeira** | **Sim — carrier principal** | Afinar os tocos em **C#, D, G#, A**; usar **C#–D** ou **G#–A** (2ªs menores da escala) e reservar **D–G#** para o acento; corpo em 300–1.200 Hz | Sem topo metálico; o intervalo deve ser ouvido na fundamental, não num harmônico brilhante |
| **Stab** | **Sim — chord layer** | **+5** (F#) como recheio; **+6** (D–G# na escala, ou C#–G cromático) e **+13** (D) como tensão; aplicar só em passos selecionados | O chord tool fixo gera cromatismo em várias bases; em C# frígio, +6 só é seguro em D/G# e +13 só em C#/G# |
| **Subida** | **Não é o alvo** | O vídeo não ensina riser; se a subida carregar motivo, usar C# como centro e a célula, sem empilhar chord tool | O salto agudo no compasso 32 foi rejeitado no diagnóstico; não reintroduzi-lo via transpose |
| **Atmosfera** | **Secundário (extensão)** | O vídeo manda escolher notas de pad/acorde que caibam no sistema tonal da sequência (*"notes for a pad or quarts … fit into that tonal system"*, 00:15:06.800–00:15:15.320); um drone **C# + D** ou **G#–A** dá tensão sem brilho | Manter fora do sub; em fonte acústica, wet ≤25% ou paralelo (regra do dry no material de referência) |

### Onde no tempo (proposta, não fala do vídeo)

O diagnóstico do motor divide os 64 compassos em oito cenas. Uma progressão possível da célula, sem tocar no
groove:

- **0:15–0:30 (compassos 9–16):** a madeira apresenta **só C#–D**; sem chord layer. É a assinatura frígia.
- **0:30–0:45 (17–24):** a resposta acrescenta **G#–A** ou o trítono **D–G#**; manter **uma** dissonância por
  frase, como o vídeo faz ao "deixar as segundas e ir para o zero" (00:07:49.960–00:07:54.909).
- **1:30–1:45 (49–56):** o par agudo **G#–A** vira o acento principal — a tradução do par +18/+19 que está
  *"standing out the most"* no vídeo (00:09:12.720–00:09:35.269); em **1:45–2:00**, retirar uma das notas para resolver.

### Regras para não engordar o sub nem criar brilho metálico

1. **Nada de intervalo abaixo de ~200 Hz.** Kick e sub ficam intocados; o baixo mantém as notas atuais. A 2ª menor
   só entra em madeira/stab/percussão de resposta.
2. **High-pass suave (~180–200 Hz) em qualquer camada melódica nova** — o suficiente para não somar energia ao sub,
   preservando o corpo de 300–1.200 Hz (`HIPÓTESE` de ponto de partida; o vídeo não dá valores).
3. **+13 nunca em nota grave.** O chord layer de 9ª menor só em C#/G# na oitava 3–4; em base grave ele vira lama.
4. **Timbre de madeira, não de metal.** Nada de sino, prato afinado, exciter ou shelf de agudo; a tensão é de
   **intervalo**, não de brilho. O diagnóstico do motor registra a rejeição da serra metálica, e a direção estética
   do material pede timbres orgânicos de madeira.
5. **Não mexer em posição, duração ou velocity.** O vídeo é pitch-only (00:02:19.280–00:02:25.670); o groove .27/.77
   e as chamadas aprovadas permanecem.
6. **A/B obrigatório:** mutar a camada melódica e conferir se o sub, a soma mono e o balanço 300–1.200/1.200–4.000 Hz
   mudaram. Se a 2ª menor criar aspereza em 1.200–4.000 Hz, descer a oitava ou trocar o carrier — não abrir EQ de
   brilho para "compensar".

## Prioridade e esforço

**Prioridade: alta.** É a frente melodia da pesquisa e a técnica ataca exatamente a tensão harmônica dentro do
frígio: em vez de "escolher notas bonitas", o vídeo dá um **procedimento auditável** (randomizar → comprimir a uma
oitava → ler intervalos em semitons → podar 2ªs menores empilhadas → eleger centro tonal). Custa zero plugin novo,
não mexe no groove e pode preencher os dois vales medidos (300–1.200 e 1.200–4.000 Hz) com corpo de madeira/stab, sem
subir o sub nem o brilho.

**Esforço: baixo para implementar / médio para curar de ouvido.** A implementação é edição de MIDI num clipe de 16
passos; o tempo real é gasto no julgamento entre *"that's way too friendly"* (00:04:54.189) e *"the recipe to become
too disent"* (00:07:31.759) — o próprio vídeo passa a maior parte dos 18 minutos nesse vaivém. Riscos: excesso de
semitons empilhados, contaminação do grave se a célula descer para o baixo, e aspereza metálica se o carrier for
brilhante. Tudo reversível por mute/undo de MIDI.

## Trechos de prova: 3 citações literais da legenda com timestamp

**1. As três dissonâncias úteis: 2ª menor, 7ª maior e trítono (00:03:16.560–00:03:39.400):**

> 00:03:16.560 defined our most interesting dissonant
> 00:03:20.040 intervals to be uh the minor 2 which is
> 00:03:23.799 just one semitone also the major 7th
> 00:03:27.920 which is 11 semitones or one semitone
> 00:03:31.280 downwards and the other one is the trone
> 00:03:33.630 the most dissonant of them all because
> 00:03:35.640 it doesn't really fit anywhere and that
> 00:03:39.400 is all plus six or minus six semitone steps

*(“trone” = tritone na legenda automática.)*

**2. O centro tonal é a nota que mais aparece (00:06:37.350–00:06:52.240):**

> 00:06:37.350 what we have in here is a few notes
> 00:06:37.360 that happen more often and that plus
> 00:06:39.840 three or the plus two might become our
> 00:06:44.280 root note because we hear them the most
> 00:06:46.560 often and we get primed on

*(A frase continua em "them" no cue seguinte.)*

**3. Empilhar 2ªs menores é a receita para dissonância demais (00:07:21.280–00:07:40.510):**

> 00:07:21.280 because we had the plus three + 4 + 5
> 00:07:25.680 and the plus six in there those are all
> 00:07:28.560 uh minor second steps and that is quite
> 00:07:31.759 the recipe to become too disent in
> 00:07:34.840 somewhat

*(“disent” = dissonant na legenda automática.)*

## Fontes consultadas

- Material de referência (set de origem do pacote): tônica C# frígio, melodia de 2–3 notas em oitavas 3–4, low-end mono, regra do dry em fonte acústica; diagnóstico do motor de 26/10 (sub = Operator + Saturator, MIDI 25; baixo = notas 37/38/44/49/50; sub em .27 e baixo em .50/.77; preservar groove; salto agudo rejeitado; **300–1.200 Hz −4,83 dB; 1.200–4.000 Hz −5,76 dB**). Contexto de low-end mono e .27/.77: veio do diagnóstico, não medido de novo.
- Nenhum estudo específico sobre "intervalos dissonantes em techno hipnótico" acompanha este mapa; é a primeira extração desta técnica a partir deste vídeo.

## Limites e o que NÃO foi verificado

- **Nenhum render, escuta, A/B ou medição de áudio** foi feito no estudo. O mapa é leitura de legenda + tradução.
- **Nenhum set do Live foi aberto, salvo ou alterado**; nenhum plugin foi carregado ou testado.
- O vídeo **não dá** BPM, tonalidade, valores de EQ, cutoff, Q, níveis, duração de notas ou número de passos. Nenhum
  número foi inventado; onde se sugere valor, está marcado `HIPÓTESE`.
- O vídeo **não ensina** kick, sub, baixo, hats ou percussão; as linhas dessas funções são "não se aplica" ou
  extensão, não conteúdo do vídeo.
- A aritmética de C# frígio (+5/+6/+13 caindo dentro ou fora da escala) e o corte em ~200 Hz são `INFERÊNCIA`/
  `HIPÓTESE`, não afirmações do vídeo.
- A equivalência "chord tool" → **Chord** (MIDI effect do Live 12) é tradução, não nome dado no vídeo. O vídeo só diz
  "chord tool"/"chord generator".
- O vídeo não diz "Ableton" nem "Max for Live"; "Operator" e "ml 185" são os únicos nomes de dispositivo. A
  identificação de Operator como stock do Live é `INFERÊNCIA`.
- Não há legenda manual; a automática erra "trone" (tritone), "disent" (dissonant) e "qu generator" (chord
  generator). As citações acima preservam o erro literal.
