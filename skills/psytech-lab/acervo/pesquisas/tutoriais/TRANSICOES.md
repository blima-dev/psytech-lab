# Transições — tutoriais traduzidos

> **Frente:** `transicoes` · **Mapas da frente:** `qvJqxGrAtCc` (Sonic Academy) e `44m_K42KtX8` (Sonic Academy). **Mapas vizinhos usados só no mecanismo de fronteira:** `ORj8Vgu2vNs`, `6x1_XZDcI8I`, `sTizY7Qln78`, `TdNE8oEb2Lk`; `VSYCY__WVQ8` entra apenas como tensão declarada.
> **Nada foi aplicado num projeto real; nenhum áudio de vídeo foi escutado.**
> **Grid:** a 128 BPM, 1 compasso = 1,875 s. `0:44–0:45` é o último segundo do c24 e `0:45` é o c25; `0:59,5–1:00` é o último meio segundo do c32 e `1:00` é o c33 (posições do arranjo de referência).

**Por que esta frente existe:** o projeto de referência corta em silêncio **1,33 vez/min** contra no máximo **0,80** da família de referências — o corte seco virou hábito e perdeu valor dramático. A tradução dos tutoriais não é "mais FX": é **transformar a fronteira** em cauda ou gesto, com um único dono.

## Use quando

- Escolher o que acontece numa fronteira de seção (0:15, 0:30, 0:45, 1:00, 1:15, 1:30, 1:45, 2:00).
- Preencher ou proteger os dois respiros internos `0:44–0:45` e `0:59,5–1:00` sem refazer o groove.
- Decidir entre riser, reverse, sweep, crash, throw ou silêncio — e recusar o que for hábito.
- Montar ou portar um grupo de FX de transição entre projetos.
- Substituir um corte seco por cauda/transformação quando a seção muda.

Toda receita abaixo é **candidata de design**; só vira decisão depois de A/B com o ouvido do produtor.

## Regras

- **Reverse do alvo** — a subida é o próprio elemento que vai entrar, invertido e com fade, morrendo no acento; não é um riser separado (`ORj8Vgu2vNs` 00:28:40–00:29:32).
- **Um dono por fronteira** — um gesto por corte; se já existe reverse, crash ou sweep, **substituir**, não somar (`qvJqxGrAtCc` 00:02:01.480–00:02:07.390 e 00:05:01.720–00:05:08.790). O "banco de 6–8 efeitos" de `VSYCY__WVQ8` não se copia como densidade.
- **Curto cabe no respiro** — o gesto dura o que a janela permite (1 s em `0:44–0:45`; 0,5 s em `0:59,5–1:00`) e morre no downbeat. Oito compassos só no build `1:30–1:45`, e sem riser tonal (`44m_K42KtX8` 00:04:10.680).
- **Fora do grave** — HP ≥120 Hz em todo FX de transição; retorno de reverb em 200–300 Hz; nada de kick, sub ou baixo no return.
- **Contraste por subtração** — antes da fronteira, retirar o **gesto** de topo (crash, ride, percussão de resposta) por 1–2 compassos, não o chão contínuo de hats/shaker; o drop ganha por ausência, não por ruído somado (`6x1_XZDcI8I` 00:16:43–00:16:45; tensão com a diretriz de topo contínuo do projeto de referência, declarada nas cautelas).

## Receitas traduzidas

| Fonte | Gesto (timestamp) | Onde aplicar | Guarda |
|---|---|---|---|
| **`qvJqxGrAtCc`** | Grupo portátil de FX de transição com crash, reverse-crash, noise-up e noise-down; HP por pista; primeiro clipe ancora no "one"; apagar snare roll duplicado; corrigir overlaps e reequilibrar no destino (00:01:37.320–00:01:48.350; 00:02:01.480–00:02:07.390; 00:05:01.720–00:05:08.790). | Dois clipes-âncora: um em `0:44→0:45`, outro em `0:59,5→1:00`; os gestos morrem nos downbeats c25/c33. | Um evento por respiro; sem snare roll se o motor já tem resposta; sidechain do crash só no noise do grupo (00:04:47.560–00:04:53.350). |
| **`ORj8Vgu2vNs`** | Inverter + fade do clip que vai entrar, alinhando o fim do reverse no acento, para o som "já soar familiar" quando chega (00:28:40–00:29:32); low-cut do side ~300 Hz para o material lateral não competir com o grave (00:20:17–00:20:19). | Entrada de madeira/stab/atmosfera em `0:45` e `1:00`; portas de 8 quando houver troca de camada. | É reverse do alvo, não elemento novo; HP ≥120; não cobrir o ataque do c25/c33; offsets do bolso intactos. |
| **`6x1_XZDcI8I`** | Contraste por subtração do topo antes do drop (00:16:43–00:16:45); entrada de camada por curva de volume de 1–2 compassos, não "no downbeat" (00:09:07–00:09:33). | c23–24 antes de `0:45` e c31–32 antes de `1:00`; a camada que entra é a mesma, só com fade. | Subtrair **gesto**, não o chão de hats/shaker; não somar ruído para "subir"; não repetir o salto agudo do c32 (rejeitado na escuta do projeto de referência). |
| **`44m_K42KtX8`** | **Só a metade sweep é traduzível:** ruído + banda de EQ ressonante automatizada de baixo para cima, HP, ~1 compasso (00:01:02.280–00:02:26.819). O riser tonal 2→24 st em 8 compassos fica vetado (00:04:07.860–00:04:24.240). | Fronteira que pedir transformação (0:30 ou 1:00), nunca junto do reverse no mesmo respiro. | Pink/Brown, LP ~8 kHz, Q moderado; Shifter desligado ou ±10–80 Hz (não 2 kHz); pico móvel atravessa os vales medidos, não estaciona em 2–4 kHz. |
| **`sTizY7Qln78`** | Throw pontual: send em pulso curto para return com reverb 100% wet, HP e filtro no send bus; automatizar o send no fim da seção para a cauda atravessar a virada (00:03:29.120–00:03:40.830; 00:04:10.560–00:04:16.040; 00:05:11.390–00:05:36.240). | Stab/madeira/atmosfera nos respiros; a cauda faz o papel de "outro" da fronteira. | Sem kick/sub/baixo no return; cauda extinta antes do drop; Redux/8-bit desligado (00:02:03.960; o autor chama de "too heavy", 00:02:19.239). |
| **Assinatura de transição do projeto de referência (provisória)** | 1–2 compassos de vácuo de kick → sucção/puxada → gota de foley no tempo 1 → ar vazando por 2–4 compassos. | Fronteiras estruturais; não nos dois respiros internos, para não repetir a assinatura. | **Provisória** no projeto de referência; não empilhar com outro dono. |

## Conflitos e cautelas

| Tutorial | O que o vídeo faz | Como adaptar |
|---|---|---|
| **Riser tonal 2→24 st em 8 compassos** (`44m_K42KtX8` 00:04:07.860–00:04:24.240; mapa `:117-119`) | Riser EDM | Não copiar — é o gesto que o projeto de referência aposentou. Usar reverse do alvo, sucção ou gota. Se mantiver sweep, ele é de ruído, 1–2 compassos, sem pitch tonal e com HP ≥120. O reverb 100→0 do vídeo vai para return ou cópia paralela, nunca serial em fonte acústica. |
| **Riser + snare roll + banco de 6–8 FX como transição padrão** (`TdNE8oEb2Lk:111`; `VSYCY__WVQ8` 00:08:28–00:08:59; `6x1_XZDcI8I` 00:11:50) | Densidade de FX | No máximo 2–3 micro-gestos. Um único hit de snare, nunca roll. O contraste é por subtração de gesto, não por desligar o chão de hats. `qvJqxGrAtCc` é o guardrail: ele mesmo apaga o snare roll que duplica (00:02:01.480–00:02:07.390). |
| **Washout no mix inteiro + riser no build** (`TdNE8oEb2Lk` 00:09:28.920–00:09:35.040 e 00:16:06.170–00:16:14.930) | Washout global | Washout só em return, com o send automatizado a zero no downbeat; provar a extinção. Riser vira reverse/sucção. Não copiar o corte global de 200–500 Hz nem o boost de 3 kHz no master (mapa `:111`). |
| **Reverb 100% wet longo + Redux 8-bit no retorno** (`sTizY7Qln78` 00:01:22.920 e 00:02:03.960) | Cauda longa | Manter return e HP; o 100% wet é do return, não do solista. Redux desligado ou blend ≤10–20% — o próprio autor diz que é pesado (00:02:19.239). |
| **"Tirar o agudo/hats antes do drop"** (`6x1_XZDcI8I` 00:16:43–00:16:45) | Mutar o chão | Subtrair o **gesto** de topo (crash, ride, resposta), preservando o chão contínuo do projeto de referência. Mutar o chão só como exceção auditiva registrada — não é regra homologada. |
| **Pendência — proibição de riser é total ou parcial?** (mapa `:189-192`) | Sweep longo | **Sem escolha neste doc:** riser tonal de 8 compassos e snare roll ficam vetados; sweep de 1 compasso/ruído fica como candidato de A/B. A biblioteca de referência mede sweep-longo como 53% do material externo, mas a diretriz do projeto proíbe riser — só o produtor decide se o sweep longo está liberado ou não. |

## A/B

**A/B 1 — respiro de `0:44–0:45` (reverse do alvo × silêncio preservado).**
Baseline: como está, com o vácuo de kick preservado e sem FX novo. Candidato: inverter o elemento que entra em `0:45` (madeira/stab) + fade, terminando no downbeat, com a cauda no return.
Critério mensurável: (1) 20–120 Hz da janela idêntico ao baseline — o vácuo continua sem kick+subs (medido na janela, não "parece mudo"); (2) pico do gesto ≤ pico do elemento que entra (volume casado); (3) em `0:45–0:45,2` a cauda está em decay, não crescendo; (4) nenhum onset novo nos offsets `.27/.77`. Descarta se houver energia nova abaixo de 120 Hz ou se o reverse cobrir o ataque do c25.
Medição: captura estéreo na taxa original e energia por banda; nada de medir topo ou estéreo após reamostrar.

**A/B 2 — respiro de `0:59,5–1:00` (micro-gesto × silêncio preservado).**
Baseline: silêncio atual. Candidato: micro-gesto de 0,5 s — sweep curto de ruído com HP ≥120 ou um único hit de crash/reverse — que morre em `1:00`.
Critério mensurável: (1) 20–120 Hz inalterado; (2) o gesto dura ≤0,5 s e não avança sobre o c33; (3) 5–12 kHz pode subir na janela, mas `1:00–1:01` volta ao baseline — o gesto não vira cama; (4) nenhum onset novo em `.27/.77`. Se o baseline (silêncio) vencer, o respiro fica vazio: isso é resultado, não falha.
Medição: mesma do A/B 1. Nenhum dos dois A/B foi executado.

## Evidência

Os mapas completos por vídeo (um por ID, com timestamps) não acompanham este pacote; os IDs listados identificam cada fonte: qvJqxGrAtCc e 44m_K42KtX8 (mapas primários); ORj8Vgu2vNs, 6x1_XZDcI8I, sTizY7Qln78, TdNE8oEb2Lk e VSYCY__WVQ8 (mapas vizinhos).

## NÃO VERIFICADO / pendências

- **Nenhum A/B executado**; nenhum áudio de vídeo foi escutado como fonte musical. Os mapas são leitura de legenda automática, ASR local ou descrição — "o vídeo diz" não é "o som funciona".
- **Grupo de FX de transição não existe por padrão no projeto de destino.** Criar ou não é decisão de implementação, não fato.
- **Os dois respiros não foram medidos nesta escrita.** Se `0:44–0:45` e `0:59,5–1:00` estão hoje vazios de FX e com kick+subs zerados é `NÃO VERIFICADO`; exige medição na janela.
- **Proibição de riser em aberto no projeto de referência** (total ou só do riser tonal/snare roll). Este doc não escolhe; até a decisão, riser tonal de 8 compassos e snare roll ficam vetados, sweep curto fica como candidato.
- **Shaker contínuo em 16avos** tangencia o "contraste por subtração". Se o chão de hats for a regra viva, o contraste só pode retirar gesto; se a proibição do shaker for a regra viva, o próprio chão já é condicional. Decisão do produtor.
- **Diretrizes provisórias** do projeto de referência foram usadas como critério de projeto, não como lei homologada. Se não forem homologadas, a regra anterior (topo percussivo contínuo) prevalece.
- **`44m_K42KtX8` não dá valores** de Q, ganho, HP, decay nem attack; onde há número de aplicação, é hipótese do mapa, não fala do autor. `VSYCY__WVQ8` não tem legenda oficial (ASR) e as contagens de efeitos são reconstrução (00:00:50–00:01:15) — não usar como número.
