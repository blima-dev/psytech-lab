# Bateria + graves psytech — especificação de cena, vetos e auditoria técnica

## Sumário executivo

**Veredito:** o caso medido (uma faixa psytech de referência) já tem o fundamento estrutural do gênero. O problema aberto **não é "falta de sub" e também não é "falta de sidechain"**. O bloco está mais ameaçado por três coisas mensuráveis: **topo insuficiente apesar de presença médio-aguda já excessiva; densidade de transientes acima da própria régua da cena; e concentração anormal em 55–75 Hz em relação ao corpo do kick**.

A pesquisa encontrou um ponto importante: **não existe uma especificação pública 2024–2026 da cena dizendo "kick = X LUFS, bass = Y dB, sidechain = Z ms"**. Zenon Education ensina explicitamente alinhamento de fase, articulação do baixo, envelopes, repetição, diálogo e arranjo de percussão, mas não publica esses valores como norma. Portanto, os números abaixo separam rigorosamente três classes: **consenso técnico (C)**, **medição do corpus/referências (R)**, e **faixa de engenharia recomendada (E)**, sem transformar heurística em lei.

| Descoberta | Veredito |
|---|---|
| **Fundamento 25–40 Hz** | **RESOLVIDO.** `sub−kick = −2,64 dB` (caso medido), praticamente Slippery Slope `−2,24 dB` e dentro do envelope Kaled/Gazolla/ISMAIL `+0,34…−6,77 dB`. Não reabriria "falta sub". |
| **55–75 Hz** | **NOVO RISCO DE GRAVE.** Caso medido: `55–75 − 40–55 = +4,0 dB`; referências: Kaled `+1,4`, Gazolla `−1,2`, ISMAIL `0,0 dB`. Está ~`+2,6 dB` além até da referência mais extrema do pequeno corpus. |
| **Topo / ar** | **FORA.** 8 kHz+: `−27,1 dB` contra média das três refs `−20,8 dB`: déficit de **6,3 dB**. "Ar": `−21,0` contra média `−16,47`: déficit de **4,53 dB**. Centroide interno `202` contra `266–287`. |
| **Mas "abrir" 2–4 kHz?** | **NÃO.** Presença já é `0,64` contra `~0,51`. Somar presença para resolver brilho tende a atacar a região errada. Frequências agressivas de pratos/transientes frequentemente aparecem entre 4–10 kHz, portanto um shelf global de +5/+7 dB também é uma solução perigosa. |
| **Densidade** | **FORA.** `7,57 picos/s` contra teto interno `6,99`: **8,3% acima**; Slippery Slope trabalha nos trechos densos em `6,0–6,8 onsets/s`. Antes de acrescentar hats, provavelmente é preciso **redistribuir eventos**. |
| **Sem sidechain nos graves** | **DEFENSÁVEL.** Zenon coloca alinhamento de fase e articulação no centro do kick×bass; sidechain é uma técnica possível, não um requisito físico. FabFilter confirma que kick→bass é comum, mas também alerta que tempos agressivos podem distorcer o baixo. |
| **Low-end mono** | **DENTRO DO CONCEITO.** A régua ≤120 Hz é coerente e conservadora. O que ainda falta é comprovar no render a energia lateral/correlação abaixo de 120 Hz, porque ter Utilities no Set não prova sozinho o resultado final. |
| **Master −10,2 LUFS / −0,6 dBTP** | **LUFS defensável; TP não é seguro para Spotify.** Spotify recomenda, para masters acima de −14 LUFS, TP abaixo de `−2 dBTP`; o caso está ~`1,4 dB` acima disso. Beatport, por outro lado, declara que não normaliza/remasteriza o WAV recebido, portanto "Beatport = −8 a −6 LUFS" **não é regra oficial da plataforma**. |

Há ainda **duas correções de diagnóstico** importantes:

1. O briefing chamava o rolling bass de **"C#2 ≈ 103,8 Hz"**. Isso é inconsistente: C#2 é `69,3 Hz`; `103,8 Hz` é aproximadamente **G#2**. A auditoria confirma o canal como sub roll em G#2. É falha de documentação/metadado, não evidência de erro sonoro — **nunca confie no nome, meça**.
2. **Não se considera provado** que "2× EQ8 + 2× Utility na mesma cadeia = dupla rotação de fase problemática". Número de plugins ≠ dano de fase. O teste correto é resposta de fase/impulso ou null test com a cadeia, não contagem de devices.

O contexto atual da própria cena confirma que 128 BPM permanece perfeitamente válido: lançamentos Psy-Techno de Luis M em 2026 incluem `Singularity` e `Primordial` a 128 BPM; AlpaKa descreve lançamentos atuais em termos de rolling basslines, driving percussion, hypnotic grooves e bushtech de graves "chunky".

## Parte A — O que PRECISA ter

### Checklist técnico do bloco

| Item | Papel / faixa | Métrica e alvo | Tolerância / gate | Evidência |
|---|---|---|---|---|
| **Tempo** | Motor hipnótico | **126–132 BPM** é claramente corrente no ecossistema; `128` é centro válido | Não tratar 128 como problema | Beatport mostra Luis M 128–130 e AlpaKa 2026 descreve psytech 130–132. **R/estética atual.** |
| **Kick — fundamento** | Impacto + âncora tonal do pulso | Sample nominal `48 Hz` no caso; região técnica relevante para fundamentos graves é aproximadamente `40–80 Hz` | Frequência isolada não decide qualidade; medir cauda/overlap | iZotope aponta fundamentos de bass/kick frequentemente na região `40–80 Hz`. **C geral**, não regra Zenon. |
| **Kick — ataque/click** | Faz o kick sobreviver sobre o baixo e sistemas menores | Deve ter conteúdo acima do fundamento; Zenon ensina explicitamente adicionar altas frequências ao ataque | **Não existe dB universal publicado** | Zenon Education dedica módulo específico a "Clicks and high frequencies" do kick. **R cena.** |
| **Sub/fundamento** | Pressão física, não movimento estéreo | Para **este corpus**: `sub−kick 25–40 / 40–55` observado entre `−6,77 e +0,34 dB`; zona de "peso" defensável aproximadamente `−3…+0,5 dB` | Abaixo de ~`−7 dB` seria claramente mais magro que as três refs; acima de ~`+1 dB` exigiria validação de headroom | **R corpus**, não norma universal |
| **Região kick/rolling 40–75** | Evitar um único andar grave dominar | Nas três refs: `(55–75) − (40–55)` = `−1,2…+1,4 dB` | Gate pragmático: **±1,5 dB**. >`+2 dB` persistente merece investigação | **R corpus** |
| **Baixo rolling** | Movimento/hipnose | 16 avos a 128 BPM = **117,19 ms por célula** | Nota/envelope deve terminar ou liberar espaço suficiente antes do próximo evento relevante | Cálculo temporal + articulação explicitamente ensinada pela Zenon. |
| **Duração da nota rolling** | Define seco/legato e separação kick×bass | Ponto de partida: **~64–94 ms** = 55–80% de um 16º a 128 BPM | `~50–105 ms` pode continuar plausível dependendo do envelope; acima dos `117 ms` há sobreposição por construção | **E.** Heurísticas atuais de psytrance sugerem ~60–90 ms a 145 BPM, mas não são norma Zenon. |
| **Kick × bass temporal** | Deve funcionar como um único motor, sem somar duas caudas contraditórias | Medir primeiros `0–117 ms` após cada kick; avaliar overlap, polaridade e mono-sum | Gate de QA sugerido: investigar qualquer trecho repetitivo com **perda >3 dB ao somar em mono** ou cancelamento consistente | Zenon ensina alinhamento de fase kick/bass; iZotope enfatiza mascaramento e interação, não EQ isolado. **C/R.** |
| **Ducking / shaping** | Criar espaço somente se arranjo/envelope não bastar | **0 dB de ducking pode ser correto.** Se utilizado, deve encerrar antes da próxima nota relevante | Não existe justificativa para impor `2–6 dB` só por gênero | FabFilter: kick→bass é prática comum, mas ataque/release rápidos demais podem começar a modificar ciclos de onda e distorcer. **C.** |
| **Microtiming do kick** | Mantém motor estável | **0–5 ms** da grade como alvo de engenharia | Não há razão para humanizar aleatoriamente o kick | **E**, não lei de gênero |
| **Microtiming de hats/percussão** | Sensação humana sem perder precisão | **5–20 ms intencionais** são uma região segura de experimentação | `~19–24 ms` já chega ao limiar médio de detecção para kick/snare/hat em estudo recente; offsets aleatórios >`25 ms` passam a ser de alto risco | JND = menor diferença temporal detectável de forma confiável. Estudo 2025: drums ≈19–24 ms; bass ≈31–35 ms. **C perceptual.** |
| **Densidade forte em marcha/drop** | Pressão contínua sem virar parede | Corpus: **6,0–6,8 onsets/s**; gate interno **≤6,99/s** | `>7,0/s` persistente é fora do corpus atual | **R corpus/Slippery** |
| **Polos rítmicos** | Criar empuxo sem preencher todo 16º | Primeiro tempo + último 16º antes do próximo pulso são um desenho forte na Slippery Slope | Não é obrigatório em toda faixa; é assinatura particularmente compatível | A Zenon ensina repetição + "dialogue" entre percussionistas, não preenchimento contínuo. |
| **Top percussion** | Contraste, percepção de velocidade e abertura | Pela régua interna do corpus: `8k+ ≈ −22…−20 dB`; "ar" ≈`−17,5…−16 dB`; centroide `266–287` | Usar **a mesma régua**, porque "centroide 266" não é comparável a valores externos sem definição da implementação | **R corpus** |
| **Aspereza** | Agudo útil sem chiado | Não fechar uma lacuna de 6 dB com um shelf global equivalente | `4–10 kHz` é justamente uma faixa frequente de agressividade/sibilância; corrigir seletivamente | iZotope 2025. **C geral.** |
| **Mono grave** | Robustez em PA/mono e imagem central | **Régua do corpus: mono até 120 Hz** | No render: correlação abaixo de 120 Hz deve estar próxima de `+1`; `≥0,98` é um gate prático, não norma industrial | A prática de manter o sub central é coerente; valores exatos de crossover variam. Heurísticas de psytrance publicadas vão até ~150–200 Hz, portanto **120 não é agressivo**. |
| **Largura acima do grave** | Separar centro monolítico de texturas/percussão | Referências do corpus: correlação média `0,32–0,44`; gate interno `0,32–0,55` | Isso é para **banda média/full context**, não para sub | **R corpus** |
| **Break** | Retirar a certeza rítmica e criar contraste | Onset pode chegar literalmente a **0/s** | Não há obrigação de preservar kick ou tops | Slippery Slope medida: ~15 s sem transientes. Zenon também ensina progressão por muting/arrangement. |
| **Intro** | Preparar identidade e escala de energia | Kick pode estar presente **ou ausente** | "Intro sem kick" é estética, não requisito | A própria Slippery entra sem kick; o caso entra com kick. Ambos são compatíveis com a lógica de contraste. |
| **Outro** | Reduzir camadas preservando mixabilidade/DJ utility | Um desenho particularmente útil é retirar top antes do grave | Não obrigatório | O comportamento da Slippery demonstra exatamente isso |
| **LRA** | Macro-dinâmica entre marchas/breaks | `~4–7 LU` é uma faixa moderna plausível, não específica de psytech | `5,6 LU` do caso está no intervalo | Estudo iZotope 2024: metade do corpus Billboard analisado ficou em `3,7–6,8 LU`; usar apenas como sanity check. |
| **LUFS integrado** | Competitividade/master | **Não existe alvo oficial Beatport −8…−6.** O mercado atual mostra masters fortes, mas loudness não deve ser gate de gênero | `−10,2 LUFS` não desqualifica a faixa | Beatport entrega o WAV recebido, sem normalização. Spotify normaliza playback. |
| **True Peak** | Segurança de encode | Spotify: master >`−14 LUFS` → **TP < −2 dBTP** recomendado | `−0,6 dBTP` falha nesse critério específico de streaming em `1,4 dB` | **C de entrega**, não estética. |

### O ponto mais importante sobre kick × bass

A literatura de cena encontrada **não sustenta a regra "psytech obrigatório = compressor sidechain"**. A própria Zenon Education estrutura o ensino em **phase alignment → kick EQ → bass articulation**; no módulo de kick, fala em corrigir problemas no shape antes de tentar salvá-los com EQ.

Portanto:

> **Separação por arranjo + envelope curto + fase coerente é solução tecnicamente legítima. Sidechain é contingência, não requisito.**

Isso é particularmente importante porque usar ducking rápido em sinais graves pode gerar distorção quando o compressor começa a seguir ciclos individuais da onda; a FabFilter também observa que ataques menores que ~50 ms em fontes graves percussivas podem alterar excessivamente seu low-end.

A única pergunta correta é: **o render prova que kick e baixo coexistem sem mascaramento/cancelamento?** No caso medido, com os dados disponíveis, essa resposta é `INDETERMINADO`.

## Parte B — O que NÃO PODE ter

A ordem abaixo é de **risco técnico/club playback**, não de gosto.

| Gravidade | Veto / erro | Limiar prático | Por que fecha a faixa |
|---|---|---|---|
| **CRÍTICO** | Cancelamento recorrente kick×sub | Reprovar se mono-sum ou combinação kick+bass perde **>3 dB** repetidamente na zona `25–120 Hz` em hits equivalentes | Duas ondas graves fora de fase podem subtrair energia justamente onde o PA deveria entregar pressão; Zenon trata phase alignment como assunto central. |
| **CRÍTICO para streaming** | TP excessivamente próximo de zero em master loud | Spotify: >`−14 LUFS` → **<−2 dBTP** | Encode com perdas pode gerar overs adicionais; Spotify explicita risco de distorção. `−10,2 LUFS / −0,6 dBTP` → **FORA** para esse critério. |
| **ALTO** | Baixo ocupar a próxima célula sem intenção | A 128 BPM, um 16º = `117 ms`; envelope efetivo >`117 ms` necessariamente invade a célula seguinte | Transforma rolling seco em sustentação/legato e reduz espaço para kick/percussão |
| **ALTO** | Excesso persistente de 55–75 sobre 40–55 | Corpus: `−1,2…+1,4 dB`; investigar acima de `+1,5`; forte alerta >`+2` | Torna o grave "um andar só", aumenta carga no limiter e pode deslocar a percepção de kick. O caso mediu **+4,0 dB** → **FORA** |
| **ALTO** | Densidade destruir espaço negativo | Corpus forte: `6,0–6,8/s`; gate `6,99/s` | Em estética minimal/hipnótica, acrescentar onsets reduz hierarquia e transforma microvariação em preenchimento. Caso: `7,57/s` → **FORA** |
| **ALTO** | Humanização aleatória grande em bateria | >`~25 ms` em hats/kick começa a ultrapassar o JND médio mensurado; `40+ ms` já é deliberadamente grande | O motor deixa de soar tensionado e começa a soar atrasado/descoordenado |
| **MÉDIO-ALTO** | "Corrigir" mix fechada adicionando 2–4 kHz indiscriminadamente | Presença atual `0,64` > ref `0,51` | Aumenta o que já está excessivo sem fechar a falta real de 8k+ |
| **MÉDIO-ALTO** | Shelf global de +5/+7 dB para igualar 8 kHz+ | A lacuna medida é `5–7 dB`, mas **não deve virar ganho de shelf equivalente** | 4–10 kHz é zona sensível de aspereza; um número espectral correto pode produzir um timbre pior. |
| **MÉDIO** | Grave estéreo não controlado | ≤`120 Hz` deve ser mono; reprovar resultado com correlação significativamente abaixo de `~0,98` nessa banda | Muda peso entre mono/stereo e entre sistemas |
| **MÉDIO** | Limiter trabalhar como envelope rítmico involuntário | Se a redução reaparece ~a cada kick/16º e crest dos drops cai abaixo de `6 dB`, investigar | O kick deixa de comandar a dinâmica; o limiter passa a comandá-la |
| **MÉDIO** | Trigger sidechain multiplicado por cópias sobrepostas sem validação | 8 eventos simultâneos coerentes poderiam teoricamente somar até ~`+18 dB` antes de qualquer limitação/retrigger | Pode alterar thresholds dos duckers de forma invisível e tornar calibração dependente de acidente estrutural. **Medir o trigger com 1 cópia vs N cópias antes de qualquer decisão.** |
| **BAIXO/MANUTENÇÃO** | Automação em device desligado / lanes órfãs | Não existe limiar sonoro se o device realmente está off | Aumenta complexidade e risco de futura ativação acidental |
| **TOLERÁVEL** | Não usar sidechain nos graves | `0 dB GR` é permitido se a separação física funcionar | Sidechain é meio, não resultado |
| **TOLERÁVEL** | Kick na intro | bar 1 / `0:00` | É decisão formal, não erro de gênero |
| **TOLERÁVEL** | Pump de rolling OFF | decisão explícita | Não há evidência de que pump seja necessário |

### O maior veto conceitual

O erro mais provável neste estágio seria:

> **"A faixa está fechada; então vamos adicionar mais hats, abrir 2–4 kHz e dar +6 dB de shelf no ar."**

Os números do caso apontam na direção oposta. Ele já tem:

- **densidade demais:** `7,57 > 6,99/s`;
- **presença demais:** `0,64 > 0,51`;
- **mas energia 8 kHz+ de menos:** `−27,1` vs `−20…−22`.

Logo o problema não é simplesmente **quantidade de agudo**. É **onde os poucos transientes fortes estão espectralmente, temporalmente e espacialmente posicionados**.

A solução de menor risco é: **menos eventos concorrentes, mais contraste nos eventos que sobreviverem, e abertura acima da presença já carregada**. Isso é consistente com a atenção que Zenon dá a envelopes, diálogo/repetição e arranjo de percussão, em vez de recomendar paredes contínuas de high-frequency material.

## Parte C — O que há EM COMUM na cena

Zenon ainda descreve oficialmente seu som como minimal/electronica profunda, musical e com design sonoro futurista; AlpaKa, em lançamentos de 2026, descreve bushtech como **chunky basslines + heavy rolling grooves + psychedelic textures**, e psytech atual como **hypnotic grooves + rolling basslines + driving percussion**. Isso é uma convergência estética forte entre fontes primárias da cena.

### Denominador comum versus assinatura

| Aspecto | Denominador comum | Variação aceitável | Classe |
|---|---|---|---|
| **Low-end central** | Kick+baixo são tratados como uma relação única que precisa de coerência temporal/espectral | Mais kick-led, mais sub-led, rolling mais curto ou mais sustentado | **Consenso técnico + estética** |
| **Rolling/hypnose** | Repetição forte com pequenas mudanças | 16º contínuo, padrões quebrados, ghost events, acentos de velocity | **Estética de cena** |
| **Kick×bass** | Fase/articulação importam mais que receita de plugin | Arranjo, envelope, volume-shaper, compressor, gate ou combinação | **Consenso técnico** |
| **Percussão** | É fonte de groove e diálogo, não apenas preenchimento de espectro | Metálica, orgânica, glitch, wood, hats muito secos ou mais espaciais | **Cena**; Zenon ensina repetição, diálogo e polirritmia. |
| **Negative space** | Contraste por ausência é extremamente compatível | Intro sem kick, breaks zerados, retirada apenas do sub, top surviving, etc. | **Assinatura formal**, não lei |
| **Médio escuro** | Não há obrigação de parede brilhante tipo full-on clássico | Artistas variam bastante no topo/textura | **Estética** |
| **Sub mono / textura larga** | Centro robusto embaixo, liberdade crescente em cima | crossover exato varia | **Engenharia + estética** |
| **Duração longa** | Desenvolvimento em ciclos, não "song form" pop | 6–9 min é comum no ecossistema; Hourglass 8:35, remixes 7–9:34 | **Cena atual** |
| **128 BPM** | Continua plenamente dentro da família atual | 126–132 e extensões maiores aparecem | **Cena atual** |

### Onde os quatro ramos se separam

| Família | O centro de gravidade estético | O que costuma distinguir |
|---|---|---|
| **Minimal psytech** | Techno primeiro, psicodelia por textura/microvariação | Menos eventos simultâneos, kick firme, arranjo econômico, tensão pela repetição |
| **Dark Zenon / zenonesque** | Psicodelia profunda + programação detalhada | Baixo articulado, timbres orgânicos/futuristas, ritmos menos óbvios, diálogos e polirritmia. A descrição oficial da Zenon enfatiza profundidade/minimalismo e design futurista. |
| **Bush tech** | Groove físico/orgânico e sensação "dusty" | AlpaKa 2026 usa explicitamente "chunky basslines" e "heavy rolling grooves"; matéria orgânica e pressão mais corpórea. |
| **Dark progressive** | Jornada e desenvolvimento gradual | Rolling mais lento, atmosfera, glitch/detalhe, menos dependência de ataque peak-time. O Hourglass EP descreve um remix dark progressive como glitch-heavy, detalhado e de "controlled chaos". |

**Consenso técnico:** alinhamento/overlap de kick e baixo; envelopes e articulação; prevenção de mascaramento; controle do low-end; headroom/true peak apropriado ao destino; medir o resultado, não o nome do plugin.

**Opinião/assinatura estética:** kick desde o compasso 1 ou não; quantos compassos sem bateria; quantidade de swing; quanto glitch; quanto wood; se a reentrada é explosiva ou incompleta; se o bass é predominantemente 16º ou cria vazios.

Isso é relevante porque três decisões comuns que parecem "estranhas" são, na verdade, **boas candidatas a assinatura**:

**kick desde o bar 1 / 0:00**, **breakdown totalmente sem bateria de ~45 s**, e **vácuos de cama de sub de dois tempos**. Não se normaliza nenhuma delas para imitar a Slippery Slope.

## Parte D — As verificações mais caras (metodologia de fechamento)

| Prioridade | Verificação | Por que custa caro | Como fechar objetivamente |
|---|---|---|---|
| **1** | **Topo baixo + presença já alta** | A correção intuitiva pode piorar o mix: faltam ~`6,3 dB` em 8k+, mas 2–4k já está ~25% acima da régua de presença | Renderizar **bateria, hats/shaker e full** separadamente; medir 1.5–3k / 3–6k / 6–8k / 8–12k / 12k+ por seção. A meta não é +6 dB de EQ; é aproximar 8k+ de `−22…−20` mantendo presença ≤`~0,51` |
| **2** | **Densidade 7,57/s** | Não há espaço para simplesmente adicionar mais top; o mesmo bloco precisa ficar **mais brilhante e menos cheio** | Medir onsets separadamente por seção (drop 1, pico, drop 2). Meta: fortes `6,0–6,8/s`, global/drop ≤`~6,99/s` |
| **3** | **55–75 excessivo vs 40–55** | Pode manter a sensação de low-end "cheio para dentro" mesmo com o sub de fundamento corrigido | Acrescentar banda `75–100 Hz` e stems dos graves separados. Primeiro alvo: trazer `(55–75)-(40–55)` de `+4,0` para **≤+1,5 dB** sem perder `sub−kick ≈−3…0 dB` |
| **4** | **Separação kick×bass ainda não provada** | Uma arquitetura elegante pode estar acusticamente errada; esse é o risco de PA mais caro | Exportar kick + cada grave. Medir envelope/energia em janelas `0–30`, `30–60`, `60–90`, `90–117 ms` após cada kick; conferir polaridade e perda no mono-sum. Também resolver a unidade de qualquer duração de nota sem unidade declarada |
| **5** | **Master de streaming a −0,6 dBTP** | Está tecnicamente acima da recomendação oficial para master com −10,2 LUFS | Testar versão com **≤−2,0 dBTP**, loudness-matched contra a atual. Beatport não exige LUFS −8/−6; não comprimir mais só para "recuperar" o volume. |

**Uma medição adicional vale especialmente a pena:** medir o nível real do trigger do sidechain com **1 cópia versus 8 cópias**. Oito sinais idênticos somados linearmente poderiam, no limite teórico, produzir cerca de **+18 dB**; porém retrigger, voice handling e o ponto exato da rota podem impedir isso. Hoje o problema estrutural é verificável; o aumento de nível é apenas hipótese até medir.

## Parte E — Ideias (experimentos candidatos, não instrução)

As ideias abaixo **não são instrução para alterar um projeto**. São experimentos com critério explícito de aceitação.

### Ideias que mudam a música

| Ideia | Intenção | Como fazer com o que existe | Como provar |
|---|---|---|---|
| **Drop 2 em duas resoluções** | Fazer a reentrada parecer maior sem adicionar elementos | No primeiro tempo do drop 2, devolver kick + fundamento/rolling; fazer open hat/shaker responder só depois, ou no último 16º antes do próximo tempo | A/B nivelado: o drop precisa manter impacto de grave, mas a densidade no primeiro segundo cair e o pico de 8k+ aparecer **depois** do low-end |
| **Transformar os vácuos da cama de sub em eventos formais** | Fazer a ausência do sub "falar", em vez de parecer apenas mute | Nos dois tempos vazios já consagrados, não recolocar grave: permitir **uma única resposta seca** de wood/hat/glitch no último 16º | O sub continua em zero nos vácuos; onset total não cresce acima do gate; ouvintes A/B devem localizar a pergunta/resposta sem conhecer o arranjo |
| **Outro por erosão vertical** | Fazer o motor parecer inevitável enquanto a superfície desaparece | Retirar primeiro open hat/shaker/closed hat em etapas, mantendo kick/rolling/sub por mais um ciclo; só depois desmontar o centro | Curva 8k+ deve cair antes de 25–75 Hz; o bloco deve continuar DJ-mixable. É a mesma lógica estrutural observada na Slippery, não cópia de timbre |

A terceira ideia tem aderência forte ao gênero porque lançamentos atuais de AlpaKa continuam enfatizando rolling basslines, grooves hipnóticos e driving percussion como componentes que podem ser manipulados independentemente na forma.

### Ideias com canais e patches existentes

| Ideia | Intenção | Como fazer | Como provar |
|---|---|---|---|
| **Open hat e shaker como uma só voz distribuída** | Abrir o topo sem duplicar densidade | Onde o open hat dispara forte, reduzir/omitir um shaker próximo; onde ele cala, deixar o shaker assumir. Usar AutoPan/Haas apenas no topo | Onsets/s devem **cair ou permanecer iguais**, 8k+ subir `2–3 dB` no primeiro teste, presença 2–4k não subir |
| **Hat-esteira quase inativo como exceção, não cama** | Ganhar um "flash" de ar sem criar hiss permanente | Usar o canal quase inativo em poucas janelas de 1–2 barras perto de transições; nada de esteira contínua | 8k+ melhora localmente; média global de densidade não passa de `6,99/s`; espectro 6–12k não vira plateau contínuo |

### Ideias de diálogo

**Kick ↔ sub — "pergunta no 1, resposta no último 16º".**
**Intenção:** reforçar o padrão de dois polos já encontrado na Slippery sem virar cópia.
**Como:** preservar o kick limpo no primeiro tempo e escolher, em ciclos específicos, uma resposta do rolling no último 16º anterior ao pulso seguinte; nunca adicionar os dois se já houver evento equivalente.
**Prova:** histograma de fase dos onsets deve ganhar concentração nesses dois polos **sem aumentar o total de onsets**. A Zenon Education trata explicitamente repetição e diálogo como mecanismos de groove.

**Closed hat ↔ shaker — "um ocupa o centro temporal, o outro a borda".**
**Intenção:** tornar o groove mais tridimensional e menos simultâneo.
**Como:** closed hat fica com eventos mais precisos/centrados; shaker usa os desvios existentes de AutoPan/Haas e atrasos intencionais de **5–15 ms**, não randomização de 20–40 ms.
**Prova:** correlação acima de 1–2 kHz deve cair, enquanto low-end segue mono e o timing do kick não muda. A faixa 5–15 ms está abaixo ou próxima do JND médio de ~19–24 ms medido para drums, portanto tende a ser percebida mais como sensação do que como atraso explícito.

### Ideias específicas para o topo/ar

**Redistribuição espectral, não "mais hats".**
**Intenção:** transformar o mesmo orçamento de transientes em mais 8 kHz+ e menos 2–4 kHz.
**Como:** identificar qual elemento entrega mais `8–12 kHz / 2–4 kHz`; privilegiá-lo nos eventos já existentes e reduzir o elemento que produz muito 1,5–4 kHz nos mesmos instantes.
**Prova:** primeira meta experimental: 8k+ de `−27,1` para aproximadamente **`−24…−23 dB`**, presença de `0,64` para **≤0,58**, com densidade **não aumentando**. Se funcionar, só então buscar o envelope das refs `−22…−20`. Isso evita atravessar de uma vez a zona 4–10 kHz associada à aspereza.

**Abrir horizontalmente o que já é agudo.**
**Intenção:** aumentar sensação de abertura sem mexer no centro grave.
**Como:** explorar AutoPan do open hat/closed hat e Haas ~8% já existente no shaker, restringindo qualquer ampliação a material acima do low-mid; **não tocar na régua mono ≤120 Hz**.
**Prova:** correlação da banda superior deve cair, enquanto correlação <120 Hz permanece ≈`1,0`; 8k+ pode permanecer igual e ainda assim a percepção espacial melhorar. Se o ganho só aparece porque houve aumento de RMS, o teste falhou.

### Anti-obviedades

**Abrir a faixa escurecendo antes do Drop 2.**
**Intenção:** produzir mais contraste de brilho sem elevar o brilho absoluto da faixa inteira.
**Como:** nos bars finais que precedem o silêncio total do breakdown, reduzir progressivamente os poucos tops que ainda estiverem ativos; no drop 2 volta ao nível atual.
**Prova:** o render do drop 2 não precisa ganhar nenhum dB em 8k+; ainda assim, o salto pré-drop→drop deve aumentar. Se o A/B isolado do drop continua idêntico, mas no contexto ele parece "abrir", a ideia funcionou.

**Para soar mais aberto, primeiro retirar presença.**
**Intenção:** resolver o paradoxo `presença 0,64` + `8k+ −27,1`.
**Como:** antes de qualquer shelf, fazer um teste que reduza **~1–2 dB** apenas no material que domina `2–4 kHz` e preserve/realoque transientes `6–10 kHz`.
**Prova:** presença deve cair em direção a `0,51–0,56`; 8k+ deve subir relativamente ou permanecer estável; A/B nivelado precisa soar menos "pra dentro" sem mais hiss. Essa proposta é deliberadamente contraintuitiva: a faixa pode precisar de **menos médio-agudo para o agudo que já existe ter espaço**, não de mais energia total.

A tese criativa resultante é simples:

> **A faixa não precisa ficar "mais cheia". Precisa ficar mais hierárquica.**
> O low-end já tem peso; o próximo salto de qualidade vem de **menos concorrência temporal + melhor distribuição espectral + contraste formal mais explícito**.

## Fontes e evidência

A pesquisa externa privilegiou **fontes primárias da cena**, documentação/fabricantes e material recente de engenharia. Quando uma fonte é apenas uma heurística de produção, ela está marcada como tal e **não foi promovida a consenso**.

| Fonte | Tipo | Evidência literal curta | URL |
|---|---|---|---|
| **Zenon Records — site oficial, consultado 2026** | Cena / estética primária | "deep and intelligent minimal/electronica … musicality and futuristic sound design" | `https://www.zenonrecords.com/releases` |
| **Zenon Education — Music Production Suite** | Cena / ensino primário | "Phase … and its importance in the Kick and Bass relationship." | `https://www.zenon-education.com/zenon-records-music-production-suite` |
| **Zenon Education — Perc + Drums** | Cena / ensino primário | "repetition and dialogue in order to add catchy rhythms" | `https://www.zenon-education.com/zenon-records-music-production-suite` |
| **AlpaKa MuziK — NVU Hourglass EP, agosto de 2026** | Cena / bushtech primário | "chunky basslines, heavy rolling grooves and twisted psychedelic textures" | `https://alpakamuzik.bandcamp.com/album/nvu-hourglass-ep` |
| **AlpaKa MuziK — Into The Dark EP, junho de 2026** | Cena / psytech primário | "hypnotic grooves, rolling basslines, and haunting atmospheres" | `https://alpakamuzik.bandcamp.com/album/into-the-dark-ep` |
| **Beatport — Luis M, 2026** | Metadados atuais da cena | `Singularity` / `Primordial`: "Psy-Techno 128 BPM - Db Major" | `https://www.beatport.com/artist/luis-m/137444/tracks` |
| **iZotope — Mixing Low End, maio de 2025** | Engenharia | "20 Hz–160 Hz typically hosts the most energy" em fontes low-end-centric. | `https://www.izotope.com/community/blog/7-tips-for-mixing-the-low-end` |
| **iZotope — Mastering Low End, setembro de 2025** | Engenharia | "bass fundamentals – often down between 40 and 80 Hz" | `https://www.izotope.com/community/blog/mastering-low-end` |
| **FabFilter — Side-chain Compression** | DSP / fabricante | "Bass sounds … are particularly prone to this" ao usar compressão rápida que acompanha ciclos da onda. | `https://www.fabfilter.com/learn/compression/side-chain-compression` |
| **Sciety / Câmara et al., versão 2025** | Pesquisa perceptual recente | "Kick, Snare, and Hi-hat yielded the lowest JNDs (≈19–24ms)" | `https://sciety.org/articles/activity/10.31234/osf.io/jsg94_v3` |
| **iZotope — De-essing, 2025** | Engenharia | "harsh frequencies typically happen anywhere between 4 and 10 kHz" | `https://www.izotope.com/community/blog/the-dos-and-donts-of-de-essing` |
| **iZotope — Mastering Trends 2024** | Benchmark amplo, não psytech | "50% of the songs exhibit an LRA between 3.7 and 6.8 LU" | `https://www.izotope.com/community/blog/mastering-trends` |
| **Spotify for Artists — Loudness Normalization, vigente em 2026** | Entrega / codec | "If your master is louder than -14dB … keep True Peak below -2dB" | `https://support.spotify.com/tl-pt/artists/article/loudness-normalization/` |
| **Beatport Support — atualizado em 2026** | Entrega / loja | "We do not normalize, re-master or engineer our files in any way." | `https://support.beatport.com/hc/en-us/articles/4412309674260-What-should-I-do-if-I-have-a-problem-with-a-track-that-I-purchased` |
| **Myloops — Kick/Bass 2026** | **Heurística secundária**, não norma Zenon | "decay around 60–90 ms … release 20–40 ms" | `https://www.myloops.net/how-to-make-psytrance-kick-and-bass-work-together` |

**O que a pesquisa confirma das régua internas do caso:** `128 BPM`, low-end central/mono, LRA `5,6`, uso forte de negative space e a preocupação com phase/articulation estão coerentes com a cena e com engenharia moderna. A meta de densidade `≤6,99/s`, as relações de bandas e o centroide `266–287` são **boas régua internas porque vêm do corpus medido**, mas não devem ser apresentadas como padrões universais publicados.

**O que a pesquisa contesta:** `Beatport −8…−6 LUFS` não é especificação oficial; `−14 LUFS` é referência de normalização do Spotify, não obrigação artística de master; `−0,5…−1,2 dBTP` não é seguro como gate universal de streaming para um master de `−10,2 LUFS`, pois o Spotify hoje recomenda **<−2 dBTP** nessa condição.

**O que permanece não comprovado e vale medir antes de qualquer decisão:** duração real de notas sem unidade declarada; cauda do kick em ms; overlap/phase kick×cada grave; correlação renderizada <120 Hz; banda `75–100 Hz`; crest factor por drop; densidade por seção; contribuição de cada canal para 2–4/4–8/8–12/12k+; efeito real das cópias sobrepostas do trigger de sidechain; e resposta de fase de cadeias redundantes.

**Internet consultada:** sim. As conclusões externas se apoiam principalmente em **Zenon Records/Zenon Education, AlpaKa MuziK, Beatport, Spotify for Artists, FabFilter, iZotope e pesquisa perceptual de 2025**. Os números específicos do caso e de Slippery/Kaled/Gazolla/ISMAIL foram tratados como **medições fornecidas pelo projeto de origem**, não como dados inventados ou extrapolados da web.
