# I Watched 10 Techno Low-End Tutorials So You Don't Have To

- **Canal:** Sonic Academy
- **URL:** https://www.youtube.com/watch?v=iteUJHS5YNE
- **Tema:** low-end / pressão de grave
- **Legenda:** o vídeo tem faixa de legenda automática em inglês, mas ela estava indisponível no momento do estudo (limite de requisições do YouTube); a transcrição usada veio do **áudio real** (reconhecimento automático de fala, modelo small em inglês, ~21 min de fala). **As citações abaixo são literais dessa transcrição ASR, com erros de reconhecimento preservados** — ex.: "roar" = Roar, "9-on-nine" = 909, "one six" = 1/16. Capítulos citados vieram da descrição oficial do vídeo (upload de 23/10/2026, duração 1263 s).

## Técnica ensinada (2-4 frases)

O vídeo testa 8 formas de fazer o low-end (toms, rumble por cadeia de delays, reverse kick, grain rumble, LFO subs, sample de sub, dois subs em camadas, e 909 + synth sine sequenciado) e conclui que as três melhores são **LFO subs**, **dois subs em camadas** e **synth sine sequenciado**. A tese central é que o resultado vem da **escolha da fonte** — kick curto e punchy + sine puro — e não do processamento: EQ subtrativo, compressão suave e nada de "reverb wash" no grave. No detalhe, o sine é sequenciado **fora do beat 1** para o kick cortar, com **velocidade variável** e um **segundo oscilador com ataque** que dá "bite". A variação rítmica vem de **LFOs**, cuja vantagem é poder ser sincronizados em valores que não são só binários ou tercinas (5/16, 3/16 etc.), e o bus de grave fecha com **glue compressor de ataque longo/release curto + compressor de pico num canal de retorno + um toque de saturação**.

## Ferramenta usada no vídeo (plugin/stock)

**100% stock do Ableton Live.** Citação literal: `"And another one is just having this roar, so you don't need fancy plug-in. I actually did everything with the plug-ins from Ableton."` (19:26). Inventário do que aparece na fala: sample de **909**, **Operator**, **Wavetable**, **Simpler/Sampler** (sample de rumble), **EQ**, **Compressor** (bus e retorno), **Echo**, **Utility** (width), **Roar** (saturação) e um sequenciador de passos citado como "MDD snake" (05:44 — nome não confirmado pela transcrição; não afirmo qual device é). Nenhum plugin de terceiro é usado ou ensinado.

## Tradução para ambiente comum: Serum 2, Diva, Vital, Massive X, Surge XT, Live 12 nativo

**Tradução praticamente 1:1 — não falta nada.** Tudo que o vídeo usa existe no Live 12 nativo: Simpler/Sampler, Operator, Wavetable, EQ Eight, Compressor, Echo, Utility e Roar. O vídeo **não** depende de plugin pago de terceiros, então não há conceito a contornar.

| No vídeo (Live) | Equivalente | Observação |
|---|---|---|
| Operator com onda sine + LFO | **Operator** (nativo, idêntico) ou **Serum 2** (Osc A sine + LFO) | Serum 2 ganha em desenho de LFO e em valores pontuados/tercina |
| Wavetable com LFO de rates ímpares | **Wavetable** nativo ou **Serum 2** / **Vital** / **Massive X** / **Surge XT** | o ponto não é a wavetable, é o LFO poder sair do grid binário/tercina |
| Sample de sub/rumble em Simpler | **Simpler/Sampler** (nativo) ou **Serum 2 SampleOsc** | manter um take longo no tempo e outro no offbeat |
| Compressor de bus + compressor de retorno | **Compressor** nativo em bus e em return | mesmo rack, dois papéis diferentes |
| Roar no bus | **Roar** (nativo) | "just a touch" — o autor insiste em pouco |
| Utility width para domar | **Utility** (width) | casa com a prática de low-end mono |
| Echo no layer com ataque | **Echo** nativo | só em camada com brilho, nunca no sub |
| Grain rumble / reverse kick | **Grain** / Simpler reverse | grain: o autor **rejeita** ("I'm also not a big fan of this grain rumble"); reverse kick: gostou `"has nice feeling but it needs some bit more layering"` (03:52–04:02) |

O único ponto de atrito: o sequenciador de passos "MDD snake" citado em 05:44 (nome não confirmado). A função dele — gerar 8 passos de notas que o autor depois edita — é coberta pelo **piano roll do Live** ou pelo **arpejador/sequenciador do Serum 2**, sem perda conceitual.

## Aplicação por função (guardrails gerais, **proposta**)

O vídeo é quase todo subtrativo (EQ que tira o que não precisa), então ele **não resolve** carência de médios — a tradução abaixo diz onde ele ajuda e onde ele não serve.

**Kick.** A regra do autor é curto e punchy: `"choose a kick that has punch and is not that long"` (17:15) e `"the kick is picking around like -8.3... I think it can have fairly good results with having kicks between like -8 or -9"` (05:06–05:15). Ele mede o próprio kick em **150 ms** e diz que isso é "maybe 1/16th with this tempo". **A 128 BPM, 1/16 = 117 ms** (60/128/4), então o alvo a 128 BPM é corpo de kick **≤ ~117–130 ms**. Afine o kick na tônica da faixa (o dele é G). Nada de kick de cauda longa: `"if we have long kick with long tail and you want to add subby rumble thing, that's not gonna work that well"` (17:07).

**Sub.** Sine puro na **primeira oitava**, nota **logo acima** da do kick para diferenciar (`"If a kick is playing G then the sub can be a little up and then there's like good differentiation between them"`, 06:17). **Não colocar nota no beat 1**: `"avoiding placing the notes on one... really, we want the kick to cut through"` (16:47–17:02). Velocity variando (pouco), compressor só para domar, EQ subtrativo. Mono forçado (Utility width 0 — o vídeo usa exatamente Utility para "tame"). E o posicionamento fora do downbeat é a favor do kick: o vídeo já desloca a nota do beat 1 por princípio.

**Baixo / rolling.** Aqui está o achado principal: **LFO subs**. Duas notas "like every three sixteenths" (09:02) com LFO **100% sync em 1/16** (09:21), ataque e sustain no envelope, e o LFO desenhado à mão: `"you can create a really cool envelope of that LFO and really shape that movement"` (09:59). O segundo take usa **Wavetable** justamente porque o LFO dela aceita rates fora do binário/tercina — `"here I can go like 5/16, 1/38, 3/16"` (11:33, "1/38" é ruído de ASR, provavelmente 1/32) — e ele modula **LFO rate com outro LFO** e **pitch** com LFO (`"just adding a bit of LFO one to pitch"`, 12:08). Tradução: no **Serum 2**, LFO com sync pontuado/tercina e curva desenhada faz o mesmo papel; no **Operator/Wavetable** nativos, idem. **Cuidado com o groove da faixa:** usar o LFO como **modulação de amplitude/posição**, não como gerador de onsets novos, senão o pocket existente é sobrescrito. Se a cadência de 3/16 for usada, ela entra como **polirritmia** por cima do grid existente, não no lugar dele.

**Camada dupla de sub (variação).** Técnica #7: **o mesmo sample em dois takes**, um nota longa, outro no offbeat, com pitch `"up, down, down, up"` (16:00), somados e alinhados. É a receita mais barata de "respiração" no low-end sem mexer no desenho rítmico: o mesmo take da tônica em dois pontos (um no tempo deslocado, outro em outro ponto do groove) e variação de pitch — reforça o groove em vez de competir com ele.

**Hats/shaker.** O vídeo **não trata** de hats/shaker (é só low-end). O que aproveita é estrutural: o par "glue compressor no bus + compressor de pico no retorno" pode ir para o **bus de tops**, com o mesmo ajuste (ataque longo/soltar o transiente no bus; ataque afiado/release curto no retorno). Fora isso, nada a extrair.

**Percussão de resposta.** Técnica #1 (toms como low-end) é justamente o que o autor acha redundante com o sine sequenciado: `"I really like as well Tom's... but the principle is really similar to the sequenced sort of like a sine wave synth"` (03:40). Serve como **camada esporádica de resposta** afinada na tônica, nunca contínua — se virar groove principal, briga com kick+sub.

**Camada de "bite".** O vídeo não fala de fontes orgânicas; o único princípio transferível é o **"bite"**: `"I've added a bit of second oscillator that has a bit of attack... it adds that sort of like a tiny bite to it"` (07:19–07:36). Tradução: um transiente curto de percussão/material orgânico **acima** do sub, com o sub mantido sine puro — o ataque empresta presença sem engordar o grave. (**inferência** — o vídeo não cita madeira.)

**Atmosfera.** O autor é explicitamente contra wash de reverb no grave: o sine é `"more even than all the reverb washes and so on"` (07:02), e ele rejeita o "chain rumble" com delay+overdrive+reverb por soar `"bubbly"` e inconsistente (04:11–04:24). Tradução: **manter Echo/Hybrid Reverb fora do sub e do bus de grave**; se o Echo entrar numa camada com ataque, retornar com high-pass e Utility mono — foi o que ele fez (13:05–13:10).

**Processamento de bus (vale para a faixa inteira).**
- **Glue compressor no bus de grave**: `"long attack, short release, just to tame stuff that the kick through"` (18:33) — ataque longo deixa o kick passar, release curto recolhe o que sobra. Muito suave: `"it's very, very gentle"` (18:46).
- **Compressor de pico num canal de retorno**: ataque afiado, release curto, recebendo o bus inteiro (`"sharp attack, short release, so just catching the peak"`, 19:05).
- **Saturação (Roar) só como toque no bus**, e mandar mais de canais separados se precisar de mais rumble/kick (19:38–19:49). Como o **Roar gera harmônicos** (risco de brilho metálico), usar mix baixo e **high-shelf cortado acima de ~1,5 kHz** depois do Roar — **inferência**, não está no vídeo.
- O autor resume: `"if you really need a lot of processing, that means you have shitty sounds"` (18:03) e `"don't do fancy processing"` (19:54).

**Onde o vídeo NÃO resolve.** Ele não trata de preencher médios (300–4.000 Hz); toda a receita é subtrativa de grave. Para uma faixa com buraco de médios, o único gancho do vídeo é a **camada de "bite"/overtone** e os **samples em dois takes** — usados ali para dar ataque e variação, não para corrigir curva. Tratar isso como correção de médios seria extrapolação, e o estudo não faz.

## Trechos de prova

Todas as citações são literais da transcrição ASR do áudio.

1. **[18:25]** — `"So with my processing, I have a bit of like a glue compression on the bus, which was grouping the low end. So you see long attack, short release, just to tame stuff that the kick through."`
2. **[16:47–17:15]** — `"I really like using sequencers for that, but just be aware of like, avoiding placing the notes on one. It can work in some ways, but really, we want the kick to cut through. So while we're on the kick, kick, short kick, and thumbs up, this will work together if we have long kick with long tail and you want to add subby rumble thing, that's not gonna work that well."`
3. **[06:59]** — `"And this is what I like about this technique and using sine wave. It has really steady tone, fairly even, more even than all the reverb washes and so on. So it gives you really nice consistent results and allows you to achieve really strong, powerful low end that has weight."`

Citações de apoio usadas nas seções (mesma fonte): `"I actually did everything with the plug-ins from Ableton."` **[19:30]**; `"LFO 100% synced to one six"` **[09:21]**; `"here I can go like 5/16, 1/38, 3/16"` **[11:33]**; `"I think people really in those tutorials overdone their processing."` **[17:51]**.

## Limites do estudo

- Sem escuta do áudio; citações vêm de reconhecimento automático de fala (ASR), com erros de reconhecimento preservados e anotados.
- O valor de pico de kick "−8 a −9" é o que ele lê no meter dele, sem unidade declarada (provavelmente dBFS); tratar como referência de ordem de grandeza, não alvo.
- O BPM do vídeo não é citado; os 150 ms de kick são a leitura dele.
