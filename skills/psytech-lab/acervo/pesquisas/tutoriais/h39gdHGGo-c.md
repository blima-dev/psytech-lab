# Use This Instead Of Rumble - Create Techno Subs With Noises

**Canal:** SINEE Global · **ID:** `h39gdHGGo-c` · **Duração:** 404 s (6:44) · **Tema:** pressão de grave.
**Fonte:** legenda automática em inglês, obtida via yt-dlp (legenda completa — última marcação 00:06:43.800). **`temLegenda = true`.** Todos os timestamps abaixo vêm desse arquivo. Descrição do vídeo também lida (`yt-dlp --print "%(description)s"`). **Áudio não escutado.**

## Técnica ensinada (2-4 frases)

Em vez de fazer o rumble do jeito padrão — kick encharcado de reverb e delay com sidechain por cima —, o vídeo usa **fontes abstratas de ruído** como matéria-prima do grave: loops de noise ou field recordings já muito processados, distorcidos e "mangled", que naturalmente **não têm grave nenhum**. Esses loops entram num **frequency shifter** (Shifter do Ableton, modo de deslocamento de frequência) que empurra o conteúdo do ruído para baixo, criando material novo na região do baixo para ser moldado; sem filtro depois disso, segundo o autor, aquilo não é rumble. Os loops são cortados e têm o **envelope de volume desenhado espelhando o envelope do kick**, para que as duas coisas não se atrapalhem, e o resultado é filtrado e sidechainado ao kick original. O motivo declarado para escolher esse método é controle: com camadas de ruído posicionadas à mão você manda no groove, coisa que reverb e delay tradicionais borram.

## Ferramenta usada no vídeo (plugin/stock)

**Tudo stock do Ableton Live.** O vídeo não usa nenhum plugin de terceiro na demonstração:

| Ferramenta | Trecho literal | Timestamp |
|---|---|---|
| Ableton **Shifter** (deslocamento de frequência) | "that is where ableton's shifter comes into play." | 00:02:21.0–00:02:26.0 |
| Filter (tipo não nomeado em voz alta) | "that's not really a rumble when there's no filter engaged - I engage a filter." | 00:03:52.1–00:03:56.8 |
| Delay + Saturator + Overdrive | "You can hear a little bit of delay going on this saturator... ...overdrive and of course everything is filtered down" | 00:04:29.8–00:04:39.3 |
| Sidechain ao kick original | "...and side chains to the original Kick Drum." | 00:04:35.7–00:04:39.3 |
| **Echo** no grupo inteiro | "I also used an Echo device on the complete group. Just to add another level of Timbre shaping and movement." | 00:05:24.1–00:05:35.2 |

**Fonte de material (não é plugin):** o sample pack **"Schmutz"** — "So today I'm gonna use this sample pack. It's called Schmutz, which in German just means dirt." (00:01:25.9–00:01:32.4). O autor explica por que esse pack: "there is a ton of sampled noises in there noise... loops" (00:01:44.2–00:01:51.9). É pack pago do próprio canal.

**Atenção — a descrição engana:** ela anuncia "Kikzilla Rumble Generator" e "Chop Suey Kick Drum Designer". São **links de propaganda**; os dois plugins **não aparecem na técnica ensinada** e não são citados na legenda. Não confundir com o método.

## Tradução (Live 12 nativo / Serum 2)

**O vídeo não depende de nada além do Live stock.** O device central — Shifter — é nativo do Live. Não há lacuna de equipamento aqui; há uma lacuna de **disciplina de banda**, explicada na seção de aplicação.

### Mapa gesto → ferramenta

| Gesto no vídeo | Equivalente | Fidelidade |
|---|---|---|
| Fonte = noise loop / field recording já destruído | Qualquer noise loop denso e sujo do acervo próprio, ou **Serum 2 Noise osc** (Pink / Brown — mais grave que white) para não depender de pack | direta em função; o pack "Schmutz" é do canal e substituível |
| **Shifter** em modo de deslocamento de frequência | **Live 12 → Shifter**, modo Frequency Shifter (é literalmente o mesmo device) | direta |
| Alternativa fora do Live | Serum 2 **SpectralOsc** com warp em modo **Spectral Shift** (ou Spectral Pitch Shift) — deslocamento no domínio espectral | conceito equivalente; comportamento sonoro não testado em áudio nesta sessão |
| Cortar os loops e desenhar o envelope espelhando o kick | Simpler/Sampler + **envelope de volume do clipe** no Arrangement (desenho por golpe); ou, no Serum 2, envelope com decay curto e sustain 0 roteado ao volume + notas MIDI só nos pontos desejados | direta |
| Filtro obrigatório depois do shifter | Auto Filter / EQ Eight no Live, ou low-pass 24 dB/oct no Serum 2 | direta |
| Vários canais com noises diferentes em posições diferentes | **Uma track por camada** dentro do grupo do grave, eventos posicionados à mão | direta |
| "extra filtered kick drum sounds" para groove | Cópia filtrada do kick no Simpler, ou um kick curto de biblioteca passado por LP | direta |
| Delay + Saturator + Overdrive, tudo filtrado e sidechainado | Saturator (Drive/Soft Clip) + Delay curto; sidechain = **Compressor nativo** com key do kick | direta |
| **Echo no grupo inteiro** | Echo nativo — **mas só com guarda** (ver freios): prática conservadora evita wet de delay/reverb no núcleo do grave | parcial, com restrição declarada |
| Pack "Schmutz" | Não incluído. É só a **fonte**, não o método — substituível | ausente, contornável |

### Receita-base no Serum 2 (proposta; **o vídeo não dá nenhum número**)

1. **Fonte:** oscilador Noise (Pink ou Brown — mais grave que white), OU spectral source apontando para um noise `.wav`.
2. **Deslocar para baixo:** warp em modo **Spectral Shift** com amount a gosto. **Este é o ponto que o vídeo deixa sem número** — no Live, o Shifter mostra o valor na tela, mas ele não é dito em voz alta. Ajuste por analisador: desça até o centróide espectral do ruído pousar na faixa que você quer usar.
3. **Filtro:** low-pass 24 dB/oct e high-pass 24 dB/oct em série. No Live, atenção às unidades do cutoff (Hz); no Serum 2, conferir a escala do parâmetro antes de escrever valores.
4. **Envelope que espelha o kick:** attack ~0.0005 s, decay curto, **sustain 0**, release curto. Toque notas MIDI **só** nos pontos onde o ruído deve existir — o envelope vira o "espelho" que o vídeo desenha à mão.
5. **Mono:** modo mono ligado, sem voz duplicada, sem unison.

### Limitações declaradas desta tradução

- O vídeo **não fornece nenhum valor numérico**: nem quantidade de deslocamento, nem corte de filtro, nem time de delay, nem nível. Tudo acima é proposta.
- Não abri o vídeo em imagem. Os valores que aparecem na tela do Shifter **não foram lidos** — `NÃO VERIFICADO`.
- Não testei o modo Spectral Shift em áudio nesta sessão; o modo existe no Serum 2, o comportamento sonoro não foi ouvido aqui.

## Aplicação por função (kick, sub, baixo/rolling, hats/shaker, percussão de resposta, madeira, stab, subida, atmosfera)

**Leitura crítica antes da receita.** O contexto de auditoria diz que o déficit típico está nos **médios** (300–1.200 Hz a **−4,83 dB**; 1.200–4.000 Hz a **−5,76 dB** contra a média de 6 referências) e que o **low-end já é mono e tem pressão**. Ou seja: esta técnica **não conserta o problema medido** — ela é ferramenta de *groove e pressão pontual*, não de preenchimento. Aplicada como cama contínua, ela piora exatamente o que já está resolvido (engorda o grave) sem tocar no que falta. A tradução correta é **cirúrgica**: eventos curtos, mono, na faixa 60–200 Hz, posicionados nas subdivisões deslocadas que o groove já usa — porque preservar essas posições é justamente o que o vídeo chama de "total control over the groove" (00:03:28.8–00:03:43.5). **Todos os números de banda e nível abaixo são proposta; o vídeo não fornece nenhum.**

| Função | O que fazer | Banda / automação | Freio |
|---|---|---|---|
| **kick** | Não processar o kick. A camada de ruído deslocado entra **nos vãos**, com o envelope desenhado para não coincidir com o golpe — o vídeo é explícito: o envelope é espelhado "so they don't interfere with each other" (00:03:10.4–00:03:12.9). Opcional: `extra filtered kick drum sounds` (00:04:19.3–00:04:27.1) como reforço de groove, filtrado. | Corpo 60–200 Hz. | Sem transiente novo no mesmo instante do kick. O kick continua dono de 30–90 Hz (anti-mascaramento clássico). |
| **sub** | **Não colocar nada disso no canal de sub.** Prática consolidada: "a sujeira fica na camada média, nunca no sub" — o sub é sine, unison 1, sem warp, sem filtro. O papel de "pressão" é cumprido por uma **track separada**, não pelo sub. | Canal de sub intocado. | Regra de ouro: se a camada encostar no sub, ela deixa de ser o que o vídeo faz e vira tapete. |
| **baixo/rolling** | Não sobrepor. Se a camada de ruído ocupar 90–250 Hz, ela briga com o rolling. Solução: HP em **~100 Hz** quando o rolling estiver tocando, ou **ducking dinâmico keyed no rolling**. | 100–200 Hz só nos buracos do rolling. | O rolling é a articulação rítmica; a camada é textura de pressão. |
| **hats/shaker** | **Não aplicar.** Deslocar ruído para cima produz conteúdo inarmônico e brilho metálico — o oposto do que se quer. | — | A faixa 1.200–4.000 Hz já é carente; não é para preencher com metal. |
| **percussão de resposta** | **Melhor uso do vídeo.** Um noise curto deslocado para baixo, com envelope de decay curto, colocado **exatamente nas posições deslocadas do groove** — vira resposta percussiva grave, não cama. É a versão do "extra filtered kick drum sounds just to add even more Groove" (00:04:19.3–00:04:27.1). | 80–200 Hz, evento curto (< 150 ms). | Um evento por resposta, não uma sequência. Não duplicar a subdivisão que a percussão acústica já faz. |
| **madeira** | Não aplicar. Madeira é seca (dry preservado em solista acústico). | — | — |
| **stab** | Não aplicar. | — | — |
| **subida** | Usar como riser: deslocamento subindo ao longo de 8–16 compassos + LP abrindo devagar, sempre mono e com teto de banda. | Começa 60–150 Hz, abre até ~800 Hz. | HP fixo para não invadir o sub durante a subida. |
| **atmosfera** | O vídeo **separa** esse uso: camadas de noise "usually you see them in the context of textures and the overall feel of a track" (00:01:15.0–00:01:22.1), e o foco dele é outro — "using abstract sound sources for low end" (00:01:22.1–00:01:25.9). Se usar para atmosfera, é outra camada, com HP alto. | Acima de 300 Hz. | Não é o alvo deste mapa; atmosfera tem material próprio. |

### Freios para não engordar o sub nem criar brilho metálico

- **Sub:** HP **45–60 Hz, 24 dB/oct, depois do shifter** (nunca antes — o shifter é quem cria a energia grave). O deslocamento de frequência cria bandas laterais que podem cair abaixo de 20 Hz; é o mesmo risco conhecido de FM/RM em notas graves — **HP obrigatório** e conferir 20–60 Hz.
- **Mono:** `Utility` em mono na camada inteira. O low-end do projeto é mono; o low-end do vídeo é estéreo por natureza (ruído). Essa é a adaptação que **não pode ser copiada**.
- **Metálico:** deslocamento **só para baixo**, nunca para cima; **não usar o modo Ring Mod** do Shifter (soma e diferença geram bandas laterais agudas); LP em **200–300 Hz**; nada de filtro comb/resonante; Q baixo.
- **Echo do vídeo (Rumble 2):** prática conservadora veta delay/reverb wet no núcleo do grave. Tradução: o Echo entra **só numa camada de movimento separada**, com o retorno filtrado acima de ~200 Hz; o núcleo 60–200 Hz fica **seco**. Sem essa guarda, o "Echo on the complete group" (00:05:24.1–00:05:35.2) vira lama.
- **Densidade:** eventos, não cama. O ganho do método é controle, e controle se perde no momento em que a camada toca sem parar.
- **Groove:** as posições deslocadas do groove são o esqueleto. A camada se posiciona nelas — não cria uma grade nova, não usa LFO em 1/16 ou 1/8.

### Como provar (A/B sugerido)

1. Mute A/B em **0:00–1:00** e **1:00–2:00** do trecho de teste.
2. Medir **20–60 Hz** com a camada ligada e desligada: **deve ficar igual** (teste do "engordou o sub").
3. Medir **200–300 Hz**: subir no máximo moderado; se disparar, o LP está alto demais.
4. Medir **5–10 kHz**: não pode saltar (teste do brilho metálico).
5. Conferir correlação L/R abaixo de 120 Hz: não pode haver conteúdo estéreo.

## Prioridade e esforço

| Dimensão | Valor | Justificativa |
|---|---|---|
| **Prioridade** | **alta** | É pressão de grave *sem tapete* — exatamente o motor de grave + jogo de ausência de kick do estilo. |
| **Esforço** | **médio** | Nenhum plugin novo, nenhuma compra: Shifter, Auto Filter, Saturator, Echo e Compressor já existem no Live. O custo está no **acabamento** — desenhar envelope golpe a golpe, achar o ponto do shifter por analisador, provar mono e HP. Não é plug-and-play, mas também não bloqueia a primeira versão. |

## Trechos de prova: 3 citações literais da legenda com timestamp

1. **"So this is just a Pure Noise sound and we can clearly see there's a lot of low end information... missing but that is where ableton's shifter comes into play."** — 00:02:15.5–00:02:26.0
   *Prova da premissa: a fonte é ruído **sem grave**, e o Shifter é quem fabrica o grave que não existe.*

2. **"I cut them up and then I modified the envelope. So I essentially mirrored the envelopes from the... ...kick drum so they don't interfere with each other."** — 00:03:03.3–00:03:12.9
   *Prova do mecanismo anti-conflito: não é sidechain de compressor, é desenho de envelope espelhando o kick.*

3. **"you have total control over the groove which is way harder to... ...accomplish with things like traditional reverbs and delays."** — 00:03:34.0–00:03:43.5
   *Prova do motivo declarado: o ganho do método é controle rítmico — e é por isso que ele serve ao groove deslocado.*

## Fontes consultadas e limites

**Legenda (fonte primária):** legenda automática EN do vídeo `h39gdHGGo-c`, obtida via yt-dlp; lida integralmente (legenda completa). As citações foram conferidas contra ela.

**Descrição do vídeo:** lida — usada só para os capítulos (00:01:23 Technique Explained · 00:02:59 Rumble 1 · 00:05:03 Rumble 2 · 00:06:04 Rumble 3) e para identificar os dois plugins de propaganda que **não** aparecem na técnica.

**Conhecimento geral usado no corpo:** princípios de anti-mascaramento kick/bass (kick dono de 30–90 Hz, bass 90–250 Hz), low-end mono, HP 45–60 Hz pós-shifter (mesmo risco de bandas laterais <20 Hz de FM/RM em notas graves) — práticas consolidadas do estilo, não citações do vídeo.

**O que NÃO foi feito / não verificado:**
- Não abri o DAW, não criei preset, não renderizei, não medi áudio. Nenhuma verificação de runtime foi executada.
- Não assisti ao vídeo em imagem: os **valores numéricos que aparecem na tela** (posição do Shifter, corte do filtro, time do delay) não foram lidos e não são afirmados aqui.
- O vídeo **não dá nenhum número** em voz alta; toda banda, corte e nível proposto é proposta.
- Não verifiquei se o acervo tem noise loops comparáveis ao pack "Schmutz".
- O modo Spectral Shift do Serum 2 não foi testado em áudio nesta sessão.
