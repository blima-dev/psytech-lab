# PACK DE CONHECIMENTO P0 — Canônico para o Executor

> **Classificação: Spike de curadoria (candidato -> P0 aprovado)**
> Material bruto desdogmatizado, sem plugins específicos, alinhado a targets funcionais (Fox Artemis / AlpaKa MuziK) e com as diretrizes PME congeladas nesta fase.

---

## 1. As 12 Camadas do P0

### Camada 1 — Invariantes do método
1. **Intenção antes da ferramenta**: Antes de abrir plugin, definir qual transformação auditiva estamos tentando obter.
2. **Espaço é parte do groove**: Silêncio, retirada e lacunas têm valor igual ao som.
3. **Low-end repetível**: Kick/bass com comportamento consistente entre hits (phase retrigger e envelopes reproduzíveis).
4. **Psychedelia por transformação**: Wavetable, FM, filtro, modulação e textura criam evolução sem escrever melodia nova.
5. **Resampling como instrumento criativo**: Renderizar -> processar -> recortar partes boas.
6. **Microvariação sem quebrar a hipnose**: Mudanças pequenas em timbre/FX a cada frase; não criar novidade musical o tempo todo.
7. **Referência ensina estrutura**: Mapear entradas, saídas, densidade e breaks; não copiar composição.
8. **Layer somente por função**: Elemento novo precisa resolver um vazio auditivo/estrutural específico.
9. **Reverb/Delay com controle**: Returns filtrados, caudas deliberadas, sem sends zerados e sem lama.
10. **O ouvido ganha da receita**: O método fornece o caminho; a escuta valida a música.

---

### Camada 2 — Low-End: Regras Práticas
- **Meta**: Repetibilidade + Pocket + Kick legível + Bass seco + Propulsão hipnótica.
- **Promovido**:
  - Oscillator phase/retrigger consistente no bass;
  - Sub estritamente mono (<120 Hz);
  - Envelope de decay curto (sem embolar o próximo 16th);
  - Zero reverb/delay no sub;
  - Sidechain como ferramenta rítmica e de limpeza;
  - Saturação/harmônicos acima do sub (150–300 Hz) para legibilidade;
  - Kick e Bass avaliados sempre juntos.
- **Não promovido (Rejeitado)**:
  - Phase 0% cega em tudo;
  - Notch obrigatório em 140 Hz (receita de patch);
  - Kick fixo em 231 ms;
  - Regra de afinar kick sempre na tônica/quinta.
- **Conflito método x referência**: Quando divergirem, **a referência auditiva vence**.

---

### Camada 3 — Psy Sound Design (Abstração de Ferramentas)
O material original cita Rift, Portal, Infiltrator, Trash, Vital.
Traduzir em **funções sonoras no stack disponível**:
`distort`, `granularize`, `frequency-shift`, `filter`, `modulate`, `resample`, `delay`, `re-contextualize`.

---

### Camada 4 — Dark Atmos / Drone
- Pitch motion = MÍNIMO (atonal, sem revelar escalas).
- Timbral motion = ALTO (filtros lentos, modulação de textura).
- Rhythmic attention = BAIXO (cama hipnótica).
- Atmospheric tension = ALTA.
- Origem: reverb tails congeladas, noise, texturas analógicas.

---

### Camada 5 — Groove e Percussão
- Offbeat hats como condução;
- Ghost percussion e micro-timing;
- Congas/shakers quentes para balanço de quadril (Tech House 2018);
- Fills pequenos de 1 compasso;
- Retirada de hits (subtração) antes de quedas/reentradas.

---

### Camada 6 — Arrangement por Blocos de Energia
`INTRO (linguagem)` -> `GROOVE (hipnose)` -> `EVOLUTION (novas relações)` -> `SIMMER/BREAK (redução/respiro)` -> `REENTRY/DROP (impacto)` -> `PEAK (clímax)` -> `OUTRO`.
Blocos têm funções energéticas; tempos são flexíveis.

---

### Camada 7 — Mix e Espaço (Guardar para a fase de mix)
Mono low-end, returns filtrados, sidechain em FX, gain staging. (Receitas de master chains congeladas até a mix estar pronta).

---

### Camada 8 — Tradutor de percepção -> causa técnica
- *"Tá videogame"* -> Waveform simples demais, nota reconhecível, envelope repetitivo sem saturação/filtro.
- *"Tá melódico demais"* -> Intervalos reconhecíveis, arpejo de escala, release longo criando acordes.
- *"Tá muito clean"* -> Falta de saturação, sends zerados, transientes excessivamente digitais.
- *"Falta conversa"* -> Elementos tocando juntos sem espaço; falta de delay response em estéreo.
- *"Tá parado"* -> Investigar: 1. Timbre, 2. Filtro/Modulação, 3. Dinâmica, 4. Estéreo, 5. Microvariação de percussão. Pitch só por último.
- *"Tá muito triste"* -> Falta de suingue, ausência de percussão orgânica dançando no break, drone estático funerário.
- *"Tem safadeza"* -> Balanço de quadril, congas/shakers sincopados, malandragem de Tech House BR 2018.

---

### Camada 9 — Catálogo de Técnicas Disponíveis
Consultar quando houver problema específico a resolver:
`phase retrigger`, `FM`, `spectral morph`, `notch modulation`, `resampling`, `granular`, `foley`, `reverb tail capture`, `weak/strong ducking`, `microvariation`, `anticipation by subtraction`.

---

### Camada 10 — Hierarquia de Decisão
1. **A escuta do produtor** — Gosto, ouvido e decisão final;
2. **CONTRATO DA FAIXA** — BPM, tonalidade e referências definidos por projeto (ex.: 132 BPM, C#m, Yao Ofosu / AlpaKa);
3. **Targets funcionais** — Fox / AlpaKa / Black Belt;
4. **Método P0** — Construção Psytech;
5. Conhecimento geral de produção;
6. Defaults de plugins.

---

### Camada 11 — Escopo
Nada aqui vira regra universal. Cada técnica entra como candidata no escopo do gênero (psytech-dark-prog) e vale enquanto a escuta aprovar.

---

### Camada 12 — Pacote Resumo do Executor
```text
P0
CORE: intention before tools | negative space | repeatable low-end | movement by timbre | microvariation | functional layering | controlled spatial FX | ear > recipe
LOW-END: dry bass | mono sub | short envelope | deliberate pocket | a referência auditiva sobrepõe receitas genéricas
SOUND DESIGN: FM | morph | filtering | distortion | granular | atonal stabs
ATMOS: textures | reverb tails | slow filtering | minimal pitch motion
GROOVE: ghost hits | congas safadeza | subtraction | microvariation
ARRANGEMENT: energy blocks | reduce before re-entry | evolve via transformation
GATES: no fixed recipes | 1 coherent delta per experiment | a escuta é o gate musical
```
