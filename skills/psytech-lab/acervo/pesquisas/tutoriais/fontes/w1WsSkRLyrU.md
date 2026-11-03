# How And Why To Mono Your Low End

**Canal:** Sonic Academy · **Apresentador:** Rory (Hyper Production) · **Vídeo:** https://www.youtube.com/watch?v=w1WsSkRLyrU · **Duração útil:** ~4:45
**Fonte:** legenda automática EN. Técnica de mixagem em pista/bus (Logic Pro + FabFilter Pro-Q 2); sem sound design.

## Técnicas-chave

- **Por que monoar** — praticamente todo sistema de clube soma o grave em mono: um low end estéreo sofre mismatch de fase no PA e pode cancelar (o baixo some).
- **Caminho 1: mono na fonte** — kick e baixo em mono na própria pista (no Logic, um clique; no Live, Utility Width 0% ou sample mono).
- **Caminho 2: low-cut só no Side** — EQ em modo mid/side processando apenas o canal Side com low-cut: remove-se só a informação estéreo abaixo do corte; o Mid (o conteúdo real) fica intocado. No exemplo dele o corte sobe até ~200 Hz; critério de segurança: se não soar diferente, está seguro.
- **Nunca cortar o Mid** — cortar o Mid removeria frequências de verdade; a operação correta é sempre no Side.
- **Topo livre** — acima do corte, as frequências podem ficar tão largas quanto se quiser; o mono é essencial só no low end.

## Notas de aplicação

- No Live: EQ Eight em M/S editando o S com low-cut ~120 Hz no bus (último insert antes do limitador) e/ou no bus de bateria; Utility Bass Mono ~120 Hz na fonte.
- Em projeto de low-end já mono, a técnica é garantia e auditoria, não conserto; o side-cut não corrige déficit de corpo e não soma nível ao Mid.
- Corte em 200 Hz estreitaria o corpo de madeiras (150–500 Hz) — em psytech, manter o corte em 120–150 Hz.
- Se o A/B baixar o volume, o material era majoritariamente side/fora de fase: checar fase, não compensar com ganho.
