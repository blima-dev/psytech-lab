# OTT Explained: How to Use It (And When Not To!)

> **id:** Kt22wEkGx-Y · **canal:** Sonic Academy (Nate, Produce Culture) · **publicado:** 2026-10-15 · **duração:** 13:27 · **tema:** meio-espaço
>
> **Método:** legenda automática EN (560 cues). Conferência cruzada pontual com transcrição local (whisper.cpp, `ggml-small`) só para resolver nomes que a ASR do YouTube deturpa — **as citações abaixo são sempre o texto da legenda oficial** (com o artefato de ASR apontado quando existe), não o da transcrição local.
>
> **Contraste citado no estudo:** um set de trabalho medido no levantamento original mostrou o meio carente (300–1.200 Hz −4,83 dB e 1.200–4.000 Hz −5,76 dB contra a média de 6 referências externas), low-end mono e subdivisões deslocadas do grid. Essas medições são do set de referência, não do vídeo.

## Técnica ensinada (2-4 frases)

O OTT é compressão multibanda que soma **upward compression** (levanta o que está baixo) à compressão downward, e o "fizz/punch" característico vem exatamente de amplificar o conteúdo quieto de alta frequência. A consequência prática — que é a tese do vídeo — é que a upward compression **desfaz cortes de EQ** feitos antes dela: qualquer coisa que caia na zona de upward volta a subir, então o OTT tem de entrar **cedo na cadeia, antes do EQ subtrativo**. Empilhado em vários elementos ele adiciona camadas de conteúdo quieto ao master e faz o limiter trabalhar em cima de densidade em vez de dinâmica — o mix fica "cheio" e menos alto. O uso defensável é pontual: num som individual/lead, em paralelo e em dose pequena, quando o arranjo é minimalista e há espaço para aquele elemento subir; e o reverb/send entra **depois** dele, nunca antes.

## Ferramenta usada no vídeo (plugin/stock)

- **Clone de OTT** — a legenda transcreve o nome como "VOTT": *"I have VOTT installed. I don't have the original plugin on my computer right now. They both do roughly the same thing."* (01:23–01:31). O plugin original do OTT não está na máquina dele.
- **Bitwig — Dynamics (stock)**, usado só para **visualizar a curva de transferência** (03:22–03:32). É o único ponto em que o vídeo depende de Bitwig, e é demonstração visual, não sonora.
- **iZotope Ozone — Maximizer**, citado como exemplo de plugin que também traz upward compression (05:28–05:36).
- **ANA** — de onde veio o som de teste: *"Here is the audio I took from Ana."* (01:03–01:05). É só a fonte, não a ferramenta ensinada. **INFERÊNCIA:** "Ana" deve ser o synth ANA (Sonic Academy), mas o vídeo não nomeia o produto.
- **Unmask** (citado como *"tools like Unmask, which is also from TBTech"*, 02:49–02:54) — usado só para mostrar o mesmo princípio **no nível espectral**: *"here, it amplifies what is quiet in the signal"* (03:05–03:11).
- Nada do que o vídeo ensina exige ANA 2, VELA, SideKick, Kick 3 ou Bitwig. O Bitwig aparece como tela de análise.

## Tradução para ambiente de trabalho comum: Live 12 nativo + synths (Serum 2, Diva, Vital, Massive X, Surge XT, Kontakt 8)

### Live 12 — a rota real (o OTT mora aqui, não no synth)

- **Multiband Dynamics** é o equivalente direto do "Dynamics" mostrado no vídeo: a seção **Above** é a compressão downward e a **Below** é a upward, banda por banda, com **Amount** controlando a intensidade. É o mesmo par de curvas que ele manipula na tela (04:12 *"This is the upward compression component here now."*).
- A parte **expander** que ele cita na arquitetura do OTT (01:34) não é necessária. A legenda oficial registra essa passagem como *"It seems like OTT is just upstream and downstream compression. Without expansion section."* (01:37–01:41) — "upstream/downstream" é artefato de ASR; a transcrição local, no mesmo ponto, diz "I think the OTT is actually just upward and downward compression, not the expansion section". Se quiser a arquitetura completa, o modo **Expand** do Compressor do Live cobre o expander.
- Monte num **Audio Effect Rack** no canal (nunca no master), com um Macro de Amount para A/B. 3 bandas, **Below** ligado só nas bandas média/alta.
- **Simpler / Sampler / Grain / Operator** são fontes — não fazem upward compression; o OTT entra depois deles, no canal. **Echo / Hybrid Reverb** são justamente os sends que precisam vir **depois** do OTT (ver a regra do reverb abaixo). **AutoPan / Shifter** não têm relação com o conceito.

### Synths (Serum 2, Diva, Vital, Massive X, Surge XT)

- OTT **não é função de síntese**: não existe em GranularOsc, em wavetable, em unison nem em filtro. É processamento de dinâmica pós-synth — mantenha o patch seco e processe depois. O vídeo chega à mesma conclusão pelo lado dos sends: *"It's better to leave the signal dry and then add boost after the upstream compression."* (10:48–10:53).
- **NÃO VERIFICADO:** não está confirmado se toda versão do Serum 2 traz compressor multibanda no rack de FX. Se trouxer, ele pode fazer o papel; o caminho verificável é o Multiband Dynamics do Live.
- Diva, Vital, Massive X e Surge XT: mesma regra — nada dentro do instrumento; insert no canal.

### Kontakt 8 (bibliotecas acústicas/orgânicas)

- Instrumentos acústicos/orgânicos: a regra de good practice (dry preservado; wet baixo ou processamento paralelo) já aponta na direção que o vídeo defende. Se usar, **paralelo e em dose pequena**, e nunca depois da cauda de reverb — o vídeo mostra que a upward compression trata a cauda como "componente quieto": *"the reverb starts to be considered the same quiet component, and it all becomes too much"* (10:26–10:30) e o preset *"suddenly becomes too damp"* (10:39–10:41).

### O que não é necessário

Bitwig Dynamics (só demo visual), Ozone Maximizer (só citado) e o clone "VOTT". **Nenhum é necessário** — o conceito sobrevive inteiro no Multiband Dynamics do Live.

## Aplicação por função

**Aviso que vale mais que o efeito:** num set com o meio carente (no exemplo medido, ~−5 dB abaixo da média das referências em 300 Hz–4 kHz), OTT **não corrige curva de mix** — ele levanta o que é quieto dentro de *um* som. Aplicado em vários canais, produz exatamente o que o vídeo descreve: *"you're essentially adding more and more frequency content to your master"* (08:14–08:17), e o limiter passa a trabalhar em camadas de som quieto que ficou alto (08:20–08:33).

### Por função

**INFERÊNCIA do estudo:** as linhas abaixo aplicam o mecanismo descrito no vídeo a um motor psytech. O vídeo não fala de kick, sub, rolling, nem de groove deslocado — ele só enuncia a regra geral (upward compression levanta o que é quieto e desfaz corte de EQ anterior).

| Função | Usar? | Como / por quê |
|---|---|---|
| **kick** | **Não** | Upward compression levanta a cauda/o quarto e adiciona HF; o kick precisa de ataque seco e cauda curta. |
| **sub** | **Não** | Nem Below na banda baixa: sobe conteúdo sob o fundamental, mexe no nível percebido e suja o mono. O grave fica intocado. |
| **baixo/rolling** | **Não no sinal principal** | O groove vive do vazio entre as notas (subdivisões deslocadas do grid); upward compression preenche esse vazio. Se algum dia precisar de corpo, só em paralelo, Below apenas acima de ~300 Hz e Amount baixo — e A/B do groove antes de aceitar. |
| **hats/shaker** | **Evitar** | É o caso em que ele faz o efeito que o gênero rejeita: *"That's why you get that sizzling and energetic effect."* (02:40–02:46) — a transcrição local no mesmo ponto diz "fizzy punchy kind of effect". Presença de shaker se resolve com EQ/saturação, sem o brilho metálico. |
| **percussão de resposta** | **Melhor candidato** | Som individual, com espaço no arranjo. Em paralelo, Amount baixo, crossovers em ~300 Hz e ~4 kHz e Below ligado só na banda do meio; EQ subtrativo depois para tirar o fizz. |
| **madeira** | **Segundo candidato** | Mesma receita (crossovers ~300 Hz / ~4 kHz, Below só no meio), mais conservador: o timbre orgânico é o ativo, e o OTT tende a endurecer transiente. |
| **stab** | **Condicional** | Só se for o único elemento desse tipo no trecho — o vídeo pergunta exatamente isso: *"But you also have to consider whether this is the only lead sound you're working with at a particular point in the track."* (06:06–06:15). Dois stabs empilhados: não. |
| **subida** | **Pode, com automação** | O upward compression segura a cauda; o riser continua "presente" depois de acabar. Automatize o Amount para zero no drop. |
| **atmosfera** | **Nunca depois do reverb** | Ordem correta: seco → OTT → send de reverb. O vídeo é explícito: a cauda passa a contar como componente quieto e o preset *"suddenly becomes too damp"* (10:39–10:41). |
| **master** | **Não** | É o cenário que o vídeo passa o bloco 07:55–08:33 inteiro desaconselhando. |

### Ordem na cadeia (a regra central do vídeo)

`fonte → OTT → EQ subtrativo → saturação/caráter → sends`

Se o EQ vier antes, o OTT devolve o que foi cortado: *"you're essentially just undoing what you did here"* (06:43–06:50) e *"Make sure it's before other effects, before the equalizer, so you can properly cut out the excess"* (12:13–12:18). O motivo é o mesmo que explica o fizz: *"it boosts the quiet parts of the signal"* (02:06–02:09).

### Attack/release e groove

**O vídeo não fala de attack/release** — o que segue é proposta do estudo, não ensinamento dele. Com release rápido o ganho "respira" no grid de 1/16 (117 ms a 128 BPM) e pode apagar as subdivisões deslocadas; comece com release ≥ 150 ms e Amount baixo, e confirme por A/B que o deslocamento rítmico continua audível.

### Low-end mono

O OTT não gera largura estéreo, então não quebra o mono por si. O risco é de **nível e timbre** no grave — por isso a banda baixa fica fora (Below desligado abaixo de ~300 Hz).

## Prioridade e esforço

**Prioridade: média · Esforço: baixo.**

- **Média e não alta:** o valor do vídeo é sobretudo um **guardrail** (onde não usar, e a ordem OTT → EQ) mais um candidato pontual (percussão de resposta / madeira). OTT não fecha o gap do meio carente; quem fecha é EQ subtrativo e rebalanceamento de arranjo.
- **Esforço baixo:** um insert de Multiband Dynamics com Macro de Amount, sem comprar nada, A/B em minutos.
- **Risco desproporcional ao ganho:** é literalmente a fábrica do "serra metálica" que o estilo rejeita. Um Amount alto em hats/shaker ou em dois stabs empilhados destrói o meio que se quer reconstruir.

## Trechos de prova

1. **02:06.173–02:09.990** — *"But what else it does / to improve the sound is it / boosts the quiet / parts of the signal."* (cues consecutivos, concatenados).
2. **06:43.816–06:50.237** — *"And when you / submit this to an / OTT-type plugin, you're essentially / just undoing what you / did here."* — "submit" é artefato da ASR do YouTube; a transcrição local diz "running that into an OTT style plugin, you're essentially just negating what you've done here".
3. **12:13.833–12:18.681** — *"Make sure it's / before other / effects, before / the equalizer, so you / can properly / cut out the excess"*.
