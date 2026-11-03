# Psytech Lab

v0.1.2 · 03/11/2026

Plugin de produção **psytech / minimal progressivo a 128 BPM**: réguas destiladas com número e fonte, casos medidos por sintoma e acervo de pesquisa por domínio — grave e kick, mix, arranjo, sound design e referências por artista.

**Pra quem:** uso pessoal do Bruno e dos agentes que trabalham com ele (ZCode, Claude Code, ChatGPT/claude.ai) na produção desse gênero. Não é pacote genérico de tutorial — é o lab destilado de um projeto real.

```
plugins/psytech-lab/
├── .zcode-plugin/plugin.json        # manifesto ZCode
├── .claude-plugin/                  # manifesto + marketplace (formato Claude Code)
├── gpt/                             # consolidados + instructions para ChatGPT/claude.ai
│   ├── instructions.md
│   ├── perguntas-canonicas.md
│   └── MANIFEST.json                # versão, data, contagem e sha256 dos consolidados
├── skills/psytech-lab/SKILL.md      # o roteador (pergunta → arquivo certo)
├── skills/psytech-lab/INDEX.md      # inventário do conteúdo (réguas, casos, acervo)
├── skills/psytech-lab/reguas/       # 6 réguas destiladas
├── skills/psytech-lab/casos/        # casos reais: sintoma → causa medida → correção
└── skills/psytech-lab/acervo/       # fonte profunda, 7 pastas por domínio (352 arquivos)
```

## Instalação

### ZCode
1. **Plugin Marketplace → Add → Add Plugin Marketplace** e aponte para a pasta `plugins/` deste repo (ela contém o catálogo `marketplace.json`, com a entrada `psytech-lab` em `source: ./psytech-lab`).
2. Instale **psytech-lab** a partir do catálogo adicionado.
- Alternativa: adicionar o mesmo repo publicado (a pasta `plugins/` é o marketplace).

### Claude Code
1. `/plugin marketplace add <caminho>` — aponte para a pasta `plugins/psytech-lab/` (é lá que mora o `.claude-plugin/marketplace.json` deste layout) ou para o repo, se ele for publicado com essa pasta na raiz.
2. `/plugin install psytech-lab@psytech-lab`.

### ChatGPT / claude.ai
Não há plugin nativo — use a pasta `gpt/`:
- `gpt/perguntas-canonicas.md` é o consolidado: as 10 perguntas canônicas do gênero e o arquivo do pacote que responde cada uma, com caminhos relativos à pasta da skill.
- Cole esse arquivo como **instructions** de um GPT customizado (ou no Custom Instructions): o modelo passa a rotear a pergunta para o arquivo certo e você anexa/consulta os arquivos citados.
- Os demais `consolidado-*.md` da mesma pasta são o conteúdo completo por domínio, para anexar ao GPT quando quiser responder sem sair da conversa.

## Como atualizar

Este pacote é **artefato gerado, não fonte editável**. Quando o acervo ou as réguas mudarem, regenere pelo pipeline de destilação que o produziu (acervo → réguas/casos/INDEX → consolidados `gpt/` → novo `MANIFEST.json` com data e sha256) e publique a pasta de novo. Nunca edite os arquivos do pacote na mão: toda edição manual morre na próxima regeneração e dessincroniza o `MANIFEST.json`.

## Nota de uso pessoal

O conteúdo é destilado do acervo pessoal do Bruno — **e esse acervo cita material pago de terceiros** (cursos, masterclasses, packs), reproduzido aqui apenas para uso pessoal de estudo. Não redistribua, não publique e não compartilhe este pacote ou qualquer arquivo dele.

Todo número cita arquivo + data, e item marcado **EM DISPUTA** nas réguas é conflito aberto que só o ouvido decide. Métrica é mapa, não alvo: a régua orienta, a decisão final é auditiva. Regra das duas falhas (dos casos): se a mesma correção falhar duas vezes, a premissa está errada — não a dose.
