# Tech Tip - Granular Guitar in Ableton

**Vídeo:** https://www.youtube.com/watch?v=4q6GrRSEfhI · **Canal:** Sonic Academy (Tech Tips Vol. 38 com WNTER)
**Legenda:** automática EN — **temLegenda = true**. Descrição confirmada via `yt-dlp --skip-download --print "%(description)s"`: *"In this Tech Tip WNTER uses the texture mode in Ableton on a time stretched guitar sample to create a granular style effect."*

> **Nota de ASR (INFERÊNCIA):** a legenda automática grafa `reap itch mode` (00:02:05.509) onde o contexto é o warp mode **Repitch**; `gray at 226` (00:03:40.540) por **grain at 226**; `hit our` (00:05:14.830, 00:05:50.539) por **hit R** (reverse); `time searching` (00:06:33.200) por **time-stretching**; `grand in their style mode` (00:08:57.280) por **granular style mode**; `PAC's library` (00:01:35.360) por **Packs library**. Cito literalmente e sinalizo `[ASR: …]` quando a palavra crua não faz sentido.

---

## Técnica ensinada (2-4 frases)

O vídeo ensina a transformar **uma única nota longa de guitarra** em pad granular sustentado usando só o **warp mode "Texture"** do Ableton: recorta-se um trecho com ataque e fim definidos (00:03:21.650 "so we'll slice our audio so that we have just our start and end points there"), muda-se de Repitch para Texture (00:02:05.509 "change this from reap itch mode [ASR: Repitch] to texture mode"), **zera-se o Flux** e sobe-se o **Grain Size até 226** (00:03:38.140 "turn the flux all the way down and put the gray [ASR: grain] at 226"; 00:06:14.389 "put the grain size all the way up so we have really nice long grains and put the flux all the way down"), e então **estica-se o clipe ao máximo** (00:04:02.770 "to time stretch this all the way so just slow that down as much as possible"). O resultado é um tom contínuo, sem o "pulo" de altura que o Repitch fazia (00:06:30.380 "so it gives us a nice sustained tone"; 00:06:38.120 "when it was just set to the standard reach mode [ASR: Repitch] I didn't actually play one sustained note it kind of jumped around"). Em seguida o áudio é **resampleado** para uma track nova (00:04:31.700 "we're going to go ahead and resample this into a new audio channel"), **revertido** (00:05:13.270 "go ahead and reverse that"), **esticado duas vezes** (00:05:23.680 "time stretch it twice so slow down once and then once more"), revertido de novo, tem o **início cortado** porque ali ainda não há tom sustentado (00:05:52.759–00:05:59.870 "because it's just gonna sound a little bit strange because it's not going to give us a sustained tone") e recebe Texture outra vez. Por fim, **duas cópias transpostas — −5 e −8 semitons — formam o padrão melódico** (00:06:50.150 "turn this down five semitones"; 00:07:00.950 "we're gonna pitch this down negative eight semitones"; 00:07:06.789 "that just gives us a nice melodic pattern") e o som é lavado com delay e reverb (00:07:31.840 "add a little bit of reverb and delay to kind of wash out the sound").

O ponto mecânico que sustenta tudo é explicado no início: o Texture "cuts your audio into small little slices or grains that have been played backed in sequence" (00:01:12.500–00:01:16.399) e "gives us really nice glitchy texture audio upon playback" (00:01:18.049). O vídeo trata o artefato de esticamento como **feature**, não defeito: 00:07:21.900 "you can also hear some nice audio artifacts in the top end of that signal as well some sort of time stretching distortion".

**O que o vídeo NÃO ensina:** não há EQ, não há high-pass, não há sidechain, não há receita de arranjo; e o trecho musical do vídeo não está em nenhuma tonalidade específica (a transposição −5/−8 é só para criar intervalo, não para afinar em tonalidade). A frase final sobre o Simpler (00:09:04.870 "it's also available in the simpler instruments device as well") é mencionada de passagem, sem demonstração.

---

## Ferramenta usada no vídeo (plugin/stock)

**100% stock do Ableton Live — nenhum plugin de terceiro.**

- **Warp mode "Texture"** do clipe de áudio (o núcleo). Parâmetros expostos usados: **Grain Size** (levado a 226) e **Flux** (zerado). 00:01:07.729 "texture time stretching mode or the warp mode in Ableton Live".
- **Repitch** como modo de comparação/controle (00:02:05.509; 00:06:38.120).
- **Resampling** via "external in" para uma track de áudio nova (00:04:33.200 "change the external in to the guitar loop"; 00:04:51.480 "make sure to record enabled out").
- **Reverse** do clipe, tecla R (00:05:13.270).
- **Simple Delay** — 00:07:41.240 "go over to the simple delay"; ajustes: delay time "three … three and three so it's the same" (00:07:46.639), feedback "about 35%" (00:07:52.039), dry/wet "just over 30" (00:07:54.560). **A unidade do tempo de delay não é dita no vídeo** — o texto só registra "three and three"; não se inventa ms nem divisão.
- **Reverb** stock, ajustes default com dry/wet "up slightly to about 65" (00:08:13.720).
- Material: **guitar loop da Core Library** do Live (00:02:52.680–00:02:58.980 "this is just a guitar loop from the core library in Ableton Live"). O demo didático usa um drum loop da Packs library (00:01:35.360).
- Menção final: o mesmo warp mode estaria disponível no **Simpler** (00:09:04.870–00:09:12.070) e no sampler (00:09:15.970–00:09:20.680 "you could always do it in the sampler"), para patch tocável por MIDI.

**Nota de versão (INFERÊNCIA, não é fala do vídeo):** o vídeo usa **Simple Delay**, device que não é o device de delay da interface atual do Live 12 (o par do Live 12 é **Echo**/**Delay**). Isso não muda a técnica: o papel dele é lavar transiente.

---

## Tradução e receita

### O núcleo traduzível, em 5 operações

A técnica não depende de um plugin — depende de uma cadeia de 5 decisões:

1. **Fonte com evento longo e sustentado** (não um loop inteiro, não um hit curto): 00:03:15.780 "grab this individual long guitar note that's right in this section".
2. **Motor de grãos com grão grande** (Grain Size 226).
3. **Zero aleatoriedade/variação de leitura dos grãos** (Flux 0) — é isso que produz o tom estável em vez de "pular".
4. **Esticamento extremo** do material = leitura muito lenta do grão, que vira cama.
5. **Empilhamento transposto de 2 cópias** (−5 / −8) + **delay/reverb** para colar transientes.

Todas as 5 existem no Live 12 nativo. **Nada aqui usa ANA 2, VELA, SideKick, Kick 3 ou Bitwig.**

### Live 12 nativo — o caminho idêntico (primeira escolha)

Não há tradução a fazer: é o mesmo device. No Live 12, o clipe de áudio tem **Warp → Texture** com **Grain Size** e **Flux**. Receita literal do vídeo:

| Passo | Ação no vídeo | Como fazer no Live 12 |
|---|---|---|
| 1 | recortar uma nota longa | Warp on, recortar start/end no clipe |
| 2 | trocar Repitch → Texture | dropdown de warp mode |
| 3 | Flux 0, Grain Size 226 | os dois knobs do Texture |
| 4 | esticar ao máximo | arrastar a borda do clipe / mudar o tempo do clipe |
| 5 | resamplear | track nova, input = **Resampling** (o vídeo usa "external in" para a track de origem — mesmo efeito) |
| 6 | reverse → stretch ×2 → reverse | tecla **R** duas vezes, esticando no meio |
| 7 | cortar o início instável | trim no início até o tom estabilizar |
| 8 | Texture de novo, Grain Size máximo, Flux 0 | mesmos knobs |
| 9 | duas cópias −5 e −8 semitons | campo **Transpose** do clipe (depois reafinar para a tonalidade da track) |
| 10 | delay + reverb | **Echo** (no lugar do Simple Delay) + **Hybrid Reverb** |

### Serum 2 — GranularOsc

O GranularOsc é um motor de grãos de verdade (aceita `.wav` e reprocessa por grãos), então ele cobre os passos 2–3 melhor que o Texture, mas **não expõe controle de "scan rate"/tempo de leitura** — ou seja, o **esticamento extremo (passo 4) não tem equivalente direto** nos parâmetros expostos pelo gerador de presets. Tradução correta: fazer o esticamento no clipe do Live primeiro (Texture), congelar/resamplear para `.wav` e só então alimentar o GranularOsc.

Mapeamento dos parâmetros que **existem**:

| Vídeo | Função | GranularOsc |
|---|---|---|
| Grain Size 226 (grande) | grãos longos = tom sustentado | `granular_grain_length` alto (o default documentado é 100 ms; referência real de fábrica usa 124 ms para textura rica — para "cama sustentada" ir bem acima disso) |
| Flux 0 | nenhuma variação de leitura | `granular_random_offset = 0`, `granular_random_grain_length = 0`, `granular_random_pitch = 0`, `granular_random_window_amount/skew = 0` |
| loop do grão (implícito no sustentado) | grão se repete dentro da janela | `granular_loop = true` (já é o default) |
| densidade do tecido | quanto de grão sobreposto | `granular_density` (escala 0–30; mais alto = mais contínuo, mais baixo = grãos audíveis) |
| esticar ao máximo | leitura lenta | **sem equivalente exposto** → pré-esticar no Live (acima) |

### Kontakt 8 — de onde vem a fonte, não o motor

Os instrumentos (Rubber Bridge Guitar, LOOP GARDEN, Ethereal Earth, Vintage Organs) **não são engines granulares**. O valor deles aqui é o **passo 1**: o **Rubber Bridge Guitar** entrega exatamente o tipo de nota longa e morta que o vídeo usa como matéria-prima (guitarra). Ethereal Earth e LOOP GARDEN servem como fonte alternativa de nota sustentada para granularizar. O processamento granular continua sendo Live ou Serum.

### Diva / Vital / Massive X / Surge XT

- **Diva**: não é granular — é modelagem analógica. Serve para a **camada tonal** (o par −5/−8 pode ser feito com dois Diva em uníssono desafinado), não para o grão.
- **Surge XT**: tem oscilador granular; o princípio (grão longo + zero randomização + leitura lenta) se aplica igual.
- **Vital / Massive X**: o vídeo não mostra nenhum deles, e não se confirma aqui qual modo granular cada versão instalada expõe — tratar como **NÃO VERIFICADO** e usar Live/Serum como rota primária.
- Em qualquer um deles, o que **não** deve ser reproduzido é o "Flux alto": sem zerar a randomização, o resultado "pula" como o Repitch do vídeo (00:06:43.400 "it kind of jumped around a little bit").

**Conclusão de traduzibilidade:** `traduzivel = true`. A técnica é stock, determinística, e a parte que falta no Serum (esticamento extremo) resolve-se antes dele, no próprio Live.

---

## Aplicação por função (kick, sub, baixo/rolling, hats/shaker, percussão de resposta, madeira, stab, subida, atmosfera)

**Contexto de referência citado no levantamento original:** um set de trabalho medido mostrou o meio carente (300–1.200 Hz e 1.200–4.000 Hz abaixo da média de 6 referências externas), low-end **mono** e groove com subdivisões deslocadas a preservar.

O ponto central: **a camada granular é excelente exatamente onde o set de referência é carente (médios) e perigosa exatamente onde há problema típico (topo metálico e grave mono).** Por isso ela entra com high-pass e low-pass obrigatórios.

| Função | Veredito | Como aplicar / por que não |
|---|---|---|
| **kick** | **NÃO** | A técnica destrói transiente e o próprio vídeo assume artefato de topo (00:07:21.900). O kick é o motor do groove — nada de grão nele. |
| **sub** | **NÃO** | Low-end é mono. Grão cria decorrelação e ruído de janela. Se qualquer camada granular existir, **high-pass 180–300 Hz** obrigatório antes de somar. |
| **baixo / rolling** | **NÃO** | O rolling vive de articulação por nota e do microdeslocamento do groove; grão borra ataque e desalinha a subdivisão. |
| **hats / shaker** | **NÃO** | São eventos curtos, e a técnica exige fonte longa e sustentada (passo 1). Além disso, o groove deslocado precisa ficar nítido — grão transforma grade em nuvem. |
| **percussão de resposta** | **uso restrito** | Só como **cauda** de uma resposta no fim de frase, e só depois de alongar a fonte. Risco: apagar o "call-response". Default = fora. |
| **madeira** | **USAR — melhor alvo com atmosfera** | Pegar **uma** nota longa de madeira/marimba (Rubber Bridge Guitar, marimba do Kontakt), Texture + Flux 0 + Grain Size alto, esticar. É a tradução direta do "guitar → pad" (orgânico → digital → orgânico). Preenche 300–1.200 Hz sem sintetizar brilho. |
| **stab** | **NÃO no ataque / SIM na cauda** | Stab precisa de transiente; a técnica remove justamente isso. Usar o material granulado como camada **sustentada por baixo** do stab, com low-pass. |
| **subida** | **USAR** (derivação) | O par reverse → stretch ×2 mantido reverso é matéria-prima de riser lento; o vídeo usa o mesmo gesto para sustain (00:05:23.680), não para riser — marcado como **INFERÊNCIA**, não como fala do vídeo. |
| **atmosfera** | **USAR — alvo principal** | É literalmente o propósito declarado: 00:00:15.809 "can use as ambiences for our songs". Cama contínua, não rítmica → não compete com o groove. |

### Como não engordar o sub nem criar brilho metálico

1. **High-pass 180–300 Hz em toda camada granular** — boa prática medida em estudos de atmosfera. Isso mantém o low-end mono intocado.
2. **Low-pass em ~6 kHz** (ou shelf suave acima de 6 kHz). O artefato que o vídeo elogia mora no topo (00:07:21.900 "audio artifacts in the top end … time stretching distortion"); na faixa de 1,2–4 kHz ele até ajuda, mas acima de ~6 kHz vira o "brilho metálico" a evitar em perfil escuro.
3. **Diferença L/R só acima de ~150–250 Hz** — boa prática geral: gerar diferença estéreo real só acima dessa faixa; abaixo, mono.
4. **Delay com 35% de feedback acumula energia nos médios** — como 300–1.200 Hz é justamente a banda carente do set de referência, algum acúmulo é bem-vindo, mas medir antes de subir o wet.
5. **Reverb a 65% de wet (como no vídeo) não é solista acústico** — aqui a fonte já está transformada, então 65% é defensável. Mas se a madeira precisar soar como madeira, separar: dry na frente, wet em paralelo ≤25% (boa prática para fontes acústicas).
6. **A cópia −5/−8 semitons precisa ser reafinada** para a tonalidade da track; o intervalo do vídeo é para criar movimento, não para dar a tonalidade.

### Onde encaixar no arranjo

Cama de **atmosfera/madeira** entrando **antes do primeiro kick** (para dar chão sem competir) e permanecendo sob o motor, com **buracos reais** a cada 2–8 bars — o método "atmosfera granular 'miragem'" pede uma única fonte, várias regiões granuladas, posição de grão modulada devagar e cortes reais, em vez de empilhar três beds. O vídeo dá a variação barata: 00:08:43.200 "you could always start a little bit earlier on in the sample" — mudar o ponto de entrada muda a textura sem mudar o patch.

---

## Prioridade e esforço

**Prioridade: ALTA.** Ataca diretamente o déficit típico de médios (300–1.200 Hz e 1.200–4.000 Hz medidos no set de referência), entrega a camada de atmosfera que a frente de textura pede, e não exige nenhum plugin novo — é stock do Live 12 inteiro.

**Esforço: BAIXO–MÉDIO.** A receita é determinística e curta (10 passos), mas tem duas parcelas de trabalho real: (a) escolher uma fonte com **uma** nota longa e estável — o passo que o vídeo resolve com um loop de biblioteca; (b) fazer o resample/bounce e a afinação das duas cópias na tonalidade da track. Não há automação de detecção, não há dependência de plugin pago, não há risco de quebrar o Set se for feito em canal separado.

**Risco de execução:** baixo, desde que a camada entre com high-pass e fora do caminho do sub/kick.

**Fontes consultadas na sessão original:**
- Transcrição: legenda automática EN do vídeo (221 cues, lida inteira).
- Descrição: `yt-dlp --skip-download --print "%(description)s"`.
- Números de banda (300–1.200 / 1.200–4.000 Hz), low-end mono e groove deslocado: dados do set de referência fornecidos no levantamento original, **não re-medidos**.

---

## Trechos de prova

1. **00:01:07.729–00:01:18.049** — "texture time stretching mode or the warp mode in Ableton Live what this does is it essentially cuts your audio into small little slices or grains that have been played backed in sequence this gives us really nice glitchy texture audio upon playback of the sample"

2. **00:06:14.389–00:06:22.939** — "and make sure that that's also set to texture mode again and put the grain size all the way up so we have really nice long grains and put the flux all the way down so now it sounds like this"

3. **00:06:50.150–00:07:08.589** — "we're gonna do for the sound is turn this down five semitones so we'll pitch it down a little bit gives us a little bit deeper of a tone I'm gonna copy that over and then we're gonna pitch this down negative eight semitones that just gives us a nice melodic pattern"

*Provas adicionais usadas acima:* 00:03:38.140–00:03:41.020 ("turn the flux all the way down and put the gray [ASR: grain] at 226"); 00:06:30.380 ("so it gives us a nice sustained tone"); 00:06:38.120–00:06:46.310 ("when it was just set to the standard reach mode [ASR: Repitch] I didn't actually play one sustained note it kind of jumped around a little bit"); 00:07:21.900–00:07:29.740 ("audio artifacts in the top end … time stretching distortion"); 00:07:46.639–00:07:58.340 ("set that to the delay time of three … feed back up to something about 35% and the dry/wet down to just over 30"); 00:08:13.720 ("bring that dry/wet up slightly to about 65"); 00:08:43.200–00:08:47.830 ("you could always start a little bit earlier on in the sample"); 00:09:04.870–00:09:12.070 ("it's also available in the simpler instruments device as well").
