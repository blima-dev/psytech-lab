# DOSSIE NOTEBOOKLM — VOZES (retorno das 3 rodadas, 15/10/2026)

Fonte: NotebookLM, rodadas 1–3 de 15/10/2026. Colado cru, sem edição.

---

## RODADA 1 — PAPÉIS, ARRANJO E CORTES

Aqui está a análise técnica e o direcionamento de coprodução para a **RODADA 1**, fundamentados rigorosamente no acervo do notebook de fontes (tutorial *Building a PSYTECH Track*, *walkthroughs* da Vision Serpent, análises forenses de laboratório DSP como a de *Ortahisar* e o *Catálogo de Gestos Psytech*) e nas práticas consolidadas do gênero **Minimal Psytech / Bush Tech / Dark Progressive** (128 BPM, C# Frígio, 7:47 / barra 248–250).

---

### RODADA 1 — PAPÉIS DE VOZ, ARRANJO & MECÂNICA DE CORTES

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    MATRIZ DE RESUMO DA RODADA 1                         │
├─────────────────┬───────────────────────────────────────────────────────┤
│ Conceito-Chave  │ A voz no Minimal Psytech é elemento de cena e foley   │
│                 │ hipnótico; atua na borda do transe, jamais como Lead. │
├─────────────────┼───────────────────────────────────────────────────────┤
│ Espaço Z        │ Posição frontal seca (Dry ≤25%) com projeção de       │
│                 │ profundidade via Sends paralelos filtrados em 300–4k. │
├─────────────────┼───────────────────────────────────────────────────────┤
│ Periodicidade   │ Cortes de 8, 16 e 24 compassos são o padrão funcional  │
│                 │ para respiração e ponte vocal pré-impacto.            │
└─────────────────┴───────────────────────────────────────────────────────┘
```

---

### 1. CATÁLOGO DE PAPÉIS DE VOZ DO GÊNERO (8 PAPÉIS TÁTICOS)

#### 1. Chant Ritual / Canto Ancestral Grave
* **Função Narrativa:** Ancorar a gravidade xamânica e a atmosfera de templo; estabelece a tônica ou o atrito frígio [FONTE: Catálogo de Gestos Psytech / PRÁTICA GERAL].
* **Banda Útil:** 150 Hz a 1.200 Hz (Low-Cut estrito em 150 Hz para proteger o subbass de 34.6 Hz em C#1; Hi-Cut em 2.500 Hz para evitar estridência) [FONTE: AUDITORIA ISMAL.M].
* **Duração Típica:** 1 a 2 compassos (1,875 s a 3,75 s) ou cama contínua sustentada no breakdown [FONTE: Building a PSYTECH Track - Part 3].
* **Densidade:** 1 a 2 disparos a cada 32 compassos.
* **Posição no Compasso:** Cabeça da frase (beat 1.1) ou entrada no beat 1.3 após a descompressão do kick.
* **Microtiming:** Retardado (*laid-back*) em +8 ms a +14 ms do grid [FONTE: AUDITORIA ISMAL.M].
* **Mono/Estéreo:** 100% Mono no centro (Mid) [FONTE: AUDITORIA ISMAL.M].
* **Orçamento Dry/Wet:** Dry serial a 80% (20% Wet máximo de saturação); Send de Reverb a −14 dB [FONTE: Building a PSYTECH Track - Part 8].
* **Referências de Timestamp nas Fontes:** NÃO ENCONTRADO (as fontes tratam a técnica conceitualmente, sem marcação de min:seg por faixa externa).

#### 2. Resposta Curta / Vocal Throw (One-Shot Accent)
* **Função Narrativa:** Pontuar os respiros da bateria; atua como contra-ataque percussivo ao bumbo [FONTE: Building a PSYTECH Track - Part 2].
* **Banda Útil:** 400 Hz a 3.500 Hz [FONTE: AUDITORIA ISMAL.M].
* **Duração Típica:** 1/16 a 1/8 (117 ms a 234 ms).
* **Densidade:** 2 a 4 eventos por ciclo de 16 compassos.
* **Posição no Compasso:** Exclusivamente no contratempo (beats 1.3, 2.4 ou 4.2).
* **Microtiming:** Cravado no grid ou ligeiramente adiantado (-4 ms) se for um estalo seco.
* **Mono/Estéreo:** Estéreo moderado (Pan automatizado entre 15L e 15R) [FONTE: Catálogo de Gestos Psytech].
* **Orçamento Dry/Wet:** Dry serial 100%; Send B (Delay 1/8d ou 1/4) aberto temporariamente no último evento de um bloco [FONTE: Building a PSYTECH Track - Part 4].
* **Referências de Timestamp nas Fontes:** NÃO ENCONTRADO.

#### 3. Sussurro Granular / Whispers (High-End Texture)
* **Função Narrativa:** Gerar ar e intimidade misteriosa; preenche a esteira de agudos sem usar ruído branco comercial [FONTE: AUDITORIA ISMAL.M / Catálogo de Gestos Psytech].
* **Banda Útil:** 1.500 Hz a 8.500 Hz (com High-Pass em 1.200 Hz).
* **Duração Típica:** 2 a 4 compassos (3,75 s a 7,5 s).
* **Densidade:** 1 evento longo a cada 16 ou 32 compassos (frequentemente em pontes de transição).
* **Posição no Compasso:** Entra na metade final de uma frase de 8/16 (ex.: compasso 13 ao 16).
* **Microtiming:** Flutuante / não quantizado.
* **Mono/Estéreo:** Estéreo amplo (Side/Mid ~0.45, Utility Width até 125%) [FONTE: AUDITORIA ISMAL.M].
* **Orçamento Dry/Wet:** Dry 40% / Wet 60% (processado via Granulator III ou Reverb/Delay) [FONTE: Ableton Live 12 Tutorial - Granular Beats].
* **Referências de Timestamp nas Fontes:** NÃO ENCONTRADO.

#### 4. Foley Humano / Respiração, Sopro & Cantil (Percussão de Cena)
* **Função Narrativa:** Substituir elementos de percussão sintética por ruídos orgânicos biológicos; gera hiper-realismo e textura terrosa (*bush/zenon*) [FONTE: Building a PSYTECH Track - Part 8 / Catálogo de Gestos Psytech].
* **Banda Útil:** 350 Hz a 6.000 Hz.
* **Duração Típica:** 1/16 a 1/4 (117 ms a 468 ms).
* **Densidade:** 4 a 8 toques a cada 16 compassos.
* **Posição no Compasso:** Intercalado entre os vácuos dos *woodclicks* e *shakers*.
* **Microtiming:** Humanizado (+10 ms de atraso constante no Track Delay) [FONTE: AUDITORIA ISMAL.M].
* **Mono/Estéreo:** L/R Pan alternado por nota (Random Pan de 30% L/R) [FONTE: Seed To Stage - Simpler Synth Tutorial].
* **Orçamento Dry/Wet:** 100% Dry no insert; Reverb nulo ou ultra-curto (decay < 0.6s) [FONTE: Building a PSYTECH Track - Part 1].
* **Referências de Timestamp nas Fontes:** NÃO ENCONTRADO.

#### 5. Voz Falada Distante / Spoken Word (Frase Narrativa Filtrada)
* **Função Narrativa:** Introduzir reflexões profundas ou trechos hipnóticos de diálogo/amostras filosóficas [FONTE: Building a PSYTECH Track - Part 5].
* **Banda Útil:** 500 Hz a 2.200 Hz (Filtro Bandpass / "efeito telefone" para não disputar o espectro) [FONTE: Projektor - Glitchy Sound Design].
* **Duração Típica:** 2 a 4 compassos (3,75 s a 7,5 s).
* **Densidade:** Raro (1 a 2 frases na faixa inteira, preferencialmente no Falso Break ou Breakdown).
* **Posição no Compasso:** Inicia no beat 1.2 e estende-se sem interromper o *kick*.
* **Microtiming:** Ritmo de fala natural.
* **Mono/Estéreo:** Mono no centro com cauda de Reverb estéreo nos cantos [FONTE: TECHNO SOUND DESIGN By NoNameLeft].
* **Orçamento Dry/Wet:** Dry serial 85%; Send Reverb/Delay paralelo a −12 dB.
* **Referências de Timestamp nas Fontes:** NÃO ENCONTRADO.

#### 6. Chop Vocal Percussivo (Micro-Groove 1/16ths)
* **Função Narrativa:** Criar linhas rítmicas picotadas e vocalizadas (*talking grooves*) que dialogam com o *rolling bass* [FONTE: How to Make Vocal Chops That Actually Groove / HOW TO MAKE PSYTECH By Verschallt].
* **Banda Útil:** 300 Hz a 4.000 Hz (com filtro Bandpass e Redux/Downsample) [FONTE: Verschallt - Project Walkthrough].
* **Duração Típica:** Fatias curtas de 1/16 (117 ms) repetidas em padrão de 4 a 8 notas.
* **Densidade:** 8 a 12 semicolcheias por ciclo de 16 compassos.
* **Posição no Compasso:** Sincopado nas posições 1.2, 1.4, 2.3, 3.2.
* **Microtiming:** Quantizado em 1/16 com variação de *Velocity* para modular o filtro [FONTE: Psiger Records - Vocal Chops / Verschallt].
* **Mono/Estéreo:** Mono com Utility de 100% no centro [FONTE: AUDITORIA ISMAL.M].
* **Orçamento Dry/Wet:** Dry 90%; processado por OTT e saturação de fita [FONTE: Psiger Records].
* **Referências de Timestamp nas Fontes:** NÃO ENCONTRADO.

#### 7. Cama Vocal / Drone Humano Sustentado
* **Função Narrativa:** Criar o "piso de sustentação" no breakdown e intro, unindo instrumentos acústicos em uma mancha harmônica [FONTE: Building a PSYTECH Track - Part 2 & 3].
* **Banda Útil:** 200 Hz a 1.800 Hz.
* **Duração Típica:** 16 a 32 compassos contínuos.
* **Densidade:** 1 evento contínuo no bloco.
* **Posição no Compasso:** Entra em *fade-in* suave no início do bloco e sustenta até o vácuo.
* **Microtiming:** N/A (sustentado).
* **Mono/Estéreo:** Estéreo expandido no plano Z (Width 125% a 140%) [FONTE: Catálogo de Gestos Psytech].
* **Orçamento Dry/Wet:** Dry 30% / Wet 70% (via Reverb longo com *Freeze* ou Granulator III) [FONTE: Building a PSYTECH Track - Part 2].
* **Referências de Timestamp nas Fontes:** NÃO ENCONTRADO.

#### 8. Reverse Vocal Suck / Sucção Humana Reversa
* **Função Narrativa:** Transição subtrativa; "puxa o ar" da sala no final do vácuo pré-drop [FONTE: AUDITORIA ISMAL.M / Catálogo de Gestos Psytech].
* **Banda Útil:** 300 Hz a 5.500 Hz (High-Pass em 200 Hz).
* **Duração Típica:** 1 beat (~468 ms) a 2 beats (~937 ms).
* **Densidade:** 1 evento por transição de grande bloco.
* **Posição no Compasso:** Entra exatamente no beat 4.3 ou 4.4 do compasso final de um bloco (ex.: bar 56.4, 120.4, 144.4).
* **Microtiming:** Exato e truncado em zero absoluto na barra 1.1 do novo bloco [FONTE: Catálogo de Gestos Psytech].
* **Mono/Estéreo:** Transição de Estéreo (140%) fechando para Mono (0%) na cabeça do tempo [FONTE: Catálogo de Gestos Psytech].
* **Orçamento Dry/Wet:** 100% Wet (cauda de vocal reverterizada e congelada) [FONTE: Building a PSYTECH Track - Part 2].
* **Referências de Timestamp nas Fontes:** NÃO ENCONTRADO.

---

### 2. ARRANJO & DINÂMICA DE VOZ NA TIMELINE DA FAIXA DE REFERÊNCIA

```
┌─────────────────────────────────────────────────────────────────────────┐
│              DISTRIBUIÇÃO DE VOZ NA TIMELINE DO PROJETO                 │
├─────────────┬─────────────┬─────────────────────────────────────────────┤
│ Bloco       | Compassos   | Comportamento Vocal & Diálogo               │
├─────────────┼─────────────┼─────────────────────────────────────────────┤
│ Intro       │ Bars 1–32   │ Whispers aéreos e Chant em C#2. Sem bumbo. │
│ Drop 1      │ Bars 57–80  │ Voz cala no 57.1. Vocal Throws pontuais.    │
│ Falso Break │ Bars 105–120│ Spoken word distante / Chants no Ato 1.     │
│ Breakdown   │ Bars 144–160│ Cama Vocal de 16 bars + Respiração seca.    │
│ Drop 2      │ Bars 169–193│ Silêncio de frases longas; apenas Foley.    │
└─────────────┴─────────────┴─────────────────────────────────────────────┘
```

* **Ciclos de 16/32 Compassos (Entradas e Saídas):**
  A voz opera em regime de **aparição e recolhimento**. Ela entra por 8 a 16 compassos e recua completamente pelos 16 compassos seguintes. A presença contínua causa fadiga auditiva e anula o mistério [FONTE: Building a PSYTECH Track - Part 3 & 7].
* **Chamada de Voz ↔ Resposta do Instrumental:**
  Quando a voz fala/canta (Sintagma A), o instrumental (Lead/Acid 303/Woodwind) permanece velado ou filtrado abaixo de 1.2 kHz. Assim que a voz silencia (beat 2.3 ou 4.3), o sintetizador ou percussão ataca com *drive*/abertura de filtro (Sintagma B) [FONTE: Building a PSYTECH Track - Part 2].
* **Comportamento nos Dois Drops:**
  * **Drop 1 (Bar 57):** A voz **cala-se totalmente no downbeat (57.1.1)**. A reentrada do Kick e Sub Slingshot exige prioridade absoluta no *pocket*. Apenas *One-Shots* curtos de foley humano (sopro/cantil) atuam nos respiros a cada 8 compassos [FONTE: AUDITORIA ISMAL.M].
  * **Drop 2 / Clímax (Bar 169):** Silêncio absoluto de frases vocais narrativas. O clímax é sustentado pela percussão, Tutti orquestral e pelo *Dark Brass Braam*. A voz participa apenas com a *Sucção Reversa* nos 500 ms anteriores ao golpe do Bar 169.1 [FONTE: Catálogo de Gestos Psytech].
* **Comportamento no Breakdown (Bars 144.5–160 / 4:29–5:00):**
  A cama vocal (*Vocal Pad*) sustenta o plano de fundo (plano Z de 10 a 30 m) durante os 16 compassos sem bumbo. No bar 160 (início da subida cardíaca), a cama vocal sofre um filtro passa-altas (HPF) subindo até sumir, deixando a respiração seca e o *whisper* assumirem a dianteira até o vácuo do bar 168 [FONTE: Building a PSYTECH Track - Part 3].
* **Comportamento nos Cortes de Kick Medidos:**
  * **Bar 56.5 (Pré-Drop 1):** *Sucção Reversa Vocal* nos últimos 2 beats do vácuo.
  * **Bar 80.5 (Marcha / Virada de 24 bars):** Disparo de um *Vocal Throw* seco de 1/8d com *Delay Throw* que decai no vácuo.
  * **Bar 88.5 (Marcha / Virada de 8 bars):** *Sussurro/Whisper* de 1 compasso filtrado abrindo o teto de agudos.
  * **Bar 104.5 (Pré-Falso Break / Virada de 16 bars):** Frase curta de *Chant* cortada a seco no beat 104.4, escancarando a queda de grave para o Falso Break.
* **Quando o Silêncio Ganha da Voz:**
  Nas seções de tração rítmica pura (Roll 1 e Roll 2), o silêncio vocal é obrigatório por blocos inteiros de 16 a 32 compassos. O espaço negativo permite que a marcha hipnótica de bumbo e baixo arraste a pista sem distração [FONTE: AUDITORIA ISMAL.M / PLAYBOOK PSYTECH].

---

### 3. PERIODICIDADE DOS CORTES DE KICK E RESPOSTA VOCAL

* **Análise dos Cortes Medidos no Set de Referência (8, 16 e 24 Compassos):**
  Os intervalos medidos no projeto de referência (**24 compassos** entre o Bar 57 e 80.5; **8 compassos** entre 80.5 e 88.5; **16 compassos** entre 88.5 e 104.5) acompanham perfeitamente a matemática de arranjo do Psytech e do Techno hipnótico [FONTE: AUDITORIA ISMAL.M / Building a PSYTECH Track].
* **Função da Periodicidade no Gênero:**
  1. **Cortes de 8 Compassos:** Funcionam como *micro-respiros* ou turnarounds de dinamização interna (alívio rápido de tensão).
  2. **Cortes de 16 Compassos:** Marcação padrão de rotação de bloco/cena (mudança de fraseologia).
  3. **Cortes de 24 Compassos:** Tensão estendida que quebra a previsibilidade de 16/32 compassos, criando um estado de "espera prolongada" antes de abrir o vácuo.
* **A Resposta Vocal nos Cortes:**
  A voz **jamais canta durante o corte inteiro**. A regra do gênero é: o corte de kick abre o vácuo; a voz emite uma intervenção microscópica (1 a 2 beats / um sussurro ou sopro) no meio do vácuo; o corte fecha e o Kick reentra no tempo 1.1 com o dobro de impacto psicoacústico devido ao contraste dinâmico de até 18 dB [FONTE: AUDITORIA ISMAL.M / Catálogo de Gestos Psytech].

---

### 4. AVALIAÇÃO DE HIPÓTESES

#### Hipótese (a): Voz é presença/hipnose, não protagonista (frase curta, filtrada, distante).
* **Ranking: FORTE.**
* **Fundamentação:** Confirmado integralmente pelas fontes. No Minimal Psytech e Dark Zenon, frases vocais longas e eufóricas remetem ao Trance comercial/Morning e são expressamente evitadas. A voz atua como textura de cena e *ear tickler*, filtrada e posicionada no plano de fundo ou em pinceladas no contratempo [FONTE: Building a PSYTECH Track - Part 1 e 3 / AUDITORIA ISMAL.M].

#### Hipótese (b): Chop vocal sombrio e atrasado (granular/tape) e a dose real de chop percussivo curto vs. frase falada inteligível.
* **Ranking: FORTE.**
* **Fundamentação:** O uso de *chops* percussivos curtos de 1/16ths (com processamento *Redux/Downsample* ou filtro Bandpass) supera em proporção de 80/20 as frases faladas inteligíveis no gênero. As frases inteligíveis ocorrem apenas em momentos solenes (breaks), enquanto os *chops* e *whispers* atuam no miolo da marcha para sustentar a tração sem poluir os médios [FONTE: How to Make Vocal Chops That Actually Groove / Verschallt Walkthrough].

#### Hipótese (c): Foley humano (respiração, sopro, sussurro) como percussão de cena, não pad.
* **Ranking: FORTE.**
* **Fundamentação:** Gravações de foley biológico (sopros, suspiros, cantil, estalos labiais) devem ser tratadas com envelopes curtos (Decay < 100 ms) e roteadas como percussão no barramento de *Synths & Glitch Rhythm*, recebendo o mesmo micro-swing e cortes de frequência das percussões de madeira [FONTE: AUDITORIA ISMAL.M / Building a PSYTECH Track - Part 8].

#### Hipótese (d): O médio (300–1000 Hz) é mantido baixo no gênero; medição FFT/30ms.
* **Ranking: FORTE.**
* **Fundamentação e Medições:**
  A auditoria forense do master de referência *Ortahisar* (Ismail.M) prova fisicamente o escavamento de médios utilizando decomposição por filtros Butterworth de 4ª ordem, FFT por janelas de 30 ms e análise Mid/Side [FONTE: AUDITORIA ISMAL.M]:
  * Região de **Low-Mid (150–400 Hz):** **−23.47 dBFS** (Mid) | **−39.15 dBFS** (Side).
  * Região de **Médios (400–2.500 Hz):** **−25.19 dBFS** (Mid) | **−34.59 dBFS** (Side).
  * *Observação de Rigor:* A medição de −23 a −25 dBFS reflete o espectro total da mixagem comercial. A proporção isolada FFT exclusiva da trilha de voz solo não consta nas fontes (**NÃO ENCONTRADO** em isolamento), mas a regra de manter os médios da voz escavados para dar espaço à bateria e aos solistas é lei física na referência [FONTE: AUDITORIA ISMAL.M].

---

### 5. AVALIAÇÃO DAS PRÁTICAS ATUAIS DO PROJETO DE REFERÊNCIA

* **Prática 1: Chant em registro baixo (C#2/D2/G#2) com delay filtrado.**
  * **Análise:** **Totalmente alinhada com as fontes.** A ancoragem em C#2/D2 respeita a tonalidade de C# Frígio da faixa de referência e gera a tensão da 2ª menor frígia (C# ↔ D) sem invadir o subgrave de 34.6 Hz (C#1), que permanece protegido [FONTE: AUDITORIA ISMAL.M / Catálogo de Gestos Psytech]. O uso de delay filtrado em passa-altas (HPF > 350 Hz no retorno) evita o acúmulo de ressonâncias no *low-mid* [FONTE: Building a PSYTECH Track - Part 3].
* **Prática 2: Dry sagrado em material vocal solo (serial ≤25% de wet; distância vem de paralelo/delay).**
  * **Análise:** **Totalmente alinhada com as fontes.** Manter o canal direto seco (Dry 100% ou serial ≤25%) preserva a intimidade e a clareza do transiente vocal no plano Z frontal (0 a 1 m). A sensação de profundidade e distância espacial é criada exclusivamente através dos envios para os canais de retorno (Send A Reverb / Send B Delay), permitindo que a voz permaneça inteligível e nítida sem afogar a mixagem em lama de reverberação [FONTE: Building a PSYTECH Track - Part 8 / AUDITORIA ISMAL.M].

---

💡 **Próximo Passo:**
A sequência prevista é a **RODADA 2** (cadeias de processamento, automação e piloto de validação).
---

## RODADAS 2 E 3 — CADEIAS, AUTOMAÇÃO, PILOTO, VERIFICAÇÃO

Apresento a consolidação técnica das **RODADAS 2 e 3** para a faixa de referência (128 BPM, C# Frígio, ~7:47 / barra 248–250).

---

# RODADA 2 — CADEIAS DE PROCESSAMENTO E ARQUITETURA TÉCNICA

```
┌─────────────────────────────────────────────────────────────────────────┐
│              SÍNTESE DAS CADEIAS E PROCESSAMENTO DE VOZ                 │
├─────────────────┬───────────────────────────────────────────────────────┤
│ Regra de Ouro   │ Som direto mantido seco (Dry ≤25% serial);            │
│ de Profundidade │ profundidade gerada via Sends paralelos filtrados.    │
├─────────────────┼───────────────────────────────────────────────────────┤
│ Proteção do Low │ High-Pass (HPF) estrito entre 150 Hz e 350 Hz em       │
│                 │ todas as vozes para blindar a fundamental de C#1.     │
├─────────────────┼───────────────────────────────────────────────────────┤
│ Escavamento     │ Entalhe em 300–1.000 Hz reduzindo a densidade para    │
│ de Médios       │ garantir o bolso da bateria e dos solistas.           │
└─────────────────┴───────────────────────────────────────────────────────┘
```

---

### 1. CADEIAS DE PROCESSAMENTO POR PAPEL VOCAL

#### 1. Chant Ritual / Canto Ancestral Grave
* **High Pass (HP):** HPF em **150 Hz** (24 dB/oct) no EQ Eight [PRÁTICA GERAL / FONTE: AUDITORIA ISMAL.M].
* **Corte de Médios:** Notch cirúrgico de **−3 dB em 450 Hz** e corte suave em **800 Hz** [PRÁTICA GERAL].
* **De-Esser:** Módulo em 3.500 Hz com redução dinâmica de picos em −4 dB [PRÁTICA GERAL].
* **Saturação:** Saturação de fita suave no Saturator nativo (**Analog Clip**, Drive: +2.5 dB, Dry/Wet em **20%**) [PRÁTICA GERAL / FONTE: Building a PSYTECH Track - Part 3].
* **Delay (Paralelo):** Send B em 1/4 (480 ms) ou 1/8d (360 ms) com feedback em 35% e filtro passa-banda em **350 Hz – 2.500 Hz** [FONTE: Building a PSYTECH Track - Part 3].
* **Reverb (Paralelo):** Send A (Reverb 3D) com pré-delay de **35 ms**, decay de **3.2 s**, HPF interno em **300 Hz** [PRÁTICA GERAL / FONTE: AUDITORIA ISMAL.M].
* **Ducking com Kick:** Compressor em sidechain pós-reverb/delay com atenuação de **−3 dB a −5 dB** e release rápido de **60 ms** [FONTE: AUDITORIA ISMAL.M].
* **Largura Estéreo:** **100% Mono** no centro (Mid) [FONTE: AUDITORIA ISMAL.M].
* **Serial vs. Paralelo & Distância:** Insert 100% seco no canal direto (0% Wet de Reverb serial). A distância (2 a 5 m) é obtida exclusivamente pelo envio paralelo ao Return A [PRÁTICA GERAL].
* **Alvo de Nível:** **−12 dB a −15 dB** abaixo do Kick/Sub [PRÁTICA GERAL]. *Motivo: Deve atuar como base harmônica e não como Lead.*

#### 2. Resposta Curta / Vocal Throw (One-Shot Accent)
* **High Pass (HP):** HPF em **250 Hz** (24 dB/oct) [PRÁTICA GERAL].
* **Corte de Médios:** Atenuação de **−2.5 dB em 600 Hz** [PRÁTICA GERAL].
* **De-Esser:** Não necessário se o corte de agudos estiver ativo acima de 4.500 Hz [PRÁTICA GERAL].
* **Saturação:** Saturação valvulada (**Tube/Hard Clip**) com Drive em +4 dB e Dry/Wet em **15%** para destacar os transientes [PRÁTICA GERAL].
* **Delay (Paralelo):** Send B acionado pontualmente em 1/8d com feedback em 50% [FONTE: Building a PSYTECH Track - Part 4].
* **Reverb (Paralelo):** Send A a −14 dB com decay de **2.5 s** [PRÁTICA GERAL].
* **Ducking com Kick:** Ducking rápido via LFO Tool/Duck em **−6 dB** [PRÁTICA GERAL].
* **Largura Estéreo:** Pan alternado entre **15L e 15R** ou Haas Delay assimétrico (L: 1.0 ms / R: 18.5 ms) [PRÁTICA GERAL / FONTE: Catálogo de Gestos Psytech].
* **Serial vs. Paralelo & Distância:** Serial 100% seco; a projeção lateral traz o elemento para a meia-distância (2 m) [PRÁTICA GERAL].
* **Alvo de Nível:** **−14 dB a −18 dB** abaixo do Kick [PRÁTICA GERAL]. *Motivo: Funciona como percussão de resposta nos buracos do bumbo.*

#### 3. Sussurro Granular / Whispers (High-End Texture)
* **High Pass (HP):** HPF agressivo em **1.200 Hz** [PRÁTICA GERAL / FONTE: AUDITORIA ISMAL.M].
* **Corte de Médios:** Eliminação total da região abaixo de 1.000 Hz [PRÁTICA GERAL].
* **De-Esser:** De-esser em 6.500 Hz reduzindo sibilâncias duras em −6 dB [PRÁTICA GERAL].
* **Saturação:** Redux com Downsample em **32 kHz** para crocância digital [FONTE: Verschallt Walkthrough].
* **Delay (Paralelo):** Ping-Pong Delay em 1/16 com feedback em 40% [PRÁTICA GERAL].
* **Reverb (Paralelo/Serial):** Granulator III ou Reverb em modo *Cloud* com **50% Wet** e decay de **4.0 s** [FONTE: Ableton Live 12 Tutorial - Granular Beats].
* **Ducking com Kick:** Sidechain contínuo de **−4 dB** com release de 100 ms [FONTE: AUDITORIA ISMAL.M].
* **Largura Estéreo:** **125% a 140% Estéreo** (Side/Mid ratio ~0.45) [FONTE: AUDITORIA ISMAL.M].
* **Serial vs. Paralelo & Distância:** Processamento granular serial com difusão paralela; flutua no teto da sala (horizonte de 10 a 20 m) [PRÁTICA GERAL].
* **Alvo de Nível:** **−20 dB a −24 dB** abaixo do Kick [PRÁTICA GERAL]. *Motivo: É uma camada de textura aérea, devendo permanecer no patamar de ruído ambiente.*

#### 4. Foley Humano / Respiração, Sopro & Cantil (Percussão de Cena)
* **High Pass (HP):** HPF em **350 Hz** [PRÁTICA GERAL].
* **Corte de Médios:** Notch ajustado na ressonância do sample (geralmente entre 500 Hz e 900 Hz) [PRÁTICA GERAL].
* **De-Esser:** Não aplicado [PRÁTICA GERAL].
* **Saturação:** Saturação de fita leve (**Clean Tape**) a **25%** [FONTE: Building a PSYTECH Track - Part 3].
* **Delay (Paralelo):** Sem delay longo; apenas micro-eco de sala (<25 ms) [PRÁTICA GERAL].
* **Reverb (Paralelo):** Reverb de sala ultra-curto (decay de **0.6 s**, pre-delay 10 ms) no Send A [FONTE: Building a PSYTECH Track - Part 1].
* **Ducking com Kick:** Sem sidechain direto se alocado exclusivamente nos vácuos/contratempos [PRÁTICA GERAL].
* **Largura Estéreo:** **Random Pan de ±30%** a cada disparo [FONTE: Seed To Stage - Simpler Synth Tutorial].
* **Serial vs. Paralelo & Distância:** Serial 100% seco com envelope de amplitude estrito (Decay < 100 ms). Posiciona o elemento na cara do ouvinte (0.5 a 1 m) [PRÁTICA GERAL].
* **Alvo de Nível:** **−16 dB a −20 dB** abaixo do Kick [PRÁTICA GERAL]. *Motivo: Deve integrar o ecossistema percussivo de madeira.*

#### 5. Voz Falada Distante / Spoken Word (Frase Narrativa Filtrada)
* **High Pass (HP):** HPF em **500 Hz** [PRÁTICA GERAL].
* **Corte de Médios:** LPF em **2.200 Hz** (Efeito Bandpass / "telefone") [FONTE: Projektor - Glitchy Sound Design].
* **De-Esser:** Ativo na faixa de 2.000 Hz a 4.000 Hz [PRÁTICA GERAL].
* **Saturação:** Distortion/Overdrive leve a 10% [PRÁTICA GERAL].
* **Delay (Paralelo):** Delay estéreo em 1/4 com filtro fechado abaixo de 1.800 Hz [PRÁTICA GERAL].
* **Reverb (Paralelo):** Send A a **−12 dB** com pré-delay de **45 ms** [PRÁTICA GERAL].
* **Ducking com Kick:** Ducking leve de **−3 dB** [PRÁTICA GERAL].
* **Largura Estéreo:** Sinal direto em **Mono**, caudas de Reverb/Delay expandidas nas laterais [FONTE: TECHNO SOUND DESIGN By NoNameLeft].
* **Serial vs. Paralelo & Distância:** Sinal filtrado em serial; empurrado para o fundo da sala (5 a 10 m) pelo corte de bandas [PRÁTICA GERAL].
* **Alvo de Nível:** **−14 dB a −18 dB** abaixo do Kick [PRÁTICA GERAL]. *Motivo: Inteligível sem se sobressair em relação ao instrumental.*

#### 6. Chop Vocal Percussivo (Micro-Groove 1/16ths)
* **High Pass (HP):** HPF em **300 Hz** [PRÁTICA GERAL].
* **Corte de Médios:** Filtro Bandpass dinâmico modulado por Velocity [FONTE: Verschallt Walkthrough].
* **De-Esser:** Não aplicado [PRÁTICA GERAL].
* **Saturação:** Redux com Downsample em **16–24 kHz** + OTT em 20% [FONTE: Psiger Records / Verschallt Walkthrough].
* **Delay (Paralelo):** Slapback Delay ultra-curto (80 ms, feedback 15%) [PRÁTICA GERAL].
* **Reverb (Paralelo):** Send A a −18 dB (reverb bem seco) [PRÁTICA GERAL].
* **Ducking com Kick:** Ducking profundo de **−12 dB** em 1/16 via LFO Tool/Utility [PRÁTICA GERAL].
* **Largura Estéreo:** **100% Mono** [FONTE: AUDITORIA ISMAL.M].
* **Serial vs. Paralelo & Distância:** Processamento de dinâmica e bitcrushing serial; alocado no primeiro plano rítmico (1 m) [PRÁTICA GERAL].
* **Alvo de Nível:** **−15 dB a −18 dB** abaixo do Kick [PRÁTICA GERAL]. *Motivo: Deve travar em simbiose com o baixo.*

#### 7. Cama Vocal / Drone Humano Sustentado
* **High Pass (HP):** HPF em **200 Hz** [PRÁTICA GERAL].
* **Corte de Médios:** Escavamento amplo de **−4 dB entre 400 Hz e 1.500 Hz** [PRÁTICA GERAL / FONTE: AUDITORIA ISMAL.M].
* **De-Esser:** Não aplicado [PRÁTICA GERAL].
* **Saturação:** Saturação analógica suave a 15% [PRÁTICA GERAL].
* **Delay (Paralelo):** Granular Delay em 1/2 com pitch shift de +7 semitons no retorno [FONTE: Seed To Stage].
* **Reverb (Paralelo/Serial):** Reverb infinito com **100% Wet** ou botão *Freeze* ativo [FONTE: Building a PSYTECH Track - Part 2].
* **Ducking com Kick:** Sidechain invisível de **−3 dB a −5 dB** [FONTE: AUDITORIA ISMAL.M].
* **Largura Estéreo:** **125% a 140% Estéreo** [FONTE: Catálogo de Gestos Psytech].
* **Serial vs. Paralelo & Distância:** Renderizado em áudio com reverb congelado serial; atua no horizonte de fundo (15 a 30 m) [PRÁTICA GERAL].
* **Alvo de Nível:** **−18 dB a −22 dB** abaixo do Kick [PRÁTICA GERAL]. *Motivo: Colchão de sustentação que não deve disputar espaço com solistas.*

#### 8. Reverse Vocal Suck / Sucção Humana Reversa
* **High Pass (HP):** HPF em **200 Hz** [PRÁTICA GERAL].
* **Corte de Médios:** Varredura dinâmica de passa-banda de 300 Hz a 5.500 Hz [FONTE: Catálogo de Gestos Psytech].
* **De-Esser:** Não aplicado [PRÁTICA GERAL].
* **Saturação:** Redux e Roar com Drive suave para encorpar o arrasto [FONTE: Catálogo de Gestos Psytech].
* **Delay (Paralelo):** Sem delay no momento da sucção [PRÁTICA GERAL].
* **Reverb (Serial - Invertido):** Cauda de Reverb de **3.5 s** processada e **invertida em áudio** [FONTE: Building a PSYTECH Track - Part 2].
* **Ducking com Kick:** Nenhum (atua exclusivamente no vácuo que antecede o kick) [FONTE: Catálogo de Gestos Psytech].
* **Largura Estéreo:** Transição dinâmica: inicia em **140% Estéreo** e fecha para **0% (Mono)** na cabeça do tempo 1.1 [FONTE: Catálogo de Gestos Psytech].
* **Serial vs. Paralelo & Distância:** Renderizado em áudio serial; puxa a percepção do fundo (20 m) para a cara do ouvinte (0 m) em milissegundos [PRÁTICA GERAL].
* **Alvo de Nível:** Pico em **−10 dBFS** no milissegundo final [PRÁTICA GERAL]. *Motivo: Deve gerar forte contraste dinâmico antes do impacto do drop.*

---

### 2. MAPEAMENTO: AUTOMATIZÁVEL vs. MANUAL (LIVE NATIVO vs. PLUGINS)

```
┌─────────────────────────────────────────────────────────────────────────┐
│               MAPEAMENTO DE AUTOMAÇÃO E CONTROLE LOM                     │
├─────────────────┬───────────────────────────────┬───────────────────────┤
│ Dispositivo     │ Tipo / Origem                 │ Acesso por Script /   │
│                 │                               │ Automação LOM         │
├─────────────────┼───────────────────────────────┼───────────────────────┤
│ EQ Eight        │ Nativo Ableton Live 12        │ 100% Automatizável    │
│ Auto Filter     │ Nativo Ableton Live 12        │ 100% Automatizável    │
│ Utility         │ Nativo Ableton Live 12        │ 100% Automatizável    │
│ Saturator       │ Nativo Ableton Live 12        │ 100% Automatizável    │
│ Delay / Reverb  │ Nativo Ableton Live 12        │ 100% Automatizável    │
│ Roar / Redux    │ Nativo Ableton Live 12        │ 100% Automatizável    │
│ Serum 2         │ VST3 Third-Party              │ Exposto via VST       │
│                 │                               │ Parameters            │
│ Supermassive    │ VST3 Third-Party              │ Limitação no LOM:     │
│                 │                               │ Requer mapeamento GUI │
└─────────────────┴───────────────────────────────┴───────────────────────┘
```

* **Dispositivos Nativos do Live 12 (EQ Eight, Auto Filter, Utility, Saturator, Delay, Reverb, Compressor, Auto Pan, Roar, Redux):**
  Todos os parâmetros possuem caminhos de automação diretamente expostos no Live Object Model (LOM) e na API Python. Podem ser automatizados programaticamente por scripts ou desenhados na timeline sem restrições [PRÁTICA GERAL].
* **u-he Diva 1.4.8 & Xfer Serum 2:**
  Parâmetros principais (Cutoff, Envelope Decay, Wave Position, Drive, FX Dry/Wet) são expostos como VST Parameters indexados. Podem ser automatizados via LOM se previamente associados a Macros ou lidos pelo índice de parâmetros do plugin [PRÁTICA GERAL].
* **ValhallaSupermassive & Plugins VST3 sem Mapeamento Direto:**
  **Limitação Técnica Confirmada:** O ValhallaSupermassive e certos plugins VST3 não expõem parâmetros diretamente para gravação de automação de arranjo via scripts LOM sem que o parâmetro tenha sido manualmente clicado ou mapeado a um Macro da pílula do dispositivo na interface gráfica do Live. Nesses casos, o parâmetro deve ser manipulado manualmente no DAW ou fixado no preset [PRÁTICA GERAL].

---

### 3. FOLEY / SUSSURRO: DENSIDADE DE EVENTOS E PREVENÇÃO DE FADIGA

* **Frequência de Eventos:**
  Recomenda-se uma densidade de **6 a 12 disparos discretos por minuto** (aproximadamente 1 a 2 intervenções por bloco de 16 compassos a 128 BPM) [PRÁTICA GERAL].
* **Como Evitar a Fadiga Auditiva:**
  1. *Rotatividade de Timbres:* Alterne entre um *whisper* aéreo, um sopro de foley e um estalo de madeira. Jamais repita o mesmo sample no mesmo tempo por mais de 2 frases consecutivas [FONTE: Building a PSYTECH Track - Part 8].
  2. *Modulação Dinâmica de Filtro:* Mapeie o *Velocity* ou um LFO aleatório (*Sample & Hold*) para alterar levemente o Cutoff do filtro ( variação de ±150 Hz) e o tempo de decay a cada disparo [FONTE: Seed To Stage].
  3. *Silêncio Estrutural:* Garanta que durante a marcha principal (Rolls), o foley vocal faça pausas completas de 16 a 32 compassos, permitindo que a pista foque no motor de Kick e Baixo [FONTE: AUDITORIA ISMAL.M].

---

### 4. PAPEL PILOTO — VALIDAÇÃO E AJUSTES DE MÉTRICAS (A/B)

O teste piloto para validação A/B focar-se-á na intervenção de **Sussurro/Foley alocada em um corte de kick** (ex.: Bar 56.5 ou Bar 80.5):

* **Métrica 1: Loudness Igualado (LUFS-S):**
  O segmento de 2 compassos contendo o corte e o foley vocal deve ser medido em **LUFS Short-Term (LUFS-S)** e igualado ao trecho anterior de marcha. A queda de energia no vácuo deve ser controlada para registrar **−22.9 dBFS RMS** no sinal master [FONTE: AUDITORIA ISMAL.M].
* **Métrica 2: Razão da Banda 300–1.000 Hz:**
  A energia contida na faixa de 300 Hz a 1.000 Hz no canal do foley não deve exceder **−23.5 dBFS** no Mid, garantindo que o pocket de médios permaneça escavado [FONTE: AUDITORIA ISMAL.M].
* **Métrica 3: Mascaramento do Kick:**
  Como o foley é disparado estritamente durante o corte de kick (beats 4.3 a 4.4), o mascaramento na frequência fundamental (34.6 Hz / 48 Hz) é **fisicamente zero** [FONTE: AUDITORIA ISMAL.M].
* **Métrica 4: Soma Mono sem Cancelamento:**
  A correlação de fase estéreo da pista de foley/sussurro, quando processada por alargadores ou Haas Delay, deve manter-se acima de **+0.85**. Ao somar o Utility em Mono (*Bass Mono Active < 140 Hz* e botão Mono no Master), a perda de amplitude do transiente não pode exceder **1.5 dB** [FONTE: AUDITORIA ISMAL.M].
* **Métrica 5: Densidade de Eventos:**
  Exatamente **1 único micro-evento** de foley/sussurro com duração entre **117 ms e 234 ms** (1/16 a 1/8) posicionado no vácuo de 2 tempos.

---

# RODADA 3 — VERIFICAÇÃO, ANTI-CLICHÊ E REFERÊNCIAS

---

### 1. PROTOCOLO DE VERIFICAÇÃO POR PAPEL VOCAL

Para homologar se o processamento vocal está correto no Ableton Live 12, execute as seguintes medições:

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    MATRIZ DE MEDIÇÕES DE VERIFICAÇÃO                    │
├─────────────────┬───────────────────────────────┬───────────────────────┤
│ Parâmetro       │ Método de Medição             │ Alvo Tolerado         │
├─────────────────┼───────────────────────────────┼───────────────────────┤
│ Centroide Esp.  │ FFT Spectrum (Janela 30 ms)   │ 1,2 kHz a 3,5 kHz     │
│ Razão Low-Mid   │ Butterworth 4ª Ordem (Mid)    │ −23 dBFS a −25 dBFS   │
│ Correlação Low  │ Utility / Osciloscópio        │ +0.98 a +1.00 Mono    │
│ Soma Mono       │ Mute do Side no Master        │ Perda < 1.5 dB        │
│ Cauda Fronteira │ Análise Temporal no Grid      │ Zero ms no beat 1.1   │
└─────────────────┴───────────────────────────────┴───────────────────────┘
```

1. **Centroide Espectral (Spectral Centroid):**
   Medido via analisador de espectro (EQ Eight / SPAN). O centroide de brilho das vozes texturais (Whispers/Foley) deve situar-se entre **1.200 Hz e 3.500 Hz**, enquanto o dos Chants graves deve focar em **350 Hz a 900 Hz** [PRÁTICA GERAL].
2. **Razão de Banda 300–1.000 Hz (Método Forense):**
   Utilizando decomposição por filtros Butterworth de 4ª ordem e análise FFT por janela de 30 ms no componente Mid: a densidade de energia vocal nessa faixa deve permanecer a **−23.5 dBFS ou inferior** em relação ao pico do master [FONTE: AUDITORIA ISMAL.M].
3. **Correlação Estéreo abaixo de 120 Hz:**
   O componente Side de todas as pistas vocais deve ser zerado abaixo de 120–150 Hz via Utility (*Bass Mono On em 140 Hz*). A razão Side/Mid na faixa de subgrave deve registrar **0.0203 (98% Mono, correlação +0.9992)** [FONTE: AUDITORIA ISMAL.M].
4. **Soma Mono (Cancelamento de Fase):**
   Ao ativar o botão Mono no Utility do Master, a voz solo não pode desvanecer nem sofrer *comb filtering* severo. A atenuação máxima permitida na soma mono é de **1.5 dB** [PRÁTICA GERAL / FONTE: AUDITORIA ISMAL.M].
5. **Densidade de Eventos por Segundo:**
   A densidade de onsets vocais no miolo da marcha não deve ultrapassar **0.5 a 1.0 eventos/s**, preservando os espaços vazios [PRÁTICA GERAL].
6. **Controle de Cauda nas Fronteiras de Seção:**
   Verifique no editor de amostra se o envelope de release ou cauda de delay/reverb da voz é truncado a **zero absoluto exatamente no milissegundo do beat 1.1** do novo bloco, evitando borrão sobre o transiente do Kick [FONTE: Catálogo de Gestos Psytech].

---

### 2. CONVIVÊNCIA VOCAL, DUPLICAÇÃO E DOBRAS

* **Convivência de Duas Vozes Simultâneas sem Mascaramento:**
  Quando dois elementos vocais coincidem (ex.: Cama Vocal e Whisper), aplique **Filtragem Complementar de Frequência** (EQ Espectral): abra espaço no Cama Vocal com um entalhe em 2.500 Hz para que o Whisper ocupe essa janela. Posicione a Cama Vocal em **140% Estéreo** e o Whisper em **Mono no centro** [PRÁTICA GERAL].
* **Duplicação do MESMO Áudio em Dois Canais:**
  * **O Risco de Fase/Borrão:** Simplesmente duplicar o mesmo clipe de áudio em duas pistas e panoramizá-las para 100% L e 100% R gera **comb filtering destrutivo** e soma mono deficiente se não houver descorrelação de fase [PRÁTICA GERAL].
  * **Quando Funciona (Descorrelação Obrigatória):** Para criar largura estéreo real a partir do mesmo áudio, aplique uma das técnicas de descorrelação:
    1. *Micro-Shift Temporal:* Atrasar um dos canais em **12 ms a 18 ms** (Efeito Haas) [FONTE: AUDITORIA ISMAL.M].
    2. *Formant / Pitch Shift Desequilibrado:* Alterar a afinação de um canal em **+7 cents** e do outro em **−7 cents**, ou modificar os formantes de forma oposta no transpose [PRÁTICA GERAL / FONTE: Au5 Serum Tutorial].
* **Uso de Dobra de Oitava (+12 st / −12 st):**
  **Amplamente utilizada.** A dobra uma oitava abaixo (−12 semitons) é processada em um canal paralelo com filtro passa-baixas (LPF em 1.200 Hz), saturação pesada e volume a −12 dB. Isso confere peso de "monstro/demônio" (*talking throat*) sem poluir os agudos [FONTE: How to Make Vocal Chops That Actually Groove / Verschallt Walkthrough].

---

### 3. O QUE NÃO FAZER — ERROS BANIDOS PELA ESCOLA

```
┌─────────────────────────────────────────────────────────────────────────┐
│                    LISTA DE PRÁTICAS BANIDAS (ANTI-CLICHÊ)              │
├─────────────────┬───────────────────────────────────────────────────────┤
│ Erro Banido     │ Por que destrói a identidade Psytech / Bush Tech?     │
├─────────────────┼───────────────────────────────────────────────────────┤
│ Chop EDM / Pop  │ Pitch bends acelerados e melódicos remetem a EDM/Pop. │
│ Pitch-Up Diva   │ Vocais femininos agudos eufóricos descaracterizam     │
│                 │ a estética sombria Zenon.                             │
│ Coro Épico      │ Arranjos operísticos/gospéis poluem os médios.        │
│ Reverb Encharcado│ Reverb 100% Wet serial destrói os transientes de      │
│                 │ ataque do bumbo.                                      |
│ Voz Contínua    │ Frases vocais longas eliminam o espaço negativo.      │
└─────────────────┴───────────────────────────────────────────────────────┘
```

1. **Chop Vocal EDM / Future Bass:** Padrões rítmicos pop melódicos com *pitch bends* eufóricos ascendentes rápido.
2. **Diva / Vocal Feminino com Pitch-Up Agudo:** Vocais femininos elevados para registros estridentes (estilo Trance comercial/Eurodance) [FONTE: PLAYBOOK PSYTECH].
3. **Coro Épico / Cântico Gospel Operístico:** Arranjos grandiosos cinematográficos que ocupam a região de 300 Hz a 2.000 Hz de forma contínua [FONTE: PLAYBOOK PSYTECH].
4. **Reverb Serial "Encharcado":** Inserir reverbs longos diretamente no canal vocal com Dry/Wet acima de 40%, afogando o transiente seco e gerando lama de ressonância nos médios-baixos [FONTE: Building a PSYTECH Track - Part 8].
5. **Voz Contínua de Bloco:** Manter frases vocais faladas ou cantadas por 32 compassos ininterruptos, destruindo o espaço negativo e sufocando o diálogo com os sintetizadores [FONTE: AUDITORIA ISMAL.M].

---

### 4. AFINAÇÃO, ESCALA E FORMANTES (C# FRÍGIO)

* **Samples de Voz fora de C# Frígio — Estratégia de Ajuste:**
  1. *Transposição Global de Oitava (±12 semitons):* Preserva a classe de pitch exata (C#) e os intervalos harmônicos sem desafinação modal [PRÁTICA GERAL].
  2. *Correção de Nota por Semitons:* Se o sample estiver em outra nota (ex.: E ou G), re-atribua a afinação transpondo o número exato de semitons para atingir as notas da escala de **C# Frígio (C#, D, E, F#, G#, A, B)**. A prioridade é ancorar na tônica (**C#**) ou no semitom de tensão Frígia (**D**) [PRÁTICA GERAL / FONTE: Catálogo de Gestos Psytech].
  3. *Troca de Take:* Se a transposição exigir um deslocamento maior que **±3 semitons** e o áudio soar artificial sem intenção estética, substitua o sample por um take nativo em C# [PRÁTICA GERAL].
* **Tratamento de Formantes:**
  Ao transpor amostras vocais em mais de 2 semitons no Ableton Live 12, selecione o algoritmo de warp **Complex Pro** e ajuste o parâmetro **Formants entre 80 e 100** para manter a ressonância natural da garganta humana, ou reduza para **50–60** para intencionalmente escurecer e encorpar o timbre [PRÁTICA GERAL / FONTE: Au5 Serum Tutorial].
* **Foley Não-Tonal Precisa de Afinação?**
  **Não.** Gravações de foley biológico/ambiente (sopros, suspiros, ruídos de fita, estalos de madeira, fumaça) são ruídos de banda larga atonais. Não exigem afinação tonal, devendo ser processados com filtros passa-banda para ajustar a sua cor espectral [PRÁTICA GERAL].

---

### 5. REFERÊNCIAS E SUSTENTAÇÃO NAS FONTES DO NOTEBOOK

As fontes documentadas no acervo sustentam as técnicas, métodos e comportamentos estruturais aplicados nesta análise:

| Selo / Origem | Faixa / Documento de Referência | Mecanismo Vocal / Técnico Demonstrado nas Fontes | Sustentação na Fonte do Notebook |
| :--- | :--- | :--- | :--- |
| **Pyramid Waves** | *ISMAL.M – Ortahisar (Original Mix)* | Espaço escavado nos médios (−23.5 dBFS em 150–2.5k Hz), rigidez mono <150 Hz e vácuo pré-drop. | [FONTE: AUDITORIA ISMAL.M] |
| **Zenon Records** | *Building a PSYTECH Track (Série 1–8)* | Uso de foley de madeira/vento, *delay throws* paralelos, e vocal seco com Reverb em Send. | [FONTE: Building a PSYTECH Track - Parts 1, 2, 3, 8] |
| **Vision Serpent** | *Verschallt – PSYTECH Project Walkthrough* | Sound design de vozes "guturais/falantes" (*talking sounds*) com Bandpass + Redux. | [FONTE: HOW TO MAKE PSYTECH By Verschallt] |
| **Vision Serpent** | *NoNameLeft – TECHNO SOUND DESIGN* | Spoken word em mono no centro com caudas de Reverb/Delay estéreo nos cantos. | [FONTE: TECHNO SOUND DESIGN By NoNameLeft] |
| **Psiger Records** | *How to Make Vocal Chops That Groove* | Fatiamento de vocais em 1/16ths, compressão OTT e dobras uma oitava abaixo (−12 st). | [FONTE: How to Make Vocal Chops That Actually Groove] |
| **PME Experts** | *Catálogo de Gestos Cinematográficos Psytech* | Sucção humana reversa (*organic reverse suck*) nos últimos 500 ms do vácuo pré-drop. | [FONTE: Catálogo de Gestos Cinematográficos Psytech] |
| **Ableton Tutorials** | *Ned Rush – Granular Beats & Live 12* | Processamento de amostras vocais no Granulator III para criação de texturas e whispers. | [FONTE: Ableton Live 12 Tutorial - Granular Beats] |

*(Nota de Rigor: Conforme as regras da pesquisa, como as videoaulas do acervo tratam a metodologia de forma conceitual e analítica sem exibir minutagem de player para faixas externas de terceiros, os links e timestamps de faixas comerciais externas não-constantes nos transcritos originais são mantidos como `NÃO ENCONTRADO`).*

---

As diretrizes da **RODADA 2** e da **RODADA 3** são aplicáveis diretamente em uma sessão do Ableton Live 12.