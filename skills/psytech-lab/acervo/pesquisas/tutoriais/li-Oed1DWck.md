# Granular Sound Design: Offset Playheads & Poly-Modulation for Lush Atmospheres

- **Canal:** Sonic Academy
- **URL:** https://www.youtube.com/watch?v=li-Oed1DWck
- **Duração:** 8:10 (490 s)
- **Tema:** textura-atmosfera (sound design granular)
- **Legenda:** automática em inglês, faixa original — lida integralmente. (A tentativa de baixar a faixa "en" padrão esbarrou em limite de requisições do YouTube; a faixa original do idioma baixou e foi lida. Não há legenda manual.)
- **Natureza:** aula de sound design; todas as citações abaixo são literais da transcrição, com timestamp; números da seção de aplicação são **proposta do estudo**, não conteúdo do vídeo.

## Técnica ensinada (2-4 frases)

O vídeo transforma uma guitarra de biblioteca em uma atmosfera granular usando grãos longos, densidade alta e um envelope de grão não percussivo; o autor diz que grão longo + densidade alta fica "more smooth", enquanto um envelope percussivo fica "scratchy" (00:01:19.400, 00:01:31.160, 00:01:39.640). O ponto central é separar os **playheads**: `repeats` apenas gera grãos extras do mesmo ponto (e tende a somar volume), então ele liga o **voice stack** e desloca o playhead de cada uma das quatro vozes para uma região diferente do sample (00:02:44.160–00:02:55.440, 00:03:59.840–00:04:17.079). Cada voz ganha pan, pitch, densidade e tempos próprios; o mesmo "random por voz" pode ser feito com um modulador Random em **poly mode**, que dá um valor diferente a cada voz (00:05:10.440–00:05:18.520). Ele fecha com uma voz uma oitava acima e outra uma oitava abaixo, envelope, pitch tracking ligado e delay/diffusion (00:06:17.360, 00:06:26.560, 00:06:51.680, 00:07:07.120).

## Ferramenta usada no vídeo (plugin/stock)

| Elemento | O que o vídeo mostra | Prova |
|---|---|---|
| **Fragments** | Device granular mostrado no vídeo; a nomenclatura (Fragments/voice stack/Diffusion) indica Bitwig Studio — ver nota abaixo. É para onde vai o sample de guitarra. | "we're going to go straight to fragments here" (00:00:36.120); "This fragments is really really fun to play around with" (00:07:38.520) |
| **Voice stacking** | Transforma 1 playhead em 4 playheads independentes. | "we just turn that on, and then we can have four different playheads here" (00:02:53.080–00:02:55.440) |
| **Random modulator (poly mode)** | Modulação aleatória independente por voz; também pode ser estática com "hold rate zero". | "set to poly mode ... give each one uh a different um random value" (00:05:10.440–00:05:18.520); "hold rate zero" (00:05:30.840–00:05:40.120) |
| **Diffusion** | Reverb/difusão com algoritmos "reverse" e "space" no final. | "one of the diffusions like the reverse or the space algorithm" (00:06:51.680) |
| **Fonte** | Guitarra de uma "contact library" (provavelmente Kontakt; a legenda automática escreve "contact"). | "I've just played in from a contact library just some sort of guitar part here" (00:00:16.640) |
| **Pitch tracking** | Ligado para tocar em escalas/tonalidades. | "pitch tracking is on so we can play this on different scales and keys" (00:07:07.120) |

**Dependência real:** Bitwig Studio. O vídeo não nomeia o DAW na transcrição; a identificação vem dos devices (Fragments, voice stack, Diffusion) — **inferência**, não fala literal. Não há ANA 2, VELA, SideKick nem Kick 3 no vídeo.

### O que o vídeo NÃO especifica

- Não dá valores numéricos de grain size, density, offset, pan, random pitch, decay de reverb ou mix. Ele ajusta de ouvido e descreve qualitativamente ("longer grain", "higher density", "slight pitch variation").
- Diz apenas "an entire octave" para a voz 4 e "down an octave" para a voz 1; "four different playheads"; "hold rate zero"; "loop two / ping pong".
- Não nomeia a biblioteca de guitarra além de "contact library".

## Tradução para ambiente comum: Serum 2 (GranularOsc), Live 12 (Granulator III / Simpler / Echo / Hybrid Reverb / AutoPan), Kontakt (fonte), Vital/Massive X/Surge XT/Diva (apoio tonal)

O conceito não depende do Bitwig: qualquer motor granular com sample + múltiplas vozes + random por voz + pan + reverb difuso reproduz. A única coisa que não mapeia 1:1 é o **playhead independente por voz**; resolve-se com múltiplas instâncias/slots.

### Serum 2 — GranularOsc (caminho principal)

| Conceito no vídeo | Equivalente no Serum 2 | Observação |
|---|---|---|
| Guitarra no sampler | oscilador com fonte granular (WAV) | os slots A/B/C = até 3 "playheads" por instância |
| Fragments (granular) | GranularOsc | mesmos controles básicos: density, grain length, random |
| Density | `granular_density` (0–30) | mais alto = mais grãos |
| Grain size | `granular_grain_length` (ms) | longo = corpo/suave; curto = brilho/scratch |
| Forma do grão | `granular_random_window_amount` / `granular_random_window_skew` (parcial) | a window shape completa não é exposta por automação; ajustar na GUI |
| Repeats | `granular_density` + `granular_max_grains` | não há "repeats" separado; `max_grains` é o teto de sobreposição |
| Motion/random | `granular_random_offset`, `granular_random_pitch`, `granular_random_pan`, `granular_random_grain_length` | `random_offset` é spray por grão, **não** offset estático por playhead |
| 4 playheads deslocados | 3 slots granulares com regiões/samples diferentes + 1 instância extra (ou 3 instâncias) | a posição do playhead por voz não é exposta por automação; se a GUI tiver, ajustar lá |
| Voice stack spread | pan por oscilador + `granular_random_pan`; `voice_unison.random_pan` no GLOBAL | |
| Random por voz ("poly") | `voice_unison.random_pan` / `random_detune` / `random_filter_cutoff` (GLOBAL > VOICE CONTROL) ou `random1`/`random2` na matriz | `random1/2` são por nota; para por playhead, instâncias separadas |
| Pitch sutil por voz | `granular_random_pitch` (0–12 st) | manter ≤0,5 st para não sair do campo da faixa |
| Voz +1 oitava | `oscillators[].octave = +1` | |
| Voz −1 oitava | `oscillators[].octave = −1` | **evitar em atmosfera psy**: engorda o sub; se usar, HPF 250–300 Hz |
| Pitch tracking | o granular responde ao MIDI por nota; `granular_length_key_track` é outro parâmetro (tamanho do grão segue a nota) | conferir o toggle de pitch tracking na GUI |
| Loop / ping-pong | `granular_loop` (loop dentro da janela do grão) e `granular_reverse` | no vídeo o loop é acionado no próprio device ("loop two", "ping pong"); não é o mesmo controle |
| Diffusion | Hybrid Reverb + Echo no Live | não há algoritmo "reverse/space" idêntico; o papel é a cauda difusa |

**Limite importante:** o controle de **posição do playhead** (o coração do vídeo) não se automatiza de forma confiável via patch — use a GUI do Serum 2 ou separe em 2–3 instâncias/slots com posições diferentes.

### Live 12

- **Granulator III** (Max for Live; incluído no Suite — conferir instalação) é o equivalente mais literal do Fragments: uma instância por playhead, com position/spray/size/pitch/voices. Para 4 playheads, 4 instâncias (ou 3 + uma camada de oitava).
- **Simpler/Sampler** não têm modo granular; seguram a fonte, não granulam. O papel granular é do Granulator III.
- **AutoPan** → movimento lento de pan por camada; o voice stack spread do vídeo é **pan estático por voz**, então o pan principal é manual por instância; AutoPan entra só como movimento extra.
- **Echo** → delay filtrado, feedback baixo, sync pontuado.
- **Hybrid Reverb** → cauda longa e difusa, low cut no retorno.
- **Shifter** → não é necessário; para oitavas, mude o pitch na própria instância granular (evita artefato de formante).
- **Operator** → não tem papel granular nesta receita; fica para reforço tonal/sub, se necessário.
- **"Poly modulation" por voz:** no Live, o caminho robusto é MPE ou instâncias separadas; não dependa de um Random global para soar "por voz". (Recomendação do estudo, não do vídeo.)

### Kontakt (fonte) e os outros synths

- **Rubber Bridge Guitar** (quando disponível) é a fonte mais próxima da guitarra do vídeo. Renderize uma nota/frase na tônica da faixa (4–8 compassos), normalize e alimente o GranularOsc/Granulator.
- Outras bibliotecas atmosféricas servem como matéria-prima; um órgão/organ dá sustain tonal estável para camada de reforço. O Kontakt é **fonte**, não o motor granular desta receita — a alocação específica de bibliotecas é inferência a partir do papel de cada uma.
- **Diva, Vital, Massive X, Surge XT:** não são o carrier granular desta receita e o vídeo não usa nenhum deles. Uso possível: pad tonal de reforço **abaixo** da atmosfera, ou dobrar a fundamental com filtro. Não tente reproduzir o Fragments neles; o caminho direto é Serum 2 ou Granulator III.

## Aplicação concreta (**proposta**)

**Onde:** a função principal é **atmosfera** — uma cama sustentada que preenche o miolo (300–1.200 Hz) e parte do alto-médio (1.200–4.000 Hz) sem tocar no sub. A mesma fonte pode virar uma camada secundária de **madeira** (grãos mais curtos, banda 400–2.000 Hz). Não é elemento rítmico.

### Receita proposta (números = proposta do estudo)

1. **Fonte e afinação.** Guitarra de biblioteca, madeira ou field recording; toque na tônica da faixa e renderize 4–8 compassos. Normalize, corte silêncio. O vídeo parte de guitarra (00:00:16.640).
2. **Três camadas/playheads** (3 slots granulares do Serum 2, ou 3 instâncias de Granulator; no Live, um Instrument Rack com 3 chains recebendo o mesmo MIDI):
   - **A — corpo:** grain 120–200 ms, density 12–18, max_grains 24–48, random_offset 15–30%, random_pitch 0, pan centro, HP 250 Hz.
   - **B/C — movimento/largura:** mesmo sample em outra região (outro crop ou scan da GUI), grain 80–150 ms, density 18–24, max_grains 32–48, random_offset 30–50%, random_pitch 0,1–0,3 st, pan 35–50% L/R, HP 300 Hz.
   - **D — ar (opcional):** +1 oitava, grain 60–100 ms, density 18–24, HP 400–500 Hz, nível baixo, pan oposto. É a camada que ataca o vale de 1.200–4.000 Hz sem deixar o corpo metálico.
   - **Não** adicione a camada −1 oitava. O vídeo faz isso para "make this even bigger" (00:06:26.560); aqui ela engordaria o sub e brigaria com o low-end mono. Se usar em breakdown, HP 300 Hz.
3. **Variação por voz.** random_pitch ≤0,5 st; random_pan 15–30%; random_grain_length 10–20%; densidades diferentes por camada. O vídeo usa "slight pitch variation" e variação de density/times (00:05:54.360, 00:06:01.440); os valores são do estudo.
4. **Estéreo.** Pan manual 35–50% por camada, nunca hard; a decorelação vem dos playheads diferentes, não de delay Haas. Confira correlação/mono: o grave continua mono; a atmosfera é estéreo acima de 300 Hz.
5. **Filtros.** HP 250–300 Hz (24 dB/oct) em todas as camadas; low-pass suave em 7–9 kHz (12 dB/oct). Se precisar de corpo, um sino largo de +1–2 dB em 600–900 Hz; se precisar de ar, a camada D em banda 1–3 kHz é mais segura que um shelf brilhante.
6. **Espaço.** Envie para Hybrid Reverb (decay 4–8 s, difusão alta, low cut 300 Hz, high cut 7 kHz, wet 20–30% em paralelo) e Echo (3/16 pontuado, feedback 20–30%, high cut 5 kHz, wet 10–15%). O vídeo usa "diffusions like the reverse or the space algorithm" (00:06:51.680); Hybrid Reverb cumpre o papel, não o algoritmo exato.
7. **Nível e dinâmica.** −18 a −24 dB sob o groove (proposta). Se a cama mascarar o kick, sidechain suave de 1–2 dB com release lento — opcional, não é do vídeo. Evite pumping.
8. **Automação de arranjo (proposta).** Entrada por camadas ao longo da seção: primeiro só A, em nível baixo; depois B; depois C; por último D e reverb aberto no clímax. O vídeo não monta arranjo.
9. **Checagem de groove.** Nada de gate/retrigger em 1/16 nem LFO tempo-sync; os LFOs ficam livres e lentos. Não coloque transientes granulares nos pontos rítmicos do groove. Confira com o groove solo e depois com o kick/subbass.

### Por função

| Função | Aplicar? | Como / por quê |
|---|---|---|
| **kick** | Não | A atmosfera não entra no bus do kick; HP e nível baixo protegem o transiente. |
| **sub** | Não | Low-end é mono; nenhuma camada granular abaixo de 250 Hz, nenhum envio para o bus de sub. |
| **baixo/rolling** | Não no fundamental | Granular no baixo borra as subdivisões do groove. Se quiser "ar", uma camada paralela 500–1.200 Hz, sidechain no baixo, nível muito baixo — extensão do estudo, não ensinada. |
| **hats/shaker** | Não | O próprio vídeo diz que envelope percussivo vira "scratchy" (00:01:31.160); em hats isso vira brilho metálico. Não granule o shaker. |
| **percussão de resposta** | Extensão opcional | Um playhead só, grão curto, envelope percussivo, BP 800–2.500 Hz, random_pitch 0 (ou ≤0,1 st), nível baixo. O vídeo ensina o **caráter** "scratchy" do grão percussivo, mas não demonstra percussão de resposta. |
| **madeira** | Sim (secundária) | Mesma fonte, grão 60–120 ms, BP 400–2.000 Hz, pan moderado. Reforça a estética orgânica sem competir com a percussão. |
| **stab** | Não (ou só cauda) | Stab precisa de ataque; granular borra o transiente. Se usar, só como cauda da atmosfera, nunca como ataque. |
| **subida** | Extensão | Automatize density/random_pitch ou faça crossfade entre duas instâncias com offsets diferentes; o vídeo não demonstra riser. |
| **atmosfera** | **Sim — principal** | 3–4 camadas/playheads como acima, preenchendo 300–1.200 Hz e 1.200–4.000 Hz, estéreo acima de 300 Hz, sub intocado. |

### Regras de segurança (**proposta**)

**Anti-sub:**
- HP 250–300 Hz na atmosfera, antes do reverb; low cut 300 Hz no retorno.
- Nenhuma voz −1 oitava; nenhum envio para o bus de sub; grave abaixo de 120 Hz só mono.
- Confira a soma mono: a camada pode ser larga, mas não pode cancelar o corpo.

**Anti-brilho-metálico:**
- Grão longo + densidade alta + envelope não percussivo — é a receita literal do vídeo (00:01:24.040, 00:01:39.640).
- random_pitch ≤0,5 st; melhor 0–0,3 st. Pitch aleatório grande desafina o campo da faixa e soa metálico.
- Fonte escura (guitarra de ponte macia, madeira, feltro), low-pass 7–9 kHz, sem exciter/ressonância alta.
- Evite grão curto + densidade alta no corpo; reserve o grão percussivo para a percussão de resposta, em banda estreita.

**Anti-groove:**
- Nada de LFO tempo-sync, gate ou retrigger rítmico; a atmosfera é sustentada.
- Nível baixo e HP impedem que ela masque o groove; teste com o groove solo.

## Valor e custo

- **Valor: alto.** A atmosfera granular é a camada mais direta para os dois vales comuns do estilo (300–1.200 Hz e 1.200–4.000 Hz), adiciona movimento/estéreo e não toca no low-end mono nem no groove. A técnica do vídeo é diretamente traduzível.
- **Custo: médio.** Exige preparar/afinar a fonte, montar 3–4 camadas com offsets, HP/pan/reverb e checar mono/fase. O limite do playhead por voz força ajuste na GUI ou múltiplas instâncias — é o principal custo.
- **Riscos:** brilho metálico (grão curto/pitch random alto), acúmulo no médio mascarando madeira/percussão, cancelamento de fase em mono, CPU com 3–4 instâncias granulares. Mitigação nas regras acima.

## Trechos de prova

> *"So, these repeats are basically just extra grains from the same playhead. Um but if you want to add in additional playheads, uh that's done with a voice stack."* — **00:02:44.160**

> *"And what I really want to do is separate the play heads so that what we're getting is um multiple different areas across this entire sample that they're generating the grains from."* — **00:04:02.400**

> *"Um that one you could do by using a random modulator and just making sure that it's set to poly mode which just means it's going to give each one uh a different um random value."* — **00:05:10.440**

### Outras citações usadas no corpo

- *"If you're looking for something that's going to turn into sort of a smooth atmosphere, uh typically like a longer grain with this kind of shape is going to be a good thing"* — 00:01:19.400
- *"Obviously this kind of percussive shape is going to give you a more scratchy kind of uh texture."* — 00:01:31.160
- *"Higher density with longer grains is going to be more smooth like that."* — 00:01:39.640
- *"just do watch your volume then, cuz now at this stage they're all kind of being generated from the same point."* — 00:01:52.240
- *"we just turn that on, and then we can have four different playheads here."* — 00:02:53.080
- *"The voice stack spread is also useful."* — 00:03:11.720
- *"by default, they have repeats and motion currently on. So, there is already randomization happening."* — 00:03:50.120
- *"We can have this loop two. Ping pong looping."* — 00:04:49.240
- *"you could also have that as a static one obviously by doing hold rate zero and then triggering that with a sync like so. So, it generates a different value for each voice."* — 00:05:30.840
- *"We can add some slight pitch variation."* — 00:05:54.360
- *"Add variation to the density and to the times."* — 00:06:01.440
- *"voice four. We'll pitch that right up an entire octave."* — 00:06:15.200
- *"And to make this even bigger, we can go down an octave with voice one."* — 00:06:24.960
- *"if we run it through one of the diffusions like the reverse or the space algorithm on this one is really really nice for this kind of stuff."* — 00:06:47.360
- *"let's also make sure that pitch tracking is on so we can play this on different scales and keys."* — 00:07:05.040

## Limites do estudo

Sem escuta do áudio; leitura integral da legenda. Todos os números da receita são proposta de partida (a legenda não registra valores); os parâmetros citados do Serum 2 seguem a nomenclatura de automação dele — conferir os nomes na GUI.
