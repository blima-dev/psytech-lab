# PSYTECH SOUND DESIGN By MVND

- **Canal:** Vision Serpent · **Convidado:** Klaus / MVND (produtor de psychedelic techno, mentor em pickyourself.com — 00:00:05.760)
- **URL:** https://www.youtube.com/watch?v=Wmr4dnvhVkc · **Duração:** 10:20 (620 s, medido com `yt-dlp --print "%(duration)s"`)
- **Legenda:** automática `en-orig`, 1696 linhas, falada de 00:00:03.400 a 00:10:05.600. `temLegenda=true`.
  A trilha `en` espelho falhou com HTTP 429; a `en-orig` baixou completa (60,76 KiB) e cobre todo o trecho falado do vídeo.
- **Escopo real do corte público:** o vídeo abre prometendo variações com Infiltrator e Portal (00:00:28.360), mas o áudio termina em 00:10:05.600 — o corte público cobre **só a construção do lead no Serum**. As variações ficam no full-length do Patreon (descrição). Nada sobre elas foi inventado aqui.

---

## Técnica ensinada (2-4 frases)

Klaus monta um lead psytech do zero — "we're not going to use presets" (00:00:35.240) / "We're going to do everything from scratch" (00:00:38.320) — sobre uma base de saw simples escolhida pelos overtones ("the saw wave has all the overtones that we need for a nice rich foundation", 00:03:48.360), somando uma segunda camada de caráter no Osc B ("I'm going to use this as the character layer", 00:04:03.760) e uma camada duas oitavas abaixo ("Also two octaves down", 00:05:32.919). O movimento vem de imperfeições pequenas por nota, em modo livre — "add some little imperfections into the sound… moving but at a subconscious level" (00:04:43.840 / 00:04:47.720), "every note feels different" (00:04:57.120). A escolha de timbre acontece por audição de pontos de operação, não por receita: "these are all sweet spots. It's not like there is a recipe for how to do this" (00:07:46.800), e ele **recusa explicitamente** o lead de trance clássico de LPF com ressonância — "we've heard it before. Like, come on, let's get over it" (00:06:29.320) — trocando por um filtro "eccentric" (00:06:47.640). Fecha com dois filtros em série ("filter one is going to filter two, because filter two is then going to be our cutoff", 00:08:21.000), envelope plucky no cutoff (00:08:41.719), macro no decay desse envelope para performar ao vivo (00:09:24.040 / 00:09:33.040) e **sync nos dois osciladores amarrado ao mesmo envelope** — "as the filter opens up we're also going to get more sync" (00:09:56.280), resultando em "more texture and more grit" (00:10:05.600).

---

## Ferramenta usada no vídeo (plugin/stock)

| Ferramenta | Papel no vídeo | Prova literal |
|---|---|---|
| **Ableton Live** | DAW / sessão onde tudo acontece | "we're going to jump into Ableton" (00:00:21.720) |
| **Xfer Serum** | a maior parte do sound design do lead | "I'm going to use Serum for most of the sound design" (00:00:23.840) |
| **Infiltrator** | variações do lead — **só citado, não demonstrado no corte** | "we're going to create variations of the main lead using Infiltrator and Portal" (00:00:28.360) |
| **Portal** | variações do lead — **só citado, não demonstrado no corte** | idem (00:00:28.360) |

Nenhum device stock do Live é nomeado no trecho falado. O vídeo não define o que Infiltrator ou Portal fazem — a tradução conceitual deles está na seção seguinte e é marcada como inferência.

---

## Tradução para um arsenal compatível: Serum 2 (tem GranularOsc nativo), Diva, Vital, Massive X, Surge XT, Kontakt 8 (Rubber Bridge Guitar, LOOP GARDEN, Ethereal Earth, Vintage Organs), Live 12 nativo (Simpler/Sampler/Grain, Operator, Echo, Hybrid Reverb, AutoPan, Shifter). Sem ANA 2, VELA, SideKick, Kick 3, Bitwig — se o vídeo depende deles, explique o conceito equivalente.

O vídeo **não depende de nada fora desse arsenal**: tudo é Serum + Live. `traduzivel=true` sem perda.

| Bloco do vídeo | Prova | Equivalente |
|---|---|---|
| Saw rica como fundação | 00:03:48.360 | Serum 2 Osc A em `analog_basic` / `analog_warm` (saw); alternativa Diva ou Surge XT se quiser deriva analógica. `Vintage Organs` serve como fonte de harmônicos ricos e "madeira" no meio. |
| Camada de caráter no Osc B com wavetable "out there" | 00:04:03.760, 00:04:05.800 | Serum 2 Osc B com `wavetable` fora do óbvio (`pwm`, `digital_fm`, `custom_harmonics`); Vital e Massive X fazem o mesmo papel. **Extra possível:** o `GranularOsc` do Serum 2 dá uma camada de caráter que o vídeo não tinha — usar em profundidade baixa, só como textura. |
| Camada duas oitavas abaixo | 00:05:32.919 | `octave: -2` em um oscilador do Serum 2 (schema expõe `octave` de −4 a +4). Uso restrito ao corpo do lead/stab — nunca na pista de sub. |
| Imperfeições subconscientes / modo livre | 00:04:43.840, 00:04:47.720, 00:05:52.760 | Fonte aleatória por voz do Serum (`random1`/`random2`) em quantidade pequena, ou LFO com `mode='Free'` (`beat_sync=false`) — o "put the path to free, so we don't always get the same sound" (00:05:52.760) é exatamente isso. Em Live: AutoPan em LFO livre, ou humanização no Simpler. |
| Dois filtros em série, Filter 2 = cutoff | 00:08:21.000 | Serum 2 `filters[0].output_routing='series'` + `filters[1]` com o cutoff; Diva, Vital, Massive X e Surge XT têm roteamento duplo equivalente. |
| Filtro "eccentric" em vez do LPF ressonante de trance | 00:06:17.640, 00:06:19.840, 00:06:29.320, 00:06:47.640 | No Serum 2: `comb`, `formant`, `bandpass` ou `moog_lowpass` com ressonância baixa. É escolha de caráter, não de marca. |
| Envelope plucky no cutoff | 00:08:41.719 | Serum 2 `Env 2` (índice 1) → `filter1.cutoff`, decay curto; no Live, o envelope de filtro do Operator/Simpler. |
| Macro no decay do envelope para performar | 00:09:24.040, 00:09:33.040 | `macro0` → `env1.decay` no Serum 2; no Live, macro do rack → Auto Filter. |
| Sync dos osciladores + decay | 00:09:48.120, 00:09:56.280 | No schema do gerador de presets do Serum 2, a rota exposta é `warp_mode='sync'` com `warp_amount` modulado pelo mesmo envelope/macro. |
| Variações (Infiltrator / Portal) | 00:00:28.360 — **não demonstrado** | **INFERÊNCIA, não do vídeo:** cadeia de multi-efeito modulada = Echo + Shifter + AutoPan + Redux no Live; granular/espectral = Grain (Grain Delay) / Shifter / `GranularOsc` do Serum 2 / `LOOP GARDEN` e `Ethereal Earth` do Kontakt 8 para camadas de textura. |

**Kontakt 8 no lugar certo:** `Rubber Bridge Guitar` (palhetada, corpo no meio) é a fonte orgânica mais próxima do gesto "plucky" que o vídeo constrói por síntese; `LOOP GARDEN` / `Ethereal Earth` cobrem a camada atmosférica que o corte não chega a mostrar.

**Ressalva de transcrição (não inventar parâmetro):** em 00:05:44.760 o áudio sai como "attach the Y" — a legenda automática pode ter perdido a palavra (o modulador é citado antes, mas não nomeado de forma clara). O que está literal e verificável é o gesto: prender o modulador a uma faixa estreita ("to just this section here", 00:05:48.080) e deixá-lo em modo livre (00:05:52.760). `HIPÓTESE` sobre o nome do parâmetro; `VERIFICADO` sobre o gesto.

---

## Aplicação concreta em um motor minimal de 2 minutos

Contexto medido do set de referência: meio 300–1.200 Hz **−4,83 dB** e 1.200–4.000 Hz **−5,76 dB** contra a média de 6 referências externas; low-end é mono; groove usa subdivisões deslocadas **.27/.77** e deve ser preservado.

O vídeo **não fala de kick, sub, hats nem percussão**. Tudo abaixo é ou tradução direta do que ele faz no lead, ou marcado como `INFERÊNCIA`.

| Função | O que o vídeo dá | O que fazer no motor |
|---|---|---|
| **Kick** | **Nada.** O vídeo não trata de kick. | Não extrair nada daqui para o kick. Zero mudança. |
| **Sub** | **Nada.** O vídeo não trata de sub. | Não aplicar. A camada "two octaves down" (00:05:32.919) é do lead e **não pode** descer para a pista de sub — o low-end é mono e o sub não pode engordar. |
| **Baixo / rolling** | **Nada direto.** Só o conceito de "camada de caráter". | `INFERÊNCIA`: se quiser grit no rolling, criar uma camada separada **acima de ~200 Hz**, com filtro próprio e sem sync no corpo do baixo. Sync no baixo gera harmônicos que comem headroom do sub e soam metálicos. |
| **Hats / shaker** | **Nada direto.** Só o princípio "imperfeições subconscientes" (00:04:43.840 / 00:04:47.720). | `INFERÊNCIA`: variação imperceptível por hit (velocity/decay/sample no Simpler), nunca pan — pan quebra a regra de low-end mono se vazar para o grave. Baixa prioridade. |
| **Percussão de resposta** | **Nada direto.** O molde de filtro "eccentric" + envelope plucky serve se a resposta for sintética. | `INFERÊNCIA`: usar o mesmo patch do stab em versão mais curta, sem camada de duas oitavas abaixo. Se a resposta for sample, nada a fazer. |
| **Madeira** | **Alvo principal.** Saw rica + camada de caráter + dois filtros em série + envelope plucky. | Montar o patch de duas camadas: Osc A saw (fundação, 00:03:48.360) + Osc B com wavetable de caráter em nível baixo (00:04:03.760); Filter 1 → Filter 2 em série com Filter 2 como cutoff (00:08:21.000); Env 2 plucky no cutoff (00:08:41.719); macro no decay do envelope (00:09:24.040). Esse patch vive exatamente em 300–1.200 Hz — é o que tapa o buraco de −4,83 dB. |
| **Stab** | Mesmo patch, gesto mais curto; a performance vem do macro. | Encurtar o decay do Env 2 e deixar `macro0 → env1.decay` para abrir/fechar na mão (00:09:33.040). O stab é a versão de 1–2 notas que preenche o meio sem competir com o groove .27/.77. |
| **Subida / transição** | Sync + abertura de filtro = "as the filter opens up we're also going to get more sync" (00:09:56.280) → "more texture and more grit" (00:10:05.600). | Automatizar `warp_amount` (sync) junto com o cutoff ao longo de 8–16 compassos. É um riser de **grit no meio**, não de brilho: não sobe o topo. Fechar com Echo + Hybrid Reverb. |
| **Atmosfera** | LFO livre modificando uma faixa estreita ("attach the Y to just this section here", 00:05:44.760; "put the path to free", 00:05:52.760). | `INFERÊNCIA`: LFO Free + `random1` em profundidade pequena na posição de wavetable de uma camada Grain/LOOP GARDEN. Movimento que não se nomeia — é exatamente a descrição dele ("at a subconscious level"). |

### Guardas contra engordar o sub e contra brilho metálico

1. **Duas oitavas abaixo só no miolo.** Se usar a camada de 00:05:32.919, ela entra no lead/stab com high-pass e nível baixo; jamais na pista de sub. (A necessidade de HPF é `INFERÊNCIA` — o vídeo não fala de frequência.)
2. **Nada de pan spread no que toca o grave.** As "imperfeições" vão em posição de wavetable, cutoff e decay — não em pan. Mantém o low-end mono como já está.
3. **Sem o LPF ressonante que ele recusa.** O próprio vídeo rejeita o "classic side trance lead… with the filter resonance" (00:06:17.640 / 00:06:19.840). Ressonância alta + sync em cutoff aberto é a receita do brilho metálico; escolha um filtro de caráter (comb/formant/bandpass) e mantenha o Q baixo.
4. **O grit fica na faixa que está faltando.** O conteúdo de sync serve ao buraco de 1.200–4.000 Hz (−5,76 dB). Se ele espirrar acima disso, shelf suave — não corte o miolo. (`INFERÊNCIA`; o vídeo não dá número de frequência.)
5. **O groove manda.** Klaus escreve um groove só para ouvir o lead — "I'm just adding this groove so I can kind of listen in on the lead" (00:03:14.080) — e diz que "this is by no means the final groove" (00:03:18.640). No material de referência é o inverso: o groove deslocado (.27/.77) governa. O envelope plucky tem de ser curto o bastante para deixar as subdivisões deslocadas respirarem; não copiar o groove dele.
6. **A tônica não vem do vídeo.** A track dele é "in D" (00:03:11.640). O lead/madeira do material de referência sai em C# frígio — copiar só o gesto, nunca a altura.

---

## Prioridade e esforço

- **Prioridade: alta.** Entrega um patch plucky de meio (madeira/stab) prontamente encaixável no buraco medido de 300–1.200 Hz (−4,83 dB). A frente é textura-atmosfera, e o mesmo patch serve para a camada de atmosfera com LFO livre.
- **Esforço: médio.** Tudo existe no Serum 2, sem plugin novo; o custo é tempo de audição de wavetables e de "sweet spots" — o próprio autor avisa que fica "silent for like ages" ouvindo (00:08:03.640). Não é trabalho de uma passada; é sessão de sound design dedicada.
- **Não cobre:** kick, sub, hats e percussão de resposta. Para o motor dos 2 minutos, o retorno é no miolo, não no peso. Por isso não sobe para prioridade máxima do motor.

---

## Trechos de prova: 3 citações literais da legenda com timestamp

1. **00:04:03.760** — "oscillator B and I'm going to use this as the character layer." (contexto: 00:04:01.440 "instead I am going to activate")
2. **00:07:46.800** — "these are all sweet spots. It's not like there is a recipe for how to do this."
3. **00:09:56.280** — "as the filter opens up we're also going to get more sync." (resultado em 00:10:05.600: "we're getting more texture and more grit.")
