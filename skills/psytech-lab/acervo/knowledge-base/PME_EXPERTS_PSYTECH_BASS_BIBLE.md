# BÍBLIA TÉCNICA PSYTECH & BASS DESIGN — PME EXPERTS & FREAK AUDIO

> Compilação das masterclasses do canal **@PMEExperts** (Eduardo Juliato, Lucas Darkside) e **Freak Audio**.

---

## 1. O Diagnóstico: Por que o baixo fica "marcado e rasgado"?

### Causa 1: Excesso de agudos abertos (Rasgado)
No Serum ou qualquer sintetizador, ondas Sawtooth ou Square puras geram harmônicos que vão até 15.000 Hz. Se o filtro estiver muito aberto ou se o envelope do filtro abrir demais o cutoff:
* O baixo perde o foco sub e vira um "zumbido de abelha" rasgado.
* A referência da Fox (Artemis Remix) e as faixas da AlpaKa/Zenon **não têm praticamente nenhuma energia acima de 300–400 Hz no canal de bass**. O filtro (MG Low 24 ou Low 18) precisa repousar fechado (~120–250 Hz), com a modulação de envelope curta e controlada (+15% a +25%).

### Causa 2: Envelope ultracurto sem sustain (Marcado / Pluck Magro)
Como ensina Eduardo Juliato em *"O Erro que Todos Cometem no Baixo"*:
> *"Muitos produtores fazem o baixo soar bom no fone deixando-o super 'pluck' e percussivo. Quando você vai para os monitores ou pista, o som fica magro, seco e sem corpo, parecendo cliques robóticos."*
* Para ter **peso e corpo**, a curva do envelope/LFO precisa ter uma leve "barriga" (hold/decay sustentado), mantendo a energia vibrando durante a fração da semicolcheia antes de fechar.
* Se a nota é cortada a seco (decay 60ms, release 0ms), ela soa mecânica e desconectada.

---

## 2. Como Dar Corpo ao Baixo (Frequências e Saturação)

### A Relação Harmônica Fundamental
Em um tom como **C#** (Dó sustenido):
1. **Fundamental (Sub)**: ~69 Hz (C#1) — dá a pressão de peito/estômago.
2. **Segundo Harmônico (Corpo)**: ~138 Hz (C#2) — **é aqui que mora o corpo da track!** Se essa região estiver fraca, o baixo parece um subwoofer sem peso ou um clique vazio.
3. **Terceiro Harmônico (Definição)**: ~207 Hz (G#2).

### A Técnica da Saturação Cirúrgica (Super Punch)
Como ensina o PME Experts em *"Bass Saturation Trick"*:
* Saturar o canal direto pode embolar o sub ou distorcer os picos.
* **Solução**: Saturação quente (Tube ou Soft Sine) concentrada na faixa de **140 Hz a 250 Hz**, com o sub mono abaixo de 120 Hz mantido 100% puro e os agudos acima de 400 Hz cortados. Isso gera a "gordura" analógica sem rasgar os ouvidos.

---

## 3. Caudas e Respiração (O Envelope e a Continuidade)

### A Lição do Fox (Artemis Remix)
Análise espectral do stem isolado de bass da referência Fox revelou:
* **Tempo 1.1 (Kick)**: Energia de bass em 0.05 (silêncio quase absoluto, pocket para o kick bater limpo).
* **Tempo 1.2 (Semicolcheia 2)**: Subida para 0.35.
* **Tempo 1.3 (Offbeat / Semicolcheia 3)**: Pico de pressão em 0.45.
* **Tempo 1.4 (Semicolcheia 4)**: Cauda sustentada em 0.22, entregando o ar e a pressão suavemente para o próximo kick.

O baixo não é uma metralhadora de cliques soltos; **é uma onda contínua que respira com o kick**:
KICK (pocket) -> RISE -> PEAK (offbeat) -> TAIL (sustentação) -> KICK

Para conseguir isso:
* **Release**: Ajustado em 40–80 ms para não cortar a cauda bruscamente ao soltar a tecla MIDI.
* **Mono Legato & Portamento/Glide sutil**: Transições conectadas entre notas.

---

## 4. A "Malandragem" (Groove, Síncope e Humanização)

Extraído da masterclass *"Bass Grooves Formulas"* e de Lucas Darkside:

1. **Baixo Sincopado (Estilo AlpaKa / Zenonesque / Prog Dark)**:
   * Evitar bater sempre igual em todas as cabeças de tempo.
   * Valorizar as casas **menos acentuadas** do compasso (2ª e 4ª semicolcheias) para criar o contrabalanço de malandro.
2. **Dinâmica de Velocity (Escadinha Humana)**:
   * Em vez de todas as notas a 100 fixo:
     * Nota 1: vel 45 (fantasma / respiração)
     * Nota 2: vel 95 (corpo)
     * Nota 3: vel 118 (punch principal)
     * Nota 4: vel 80 (cauda de passagem)
   * Modulação do Velocity ligada ao **Cutoff** do filtro e ao **Drive**: quando a nota bate com mais força, ela abre discretamente o filtro e morde mais; quando bate fraco, soa macia e profunda.
3. **Ghost Notes e Viradas de Compasso**:
   * A cada 4 ou 8 compassos, uma pequena quebra rítmica (uma síncope com note bend ou slide de 1 semitom) quebra a rigidez alemã/industrial e injeta o gingado underground.

---

## 5. Arquitetura de Presets do Serum 2 (BLACKBOX / Dimensions)

Presets recomendados do banco de usuário (`User/BLACKBOX/`):
* `[DIMENSIONS 2] - [BASS] - JONNY.SerumPreset`: Destacado na aula do PME Experts como a fórmula do groove com mono legato e corpo gordo.
* `[DIMENSIONS 2] - [BASS] - SQUARISH.SerumPreset`: Timbre square arredondado estilo AlpaKa / Zenon.
* `[DIMENSIONS 3] - [BASS] - CLEAN.SerumPreset`: Sub bass puro com fase travada e zero ressonância espúria.
* `[PSYBASS 4 SERUM] - [BASS] - PURE ROLLING.SerumPreset`: Envelopamento clássico calibrado com rampa.
