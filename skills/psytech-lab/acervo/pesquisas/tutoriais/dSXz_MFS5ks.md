# How Default Stereo Reverb Ruins Mix Space (And Why Mono Can Better)

> **Fonte:** legenda automática EN (faixa `en-orig`, English Original) obtida via yt-dlp; vídeo ~6:43.
> **temLegenda = true.** Canal: Sonic Academy · Tema: meio/espaço de mix · Áudio não escutado.
> Nota de coleta: a faixa `en` não estava disponível (HTTP 429) e `--write-subs` respondeu "There are no
> subtitles"; a faixa disponível era `en-orig` e baixou normalmente.

## Técnica ensinada (2-4 frases)

O vídeo manda a reverb por **send/effects bus, 100% wet**, e em vez de deixar o retorno estéreo com o width no máximo ("width full up"), **soma esse retorno em mono**. A tese é que largura percebida nasce do contraste entre centro e laterais — *"one of the key things for creating a wide mix is to have less wide components in it"* —, então monoar a reverb deixa o dry no centro e a cauda como uma fonte mono posicionável. Reduzir a largura também gera um phasing L/R que o autor associa a um som mais retrô, e o retorno mono pode ser jogado para o lado oposto ao elemento seco: *"two mono signals that actually create something that's a lot more uh wide"*. Ele fecha pedindo para não evitar efeitos mono: o default de "tudo largo e moderno" é justamente o que apaga a sensação de largura.

## Ferramenta usada no vídeo (plugin/stock)

- **Bitwig nativo, nenhum plugin de terceiros:** "we'll try this out just with reverb stocks uh stock stuff from Bitwig" `[00:01:06.000]`.
- **Effects bus / send effect** com a Reverb stock do Bitwig: "some reverb via a send effect" `[00:00:52.160]`, "We'll add an effects bus here" `[00:01:00.760]`, com o **dial de width tipicamente em 100%** `[00:01:12.560–00:01:14.600]`.
- **Material de teste:** um drum break estéreo `[00:00:33.000–00:00:35.280]`, um som de string com arpeggiator `[00:00:38.040–00:00:39.240]` e o synth stock **Polymer**, tornado mono para o teste de pan `[00:05:02.360–00:05:07.720]`.
- **Extras opcionais no tanque da reverb:** chorus com **pitch shift oposto em L e R dentro do tanque**, aplicado só na cauda `[00:02:32.440–00:02:40.959]` e `[00:02:56.760–00:02:58.280]`; e **redução leve de sample rate só na cauda** `[00:03:13.000–00:03:18.840]`, descrita como forma de empurrar para o território old school.
- O vídeo **não** cita modelo de reverb, valores de decay, pré-delay, HP/LP ou medições. A demo é por escuta A/B.

## Tradução para ferramentas Live 12

**Rota principal — Live 12 nativo (não depende de Bitwig):**
`Send → Return track → Hybrid Reverb (100% wet) → Utility com Stereo Width em 0% (soma mono) → pan do retorno`.
É o gesto do vídeo inteiro sem plugin novo.

Ressalva geral do device: no **Utility** do Live, o parâmetro Stereo Width não é linear (o histórico de uso registra comportamento quadrático) — para **0% (mono)** isso é irrelevante, mas não leia 50% como "metade da largura".

**Chorus dentro do tanque (pitch shift oposto L/R, só na cauda):** no Live, coloque a modulação **depois** da reverb, no retorno molhado — Chorus-Ensemble, ou duas instâncias de **Shifter** com fine detune oposto (uma L, uma R). Como o retorno é somado em mono em seguida, os desvios opostos produzem exatamente o phasing que o vídeo descreve em `[00:04:10.880–00:04:18.200]`.

**Redução de sample rate só na cauda:** **Redux** no retorno, depois da reverb, com redução leve. Só na cauda, nunca no dry.

**Serum 2 / Diva / Vital / Massive X / Surge XT / Kontakt 8:** a reverb interna de qualquer instrumento sai somada ao dry no canal estéreo do plugin — é exatamente o default que o vídeo critica. A tradução é **zerar/desligar a reverb interna** e fazer a cauda no retorno do Live. Serum 2 tem FX bus interno (racks e sends próprios), mas ele continua **dentro** do instrumento: não dá para posicionar a cauda separada do dry no mixer nem panar o retorno independente do som seco. *(INFERÊNCIA de arquitetura, não é fala do vídeo.)*

**O que NÃO usar para isso:**
- **AutoPan** para posicionar a reverb: posicionamento estático se faz com o **pan do retorno**; AutoPan é movimento, não posição.
- **Shifter/Redux no dry** para "dar caráter": o efeito retrô do vídeo é na cauda; no dry ele destrói transiente e pode virar aspereza.

**Alternativas nativas equivalentes:** Convolution Reverb com IR curta no mesmo esquema (retorno mono) para sala seca; Grain Delay/Spectral Blur só como atmosfera, não no motor.

## Aplicação por função

**Contexto de auditoria (set de referência contra a média de 6 referências do estilo):** meio 300–1.200 Hz em **−4,83 dB** e 1.200–4.000 Hz em **−5,76 dB**; low-end é mono; groove com subdivisões deslocadas fora do grid, a preservar.

**Retorno único "MONO ROOM":** Hybrid Reverb (100% wet) → EQ8 com **HP 280–320 Hz** e **LP 4–5 kHz** → Utility Width 0% → pan. O HP protege o sub; o LP evita o brilho metálico que o phasing do mono pode criar. *(Números são proposta — INFERÊNCIA; o vídeo não dá valores.)*

| Função | Send / retorno | Como e por quê |
|---|---|---|
| **Kick** | zero | Prática do estilo: sem desfasamento estéreo no kick; qualquer cauda borra o transiente que ancora o groove. |
| **Sub** | zero | Low-end < 150 Hz rigorosamente mono. |
| **Baixo / rolling** | zero (ou desprezível, HP ≥ 500 Hz) | O groove deslocado vive do ataque; o phasing da largura reduzida `[00:04:10.880]` borra justamente isso. Preferência: seco. |
| **Hats / shaker** | send baixo, HP > 2 kHz, retorno no lado oposto | Candidato secundário. Se o topo já orbita com AutoPan, a reverb mono pode achatar a órbita — testar A/B antes. |
| **Percussão de resposta** | **melhor candidato**: send −12 a −18 dB, decay curto, HP ~300 Hz, retorno no lado oposto ao hit seco | É o caso do vídeo: dry em 0.28R, cauda mono em 0.28L. Preenche 300–1.200 Hz com densidade **central**, sem alargar as laterais nem mexer no groove. |
| **Madeira** | send médio, HP 250–300 Hz, LP ~4 kHz | Principal ferramenta para o déficit de 300–1.200 Hz sem EQ. Para o retrô do vídeo: detune oposto L/R na cauda + soma mono. Manter o LP para não criar brilho metálico. |
| **Stab** | send baixo, retorno no lado oposto | Reforça o diálogo pergunta-resposta. Não aplicar no stab que carrega a melodia principal se ela precisa ficar legível. |
| **Subida** | **exceção: deixar larga/estéreo** | A lição é contraste — a subida só soa grande porque o motor em volta é mono. Monoar a subida a encolhe. |
| **Atmosfera** | reverb estéreo é legítima | O vídeo pede para não fazer do estéreo o default de **tudo**, não para monoar tudo. Se a atmosfera mascara o meio, monoar reduz o espalhamento e libera centro. |

**Regra de segurança contra brilho metálico:** monoar a cauda de uma reverb estéreo gera phasing (`[00:04:10.880–00:04:18.200]`); em material com muito conteúdo acima de 4 kHz isso vira aspereza. Por isso: LP no retorno, send conservador e **nunca** colapso de largura no dry.

**Por que funciona no estilo:** o vídeo dá o mecanismo do espaço negativo sem custo de EQ — em vez de empurrar 300–1.200 Hz no bus, você devolve densidade **no centro** por uma cauda curta e mono, enquanto as laterais ficam vazias para o topo orbitar.

## Prioridade e esforço

- **Prioridade: alta.** Ataca de frente o espaço negativo + low-end mono e o déficit medido de 300–1.200 Hz sem boost de EQ nem ganho; é mudança de arquitetura de mix, não de timbre.
- **Esforço: baixo.** Um return, Hybrid Reverb, EQ8, Utility e pan — tudo nativo, sem plugin novo e reversível em um clique. As variações retrô (chorus/Redux na cauda) são **esforço médio** e opcionais.
- **Risco:** baixo. O único risco real é monoar a cauda de um elemento cujo topo precisa da órbita (hats/shaker) — mitigado deixando esse send baixo e testando A/B.

## Trechos de prova

1. `[00:01:34.760–00:01:37.440]` **"sometimes it can be very valuable to actually mono that reverb as well."**
2. `[00:01:50.480–00:01:53.480]` **"uh one of the key things for creating a wide mix is to have less wide components in it."**
3. `[00:05:34.520–00:05:38.880]` **"by doing so, that you can have two mono signals that actually create something that's a lot more uh wide."**

**Limites do estudo:** análise só da legenda automática (ASR); áudio não escutado; o vídeo não cita modelo de reverb nem valores — tudo que tem número aqui é proposta, não receita do autor.
