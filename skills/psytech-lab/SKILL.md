---
name: psytech-lab
description: Roteador do Psytech Lab — abra para qualquer dúvida de produção psytech/minimal progressivo (grave e kick, mixagem e master, arranjo e transição, melodia e harmonia, texturas e sound design, referências por artista) ou quando algo "não sai" e o número briga com o ouvido. Números de BPM e key têm duas leituras — leia o contexto antes de calcular.
---

# Psytech Lab — roteador

v0.1.2 · 03/11/2026

**Presupõe Ableton Live:** as réguas citam devices por nome (Utility, Multiband Dynamics, Glue Compressor, Serum 2, Kickstart 2). Em outro DAW, aplique a função descrita, não o nome do device.

**Contexto do gênero (fontes do pacote):** low-end mono ≤ 120 Hz — o DNA do gênero manda sub "monofônico absoluto abaixo de 120 Hz" (`acervo/genre-dna/psytech-dark-prog.md` §2) e a régua de baixo valida 120 como conservador (`reguas/regua-baixo-kick.md` §4.6). **BPM tem duas leituras sem veredito:** o cânon de cálculo das réguas é 128 (semicolcheia = 117,19 ms; estudo de 17/10) e o DNA do gênero aponta faixa 130–134 como padrão do estilo (`acervo/genre-dna/psytech-dark-prog.md` §2). Ao calcular célula temporal, leia `reguas/regua-baixo-kick.md` §8.2 antes de escolher o número.

**Contexto do projeto do autor (referência, não regra):** o set do autor roda a 130 BPM (16º ≈ 115,4 ms) e a key dele é C# frígio (`acervo/diagnosticos/DOSSIE-HOMOLOGADO-CERTIFICACAO-CANONICA-SET-REF.md` — dossiê do set de referência; os "Casos" da régua de baixo tratam C# como key do set, §9.2–9.3). O DNA do gênero no pacote não fixa tônica nem modo — **C# frígio não é lei do gênero**. O princípio que governa está na régua: afine o kick em grau consonante da key do SEU projeto e o bass contra o pitch real do kick (`reguas/regua-baixo-kick.md` §2.1, §4.2).

**Como usar:** leia a pergunta, abra o arquivo certo nas tabelas abaixo (caminhos relativos a esta pasta) e responda com o que ele traz. Réguas = resposta destilada, com número e fonte (arquivo + data) em cada item; item marcado **EM DISPUTA** na régua é conflito aberto do mapa — a régua registra as leituras, não decide; decidir é do ouvido. Acervo = fonte profunda, citada no cabeçalho "Fontes" da própria régua.

**Força da evidência:** as classes **C = consenso técnico · R = medido em referências externas · E = faixa de engenharia recomendada** valem só para `acervo/pesquisas/ESTUDO-BATERIA-E-BAIXO-20261017.md` (17/10), onde a legenda C/R/E está definida. **Não confunda com a hierarquia A–E de evidência do lab** (`acervo/PSYTECH-LAB/01-MISSAO-E-HIERARQUIA-EVIDENCIAS.md`: A física/experimentos · B documentação oficial · C práticas documentadas · D medições do corpus · E hipóteses/estética) — são duas escalas independentes, e as letras C e E significam coisas diferentes em cada uma; leia o rótulo no documento que o usa. Item de fonte sem classe (ex.: compilação de aula, PME s.d.) é receita de instrutor, não medição — mesmo lendo a régua sozinha, sem este roteador. O acervo é texto bruto de aulas e estudos — pode entregar estimativa de stem como "revelada" e opinião de aula como técnica; a disciplina de rótulo (EM DISPUTA, ESTIMATIVA, classe) mora na régua, não lá.

**"Casos" tem dois usos — não confunda:** a pasta `casos/` deste roteador é porta de entrada por sintoma de sessão (elemento some, número briga com o ouvido); a seção "Casos" dentro de cada régua é contraste numérico com o set do autor — referência, não regra, e os números de lá não valem para o seu set.

## reguas/ — resposta destilada (6 arquivos)

| Arquivo | Responde |
|---|---|
| `reguas/regua-baixo-kick.md` | Sub, kick, sidechain, jogo de ausência do kick, anti-mascaramento, afinagem por nota |
| `reguas/regua-mixagem-e-master.md` | Headroom, dinâmica, low-end mono, medição e unidades |
| `reguas/regua-arranjo-e-transicao.md` | Macro-forma, tensão e movimento, transições, vácuo, riser como conteúdo |
| `reguas/regua-melodia-e-harmonia.md` | Modos, frases, motivos, tensão harmônica, densidade sóbria |
| `reguas/regua-texturas-e-sounddesign.md` | Serum, madeira orgânica, atmosferas, FX |
| `reguas/regua-referencias-artistas.md` | O que cada artista de referência faz, com números |

## casos/ — porta de entrada por sintoma (1 arquivo)

| Arquivo | Responde |
|---|---|
| `casos/cicatrizes-como-caso.md` | Elemento some ou "não sai", timbre muda sozinho, número briga com o ouvido, groove afobado ou fora — check de 60 s, depois sintoma → causa medida → correção |

## acervo/ — fonte profunda, pastas por domínio (7 pastas)

Catálogo completo com contagem por pasta (352 arquivos medidos em 03/11/2026): `acervo/INDEX.md`.

| Pasta | O que tem |
|---|---|
| `acervo/PSYTECH-LAB/` | Núcleo do lab: missão, frentes, síntese sonora, protocolos (comece por `00-INDICE-PSYTECH-LAB.md`) |
| `acervo/diagnosticos/` | Auditorias e medições do set |
| `acervo/genre-dna/` | DNA do gênero (`psytech-dark-prog.md`) |
| `acervo/knowledge-base/` | Aulas e manuais — Serum, bass bible, método de mix |
| `acervo/pesquisas/` | Estudos e mapeamentos — cursos, dossiês, refs-artistas, tutoriais |
| `acervo/receitas-referencias/` | Uma receita por faixa de referência |
| `acervo/raiz/` | `CICATRIZES-20261030.md` (corpus dos casos) e `MAPA-DE-LACUNAS-E-CONFLITOS-20261030.md` (conflitos abertos) |

## Limitações conhecidas do pacote

- `acervo/raiz/MAPA-DE-LACUNAS-E-CONFLITOS-20261030.md` acompanha só as seções 1–3 (cobertura P0–P2, lacunas restantes, regras de medição). Os **números de conflito** que as réguas citam (ex.: conflitos 3/4/5/7 nos itens EM DISPUTA de `reguas/regua-baixo-kick.md` §8) e o **§6 do mapa** citado no rodapé dessa régua **não têm corpo no pacote** — a nota final do arquivo diz que as seções de estado ficaram no repositório de origem. Trate a citação como ponteiro para o arquivo completo, que não veio; as duas leituras de cada ponto EM DISPUTA continuam registradas na própria régua.
- Os protocolos **EXP-…/SYN-…** citados pelas réguas moram em `acervo/PSYTECH-LAB/05-LAB-EXP-SYN-PROTOCOLOS.md` (EXP-01…10 + SYN-01…10 — protocolo reproduzível, sem execução).
