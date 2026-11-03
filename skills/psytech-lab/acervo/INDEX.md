# Acervo do Psytech Lab — catálogo por domínio

v0.1.0 · 03/11/2026

Inventário das pastas de `acervo/` — a fonte profunda da skill. Para rotear por pergunta, use o `SKILL.md`; este arquivo é o catálogo: cada domínio com contagem de arquivos e o que cobre. Caminhos relativos a esta pasta (`acervo/`).

| Domínio | Arquivos | O que cobre |
|---|---|---|
| `PSYTECH-LAB/` | 8 | Núcleo documental do lab: índice, missão e hierarquia de evidências, frentes P0–P2, síntese sonora e receitas por função, protocolos de lab, corpus e matriz de perfis, operação offline, ingestão documental (comece por `00-INDICE-PSYTECH-LAB.md`) |
| `diagnosticos/` | 16 | Auditorias e medições do set: grupos de synths e efeitos, automação de cortes do kick, raio-x e dossiê de certificação do set de referência, régua de áudio, mapas de artistas × set de referência, rastreio de preset de Serum |
| `genre-dna/` | 1 | DNA do gênero psytech / dark progressive / zenonesque (`psytech-dark-prog.md`) |
| `knowledge-base/` | 39 | Aulas, masterclasses e manuais: PME Experts (bass bible), KUNI Sound, Serum 2, método de mix psytrance, anti-mascaramento, arranjo anti-estase, PME tensão/movimento e análises de faixas por artista (Gazolla, Kaled Nasser, Yao Ofosu, Akari, AIO…). As masterclasses de YouTube ficaram como resumo de 1 linha com ID do vídeo (transcrições removidas na higienização para publicação) |
| `pesquisas/` | 174 | Estudos e mapeamentos medidos — 23 diretos (estudos de faixa, mix, master, dossiê de dinâmica, mapeamentos de canais e packs) + as subpastas abaixo |
| `pesquisas/cursos/` | 10 | Dissecções de cursos e projetos de aula: Drift (152 presets de Serum), PML (Moog Sub 37, Diva), Omar Meho, Tim Engelhardt, Cercle, Giants, Mixing a Track |
| `pesquisas/tutoriais/` | 115 | Frentes de tutorial traduzidas para fluxo psytech — 11 nomeadas (arranjo-mix, groove, melodia, pressão grave, texturas, transições…; comece por `INDEX-TUTORIAIS.md`) + 81 mapas por vídeo (nome = ID do YouTube) + `fontes/` (22 transcrições) + `receitas-referencias/` (1 receita) |
| `pesquisas/refs-artistas/` | 16 | Análises comparativas e dissecações por artista de referência: Gazolla, Kaled Nasser, Star System, Artefakt/Undertow, audiometria física do psytech, remakes e estudos forenses |
| `pesquisas/dossies-notebooklm/` | 7 | Retornos NotebookLM/Gemini: set de referência estendido, IsmailM × set de referência, partitura e música, vozes, braam portador, dinâmica de FX, sound design completo |
| `pesquisas/dossies-deep-research/` | 3 | Retornos de deep research: Argon (balanço místico e voz 3D), balanço místico, orquestra |
| `receitas-referencias/` | 112 | Uma receita medida por faixa de referência (análise automática de áudio, sem escuta — comece por `INDEX.md`) |
| `raiz/` | 2 | Corpus dos casos e dos conflitos abertos: `CICATRIZES-20261030.md` (lições que custaram horas) e `MAPA-DE-LACUNAS-E-CONFLITOS-20261030.md` (pontos EM DISPUTA) |

Contagem medida em 03/11/2026 com `find <dominio>/ -type f -name '*.md'` — 351 arquivos, todos `.md`, batendo com `gpt/MANIFEST.json` (`"arquivos": 368`, data 2026-11-03). Subcontas de `pesquisas/`: 23 diretos + cursos 10 + tutoriais 92 (81 mapas + 11 nomeados) + `tutoriais/fontes/` 22 + `tutoriais/receitas-referencias/` 1 + refs-artistas 16 + dossies-notebooklm 7 + dossies-deep-research 3 = 174. O censo `SONIC-ACADEMY-E-CANAIS-MAPEAMENTO-20261027.md` saiu do pacote na higienização v0.1.0 (movido para fora, em `plugins/_removidos-psytech-lab-v0.1.0/`).
