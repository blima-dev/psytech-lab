# How to Make Techno Kick Like Charlotte de Witte, UMEK and Joyhauser

**ID:** IbeXMrvWAew · **Canal:** Audioreakt · **URL:** https://www.youtube.com/watch?v=IbeXMrvWAew
**Duração:** 25:51 · **Tema:** pressão de grave (kick de 3 artistas) · **Prioridade:** P2
**Fonte de estudo:** legenda automática em inglês lida integralmente (`yt-dlp --write-auto-subs`); descrição lida com `yt-dlp --print "%(title)s|||%(description)s"`.

**Aviso de ASR.** A legenda é automática e erra nomes de forma sistemática: `baton` = provável **Ableton**,
`9-iron` / `99 coke` = **909**, `gyros` = **Joyhauser**, `shallow Dewey's` = **Charlotte de Witte**,
`you Mack` = **UMEK**, `else` = **Hz**, `6 gb` = **6 dB**, `remote` / `ramble` / `rum rou` = **rumble**,
`medical corpus` = provável **Corpus** (o ressonador nativo do Live), `phryges` = **reduce**.
Nas citações de prova o texto fica **literal, sem correção**; o glossário fica fora da citação.

**Estrutura (verificada na descrição):** `00:56 Joyhauser Kick` · `08:46 Charlotte de Witte Kick` · `15:00 Umek Kick`.
A descrição afirma: "You only need ableton devices." — logo não há plugin de terceiro no processo.

## Técnica ensinada (2-4 frases)

Os dois primeiros kicks (Joyhauser e Charlotte de Witte) partem de **um único sample 909**
dentro de um Drum Rack, com a velocity no máximo, e o motor é o mesmo nos dois: um **filtro low-pass
ressonante** (24 dB no primeiro exemplo) com o corte baixado até ~**485 Hz** e **ressonância ~80%**, cuja
frequência é aberta por um **envelope de filtro rápido** — é isso que produz o "punch"/"snap" de ataque
("you add a low-pass filter but you're gonna apply an envelope to open the switch are quick", 00:01:32–00:01:37).
Em cima disso ele empilha **dois estágios de saturação com funções diferentes** e faz questão de colocá-los
**fora do Drum Rack**, porque todas as chains do rack já vão para um return com outro efeito e a saturação
somaria errado (00:03:05–00:03:16); e acrescenta um **reverb curtíssimo em paralelo** junto de um EQ ("Kick Punch"),
que fica "on the top" do kick, não como rumble (00:04:34–00:04:43), subindo o send **só até começar a ouvir**
(00:05:17–00:05:19). No fecho ele **recomenda** — e diz que ainda vai atualizar o rack, porque não fez isso na
versão original ("one thing I haven't done in the original right but I need to make an update", 00:06:39–00:06:43) —
pôr **Utility com bass-mono abaixo de 120 Hz** no rumble, mais um **limitador no fim da cadeia**, que existe para
poder saturar muito "without getting crazy" (00:13:43–00:13:51).

O terceiro kick (UMEK, 15:00) muda o método: em vez de uma cadeia sobre um sample, ele usa um rack de
**camadas** — um corpo (o "sound design center of the kick") mais um **Simpler com um 'click' afinado**, cujo papel é
"cut through the mix" e que quase não se ouve sozinho (00:15:17–00:15:33; 00:17:32–00:17:38). Depois passa por
**multi-band dynamics** (três bandas, crossover entre low-mid e mid-high, 00:20:33–00:20:43), EQ com HPF e
**boost em 3–4 kHz** (00:22:25–00:22:29), distorção valvulada e mono.

## Ferramenta usada no vídeo (plugin/stock)

**100% Ableton Live stock** — confirmado pela descrição ("You only need ableton devices"). Aparelhos citados
ou inequívocos na legenda:

- **Drum Rack** (o container de cada kick) e **Simpler** (o layer de "click" do terceiro kick, 00:15:30; 00:16:52).
- **Filtro low-pass de 24 dB** com drive: "I brought this low pass filter 24 DB" (00:01:39).
- **Envelope de filtro** do próprio instrumento: "you go to control and then you go to envelope and you have filter envelope here" (00:02:10–00:02:15).
- **Saturator** (dois estágios, modelos/curvas diferentes; ele chama um de "DC model" em 00:04:15 — nome não confiável na ASR).
- **Saturação valvulada** ("there is a lot of kicks nowadays with tube distortion", 00:11:20–00:11:24).
- **Utility** com bass-mono (00:06:43–00:06:49).
- **Limitador** (00:13:43; 00:08:26).
- **Multi-band Dynamics** de três bandas (00:20:25–00:20:43).
- **EQ** com HPF e boost (00:22:04–00:22:29).
- **Reverb curto** em paralelo (00:05:06) e um **ressonador** ("medical corpus is a resonator", 00:10:33 — leitura provável: **Corpus**).
- **Racks gratuitos do canal**, linkados na descrição: **Kick Punch** (`youtube.com/watch?v=guzmn4nhfg8`), **Kickverb** (`9y3szLs04RA`) e **Kick Designer Rack** (`pmlqlxagoKI`).
- **Samples:** pacote gratuito `AYNIL_PeakTime_Kick.zip` (mediafire, na descrição) + um 909 da biblioteca dele.

**Nada aqui depende de ANA 2, VELA, SideKick, Kick 3 ou Bitwig.** O único obstáculo é que os três racks gratuitos do canal não acompanham o pacote, e todos os três são reconstruíveis com devices nativos (ver abaixo).

## Tradução para Live 12 stock (Serum 2, Diva, Vital, Massive X, Surge XT)

O vídeo não depende de nada além do Live. Ressalva de método: **aplicar a técnica de ataque/cauda sobre o sample de kick que já existe** no projeto, não trocar a fonte.

| No vídeo | Equivalente | Como |
|---|---|---|
| LP 24 dB + envelope de filtro (485 Hz, res ~80%) | **Simpler** (aba Filter: tipo LP24, Freq, Res, envelope amount + A/D) ou **Sampler** | É o coração do "punch". Também em **Serum 2**: filtro `lowpass_24` + `Env → filter.cutoff` + drive do filtro. **Diva / Vital / Massive X / Surge XT** fazem o mesmo par LP24+env, mas só valem se for sintetizar o corpo — não é o caso. |
| Ressonador afinado para dar corpo ("according out to you tune", 00:10:44) | **Corpus** (nativo Live 12) | Usar com Q baixo e afinação na tônica. Ver risco em "madeira" abaixo. |
| Dois Saturator em série, funções diferentes | **Saturator** (Soft Sine / Medium Curve) + **Roar** modo *Tube* (Live 12) | Primeiro estágio = corpo; segundo = topo distorcido. Roar cobre o "tube distortion" que não existe no Saturator. |
| "crank up the output and then bring down the drive" (00:11:28) | **Roar** (Output ↑, Drive ↓) ou Saturator com Output compensado | Regra transferível e barata: saturar pelo ganho de saída, não pelo drive alto. |
| Kick Punch = EQ + reverb curto em paralelo, "on the top" | **Rack do Live**: chain paralela com **EQ Eight** + **Hybrid Reverb** 100% wet e decay curtíssimo | Reconstruível em 2 chains dentro de um Audio Effect Rack; sem o rack do canal. |
| Kickverb (rumble) | **Echo** + filtro, ou pular | **Pular** em low-end mono com groove de ausência — ver "sub" abaixo; é o item que engorda o low-end. |
| Utility bass-mono abaixo de 120 Hz | **Utility** → *Bass Mono* @ 120 Hz | Em low-end mono já configurado, é **verificação**, não mudança. |
| Multi-band Dynamics (3 bandas) | **Multiband Dynamics** (Live 12) | Só o corte low / low-mid / mid-high, com ganho pequeno. |
| Boost 3–4 kHz | **EQ Eight**, banda estreita | +1 a +2 dB no máximo, e só no transiente. |
| Limitador no fim da cadeia | **Limiter** (Live 12) | **Conferir a cadeia existente antes** — ver "Prioridade e esforço". |
| Camada de "click" com Simpler afinado | **Simpler** com o próprio click/hat sample, pitch up | Só se o ataque do kick estiver sem definição. |

**Kontakt 8 não se aplica** — o vídeo não usa instrumento melódico nem textura; forçar Kontakt aqui só adicionaria camada.
**Serum 2 / GranularOsc** também não é necessário: granular não resolve ataque de kick. O uso legítimo de Serum 2
aqui é o par LP24 + envelope e — detalhe que o vídeo não tem — **rotar o sub para `master` e filtrar só o topo** com
`filter_routing`, que é exatamente o que evita engordar o sub ao aplicar ressonância.

## Notas de aplicação por função (motor de ~2 min)

Regra de ouro: **a técnica é de timbre/cadeia, não de nota.** Nenhuma posição de nota, nenhum evento deslocado do groove, nenhuma automação de groove muda. O A/B é sempre no mesmo compasso, com o mesmo sample.

**kick — aplicar (alvo principal).**
Sobre o kick que já existe, em três movimentos:
1. **Filtro**: Simpler/Sampler em LP24 com envelope de filtro rápido, amount alto e decay curto — o vídeo usa
   "I put it to maximum and after I pay with" (00:02:25–00:02:27; "pay with" = "play with") e ajusta o corte "around 300"
   (00:02:43) no segundo exemplo, ~485 Hz no primeiro. Ponto de partida: varrer o corte entre 380–550 Hz no próprio sample e começar com
   ressonância **40–55%**, não os ~80% do vídeo. Motivo: 80% em 485 Hz é um pico estreito; num sample já
   processado ele vira assobio e é a via mais curta para brilho metálico. Subir ressonância só depois de
   confirmar que o pico não "canta" sozinho na cauda.
   *Observação de cálculo (inferência, não está no vídeo):* 485 Hz fica ~31 cents abaixo de **B4 (493,88 Hz)**,
   que é a sétima menor de C# — ou seja, o pico do vídeo não briga com a tônica de um projeto em C#. Bom ponto de
   partida, mas medir no próprio sample.
2. **Saturação**: dois estágios no canal do kick, **fora do instrumento** (o princípio do vídeo em 00:03:05–00:03:16
   é não empilhar a mesma saturação na chain e no return). Estágio 1 corpo: Saturator Soft Sine, drive ~**6 dB**
   (o vídeo diz "6 gb of drive is fine", 00:03:28 — é 6 dB). Estágio 2 topo: Roar *Tube* com **output alto e drive
   baixo** (00:11:28–00:11:31). Nunca os dois com drive alto: é a receita de intermodulação metálica.
3. **Cauda**: reverb **curto e paralelo**, 100% wet, com HPF (para não devolver grave), e o send subido
   **só até começar a ouvir** e parado ali — é literalmente a instrução dele (00:05:17–00:05:19), e é a diferença
   entre "top" e "rumble" (00:04:34–00:04:43). **Sem camada de rumble nova.**
Onde escutar: os primeiros 30–60 ms (ataque/"chick") e a cauda até o próximo kick. O ganho esperado é justamente
na faixa **300–1.200 Hz** — a ressonância em ~400–500 Hz preenche esse miolo sem tocar no sub.

**sub — não aplicar (rumble).**
Este é o ponto de maior risco do vídeo para um motor com groove de ausência de kick. Ele adiciona um **rumble** e o quer **offbeat**
("I want my remote to be like kind of offbeat", 00:06:00–00:06:02). Em um groove com subdivisões deslocadas
(.27/.77), uma camada offbeat de rumble cai exatamente no espaço negativo que o groove usa, e ainda engorda o
low-end mono. **Decisão: pular o rumble por completo.** Se em algum teste ele for usado, obrigatoriamente
com HPF (≥120–150 Hz) e só como textura de miolo, nunca como grave. A parte do vídeo que **serve** é a de
controle: "either bust mono one under under 120" (00:06:46–00:06:49) — usar Utility @120 Hz como **checagem**
de que o kick não abre estereo abaixo de 120 Hz, não como processamento novo.

**baixo/rolling — não é o tema do vídeo (extrapolação).**
O vídeo não fala de baixo. O único princípio transferível é o **envelope de filtro rápido** para dar transiente
sem volume. Se for tentado, que seja só como realce de ataque no rolling e sempre A/B com o kick ligado — o
risco é mascarar o kick na faixa 300–1.200 Hz que se quer recuperar. Marcar como **HIPÓTESE**, não como
técnica do vídeo.

**hats/shaker — preservar; cuidado de mascaramento.**
Não mexer no groove nem nos níveis. O risco vem do terceiro kick: o "click" (00:17:32–00:17:38) e o
boost de **3–4 kHz** (00:22:25–00:22:29) ocupam a mesma faixa do hat/shaker. Se o click for aplicado, a regra é
**subir o click no kick, não subir o hat** — e conferir se o hat perde definição. Se o meio-alto estiver deficitário
(1.200–4.000 Hz), há espaço, mas é espaço para **transiente curto**, não para brilho contínuo.

**percussão de resposta — aplicar só a regra do reverb curto.**
O que transfere é a regra que ele aplica em 00:05:17–00:05:19: subir o efeito só até começar a ouvir e parar ali.
Numa percussão de resposta, um reverb paralelo curtíssimo dá corpo e lugar sem deixar cauda preenchendo o espaço negativo.
Não copiar a saturação em cadeia nem o multi-band: são específicos de kick.

**madeira — não aplicar; proteger.**
A ressonância afinada é a alma da madeira. Se aplicar ressonância no kick (passo 1) com Q alto perto de
400–500 Hz, o pico do kick compete com o formante da madeira. Por isso a ressonância do kick deve ser **larga**
(Q baixo) — e aí a técnica do vídeo continua válida sem criar conflito tímbrico.

**stab / subida / atmosfera — não se aplicam.** O vídeo trata exclusivamente de kick; não discute ambiência além do reverb curto paralelo.

## Prioridade e esforço

**Prioridade: média (P2).** O encaixe é bom: a técnica ataca exatamente a faixa deficitária (300–1.200 Hz) via
ressonância de filtro, **sem** acrescentar grave. Mas é refinamento de ataque/cauda de um kick que já existe — não
resolve ausência de low-end nem substitui a fonte.

**Esforço: baixo.** Tudo é nativo do Live 12 (Simpler, Saturator, Roar, Hybrid Reverb, EQ Eight, Utility,
Limiter, Multiband Dynamics) e roda sobre o sample atual, sem novo desenho de som. O único item caro — a camada de
rumble e o rack Kickverb — é justamente o que se pula. A reconstrução do "Kick Punch" como rack paralelo
(EQ + reverb curto) é o único trabalho manual, e é pequeno.

**Ressalva de gate:** o vídeo usa **limitador no fim da cadeia do kick** para poder saturar mais (00:13:43–00:13:51).
**Não inserir um segundo limitador às cegas** — checar a cadeia real do canal antes; dois
limitadores em série no mesmo canal comem o transiente que a técnica toda tenta criar.

## Trechos de prova: 3 citações literais da legenda com timestamp

> Citações **literais** da legenda automática, com os erros de ASR preservados de propósito.

1. **00:01:32.520 – 00:01:37.880** — "you add a low-pass filter but you're gonna apply an envelope to open the
   switch are quick and you're gonna get this punch it"
   *(o mecanismo central: LP + envelope de filtro rápido = punch; "switch" é ASR.)*

2. **00:01:58.320 – 00:02:07.979** — "the frequency around yeah let's say 485 else and I'm gonna crank up the
   resonance as well around 80%"
   *("else" = Hz; corte ~485 Hz, ressonância ~80% — os dois números que definem o timbre do primeiro kick.)*

3. **00:03:05.510 – 00:03:16.549** — "saturator just be careful bring it outside of the of the drum rack because
   here basically all of the chain are going into this return where there is another effect"
   *(a regra de higiene de cadeia: saturar fora do rack para não somar com o efeito do return.)*

**Citações de apoio (usadas no corpo):**
"there is absolutely nothing on the master" (00:00:16–00:00:19) · "gonna put the velocity at the maximum" (00:01:22) ·
"and you can just 6 gb of drive is fine" (00:03:28) · "it keep the original signal and you have a parallel signal
where I apply and a cue and reverb but it's not Rumble it's really on the top" (00:04:34–00:04:43) ·
"bringing the effect just when I start to hear it I stopped" (00:05:17–00:05:19) ·
"either bust mono one under under 120" (00:06:46–00:06:49) ·
"crank up the output and then bring down the drive" (00:11:28–00:11:31) ·
"always walk with the limiter at the end of the chain when I'm walking with my kick because it's a way to crank up
use distortion saturation a lot without getting crazy" (00:13:43–00:13:51) ·
"the frequency range in in three and you have this crossover frequency basically between the low mid and mid high"
(00:20:33–00:20:43) · "then I'm just gonna boost around 3 4 kilo" (00:22:25–00:22:29) ·
"a good way to do that is phryges the decay" (00:24:36–00:24:37, "phryges" = reduce).
