# 3 Levels of Rolling Bassline for Peak Time Techno

> id `_W_mwJVDhqA` · canal **SINEE Global** (apresentador Lucas) · ~14:36 (fim da última cue) ·
> legenda automática EN do vídeo obtida e lida (99,53 KiB; 675 cues; 334 linhas úteis após remover cabeçalhos,
> tags e duplicatas consecutivas). **temLegenda=true**.
>
> **Ressalvas de legenda automática (não inventar a partir do erro):** "Sign Global" = **SINEE Global**;
> "zero octave area" (00:02:08) = provavelmente *low octave area*; "P-Funk Techno" (00:13:46) = *peak time
> techno*; "not not fully faded out" (00:05:29) = repetição do ASR. Onde a legenda é ambígua, o mapa marca.
>
> **Escopo real do vídeo:** rolling bassline de peak time techno em três níveis — síntese (Wavetable),
> variação de MIDI e processamento/camada. O vídeo **não** trata de hats/shaker, percussão de resposta,
> madeira, stab, subida, atmosfera, arranjo ou master. O que não estiver ancorado em timestamp é tradução
> deste estudo, marcada como `INFERÊNCIA`.

## Técnica ensinada (2-4 frases)

O vídeo ensina um rolling bassline de peak time techno em três níveis. O nível 1 é o esqueleto: 16º em
Wavetable mono com onda saw, o primeiro 16º de cada tempo removido para o kick ocupar o espaço
(00:01:24–00:01:32), filtro em ~200 Hz modulado pelo envelope 2 a +55% (00:03:23–00:03:34), sustain 0 e decay
inicial igual à duração do 1/16 — 111 ms no tempo dele (00:03:47–00:04:05). O nível 2 é variação de MIDI: 8º e
32º, o downbeat de volta transposto +1 oitava como acento (00:06:37–00:07:12), velocity mais baixa no segundo
16º de cada tempo para não brigar com o kick (00:07:36–00:07:53). O nível 3 é processamento e camada: EQ
cortando altos e atenuando médios-baixos, saturação forte mas a 40%, segundo EQ nos médios, compressor 50% no
preset "Drum Full Parallel", auto filter aparando agudos, LFO Tool para sidechain ducking (00:09:14–00:11:33),
e uma segunda camada com o mesmo MIDI, com o grave cortado, só para o timbre ressonante (00:12:24–00:13:11).
A tese é que, no techno, o rolling é o substituto do rumble bass: por isso é curto, mono, filtrado e duckado,
não um baixo melódico com brilho (00:11:03–00:11:17).

## Ferramenta usada no vídeo (plugin/stock)

A base do vídeo é **Ableton Live stock** — Wavetable e os devices da cadeia —, exceto o **LFO Tool** (plugin de
terceiro; a marca não é citada no vídeo) no fim da cadeia. A segunda camada é "just any preset that you like"
(00:13:02–00:13:05), então pode ser de terceiro. O próprio autor diz que a técnica não é do Wavetable: "you can
obviously pick every other VST synth, soft synth because the moves we're making are super easy. You can do that
in every other synth." (00:02:36–00:02:53).

| Device / ferramenta | Papel no vídeo | Prova literal (timestamp) |
|---|---|---|
| **Wavetable** (Live) | Synth mono, onda saw, filtro 1 com Env 2 | "I'm going to show you that iconic sound in Ableton using Ableton's wavetable synth." (00:00:18–00:00:21); "First move is to set it to mono. And we pick a saw wave." (00:02:53–00:02:58) |
| **Amp Envelope** (Wavetable) | Attack baixo, release ~10 ms | "Set the attack quite low. And the release time at around 10 milliseconds." (00:03:01–00:03:09) |
| **Envelope 2 → Filter 1 Frequency** (Wavetable) | Cutoff +55% positivo; sustain 0; release 10 ms; decay = 1/16 | "map that to 55% in the positive" (00:03:23–00:03:29); "set the sustain to zero, release time to 10 milliseconds again" (00:03:36–00:03:41); decay de 111 ms como ponto de partida (00:03:47–00:04:05) |
| **Filtro 1** (Wavetable) | Low-pass em ~200 Hz | "Let's lower the filter frequency to around 200 hertz." (00:03:31–00:03:34) |
| **EQ** (Live; ele só diz "EQ") | Corta altos e atenua médios-baixos | "That adds some cut to the high end, as well as some attenuation to the lower mids." (00:09:22–00:09:30) |
| **Saturator** (Live; ele só diz "saturator") | Drive alto/clipping, mix ~40%; aquece graves, cria harmônicos, borra transientes | "quite heavily driven and clipping ... only dialed in to about 40%" (00:09:48–00:10:01); "warming up the lows, creating some harmonic overtones, smearing the transients, and taking off some of that percussive nature" (00:10:05–00:10:15) |
| **EQ 2** (Live) | Cuida dos médios | "That is followed by another EQ, taking some care of the mids" (00:10:15–00:10:20) |
| **Compressor** (Live) | 50% no preset "Drum Full Parallel", para manter dinâmica | "50% dialed in the drum full parallel preset from Ableton" (00:10:23–00:10:29); "that serves just to keep the dynamics in place" (00:10:32–00:10:36) |
| **Auto Filter** (Live) | Apara agudos, deixa o som muffled | "the auto filter again, takes care of the high end and shaves off some of the highs" (00:10:41–00:10:50) |
| **LFO Tool** (terceiro; marca não citada) | Fonte do sidechain ducking | "Last in chain is the LFO tool, and that is my source of sidechain ducking." (00:11:18–00:11:23) |
| **Segunda camada** (outro synth/preset) | Baixo ressonante por cima, com o grave cortado | "duplicating our MIDI line" (00:12:27–00:12:31); "Just cut the bass make it sit on top" (00:13:05–00:13:11) |

O pack citado no fim (570 samples, 128 presets de Serum, 54 racks, 5 projetos) é oferta comercial
(00:13:14–00:13:51); a técnica demonstrada usa só Wavetable + devices stock + LFO Tool.

## Tradução para um arsenal compatível: Serum 2, Diva, Vital, Massive X, Surge XT, Kontakt 8 e Live 12 nativo — sem ANA 2, VELA, SideKick, Kick 3 nem Bitwig

### Live 12 nativo — rota 1:1 (principal)

O vídeo **não depende de nenhum plugin fora desse arsenal**, exceto o LFO Tool — e ele mesmo oferece as
alternativas nativas: "Use a compressor, use some gain automation, or use tools like LFO tool to take care of
that." (00:11:23–00:11:33). A tradução é direta:

- **Wavetable** → Wavetable do Live 12. É o mesmo device: mono, saw, filtro 1 LP, Env 2 na matriz, amp
  envelope com attack baixo e release ~10 ms.
- **EQ / EQ 2** → EQ Eight (ou Channel EQ). **Não copiar as bandas do vídeo às cegas:** ele corta altos e
  atenua médios-baixos para abrir espaço para o kick e os outros instrumentos (00:09:22–00:09:39). O set de
  referência já está **−4,83 dB em 300–1.200 Hz** e **−5,76 dB em 1.200–4.000 Hz**; cortar essa região no rolling
  aprofundaria o buraco. Usar EQ Eight só como corte de ar acima de ~6–8 kHz, se o patch estiver clicky.
- **Saturator** → Saturator do Live 12, drive alto e **Dry/Wet ~40%**; a curva não é nomeada no vídeo, então
  escolher uma suave e A/B. O objetivo declarado é "warm up the lows" e criar harmônicos (00:10:05–00:10:13),
  não endurecer.
- **Compressor 50% "Drum Full Parallel"** → Compressor do Live 12 com **Dry/Wet ~50%**. Se o preset
  "Drum Full Parallel" não estiver na biblioteca, recriar a ideia: compressão paralela a 50%, ataque/release
  médios, só para segurar a dinâmica (00:10:32–00:10:36).
- **Auto Filter** → Auto Filter do Live 12 em low-pass. No vídeo ele apara os agudos para o som ficar
  "muffled, more filtered, more centered to the low end" (00:11:03–00:11:15). Nesta versão, usar o corte
  **acima de ~6 kHz**, não em 1,2–4 kHz, pelo mesmo motivo do EQ.
- **LFO Tool** → **Compressor com sidechain do kick** (entrada lateral) ou **automação de ganho** (clip
  envelope de Utility/Volume). As duas rotas são literalmente sugeridas no vídeo (00:11:23–00:11:33). O
  resultado que ele busca é limpar o low end e ganhar headroom (00:12:11–00:12:19), não um pumping artístico.
- **Segunda camada** → outro Wavetable, Serum 2, Diva ou Vital com o mesmo MIDI, **high-pass** para cortar o
  grave e deixar só o timbre ressonante por cima (00:13:00–00:13:11). Manter mono abaixo de ~120 Hz; se abrir
  estéreo, só acima da crossover.
- **Não nomeados no vídeo:** Simpler/Sampler/Grain, Operator, Echo, Hybrid Reverb, AutoPan, Shifter. Não
  forçar papel para eles nesta técnica.

### Serum 2 — o mesmo patch, com filtro e envelope no lugar

O Serum 2 não é obrigatório (tem Wavetable nativo), mas reproduz a topologia:

- **Osc A:** saw (no léxico do gerador, `analog_basic` ou `analog_warm`; posição de frame de saw). O vídeo usa
  "saw wave" (00:02:55–00:02:58).
- **Global:** mono / 1 voice. O vídeo abre com "set it to mono" (00:02:53–00:02:55).
- **Filter 1:** lowpass 24; cutoff ~200 Hz como ponto de partida (00:03:31–00:03:34).
- **Env 1 (amp):** attack ~0; release **0,01 s** (10 ms).
- **Env 2 → `filter0.cutoff`:** amount **positivo ~55**; sustain **0**; release **0,01 s**; decay **0,117 s**
  (1/16 a 128 BPM; o vídeo usa 111 ms porque o tempo dele é outro — ver cálculo abaixo).
- **Ressonância:** um pouco, "until it sounds good" (00:04:31–00:05:05). Não é valor cravado.
- **FX:** deixar a cadeia no Live, na ordem do vídeo, para manter a comparação. O Saturator/Compressor/Auto
  Filter do Live são os devices que ele usa.
- **GranularOsc:** **não é usado pelo vídeo**. O baixo é saw + LPF + envelope; granular seria outro timbre.
  Se quiser a segunda camada "ressonante", um saw/filter no Serum 2 chega mais perto do que granular.
- **Ressalva de escala:** o "+55%" do Wavetable é percentual da faixa do parâmetro; o amount do Serum 2 também
  é percentual, mas as faixas não são idênticas. Tratar 55 como ponto de partida e calibrar de ouvido.

**Cálculo de tempo (INFERÊNCIA aritmética, não fala do vídeo):** 1/16 a 128 BPM = 60 ÷ 128 ÷ 4 = **0,1172 s
(117,2 ms)**. Os 111 ms exibidos no vídeo correspondem a ~135 BPM (60 ÷ 135 ÷ 4 = 0,1111 s). O conceito é
"decay = 1/16 do seu tempo"; o valor absoluto muda com o BPM.

### Diva, Vital, Massive X, Surge XT — alternativas

- **Diva:** saw + filtro ladder + envelope no cutoff; tende a arredondar mais o transiente. Boa para a versão
  "much more rounded, much more bass heavy, and hollow" que ele descreve na cadeia processada
  (00:08:56–00:09:02).
- **Vital:** saw + LPF + envelope; mais limpo, exige mais saturação para chegar ao "warm" do vídeo.
- **Massive X:** wavetable saw + insert FX; útil se a camada de cima precisar de um caráter mais duro/digital.
- **Surge XT:** saw + LPF + envelope; fonte gratuita, mesmo caminho.
- Em todos, o caráter vem da **articulação** (Env 2 com sustain 0) e da cadeia, não do synth escolhido — é o
  que o próprio vídeo diz em 00:02:36–00:02:53.

### Kontakt 8 — sem papel nesta técnica

As bibliotecas do arsenal (Rubber Bridge Guitar, LOOP GARDEN, Ethereal Earth, Vintage Organs) são
orgânicas/acústicas; o vídeo faz um baixo **sintético** (saw + LPF + saturação), sem camada acústica. Não há
tradução direta. Forçar uma corda ou órgão seria outro desenho, não esta técnica. A segunda camada do vídeo é
um "resonant bass" (00:12:39–00:12:45), não uma textura orgânica.

### O que não há

- **LFO Tool:** plugin de terceiro (marca não citada); o conceito é **sidechain ducking**. Equivalente nativo: Compressor com
  sidechain do kick ou automação de ganho — as duas alternativas citadas pelo próprio autor
  (00:11:23–00:11:33). Não há perda de conceito.
- **ANA 2, VELA, SideKick, Kick 3, Bitwig:** não são usados no vídeo. Nenhuma dependência; nada precisa de
  equivalente.
- **Pack "Peak Time Techno Production Suite":** oferta comercial; não é necessário para a técnica.

## Aplicação concreta em um motor minimal de 2 minutos: por função (kick, sub, baixo/rolling, hats/shaker, percussão de resposta, madeira, stab, subida, atmosfera)

**Contexto medido do set de referência (dado do diagnóstico, não do vídeo):** 300–1.200 Hz está **−4,83 dB** e
1.200–4.000 Hz **−5,76 dB** contra a média de 6 referências externas; o low-end é **mono**; o groove usa subdivisões
deslocadas **.27/.77** e deve ser preservado. O vídeo não fala desses números; a ponte abaixo é deste estudo.

| Função | O que o vídeo oferece | Como aplicar no motor de referência | Guarda-corpo |
|---|---|---|---|
| **Kick** | Resample de kick com no máximo **1/8 de nota**; o root do baixo casa com o tuning do kick; o primeiro 16º de cada tempo fica vazio para o kick | Medir o kick atual: a 128 BPM, 1/8 = **234,4 ms**. Se o sample passar disso, encurtar/gatear. Conferir o tuning em C#. Manter o slot do kick livre no padrão de rolling — mas **no ponto onde o kick realmente cai** (.27/.77), não numa grade reta copiada. | O 1/8 é **teto**, não meta: não alongar um kick mais curto. O tuning é de ouvido/analisador, não do vídeo. |
| **Sub** | O rolling é **substituto do rumble bass**; mono; "centered to the low end" (00:11:05–00:11:17) | O sub do motor de referência continua dono do C#1. O rolling entra **acima** dele: escrever em C#2 (69,3 Hz) e, se precisar separar, high-pass em ~50–60 Hz — **não** em 80–100 Hz, que comeria o fundamental de C#2. Manter tudo mono abaixo de ~120 Hz. | **Não empilhar outro sub.** Se o rolling tocar C#1, ele duplica o sub e engorda o low-end. |
| **Baixo / rolling** | Receita completa: 16º, 1º 16º de cada tempo fora, saw mono, LP ~200 Hz, Env 2 +55%, sustain 0, decay = 1/16, notas curtas, velocity menor no 2º 16º, downbeat +1 oitava, cadeia e camada | Montar **uma** camada de rolling em Wavetable/Serum 2 com decay **117 ms** (128 BPM). Preservar .27/.77: o padrão do vídeo é 16º reto; a grade de referência é deslocada, então ancorar os eventos nas posições .27/.77 e aplicar a lógica de "deixar o slot do kick vazio" nesses pontos. Usar a cadeia adaptada (abaixo) e, se precisar de timbre, uma segunda camada high-passed. | **Não quantizar para 16º reto** por cima do .27/.77. **Não copiar** o corte de médios-baixos/1,2–4k. **Não criar brilho**: saturação suave + low-pass depois. |
| **Hats / shaker** | **Não abordado.** A única ligação é indireta: o baixo é deixado muffled/aparado nos agudos para sobrar espaço para os outros instrumentos (00:09:30–00:09:39; 00:10:54–00:11:15) | Nenhuma técnica específica. Manter o desenho atual; o corte de agudos do rolling (acima de ~6 kHz) já deixa a faixa livre para hats/shaker. | Não clarear hats para "compensar" o buraco de 1,2–4 kHz; isso não vem do vídeo. |
| **Percussão de resposta** | **Não abordado.** | Nenhuma aplicação direta. `INFERÊNCIA`: o ducking do kick abre um buraco regular que uma resposta pode habitar, mas isso é decisão de arranjo, não receita do vídeo. | Não citar o vídeo como fonte de arranjo de resposta. |
| **Madeira** | **Não abordado.** | Nenhuma aplicação direta. `INFERÊNCIA`: como o 300–1.200 Hz do set de referência já está −4,83 dB, o espaço que o vídeo tenta abrir cortando o baixo **já existe**; a madeira pode ocupá-lo sem mais um corte no rolling. | Não usar o vídeo para EQ de madeira. |
| **Stab** | **Não abordado.** | Nenhuma aplicação. | Sem base. |
| **Subida** | **Não abordado.** O filtro/auto filter é timbre, não riser. | Nenhuma aplicação. | Sem base. |
| **Atmosfera** | **Não abordado.** Não há reverb/pad no vídeo. | Nenhuma aplicação. | Sem base. |
| **Articulação (transversal)** | O núcleo: saw → LPF → Env 2 com **sustain 0**, attack baixo, decay = 1/16, release 10 ms; notas de MIDI encurtadas para o transiente anterior não comer o próximo (00:05:07–00:05:48) | É a parte para copiar quase 1:1 no rolling: Env 2 sustain 0, decay 117 ms, release 10 ms; notas curtas. Se ficar "choppy", aumentar o release (00:06:00–00:06:09). | O filtro não pode fechar tanto que o rolling vire só click; A/B na nota real. |

### Guardas específicas: não engordar o sub, não criar brilho metálico

1. **Mono de verdade.** O vídeo abre o Wavetable em mono (00:02:53–00:02:55). No Serum 2, mono/1 voice; no
   Live, conferir com Utility. O low-end de referência já é mono e continua mono abaixo de ~120 Hz.
2. **O C#1 é do sub, não do rolling.** O vídeo escolhe G porque G está no meio da faixa que ele considera
   com boa resposta — "D sharp, E flat to A. Everything above is too weak. Everything below is inaudible"
   (00:02:12–00:02:23). A tônica de referência é **C#**, que fica abaixo dessa faixa. Copiar a escolha de nota
   exigiria trocar a tônica; a tradução é manter C# no sub/kick e usar o rolling como camada acima (C#2) ou
   como linha que percorre as notas frígias dentro de D#–A (D#, E, F#, G#, A). `INFERÊNCIA`.
3. **Inverter o EQ do vídeo.** Ele corta altos e atenua médios-baixos para abrir espaço (00:09:22–00:09:39).
   O 300–1.200 Hz de referência está −4,83 dB e o 1.200–4.000 Hz −5,76 dB: esse espaço já está vazio. No máximo, cortar
   acima de ~6–8 kHz; **não** atenuar 300–4.000 Hz no rolling.
4. **Saturação sem metal.** O vídeo usa um Saturator a 40% e depois um Auto Filter para aparar os agudos
   (00:09:48–00:10:01; 00:10:41–00:10:50). Fazer o mesmo: saturação suave, mix ~40%, low-pass depois. Não
   empilhar high shelf + bitcrush + clip no mesmo caminho.
5. **Ducking é limpeza, não bomba.** O LFO Tool entra para "clean up our low end" e ganhar headroom
   (00:12:11–00:12:19). Se o ducking sumir com o rolling, está exagerado. Compressor sidechain do kick ou
   automação de gain, ambos citados no vídeo (00:11:23–00:11:33).
6. **O groove .27/.77 manda.** O padrão do vídeo é 16º reto; o de referência é deslocado. Preservar as posições
   .27/.77 e adaptar a lógica de "primeiro 16º vazio" ao ponto onde o kick cai. Se o rolling reto mascarar o
   deslocamento, usar como ghost layer com furos/acentos, não como substituto da grade.

### Ordem de cadeia sugerida (adaptada do vídeo)

`Wavetable/Serum 2 (mono, saw, LP ~200 Hz, Env 2 +55%, sustain 0, decay 117 ms) → EQ Eight (só corte acima de
~6–8 kHz; NÃO cortar 300–4k) → Saturator (drive alto, Dry/Wet ~40%) → EQ Eight (mids, se necessário; cuidado
com o deficit) → Compressor (Dry/Wet 50%, paralelo) → Auto Filter (LP acima de ~6 kHz) → Compressor sidechain
do kick / automação de gain → [camada 2: mesmo MIDI, high-pass, pan só acima de ~120 Hz]`.

A ordem é a do vídeo (00:09:14–00:11:33); a diferença é a decisão de EQ, invertida para o buraco de
médios do set de referência. O LFO Tool está no fim da cadeia (00:11:18–00:11:23); o ducking faz parte da receita dele.

## Prioridade e esforço

**Prioridade: alta.** É a frente de pressão de grave no osso: o rolling é o motor dos dois primeiros minutos,
e o vídeo entrega a receita completa de convivência kick/baixo — slot vazio, kick ≤ 1/8, tuning, envelope de
filtro com decay de 1/16, sidechain. Nenhum plugin faltante; o atrito está na adaptação ao groove deslocado e ao
balanço de médios do set de referência.

**Esforço: médio.** Um patch (Wavetable ou Serum 2), um padrão de MIDI, cinco devices nativos e uma camada
opcional. O custo real é o A/B: decalcar .27/.77, medir o sub para não empilhar C#1 e inverter o EQ do vídeo
para não aprofundar o −4,83/−5,76 dB medidos. Estimativa: uma sessão de sound design + uma de A/B; não é um preset de
dez minutos.

## Trechos de prova

1. **[00:01:24–00:01:32]** "And we can do that by just leaving out every first 16th note of every beat and
   tada, we have space for our kick drum to hit." — a regra de convivência kick/rolling.
2. **[00:03:47–00:04:05]** "So, what you might want to do is measure 1/16 note in your track in your host
   tempo. And by hovering your mouse over it, you can see down here in that lane that says duration 111
   milliseconds. And that might be your starting value for your decay time at your filter envelope." — o
   decay do Env 2 é derivado da subdivisão, não chutado.
3. **[00:11:18–00:11:33]** "Last in chain is the LFO tool, and that is my source of sidechain ducking. You
   can use whatever you like. Use a compressor, use some gain automation, or use tools like LFO tool to take
   care of that." — o ducking é conceito, não plugin; há rota nativa.
