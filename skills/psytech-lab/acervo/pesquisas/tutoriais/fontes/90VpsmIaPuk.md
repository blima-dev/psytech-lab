# How to Make Techno Ambient Drone Atmosphere

**Canal:** Audioreakt · **Duração:** 23:28 · **Legenda:** automática em inglês (836 cues), obtida e lida na sessão original de dissecação.
**Descrição (confirmatória):** "how to easily create drone ambience sound to put in the background… set the mood of you track and as well sometimes to glue together other element of your track and give cohesion." A descrição também lista **Padmaker Rack**, **Detune Fx Rack** e **Ultimate Fx Rack** como os racks usados.

---

## Técnica ensinada (2-4 frases)

O vídeo constrói um drone harmônico no **Operator em parallel mode**: quatro osciladores afinados em múltiplos inteiros — raiz, uma oitava acima, oitava + quinta e outro múltiplo — com volumes decrescentes (00:03:03–00:03:52). Depois duplica o Operator num rack e mapeia macros para **pitch de cada Operator, forma de onda (shape), coarse de todos os osciladores com faixas escalonadas 1/2/3/4 ("space"), volume de todos os harmônicos menos A1, detune com teto diferente por oscilador (14/3/26/34, sem passar de 40) e feedback a 50% modulado por LFO** (00:04:24–00:17:45). O movimento vem da síntese, não do efeito — ele mostra o rack "no effect yet" (00:10:27) antes de aplicar filtro e a cadeia de delay/reverb (00:14:25–00:14:50). O resultado é uma cama contínua que serve para "setting the mood or adding tension" (00:00:31.840), tocada em volume de fundo e que não deve embolar com baixo e kick (00:21:33).

---

## Ferramenta usada no vídeo (plugin/stock)

- **Ableton Live + Operator (stock)**, em **parallel mode**, com 4 osciladores e feedback por oscilador (00:03:03; 00:17:23).
- **Instrument Rack + Macro Controls** (macros 4, 5, 6 e 7 citadas explicitamente: 00:05:27, 00:07:41, 00:10:59, 00:12:05).
- **Spectrum** (stock) para visualizar os harmônicos que cada oscilador adiciona (00:03:15).
- **Racks do próprio canal**: **Padmaker Rack** ("pile maker rack" na legenda automática, 00:14:48; nome correto confirmado na descrição) e **Detune Fx Rack** (00:19:44–00:19:52; descrição). A descrição lista ainda **Ultimate Fx Rack**.
- **Nenhum sintetizador de terceiros.** O vídeo não usa ANA 2, VELA, SideKick, Kick 3 nem Bitwig.

---

## Tradução para Serum 2, Diva, Vital, Massive X, Surge XT, Kontakt 8 e Live 12 nativo

O vídeo usa **exatamente o Operator**, que já existe no Live 12 — a tradução é quase literal, não analógica. Nada no vídeo depende de ANA 2, VELA, SideKick, Kick 3 ou Bitwig (nenhum aparece), então não há conceito a substituir. O único item externo são os racks do autor, e o que eles fazem (delay + reverb longos; detune/width) existe nativo.

| Elemento do vídeo | Equivalente |
|---|---|
| Operator em **parallel mode**, 4 osciladores (00:03:03) | **Operator (Live 12)** — mesmo device, mesmo modo. Alternativas: **Serum 2** (3 osciladores + sub, sem a mesma liberdade de ratio no sub → duas instâncias para 4 harmônicos independentes), **Diva** (3 osciladores, afinação por oscilador), **Vital** (3 osciladores), **Massive X**, **Surge XT**. |
| Múltiplos inteiros: 1×, 2×, 3×, 4× (a legenda diz "one octave upper", "the fifth… plus seven", "go four", 00:03:22–00:03:52) | **Coarse** do Operator por oscilador. No Serum 2: `octave`/`semitone`/`fine` por oscilador; no Vital: semitone + fine; no Surge XT/Massive X: pitch por oscilador. A matemática 2× = +12, 3× = +19, 4× = +24 semitons é **INFERÊNCIA** (a legenda não nomeia o parâmetro; o próprio autor diz que "it's not like a multiplication… sometimes it's giving the fifth", 00:08:34). |
| Dois Operators para deslocar um contra o outro (00:03:59; "so i'm still playing one note", 00:04:44) | **Instrument Rack com dois Operators** e macros do rack mapeadas nos parâmetros dos dois (o Live permite mapear uma macro a parâmetros de devices diferentes). |
| Macro 4 = **shape** de todos os osciladores (00:05:27–00:05:44) | Waveform por oscilador do Operator, mapeada a uma macro. Serum 2: table position/warp; Vital: shape; Massive X: wavetable. |
| Macro 5 = **coarse escalonado** (valores 1/2/3/4 mapeados um por oscilador, 00:08:04–00:08:11) | **Macro do Live com Min/Max independentes por parâmetro mapeado** — é isso que produz o escalonamento 1/2/3/4 → 2/3/4/5. No Serum 2: macro com `amount` diferente por rota. |
| Macro 6 = **volume de todos menos A1** (00:10:56–00:10:59) | Níveis por oscilador do Operator. Serum 2: volume por oscilador; Vital/Massive X idem. |
| Macro 7 = **detune** no fine de cada oscilador, com tetos 14/3/26/34 e limite 40 (00:12:14–00:12:53) | **Fine** por oscilador do Operator (mais o **Spread** global, que ele também mapeia ao detune, 00:13:47). Serum 2: `fine` por oscilador + unison detune; Vital: detune; largura extra com **AutoPan**. |
| **Feedback 50% + LFO** no feedback do oscilador B (00:17:23–00:17:45) | **Feedback por oscilador do Operator**. O LFO pode ser o interno do Operator **se** a versão expuser Feedback como destino (não verificado na sessão original) ou, com segurança, um **LFO device mapeado ao parâmetro Feedback**; sem LFO, automação/envelope do parâmetro resolve. No Serum 2 esse mecanismo não existe igual — modular warp/FM ou ruído dá outra coisa, não o mesmo feedback. |
| Filtro no fim "to have a bit more control" (00:14:25) | **Filter** do Operator ou **Auto Filter** no canal/rack. |
| "A lot of delay and reverb" / Padmaker Rack (00:14:48) | **Echo + Hybrid Reverb** em send/retorno (ou em série dentro do rack). O Padmaker é só a receita dele; não é necessário. O **Detune Fx Rack** equivale a **Chorus-Ensemble / Shifter / AutoPan** nativos. |
| Papel de Serum 2 GranularOsc, Grain/Simpler, Kontakt 8 etc. | Opcionais, **não** usados no vídeo: GranularOsc do Serum 2 ou **Grain** (gravando o drone e granulando) esfumaçam a cauda — textura, não afinação; Kontakt 8 (Ethereal Earth) pode servir de camada de fundo, mas isso já é composição, não a técnica ensinada. Simpler/Sampler não têm papel aqui: a fonte é síntese, não amostra. |

**Conclusão de traduzibilidade:** sim, integralmente. A técnica é 100% Live/Operator + macro; os racks do autor são conveniência, não dependência.

---

## Aplicação por função (kick, sub, baixo/rolling, hats/shaker, percussão de resposta, madeira, stab, subida, atmosfera)

Contexto de referência citado no levantamento original: um set de trabalho medido mostrou o meio carente (300–1.200 Hz e 1.200–4.000 Hz abaixo da média de 6 referências externas), low-end **mono** e groove com subdivisões deslocadas a preservar. Boas práticas de cama atmosférica: **HPF ~160 Hz no bus de FX/Atmos**, **notch ~320 Hz / ~1.2 kHz** na cama, e **corte de sub (<90 Hz)** num drone tonal âncora — há uma divergência real entre 90 Hz e 160 Hz nos trechos do levantamento; decidir por A/B no set. *(Valores de boa prática do estudo, não do vídeo.)*

*Cuidados da coluna direita são **INFERÊNCIA** a partir do vídeo + boas práticas de psytech, não estão no vídeo.*

| Função | O que aplicar (com base no vídeo) | Cuidado para não engordar sub nem criar brilho metálico |
|---|---|---|
| **Kick** | Nada do vídeo é dirigido ao kick. O drone deve ficar **contínuo e estável**, como ele descreve ("more like a steady drone", 00:21:06). | **Não** sidechainar o drone ao kick: ducking por kick cria pulso rítmico que o vídeo não tem e pode competir com o groove. Se mascarar, abaixe pelo macro de volume (00:10:56) ou por automação de arranjo. O próprio autor avisa para não embolar com baixo e kick (00:21:33). |
| **Sub** | Intocado. O vídeo não trata sub; o drone é harmônico e contínuo. | HPF no drone (90–160 Hz, ver acima). Abaixo de 120 Hz, **mono**. O detune do vídeo gera batimento: se sobrar energia grave, o batimento vira wobble contra o sub mono. |
| **Baixo/rolling** | Não coberto. A regra útil é de arranjo: o drone fica **fora do registro do rolling**. | Preservar o groove — **não** sincronizar o LFO do feedback ao grid (o vídeo usa LFO livre) e não aplicar delay rítmico no drone. Se houver máscara em 200–400 Hz, automação de volume no drone em vez de EQ cirúrgico no rolling. |
| **Hats/shaker** | Não coberto. O macro de shape (00:05:27) permite escolher sine/triangle em vez de square/saw quando o topo está ocupado (00:06:10–00:06:36). | É aqui que o shape square/saw + feedback alto criam **brilho metálico**. Para perfil escuro, preferir triangle/sine, feedback moderado e low-pass no topo do drone. Não usar o drone para "levantar" 1.2–4 kHz: o déficit se corrige com presença tonal (harmônicos de 300–1.200), não com aspereza. |
| **Percussão de resposta** | Não coberto. O princípio transferível é o drone como **fundo que não reage** a cada golpe. | Manter o drone estático durante a resposta; nada de reverb throw nem abertura de filtro no drone nesses tempos. Transiente de resposta tem de passar limpo. |
| **Madeira** | Não coberto, mas o miolo harmônico do drone (raiz + oitava + quinta, 00:03:22–00:03:42) ocupa a mesma faixa do corpo de madeira (300–1.200 Hz). | Usar o notch de ~320 Hz e **alternar** drone/madeira no arranjo (ou dip de 1–2 dB no drone quando a madeira entra). Empilhar os dois "para engordar" mascara a madeira e não resolve o vale de médios. |
| **Stab** | Não coberto. O drone é tonal; o vídeo o mantém em uma nota e move por macro. | Congelar o macro "space" (coarse) enquanto o stab toca — drift de pitch contra a tônica soa desafinado, não hipnótico. Detune pequeno no drone; nada de detune grande no momento do stab. |
| **Subida** | A mecânica de macro (space, shape, feedback) serve de **automação lenta** de textura (00:22:00–00:22:05 lista filter/LFO/feedback/pitch envelope como formas de variar). | Preferir **abertura de filtro** a subir pitch: subir o coarse leva o drone para registro agudo e metálico. Automação em 4–8 compassos, sem repique (riser de corte rítmico é vetado em boas práticas de psytech). |
| **Atmosfera** | **Alvo principal.** Operator parallel com 3–4 osciladores em ratios inteiros, macros de shape/detune/volume, feedback ~50% com LFO lento, filtro e **muito delay + reverb** (00:14:48). Volume de fundo, "they are not like in the front" (00:01:34–00:01:42). | Largura estéreo **só acima do HPF**; abaixo de 120 Hz mono. Reverb/delay em **send**, não 100% wet em série (a cauda longa ainda come o miolo). Notch ~1.2 kHz na cama atmosférica. |

**Receita mínima (INFERÊNCIA de aplicação, não está no vídeo):** começar com **um** Operator (não dois) em parallel, osciladores em 1×/2×/3× sobre a tônica da track (0/+12/+19), volumes decrescentes como no vídeo; uma macro de shape, uma de detune (tetos pequenos: 3–8, bem abaixo dos 26/34 dele, para não virar coro metálico) e uma de volume dos harmônicos. Entrar no início do arranjo em volume de fundo e abrir a macro de volume ao longo dos primeiros 8–16 compassos; o LFO de feedback fica livre e lento. Só depois avaliar o segundo Operator para o batimento entre camadas. Como teto de referência, um levantamento anterior fixou **0.35 (−9 dB)** para a cama de atmosfera durante solos — usar como referência, não como valor obrigatório.

---

## Prioridade e esforço

**Prioridade: alta (P1).** É a frente de **textura-atmosfera**: ataca o miolo medido como carente (300–1.200 e 1.200–4.000 Hz) com material **tonal** em vez de brilho, e o tipo de projeto psytech minimal já tende a ter um slot documentado de drone tonal âncora.

**Esforço: médio.** Um Operator com 3 osciladores + macros de shape/detune/volume é uma sessão curta (baixo). O que puxa para médio é o **mapeamento escalonado** do macro "space" (cada parâmetro com Min/Max próprio), o segundo Operator e o A/B de registro/EQ contra o sub mono e o groove deslocado. Não exige plugin novo nem download de rack.

---

## Trechos de prova: 3 citações literais da legenda com timestamp

1. **00:03:03.200–00:03:06.550** — "basically the idea was many so you get operator and i put in parallel mode"
2. **00:08:06.560–00:08:09.029** — "starting at one second one starting at two third one starting at three" *(o quarto valor completa no cue seguinte, literal: "and fourth one starting at four and this way now", 00:08:11.840–00:08:12.710)*
3. **00:12:39.120–00:12:41.670** — "i like to don't go more than 40. so basically what i will do is i"

*(Citações literais da legenda automática; erros de transcrição foram preservados de propósito. Outras passagens usadas no corpo: "destination b oscillator feedback i put it insane" (00:17:41.919–00:17:45.190); "you get this nice evolving bad kind of sound" (00:18:08.320–00:18:12.710); "but obviously you don't want you don't to be too sexy and to me mix up with you" (00:21:33.919–00:21:36.950) + "baseline and kick" (00:21:41.200); "there is no effect yet" (00:10:27.040).)*

**Limites desta dissecação:** a sessão original não abriu Live nem testou parâmetros. A lista de destinos do LFO interno do Operator não foi verificada (o manual não abriu: HTTP 404); por isso a tradução oferece o caminho seguro (LFO device/automação mapeado ao Feedback).
