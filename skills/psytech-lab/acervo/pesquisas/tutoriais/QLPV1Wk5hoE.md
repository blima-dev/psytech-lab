# Designing Custom Background Atmos for Progressive and Minimal Tracks

**Canal:** Sonic Academy · **ID:** `QLPV1Wk5hoE` · **Duração:** 7:34 (454 s)
**Fonte:** legenda automática em inglês do vídeo (YouTube), transcrita com timestamps. **`temLegenda = true`.** Todos os timestamps abaixo vêm desse arquivo.
**Legenda de evidência:** tudo entre aspas com timestamp é **literal da legenda**; valores de banda, nível, tempo e parâmetros sem citação são **proposta deste estudo**, não conteúdo do vídeo. **O áudio do vídeo não foi ouvido** — a análise é só da legenda.

## Técnica ensinada (2-4 frases)

O vídeo ensina a fabricar uma cama atmosférica ("granular pad") a partir de um trecho curto de uma amostra orgânica — voz, guitarra ou piano — em vez de partir de um preset de pad: o trecho entra no sampler, é isolado, desacelerado e trocado para o modo granular ("textures"), que fatia a amostra em grãos. Grain size e motion definem a textura, e o loop é posto a tocar para frente e para trás. Sobre isso ele empilha até oito vozes/uníssonos com pontos de entrada diferentes, espalhamento estéreo e velocidade/motion levemente diferentes por voz, e fecha com delay, difusão e reverb para borrar as emendas entre os grãos. Por fim, usa filtro automatizado como ferramenta de arranjo — a cama sobe e desce em pontos diferentes da faixa.

## Ferramenta usada no vídeo (plugin/stock)

**Stock do Bitwig Studio: o Sampler nativo, no modo "Textures" (granular).** Não é plugin de terceiro — o próprio vídeo diz que a técnica não exige plugin específico:

> "They don't need to have a very specific plugins for this. Um most DAWs" — 00:00:27.9–00:00:31.9

Ele cita alternativas de DAW ("Cubase, for example, has Padshop." 00:00:32.4–00:00:33.4; "Bitwig actually has its own granular features as well." 00:00:35.0–00:00:36.7) e reconhece que esses recursos não são óbvios ("Uh they're not super obvious." 00:00:37.2–00:00:38.9). A demonstração é no Sampler do Bitwig:

> "in Bitwig you have this other mode that you can change the sampler to." — 00:01:09.9–00:01:14.1
> "but if we go on to textures, this is more close to what a granular sampler would be like." — 00:01:28.2–00:01:32.6

O modo "cycles" é descrito como "works like a wave table almost" (00:01:16.7–00:01:22.7) e **não** é o usado na demonstração.

**Controles usados no vídeo (todos no Sampler):**

| Controle | Trecho literal | Timestamp |
|---|---|---|
| isolar um trecho da amostra | "we're going to single out a section here." | 00:00:57.5–00:00:58.3 |
| desacelerar | "Let's slow this right down." | 00:01:39.4–00:01:40.2 |
| tamanho do grão | "Now, we can change the grain size." | 00:01:44.9–00:01:45.6 |
| motion | "We can add some motion in there, too." | 00:01:53.4–00:01:54.6 |
| loop ping-pong | "let's set this also to just loop backwards and forwards." | 00:02:12.5–00:02:14.4 |
| uníssono / voice stacking | "All we need to do is really turn on the unison or the voice stacking for this sampler." | 00:02:37.9–00:02:44.6 |
| 8 vozes | "we can actually go right up to eight. Let's go with eight voices" | 00:02:55.1–00:02:58.5 |
| volume ao empilhar | "you do want to just watch the volume… it's stacking them on top of one another." | 00:02:59.4–00:03:03.9 |
| play position | "what we can do is play around with things like the play position." | 00:03:09.0–00:03:12.8 |
| start point por voz | "We're going to set up a different start point for each voice." | 00:03:28.2–00:03:32.0 |
| stack spread L/R | "we can also stack spread the left and right signals here as well." | 00:03:45.2–00:03:48.7 |
| espalhar o campo estéreo | "assign this one to the left and right to kind of spread out the stereo field" | 00:03:59.2–00:04:05.2 |
| velocidade/motion por voz | "assign slightly different values to the speed, perhaps, and the motion." | 00:04:10.9–00:04:15.0 |
| delay | "let's go with some delay on this to really kind of blur out the lines between the two or between the grains" | 00:04:40.6–00:04:50.2 |
| difusão | "We can add in some diffusion on these, too." | 00:04:57.6–00:05:04.6 |
| reverb | "And we'll go some reverb, too, just to kind of drown everything out." | 00:05:08.2–00:05:11.1 |
| filtro como arranjo | "you can actually use this as an arrangement tool… add in a bit of filtering" + "raised and lowered in various different points of the track." | 00:05:32.6–00:05:43.9 |

**Não usa** ANA 2, VELA, SideKick nem Kick 3. A cadeia demonstrada é 100% stock do Bitwig (Sampler + efeitos nativos).

## Tradução para um arsenal compatível: Serum 2 (tem GranularOsc nativo), Diva, Vital, Massive X, Surge XT, Kontakt 8 (Rubber Bridge Guitar, LOOP GARDEN, Ethereal Earth, Vintage Organs), Live 12 nativo (Simpler/Sampler/Grain, Operator, Echo, Hybrid Reverb, AutoPan, Shifter). Sem ANA 2, VELA, SideKick, Kick 3, Bitwig — se o vídeo depende deles, explique o conceito equivalente.

O gesto central — sample orgânico → grãos → empilhamento de vozes → efeitos — **sobrevive sem o Bitwig**. A rota principal é o **Serum 2 GranularOsc**; a rota secundária é o **Live 12**. O Bitwig entra apenas como demonstração: o conceito equivalente é "um sampler com motor granular, posição de leitura aleatorizada por grão, vozes empilhadas e loop longo". Um arsenal com Serum 2 (wavetable, sample, multisample, granular, spectral) não tem lacuna de motor de síntese que justifique comprar outro sintetizador para esta função.

### Mapa Bitwig → arsenal compatível

| Gesto no vídeo (Sampler do Bitwig) | Equivalente no arsenal | Fidelidade |
|---|---|---|
| Modo "textures" (granular) | Serum 2 `GranularOsc`: campo `granular_source` recebe o caminho de um `.wav` | direta |
| "slow this right down" + grain size | `granular_grain_length` (ms) + `granular_density` | direta em função; **o vídeo não dá valores** |
| "motion" | `granular_random_offset`, `granular_random_grain_length`, `granular_random_window_amount` + automação de filtro no Live | parcial: o gerador de presets não expõe SCAN/varredura contínua da posição de leitura |
| 8 vozes/uníssono | `unison` do oscilador (o schema aceita até 16) + `granular_random_pan` | direta no número de vozes; o empilhamento é por voz do sintetizador, não por "voz do sampler" |
| start point diferente por voz | `granular_random_offset` (% de offset de início por grão) | parcial: randomização por grão, não por voz |
| stack spread L/R | `granular_random_pan` + `voice_unison.pan` (pan por voz, −100…+100) | direta |
| speed/motion diferente por voz | `granular_random_grain_length` + detune/uníssono + automação de grain length | parcial: não existe "play speed por voz" no motor granular |
| loop "backwards and forwards" | **não existe no GranularOsc**: `granular_loop` é loop *dentro de cada grão*, não ping-pong do sample | ausente no motor — usar Live Sampler com loop ping-pong, ou gravar o WAV já em ping-pong/seamless |
| delay para borrar os grãos | Live Echo, ou `FXDelay` no Serum (com `kParamBeatSync: false`, senão `kParamTimeL/R` **não** significam segundos — gotcha documentado no schema do gerador) | direta em função |
| difusão + reverb | Hybrid Reverb em retorno 100% wet, filtrado | direta em função |
| filtro automatizado como arranjo | EQ Eight / Auto Filter automatizados por seção no Live | direta |

### Receita-base no Serum 2 (proposta deste estudo; o vídeo não dá números)

Fonte: schema do gerador de presets do Serum 2 (campos `granular_*`, `unison`, `filters`, `voice_unison`).

1. `oscillators[0].granular_source` = caminho de um `.wav` (só `.wav` é aceito). O engine **copia** o arquivo para a Samples library do Serum — se o preset for compartilhado, o WAV tem de ir junto, senão o slot abre vazio.
2. `granular_grain_length`: **120–300 ms** para cama lisa; **30–120 ms** só se quiser textura mais granular/metálica (um preset Factory real usa 124 ms para textura "smooth/rich").
3. `granular_density`: baixa/média na escala 0–30 do próprio Serum (mais alto = nuvem mais contínua; mais baixo = grãos individuais audíveis). Começar em ~6–12 e ajustar de ouvido.
4. `granular_random_offset`: 40–80% → é o equivalente funcional ao "different start point for each voice" (por grão).
5. `granular_random_pitch`: **≤ 2 st**. Recomendação de uso do motor granular: acima disso a afinação flutua e borra o centro tonal do material (no set de referência, C#).
6. `granular_random_pan`: 40–70%; `granular_random_grain_length`: 30–60%; `granular_random_window_amount`: 30–60%.
7. `granular_loop`: ligado; `granular_max_grains`: 16–24.
8. `unison`: 8 (o número que o vídeo usa), `detune` baixo, e `voice_unison.pan` por voz para o stack spread L/R.
9. Filtro: `filters[0]` = `highpass_24` mirando **250–300 Hz** (atenção: no schema do gerador o campo `cutoff` é normalizado 0..1, não Hz — converta antes de escrever). Se quiser o teto de agudos dentro do próprio Serum, `filters[1]` = `lowpass_24` mirando **5–6 kHz** e `filters[0].output_routing = "series"` (não colocar os dois em `series`, que cria ciclo e o engine recusa).
10. Efeitos: delay curto não sincronizado (Echo ou `FXDelay`) para borrar as emendas; Hybrid Reverb em retorno filtrado.

**Limitações declaradas desta tradução:**
- O modo "loop backwards and forwards" do Bitwig não tem equivalente no `GranularOsc`; `granular_loop` é outra coisa (loop dentro do grão). Para ping-pong real: Live Sampler, ou WAV já editado.
- O gerador de presets não expõe a forma da janela do grão (Tukey/ExpDec no Serum). Se o preset for editado à mão no Serum, janela suave reduz zumbido metálico.
- O vídeo **não fornece nenhum valor numérico** de grain size, densidade, HP, delay ou reverb. Todos os números acima são proposta, não reprodução.

**Live 12:** Simpler/Sampler resolvem o loop ping-pong e o start point que faltam ao GranularOsc. O **Granulator III** (Max for Live) é citado em material de referência como a rota mais fiel a essa função granular para pads/texturas. **Não verificado** se o Granulator III está instalado na máquina de destino. Se estiver, é a rota mais fiel ao Bitwig; se não, Serum 2 + Sampler cobre.

**Diva, Vital, Massive X, Surge XT:** não são o motor do gesto. Podem fazer a cama sustentada, mas a granularização do vídeo é sampling, e o Serum 2 já cobre essa função — não há motivo para trazê-los para esta tarefa.

**Kontakt 8:** entra como **fonte**, não como motor granular. O vídeo diz que guitarra e piano são bons materiais: *"Guitars actually work pretty well sometimes and pianos and things like that."* (00:06:51.2–00:06:55.0). O **Rubber Bridge Guitar** é a fonte orgânica mais direta para esse gesto. **LOOP GARDEN / Ethereal Earth** servem de referência de textura, mas usá-los como pad pronto pula a técnica do vídeo. Vintage Organs não é citado pelo vídeo; não é necessário.

## Aplicação concreta em um motor minimal de 2 minutos: por função (kick, sub, baixo/rolling, hats/shaker, percussão de resposta, madeira, stab, subida, atmosfera)

**Contexto medido do set de referência:** 300–1.200 Hz está **−4,83 dB** e 1.200–4.000 Hz **−5,76 dB** contra a média de 6 referências externas; o low-end é **mono**; o groove usa subdivisões deslocadas **.27/.77** e deve ser preservado. Conclusão: a cama granular é um **preenchedor de médios**, não uma camada de baixo — e o vídeo reforça a função: *"having them there really does fill a gap in the mix at the end of the day."* (00:07:03.9–00:07:08.2). **Os valores de banda, nível e automação abaixo são proposta deste estudo; o vídeo não fornece nenhum número.**

| Função | O que fazer | Banda / automação | Freio |
|---|---|---|---|
| **kick** | Não processar o kick. A cama sobe **1–2 dB nas ausências do kick** e desce quando ele volta — é o uso que o vídeo chama de "arrangement tool" ("raised and lowered in various different points of the track", 00:05:39.8–00:05:43.9). | Corpo em 1,2–4 kHz. | Sem transiente e **sem sidechain por golpe**: um duck por kick criaria pulso de 1/4 e competiria com o groove .27/.77. A automação é por seção. |
| **sub** | Nada. High-pass **250–300 Hz, 24 dB/oct, depois do granular**. Conferir que 20–120 Hz ficam vazios. O low-end mono permanece intacto. | Nenhuma energia abaixo de 250 Hz. | Grãos podem gerar lixo de baixa frequência; o HP é obrigatório — e o **retorno de reverb também leva HP**. |
| **baixo/rolling** | Corpo da cama em **1,2–4 kHz** (onde o déficit é maior). Em 300–800 Hz, usar ducking/dynamic EQ keyed no baixo, só onde mascarar. | 1,2–4 kHz primário; 300–800 Hz secundário e ducked. | Não sincronizar LFO nem delay à grade **.27/.77**; o rolling continua sendo a articulação rítmica. |
| **hats/shaker** | Teto em **5–6 kHz**, grãos longos, random pitch ≤2 st. | 1,2–5 kHz. | Evita **brilho metálico** e deixa o topo dos hats limpo. Nada de grãos curtos + densidade alta nessa faixa. |
| **percussão de resposta** | Ataque lento, loop longo, **sem retrigger**. Movimento em **2–8 compassos**. O vídeo sustenta a ideia: *"extend this to be nine so it's not constantly re-triggering the whole time."* (00:05:53.4–00:06:01.1) | 1,2–4 kHz. | A resposta percussiva é o evento; a cama é o fundo. Nada de LFO em 1/16 ou 1/8. |
| **madeira** | Granularizar uma **cópia** de madeira/guitarra/piano (ex.: Rubber Bridge Guitar). A madeira original continua seca. | 300 Hz–5 kHz na cópia. | Regra do material de referência: **dry sagrado** em solista acústico — nunca 100% wet no original; wet ≤25% ou paralelo. |
| **stab** | Não aplicar. Stab seco. | — | A cama não deve competir com o ataque do stab. |
| **subida** | Usar como riser: automação de abertura de filtro + densidade/random subindo ao longo de 8–16 compassos; HP acompanhando. | Começa 300 Hz–2 kHz, abre até 6 kHz. | Não deixar a subida invadir o sub; teto de 6 kHz evita hiss metálico. |
| **atmosfera** | **Uma** cama, **uma** fonte, estéreo decorrelacionado acima de 250 Hz, nível baixo, com **silêncios** — não automação constante. | 1,2–4 kHz primário; 300–1.200 Hz secundário. | Uma cama, não três: um diagnóstico do material de referência conclui que o problema é densidade, não falta de conteúdo. |

### Freios para não engordar o sub nem criar brilho metálico

- **Sub:** HP 250–300 Hz 24 dB/oct **na saída do granular** (não antes: os grãos recriam energia grave). Medir 20–120 Hz e provar que a cama não muda o low-end mono.
- **Metálico:** grãos **longos** (≥100 ms), densidade moderada, **sem** `warp_mode` `fold` / `hard_clip` / `quantize`, low-pass em 5–6 kHz, Q baixo entre 1–4 kHz, reverb/delay com retorno filtrado.
- **Afinação:** `random_pitch` ≤2 st para não borrar o centro tonal (C# no set de referência).
- **Groove:** nenhum LFO/retrigger em 1/16 ou 1/8; movimento em 2–8 compassos.
- **Estéreo:** L/R real só acima de ~250 Hz; abaixo disso, mono.
- **Densidade:** a cama entra como informação rara e deliberada, com buracos; não como colchão permanente.

### Como provar (A/B a executar)

1. Mute A/B em **0:00–1:00** (bars 1–32) e **1:00–2:00** (bars 33–64) do arranjo de referência.
2. Medir 20–120 Hz com a cama ligada e desligada: **deve ficar igual**.
3. Medir 300–1.200 Hz e 1.200–4.000 Hz: devem subir em direção à média das 6 referências.
4. Medir 5–10 kHz: não pode saltar (é o teste do brilho metálico).
5. Conferir correlação L/R: acima de 250 Hz pode cair (é o side desejado); abaixo de 120 Hz não pode haver conteúdo.

## Prioridade e esforço

| Dimensão | Valor | Justificativa |
|---|---|---|
| **Prioridade** | **alta** | Ataca exatamente o déficit medido de 300–4.000 Hz; o vídeo é curto e direto ao alvo (atmos para minimal tracks). |
| **Esforço** | **baixo** | Uma instância de Serum 2 + um WAV; nenhum plugin novo, nenhuma compra. O vídeo é um tech tip de 7:34 com uma cadeia curta. O acabamento (automação por seção, checagem mono/estéreo, escolha da fonte) é **médio**, mas não bloqueia a primeira versão. |

## Trechos de prova: 3 citações literais da legenda com timestamp

1. **"one of the first things I always end up doing for the tracks to kind of get some sort of atmospheric components into it."** — 00:00:08.0–00:00:12.4
   *Prova de que a cama atmosférica é tratada como componente estrutural da faixa, não enfeite.*

2. **"So, I'm just going to grab a sample, something like a vocal often works really well. Anything organic often works pretty well."** — 00:00:46.9–00:00:52.2
   *Prova da fonte: sample orgânico (voz, e depois guitarra/piano) é o material da cama.*

3. **"but if we go on to textures, this is more close to what a granular sampler would be like."** — 00:01:28.2–00:01:32.6
   *Prova do motor: o modo usado é o granular ("textures"), não o "cycles" (wavetable).*

## Fontes e limites

**Legenda (fonte primária):** legenda automática EN do vídeo `QLPV1Wk5hoE`, baixada do YouTube (`yt-dlp --skip-download --write-auto-subs --sub-langs en --convert-subs vtt`) e lida na íntegra; as citações foram conferidas contra ela.

**O que NÃO foi feito / não verificado:**
- Nenhum áudio foi ouvido, nenhum preset foi criado ou renderizado; nenhuma verificação de runtime foi executada.
- Não verificado se o Granulator III está instalado na máquina de destino.
- O vídeo não dá valores numéricos; a receita é proposta.
- A legenda automática tem ruídos: em 00:03:53.7 aparece "add in a different stack spread jerkily" — não se interpreta "jerkily" e não se afirma o que significa. Em 00:03:25.1 "naught to plus one" — leitura como a forma falada de "nought to plus one" (0 a +1), mas a unidade exata não é dita.
- O canal não nomeia o apresentador na legenda; nenhum nome foi inventado.
