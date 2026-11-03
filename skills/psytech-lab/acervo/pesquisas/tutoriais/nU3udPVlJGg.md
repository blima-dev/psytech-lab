# How To Make Dark Room Techno - Drone

**Canal:** Sonic Academy · **Vídeo:** `nU3udPVlJGg` · **Duração:** ~13:06 · **Instrutor citado na descrição:** Kirk Degiorgio
**Fonte:** legenda automática em inglês, lida integralmente (69 KB; **sem legenda humana** — só faixas automáticas). Tem legenda. A descrição confirma o tema: "Kirk creates the all important subliminal background drone."

## Técnica ensinada

O drone não é um pad largo: é uma camada **subliminar** `[05:13]`, feita de um acorde **dominante com sétima e quinta bemol** `[01:15]`–`[01:39]` gerado por um MIDI effect que monta o acorde e permite randomizar a inversão, com a **nota de baixo desligada** para não duplicar o grave `[03:26]`–`[03:37]`. O acorde vai para um synth (Massive), passa por um **corte agudo que remove o material baixo** `[06:04]`, é **duckado pelo kick com ataque e release lentos** `[09:07]` para ganhar groove, e recebe **dois autopans em velocidades diferentes** `[09:36]`–`[10:24]` para um espaço 3D sutil. Fecha com reverb longa de **pre-delay sincronizado** mantida baixa no mix `[11:18]`–`[11:37]` e um **phaser discreto** para enfatizar harmônicos `[11:58]`–`[12:06]`. O resultado pretendido é sujo e difícil de localizar — "industrial metallic sound it's very hard to pinpoint" `[07:43]`, "that's roughening up the track" `[07:33]`.

## Ferramentas usadas no vídeo (plugin/stock)

- **Random Chord Generator Pro** — Max for Live / Max MIDI Effect: "random chord generator Pro I put of instance on here" `[01:01]`.
- **Native Instruments Massive** — "I especially like Native Instruments massive" `[03:49]`; o vídeo audiciona presets e ajusta por escuta, mas **não explica a programação do oscilador**.
- **EQ com analisador espectral ("sonogram")** — `[05:50]`–`[06:04]`. O nome do fabricante sai garbled na legenda automática ("elder productions"); **não se sabe qual EQ é**.
- **Kick duplicado em "Sends Only" como fonte de sidechain** — "put it to sends only" `[08:13]`, "this then becomes a sidechain source" `[08:17]`.
- **Ableton Compressor** com sidechain externo — "go to Ableton's compressor" `[08:37]`, "if you choose generic compressor" `[08:43]`; ataque e release lentos `[09:07]`. A legenda **não dá** threshold, ratio nem redução de ganho.
- **Panner 3D com dois panners independentes** (amarelo/vermelho), sincronizado ao host, velocidade em compassos, volume por panner e mix — "this is synced to the host tempo" `[09:52]`, "spotted eights" `[10:24]` (legenda automática de "dotted eighths"). **Marca não é dita.**
- **Hybrid Reverb** — a legenda escreve "their H reverb" (identificado pelo contexto de pre-delay sincronizado; inferência), preset longo, "it's got the pre-delay tempo synched" `[11:18]`.
- **Phaser do Live** — "choose their phaser" `[12:03]`, "more subtle with my effects" `[12:06]` (inferência pela legenda "their phaser", sem nome limpo).

## Equivalentes no Live 12 (conceito por conceito)

> Toda esta seção é **inferência de mapeamento**: o vídeo nomeia Massive, um EQ, um panner 3D, o Compressor, o Hybrid Reverb e o Phaser. Não depende de plugin especial — a tradução é direta.

**1. Gerador de acorde (Random Chord Generator Pro → Live 12 MIDI).**
O device faz quatro coisas: monta um dominante 7(b5) a partir de uma tecla, restringe à escala menor, randomiza a inversão e permite desligar a nota de baixo `[01:01]`–`[03:26]`. No Live, o equivalente mínimo é o **Chord** MIDI effect com intervalos fixos, ou desenhar o acorde direto no clip:
- **Exemplo num projeto em C# frígio — shell seguro:** C#–E–B (menor com sétima, sem quinta) ou C#–B (root + b7). São notas da escala e cabem em oitava 4 — C#4 277 Hz, E4 330 Hz, B4 494 Hz — cobrindo a parte baixa de um vale de médios 300–1.200 Hz.
- **Mordida do 7(b5):** C#–G–B (root, b5, b7) preserva o trítono C#–G e a sétima menor, sem a terça maior. O G natural é fora do frígio; entra só como teste A/B.
- **Acorde completo do vídeo:** C#7(b5) = C#–F–G–B (o F é a terça maior, escrita E#). O F é nota fora do modo frígio — entrar só como teste A/B, não por padrão.
- O "bass note off" do vídeo `[03:26]` vira regra: **não escrever abaixo de C#4 (277 Hz)** e high-pass depois. O motivo é o mesmo do vídeo: "can get too muddy otherwise" `[03:37]`.
- O device randomiza inversão; alternativa determinística: 2–3 clips com inversões diferentes e troca por compasso — evita aleatoriedade não reproduzível.

**2. Synth (Massive → Massive X / Serum 2 / Diva / Surge XT).**
O vídeo só audiciona presets; não há receita de oscilador. Tradução por papel:
- **Massive X:** osciladores wavetable, unison 2–4, detune pequeno, filtro band-pass/low-pass ~1,5–2,5 kHz, **sem camada de sub**, distorção leve no insert. Substituto mais direto do Massive.
- **Serum 2:** oscilador **granular** com fonte sustentada (madeira raspada, órgão, corda friccionada) + um oscilador analógico fino para o núcleo afinado; **sem Sub osc**; filtro band-pass; warp leve. O granular entrega o "hard to pinpoint" `[07:43]` sem sample de metal.
- **Diva:** 2–3 VCOs detunados, filtro ~2 kHz, chorus desligado (chorus amplia fase e borra o centro).
- **Vital / Surge XT:** alternativas. Vital tende a brilhar, então low-pass obrigatório; Surge XT tem phaser/chorus internos para a etapa final.
- **Bibliotecas sampleadas:** material sustentado orgânico (pad/atmosfera, órgão com batimento, textura de raspagem) como matéria-prima do leito — não como fonte de ataque.

**3. EQ (→ EQ Eight).**
"I like a really sharp cutoff here and I can remove all this low material" `[06:04]`. Tradução: **EQ Eight, high-pass 24 dB/oct em 250–350 Hz** e **low-pass 12 dB/oct em 5–6 kHz**. O HP protege o sub e o low-end mono; o LP impede o brilho metálico que o vídeo busca de propósito ("industrial metallic") e que projetos de madeira orgânica não querem. **Sem boost:** um vale de 300–1.200 Hz é preenchido pela fundamental/harmônicos do drone, não por EQ.

**4. Sidechain (→ Compressor + kick duplicado).**
Mecanismo idêntico no Live: duplicar o kick, **Audio To = Sends Only**, zerar os sends (para ficar realmente inaudível) e escolher essa track como **Ext. In** do Compressor do drone `[08:13]`–`[08:17]`. O vídeo usa o compressor do Live, na opção que a legenda chama de "generic compressor" `[08:37]`–`[08:43]`, com ataque e release lentos `[09:07]` e **sem valores numéricos**. Proposta de partida: attack 15–25 ms, release 250–400 ms, ratio 2:1–4:1, redução 2–4 dB. O ataque lento faz o duck chegar **depois** do transiente, então o drone respira no espaço do kick em vez de recortar o ataque.

**5. Panner 3D (→ dois AutoPan + Utility).**
O device tem dois panners independentes: um rápido (colcheias pontuadas) e um lento (compasso), com volume e mix `[09:36]`–`[10:24]`; ele abre "extreme" para ouvir e depois "take it right down" `[10:54]`–`[10:57]`.
Tradução: **AutoPan 1** em 1/8 pontuado, **Phase 180°** (modulação binaural em contrafase evita tremolo comum), amount 20–30%; **AutoPan 2** em 1 compasso, amount 10–20%; **Utility → Bass Mono ~200 Hz** depois dos pans.
- **Shifter:** não é necessário; o vídeo não usa pitch shift. Se quiser batimento, detune os osciladores (fine ±3–6 cents) em vez de desafinar L/R.
- **Echo:** o vídeo não usa delay; não adicionar — atraso no drone borra subdivisões deslocadas.

**6. Reverb (→ Hybrid Reverb).**
Mesmo device. Preset longo, **pre-delay sincronizado** (1/16 ou 1/8), 100% wet num **return**, EQ no retorno (HP 400 Hz, LP 6 kHz) e nível baixo — "keep it nice and low in the mix" `[11:37]`.

**7. Phaser (→ Phaser do Live / FX do synth).**
Rate muito lento, depth baixo, feedback baixo, só na banda 300 Hz–4 kHz: "emphasizing different harmonics" `[11:58]`, "more subtle with my effects" `[12:06]`.

## Notas de aplicação (por função)

**Contexto do projeto de referência:** médio 300–1.200 Hz em **−4,83 dB** e 1.200–4.000 Hz em **−5,76 dB** contra a média de 6 referências; low-end mono; groove com subdivisões deslocadas **.27/.77** a preservar. O vídeo não dá valores de EQ, sidechain, pan ou nível — os números abaixo são **proposta** (inferência).

**Cadeia proposta:** `synth granular + osc analógico → EQ Eight (HP 280–320 Hz, 24 dB/oct; LP 5,5–6 kHz, 12 dB/oct) → Compressor (sidechain do kick silencioso; 2–4 dB GR) → AutoPan 1/8 pontuado (Phase 180, 20–30%) → AutoPan 1 compasso (10–20%) → Utility Bass Mono 200 Hz → fader −18 a −24 dB → send para Hybrid Reverb (pre-delay 1/16–1/8; return HP 400/LP 6k)`.

| Função | O que fazer | Por quê |
|---|---|---|
| **Kick** | zero drone; só a duplicata silenciosa como fonte de sidechain `[08:13]`–`[08:17]` | O kick real não muda; a cópia em Sends Only com sends zerados é inaudível e serve de gatilho. |
| **Sub** | zero; **sem Sub osc**, HP ≥ 280 Hz, Bass Mono | Low-end < 150 Hz rigorosamente mono (prática de referência); o drone não pode escrever grave. |
| **Baixo / rolling** | drone não escreve abaixo de C#4 (277 Hz) e **não** recebe sidechain do baixo, só do kick | O groove deslocado vive do ataque do rolling; sidechain do baixo no drone criaria bombeamento duplo. Se o harmônico do baixo conflitar em 250–350 Hz, dip estreito de 1–2 dB **no drone**, nunca no baixo. |
| **Hats / shaker** | drone fica abaixo de 5–6 kHz; não usar fonte metálica | O topo é o espaço do shaker; "industrial metallic" compete com ele e vira aspereza. |
| **Percussão de resposta** | drone −18/−24 dB; o duck lento abre buracos depois do kick | É onde a resposta aparece; o drone não pode mascarar o transiente. |
| **Madeira** | melhor fonte do drone: material orgânico de madeira (sample/granular) | Mantém o caráter orgânico e entrega o "grungy" / "scraping" `[07:42]` sem metal. |
| **Stab** | drone atrás; se o stab usa C#–E–B, o drone usa C#–G–B ou só C#+B | O vídeo trata o stab como terceiro elemento separado do drone `[00:33]`–`[00:39]`; evitar voicing duplicado. |
| **Subida** | **o vídeo não ensina transição.** Se usar, o drone é leito com LP automatizado, não um elemento novo | Marcação explícita: isto é inferência, não técnica do vídeo. |
| **Atmosfera** | **função principal**: drone em oitava 4 (C#4–B4) + harmônicos de saturação suave | Ocupa 300–1.200 Hz pelas fundamentais (a partir de ~277 Hz) e pelos harmônicos, preenchendo o vale sem EQ de boost. |

**Sem engordar o sub:** nenhum Sub osc; HP 24 dB/oct ≥ 280 Hz; Bass Mono; o sidechain não adiciona grave; conferir em analisador que não há energia nova < 150 Hz.
**Sem brilho metálico:** LP 12 dB/oct em 5,5–6 kHz; fonte de madeira em vez de metal; saturação leve (Soft Sine / soft clip); se aparecer aspereza em 3–5 kHz, notch dinâmico estreito; phaser lento em vez de chorus.
**Batimento:** o vídeo gosta do "nice little beating sound" `[06:18]`. Em C#4 (277 Hz), dois layers com ±5 cents batem ~0,8 Hz — lento, tipo respiração, não chorus.
**Groove deslocado:** grãos granulares criam transientes fora do grid se a densidade for baixa ou o grain length curto. Usar grain length ≥ 120 ms e densidade alta (textura contínuua), ou manter o núcleo como sample em loop (Sampler) e o granular só como camada paralela baixa. O duck lento do kick não cria hits; ele só abre/fecha o drone, então preserva as subdivisões deslocadas.
**Nível/alvo:** o vídeo diz "subliminal" `[05:13]` e "low in the mix" `[11:37]`, mas **não dá dB**. Proposta: drone 12–18 dB abaixo do elemento principal, confirmado por A/B e analisador.

## Prioridade e esforço

**Prioridade: alta.** É a camada que ataca um vale medido de 300–1.200 Hz (e parte de 1.200–4.000 Hz) sem EQ de boost, e reforça a pressão hipnótica com um elemento que o vídeo descreve como subliminar e difícil de localizar. Não exige plugin novo.

**Esforço: médio.** Precisa de desenho de patch (granular ou Massive X), roteamento de kick duplicado em Sends Only para o sidechain, dois moduladores de pan, um return de reverb e A/B contra o rolling. Não é baixo porque não é "carregar preset"; não é alto porque tudo é device stock e a receita do vídeo é curta.

**Risco:** mascarar o rolling em 250–400 Hz e criar aspereza metálica em 3–5 kHz. Controlado por HP/LP, nível e escolha de fonte de madeira. Divergência deliberada do vídeo: ele quer "industrial metallic" `[07:43]`; um projeto de madeira orgânica prefere fonte orgânica.

## Trechos de prova

1. `[01:15]` **"one of the most popular chord types to use in this type of music is the dominant seven"** · `[01:39]` **"dominant seven with a flatted fifth"**
2. `[03:26]` **"just turn the bass note off"** · `[03:37]` **"I don't want it interfering with the bass the very heavy bass that we've already got can get too muddy otherwise"**
3. `[05:13]` **"you generally want it to be very subliminal you don't want it taking up too much of the mix"**

> Citações reproduzidas do texto deduplicado da legenda automática; o VTT cru repete cada linha em cues consecutivos, removidos na leitura.

## Limites da legenda (o que o vídeo não diz)

- **Sem valores numéricos** de HP/LP, attack/release, ratio, decay de reverb, amount de pan ou dB.
- **Sem fundamental do acorde**: o vídeo diz o tipo (dominante 7(b5)) e a escala (menor), mas não a fundamental do acorde gerado — ele só diz que toca um C no teclado.
- **Marcas garbled/não ditas**: o EQ ("elder productions") e o panner 3D não têm fabricante confirmável na legenda; "H reverb" e "their phaser" foram identificados como Hybrid Reverb e Phaser do Live pelo contexto, não por nome limpo.
- **Sem arranjo**: não há posição na timeline, nem técnica de subida/transição, nem relação com kick/bass além do sidechain.
- O vídeo tem ~13 min e termina em propaganda; ele constrói **só o drone**, não a faixa inteira.
