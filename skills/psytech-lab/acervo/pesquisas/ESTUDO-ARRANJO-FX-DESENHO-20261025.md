# ESTUDO — Arranjo · FX · Desenho das referências (25/10/2026)

> Dissecção nota a nota, fronteira a fronteira, de 10 faixas de referência do gênero + a faixa do projeto.
> Ferramenta: script de dissecação de arranjo/FX (validado em 3 âncoras do Slippery: quebra ~180 s ✓,
> pêndulo B↔F# ✓, simultâneo com drums 39%≈41% ✓). Dados brutos: JSONs por faixa; tabelas consolidadas.
> Regra de medição respeitada: topo (8–16 kHz) e estéreo medidos na taxa nativa 44,1 kHz;
> pyin a 22.050 só para f0 ≤ 3,5 kHz (declarado).

## As 10 faixas

Faixa do projeto (render 452 s) · Akari-Slippery · Antonio-Esfera ·
Artemis-DarkVoices · Gazolla-AuraNova · HNGT-FabricOfReality · Kaled-Muub ·
Miles-CallToTheWild · Yao-Limbo · Yao-Demons.

## 1. Arranjo — duas escolas de escala de tempo

| métrica | família (min–max) | mediana | projeto |
|---|---|---|---|
| estado mediano de camadas | 2–8 comp | 3–4 | 5 comp |
| turnover de estados/min | 2,8–6,7 | ~5 | **3,06 (abaixo)** |
| fronteiras multi-stem | 29–75 | ~58 | 53 |
| fronteiras com FX | 26–53% | ~35% | 49% |

- **Escola nervosa**: Slippery, HNGT, Miles, Limbo (estado 3 comp, turnover 5–6/min).
- **Escola calma**: Aura Nova (8 comp), Esfera/Artemis (4–5).
- O projeto está entre as escolas — o problema não é a escala, é o QUE acontece nas fronteiras (§2) e o QUE o lead faz (§3).

## 2. FX — o silêncio é o vício do caso; a família transforma em vez de cortar

| FX/min | família (min–max) | projeto |
|---|---|---|
| gap_silencio | 0,11–0,80 | **1,33 (3–12× o máximo deles)** |
| downlifter | 0,15–1,12 | 0,93 (2º maior) |
| reverb_wash | 0,42–2,0 | 1,2 (2º) |
| riser | 0–1,38 | 0,53 (normal) |
| sweep | 0–1,6 | 0,93 (normal) |
| impact / roll_build | 0–0,3 | 0,27/0,13 (raro em todos) |

- Riser e downlifter funcionam **em pares** nas refs (sobe antes da fronteira, desce depois).
- **Gap de silêncio**: 1–3 por faixa, quase sempre no último terço — arma de drop.
  O caso usa 1,33/min do começo ao fim = o corte total perdeu o valor dramático.
- Miles é o mais carregado (43 eventos/min); HNGT o mais denso em riser+gap (1,33/0,80 — coerente com a masterclass deles).
- Macro-arco: o último terço é o depósito de FX em quase todas (Aura Nova 25 fronteiras no T3; Slippery põe gap e roll SÓ lá).

## 3. Desenho e conversa — o coração do estudo

| métrica do lead | família (mediana) | projeto |
|---|---|---|
| simultâneo com drums | ~50% (até 68) | **28%** |
| no buraco (sem kick/bass) | ~16% (até 70) | **44%** |
| resposta atrasada 80–400 ms | ~5% | 7,6% (ok) |
| duração média da nota | 0,085–0,92 s (mediana ~0,22) | **0,59 s (o mais longo)** |
| % na tônica | ~65–95 (ou 100% na quinta) | 38% (vagueia) |
| % b2 no lead | 0–5 (só Esfera 36) | 22,9 |

- **Conversa = sobreposição**: o lead dos caras fala JUNTO com a bateria (HNGT 68%, Aura Nova 63%, Limbo 59%). "Resposta" atrasada é minoria em TODAS — conversa não é esperar o outro calar, é falar por cima no ritmo.
- **O lead é econômico**: mora na tônica (HNGT 94%, Yao Demons 95%) OU na quinta (Slippery 100% F#, pêndulo B↔F#). A cor frígia (b2/b7) vem do GRAVE, não do lead.
- **Staccato**: notas de 0,1–0,3 s. O caso 0,59 s = "trilha sonora" (diagnóstico de ouvido confirmado por medição).

## 4. Crescimento — eles estreitam, o caso abre

- Intervalos distintos no quartil final: HNGT 7→3 · Miles 9→6 · Limbo 6→4 (**simplificam o vocabulário no fim**); o caso 7→**20**.
- Registro no fim: família desce ou segura (Limbo 71→59, Esfera 58→49, Miles 61→54); o caso **sobe** 61→68.
- Densidade: família mantém após o drop; o caso 12→32 no Q2 e segura.

## 5. Tradução prática (receita da família)

1. **Silêncio total**: guardar para 1–3 momentos (quebra ~180 s estilo Slippery e pré-drop 2). Nas outras fronteiras, usar sweep/wash/riser (transformação), não desligamento.
2. **Lead**: staccato ~0,2 s, ancorado na tônica (C# no caso de referência), a quinta como pêndulo (F#); b2 é do GRAVE.
3. **Conversa**: nota do lead em cima do kick/percussão (simultâneo ≥50%), no buraco como tempero (~15%, tipo Aura Nova).
4. **Final da faixa**: reduzir intervalos distintos, segurar/descer registro — fechar o vocabulário.

## 6. Recursos de ensino (mapeados na mesma sessão)

- **Zenon Records Music Production Suite** (300 EUR, 20 h, 12 artistas do selo): módulos ARRANGEMENT (Amortalist: build-ups & drops), STABS+HOOKS (Krumelur: transição pro break + riser rítmico), Drum Arrangement (Mirror Me: diálogo percussivo), Call/Response 45 min (Grub).
- **Vision Serpent** (canal YT + Patreon ~US$6,50/mês): série "How to make psytech [Project Walkthrough]" por produtores do roster (Verschallt, Wachter & Böhm, SLUG, MVND).

## 7. Limites e pendências declaradas

- `NÃO VERIFICADO`: escuta — as métricas são régua técnica; a soberania é do ouvido.
- Notas do lead via pyin = subamostra do melódico tonal dominante (serve para campo/registro/conversa; densidade absoluta vem dos onsets).
- **Acervo amplo (266 do Psy4 + Tech Psy SC) NÃO rodou nesta rodada** (falhas de infra na sessão: bug de path, segfault do beat_track em py3.13 → fallback autocorrelação, pyin lento em GPU e quedas de VM). Playbook pronto para sessão nova.
- BPM por fallback de autocorrelação tem desvio ~1,2% vs beat_track (127,7 vs 129,2 no Slippery).
