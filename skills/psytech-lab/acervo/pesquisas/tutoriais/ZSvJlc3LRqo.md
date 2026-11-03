# How to Clean Up Vocals and Create Custom Textures with Ableton Live Warp Modes

**ID:** ZSvJlc3LRqo · **Canal:** Sonic Academy (Paul Lasky) · **Duração:** 18:29 · **Publicado:** 2026-08-06
**Legenda:** automática em inglês (`en-orig`) do vídeo · **temLegenda:** true
**Escopo desta dissecação:** leitura da legenda automática; **nenhum áudio foi ouvido** no estudo. `yt-dlp --print` confirmou título, canal, duração e data.

> Erros típicos da legenda automática: "P Lask" = P-Lask; "1 100 BPM" = 100 BPM; "&gt;&gt;" = marca de troca de fala; "[music]" = música de fundo. Nenhuma conclusão abaixo depende dessas palavras.
> **Legenda do mapa:** `VERIFICADO (vídeo)` = está na legenda; `INFERÊNCIA` = leitura do estudo para o arsenal/material, não é conteúdo do vídeo.

---

## Técnica ensinada (2-4 frases)

O vídeo usa **só o Warp do Ableton Live** e separa a técnica em limpeza e destruição. Na limpeza, corrige o **Segment BPM** (apaga o último warp marker, seleciona o primeiro e digita o BPM original — 00:02:31.120–00:03:55), transpõe a voz por **pitch** (D→G, −7 semitons — 00:03:52.280) e troca o **Beats** por **Complex Pro**, usando **formant preservation** e **spectral envelope** para preservar vogais e esculpir o timbre (00:04:55.080–00:06:53). Na parte criativa, usa o **Beats** com *preserve* em **1/8**: o sample é fatiado a cada colcheia e as fatias são espaçadas; com o *transient loop* desligado e o *transient envelope* curto, isso vira um **gate rítmico de colcheias** que o vídeo descreve como quase uma textura de synth, não uma voz (00:07:38.840–00:09:08). Depois usa **Re-Pitch** (pitch e velocidade acoplados, como sampler/toca-discos — 00:11:18.480) e **Tones/Texture**, os modos **granulares**, com **grain size** e **flux** (LFO aleatório que randomiza o tamanho dos grãos — 00:13:21.400–00:13:31.910); com estiramento extremo, loop de um trecho do meio, reverse e automação de grain size por clip envelope (seno de 16 compassos), constrói uma textura contínua que ele chama de *"pure weird texture"* (00:15:19.720–00:17:31; a frase em 00:15:57.480–00:15:58.520).

## Ferramenta usada no vídeo (plugin/stock)

- **Ableton Live — Clip View / Warp**; nenhum plugin de terceiros é nomeado ou demonstrado. A técnica acontece no clip de áudio.
- Modos demonstrados: **Beats** (o default dele), **Complex / Complex Pro**, **Re-Pitch**, **Tones**, **Texture**.
- **Preferences → Record/Warp/Launch**: define o warp mode padrão (*"if you go to the record warp launch tab, you can set a default warp mode from here"*, 00:01:26.360–00:01:30.630). Ele deixa **Beats** porque trabalha muito com loops de bateria e preservação de transiente (00:01:30–00:01:42). Na lista de default **não existe Complex Pro**: *"I'm not sure why they don't have complex pro on this list"* (00:01:42.840) — Complex Pro só é escolhido manualmente no clip (00:04:55.080).
- Parâmetros citados: **Segment BPM**, **warp markers**, **Pitch**, **Formants**, **Spectral Envelope** (Complex Pro), **Preserve** (Beats), **Transient Loop**, **Transient Envelope**, **Grain Size**, **Flux** (Texture), **Grain Size** (Tones), **clip envelope** (right-click → insert shape).
- **Send C** com delay (00:14:41.040, sem nome de plugin) — o vídeo usa um retorno já existente.
- **Não aparece**: ANA 2, VELA, SideKick, Kick 3, Bitwig, nenhum sintetizador. Não há dependência de plugin fora de um arsenal Live 12.

## Tradução para um arsenal compatível: Serum 2 (tem GranularOsc nativo), Diva, Vital, Massive X, Surge XT, Kontakt 8 (Rubber Bridge Guitar, LOOP GARDEN, Ethereal Earth, Vintage Organs), Live 12 nativo (Simpler/Sampler/Grain, Operator, Echo, Hybrid Reverb, AutoPan, Shifter)

**A notícia boa:** o vídeo ensina exatamente o motor que o arsenal já tem — **o Warp do Live 12**. Não é preciso plugin, compra nem workaround. A tradução é quase 1:1; o que muda é a **finalidade** (no material de referência, textura/atmosfera, não limpeza de vocal) e as **regras de low-end/groove** do material.

### Live 12 nativo — rota principal (1:1)

| Conceito do vídeo (VERIFICADO) | Equivalente no Live 12 | Observação |
|---|---|---|
| Warp de clip: Beats, Complex Pro, Re-Pitch, Tones, Texture | Os mesmos modos, no clip de áudio | Rota direta; nenhum plugin |
| Segment BPM + warp markers | O mesmo campo e os mesmos marcadores | Correção e "mentira" de BPM (ver abaixo) |
| Formants + Spectral Envelope | Complex Pro do Live 12 | Mesmos dois controles |
| Preserve 1/8 + Transient Loop + Transient Envelope | Beats do Live 12 | Mesmos controles; o vídeo mostra os três comportamentos de loop (ida-e-volta, só frente, tocar e parar) |
| Grain Size + Flux | Texture do Live 12 | Granular de verdade, nativo |
| Grain Size (sem flux) | Tones do Live 12 | Granular com um controle só |
| Clip envelope no grain size | Envelope do clip no Live 12 | Right-click → insert shape; desvincular para alongar (00:16:18.480–00:16:54.680) |
| Delay num send | **Echo** num return, ou um send já existente | O vídeo não nomeia o delay |
| Re-Pitch (pitch sobe ao acelerar) | Re-Pitch do Live; Simpler no modo classic | Mesmo comportamento de sampler |
| Printar a textura e reusar | Freeze & Flatten / Consolidate; recarregar em Simpler/Sampler | `INFERÊNCIA` operacional; não testado |

- **Simpler/Sampler** têm seção de warp com os mesmos modos do clip — `HIPÓTESE de GUI`, não verificada na interface. Se confirmar, é o caminho para aplicar a textura a um **one-shot** sem depender do clip.
- **Grain**: o device stock correspondente no Live é o **Grain Delay**. Ele granulariza em tempo real, mas é um delay, não o algoritmo de time-stretch do Texture — serve para **textura**, não para "limpar" ou esticar mantendo forma.
- **Operator**: só como fonte sintetizada (uma nota/sustained) para depois warpar; o vídeo não usa sintetizador.
- **Hybrid Reverb**: cauda da atmosfera, em paralelo e com low cut no retorno.
- **AutoPan**: movimento lento e **livre** (não tempo-sync) no lugar do flux quando o grain size já está fixo.
- **Shifter**: deslocamento de formante/pitch numa cópia, se a fonte precisar entrar na tônica (C#) sem repitch do arquivo.

### Serum 2 — rota de preset reutilizável (granular)

O **GranularOsc** do Serum 2 é o equivalente ao Tones/Texture, com controles em unidades reais:

| Conceito do vídeo | Campo do gerador | Observação |
|---|---|---|
| Grain Size | `granular_grain_length` (ms, literal) | O vídeo usa "65" (00:14:23.800); no Serum o valor é em ms, então **não copie o 65** — calibre de ouvido |
| Grain grande = mais picotado; pequeno = mais tonal (00:14:06–00:14:29) | `granular_grain_length` + `granular_density` | Grão curto + densidade alta = textura; grão longo + densidade baixa = cama |
| Flux | `granular_random_grain_length` (%) + `granular_random_offset` (%) | O vídeo descreve flux como LFO aleatório no tamanho do grão (00:13:26.320) |
| Tones (sem flux) | os mesmos campos com random = 0 | — |
| Loop de um trecho do meio | `granular_loop` ligado (no SampleOsc: `sample_loop`) | No granular, `granular_loop` mantém a nuvem |
| Reverse | `granular_reverse` (marcado `uncertain` no schema) ou reverter o WAV na fonte | Preferir reverter o WAV: comportamento conhecido |
| Re-Pitch | **SampleOsc** (`sample_playback_source`) | Pitch e duração acoplados, como o Re-Pitch do vídeo; referência C5 |
| Automação do grain size | **não há rota de modulação para parâmetros granulares** | A lista de destinos de modulação do gerador de presets (`MOD_DEST_TARGETS`) não cobre grain/density — cobre oscilador, filtros, envelopes, LFO rate, macros, noise, arp e global. Automação de grain size no Serum tem de ser feita na GUI ou printando variações |

- `granular_random_pitch` **= 0** para material na tônica; a variação vem de posição/tamanho, não de afinação. O uso recomendado permite no máximo ±2 st, e só para textura.
- O gerador escreve `granular_grain_length` em **milissegundos reais** — o valor "65" do Live não é transferível.

### Kontakt 8 — fonte, não motor

- **Rubber Bridge Guitar**: pluck orgânico com corpo de médio — boa fonte para Texture/Tones.
- **LOOP GARDEN**: loops e frases rítmicas — material para o Beats 1/8 (gate) ou para Re-Pitch.
- **Ethereal Earth**: pads/atmosfera — fonte pronta para estirar e granularizar.
- **Vintage Organs**: sustain harmônico estável — fonte para drone/atmosfera.
- O vídeo **não usa Kontakt**; a alocação é `INFERÊNCIA` pelo papel de cada biblioteca. O caminho é tocar, printar uma nota/compasso e aplicar o warp.

### Diva, Vital, Massive X, Surge XT

Não são o caminho: o vídeo não os usa e o papel de textura já está coberto pelo Live/Serum. No máximo, são **fonte sintetizada** para printar e depois warpar. Não se afirma que algum deles tenha motor granular próprio — **não verificado**.

### Sobre ANA 2, VELA, SideKick, Kick 3, Bitwig

Nenhum aparece no vídeo; não há dependência a contornar. **`traduzivel = true`**.

## Aplicação concreta em um motor minimal de 2 minutos: por função (kick, sub, baixo/rolling, hats/shaker, percussão de resposta, madeira, stab, subida, atmosfera)

Contexto medido do set de referência (**diagnóstico prévio, não re-medido**): **300–1.200 Hz está −4,83 dB** e **1.200–4.000 Hz −5,76 dB** contra a média de 6 referências externas; **low-end é mono**; o groove usa **subdivisões deslocadas .27/.77** e deve ser preservado. O motor de referência vai até **2:00 = 64 compassos**. Preservar os **vazios de kick em 0:44–0:45 e 0:59,5–1:00**; fonte nova, se necessária, é de biblioteca própria, não recorte da referência externa.

**Regra-mãe:** o warp/granular do vídeo produz **sustain com movimento**, não ataque. Ele entra onde o motor precisa de **corpo médio e cauda** — nunca no transiente do kick, nunca abaixo do HP, nunca numa camada que carrega o .27/.77.

| Função | Usar? | Como (ponto de partida — `HIPÓTESE`) | Por que / cuidado |
|---|---|---|---|
| **kick** | Não | — | Warp/granular borra o transiente e pode criar pré-eco; o kick carrega a pressão e o mono |
| **sub** | Não, nunca | — | Qualquer estiramento modula a fundamental; nada granular abaixo de ~120–180 Hz |
| **baixo/rolling** | Não no corpo | No máximo a **cauda** de uma nota, em paralelo, HP ≥300 Hz | O .27/.77 vive da articulação seca; grão aleatório borra a subdivisão deslocada |
| **hats/shaker** | Evitar o gate do vídeo | Se usar: camada **separada** (não o shaker do groove), fonte de ruído/sala, Texture, grain ~65, flux baixo, HP ≥2 kHz, nível baixo | O *preserve* 1/8 do vídeo é **grade reta**; aplicado no shaker, re-quantiza e mata o .27/.77. Risco de ring metálico em grão curto |
| **percussão de resposta** | Sim, como **cauda/textura** | Copiar uma madeira/voz curta, Texture com grain ~65 e flux baixo, HP ≥300 Hz, disparar **no .27/.77** mantendo o ataque seco original na frente | O evento de resposta continua seco; a textura só abre o timbre depois do transiente. Não usar tempo-sync |
| **madeira** | **Sim — fonte principal** | (a) Texture/Tones numa nota de madeira para nuvem de médios; (b) Re-Pitch para caráter de sampler, **conferindo a afinação** | Re-Pitch acelera e **sobe o pitch** (00:11:18.480); se a madeira já está em C#, acelerar tira do C#. Para a camada principal, prefira Texture com pitch estável |
| **stab** | Só a **cauda** | Copiar o stab, Complex Pro ou Texture, HP ≥300 Hz; o stab seco continua na frente | Granular no ataque apaga a definição; a cauda pode preencher 300–1.200 Hz |
| **subida** | **Sim** | Tones, estiramento extremo (×2), grain pequeno, loop de um trecho do meio, reverse, clip envelope de **16 compassos** no grain size | O vídeo faz exatamente isso (00:15:19.720–00:17:31). Evitar o salto agudo no compasso 32, já rejeitado no diagnóstico; subida lenta, filtrada |
| **atmosfera** | **Sim — casa principal** | Texture/Tones em voz/madeira/sala da biblioteca de samples; grain ~65, flux baixo; clip envelope de 16 compassos (seno) no grain size; HP 120–300 Hz; L/R real só acima de ~150–250 Hz; delay no send | É a camada que preenche **300–1.200 Hz** (e parte de 1.200–4.000) sem tocar no low-end mono. Deve **respirar**; não preencher os vazios de kick de 0:44–0:45 e 0:59,5–1:00 |
| **voz (fora do motor)** | Opcional | Complex Pro + **formants 100%** + spectral envelope **abaixo** do default; pitch/correção de Segment BPM como no vídeo | Se uma voz falada entrar, é a rota de limpeza do vídeo (00:04:55.080–00:06:53). Não é requisito do motor instrumental |

### Receita mínima (10–20 min por camada)

1. Escolher um sample de **1–4 s com sustain** na biblioteca de samples — voz, madeira, sala, guitarra. Fonte própria de biblioteca, não recorte da referência externa.
2. Ligar o **Warp** e escolher **Texture** (com flux) ou **Tones** (sem flux).
3. **Estirar**: apertar o **×2** do Segment BPM duas ou três vezes, ou "mentir" o Segment BPM para 2–4× o original — é o mesmo gesto do vídeo (00:04:06.600–00:04:30; *"it's going to slow this audio file way down"*, 00:04:28.680). O vídeo bate no limite do ×2 em 00:15:27.400 — o estiramento extremo tem teto.
4. **Grain size ~65** e **flux baixo** como ponto de partida do vídeo (00:14:23.800 / 00:14:31.640). Grão grande = mais picotado; pequeno = mais tonal (00:14:06–00:14:29).
5. **HP 120–300 Hz** na camada; manter **mono abaixo de ~150–250 Hz**; L/R real só acima disso.
6. **Clip envelope no grain size**: right-click → insert shape; desvincular e esticar para **16 compassos**; o valor é percentual (00:16:18.480–00:17:10.959).
7. **A/B**: mute a camada. Se o sub "encher" ou o topo ficar metálico, o problema é fonte/grão/HP — não corrigir com EQ depois.

### Regras anti-engorda-sub e anti-brilho-metálico

- **Nada de granular abaixo de ~120–180 Hz.** HP em toda camada; não mandar para o bus de sub nem para o lado mono do grave.
- **Pitch estável** no Serum (`granular_random_pitch = 0`); no Live, não usar Re-Pitch na camada principal em C#. A variação vem de posição/tamanho.
- **Brilho metálico ≠ agudos.** O risco vem de **inarmonicidade**: grão curtíssimo + pitch/offset aleatório. Para atmosfera, prefira grão médio/longo e flux baixo; grão curto só para FX/subida. `INFERÊNCIA` deste estudo, não afirmação do vídeo.
- **Não usar o gate 1/8 em quem carrega o groove.** A grade do vídeo é reta; o .27/.77 é deslocado. Textura rítmica só em camada independente.
- **O spectral envelope pode brilhar:** o vídeo mostra que subir o controle traz mais agudos (00:05:59.720) e *"sounds a little bit weird"* (00:06:03.960); ele reduz o envelope no final (00:06:34.200). Para este caso, deixar neutro ou abaixo.
- **Fonte tem de ter médio.** EQ não cria o que não existe — a mesma lição do diagnóstico do motor de referência (kick seno, sub seno e percussão FM filtrada não têm 2–6 kHz). Escolher voz/madeira/guitarra, não uma senoide.
- **Vazios de kick preservados:** a atmosfera não deve ser um colchão contínuo por cima de 0:44–0:45 e 0:59,5–1:00; automatizar o gain para abrir nesses pontos.

## Prioridade e esforço

- **Prioridade: alta.** É uma das técnicas da pesquisa que atacam diretamente o **vale de 300–1.200 Hz (−4,83 dB)** com material já disponível — a biblioteca de samples — e faz isso **nativo no Live 12**, sem compra. Não é P0 porque não resolve o núcleo do motor (kick/sub/baixo/rolling); é camada de **textura/atmosfera**.
- **Esforço: baixo a médio.** Baixo na rota Live (mesmos modos, mesma GUI); **médio** na curadoria da fonte e na calibração grain/flux para preencher o médio sem ring metálico. A rota Serum é média/alta para automação, porque o gerador **não modula parâmetros granulares** — só GUI ou renders.

## Trechos de prova: 3 citações literais da legenda com timestamp

> *"I'm going to tell it to preserve Let's try eighth notes. So, it's ignoring the transient markers, and then what it's doing is just going through the sample and every eighth note"* — **00:07:38.840–00:07:45.240**

> *"These are both granular time stretch modes"* — no time stretch granular o áudio é cortado em grãos/chunks minúsculos do sample — **00:12:58.960–00:13:08.040**

> *"Flux is kind of like a random LFO that's randomizing the grain slices or the grain sizes, I should say."* — **00:13:26.320–00:13:31.120**

### Provas adicionais citadas no corpo

- *"warping vocals like this, complex pro is usually a good one"* — 00:04:55.080; *"because it gives us this formants parameter here, which allows us to preserve formants"* — 00:04:58.440
- *"I'm not sure why they don't have complex pro on this list"* — 00:01:42.840
- *"the beats mode, as I mentioned earlier, is designed for preserving transients"* — 00:07:00.240
- *"kind of a cool rhythmic effect, just a nice even eighth note gating effect"* — 00:08:20.600
- *"Now, it's almost more like just a synthy texture than it is a vocal"* — 00:08:58.360
- *"re-pitch mode, pitch and playback speed are interconnected like they would be on a sampler"* — 00:11:18.480
- *"grain size is how large are the slices, how large or small are they, I should say"* — 00:13:21.400
- *"Let's go back to 65"* — 00:14:23.800; *"Let's pull it down a bit"* (flux) — 00:14:31.640
- *"It just gives us a grain size parameter"* (Tones vs Texture) — 00:15:19.720
- *"we'll just loop a portion in the middle of this"* — 00:15:38.160; *"And I might even reverse this"* — 00:15:47.200
- *"we could also try unlinking the envelope"* — 00:16:31.839; *"now we have a 16-bar long rise-fall"* — 00:16:54.680
- *"the values we see here are a percentage. You see it says 100%"* — 00:17:06.720
