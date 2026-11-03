# Consolidado PSYTECH-LAB
Psytech Lab v0.1.0 · 03/11/2026

## 00-INDICE-PSYTECH-LAB.md

# PSYTECH LAB — Índice documental

> Coleção 100% documental: teoria, protocolo e templates. Sem execução, sem render, sem número inventado.

| # | Doc | O que resolve |
|---|---|---|
| 01 | `01-MISSAO-E-HIERARQUIA-EVIDENCIAS.md` | Missão, pergunta central, classes A–E, fontes prioritárias |
| 03 | `03-FRENTES-P0-P2-E-INVESTIGACOES-A-G.md` | 12 frentes + 7 investigações críticas + cobertura do estudo |
| 04 | `04-SINTESE-SONORA-E-RECEITAS-POR-FUNCAO.md` | Síntese como P0 novo + receitas por função (templates, sem número inventado) |
| 05 | `05-LAB-EXP-SYN-PROTOCOLOS.md` | EXP-01…10 + SYN-01…10: protocolo reproduzível, sem execução |
| 06 | `06-CORPUS-E-MATRIZ-PERFIS.md` | Protocolo comparativo + matriz vazia por perfil |
| 07 | `07-OPERACAO-OFFLINE-WEB-OPENCODE.md` | Biblioteca offline + `webfetch`/`websearch` no OpenCode |
| 08 | `08-HIERARQUIA-E-INGESTAO-DOCUMENTAL-20261030.md` | Hierarquia 1–7, proveniência, alerta de divergência de versões (doc LOM vs Live instalada vs release notes) |


---

## 01-MISSAO-E-HIERARQUIA-EVIDENCIAS.md

# 01 — Missão e hierarquia de evidências

## Missão
Produzir base técnico-científica e operacional para IA compreender, investigar e explicar por que uma combinação de sons gera impacto, pressão, profundidade, clareza e movimento — e outra, aparentemente similar, gera cancelamento, mascaramento, lama, aspereza ou perda de dinâmica.

Especialização: Minimal Psytech, Psytechno, Bush Tech, Dark Progressive, estética Zenon/AlpaKa. Reutilizável.

## Pergunta central
> Por que uma combinação gera impacto/profundidade/clareza enquanto outra gera cancelamento/mascaramento/lama/aspereza/perda de dinâmica?

Resposta exigida: mecanismo + meio de comprovação + alternativa proporcional. Não só preset/número fixo.

## Classes de evidência (carimbar toda afirmação)

| Classe | Tipo |
|---|---|
| A | Física, matemática, padrões técnicos, experimentos reproduzíveis |
| B | Documentação oficial, literatura técnica, demonstrações controladas |
| C | Práticas documentadas de produtores/engenheiros |
| D | Medições verificadas do corpus de referência |
| E | Hipóteses, estética, recomendações não testadas |

Regra: física de onda (A) ≠ preferência de produtor (E). Medição de 3 faixas (D) ≠ regra de gênero.

Registrar sempre: URL, autor, publicação, versão, contexto, unidade, metodologia, limitações, evidência usada.

## Fontes prioritárias
ITU, EBU, literatura psicoacústica/DSP, Ableton, FabFilter, iZotope, Sound On Sound, Zenon Education, docs de instrumentos, produtores reconhecidos. YouTube/entrevista = prática real (C), número informal = classificar pela evidência disponível, nunca promover a (A/B) sem método.


---

## 03-FRENTES-P0-P2-E-INVESTIGACOES-A-G.md

# 03 — Frentes P0–P2 e investigações A–G

## Frentes (teoria + demo + medição + aplicação psytech)

| Pri | Tema | Questões obrigatórias | Cobertura do estudo |
|---|---|---|---|
| P0 | Ondas, senoides, fase | amplitude, ciclo, polaridade, soma ±, defasagem, harmônicos | Parcial (física básica + Zenon). Falta EXP-01/02 |
| P0 | Kick×Bass×Sub | envelope, fase, caudas, overlap, fundamental/harmônicos, sidechain, espaço rítmico | Lacuna discriminante |
| P0 | Mascaramento espectral | competição; auditivo vs cancelamento físico; nível/duração/simultaneidade | Parcial |
| P0 | Dinâmica/impacto | transiente, attack/release, crest, compressão, clipping, headroom, microdinâmica | Parcial |
| P0 | Medição/ganho | dBFS, dBTP, RMS, LUFS, LRA, pico momentâneo, fader/automação | Parcial |
| P1 | EQ/filtros | HP/LP, Q, slopes, group delay, fase mín/lin, pre-ringing, EQ dinâmico | Parcial |
| P1 | Estéreo/mono | M/S, correlação, mono-compat, largura por banda, Haas, decorrelação, PA | Parcial (baixos em mono) |
| P1 | Saturação/harmônicos | não-linear, waveshaping, aliasing, oversampling, comportamento de graves | Parcial-baixa |
| P1 | Espaço/profundidade | reverb, predelay, early, delay, caudas paralelas, ducking, mascaramento temporal | Parcial |
| P1 | Masterização | ordem, bus comp, limiter, true peak, transcode, versões | Lacuna crítica |
| P2 | Percepção | loudness, grave, fadiga, contraste, localização, monitoração | Parcial |
| P2 | Arranjo/identidade | densidade, silêncio, groove, energia, contraponto, transições | Parcial |

## Investigações críticas (exigem prova, não opinião)
* **A. Cancelamento físico:** 0°/90°/180°, amplitude, freq, delay, sinal complexo. Por que inverter polaridade não resolve fase.
* **B. Kick vs bass:** 4 mecanismos — envelope, interferência, mascaramento, bombeamento pós-processamento. Que medição distingue cada um; quando sidechain é necessário vs contingência.
* **C. Alto sem impacto:** LUFS alto + transiente fraco + graves instáveis. Comparar a loudness perceptivo igualado.
* **D. Frequências acumuladas:** mesma banda ≠ problema. Decidem nível, harmônico, simultaneidade, função musical.
* **E. Estéreo frágil:** widening/microdelay/reverb/M-S na soma mono e na profundidade.
* **F. Processo que cria o problema:** EQ/sat/filtros/resample/paralelo gerando defasagem, harmônico, distorção, perda de impacto.
* **G. Ambiente:** separar arquivo vs fone/sala/modo/PA/clube.


---

## 04-SINTESE-SONORA-E-RECEITAS-POR-FUNCAO.md

# 04 — Síntese sonora e receitas por função (P0 novo)

> Tese: se o bass soa vazio, pode faltar harmônico na síntese — volume/EQ não resolve. Sub instável pode ser fase inicial por nota. IA deve saber mecanismo → instrumento → teste → medida.

## O que a IA deve dominar
* Osciladores: seno/tri/saw/square, ruído, fase inicial, retrigger.
* Motores: subtrativo, aditivo, FM/PM, wavetable, granular, espectral, sample, modelagem física.
* Envelopes: ADSR, pitch-env, release, retrigger, legato/glide.
* Modulação: LFO, matriz, automação, sync vs free, áudio-rate.
* Timbre: filtros, ressonância, distorção, wavefolding, formantes.
* Vozes: mono/poly, unison, detune, low-end em mono, estabilidade de graves.
* Sampling: transpose, warp, resample, multisample, transient shaping.
* FX criativo: delay/comb/phaser/flanger/granular/spectral/resonator.

## Instrumentos prioritários (separar física vs controle real)
Ableton Live 12 (Operator, Wavetable, Meld, Sampler/Simpler, nativos, Max) + Serum 2 + Vital. Para cada mecanismo registrar: o que faz fisicamente · quando usar · como construir no instrumento disponível · como medir · efeito colateral · **controle comprovadamente acessível ao executor** (doc do plugin ≠ controle do agente). Versão importa.

## Receitas por função (template, sem número inventado)
Cada receita: hipótese + controles + teste + resultado esperado + alternativa sem plugin pago.

1. Kick (ataque/corpo/cauda independentes).
2. Sub (fundamental estável + harmônicos controlados).
3. Baixo psytech (movimento sem engolir o kick; filtro final pós-distorção — Scionaugh `2YgKSex63Wg`).
4. Bass-rips/FM/bubbly + variações orgânicas.
5. Percussão sintetizada/transientes curtos.
6. Atmos/drones com movimento sem mascarar (Tom Cosm split SUB/HIGH; PML Diva note-length).
7. FX transição/tensão/impacto/vácuo.
8. Camadas acústica+sintética complementares.

Cobertura do estudo: parcial-baixa (Scionaugh rip, Tom Cosm Operator, PML Diva mono/ghost-kick, Vital). Falta SYN-01…10 sistemáticos — ver `05-LAB-EXP-SYN-PROTOCOLOS.md`.


---

## 05-LAB-EXP-SYN-PROTOCOLOS.md

# 05 — Lab EXP + SYN: protocolos (sem execução)

> Nenhum experimento foi executado ainda. Cada EXP/SYN só existe quando entregar os 7 itens. Saída como artefato de medição isolado — nunca aplicada direto no projeto em produção.

## Template obrigatório por experimento
1. Hipótese + mecanismo físico. 2. Arquivos original/processado. 3. Parâmetros, SR, duração, janela e ponto de captura. 4. Gráfico temporal/espectral/fase. 5. A/B auditivo nivelado. 6. Resultado, hipótese rejeitada, limitações. 7. Implicação de mix. Registrar também quando a intervenção **não melhora**.

## EXP-01…10 (mistura/fase/dinâmica)
* 01: senoides 50 Hz a 0°/90°/180°, amplitudes controladas.
* 02: senoide + cópia atrasada → pente por frequência.
* 03: kick+sub com deslocamento gradual → transiente vs energia.
* 04: kick+rolling, envelopes diferentes, mesmas notas/volumes.
* 05: original vs paralelo (latência/filtros/compensação).
* 06: mesma mix estéreo vs mono, perdas por banda.
* 07: EQ fase mínima vs linear em transiente, A/B cego.
* 08: saturação/clipping por nível → harmônicos, aliasing, crest.
* 09: compressão/limitação progressiva a loudness igualado.
* 10: overlap espectral resolvido por arranjo vs volume vs EQ estático vs dinâmico.

## SYN-01…10 (síntese)
* 01: seno vs seno+harmônicos (tradução do sub). 02: fase fixa vs random (estabilidade ataque). 03: unison/detune no grave (soma mono). 04: FM razões/intensidades. 05: pitch-env + amplitude (kick). 06: distorção pré/pós-filtro. 07: glide/duração MIDI (bassline). 08: mod sync vs free. 09: granular/spectral (transientes/artefatos). 10: mesma receita em instrumentos diferentes.

Prioridade de execução futura: EXP-03/04 + SYN-02/05 (estabilidade sub + kick). Motor: render offline do synth (ex.: Serum), >100×, no BPM do projeto.


---

## 06-CORPUS-E-MATRIZ-PERFIS.md

# 06 — Corpus e matriz por perfil (protocolo, sem medição nova)

## Seleção
AlpaKa, Zenon, Kaled Nasser, Gazolla, ISMAIL.M + pertinentes ao DNA do estilo. Separar por perfil: minimal, groove-forward, dark, orgânico, agressivo. Não selecionar só o que confirma número atual. Preservar caráter artístico; não reconstruir obra identificável.

## Protocolo comparativo (obrigatório)
* Trechos equivalentes: intro/marcha/drop/break/retorno. Nivelar antes de comparar impacto.
* Janelas consistentes, método + config declarados (medir em taxa nativa/estéreo; nunca 22,05 kHz/mono para topo/estéreo).
* Medir: espectro, dinâmica, transientes, densidade, energia temporal, estéreo, graves. Stems originais > Demucs (marcar `ESTIMATIVA`).
* Diferenciar arquivo cheio vs instrumento isolado.

## Matriz (vazia — preencher só com medição)

| Perfil | Faixa/trecho | Janela/método | Sub 20–60 | Punch 60–120 | Low-mid | Pres/ar | Crest/LUFS/TP | Estéreo/mono | Conf (A–E) |
|---|---|---|---|---|---|---|---|---|---|
| minimal | — | — | — | — | — | — | — | — | — |
| groove | — | — | — | — | — | — | — | — | — |
| dark | — | — | — | — | — | — | — | — | — |
| orgânico | — | — | — | — | — | — | — | — | — |
| agressivo | — | — | — | — | — | — | — | — | — |

Sem inventar padrão único de volume. Amostra + variabilidade + método + confiança.


---

## 07-OPERACAO-OFFLINE-WEB-OPENCODE.md

# 07 — Operação offline + web no OpenCode

## Arquitetura
Pesquisa externa → biblioteca local versionada → ferramentas sob demanda → DAW + áudio real (read-back, A/B, decisão final de ouvido). Operação diária **não exige web search**.

Categorias locais:
`FUNDAMENTOS/` (física/síntese/DSP) · `INSTRUMENTOS/` (por device/versão) · `RECEITAS/` (por função) · `DIAGNOSTICOS/` (sintoma→hipótese→teste) · `REFERENCIAS/` (pesquisas/corpus/EXP) · `PROJETOS/` (baseline/decisões/evidências). Índice pequeno com gatilhos; reusar skills existentes.

## Web no OpenCode
Docs: `https://opencode.ai/v2/docs/tools/` + `/websearch/`. Web é ferramenta do harness, não do modelo.

* `webfetch`: 1 URL → markdown/texto, sem chave, permissão `webfetch`. Limites: 429 em lote, SPA/JS.
* `websearch`: requer provider `exa|firecrawl|parallel|tavily|tinyfish` via `/connect` ou `TAVILY_API_KEY=…` + `"websearch":{"provider":"tavily"}` (ou `"random"`). Sem chave configurada, a primeira busca pede provider. `websearch:false` remove a tool.
* YouTube: `webfetch` lê página; canal/playlist = `yt-dlp --flat-playlist` + legenda; 429 em canal grande → fallback leitor de web alternativo.
* Ordem: local → URL dada → extração canal/playlist → validar fonte → registrar (caminho+data+limite). Busca aberta opcional. Ausente = `NÃO COMPROVADO`, nunca instrução inventada.

## Chrome real via CDP
* Depuração remota do Chrome na porta `127.0.0.1:9222` responde só via WebSocket (`/devtools/browser/` → `101 Switching Protocols`); `curl /` e `/json/list` devolvem 404 — esperado, não é falha.
* Armadilha: cada conexão nova dispara o prompt "Permitir a depuração remota?" e SPAs re-navegam após `goto` — por isso automação "nunca acerta de primeira". Caminho estável: subir um agente persistente uma vez e falar com ele por HTTP local (`/tabs`, `/exec` com `match` por URL), com checagem de saúde `/ping`.

## Critério de aceite do agente (sem internet)
Explicar comportamento · apontar mecanismo sem confiar em nome de preset · escolher instrumento/técnica compatível provada · construir teste reversível · medir saída real · registrar fontes/parâmetros/versões/limites · reconhecer quando a decisão final é do ouvido humano.


---

## 08-HIERARQUIA-E-INGESTAO-DOCUMENTAL-20261030.md

# 08 — Hierarquia e ingestão documental (2026-10-30)

> Documental primeiro. Sem download indiscriminado. `webfetch` por capítulo + curadoria local com proveniência.

## Manual oficial do Live 12
Existe e cobre 43 capítulos. Documentação LOM: **12.4.5** (`https://docs.cycling74.com/apiref/lom/`). Release notes públicas: **12.4.15** (Adaptive Q no EQ8 + `root_note/scale_*` no M4L) e seguintes. **Alerta de versão:** doc geral, versão da LOM, Live instalado localmente e release notes mais recentes podem divergir — consultar todas juntas e confirmar a versão local antes de aplicar qualquer comportamento.

## Ordem de ingestão
1. Live Manual + Release Notes → comportamento + delta de versão.
2. Instrument Reference → síntese/timbre.
3. Audio Effect Reference → processamento/filtros/dinâmica/espaço.
4. MIDI Effect Reference → transformação/geração.
5. Max for Live + Cycling 74 → DSP/modulação/API.
6. LOM → controle real e limites (ex.: Serum VST3 expõe só `Device On` na LOM).
7. Guias próprios + experimentos → tradução ao arsenal/estética.

Skills/playbooks de agente não substituem a doc oficial.

## Ficha de proveniência por capítulo ingerido
URL + título · versão software · data consulta · device/API · controles documentados · restrições · exemplo reproduzível · relação com saber existente · oficial vs medido local.

## Lacunas de guia por device identificadas
Operator · Meld · Drift · Sampler/Simpler · Max for Live/LOM · matriz de efeitos nativos.
