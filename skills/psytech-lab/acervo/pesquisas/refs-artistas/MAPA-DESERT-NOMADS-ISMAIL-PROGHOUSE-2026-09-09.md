# MAPA — Desert Nomads × Gazolla × ISMAIL.M (prog house) — 2026-09-09

Missão: mapear o estilo prog house da escola ISMAIL.M × Desert Nomads como base para uma faixa nova no estilo. Mapeamento cego por régua DSP própria (sem priming — lição do blind cross-check). **Nada de áudio tocado** (sistema mutado, leitura de bytes).

## 1. VERIFICADO: Desert Nomads = projeto do Gazolla

Três faixas **idênticas byte-a-byte** sob os dois nomes (mesmo BPM, tonalidade, duração e perfil de energia):

| Faixa | Assinatura idêntica |
|---|---|
| Quartzo | 121,6 BPM · C maj (r0,77) · 414 s |
| Sand Runners | 122,4 BPM · C# min (r0,47) · 440 s |
| Tiger Eyes | 118,8 BPM · E min (r0,43) · 430 s |

+ crédito compartilhado: "Desert Nomads, Andre Gazolla, Braygptian — In My Mind". É o mesmo coletivo/projeto. Catálogo prog house/: Quartzo · Sand Runners · Tiger Eyes · Desert Guardians · Wolves and Ravens · Journey of the Soul · Lost Dinasty · In My Mind + remixes (Rikfell In My Head DN Rmx, Gutenn Beirut Gazolla/Bragyptian/DN Rmx).

## 2. DNA medido (18 faixas, janela de pleno de 60 s cada)

| Métrica | Valor | Nota |
|---|---|---|
| **BPM** | **118,8–125,3 · modo 121,6–122,4** | 15/18 entre 118–125 |
| **Kick (40–120 Hz)** | **2,0–2,4 onsets/s** | 4/4 confirmado |
| **Baixo (120–300 Hz)** | **2,1–2,4 onsets/s** | **IGUAL ao kick — NÃO é rolling 16ths (8/s)** |
| **Synth (300–1,2k)** | **2,3–2,5 onsets/s** | também ~2/s: as 3 vozes conversam |
| **Centroide synth** | 1,4–2,5 kHz (mediana ~2,1 k) | brilhante, atmosférico |
| **Pausas estruturais** | 1–3 por track | breaks/breakdowns |
| **Duração** | 5:32–7:25 | long-form |
| **Tonalidade** | C maj ×6 · E min ×3 · F maj ×2 · C# min · F min · C min · D min · C# maj | **maior presente em 1/3 do catálogo** |

**O achado central (o que separa esse estilo do psy rolling):** kick, baixo e synth rodam na MESMA densidade ~2–2,5 eventos/s. É um groove intercalado "falado" — cada voz emite ~2 golpes/bar e o movimento nasce da CONVERSA entre elas, não da densidade. Um rolling de 16ths roda a ~8 eventos/s por voz; aqui é 3× mais ar.

## 2b. CORREÇÃO DE MÉTRICA + triangulação de gênero (rodada 2, mesma noite)

A métrica de densidade da seção 2 (p97) **satura ~2,5/s para todo gênero** — não serve de discriminador. O discriminador válido é a distribuição de intervalos entre onsets (IOI, p90) na banda do baixo:

| Grupo | Faixa | Baixo: onts/s | IOI mediano | % IOI<160 ms |
|---|---|---|---|---|
| DN/Gazolla | Quartzo | 5,2 | **232 ms** | **44%** |
| DN/Gazolla | Tiger Eyes | 5,5 | 139 ms | 57% |
| ISMAIL.M | Hypnosis | 5,6 | 128 ms | 59% |
| PROG house BR | Rass — Arabic Spirit | 5,0 | 209 ms | 50% |
| Melodic Techno | Anyma — The Sign | 6,2 | 128 ms | 77% |
| Tech House | Sorry (Hype Rmx) | 5,3 | 128 ms | 63% |

**Veredito de gênero (com régua):** o catálogo DN/Gazolla fica na **zona-ponte entre prog house BR e psy** — baixo mais intercalado que psy rolling (âncora do psy: ~116 ms / 77% curtos = 16ths contínuos), com variação interna (Quartzo bem intercalado 232 ms; Tiger Eyes/Hypnosis já piscam 16ths). BPM 118–125 + breaks + long-form = prog house BR pela cena; Beatport chamaria de Melodic House & Techno. **O rótulo "prog house" é defendível e é o nome da cena; não é psytrance rolling nem prog clássico europeu.**

Blueprint ajustado: o baixo de uma faixa no estilo = **intercalado com rajadas ocasionais de 16ths** (entre o Quartzo e o Tiger Eyes), não 16ths parede nem só 2 golpes/bar.

## 3. Blueprint sintetizado do estilo (para uma faixa nova no estilo)

- **BPM 122** (modo do catálogo)
- **Tonalidade**: o catálogo vive em C maj; manter um centro menor com cor maior (a relativa maior no refrão/melodia) pega a cor do estilo sem abandonar o centro escuro
- **Groove**: kick 4/4 · baixo intercalado com rajadas ocasionais de 16ths (entre Quartzo e Tiger Eyes; preencher o vale, nunca parede) · synth/atmosfera 2–3 eventos/bar com centroide ~2 kHz
- **Estrutura**: 2–3 breaks (pausas de ~8–16 bars), duração-alvo 6:00–7:00
- **Melodia**: frase oriental/atmosférica como personagem (escola ISMAIL.M), sustentada e filtrada — não ostinato
- **Camadas**: kick suave, bass intercalado, pluck/arp atmosférico, pad, perc orgânica leve

## 4. Fontes e método

- Régua: ffmpeg 22.05k mono + numpy (autocorrelação onset c/ fold de tempo; chroma+Krumhansl; onsets por banda p97; energia 4 s)
- Blind cross-check do atlas (sessão irmã): rótulos "rolling psy" eram artefato de prompt; fenômeno hipnótico sobreviveu cego → este mapa usa só descritores medidos
- ISMAIL.M mapeado: Visionary (Cerato Rmx) 121,6 D min · Cyber Attack 121,6 C maj · Sunrise in Odessa 121,6 F maj · Hypnosis 121,6 C# maj · Sacred Lotus 125,3 C maj · Udja 118,8 C maj. Turkish Miracles (álbum): não analisado.
