# Cursos — o que cada um acrescenta

**Use quando** a frente de trabalho pedir uma demonstração completa (não um truque isolado): escolha de escala, kick/sub, arranjo, automação ou mastering. Cada curso tem um mapa com timestamps e trechos de prova; os mapas completos não acompanham este pacote — este documento é o resumo operacional.

## 1. Future Media — Psychedelic Techno Production with Re:Set

- **Fonte:** curso em vídeo 3h12, transcrição ASR completa (mapa não incluído no pacote).
- **O que acrescenta a um arranjo de referência de ~2 min:**
  1. **Um kick + um sub bastam.** O curso é explícito: eles já ocupam o grave; não somar 808 nem camada nova. A camada de sub de referência já faz esse papel.
  2. **Macros/automação embutidos no som** — mapear decay, filtro e send nas camadas de baixo/stab/madeira e automatizar ao longo dos 64 compassos; evolução sem camada nova, preservando os offsets do bolso de referência.
  3. **Conteúdo no gap 300–4.000 Hz** — beep/alarme curto (seno + transiente 5 ms) e respostas de madeira/stab nos buracos do bolso; preencher com conteúdo, não com EQ.
  4. **Separação por oitava** — não duplicar o baixo; material novo em C#3–C#4, sem +12/+24 cego.
  5. **Kick+sub consistentes e medidos** — mesmo som em todo hit; decay em ms; reverb de 1 compasso = 1,875 s a 128 BPM; conferir fase.
- **Conflitos:** o curso demonstra em **F harmonic minor** e afina drums em F 43,7 Hz — não transplantar; o 808 separado contraria o princípio "um kick + um sub"; hats em 4–7 camadas colide com o teto de densidade de topo; riser de noise precisa da forma curta/extinta antes do downbeat; sub FM em C#1 põe harmônico em 69,3 Hz, banda sensível do grave.
- **Teste mais barato sugerido pelo mapa:** beep/alarme + macros na camada de baixo, sem tocar em kick/sub.

## 2. Future Media — Advanced Synthesis with Will O Wisp

- **Fonte:** curso em vídeo 3h11, transcrição ASR completa (3.812 falas; mapa não incluído no pacote).
- **O que acrescenta a um arranjo de referência de ~2 min:**
  1. **Wavetable por posição, não por nota** `[00:56:54]` — o timbre muda com a nota e a levada `.27/.77` fica travada. Rota barata de movimento para a camada de baixo (Serum 2) sem criar camada nem banda nova.
  2. **Random + Scale + gravar MIDI** `[02:09:04]` — ideação de frases de 2–3 notas que depois viram nota editável. Serve ao miolo 300–4.000 Hz, com Scale na escala frígia do projeto e teto na oitava 4.
  3. **Gravar áudio e salvar preset de cada som aprovado** `[03:01:05]` — documentar cada som aprovado na prática; evita perder patch de Serum 2 entre A/B.
- **Limite honesto:** 31% das linhas são loop de ASR e dois trechos estão inutilizáveis (`00:12:35–00:28:25` e `02:21:33–02:30:03`), incluindo a montagem do patch subtrativo. O curso **não dá nenhum valor de operação** (threshold, ratio, dB, profundidade) — nada dele virou número de receita.
- **Conflitos:** FM inarmônico/bell (timbre metálico); saw no grave; delay curto em kick+bass; random no pitch; melodia C4–C6 acima do registro de referência; grain freeze de kick+bass (não é camada de grave).
- **Quando entrar:** frente de **textura/atmosfera** e **síntese** — sound design de camada, não de motor.

## 3. Sonic Academy — How To Make Ambient with Bluffmunkey

- **Fonte:** 14 aulas, 2h44, transcrição ASR com marcador por aula (22.232 palavras; mapa não incluído no pacote).
- **O que acrescenta a um arranjo de referência de ~2 min:**
  1. **Camada por família** — synth + sample + instrumento real (madeira, atmosfera, stab) para ocupar os 300–4.000 Hz com **conteúdo tocado**, não com EQ.
  2. **Máscara se resolve tirando** — HP em pads e cordas, mono do low-end, corte da fundamental que briga — antes de somar qualquer camada nova.
  3. **Evolução lenta** por automação de mod wheel/cutoff por clipe e performance ao vivo com compensação de ataque em madeira/stab, sem mexer no bolso.
- **Conflitos:** o mais importante: **pad longo mascara o gap** em vez de preenchê-lo, e reverb como estrutura atenta contra o mono do grave e contra os respiros escritos do arranjo.
- **Quando entrar:** frente de **atmosfera/cama**, **orgânicos**, **strings/modulação** e **master**. É ambient: serve à camada, nunca ao motor rítmico.

---

**Regra de uso:** curso é **fonte**, não lei. Antes de aplicar, passar pela seção de conflitos/cautelas do documento da frente correspondente.
