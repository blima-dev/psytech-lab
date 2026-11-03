# Rastreio — aplicar preset no Serum 2 direto (frente "preset direto")

> Estudo operacional do acervo psytech-lab, anonimizado (data original: 15–16/09/2026, Live 12.4.5/12.4.6,
> Serum 2 VST3 + AU). Objetivo: trocar/carregar preset nas instâncias de Serum **sem clique humano**, com
> rastreio de evidência. Nomes de pistas/patches do set de referência foram anonimizados; nomes de presets
> de fábrica do Serum foram mantidos porque são referência externa.

## 1. O que era verdade no começo (estado herdado)

| Fato | Evidência |
|---|---|
| Geração de `.SerumPreset` e leitura do patch de cada canal já existiam | inventário de patches por canal (arquivo do projeto) |
| `Device.parameters` de cada Serum = **1** ("Device On") | medido em 24 devices, código dentro do Live (15/09) |
| Escrever estado de plug-in no `.als` → crash do Live | log de crash do sistema: thread principal dentro de `Serum2.vst3` |
| Browser interno do Serum carrega preset (busca + duplo clique) | funcionou 1×; abrir a janela por coordenada falhou depois |

## 2. Medições desta rodada

### 2.1 LOM nativo (hipótese "PluginDevice.presets") → REFUTADO
- `Device.presets` existe (StringVector) e `selected_preset_index` existe (int, com listener).
- **Medido nas 24 instâncias** (VST3 `PluginDevice` e AU `AuPluginDevice`, instrumentos e FX):
  `presets = ["Default"]` (1 entrada; IndexError no índice 1), `selected_preset_index = 0`.
- Leitura: o Serum **não publica** a lista de presets para o host → trocar por índice via LOM não tem para
  onde ir. Consequência: `selected_preset_index` não serve como fundação.

### 2.2 Estado de plug-in por arquivo (`.adv` / `.aupreset`) → RECEITA VALIDADA OFFLINE, sem teste no Live
- Formato do estado: `XferJson\0` + (len,flags) + JSON meta + (len,flags=2) + zstd → CBOR.
- **Achado que explica o crash**: o AU **descarta em silêncio** estado em que `processor` e `controller` usam
  o MESMO corpo (o corpo do `.SerumPreset`). Ele aceita e aplica quando:
  - `processor` = estado COMPLETO (162 chaves) com os valores do patch sobrescritos;
  - `controller` = corpo de controller (~59 chaves) com `presetName/presetAuthor/presetDescription/selectedPresetPath` do alvo;
  - o blob `data` é **regerado pelo próprio plug-in** (sem risco de dado velho).
- Verificação offline (instanciando o AU fora do Live, round-trip de `kAudioUnitProperty_ClassInfo`):
  estado devolvido = alvo; **som mudou** (default −18,8 dBFS/4334 Hz · patch antigo −30,1/3194 · artefato
  −37,1/2108; correlação ≤0,21).
- **NÃO VERIFICADO**: carregar esses artefatos DENTRO do Live (o teste exige set descartável e aceitar o
  risco de crash).
- Observação: o Live **não registra** `.aupreset` no `Info.plist`; e não há `.adv` de plug-in na máquina
  (o molde foi construído a partir do `PluginDevice` do próprio `.als`).

### 2.3 Program Change (VST3) por clip MIDI → CAMINHO MAIS PROMISSOR
- Fontes (VERIFICADO por leitura): Live 12.2+ suporta PC em VST3 (release notes oficiais); KB do Ableton
  sobre Bank/Sub-Bank/Program em clips (banco = CC0, sub-banco = CC32); **staff da Xfer confirma que o
  Serum 2 aceita PC** ("not documented in the manual"; Live adicionou suporte em 12.2).
- Local: todo `<MidiClip>` do `.als` tem `<BankSelectCoarse>/<BankSelectFine>/<ProgramChange>` (default −1)
  e o LOM **não** expõe esses campos → edição offline, cirúrgica.
- **⚠️ Armadilha de teste:** set descartável só salva se for **pasta de projeto completa** (`Samples/` +
  `Ableton Project Info/`) — cópia solta fora de pasta de projeto é recusada pelo save; e o transporte via
  API pode entrar em stall na cópia.

### 2.4 Preferência do próprio Serum (`Enable CCForRockers`) → plano B, exige backup
- Manual instalado do Serum 2, Apêndice D: `Enable CCForRockers: 1` (CC) ou `2` (notas) +
  `CCForRocker Preset +/-`; setas ‹ › navegam a pasta atual; ↑/↓ no browser.
- `Serum2Prefs.json` existe com essas chaves; risco: é **global** (todos os projetos), passo relativo (±1) e
  histórico de "preset skips" ao tocar nota. Só com backup do prefs.

## 3. Conclusão (parecer da época)

1. **LOM nativo está fechado** pelo próprio plug-in: medido em 24/24 instâncias. Não insistir.
2. **Cirurgia de estado no `.als` continua proibida** (crash documentado). A receita coerente existe e
   funciona fora do Live, mas o carregamento dentro do Live **não foi testado**.
3. **O caminho mais barato e correto é o Program Change por clip MIDI** (menor mecanismo que resolve, nativo
   do Live, sem infra nova). Falta o teste com set descartável — e o resultado já é útil musicalmente
   (troca de patch dentro do arranjo).
4. **Fallback documentado**: `.adv` coerente → carga nativa pelo Live; e por último automação da janela do
   Serum (1× provado, frágil) — nunca como arquitetura.
5. Para poucos canais com patch fora de papel: os 2 cliques continuam sendo o caminho mais rápido; a
   automação é para escala.

## 4. Regras que ficam (lições de método)

- **Nativo primeiro**: testar o que já existe no Live/LOM antes de construir ponte.
- **Menor mecanismo correto**: só criar registry/PC/loader quando houver lacuna comprovada.
- **Nada de state surgery no `.als`/VST3** (risco alto, evidência de crash).
- **Set descartável só vale se for pasta de projeto completa** (`Samples/` + `Ableton Project Info/`) —
  cópia solta não salva.
- **Set auto-contido**: `File > Collect All and Save` + gate de mídia (todas as referências dentro da pasta).
- Evidência crua sempre: caminho + medição + comando.

## 5. Teste P1 (Program Change) — primeira rodada: NÃO CONCLUÍDO (armadilha de verificação nomeada)

1. Grade de sondagem offline: 6 pistas, bancos 0/1 × programas 0..2 — edição verificada (6 clips alterados,
   404 intactos, audit ok).
2. Playback cruzou **todos os 6 clips** — confirmado pelo playhead.
3. Save da cópia ok (pasta de projeto completa).
4. **Read-back: patches IGUAIS ao baseline nos 6 canais.**

**Por que isso NÃO fecha o veredito:** o read-back depende do estado que o Live grava no `.als`, e já havia
sido medido que **o Live salva o estado em cache do plug-in sem consultá-lo** (teste de sentinela). Se a
troca aconteceu *dentro* do Serum, o save pode persistir o estado antigo → **falso negativo possível**.

**Tentativa de read-back independente (áudio A/B):** captura de 8 s de uma pista em solo na cópia = OK; a
captura equivalente no set de trabalho **falhou** (diálogo de save bloqueando a troca de documento e o
`start_playing` pela LOM não engatando de forma consistente). Sem o "antes", o A/B não fecha.

**Receita para fechar (determinística):** (a) criar um clip de SESSÃO com 3-4 notas numa pista de Serum via
LOM, salvar; (b) fechar e editar o `.als` para pôr `BankSelectCoarse/Fine/ProgramChange` nesse clip de sessão
(o manual do Ableton é explícito: o PC sai **ao dar launch no clip** — mais determinístico que depender do
playhead cruzar clip de arranjo); (c) reabrir e dar launch; (d) verificar por áudio **e** por janela do Serum.

## 6. Cruzamento com pesquisa externa e o que muda

- Confirmação pelas fontes oficiais: o manual do Live autoriza Bank/Sub-Bank/Program para plug-ins (até 128³
  combinações); o Live 12.2 trouxe PC para VST3 (com correções em 12.2.5/12.3).
- **Nuance de verificação importante**: no Serum 2, **Module Locks sobrevivem à troca de preset** (manual
  oficial) → "preset X selecionado" não prova que o som inteiro é X; o read-back ideal é áudio e/ou janela do
  Serum, não só o nome.
- Fonte `github.com/Serum-2` descartada (aparência de SEO/repack); autoridade = `xferrecords.com`.
- **Melhoria real no fallback**: desde o **Live 12.4.3**, um device Max for Live consegue abrir/fechar a
  janela de editor do plug-in via LOM → o clique frágil por coordenada sai da equação.
- Repos de referência citados (não instalar ainda): gerador de `.SerumPreset` (não carrega), mapa CC,
  fork com "128 params curados", host VST em Max `vst~` (mudança arquitetural grande).

**Sequência final:** LOM nativo (❌ medido: lista vazia em 24/24) → P1 PC por clip de sessão (pendente) →
P2 `.adv` de estado coerente (receita validada offline) → P3 M4L abre editor + automação interna do Serum
(último recurso, mais barato desde o 12.4.3).

---

## 7. ATUALIZAÇÃO 16/09 — spike executado: PC **não** validado (negativo com read-back duplo)

Set descartável completo (cópia do set de referência + `Samples/` + `Ableton Project Info/`), Live **12.4.6**.
Ferramenta nova: injetor de `ProgramChange`/`BankSelectCoarse` por faixa, por bytes, com dry-run + validação
XML; `als_audit` ok nas duas sondas.

| Teste | Configuração | Resultado |
|---|---|---|
| A — clip de ARRANJO | PC=0/1/2 em 3 pistas de sonda (open hat / sub bass / motif), 44 clips alterados, playhead 20→262 | **nenhum preset mudou** |
| B — clip de SESSÃO (`ClipSlot.fire()`) | clips de sessão das 3 pistas patchados, disparados e tocando | **nenhum preset mudou** |
| C — banco + programa | `BankSelectCoarse=0` + PC 0/1/2 (43 clips) | **nenhum preset mudou** |

**Read-back duplo, dois métodos independentes concordando:** (i) leitura do `presetName` no `.als` salvo;
(ii) **janela do Serum aberta por código** (`Device.is_editor_open = True` — capacidade verificada) +
captura de tela → a pista-sonda mantinha o patch original.

**Outros fatos medidos:**
- `PluginDevice.presets = ["Default"]` nas **26** instâncias (re-confirmado).
- **O browser do Live não indexa `.SerumPreset`** → o hot-swap de preset do Serum pelo browser **não tem
  item para carregar**.
- O Live **detecta** o parâmetro de PC do Serum: `VST3: Found 1 program change parameters for plugin Serum 2`
  (26× no load).
- `Serum2Prefs.json`: `CCForRockers = 0`, todos os CCs em `-1`; **não existe switch de Program Change** nas
  preferências.
- **`open "<outro>.als"` troca o Set sem `Cmd+Q`** (com o doc limpo, sem prompt) — reload mais barato.
- O `.als` salvo guarda o `presetName` de cada Serum na meta do `ControllerState` → **read-back de preset por
  arquivo, sem UI**.

**Conclusão:** com **3 configurações e 0 mudanças** (e read-back duplo), a rota do Program Change **não
estava validada** — e a observação anterior ("PC=1 injetado num clip de sessão → Init Preset") **não se
reproduziu**. **Discriminador:** setar o PC **pela UI** (painel de propriedades do clip) na sonda e ver se o
preset muda — se mudar pela UI e não pelo XML, o problema é o campo/leitura do campo; se não mudar nem pela
UI, o Live não está entregando PC ao Serum na versão testada.

### 7.1 SPIKE S2 — **O PC FUNCIONA: era BANCO, não suporte**

Sonda com 3 pistas com clips de sessão patchados:

| pista | `BankSelectCoarse` | `ProgramChange` | resultado |
|---|---|---|---|
| sonda 1 | 15 | 0 | sem mudança |
| sonda 2 | 16 | 0 | sem mudança (**PC=0 = no-op**) |
| **sonda 3** | **16** | **1** | **MUDOU: patch original → `CH - Beach Club`** (preset de fábrica) |

Disparo = `ClipSlot.fire()` (o PC sai no **launch**; playhead cruzando clip de arranjo **não** dispara).
Leitura = `presetName` no `.als` salvo. A troca **foi persistida pelo save** (no arquivo).

**⚠️ CRASH — 2× no mesmo dia, assinatura IDÊNTICA:** logs de crash do sistema no instante da troca de set e
~20 s depois do save, transporte tocando: `EXC_BAD_ACCESS KERN_INVALID_ADDRESS` · **MainThread** · 5 frames
idênticos dentro do `Serum2` chamados de `__CFRunLoopDoTimer` → é o **timer do Serum na thread principal**.
**Correlação — HIPÓTESE (não provada):** burn de ~1 core e crash podem compartilhar um loop/timer interno;
o que está provado é só que **o timer que caiu é do Serum** (medição com `sample` mostrou os frames do
burn em outra faixa de endereços; discriminador: novo `sample` pós-upgrade × este baseline).
**Procedência dos binários (verificada com `codesign -dv`):** o **VST3 era `adhoc` / sem Team ID (build
modificado, não assinado pela Xfer)**; o **AU era genuíno** (`Developer ID: Steve Duda`). Os pacotes vinham
de distribuição não oficial e **os crashes + o burn estavam no VST3** → "bug da versão" concorre com "build
não oficial" como causa. Baseline limpo = instalar build **assinado pela Xfer** e repetir o gate.
**Mistura VST3 × AU (contagem lida do `.als`):** **19 VST3 + 7 AU** — o PC vale para os 19 VST3.

### 7.2 A REGRA DO PC FOI RESOLVIDA (16/09) — agora dá para escolher preset **POR NOME**

- **bank** = posição **1-based** da PASTA do preset na lista alfabética **case-sensitive** de todos os
  diretórios de `…/Serum 2 Presets/Presets`;
- **program** = índice **0-based** na lista do **`presets.db`** daquela location, em ordem de nome
  **case-insensitive**.
- **Validado no Live (10 pontos sem erro):** bancos 13–17 → `BA - Bubba`/`BL - Kinderjoy`/`BR - Brass Wall`/
  `CH - Beach Club`/`DR - Clap Machine` (presets de fábrica); e 4 presets de User/alvo do projeto validados
  no mesmo ciclo.
- **Ferramenta:** um mapa bank/PC por nome de preset, que imprime **fingerprint** a cada chamada (versão do
  Serum + hash/mtime do `presets.db` + hash/contagem da árvore de Presets).
- **Limites:** `ProgramChange=0` é **no-op** (preset no índice 0 não é selecionável assim); pastas privadas
  do projeto não resolvem → usar as cópias em `User/`.
- **Persistência pós-reload PROVADA:** sonda salva com presets trocados, **fechada, reaberta** e, ao forçar
  um save, os nomes continuavam os trocados ✓ (fecha o critério "save → fechar → reabrir").
- **A regra é do CORPUS ATUAL, não do Serum em abstrato:** a lista viva muda com a pasta; o fingerprint do db
  (neste ciclo: 659 KB, 72 locations / 2.162 presets; 91 dirs; 1.624 arquivos) faz parte da prova.
  **Recalcular sempre — o par (bank, PC) não é para memorizar.**
- **Consequência:** a varredura cega de bancos **morreu** — o par (bank, PC) de qualquer preset em
  `Factory/`/`User/` é **calculável**. O gargalo de "trocar preset sem clique" está fechado por cálculo.
