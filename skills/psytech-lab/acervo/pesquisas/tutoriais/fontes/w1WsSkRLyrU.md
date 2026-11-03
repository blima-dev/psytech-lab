# How And Why To Mono Your Low End

**Canal:** Sonic Academy · **Apresentador:** Rory (Hyper Production) · **Fonte:** legenda automática em inglês do vídeo. **Natureza do vídeo:** técnica de mixagem em pista/aux, não sound design. Duração útil ~4:45.

## Técnica ensinada (2-4 frases)

O vídeo parte do fato de que praticamente todo sistema de clube soma o grave em mono: um low end estéreo chega ao PA e, ao ser somado, sofre diferença de fase e pode cancelar — "you've got no bass" (00:00:46.910–00:00:49.160). A solução tem dois caminhos: (1) **mono na fonte**, colocando kick e baixo em mono na própria pista; ou (2) num canal/aux estéreo, abrir um **EQ em modo mid/side, selecionar só o canal Side e aplicar low-cut** — assim remove-se apenas a informação estéreo abaixo do corte, sem cortar o Mid. No exemplo ele sobe o corte até ~200 Hz e valida de ouvido: se não soar diferente, está seguro. Acima do corte, o topo pode continuar tão largo quanto se quiser.

## Ferramenta usada no vídeo (plugin/stock)

- **Mono da pista no Logic Pro 10** — "you switch them to mono like here on Logic Pro 10 you could just click that icon there and then it sets it to mono" (00:01:23.840–00:01:32.510).
- **Channel EQ nativo do Logic 10.3.2 em dual mono** — "in dual mono mode you can process the mid and the side" (00:02:03.840–00:02:13.220). Ele avisa que em estéreo comum não funciona para esse fim: "because in stereo it won't work" (00:02:38.820–00:02:40.850).
- **FabFilter Pro-Q 2**, preset "stereo cut low side" — "default setting stereo cut low side and then you just change how little or how much you want to put in mono" (00:04:19.530–00:04:28.450).
- Não há sintetizador nem plugin de sound design no vídeo; toda a operação é EQ mid/side ou mono de pista.

## Tradução para ferramentas comuns

O vídeo **não depende** de ANA 2, VELA, SideKick, Kick 3 nem Bitwig — usa Logic + Pro-Q 2. Não há conceito a substituir desses; o equivalente é puramente EQ mid/side + mono de pista.

| Ferramenta | Equivalente direto / o que fazer |
|---|---|
| **Live 12 nativo — EQ Eight** | Equivalente exato do dual-mono do Logic: ativar a edição **M/S**, selecionar **S (Side)** e aplicar low-cut. O Mid fica intocado. É o mesmo gesto do Pro-Q "stereo cut low side". [adaptação] |
| **Live 12 nativo — Utility** | `Bass Mono` + frequência (prática comum: 120 Hz) ou `Width = 0%` para mono de pista. Cobre o caminho (1) do vídeo sem EQ. [adaptação] |
| **Live 12 nativo — Simpler/Sampler/Grain, Operator, Echo, Hybrid Reverb, AutoPan, Shifter** | A técnica não muda esses devices: ela age depois deles (Utility na pista, EQ Eight no bus). AutoPan/Shifter/Echo/Hybrid Reverb podem gerar side abaixo do corte; o side-cut no bus resolve sem mexer no efeito. AutoPan no topo, acima do crossover, não é afetado. [adaptação] |
| **Serum 2** | GranularOsc **não tem papel** aqui — a técnica é de barramento, não de síntese. O cuidado é na fonte: Sub/uníssono/efeitos de alargamento não devem criar side abaixo do crossover; se criarem, o EQ Eight em S corrige. [adaptação] |
| **Diva** | Vozes sem alargamento estéreo por uníssono; o risco está em chorus/delay internos. Manter o grave seco ou deixar o side-cut do bus tratar. [adaptação] |
| **Vital** | Uníssono e roteamento estéreo podem alargar o fundamental; mesma regra: mono abaixo do crossover, largura só acima. [adaptação] |
| **Massive X** | Uníssono estéreo idem; não compensar o mono com mais width no sub. [adaptação] |
| **Surge XT** | Uníssono/width idem; o side-cut no bus garante o resultado. [adaptação] |
| **Kontakt 8 — Rubber Bridge Guitar, LOOP GARDEN, Ethereal Earth, Vintage Organs** | São patches estereofônicos; se tiverem corpo abaixo do crossover, aplicar o side-cut no canal do Kontakt ou no bus, nunca no Mid. Instrumentos de madeira/órgão têm corpo em 150–500 Hz: com o corte em 120–150 Hz o corpo permanece; com o corte de 200 Hz do exemplo, estreitaria essa faixa. [adaptação] |

Regra de ouro da tradução: **cortar só o Side**. O vídeo é explícito que cortar o Mid removeria conteúdo de verdade — "you don't wanna cut it from the mid because then you will be cutting out the frequencies" (00:04:35.810–00:04:39.110).

## Aplicação por função (kick, sub, baixo/rolling, hats/shaker, percussão de resposta, madeira, stab, subida, atmosfera)

**Leitura de contexto:** em um projeto em que o low-end já é mono, esta técnica entra como **garantia e auditoria**, não como conserto. O side-cut não altera o Mid — logo não mexe nos níveis de médio; ele não é ferramenta para corrigir déficits de corpo/presença e não deve ser usado como tal. Onde aplicar: **um EQ Eight em M/S com low-cut só no S a 120 Hz** no bus principal (último insert antes do limitador) e/ou no bus de bateria; **mono na fonte** no kick e no sub. Prática comum em psytech: Utility Bass Mono a 120 Hz e mono rígido <120 Hz — o vídeo confirma essa lei, não a substitui.

| Função | O que fazer | Limite / por quê |
|---|---|---|
| **Kick** | Mono na fonte (Utility `Width 0%` / sample mono). Se houver sala/room estéreo por send, manter o send estéreo e aplicar o side-cut só no retorno abaixo de 120 Hz. | O vídeo manda "switch them to mono" kick e baixo (00:01:23.840–00:01:32.510). Não alargar o corpo do kick para "recuperar" largura. |
| **Sub** | Mono rígido, sem uníssono/detune/width. | É o alvo central do vídeo: grave estéreo vira cancelamento no PA ("phase mismatch... cause phase cancellation", 00:00:35.370–00:00:42.410). Não há ganho a compensar: o side-cut preserva o Mid. |
| **Baixo/rolling** | Fundamental mono; harmônicos superiores podem ficar largos. Se usar uníssono no Serum 2/Vital/Massive X/Surge XT, manter a largura só acima do crossover. | O próprio vídeo admite manter o baixo largo no topo: "keep the bass track quite wide at the top which is absolutely fine" (00:01:40.049–00:01:42.869). Não usar chorus no fundamental. |
| **Hats/shaker** | **Não tocar.** Acima do crossover, seguem largos, com os offsets deslocados do groove intactos. | "By all means keep the upper frequencies as wide you like" (00:00:59.700–00:01:09.560). Mono summing não desloca tempo — [adaptação]; deslocamentos humanos de ~10 ms ficam preservados. |
| **Percussão de resposta** | Sem mudança; se algum corpo tiver energia <120 Hz, o side-cut do bus resolve. | O side-cut não corta o Mid — só remove a diferença L−R abaixo do corte (00:02:53.160–00:03:05.720); preservar o transiente é [adaptação]. |
| **Madeira** | Largo, sem side-cut de 200 Hz no bus de madeiras; usar no máximo 120–150 Hz. | O corpo de madeira vive em 150–500 Hz; o exemplo de 200 Hz do vídeo estreitaria essa faixa. [adaptação] |
| **Stab** | Largo; side-cut só abaixo de 120–150 Hz. | Mesma lógica: preservar o Mid e a largura útil. |
| **Subida** | Aplicar o side-cut no bus de FX/subidas em 120 Hz; manter o topo do riser largo. | Evita que o rumble estéreo da subida module/cancele contra o sub mono. [adaptação] |
| **Atmosfera** | Manter estéreo; se houver drone com energia <120 Hz, high-pass ou side-cut nele. | O vídeo permite topo largo; o grave é que precisa ser mono. [adaptação] |

**Como não engordar o sub:** o side-cut remove só a diferença lateral, não soma nível ao Mid. Se o A/B baixar o volume, o material era majoritariamente side/fora de fase — a resposta é checar fase, não subir ganho. Não usar EQ boost no sub para "compensar" o mono.

**Como não criar brilho metálico:** esta técnica não abre nem excita o topo; só remove side no grave. Não acoplar widener/exciter/chorus no topo para compensar déficit de presença — isso é outro problema e outro mapa. O topo deve permanecer exatamente como está, com hats/shaker nos offsets deslocados do groove.

**Onde inserir (ordem prática):**
1. Fonte: Utility `Width 0%` no kick e no sub (ou sample mono).
2. Bus de bateria: EQ Eight M/S → editar **S** → low-cut 120 Hz, 12 dB/oitava.
3. Bus principal: repetir o EQ Eight M/S no S a 120 Hz, último insert antes do limitador.
4. Auditoria: subir o corte até 150 Hz e alternar; se soar diferente, voltar. O critério é o do vídeo: "as long as it doesn't sound any different then there is no problems whatsoever" (00:03:43.470–00:03:47.330). O valor ~200 Hz citado no vídeo (00:03:41.040–00:03:43.460) é exemplo dele, não meta — prática comum em psytech mantém o mono <120–150 Hz.

## Prioridade e esforço (alta/média/baixa e baixo/médio/alto, com justificativa curta)

- **Prioridade: alta.** Protege a pressão de sub e a tradução do mix em sistema de clube. Quando o low-end já é mono, o custo de garantir é mínimo e o risco de regressão é alto se algum layer novo entrar estéreo.
- **Esforço: baixo.** Dois pontos de insert (bus de bateria e bus principal) + mono na fonte; nenhum plugin novo, só EQ Eight e Utility. A auditoria de correlação por bus é média, mas é leitura, não redesign.

## Trechos de prova: 3 citações literais da legenda com timestamp

> "99% of club sound systems will automatically sum the low end to mono so if you've got a stereo low end it's going to have a phase mismatch as soon as that PA system their mono is it for you which then can cause phase cancellation" — **00:00:26.849–00:00:42.410**

> "you go to mid/side processing and you're going to click on side at the top here so now you are just processing the side information so then if we do a low-cut here we're not doing a low-cut where we're cutting out all the frequencies we're purely cutting out these side information ie the stereo so from this red bit here all of this bit is now going to be in mono" — **00:02:44.520–00:03:05.720**

> "mono your low-end by all means keep the upper frequencies as wide you like because it will sound great over a system but the mono and the low-end is pretty pretty essential" — **00:00:59.700–00:01:09.560**
