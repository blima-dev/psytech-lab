# How I Arranged Hypnotic Techno Track - Arrangement Breakdown

**Canal:** Hypnotic Techno Production · **Vídeo:** https://www.youtube.com/watch?v=6x1_XZDcI8I
**Fonte:** legenda automática em inglês (348 cues após dedupe). `temLegenda = true`.
**Nota de leitura:** a legenda é automática; "high heads" = hi-hats, "aonal" = atonal, "cutff" = cutoff, "flounder/flander" = flanger, "Perks flash" = perc flash. Marcadores `[music]` foram removidos das citações; o texto das palavras é literal.

## Técnica ensinada (2-4 frases)

O arranjo é construído em camadas **frase a frase, sem trocar o groove**: a camada nova entra com uma **curva de volume** em vez de entrar "no tempo" — *"sometimes it's it's nice to add them a bit of like a curve, a volume curve"* [00:09:17], *"this way the sounds like blends uh rather than like starts"* [00:09:30]. O elemento central é um **drone com muitos LFOs**, no qual ele toca uma nota só e deixa o movimento vir da **filter automation gravada à mão** [00:06:42–00:07:09], somando 2–3 notas extra para criar dissonância em vez de harmonia [00:07:21–00:07:40]. A variação de energia vem de **trocar a sequência/instrumento mantendo a mesma grade rítmica** — *"we keep keep the groove going by but just swapping the instrument"* [00:18:35] — e de **contraste por subtração**: sobe cutoff + soma ruído para o clímax [00:11:50] e tira o agudo antes do drop, *"we need that contrast in highend. No highend"* [00:16:43–00:16:45]. Por fim, ele **remove camadas** que roubam atenção em vez de empilhar, porque o track vive em DJ set e precisa de espaço negativo [00:21:30–00:22:34].

## Ferramenta usada no vídeo (plugin/stock)

- **Ableton Live** (Arrangement View) — *"let's switch to Ableton and let's listen to the arrangement"* [00:00:29].
- **u-he Frequency Shifter** (versão antiga) sobre um **ride 909 com reverb** — *"It's just a ride 909 ride with a bit of uh reverb on it. And I'm using the old edition of U frequency shifter"* [00:15:48–00:15:58]; ele mesmo pondera se o efeito é do frequency shifter ou de um flanger — *"or maybe flanger does it. Yeah, flounder does it"* [00:16:12–00:16:14].
- **Filter automation de clip** (não é plugin) — *"not volume automation but filter automation which is again super rudimentary uh but it works"* [00:16:23–00:16:30].
- Amostras: ride 909, hi-hats (camada "snappy" + camada de corpo) [00:08:31–00:08:37], shaker loop para o *perc flash* [00:20:30–00:20:32], ruído para o clímax [00:11:50].
- **Nenhum** ANA 2, VELA, SideKick, Kick 3 ou Bitwig aparece ou é citado no vídeo. O único dependente externo é o u-he Frequency Shifter — conceito coberto nativamente pelo **Shifter** do Live 12.

## Tradução para Live 12 nativo, Serum 2, Diva, Vital, Massive X, Surge XT e Kontakt 8

O vídeo não depende de nenhum plugin que falte num arsenal típico de psytech. Tradução item a item:

| O que o vídeo faz | Equivalente | Como |
|---|---|---|
| Drone de 1 nota com "a lot of LFOs" modulando o som [00:06:42] | **Serum 2** (2 LFOs → cutoff e posição de wavetable) ou **Diva/Vital**; **Kontakt Ethereal Earth** para o atmo por baixo | Nota longa, release alto; LFO lento/sincronizado no cutoff; gravar a automação de filtro como clip envelope no Live |
| Filter automation gravada à mão + edições manuais no drone [00:06:54–00:07:06] | **Live 12 AutoFilter** (ou cutoff do Serum) com **clip envelope** desenhado/gravado | Automação de cutoff em 2–3 pontos por frase; nada de LFO no lugar da automação — o vídeo usa as duas coisas juntas |
| Notas extras criando dissonância (G, D#, D, G#) [00:07:30] | Qualquer pad/drone (**Serum 2**, **Surge XT**, **Kontakt Ethereal Earth**) | Segurar 3–4 notas em intervalos de 2ª menor/3ª menor, sem resolver o acorde; transpôr para a tonalidade da track em produção |
| Duas camadas de hi-hat (uma "snappy", uma de corpo) [00:08:22–00:08:37] | **Live 12 Simpler/Sampler** com dois one-shots; **AutoPan** para separar | Camada A curta/estalada, camada B mais escura com decay; mesma sequência nas duas |
| Entrada de camada com curva de volume [00:09:17–00:09:33] | **Automação de volume de clip/track no Live** | Fade de 1–2 compassos subindo no ponto de entrada, em vez de nota "no downbeat" |
| Ride 909 + reverb + frequency shifter/flanger [00:15:48–00:16:14] | **Live 12 Shifter** (modo Frequency Shifter) + **Echo** + **Hybrid Reverb** | Shifter com shift pequeno e LFO lento; Echo com filtro no feedback; reverb curto |
| Trocar a sequência de instrumento mantendo o groove [00:17:43 / 00:18:35] | **Live 12**: mesmo clip MIDI roteado para outro instrumento (Simpler, Serum 2, Kontakt) | Duplicar o clip e trocar só o device; a grade rítmica fica intocada |
| Efeitos por frase: hi-hat splash com feedback grande, perc flash de shaker loop [00:20:05–00:20:32] | **Live 12 Echo** (feedback alto + filtro) sobre 2–3 notas de hat; **Simpler** com trecho de shaker | Feedback ~60–70% com LP no caminho de feedback; usar uma vez por frase |
| Contraste de agudo antes do drop [00:16:43–00:16:45] | **Automação de mute/filtro** (AutoFilter HP, ou mute da track de hats) | 1–2 compassos sem topo antes da subida/drop |
| Ruído somado ao subir o cutoff para o clímax [00:11:50] | **Live 12 Grain** ou **Serum 2** (Noise/GranularOsc) + **Hybrid Reverb** | Ruído filtrado subindo junto com o cutoff; cortar no drop |
| "Esconder" a camada que já tem automação própria [00:13:34–00:13:47] | **Automação de volume** na camada redundante | Abaixar o elemento antigo quando o novo já carrega o movimento |

## Aplicação por função (kick, sub, baixo/rolling, hats/shaker, percussão de resposta, madeira, stab, subida, atmosfera)

Contexto de referência citado no levantamento original: um set de trabalho medido mostrou o meio carente (300–1.200 Hz e 1.200–4.000 Hz abaixo da média de 6 referências externas), low-end mono e groove com subdivisões deslocadas a preservar.

Regra que atravessa tudo: o vídeo **não repete loops nem sequências** (*"I'm not repeating the same loops uh or the same sequences. You see, I'm playing with different sequences"* [00:15:23–00:15:27]) mas **mantém a grade** (*"I'm keeping the groove going. It's fairly the same"* [00:15:28–00:15:32]). Traduzido: **o groove deslocado não se mexe; muda só o timbre/sequência em cima dele**. Toda variação abaixo é automação ou troca de fonte — nenhuma acrescenta nota ao sub.

| Função | O que o vídeo autoriza | Como aplicar | Cuidado (sub / brilho metálico) |
|---|---|---|---|
| **Kick** | O vídeo não trata kick. A técnica transferível é o contraste por subtração antes do drop [00:16:43] e a filter automation "rudimentar que funciona" [00:16:23]. | Antes da subida/drop: automar o **HP/mute do topo** (hats e perc) por 1–2 compassos. Não mexer no corpo do kick. | `INFERÊNCIA`: mexer no topo do kick aqui só cria pico em 1,2–4 kHz. Sub permanece mono e intocado. |
| **Sub** | O vídeo não trata sub. O princípio aplicável é o de **remover** o que rouba atenção [00:21:30–00:21:53], não empilhar. | Manter **uma** fonte de sub. Se entrar drone/atmo, **high-pass em ~150–200 Hz** nele. | Não copiar a ideia de "duas camadas" para o grave: o vídeo só aplica duas camadas em hi-hat [00:08:22]. Low-end segue mono. |
| **Baixo/rolling** | Trocar o instrumento sobre a **mesma** sequência [00:17:43 / 00:18:35]; variação de sequência usada **só naquele momento** [00:18:44–00:18:54]. | Duplicar o clip do rolling, manter as notas do groove idênticas e trocar só o device (Serum 2 → Diva, ou um take de Surge XT). Uma variação de sequência, uma vez, na virada de frase. | Troca de fonte muda o conteúdo harmônico — conferir que a fundamental não sobe para a faixa do sub. Sem saturação nova. |
| **Hats/shaker** | **Duas camadas**: uma "really snappy" e uma de corpo [00:08:22–00:08:37]; entrar com **curva de volume**, não no downbeat [00:09:07–00:09:33]; efeito de splash por frase com feedback grande [00:20:05]. | Camada A curta e seca; camada B mais escura (decay maior). Entrada da camada B com fade de 1–2 compassos. Sequência alternativa por frase, mesma grade. Ride 909 + **Shifter** (modo Frequency Shifter, shift pequeno, LFO lento) + **Echo** com filtro no feedback. | Esta é a função de maior risco de **brilho metálico**: o frequency shifter gera conteúdo inarmônico. Shift pequeno, wet baixo, LP depois; o próprio autor reclama que os efeitos são *"kind of like harsh here and there"* [00:19:44] e que o ajuste seria para que *"they don't sound so splashy, so noisy"* [00:19:55]. |
| **Percussão de resposta** | **Perc flash** feito a partir de um shaker loop [00:20:30–00:20:32]; efeitos "every kind of phrase" [00:19:23]. | Recortar 1 golpe de shaker, mandar em **Echo** com feedback alto e filtro no feedback; usar como resposta uma vez por frase, em volume baixo. | Feedback alto sem LP vira wash em 1,2–4 kHz — manter LP no loop de feedback. Não dobrar com o splash do hat no mesmo tempo. |
| **Madeira** | Drone de nota única com LFOs + **filter automation** + notas extras dissonantes [00:06:42–00:07:40]; mantido 2–3 frases sem cansar *"because we have automation and we have the added notes"* [00:12:28–00:12:32]. | Uma nota longa de madeira (Kontakt Rubber Bridge / LOOP GARDEN, ou Serum 2) com LFO lento no filtro; automação de cutoff em 2–3 pontos; 2 notas extras em 2ª menor para tensão. | Notas extras só acima de ~200 Hz; se descerem para o sub, cortar. A dissonância é intencional, não é "acorde" a resolver. |
| **Stab** | Trocar o instrumento na mesma sequência e usar aquela sequência **só ali** [00:18:35–00:18:54]. | Um stab com a mesma figura rítmica do groove, aparecendo uma vez por bloco; ao trocar de frase, troca o device em vez de somar um segundo stab. | Stab curto com LP; evitar camada de ruído junto (soma em 1,2–4 kHz). |
| **Subida** | Subir o **cutoff** e **somar ruído** para criar intensidade, e então **tirar o agudo** (*"No highend"*) antes do drop [00:11:50 / 00:16:43–00:16:45]. | Riser = AutoFilter/Serum cutoff subindo + Grain/Noise entrando; nos 1–2 compassos anteriores ao drop, **mutar hats e perc** (contraste por ausência). | É a aplicação mais segura para um perfil escuro de médios: o drop ganha impacto **sem** adicionar brilho — o contraste é feito tirando, não pondo. |
| **Atmosfera** | Miolo hipnótico com **só drone + atmo** [00:12:01–00:12:10]; variação por automação e notas extras; remover o som que rouba atenção [00:21:30–00:21:53]. | No trecho sem kick, deixar drone + atmo com automação de filtro e uma nota extra entrando por frase. Quando entrar o novo elemento rítmico, **abaixar** ("hide") a camada antiga [00:13:45]. | Atmo com HP em ~150–200 Hz. Nada de reverb longo no grave; reverb só no que já está acima da faixa do sub. |

**Princípio de mix que o vídeo declara:** menos camadas = mais dinâmica — *"There is more dynamics, there is more um silent moment and filled moment"* [00:22:25–00:22:34], e tracks cheios de som *"wouldn't sound good"* [00:22:44–00:22:45]. Para um set com meio deficiente, isso indica: em vez de preencher 300–1.200 Hz e 1,2–4 kHz com camadas novas, o caminho do vídeo é **trocar** o que já está lá e criar silêncio antes do drop.

## Prioridade e esforço

Prioridade da frente: **média (P2)** — é breakdown de arranjo, não desenho de som do motor. Esforço: **baixo** — quase tudo é automação/roteamento no Live, sem sound design novo.

| Item | Prioridade | Esforço | Justificativa |
|---|---|---|---|
| Contraste por subtração de agudo antes do drop [00:16:43] | **alta** | **baixo** | Uma automação de mute/filtro resolve; ataca exatamente o perfil escuro em 1,2–4 kHz sem somar brilho. |
| Entradas de camada com curva de volume [00:09:07] | **alta** | **baixo** | Fade de 1–2 compassos no clip; muda a percepção de "blend" vs "start" sem tocar em timbre. |
| Manter grade e trocar instrumento/sequência [00:18:35] | **alta** | **baixo** | Duplicar clip + trocar device; preserva o groove por construção. |
| Duas camadas de hat + ride com Shifter/Echo [00:08:22 / 00:15:48] | **média** | **médio** | Exige escolher amostras e ajustar Shifter/Echo com cuidado para não gerar brilho metálico. |
| Drone com filter automation + notas extras [00:06:42] | **média** | **médio** | Depende da frente de atmosfera; a automação é rápida, a escolha das notas dissonantes exige escuta. |
| Efeitos por frase (splash, perc flash) [00:19:23–00:20:32] | **baixa** | **baixo** | O autor classifica os próprios efeitos como harsh/splashy [00:19:42]; risco alto de piorar o brilho. |
| Remover camada redundante ("hide") [00:13:45 / 00:21:30] | **alta** | **baixo** | Só automatiza volume; é o que mais aproxima do "menos bateria, mais espaço" do minimalismo. |

## Trechos de prova

1. **[00:06:42]** — *"because there is a lot of LFOs going on that modulate this sound. I could play one note and just uh just just make it drone uh drawn with one note but um I have filter automation here that I recorded while I was doing the recording of this arrangement"*
2. **[00:09:07]** — *"And what I did here was actually like to add layers, not the sometimes it it's nice that they start like bang on the new new beat, but sometimes it's it's nice to add them a bit of like a curve, a volume curve."*
3. **[00:18:35]** — *"Yeah. So we keep keep the groove going by but just swapping the instrument. And this is one of the most effective way I always tell my students you can use that."*
