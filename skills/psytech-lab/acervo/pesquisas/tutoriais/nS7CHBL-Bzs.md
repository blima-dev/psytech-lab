# Fix Muddy Low-End with Auto Phase Alignment in SideKick

**Vídeo:** https://www.youtube.com/watch?v=nS7CHBL-Bzs · **Canal:** Sonic Academy
**Legenda:** automática em inglês, lida integralmente (6.804 linhas de VTT). Tem legenda.

> **Nota de ASR (inferência):** a legenda automática grafa "barrel" onde o contexto só faz sentido como *kick* (ex.: 00:10:54.240 "want to get rid of the barrel"; 00:17:08.779 "if you don't have a barrel in that section"). Cito literalmente e sinalizo `[ASR: kick]` quando necessário. Não é fala literal do vídeo, é leitura do contexto.

---

## Técnica ensinada

O vídeo ensina a usar a nova seção de *phase detection / phase alignment* do SideKick para comparar o baixo com o kick que chega pela entrada de sidechain, mostrar onde a fase está errada e alinhá-la — automaticamente ou girando a fase na mão (00:16:10.897 "So now Sonic Academy has added a phase detection and phase alignment tool here."; 00:17:50.540 "play the sound, turn on phase equalization, and click 'detect.' You will see that it will start to show where the problems are occurring."; 00:18:11.921 "you can do it manually now by just changing the phase."). O problema que isso resolve é que o ducking sozinho não basta: mesmo com o sidechain ligado o kick continua entrando na região em que o baixo soa (00:16:47.485 "you can see that there is some overlap, even though the sidechain is now enabled. Um, the drum still goes into those areas where the bass is also heard.") e, fora de fase, o baixo "desmonta" e chega a soar como outra nota (00:20:05.617 "they're completely out of phase now."; 00:20:08.676 "It even almost sounds like a completely different note because of the connection to the barrel."). O alvo do ajuste é o **ataque** do baixo (o "rich bit"), não a cauda (00:20:28.449 "the results are almost perfect for me. It's less of an issue in the tail end of the bass, but it seems to really hit that rich bit at the beginning..."; 00:18:32.955 "I don't really care about the tails if there's a little bit of phase shift there."). No modo automático o alinhamento é recalculado quando a nota/harmonia muda (00:19:30.880 "Now it will dynamically update the phase alignment.").

**O que o vídeo NÃO ensina:** não há EQ, não há correção de presença de médios, não há receita de arranjo. É uma demonstração do plugin (≈16:00–20:30 é o bloco de fase); o resto é overview de multibanda, mid/side, espectral e triggers.

---

## Ferramentas usadas no vídeo (plugin/stock)

- **SideKick (Sonic Academy)** — plugin (não stock). Demonstrado dentro do **Bitwig Studio** (00:07:50.638 "through the audio sidechain in Bitwig"; 00:09:29.435 "I have a note receiver set up here in Bitwig").
- Recursos mostrados, todos no próprio SideKick:
  - multibanda de **3 lanes** (00:00:54.087 "the multi-lane section is now not two-lane, but a full three-lane");
  - crossovers com opção **12 dB** ou **linear phase** (00:02:05.515; 00:02:08.723 "using 12 dB in most cases.");
  - **mid/side**: mutar só o meio, só os lados, ou misturar (00:10:46.881);
  - **spectral mode**: ducking espectral que remove só o que existe no kick (00:12:16.051; 00:13:08.592 "it only removes what is needed and nothing else.");
  - triggers **sync / audio / MIDI** (00:08:16.177; 00:09:28.191);
  - **phase detect + phase alignment** (o foco, 00:16:10.897).
- O conceito de fase é independente de DAW e de plugin; a detecção automática é exclusiva do SideKick.

---

## Como fazer sem o plugin (protocolo manual em qualquer DAW)

### O núcleo traduzível (o que o SideKick faz, em termos de áudio)

O SideKick precisa da entrada de sidechain mesmo em modo sync porque é dela que ele tira a informação de fase do kick e usa isso para equalizar o baixo (00:17:41.565 "it needs to get the phase information from your drum coming through the sidechain, and then it will use that to equalize your bass."). Traduzido (inferência): **é uma comparação de fase entre dois sinais de grave que somam em mono, seguida de uma rotação de fase do baixo.** O objetivo é fazer a fundamental do baixo e a do kick **somarem** em vez de se cancelarem parcialmente. Não é EQ, não é compressão e não adiciona nível — por isso não engorda o sub nem cria harmônicos (leitura técnica, não fala do vídeo).

Duas grandezas diferentes que o vídeo trata como uma só:

- **Polaridade (180°)** — barato e nativo: `Utility` do Live (ou inversão de fase de qualquer DAW) tem inversão de fase L/R (botões `Ph`). Resolve os casos de cancelamento total; não resolve os parciais.
- **Rotação de fase arbitrária (0–360°)** — é o que o plugin faz. Quando o baixo é **sintetizado**, a rotação pode ser feita na fonte, no próprio oscilador.

### Protocolo (Live 12 + Serum 2 / Operator como exemplo)

1. **Medir antes.** Solo kick + sub. `Spectrum` (stock) em 20–150 Hz. Calcular a fundamental da tônica do projeto — exemplo em C#: **C#1 = 34,65 Hz** (período 28,9 ms; 180° = 14,4 ms; 90° = 7,2 ms); **C#2 = 69,30 Hz** (período 14,4 ms; 180° = 7,2 ms; 90° = 3,6 ms). (Cálculo matemático; não vem do vídeo.)
2. **A/B de polaridade.** `Utility` no bus do sub/baixo, botões `Ph` L/R. Nivelar antes de comparar. Ficar com a versão em que a banda de 30–100 Hz lê mais alta e estável. É o equivalente nativo dos 180°.
3. **Fase inicial na fonte (o equivalente real da rotação).** No **Serum 2**, fixar o controle de fase inicial do oscilador (`Phase`, 0–360°) e o modo de retrigger, com `Rand` em zero, para que **toda nota comece na mesma fase**. No **Operator** (sub), oscilador sine com `Phase` fixa; conferir no patch que o retrigger (`Repeat`) reinicia a fase a cada nota. É o caminho prático para 90°/45° sem plugin.
   - **Nuance honesta:** em um oscilador **sine** (sub), girar a fase é rotação pura, sem mudar timbre. Em um baixo **multi-harmônico**, a fase inicial gira cada harmônico por n×, ou seja **muda a forma de onda e o ataque** — que é exatamente o "rich bit" que o vídeo quer alinhar (00:20:35.728 "rich bit at the beginning"). Pode ser o efeito desejado, mas é mudança de timbre, não só de fase: auditar o A/B inteiro, não só o grave.
4. **Checar nota a nota.** O vídeo mostra que trocar a harmonia muda o alinhamento (00:18:44.158 "what happens when you start changing keys? Because then your phase alignment starts to change."). Com 2–3 notas de vocabulário restrito, dá para checar cada uma. A alternativa nativa ao modo automático é **repetir o passo 2 para cada nota** e, se uma nota cancelar, mudar a fase inicial dela ou a oitava/voicing — nunca mexer no tempo.
5. **Afinação do kick.** O próprio autor diz que afinar o kick ajuda o alinhamento (00:18:36.738 "You'll probably find that everything is more in phase if you've also tuned the [ASR: kick]. I don't always do that."). Se a fundamental do kick não estiver na tônica, o alinhamento de fase contra um baixo afinado fica mal definido — isso é decisão de afinação, não de EQ.

### O que não dá para reproduzir sem o plugin (limite declarado)

- **Detecção automática de fase** (o "detect" do SideKick) não existe em stock. O substituto é o protocolo manual acima, repetido por nota.
- **Auto-update dinâmico** quando a harmonia muda (00:19:30.880) não tem equivalente nativo. Ou se checa manualmente, ou se automatiza a fase inicial do synth por nota (possível, mas frágil e trabalhoso).
- **Ducking espectral** (00:12:16.051; 00:13:08.592) não tem equivalente no Live stock. O mais próximo é **ducking multibanda**: Audio Effect Rack + EQ Eight dividindo bandas + um `Compressor` por banda com sidechain externa do kick. Isso reproduz *duckar só o grave e deixar o resto passar*, não *remover só as frequências presentes no kick*.
- **Mid/side** do SideKick (00:10:46.881) é reproduzível com rack/Utility — mas em projeto com **low-end mono** (prática adotada como referência abaixo do crossover), "mutar só o meio" = duckar o grave inteiro. O ganho de transparência que o vídeo descreve (00:11:35.975) só valeria para os harmônicos estéreo acima do crossover.
- **Delay como rotador de fase:** rejeitado quando o groove tem transientes deslocados. Um atraso de alguns ms no bus inteiro gira a fase da tônica, mas move o transiente e destrói a subdivisão deslocada. A correção tem que ser em fase na fonte, não em tempo no bus.

---

## Notas de aplicação (protocolo kick + sub + baixo)

1. **Kick sozinho**: medir a fundamental. Se não for a tônica, decidir afinação antes de qualquer fase.
2. **Kick + sub**: `Utility Ph` A/B; depois `Phase` do oscilador do sub (Operator/Serum) em passos de 45–90°, sempre nivelado. Critério: banda 30–100 Hz mais alta e **estável entre notas**, não mais alta num só hit.
3. **Kick + sub + baixo**: repetir por nota do baixo. Onde kick e baixo **coincidem** (o downbeat), é ali que a fase importa; onde o kick está ausente, não há problema de fase a resolver — o próprio autor prefere essa saída (00:17:05.375 "Um, what I would often do, depending on the circumstances, is just cut out the [ASR: kick], because if you don't have a [ASR: kick] in that section, you don't have a phase alignment problem."). Isso casa com projetos de **jogo de ausência de kick**.
4. **Não mover nada no tempo**: sem `Track Delay`, sem nudge de clipe/nota, sem delay no bus. O groove deslocado é intocável.
5. **Nivelar para baixo, não para cima**: se o alinhamento recuperar soma no grave, **reduzir** o low band do baixo/sub. Não levantar o kick nem o sub para "compensar".
6. **Reconferir com tudo ligado**: hats/shaker e percussão podem mascarar o cancelamento no solo.

### Por função

| Função | O que fazer | Onde / parâmetro | Cuidado |
|---|---|---|---|
| **Kick** | É a referência. Não processar para "corrigir fase". Se a cauda longa invade o baixo, encurtar a cauda ou cortar o kick onde o baixo sustenta. | Afinação do kick; duração da cauda | Não matar o punch — a pressão vem dele. |
| **Sub** | Maior beneficiário. Sine na tônica (ex.: C#1/C#2), fase fixa, mono. A/B de polaridade e depois `Phase`. | Operator: sine + `Phase` + `Repeat`; Serum 2: osc sub + `Phase`/`Rand=0`/retrigger; `Utility` `Ph`; `Bass Mono` ~100–120 Hz | Não boostar. Alinhamento pode **aumentar** o grave; compensar para baixo. |
| **Baixo / rolling** | Segundo maior beneficiário. Fase inicial fixa + retrigger para cada nota começar igual; checar nota a nota. | Serum 2 `Phase`/`Rand`/retrigger | Girar fase de baixo multi-harmônico muda o ataque/timbre. Auditar o A/B inteiro. Não usar Track Delay. |
| **Hats / shaker** | Nenhum alinhamento de fase. Só manter fora da soma de grave. | HPF 200–300 Hz | Se vazar em 100–300 Hz, atrapalha a leitura do A/B. |
| **Percussão de resposta** | Nenhum alinhamento. HPF para não entrar no low-end mono. | HPF 150–250 Hz | O papel dela é transiente/médio; não é para somar pressão. |
| **Madeira** | Nenhum alinhamento contra o kick **se** estiver filtrada. Se tiver corpo grave, entra no A/B. | HPF 150–200 Hz | Madeira com corpo em 150–300 Hz pode borrar a leitura; manter fora do mono. |
| **Stab** | Só entra no protocolo se tiver fundamental grave. Caso contrário, não. | HPF se for o caso | Stab com sub curto pode cancelar no downbeat. |
| **Subida** | Manter a varredura fora de 30–80 Hz no momento do drop; se houver camada de sub no riser, automatizar HPF/fade antes do kick entrar. | HPF automatizado / fade da camada sub | Um sweep grave cruzando o kick cria cancelamento momentâneo — soa como "buraco", não como riser. |
| **Atmosfera** | Nenhum alinhamento. HPF no retorno de reverb. | HPF 150–200 Hz no return | Reverb com grave suja a leitura e o mono. |

### Quando a técnica NÃO resolve (contexto do projeto de referência)

- Médios **300–1.200 Hz em −4,83 dB** e **1.200–4.000 Hz em −5,76 dB** contra a média de 6 referências: **este vídeo não trata disso**. Alinhamento de fase pode dar mais clareza no grave e, no máximo, revelar que o baixo estava cancelando; não preenche médio. Não usar a técnica como justificativa para exciter, saturação ou brilho — é o caminho para o "brilho metálico".
- **Low-end mono** (prática de referência para pressão de sub): o cancelamento é total, não parcial. É por isso que essa frente vale muito nesse caso — o erro de fase não tem para onde "escapar" no estéreo.
- **Groove deslocado**: preservado por construção, porque a correção é em fase na fonte e em polaridade, sem deslocar tempo.

---

## Prioridade e esforço

- **Prioridade: ALTA.** Em projeto que depende de pressão de sub em mono, erro de fase entre kick e baixo vira cancelamento audível e inconsistência de nível nota a nota — o sintoma exato que o vídeo descreve (00:20:05.617; 00:20:08.676). É barato de diagnosticar e não exige plugin novo.
- **Esforço: BAIXO–MÉDIO.** Baixo para o teste (Utility + Spectrum, 2–3 notas, ~15 min). Médio para tornar repetível: não há detecção automática, e cada nota/camada precisa de conferência nivelada; o A/B de fase inicial em baixo multi-harmônico também mexe no timbre e exige escuta completa, não só do grave.

---

## Trechos de prova

1. `00:16:10.897` — "So now Sonic Academy has added a phase detection and phase alignment tool here."
2. `00:17:41.565` — "it needs to get the phase information from your drum coming through the sidechain, and then it will use that to equalize your bass."
3. `00:20:28.449` — resultado "almost perfect": o efeito maior está no ataque do baixo, onde as fases de bateria e baixo precisam se alinhar (Sonic Academy).

*Citações literais da legenda automática (blocos rolantes reunidos; o texto aparece palavra por palavra nos blocos a partir do timestamp indicado).*
