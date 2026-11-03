# Menu de testes de escuta — método e design system (12/09/2026)

> Estudo do acervo psytech-lab, anonimizado. O original é um menu de A/B para escuta no set (números de
> canal, comandos de script e estado de mutes) — essa parte é estado puro e foi removida. Fica o **método do
> menu de teste** e o **design system da conversa**, que são transferíveis.

## 1. O método do menu (replicável)

- Cada teste nasce **mutado por padrão**; ouve-se UM por vez (desmute → ouvir → voltar ao estado).
- Cada teste registra: **sensação** (o que promete), **pergunta que responde**, **como ouvir** e **como voltar**.
- Loop de trabalho fixo (o mesmo trecho sempre) para comparar testes entre si.
- **Teste conjunto declarado:** combinar dois testes que competem no mesmo papel para ouvir a hipótese em
  pares ("topo corre veloz + órbita" → hipótese "acelero Akari + elasticidade Greenwolve").
- **Alternador** para famílias com múltiplas versões (ex.: kicks): um candidato por vez, com pergunta final
  registrada ("versão sem transposição vs transposta +0,65 st").

## 2. As perguntas do menu (o caso)

| Teste — sensação | Pergunta que responde |
|---|---|
| **Micro-hats 16th sintopado** — velocidade no topo | O 16th sintopado deixa a faixa mais rápida sem virar metralhadora? |
| **Ear ticklers 3D órbita** — movimento ao redor da cabeça | Os micro-ticks ×.772 orbitando dão profundidade sem Auto Pan em tudo? |
| **Wood click resposta** — conversa | O wood respondendo nos gaps cria diálogo ou fica espalhado? |
| **Perc orgânica sincopada** — corpo no centro | A perc sincopada dá malandragem sem encher o groove? |
| **Shaker swing malandro** — atraso sensual | O shaker com +0.02 beat traz o swing do tech house antigo ou fica datado? |
| **Personagem B resposta (duelo −1 oit)** — diálogo bass/lead | O duelo −1 oitava funciona em toda a música? (B responde TODAS as frases do A) |
| **Personagem C tema (enters nos cortes)** — o inesperado | O tema malandro entrando nos cortes de kick (espera o kick e não vem) vira surpresa boa? |

## 3. Design system da conversa (A pergunta → B responde → C entra)

- **A pergunta** (personagem principal) → **B responde** grave no vácuo, espelhado −1 oitava
  (61→49, 62→50, 56→44, 68→56), shift +2.0/1.5/2.5 sem colisão, velocity −10~14, fecho na quinta (44).
- **Kick corta** → **C entra inesperado** rasgando em 3D (células malandras nos cortes reais do kick;
  vocabulário 68→62→56→50 com mordida no bII frígio + ghosts vel 52).
- **Auto Pan-Tremolo em Panning** (Sine, 68%, synced 1 bar, Phase 180°) = o rasgo 3D de um lado pro outro
  (linguagem Greenwolve/Ear Ticklers).
- Anti-colisão: resposta nunca toca junto com o A; célula nunca sobrepõe A, B ou outra C — a varredura pula
  posições ocupadas.

**Papéis por artista de referência:** Akari = chão quase reto; Gazolla = corte seco e PUSH;
Desert Nomads/Tiger Eyes = retorno deslizante; Greenwolve = malandragem lateral; Rolling = PULL sensual.

## 4. A decisão de profundidade (pergunta de curadoria)

| Opção | O que é |
|---|---|
| **Profundidade cruda** | famílias ×5 somadas (cama/drone/chant/glitch/swells/reverse) — o que estava no ar |
| **Profundidade organizada** | 1 versão por família (mantém uma, muta as outras 4) |

O objetivo do teste: decidir se a soma quíntupla é **assinatura** ou **vazamento**. (No caso original a
decisão ficou em aberto — é decisão de escuta.)

## 5. Limitações registradas

- Os canais de teste tinham devices herdados de outro material (delay ping-pong) — parte do caráter vem da
  herança; isolar o caráter novo exige limpar a cadeia herdada.
- Duas camadas de kick estavam dobradas em uma seção da intro e foram reduzidas a uma (estado registrado para
  não "consertar" duas vezes).
- Estado de sessão não salvo no momento dos testes — o estado de mutes era volátil (lição: registrar o estado
  antes de ouvir).
