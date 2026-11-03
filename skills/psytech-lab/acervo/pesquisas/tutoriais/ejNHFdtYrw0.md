# Top 5 Tips For Creating Organic Drums

**Canal:** Sonic Academy · **Apresentador:** Protoculture (Nate) · **Duração:** 15:16 · **Legenda:** automática em inglês obtida e lida via yt-dlp.
**Descrição (confirmatória):** "Using tools found in any DAW such as micro delays, randomisation and loop slicing, Nate runs through some simple methods to help make your beats less 'machine like'".

---

## Técnica ensinada (2-4 frases)

O vídeo ensina cinco blocos de técnicas para humanizar bateria programada: (1) **micro-delays** entre camadas (dois claps a +15 ms e −10 ms) para soltar o groove, com a regra de que atrasar depois do kick gera sensação "dragged"/relaxada e empurrar à frente do kick gera sensação "rushed"/apertada; (2) **randomização de posição** do shaker com faixa pequena, para ele não cair sempre nos mesmos beats; (3) **dinâmica por velocity** — programar um padrão de hats com acentos e depois randomizar velocity; (4) **variação do som em si** — pitch random sutil, *round robin* de amostras (número ímpar de camadas gera sensação quase polirrítmica; número par volta a alinhar nos beats em 4/4) e fatiar um loop gravado em slices mapeados no teclado para montar o padrão com variações; (5) passar todos os drums por um **drum bus** com o mesmo reverb, saturação e compressão para simular a mesma sala.

O próprio autor declara que o conceito é independente do DAW: "most DAWs will have similar tools so you can apply these concepts to pretty much any DAW or plugin that you wish" (00:00:14–00:00:22).

---

## Ferramenta usada no vídeo (plugin/stock)

- **Cubase** — track delays por pista (00:01:23–00:01:47), `MIDI modifiers → Random → Position` e `Random → Velocity` (00:03:29–00:04:06; 00:05:57–00:06:07), Sampler Track com botão **Slice** (00:11:06–00:11:10), group track / drum bus (00:12:50–00:13:02).
- **Groove Agent** — camadas mapeadas por velocity, botão **randomize** de pitch (00:08:02–00:08:20) e modo **round robin** (00:09:32–00:09:50).
- **ANA 2** — aparece só como fonte do acorde de preenchimento (00:00:47–00:00:49), **não** faz parte da técnica de bateria.
- **Near Verb** (como soa na legenda, descrito como "reverb assistant") + saturação + compressão no bus (00:13:08–00:13:52); **AutoPan** citado como passo extra de movimento (00:14:35–00:14:41).

---

## Tradução para ferramentas Live 12 / Serum 2

O vídeo não depende de nada exótico: Cubase track delay, MIDI modifiers e Groove Agent têm equivalentes diretos no Live 12. **ANA 2 não é necessária** (só servia de acorde); **VELA, SideKick, Kick 3 e Bitwig não aparecem no vídeo**, então não há nada a substituir.

| Técnica do vídeo | Equivalente (Live 12) |
|---|---|
| Micro-delay por clap/pista (Cubase track delay) | Campo **Delay (ms)** do mixer de cada track no Live — dois claps em duas tracks com +15/−10 ms. O vídeo também autoriza fazer "manually in the MIDI itself" (00:01:29–00:01:32): nudge nas notas do clip resolve o mesmo. Como o delay do Live é **por track**, deslocar notas individuais dentro de uma mesma track exige nudge manual ou tracks separadas. |
| Random position do shaker (MIDI modifier) | Nudge manual/aleatório no editor de notas, ou **Groove Pool** com quantidade (Timing/Random) aplicada só ao clip do shaker. Equivalente conceitual, não idêntico: no vídeo a randomização é contínua por nota. |
| Random velocity | Randomização de velocity no lane de velocity do clip + Groove Pool. Mesma lógica: offsets de ±10–15 em unidades de velocity MIDI. |
| Pitch random sutil (Groove Agent randomize) | **Serum 2** tem fontes nativas random (`random1`/`random2`) roteáveis a pitch de oscilador — ideal para shaker sintético. Em sample, **Sampler** com LFO Random/S&H → pitch (retrigger por nota dá valor novo a cada hit); Simpler aceita transpose por nota no clip. Vital/Massive X/Surge XT também servem via LFO Random → pitch. |
| Round robin de shaker (camadas + modo round robin) | **Sampler (Live)** com várias zones e `Sample Select` modulado por LFO Random (ou velocity); alternativa: 3 tracks/clips com 3 shakers diferentes alternados. **GranularOsc do Serum 2 não é round robin** — ele texturiza; use só se o objetivo for nuvem de textura, não repetição orgânica de amostra. Kontakt 8 só entra se a biblioteca escolhida já tiver round robin (não verificado nas bibliotecas citadas). |
| Slice de loop de hi-hat (Cubase Sampler Track) | **Simpler em modo Slice** (ou Slice to New MIDI Track) é o equivalente direto: fatias mapeadas no teclado, padrão montado com fatias diferentes. Também dá para fatiar no **Grain** se a intenção for textura, mas para padrão rítmico o Slice do Simpler é o caminho fiel. |
| Drum bus com mesmo reverb/saturação/compressão | **Group track** no Live + **Drum Buss** (drive/crunch/comp) ou **Saturator** + **Glue Compressor**, e um **Hybrid Reverb** curto tipo sala. **AutoPan** para o movimento que o vídeo cita no fim. Tudo nativo. |
| Papel dos synths de apoio | Diva/Vital/Massive X/Surge XT/Operator podem gerar o shaker/wood sintético que recebe o pitch random; Kontakt 8 (Rubber Bridge Guitar, Vintage Organs, Ethereal Earth) pode fornecer material orgânico para fatiar **se** o timbre for de madeira/percussão — não é o caso de órgão, que não tem transiente percussivo. LOOP GARDEN só é candidato ao método de slicing se contiver loops de percussão (conteúdo não verificado nesta sessão). |

**Conclusão de traduzibilidade:** sim. Todas as cinco técnicas sobrevivem sem Cubase/Groove Agent; o que muda é o nome do recurso. O vídeo é genérico de gênero — os números (±15/−10 ms, −78/+60, 10/10, −15/15) são demonstrações, não prescrições para psytech.

---

## Aplicação por função

Contexto de auditoria (set de referência contra a média de 6 referências do estilo): 300–1.200 Hz em **−4,83 dB** e 1.200–4.000 Hz em **−5,76 dB**; low-end mono; groove com subdivisões deslocadas fora do grid que não podem ser descaracterizadas.

*Na tabela, a coluna "O que aplicar" cita o fato do vídeo (com timestamp); a coluna "Cuidado" combina o vídeo com proteções técnicas — estas são **inferência**, não estão no vídeo.*

| Função | O que aplicar (com base no vídeo) | Cuidado para não engordar sub nem criar brilho metálico |
|---|---|---|
| **Kick** | Nada de micro-delay/random: o vídeo usa o bass drum como âncora ("we've got the bass drum anchoring it", 00:12:08) e adiciona um hat de contratempo para estabilizar quando há muita randomização (00:12:03–00:12:14). | Kick fica no grid e fora de qualquer randomização. O benefício do vídeo de "removing the transients from the claps… so that your kick drum doesn't get interfered with" (00:01:57–00:02:04) é exatamente separar transientes do kick — aplique nos claps/respostas, não no kick. |
| **Sub** | Intocado. O vídeo não randomiza o "808 style bass drum" (00:00:43–00:00:46); ele é a referência de peso. | Manter mono e fora do bus com saturação/AutoPan. Qualquer pitch random no sub destroi a pressão. |
| **Baixo/rolling** | O vídeo não trata bassline. Infraestrutura: preservar as subdivisões deslocadas do groove como estão. A regra "delay after the kick = dragged" vale para a percussão de resposta, **não** para o rolling. | Se atrasar o rolling junto, as posições deslocadas perdem a assinatura e viram lama. Mexer só no que está ao redor. |
| **Hats/shaker** | Principal alvo. Random position pequeno (o vídeo termina em −3 a +9 unidades, 00:04:53–00:05:01 — adaptar para ~1–8 ms), random velocity ±10–15 (00:05:49–00:06:34), pitch random sutil (00:07:29–00:08:20) e round robin/slices (00:08:34–00:11:10). | Ataca o déficit de 1.2–4 kHz por **movimento**, não por EQ. Pitch random só para baixo ou ±poucos cents; randomizar para cima + saturação é a receita do brilho metálico. "the trick is to keep it subtle" (00:07:48). |
| **Percussão de resposta** | Micro-delay de **+15 a +25 ms atrás do kick** (dragged/relaxado) ou **−5 a −20 ms à frente** (rushed/apertado) — escolher uma direção por bloco. Round robin de 3 variações para não metralhar. | Uma direção só; misturar atrasado e adiantado no mesmo bloco vira instabilidade, não groove. Não usar delay no elemento que sustenta o desenho deslocado do groove. |
| **Madeira** | Fatiar um loop de madeira gravado com o método do hi-hat loop (00:10:44–00:11:10) no **Simpler Slice**; montar o padrão com fatias diferentes e pequena variação de velocity. Round robin de 3 amostras de madeira. | É o caminho mais direto para percussão orgânica de madeira e para o miolo de 300–1.200 Hz (déficit medido) com corpo orgânico. Não empilhar madeira + sub para "engordar": o corpo vem do transiente e do miolo, não de graves novos. |
| **Stab** | Não coberto pelo vídeo. Só transferir o princípio de "mesmo espaço" do drum bus (00:12:39–00:13:47) se o stab for percussivo/de madeira. | Não randomizar pitch de stab: quebra a tônica. Reverb compartilhado, não pitch. |
| **Subida** | Não coberto. O único princípio transferível é o de âncora: manter um elemento estável enquanto os outros variam (00:12:03–00:12:14). | Não aplicar random position/pitch numa subida — borra a transição e cria artefato. |
| **Atmosfera** | Não coberto. Se usar o princípio de sala do drum bus, um único **Hybrid Reverb** curto e discreto; AutoPan do vídeo (00:14:35–00:14:41) só em percussão aguda. | Não mandar kick/sub para o send de reverb (low-end mono). Reverb curto e baixo: o alvo de 1.2–4 kHz não se corrige com cauda longa. |

**Ordem de execução sugerida (menor esforço → maior):** micro-delays nos claps/respostas → random velocity + posição no shaker → pitch random sutil → round robin/slice da madeira → drum bus. As três primeiras são edição de clip (uma sessão); as duas últimas exigem montagem de Sampler e A/B.

**Proteções recomendadas (inferência a partir do contexto de auditoria + fatos do vídeo):**
- Saturação no bus gera harmônicos em 1.2–4 kHz; como o vídeo aplica saturação a **todos** os drums (00:13:35–00:13:47), usar drive baixo e conferir de ouvido contra o brilho metálico. Não usar a saturação como atalho para "levantar" o miolo.
- O drum bus do vídeo provavelmente inclui o bass drum; num set minimalista, kick/sub devem ficar fora (ou o bus precisa preservar mono abaixo do corte) para não violar o low-end mono.
- O random velocity do vídeo é aplicado em shaker/hats; não aplicar no kick/sub nem no elemento que sustenta o desenho deslocado do groove.

---

## Prioridade e esforço

**Prioridade: alta (groove/percussão orgânica).** Ataca diretamente a percussão orgânica de madeira e o miolo deficiente em 300–1.200/1.200–4.000 Hz, sem depender de plugins além do DAW.
**Esforço: baixo a médio.** Três das cinco técnicas (micro-delay, random position, random velocity) são edição de clip de uma sessão. Round robin/slicing exige montar Sampler/Simpler (médio). Drum bus exige A/B e controle de saturação (médio).

**Ressalva de prioridade:** o vídeo é genérico de "organic drums", não é um tutorial de minimal psytech. Os valores são demonstrações; a regra de "dragged vs rushed" é a parte mais valiosa e a que dialoga com o jogo de ausência de kick do estilo.

---

## Trechos de prova (3 citações literais da legenda com timestamp)

1. **00:01:05.000–00:01:07.720** — "using micro delays to loosen up the feel of a track."
2. **00:02:11.640–00:02:22.880** — "if you delay after the kick, you're going to create a sort more of a dragged uh sort of relaxed feel to your grooves. Uh if you push them in front of the kick, you're going to tend to create a slightly more rushed and up-tight kind of feel to your drum grooves as well."
3. **00:09:11.800–00:09:20.400** — "by adding uneven layers to this, this will give you kind of a nice sort of almost polyrhythmic s- kind of feel to it. Uh by adding an even numbers, it'll reset itself on the beats if you're working in 4/4"

*(Citações literais da legenda automática; erros de transcrição como "a sort more" e "an even numbers" foram preservados de propósito.)*
