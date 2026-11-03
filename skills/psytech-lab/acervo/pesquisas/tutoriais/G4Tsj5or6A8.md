# Building Solid Raw / Hypnotic Techno Drums In Ableton Live

**Canal:** SINEE Global · **ID:** `G4Tsj5or6A8` · **Duração:** 17:13 · **Tema:** groove (bateria raw/hypnotic) · **Prioridade:** P1
**Fonte de estudo:** legenda automática em inglês do vídeo, lida integralmente → `temLegenda=true`.
**Fonte secundária:** descrição do vídeo, que nomeia os dois plugins da casa — "Chop Suey Kick Drum Designer" e "Kikzilla Rumble Generator". A legenda automática corrompe nomes ("chopi" [00:44], "Kick Zilla" [02:03], "soup" [08:04], "dester" [11:13], "sound toise" [15:31]); os nomes ficam como a legenda escreveu, com a ressalva quando a descrição confirma.

## Técnica ensinada (2-4 frases)

O groove é montado por **camadas curtas e complementares**, não por um kick único: kick desenhado em transiente/corpo/cauda [00:47–00:55], um gerador de rumble no próprio kick [02:03–02:19], um "ghost track" que é o kick duplicado e encurtado "so we don't have interference in the uh in the low frequencies" [03:41–03:50], percussão grave em uma única nota no primeiro offbeat [04:28–04:34] e percussão média de caixa com velocity randomizada [05:44–05:50].

A hipnose vem de **velocity, swing e modulação lenta**, e não só de mais camadas: as hats são sequenciadas com gates de 16, swing e "shapes" de velocity que definem o groove [06:34–06:53], e o LFO interno do Simpler modula volume e pan em profundidade "very very low" [08:42–08:49].

Nos agudos, a regra é **cortar ressonância e saturar em vez de subir volume**: Pro-Q tira "nasty frequencies" [07:32–07:39], o reverb fica "very very low in the mix" [07:50], e o autor avisa que a hat pode soar "dull" sozinha porque o processamento vem depois [08:23–08:27]; quando ela fica "too forward" ou "too resonancy", testa-se saturação — "overdrive and saturation is the solution to the problem 99% of the time" [11:23–11:47].

O bus fecha com compressão 6:1 com mix todo aberto e ganho de entrada compensado na saída [14:26–14:46], EQ com cortes e um leve boost em 51 Hz [15:10–15:23], e Decapitator com drive entre 2 e 3, tone escurecido e output reduzido para casar nível [15:31–15:52].

## Ferramenta usada no vídeo (plugin/stock)

O vídeo roda **inteiro em Ableton Live**: o que aparece é Max for Live + plugins da SINEE + third-party (nenhum ANA 2, VELA, SideKick, Kick 3 nem Bitwig):

| Ferramenta | O que faz no vídeo | Onde |
|---|---|---|
| **Chop Suey** (SINEE; legenda "chopi") | Kick em 3 seções — transiente, corpo e cauda — com sample próprio por seção, seção de filtro, "beef section which is an internal overdrive saturation" e waveform em tempo real | [00:44–00:57], [01:18–01:51] |
| **Kikzilla** (SINEE; legenda "Kick Zilla") | Gerador de rumble: threshold, envelope, filtro 12/24 dB e distorção em modo pre-reverb/pre-filter/post-filter com amount | [02:03–03:02] |
| EQ não nomeado | "just to take out even more of the low mid content and to push a little bit around 55 Herz" | [03:17–03:28] |
| **Opal** (Max for Live) | "a four-part synthesizer drum machine thingy" usado como percussão grave | [04:05–04:19] |
| Sidechain da Cableguys | "I use this one from cable guys because it just works" | [04:52–04:58] |
| **Decimort 2** (D16) | Bit crusher, preset MPC 60, para "beef up" a percussão grave | [05:05–05:14] |
| **Snake** (Max for Live) | Sequenciador de hats; notas todas na mesma nota, gates de 16, swing e shapes de velocity | [06:13–06:53] |
| **Pro-Q** | Corta "nasty frequencies in the upper range" | [07:32–07:39] |
| Reverb (legenda "aon's Reverb") | "very very low in the mix" | [07:50–07:56] |
| Tamer de ressonância (legenda "soup") | "just to tame it even more" | [08:04–08:07] |
| **Simpler** (stock) | LFO interno modulando volume e pan | [08:31–08:49] |
| "Voda"/"voder" | Vocoder com opção de ruído; 3 LFOs no release, no depth do LFO1 e no formant shift | [10:19–10:58] |
| Auto Filter / Glue Compressor | Tira graves do shaker e "tame the spikes" | [11:00–11:11] |
| "dester" | "a multiband distortion unit" | [11:13–11:20] |
| "H" | "a psycho acoustic effect … changes a little bit of your perception where in the stereo field your high is" | [12:39–12:50] |
| EQ8 + Reverb + Glue Compressor + Delay | Cadeia da track de noise (ride substituto) | [13:20–13:38] |
| **Distressor** | Compressor do bus de bateria, ratio 6:1 | [14:26–14:46] |
| EQ do bus | Cortes + boost leve em 51 Hz | [15:10–15:23] |
| **Soundtoys Decapitator** | Saturação do bus, drive entre 2 e 3, tone escurecido | [15:31–15:52] |

## Tradução para Live stock + synths comuns (Serum 2, Vital etc.)

| No vídeo | Conceito | Equivalente |
|---|---|---|
| Chop Suey | Kick como 3 samples independentes (transiente/corpo/cauda), cada um filtrável e saturável | **Live 12:** Drum Rack com 3 Simplers (ou Sampler) em cadeia; corpo pode ser **Operator** (sine + envelope de pitch) ou **Serum 2** (osc sine + pitch envelope). "Beef" = **Saturator** leve no corpo/cauda. Waveform em tempo real = display do Simpler |
| Kikzilla | Rumble gerado a partir da cauda do kick, com filtro e distorção pré-filtro | **Live 12:** cópia do kick (só cauda) → **Hybrid Reverb/Echo** → **Auto Filter** (LP 12/24 dB) → **Saturator** → **Compressor** com sidechain no kick. A ordem "distortion pre-filter" [02:43] = Saturator **antes** do Auto Filter |
| Opal | Percussão grave sintética de 4 partes, uma nota | **Serum 2** (sine/triangle + envelope de pitch curto + filtro) ou **Simpler** com tom/perc; as 4 partes viram 4 camadas no Drum Rack |
| Sidechain Cableguys | Ducking da percussão grave pelo kick | **Compressor** do Live com sidechain externo |
| Decimort 2 / MPC 60 | Bit reduction para "engordar" sem grave | **Redux** (Live 12) ou warp "quantize" do **Serum 2** |
| Snake | Sequenciador com gates de 16, swing e shapes de velocity | **Live 12:** clip MIDI em 16 avos + **Groove Pool** (swing) + **Velocity** MIDI effect (Random) + comprimentos de nota por step |
| Pro-Q | Cortes estreitos de ressonância | **EQ Eight** |
| "soup" (tamer) | Reduzir ressonância sem matar o timbre | Sem de-ressor dedicado no stock. Substituto: EQ Eight com Q alto nos picos + redução de nível; declarar o limite (sem Soothe, o resultado é menos transparente) |
| Simpler LFO | Movimento lento em volume e pan | **Nativo, idêntico:** LFO do Simpler → destinos Volume e Pan |
| "Voda"/"voder" | Vocoder com carrier de ruído + formant shift + release modulado | **Vocoder** do Live 12 (Carrier = Noise, Formant, Depth, Rate, Release) + LFOs; **Shifter** cobre o formant shift |
| Auto Filter / Glue / "dester" | Tirar graves, colar, distorcer multibanda | **Auto Filter**, **Glue Compressor**, **Drum Buss** (drive/crunch) ou **Saturator**; distorção multibanda pura não existe nativa → Drum Buss + EQ por faixa |
| "H" | Percepção estéreo dos agudos | **Auto Pan** lento + **Utility** (width) |
| Distressor 6:1 | Compressão de bus agressiva com mix alto | **Glue Compressor** (ratio 6, mix alto, input ↑ / output ↓) |
| Decapitator | Saturação de bus com tone escurecido | **Saturator** (Soft Sine/Analog Clip) + corte de agudo no EQ; **Drum Buss** como alternativa |

**Traduzível, com duas ressalvas:** nenhum plugin do vídeo é obrigatório — Chop Suey, Kikzilla, Opal, Snake, Decimort, Pro-Q, Distressor, Decapitator e "H" viram combinações de dispositivos nativos do Live + Serum 2. Só o tamer de ressonância (Soothe) e a distorção multibanda não têm equivalente nativo direto.

## Notas de aplicação por função (motor de ~2 min)

**Contexto geral:** em um motor de referência, o miolo 300–1.200 Hz costuma ser a região mais fraca e o low-end é mono; o groove usa subdivisões deslocadas (ex.: .27/.77) e deve ser preservado.

### Kick
Onde: canal do kick. Como: montar 3 camadas no Drum Rack — transiente (baixo no mix, como no vídeo [01:30]), corpo e cauda de 808 curto [01:18–01:25]; filtro + saturação leve no corpo ("beef" [01:48–01:51]). No EQ: cortar low-mid e dar um sino pequeno **na fundamental do próprio kick** — o vídeo empurra 55 Hz [03:20–03:28], mas 55 Hz é A1; copiar o **princípio** (cortar low-mid, empurrar a fundamental do próprio projeto), não o número. O próprio autor diz que o kick sozinho "doesn't really Groove yet" [03:33–03:35] — a batida só anda com as camadas seguintes.

### Sub
O vídeo não mostra nem menciona **canal de sub separado** — o grave que ele trata vem do próprio kick. O que se importa é a regra de não-interferência: o ghost é o kick encurtado para não colidir no grave [03:41–03:50], e o Kikzilla tem filtro para tirar "the frequencies we don't want" [02:36]. Aplicação: qualquer rumble, ghost ou percussão grave passa por **Auto Filter (HP)** acima da fundamental do sub; o sub continua mono e sem camada duplicada. *Inferência de engenharia, alinhada ao princípio do vídeo.*

### Baixo / rolling
**Não abordado no vídeo.** O único princípio transferível é o ducking por sidechain que ele usa nas percussões [04:34–04:58]: **Compressor** com sidechain do kick no bus do rolling. *Inferência, não está no vídeo.*

### Hats / shaker
Onde: canais de hat e shaker. Como: 16 avos com gates de 16 e um pouco de swing [06:34–06:46]; **velocity é o groove** — "the velocities are responsible for the swing and the overall feel" [06:46–06:55]; uma segunda closed hat mais alta no espectro como acento [09:08–09:20]; cortes estreitos de ressonância [07:32–07:39, 09:26]; reverb "very very low in the mix" [07:50]; LFO lento do Simpler em volume e pan com profundidade mínima [08:42–08:49]. Para um vale em 1.200–4.000 Hz: preencher com a camada de shaker/noise, **não** com high-shelf no bus *(inferência de mix; o vídeo diz que o noise "fills out the frequency spectrum in the high end" [13:09–13:12] sem medir faixa)*. Se a hat soar opaca no solo, está dentro do método — "don't worry if this sounds a little bit dull right now" [08:23–08:27].

### Percussão de resposta
Duas camadas do vídeo são candidatas naturais para um vale em 300–1.200 Hz (o vídeo fala em "low end" [04:17–04:22] e "mid-range" [06:00–06:03], sem medir faixas):
- **Grave:** uma nota no primeiro offbeat [04:28–04:34], delay de colcheia pontuada "quiet in the background" [04:45–04:49], sidechain no kick [04:52–04:58] e bit reduction MPC 60 [05:05–05:14]. No grid, ancorar na subdivisão deslocada já existente, sem mover as hats.
- **Média:** sample de caixa com velocity randomizada [05:44–05:50] — é a camada que enche 300–1.200 Hz de forma orgânica, sem EQ. *(Inferência de mix.)*

### Madeira / stab / subida
**Não abordados no vídeo.** Nada a traduzir; não inventar receita.

### Atmosfera
A track de **noise no lugar do ride** [12:52–13:12] é o parente mais próximo de atmosfera: EQ8 estreito, reverb, Glue Compressor com sidechain (alvo não transcrito: "side chaining to a" [13:29–13:38]) e delay. Aplicação: camada de ar em nível baixo, com HP para não tocar o sub. *(Inferência de mix: o HP não está no vídeo.)*

### Bus
Compressor 6:1 com mix todo aberto e input ↑ / output ↓ [14:26–14:46]; EQ com cortes e boost leve em 51 Hz [15:10–15:23]; saturação com tone escurecido e output compensado [15:31–15:52]. Aplicação: **Glue Compressor + Drum Buss/Saturator só no grupo de bateria**, com o tone escurecido e comparação de nível — o autor reforça que é sutil mas aparece "on bigger sound systems" [16:11–16:18].

### Regras para não engordar o sub nem criar brilho metálico

1. **Ghost/rumble sempre filtrados** — o vídeo encurta o ghost e filtra o rumble [02:36, 03:41–03:50]; em low-end mono, HP obrigatório acima do sub. *(Inferência de engenharia, alinhada ao vídeo.)*
2. **Saturação antes de EQ** nos agudos [11:23–11:47]: saturar e depois cortar ressonância rende mais que subir agudo.
3. **Nível baixo + LFO lento** no Simpler [08:42–08:49] cria movimento sem adicionar camada nem brilho.
4. **EQ estreito** no noise/hat [07:37, 13:23] em vez de boost largo.
5. **Bus com tone escurecido e level match** [15:45–15:52] para a saturação não virar aspereza metálica.

### Ordem de construção sugerida (inferência, não está no vídeo)
Compassos 1–16 kick + rumble + ghost · 17–32 percussão grave e média · 33–48 hats + shaker · 49–56 open hat pontual + noise · drop: mesma base com bus e acentos. Respeitar as subdivisões deslocadas do groove em todas as camadas.

## Prioridade e esforço

- **Prioridade: alta.** Ataca exatamente a fundação que o motor precisa: kick em camadas, rumble, ghost e hats por velocity. Nada disso depende de compra.
- **Esforço: médio.** São 4 cadeias para montar (kick 3 camadas, rumble com sidechain, hats/shaker com LFO + vocoder, bus), todas com stock do Live 12 + Serum 2. O custo real é de escuta e ajuste fino, não de instalação. Os pontos de risco são o controle de low-end no rumble/ghost e a escolha de saturação no bus.

## Trechos de prova

> "ghost track just duplicated my kick drum but made it way way shorter so we don't have interference in the uh in the low frequencies" — [00:03:41–00:03:50]

> "the velocities is where the fun comes in because the velocities are responsible for the swing and the overall feel of my higher track" — [00:06:46–00:06:55]

> Recurso esquecido do Simpler: LFO interno lento modulando volume e pan (SINEE Global) — [00:08:31–00:08:49]
