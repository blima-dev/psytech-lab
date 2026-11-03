# Casos medidos: quando algo "nao sai", "mudou sozinho" ou "o numero nao bate"

> **O que e:** casos reais que ja custaram horas de diagnostico em projetos de producao eletronica, reescritos
> de forma generica. Para cada caso: **sintoma → causa medida → correcao que funcionou**. Nenhuma correcao
> aqui e dogma: sao saidas que resolveram casos concretos, com a medida que provou a causa.
> **Quando abrir:** um elemento some ou "nao sai"; o timbre muda sozinho; um numero briga com o ouvido; o
> groove soa afobado, reto ou fora; o grave embola; o drop nao chega; o solo desaparece no registro; e antes
> de dissecar timbre por horas.
> **Como usar:** ache a familia pelo sintoma, rode o check da causa medida, so entao mexa. Se a causa nao
> aparecer em 5 minutos, pare e meca o alvo diretamente. Se a mesma correcao falhar duas vezes, a premissa
> esta errada, nao a dose.

## 1. O check de 60 segundos

Quando um elemento "sumiu", "nao sai" ou "esta estranho", nesta ordem, sem pular:

1. **Alvo.** Canal + compasso + janela (min:seg). Feito quando voce consegue escrever "canal X, compassos A–B, 1:30–1:45".
2. **Existencia.** Mute do grupo → mute do canal → mute do clipe → janela do clipe (marcador inicial, fim,
   loop) → pico do arquivo de audio. Feito quando o primeiro elo quebrado tem nome e numero.
3. **Sinal.** Device ligado e ultimo device da cadeia → fonte do sidechain tem sinal → fader × automacao de
   volume → botao de saida/monitoramento. Feito quando o medidor do canal reage ao solo.
4. **Numero.** Render atual (data/hash), clipe que realmente toca, nota isolada, banda onde o elemento vive,
   unidade certa. Feito quando um controle proposital muda o numero.
5. **Mudanca.** Uma alteracao pequena e reversivel, backup antes, leitura de volta depois. Feito quando a
   leitura de volta mostra o valor novo, com o antes/depois lado a lado.

## 2. Padroes recorrentes (observacao, nao lei)

Quase todos os casos abaixo caem em uma de tres falhas:

- **(a)** o estado real nao era o que o documento, o nome ou o mapa dizia;
- **(b)** o numero era de outro objeto, outra janela ou outra unidade;
- **(c)** a correcao atacou a camada errada (fader onde o problema era papel, EQ onde era oitava, nota onde
  era clipe sobreposto).

## 3. Familia 1: silencio e sinal ("nao sai", "sumiu", "esta mudo")

**Caso 1: todas as capturas de teste sairam a −44 dBFS; so o canal do kick sozinho passava.**
Causa medida: um grupo pai estava mudo e silencia os filhos mesmo com todos os filhos desmutados; a lista de
canais nao mostra o mute do grupo.
Correcao que funcionou: antes da primeira captura, varrer os grupos pai por mute.

**Caso 2: solo num canal especifico e nao sai som nenhum.**
Causa medida: o grupo pai estava mudo; o solo do filho nao derruba o mute do pai.
Correcao que funcionou: desmutar o grupo.

**Caso 3: "nada esta mudo" e "o grupo esta mudo" no mesmo projeto; um mapa automatico concluiu que o canal
"nao pergunta para ninguem" e a investigacao virou horas de trabalho perdido.**
Causa medida: o sinalizador de saida de audio no arquivo do projeto estava sendo lido ao contrario: o valor
lido como "desligado" significa ligado (confirmado em 186 projetos); o mute de clipe e um campo diferente do
mute do canal; e a automacao de volume vence o mute manual.
Correcao que funcionou: ler o campo certo (provar o sentido com um canal de estado conhecido) e fazer um solo
de 30 s no canal acusado antes de qualquer reparo.

**Caso 4: canal com notas armazenadas e silencio total na janela esperada.**
Causa medida: notas fora da janela de reproducao; o marcador inicial do clipe jogava a primeira nota para um
compasso distante, e o fim do clipe e o loop recortavam o resto.
Correcao que funcionou: recalcular a janela (inicio absoluto, fim, loop) e comparar a primeira nota absoluta.

**Caso 5: "o instrumento nao tem partitura"; 52 clipes lidos como vazios foram apagados.**
Causa medida: a rotina de leitura usava um argumento de intervalo de notas zerado, que devolve lista vazia
sempre, sem erro.
Correcao que funcionou: ler um clipe sabidamente cheio como controle antes de apagar qualquer coisa em massa.

**Caso 6: um instrumento melodico com zero notas em dezenas de compassos.**
Causa medida: 14 dos 22 clipes estavam mudos no proprio clipe; o canal tinha mute desligado, volume e devices ok.
Correcao que funcionou: checar o mute por clipe antes de acusar o canal.

**Caso 7: dezenas de clipes "funcionalmente vazios" (~8% do total).**
Causa medida: a janela de reproducao atravessava so ~3% da frase; as notas existem, mas fora do que o cursor
percorre.
Correcao que funcionou: comparar a duracao do loop com a janela antes de chamar um clipe de fragmento.

**Caso 8: um canal de textura sem som nenhum em 32 clipes.**
Causa medida: os 32 clipes apontavam para WAVs de silencio digital, fatias cortadas do inicio de stems cuja
cabeca e silencio.
Correcao que funcionou: medir o pico do arquivo de cada clipe, nao confiar no clipe existir.

**Caso 9: "arrasto" atribuido a 12 duckings aparentemente armados; nenhum comprimia.**
Causa medida: o instrumento que gatilhava os sidechains estava sem sample carregado, gatilho decorativo.
Correcao que funcionou: solo + medir o pico do canal do gatilho antes de auditar qualquer ducking.

**Caso 10: o kick sumiu ao "desbloquear" um plugin.**
Causa medida: duas instancias de um plugin de ducking em serie, sem entrada de sidechain e com mix em 100%,
silenciavam tudo (uma senoide a −12 dBFS saia como silencio).
Correcao que funcionou: ler o ultimo device da cadeia antes de culpar o sample.

**Caso 11: o projeto inteiro mudo.**
Causa medida: automacao de volume do master travada em −70 dB desde o inicio da timeline.
Correcao que funcionou: ler o volume do master no inicio da timeline antes de procurar por canal.

**Caso 12: o export saiu com 92 bytes; "o som nao sai" em dezenas de tentativas; toda auditoria virou
analise de arquivo.**
Causa medida: o motor de audio estava sem device de saida selecionado; nenhuma A/B podia ser ouvida.
Correcao que funcionou: confirmar device de saida + medidor de atividade antes de abrir qualquer auditoria.

**Caso 13: "toda medicao de melodia mede outro canal".**
Causa medida: o filtro passa-baixa do lead estava travado perto de 20 Hz por 8 eventos de automacao; a medicao
capturava outra pista por onde o teste passava.
Correcao que funcionou: solo do canal e medir a banda alvo (ex.: 2–6 kHz) antes de escrever sobre melodia.

## 4. Familia 2: preset, timbre e clipe ("mudou sozinho", "voltou", "esta metalico")

**Caso 14: o preset volta ao de fabrica a cada play; "toda vez da esse bug".**
Causa medida: um mecanismo de integracao re-disparava o program change na abertura e sobrescrevia o estado
salvo do device.
Correcao que funcionou: procurar a flag de re-disparo e desliga-la nos canais que nao usam program change;
so depois investigar o arquivo do preset.

**Caso 15: carregar preset por indice carrega outro patch.**
Causa medida: o indice e alfabetico a partir de zero na pasta, e a lista fica congelada na instancia; renomear
arquivo nao entra.
Correcao que funcionou: abrir o preset pelo nome na interface antes de mapear qualquer indice.

**Caso 16: edicao offline do patch "voltou pro anterior" e perdeu ajustes.**
Causa medida: a injecao substituia blocos inteiros de estado do device e apagava os ajustes finos (o bloco
caiu de 3.520 para 2.984 caracteres).
Correcao que funcionou: comparar hash/tamanho do estado antes e depois de injetar; injetar so o delta, nao o
bloco inteiro.

**Caso 17: preset editado perde wavetable customizada e unison.**
Causa medida: a ferramenta de edicao substituia o slot do oscilador inteiro, e o unison nao era aplicado.
Correcao que funcionou: salvar o slot antes de editar e conferir o estado final por leitura de volta.

**Caso 18: ajuste recem-feito sumiu ao fechar o programa.**
Causa medida: um device adicionado na sessao existia so na memoria (nao salvo ha horas) e a opcao "nao salvar"
foi escolhida sem olhar.
Correcao que funcionou: inventariar o que existe so na sessao antes de dispensar o dialogo de salvar.

**Caso 19: nomes mentem em tres frentes: um preset nomeado com a tonica nao estava nela (mediu 56/112 Hz);
um preset chamado "suspiro vocal" tinha 96,8% da energia abaixo de 150 Hz; um instrumento acustico tocava com
preset de baixo.**
Causa medida: o nome nao comprova o conteudo.
Correcao que funcionou: medir pitch, energia e sample antes de catalogar ou confiar no nome.

**Caso 20: um impacto "metalico e so, sem corpo", mesmo trocando de sample varias vezes.**
Causa medida: preset desenhado para durar 8 compassos, disparado por notas de 1–3,5 beats; sobra so o ataque.
Correcao que funcionou: comparar a duracao que o preset pede com a duracao das notas do clipe.

**Caso 21: impacto estridente, "cheio de harmonicos".**
Causa medida: a fabrica de harmonicos era o saturador, nao o EQ.
Correcao que funcionou: A/B do saturador antes de mexer no EQ.

**Caso 22: voz soando "nasal" em todo o trecho.**
Causa medida: EQ copiado de outro canal com realces pesados (+10,8 dB @194 Hz e +9,05 dB @37,5 Hz), curva
herdada de um timbre de corda grave.
Correcao que funcionou: comparar a curva do EQ com a do canal de origem ao copiar cadeias.

**Caso 23: "notas rapidas" aparecendo num solo.**
Causa medida: 6 copias do mesmo solo, defasadas de ¼ a 1 tempo, tocando juntas; cada nota vira 4–6 ataques.
Correcao que funcionou: agrupar clipes por nome + conteudo de notas e examinar starts e sobreposicao.

**Caso 24: lead "dobra" depois de reescrever clipes (469 + 187 notas duplicadas).**
Causa medida: criar clipe MIDI sobre zona ocupada trima o clipe existente, e os fragmentos mantem todas as
notas.
Correcao que funcionou: deletar por posicao de inicio em toda a zona antes de criar; conferir contagem de
notas depois.

**Caso 25: milhares de notas apagadas (1.849) com o log dizendo so "ERRO".**
Causa medida: remocao e adicao de notas no mesmo bloco de tratamento de erro: a remocao rodou, a adicao
estourou, o clipe ficou vazio.
Correcao que funcionou: construir todas as especificacoes antes de mutar; usar operacao de modificacao atomica
quando existir.

**Caso 26: um instrumento "morre, perde a forca e volta" ao longo da frase.**
Causa medida: 11 clipes sobrepostos reiniciando o mesmo ostinato em pontos proximos da timeline.
Correcao que funcionou: contar os reinicios do padrao antes de acusar timbre ou nivel.

## 5. Familia 3: medicao e grade ("o numero nao bate com o ouvido")

**Caso 27: captura ao vivo diz −19,3 dBFS; o export diz −6,1.**
Causa medida: captura ao vivo nao e evidencia de mix; o sinal e o momento nao sao os do arquivo final.
Correcao que funcionou: medir so o arquivo exportado.

**Caso 28: alvo de "+8 a +12 dB no drop" que nao existia; plano substituido em menos de 1 hora.**
Causa medida: o render de referencia era anterior ao save que todos liam, e tres valores diferentes foram
medidos para "o drop".
Correcao que funcionou: congelar um render com hash e comparar a data de modificacao com a do arquivo do
projeto.

**Caso 29: um verificador automatico reprova uma barra inteira e outro parametro fica "folgado" com +58 dB
de diferenca.**
Causa medida: mediu-se a barra inteira, nao a sub-janela declarada; o salto vinha de outra secao esvaziada de
proposito.
Correcao que funcionou: medir exatamente a janela declarada, contra o piso declarado.

**Caso 30: "grave demais" onde o sub mediu −68,8 dB.**
Causa medida: filtro de baixa ordem rotulado "20–120 Hz" deixa saia ate ~300 Hz e infla +17,3 dB na faixa onde
o grave e vazio.
Correcao que funcionou: filtro de ordem alta ou medir sub-bandas separadas (20–60 e 60–120 Hz).

**Caso 31: um release medido em 250 ms quando a nota isolada sobe em 30–60 ms; cinco documentos carregaram
o numero errado.**
Causa medida: a medicao somou 3 semicolcheias emendadas em vez de medir a nota isolada.
Correcao que funcionou: medir 1 nota isolada e tratar o encavalamento entre notas a parte.

**Caso 32: alarme de "densidade 15,42/s contra teto 6,99"; 33 rodadas de investigacao.**
Causa medida: note-ons MIDI comparados com transientes de audio; 2.028 notas armazenadas contadas como ataques.
Correcao que funcionou: nomear a metrica (MIDI × ataque × transiente) antes de comparar com qualquer teto.

**Caso 33: "202 s de som dentro de uma janela de 165 s".**
Causa medida: beats comparados com segundos.
Correcao que funcionou: mesma unidade nos dois lados (beats ÷ BPM × 60 = segundos).

**Caso 34: inventario de clipes fechava em 81 quando deveria dar 83.**
Causa medida: agregacao por nome; dois canais com o mesmo nome (indices diferentes).
Correcao que funcionou: agregar por indice/ID do canal, nunca por nome.

**Caso 35: um ranking de afinacao "aprovava" uma voz fora de escala; ranking inteiro invalidado.**
Causa medida: estimador de pitch com resolucao de ~5,4 Hz e fundamental fora do alcance; uma senoide grave de
altura conhecida devolvia outra nota.
Correcao que funcionou: validar o medidor com uma senoide de altura conhecida antes de confiar nele.

**Caso 36: um A/B concluiu que "nosso topo e mais aberto"; conclusao falsa.**
Causa medida: um arquivo foi reduzido a mono (+3,01 dB no downmix) e comparado com media calculada no outro.
Correcao que funcionou: mesmo carregador/caminho de decodificacao nos dois arquivos.

**Caso 37: veredito de sentimento sobre duas faixas saiu fusionado numa analise so.**
Causa medida: os dois audios foram enviados numa chamada unica; a emenda foi tratada como fim de faixa.
Correcao que funcionou: 1 faixa por chamada, com marca explicita de inicio e fim.

**Caso 38: um modelo de escuta "ouviu riser" onde a envoltoria cai 41 dB; 3 escutas invalidadas.**
Causa medida: confabulacao do modelo + vies de posicao (escolhia sempre a 2ª opcao).
Correcao que funcionou: controle cego (trecho que so decai) e inversao da ordem das opcoes.

**Caso 39: "nada comeca no tempo 1, tudo cortado"; 2 dias de trabalho parado tratando como timbre.**
Causa medida: o projeto inteiro estava +0,727 beat fora do grid (335,9 ms de vacuo antes do tempo 1).
Correcao que funcionou: comparar a primeira nota absoluta do primeiro clipe com 0.0.

**Caso 40: "o swing ficou horrivel" depois de uma reescrita.**
Causa medida: o motor da sessao estava deslocado +0,363 beat e o shaker foi escrito na grade inteira.
Correcao que funcionou: ler o offset dos clipes da bateria antes de escrever nota nova.

**Caso 41: um elemento "nao esta com a mesma partitura" do restante.**
Causa medida: o kick muda de fase por secao (0 / 0,47 / 0,1 do beat) e o novo elemento foi escrito numa grade
unica.
Correcao que funcionou: derivar as posicoes das notas reais de cada secao, nao de uma grade teorica.

**Caso 42: "o sub chega 150 ms atrasado".**
Causa medida: 886 notas colocadas em cruzamentos de semicolcheia (x,5 = 58,6 ms rigidos) + ataque do patch.
Correcao que funcionou: medir offset e desvio-padrao das notas antes de acusar o envelope.

**Caso 43: groove "afobado/atropelando"; 8 rodadas numa noite sem resolver.**
Causa medida: swing em toda nota + ghost em todo beat + antecipacao em todo par, empilhamento de semantica
de pressa.
Correcao que funcionou: declarar a regra do groove antes de escrever ritmo, e aplicar uma dimensao por vez.

## 6. Familia 4: grave ("embolou", "cancelou", "o sub nao enche")

**Caso 44: "ta bom mas ta sendo cancelado"; 5 ajustes no mesmo dia sem resolver.**
Causa medida: a fundamental do kick estava uma quarta acima da do sub (ex.: F#1 ≈ 46 Hz contra C#1 ≈ 34,6
Hz), exatamente na faixa que o sub mascara; o EQ ainda realcava 46,95 Hz.
Correcao que funcionou: medir a fundamental do kick contra a do sub antes de trocar ou equalizar; resolver o
conjunto, nao o atacante.

**Caso 45: "o kick esta no vermelho e ninguem faz nada".**
Causa medida: sample a −0,10 dBFS + bell de +5,08 dB @89 Hz + velocidades 119–126 ≈ +5 dBFS no pico.
Correcao que funcionou: medir o pico do canal, nao a nota ou a velocidade.

**Caso 46: "o sub sumiu praticamente" depois de encurtar notas (0,7 → 0,22 beat).**
Causa medida: o synth de sub nao chega ao nivel em ~100 ms; abaixo de ~0,4 beat a nota morre antes de soar.
Correcao que funcionou: nao encurtar sub abaixo de ~0,4 beat.

**Caso 47: sub 8–10 dB abaixo do esperado mesmo com +16 dB no render.**
Causa medida: patch de bass com sustain 0 e decay 0,18 s: nota longa vira silencio; ganho so empurra o bus e o
limiter depois.
Correcao que funcionou: medir a banda com o canal ligado × desligado; consertar o envelope, nao o ganho.

**Caso 48: "depois dos 2 minutos encavala um sub no outro"; reprovacao dupla.**
Causa medida: dois canais ligados com o mesmo preset na mesma nota, mural de semicolcheias com acento na cabeca.
Correcao que funcionou: contar quantos canais ligados tocam a mesma nota no mesmo beat.

**Caso 49: "tem uma frequencia dominando, ressonando sozinha".**
Causa medida: nota longa do baixo com pico estreito (~9 Hz de largura) a +5,7 dB acima da media de 30–500 Hz
(70,3 Hz): ressonancia de nota, nao de fader.
Correcao que funcionou: FFT de janela longa: pico estreito = nota; pico largo = transiente.

**Caso 50: o corte de vacuo nao "despressuriza" a mix.**
Causa medida: cortou-se o ataque do kick e o baixo continuou rolando; a referencia faz o contrario (baixo
praticamente sai no buraco, −79,6 dB).
Correcao que funcionou: medir o Δ por stem dentro do buraco antes de decidir o que cala.

**Caso 51: "embolado, sub totalmente fora"; perguntam "cade a teoria musical".**
Causa medida: o elemento novo tocava uma oitava abaixo do sub existente (ex.: 34,4 Hz contra 69,6 Hz).
Correcao que funcionou: medir o f0 da voz nova contra o sub antes de entrar com ela.

**Caso 52: "sinto falta do baixo" mesmo com tres canais de sub; 2 exports reprovados.**
Causa medida: so um dos canais escrevia a fundamental real; os outros saiam uma oitava acima; o sub estava
−19,1 dB contra a regua de −4 a −6 dB.
Correcao que funcionou: ler as alturas reais por clipe, nunca o nome do canal.

**Caso 53: kick esmagado depois de mexer no transpose.**
Causa medida: o calculo de pitch nao incluia o fator nota-raiz: `2^(T/12)` deu 326 Hz onde o real era 64,8 Hz.
Correcao que funcionou: incluir `2^((nota−root)/12)` na conta e provar com tom de referencia.

**Caso 54: grave "na regua" mas bateria "muito baixa"; 3 rodadas.**
Causa medida: a sub-banda estava ok (20–60 Hz +0,30 dB contra a referencia), mas o topo media 16,6 dB abaixo
(5–12 kHz): hats enterrados (−14 dB) e filtro passa-baixa em 5,1 kHz no kick.
Correcao que funcionou: medir por banda contra a referencia antes de subir o grave.

## 7. Familia 5: arranjo e orquestra ("colado", "reto", "o drop nao chega", "sumiu no registro")

**Caso 55: aos 1:00 a mix bate menos que aos 0:30; reversao necessaria.**
Causa medida: cortou-se um open hat de tensao/riser aprovado (velocities 93→108 em 11 disparos); o salto caiu
de +2,3 para +0,2 dB.
Correcao que funcionou: classificar a funcao (sustenta/constroi/decora) antes de cortar qualquer camada.

**Caso 56: "muito colada, nao tem respiro"; plano reescrito.**
Causa medida: o plano tirava 3,2 camadas por bloco de 8 compassos; a versao de referencia tirava 10,8; o RMS
variava so +0,3 dB.
Correcao que funcionou: contar camadas ativas por bloco, nao olhar RMS.

**Caso 57: "vacuo perfeito de 4 tempos" que nao chega ao audio; 7 pareceres divergiram.**
Causa medida: zero notas de kick/sub na janela, mas −11,54 dBFS: camas, risers e vozes atravessavam o compasso.
Correcao que funcionou: medir o LF por 1/16 dentro do vacuo, nao so os elementos declarados.

**Caso 58: "o kick vai sozinho"; 3 sessoes de tentativa.**
Causa medida: o kick e 4/4 constante e a referencia tambem; o problema e o entorno, com 15/16 celulas vizinhas
ocupadas e offbeat com 4 donos.
Correcao que funcionou: contar as celulas vizinhas antes de swingar o kick.

**Caso 59: "a faixa soa lenta" virou meta de ≥10 onsets/s; 2 rodadas em direcoes opostas.**
Causa medida: o teto medido da referencia era 6,99/s e a versao atual ja media 12,08/s, 1,7× acima.
Correcao que funcionou: checar a regua da referencia antes de transformar sensacao em meta numerica.

**Caso 60: "reto e previsivel" no miolo da faixa.**
Causa medida: 9 vacuos identicos de 2 tempos cortando as mesmas pistas; a referencia varia 1, 2, 3 e 6
compassos.
Correcao que funcionou: variar duracao e conteudo das quebras.

**Caso 61: dogma "topo percussivo nao cai" impedindo cortes; 2 rodadas presas.**
Causa medida: nos 13 buracos medidos na referencia, a ritmica inteira cala junto; 9 comecam no 3º tempo.
Correcao que funcionou: medir o corte na referencia em vez de obedecer doutrina.

**Caso 62: hat soando "flutuante".**
Causa medida: loop identico a cada tempo e crescendo so no fader (−23 dB).
Correcao que funcionou: olhar o padrao antes do fader; medir o desvio-padrao por compasso.

**Caso 63: breakdown lido como "o ponto de maior pressao"; alvo em aberto.**
Causa medida: a referencia cai ~4,9 dB e troca o dono (melodia −3,5 dB no break, −17,5 no drop); a versao
atual caia 24 dB.
Correcao que funcionou: comparar o nivel da mix e a troca de dono, nao o nivel de um elemento isolado.

**Caso 64: "a orquestra esta matando a musica"; rebuild completo.**
Causa medida: 18 camadas entravam juntas no mesmo compasso; a secao mudava a cada 3,7 compassos (referencia:
8,8–16,1).
Correcao que funcionou: escalonar entradas em 1–2 compassos e manter um fio condutor continuo.

**Caso 65: o drop "nao salta"; 6 dias de tentativa.**
Causa medida: o build esta a 2,1 dB do drop; os dois compassos anteriores picam 2,3 dB acima do proprio drop.
Correcao que funcionou: tirar peso do build, nao abrir espaco no downbeat.

**Caso 66: solista inaudivel; reescrita reprovada.**
Causa medida: escrito no registro de MIDI 49–57, onde 8 canais ativos vivem na mesma janela.
Correcao que funcionou: contar notas por canal e por registro na janela antes de escolher a oitava do solo.

**Caso 67: um instrumento acustico "uma oitava abaixo" do parceiro; EQ nao resolveu.**
Causa medida: registro, nao equalizacao: um preset com osciladores em octave −1 e o outro em 0 = 12 semitons
de diferenca.
Correcao que funcionou: comparar os octaves dos dois presets antes de qualquer EQ.

**Caso 68: "esta distoando do nosso bloco"; 2 rodadas sem achar.**
Causa medida: 100% das notas dentro da escala do projeto, mas duas vozes colidiam em unissono batido com o
lead e com o topo do outro instrumento (ex.: notas 68/73 contra o pitch do lead).
Correcao que funcionou: cruzar os pitches dos canais entre si antes de acusar a escala.

**Caso 69: lead "morre do nada, sem resolucao"; reescrita inteira.**
Causa medida: a frase terminava na 5ª do tom, segurada e sem envelope; 8 blocos do instrumento parceiro
tambem fechavam na 5ª.
Correcao que funcionou: ler a ultima nota de cada clipe e resolver a cadencia.

**Caso 70: orquestra "plastica" / cello aspero; 3 pistas, 2 sessoes.**
Causa medida: patch sintetico em pista acustica, 1–3 oitavas abaixo; cello com Octave −1 gerando 34 Hz.
Correcao que funcionou: solo + ler oscilador e oitava antes de reverb ou EQ.

**Caso 71: instrumento de arco com "quack"; foi expurgado a toa.**
Causa medida: arco acustico picado em staccato <0,5 beat no grid.
Correcao que funcionou: arco nao se pica no grid; sustentar a nota ou trocar a tecnica.

**Caso 72: instrumento de corda "menos metalico"; a causa nao era timbre.**
Causa medida: o reverb estava desligado (instrumento seco vira clique), somado a realces de EQ e saturador
herdados.
Correcao que funcionou: ler o estado liga/desliga dos devices antes de julgar o timbre.

**Caso 73: cello "leva sozinho, fica repetitivo".**
Causa medida: 6 dos 9 devices desligados, inclusive reverb e EQ ja ajustados.
Correcao que funcionou: ler o estado de cada device antes de compor o parceiro.

## 8. Familia 6: pedido e processo ("nao era isso", "voce religou", "nao mudou nada")

**Caso 74: "arruma isso" virou redesenho; reversao necessaria.**
Causa medida: a intencao era restaurar o estado que funcionava; quem executou redesenhou.
Correcao que funcionou: devolver o estado anterior; melhorar so com pedido explicito.

**Caso 75: "melhorar" executado como troca mecanica; reprovado.**
Causa medida: correcao de −12 semitons quando o pedido era refazer partitura e timbre por inteiro.
Correcao que funcionou: escalar a resposta a ambicao do pedido, nao ao minimo executavel.

**Caso 76: um trecho aprovado mudou por baixo do ouvido.**
Causa medida: depois do elogio, a fonte de um elemento foi trocada de instrumento e outro canal foi mutado.
Correcao que funcionou: capturar o trecho aprovado antes de trocar fonte; elogiado fica.

**Caso 77: "desativei canais e voce reativou".**
Causa medida: quem executou "restaurou" o que parecia quebrado e religou 13 mutes intencionais.
Correcao que funcionou: mutes do produtor sao decisao, nao defeito; espelhar, nao consertar.

**Caso 78: o pedido era sobre a musica A e executou-se na B.**
Causa medida: "nossa musica" nao significa o projeto aberto na tela.
Correcao que funcionou: repetir o alvo em 1 linha antes de mutar qualquer coisa.

**Caso 79: reportou "pronto" com o trecho pedido vazio.**
Causa medida: escreveu em outro trecho e nao reabriu o alvo pedido antes de reportar.
Correcao que funcionou: provar 1 nota no trecho citado antes de declarar conclusao.

**Caso 80: uma palavra ambigua do briefing ("demais") lida com a intencao errada.**
Causa medida: a mesma palavra e intensificador ("melhorou demais") e enumeracao ("o kick e demais" =
"e o resto"); o contexto anterior define.
Correcao que funcionou: classificar elogio/reprovacao/lista pelo contexto antes de corrigir; na duvida, uma
pergunta de 1 linha com as duas leituras concretas.

**Caso 81: "esta roubando a cena".**
Causa medida: o elemento estava a 0 dB, o mesmo fader do elemento de base, enquanto o que ele substituia vivia
a −26 dB.
Correcao que funcionou: repor o papel (fader, banda, duracao da nota, funcao percussiva), nao so baixar o
volume.

**Caso 82: 33 mudancas de mix e "nao notei diferenca".**
Causa medida: tudo concentrado na mesma celula harmonica e com poucos dB cada; um mascara o outro.
Correcao que funcionou: 1 mudanca de ~6 dB audivel antes de empilhar 33 mudancas de 1 dB.

**Caso 83: plano de 13 remocoes e 2 adicoes: "senti quase nada"; 4 horas perdidas.**
Causa medida: as 2 adicoes nunca foram aplicadas; o plano era majoritariamente subtrativo.
Correcao que funcionou: contar remocoes × adicoes e conferir se as adicoes foram executadas de verdade.

**Caso 84: 22 de 62 mapas de dissecacao fora das regras do projeto; 14 conflitos nao declarados.**
Causa medida: o briefing nao mandava ler as regras; cada executor decidiu sozinho o que seguir.
Correcao que funcionou: 3 linhas de "leia isto" + campo obrigatorio "conflito com as regras" em todo briefing.

**Caso 85: a nota final do instrumento "nao ficou boa"; 34 notas revertidas.**
Causa medida: uma varredura automatica de choques de 2ª menor reescreveu as notas finais de frase, onde o
atrito e resolucao intencional (135 choques → ~4).
Correcao que funcionou: tratar a nota final de frase como excecao da regra automatica.

**Caso 86: um script "homologado" quebrou 9 dias depois com `ModuleNotFoundError`; a correcao do motor
pressupunha um ambiente que tinha sido apagado junto.**
Causa medida: o ambiente Python da ferramenta morava numa pasta de artefatos (que e limpa periodicamente) e
nenhuma documentacao marcava a perda.
Correcao que funcionou: antes de usar script canonico, provar o runtime que ele chama (checar o ambiente +
import); ambientes de ferramenta nunca em pasta de artefato; registrar a localizacao real na documentacao.
