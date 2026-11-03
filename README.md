# Psytech Lab

Plugin de producao **psytech, techno e minimal progressivo (multi-tempo)**: reguas destiladas com numero e fonte, casos medidos por sintoma e acervo de pesquisa por dominio, de grave e kick a mix, arranjo, sound design e referencias por artista.

**Pra quem:** uso pessoal do Bruno e dos agentes que trabalham com ele (ZCode, Claude Code, ChatGPT/claude.ai) na producao desse genero. Nao e pacote generico de tutorial; e o lab destilado de um projeto real.

```
plugins/psytech-lab/
├── .zcode-plugin/plugin.json        # manifesto ZCode
├── .claude-plugin/                  # manifesto + marketplace (formato Claude Code)
├── gpt/                             # consolidados + instructions para ChatGPT/claude.ai
│   ├── instructions.md
│   ├── perguntas-canonicas.md
│   └── MANIFEST.json                # versao, data, contagem e sha256 dos consolidados
├── skills/psytech-lab/SKILL.md      # o roteador (pergunta → arquivo certo)
├── skills/psytech-lab/INDEX.md      # inventario do conteudo (reguas, casos, acervo)
├── skills/psytech-lab/reguas/       # 6 reguas destiladas
├── skills/psytech-lab/casos/        # casos reais: sintoma → causa medida → correcao
└── skills/psytech-lab/acervo/       # fonte profunda, 7 pastas por dominio (351 arquivos)
```

## Instalacao

### ZCode
1. **Plugin Marketplace → Add → Add Plugin Marketplace** e aponte para a pasta `plugins/` deste repo (ela contem o catalogo `marketplace.json`, com a entrada `psytech-lab` em `source: ./psytech-lab`).
2. Instale **psytech-lab** a partir do catalogo adicionado.
- Alternativa: adicionar o mesmo repo publicado (a pasta `plugins/` e o marketplace).

### Claude Code
1. `/plugin marketplace add <caminho>`: aponte para a pasta `plugins/psytech-lab/` (e la que mora o `.claude-plugin/marketplace.json` deste layout) ou para o repo, se ele for publicado com essa pasta na raiz.
2. `/plugin install psytech-lab@psytech-lab`.

### ChatGPT / claude.ai
Nao ha plugin nativo; use a pasta `gpt/`:
- `gpt/perguntas-canonicas.md` e o consolidado: as 10 perguntas canonicas do genero e o arquivo do pacote que responde cada uma, com caminhos relativos a pasta da skill.
- Cole esse arquivo como **instructions** de um GPT customizado (ou no Custom Instructions): o modelo passa a rotear a pergunta para o arquivo certo e voce anexa/consulta os arquivos citados.
- Os demais `consolidado-*.md` da mesma pasta sao o conteudo completo por dominio, para anexar ao GPT quando quiser responder sem sair da conversa.

## Como atualizar

Este pacote e **artefato gerado, nao fonte editavel**. Quando o acervo ou as reguas mudarem, regenere pelo pipeline de destilacao que o produziu (acervo → reguas/casos/INDEX → consolidados `gpt/` → novo `MANIFEST.json` com data e sha256) e publique a pasta de novo. Nunca edite os arquivos do pacote na mao: toda edicao manual morre na proxima regeneracao e dessincroniza o `MANIFEST.json`.

## Nota de uso pessoal

O conteudo e destilado do acervo pessoal do Bruno, **e esse acervo cita material pago de terceiros** (cursos, masterclasses, packs), reproduzido aqui apenas para uso pessoal de estudo. Nao redistribua, nao publique e nao compartilhe este pacote ou qualquer arquivo dele.

Todo numero traz a fonte no bloco "Fontes" do cabecalho da regua, e item marcado **EM DISPUTA** nas reguas e conflito aberto que so o ouvido decide. Metrica e mapa, nao alvo: a regua orienta, a decisao final e auditiva. Regra das duas falhas (dos casos): se a mesma correcao falhar duas vezes, a premissa esta errada, nao a dose.
