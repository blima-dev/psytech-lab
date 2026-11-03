# Jaytech's Panning Technique!

> id `OJ3Fxk4E0gU` · Sonic Academy · 7:03 (423 s) · tema `meio-espaco`
> Legenda automática EN obtida e lida (319 blocos de cue no arquivo; **139 linhas de texto úteis** após remover
> `WEBVTT`, tags `<c>`, marcações de tempo isoladas e duplicatas consecutivas) · `temLegenda=true`.
>
> **O que o vídeo é:** uma demonstração de **posicionamento estático de pan**, faixa por faixa, com um boost
> temporário de +6 dB para ouvir cada som. Não é aula de alargamento estéreo, não usa plugin de width, não mede
> correlação e não fala do vale de 300–4.000 Hz do contexto medido. Toda leitura de "quanto isso resolve um meio
> estreito" é do estudo, marcada `INFERÊNCIA`.

## Técnica ensinada (2-4 frases)

Jaytech trata o campo estéreo como um semicírculo de relógio — *"9:00 on the left-hand side and 3:00 on the
right-hand side"* (00:00:28.670–00:00:30.590) — com os elementos mais importantes apontando para o 12, o centro
(00:00:33.070–00:00:40.310). Ele percorre a mixagem som por som, colocando cada faixa *"under a microscope"*
(00:00:58.230) e varrendo o pan até achar o ponto do semicírculo onde aquele som *"shine[s] through without being
sort of over overtaken overlapped by some other kind of sound"* (00:00:47.110–00:00:56.270). Para ouvir a posição,
insere um Utility e sobe *"about 6 dB"* (00:01:29.710–00:01:31.790), dá *"a bit of a flick left and right"*
(00:01:42.550), escolhe o ponto e **tira o boost depois** (00:02:41.430–00:02:44.630). Kick, sub e caixa ficam sem
pan nenhum (00:01:01.830–00:01:09.270); a doutrina que ele atribui a Eric Prydz é manter *"all of the clubby stuff
all of the actual kind of music right in the mono"* e reservar o estéreo para *"ethereal trippy effects"*, echoes e
reverbs (00:02:11.190–00:02:22.790) — porque *"the tracks will translate well to a club system where everything is
mono"* (00:02:26.630–00:02:29.070).

## Ferramenta usada no vídeo (plugin/stock)

**Utility, device stock do Ableton Live.** É a única ferramenta nomeada no áudio — a legenda diz apenas *"utility"*, identificada como o device stock Utility do Live (`INFERÊNCIA`): *"So I I usually place a utility on a track. I turn it up by about 6 dB"* (00:01:29.710–00:01:31.790). O uso é de **ganho de escuta**, não de width: ele sobe ~6 dB
para o som saltar do resto da mixagem, varre o pan, escolhe o ponto e manda tirar o boost — *"Make sure you take that
off afterwards as well otherwise you'll have a part that's like sticking out uh pretty loud"*
(00:02:41.430–00:02:46.870).

O controle de pan em si **não é nomeado** na legenda. Os valores em que ele fecha — *"at 6 right"* (00:03:27.630),
*"at 16 L"* (00:04:38.080) e *"at 20 right"* (00:04:47.470) — leem-se como o mostrador L/R do pan do Live
(`INFERÊNCIA`), não como horas do relógio: no modelo dele o semicírculo vai de 9:00 a 3:00, então não existe
posição "6 horas".

A legenda **não nomeia** nenhum outro plugin, analisador, medidor de correlação ou ferramenta de width, e não
menciona ANA 2, VELA, SideKick, Kick 3 nem Bitwig — nada na técnica depende deles.

## Tradução para ambiente de trabalho comum

| Conceito do vídeo | Equivalente real | Observação |
|---|---|---|
| Utility com +6 dB temporário | **Utility (Live 12 nativo)** — Gain +6 dB, e voltar a 0 dB no fim | O próprio vídeo manda tirar (00:02:41.430–00:02:46.870). Alternativa: fader do canal +6 dB, com o custo de perder a referência de nível ao voltar |
| Varredura manual de pan | **Pan do canal (Live 12)** ou **Utility → Balance** | `AutoPan` **não** é equivalente: ele modula no tempo; o vídeo é posicionamento estático. Um estudo de mix do levantamento (17/10) já registrou que AutoPan não resolveu a largura (correlação 0,80 no set de referência) |
| Relógio 9–12–3 | Convenção mental, sem plugin | 12 = pan 0; 9:00 = L50; 3:00 = R50. Os pontos que ele cita (6R, 16L, 20R) são desvios pequenos, não extremos |
| Ouvir a faixa inteira enquanto ajusta | Não usar Solo; manter o canal tocando no contexto | 00:03:03.950–00:03:13.830. O +6 dB já é o "microscópio" |
| Duas passadas | Duas sessões de escuta | 00:03:36.710–00:03:46.630: uma para o layout geral, outra para apertar |
| Música no mono, efeitos no estéreo | Organização **por função**, não por plugin | 00:02:11.190–00:02:29.070 |
| Instrumentos (Serum 2, Diva, Vital, Massive X, Surge XT, Kontakt 8) | Entram como **fonte**: o que já entregam de imagem (pan por oscilador, unison spread, FX estéreo) | A técnica é de mixagem, não de sound design. Em Live, o Pan do canal é *balance*: em fonte estéreo ele atenua um lado, não rotaciona a imagem — por isso posicione fonte estreita/mono e deixe o estéreo real para as camas (estudo Synth e Atmos, 17/10) |
| Alargar / criar Side | **Não é o que o vídeo ensina** | Largura real vem de conteúdo Side acima de ~150–250 Hz, não de pan de material mono (estudo Synth e Atmos, 17/10: "conteúdo Side real em camas/tails, não pan extra") |

Nada aqui precisa de ANA 2, VELA, SideKick, Kick 3 nem Bitwig: o único device **nomeado** no vídeo é stock do Live. Serum 2, Diva, Vital, Massive X, Surge XT e Kontakt 8 não são necessários para executar a técnica; eles só determinam quão larga é a fonte que vai ser posicionada. O **GranularOsc do Serum 2** não tem papel aqui: a técnica não é de síntese. Se uma camada granular entrar no motor, ela entra como **fonte estéreo a ser posicionada** — e, pelo estudo de 17/10, granular é justamente uma das rotas boas para gerar Side real acima de 150–250 Hz, o que é outro trabalho (largura), não este (posição).

## Aplicação por função

Contexto de contraste citado no levantamento original: num set de referência medido, o meio **300–1.200 Hz em −4,83 dB** e o agudo-médio **1.200–4.000 Hz em −5,76 dB** contra a média de 6 referências; low-end mono; groove com subdivisões deslocadas do grid.

Duas consequências antes de qualquer coisa. **(1)** Pan **não adiciona energia em banda** — ele reduz sobreposição.
Então esta técnica não preenche o vale: ela *desmascara* o meio para que nível/EQ possam subir depois sem o mix
embolar. **(2)** Se a medição for em soma mono (Mid), afastar do centro o único elemento que carrega a banda
**piora o número**. Portanto: pane o segundo/terceiro portador da banda, mantenha o portador principal perto do
centro e re-meça depois. `INFERÊNCIA`.

| Função | O que o vídeo autoriza | Posição de partida (escala Live L50–R50, `HIPÓTESE`) | Cuidado |
|---|---|---|---|
| **Kick** | Não panear (00:01:03.630–00:01:06.430) | 0 (centro) | É a âncora do clube mono; qualquer pan come pressão |
| **Sub** | Não panear (00:01:06.430) | 0, com Bass Mono ≤120 Hz | Low-end mono é convenção do estilo. Pan aqui só cria cancelamento na soma |
| **Baixo/rolling** | Entra em *"clubby stuff … right in the mono"* (00:02:14.630) | 0 | O groove deslocado é deslocamento **temporal**; não converta em movimento estéreo nem em AutoPan |
| **Hats/shaker** | É o exemplo literal dele: closed hi-hat em *"6 right"* (00:03:27.630) | hat 4–8 R; shaker 8–12 R (mesmo lado, um pouco mais aberto — só separe para o outro lado se forem timbres/rítmicas claramente distintos) | Posição pequena. Nada de AutoPan no topo: modulação faz o 16º parecer instável e briga com o groove deslocado |
| **Percussão de resposta** | *"things like stacks … just move things around just a little bit"* (00:01:14.350–00:01:20.790) | 16–20 L, lado oposto às hats | Melhor candidata a sair do centro. Pan estático não muda o ataque: a resposta continua no seu lugar rítmico |
| **Madeira** | O exemplo dele é uma *"main chord line"* que fica enterrada no centro, passa bem em *"16 L"* e muito clara em *"20 right"* (00:04:29.630–00:04:49.430) | acorde principal 8–12 L; madeira-resposta 12–16 L | Não abrir demais: é uma das portadoras da identidade tonal — largura demais vira borrão de afinação |
| **Stab** | Mesma lógica, desde que não caia no mesmo ponto | 14–18 R, lado oposto da madeira | Se madeira e stab soam juntos em 300–1.200, é exatamente o par que o pan deve separar |
| **Subida** | *"saves the stereo field for … ethereal trippy effects"* (00:02:17.750–00:02:20.270) | livre; abrir só na metade de cima | Não alargue a parte baixa do sweep: engorda o sub e o build perde foco |
| **Atmosfera** | Mesma licença Prydz | estéreo real acima de ~150–250 Hz, não pan de mono | É aqui que o estéreo deve morar, não no motor |

### Ordem de operação

1. **Preparar o grave antes do pan:** Bass Mono ou HP em 120–150 Hz no material que vai sair do centro, para não
   levar low-end para o lado.
2. **Utility → Gain +6 dB** só para ouvir. Não deixe esse ganho entrar na decisão de nível.
3. **Tocar a música inteira, sem Solo**, e varrer o pan devagar — o hábito que ele descreve em
   00:03:03.950–00:03:13.830 é *"listening to everything but that sound"*.
4. **Parar no ponto onde o som tem espaço próprio** — não no ponto mais extremo.
5. **Voltar o Gain a 0 dB** (00:02:41.430–00:02:46.870).
6. **Segunda passada**, para apertar (00:03:36.710–00:03:46.630).
7. **Re-medir** 300–1.200 / 1.200–4.000 e a correlação **antes** de mexer em nível/EQ do meio. Se a banda caiu, o
   pan tirou energia do centro: devolva o portador principal ao centro.

### Checagem mono obrigatória

O argumento do vídeo é justamente tradução em clube mono (00:02:29.070). Some o master em mono e confirme que nada
posicionado **desaparece**; se desaparecer, havia cancelamento de fase, não posicionamento. Pan estático de fonte
mono não deve sumir — só reposicionar.

### Regras para não engordar o sub nem criar brilho metálico

1. **Nada abaixo de 120 Hz sai do centro** — Bass Mono/HP antes do pan. Pan de grave só cria cancelamento na soma
   (estudo Synth e Atmos, 17/10).
2. **Pan estático, nunca microdelay/Haas.** O vídeo posiciona só com pan, não com atraso; abrir com delay curto cria
   comb filtering e é exatamente a receita de brilho metálico (estudo Synth e Atmos).
3. **Não trocar a técnica por Utility Width nem AutoPan**: o estudo de 17/10 mediu que isso não cria Side real e a
   correlação continuou em 0,80 no set de referência.
4. **Posições pequenas**, como as dele (6R / 16L / 20R) e o aviso *"with a dance track you don't want to go too in
   too crazy"* (00:02:06.470–00:02:09.190).
5. **Hat brilhante não se conserta com pan** — só fica mais exposto. Mantenha a fonte escura.
6. **Se o elemento paneado é o único portador da banda que está baixa, não o afaste do centro.** Pane o vizinho que
   o está mascarando.

## Prioridade e esforço

**Prioridade: alta.** É o procedimento que torna executável a recomendação que um estudo de mix do levantamento
(17/10) já fez — redistribuir pans aglomerados (no set de referência, concentrados em `0.00`/`0.35R`). Custa um device
stock, é reversível e é pré-requisito para subir o meio sem máscara.

**Esforço: baixo.** Um Utility por canal, valores estáticos, sem automação, sem plugin novo. O custo real é
*escutar* duas vezes, não editar.

**Limite honesto:** o vídeo **não resolve** o vale de −4,83/−5,76 dB nem a correlação de 0,80 do set de referência. Ele não cria conteúdo
Side (o estudo de 17/10 é explícito: a ferramenta prioritária é Side real em camas/tails, "não pan extra"). Para uma escuta binaural 3D ele cobre **um eixo só — esquerda/direita**: não trata profundidade,
frente/trás nem altura. Serve como a passada de organização espacial que antecede o trabalho de banda e de Side.

## Trechos de prova (legenda literal, timestamps do VTT)

**1. O modelo do relógio e o objetivo do posicionamento (00:00:20.750–00:00:56.270):**

> Modelo do relógio (Jaytech/Sonic Academy): o campo estéreo é um semicírculo — 9:00 à esquerda, 3:00 à direita — e cada pista acha seu lugar para brilhar sem ser sobreposta — 00:00:20.750–00:00:56.270

**2. O que não se paneia (00:01:01.830–00:01:09.270):**

> O que não se paneia: kick, sub e provavelmente snare (Jaytech/Sonic Academy) — 00:01:01.830–00:01:09.270

**3. A doutrina Prydz: música no mono, estéreo para efeitos (00:02:11.190–00:02:29.070):**

> Doutrina Prydz (citada por Jaytech/Sonic Academy): a música "clubby" no mono, campo estéreo reservado a efeitos etéreos (echo, reverb) — é o que faz o mix traduzir em sistema de clube, mono — 00:02:11.190–00:02:29.070

---

**Referências consultadas (além da legenda):** estudos de mix e synth/atmos do levantamento original (17/10/2026) — correlação da banda média 0,80 no set de referência vs. referência 0,32–0,44, recomendação "Center: Kick, snare, bass…; 30-70% L/R: keys, percussion", ação de redistribuir pans, AutoPan não resolveu a largura, mono ≤120 Hz, microdelay gera comb filtering, gate de correlação 0,55–0,65 e "Side real em camas/tails, não pan extra". O contexto medido de 300–4.000 Hz e o groove deslocado vieram do briefing do levantamento original.
