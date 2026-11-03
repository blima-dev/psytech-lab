# OMAR MEHO — Music Production & Sound Design In Ableton Live (Udemy, 2022)

**Fonte:** curso em vídeo baixado do torrent `rutracker-6281778`, 10 capítulos + 1 workshop de 1 h.
**Material lido:** as **9 legendas `.vtt` recuperadas** (1 a 9) = **~39.100 palavras**, mais o **cheat sheet de 36 páginas** em PDF (§9), que é o material mais estruturado do pacote. Os capítulos 3, 7 e 9 têm 1,4–2,7 KB porque são demonstração de tela sem fala; **o conteúdo está nos capítulos 1, 2, 4, 5, 6 e 8 e no cheat sheet**.

**Formato:** não é aula expositiva. É **mentoria gravada** — Omar (produtor de tech house / label Atmospheric Temperature Records) ensinando um aluno ao vivo. Isso tem duas consequências: (a) as técnicas aparecem em ordem de uso real, com decisão e motivo; (b) a transcrição automática corrompe nomes (`Sarah`/`Sarum` = Serum, `Devah` = Diva, `Oprey`/`Prius` = Operator, `comedy`/`mide` = MIDI, `klap` = clap, `also filter` = Auto Filter, `spine`/`spam` = SPAN). Toda leitura abaixo já corrige o nome pelo contexto.

**Status:** `VERIFICADO` = está dito na transcrição e o contexto fecha. `INFERÊNCIA` = dedução do leitor. Nenhum áudio do curso foi renderizado.

---

## 1. A espinha: hierarquia de construção (cap. 5)

É a regra que organiza o resto do curso. Ordem **fixa**, justificada por ocupação do espectro:

1. **Kick** — "o elemento mais importante da track"
2. **Clap / snare**
3. **Hi-hats** (ritmo)
4. **Percussão**
5. **Bassline**
6. **Vocal**
7. **Efeitos** — "o último, porque é o que menos importa" (cap. 4)

Motivo declarado: preencher o espectro **de baixo para cima**, e **cortar o grave dos elementos que não são kick nem bass** (hats, claps, snares) para deixar o low end livre. Só depois disso o baixo entra, já encontrando espaço.

E: **"eu gosto de construir o drop primeiro"** — 16 compassos de drop, e só então sair preenchendo para os lados.

### 1.1 O kick tem três partes

`click` (o estalo de madeira) · `body` (o aspecto de grave) · `tail` (o release). É a decomposição que ele usa para escolher e para corrigir kick — o eixo clássico de diagnóstico de kick.

---

## 2. O mapa de mixdown (cap. 6) — o mais útil do curso

O cap. 6 é uma prancha só, com dois eixos: **X = pan** (esquerda ↔ mono/centro ↔ direita) e **Y = frequência** (grave embaixo, agudo em cima). A regra de cada elemento:

| Elemento | Pan | Frequência | Observação |
|---|---|---|---|
| **Kick** | **centro, mono** | grave | nunca stereo |
| **Bass** | **centro, mono** | grave, **abaixo** do kick | "se só sai no alto-falante esquerdo, quem está à direita do festival perde o baixo" |
| Percussão | split, pequeno L/R | acima do bass | |
| **Vocal** | centro | mids + agudos, faixa larga | |
| Piano | 25L/25R (ou 10–15 cada) | ~50 Hz + 200–250 Hz + 500 Hz–1,5 kHz | |
| Metais | alta, L/R | acima do piano | |
| **Strings** | **50L/50R, o mais aberto** | alta | o **mais baixo** de volume: "tickling the ears"; Auto Pan entrando e saindo |
| **Hi-hat** | 40–45 split L/R | **10–20 kHz** | mais central e mais alto que as strings |

Duas ideias que valem mais que a tabela:

1. **Volume é profundidade, não só nível.** "Se você abaixa o volume de uma track, ela passa a sentar *mais fundo* na mix; se abaixa o baixo, ele senta embaixo do kick; se abaixa o kick, ele fica embaixo do baixo." Ou seja: profundidade se faz com fader, não só com reverb.
2. **Mixar em mono.** Ele põe a Utility no master, faz o mixdown inteiro em mono e só então confere em estéreo. Razão: se o mix funciona somado, funciona em P.A. e em celular; se só funciona em estéreo, ele está se enganando.

E o master de export: **−6 dB** no master, com a Utility.

---

## 3. A receita de transição (cap. 2) — o capítulo mais longo

O aluno pergunta literalmente: *"eu só tiro a bateria por 2 compassos e volto com o baixo — é simples e não soa bem"*. A resposta ocupa a hora inteira.

### 3.1 O arco que ele usa

`Intro → build → BUILD UP → BRIDGE (2–4 compassos) → DROP → BREAKDOWN → OUTRO`

- **Bridge** = os 2–4 compassos imediatamente antes do drop. É onde a transição acontece de verdade.
- **Drop** = "a parte mais cheia, mais energética e mais alta; é a primeira vez que tudo entra em volume cheio".
- **Breakdown** = tirar a bassline + filtrar o vocal.
- **Outro = igual à intro**: cortar elementos, deixar kick + hats, fazer um **outro estendido** para o DJ conseguir filtrar e mixar a próxima.

### 3.2 Os elementos de bridge, na ordem em que ele monta

1. **Tirar kick, hats e clap** (o básico, que o aluno já fazia)
2. **Crash sample** com muito reverb + delay, **sidechain no kick**, em volume baixo — "creeping in", não em volume cheio
3. **Riser de ruído branco feito do zero**: Operator → oscilador em **Noise (white)** → filtro **band-pass com ressonância ~55** → **automatizar o sweep do filtro**; depois **Auto Pan** para mover L↔R, e reverb no fim. (Alternativa: qualquer sample de white noise + a mesma automação de filtro.)
4. **Top loop / hi-hats** como elemento rítmico da transição
5. **Beat Repeat** no vocal, picado, para "virar outra coisa"
6. **Reverse crash** e **reverse kick** imediatamente antes do drop, "para dar velocidade e ênfase"
7. **No drop**: crash com reverb + delay + sidechain no kick = peso; e um kick extra por baixo

### 3.3 As frases que são regra

- **"Sempre que você precisa anunciar alguma coisa, bota um crash ali."**
- **"Nine point nine times out of ten, sidechain o baixo no kick."** E sidechain **sutil** — não descer o threshold todo, senão você "mata" a bassline. A ordem de importância: bass ← kick é o nº 1; depois clap, crash, vocal, e até as strings são sidechained ao kick "só para criar espaço".
- **Auto Filter no lugar de gate.** Gate corta as bordas do som (encurta); Auto Filter corta frequências e a ressonância aquece. São coisas diferentes — ele usa gate quando quer encurtar, filtro quando quer escurecer.
- **Copiar e colar um filtro de outra pista traz a automação junto.** Atalho direto para replicar um sweep em várias pistas.
- **Warp markers + Consolidate** = time-stretch junglista: marcar transientes do vocal, arrastar, consolidar.
- **Nunca abrir em stereo o que tem que ficar mono.** "Não usaria em bass ou kick, porque eles precisam ficar mono. Mas tudo o resto — hats, vocal, crash — sim."
- **Efeitos crescem de volume ao longo do tempo**: "eu gosto que meus efeitos aumentem de volume, porque soa como se estivessem saltando pra fora".

---

## 4. Receitas de baixo (cap. 1 e cap. 2)

### 4.1 Recrear uma bassline de referência (cap. 1, Jay Lumen)

Sequência usada, na ordem:

1. **One-shot** de baixo parecido (não sintetizar do zero)
2. **Desenhar as notas** no piano roll — e o ponto central: **o que importa é o espaço entre as notas, não as notas**. Ele passa minutos ajustando o *spacing* até casar com a referência
3. **Oitava abaixo** se estiver agudo demais
4. **Auto Filter cortando o agudo** → "só o rumble de baixo"
5. **EQ** para o que sobra
6. **Sidechain no kick** ("shaping up to kick")
7. **Overdrive / Saturator** para recuperar o carácter que o processamento tirou — a frase dele: *"a parte chata é que quando você troca o sample, perde todo o som que você queria. É por isso que eu uso overdrive: você consegue a maior parte de volta."*
8. **Microscopic echo** (delay em ~1/16 com dry/wet 10–20%) — quase inaudível como eco, só "mantém o som acontecendo" e abre largura

### 4.2 Baixo que convive com vocal (cap. 2)

O problema: baixo de mid-range briga com vocal. As saídas dele, nesta ordem:

1. **Sub-bass** (frequência bem baixa) tocado ritmicamente — "o vocal ocupa o agudo, o sub ocupa o fundo, eles não competem". Reverter o sample para matar o clique.
2. **Acid bassline** — *"nine times out of ten, um acid bass senta bem com vocal"*
3. **EQ de separação**: cortar o agudo do baixo **e** cortar o grave do vocal. O corte do vocal é a parte mais agressiva: **cortar abaixo de ~500 Hz** "nove de dez vezes você pode cortar o grave do vocal e ele soa igual" — e libera kick + sub.
4. **Sidechain do vocal no kick**, sutil, "humanizado" — não robótico.

E uma regra de arranjo sobre camadas de baixo: **não sobrepor baixos.** "Quando você mixa baixos, é bom ter um baixo, um one-shot, e ir para outro em vez de deixá-los sobrepostos. Deixa a mix muito mais limpa e dá call-and-response."

---

## 5. "Full and rich sound" (cap. 4) — o capítulo mais solto

É sessão de escuta e conversa, mas saem técnicas concretas:

| Técnica | Detalhe |
|---|---|
| **Converter loop de bateria em MIDI** | botão direito no clipe → *Convert Drums to New MIDI Track*. "Não é 100% preciso" — ele costuma virar snare + hi-hat no lugar do kick; apagar os hits errados e remover o sample |
| **Matar clique de sample** | encurtar a seleção do clipe até o clique sumir. "Detalhe é tudo: garanta que não tem clique" |
| **Simpler > Sampler** | preferência declarada: "o Simpler estica o sample mais bonito e é mais amigável"; Sampler só quando precisa de mais controle |
| **Width ≠ volume** | "tem aumentar o volume e tem abrir a largura — são coisas diferentes"; Overdrive/Saturator é onde ele busca "girth" |
| **Delay microscópico** | 10–20% dry/wet num delay de 1/16 = largura sem bounce audível |
| **Resonator** | transforma o som em "piano" — automatizar o dry/wet; usar em kick para camada tonal |
| **Corpus** | "adiciona uma forma ao som", preenche as partes quietas da track |
| **Erosion** | joga ruído branco no kick e vira techno/warehouse |
| **Lo-fi hat** | cortar o agudo do hat = lo-fi na hora |
| **Testar se um loop cabe na track** | solar o loop junto com o **kick**, só os dois |
| **Agrupar vocais (Cmd+G)** e processar o grupo | "para dar cola, porque não são a mesma pessoa cantando" |
| **Vocais:** echo **50% ping-pong** + limiter em **−3 dB** | limiter não brickwall: "perde qualidade, fica óbvio" |

**Preferência de sintetizador (declarada, e polêmica):** ele prefere **Diva** a Serum — "mais grosso e mais quente, mais classe"; diz que os presets do Serum "têm muito movimento e não têm essa espessura", e que "muita gente acha que o Serum é a chave pra fazer música boa, e não podia estar mais longe". Serum para ele vale por **wavetable** e por aceitar qualquer sample arrastado. Tyrell N6 (u-he, grátis) é a alternativa que ele indica.

---

## 6. Build-up de bateria (cap. 8) — a receita mais concreta do curso

O drumroll dele (citando Sidney Charles):

- Kick em **1/4** → depois **1/8** → **8 kicks** nessa divisão → depois **1/16 por 4 compassos** → depois 1/32
- Como fazer: duplicar o clipe e usar o **÷2** ("half the time") para dobrar a velocidade a cada vez
- **Durante o build: volume DESCENDO e filtro fechando.** Isso é o truque declarado: *"o volume vai caindo, então dá a ilusão de que o drop é mais alto, e o filtro tira o mid pra deixar mais quieto"*
- **Gap antes do drop** (silêncio curto) e volta — "mini edit"

É a mecânica de contraste que produz o "drop soa maior" sem aumentar o master.

### 6.1 Fechamento e export (cap. 8)

- **Freeze (azul) → Flatten** = MIDI vira áudio. Ele faz isso no final para "poder enviar o projeto".
- **Exportar com os echos e efeitos desligados.**
- **Ouvir em outros lugares**: carro, chuveiro, fone, e voltar depois com ouvido fresco. "Cada vez que você ouve de novo, escuta coisa diferente."
- **SPAN** (Voxengo, grátis) como analisador — ele não usa o Spectrum nativo: "o SPAN é maior e eu vejo como eu quero ver".
- Master: limiter/compressor + saturação + stereo width.
- "Não existe track perfeita. Faz o seu melhor e vai para a próxima."

---

## 7. O que NÃO se aplica

- **Datado (2022, Live 10/11).** Vários recursos citados como novidade ("o 11 vai ter probabilidade e escalas") já existem no Live 12.
- **Muito papo de plugin pirata** — cap. 2 e 4 têm trechos longos sobre cracks, licença do Serum e ruído branco de demo do Tantra. Zero valor técnico.
- **A maior parte do cap. 4 é conversa**, não aula: sample packs, site de acapella, Spotify, carreira. As técnicas úteis estão isoladas na tabela da §5.
- **Ele trabalha muito em Ableton Standard** — metade das soluções dele é "não tenho esse device, uso outro". Quem usa Suite não precisa de várias dessas gambiarras.

---

## 8. Cruzamento ilustrativo com um set de referência psytech

Isto é `INFERÊNCIA`, ligando a transcrição às medições de um set de referência psytech (medições da mesma data).

| Regra do curso | No set de referência psytech (medido) | Leitura |
|---|---|---|
| **Não sobrepor baixos** (um one-shot por vez, call-and-response) | patches de bass do set de referência têm **3 camadas / 5 FX / 8 rotas de modulação / release 0,20 s**; o pack de referência tem **2 / 2 / 3 / 0,076 s** | a bass do set de referência é construída como *lead* do pack — e o low-mid medido (13,7% vs 9,4% da mediana) é o sintoma esperado de camadas sobrepostas |
| **Cortar grave de hats/claps/snares** para liberar o low end | low-mid 120–400 Hz do set de referência está **+4,3 pontos** acima da mediana de 15 referências | mesma região, mesma causa provável |
| **Mixar em mono** e só depois abrir | o grave do set de referência já é **9 dB mais mono** que a mediana — esse item já está resolvido | não mexer |
| **Bridge de 2–4 compassos antes do drop**, com crash/riser/reverse | a escuta de referência apontou "transições sem conexão" | é exatamente a peça que o curso formaliza |
| **Build com volume descendo + filtro fechando** | — (não medido) | teste barato: A/B num build existente |
| **Strings no extremo, 50L/50R, mais baixas de volume** | air 6–16 kHz do set de referência = **0,5%** vs 1,6% da mediana; nenhuma pista de bateria com reverb | o curso explica *onde* esse ar deveria vir (strings/crash em largura) |
| **Crash sempre que precisa anunciar algo** | nenhuma pista de bateria com reverb no set de referência | o "anúncio" está faltando na fonte mais óbvia |

**O que aplicar primeiro, na ordem de menor risco:**

1. **Build-up com volume descendo + filtro fechando** (só automação — reversível, não muda timbre)
2. **Bridge de 2–4 compassos** com crash + reverse antes do drop principal
3. **Reduzir a bass de 3 camadas para 2** e comparar o low-mid por medição, não de ouvido
4. **Cortar 180–350 Hz** só nos elementos que não são kick nem bass

Nada disso foi aplicado no set de referência. Tudo isso mexe na música e exige decisão estética.

---

## 9. O cheat sheet de 36 páginas — o melhor documento do pacote

`9 - Music-Workflow-Academy-Music-Production-Cheat-Sheet-Omar-Meho.pdf` (2,25 MB, 36 páginas, texto extraível). É um **manual de produção escrito**, não transcrição de conversa: 12 seções com regras numeradas. As principais:

### 9.1 Bassline — as cinco formas

Regras gerais, literais: *"bass é tipicamente um synth pluck com um sub por baixo"* · *"padrão curto, **não deve passar de 2 compassos**"* · *"**não faça camadas demais** — só acrescente um sub se não houver grave suficiente"* · *"se for fazer sub, **sempre senoide**, porque você quer o sinal mais limpo"* · *"**deixe um tempo do compasso para respirar**"* · *"notas de orientação"* (curtas, para ligar uma nota longa a outra).

| Estilo | Definição |
|---|---|
| **Rolling** | notas rolam para cima e para baixo umas em direção às outras (E→G→B→G→E) |
| **Single** | uma nota só — típico de house |
| **Jumping** | notas saltam de oitava (E4→E5) |
| **Techno/Bigroom** | nota fundamental tocando **o compasso inteiro, em todos os tempos** |
| **Techno/Bigroom, variação "psystyle"** | **deixar o primeiro passo vazio** e colar a bassline nos outros passos do compasso |
| **Pedal note** | uma nota no compasso inteiro |

A última linha é o desenho psystyle do motor de grave: **kick no 1, bass nos contratempos, primeiro passo vazio.**

### 9.2 Arranjo — pontos de nota e transições

**Pontos de nota:** a cada **4 ou 8 compassos**, um som **curto** que "tira o ouvinte da track por um instante e quebra a repetição". O mais comum é **crash**, mas serve clap, instrumento ou efeito curto. "Pode usar o mesmo ponto de nota a track inteira."

**Transições** — a lista canônica, em ordem de simplicidade:

1. **Tirar algo antes de entrar algo novo** — "a transição mais fácil que existe"
2. **Drum fill** (pode ser feito à mão com um sample de snare) + remover outros elementos
3. **Vocal shout / frase / loop** antes do drop
4. **Transição instrumental por "upbeat"**: a melodia da seção seguinte começa **antes** dela — se a primeira nota é F, põe um C antes, subindo para o F
5. **Silêncio**: apagar tudo um compasso antes do drop; **dois compassos** para mais impacto
6. **Um reverb/clap/snare grande na frente do drop** (o bigroom fazia com snare invertida)
7. **Som de efeito** (o telefone tocando é o exemplo dele)
8. **"A transição mais profissional é a combinação de todas essas."**

**Elementos de preenchimento:**
- **Drop blaster** — som gigante no início do drop, alto, "ótimo em tech house e techno"
- **Drop tone** — uma nota pedal em cima da ideia principal, aguda, **suave**, tipo pad/strings
- **Synth extra** — padrão curto de **1 tempo**, copiado pela track
- **Synth filler** — arpejo atrás, mais baixo que o elemento principal
- **Reverb swell automatizado**: sobe o swell, **corta o grave enquanto o swell cresce**, silêncio, e corta tudo antes do drop

**Elemento motor:** "deve haver sempre **uma** coisa em que o ouvinte foca"; escolha **um** instrumento para conduzir e **centralize todo o resto em volta dele**; se um padrão é complexo, **todos os outros ficam simples**.

### 9.3 Mixagem — cruzada com os números do set de referência

| Regra do cheat sheet | Número medido no set de referência |
|---|---|
| **"Mud zone" do kick: 100–200 Hz** — é onde o kick fica lamacento, "puxe sutilmente para fora" | o set de referência concentra cortes de EQ em **100–250 Hz (51 bandas)** — já em prática |
| **"Screech zone": 5–10 kHz** — cortar | não medido |
| **Kick:** achar o ataque/click e **dar um boost sutil** para punch | já em prática (boosts 1,5–4 kHz dominam) |
| **Hats:** remover o grave | — |
| **"Só use reverb curto na bateria"**; reverb longo é "ar", curto é "espaço" | nenhuma pista de bateria com reverb no set de referência |
| **Não aplicar reverb nem delay no kick/bass/graves** | respeitado no set de referência |
| **Manter todos os elementos no mesmo espaço** | — |
| **Não panar kick, bass, graves nem o vocal principal** | o grave do set de referência já é 9 dB mais mono que a mediana |
| **Haas: duplicar + atrasar <40 ms** · **Microshifting: duplicar + ±30 cents** | não usado |
| **Slapback: 160 ms, feedback ~12%, stereo** — bom em vocal | — |
| **Compressão de bass: ratio 6–10**, release baixo para punch | — |
| **Cola de bus: ratio ≤3,5**, ataque e release altos, agulha gentil | referência medida: Glue em paralelo 4,8–7,9% wet (master do pack Tim Engelhardt) |
| **Não comprimir sample de bateria já comprimido** (checar se bate 0 no meter) | — |
| **"Em EDM quase não há dinâmica; compressor não é obrigatório"** | anti-dogma útil |
| **Método de EQ:** boost estreito no máximo, varrer achando o ruim, cortar; depois segunda EQ com notch largo achando o bom, boostar | é o método clássico de varredura (sweep) |
| **Zona de presença 1,5k–5k** = onde o ouvido é mais sensível; **não boostar tudo ali** | o set de referência concentra boosts em 600 Hz–4 kHz |

---

## 10. Tabela de provas

| Afirmação | Alvo | Como foi verificado | Saída |
|---|---|---|---|
| Curso tem 9 VTT + 1 workshop | torrent | `find -iname "*.vtt"` | 9 arquivos, cap. 10 sem legenda |
| 7 capítulos transcritos lidos | a pasta das transcrições | contagem de palavras das transcrições | 68.052 + 113.091 + 1.847 + 53.937 + 10.799 + 9.729 + 54.554 B; 38.700 palavras |
| Cada VTT mora em 1 peça de 2 MB | `.torrent` (bencode) | mapa offset→piece | VTT 1=peça 0 · 2=519 · 3=1233 · 4=1244 · 7=1680 · 9=2301 |
| Download completo tinha só 15% das peças | `.aria2` bitfield | parse do bitfield | `397 / 2660` peças |
| Hierarquia de 7 elementos | cap. 5 | leitura integral | "kick, clap, high hat, percussion, bassline, vocal, effects" |
| Mapa de mixdown | cap. 6 | leitura integral | kick+bass mono/centro; strings 50L/50R mais baixas; hat 10–20 kHz 40–45 |
| Build 1/4→1/8→8 kicks→1/16 4 compassos | cap. 8 | leitura integral | "goes on for about eight kick drums... then 16. For like four bars" |
