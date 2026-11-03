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
