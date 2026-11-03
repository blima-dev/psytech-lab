# Mono vs. Stereo: How to Create a Wide Club-Ready Techno Mix

**ID:** CixBgwVAAYg · **Canal:** Hypnotic Techno Production · **URL:** https://www.youtube.com/watch?v=CixBgwVAAYg
**Duração:** 6:23 · **Tema:** meio/espaço (separação mono/stereo) · **Prioridade:** P0
**Fonte de estudo:** legenda automática em inglês do vídeo (`yt-dlp --write-auto-subs`), lida integralmente.
**Aviso de ASR.** A legenda corrompe termos de forma sistemática: `high heads` = **high hats**, `monomid` = **mono/mid** (o termo usado no vídeo), `meets` = **mids**, `stereo input` = leitura provável de "stereo width/input" do device de echo, `"And I can do that in effect"` = provável "in the effect". Nas citações o texto fica **literal, sem correção**; o glossário fica fora da citação.

**Estrutura (verificada na descrição):** `0:00 Introduction` · `1:28 Working out Mid-Side between lead & pads` · `2:23 Percussion` · `3:55 High Hats` · `4:50 FX's` · `5:33 Summary`.
A descrição define o tema como **mid-side separation**: "a clear contrast between stereo and mono elements".
A DAW **não é nomeada** nem na legenda nem na descrição; o device `utility` é nativo do Ableton Live → **INFERÊNCIA**.

## Técnica ensinada (2-4 frases)

O vídeo ensina **separação mid/side como decisão de arranjo, não como plugin**: cada elemento tem que ser
**designado** para o campo mono/mid (precisão, punch) ou para o campo estéreo (largura, decoração), e é essa
divisão que cria contraste — "keeping the mids and side um content separated or in other words like creating
contrast between stuff that you have in the stereo field and in the monomid field" (00:03.919–00:18.470).
O diagnóstico que ele ataca é o mix de iniciante em que "there is a lot of content happening stereo everything has
a delay everything has a reverb and thus tracks don't have punch don't have uh clearness don't have that
precision" (00:28.640–00:40.389) — ou seja: **largura onipresente destrói punch**, não o contrário.
O conserto é **estreitar o elemento culpado na própria fonte**: baixar o "stereo input" de um echo que está a
**100% stereo** (01:39.350–01:48.710) e estreitar clap/snare até "fairly mono, fairly like precise"
(02:51.440–02:57.270); quando o sample ou o VST não tem controle de largura, entra **Utility** para "decrease the
width" (03:05.440–03:12.630).
A largura volta **só onde ela é ganha de propósito**: o open hat fica "fairly mono, like 100% mostly"
(04:12.879–04:19.270) e o estéreo vem de **posicionar as ghost notes à esquerda e à direita** ("I just moved them
here so they sit in left and right", 04:24.560–04:36.150), enquanto conteúdo de alta frequência e FX podem ser
largos porque funcionam "kind of like a layer" (04:49.759–05:02.603).

## Ferramenta usada no vídeo (plugin/stock)

**Nenhum plugin de terceiro.** Só dois recursos nativos do Live:

- **Utility** — o device de largura/ganho nativo, citado pelo nome: "you can always use utility and decrease the
  width" (03:05.440–03:12.630). É a ferramenta de resgate quando o sample/fonte não tem controle de largura
  ("if you like using sample or something, you don't have that control in the VST or the plug-in or the effect
  you're using", 02:57.280–03:09.110) — e ele confirma que o efeito é idêntico ao controle embutido: "That's this
  is the same effect" (03:12.640–03:16.470).
- **Controle de largura do próprio device de efeito** — ele baixa o "stereo input" de um echo que estava a
  "100% stereo" (01:39.350–01:48.710), e ajusta a largura do clap no próprio instrumento/fonte
  (02:39.040–02:48.326, "too [music] wide in my opinion. So let's clap stereo").

**Limite honesto:** o vídeo **não dá valores numéricos de width por elemento**. Os dois únicos números da legenda
são o echo a **100% stereo** (ponto de partida ruim) e o open hat "**like 100% mostly**" mono (alvo de precisão).
Não existe tabela de percentuais no vídeo — qualquer valor intermediário aplicado é escolha de quem aplica, não
reprodução da fonte.

## Tradução para ferramentas comuns

**Tradução 1:1 — não falta nada.** O vídeo inteiro roda no Live com devices nativos:

| No vídeo | Equivalente | Como |
|---|---|---|
| **Utility** → *Width* ↓ | **Utility** (Live, nativo) | É o coração. Width 0% = mono; 100% = largura original do material. Usar no canal **e nos returns**. |
| "lower the stereo input" do echo (01:39–01:48) | **Echo** (nativo Live) → largura/`Stereo` do próprio device, ou **Utility** logo depois dele | O Echo é exatamente o caso do vídeo. Se o preset veio wide, estreitar; não empilhar um segundo delay. |
| Clap/snare "fairly mono" (02:51–02:57) | **Drum Rack**: pan/largura por chain, ou **Utility** no canal | O clap precisa de transiente seco e centrado. |
| Ghost notes "left, right, left, left, right" (04:24–04:36) | **Drum Rack** com pan por chain; ou canal separado de ghost com **Auto Pan** | A largura vem de **posicionamento**, não de widener. Alternativa: duas chains (L/R) com as ghost notes distribuídas. |
| Conteúdo de alta frequência largo "as a layer" (04:49–05:02) | **Utility** no canal de FX/percussão de topo; **Hybrid Reverb** com Low Cut no return | É onde a largura é permitida. |
| (não está no vídeo) | **Unison de synth (Serum 2/Diva/Vital/Massive X/Surge XT)** | **Não usar como ferramenta de largura em elemento de precisão.** Unison largo é largura *de fonte* — o vídeo pede o oposto: fechar a fonte de precisão. Em atmosfera/FX é legítimo. |
| (não está no vídeo) | **Instrumentos sampleados (Kontakt etc.)** | Só entram como **atmosfera/camada wide**. Nenhum é necessário para a técnica. |

**Nada depende de DAW ou plugin específico** — não há sidechain dinâmico, kick-shaper nem dependência de DAW.

**Ressalva metodológica:** o vídeo **não recomenda estreitar tudo**. Ele estreita o que carrega precisão e
**preserva/move** a largura para onde ela é decoração. Aplicar "Width 0% em tudo" seria ler o vídeo ao contrário e
mataria o "wide club-ready" do título.

## Notas de aplicação em produção psytech (por função)

**Regra de ouro.** É técnica de **posicionamento no campo**, não de EQ, não de nota. Nenhum evento rítmico muda —
width não desloca tempo, então o groove fica intacto por construção. E é importante dizer o que ela **não** faz:
**não sobe o nível de nenhuma banda**. O ganho aqui é de **clareza percebida** (menos borrão/mascaramento), não de
nível. Se o meio espectral estiver deficitário no próprio set, medir antes: largura não é a ferramenta para esse
problema.

- **kick — não aplicar largura; usar como âncora do mid field** (INFERÊNCIA: o vídeo não menciona kick). O
  princípio é geral e explícito: elemento de precisão fica no campo mono ("thus tracks don't have punch",
  00:35.600). O que aqui é ação real não é no kick, é no **return**: se o kick manda send para um reverb/delay
  largo, o vídeo dá o diagnóstico exato ("everything has a delay everything has a reverb", 00:30.640–00:35.590) e
  o punch morre na soma. Conferir a largura dos returns que recebem kick. **Não** colocar widener em kick.
- **sub — não aplicar; a técnica só confirma a prática existente.** Conteúdo que precisa de peso e precisão não
  é conteúdo de campo estéreo; low-end mono é convenção do gênero. O risco a evitar é o oposto do vídeo: usar um
  widener "para abrir" e acabar com cancelamento no grave. Nenhuma ação.
- **baixo/rolling — manter centrado** (INFERÊNCIA: fora do escopo do vídeo). O rolling é conteúdo de precisão e
  de groove, então fica no mid field. Se o patch tiver camada estéreo (unison largo), fechar **no patch**, não com
  widener depois.
- **hats/shaker — aplicar (melhor alvo do vídeo).** O vídeo dedica o capítulo `3:55 High Hats` a isso. Dois
  movimentos: (1) hat principal / pulso aberto no centro, ~mono — "With open high head, I want it to be fairly
  mono, like 100% mostly" (04:12.879–04:19.270); é ele que sustenta a leitura rítmica junto com o kick. (2) A
  largura vem das ghost notes, por posição — "left, right, left, left, right. Yes. So, I just moved them here so
  they sit in left and right" (04:24.560–04:36.150). Implementação: Drum Rack com pan por chain, ou canal
  separado de ghost com Auto Pan. **Não** usar widener/chorus/Haas no bus inteiro de hats: é o caminho para
  brilho metálico (comb filtering — INFERÊNCIA, não está no vídeo). E **não** pendurar um echo estéreo no hat:
  é literalmente o caso que ele corrige em 01:39.
- **percussão de resposta — aplicar; é o candidato natural a "layer" largo.** O vídeo libera explicitamente
  largura para conteúdo de alta frequência que funcione como camada: "we have this guy being fairly stereo as
  well, which is okay. Like high frequency content. It's kind of like a layer, so it works well"
  (04:49.759–05:02.603). Pode receber pan por golpe (L/R alternado) e alguma largura. **Cuidado:** na parte do
  golpe que tiver corpo no miolo (300–1.200 Hz), manter o corpo centrado e largar só o topo.
- **madeira (percussão orgânica) — aplicar só como proteção.** Formante e corpo são "precisão" → mid field;
  largura só numa camada de topo/ruído, nunca num widener sobre o corpo. Widener em material com formante
  estreito produz borrão de fase que soa "metálico/oco" — INFERÊNCIA. Espaço dela é panorâmica discreta, não
  cauda de reverb.
- **stab — aplicar estreito.** Ocupa o miolo; conteúdo de precisão: centro, Width baixo. Se o preset já é largo
  (unison/chorus), fechar no patch ou com Utility — não "consertar" com EQ depois.
- **subida — aplicar na parte de cima** (INFERÊNCIA: o vídeo não menciona riser). O capítulo `4:50 FX's` é onde
  ele libera os FX largos. Uma subida pode abrir no topo e ficar estreita embaixo — mas a parte de baixo continua
  mono. Se a subida for um sweep de ruído, é justamente o tipo de "high frequency layer" que ele autoriza.
- **atmosfera — aplicar (é a casa da largura).** É o "stuff in the stereo field" do vídeo: larga e **fora do
  miolo**, deixando o centro livre para kick/sub/hat/rolling. Hybrid Reverb com Low Cut no return, Utility para
  largura. O vídeo não fala de reverb em si — o Low Cut é engenharia de quem aplica, para não engordar o sub.

**Onde a técnica realmente beneficia** (INFERÊNCIA, não é do vídeo): estreitar conteúdo largo que compete no
centro **reduz mascaramento** dos elementos que carregam o miolo — a percepção de "meio vazio" pode melhorar
**sem EQ**. Se o meio continuar deficitário depois do A/B, o problema é de nível/arranjo e precisa de outra
frente.

**A/B de escuta (o método do próprio vídeo).** Ele ouve, nomeia o culpado, mexe, e ouve de novo: "instantly I can
hear that separation [music] stuff in the mids, stuff in the stereo" (02:09.681–02:16.070). Repetir no próprio
material: mesmo compasso, solo no canal, botão de width/bypass, e decidir. O critério de aceitação declarado no
vídeo é "this mix [music] has more precision sits better" e "100% would work better on the uh huge speakers
because it has that separation. It will have that punch" (05:16.358–05:33.670) — club-readiness.

## Prioridade e esforço

- **Prioridade: alta.** A decisão **atravessa o mix inteiro** (cada canal precisa ser classificado em mid ou
  side), é curta de assistir (6:23) e ataca um vício que a própria descrição nomeia como o problema do produtor
  iniciante. Ressalva honesta: **não é a cura de um déficit espectral medido** — déficit de banda é nível/EQ, e
  este vídeo não toca em EQ. Prioridade alta para *clareza e punch*.
- **Esforço: baixo.** Tudo é nativo (Utility, pan de chain do Drum Rack, Auto Pan, Echo). Não há desenho de som
  novo, plugin a comprar nem automação. O trabalho real é uma **tabela de decisão por canal** (mid vs side) e um
  A/B de 1 compasso por elemento. A parte chata é auditar os **returns** — se tudo manda para um reverb/delay
  largo, olhar ali antes de mexer nos canais.

## Trechos de prova: 3 citações literais da legenda com timestamp

> Citações **literais** da legenda automática, com os erros de ASR preservados de propósito.

1. **00:03.919 – 00:18.470** — "about one important thing uh in mixing which is keeping the mids and side um
   content separated or in other words like creating contrast between stuff that you have in the stereo field and
   in the monomid field."
   *(a tese do vídeo: contraste entre campo estéreo e campo mono/mid — "monomid" é o termo dele.)*

2. **00:28.640 – 00:40.389** — "there is a lot of content happening stereo everything has a delay everything has a
   reverb and thus tracks don't have punch don't have uh clearness don't have that precision."
   *(o diagnóstico: largura onipresente + delay + reverb = sem punch, sem clareza, sem precisão.)*

3. **02:57.280 – 03:12.630** — "if you like using sample or something, you don't have that control in the VST or
   the plug-in or the effect you're using, you can always use utility and decrease the width."
   *(a ferramenta e o critério: quando a fonte não tem controle de largura, Utility resolve.)*

**Citações de apoio (usadas no corpo):**
"this one has an echo on it with 100% stereo. So very quick fix we could do is to lower the stereo input"
(01:39.350–01:48.710) · "And I want always clap and snares to be fairly mono, fairly like precise"
(02:51.440–02:57.270) · "too [music] wide in my opinion. So let's clap stereo" (02:39.040–02:48.326) ·
"That's this is the same effect. You're going to decrease the width of the sound" (03:12.640–03:16.470) ·
"With open high head, I want it to be fairly mono, like 100% mostly" (04:12.879–04:19.270) ·
"left, right, left, left, right. Yes. So, I just moved them here so they sit in left and right"
(04:24.560–04:36.150) · "this pattern, it's fairly stereo. Uh, it has that differentiation between meets and
sides" (04:33.199–04:40.988, "meets" = mids) · "we have this guy being fairly stereo as well, which is okay. Like
high frequency content. It's kind of like a layer, so it works well in my opinion" (04:49.759–05:02.603) ·
"this mix [music] has more precision sits better and 100% would work better on the uh huge speakers because it has that
separation. It will have that punch" (05:16.358–05:33.670).

**Nota de leitura:** o "100%" em 05:23.520 ("and 100% would work better on the uh huge speakers") está ambíguo na
legenda automática — não fica claro a que ele se refere. **Não usar como especificação.** O que está claro e
citável é a conclusão logo depois: "because it has that separation. It will have that punch."
