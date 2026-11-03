# Durosai - Psy-Techno Track Breakdown

**Vídeo:** "Psy-Techno Track Breakdown [Ableton Project File Available (143 in my G37)]" · **Canal:** Durosai (avulso) · **Duração:** 33:08
**Legenda:** automática em inglês, lida integralmente (6.376 linhas de VTT; 797 cues após remover cabeçalhos, tags e duplicatas consecutivas). Tem legenda.
**Descrição:** só links comerciais (project file, SoundCloud, DistroKid, redes). Nenhuma informação técnica — usada apenas para confirmar título, duração e canal.

**Escopo declarado do vídeo:** breakdown de uma faixa de psy-techno/psy-trance em **A menor / E** (00:27:15), com o kick em **A, 55 Hz** (00:03:00). O vídeo **não informa o BPM** — "143" é o nome da faixa ("143 in my G37"), não o andamento. Toda transposição para outra tônica é conta do leitor, não do vídeo.

---

## Técnica ensinada

O motor do vídeo é montado com pouca correção e muita escolha de fonte: o kick é um sample **BT 808** com decay encurtado, afinado por frequency shifter e comprimido com ataque lento para preservar o bite e cortar o corpo **depois de 50 ms** (00:02:33–00:03:25); o baixo é dividido em **sub mono** e **stereo bass** — o mesmo patch de Serum (sawtooth, attack 21 ms, decay 98 ms, LFO em modo envelope no low-pass) com warp de assimetria, unison 5 e alargamento só na camada média/aguda, que passa por um HPF antes e outro depois da saturação (00:04:48–00:08:41). O elemento principal é um **arp que não é arp**: uma nota longa tocada por três LFOs — um de curva em degraus no cutoff, um de 1 compasso que abaixa o cutoff na metade, e um de **1/16 no volume** — sobre um filtro **band-pass 24 com ressonância alta** (00:09:47–00:13:52). O arranjo usa **dois patches quase iguais** do mesmo arp em **call and response** (00:14:22–00:15:20), e a mixagem resolve colisão de frequência por **sidechain** (kick, snare, lead, formant) em vez de EQ, além de **suavizar o ataque da snare** para ela dividir headroom com o kick (00:28:55–00:29:34).

---

## Ferramentas usadas no vídeo (plugin/stock)

| Ferramenta | Onde aparece | O que faz no vídeo |
|---|---|---|
| **Serum** (Xfer) | sub, stereo bass, os dois arps, stab, pitch-bend, formant, lead (00:04:48; 00:08:59; 00:17:52; 00:22:11) | "a lot of the sounds in this track were made in Serum" (00:08:59). Wavetables digital/spectral, warp de assimetria, unison, LFOs com curva editável, filtro BP 24, FX internos (distortion, chorus, phaser, hyperdimension, reverb) |
| **Ableton Live** | todo o projeto | EQ Eight, Echo, Simpler, compressor, saturator, "SSL compression" (não nomeia o plugin), automação de cutoff, sidechain |
| **BT 808 kick sample** | 00:02:33 | fonte do kick; decay encurtado |
| **RComp** | 00:03:03 | compressor do kick; ataque lento, ação depois de 50 ms |
| **Hyperdimension** | 00:07:46; 00:13:55 | alargamento estéreo; mix 16% e 8% |
| **Kickstart** | 00:21:14; 00:31:11 | sidechain "plug-in" — o autor o descreve como sidechain, não como compressor |
| **Solina (Arturia)** | 00:20:22 | pads; preset "air string two" |
| **Sound Shifter** | 00:19:43 | pitch shifter; automação de pitch na transição |
| **Waves X-Noise** | 00:25:14 | denoise por "learn" num sample de documentário; ele cita iZotope RX como alternativa |
| **FabFilter Pro-MB** | 00:22:45 | domar low-mid do lead |
| **Valhalla reverb** | 00:29:37 | reverb da snare |
| **909 sample, tops loops, fills, vocais** | 00:31:27; 00:27:44; 00:32:00; 00:23:50 | samples de packs; vocais já vinham com reverb/delay |
| **NÃO aparece** | — | ANA 2, VELA, SideKick, Kick 3, Bitwig. O vídeo é Live + Serum + plugins de terceiros avulsos |

---

## Equivalentes em ferramentas comuns (Serum 2, Live 12, synths de terceiros comuns)

O núcleo do vídeo é **Serum + Live**. Nada depende de ANA 2, VELA, SideKick, Kick 3 ou Bitwig. O que não é stock são os plugins avulsos (RComp, Hyperdimension, Kickstart, Sound Shifter, X-Noise, Pro-MB, Valhalla, Solina); quase todos têm equivalente conceitual nativo ou no Serum 2 — a exceção real é o **X-Noise** (denoise espectral), sem equivalente nativo no Live.

| Elemento do vídeo | Equivalente | Observação |
|---|---|---|
| **Serum**: wavetables digital/spectral, warp de assimetria, unison, LFO com curva por pontos, BP 24, drive, chorus, phaser, hyperdimension, reverb | **Serum 2** — mesmo motor: wavetables digitais/análogas, modos de warp (`bend`, `pwm`, `fold`, `sync`…), unison/detune, filtros band-pass 24, LFOs com curva por pontos | Tradução literal do motor. O modo exato de **assimetria** do vídeo **não foi identificado** — o caráter equivalente teria de ser conferido no app, não presumido. O que importa é a curva em degraus do LFO |
| **HPF antes do drive + HPF depois do drive** | **EQ Eight** (ou High Cut do próprio Serum) | É a técnica mais transferível do vídeo e a que impede o sub de engordar |
| **RComp** (ataque lento, age após 50 ms) | **Compressor** do Live com ataque ~50 ms e threshold que só pega o corpo | O vídeo descreve o comportamento, não os valores de ratio/threshold — não copiar número que ele não dá |
| **Kickstart** (sidechain) | **Compressor** do Live com sidechain externo, ou automação de volume/Shaper | O conceito é ducking por fonte, não o plugin |
| **Hyperdimension / chorus / unison** | **Chorus-Ensemble** · **AutoPan** · **Utility** (width); no Serum 2, o FX de chorus/width do próprio patch | Só na camada média/aguda; nunca no sub. O nome exato do FX equivalente no Serum 2 **não foi verificado** nesta leitura |
| **Sound Shifter** (pitch automatizado) | **Shifter** (modo Pitch) automatizado, ou automação do Transpose do clipe/Simpler | Shifter tem latência/artefato; para loop inteiro, automação de transpose do clipe é mais limpa. **Não verificado** |
| **Waves X-Noise / iZotope RX** | **Live 12 não tem denoiser espectral nativo** | Sem equivalente direto. Gate/EQ cirúrgico não é a mesma coisa; se a fonte tiver chiado, resolver na curadoria da fonte |
| **FabFilter Pro-MB** | **Multiband Dynamics** (Live) | Mesma função: domar low-mid sem cortar o corpo inteiro |
| **Solina (Arturia)** | **Diva** ou **Serum 2** (saw/Juno + chorus); biblioteca de pads orgânicos se a textura for mais acústica | O que define o pad do vídeo é a voicing e o movimento do acorde, não a marca. Solina é máquina de cordas; Diva é analógico — não é o mesmo timbre, é o mesmo papel |
| **Valhalla reverb** | **Hybrid Reverb** | — |
| **"SSL compression"** | **Glue Compressor** (Live, modelo SSL bus) | O vídeo não nomeia plugin; "SSL compression" é a descrição dele |
| **BT 808 / 909 / tops / fills / vocais de pack** | **Simpler/Sampler** com samples; ou síntese | Nota: o vídeo resolve metade do som por curadoria de sample de pack. Quem trabalha com fonte só sintetizada não transpõe essa metade automaticamente |
| **Ableton Echo / EQ Eight** | **Echo / EQ Eight** | Nativo, literal |
| **Pads, vocais, fills** | Atmosfera/arranjo | Fora do núcleo do motor de grave |

**Conclusão de traduzibilidade:** **sim**, com uma ressalva real. A arquitetura (split sub/corpo, pluck por LFO, arp por gate de 1/16, sidechain por colisão de frequência, HPF em volta da saturação) sobrevive inteira sem os plugins do canal. O que **não** sobrevive é a dependência de samples de pack: o vídeo resolve metade do som por curadoria de amostra.

---

## Notas de aplicação (referência)

**Contexto do projeto de referência usado nas notas:** médio 300–1.200 Hz em **−4,83 dB** e 1.200–4.000 Hz em **−5,76 dB** contra a média de 6 referências externas; low-end **mono**; groove com subdivisões deslocadas **.27/.77**. Nesse contexto, 5–12 kHz também estava deprimido contra a média, mas com **mais** agudo relativo que duas das referências — conclusão: não subir hat para "fechar" a média; o alvo é uma das referências, não a média.

*As notas abaixo são aplicação do estudo; os valores citados do vídeo são literais e estão com timestamp.*

- **Kick**: conferir corte abaixo de 30 Hz (o vídeo corta, 00:02:48); testar compressor com ataque lento agindo **após ~50 ms** só no corpo, mantendo o transiente (00:03:03); camada de hat só se o topo do kick estiver opaco, e **band-limited** (cortar graves e o extremo superior, 00:03:42). **Não copiar** a afinação de 55 Hz/A: afinar na tônica própria e medir a fundamental real — afinar "no nome da nota" sem medir pode duplicar energia com o sub.
- **Sub/baixo**: a regra que entra primeiro é a **dupla de HPF em volta de qualquer drive** — cortar antes de saturar e cortar de novo depois (00:06:32–00:06:55). O desenho attack 21 ms / decay 98 ms / LFO no low-pass é um **sub curto e plucky** — testar só se o sub atual estiver longo/embolado. **Nunca** unison/chorus/alargamento no SUB: o vídeo alarga só a camada média/aguda.
- **Hats/shaker**: dois patches **complementares** (não iguais — "they're not playing the exact same pattern, but they are complementing each other", 00:30:03), ambos no upbeat e diferindo nos fillers; **cortar a aspereza em ~6 kHz** em vez de realçar (00:30:57); sidechain da hat na snare quando os dois caem juntos. Não usar o topo para levantar 1.2–4 kHz: o próprio vídeo corta o extremo agudo da hat e low-passa o loop de fundo para tirar o prato (00:28:32).
- **Percussão de resposta / call and response**: duplicar o patch, mudar só wavetable/warp e o desenho do LFO, e deixar um chamar e o outro responder (00:14:22–00:15:20). O sidechain da cama (atmosfera/pad) para a resposta faz a resposta aparecer sem subir volume (00:21:55). Separar por **papel** e sidechain, não por volume.
- **Tensão harmônica por nota adicionada**: o stab é um acorde "kind of an E minor" com **F# acrescentado** "just to make it sound a little bit more dissonant" (00:15:39). O gesto transferível é a nota de tensão, não o acorde — a escolha é decisão musical do projeto, não tradução automática.
- **Subida sem riser**: automação de **pitch** no elemento que já existe (00:19:47) ou **delay time descendente + feedback** no vocal/efeito (00:26:04). Ambas cabem em Shifter/Echo nativos e não pedem riser novo; sweep de ruído branco é anti-pattern declarado do psytech de referência. Subida gradual terminando no fade, sem salto agudo na virada.
- **Atmosfera**: loop/textura contínua filtrada (low-pass para não trazer prato/chiado), volume baixo, sem reverb longo — "cama de movimento em vez de EQ estático" para o miolo. Fonte: síntese ou material já existente, se o projeto não admite sample de pack.

**Ordem de ataque sugerida (1 mudança por A/B):** (1) HPF antes/depois do drive no sub e no baixo — menor risco, maior retorno; (2) sidechain por colisão de frequência (hat→snare; cama→resposta/lead); (3) pluck por LFO envelope no cutoff em resposta/stab; (4) gate de 1/16 no volume só numa camada de resposta, nunca no baixo/rolling (é onde o groove deslocado corre risco); (5) dois patches em call/response; (6) articulação de baixo por seção (mexer em acentuação, não em padrão); (7) kick por último — é o elemento mais sensível e o mais provável de já estar aprovado.

---

## Trechos de prova: citações literais da legenda com timestamp

> "Kick is also actually straightforward. Um it's just this BT 808 kick sample. Just shortening that decay so it doesn't ring out super long."
> — 00:02:33.840–00:02:37.830

> "...but what I'm doing is after 50 milliseconds, I'm tailing this off a little bit. So, what that's going to do is going to make the kick a bit more punchy, also save me some headroom in my mix cuz the kick's not going to be as loud for so long."
> — 00:03:09.440–00:03:25.830

> "So, I have it at 21 and then it's a pretty short decay, 98 milliseconds. So, that's what's making it sound very plucky."
> — 00:04:59.760–00:05:04.030

> "This plugin, because it's adding like drive and saturation, it's going to bring in again some of those more lows. So, that's why I have the second high pass right here."
> — 00:06:44.080–00:06:55.550

> "...this pattern is just one long note. So, I want this to keep looping. So, I have it set to 1/16. So, this envelope's going to repeat um every 16th note, and that's what that arp is playing."
> — 00:12:48.240–00:12:59.510

> "And they're playing off each other. This is like a call and response thing. So, this is calling, this is responding."
> — 00:14:43.949–00:14:49.550

> "they're not playing the exact same pattern, but they are complementing each other."
> — 00:30:03.520–00:30:07.910

**Limite desta leitura:** legenda automática, com erros de reconhecimento (por exemplo "Dudesai" por "Durosai", "side techno" por "psy-techno", "sub great table" por "sub wavetable"). Nenhuma afirmação acima depende de corrigir essas palavras. O que o vídeo **não** diz: BPM, valores de ratio/threshold dos compressores, redução exata de cada EQ, nomes dos samples de pack, e a marca da maioria dos plugins de terceiros (RComp, Hyperdimension, Kickstart, Sound Shifter, Valhalla) — o autor não as nomeia.
