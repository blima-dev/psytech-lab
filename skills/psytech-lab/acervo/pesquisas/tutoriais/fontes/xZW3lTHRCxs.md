# 5 Tips for the Perfect Fitting Techno Kick Drum

> **Fonte:** legenda automática em inglês do vídeo (VTT, 62,4 KiB; 1576 linhas; vídeo ~9:26).
> Canal: SINEE Global · Frente: pressao-grave · Prioridade: P1.
> Apresentador: "I'm Le." `[00:00.160]`. Demo com stock devices da Ableton; nenhum plugin de terceiros aparece na legenda (Roar é device do Live — INFERÊNCIA a partir de "stock plugin... from Ableton" `[04:36.150]`).

## Técnica ensinada (2-4 frases)

O vídeo ensina um checklist de cinco passos para encaixar um kick de techno no projeto: (1) afinar o kick numa nota correlata ao sub — no caso, sub em C# e kick buscado em G# `[00:47.830]` `[01:02.640]`; (2) encurtar a cauda quando existe um sub grande, porque um kick "short and snappy" perfura melhor e não mascara o grave `[01:57.759]` — com a ressalva de que, sem tanto sub, "a longer tailed kick drum is great... especially if you go for the samples in the style of 808" `[02:57.910]`; (3) fazer EQ **só subtrativo**, antes da distorção, para não realçar faixas indesejadas `[03:20.790]` `[03:38.470]`; (4) distorcer em multibanda com o grave "soft and clean" e o mid/high no tube, usando Roar e o preset "drum second opinion" `[04:36.150]` `[04:51.680]`; (5) comprimir com ratio 4:1, attack de 100 ms e release mínimo, ajustando o threshold de ouvido e refazendo o gain staging `[05:51.759]` `[06:03.199]`. O bônus é explícito: se o kick não está punchy, não está passando na mix ou não está conduzindo a faixa, volte à fonte, troque o sample e afine até sentar `[08:29.120]` `[08:53.120]`.

**Nota de legenda:** no trecho da correlação a legenda erra ("Five semmitones apart which is this case or seven semmitones apart or one semmitone apart" `[01:34.310]`); o alvo concreto declarado é G# com sub em C# `[00:47.830]` `[01:02.640]`, que é a quinta abaixo (G#0 ≈ 52,41 Hz). Registra-se a coincidência com a prática comum de tuning kick/sub, sem corrigir a fala.

## Ferramenta usada no vídeo (plugin/stock)

- **Ableton Live stock, sem terceiros.** O vídeo nomeia o Roar como "the stock plugin called Roar from Ableton" `[04:36.150]` e o preset "drum second opinion" `[04:40.150]`; a legenda também cita "the tuner" `[02:15.599]`, "an EQ" `[03:27.840]`, "compressor" `[05:49.919]`, "a gate gain staging utility" `[03:54.959]` e "the filter... on our sample" `[05:22.639]`.
- **Roar (multibanda):** "This one has low, mid, and high. It's a multiband distortion." `[04:45.040]`; "Set the tube setting here on high and mid. Uh the low is soft and clean." `[04:48.080]` `[04:51.680]`; e "make sure to get some low punch through" `[04:58.320]`.
- **Compressor:** "This one has a 4.00 ratio." `[05:51.759]`; "an attack of 100 milliseconds to make sure that a lot of our punch from the kick comes through." `[05:55.120]`; "The release is set to the shortest amount possible..." `[06:03.199]`; threshold ajustado de ouvido `[06:11.830]` `[06:42.819]`.
- **Tuner:** usado para achar G# `[01:02.640]`; depois removido da cadeia `[02:15.599]`.
- **EQ:** não nomeado; a legenda só diz "an EQ" `[03:27.840]`. Provável EQ Eight do Live (INFERÊNCIA), mas não confirmado.
- **Sample:** kick 909 `[00:38.000]`, fora do tom (o 909 costuma vir em G por padrão `[00:51.190]`); sub do projeto em C# `[00:47.830]`.
- **Não aparecem na legenda:** ANA 2, VELA, SideKick, Kick 3, Bitwig, Serum, Diva, Vital, Massive X, Surge XT, Kontakt (busca textual sem ocorrência). Nada a traduzir desses.

## Tradução para ferramentas comuns: Live 12 nativo, Serum 2, Diva, Vital, Massive X, Surge XT, Kontakt 8

**Rota direta — Live 12 nativo (quase 1:1):**
`Tuner → Simpler/Sampler (sample 909) → EQ Eight (subtrativo) → Roar (multibanda, grave limpo) → Compressor (opcional) → Utility (gain staging)`.
O vídeo usa exatamente essa arquitetura de stock. **Roar é stock do Live 12** (o vídeo o chama de stock da Ableton `[04:36.150]`); se a edição não o tiver, o fallback é **Saturator** (drive baixo, HQ) + **EQ Eight** dividindo as bandas, ou o drive do **Drum Buss** — mais trabalho, mesmo conceito. O **Tuner** do Live confere a fundamental; o **Simpler** encurta a cauda no envelope ou no fim do sample; o **Sampler** idem com mais controle. Um **Drum Buss** no fim da cadeia (damping no topo) é opcional para conter brilho — não vem do vídeo.

**Serum 2:** não é necessário para o kick; o vídeo parte de um sample 909, e o caminho mais curto é Simpler/Sampler. Se quisermos o kick dentro do Serum 2, o **SampleOsc** (`sample_playback_source`) toca o one-shot e pitch/octave/fine ajustam a nota; o **GranularOsc** não tem função aqui (o vídeo não é granular — não force). Diva, Vital, Massive X e Surge XT não são usados pelo vídeo; servem para sub/rolling/stab, e a única lição transferível é afinar a fundamental contra a nota do sub (ver aplicação). Kontakt 8 não é rota para kick. **Grain, Operator, Echo e Hybrid Reverb** também não aparecem na técnica: o vídeo é um one-shot de kick processado por EQ, distorção e compressor; forçá-los só adicionaria cauda/brilho ao kick.

**O que não temos no vídeo:** ANA 2, VELA, SideKick, Kick 3, Bitwig. O vídeo não usa nenhum deles, então não há conceito equivalente a improvisar — a tradução é stock do Live.

**O que não usar (adaptando ao estilo psytech):** o **click do filtro** do passo 4 `[05:20.790]` é um estalo de Tech House — em um projeto que exige kick sem estalo agudo, vetar. O **corte amplo de mids** do passo 3 também é condicional: o vídeo chama o kick de "a little bit woody, a little bit too much mids" `[04:19.199]`, mas em um projeto em que madeira é elemento de identidade o corte não se transfere. E nada de **AutoPan/Shifter/alargamento** no kick ou sub — low-end mono (<150 Hz) é prática padrão.

**O que é novo vs. o que é prática comum:**
- **Prática comum (confirmação, não novidade):** tuning kick = quinta da nota do sub (ex.: G#0 ≈ 52,41 Hz sobre sub em C#); kick curto/aveludado com sub grande; low-end mono.
- **Novo/adaptável:** EQ subtrativo antes da distorção `[03:38.470]`; Roar multibanda com low clean `[04:51.680]`; compressor 4:1 / 100 ms / release mínimo `[05:51.759]` `[06:03.199]`; gain staging sem clip `[07:06.720]`.
- **Vetado (para o estilo):** click de filtro `[05:20.790]`.
- **Invertido (condicional):** o corte de "a little bit woody, a little bit too much mids" `[04:19.199]` — se a madeira for identidade do projeto, é identidade, não defeito.

## Aplicação por função (kick, sub, baixo/rolling, hats/shaker, percussão de resposta, madeira, stab, subida, atmosfera)

| Função | O que o vídeo oferece | Como aplicar (e o que evitar) |
|---|---|---|
| **Kick** | Tuning contra o sub `[00:47.830]`; cauda curta com sub grande `[01:57.759]`; EQ subtrativo antes da distorção `[03:38.470]`; Roar multibanda com grave limpo `[04:51.680]`; compressão 4:1/100 ms/release mínimo `[05:51.759]` `[06:03.199]`; gain staging `[07:06.720]` | **Aplicar:** afinar a fundamental contra a nota do sub (ex.: quinta — G# ≈ 52,41 Hz sob sub em C#); EQ Eight só cortando, Q alto, antes do Roar; Roar com low "soft and clean" e tube **só no mid** (o vídeo usa high+mid `[04:48.080]`, mas o high é o risco de brilho metálico); compressor opcional com A/B de ouvido. **Evitar:** click de filtro `[05:20.790]`; acumular energia em 55–75 Hz (engorda o sub); corte amplo de "woody mids" se madeira é identidade; estéreo no kick. |
| **Sub** | Nenhuma lição direta de design; a lição é de divisão de trabalho: "If you have a big sub... short and snappy kick" `[01:57.759]` | Manter o sub mono; não passar o sub pelo high band do Roar; não alargar. A cauda curta do kick é o que dá espaço ao sub — não compensar engordando o kick em 55–75 Hz. |
| **Baixo / rolling** | O **princípio** multibanda (grave limpo, mid/high com tube) `[04:45.040]` `[04:51.680]` e o EQ antes da distorção `[03:38.470]` | **Melhor uso novo do vídeo (INFERÊNCIA):** Roar no rolling com **low clean** (protege o sub), **tube no mid** para preencher o corpo de médio e **high contido** para não criar brilho metálico. EQ Eight antes do Roar. Compressão de release rápido é opcional; preservar os bolsos e offsets do groove — não mover onset. |
| **Hats / shaker** | Não coberto | **Não aplicar** Roar/multibanda: o "bite and grit" `[05:14.960]` vira brilho metálico no topo. Só valem o gain staging sem clip `[07:06.720]` e o princípio de EQ subtrativo antes de qualquer saturação `[03:38.470]`. |
| **Percussão de resposta** | O tuning por correlação `[01:29.840]` `[01:34.310]`, se a percussão for tonal | **Transferência leve (INFERÊNCIA):** afinar a fundamental da madeira/percussão para a tônica/quinta do projeto; manter o hit curto para responder sem mascarar o kick; EQ subtrativo. Não adicionar click. |
| **Madeira** | O vídeo corta "a little bit woody, a little bit too much mids" do kick `[04:19.199]` | **Inverter a lição quando a madeira é identidade:** não cortar o mid da madeira; se saturar, EQ antes da distorção para não realçar ressonâncias `[03:38.470]`. |
| **Stab** | EQ antes da distorção `[03:38.470]` e gain staging `[07:06.720]` | Aplicar só se o stab for distorcido; sem tube no high (metal). Não usar o tuning do kick no stab. |
| **Subida** | Não coberto | Só gain staging/no red `[07:06.720]`. Não aplicar click/distorção do kick; a subida é transição. |
| **Atmosfera** | Não coberto | Sem aplicação. Não rodar a cadeia do kick na atmosfera. |

**Regra de segurança contra engordar o sub e contra brilho metálico:** o low band do Roar fica "soft and clean" `[04:51.680]`; o tube vai para o mid, nunca para o high do kick; o click de filtro `[05:20.790]` fica de fora em estilos que rejeitam estalo; a compressão não pode achatar a dinâmica de velocity nem deslocar os offsets do groove. Evitar EQ em modo linear-phase no kick (o pré-ringing pode borrar o transiente — INFERÊNCIA, não é fala do vídeo).

**Por que serve a um projeto psytech:** o vídeo não é uma receita de timbre para copiar; é um procedimento de encaixe. O que acrescenta é a ordem (EQ antes da distorção) e a disciplina do grave limpo, que permitem usar o Roar no **mid do rolling** para preencher o corpo de médio sem tocar no sub mono nem no kick aveludado.

## Prioridade e esforço

- **Prioridade: alta (P1).** É o encaixe do kick, coração da pressão de grave; duas das cinco dicas confirmam práticas comuns (tuning da quinta e cauda curta), e a transferência do multibanda para o rolling preenche o corpo de médio sem boost no sub.
- **Esforço: médio.** Tudo stock (Tuner, EQ Eight, Roar, Compressor, Utility), uma sessão de A/B; o custo real é ouvido (threshold, tuning, checar o bolso), não plugin.
- **Risco: médio.** Três armadilhas: (a) o click do filtro pode ser proibido pelo estilo; (b) o corte de mids do vídeo piora o corpo se madeira é identidade; (c) compressão/ganho podem achatar a velocity e o groove. Mitigação: A/B bypass, medir o médio antes/depois, não tocar no timing.

## Trechos de prova

1. `[00:17.520–00:26.080]` **"Finding out what tune you need for your kick is essential, I would say, and it makes sure that everything yells together."**
2. `[00:01:57.759–00:02:07.520]` **"If you have a big sub and so on, you would like to have kind of a short and snappy kick drum to make sure that it punches through, right? You don't want to have a longtailed kick drum."**
3. `[00:03:38.470–00:03:44.550]` **"So, we want to EQ as much as possible before the distortion to make sure that we don't enhance any frequency ranges that we don't desire."**
