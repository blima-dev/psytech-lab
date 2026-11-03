# Tech Tip - Granular Drone

**Vídeo:** `vREN7ACIcFc` · **Canal:** Sonic Academy (Tech Tips Volume 27) · **Apresentador:** Bluffmunkey · **Duração:** 8:53 (533 s)
**Legenda:** automática em inglês, lida integralmente. **Tem legenda.**
**Descrição oficial (lida):** "In this Tech Tip Bluffmunkey uses Sound Guru's 'The Mangle' to transform a guitar sample into a pad sound."

---

## Técnica ensinada (2-4 frases)

O vídeo pega um sample curto de guitarra strumming da biblioteca padrão do Ableton Live e o transforma em pad/drone tonal dentro do granular **The Mangle**, desligando o canal original do sample. A regra central é **não mexer no pitch**: ele fica travado por nota, com key mapping de faixa inteira, para o drone poder ser usado melodicamente em vez de virar textura caótica. O corpo vem de reverse em ~50/50, grain attack/release ajustados até ficarem "nice and smooth" (o vídeo não diz a direção nem o valor), um pequeno tail no release da voz, start position aleatório por nota e LFOs de amount pequeno no rate, no pan e no filtro low-pass interno. Fecha com chorus sutil, EQ cortando graves e um reverb grande (preset "Large Space Chorus" do Ableton Reverb) também com corte de graves.

## Ferramentas usadas no vídeo (plugin/stock)

- **The Mangle** (Sound Guru) — granular third-party, citado como ~£20: *"the mangle is is only about 20 pounds"* (00:08:15.470). Nome confirmado na descrição oficial do vídeo.
- **Fonte:** *"a guitar strumming sample in the standard Ableton Live library"* (00:00:16.980). O canal original é desligado depois: *"then we don't need this Chung anymore so we can switch off"* (00:00:39.250 — "Chung" é erro da legenda automática, provavelmente "channel").
- **Filtro:** low-pass embutido no próprio Mangle: *"there is a filter built into mango so if we just keep on low-pass"* (00:04:20.669 — "mango" = Mangle na legenda automática).
- **Efeitos Ableton (stock):** chorus (00:05:29.650), EQ (00:06:27.059), Ableton Reverb com preset *"large space chorus"* em high quality mode (00:06:49.269 e 00:07:01.419).

### O que o vídeo NÃO especifica (não inventar números)

Grain size, densidade/overlap, taxa dos LFOs, valores de EQ, decay do reverb e o quanto de reverse além de "probably about 50/50" **não são ditos**. O autor ajusta "de ouvido" (*"if we have it around about there it makes it nice and smooth"*, 00:03:02.209). Qualquer valor em Hz/ms/° abaixo marcado como **proposta** é tradução, não conteúdo do vídeo.

## Como reproduzir sem o plugin

Não ter o Mangle **não bloqueia** o conceito: o vídeo usa apenas operações que existem em qualquer motor granular (sample, posição, tamanho/densidade de grão, reverse, random start, LFOs, filtro). O papel é coberto por **Serum 2 (GranularOsc)** ou **Live 12 Suite (Granulator III, Max for Live)**.

### Conceito por conceito

| Conceito no vídeo | Como realizar | Observação |
|---|---|---|
| Sample de guitarra no lugar do oscilador | GranularOsc do Serum 2 com fonte WAV (slot de oscilador granular); ou Granulator III (Max for Live) | usar one-shot curto; estrumado/plucked. Biblioteca de guitarra/organics serve como fonte antes de renderizar |
| Reverse ~50/50 | Camada reversa (no Serum 2, `granular_reverse` é binário: para 50/50, duas camadas iguais — uma normal, uma reversa — ou aceitar 100% e compensar no random offset) | **não é mix** no motor |
| Start position aleatório por nota | Random offset / spray (posição aleatória por nota) | é o mapeamento mais direto do gesto do vídeo |
| Rate / sobreposição de grãos | Densidade + máximo de grãos | o vídeo só diz "modulate the rate just a little bit" |
| Tamanho do grão | Grain length (ms) | grão longo = corpo; grão curto = brilho metálico |
| Grain attack/release "nice and smooth" | Window shape / envelhecer com grão longo + filtro | o motor de presets pode não expor a janela; ajustar na GUI do synth |
| Pan LFO lento | AutoPan no Live (ou LFO → pan da camada) | distinto do *random pan* por grão, que é spread aleatório |
| Pitch travado (regra do vídeo) | Random pitch = 0 + sem rota de pitch | é o principal antídoto contra brilho metálico |
| Loop/sustentação | Loop de grãos ligado | manter ligado para o drone não morrer |

**Nota honesta:** o GranularOsc real do Serum tem ~20 parâmetros (window shape, density/length sincronizados a BPM, unison, scan/posição) que a receita acima não cobre em nomes exatos; nada disso impede a receita — só exige ajuste manual na GUI se você quiser o grão "smooth" exato do vídeo.

### Live 12 nativo (o mais próximo do fluxo do vídeo)

- **Granulator III** (Max for Live, incluído no Live 12 Suite) é o equivalente direto do Mangle. O próprio vídeo recomenda essa rota sem nomear o device: *"if you've got max for live there's a good granular program"* (00:08:08.480). Use position/spray para o start aleatório, size/density para o corpo, pitch travado, e o filtro interno.
- **AutoPan** → o *"some LFO on the panning"* (00:02:38.450).
- **Auto Filter** → low-pass com LFO, substituindo o filtro modulado do Mangle (00:04:20.669).
- **Chorus / Chorus-Ensemble** → o chorus sutil do vídeo (00:05:29.650).
- **EQ Eight** → o corte de graves (00:06:27.059).
- **Hybrid Reverb** → no lugar do Ableton Reverb "large space chorus", com decay longo e low cut no retorno.
- **Simpler/Sampler** não têm modo granular; no máximo seguram o sample reto. A granulação fica no Granulator III.

Os nomes de parâmetro do Granulator III acima vêm de conhecimento geral e **não foram abertos/verificados** — conferir na GUI antes de automatizar.

### Outros synths

- **Diva, Vital, Massive X, Surge XT** não são o caminho granular aqui (o vídeo não usa nenhum). Uso possível: pad tonal de reforço **abaixo** do drone, ou dobrar a fundamental na tônica do projeto. Não tente reproduzir o Mangle neles.
- **Nenhum** dos plugins citados no cenário comum (ANA 2, VELA, SideKick, Kick 3, Bitwig) aparece neste vídeo. Não há dependência a contornar.

## Notas de aplicação

**Onde:** função **atmosfera**, como cama contínua sob o motor da faixa. Não é elemento rítmico e não substitui kick, sub nem baixo.

**Contexto do projeto de referência:** 300–1.200 Hz está −4,83 dB e 1.200–4.000 Hz −5,76 dB contra a média de 6 referências; low-end em mono; groove com subdivisões deslocadas .27/.77 a preservar.

> **Status da evidência:** a medição acima é contexto do projeto de referência (fora deste vídeo). A alocação do drone por faixa e todos os valores de HP, corte de filtro e nível são **inferência/proposta de design** — o vídeo não mede nada.

### Receita proposta (números marcados como proposta são do estudo)

1. **Fonte afinada na tônica (ex.: C#).** Sample de guitarra/cordas dedilhadas renderizado de biblioteca, ou strum do Live. Ajustar o pitch do sample **antes** de granularizar — o vídeo insiste em pitch estável: *"we don't want it wavering in pitch because we can use this melodically"* (00:00:59.570).
2. **Granulação:** grain length longo o suficiente para o grão não "pipocar" (proposta: 150–300 ms), density alta e máximo de grãos alto para sobrepor; random offset para o start variar por nota; random pitch = 0.
3. **Reverse ~50/50:** duas camadas iguais (uma normal, uma reversa), como o *"probably about 50/50"* (00:02:38.450).
4. **Filtro low-pass com LFO lento e amount pequeno** — o vídeo: *"won't give it too much modulation but that does add some nice extra an extra layer of interest"* (00:04:34.169). Deixar o corte alto o bastante para o drone alcançar 1.200–4.000 Hz (é o vale de −5,76 dB) mas abaixo do brilho metálico. **Proposta:** 3–5 kHz, a calibrar de ouvido.
5. **HP antes do reverb, low cut no retorno.** É o movimento literal do vídeo em dois pontos: *"I just want to take out any of the bottom own that might sound a bit boo me"* (00:06:27.059, "bottom own" = bottom end) e *"take out some bottom end just in case we get any boom"* (00:06:57.519). **Proposta:** HP 24 dB/oct em 120–150 Hz na camada; low cut equivalente no retorno do reverb. Isso protege o low-end mono.
6. **Espaço:** LFO de pan lento (AutoPan ou LFO → pan), sem random pan exagerado; reverb grande (Hybrid Reverb), decay longo e low cut.
7. **Nível de cama:** o vídeo trata o drone como pad; aqui ele é fundo. **Proposta:** −18 a −24 dB sob o motor, a calibrar.
8. **Groove deslocado:** **não** sincronizar nada do drone em 1/16, **não** aplicar gate/retrigger rítmico. Os LFOs ficam lentos e livres (não tempo-sync), então o drone não compete com as subdivisões deslocadas.

### Por função

| Função | Aplicar? | Como / por quê |
|---|---|---|
| **kick** | Não | O drone não entra no bus do kick; o HP protege o transiente e o peso. |
| **sub** | Não | Low-end é mono; granular só acima do HP. Não mandar para o bus de sub. |
| **baixo/rolling** | Não | Textura granular borra as subdivisões deslocadas. Preencher o miolo é papel do drone, não do baixo. |
| **hats/shaker** | Não (o vídeo não cobre percussão) | Grão curto + random offset poderia gerar "nuvem de shaker", mas isso é **extensão não ensinada** — não atribuir ao vídeo. |
| **percussão de resposta** | Não | Fora do escopo do vídeo; o drone é sustentado e não responde a acento. |
| **madeira** | Sim, como fonte | Guitarra dedilhada é material de corda; um drone granular de madeira reforça o caráter orgânico sem competir com a percussão. |
| **stab** | Não | O vídeo constrói sustain, não ataque. |
| **subida** | Extensão, não ensinada | Reverse 50/50 + random start produz swells que podem virar subida de 1–2 compassos, mas o vídeo não demonstra riser. |
| **atmosfera** | **Sim — casa principal** | Camada de fundo, preenchendo 300–1.200 Hz e parte de 1.200–4.000 Hz. |

### Checklist anti-brilho-metálico
- Pitch travado (random pitch = 0, sem rota de pitch) — é instrução literal do vídeo.
- Grão longo + densidade alta (grão curto + spread = brilho metálico).
- Low-pass com LFO pequeno; nada de exciter/saturação no topo.
- Reverb com low cut (evita boom, não brilho).

### Checklist anti-engorda-sub
- HP na camada **antes** do reverb.
- Low cut no retorno do reverb.
- Drone não vai para o bus de sub nem para o lado mono do grave; é camada de médio em estéreo.

## Prioridade e esforço

- **Prioridade: alta.** O drone granular vive exatamente em 300–1.200 Hz, o vale de −4,83 dB medido, e ainda ajuda em 1.200–4.000 Hz se o low-pass não fechar demais. É a camada que preenche o miolo mais rápido sem tocar no low-end mono nem no groove.
- **Esforço: médio.** A receita é curta (poucos parâmetros + três efeitos), mas exige escolher/afinar a fonte na tônica, montar o 50/50 de reverse (o GranularOsc do Serum não tem mix de reverse) e calibrar HP/low cut de ouvido.
- **Riscos:** brilho metálico se o grão for curto ou o pitch variar; boom se o HP ficar baixo; drone "morto" se os LFOs passarem de amount pequeno — o vídeo reforça isso duas vezes (00:01:46.700 e 00:02:19.840).

## Trechos de prova

> *"but I'm not what I'm not going to do this time is I'm not going to mess around with a pitch too much because we want to keep this at the same same pitch on each note so we don't want it wavering in pitch because we can use this melodically"* — **00:00:59.570**

> *"probably about 50/50 and then definitely some LFO on the panning so let's bring that down"* — **00:02:38.450**

> *"take out some bottom end just in case we get any boom"* — **00:06:57.519**

### Provas adicionais citadas no corpo
- *"we're gonna take another look at mangle the granular plugin and we're going to create more of a tonal or musical pad or drone this time"* — 00:00:07.859
- *"I want to assign of random modulation source to the position the start position"* — 00:03:18.290
- *"this will make each note we press start anywhere along this point here"* — 00:03:28.490
- *"these little dots show you what where the grains are starting"* — 00:03:43.349
- *"it's text draw it's um it's ambien it's its atmospheric so that's what we're looking for"* — 00:03:57.879 ("text draw" = textural)
- *"if you've got max for live there's a good granular program"* — 00:08:08.480
