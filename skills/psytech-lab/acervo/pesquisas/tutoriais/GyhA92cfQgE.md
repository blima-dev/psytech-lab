# HOW TO MAKE PSYTECH By Verschallt [Project Walkthrough]

> ID `GyhA92cfQgE` · canal **Vision Serpent** · apresentador **Verschallt** · faixa **"Space Invader"** · 13:46 ·
> **Fonte de estudo:** legenda automática EN obtida e lida (`yt-dlp --write-auto-subs`; 77.458 bytes; 2.256 linhas). **temLegenda=true**.
>
> **Escopo real do vídeo:** walkthrough de uma faixa pronta. Ele abre o **low end** (kick + sub + mid bass), a
> automação de filtro/sidechain, a **camada estéreo duplicada do baixo** e um sound design de **"talking sounds"**.
> **Não** há seção de hats/shaker, percussão de resposta, madeira, stab, atmosfera, arranjo dos dois primeiros
> minutos nem BPM. O próprio autor chama o groove de *"this indie dance vibe"* (00:05:45.760–00:05:52.270), embora o
> título diga psytech. O tempo nunca é declarado no vídeo.
>
> **Convenção de evidência:** trecho entre aspas + timestamp = legenda literal. Toda a tradução para outros
> setups é **inferência de aplicação** — o vídeo não conhece nenhum projeto específico.

## Técnica ensinada (2-4 frases)

O low end é montado em **três camadas declaradas** — kick, sub e mid bass (00:03:27.320–00:03:35.229). O baixo
principal usa uma **sine que carrega o fundamental** somada a uma **saw cuja fundamental foi removida no editor de
wavetable do Vital**; a sine devolve o fundamental e a saw entrega só os harmônicos (00:06:01.400–00:06:23.110). O
sub exige **phase randomization desligada** (00:06:39.520–00:07:07.430), enquanto a camada estéreo duplicada do baixo
aceita phase randomization leve, **unison** e **ruído branco** (00:08:37.680–00:09:04.440). O "pump" nasce de
**automação de filtro abrindo no fim de meio compasso + sidechain do LFO Tool em 1/8**
(00:08:11.400–00:08:30.110; 00:09:36.000–00:09:49.590), e o kick ganha **corte de agudos + um hat curtíssimo só de
transiente** para dar "sand" (00:05:20.400–00:05:45.750). O resto do vídeo é a receita do som **"talking"**: fonte
FM/qualquer → bandpass → **Redux/downsample** → multiband → reverb/ping-pong/S&H (00:09:55.520–00:13:16.910).

## Ferramenta usada no vídeo (plugin/stock)

| Ferramenta | Papel no vídeo | Prova literal (timestamp) |
|---|---|---|
| **Vital** (synth) | Patch principal do low end, camada estéreo duplicada e fonte do "talking sound" | "um which is consisting of a sine wave and uh saw wave where I removed the fundamental" (00:06:01.400–00:06:07.120); "for the patch, I also used uh Vital" (00:08:46.120–00:08:49.470); "I just uh open up a new instance of Vital" (00:10:59.120–00:11:03.310) |
| **Kick sample "Kashmir"** | Fonte do kick, afinada **um semitom abaixo** para a tonalidade F | "the kick is just a sample from Kashmir which I pitch down one semitone so it's in the key of F" (00:03:35.959–00:03:44.519) |
| **LFO Tool** (Xfer) | Sidechain/pump e envelope de 1/8 no filtro | "here I used LFO tool, but normally I use" (00:04:01.480–00:04:05.000); "with the side chain from the LFO tool" (00:08:24.240–00:08:28.030); "I used a LFO tool for an envelope um on 1/8 notes" (00:09:36.000–00:09:42.990) |
| **Ocular Oscilloscope** (nome dele; osciloscópio de 2 canais) | Conferir fase kick×baixo; separar canais por cor | "I think it's ocular oscilloscope or so it's something called" (00:04:08.280–00:04:12.350); "you can separate channels and then you have the kick and the bass colored in different uh colors" (00:04:14.000–00:04:21.079) |
| **Filtro analog 24 dB do Vital** | Filtro do low end, com drive; repetido no segundo patch | "I added just analog 2040B filter, give it some drive" (00:07:07.440–00:07:13.150); "same uh analog 12 uh 24 dB" (00:09:45.360–00:09:49.590) — a legenda escreve "2040B", mas o próprio autor confirma "24 dB" depois |
| **Multiband compression / OTT** | Densidade e nível do baixo | "compression which is similar to those you get in Ableton stock OTT" (00:07:15.919–00:07:20.120) |
| **Saturation / distortion** | Cor e densidade | "Add a little bit of um saturation" (00:07:23.909–00:07:25.710); "and just some uh distortion" (00:09:50.720–00:09:55.510) |
| **Redux** (Live stock) | Downsample do "talking sound" | "the most important part is here that you use uh a Redux or um I think it's here called down sample" (00:11:27.560–00:11:33.430) |
| **Infiltrator** (Devious Machines), preset **"Power Toad"** | Bandpass + Redux que dão o caráter "talking" | "because I used um Infiltrator uh and used their uh the power toad, it's called" (00:10:14.520–00:10:22.670) |
| **Reverb + ping-pong delay + random S&H** | Espaço e movimento do "talking sound" | "just put the reverb and some delay some ping pong" (00:12:34.400–00:12:41.950); "modulate with a um random sample and hold to give it like more uh as like this psy vibe" (00:12:59.350–00:13:05.720) |

**Não usados no vídeo (busca literal = 0):** Bitwig, ANA 2, SideKick, Kick 3, VELA. Também 0 para BPM, shaker,
madeira, stab, riser e atmosfera — ou seja, essas funções não são ensinadas aqui.

## Tradução para outros setups (Serum 2, Diva, Vital, Massive X, Surge XT, Kontakt 8, Live 12 nativo)

O vídeo **não depende** de plugins raros. Vital é gratuito; o resto tem equivalente nativo ou é conceito reproduzível. A tradução abaixo é **inferência**.

| Ferramenta do vídeo | Conceito | Equivalente | Traduz? |
|---|---|---|---|
| **Vital** | Synth do low end e do "talking" | **Vital** ou **Serum 2** | **Sim, direto** |
| **Saw com fundamental removida** no editor de wavetable | Separar fundamental (sine) de harmônicos (saw) | **Serum 2**: editor de wavetable/`custom_harmonics` (frame com índice 0 = 0 e harmônicos 1/n); a sine fica num oscilador separado | **Sim** — é a tradução mais importante deste vídeo |
| **Phase randomization** do oscilador | Kick×baixo sem fase aleatória no sub | No Vital é o próprio controle; no **Serum 2**, o controle de fase/randomização do oscilador; no **Operator**, não confirmado na UI se existe randomização por nota — o ponto é *não adicionar* uma camada com fase aleatória | **Sim** (conceito) |
| **LFO Tool** | Curva de gain/filtro custom, retriggerada | Live 12: **automação desenhada de Utility/filtro** no Arrangement; **Compressor com sidechain** do kick; **AutoPan** só para LFO periódico simples (não tem curva custom) | **Sim, conceito** — a ferramenta exata não é stock |
| **Ocular Oscilloscope** | Ver fase kick×baixo e separar canais | Usar medidor de correlação/escopo disponível ou **A/B mono**; não inventar um device | **Parcial** |
| **OTT / multiband compression** | Compressão multibanda densa | **Live 12 Multiband Dynamics** (o preset OTT é o caminho óbvio; inferência de catálogo, não verificação de UI) | **Sim, conceito** |
| **Filtro analog 24 dB + drive** | Filtro do baixo com saturação | **Serum 2 Lowpass 24** ou o filtro do Vital; **Saturator** para o drive | **Sim** |
| **Redux** | Downsample/bitcrush | **Redux** nativo do Live 12 | **Sim, direto** |
| **Infiltrator "Power Toad"** | Bandpass + Redux + movimento | **Auto Filter** em bandpass + **Redux** + LFO/automação; ou dentro do **Serum 2**: filtro bandpass + warp `quantize` + LFO | **Parcial (conceito)** — o preset exato não existe |
| **Reverb + ping-pong delay** | Espaço do "talking" | **Hybrid Reverb** + **Echo** (ping-pong nativo) | **Sim** |
| **Random sample & hold** | Movimento aleatório do filtro | LFO do **Serum 2** com shape `random_sh`; LFO do **Vital**; ou automação | **Sim** |
| **Kick "Kashmir"** | Fonte do kick afinada | Usar o kick do próprio projeto e aplicar só o **princípio** (afinação/fase), sem trocar a fonte | **Parcial (princípio)** |
| **Bitwig / ANA 2 / VELA / SideKick / Kick 3** | — | Não aparecem no vídeo; nada a traduzir | **N/A** |

## Notas de aplicação por função (motor de ~2 min)

**Contexto típico de um motor psytech:** SUB mono (sine + saturação leve), baixo em camada separada, groove com subdivisões deslocadas (ex.: .27/.77) a preservar; num set de referência medido contra faixas de artista, o miolo 300–1.200 Hz tende a ser o déficit e o sub costuma estar resolvido.

| Função | O que o vídeo ensina (timestamp) | Como aplicar | Limite / risco |
|---|---|---|---|
| **Kick** | Sample afinado **1 semitom** para a tonalidade F; ele diz que kick e baixo "normally" são a mesma nota, mas neste caso **não são e ainda funciona** se não estiver "too phasy" e o transiente ficar constante (00:03:35.959–00:05:18.390). Depois **corta um pouco dos agudos** do kick e **adiciona um hat curtíssimo só de transiente** para dar "sand" (00:05:20.400–00:05:45.750). | **Não reafinar o kick já aprovado do projeto.** O vídeo aceita kick×baixo fora da mesma nota; o gesto seguro é **conferir fase/mono** kick×SUB×baixo (escopo/medidor de correlação ou A/B mono). Se testar o "sand", colocar o hat **dentro do kick, no mesmo trigger**, high-passed, e medir o topo (8k+) sem subir presença 2–4k. | O vídeo **não dá a frequência do corte**. Não cortar agudo no escuro. O hat extra **não pode virar evento novo** fora do grid: medir densidade antes/depois. |
| **Sub** | Patch de low end = **sine + saw sem a fundamental**; a sine devolve o fundamental (00:06:01.400–00:06:23.110). Para o sub, **phase randomization desligada** — "especially for the low end, so be sure to at least have for the sub" (00:07:00.040–00:07:05.230). Depois filtro **analog 24 dB + drive + OTT + saturação** (00:07:07.440–00:07:25.710). | **Manter SUB sine, mono.** O risco real é **adicionar** uma camada com fase aleatória. **Não** colocar saw, ruído ou unison no SUB — isso engorda o sub. A saw sem fundamental é receita de **baixo**, não de SUB. Se usar Serum 2 como sub, manter a fase fixa (sem randomização) e sem unison. | **OTT no SUB é contraindicado** em low-end com excesso já medido: ele levanta sub contínuo. Se usar OTT, usar no baixo. |
| **Baixo/rolling** | Baixo "it's mostly rooted uh uh at the root note", com **semitom no fim** e um "third uh semitone"; "always gives a bit of groove" (00:07:41.800–00:07:58.320). Automação de filtro **abrindo no fim de meio compasso** + **sidechain do LFO Tool** = pump (00:08:11.400–00:08:30.110). Camada **estéreo duplicada** com Vital, phase randomization leve, **unison**, **ruído branco** e macro que abre filtro + induz ruído (00:08:37.680–00:09:21.550). LFO Tool em **1/8** também no filtro; multiband + distortion (00:09:36.000–00:09:55.510). | **(a) Camada harmônica:** testar no baixo atual uma **sine de fundamental + saw sem fundamental** (`custom_harmonics`: índice 0 = 0, harmônicos 1/n). É o gesto que ataca o **300–1.200 Hz** sem acrescentar fundamental nem sub — a saw só contribui de 2f para cima. Rodar **A/B de 8–16 compassos**. **(b) Movimento:** semitom só no **fim da frase e só no baixo** (ex.: tônica→2ª menor do modo). **Não** levar o semitom para o SUB. O "third uh semitone" está ambíguo na legenda — não transcrever sem ouvir. **(c) Pump:** a abertura lenta de filtro em meio compasso **não toca o grid** e é a primeira a testar. Se usar pump, fazer **duck de gain suave só no baixo**, keyed no kick, terminando antes da próxima nota; **não** aplicar pump reto de 1/8 no SUB. **(d) Estéreo:** duplicar **só acima da banda mono**; unison/detune/phase randomization só na cópia high-passed. **(e) Macro:** abertura de filtro + ruído em 8–16 compassos, na camada média; ruído limitado em banda e curto. | Os intervalos do vídeo (F/G) têm de ser reescritos para a tônica do próprio projeto, não copiados. A camada estéreo duplicada **não pode** duplicar o grave. Sidechain não é obrigatório no gênero; ataque/release agressivos podem distorcer o baixo. |
| **Hats/shaker** | **Não ensinado.** A única menção a hat é o **transiente do kick** (00:05:30.840–00:05:45.750). | **Nada a aplicar.** Se o "sand" for testado, ele entra **dentro do kick**, não como padrão de hat. | Qualquer hat novo aumenta densidade de eventos — medir antes. |
| **Percussão de resposta** | **Não ensinado.** O "side sound"/"talking" é textura de synth, não percussão (00:09:55.520–00:13:16.910). | O "talking" pode virar resposta textural em outro contexto, mas é camada nova — não é o motor. | Fora do escopo de um motor de 2 min; se testar, é ideia nova, com A/B próprio. |
| **Madeira** | **Não ensinado.** | O corpo de 300–1.200 Hz deve vir da **camada harmônica do baixo + percussão orgânica aprovada**, não de um boost de EQ. | Cuidado para a camada harmônica do baixo não mascarar a madeira; alternar/abaixar em vez de empilhar. |
| **Stab** | **Não ensinado.** | — | — |
| **Subida** | **Não ensinado como riser.** O único gesto de build é a **macro do baixo** que abre filtro e induz ruído, "until the beginning of eight bars or 16 bars, just to build up a little bit" (00:09:06.320–00:09:33.070). | Se adaptar, usar **no baixo**, em 8–16 compassos, ruído em banda e curto, sem topo metálico. | O vídeo não faz riser; não tratar isso como receita de subida. |
| **Atmosfera** | **Não ensinado como atmosfera.** Reverb + ping-pong + S&H são aplicados ao **"talking sound"** (00:12:24.000–00:13:16.910). | Se a receita for usada depois, em send, com low-end fora do reverb/delay e sem 100% wet em série. | Não é cama atmosférica. |

**Regra de ouro (inferência):** o ganho de harmônicos vai todo para o **baixo**; o **SUB** continua sine, mono, sem saw, sem ruído e sem unison. No topo, o único gesto autorizável é o **hat-transiente dentro do kick**, high-passed e medido — nada de shelf global, nada de boost 2–4 kHz e nada de ruído contínuo. Se o A/B não mostrar o topo melhor sem subir presença e sem aumentar eventos, o gesto é descartado.

## Prioridade e esforço

| Item | Prioridade | Esforço | Justificativa |
|---|---|---|---|
| **Phase randomization / conferência de fase kick×sub×baixo** | **Alta** | **Baixo** | É o item mais barato e o que protege a lei de low-end mono; o próprio vídeo trata fase como checagem obrigatória (00:06:39.520–00:07:07.430). |
| **Sine + saw sem fundamental no baixo (camada harmônica)** | **Alta** | **Médio** | Ataca diretamente o **300–1.200 Hz** sem acrescentar fundamental/sub; é a tradução mais fiel do vídeo (00:06:01.400–00:06:23.110). Exige patch/A-B, não é um knob. |
| **Corte de agudos + hat-transiente no kick ("sand")** | **Média** | **Baixo** | Pode ajudar o topo, mas mexe em densidade e presença; só com medição e A/B. |
| **Automação de filtro em meio compasso + pump suave no baixo** | **Média** | **Baixo–médio** | A abertura lenta não toca o groove; o pump só entra se o A/B provar que não re-gradeia o baixo nem distorce. Sidechain é contingência, não requisito. |
| **Camada estéreo duplicada (unison/ruído/macro)** | **Baixa–média** | **Médio** | Ajuda a largura do meio, mas o risco de violar o mono do grave é alto; só depois de a camada harmônica mono resolver o miolo. |
| **"Talking sound" (bandpass + Redux + Infiltrator/S&H)** | **Baixa** | **Médio** | É sound design de "side sound", não motor de 2 min; o vídeo dedica 3+ minutos a ele, mas não há função de motor correspondente. |
| **Reverb/ping-pong/S&H no "talking"** | **Baixa** | **Baixo** | Só faz sentido se o "talking" for usado; fora do motor. |

**Veredito geral:** **prioridade alta / esforço médio**. O vídeo entrega duas coisas diretamente úteis: a
**separação fundamental×harmônicos** (corpo de meio sem engordar o sub) e a **regra de fase** no low end. Não entrega
hats, percussão, madeira, stab, subida ou arranjo — essas funções continuam sem receita deste vídeo.

## Trechos de prova (3 citações literais da legenda com timestamp)

1. **00:06:01.400–00:06:07.120** — "um which is consisting of a sine wave and uh saw wave where I removed the
   fundamental."
2. **00:07:00.040–00:07:07.430** — "especially for the low end, so be sure to at least have for the sub um the phase
   randomization turned off."
3. **00:08:11.400–00:08:26.120** — "I automated uh the filter, which is always opening up a little bit um towards the
   end of uh half a bar, so you always get this pumping together then with the side chain from the LFO tool."

## Limites e o que NÃO foi verificado

- **O vídeo não ensina** hats/shaker, percussão de resposta, madeira, stab, atmosfera, arranjo dos 2 primeiros
  minutos nem BPM. As linhas correspondentes da tabela estão marcadas como "não ensinado" — não preenchido com
  invenção.
- **Articulação/envelopes:** o vídeo não dá valores de attack/decay/release nem comprimento de nota; só fala de
  transiente do kick e de fase.
- **Tempo e tonalidade não são declarados no vídeo:** o kick dele está em F e o baixo em G
  (00:03:35.959–00:03:44.519; 00:07:41.800–00:07:47.630). Transpor para a tônica do próprio projeto.
- **"Third uh semitone" é ambíguo** na legenda automática (00:07:55.680–00:07:57.870). Não transcrito como uma nota específica.
- **A legenda escreve "analog 2040B"** em 00:07:07.440; o próprio autor diz "analog 12 uh 24 dB" em
  00:09:45.360–00:09:49.590. Tratado como filtro analog 24 dB, não como um modelo "2040B".
- **O mapeamento phase randomization → controle de fase do oscilador do Serum 2 e OTT → preset do Multiband Dynamics é inferência** de conceito, não verificação de UI.
- **O áudio do vídeo não foi analisado.** O estudo é baseado só na legenda; a balança de bandas da faixa dele não foi medida.
