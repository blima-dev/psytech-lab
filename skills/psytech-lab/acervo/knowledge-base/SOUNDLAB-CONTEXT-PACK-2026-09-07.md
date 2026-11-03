# Pacote de contexto de produção psytech — síntese de estudo (2026-09-07)

> Versão de estudo: deste pacote de transferência de sessão foram preservadas apenas as seções de conhecimento musical (DNA, aprendizados, playbooks, regra de uso de referência e tradutor de percepção). O estado de sessão, caminhos locais, governança de agentes e infraestrutura de VST não fazem parte do acervo.

---

# DNA MUSICAL

## North Star

> **Movimento > pressão.**

Não interpretar "mais energia" automaticamente como:

```text
full-on
peak-time genérico
melodic techno
melodic trance
tech-house
rave festival
```

O DNA registra kick firme, low-end limpo, pocket claro, movimento hipnótico, psicodelia por modulação/filtro/espaço/delay/transformação, call-response, microvariação e espaço negativo.

## Desejado

```text
KICK
firme, legível, físico

LOW-END
limpo, pocket respirando, bass físico quando apropriado

GROOVE
hipnose + malandragem + microdeslocamentos

PSY
movimento tímbrico, FM, filtering, delay, resposta,
textura, resampling, surpresa

MUSICALIDADE
fraseado, emoção e narrativa sem virar trance

ARRANJO
tensão → retirada → retorno → transformação

DENSIDADE
respira; não permanece "tudo ligado"

PERCUSSÃO
conversa, ghosts, repiques, omissões, pequenas assimetrias

TRANSIÇÃO
evento musical, não apenas FX riser

MIX
peso definido, não parede constante
```

## Evitar por default

```text
supersaw
hoover genérico
festival lead
rave stab óbvio
clap house dominante
offbeat house bass
high-end metálico agressivo
pad progressive bonitinho demais
longos trechos sem mudança interna
camadas para preencher todo vazio
pressão contínua
breakdown emocional EDM
```

---

# APRENDIZADOS QUE VALEM

## A-001 — POCKET > "ROLLING"

O achado mais forte do low-end não é "use rolling bass".

É:

> **kick → espaço → bass.**

Na análise anterior da referência Fox, atividade de bass significativa aparecia aproximadamente **90–110 ms depois do kick**; versões problemáticas traziam energia em **20–50 ms**, percebida pela escuta como outro impacto colado no kick. A 132 BPM, 1/16 ≈ 113,6 ms.

Esses números são **referência comparável, não lei**.

Diagnóstico:

```text
double-thump?
↓
medir tail do kick + onset do bass
↓
corrigir timing/envelope
ANTES DE
trocar synth / aumentar volume / comprimir tudo
```

## A-002 — Sequenciamento provou timing, não timbre

O padrão:

```text
kick
1/16 de pocket
3 bass hits
```

recebeu forte aprovação por escuta, mas os timbres continuaram distantes.

Logo:

```text
sequenciamento válido ≠ sound design final válido
```

## A-003 — Geração fechada não governa bem microtiming

Ferramentas de geração variaram BPM, pocket, high-end e identidade sonora. Usar geração como matéria-prima pode ser útil; não como substituto automático da timeline determinística.

## A-004 — Movimento > pressão

Antes de adicionar layer:

```text
modulação resolve?
retirada resolve?
resposta resolve?
mudança de registro resolve?
automação resolve?
silêncio resolve?
transformação tímbrica resolve?
```

Só depois adicionar nova fonte.

## A-005 — Freeze do que funciona

Em calibração:

```text
UMA mudança material
→ observar
→ escuta julga
→ KEEP / REJECT
```

Não mudar simultaneamente groove + synth + mix e depois tentar adivinhar a causa.

---

# GROOVE / KICK-BASS — PLAYBOOK CRUZADO

## Pocket antes do bass

**CANÔNICO.** A descoberta mais segura. A biblioteca de sons foi analisada usando Fox/Subterranean apenas como envelope e distribuição de energia, explicitamente sem copiar material musical.

## Low-end deve ser diagnosticado temporalmente antes de timbralmente

```text
kick duration
kick tail
bass onset
bass transient
second onset
ducking
```

antes de:

```text
novo bass preset
mais saturação
mais sub
mais volume
```

## Rolling não é obrigação

Um bass pode ser:

* rolling;
* mais quebrado;
* syncopado;
* com ghosts;
* com gaps;
* sub + midbass separados;
* mais pontual;

desde que cumpra a música.

## Técnicas do material de referência derivado

```text
- fase estática no bass;
- kick curto;
- sub mono;
- strong sidechain no low-end;
- weak sidechain em material com transient importante;
- envelope/tail do kick controlados;
- silêncio antes da resposta;
```

### IMPORTANTE

Não congelar automaticamente:

```text
kick = exatamente 231ms
phase = sempre 0%
500 Hz = sempre -3dB
sidechain = sempre 100%
loudness = sempre -8
```

Esses são **pontos de partida do material de referência**, não leis.

---

# NARRATIVA MUSICAL

Uma track não fica "música de verdade" por ter 224 bars ocupados.

A unidade narrativa é:

```text
APRESENTAÇÃO
→ DESENVOLVIMENTO
→ EXPECTATIVA
→ INTERRUPÇÃO
→ RESPOSTA
→ TRANSFORMAÇÃO
→ RETORNO
```

Isso pode acontecer em 4, 8, 16, 24 ou 32 bars.

## Regra prática

Em uma região longa, perguntar:

```text
o que mudou desde o ciclo anterior?
```

Mudança suficiente pode ser pequena:

* último hit omitido;
* resposta deslocada;
* filtro abre;
* filtro fecha;
* automação de WT;
* ghost novo;
* ghost removido;
* motivo termina em outra nota;
* retorno de delay;
* alteração de registro;
* 1/4 beat vazio;
* 1 beat vazio;
* elemento ausente durante 2 bars.

### Hipnose não é repetição idêntica

> **microvariation sem quebrar hypnosis**

é mais próximo do alvo do que "sempre adicionar uma coisa nova".

---

# CALL AND RESPONSE / "MALANDRAGEM"

Não significa criar dois synths tocando alternadamente de forma óbvia.

Pode ser:

```text
CALL:
stab curto

RESPONSE:
delay transformado 1/8 depois
```

ou:

```text
CALL:
motivo de 3 notas

RESPONSE:
mesmo contorno em outro registro
```

ou:

```text
CALL:
percussão

RESPONSE:
squelch
```

ou:

```text
CALL:
frase completa

RESPONSE:
silêncio
```

## Malandragem útil

```text
pickup 1/16 antes
resposta 1/8 atrasada
último hit omitido
kick ausente pontualmente
fill de 1 beat
frase interrompida
tail atravessando um corte
segunda repetição com outro final
```

Não é humanização aleatória.

É **expectativa criada e deliberadamente desviada**.

---

# TENSÃO / BUILD-UP / BUILD-DOWN

## Build não é "adicionar tudo"

Quatro eixos principais:

```text
DENSIDADE
REGISTRO
TIMBRE/FILTRO
ESPAÇO
```

Build-up pode subir apenas dois deles.

Exemplo:

```text
menos grave
+
mais movimento de filtro
+
registro sobe
=
tensão
```

sem adicionar layer.

## Build-down é tão importante quanto build-up

Para este DNA, muitas vezes:

```text
subtração
→ expectativa
→ retorno
```

funciona melhor que:

```text
riser
→ snare roll
→ impacto
```

### Técnicas úveis derivadas do material de referência

* `Milk`: diminuir radicalmente densidade antes do retorno;
* `Suction`: remover kick/evento esperado;
* `Simmer`: preservar atmosfera/movimento enquanto o peso recua;
* retirar low-end para tornar o retorno físico;
* usar textura já existente, não necessariamente criar novo FX.

### Não transformar técnica em receita

Perguntar:

> Onde a track atual precisa ser privada de energia para que o próximo evento importe?

Não:

> Em qual bar tenho que colocar o "Milk"?

---

# SILÊNCIO / NEGATIVE SPACE

Silêncio é **evento de arranjo**.

Escalas:

```text
MICRO
1/16 – 1/4

CUT
1/4 – 1/2 beat

SUSPENSION
1 beat

BREATH
1–2 bars

MILK
seção reduzida
```

Usar para:

* quebrar previsibilidade 4/4;
* tornar a volta maior;
* abrir lugar para frase;
* revelar tail;
* mudar percepção de groove.

A retirada do quarto kick é apenas **uma implementação possível do princípio de ausência estratégica**.

---

# ATMOSFERA

Atmosfera não deve significar "pad grande tocando por 32 bars".

Funções possíveis:

```text
cola tonal
presságio
cauda de evento
movimento espacial
contraste luz/escuro
respiração em baixa densidade
textura orgânica
ponte entre seções
```

### Arsenal

```text
Granulator III
PitchLoop89
Grain Delay
Spectral Time
Echo
Hybrid Reverb
Roar
Serum 2
resampling
foley
```

Priorizar nativos/M4L antes de novas dependências.

### Técnicas

**Reverb freeze / capture**

```text
fonte da própria track
→ longa tail
→ capture/resample
→ editar apenas fragmento útil
```

**Glassy + gritty**

Contrastar uma camada limpa/alta com matéria orgânica/processada sem preencher todo o espectro.

**Foley processado**

Utilizar madeira, metal, areia, crackles etc. como matéria, não como gimmick.

**Movimento sem nova nota**

```text
S&H → cutoff
WT position
grain position
delay time
feedback
pan
spectral processing
```

---

# SOUND DESIGN PSY

## Intenção antes do plugin

Pergunta correta:

> quero que esta resposta pareça seca, elástica e alienígena.

Não:

> em qual plugin eu coloco 43% de drive?

## Fontes principais

### Serum 2

Usos:

```text
WT position
FM
filter movement
resonance
oscillator balance
envelope shape
LFO
macros
noise
short stab
squelch
midbass
response
```

### Native/M4L

Para:

```text
granulação
pitch response
spectral movement
resampling
distortion
tails
glitch
```

## Cadeia conceitual útil

```text
SÍNTESE
→ MOVIMENTO
→ SATURAÇÃO/TEXTURA
→ LIMPEZA
→ ESPAÇO
```

Não precisa corresponder a cinco plugins.

### Pós-distorção

Lição recorrente: distorção cria conteúdo novo; portanto, inspeção/limpeza **depois** dela é frequentemente mais útil do que EQ apenas antes.

---

# TRANSIÇÕES

Meta:

> fazer uma seção tornar a próxima inevitável.

Não apenas colocar um uplifter.

### Toolkit

```text
retirar kick
retirar bass
retirar apenas sub
pickup
fill curto
tail congelada
delay throw
reverse de material próprio
filter opening
filter closing
register shift
pitch response
motivo antecipado
motivo fragmentado
false return
build por subtração
resampling de som já apresentado
downlifter
silêncio
```

## Coerência por reciclagem

Uma técnica forte é derivar transições de personagens que já existem:

```text
stab
→ reverb
→ freeze
→ resample
→ reverse
→ transition
```

Assim a transição pertence à mesma música.

---

# MIX — PRINCÍPIO VS. NÚMERO DE RECEITA

## Bem alinhado

### Low-end central/coerente

Manter o sub estável e verificar mono/phase é uma boa prática de diagnóstico.

### High-end não dominar

```text
se dói
→ localizar fonte
→ reduzir/filtrar fonte
```

Não abaixar o master inteiro.

### Reverb filtrado

Especialmente em material rítmico, cauda não deve encobrir transientes.

### Headroom antes de "loudness"

## Não congelar como requisito

Do material de referência aparecem:

```text
-8 LUFS
-7.6 RMS
500 Hz -2/-3 dB
hats ~ -18 dB
20–25% width
strong SC = 100%
weak = 60%
```

Esses são **baselines/receitas derivadas**, não critérios vigentes de entrega.

### Regra

```text
medição diagnostica
ouvido decide
```

---

# MAPA DE REFERÊNCIAS

## Tier principal

### Fox (Artemis Remix)

**PRINCIPAL REFERÊNCIA TÉCNICA.**

Usar para:

```text
groove
pocket
envelope
densidade
energia
kick/bass
estrutura
dinâmica
call-response
```

Não copiar:

```text
melodia
hook
arp identificável
frase
composição
```

Fox é 132 BPM / C# minor na análise histórica, e a referência foi usada apenas como envelope/espectro, não material musical.

### Yao Ofosu

**REFERÊNCIA ATUAL EXPLÍCITA.** Papel musical específico: NÃO VERIFICADO — consultar exemplo somente quando precisar responder uma pergunta concreta.

### André Gazolla

**Hipótese de uso recorrente:** musicalidade/evolução/narrativa.

### Akary Sistem / Akari System

Referência atual explícita e âncora histórica.

**DIVERGÊNCIA DE ESCRITA:** arquivos antigos usam `Akari System`; mensagem mais recente usa `Akary Sistem`. Não normalizar silenciosamente antes de verificar o nome correto.

### Tetra Hydro

Referência atual explícita. **NÃO HÁ análise específica** — não atribuir "som Tetra Hydro = X" sem escuta/pesquisa.

### AlpaKa MuziK / AlpaKa

Cluster histórico principal e novamente referência atual. Atributos específicos devem vir de faixas, não de estereótipo de label.

### Black Belt brasileira

Cluster atual explícito e histórico importante. Mesmo cuidado: referência = banco de atributos, não target de cópia.

## Âncoras secundárias

```text
Luis M
Antônio Farhy
AIRI
AdrenaZ
Honigkater seletivamente
Kaled Nasser
Sam Sick
ISMAIL.M
Labareda como edge
Zenon como edge, não default
```

Úteis para exploração, mas não superam a lista vigente do projeto.

---

# REGRA DE USO DE REFERÊNCIA

Abstrair:

```text
groove
pocket
densidade
estrutura
energia
registro
espaço
timbre
dinâmica
fraseado
tensão/release
call-response
microvariação
```

Nunca:

```text
melodia
hook
arp
progressão distintiva
sequência reconhecível
arranjo integral
sample protegido
```

Se a escuta aprova uma melodia de referência:

```text
NÃO:
copiar notas

SIM:
abstrair
- tessitura
- direção
- comprimento
- densidade
- ritmo
- tensão/resolução

e compor material novo.
```

---

# TRADUTOR DE PERCEPÇÃO

### "Tá videogame"

Teste primeiro:

```text
timbre
filtro
harmônicos
movimento
```

Não reescrever o arranjo.

### "Tem outra coisa batendo colada no kick"

Teste:

```text
kick tail
bass onset
segundo transient
overlap
```

### "Tá bonito demais / progressive"

Teste:

```text
menos suavidade
mais fricção
FM
semitom
resampling
timbre
```

não simplesmente adicionar nota.

### "Tá muito pressão / sem movimento"

Teste:

```text
retirar layer
modular
criar resposta
abrir espaço
```

### "Tá metálico / rasgando"

Localizar fonte/resonance/top peak.

Não resolver reduzindo o master inteiro.

### Regra geral

```text
PERCEPÇÃO
→ HIPÓTESE
→ MENOR MUDANÇA
→ PROVA
→ ESCUTA
```

---

# O MATERIAL DE REFERÊNCIA — COMO USAR CORRETAMENTE

O manual é útil. Não é constituição.

### Classificação correta

```text
MÉTODO = TOOLBOX
não
MÉTODO = REGRA UNIVERSAL
```

Pergunta:

> **isso melhora esta música agora?**

Se sim, testar.

Se não, ignorar.

### O que precisa de cruzamento PME antes de virar regra

```text
kick duration exata
static phase universal
pitch bend
sidechain depth
loudness
master chain
500 Hz dip
stereo width
estrutura fixa
densidade final
```

---

# RESUMO EM UMA LINHA

> **não leia para entender o projeto inteiro; leia para responder a próxima decisão.**
