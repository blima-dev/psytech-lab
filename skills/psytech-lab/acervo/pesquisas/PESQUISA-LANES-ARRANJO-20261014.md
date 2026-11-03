# PESQUISA — Automação de Arranjo (lanes de Volume) no Live 12.4.6 (14/10/2026)

Pergunta central: existe algum caminho além do patch offline do `.als` para ler/escrever lanes
de automação de ARRANJO (track lanes, ex. Volume de uma pista)? Resposta: **NÃO** — triplamente
provado. O patch offline é o único caminho de escrita; a API nem lê.

## 1. Conclusões (os 3 pontos abertos, fechados)

### (a) A citação "Live's API only allows you to fetch one data point at a time"
- Fonte exata do post do fórum: **NÃO ENCONTRADA** (maxforlive.com 403; structure-void timeout;
  buscadores com bot-check; web reader instável em URLs longas). A citação fornecida permanece
  sem fonte primária localizada.
- Validade técnica: **confirmada por evidência melhor** — ver (b) e a prova empírica §2.2.
  Não há leitura em lote na API; e para lanes de arranjo não há leitura nenhuma.

### (b) Max for Live / LiveAPI consegue acessar envelopes de Track?
- **NÃO.** Doc oficial Max 8 — LOM (Live 12.1, docs.cycling74.com/max8/vignettes/live_object_model,
  lido por inteiro em 14/10): a classe `Track` tem **zero** membros de automação. Children:
  clip_slots, arrangement_clips, devices, group_track, mixer_device, view. O único eco fora do Clip:
  `DeviceParameter.automation_state` (sinalizador de estado, não valores) e `Song.re_enable_automation`
  / `session_automation_record` (brazão de gravação, não dados).
- Corroborado no ecossistema: `ableton-js` (leolabs) vai por bridge Max for Live (`live.api`) e o
  namespace `Envelope` é clip-level (`clip.automation_envelope`) — verificado no fonte `src/ns/clip.ts`.
- Doc oficial Python LOM (Cycling '74, lida na mesma sessão): envelope só em `Clip`.

### (c) Bibliotecas externas que escrevam FloatEvent/automação no .als?
- **NENHUMA encontrada.** Todo o ecossistema de parsers .als (ableton-parser, als-parser, pyableton,
  live-daw-tools etc., varredura de 14/10) trata metadados/samples/devices — nenhuma escreve lane de
  automação. Os 5 repositórios de API Live inspecionados são clip-only ou zero automação.
- **Consequência:** uma ferramenta de patch offline que escreve FloatEvents com disciplina de escrita
  (patch por string, nunca ElementTree/lxml; auditoria automática do arquivo salvo; eixo cru =
  ganho linear — prova 5/5; Time em beats; sentinelas Time=−63072000 (início) e ~960 (fim)) é
  prior art praticamente único. A verificação externa das armadilhas de patch não existe; a garantia
  do método é interna: string patching + auditoria + read-back no arquivo salvo.

## 2. Provas desta rodada (provas = comando → saída crua)

### 2.1 Doc oficial Max 8 LOM (Live 12.1)
- Alvo: docs.cycling74.com/max8/vignettes/live_object_model · Comando: web reader (fetch completo)
- Saída: `Track` sem nenhum membro automation/envelope · `Song`: apenas re_enable_automation,
  session_automation_record, last_event_time (escalar read-only) · Clip: has_envelopes, clear_envelope,
  clear_all_envelopes + Clip.View (select/show/hide_envelope_parameter).

### 2.2 A API do Live NEM VÊ as lanes de arranjo (prova nova, dentro do Live 12.4.6)
- Alvo: uma pista do set de referência com lane de Volume de valor constante salvo no `.als`
  (lane FloatEvent já existente no arquivo).
- Comando: código via LOM executado dentro do Live — varreu TODOS os arrangement_clips:
  `c.automation_envelope(t.mixer_device.volume)` → **None em 100% dos clipes**
- Wrapper canônico de leitura (clipe de arranjo, param Track Volume) →
  `has_envelope: false, event_count: 0`
- Consequência dupla: (1) impossível ler via API para validar; (2) impossível escrever via API —
  a lane pertence à track e não é exposta. Nem o híbrido "ler via LOM + escrever no .als" existe.

## 3. Impacto no fluxo de escrita de lane

1. Escrita de lane = `.als` offline com um writer dedicado a FloatEvents; escritor único
   (Live fechado/sem save simultâneo), out_path novo ao lado do fonte, hash esperado do arquivo
   fonte, auditoria do resultado. Sem caminho alternativo — decidido por evidência, não por preferência.
2. Validação de leitura não pode vir da API: vem de (i) reler os FloatEvents no arquivo NOVO
   salvo e (ii) audição em A/B no mesmo render.
3. O Live aberto não enxerga o arquivo novo: depois do patch, abrir o `.als` novo no Live é passo
   do fluxo (ou salvar o Set pelo Live antes do patch para realinhar os hashes).

## 4. Lacunas remanescentes (marcadas, não bloqueiam)
- Fonte exata do post citado: NÃO ENCONTRADA (sites bloqueados). Sem valor prático — a
  prova empírica §2.2 é mais forte que qualquer fórum.
- Comportamento do Live ao carregar um `.als` patchado com lane rampada nova (aceitação de eventos
  não lineares num lane FloatEvent já existente): interno OK (receita de 26/09 + 51 testes), externo
  N/D. Coberto pelo protocolo: patch → auditoria → abrir no Live → A/B.
