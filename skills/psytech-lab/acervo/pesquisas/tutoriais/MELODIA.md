# Melodia — tutoriais traduzidos

> Camada de consulta da frente **melodia** (3 mapas, um por vídeo). Nada aqui foi aplicado num projeto real e nenhum A/B foi executado; todo valor de parâmetro é ponto de partida. Os três mapas vêm de legenda automática/ASR — nenhum áudio de vídeo foi ouvido como fonte musical.
> Triagem contra as diretrizes do projeto de referência: dos 3 mapas da frente, 2 estão alinhados e 1 conflita (`rSorLiUr6xI`).

**Use quando** for escrever ou revisar motivo, frase, resposta de madeira/bongo/stab, gancho ou tensão harmônica no motor — e quando o pedido for "melodia", "motivo", "pergunta-resposta", "tensão", "hook".

## Regras

1. **ritmo antes da nota** — desenhar o esqueleto rítmico numa nota só e só depois distribuir as alturas; o mesmo motivo com outro ritmo deixa de ser reconhecível (`rSorLiUr6xI`, [00:00:57.990]–[00:01:03.520]).
2. **2–3 notas, registro médio-grave** — núcleo na tônica, b2 e 5ª da escala de referência (na tonalidade do projeto de referência: C#, D, G#); frase curta, nunca arpejo de euforia nem oitavas agudas como registro.
3. **silêncio é parte da frase** — o resto é escrito, não é volume baixo; um falante por vez na mesma oitava, e a resposta não preenche o buraco do outro (`rSor`, [00:05:57.199]–[00:06:02.000]).
4. **uma dissonância por frase** — 2ª menor a partir da tônica ou da dominante (na referência: C#–D ou G#–A), a sétima maior como inversão dela, ou o trítono b2–5 (D–G#); empilhar 2ªs é "a receita para ficar dissonante demais" (`VqPpTk3gp78`, [00:07:21.280]–[00:07:40.510]).
5. **repetição com microvariação** — espelhar o ritmo e mexer só no fim a cada duas voltas (`rSor`, [00:07:30.560] e [00:08:25.510]); hipnose vem de uma fonte com movimento desenhado à mão, não de mais camadas nem de mais LFOs (`oO2gdXg1-nE`, [00:04:46]).

## Receitas traduzidas

| Técnica (mapa) | Encaixe | Valor de partida | Guarda |
|---|---|---|---|
| Ritmo antes da nota (`rSor`) | Camada de madeira ou stab; clipe novo de 4 compassos tocando **uma** nota | Tirar 3–4 acentos por compasso do shaker e usá-los como esqueleto; só depois distribuir as 2–3 alturas | Não copiar o padrão inteiro do shaker (dobra densidade e apaga o deslocamento); usar acentos, não 16avos |
| Pergunta sobe / resposta desce (`rSor`) | Mesmo canal; 2 compassos de pergunta, 2 de resposta, 1 de silêncio | Pergunta aguda e curta; resposta grave com a última nota longa; lead com HP 180–220, unison 1, detune 0 | Resto é nota faltando, não fader baixo; o lead não fala nos offsets do baixo de referência (`rSor:76`) |
| Gancho por microvariação (`oO2g`) | Percussão de resposta/madeira existentes (5 pads do mesmo one-shot) | Mesmo sample em 5 pads variando só ataque/início e pitch; motivo de 2–3 notas na tônica, b2 e 4ª da escala | Não criar família nova; é variação de uma camada, não cinco camadas |
| Stab FM curto (`oO2g`) | Stab (Operator ou Serum 2) | Só senoides; modulador fixo em 100 Hz ou 138,6 Hz (C#3), −11 dB; LFO minúsculo na frequência do modulador; nota curta, notch ~5 kHz | 100 Hz é inarmônico na tonalidade de referência: acento, nunca cama; sem shelf de agudo |
| Célula de tensão (`VqPp`) | Madeira, stab e percussão de resposta | 2ª menor (tônica–b2 ou 5ª–b6) como acento; trítono b2–5; 5ª e b6 só como recheio; intervalos maiores só em bases seguras | Uma dissonância por frase; nada abaixo de ~200 Hz; nunca no grave |
| Acento alto e resolução (`VqPp`) | Madeira | Acento com 2ª menor sobre a 5ª no trecho antes do drop e retirar uma nota no drop | Não reintroduzir o salto agudo do compasso 32 (rejeitado na escuta do projeto de referência) |

**Preservar sempre:** a tônica como centro; camada melódica sem oscilador de sub; posição/duração/velocity das chamadas já aprovadas não mudam por causa da tensão (a célula de tensão é pitch-only); não somar 15% de swing ao groove de bolso (`oO2g`, [00:01:47]); não copiar o corte largo de 700 Hz–1 kHz (`oO2g`, [00:01:56]) — o meio já está baixo. A resposta atrasada é minoria nas referências: a conversa é **sobreposição**, não espera.

## Conflitos e cautelas

| Tutorial | O que o vídeo faz | Como adaptar |
|---|---|---|
| `rSorLiUr6xI` manda manter a melodia em **C#4–C#5** (`rSor:73,98`) | Registro agudo como padrão | **Conflito** — o projeto de referência trava o registro em **C#3–C#4**; C#5 só existe como 1 pico de lead **nomeado**, não como registro. Adaptar ao registro do projeto de destino. |
| `rSor` chama C#3 (~139 Hz) de "zona do sub" (`rSor:73`) | Terminologia do vídeo | C#3 é corpo, não sub: o lead pode usar C#3–C#4 sem engordar o grave; o que não pode é descer para a fundamental do sub. |
| `oO2g` transpõe −6 semitons "ignorando a escala" (`oO2g:76`, [00:01:29] e [00:01:41]) | Transposição fora do modo | −6 sobre a tônica sai da escala; e na oitava 3 cai em cima do kick/baixo. Usar **b2** ou +6 com a fonte na oitava 4. |
| `oO2g` trabalha "sem escala" de propósito ([00:10:50]) | Liberdade total | A liberdade é de **timbre e posição**, não de altura: o motivo continua em 2–3 notas da escala. |

## A/B

1. **Camada melódica entra/sai** — 8–16 compassos de motor, volume casado, mute reversível. Critério: 300–1.200 Hz e 1.200–4.000 Hz sobem; 20–120 Hz fica idêntico (±0,2 dB) e a correlação abaixo de 120 Hz não cai; 5–12 kHz não salta; os offsets do baixo de referência com os mesmos onsets. Se não houver ganho nas duas bandas de meio sem subir o topo nem mexer no grave, a receita é descartada — não se compensa com EQ.
2. **Monólogo vs conversa** — mesma frase com o resto escrito contra a versão preenchida. Critério: notas simultâneas na mesma oitava entre melodia e percussão de resposta/madeira = 0; a resposta não repete o ataque do outro falante; contagem de onsets da camada melódica menor na versão com silêncio. Dobra na mesma oitava reprova o take.

## Evidência

Os mapas completos por vídeo (um por ID, com timestamps) não acompanham este pacote; os IDs listados identificam cada fonte. Proveniência: legenda automática.

## NÃO VERIFICADO / pendências

- **Registro agudo (oitava 5) em aberto.** O projeto de referência tolera 1 pico de lead nomeado e proíbe oitavas 5–6 como registro; dois mapas usam C#5 como registro/resolução. Até decisão, este doc trata C#5 como exceção única e nomeada — nunca como registro. Sem essa decisão, os dois mapas ficam parcialmente bloqueados.
- **Nenhum A/B executado** e nenhuma medição nova de áudio; os critérios acima são de aceite, não resultados.
- **Estado real das camadas melódicas do projeto de destino** (notas atuais, mutes) não foi lido nesta redação — `NÃO VERIFICADO`.
- **Granulator/M4L** (método 1 do `oO2g`) pode não estar disponível; a rota sem M4L é o GranularOsc, e o playhead/SCAN exige GUI — `NÃO VERIFICADO`.
- **Régua do médio** pesa nesta frente: a melodia é uma rota para preencher o vale do médio medido, mas a régua do projeto de referência não está conciliada com esse déficit.
