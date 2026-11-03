# Building Tension in Tracks

**Canal:** Sonic Academy · **Apresentador:** Protoculture (citado na descrição: "Protoculture's back with a new video")
**Vídeo:** `bOEc9c3pGi8` · duração 1363 s (22:43)
**Legenda:** automática EN obtida e lida via yt-dlp · descrição lida — capítulos: `00:56 Classic methods · 04:31 8 bar delay · 07:46 8 bar low cut · 08:35 16 bar pitch shift · 11:15 16 bar frequency shift · 12:17 Shepard Tones · 20:22 Result`

> **Nota de escopo (não contornada):** só o capítulo `07:46–08:35` ("8 bar low cut") trata de grave. Do resto do
> vídeo, ~85% é build/tensão de arranjo e mix (modulação multi-compasso, delay/reverb, atmosfera, Shepard).
> O mapa diz explicitamente qual trecho sustenta o quê.
>
> **Legenda:** `[V]` = trecho literal da legenda automática (erros de ASR preservados); `[I]` = inferência/tradução, não dita pelo vídeo.

---

## Técnica ensinada (2-4 frases)

O vídeo troca a mudança óbvia de arranjo por **curvas de modulação sincronizadas ao projeto, em compassos** (8, 16 e 32), unipolares e com reset, que sobem e zeram a tensão repetidamente — `[00:05:46.160]` `"to sync this to the project and let's"` / `[00:05:53.440]` `"bars and we can then just adjust our"` / `[00:05:59.919]` `"going to want these set to unipolar mode"` `[V]`. Essas curvas são globais e apontadas para poucos parâmetros por vez: **low cut do kick**, **cutoff do rolling bass**, mix de delay/reverb na percussão, pitch do ride, frequency shifter e duas instâncias de flanger com LFO em oposição. A ideia central é energia sem volume: `[00:04:37.680]` `"almost be inaudible in the track but can"` / `[00:04:39.600]` `"really add to this sort of overall build"` `[V]`. A camada avançada é o **Shepard tone**: duplicar a curva e inverter a fase para dois processos fadearem um contra o outro enquanto a altura cai, gerando subida perpétua sem resolver `[V]` (`[00:13:30.639]`–`[00:13:49.720]`).

---

## Ferramenta usada no vídeo (plugin/stock)

| Ferramenta | Para quê no vídeo | Evidência |
|---|---|---|
| **Bitwig Studio — project modulation / global modulators** | Curvas de 8/16/32 compassos, sync ao projeto, unipolar, aplicáveis a qualquer parâmetro | `[00:05:05.720]` `"kind of have a set of global modulators"` / `[00:05:09.000]` `"in bitwig uh that you can apply to"` / `[00:05:32.960]` `"come to the project settings here I've"` / `[00:05:34.440]` `"got the project modulation options open"` `[V]` |
| **Bitwig — chain + global dry/wet** | Colocar os efeitos num "chain" e dosar o conjunto pelo dry/wet | `[00:18:02.039]` `"because this is in a chain we can"` / `[00:18:03.799]` `"use the global dry wet and back"` `[V]` |
| **Bitwig — delay** | Throw de delay na percussão: estéreo, difusão, feedback | `[00:06:32.800]` `"set that to stereo add up some of"` / `[00:06:35.479]` `"the little bit of diffusion a little bit"` / `[00:06:37.599]` `"of um feedback on that"` `[V]` |
| **Bitwig — flanger (2 instâncias)** | Par de flangers com LFOs em oposição de fase = Shepard em material mid-bass | `[00:16:45.800]` `"one so we've got two flanges moving in"` / `[00:16:48.680]` `"and out of each other the whole time"` `[V]` |
| **Bitwig — frequency shifter** | Deslocamento sutil e glides no loop de tamborim | `[00:11:18.160]` `"use something like a frequency shifter"` / `[00:11:45.480]` `"easy but a frequency shifter works"` `[V]` |
| **UVI Falcon — script "Shepherd"** | Shepard tone pronto, sem construir à mão | `[00:12:56.480]` `"and Falcon has a script"` / `[00:13:02.320]` `"Shepherd which will basically have this"` `[V]` |
| **Sonic Academy ANA 2 — patches "consistent Rises"** | Rises Shepard prontos que o apresentador já fez | `[00:12:41.639]` `"of Ana 2 as well um I have made some"` / `[00:12:45.199]` `"consistent Rises uh but just for the"` `[V]` |

**Não aparecem no vídeo:** ANA 2 fora da menção acima, VELA, SideKick, Kick 3, Kickstart. O vídeo **não** depende de Kick 3/SideKick — a pressão vem de modulação e filtro, não de ducking.

---

## Tradução para ferramentas Live 12 / Serum 2

**O vídeo usa três recursos fora do Live 12 nativo:** (1) moduladores **globais de projeto** do Bitwig; (2) o script **Shepard** do Falcon; (3) os patches de rise da **ANA 2**. Todos os três sobrevivem como conceito — nenhum exige o plugin.

| Conceito no vídeo | Equivalente (Live 12 / Serum 2) | Como montar | Limite / risco |
|---|---|---|---|
| **Global modulator de projeto** (uma curva serve qualquer parâmetro) | **Live 12 não tem modulador global nativo** `[I]`. Caminho garantido: automação de Arrangement. | Desenhar a rampa de 8/16/32 compassos na lane do parâmetro. Para "um controle move vários alvos": Audio Effect Rack numa **Group track**, uma Macro mapeada em vários parâmetros com min/max próprios, e automatizar só essa Macro. | Automação é por lane — não existe curva compartilhada. O Rack resolve vários alvos *dentro* de uma track/group, não no projeto inteiro. |
| **Curva sync em compassos, unipolar, com reset** | Envelope de automação em Arrangement (ou clip envelope *unlinked* em Session, com loop de 8/16 compassos) `[I]` | Rampa 0→100%→0 no span; "reset" = último ponto volta a zero no compasso de corte. | Em Session o clip envelope só vale no clip; no Arrangement é preciso redesenhar por seção. |
| **Macro limitando a profundidade** ("não quero sempre full on") | Macro do Rack com range mínimo/máximo restrito `[I]` | Macro controla o *amount* do efeito (wet, send, depth), não o parâmetro base. | — |
| **Delay throw na percussão** (estéreo, difusão, feedback) | **Echo** (Live) num Return, send automatizado pela rampa `[I]` | Echo no Return; a rampa move o **send**, não o wet do device (mantém o dry intacto). | Eco com feedback alto em hats vira lama em 16 compassos — limitar feedback. |
| **Low cut do kick em ciclo de 8 compassos** | **EQ Eight** (low cut) num ramo **paralelo** do kick `[I]` | Duplicar o kick, high-passar o ramo em 150–300 Hz, e mover frequência/ganho desse ramo pela rampa. Fundamental e sub ficam no ramo seco. | Aplicar direto no kick inteiro mexe no peso e briga com o sub. |
| **Cutoff do rolling bass via macro** | **Auto Filter** (LPF) no baixo `[I]` | Rampa de 8 compassos movendo o cutoff só entre ~300 Hz e ~1,2 kHz, sem tocar o fundamental. | Cutoff abaixo de ~250 Hz engorda/afina o sub; não descer. |
| **Pitch do ride em 16 compassos** | **Shifter** (Pitch) ou transpose do Simpler/Sampler `[I]` | Rampa de 16 compassos com ±poucos cents; o vídeo usa "speed curve" e reduz até ficar quase inaudível `[V]` (`[00:09:42.360]` `"to be even more subtle than"`). | Vira "riser" óbvio se passar de ~50 cents. |
| **Frequency shifter** | **Shifter** do Live, modo Frequency Shifter (Coarse/Fine em Hz) — correspondência 1:1 `[I]` | Só numa **cópia** do shaker/tamborim, range pequeno, rampa de 16–32 compassos. | Frequency shifter desloca todos os parciais por Hz fixo e destrói relações harmônicas → é a origem do brilho metálico. Manter mix baixo e banda limitada. |
| **Dois flangers em oposição de fase** | 2× **Phaser-Flanger** em paralelo (ou FX Flanger do Serum 2 com 2 LFOs de curva espelhada) `[I]` | Rampas opostas em Delay/Feedback e volumes cruzados; dry/wet no Rack. | Comb filtering forte em mid-bass oco; high-passar o ramo em ~300 Hz. |
| **Shepard tone** (Falcon script / ANA 2 patches) | **Vital** (LFOs com controle de fase) ou **Serum 2** (10 LFOs + curvas desenhadas + mod matrix) `[I]` | Vital: 2 osc uma oitava apart, LFO de rampa → pitch de ambos, 2 LFOs de volume com **fase 180°**. Serum 2: 2 LFOs com a defasagem **embutida na curva desenhada** (o mod matrix não expõe fase de LFO), + 1 rampa no pitch. Alternativa mais barata: construir uma vez e **resamplear 32 compassos**. | Shepard é wideband — se invadir <200 Hz, briga com kick/sub e quebra o mono. Cortar o grave da camada. |
| **"Chain" com dry/wet global** | **Audio Effect Rack** (Dry/Wet do rack) `[I]` | Empacotar o par de efeitos e dosar tudo por um knob. | — |

**Papel dos demais:** **Kontakt 8** (Rubber Bridge Guitar, LOOP GARDEN, Ethereal Earth, Vintage Organs) entra como fonte da camada de madeira/atmosfera — o vídeo não usa Kontakt, então aqui é só o material, não a técnica `[I]`. **Diva / Massive X** servem como fonte de mid-bass/stab, mas não são a rota do crossfade em oposição de fase `[I]`. **Surge XT** é alternativa gratuita se Vital não estiver disponível `[I]`. **GranularOsc do Serum 2** não é necessário para nada deste vídeo — o Shepard aqui é aditivo/crossfade, não granular.

---

## Aplicação por função (princípios)

**Contexto usado (auditoria do set de referência contra a média de 6 referências do estilo):** meio 300–1.200 Hz −4,83 dB e 1.200–4.000 Hz −5,76 dB; low-end mono; groove com subdivisões deslocadas fora do grid, a preservar. **Grade:** a 128 BPM, 1 compasso = 1,875 s; trabalhar em blocos de 8 compassos (**1 · 9 · 17 · 25 · 33 · 41 · 49…**).

O ponto decisivo: **toda modulação deste vídeo é de timbre/tempo-de-ciclo, não de posição rítmica** — nenhuma delas toca o grid. É por isso que ela é compatível com grooves deslocados: o groove continua intacto e o que "respira" é o filtro, o espaço e o brilho.

| Função | O que aplicar | Compassos | O que NÃO fazer |
|---|---|---|---|
| **Kick** | Rampa de 8 compassos movendo o **low cut de um ramo paralelo** (high-pass em 150–300 Hz, ±1–2 dB). O que muda é o peso percebido do corpo, não o nível. É a tradução literal do capítulo "8 bar low cut" `[V]` `[00:07:50.919]` `"apply uh we've got this low frequency"` / `[00:07:55.039]` `"apply to our low frequency cut as well"` / `[00:07:56.599]` `"so every eight bars"`. | 8 (1→9→17→25…) | Não aplicar no kick inteiro nem no fundamental: mexe no peso e cria bombeamento contra o sub. |
| **Sub** | Nada do vídeo se aplica direto ao fundamental. Se quiser movimento, mova só a **camada de harmônico** (2º/3º harmônico, ~80–110 Hz) ou a saturação lenta; o fundamental fica parado e mono. `[I]` | 16 ou 32 | Não modular high-pass nem ganho do sub. Low-end é mono — qualquer coisa que abra estéreo no sub quebra o princípio do estilo. |
| **Baixo / rolling** | **Cutoff do LPF via rampa de 8 compassos**, varrendo só 300 Hz–1,2 kHz (a faixa carente). O vídeo faz exatamente isso no rolling bass: `[V]` `[00:01:41.079]` `"sort of rolling bass one of the obvious"` / `[00:01:43.159]` `"ways of doing this is obviously by"` / `[00:01:44.680]` `"adjusting the filter cut off"`. | 8 | Não descer o cutoff abaixo de ~250 Hz — engorda o sub e come o fundamental. Não usar ressonância alta (apito em 300–600 Hz). |
| **Hats / shaker** | **Shifter em modo Frequency Shifter** numa **cópia** do shaker, shift de poucos Hz, rampa de 16–32 compassos; o shaker seco fica 100% dry e intocado. `[I]` — o vídeo usa `[V]` `[00:11:22.959]` `"take a look at this tambourine Loop"`. | 16–32 | Não passar o shaker inteiro pelo shifter: sidebands inarmônicos = brilho metálico. Banda limitada (≈400 Hz–6 kHz) e mix baixo. |
| **Percussão de resposta** | Duas coisas do vídeo: (a) **pontuar a cada 8/16 compassos** com uma variação pequena `[V]` `[00:04:07.840]` `"so by punctuating things as well every"` / `[00:04:09.519]` `"16 bars or every eight bars it's nice to"` / `[00:04:11.720]` `"put in just some sort of little change"`; (b) **camada com som diferente e uma nota deslocada** `[V]` `[00:02:38.640]` `"note off slightly but they do kind"` / `[00:02:40.319]` `"complement each"`. | 8 em 8 nos blocos | Não deslocar nota de kick/baixo — isso apaga a assinatura do groove. Deslocar só a resposta. |
| **Madeira** | Entra pelo conceito de **camadas introduzidas aos poucos** `[V]` `[00:02:18.040]` `"to layer sounds and then gradually"` / `[00:02:20.480]` `"the layers in as well what I"`: duplicar a frase de madeira num segundo instrumento (Rubber Bridge / LOOP GARDEN / Ethereal Earth) e subir o volume dela ao longo de 8–16 compassos. | 8–16 | Não duplicar em oitava abaixo (engorda o grave). Oitava acima ou registro médio. |
| **Stab** | Par de flangers em oposição de fase num **ramo paralelo high-passado em ~300 Hz**, mix baixo, rampas de 8 compassos. É a tradução do "shaper tone" no mid-bass `[V]` `[00:17:10.240]` `"almost creating a sort of um shaper tone"` / `[00:17:14.160]` `"effect on our mid base sound that we"`. | 8 | Flanger no stab inteiro comba o fundamental. Sempre em paralelo e com HPF. |
| **Subida** | Rampa de **16/32 compassos** (pitch ou frequency shifter) terminando no downbeat do drop, ou **Shepard** construído em Vital/Serum 2 e resampleado. O vídeo encadeia 32 compassos: `[V]` `[00:21:37.440]` `"going on over these 32 bars that we have"`. | 32 / 16 antes do drop | Não usar Shepard com conteúdo abaixo de 200 Hz; não deixar a subida "resolver" no drop — o Shepard por definição não resolve. |
| **Atmosfera** | Começar **100% dry** e **subir o retorno** (não o wet do device) ao longo de 16–32 compassos: `[V]` `[00:03:11.000]` `"like to go all dry so you've got no"` / `[00:03:13.959]` `"atmosphere playing"` / `[00:03:26.680]` `"dry and gradually over time I'm just"` / `[00:03:29.799]` `"volume fading in some atmospheric stuff"`. | 16 ou 32 | Reverb 100% wet serial em fonte acústica mata a presença do dry — aqui é send/return, dry preservado. |

**Como isso conversa com o déficit medido:** as três coisas que mais atacam 300–4.000 Hz — cutoff do rolling bass, flanger no stab, frequency shifter no shaker — são justamente as que **adicionam movimento** na faixa carente sem subir nível nem engordar o sub. O ganho é de *informação* (variação espectral ao longo dos compassos), não de dB. Isso é o oposto de "resolver o mid com EQ": a curva preenche o tempo, não a média.

**Onde não aplicar:** nada disso no sub fundamental, nada disso no kick inteiro, nada disso no grid. E não empilhar todas as curvas ao mesmo tempo — o próprio vídeo mostra o resultado final com pouquíssimos elementos: `[V]` `[00:21:39.480]` `"here and uh you don't have to have a lot"` / `[00:21:42.279]` `"of elements in the track to make this"` / `[00:21:44.120]` `"work"` / `[00:21:46.960]` `"much going on here at all there's just"` / `[00:21:49.039]` `"the mid-base parts and a"` / `[00:21:51.159]` `"sub and two melodic elements this is not"`.

---

## Prioridade e esforço

| Técnica | Prioridade | Esforço | Justificativa |
|---|---|---|---|
| **8-bar low cut no kick (ramo paralelo)** | **Alta** | **Baixo** | É o único trecho do vídeo que é literalmente pressão de grave sem volume; 2 lanes de automação e um EQ. |
| **Rampa de 8 compassos no cutoff do rolling bass (300 Hz–1,2 kHz)** | **Alta** | **Baixo** | O vídeo cita explicitamente como caminho óbvio `[V]` `[00:01:43.149]` `"sort of rolling bass one of the obvious"` / `[00:01:43.159]` `"ways of doing this is obviously by"`; mexe na faixa carente e não toca o fundamental nem o grid. |
| **Atmosfera entrando por volume em 16/32 compassos** | **Alta** | **Baixo** | Uma lane de send + um return. É o que faz "o mix mudar com o tempo" — a sensação central do vídeo — e combate o mid scoop com difusão, não com brilho. |
| **Pontuar a cada 8/16 compassos (hat/ride/fill)** | **Alta** | **Baixo** | Já é hábito de arranjo; custa um clipe por bloco e evita o loop estático. |
| **Frequency shifter só no shaker (cópia, range mínimo)** | **Média** | **Médio** | O vídeo afirma que funciona bem em tamborim `[V]`, mas o risco de brilho metálico é real e exige banda limitada + A/B. |
| **Par de flangers em oposição de fase no stab** | **Média** | **Médio** | Dá o deslocamento contínuo para cima `[V]` `[00:17:27.919]` `"you got this kind of"` / `[00:17:29.430]` `"constant shifting"` / `[00:17:29.440]` `"upwards um to make this sort of a little"`, sem subir tom, mas exige ramo paralelo high-passado e rampas opostas. |
| **Shepard tone (16/32 compassos)** | **Média** | **Alto** | Conceito forte e citado 3× pelo vídeo, mas sem Falcon/ANA 2 precisa ser construído (Vital/Serum 2) ou resampleado. É cor de transição, não motor. |
| **Modulador "global" replicado em várias tracks** | **Baixa** | **Médio** | Live não tem equivalente nativo; o ganho de replicar a mesma curva em 5 lanes é pequeno frente a desenhar só onde importa. |

---

## Trechos de prova: 3 citações literais da legenda com timestamp

1. **[00:04:34.360 → 00:04:41.759]** — a tese do vídeo (energia quase inaudível):
   `"really subtle changes which can uh"` / `"almost be inaudible in the track but can"` / `"really add to this sort of overall build"`

2. **[00:07:47.560 → 00:07:56.599]** — o único trecho de pressão de grave (8-bar low cut no kick):
   `"say maybe our kick as well if you wanted"` / `"apply uh we've got this low frequency"` / `"cut there we could say we want this to"` / `"apply to our low frequency cut as well"` / `"so every eight bars"`

3. **[00:13:30.639 → 00:13:49.720]** — a construção do Shepard (conceito, sem depender de Falcon/ANA 2):
   `"you have one sound which is"` / `"coming like from high to low basically"` / `"um but it fades in and out and as it"` / `"fades in and out another one is fading"` / `"in and out at a different point they're"` / `"basically just adjusting the phase of"` / `"two alfos that are bringing the sound in"` / `"and out the whole time whilst it's"` / `"pitching down uh so you can do that with"`

**Extras usados no corpo do mapa:**
- `[00:05:05.720]` `"kind of have a set of global modulators"` · `[00:05:09.000]` `"in bitwig uh that you can apply to"` — a ferramenta que o Live não tem.
- `[00:16:45.800]` `"one so we've got two flanges moving in"` · `[00:16:48.680]` `"and out of each other the whole time"` — flanger em oposição.
- `[00:21:39.480]` `"here and uh you don't have to have a lot"` · `[00:21:44.120]` `"work"` — poucos elementos bastam.

> Erros de ASR preservados nas citações: `"shaper tone"` = Shepard tone · `"shepher tones"` = Shepard tones · `"alfos"` = LFOs · `"flanges"` = flangers · `"Ana 2"/"an 2"` = ANA 2 · `"ATT track"` = the track. Nenhuma citação foi corrigida.
