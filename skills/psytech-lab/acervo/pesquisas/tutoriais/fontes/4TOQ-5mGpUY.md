# ANA 2 Resampling and Granular Hack

**ID:** 4TOQ-5mGpUY · **Canal:** Sonic Academy (Tech Tips Vol. 68 com Protoculture) · **Duração:** 7:26 · **Publicado:** 2021-12-17
**Legenda:** automática em inglês. **temLegenda:** true
**Descrição oficial (lida):** "From unique playable bass patches in Kick 2 to granular effects, resampled pads, and randomised arps in ANA 2" · capítulo único: "00:38 Fake Granular FX in ANA2".

> Legenda automática tem erros: "anna 2" = ANA 2; "the sample last letter" (~00:07:06) = provavelmente "sample oscillator". Nada abaixo depende dessas palavras.
> **Convenção:** `VERIFICADO (vídeo)` = está na legenda; `TRADUÇÃO/INFERÊNCIA` = leitura do estudo para rotas equivalentes, não é conteúdo do vídeo.

---

## Técnica ensinada (2-4 frases)

A ANA 2 não tem oscilador granular (*"it's obviously doesn't support granular oscillators"*, 00:00:25.599–00:00:28.550), então Protoculture constrói um **granular falso**: toca **uma nota só (C3)** do patch, dá bounce/resample, normaliza o WAV para logo abaixo de 0 dB, e arrasta esse arquivo para o **sample oscillator** da ANA 2 (*"record that and bring that back into a sample oscillator inside of the synth"*, 00:01:42.389). Depois encolhe o loop para um **trecho mínimo** e modula **loop start e loop end** com o **LFO1**, com a taxa bem baixa, para o ponto de leitura "rastejar" pelo áudio — é isso que imita o scan de um granular de verdade (*"granular oscillators essentially are just a section that is looped and then the start points of those loops... sort of move through a selection of audio"*, 00:00:59.039); o limite declarado é um loop por vez (*"we cannot generate more than one or one loop at a time"*, 00:01:10.400). As variações demonstradas são reverse do sample (00:02:54.480), **+1 oitava** para apertar/acelerar a leitura (00:03:16.560), LFO ainda mais lento para mudar a textura por completo (00:05:59.360) e alongamento até virar pad com shimmer (00:04:57.600 / 00:05:43.759). O bônus declarado é mais amplo que o granular: o resample permite empilhar uma "versão salva" de qualquer patch sobre outros sons (*"record an entire patch down to c3 bring that in and then completely change the sound up"*, 00:06:52.800).

## Ferramenta usada no vídeo (plugin/stock)

- **ANA 2** (Sonic Academy) — sintetizador; é o plugin inteiro do vídeo. Preset de fábrica de partida: **"Angel Hop"** (*"it's called angel hop"*, 00:00:44.879).
- **Sample oscillator da ANA 2** — recebe o WAV resampleado (00:01:44.159, 00:02:31.589); é onde ele mexe no loop em seguida (00:03:33.750) — inferência direta do fluxo, a legenda não nomeia o painel nesse ponto.
- **LFO1 da ANA 2** — única fonte de modulação citada: *"we're just going to go with lfo1"* (00:03:55.120), *"bring the rate right down on lfo1"* (00:04:04.000).
- **DAW: Cubase** — o bounce e a normalização acontecem nela, não na ANA 2: *"for some reason i can't drag directly from cubase"* (00:02:18.879–00:02:23.990). O vídeo não nomeia o editor de sample usado para normalizar.
- **Nada além disso é citado na legenda**: nenhum plugin de granular dedicado, nenhum stock do Live. (Não se afirma o que aparece na tela além do que a legenda menciona.) "Kick 2" só aparece no gancho da série (00:00:08.720), fora da técnica demonstrada.

## Rotas equivalentes: Serum 2 (tem GranularOsc nativo), Live 12 nativo (Simpler/Sampler/Grain), outros synths

**O ponto central:** o vídeo ensina um *workaround* para a falta de um motor granular — e synths como Serum 2 têm o motor granular nativo. A técnica se divide em duas coisas aproveitáveis: (a) o **gesto** (loop curto varrido) e (b) o **resample como fonte**, que vale em qualquer sintetizador.

### Serum 2 — caminho 1: GranularOsc (o que a ANA 2 finge ser)

| Conceito do vídeo (VERIFICADO) | Equivalente no Serum 2 | Observação |
|---|---|---|
| WAV resampleado de UMA nota, normalizado | `oscillators[].granular_source` (WAV) no slot 0–2 | mesmo fluxo: bounce → normalizar → carregar |
| "Small little snippet" + scan pelos start points (00:03:33.750) | `granular_random_offset` (%) — offset de leitura por grão | não é idêntico ao scan determinístico do vídeo; o sistema SCAN real do GranularOsc não é exposto pelo gerador de presets |
| Textura contínua/suave vs. picotada | `granular_density` (0–30, mais alto = mais contínuo), `granular_grain_length` (ms lineares), `granular_max_grains` | calibração por ouvido: grão longo = cama, grão curto = textura |
| Loop contínuo (não morrer) | `granular_loop` | manter ligado para pad/cama |
| Reverse do sample (00:02:54.480) | `granular_reverse` **ou** reverter o WAV na fonte | no vídeo é o sample inteiro invertido, não 50/50 |
| +1 oitava (00:03:16.560) | `octave: 1` / `semitone: 12` no oscilador | usar **antes** do scan para tirar energia do low-mid |
| Variação por nota | `granular_random_offset`, `granular_random_window_amount/skew` | manter `granular_random_pitch` em 0 (no máximo ±2 st) para não desafinar a fonte |

### Serum 2 — caminho 2: SampleOsc (reprodução fiel do workaround)

- `sample_loop` = `forward` (ou `ping_pong`/`tailed`), `sample_loop_start` / `sample_loop_end` = trecho curto, `sample_loop_crossfade` > 0 para evitar clique na emenda.
- **Limite do gerador de presets:** a matriz de modulação que o gerador escreve só endereça volume/pan/pitch/octave/fine de oscilador, cutoff/resonance/drive de filtro e envelopes — não há rota para loop start/end. Ou seja: **LFO → loop start/end só se faz na GUI do Serum, à mão**; pelo gerador, use o GranularOsc.
- **Armadilha do resample:** o SampleOsc toca o arquivo na afinação original quando se aperta **C5** (nota de referência fixa do engine). Se o patch está em outra nota e o WAV foi bounceado nela, tocar essa nota o reproduz **duas oitavas abaixo** — para manter o tom, tocar em C5 ou compensar com `octave`/`semitone`. O vídeo não trata de mapeamento de nota; esta é regra do instrumento (documentada no schema do engine).

### Live 12 nativo (rota sem plugin, para o resample)

- **Resample:** track de áudio com input **Resampling**, tocar a nota no patch original, gravar. **Normalizar** o clip (o vídeo pede pico "just underneath there", −0,3 dB — 00:02:02.320).
- **Grain** (Live 12 Suite): é o equivalente direto de granular de verdade — grain size / spray / position. **INFERÊNCIA**: nomes de parâmetro conferidos por memória de interface, não abertos na GUI na sessão original.
- **Simpler / Sampler:** loop curto com Start/Length pequenos e automação (clip envelope ou LFO de Max) nos pontos de loop = o mesmo gesto do vídeo. O Simpler não tem um "scan" interno; a varredura tem de vir de automação/modulação externa. `HIPÓTESE` de execução, não testada na sessão original.
- **Shifter:** atalho para a +1 oitava do vídeo numa cópia paralela, antes de granularizar.
- **Hybrid Reverb:** o "shimmer effect" final (00:05:43.759), em paralelo e com low cut no retorno.
- **Echo / AutoPan / Operator:** não são necessários para esta técnica; Echo pode empanar a cauda, AutoPan pode dar movimento lento no lugar do LFO1.

### Kontakt 8 (fonte, não motor)

Rubber Bridge Guitar, LOOP GARDEN, Ethereal Earth e Vintage Organs servem como **material a resamplear** — tocar uma nota, bouncear, carregar no GranularOsc/Grain. O vídeo não usa Kontakt; a alocação é **INFERÊNCIA** pelo papel de cada biblioteca.

### Diva, Vital, Massive X, Surge XT

Não são o caminho aqui: o vídeo não os usa e o papel granular já está coberto. Servem, no máximo, como **fonte tonal** para o resample (ex.: Diva fazendo o pad base que depois vira WAV). Não se confirma na sessão original se algum deles tem motor granular próprio — **não verificado**.

### Sobre ANA 2

O vídeo **depende da ANA 2** (sample oscillator + LFO1), mas o conceito "loop curto + ponto de leitura se movendo" é exatamente o que o **GranularOsc do Serum 2** e o **Grain do Live 12** fazem nativamente — não há dependência a contornar. `traduzivel = true`.

## Onde usar (por função: kick, sub, baixo/rolling, hats/shaker, percussão de resposta, madeira, stab, subida, atmosfera)

**Regra-mãe:** esta técnica produz **sustain com movimento**, não ataque. Ela entra onde a faixa precisa de corpo médio/cauda — nunca no transiente, nunca abaixo do HP, nunca travada no grid rítmico.

| Função | Usar? | Como (ponto de partida — `HIPÓTESE`) | Por que / cuidado |
|---|---|---|---|
| **kick** | Não | — | Loop curto + scan destrói o transiente e cria sidebands em 100–300 Hz; o kick carrega a pressão e o mono. |
| **sub** | Não, nunca | — | Qualquer varredura de loop modula o fundamental e desfaz o mono. Nenhum bus granular abaixo de 120 Hz. |
| **baixo/rolling** | Não no corpo | No máximo a **cauda** da nota, HP ≥300 Hz, como camada de movimento | O groove do rolling vive da leitura rítmica seca; grão aleatório borra a subdivisão. |
| **hats/shaker** | Evitar | Se usar: só em paralelo, HP ≥2 kHz, nível baixíssimo | Loop curtíssimo em prato = **ring metálico**. O vídeo chama o resultado de "shimmer" (00:05:43.759) — shimmer é o risco, não o objetivo. |
| **percussão de resposta** | Sim, como **cauda**, não como ataque | Resamplear uma madeira, granular a cauda, disparar junto do evento de resposta mantendo o ataque original intacto | A resposta continua sendo madeira seca; o granular só prolonga/abre o timbre depois do transiente. LFO **livre** (não tempo-sync) para não sugerir grade. |
| **madeira** | **Sim — fonte principal** | Bounce de uma nota na tônica de kanun/balafon/Rubber Bridge Guitar → GranularOsc; grãos longos, `random_offset` médio | Madeira tem transiente e ruído orgânico; é a fonte que menos soa "digital" granulada. |
| **stab** | Só a **cauda** | Copiar o stab, granular com grãos longos, HP ≥300 Hz; o stab seco continua na frente | Granular no ataque apaga a definição do stab. |
| **subida** | Extensão (o vídeo não mostra riser) | Scan acelerando (LFO mais rápido ou automação de posição) num reverse; subir o LPF devagar | Se fizer, segurar o topo com LPF suave e HP 200–300 Hz para não chover sideband. |
| **atmosfera** | **Sim — casa principal** | Bounce de madeira/voz na tônica → GranularOsc com grão longo (200 ms–2 s), densidade baixa/média, `random_pan` real, HP 180–250 Hz, camada estéreo **acima** de ~200 Hz | É a camada que preenche o vale de médios sem tocar no low-end. Boa prática geral: largura estéreo real só acima de ~150–250 Hz. |

### O truque do vídeo que vale como receita: subir 1 oitava antes do scan

O vídeo mostra *"raise an octave up it's essentially going to speed up the waveform as well"* (00:03:16.560). Se a madeira está num registro grave e você a sobe uma oitava **antes** de granularizar, o conteúdo granular sobe de registro — **sai do low-mid que engorda o sub e cai dentro do vale de médios (300–1.200 Hz)** que o set de referência mede carente. Depois, HP em 180–250 Hz como cinto de segurança.

### Receita mínima (por camada)

1. Tocar **uma nota** (na tônica da track) da fonte — madeira, voz, guitarra, stab — e **resamplear** (no vídeo: C3, 00:49.439).
2. **Normalizar** o WAV; o vídeo deixa o pico logo abaixo de 0 dB (−0,3) — 00:01:55.439 / 00:02:02.320.
3. Carregar em **GranularOsc** (Serum 2) com `granular_grain_length` longo o bastante para não "pipocar" e `granular_random_offset` médio; `random_pitch = 0`.
4. Subir **+1 oitava** no oscilador (o movimento do vídeo) e **HP 180–250 Hz** na camada.
5. LFO **livre** e lento no movimento (densidade/posição/pan), longe de 1/16 — a textura não pode espelhar nem mascarar o groove.
6. A/B: mute a camada. Se o sub "encher" ou o topo ficar metálico, o problema é fonte/HP/grão — não é para corrigir com EQ depois.

### Regras anti-engorda-sub e anti-brilho-metálico

- **Nada de granular abaixo de ~180 Hz.** HP em toda camada; não mandar para o bus de sub nem para o lado mono do grave.
- **Pitch estável** (`random_pitch = 0`; no máximo ±2 st). A variação vem de **posição** (offset/scan), não de afinação.
- **Brilho metálico ≠ agudos.** O que soa "metálico" é **inarmonicidade**: loop curtíssimo + grão curto + pitch instável. Use grão longo, fonte escura e emenda com crossfade. Não use LPF como muleta — se o set de referência já está **abaixo** das referências em 8 kHz+, cortar topo por reflexo piora o balanço.
- **Nada de tempo-sync** no LFO desta camada: a textura tem de flutuar livre sobre o groove.

## Prioridade e esforço

- **Prioridade: baixa a média.** O conceito já está resolvido em synths com GranularOsc nativo (Serum 2, Vital, Grain do Live): o vídeo ensina a burlar a ausência de um oscilador granular. O que resta de novo e útil é o **resample como fonte** (bounce de uma nota + normalização) e o **+1 oitava antes do scan** — duas ideias boas, mas periféricas a um motor minimalista centrado em kick/sub/baixo/groove.
- **Esforço: baixo a médio.** Baixo para o resample (uma ida ao bounce + normalizar). Médio para achar o ponto em que a textura preenche o vale de médios sem soar metálica nem inflar o low-end — isso é calibração de ouvido, não receita fechada.

## Trechos de prova: 3 citações literais da legenda com timestamp

> "so granular oscillators essentially are just a section that is looped and then the start points of those loops um sort of move through a selection of audio" — **00:00:59.039–00:01:10.390**

> "can take what the output of ana is and actually record that and bring that back into a sample oscillator inside of the synth" — **00:01:40.240–00:01:49.429**

> "so the granular we want to kind of just get a small little snippet so we're going to set the loop start" — **00:03:32.000–00:03:37.400**

### Provas adicionais citadas no corpo

- *"going to show you how you can do sort of fake granular effect inside of anna 2"* — 00:00:21.119
- *"it's obviously doesn't support granular oscillators"* — 00:00:25.599
- *"we cannot generate more than one or one loop at a time"* — 00:01:10.400–00:01:15.429
- *"are going to re-sample this so this is another cool trick that you can do"* — 00:01:31.040
- *"just normalize this waveform just so we have the peak level at zero"* — 00:01:55.439; *"negative zero point three"* — 00:02:02.320
- *"let's say if we wanted to reverse this"* — 00:02:54.480
- *"raise an octave up it's essentially going to speed up the waveform as well"* — 00:03:16.560
- *"assign some modulation to our loop start and end points so we're just going to go with lfo1"* — 00:03:55.120
- *"we're just going to bring the rate right down on lfo1"* — 00:04:04.000
- *"turn this into like a pad sound now as well"* — 00:04:57.600
- *"yeah really nice shimmer effect that we're getting now"* — 00:05:43.759
- *"it'll totally change the texture of the sound"* — 00:05:59.360
- *"record an entire patch down to c3 bring that in and then completely change the sound up"* — 00:06:52.800

---

**Limites:** as regras de pitch estável (±2 st), HP 180–250 Hz e calibração de grão em ms são recomendações do estudo, não do vídeo. O contexto de mix (vale de médios 300–1.200 Hz, low-end mono, groove deslocado) citado no corpo é do set de referência do levantamento original — não foi re-medido. A leitura do schema do gerador de presets (limitação de rota de modulação para loop start/end) foi feita na sessão original de dissecação.
