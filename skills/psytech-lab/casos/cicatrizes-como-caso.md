# Casos medidos — quando algo "não sai", "mudou sozinho" ou "o número não bate"

v0.1.0 · 03/11/2026

> **O que é:** casos reais que já custaram horas de diagnóstico em projetos de produção eletrônica, reescritos
> de forma genérica. Para cada caso: **sintoma → causa medida → correção que funcionou**. Nenhuma correção
> aqui é dogma — são saídas que resolveram casos concretos, com a medida que provou a causa.
> **Quando abrir:** um elemento some ou "não sai"; o timbre muda sozinho; um número briga com o ouvido; o
> groove soa afobado, reto ou fora; o grave embola; o drop não chega; o solo desaparece no registro; e antes
> de dissecar timbre por horas.
> **Como usar:** ache a família pelo sintoma, rode o check da causa medida, só então mexa. Se a causa não
> aparecer em 5 minutos, pare e meça o alvo diretamente. Se a mesma correção falhar duas vezes, a premissa
> está errada — não a dose.

## 1. O check de 60 segundos

Quando um elemento "sumiu", "não sai" ou "está estranho", nesta ordem — sem pular:

1. **Alvo.** Canal + compasso + janela (min:seg). Feito quando você consegue escrever "canal X, compassos A–B, 1:30–1:45".
2. **Existência.** Mute do grupo → mute do canal → mute do clipe → janela do clipe (marcador inicial, fim,
   loop) → pico do arquivo de áudio. Feito quando o primeiro elo quebrado tem nome e número.
3. **Sinal.** Device ligado e último device da cadeia → fonte do sidechain tem sinal → fader × automação de
   volume → botão de saída/monitoramento. Feito quando o medidor do canal reage ao solo.
4. **Número.** Render atual (data/hash), clipe que realmente toca, nota isolada, banda onde o elemento vive,
   unidade certa. Feito quando um controle proposital muda o número.
5. **Mudança.** Uma alteração pequena e reversível, backup antes, leitura de volta depois. Feito quando a
   leitura de volta mostra o valor novo, com o antes/depois lado a lado.

## 2. Padrões recorrentes (observação, não lei)

Quase todos os casos abaixo caem em uma de três falhas:

- **(a)** o estado real não era o que o documento, o nome ou o mapa dizia;
- **(b)** o número era de outro objeto, outra janela ou outra unidade;
- **(c)** a correção atacou a camada errada (fader onde o problema era papel, EQ onde era oitava, nota onde
  era clipe sobreposto).

## 3. Família 1 — Silêncio e sinal: "não sai", "sumiu", "está mudo"

**Caso 1 — Todas as capturas de teste saíram a −44 dBFS; só o canal do kick sozinho passava.**
Causa medida: um grupo pai estava mudo e silencia os filhos mesmo com todos os filhos desmutados; a lista de
canais não mostra o mute do grupo.
Correção que funcionou: antes da primeira captura, varrer os grupos pai por mute.

**Caso 2 — Solo num canal específico e não sai som nenhum.**
Causa medida: o grupo pai estava mudo; o solo do filho não derruba o mute do pai.
Correção que funcionou: desmutar o grupo.

**Caso 3 — "Nada está mudo" e "o grupo está mudo" no mesmo projeto; um mapa automático concluiu que o canal
"não pergunta para ninguém" e a investigação virou horas de trabalho perdido.**
Causa medida: o sinalizador de saída de áudio no arquivo do projeto estava sendo lido ao contrário — o valor
lido como "desligado" significa ligado (confirmado em 186 projetos); o mute de clipe é um campo diferente do
mute do canal; e a automação de volume vence o mute manual.
Correção que funcionou: ler o campo certo (provar o sentido com um canal de estado conhecido) e fazer um solo
de 30 s no canal acusado antes de qualquer reparo.

**Caso 4 — Canal com notas armazenadas e silêncio total na janela esperada.**
Causa medida: notas fora da janela de reprodução — o marcador inicial do clipe jogava a primeira nota para um
compasso distante; o fim do clipe e o loop recortavam o resto.
Correção que funcionou: recalcular a janela (início absoluto, fim, loop) e comparar a primeira nota absoluta.

**Caso 5 — "O instrumento não tem partitura": 52 clipes lidos como vazios foram apagados.**
Causa medida: a rotina de leitura usava um argumento de intervalo de notas zerado, que devolve lista vazia
sempre, sem erro.
Correção que funcionou: ler um clipe sabidamente cheio como controle antes de apagar qualquer coisa em massa.

**Caso 6 — Um instrumento melódico com zero notas em dezenas de compassos.**
Causa medida: 14 dos 22 clipes estavam mudos no próprio clipe; o canal tinha mute desligado, volume e devices ok.
Correção que funcionou: checar o mute por clipe antes de acusar o canal.

**Caso 7 — Dezenas de clipes "funcionalmente vazios" (~8% do total).**
Causa medida: a janela de reprodução atravessava só ~3% da frase; as notas existem, mas fora do que o cursor
percorre.
Correção que funcionou: comparar a duração do loop com a janela antes de chamar um clipe de fragmento.

**Caso 8 — Um canal de textura sem som nenhum em 32 clipes.**
Causa medida: os 32 clipes apontavam para WAVs de silêncio digital — fatias cortadas do início de stems cuja
cabeça é silêncio.
Correção que funcionou: medir o pico do arquivo de cada clipe, não confiar no clipe existir.

**Caso 9 — "Arrasto" atribuído a 12 duckings aparentemente armados; nenhum comprimia.**
Causa medida: o instrumento que gatilhava os sidechains estava sem sample carregado — gatilho decorativo.
Correção que funcionou: solo + medir o pico do canal do gatilho antes de auditar qualquer ducking.

**Caso 10 — O kick sumiu ao "desbloquear" um plugin.**
Causa medida: duas instâncias de um plugin de ducking em série, sem entrada de sidechain e com mix em 100%,
silenciavam tudo (uma senoide a −12 dBFS saía como silêncio).
Correção que funcionou: ler o último device da cadeia antes de culpar o sample.

**Caso 11 — O projeto inteiro mudo.**
Causa medida: automação de volume do master travada em −70 dB desde o início da timeline.
Correção que funcionou: ler o volume do master no início da timeline antes de procurar por canal.

**Caso 12 — O export saiu com 92 bytes; "o som não sai" em dezenas de tentativas; toda auditoria virou
análise de arquivo.**
Causa medida: o motor de áudio estava sem device de saída selecionado; nenhuma A/B podia ser ouvida.
Correção que funcionou: confirmar device de saída + medidor de atividade antes de abrir qualquer auditoria.

**Caso 13 — "Toda medição de melodia mede outro canal."**
Causa medida: o filtro passa-baixa do lead estava travado perto de 20 Hz por 8 eventos de automação; a medição
capturava outra pista por onde o teste passava.
Correção que funcionou: solo do canal e medir a banda alvo (ex.: 2–6 kHz) antes de escrever sobre melodia.

## 4. Família 2 — Preset, timbre e clipe: "mudou sozinho", "voltou", "está metálico"

**Caso 14 — O preset volta ao de fábrica a cada play; "toda vez dá esse bug".**
Causa medida: um mecanismo de integração re-disparava o program change na abertura e sobrescrevia o estado
salvo do device.
Correção que funcionou: procurar a flag de re-disparo e desligá-la nos canais que não usam program change;
só depois investigar o arquivo do preset.

**Caso 15 — Carregar preset por índice carrega outro patch.**
Causa medida: o índice é alfabético a partir de zero na pasta, e a lista fica congelada na instância — renomear
arquivo não entra.
Correção que funcionou: abrir o preset pelo nome na interface antes de mapear qualquer índice.

**Caso 16 — Edição offline do patch "voltou pro anterior" e perdeu ajustes.**
Causa medida: a injeção substituía blocos inteiros de estado do device e apagava os ajustes finos (o bloco
caiu de 3.520 para 2.984 caracteres).
Correção que funcionou: comparar hash/tamanho do estado antes e depois de injetar; injetar só o delta, não o
bloco inteiro.

**Caso 17 — Preset editado perde wavetable customizada e unison.**
Causa medida: a ferramenta de edição substituía o slot do oscilador inteiro, e o unison não era aplicado.
Correção que funcionou: salvar o slot antes de editar e conferir o estado final por leitura de volta.

**Caso 18 — Ajuste recém-feito sumiu ao fechar o programa.**
Causa medida: um device adicionado na sessão existia só na memória (não salvo há horas) e a opção "não salvar"
foi escolhida sem olhar.
Correção que funcionou: inventariar o que existe só na sessão antes de dispensar o diálogo de salvar.

**Caso 19 — Nomes mentem em três frentes: um preset nomeado com a tônica não estava nela (mediu 56/112 Hz);
um preset chamado "suspiro vocal" tinha 96,8% da energia abaixo de 150 Hz; um instrumento acústico tocava com
preset de baixo.**
Causa medida: o nome não comprova o conteúdo.
Correção que funcionou: medir pitch, energia e sample antes de catalogar ou confiar no nome.

**Caso 20 — Um impacto "metálico e só, sem corpo", mesmo trocando de sample várias vezes.**
Causa medida: preset desenhado para durar 8 compassos, disparado por notas de 1–3,5 beats — sobra só o ataque.
Correção que funcionou: comparar a duração que o preset pede com a duração das notas do clipe.

**Caso 21 — Impacto estridente, "cheio de harmônicos".**
Causa medida: a fábrica de harmônicos era o saturador, não o EQ.
Correção que funcionou: A/B do saturador antes de mexer no EQ.

**Caso 22 — Voz soando "nasal" em todo o trecho.**
Causa medida: EQ copiado de outro canal com realces pesados (+10,8 dB @194 Hz e +9,05 dB @37,5 Hz) — curva
herdada de um timbre de corda grave.
Correção que funcionou: comparar a curva do EQ com a do canal de origem ao copiar cadeias.

**Caso 23 — "Notas rápidas" aparecendo num solo.**
Causa medida: 6 cópias do mesmo solo, defasadas de ¼ a 1 tempo, tocando juntas; cada nota vira 4–6 ataques.
Correção que funcionou: agrupar clipes por nome + conteúdo de notas e examinar starts e sobreposição.

**Caso 24 — Lead "dobra" depois de reescrever clipes (469 + 187 notas duplicadas).**
Causa medida: criar clipe MIDI sobre zona ocupada trima o clipe existente, e os fragmentos mantêm todas as
notas.
Correção que funcionou: deletar por posição de início em toda a zona antes de criar; conferir contagem de
notas depois.

**Caso 25 — Milhares de notas apagadas (1.849) com o log dizendo só "ERRO".**
Causa medida: remoção e adição de notas no mesmo bloco de tratamento de erro: a remoção rodou, a adição
estourou, o clipe ficou vazio.
Correção que funcionou: construir todas as especificações antes de mutar; usar operação de modificação atômica
quando existir.

**Caso 26 — Um instrumento "morre, perde a força e volta" ao longo da frase.**
Causa medida: 11 clipes sobrepostos reiniciando o mesmo ostinato em pontos próximos da timeline.
Correção que funcionou: contar os reinícios do padrão antes de acusar timbre ou nível.

## 5. Família 3 — Medição e grade: "o número não bate com o ouvido"

**Caso 27 — Captura ao vivo diz −19,3 dBFS; o export diz −6,1.**
Causa medida: captura ao vivo não é evidência de mix — o sinal e o momento não são os do arquivo final.
Correção que funcionou: medir só o arquivo exportado.

**Caso 28 — Alvo de "+8 a +12 dB no drop" que não existia; plano substituído em menos de 1 hora.**
Causa medida: o render de referência era anterior ao save que todos liam, e três valores diferentes foram
medidos para "o drop".
Correção que funcionou: congelar um render com hash e comparar a data de modificação com a do arquivo do
projeto.

**Caso 29 — Um verificador automático reprova uma barra inteira e outro parâmetro fica "folgado" com +58 dB
de diferença.**
Causa medida: mediu-se a barra inteira, não a sub-janela declarada; o salto vinha de outra seção esvaziada de
propósito.
Correção que funcionou: medir exatamente a janela declarada, contra o piso declarado.

**Caso 30 — "Grave demais" onde o sub mediu −68,8 dB.**
Causa medida: filtro de baixa ordem rotulado "20–120 Hz" deixa saia até ~300 Hz e infla +17,3 dB na faixa onde
o grave é vazio.
Correção que funcionou: filtro de ordem alta ou medir sub-bandas separadas (20–60 e 60–120 Hz).

**Caso 31 — Um release medido em 250 ms quando a nota isolada sobe em 30–60 ms; cinco documentos carregaram
o número errado.**
Causa medida: a medição somou 3 semicolcheias emendadas em vez de medir a nota isolada.
Correção que funcionou: medir 1 nota isolada e tratar o encavalamento entre notas à parte.

**Caso 32 — Alarme de "densidade 15,42/s contra teto 6,99"; 33 rodadas de investigação.**
Causa medida: note-ons MIDI comparados com transientes de áudio; 2.028 notas armazenadas contadas como ataques.
Correção que funcionou: nomear a métrica (MIDI × ataque × transiente) antes de comparar com qualquer teto.

**Caso 33 — "202 s de som dentro de uma janela de 165 s."**
Causa medida: beats comparados com segundos.
Correção que funcionou: mesma unidade nos dois lados (beats ÷ BPM × 60 = segundos).

**Caso 34 — Inventário de clipes fechava em 81 quando deveria dar 83.**
Causa medida: agregação por nome; dois canais com o mesmo nome (índices diferentes).
Correção que funcionou: agregar por índice/ID do canal, nunca por nome.

**Caso 35 — Um ranking de afinação "aprovava" uma voz fora de escala; ranking inteiro invalidado.**
Causa medida: estimador de pitch com resolução de ~5,4 Hz e fundamental fora do alcance; uma senoide grave de
altura conhecida devolvia outra nota.
Correção que funcionou: validar o medidor com uma senoide de altura conhecida antes de confiar nele.

**Caso 36 — Um A/B concluiu que "nosso topo é mais aberto"; conclusão falsa.**
Causa medida: um arquivo foi reduzido a mono (+3,01 dB no downmix) e comparado com média calculada no outro.
Correção que funcionou: mesmo carregador/caminho de decodificação nos dois arquivos.

**Caso 37 — Veredito de sentimento sobre duas faixas saiu fusionado numa análise só.**
Causa medida: os dois áudios foram enviados numa chamada única; a emenda foi tratada como fim de faixa.
Correção que funcionou: 1 faixa por chamada, com marca explícita de início e fim.

**Caso 38 — Um modelo de escuta "ouviu riser" onde a envoltória cai 41 dB; 3 escutas invalidadas.**
Causa medida: confabulação do modelo + viés de posição (escolhia sempre a 2ª opção).
Correção que funcionou: controle cego (trecho que só decai) e inversão da ordem das opções.

**Caso 39 — "Nada começa no tempo 1, tudo cortado"; 2 dias de trabalho parado tratando como timbre.**
Causa medida: o projeto inteiro estava +0,727 beat fora do grid (335,9 ms de vácuo antes do tempo 1).
Correção que funcionou: comparar a primeira nota absoluta do primeiro clipe com 0.0.

**Caso 40 — "O swing ficou horrível" depois de uma reescrita.**
Causa medida: o motor da sessão estava deslocado +0,363 beat e o shaker foi escrito na grade inteira.
Correção que funcionou: ler o offset dos clipes da bateria antes de escrever nota nova.

**Caso 41 — Um elemento "não está com a mesma partitura" do restante.**
Causa medida: o kick muda de fase por seção (0 / 0,47 / 0,1 do beat) e o novo elemento foi escrito numa grade
única.
Correção que funcionou: derivar as posições das notas reais de cada seção, não de uma grade teórica.

**Caso 42 — "O sub chega 150 ms atrasado."**
Causa medida: 886 notas colocadas em cruzamentos de semicolcheia (x,5 = 58,6 ms rígidos) + ataque do patch.
Correção que funcionou: medir offset e desvio-padrão das notas antes de acusar o envelope.

**Caso 43 — Groove "afobado/atropelando"; 8 rodadas numa noite sem resolver.**
Causa medida: swing em toda nota + ghost em todo beat + antecipação em todo par — empilhamento de semântica
de pressa.
Correção que funcionou: declarar a regra do groove antes de escrever ritmo, e aplicar uma dimensão por vez.

## 6. Família 4 — Grave: "embolou", "cancelou", "o sub não enche"

**Caso 44 — "Tá bom mas tá sendo cancelado"; 5 ajustes no mesmo dia sem resolver.**
Causa medida: a fundamental do kick estava uma quarta acima da do sub (ex.: F#1 ≈ 46 Hz contra C#1 ≈ 34,6
Hz), exatamente na faixa que o sub mascara; o EQ ainda realçava 46,95 Hz.
Correção que funcionou: medir a fundamental do kick contra a do sub antes de trocar ou equalizar; resolver o
conjunto, não o atacante.

**Caso 45 — "O kick está no vermelho e ninguém faz nada."**
Causa medida: sample a −0,10 dBFS + bell de +5,08 dB @89 Hz + velocidades 119–126 ≈ +5 dBFS no pico.
Correção que funcionou: medir o pico do canal, não a nota ou a velocidade.

**Caso 46 — "O sub sumiu praticamente" depois de encurtar notas (0,7 → 0,22 beat).**
Causa medida: o synth de sub não chega ao nível em ~100 ms; abaixo de ~0,4 beat a nota morre antes de soar.
Correção que funcionou: não encurtar sub abaixo de ~0,4 beat.

**Caso 47 — Sub 8–10 dB abaixo do esperado mesmo com +16 dB no render.**
Causa medida: patch de bass com sustain 0 e decay 0,18 s: nota longa vira silêncio; ganho só empurra o bus e o
limiter depois.
Correção que funcionou: medir a banda com o canal ligado × desligado; consertar o envelope, não o ganho.

**Caso 48 — "Depois dos 2 minutos encavala um sub no outro"; reprovação dupla.**
Causa medida: dois canais ligados com o mesmo preset na mesma nota, mural de semicolcheias com acento na cabeça.
Correção que funcionou: contar quantos canais ligados tocam a mesma nota no mesmo beat.

**Caso 49 — "Tem uma frequência dominando, ressonando sozinha."**
Causa medida: nota longa do baixo com pico estreito (~9 Hz de largura) a +5,7 dB acima da média de 30–500 Hz
(70,3 Hz) — ressonância de nota, não de fader.
Correção que funcionou: FFT de janela longa: pico estreito = nota; pico largo = transiente.

**Caso 50 — O corte de vácuo não "despressuriza" a mix.**
Causa medida: cortou-se o ataque do kick e o baixo continuou rolando; a referência faz o contrário (baixo
praticamente sai no buraco, −79,6 dB).
Correção que funcionou: medir o Δ por stem dentro do buraco antes de decidir o que cala.

**Caso 51 — "Embolado, sub totalmente fora"; perguntam "cadê a teoria musical".**
Causa medida: o elemento novo tocava uma oitava abaixo do sub existente (ex.: 34,4 Hz contra 69,6 Hz).
Correção que funcionou: medir o f0 da voz nova contra o sub antes de entrar com ela.

**Caso 52 — "Sinto falta do baixo" mesmo com três canais de sub; 2 exports reprovados.**
Causa medida: só um dos canais escrevia a fundamental real; os outros saíam uma oitava acima; o sub estava
−19,1 dB contra a régua de −4 a −6 dB.
Correção que funcionou: ler as alturas reais por clipe, nunca o nome do canal.

**Caso 53 — Kick esmagado depois de mexer no transpose.**
Causa medida: o cálculo de pitch não incluía o fator nota-raiz: `2^(T/12)` deu 326 Hz onde o real era 64,8 Hz.
Correção que funcionou: incluir `2^((nota−root)/12)` na conta e provar com tom de referência.

**Caso 54 — Grave "na régua" mas bateria "muito baixa"; 3 rodadas.**
Causa medida: a sub-banda estava ok (20–60 Hz +0,30 dB contra a referência), mas o topo media 16,6 dB abaixo
(5–12 kHz): hats enterrados (−14 dB) e filtro passa-baixa em 5,1 kHz no kick.
Correção que funcionou: medir por banda contra a referência antes de subir o grave.

## 7. Família 5 — Arranjo e orquestra: "colado", "reto", "o drop não chega", "sumiu no registro"

**Caso 55 — Aos 1:00 a mix bate menos que aos 0:30; reversão necessária.**
Causa medida: cortou-se um open hat de tensão/riser aprovado (velocities 93→108 em 11 disparos); o salto caiu
de +2,3 para +0,2 dB.
Correção que funcionou: classificar a função (sustenta/constrói/decora) antes de cortar qualquer camada.

**Caso 56 — "Muito colada, não tem respiro"; plano reescrito.**
Causa medida: o plano tirava 3,2 camadas por bloco de 8 compassos; a versão de referência tirava 10,8; o RMS
variava só +0,3 dB.
Correção que funcionou: contar camadas ativas por bloco, não olhar RMS.

**Caso 57 — "Vácuo perfeito de 4 tempos" que não chega ao áudio; 7 pareceres divergiram.**
Causa medida: zero notas de kick/sub na janela, mas −11,54 dBFS: camas, risers e vozes atravessavam o compasso.
Correção que funcionou: medir o LF por 1/16 dentro do vácuo, não só os elementos declarados.

**Caso 58 — "O kick vai sozinho"; 3 sessões de tentativa.**
Causa medida: o kick é 4/4 constante e a referência também; o problema é o entorno — 15/16 células vizinhas
ocupadas e offbeat com 4 donos.
Correção que funcionou: contar as células vizinhas antes de swingar o kick.

**Caso 59 — "A faixa soa lenta" virou meta de ≥10 onsets/s; 2 rodadas em direções opostas.**
Causa medida: o teto medido da referência era 6,99/s e a versão atual já media 12,08/s — 1,7× acima.
Correção que funcionou: checar a régua da referência antes de transformar sensação em meta numérica.

**Caso 60 — "Reto e previsível" no miolo da faixa.**
Causa medida: 9 vácuos idênticos de 2 tempos cortando as mesmas pistas; a referência varia 1, 2, 3 e 6
compassos.
Correção que funcionou: variar duração e conteúdo das quebras.

**Caso 61 — Dogma "topo percussivo não cai" impedindo cortes; 2 rodadas presas.**
Causa medida: nos 13 buracos medidos na referência, a rítmica inteira cala junto; 9 começam no 3º tempo.
Correção que funcionou: medir o corte na referência em vez de obedecer doutrina.

**Caso 62 — Hat soando "flutuante".**
Causa medida: loop idêntico a cada tempo e crescendo só no fader (−23 dB).
Correção que funcionou: olhar o padrão antes do fader; medir o desvio-padrão por compasso.

**Caso 63 — Breakdown lido como "o ponto de maior pressão"; alvo em aberto.**
Causa medida: a referência cai ~4,9 dB e troca o dono (melodia −3,5 dB no break, −17,5 no drop); a versão
atual caía 24 dB.
Correção que funcionou: comparar o nível da mix e a troca de dono, não o nível de um elemento isolado.

**Caso 64 — "A orquestra está matando a música"; rebuild completo.**
Causa medida: 18 camadas entravam juntas no mesmo compasso; a seção mudava a cada 3,7 compassos (referência:
8,8–16,1).
Correção que funcionou: escalonar entradas em 1–2 compassos e manter um fio condutor contínuo.

**Caso 65 — O drop "não salta"; 6 dias de tentativa.**
Causa medida: o build está a 2,1 dB do drop; os dois compassos anteriores picam 2,3 dB acima do próprio drop.
Correção que funcionou: tirar peso do build, não abrir espaço no downbeat.

**Caso 66 — Solista inaudível; reescrita reprovada.**
Causa medida: escrito no registro de MIDI 49–57, onde 8 canais ativos vivem na mesma janela.
Correção que funcionou: contar notas por canal e por registro na janela antes de escolher a oitava do solo.

**Caso 67 — Um instrumento acústico "uma oitava abaixo" do parceiro; EQ não resolveu.**
Causa medida: registro, não equalização: um preset com osciladores em octave −1 e o outro em 0 = 12 semitons
de diferença.
Correção que funcionou: comparar os octaves dos dois presets antes de qualquer EQ.

**Caso 68 — "Está distoando do nosso bloco"; 2 rodadas sem achar.**
Causa medida: 100% das notas dentro da escala do projeto, mas duas vozes colidiam em uníssono batido com o
lead e com o topo do outro instrumento (ex.: notas 68/73 contra o pitch do lead).
Correção que funcionou: cruzar os pitches dos canais entre si antes de acusar a escala.

**Caso 69 — Lead "morre do nada, sem resolução"; reescrita inteira.**
Causa medida: a frase terminava na 5ª do tom, segurada e sem envelope; 8 blocos do instrumento parceiro
também fechavam na 5ª.
Correção que funcionou: ler a última nota de cada clipe e resolver a cadência.

**Caso 70 — Orquestra "plástica" / cello áspero; 3 pistas, 2 sessões.**
Causa medida: patch sintético em pista acústica, 1–3 oitavas abaixo; cello com Octave −1 gerando 34 Hz.
Correção que funcionou: solo + ler oscilador e oitava antes de reverb ou EQ.

**Caso 71 — Instrumento de arco com "quack"; foi expurgado à toa.**
Causa medida: arco acústico picado em staccato <0,5 beat no grid.
Correção que funcionou: arco não se pica no grid — sustentar a nota ou trocar a técnica.

**Caso 72 — Instrumento de corda "menos metálico"; a causa não era timbre.**
Causa medida: o reverb estava desligado (instrumento seco vira clique), somado a realces de EQ e saturador
herdados.
Correção que funcionou: ler o estado liga/desliga dos devices antes de julgar o timbre.

**Caso 73 — Cello "leva sozinho, fica repetitivo".**
Causa medida: 6 dos 9 devices desligados, inclusive reverb e EQ já ajustados.
Correção que funcionou: ler o estado de cada device antes de compor o parceiro.

## 8. Família 6 — Pedido e processo: "não era isso", "você religou", "não mudou nada"

**Caso 74 — "Arruma isso" virou redesenho; reversão necessária.**
Causa medida: a intenção era restaurar o estado que funcionava; quem executou redesenhou.
Correção que funcionou: devolver o estado anterior; melhorar só com pedido explícito.

**Caso 75 — "Melhorar" executado como troca mecânica; reprovado.**
Causa medida: correção de −12 semitons quando o pedido era refazer partitura e timbre por inteiro.
Correção que funcionou: escalar a resposta à ambição do pedido, não ao mínimo executável.

**Caso 76 — Um trecho aprovado mudou por baixo do ouvido.**
Causa medida: depois do elogio, a fonte de um elemento foi trocada de instrumento e outro canal foi mutado.
Correção que funcionou: capturar o trecho aprovado antes de trocar fonte; elogiado fica.

**Caso 77 — "Desativei canais e você reativou."**
Causa medida: quem executou "restaurou" o que parecia quebrado e religou 13 mutes intencionais.
Correção que funcionou: mutes do produtor são decisão, não defeito — espelhar, não consertar.

**Caso 78 — O pedido era sobre a música A e executou-se na B.**
Causa medida: "nossa música" não significa o projeto aberto na tela.
Correção que funcionou: repetir o alvo em 1 linha antes de mutar qualquer coisa.

**Caso 79 — Reportou "pronto" com o trecho pedido vazio.**
Causa medida: escreveu em outro trecho e não reabriu o alvo pedido antes de reportar.
Correção que funcionou: provar 1 nota no trecho citado antes de declarar conclusão.

**Caso 80 — Uma palavra ambígua do briefing ("demais") lida com a intenção errada.**
Causa medida: a mesma palavra serve de intensificador ("melhorou demais") e de enumeração ("o kick e demais" =
"e o resto"); o contexto anterior define.
Correção que funcionou: classificar elogio/reprovação/lista pelo contexto antes de corrigir; na dúvida, uma
pergunta de 1 linha com as duas leituras concretas.

**Caso 81 — "Está roubando a cena."**
Causa medida: o elemento estava a 0 dB, o mesmo fader do elemento de base, enquanto o que ele substituía vivia
a −26 dB.
Correção que funcionou: repor o papel (fader, banda, duração da nota, função percussiva), não só baixar o
volume.

**Caso 82 — 33 mudanças de mix e "não notei diferença".**
Causa medida: tudo concentrado na mesma célula harmônica e com poucos dB cada — um mascara o outro.
Correção que funcionou: 1 mudança de ~6 dB audível antes de empilhar 33 mudanças de 1 dB.

**Caso 83 — Plano de 13 remoções e 2 adições: "senti quase nada"; 4 horas perdidas.**
Causa medida: as 2 adições nunca foram aplicadas; o plano era majoritariamente subtrativo.
Correção que funcionou: contar remoções × adições e conferir se as adições foram executadas de verdade.

**Caso 84 — 22 de 62 mapas de dissecação fora das regras do projeto; 14 conflitos não declarados.**
Causa medida: o briefing não mandava ler as regras; cada executor decidiu sozinho o que seguir.
Correção que funcionou: 3 linhas de "leia isto" + campo obrigatório "conflito com as regras" em todo briefing.

**Caso 85 — A nota final do instrumento "não ficou boa"; 34 notas revertidas.**
Causa medida: uma varredura automática de choques de 2ª menor reescreveu as notas finais de frase, onde o
atrito é resolução intencional (135 choques → ~4).
Correção que funcionou: tratar a nota final de frase como exceção da regra automática.

**Caso 86 — Um script "homologado" quebrou 9 dias depois com `ModuleNotFoundError`; a correção do motor
pressupunha um ambiente que tinha sido apagado junto.**
Causa medida: o ambiente Python da ferramenta morava numa pasta de artefatos — que é limpa periodicamente — e
nenhuma documentação marcava a perda.
Correção que funcionou: antes de usar script canônico, provar o runtime que ele chama (checar o ambiente +
import); ambientes de ferramenta nunca em pasta de artefato; registrar a localização real na documentação.
