# How to Write Better Melodies by Starting with Rhythm First

**Canal:** Sonic Academy · **Vídeo:** `rSorLiUr6xI` · **Duração:** 9:17 (557 s)
**Série:** trecho de Tech Tips Volume 111 "Composing Melodies", com Larry Holcombe (descrição do vídeo)
**Legenda:** automática (en-orig), 457 cues, 00:00:02.560 → 00:09:11.571. Tem legenda.

---

## Técnica ensinada (2-4 frases)

O vídeo propõe compor a melodia começando pelo **ritmo**, não pelas notas: bater palma ou desenhar o ritmo primeiro e só depois escolher as alturas, porque o mesmo motivo com outro ritmo deixa de ser reconhecível — o exemplo é "Happy Birthday" com as mesmas notas em ritmo aleatório [00:00:57.990]–[00:01:03.520]. A melodia é tratada como **linguagem**: frase-pergunta que sobe, frase-resposta que desce [00:04:26.400], e "call and response" também com os outros elementos (baixo, acordes, teclado) [00:02:57.040]–[00:04:05.910]. O **silêncio é parte da melodia**: no exemplo "ruim", ele preencheu todo o espaço e o resultado virou monólogo sem conversa [00:02:27.760], [00:03:11.760]–[00:03:15.120]; no exemplo "bom", os rests são tocados como parte da frase [00:05:57.199]–[00:06:02.000]. Fecha com **espelhamento rítmico** (mesmo ritmo repetido) e **variação só no fim**, alternando a cada duas vezes para não ficar previsível [00:07:30.560], [00:08:25.510].

> Ressalva de fonte: a legenda é automática e tem erros de reconhecimento ("pictures" por "pitches" em [00:00:59.120], "bassing chords" em [00:05:40.560], "jays" em [00:00:33.440]). As citações abaixo são literais do arquivo, com o erro preservado.

---

## Ferramenta usada no vídeo (plugin/stock)

**O vídeo não nomeia nenhum plugin, DAW ou instrumento de marca em nenhum ponto da legenda.** O texto inteiro foi varrido por `serum|ableton|logic|bitwig|plugin|piano roll|midi|quantiz|grid|preset|synth|sample|velocity|scale|tempo|bpm` e as únicas ocorrências são "keyboard" (teclado físico) e "pentatonic scale" — nenhuma citação de plugin ou host.

O que a legenda efetivamente mostra como ferramenta:

- Um backing "simple drum and bass idea" [00:01:09.280] — bateria e baixo simples servindo de leito.
- **Palmas** como sketch rítmico: "so you could start off and actually try and just clap a rhythm to get yourself going" [00:01:16.720]–[00:01:21.920].
- Um part de teclado **tocado à mão**, não programado: "I played this in on the keyboard" [00:05:10.720], descrito como "staccatoish electric piano part" [00:05:16.800]–[00:05:19.039] (timbre não identificado pelo autor).

Ou seja: o método é DAW-agnóstico. **Nada a substituir** — a tradução abaixo é de método, não de plugin.

---

## Notas de método (tradução para qualquer DAW)

### 1. Sketch só de ritmo (o passo que o vídeo coloca antes das notas)

- Criar um clipe MIDI de 4 compassos no canal do lead e desenhar o ritmo **numa nota só** (ex.: a tônica em oitava média), sem escolher alturas — equivalente digital das palmas do vídeo [00:01:16.720]. Tocar o sketch com um timbre provisório simples (oscilador único, decay curto); nenhum som definitivo ainda.
- Só depois distribuir as alturas do vocabulário harmônico do projeto (2–3 notas) sobre o ritmo já escrito. Isso separa as duas decisões — que é exatamente o argumento do vídeo de "rather than starting with the notes" [00:01:45.680]–[00:01:47.119].

### 2. Timbre para o comportamento "staccatoish electric piano" (sem marca no original)

- Notas curtas (a pergunta): timbre de ataque curto — biblioteca de corda/guitarra pinçada, ou patch com decay curto e sustain baixo.
- Notas longas (a resposta): timbre sustentado — keys atmosféricos ou órgão.
- Critério geral: não mascarar o método — notas curtas reconhecíveis, sem brilho, sem unison largo/detune (some com o contorno).
- **Nada de granular no lead** — granularidade destrói o contorno que o vídeo quer audível.

### 3. Call-and-response com dois "falantes"

- Duas instâncias do mesmo patch: **pergunta** (mais aguda, notas curtas, sobe) e **resposta** (mais grave, uma nota longa, desce) — a regra "questions go up and answers go down a lot of the time" [00:04:34.639]–[00:04:36.800].
- **AutoPan** só na resposta, movimento lento e raso, para separar os dois falantes sem virar efeito.
- **Echo** em send, 1 repetição baixa e filtrada, alimentado só pela última nota da resposta — o rest fica preenchido por cauda, não por mais notas (o vídeo insiste que o rest é parte da melodia, [00:05:57.199]).
- **Reverb** discreto no retorno, com predelay, para o silêncio ter profundidade em vez de ser seco.

### 4. Espelhamento + variação

- Duplicar o clipe e mexer **só no fim** da segunda repetição — "a little bit at the end for variation" [00:07:35.680], alternando a cada duas voltas [00:08:25.510]. No Live: segundo clipe na mesma pista, editar a última nota/último tempo.

### 5. Escala — o que **não** importar

O exemplo do vídeo é "all pentatonic" [00:03:41.360]. Importa-se o método rítmico/frasal, não o conjunto de notas: cada projeto aplica os graus do seu modo.

---

## Notas de aplicação (por função)

### baixo/rolling
O vídeo trata o baixo como **interlocutor**, não como leito: há um trecho em que a legenda automática lista "bassing chords melody" [00:05:40.560], depois "answer" [00:05:44.800] e "bass" [00:05:46.400] — a narração descreve acordes, melodia e baixo se respondendo em sequência, e conclui "all these little conversations that are going on within the music and that's all creating space" [00:05:47.680]–[00:05:50.880]. Tradução: a melodia **responde depois** da frase do rolling, nunca por cima de cada nota dele. Nas subdivisões do baixo, o lead fica em silêncio — o baixo é quem "fala" ali.

### percussão de resposta
É o "outro falante" que já existe no arranjo. O vídeo mostra a conversa acontecendo **entre elementos** [00:04:05.910]–[00:04:07.439], não só dentro da melodia. Tradução: quando a percussão de resposta entra, o lead **cala** (rest escrito, não só volume baixo) e vice-versa — nunca os dois respondendo no mesmo tempo.

### madeira
Mesma lógica da percussão de resposta: a madeira pode ser o segundo falante (pergunta do lead → resposta da madeira). O vídeo não fala de timbre de madeira; a contribuição aqui é só **de função** (quem responde quando), não de som.

### stab
O vídeo descreve acordes respondendo ao baixo [00:05:40.560]–[00:05:46.400]. Tradução: stab curto **no buraco** da frase de baixo, uma vez por compasso no máximo, funcionando como resposta — não como preenchimento contínuo. Stab em bloco a cada tempo é exatamente o "monólogo" que o vídeo reprova [00:03:11.760].

### atmosfera
O vídeo não fala de pads ou camadas. A transferência possível é negativa e útil: **o rest é onde a atmosfera aparece**; usar a ambiência já existente (reverb/retorno) para preencher o silêncio, em vez de escrever mais notas. A cauda de delay/reverb deve caber dentro do rest, não invadir a frase seguinte.

### Regras de frequência para aplicar sem engordar o sub nem metalizar

1. **Fundamental do lead em oitava média** (ex.: C#4–C#5 ≈ 277–554 Hz) — em um projeto com vale de médios medido, essa faixa é a que falta; não tocar a melodia uma oitava abaixo "para dar corpo": isso só engorda o low-end.
2. **High-pass no canal do lead em ~180–220 Hz, 24 dB/oct**, e **nenhuma camada sub/oscilador grave no patch**.
3. **Unison 1, detune 0** nos sintetizadores; detune largo cria a "parede" que o vídeo chama de monólogo e some com o contorno.
4. **Sem brilho metálico**: evitar FM, comb filter, ressonância alta e exciter no lead. Se faltar presença na faixa 1.200–4.000 Hz, subir presença com **saturação suave** e filtro, não com distorção de alta ordem nem realce fixo em 3–5 kHz.
5. **Groove**: escrever a melodia na mesma grade deslocada do projeto quando ela dialoga com hats/shaker; não quantizar a resposta para semicolcheia reta, o que apagaria o deslocamento. (O vídeo não fala de microtiming — isto é regra de projeto com groove próprio, não do vídeo.)

### Receita mínima (proposta deste mapa, não do vídeo)

Compassos 1–8: 2 compassos de **pergunta** (3 notas ascendentes do vocabulário, nas subdivisões deslocadas), 2 compassos de **resposta** (as mesmas 3 notas descendo, a última longa), 1 compasso de **silêncio total do lead** deixando a percussão de resposta falar, e repetição com variação só no último tempo a cada duas voltas.

---

## Prioridade e esforço

- **Prioridade: baixa/média.** Em um motor que raramente depende do lead e limita a melodia a 2–3 notas, o vídeo ainda não é descartável: o par "rest como parte da frase" + "call-and-response entre elementos" serve direto para posicionar **percussão de resposta e stab**.
- **Esforço: baixo.** Só edição MIDI, mutes e escolha de patch entre os que já existem; nenhum plugin novo, nenhum sound design profundo, nenhuma automação. Estimativa: 1–2 h para escrever e comparar A/B.

---

## Trechos de prova

1. **[00:01:16.720]** — "so you could start off and actually try and just clap a rhythm to get yourself going" (continua em [00:01:20.479] e [00:01:21.920])
2. **[00:02:57.040]** — "what's super important in melodies is call and response" (continua em [00:02:59.280]: "melodies is call and response. Melody")
3. **[00:05:57.199]** — "I'm trying to include the rests the silence in the melody so that the rests are a part of the melody" (continua em [00:06:00.000] e [00:06:02.000])

---

## Limitações declaradas

- Legenda automática (ASR): há erros de transcrição preservados nas citações; nenhuma citação foi corrigida "para o sentido".
- O vídeo **não nomeia** plugin, DAW, BPM, velocity, automação ou processamento — tudo o que este mapa atribui a timbre, EQ, pan ou delay é **tradução**, não conteúdo do vídeo.
- "Ferramenta usada no vídeo" fica sem marca por ausência de evidência na legenda; não foi possível confirmar o DAW por outra via sem assistir ao vídeo.
