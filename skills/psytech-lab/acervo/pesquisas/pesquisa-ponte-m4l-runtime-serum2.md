# Pesquisa: Ponte Max for Live e rota runtime de troca de preset do Serum 2 (sem GUI, sem salvar Set)

Data: 2026-09-16. Ambiente de referência: Live 12.4.6, macOS arm64, controle via LOM.
Contexto já verificado (rodada 1): Program Change funciona no Serum 2 VST3 via injeção direta de `BankSelectCoarse` + `ProgramChange` no XML do .als na LAUNCH de clip; bank = posição 1-based da PASTA em "…/Xfer Records/Serum 2 Presets/Presets" (alfabética, case-sensitive), program = índice 0-based case-insensitive no presets.db — mapa muda entre versões (2.0.16 vs 2.1.5). `PluginDevice.presets` = ["Default"]; LOM não expõe clip.program_change.

Status: CONCLUÍDA (7 eixos pesquisados; rotulados VERIFICADO / INFERÊNCIA / NÃO ENCONTRADO / NÃO VERIFICADO).

---

## 1. M4L/MIDI → VST3 Program Change no Serum 2 (rota oficial)

**VERIFICADO** — Thread oficial da Xfer "Please consider bringing back Program Change to Serum 2 :)" (https://xferrecords.com/forums/general/please-consider-bringing-back-program-change-to-serum-2):
- Criada 21/03/2025 por "stelvio"; +1s de cozza_frenzy-splice (elogia o mapeamento bank=pasta do Serum 1), aleksandr.gilfanov, glenmacnab.
- **Resposta da Xfer (nick_xfer, 05/06/2025): "Serum 2 actually does support MIDI program changes"** — mas não está documentado no manual. Texto-chave: "It requires cooperation from the DAW because VST3 plug-ins do not directly receive MIDI". Linkou post confirmando que **Ableton Live adicionou o suporte na 12.2**.
- Implicação direta: a rota MIDI→PC dentro do Live 12.2+ é a via OFICIAL endossada pela Xfer; o que falta é só um emissor de MIDI dentro do Set (um bridge M4L), já que o LOM não expõe clip.program_change e o .als injetado só dispara na LAUNCH.
- Nota: stelvio confirma que "a simple Max for Live Program Change device works" como emissor (afirmação de usuário, não teste — INFERÊNCIA de viabilidade, consistente com o design de um bridge próprio).

## 2. Criar/instalar .amxd programaticamente SEM abrir o IDE do Max

**VERIFICADO** — repositório `bschoepke/ableton-live-mcp` (https://github.com/bschoepke/ableton-live-mcp, MIT, 223 stars, testado pelo autor em Live Suite 12.3.8 macOS). Arquivos lidos via raw.githubusercontent.com: `src/agent_m4l.py`, `src/ableton_paths.py`, `scripts/build_agent_m4l_device.py`, `scripts/build_agent_audio_tap.py`, `m4l/agent_m4l_host.js`.

### Formato do arquivo .amxd (container binário + patcher JSON)
- Container IFF-like, montado em `_minimal_amxd_container()` (agent_m4l.py L238-250):
  - `b"ampf"` + `u32 LE = 4` (versão) + 4CC do tipo + `b"meta"` + `u32 LE = 4` + 4 bytes zero + `b"ptch"` + `u32 LE = len(payload)` + payload.
  - Payload = JSON do patcher Max (formato `{ "patcher": { "boxes": [...], "lines": [...] } }`) em UTF-8 + byte `\x00` final.
  - 4CC do tipo: `aaaa` = audio effect, `iiii` = instrument, `mmmm` = MIDI effect (hex conferido: 0x61616161=1633771873, 0x69696969=1768515945, 0x6D6D6D6D=1835887981; esses mesmos inteiros vão no campo `"amxdtype"` do JSON do patcher).
- Estratégia dupla em `build_amxd()` (L253-264):
  1. **Template**: pegar `<Live.app>/Contents/App-Resources/Misc/Max Devices/Max MIDI Effect.amxd` (procura em `ableton_paths.py` L79-142: candidates incluem `Contents/App-Resources/Misc/Max Devices`) e substituir SOMENTE o chunk `ptch` (`replace_ptch_chunk()`, L201-219) — preserva metadados do template.
  2. **Fallback sem template**: montar o container mínimo do zero (acima). O repo funciona no autor com Live 12.3.8; os testes do repo (`tests/test_agent_m4l_build.py`) validam a estrutura dos bytes.
- **INFERÊNCIA**: para um bridge de program change nem precisa do template — o container mínimo + patcher JSON com `amxdtype: 1835887981`, `midiin`/`midiout` e UI `live.*` basta.

### Patcher JSON mínimo necessário (campos observados no `make_host_patch()`, L291-454)
- `patcher.fileversion: 1`, `appversion {major:8,...}`, `classnamespace: "box"`, `rect`/`openrect`, `openinpresentation: 1`, `devicewidth`, `gridsize`, `boxes`, `lines`, `amxdtype`.
- Boxes: `{ "box": { "id", "maxclass": "newobj"|"message"|"live.numbox"|..., "text": "midiout", "varname", "patching_rect": [x,y,w,h], "parameter_enable": 1, ... } }`.
- Lines: `{ "patchline": { "source": [id, outlet], "destination": [id, inlet] } }`.

### Instalação sem IDE
- Copiar o .amxd (e o .js companheiro, se houver) para a User Library: `~/Music/Ableton/User Library/Presets/MIDI Effects/Max MIDI Effect/` (`install_folder()` L183-185). O device aparece no navegador do Live e pode ser inserido na cadeia via LOM (equivalente a `create_midi_device` / browser) ou manualmente.
- O repo usa `js agent_m4l_host.js <args>` dentro do patcher — JS externo carregado do lado do .amxd (mesmo diretório).

### Mecanismo de amarração comando→ação (o que copiar de ideia pro bridge)
- 3 caminhos de controle no host deles: (a) `filewatch` num JSON de comandos; (b) UDP `udpreceive` com porta derivada por hash do instance_id; (c) **parâmetro do device como trigger**: `live.path this_device parameters 1` → `live.observer value` → dispara o JS (L316-319, 351-357). Ou seja: **LOM escreve no DeviceParameter → observer dentro do patcher executa ação** — o padrão FIRE.

**INFERÊNCIA**: um patcher com `[live.numbox Bank] [live.numbox Program] [live.button FIRE]` + `midiformat`/`midiout` + observer no FIRE é gerável em ~100 linhas de Python, sem Max IDE, e instalável por cópia de arquivo.

### Complemento — a rota PC→VST3 no Live 12.2+ (release notes oficiais)

**VERIFICADO** — https://www.ableton.com/en/release-notes/live-12/ :
- Live 12.2 (11/06/2025): **"Live now supports setting MIDI program change events in VST3 plug-ins."** — confirma a fala do nick_xfer.
- 12.2.5 (27/08/2025): "Fixed MIDI program change for some VST3 plug-ins, including Korg M1, Sylenth1, and Viper" — houve refinamento por plugin depois do 12.2.0; um Live 12.4.6 está depois desses fixes.
- 12.2.5/12.3 fix: "Fixed a bug where Arrangement clips starting at 1.1.1 would sometimes fail to send a program change when starting playback immediately after loading a Set" — bugs de PC em clip existiram e foram corrigidos; reforça que PC-em-clip é a rota suportada pelo host.
- **LOM relevante para instalação do bridge**: 12.3 (25/11/2025) adicionou **"Track.insert_device and Chain.insert_device"** — dá para inserir o .amxd na cadeia por código, antes do Serum.
- 12.4: parâmetros de M4L podem ser marcados non-automatable/non-undoable; "Max for Live Developer Mode" no menu Options.

**Contraponto histórico** (pré-12.2, NÃO se aplica a Live 12.4.6+): threads antigas do fórum Ableton ("VST3 no Program Change" https://forum.ableton.com/viewtopic.php?t=244159; "MIDI Program Changes sent as CC0" t=246273) e post do Steinberg (https://forums.steinberg.net/t/midi-program-change-not-handled-correctly-in-some-daws/959595) documentam que antes o Live não passava PC a VST3 e que VST2 era o workaround. Uso: apenas para entender por que material antigo na internet diz "impossível" — está desatualizado para 12.2+.

**A questão aberta (marcada como NÃO VERIFICADO localmente)**: se um `midiout` de M4L MIDI Effect a montante do Serum VST3 entrega PC da mesma forma que o PC de clip. As fontes dizem que o Live 12.2+ "seta PC em VST3", mas nenhuma fonte pública achada até agora distingue o emissor (clip vs MIDI track vs M4L midiout). O teste mínimo no fim do arquivo cobre exatamente isso.

## 3. Controlar device M4L pelo LOM

**VERIFICADO** — Docs oficiais:
- LOM (https://docs.cycling74.com/max8/vignettes/live_object_model): `DeviceParameter` representa parâmetro automável de device MIDI/áudio; `MaxDevice` herda de `Device` → parâmetros de patcher M4L (objetos `live.*` com `parameter_enable=1`) aparecem como DeviceParameter normais, acessíveis de FORA do device (`live_set tracks N devices M parameters K`), inclusive de um Python LOM externo.
- Ableton "Controlling Live using Max for Live" (https://help.ableton.com/hc/en-us/articles/5402681764242-Controlling-Live-using-Max-for-Live): trio `live.path` / `live.object` / `live.observer`.
- Max Cookbook UCI (https://music.arts.uci.edu/dobrian/maxcookbook/changing-live-device-parameters-live-api): padrão `live.path` → `live.object` → `set value`.

**VERIFICADO (código em produção)** — o `ableton-live-mcp` usa exatamente o padrão FIRE robusto: dentro do patcher, `live.path this_device parameters 1` + `live.observer value` + `prepend __command_trigger` → JS executa comando (agent_m4l.py L316-357; agent_m4l_host.js L1364-1401 cria observers automáticos para cada parâmetro com parameter_enable). O lado de fora (LOM/Python) escreve `DeviceParameter.value` e o observer interno dispara a ação.

**Gotcha documentado do FIRE por botão (INFERÊNCIA com fontes)**:
- Refpage do `live.button` (https://docs.cycling74.com/max5/refpages/m4l-ref/live.button.html): o bang sai da outlet ao CLICAR. Fóruns (ex.: https://cycling74.com/forums/parameter-modulation-without-adding-to-undo-history) mostram que `set value` via API muda o parâmetro sem disparar a outlet. Logo: NÃO confiar na outlet do live.button para trigger remoto; usar **observer do valor** (detecta 0→1) — que é o que o ableton-live-mcp faz — ou um `live.numbox` 0/1.
- Como o bridge é um patcher próprio, o observer entra dentro dele: LOM faz `param FIRE.value = 1.0` → observer interno vê → patcher monta Bank Select (CC0) + PC e manda pro `midiout`. Estado observável no sentido inverso: `live.observer` no device + LOM observa `parameters K.value` de fora — dois canais de leitura.

**Bônus VERIFICADO (release notes Live 12)**: parâmetros M4L são automáveis → 12.4 permite marcar non-automatable/non-undoable. Automatizar FIRE/Bank/Program por envelope de clip seria rota alternativa sem XML injection — manter em mente como plano B.

## 4. ProgramChanges.txt no Serum 2

**VERIFICADO (Serum 1, oficial)** — thread "Program change" (https://xferrecords.com/forums/general/program-change), steve_xfer 21/04/2017: PC no Serum = "bank (+1) and program # for a dedicated subfolder/item in the preset menu"; **"bank 1 message is dedicated for ProgramChanges.txt (if you want an absolute config, e.g. for a live show)"**.
**VERIFICADO (changelog Serum 1)** — gist 0xdevalias (https://gist.github.com/0xdevalias/a537a59d1389d5aed3bc63b544c70c8d): 1.36b3 "Program change improvements for VST3 / program change list"; 1.36b8 fix de ProgramChanges.txt com filename em branco. ProgramChanges.txt é recurso REAL do Serum 1.
**NÃO ENCONTRADO (Serum 2)**:
- Changelog do Serum 2 no mesmo gist: ZERO menções a ProgramChanges.txt ou "program change" (varri 2.0.x); a única entrada parecida é 2.0.24 "Fixed Preset prev/next button sometimes unexpectedly selecting ARP - Aardvark after loading a session".
- Threads 2025 ("Program change" citado acima; "Program Change for live use of Serum 2" https://xferrecords.com/forums/general/program-change-for-live-use-of-serum-2): nenhum usuário cita ProgramChanges.txt no Serum 2; nenhum reply de staff nessa thread.
- Buscas por "Serum 2 ProgramChanges.txt" só retornam material do Serum 1.
- **INFERÊNCIA**: no Serum 2 a resposta do nick_xfer ("does support MIDI program changes... not documented in the manual") + relato do stelvio (funciona via VST3, bank depende de quantos banks instalados) indicam que o mapeamento bank=pasta/program=índice permanece (bate com a regra medida em runtime), mas a **lista absoluta via ProgramChanges.txt parece não ter sido portada/exposta no Serum 2** — ou está oculta sem documentação. Mataria o problema de enumeração, mas hoje é aposta; testável em 2 min (criar ProgramChanges.txt em …/Xfer Records/Serum 2 Presets/ e mandar bank 1) — incluído no próximo teste.

## 6. Rotas runtime alternativas sem GUI

### 6a. Scripting/API própria do Serum 2
**NÃO ENCONTRADO** — não há SDK/scripting API pública do Serum 2 (buscas em fóruns Xfer, Reddit, GitHub). O que existe de "programático" é engenharia reversa do formato .fxp: gist 0xdevalias "Reverse Engineering Serum Preset Format" (https://gist.github.com/0xdevalias/135a18e979ac8e302ebbc700a50a8d74) com CLI para converter preset Serum 2 ↔ JSON. Serve para GERAR presets, não para trocar preset em runtime.

### 6b. CC de preset next/prev ("CCForRockers") — CONFIRMADO no Serum 2
**VERIFICADO** — thread oficial "CC for serum" (https://xferrecords.com/forums/general/cc-for-serum), **nick_xfer 21/05/2025** lista as chaves do `Serum2Prefs.json` (macOS: `~/Library/Preferences/Serum2Prefs.json`) que disparam switching por CC, default `-1` (desligado):
- `"CCForRocker Preset +"` e `"CCForRocker Preset -"` ← as que interessam;
- também OSC A/B/C/N + e - (switcher de tipo de oscilador).
Configurar (com Serum fechado) o número do CC 0–127 no lugar de -1 → cada CC recebido avança/retorna 1 preset. Confirmado em prática por usuário da thread ("that was exactly my problem" — o comportamento indesejado de trocar preset por CC existia com as chaves != -1).
- **Limitação INFERIDA**: é rota RELATIVA (anda ±1 na mesma ordem do browser), sem salto absoluto nem feedback do nome. Combinada com o presets.db (ordem conhecida), dá para WALK até o alvo — N Updates de CC. Custo: N mensagens MIDI; risco: dessincronia se alguém trocar preset na mão. Rota de fallback, não primária.
- Obs: no Serum 1 havia também a chave geral `"CCForRockers": 1` (guia Reddit https://www.reddit.com/r/ableton/comments/qt2y5c/changing_serum_presets_using_cc_from_one_midi/); no Serum 2 o nick lista as chaves por-rocker.

### 6c. Morph/variation entre presets
**NÃO ENCONTRADO**: nenhuma evidência de morph cross-preset nativo no Serum 2 — checado release notes 2.0.x (gist), fóruns, sumários de features E o manual oficial completo (PDF 354 págs., extraído com pdftotext): o "Morph - Crossfade" documentado é interno do OSCILLADOR (entre wavetables/formas), não entre presets.

### 6d. Manual oficial do Serum 2 — Appendix C documenta as rotas de preset change
**VERIFICADO** — download do manual oficial (https://www.xferrecords.com/manual/serum-2/docs entrega o PDF completo, 26 MB) + extração com pdftotext. **Appendix C: "Editing the Serum Preferences File"** (págs. 339–343) documenta textualmente:
- Arquivo: `Serum2Prefs.json` — macOS `~/Library/Preferences/`, Windows `%APPDATA%\Xfer\Serum 2\`.
- "Enabling Preset Changes using a MIDI Controller" (p. 340–341): `"Enable CCForRockers": 1` + `"CCForRocker Preset +": <CC>`, `"CCForRocker Preset -": <CC>`; **"In Serum, a value of 64 or above triggers the action (changes the preset). Similarly, Serum needs to receive a value below 64 before the action can be triggered again."** (histerese — detalhe de implementação crítico para o bridge).
- "Using Notes to Trigger Preset Changes" (p. 341–342): `"Enable CCForRockers": 2` + os mesmos rockers mapeados a NÚMEROS DE NOTE.
- Análogos para osciladores: `"CCForRocker OSC A/B/C/N +/-"`.
- **Importante**: varri o texto integral extraído do manual — ZERO ocorrências de "program change", "ProgramChanges.txt" ou "bank select". A rota bank/program absoluta funciona (provada em runtime) mas é NÃO documentada; a documentada é a relativa por CC/NOTE.

## 5. Consultar Program Lists direto do VST3 (IUnitInfo) sem GUI

### Como o PC funciona em VST3 (base técnica)
**VERIFICADO** — Sample oficial da Steinberg "programchange" (https://github.com/steinbergmedia/vst3_public_sdk, `samples/vst/programchange/source/plugcontroller.cpp`): PC em VST3 = parâmetro com flag `ParameterInfo::kIsProgramChange` + `ProgramList` registrada via `IUnitInfo` (`addProgramList`, `prgList->addProgram(title)`). É por esse parâmetro que o host (Live 12.2+) injeta o PC. Doc oficial: https://steinbergmedia.github.io/vst3_dev_portal/pages/Technical+Documentation/Presets+Program+Lists/Index.html e https://steinbergmedia.github.io/vst3_dev_portal/pages/Technical+Documentation/VST+3+Units/Index.html.
- **INFERÊNCIA decisiva**: se o Serum 2 aceita PC (aceita — nick_xfer + teste em runtime), ele QUASE CERTAMENTE publica um `kIsProgramChange` parameter e possivelmente uma ProgramList enumerável. Se a ProgramList existir, um mini-host consegue puxar a LISTA ABSOLUTA de nomes de preset direto do plugin — mataria a fragilidade do presets.db por versão.

### Ferramentas concretas
- **vst3sdk `validator`** — VERIFICADO. Host de linha de comando oficial, fonte incluída: https://github.com/steinbergmedia/vst3_public_sdk `samples/vst-hosting/validator/` (usage: `vstvalidator [options] vst3module`, validator.cpp L389). O teste embutido `ProgramInfoTest` (`source/vst/testsuite/unit/scanprograms.cpp`) chama `IUnitInfo::getProgramListCount / getProgramListInfo / getProgramName` e IMPRIME cada lista e nome de programa ("Programlist %03d (id=%d): \"%s\" (%d programs)"). Build via CMake do vst3sdk; roda em macOS arm64 headless.
- **carla-discovery** (Carla/falkTX) — VERIFICADO QUE NÃO SERVE para isso: o código (`source/discovery/carla-discovery.cpp` L1807) IGNORA parâmetros com flag `V3_PARAM_PROGRAM_CHANGE` e o scan VST3 não enumera program lists (a contagem de "programs" no arquivo é do SF2/fluidsynth). Fonte: https://github.com/falkTX/Carla.
- **pedalboard / pedalboard-pluginary** (Python) — VERIFICADO que existem (https://github.com/spotify/pedalboard, https://github.com/twardoch/pedalboard-pluginary): carregam VST3 headless e listam PARÂMETROS; **NÃO ENCONTRADO** suporte a IUnitInfo/program lists no pedalboard.
- **Host Python dedicado a IUnitInfo** — NÃO ENCONTRADO (buscas GitHub topics/vst3, fóruns JUCE/Steinberg). Caminho realista: ctypes sobre a interface C do VST3 ou fork do validator.
- **rust-vst3-host** (https://github.com/HelgeSverre/rust-vst3-host) — host headless em Rust, referência de implementação (NÃO VERIFICADO se expõe program lists).
- **Alguém já fez com Serum 2?** NÃO ENCONTRADO em nenhuma fonte pública (fóruns Steinberg/JUCE/KVR/Reddit/GitHub). O Reddit r/serum só registra bug de VST3 do Serum 2 com mensagens de parâmetro relativo/absoluto, já corrigido pela Xfer (https://www.reddit.com/r/serum/comments/1jj4wlh/noticed_a_bug_w_serum_2/). Rodar o validator no Serum2.vst3 é experimento inédito e barato.

## 7. Devices prontos da comunidade

- **swina/Max4Live-ProgramChange-** (https://github.com/swina/Max4Live-ProgramChange-) — VERIFICADO que existe: "Program Change Controller + Basic CC#'s (BETA)", device M4L que manda PC + CC7/CC10 com lista de presets via arquivo txt (feito para EmulatorX3, genérico na essência). Ressalva: o git tree só contém LICENSE — os binários do device não estão no repo atual (talvez em releases); internals NÃO VERIFICADOS. Serve de referência de UI, não como solução pronta p/ LOM.
- **Presets by killihu (Isotonik Studios)** (https://isotonikstudios.com/product/presets-by-killihu/) — VERIFICADO que existe (pago): gestão de presets/estados em M4L, com 4 bancos A–D × 64 presets e controle remoto por notes/CC/**program change**. Foco em estado de devices Live, não em PC absoluto para VST3 externo; LOM-controllável por ser M4L, mas é caixa-preta paga.
- **Thread Reddit "Change serum preset with a macro"** (https://www.reddit.com/r/ableton/comments/1osi9yp/change_serum_preset_with_a_macro/) — busca indica que alguém postou um device open-source gratuito p/ trocar preset do Serum via macro; **NÃO ENCONTRADO** o link/nome (Reddit bloqueou scraping; arquivo pullpush dos comentários não contém o link).
- **YouTube "A better way to switch presets in Ableton Live"** (https://www.youtube.com/watch?v=B5RaW4hEcTI) — descreve troca de presets sem pré-carregar devices, com device no GitHub ("github.com/ldr..."); link completo NÃO ENCONTRADO.
- **maxforlive.com** — busca direta bloqueada por Cloudflare (403); NÃO ENCONTRADO device específico "Serum program change" via buscas indiretas.
- **Conclusão**: NÃO ENCONTRADO um device pronto que faça exatamente (M4L MIDI Effect mínimo + Bank/Program absolutos + disparo via LOM) para Serum 2 no Live 12.4.6. O ecossistema confirma a viabilidade da rota (vários fazem PC via M4L), mas um bridge próprio é pequeno o suficiente (~1 patcher JSON) para valer mais que adaptar caixa-preta alheia.

---

## O QUE A PESQUISA ENTREGOU

### Capacidades novas viáveis (antes inexistentes)
1. **Endosso oficial da rota**: Xfer confirma PC no Serum 2 via DAW (Live 12.2+; um 12.4.6 está após fixes de 12.2.5). A ponte M4L→Serum não é gambiarra: é a via oficial.
2. **Gerador de .amxd sem IDE**: formato completo documentado (`ampf` + tipo + `meta` + `ptch` com JSON do patcher; `mmmm`/1835887981 = MIDI effect), com código aberto funcional de referência para copiar (~100 linhas de Python) e instalação por cópia para a User Library + inserção via LOM (`Chain.insert_device`, Live 12.3+).
3. **Padrão FIRE via LOM comprovado**: parâmetro do device (numbox/button com parameter_enable) escrito pelo LOM → `live.observer` interno dispara a ação; evitando a outlet do live.button (só dispara em clique). Estado observável nos dois sentidos.
4. **Rota de fallback DOCUMENTADA pela Xfer**: `Serum2Prefs.json` (`~/Library/Preferences/`) com `"Enable CCForRockers": 1` (CC) ou `2` (NOTES) + `"CCForRocker Preset +"/"-"` → troca de preset por CC ou NOTE com histerese (≥64 dispara, <64 rearma — detalhe de implementação oficial). Permite andar ±1 preset em runtime; combinada ao presets.db dá para WALK até um alvo absoluto.
5. **Ferramenta de enumeração absoluta**: o `validator` do vst3sdk imprime program lists via IUnitInfo — nunca rodado contra o Serum 2 publicamente; se o Serum publicar a lista, ganha-se enumeração de presets direto do plugin, imune à versão.

### Lacunas que continuam abertas
- **NÃO VERIFICADO**: se `midiout` de M4L MIDI Effect entrega PC ao VST3 na MESMA track exatamente como o PC de clip entrega (nada na internet prova nem desprova para Serum 2; é o teste mínimo abaixo).
- **NÃO ENCONTRADO**: ProgramChanges.txt no Serum 2 (ausente do manual completo extraído via pdftotext — 0 ocorrências de "program change"/"bank select" em 354 páginas — e de changelogs; a rota absoluta bank/program do Serum 1 funciona no 2 mas é não-documentada).
- **NÃO ENCONTRADO**: scripting/API oficial do Serum 2; morph cross-preset nativo; device comunitário pronto que resolva o caso exato; evidência pública de IUnitInfo/program list no Serum 2.
- **Risco mantido**: a regra bank=pasta/program=índice é não-documentada e já mudou entre 2.0.16 e 2.1.5 (medido em runtime) — qualquer dependência dessa ordem precisa de recalibração por versão.

## PRÓXIMO TESTE MÍNIMO

**Objetivo**: provar a rota mais promissora inteira sem GUI e sem tocar no .als — o bridge M4L a montante do Serum.
1. **Gerar** o bridge .amxd em Python (container `ampf`+`mmmm`+`ptch`; patcher: `live.numbox Bank`, `live.numbox Program`, `live.numbox Fire 0/1`, `live.observer` no Fire → `midiformat` monta os bytes MIDI → `midiout`). Instalar copiando para `~/Music/Ableton/User Library/Presets/MIDI Effects/Max MIDI Effect/`.
2. **Inserir via LOM** (`Chain.insert_device`/browser) ANTES do Serum 2 numa track de teste.
3. **Disparar**: LOM seta Bank/Program e `Fire.value = 1.0`; o patcher manda `CC#0 = bank-1` (Bank Select Coarse) + `PC = program` pelo `midiout`.
4. **Verificar**: abrir a UI do Serum (ou ler o título do preset via observer do plugin, se houver) e conferir se o preset trocou.
   - Se trocar → rota completa validada: encadear ao presets.db para endereçamento absoluto e dispensar XML injection.
   - Se não trocar → repetir o mesmo disparo por clip (já se sabe que clip PC funciona) para isolar se a falha foi o emissor M4L ou o threshold/histerese; em paralelo, teste B de 5 minutos: `"Enable CCForRockers": 1` + `"CCForRocker Preset +": 21` no Serum2Prefs.json e mandar CC21 pelo bridge (rota documentada pela própria Xfer).
   - Teste C (enumerador): compilar o `validator` do vst3sdk e rodar contra `Serum2.vst3`; se imprimir "Programlist ... (N programs)", tem-se a lista absoluta de presets por plugin, sem depender de presets.db.

Fontes principais: [thread Xfer PC Serum 2](https://xferrecords.com/forums/general/please-consider-bringing-back-program-change-to-serum-2) · [Live 12 release notes](https://www.ableton.com/en/release-notes/live-12/) · [ableton-live-mcp](https://github.com/bschoepke/ableton-live-mcp) · [Serum 2 manual (PDF)](https://www.xferrecords.com/manual/serum-2/docs) · [thread Xfer "CC for serum"](https://xferrecords.com/forums/general/cc-for-serum) · [vst3_public_sdk validator](https://github.com/steinbergmedia/vst3_public_sdk) · [LOM docs](https://docs.cycling74.com/max8/vignettes/live_object_model)
