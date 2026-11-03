# CICATRIZES — o que já custou horas (mapa de lições)

> **O que é:** o mapa dos erros que uma produção psytech já pagou caro — horas dissecando uma causa simples,
> ou a mesma trava repetida em datas diferentes. Cada linha tem sintoma, custo documentado, causa medida,
> o check de 1 minuto.
> **Quando abrir:** quando um elemento some ou "não sai"; quando o timbre muda sozinho; quando um número briga
> com o ouvido; quando o groove soa "afobado/reto/fora"; quando o grave embola; quando a música "cola" ou o
> drop não chega; quando o solista sumiu no registro; quando o pedido virou outra coisa — **e antes de
> dissecar timbre por horas**.
> **Como usar:** ache a família pelo sintoma, rode o check, só então mexa. Se a causa não aparecer em 5 min,
> pare e meça o alvo (Lei 3). Se a correção falhar duas vezes, mate a premissa (Lei 12).
> **Limite:** este doc é mapa, não lei. O detalhe técnico canônico fica no manual de operação do próprio
> estúdio; datas e números abaixo são os medidos nas sessões de origem.

## 1. O check de 60 segundos

Quando um elemento "sumiu", "não sai" ou "está estranho", nesta ordem — sem pular:

1. **Alvo.** Pista + compasso + janela (min:seg). *Feito quando você escreve "pista X, bars A–B, 1:30–1:45".*
2. **Existência.** Mute do grupo → mute da pista → `clip.muted` / `<Disabled>` → janela (`start_marker`,
   `CurrentEnd`, `loop`) → pico do arquivo. *Feito quando o primeiro elo quebrado tem nome e número.*
3. **Sinal.** Device on e último device da cadeia → fonte do sidechain tem sample → fader × lane de volume →
   `Speaker`. *Feito quando o medidor da pista reage ao solo.*
4. **Número.** Render atual (mtime/md5), clipe que toca, nota isolada, banda onde o elemento vive, unidade
   certa. *Feito quando um controle proposital muda o número.*
5. **Mudança.** Uma alteração pequena e reversível, backup antes, read-back depois. *Feito quando o read-back
   mostra o valor novo e o antes/depois está lado a lado.*

## 2. As 12 leis

1. **Óbvio primeiro** — antes de dissecar timbre, prove que o canal existe: grupo, clipe, janela, mídia,
   device, sample do trigger. A maior parte das "horas de dissecação" mora aqui.
2. **Nome não é prova** — canal, preset, arquivo e clipe mentem. Leia o parâmetro, o sample e a nota.
3. **Alvo, não proxy** — meça o objeto e a janela que o número afirma: captura não é export, nota armazenada
   não é ataque, banda do filtro não é banda do som, beat não é segundo.
4. **Um mecanismo por vez** — A/B de uma coisa. Duas mudanças juntas não provam nada; dois escritores no Set,
   menos ainda.
5. **Função no compasso** — sustenta, constrói ou decora. O que constrói não se corta "para abrir espaço", e
   "roubando a cena" é papel, não volume.
6. **Cortar é arranjo** — respiro se faz tirando camada, não somando. Silêncio é conteúdo; a história mora no
   padrão, não no fader.
7. **Um chão só** — kick, sub e baixo dividem a mesma fundamental. Meça o f0 antes de entrar voz nova e corte
   o conjunto, não o atacante.
8. **Registro é elenco** — a oitava decide quem é ouvido. Registro entupido não se conserta com EQ; oitava de
   preset não se conserta com filtro.
9. **Nota final é assinatura** — fim de frase resolve. O atrito intencional não se "corrige" por contagem de
   choque.
10. **Arquivo salvo é a verdade** — documento de estado, doc e relatório são hipótese; data de modificação,
    hash do arquivo e read-back decidem.
11. **Aprovado fica** — o elogiado não se toca; na reprovação, reverte só o citado.
12. **Duas rejeições matam a premissa** — se a mesma correção falhou duas vezes, o modelo está errado, não a
    dose.

## 3. As 7 cicatrizes mais caras

| # | Caso | Custo documentado | Lição | ID |
|---|---|---|---|---|
| 1 | 12 sidechains "armados" que nunca comprimiram: o Simpler do trigger estava sem sample | 162 `.als` · 3 semanas (26/09→16/10) | trigger sem sample é decorativo | A9 |
| 2 | Motor de áudio em `No Device`: nenhum A/B podia ser ouvido; tudo virou diagnóstico de arquivo | ~75 rodadas · 1 dia | device de saída antes de qualquer auditoria | A12 |
| 3 | Set inteiro +0,727 beat fora do grid, tratado como problema de timbre | 3 travamentos + 1 alinhamento em 2 dias | 1ª nota do clip 1 = 0.0 | C13 |
| 4 | 52 clipes "sem partitura" apagados: `pitch_span=0` devolve vazio sempre | 52 clipes · 48 notas · 1 backup | leia um clipe cheio como controle antes de apagar | A5 |
| 5 | Alarme de densidade 15,42/s: note-ons MIDI comparados com transientes de áudio | 33 rodadas | nomeie a métrica antes de comparar com teto | C6 |
| 6 | Mapa leu `speaker=false` e desenhou 133 notas em cima de um canal que estava ligado | ~6 h · ~1.300 comandos bloqueados | solo de 30 s antes de orçar o reparo | A3 |
| 7 | Preset do Serum voltava a cada play e apagava a edição feita dentro do patch | 2 sessões em 10 dias · ~21 canais em risco | program change persistido re-dispara na abertura | B1 |

**O padrão por trás das 85:** quase tudo cai em três falhas — (a) o estado real não era o que o documento, o
nome ou o mapa dizia; (b) o número era de outro objeto, outra janela ou outra unidade; (c) a correção atacou a
camada errada (fader onde era papel, EQ onde era oitava, nota onde era clipe empilhado). Cicatriz fechada
continua no mapa: o que se repete é o mecanismo, não o caso.

## 4. Silêncio e sinal — "não sai", "sumiu", "está mudo"

| ID | Sintoma | Custo | Causa medida | Primeiro check | Lei |
|---|---|---|---|---|---|
| A1 | 6 capturas a −44 dBFS; só o kick solo passava | 6 capturas | Grupo pai com `mute=True` silencia filhos mesmo desmutados; a lista de tracks não mostra grupo mudo | `[t for t in tracks if t.is_foldable and t.mute]` antes da 1ª captura | 1 |
| A2 | Solo em um canal e nada | 1 sessão | Grupo-pai de orquestra mudo; solo de filho não derruba o mute do pai | desmutar o grupo | 1 |
| A3 | "nada está mudo" e "o grupo está mudo" no mesmo set; um mapa chegou a concluir que um canal "pergunta para ninguém" | ~6 h / ~1.300 comandos + quase-reversão do set | `Speaker/Manual=true` = canal **ATIVO** (lido ao contrário em 186 sets auditados); `Clip.mute` é no-op; mute de clipe é `<Disabled>`; lane Speaker vence o Manual | ler o campo certo + solo de 30 s no canal acusado | 1, 2 |
| A4 | Canal com notas e silêncio total | 2 rodadas | Notas fora da janela: `start_marker=64` joga a 1ª nota para o bar 33; `CurrentEnd` manda; loop recorta | simular `start_marker`/loop e comparar a 1ª nota absoluta | 1 |
| A5 | Um riser "sem partitura": 52 clipes lidos como vazios e apagados | 52 clipes · 48 notas | `get_notes_extended(0, 0, …)`: o 2º argumento é `pitch_span`, e `0` devolve lista vazia **sempre**, sem erro | ler um clipe sabidamente cheio como controle antes de apagar | 3 |
| A6 | Pista de flauta com zero notas em 87 compassos | 12 rodadas | 14 de 22 clipes mudos no próprio clipe; a pista tinha mute=false, volume e devices ok | ler `clip.muted` antes de acusar o canal | 1 |
| A7 | 83 clipes "funcionalmente vazios" (8,3% de 1.001) | 6 rodadas | Janela = 3,1% da frase com `length` do loop intacto: as notas existem, mas fora do que o cursor atravessa | comparar `length` do loop × janela antes de chamar de fragmento | 3 |
| A8 | Canal de madeira sem som | 32 clipes · 2 canais | 32 clipes apontavam para WAV de silêncio digital: chops cortados do 0,0 s de stems cuja cabeça é silêncio | medir o pico do `file_path` de cada clipe | 1 |
| A9 | "Arrasto" com 12 duckings aparentemente armados | 162 `.als` · 3 semanas | Clipes de trigger de sidechain com Simpler sem sample (`<SampleParts/>`): nenhum ducker jamais comprimiu | solo + pico do canal do trigger antes de auditar o ducking | 1 |
| A10 | Kick sumiu ao "desbloquear" plugin | 1 rodada + desvio | 2 instâncias de Kickstart 2 em série com "Sidechain: No Input" e Mix 100%: senoide −12 dBFS saía −inf | ler o último device da cadeia antes do sample | 1 |
| A11 | Set inteiro mudo | 1 sessão | Lane de Volume do Master em −70 dB (`1.0`→`0.000316`) do beat 0 ao 960 | ler o Volume do Master no beat 0 | 1 |
| A12 | WAV de 92 bytes; "o som não sai" | ~75 rodadas · 1 dia | Motor de áudio em `No Device`; o estado não aparece no resumo do set | ler device de saída + CPU Meter antes de abrir auditoria | 1 |
| A13 | "Toda medição de melodia mede outra pista" | 2 regiões invalidadas | Um lead com low-pass pinado em ~20 Hz por 8 eventos de automação | solo do canal do lead e medida em 2–6 kHz antes de escrever melodia | 3 |

## 5. Preset, timbre e clipe — "mudou sozinho", "voltou", "está metálico"

| ID | Sintoma | Custo | Causa medida | Primeiro check | Lei |
|---|---|---|---|---|---|
| B1 | Preset volta ao de fábrica a cada play; "toda vez dá esse bug" | 10 dias · ~21 canais em risco | Program change persistido re-dispara na abertura e vence o estado salvo do patch | procurar program change persistido e desligá-lo nos canais que não usam | 10 |
| B2 | Disparo por índice carrega outro patch | 3 sessões | `program` = índice **alfabético 0-based** na pasta; a lista é congelada na instância e rename não entra | abrir o preset pelo nome na UI antes de mapear índice | 2, 10 |
| B3 | "Mexeu offline e voltou pro anterior" | 1 rodada + restauração | Injeção offline de estado de preset troca `ProcessorState`/`ControllerState` inteiros e apaga tweaks (3.520→2.984 chars) | diff de hash/tamanho do estado antes de injetar | 10 |
| B4 | Preset editado perde wavetable custom e unison | 1 wavetable | `edit_preset` substitui o slot do oscilador inteiro; `unison` não aplica | salvar o slot antes e conferir `table_pos` no read-back | 3 |
| B5 | Ajuste da sessão sumiu ao fechar | 1 ajuste + 1 rodada | "Don't Save" com device existindo só na sessão (Roar desligado não salvo desde as 18:25) | inventariar o que está só na sessão antes de dispensar o diálogo | 10 |
| B6 | Preset nomeado "C#" não está em C#; preset de "suspiro vocal" não é voz; preset de kamancheh toca baixo | 5 ocorrências | Nome não comprova conteúdo: 56/112 Hz no arquivo "C#"; 96,8% da energia do sigh abaixo de 150 Hz; pista do kamancheh com preset de baixo | medir pitch/energia/sample antes de catalogar | 2 |
| B7 | "Metálico e só, um braam sem nada" | várias trocas de sample | Preset desenhado para 8 compassos disparado por nota de 1–3,5 beats: sobra só o ataque metálico | comparar duração que o preset pede com o `length` do clipe | 3 |
| B8 | BRAAM estridente | 1 rodada | A fábrica de harmônicos era o Saturator, não o EQ | A/B do Saturator antes de mexer no EQ | 3 |
| B9 | Voz "nasal" num solo | 1 rodada | EQ com +10,8 dB @194 Hz e +9,05 dB @37,5 Hz: curva de sub herdada do cello | comparar a curva do EQ com a do canal de origem | 2 |
| B10 | "Notas rápidas" num solo | 2 sessões | 6 cópias do mesmo solo defasadas de ¼–1 tempo tocando juntas; cada nota vira 4–6 ataques | agrupar `arrangement_clips` por nome+notas e olhar starts/sobreposição | 1 |
| B11 | Lead "dobra" depois de reescrever clipes | 469 + 187 notas dobradas | `create_midi_clip` sobre zona ocupada **TRIMA** o clipe existente e os fragmentos mantêm todas as notas | deletar por start em toda a zona antes de criar | 10 |
| B12 | 1.849 notas apagadas com o log dizendo só "ERRO" | 1.849 notas + undo manual | `remove_notes_extended` e `add_new_notes` no mesmo `try`: a remoção rodou, o add estourou e o clipe ficou vazio | construir todas as specs antes de mutar; usar `apply_note_modifications` | 10 |
| B13 | Kanun "morre, acaba a força e volta" | 11 cópias | 11 clipes sobrepostos reiniciando o ostinato em 463,625–476,75 | contar reinícios do ostinato antes de acusar timbre ou nível | 1 |

## 6. Medição e grade — "o número não bate com o ouvido"

| ID | Sintoma | Custo | Causa medida | Primeiro check | Lei |
|---|---|---|---|---|---|
| C1 | Captura diz −19,3 dBFS, export diz −6,1 | 1 sessão de conserto errado | Captura ao vivo não é evidência de mix; o sinal e o momento não são os do arquivo | medir só arquivo exportado | 3 |
| C2 | Alvo de "+8 a +12 dB" no drop que não existia | 1 dia · plano substituído em <1 h | O render analisado era anterior ao save que todos liam; 3 valores de "o drop" (+26,4/+26,7/+26,81) | congelar 1 render com hash e comparar mtime com o `.als` | 3 |
| C3 | Gate reprova o bar 40 e uma regra fica "folgada" com +58 dB | 1 rodada | Mediu a barra inteira, não o t4 declarado; o salto vinha de um bar 48 esvaziado de propósito | medir a janela que o mapa declara e contra o piso | 3 |
| C4 | "Grave demais" onde o sub real era −68,8 dB | 1 rodada | Filtro "20–120" de 4ª ordem é 20–140 com saia até 300 Hz: infla +17,3 dB onde o grave é vazio | FIR/8ª ordem ou medir 20–60 + 60–120 | 3 |
| C5 | Alvo de "ataque do sub = 250 ms" e "reduzir o Release" | 5 documentos carregaram o número | Mediu a soma de 3 semicolcheias emendadas, não a nota isolada (que sobe em 30–60 ms) | medir 1 nota isolada; tratar o encavalamento | 3 |
| C6 | Alarme: "densidade 15,42/s, teto 6,99" | 33 rodadas | Note-ons MIDI comparados com transientes de áudio; 2.028 notas armazenadas contadas como ataques | nomear a métrica (MIDI × ataque × transiente) antes de comparar | 3 |
| C7 | "202,25 s de som dentro de janela de 165 s" | 2 rodadas | Beats comparados com segundos | mesma unidade nos dois lados: beat ÷ BPM × 60 | 3 |
| C8 | Inventário de 83 clipes fechava em 81 | 1 rodada | Agregação por **nome**: duas pistas com o mesmo nome (índices 49 e 50) | agregar por índice de pista | 2 |
| C9 | Ranking de afinação "aprovava" uma regra equivocada | ranking inteiro invalidado | `inscale` com resolução 5,38 Hz e fundamental cortada: senoide de C#0 devolve F | testar o medidor numa senoide de altura conhecida | 3 |
| C10 | A/B concluiu que "o topo de um lado é mais aberto" | 1 rodada | `-ac 1` do ffmpeg soma +3,01 dB no downmix e foi comparado com média numpy | mesmo carregador nos dois arquivos | 4 |
| C11 | Veredito de sentimento sobre "Faixa A" e "Faixa B" | 1 rodada | Os dois áudios foram numa chamada só; o modelo fundiu e tratou a emenda como fim de faixa | 1 faixa por chamada, com marca de início e fim | 4 |
| C12 | Escuta "ouve riser" onde a envoltória cai 41 dB | 3 escutas inválidas | Confabulação do modelo + viés de posição (escolheu o 2º em 4/4) | controle cego (trecho que só decai) e inverter a ordem | 4 |
| C13 | "Não tá start no tempo 1, tudo cortada e cagada" | 3 travamentos + 2 dias | Set inteiro +0,727129 beat fora do grid: 335,9 ms de vácuo antes do tempo 1 | comparar a 1ª nota absoluta do clip 1 com 0.0 | 3 |
| C14 | "Swing ficou horrível" | 1 reescrita | Motor em +0,363 beat e o shaker escrito na grade inteira | ler o offset dos clipes do kick antes de escrever nota nova | 3 |
| C15 | O kick "não está com a mesma partitura" | 1 rodada | O kick muda de fase por seção (0 / 0,47 / 0,1 do beat) e a percussão foi escrita numa grade única | derivar posições das notas reais de cada seção | 3 |
| C16 | "O sub chega 150 ms atrasado" | 1 rodada de DSP | 886 notas de um canal em x,5 de 16avo = 58,6 ms rígidos + ataque do patch | medir offset e SD das notas antes de acusar envelope | 3 |
| C17 | Groove "afobado/atropelando" | 8 rodadas numa noite | Swing +22 ms em toda nota + ghost em todo beat + antecipação em todo par: semântica de pressa | declarar a regra da aula de groove antes de escrever ritmo | 12 |

## 7. Grave — "embolou", "cancelou", "o sub não enche"

| ID | Sintoma | Custo | Causa medida | Primeiro check | Lei |
|---|---|---|---|---|---|
| D1 | "Tá bom mas tá sendo cancelado" | 5 ajustes no mesmo dia | Kick em F#1 (46 Hz), quarta acima do sub C#1 (34,6 Hz), exatamente na faixa que o sub mascara; o EQ ainda boostava 46,95 Hz | medir a fundamental do kick contra a do sub antes de trocar o kick | 7 |
| D2 | "O kick no vermelho e você faz nada" | 1 rodada | Sample a −0,10 dBFS + bell +5,08 dB @89 Hz + velocities 119–126 ≈ +5 dBFS | medir o pico do canal, não a nota | 7 |
| D3 | "O sub sumiu praticamente" | 2 rodadas (0,7→0,22→0,45) | Serum SUB não chega ao nível em ~100 ms; abaixo de ~0,4 beat a nota morre antes de soar | não encurtar sub abaixo de ~0,4 beat | 7 |
| D4 | Sub 8–10 dB abaixo mesmo com +16 dB no render | 1 dia | Preset talking bass com `Env1 sustain=0,00 / decay=0,18 s`: nota longa vira silêncio; ganho só empurra Glue/Limiter | medir a banda ligado × desligado | 7 |
| D5 | "Depois dos 2 min encavala um sub no outro" | 1 noite · 2 reprovações | Dois canais ligados com o mesmo preset em C#3, mural de 16avos com acento na cabeça | contar quantos canais ligados tocam a mesma nota no mesmo beat | 7 |
| D6 | "Ele está com frequência dominando, ressonando sozinho" | 1 rodada | C#2 do baixo em 70,3 Hz, +5,7 dB acima de 30–500 Hz, largura ~9 Hz: nota longa, não fader | FFT de 25 s: pico estreito = nota; largo = transiente | 3 |
| D7 | O corte não despressuriza | 1 rodada + board | Mutou o ataque do kick e deixou o baixo rolando; a referência faz o contrário (baixo a −79,6 dB) | medir o Δ por stem dentro do buraco | 6 |
| D8 | "Embolado, sub totalmente fora, cadê teoria musical" | 1 rodada | Operator nota 25 = C#0 34,4 Hz contra o sub no Serum em C#1 69,6 Hz: uma oitava de diferença | medir o f0 da voz nova contra o sub existente | 7 |
| D9 | "Tô sentindo falta do baixo" | 2 exports | Só 1 dos 3 canais de sub escrevia a fundamental C#1; os outros 2 saíam em C#2 (uma oitava acima); sub−kick −19,1 dB contra régua −4..−6 | ler as alturas reais por clipe, não o nome do canal | 2, 7 |
| D10 | Kick esmagado depois de mexer no transpose | 1 rodada | Conta sem fator nota/root: `2^(T/12)` dá 326 Hz onde a real é 64,8 | incluir `2^((nota−root)/12)` na conta | 3 |
| D11 | Grave "na régua" e bateria "muito baixa" | 3 rodadas | 20–60 Hz +0,30 dB vs Fox, mas 5–12 kHz 16,6 dB abaixo: hats a −14 dB e LP 5,1 kHz no kick | medir por banda contra a referência antes de subir o grave | 3 |

## 8. Arranjo e orquestra — "colado", "reto", "o drop não chega", "sumiu no registro"

| ID | Sintoma | Custo | Causa medida | Primeiro check | Lei |
|---|---|---|---|---|---|
| E1 | 1:00 bate menos que 0:30 | 1 rodada + reversão | Cortou um open hat de tensão, o riser aprovado (velocity 93→108 em 11 disparos); o salto caiu de +2,3 para +0,2 dB | classificar função (sustenta/constrói/decora) antes de cortar | 5 |
| E2 | "Muito colada, não tem respiro" | 1 plano reescrito | A versão anterior tirava 10,8 camadas por bloco de 8; a atual tirava 3,2 e o RMS variava +0,3 dB | contar camadas ativas por bloco de 8, não RMS | 6 |
| E3 | "Vácuo perfeito de 4 tempos" que não chega ao áudio | 3 sessões · 7 pareceres | 0 notas de kick/sub, mas −11,54 dBFS: camas, risers e chants atravessam o compasso | medir o LF por 1/16 dentro do vácuo | 6 |
| E4 | "O kick vai sozinho" | 3 sessões | O kick é 4/4 constante e a escola de referência também: o problema é o entorno — 15/16 células ocupadas e offbeat com 4 donos | contar células vizinhas antes de swingar o kick | 5 |
| E5 | "A faixa soa lenta" → meta de ≥10 onsets/s | 2 rodadas em direções opostas | O teto medido na referência é 6,99/s; a escuta já media 12,08/s, 1,7× acima | checar o teto da régua antes de transformar 10/s em meta | 3 |
| E6 | "Reto e previsível" no miolo | 1 rodada | 9 vácuos idênticos de 2 tempos cortando 13 pistas; a referência varia 1, 2, 3 e 6 compassos | variar duração e conteúdo das quebras | 6 |
| E7 | Dogma "topo percussivo não cai" | 2 rodadas | Nos 13 buracos medidos na versão anterior a rítmica inteira cala junto; 9 começam no 3º tempo | medir o corte na referência, não obedecer doutrina | 3 |
| E8 | Hat "flutuante" | 1 rodada | Loop idêntico a cada tempo e crescendo só no fader (−23 dB) | olhar o padrão antes do fader; medir o std por compasso | 6 |
| E9 | Breakdown lido como "o ponto de maior pressão" | alvo em aberto | A referência cai 4,9 dB e troca o dono (melodia −3,5 no break, −17,5 no drop); o set em produção cai 24 dB | comparar nível da mix e dono, não do elemento | 5 |
| E10 | "A orquestra tá matando a música" | 1 rebuild | 18 camadas entram juntas no compasso 456; a seção muda a cada 3,7 compassos (refs 8,8–16,1) | escalonar entradas em 1–2 compassos e manter um fio | 6 |
| E11 | O drop "não salta" | 1 board + 6 dias | O build 17–32 está a 2,1 dB do drop; b31/32 pica 2,3 dB acima dele | tirar peso do build, não abrir o LP do sub no downbeat | 6 |
| E12 | Solista inaudível | 1 reescrita reprovada | Escrito em MIDI 49–57, o registro com 8 canais em cima | contar notas por canal e por registro na janela | 8 |
| E13 | Kamancheh "uma oitava abaixo" do kanun | 2 causas + 1 reescrita | Registro, não EQ: preset do kanun com `Osc A/B octave=−1` e o parceiro em 0 = 12 semitons | comparar `octave=` dos dois presets antes do EQ | 8 |
| E14 | "Está distoando do bloco" | 2 rodadas | Tudo dentro da escala, mas 2 pistas colidiam: 68/73 (uníssono com o pitch do lead) e 61/62 (uníssono com o topo do kanun) | cruzar pitches dos canais com lead e kanun antes de acusar escala | 8 |
| E15 | Lead "morre do nada, sem resolução" | 1 reescrita inteira | A frase terminava na 5ª (G#4) segurada, sem envelope; 8 blocos do kanun também fecham em G#3 | ler a última nota de cada clipe | 9 |
| E16 | Orquestra "plástica" / cello áspero | 3 pistas · 2 sessões | Patch sintético em pista acústica, 1–3 oitavas abaixo; cello com Octave −1 gerando 34 Hz | solo + ler oscilador e oitava antes de reverb/EQ | 8 |
| E17 | Kamancheh "quack" | 1 expurgo | Arco acústico picado em staccato <0,5 beat no grid | arco não se pica no grid | 8 |
| E18 | Kanun "menos metálico" | 1 rodada | Reverb DESLIGADO (instrumento seco vira clique) + EQ +5,8 dB @1,7 kHz + Saturator drive 0,5 | ler Device On do reverb antes do timbre | 1 |
| E19 | Cello "leva sozinho, fica repetitivo" | 1 rodada | 6 dos 9 devices OFF, inclusive Reverb e EQ já ajustados | ler `[(d.name, d.is_active)]` antes de compor parceiro | 1 |

## 9. Pedido e processo — "não era isso", "você religou", "não mudou nada"

| ID | Sintoma | Custo | Causa medida | Primeiro check | Lei |
|---|---|---|---|---|---|
| F1 | "Arruma isso" virou redesenho | 1 rodada + reversão | "Arruma" = restaurar o estado que funcionava; o assistente redesenhou | devolver o estado anterior, não melhorar | 10 |
| F2 | "Melhorar" executado como troca mecânica | 1 rodada reprovada | Correção de −12 st quando o pedido era refazer partitura e timbre ("melhorar não só trocar") | refazer conteúdo e buscar no acervo instalado | 5 |
| F3 | O trecho aprovado mudou | 1 sessão | Depois do elogio, o sampler de um canal virou outro sintetizador com patch de braam e um reverso foi mutado | capturar 8 compassos do aprovado antes de trocar fonte | 11 |
| F4 | "Desativei canais e você reativou" | 1 rodada | O assistente "restaurou" o que parecia quebrado e religou 13 mutes que o produtor tinha desligado | espelhar os mutes dele | 11 |
| F5 | Pedido era para o set de referência; executou em outro set aberto | 1 sessão | A música-alvo não é o set que está aberto | repetir o set-alvo em 1 linha antes de mutar | 3 |
| F6 | Reportou "pronto" com o compasso 422 vazio | 1 rodada | Escreveu no bloco 1–225 e não reabriu o alvo pedido | provar 1 nota no compasso citado antes de reportar | 10 |
| F7 | "Demais" lido como excesso quando era "e o resto" | 1 rodada | Polaridade: 36 usos intensificadores × 19 de enumeração em 1.402 mensagens | classificar elogio/reprovação/lista antes de corrigir | 2 |
| F8 | "Tá roubando a cena" | 1 rodada | Percussão sintética em 0 dB, o mesmo fader do kick, enquanto o elemento substituído vivia em −26 dB | repor o papel (fader, banda, duração), não só baixar | 5 |
| F9 | 33 mudanças de mix e "não notei diferença" | 2 rodadas | Tudo na mesma célula C#/D/G# e poucos dB: um mascara o outro | 1 mudança de 6 dB audível antes de empilhar 33 de 1 dB | 4 |
| F10 | Plano de 13 remoções e 2 adições: "senti quase nada" | 4 h · 33 mudanças | As 2 adições nunca foram aplicadas; o plano era majoritariamente subtrativo | contar remoções × adições e conferir se as adições foram executadas | 6 |
| F11 | 22 de 62 mapas de dissecação fora da lei | 62 mapas auditados · 14 conflitos | O briefing não mandava ler as regras do projeto (cânon, gate, biblioteca); cada subagente decidiu | 3 linhas de "leia isto" + campo obrigatório "conflito com a escola" | 10 |
| F12 | Nota final da madeira "não ficou boa" | 34 notas revertidas | A varredura de choques de 2ª menor (135→~4) reescreveu as notas finais, onde o atrito é resolução | tratar nota final de frase como exceção da regra | 9 |
| F13 | Script canônico "homologado" quebrou com `ModuleNotFoundError` 9 dias depois | 1 rodada de restauração | O ambiente Python do script morava na área de artefatos (já limpa uma vez) e o catálogo de ferramentas continuava prescrevendo o caminho morto; nada no doc marcava a perda | antes de usar script canônico, provar o runtime que ele chama: o venv existe e o import do motor funciona; ambiente de ferramenta NUNCA na pasta de artefato | 10 |

## 10. Regras operacionais assumidas por este mapa

- **Segurança do Set antes de qualquer mutação:** backup do arquivo, um escritor por vez, read-back depois de
  cada mudança, e prova de salvamento (data de modificação) — a interface não salva por você.
- **Unidade certa antes de comparar:** valor cru do arquivo vs valor normalizado na UI é armadilha clássica;
  fade e automação que não sobrevivem ao save não são prova.
- **Método sintoma → causa medida → prova:** primeiro o check de 60 s (§1), depois a mudança pequena com
  antes/depois documentado.
- **Soberania da escuta:** métricas e gates são diagnóstico técnico, não aprovação artística — a decisão
  final é de ouvido.
- **Régua numérica existe em doc próprio do estúdio**; aqui os números citados são sempre os medidos nos
  casos de origem.

## 11. Fontes

Compilado em 30/10/2026 a partir de auditorias de sessão, decisões registradas e memórias de projeto entre
15/09 e 31/10/2026, por 13 leitores independentes — 233 casos brutos antes da deduplicação. As fontes
originais (transcrições de rodadas, board rooms, auditorias forenses, registros de decisão e diários de
execução) ficam no repositório de origem e não acompanham este pacote.
