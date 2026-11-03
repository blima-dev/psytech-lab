# HOW TO MAKE MINIMAL TECHNO By SLUG [Project Walkthrough]

**Vídeo:** https://www.youtube.com/watch?v=Fx3jM4xdw4M · **Canal:** Vision Serpent (artista SLUG) · **Duração:** 17:02 · **Publicado:** 15/02/2026
**Fonte de estudo:** legenda automática EN obtida com `yt-dlp --write-auto-subs`, lida integralmente (2.344 linhas, 542 cues, última marca 16:58.591). **`temLegenda = true`.**
**Descrição:** anuncia *"Watch full-length (1hour) on Patreon"* e um breakdown de *"crafting the perfect kick & bass relationship, to drum programming, sound design, arrangement"*.

> **Limite de escopo (verificado na legenda).** O corte público de 17:02 **não é** o walkthrough completo. A última fala começa em 00:16:49.680 — "the cake and the base. See you in the next chapter." — e o VTT termina em 16:58.591. O vídeo cobre **intro + kick + bass + bus de grave**, só. Drum programming, hats, percussão, sound design dos outros elementos e arrangement ficam no vídeo de 1 h do Patreon — **não estão nesta legenda**. Este estudo entrega **apenas a metade de pressão de grave**; os demais itens do motor estão marcados como "não tratado no vídeo" em vez de inventados.

> **Nota de ASR (inferência).** A legenda grafa "Stranged" (00:01:26.000) para a faixa **"Estranged"** (nome na descrição); "duning" (00:07:08.479) = detuning; "portimento" (00:08:49.279) = portamento; "htz" (00:12:27.760) = Hz; "dibels" (00:15:52.160) = dB; "cake and the base" (00:16:48.000) = kick and bass. "vis mode" (00:09:57.360) é citado cru — o vídeo não explica o que é e não se interpreta.

## Técnica ensinada (2-4 frases)

O vídeo ensina a relação **kick–baixo** de um minimal techno em quatro decisões: o kick é **um sample só**, passado por Utility "just to make it mono" (00:05:07.680), EQ que "shave off the the high end uh and and cut off uh the the low end as well" (00:05:15.840), um **transient shaper com +4 dB no ataque e curva "sharp"** (00:05:39.840) e um **limiter fazendo papel de compressor**, "actually reducing it quite heavily" (00:06:11.919). O baixo é **um oscilador saw** com quatro vozes e detune mínimo, um pouco de pan e **FM leve** "not just a pure saw" (00:07:03.280–00:07:39.919), filtro **12 dB/oitava** com pouca ressonância e "quite some overdrive" (00:08:00.560–00:08:10.560), quase sem envelope para soar longo (00:08:13.280) e **legato com ~25% de portamento**, audível só "when the notes overlap" (00:09:04.640). Kick e baixo vão para um **grupo próprio** com Glue Compressor e Utility deixando **mono abaixo de 178 Hz** (00:12:27.760), mais um rack que liga low cut + high cut na bridge e vai "making it less and less bright over time" (00:11:33.760–00:12:04.160). No canal do baixo: EQ corta grave com força e dá um **reforço de presença** chamado de "notch" (00:13:14.720), Utility reduz o stereo para **68%** e mono (00:13:47.920–00:14:02.800), compressor **4:1** com ataque rápido e release "30 milliseconds or so" (00:14:19.760–00:14:27.680), **dynamic EQ e TrackSpacer sidechainados no kick, o TrackSpacer em 20–200 Hz** (00:14:52.720–00:15:20.000), limiter **+1,5 dB** e automação do TrackSpacer onde o kick cai no offbeat (00:16:05.360–00:16:28.240).

## Ferramenta usada no vídeo (plugin/stock)

**A técnica é metade plugin de terceiro, metade stock do Ableton.**

- **Avenger (Vengeance)** — é o "go-to plugin uh synth, uh drum machine, everything" (00:04:02.480). O **kick** é um sample de um pacote do próprio Avenger, tocado no oscilador de drums (00:04:18.560 "I only have a kick here in the in the drums uh oscillator"; 00:04:25.600 "a kick that I found in one of the the packs uh that come with Avenger"). O **baixo** também nasce no Avenger (00:06:38.240 "I used uh Avenger for the bass uh to create this sound").
- **Ableton Live (stock)** — **Utility** (mono, ganho, width), **EQ** (cortes e presença), **Compressor**, **Glue Compressor**, **Limiter**, **Instrument Effects Rack** com automação on/off, e automação de macro (00:12:53.279 "now let's go through the effects chain in Ableton").
- **Neutron** — o vídeo diz apenas "neutron" (00:05:22.080); a marca **iZotope** é inferência pelo produto que combina transient shaper e dynamic EQ. Usado duas vezes: **transient shaper** no kick (00:05:22.080) e **dynamic EQ sidechainado no kick** no baixo (00:14:42.079 "This uh dynamic uh EQ uh so side chained to the kick").
- **TrackSpacer** — o vídeo diz "track spacer" (00:15:07.440); a marca **Wavesfactory** é inferência. Ducking sidechainado no kick, faixa **20–200 Hz** (00:15:09.519–00:15:20.000).
- **Headphones + laptop** — o vídeo abre dizendo que a faixa foi produzida viajando, só com MacBook Pro e headphones (00:01:14.000–00:01:36.799). É contexto de método, não de som.

**Não aparece:** nenhum ANA 2, VELA, SideKick, Kick 3, Bitwig, Serum, Diva, Vital, Massive X, Surge XT nem Kontakt.

## Tradução para outros setups (Serum 2, Live 12 nativo)

O que precisa de substituição: **Avenger**, **Neutron** e **TrackSpacer**. Nenhum dos três é insubstituível: o que eles fazem aqui é (a) tocar um sample de kick, (b) moldar transiente, (c) duckar uma faixa de frequência com o kick como gatilho.

### Caminho do kick

| Função no vídeo | Aparelho do vídeo | Equivalente | Limite da tradução |
|---|---|---|---|
| Tocar o sample de kick | Avenger, drum oscillator (00:04:18.560) | **Simpler** ou **Drum Rack** com o kick do próprio projeto | O vídeo usa sample de pacote do Avenger; aplicar a técnica sobre o kick que já existe. |
| Deixar mono | **Utility** (00:05:07.680) | **Utility** | 1:1. |
| Cortar as duas pontas | **EQ** (00:05:15.840) | **EQ Eight** | O vídeo não diz frequências nem inclinações. Ajuste por medição/ouvido. |
| +4 dB de ataque, curva "sharp" | **Neutron** transient shaper (00:05:39.840) | **Drum Buss**, knob **Transients**; ou o ataque do envelope do **Simpler**; ou **Compressor** com ataque lento | Não é o mesmo algoritmo do Neutron; o "+4 dB" é ponto de partida, não valor transferível. |
| Comprimir com limiter | **Limiter** reduzindo "quite heavily" (00:06:11.919) | **Limiter** | 1:1 de conceito. O vídeo usa o limiter como compressor de densidade, não para ganhar volume. |

### Caminho do baixo (Serum 2)

| Função no vídeo | Fala literal | Como fazer | Observação |
|---|---|---|---|
| 1 oscilador, saw | "just one one oscillator" (00:07:03.280) / "just a simple saw wave" (00:07:29.840) | OSC A em saw | 1:1. |
| 4 vozes, detune mínimo | "I'm using four voices here, but just detuning it uh minimally" (00:07:11.919–00:07:17.029) | Unison **4 vozes**, Detune baixo | O vídeo não dá o valor de detune. |
| Pan leve, sentido no topo | "adding a little bit of uh pan uh which uh especially for the high high uh high end" (00:07:17.840–00:07:27.919) | Width/pan do Unison baixo | 1:1 de conceito. |
| FM leve | "I added uh some FM, some light FM here uh to create a slightly different sound, not just a pure saw" (00:07:39.919–00:07:47.680) | Warp **FM** em quantidade baixa, ou FM from B | A curva do Avenger não é a do Serum; "light" é a instrução, não um número. |
| Filtro 12 dB/oitava | "I'm using a 12 uh u decibel per octave uh filter" (00:07:55.360–00:08:01.280) | Filtro **Lowpass 12 dB** | 1:1. |
| Pouca ressonância | "a little bit of uh resonance" (00:08:05.440) | Resonance baixa | Sem valor no vídeo. |
| Overdrive generoso | "quite some uh uh overdrive here" (00:08:08.319–00:08:11.520) | Drive do filtro | Cuidado com serra metálica: subir drive muda timbre, não volume. |
| Envelope mínimo, som longo | "there's not much of an envelope here... I wanted the bass to have that kind of like long feeling" (00:08:13.280–00:08:23.039) | Env1 com decay/sustain longos | Só faz sentido se a nota sustentar; não forçar sustain sobre groove curto. |
| Legato + ~25% de portamento | "it's a legato uh mode... about uh 25% uh on the time. So when the notes overlap, they have that bending feel" (00:09:04.640–00:09:15.440) | Global **Legato** + Portamento curto | O Serum não expõe um "%" igual ao do Avenger; acertar de ouvido e só engata se as notas se sobrepuserem. |
| Sidechain interno | "a side chain. That's how they call it, uh, here" (00:09:25.040–00:09:31.200) | **Compressor** do Live com sidechain do kick | O conceito é ducking por kick; o efeito interno do Avenger não é necessário. |
| Macro automatizada na track toda | "I'm modulating the oscillator one vis mode... lightly the resonance... the cutoff... the envelope" + automação da macro 1 (00:09:54.880–00:10:32.720) | Macros do synth + lane de automação no Live | Mapear 4 destinos: FM/warp, resonance, cutoff, envelope. Valores não são ditos. |

### Canal do baixo (depois do instrumento)

| Função no vídeo | Aparelho | Equivalente | Observação |
|---|---|---|---|
| Corte pesado de grave + presença | EQ (00:13:00.399–00:13:30.079) | **EQ Eight** | O "notch" é descrito como deixar a área "a little bit louder" — é reforço, apesar do nome. Frequência não é dita. |
| Ganho, width 68%, mono | Utility (00:13:34.880–00:14:02.800) | **Utility**: Gain, Width 68%, Bass Mono | 68% é valor exato do vídeo (dito em 00:13:51.279). |
| Compressor 4:1, ataque rápido, release ~30 ms | Compressor (00:14:08.399–00:14:33.519) | **Compressor** | 4:1 e 30 ms são exatos; ataque "very quick" é qualitativo. |
| Dynamic EQ sidechainado no kick | Neutron (00:14:42.079–00:15:02.000) | **Rack com split de banda + Compressor sidechainado** (ver abaixo) | O Live não tem dynamic EQ com sidechain nativo; a saída é processar só a banda. |
| TrackSpacer 20–200 Hz no kick | TrackSpacer (00:15:09.519–00:15:20.000) | Mesmo rack, high-cut em 200 Hz na cadeia duckada | Conceito idêntico: duck de banda estreita. |
| Limiter +1,5 dB | Limiter (00:15:40.480–00:15:52.160) | **Limiter** | 1,5 dB exato. |
| Automação do duck no offbeat | Automação do TrackSpacer (00:16:05.360–00:16:28.240) | Automação do threshold/amount do Compressor do rack | Aplicável direto ao padrão deslocado do groove. |

**Como montar o "TrackSpacer" no Live (inferência de montagem, não fala do vídeo):** Audio Effect Rack no baixo → chain 1 passa seco (ou só o topo, com EQ Eight low-cut em 200 Hz) → chain 2 com EQ Eight high-cut em 200 Hz e um Compressor com sidechain = kick, ataque rápido, release curto → as duas chains somam. Isso ducka só 20–200 Hz, que é o que o TrackSpacer faz. O Neutron dynamic EQ faz o mesmo tipo de trabalho; uma segunda banda (ex.: 200–400 Hz) pode ser adicionada com o mesmo desenho se a medição pedir.

### Bus de grave

| Função no vídeo | Aparelho | Equivalente | Observação |
|---|---|---|---|
| Colar kick + baixo | Glue Compressor (00:12:13.040) | **Glue Compressor** | 1:1. |
| Mono abaixo de 178 Hz | Utility (00:12:27.760) | **Utility → Bass Mono + Freq 178 Hz** | 178 Hz é valor exato do vídeo. O low-end do gênero já é mono; usar 178 como ponto de partida, não como dogma. |
| Low cut + high cut ligados na bridge | Instrument Effects Rack + automação (00:11:21.760–00:12:07.680) | **Audio Effect Rack + EQ Eight**, on/off e automação do high-cut | O vídeo mostra ligar na bridge e escurecer com o tempo. Serve como ferramenta de transição/contraste. |

## Notas de aplicação por função (motor de ~2 min)

### Contornos a respeitar

- **Groove:** nenhuma etapa abaixo muda MIDI, quantização ou comprimento de nota — a técnica é de timbre/cadeia, não de nota.
- **Baixo deficitário no miolo:** num set de referência medido contra faixas de artista, o miolo 300–1.200 Hz costuma ser a região mais fraca; o extremo grave, em geral, não é o problema.
- **Low-end mono** é a prática do gênero; o vídeo reforça a mesma prática em 178 Hz.
- **Veto a serra metálica:** não criar outra serra brilhante para mover banda; não somar camada de sub.

### Kick

1. No canal do kick, **Utility → mono** (00:05:07.680). Se o kick já é mono, é conferência, não mudança.
2. **EQ Eight** cortando as duas pontas, como no vídeo (00:05:15.840). O corte de grave é o que impede o kick de disputar com o SUB; o corte de agudo é o que impede brilho metálico no topo do bumbo.
3. **Drum Buss com Transients** para +4 dB de ataque (00:05:39.840). **Não usar o Boom** do Drum Buss: ele adiciona sub, exatamente o que não se quer.
4. **Limiter** no fim, com redução perceptível, como densidade e não como volume (00:06:11.919). Se a redução pesada achatar o transiente, o vídeo mesmo diz que é escolha estética ("if it sounds good to me I will use it", 00:06:20.080) — usar menos é legítimo.

Onde **não** aplicar: não copiar o corte de agudo do kick para "abrir espaço" no médio. O vídeo corta o topo do kick; ele não usa o kick para preencher 300–4.000 Hz.

### Sub

**Não tratado no vídeo como elemento separado** — não existe um canal de sub na explicação; existem o grave do kick, o baixo e o bus mono. O que é transportável:

- **Utility Bass Mono abaixo de 178 Hz** no bus de grave (00:12:27.760), que já é a prática do gênero.
- Deixar o **kick** ocupar o extremo grave e **cortar o baixo** nessa região (00:13:00.399 "EQ shaving off quite heavily the the low end u because that kick actually has a lot of low end and I didn't want them to compete").
- **Nada de camada nova de sub.** O vídeo resolve competição por corte e ducking, nunca por soma de graves.

### Baixo / rolling

1. **Serum 2**: um OSC A saw, Unison 4 com detune mínimo, Width baixa, Warp FM leve, filtro **Lowpass 12 dB**, ressonância baixa, drive moderado (00:07:03.280–00:08:11.520). O vídeo não dá números de detune, FM, ressonância, drive nem cutoff — são pontos de partida qualitativos.
2. **Legato + portamento curto** (00:09:04.640). **Pré-condição:** o portamento só aparece quando as notas se sobrepõem ("the the notes overlap slightly and that's because I added a portimento", 00:08:41.919–00:08:45.680). **Antes de ligar o glide, conferir se há sobreposição real** no MIDI atual. Se não houver, o glide não vai soar — e não se deve esticar notas para forçá-lo, porque isso mexe no groove aprovado.
3. **Reforço de presença no próprio baixo**, na faixa onde o miolo está fraco (300–1.200 Hz). O vídeo chama de "notch" mas descreve como deixar mais alto: "added this this uh notch here to to uh er make the this area a little bit louder because I wanted the that characteristic of the sound to come to uh to sound a bit more present" (00:13:14.720–00:13:30.079). **É o único mecanismo do vídeo que ataca o buraco de médio sem criar camada nova.** Frequência e Q não são ditos: achar por varredura no próprio baixo.
4. **Envelope longo** (00:08:13.280) só se a nota sustentar; caso contrário, o "long feeling" vira borrão e conflita com o groove.
5. **Canal**: Width 68% (00:13:51.279), mono (00:14:02.800), Compressor 4:1 / release ~30 ms (00:14:19.760), EQ cortando grave, e o **duck de banda 20–200 Hz** no kick (00:14:52.720–00:15:20.000).
6. **Automação do duck nos kicks de offbeat** (00:16:28.240 "it ducks the bass even more when there's kicks happening in the offbeat"). Nos grooves com eventos deslocados, isso é onde o padrão respira: aumentar o duck **apenas** nos eventos offbeat preserva o balanço e não achata o groove inteiro.

**Onde não aplicar:** não subir 1.200–4.000 Hz no baixo para compensar um vale medido. O vídeo não faz isso — ele corta agudo do kick e usa filtro 12 dB no baixo. Um boost nessa faixa no baixo é o caminho mais curto para brilho metálico.

### Hats / shaker

**Não tratado no vídeo.** A legenda não tem nenhuma menção a hats, shaker, ride ou pratos nesta parte pública. O único gesto vizinho é o high-cut automatizado do bus de grave, que deixa o som "less and less bright over time" (00:12:04.160) — é ferramenta de transição de bus, **não** uma receita de hats. Nada a extrair aqui.

### Percussão de resposta / Madeira / Stab

**Não tratados no vídeo.** Sem conteúdo.

### Subida

**Não tratado como sound design.** O que existe é o rack de low cut + high cut sendo ligado na bridge (00:11:33.760 "in the bridge I I I turn it on") e o topo escurecendo por automação (00:12:04.160). Isso é um **conceito de contraste/transição** que pode ser emprestado a uma subida ou a uma passagem — mas é extrapolação, não instrução do vídeo sobre subida.

### Atmosfera

**Não tratado no vídeo.** Sem conteúdo. (O vídeo não usa reverb nem delay em nenhum momento da legenda.)

### Bus de grave / articulação (o que amarra tudo)

- **Grupo próprio** para kick e baixo: "I like uh uh putting the kick and the bass into their own group because then I can process it" (00:10:59.519–00:11:06.880).
- **Glue Compressor** para colar (00:12:13.040), **Utility mono em 178 Hz** (00:12:27.760), **rack com low/high cut automatizados** (00:11:21.760–00:12:07.680).
- **Automação de macro ao longo da track** no baixo (00:10:21.829–00:10:32.720): é articulação de longo prazo — muda o som sem mudar nota. Aplicar como lane lenta, não como LFO audível.

### Regra de ouro desta tradução

Tudo o que o vídeo faz para abrir espaço é **subtrativo ou dinâmico** — corta, filtra, ducka, comprime. Nada é adicionado. É por isso que a técnica encaixa num motor com sub já mono e gargalo no médio: o ganho de corpo vem do **reforço de presença no baixo existente**, não de uma camada nova, e o espaço vem do **duck 20–200 Hz**, não de mais sub.

## Prioridade e esforço

**Prioridade: alta (P1).** O vídeo ataca o motor de grave e o único gargalo medido que ele endereça diretamente — o reforço de presença no baixo na faixa 300–1.200 Hz. Ressalva de escopo: como o corte público cobre só kick/baixo/bus, ele **não** resolve o motor completo sozinho; é a metade de pressão.

**Esforço: médio.**

| Bloco | Tempo estimado | Risco |
|---|---|---|
| Cadeia do kick (Utility, EQ Eight, Drum Buss Transients, Limiter) | 15–20 min | Baixo |
| Patch do baixo no Serum 2 (saw, unison, FM leve, LP12, legato, macro) | 20–30 min | Baixo |
| Rack de duck 20–200 Hz + automação no offbeat | 20–30 min | Médio — é o único bloco com montagem não óbvia |
| Bus de grave (Glue, Bass Mono 178, rack de cortes) | 15–20 min | Baixo |

**Total: ~1 h a 1 h 40.** Nenhum plugin novo, nenhum download, nenhuma compra. O custo real é de ouvido: o reforço de presença e o glide precisam ser julgados contra o groove do próprio projeto, não contra o vídeo.

**Dependência que pode travar:** o portamento só é audível se as notas do baixo se sobrepuserem. Se não se sobrepõem, esse item vira "não aplicável sem mexer no MIDI".

## Trechos de prova: 3 citações literais da legenda com timestamp

1. **00:05:39.840** — *"Uh just uh uh well adjusted about 4 dB uh to the attack and uh used a sharp uh curve for the attack."*
   Contexto: é o único valor numérico do tratamento de ataque do kick. A frase anterior, em 00:05:26.160, nomeia o aparelho: *"just to to use the transient shaper to give that attack a little bit more of uh"* — e o "punch" fecha em 00:05:32.479.

2. **00:09:04.640** — *"Yeah, you can see it's a legato uh mode in legato and uh about uh 25% uh on the time. So when the notes overlap, they have that bending feel to it."*
   Contexto: fixa o modo (legato), o valor (25%) e a condição de audibilidade (notas sobrepostas). Sem sobreposição, o efeito não existe.

3. **00:12:27.760** — *"to uh make it mono on the low end. Uh so below 178 htz uh I I uh the signal is completely mono and then uh on top it it opens a little bit"*
   Contexto: é o valor de corte mono do bus de grave (178 Hz) e a explicação de por que o topo continua estéreo — o patch do baixo tinha stereo spread próprio.

---

**Fonte:** legenda automática EN do vídeo (2.344 linhas, lida inteira; parse de cues com remoção de tags e duplicatas rolantes) + descrição do vídeo (usada só para confirmar o nome da faixa "Estranged", o canal e o corte de 1 h no Patreon). Conferência das 3 citações executada contra o texto contínuo da legenda; onsets falados medidos em 00:05:34.479, 00:09:01.279 e 00:12:24.800.
