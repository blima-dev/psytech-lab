# The Energy Curve Behind Every Hypnotic Techno Track

> **id:** `5XUULOEJ2tI` · **canal:** Hypnotic Techno Production · **publicado:** 27/08/2026 · **duração:** 8:02 ·
> **frente:** arranjo-mix.
>
> **Capítulos da metadata (lidos via `yt-dlp -J`):** 00:00 Introduction to energy levels · 00:46 Analyzing
> energy progression · 03:47 Building and dropping tension · 06:50 Applying energy fluctuations · 07:23 Workshop
> announcement.
>
> **Fonte da fala — proveniência:** a legenda automática do YouTube **não foi obtida** (o endpoint de legendas
> respondeu HTTP 429 em várias tentativas). Para não trabalhar só com a descrição, o áudio foi baixado e
> transcrito localmente com ASR (`whisper.cpp`, modelo small, 16 kHz mono) na sessão original de dissecação.
> **temLegenda=true** significa "há transcrição automática com timestamps", **não** "legenda oficial do YouTube".
> As citações abaixo são literais dessa transcrição; erros óbvios do ASR estão marcados. A descrição oficial
> (lida) diz: *"Master energy levels in your tracks by breaking down the arrangement techniques used in
> professional electronic music production"* e *"five distinct energy levels"*.
>
> **Escopo real:** é uma **análise de arranjo** de uma track de Valentino Mora, não um tutorial de sound
> design. Nenhum plugin e nenhuma DAW são nomeados **na transcrição**; o único dispositivo citado nela é um
> **EQ**, usado como leitura visual. Tudo que não estiver ancorado em timestamp é tradução do estudo, marcada
> `INFERÊNCIA` ou `HIPÓTESE`.

## Técnica ensinada (2-4 frases)

O vídeo decompõe uma track de Valentino Mora em **cinco níveis de energia** (00:00:12.600–00:00:17.600): o
nível 1 é a base com bassline, drone e toms "with some modulations on them" (00:00:46.600–00:00:57.080), que
ficam "fairly at the same level" (00:00:59.680–00:01:01.600); o nível 2 acrescenta "two elements" — um hi-hat
"t-t, t-t" e uma percussão "whoop, whoop, whoop" — e é "mostly this is driven by hat, t-t with some echo on it"
(00:01:20.880–00:01:43.760); o nível 3 acrescenta "those 16 hi-hat" (00:02:20.800–00:02:26.700); o nível 4
acrescenta "some additional layer" e "some noisy backgroundy thing" (00:02:48.440–00:03:17.940). A subida é
feita "mostly through additional layers of percussion, mostly hi-hats, plus some additional synth sounds"
(00:03:54.840–00:04:05.400), e o retorno ao nível 1 — "where we almost have no hi-hats"
(00:03:47.520–00:03:53.880) — é o gesto hipnótico. A lição é **arranjo em degraus**: cada nível é uma camada
discreta que entra/sai; o baixo, o drone e os toms ficam "fairly at the same level", com uma subida leve que
ele atribui à modulação de tom (00:01:03.280–00:01:09.060), não a uma nova camada de grave; e o autor diz que
a maioria das tracks usa uma variação dessa curva, às vezes com menos níveis (00:06:58.600–00:07:20.080).

## Ferramenta usada no vídeo (plugin/stock)

**Nenhum plugin é nomeado na transcrição.** `INFERÊNCIA`: a análise acontece numa sessão cuja DAW a
transcrição não identifica. O único elemento de interface citado nela é um **EQ**, usado como referência
visual: "we can see that on the EQ" (00:02:52.920–00:02:57.920) e "we are hitting roughly zero"
(00:03:02.360–00:03:04.580). `INFERÊNCIA`: a ferramenta real é o **mute/unmute de camadas** e a comparação
A/B; não há receita de synth, sample ou cadeia de mix.

| Item | O que o vídeo diz | Limite |
|---|---|---|
| DAW | não nomeada | não inferir Ableton, Bitwig ou outra |
| EQ | "we can see that on the EQ" (02:52); "hitting roughly zero" (03:02) | é leitura visual; não é meta de loudness |
| Camadas | hi-hat, percussão, 16 hats, open-hat, noise, synth | nomes genéricos; sem preset, sample ou dB |
| ANA 2 / VELA / SideKick / Kick 3 / Bitwig | **não são mencionados** na transcrição | não há dependência a contornar |

**Ressalvas de ASR (não virar técnica):** "level A to A" (00:04:35.920) e "in my titty, titty"
(00:06:02.600) são erros do `whisper-small`; não são nomes de nível nem de plugin. "t-t, t-t" é a
verbalização do ritmo do hat, não um dispositivo.

## Tradução: como aplicar a curva com Serum 2, Diva, Vital, Massive X, Surge XT, Kontakt 8 e Live 12 nativo

O vídeo **não depende** de nenhum plugin; a tradução é 100% de arranjo. A regra central:
**o grave fica invariante; a energia sobe pelo topo percussivo e por camadas orgânicas no meio.** Com low-end
mono e groove com microdeslocamento definido, nenhuma camada nova pode mexer em kick/sub/baixo nem
re-quantizar a levada.

| Conceito no vídeo (timestamp) | Rota | Como fazer | Limite / cuidado |
|---|---|---|---|
| **Nível 1:** bassline, drone, toms "with some modulations" (00:46–01:01) | Kick/sub/baixo constantes; drone em **Diva**, **Vital**, **Surge XT** ou **Kontakt Ethereal Earth**; toms em **Sampler/Simpler** ou **Surge XT** | Manter a base constante durante as seções; modular o drone por LFO/filtro, não por volume | Não criar nova camada de sub; não trocar o groove definido |
| **Hi-hat "t-t" com echo** (01:38–01:43) | **Live 12:** Simpler/Sampler com hat fechado escuro → **Echo** (1/16 ou 1/8 pontuado) → **AutoPan** leve | Echo com wet baixo e feedback curto; o vídeo diz "with some echo on it", não um delay longo | HPF 300–400 Hz; LPF 10–12 kHz; sem 909/clap brilhante |
| **16 hi-hats** (02:20–02:26) | **Drum Rack/Simpler:** padrão de 16tos, velocity variada, sample alternado; shaker de corpo por baixo | Usar o hat como informação rítmica; variação por omissão/acento, não por ganho | Se o set de referência já tem mais agudo relativo que as referências, **não aumentar o shaker** para "perseguir agudo" |
| **Percussão "whoop, whoop, whoop"** (01:29–01:33) | **Kontakt LOOP GARDEN / Ethereal Earth**, ou **Sampler** com woodblock/tom; **Rubber Bridge Guitar** só como pluck orgânico | Envelope curto; 1–2 respostas por compasso; corpo em 300–1.200 Hz | Evitar rim/click metálico; reverb curto, não wash |
| **Camada adicional / noisy background** (02:48–03:17) | **Serum 2 GranularOsc** (grains curtos, densidade baixa, random offset pequeno) ou **Surge XT** noise; envio a **Hybrid Reverb** | Manter sob a mix; granular como textura, não como novo protagonista | Granular pode apagar transiente e criar artefato metálico; grain curto, LPF 8–10 kHz, HPF 300 Hz, mono abaixo de 150 Hz |
| **Open-hat / decay mais longo** (04:30–04:46; 05:19–05:26) | **Sampler** com open-hat; decay médio; filtro; automação de nível | Alternativa de nível 2 sem repetir o hat fechado; o decay mais longo é uma variação, não um prato de ruído | Não abrir 8 kHz+; não usar como wash contínuo |
| **Acento em uma nota** (06:06–06:11) | Automação de velocity/volume em um hit específico; ou acento de **madeira/stab** | Acento pontual para marcar a virada | Não transformar em layer contínuo; não deslocar o groove |
| **Noise helps transition** (02:12–02:16) | **Operator** noise ou **Sampler** noise → **EQ Eight/AutoFilter** (band-pass 300–4.000 Hz) → **Hybrid Reverb** | 2–4 compassos antes da fronteira; um protagonista por transição | Sem sweep de sub; sem hiss contínuo; não repetir o salto agudo rejeitado |
| **EQ como leitura visual** (02:52–03:04) | **EQ Eight/Spectrum** no master só para comparar cenas; **Utility** para mono abaixo de 120 Hz | Medir 20–120 Hz, 300–1.200 Hz e 1.200–4.000 Hz antes/depois | "Roughly zero" do vídeo não é meta de loudness; não equalizar o master para copiar o número |
| **Additional synth sounds** (04:01–04:05) | **Serum 2 / Vital / Massive X** para stab curto; **Diva/Surge XT** para drone; **Kontakt** para madeira | Stab filtrado, atrás da madeira; timbre redondo | Evitar serra brilhante (perfil de meio rejeitado como metálico); LPF 2–4 kHz |

**Nenhum valor de EQ, filtro, delay ou dB é dado no vídeo.** As escolhas de 1/16, 1/8, HPF 300–400 Hz,
LPF 10–12 kHz, grain curto e "2–4 compassos" são `INFERÊNCIA` do estudo, não citações
do autor. O que o vídeo dá é a **ordem das camadas** e o princípio de manter o grave no mesmo nível.

**Sobre ANA 2, VELA, SideKick, Kick 3 e Bitwig:** o vídeo não os usa nem os menciona. Não há conceito
equivalente a explicar porque não há dependência: a técnica é ligar/desligar camadas e escolher samples. Se
fosse necessário traduzir uma ferramenta de movimento, o que já existe cobre: **Echo/AutoPan/Shifter** no
Live 12, **GranularOsc** no Serum 2, **LFO/filtro** em Diva/Vital/Surge XT.

## Aplicação por função (kick, sub, baixo/rolling, hats/shaker, percussão de resposta, madeira, stab, subida, atmosfera)

O vídeo não fala em compassos. A tradução usa a grade de 128 BPM (1 compasso = 1,875 s; 2:00 = 64 compassos) e
organiza **quatro cenas de 16 compassos / 30 s**. O mapa abaixo é **proposta de sobreposição da curva do vídeo a
uma estrutura de 2 minutos**, não o estado de nenhum set.

| Cena | Compassos | Nível do vídeo | Tradução |
|---|---:|---|---|
| **A** 0:00–0:30 | 1–16 | **L1** | Base reconhecível: kick/sub/baixo, drone, chamadas iniciais e percussão; madeira responde na segunda metade da cena e a subida fecha a primeira frase. Sem hat extra; manter o mínimo de hats/shaker do groove definido. |
| **B** 0:30–1:00 | 17–32 | **L2** | Entra o hat fechado "t-t" com **Echo** e a percussão de resposta ("whoop"); resposta à primeira cena, mais atividade percussiva e subida mais longa fechando a cena; preservar respirações de kick planejadas. |
| **C** 1:00–1:30 | 33–48 | **L3** | Entram os **16 hats** e o shaker de corpo; renovar uma articulação do baixo ou uma resposta de madeira; não introduzir outro conjunto de timbres. |
| **D** 1:30–2:00 | 49–64 | **L4 → L1** | 1:30–1:45: maior presença (hat 16 + open-hat/decay + textura granular + stab/madeira), **sem novo sub**. 1:45–2:00: reset para o groove esparso (quase sem hats), subida em diálogo e respiração curta. O reset longo é opção a A/B, não obrigação. |

### Por função

| Função | Onde entra | Como aplicar | O que evitar |
|---|---|---|---|
| **Kick** | A–D, constante | Mesma fonte, mesmo tuning, mesma posição; não layered | Segundo kick, click metálico para "subir", sub extra |
| **Sub** | A–D, constante | Tônica; mono; nenhuma camada nova abaixo de 150 Hz; HPF em tudo que não é grave | Tapete de sub, sidechain exagerado, sub estéreo |
| **Baixo/rolling** | A–D, constante | Preservar as articulações e o deslocamento do groove definido; não abrir filtro no L4 | Mais notas, mais gain, mais sub para "compensar" o topo |
| **Hats/shaker** | B: hat "t-t" + echo; C: 16tos; D: open-hat/decay longo | Samples escuros, velocity variada; shaker de corpo, não de brilho; LPF 10–12 kHz | Shaker mais alto/brilhante quando o set já tem agudo relativo acima das referências; 909, clap, prato |
| **Percussão de resposta** | B: "whoop"; C/D: variação | 1–2 hits por compasso; corpo 300–1.200 Hz; LOOP GARDEN/Ethereal Earth ou Sampler | Rim/click metálico, reverb longo, resposta em todo compasso |
| **Madeira** | B–D | Corpo 300–1.200 Hz; responder à chamada; LOOP GARDEN/Rubber Bridge ou Sampler | Wash de reverb, EQ boost, timbre brilhante |
| **Stab** | D | Curto, 400–2.000 Hz, atrás da madeira; Serum 2/Vital/Massive X | Serra brilhante, competir com o baixo |
| **Subida** | Fronteiras de cena (fim de A, B, D) | Noise 300–4.000 Hz, 2–4 compassos, Hybrid Reverb; um protagonista por fronteira | Sweep de sub, hiss contínuo, salto agudo |
| **Atmosfera** | A–D, constante | Drone Diva/Vital/Surge XT ou Ethereal Earth; LPF 2–4 kHz; mono abaixo de 150 Hz; sidechain leve | Encher 300–1.200 Hz demais (deixar espaço para madeira), reverb infinito, sub |

### Sem engordar o sub, sem brilho metálico

1. **Grave invariante.** O próprio vídeo mostra a base "fairly at the same level" (00:59) enquanto o topo
   sobe. Aqui: kick, sub e baixo não mudam entre A–D; nenhuma camada nova abaixo de 150 Hz; sub mono. A
   comparação de 20–120 Hz antes/depois é o teste — se subir, a camada está no lugar errado.
2. **Topo escuro, não mais topo.** O buraco medido no set de referência é 1.200–4.000 Hz, mas a faixa
   5.000–12.000 Hz já estava em −8,86 dB e o set tinha mais agudo relativo que as referências de hypnotic
   techno. Ou seja: o hat pode preencher 1,2–4 kHz, mas **não** deve empurrar 5–12 kHz. LPF 10–12 kHz, samples
   escuros, velocity/decay em vez de ganho; não subir o shaker.
3. **Meio por corpo, não por EQ.** O déficit de 300–1.200 Hz pede **madeira/percussão
   com corpo**, não shelf/boost no master. A camada de madeira e a percussão de resposta são as candidatas;
   medir a banda, não equalizar por número.
4. **Groove preservado.** Não quantizar nem deslocar o microtiming definido. Hats novos podem seguir a
   subdivisão existente ou ficar em 16tos retos, mas o kick/sub/baixo e as chamadas definidas não se movem.
5. **Estéreo com limite.** O grave é mono; quando o meio está estreito (lado/mid muito abaixo da média), hats/percussão podem ser panoramizados/AutoPan para abrir o
   meio, mas **nada de alargar sub** nem usar atraso lateral no grave.
6. **Loudness não é a curva.** O "roughly zero" do EQ do vídeo (03:02) é leitura visual; não copiar como meta
   de master nem empurrar o Limiter. A energia percebida deve vir das camadas, não do nível geral.

## Prioridade e esforço

**Prioridade: alta (P1).** A curva marca esta frente como P1, e a técnica é a espinha de um arranjo minimalista:
ela organiza **quando** cada camada entra/sai e evita a sensação de track estática. Também ataca o buraco
medido de 300–1.200 e 1.200–4.000 Hz por arranjo, sem tocar no sub e sem depender de plugin novo. É mais
valiosa que uma receita de sound design isolada porque vale para as quatro cenas e para a virada de 1:45.

**Esforço: médio.** Entender é barato (ligar/desligar camadas); executar consome curadoria e escuta: escolher
4–6 samples escuros, programar 16tos, montar as automações de cena, preservar o groove definido e fazer A/B.
Não há licença, instalação nem preset a comprar. O risco é justamente o excesso: hats/shaker demais criam
brilho metálico quando o set já tem agudo relativo acima das referências; o freio é sample escuro + LPF +
velocity, não EQ corretivo.

## Trechos de prova: 3 citações literais da transcrição com timestamp

**Proveniência:** como a legenda do YouTube não estava disponível (HTTP 429), as citações são da **transcrição
automática local** (`whisper.cpp` small) feita na sessão original, não da faixa oficial. São literais ao VTT;
erros de ASR estão apontados.

**1. O nível 2 é o hat com echo (00:01:38.760–00:01:43.760):**

> 00:01:38.760 But mostly this is driven by hat, t-t with some echo on it.

**2. O nível 3 são os 16 hats (00:02:20.800–00:02:26.700):**

> 00:02:20.800 And now we have those 16 hi-hat
> 00:02:23.400 that definitely raise the energy.

**3. O retorno ao nível 1 é o gesto hipnótico (00:03:47.520–00:03:53.880):**

> 00:03:47.520 And we drop it to level one.
> 00:03:51.900 Where we almost have no hi-hats.

**Complementares (a mesma tese, para conferência):**

> 00:03:54.840 Yeah, you see, so there is this curve of energy rising
> 00:03:57.680 mostly through additional layers of percussion,
> 00:04:01.400 mostly hi-hats, plus some additional synth sounds,

> 00:00:59.680 We are fairly at the same level.

**Nota de ASR:** "level A to A" (04:35) e "in my titty, titty" (06:02) são erros do modelo; não são nomes
de técnica. "T-t" é a onomatopeia do hat.

## Fontes

- Metadata do vídeo lida via `yt-dlp -J` na sessão original (título, canal, duração, capítulos, descrição).
- Transcrição local via whisper.cpp (gerada na sessão original).
- Números do set de referência (bandas 300–1.200 / 1.200–4.000 Hz, side/mid, shaker em −28 dB, groove
  deslocado): dados do levantamento original que contratou a dissecação, não do vídeo.

**Nenhum outro estudo consultado.** Não houve leitura de set ao vivo nem render na missão original.

## Limites e o que não foi verificado

- **Legenda oficial:** não obtida (HTTP 429 em várias tentativas). A transcrição local small pode errar
  palavras; as citações são fiéis ao VTT, não necessariamente ao áudio palavra por palavra.
- **Ferramentas:** o vídeo não nomeia DAW nem plugin; não há preset, sample, dB ou ajuste de EQ a copiar.
- **Números do vídeo:** os cinco níveis vêm de uma track (Valentino Mora); o vídeo não dá compassos, dB,
  faixas de frequência nem nomes de samples. A sobreposição dos cinco níveis às 4 cenas de 30 s é tradução do
  estudo.
- **Quinto nível:** a descrição e o vídeo anunciam "five distinct energy levels", mas a transcrição só nomeia
  explicitamente os níveis 1, 2, 3 e 4; "level A to A" (04:35) e "3.1 / 3A to B" (05:09) são variantes que o
  ASR deturpou. Não se inventou um quinto nível separado.
- **Estado:** os mapas de aplicação são propostas, não estado de nenhum set. Os resultados sonoros são
  `INFERÊNCIA` ou `HIPÓTESE` até A/B.
