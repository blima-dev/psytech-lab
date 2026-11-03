# RÉGUA — Baixo e Kick

v0.1.1 · 03/11/2026

**Sub · Kick · Sidechain · Jogo de ausência do kick · Anti-mascaramento kick × baixo**

> Destilada do acervo psytech-lab contra o mapa de conflitos de 30/10. Contexto de sessão do autor fica confinado a "Casos" (§9) e ao EM DISPUTA que cita o set (§8.3) — nas regras numeradas não há estado do set do autor.
> Todo número cita (arquivo, data); sem fonte, não entra.
> **Fontes citadas:** `acervo/pesquisas/ESTUDO-BATERIA-E-BAIXO-20261017.md` (17/10) ·
> `acervo/diagnosticos/REGUA-DE-AUDIO-20261025.md` (25/10) · `acervo/knowledge-base/PME_EXPERTS_PSYTECH_BASS_BIBLE.md`
> (compilação PME Experts/Freak Audio — sem data no corpo do arquivo, citada como s.d.) ·
> `acervo/knowledge-base/anti-mascaramento-kick-bass.md` (08/09) · `acervo/knowledge-base/gazolla-analise-faixas.md` (08/09) ·
> `acervo/knowledge-base/andre-gazolla.md` (08/09) · `MAPA-DE-LACUNAS-E-CONFLITOS-20261030.md` (30/10, só para os pontos EM DISPUTA).
> Classes do estudo de 17/10: C = consenso técnico · R = medido em referências externas · E = faixa de engenharia recomendada.
> Fontes sem classe (PME s.d., compilações de aula) são receita de instrutor, não medição.

## 1. Fundamento e balança dos graves

- **1.1.** Equilibre o peso entre as camadas do grave: `(sub 25–40 Hz) − (kick 40–55 Hz)` fica bem entre `−3 e +0,5 dB`; o corpus medido (Kaled/Gazolla/ISMAIL/Slippery) vai de `−6,77 a +0,34 dB` — abaixo de ~−7 dB o bloco fica magro, acima de ~+1 dB exige validação de headroom. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10 — R corpus)
- **1.2.** Mantenha um só "andar" dominante: `(55–75) − (40–55)` ≤ `+1,5 dB`; o corpus mede `−1,2…+1,4 dB` e dá alerta forte acima de `+2 dB`. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10 — R corpus)
- **1.3.** Deixe o kick 2–3 dB acima do bassline no fader; o método objetivo é igualar os dois por LUFS no solo e ajustar de lá. (anti-mascaramento-kick-bass.md, 08/09 — Sokolovskiy/UJAM)
- **1.4.** Régua de banda da família (mediana de 15 referências masterizadas; min–max): sub 47,5% (13,5–59,0) · bass 37,1% (22,8–52,7) · side/mid do grave −32,7 dB (−48,6 a −12,9). (REGUA-DE-AUDIO-20261025.md, 25/10)
- **1.5.** Kick psytrance: fundamental 50–70 Hz e click 2–5 kHz; fundamentos de bass/kick moram tipicamente em 40–80 Hz. (anti-mascaramento-kick-bass.md, 08/09 — Myloops; ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10 — iZotope, C geral)

## 2. Kick — afinação, cauda, ataque, timing

- **2.1.** Afine o kick em grau consonante da tonalidade — não necessariamente na tônica: a família de 53 kicks (pack Drift) mede fundamental mediana 49,1 Hz (25,6–68,0), com classes G1 (15) · G#1 (11) · A1 (6) · F#1 (5) · E1 (5). (REGUA-DE-AUDIO-20261025.md, 25/10 — §7.1)
- **2.2.** Cauda de referência do pack: decay −20 dB mediano 0,19 s (0,08–0,39); duração do arquivo mediana 0,48 s. (REGUA-DE-AUDIO-20261025.md, 25/10 — §7.1)
- **2.3.** Meça a fundamental por FFT e trate o nome do sample/rack como suspeito — o ajuste "pelo nome" erra cents. (REGUA-DE-AUDIO-20261025.md, 25/10 — §7.2; ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10 — "nunca confie no nome, meça")
- **2.4.** Reserve o "ombro" do kick (~150 Hz) para o baixo: havendo acúmulo, corte em sino Q 2–3, −3 a −6 dB. (anti-mascaramento-kick-bass.md, 08/09)
- **2.5.** Dê altas frequências ao ataque/click para o kick sobreviver sobre o baixo e em sistemas menores; click fraco pede +2–3 dB em 2–5 kHz. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10 — Zenon, R cena; anti-mascaramento-kick-bass.md, 08/09)
- **2.6.** Mantenha o kick na grade: 0–5 ms de microtiming como alvo de engenharia; offsets aleatórios grandes (>25 ms) passam o limiar de detecção (JND 19–24 ms para bateria) e descoordenam o motor. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10 — E/C perceptual)

## 3. Baixo rolling — envelope, timbre, saturação

- **3.1.** Calcule a célula pelo BPM vigente: 16 avos a 128 BPM = 117,19 ms por célula; envelope efetivo acima disso invade a próxima célula por construção (BPM em disputa — §8.2). (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10 — C)
- **3.2.** Comece a duração da nota em 64–94 ms (55–80% de um 16º a 128 BPM); ~50–105 ms continua plausível conforme o envelope. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10 — E)
- **3.3.** Feche o filtro do baixo em ~120–250 Hz e module o cutoff com envelope curto (+15% a +25%) — as referências Fox/AlpaKa/Zenon têm quase nenhuma energia de bass acima de 300–400 Hz. (PME_EXPERTS_PSYTECH_BASS_BIBLE.md, s.d.)
- **3.4.** Deixe a pressão no sub (~69 Hz = C#1) e o corpo no 2º harmônico (~138 Hz = C#2) — essa região fraca soa como subwoofer sem peso; o 3º harmônico (~207 Hz) dá definição. (PME_EXPERTS_PSYTECH_BASS_BIBLE.md, s.d.)
- **3.5.** Sature de forma cirúrgica: Tube/Soft Sine concentrado em 140–250 Hz, sub mono abaixo de 120 Hz 100% puro e agudos acima de 400 Hz cortados no canal de bass. (PME_EXPERTS_PSYTECH_BASS_BIBLE.md, s.d.)
- **3.6.** Dê "barriga" ao envelope (hold/decay sustentado pela fração da semicolcheia) e ajuste release em 40–80 ms — a cauda respira até o próximo kick em vez de cortar seca. (PME_EXPERTS_PSYTECH_BASS_BIBLE.md, s.d.)
- **3.7.** Ordene os harmônicos: fundamental (sub) como mais alta, seguida de perto pelo 2º harmônico — a relação mais importante do timbre do baixo. (PME_EXPERTS_PSYTECH_BASS_BIBLE.md, s.d.)
- **3.8.** Humanize por velocity em escadinha (45/95/118/80 por 4 notas) e module cutoff/drive pelo velocity. (PME_EXPERTS_PSYTECH_BASS_BIBLE.md, s.d.)
- **3.9.** Valorize as casas menos acentuadas (2ª e 4ª semicolcheias) no baixo sincopado; no rolling, deixe a 1ª nota fraca/duckada pelo sidechain. (PME_EXPERTS_PSYTECH_BASS_BIBLE.md, s.d.)
- **3.10.** Faça o baixo respirar com o kick: pocket no tempo do kick → subida → pico de pressão no offbeat → cauda sustentada que entrega ao próximo kick; mono legato com portamento sutil. (PME_EXPERTS_PSYTECH_BASS_BIBLE.md, s.d. — padrão medido em stem: `ESTIMATIVA`, ver §8.4)

## 4. Anti-mascaramento kick × baixo

- **4.1.** Divida o espectro: kick dono de 30–90 Hz e bass dono de 90–250 Hz; HP 90 Hz/24 dB-oct no bass e HP 30 Hz no master (rumble). (anti-mascaramento-kick-bass.md, 08/09)
- **4.2.** Garanta ~30 Hz mínimos entre as fundamentais e afine o bass contra o pitch REAL do kick (63 Hz vs C2 = 65,4 Hz dá batimento de 2,4 Hz). (anti-mascaramento-kick-bass.md, 08/09 — Sokolovskiy)
- **4.3.** Atrase o bass 5–15 ms após o kick — offset típico psytrance. (anti-mascaramento-kick-bass.md, 08/09 — Myloops)
- **4.4.** Corrija fase nesta ordem: nudge em ms → inverter polaridade → EQ linear-phase apenas em crossovers íngremes. (anti-mascaramento-kick-bass.md, 08/09)
- **4.5.** Cheque mono na zona 80–120 Hz a cada nota e sample: a combinação que perde >3 dB no mono-sum repetidamente em 25–120 Hz reprova o trecho. (anti-mascaramento-kick-bass.md, 08/09; ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10 — gate CRÍTICO)
- **4.6.** Mantenha o low-end mono até 120 Hz com correlação ≥0,98 no render (gate prático do corpus); heurísticas do gênero vão até 150–200 Hz, então 120 é conservador. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10 — R corpus)
- **4.7.** Abra o conflito "boxy" em ~300 Hz com incrementos pequenos acima de 250 Hz. (anti-mascaramento-kick-bass.md, 08/09)
- **4.8.** Cole o bus kick+bass com Glue 2:1, attack ~20 ms, release ~80 ms e 1–2 dB de GR. (anti-mascaramento-kick-bass.md, 08/09 — Myloops)
- **4.9.** Sature o BASS (não o sub do kick): harmônicos 300 Hz–3 kHz fazem o baixo aparecer em sistemas pequenos. (anti-mascaramento-kick-bass.md, 08/09)

## 5. Sidechain

- **5.1.** Resolva kick × baixo primeiro por arranjo + envelope curto + fase coerente — a ordem Zenon é phase alignment → kick EQ → bass articulation; 0 dB de ducking é válido quando a separação física funciona, e não existe justificativa para impor 2–6 dB só por gênero. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10 — C/R; a prática complementar de duckar todo elemento que colide com o ataque do kick está na régua-mixagem-e-master §4.4–4.5)
- **5.2.** Quando usar sidechain: attack 0–0,2 ms (ou ~4 ms anti-clique), ratio 4:1 a 8:1+, threshold calibrado em 8–12 dB de gain reduction, release <50 ms ou 80–100 ms afinado na cauda — o release é o dial decisivo. (anti-mascaramento-kick-bass.md, 08/09)
- **5.3.** Cuidado com o ataque rápido em fonte grave: <50 ms pode seguir ciclos individuais da onda e distorcer o low-end. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10 — citando FabFilter, C)
- **5.4.** Sem plugins: ducking por automação de gain do Utility (cai no beat, segura 30–50 ms, volta em 60–80 ms) ou Multiband Dynamics duckando só a banda low do bass. (anti-mascaramento-kick-bass.md, 08/09)
- **5.5.** Valide o trigger com 1 cópia vs N cópias antes de decidir: 8 eventos idênticos somariam até ~+18 dB no limite teórico e mudam thresholds invisivelmente. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10)
- **5.6.** Trate sidechain como meio, não resultado: a pergunta final é "o render prova que kick e baixo coexistem sem mascaramento/cancelamento?". (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10)

## 6. Jogo de ausência do kick

- **6.1.** Tire o kick por blocos longos e deixe o grave respirar: a referência Gazolla (Mayuri) tira o kick por ~30 s em duas seções e o bass sobe nesse intervalo (34,1 dB, máximo até então). (gazolla-analise-faixas.md, 08/09 — R)
- **6.2.** Abra a faixa com pulso de grave 1× por compasso: furos de LF de 0,80 s espaçados exatamente 1 compasso, 16 seguidos. (gazolla-analise-faixas.md, 08/09 — R)
- **6.3.** Vá ao zero de transientes no break: a Slippery Slope mede ~15 s sem transientes e o onset do break pode chegar a 0/s; intro com ou sem kick são igualmente válidas. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10 — R)
- **6.4.** Desenhe dois polos rítmicos: primeiro tempo + último 16º antes do próximo pulso. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10 — R Slippery)
- **6.5.** Faça pergunta e resposta: kick limpo no tempo 1 e, em ciclos específicos, resposta do rolling no último 16º — sem somar onsets totais. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10)
- **6.6.** Transforme os vácuos da cama de sub em eventos formais: sub em zero nos dois tempos vazios e uma única resposta seca de wood/hat/glitch no último 16º. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10)
- **6.7.** Saia por erosão vertical no outro: retire topo em etapas mantendo kick/rolling/sub e o centro por último — a curva 8k+ cai antes da de 25–75 Hz. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10)
- **6.8.** Corte o grave a seco nas quebras, sem reverb no low-end. (andre-gazolla.md, 08/09 — INFERÊNCIA do padrão da lane do artista: Black Belt, cena low-BPM psy nacional)
- **6.9.** Segure a densidade da marcha: corpus forte = 6,0–6,8 onsets/s, gate interno ≤6,99/s. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10 — R)
- **6.10.** Calibre microtiming de hats/percussão em 5–20 ms intencionais; a assinatura Gazolla adianta contratempos de hats 12–14 ms e mantém os 16ths no grid. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10 — C perceptual; gazolla-analise-faixas.md, 08/09 — R)
- **6.11.** Entre no drop por degrau, não por fade: saltos medidos de +52 a +62 dB no envelope LF nos drops principais. (gazolla-analise-faixas.md, 08/09 — R)

## 7. Diagnóstico do bloco grave

- **7.1.** Trate cancelamento recorrente kick×sub como problema crítico: mono-sum ou combinação kick+bass perdendo >3 dB repetidamente em 25–120 Hz reprova o trecho em hits equivalentes. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10 — CRÍTICO)
- **7.2.** Prove a separação no render: meça envelope/energia em janelas 0–30 / 30–60 / 60–90 / 90–117 ms após cada kick, conferindo polaridade e mono-sum. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10)
- **7.3.** Vigie o limiter: redução reaparecendo a cada kick/16º com crest dos drops abaixo de 6 dB indica que o limiter virou o envelope rítmico. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10 — MÉDIO)
- **7.4.** Etiquete como `ESTIMATIVA` toda leitura que dependa de stem separado por IA (Demucs e similares) — vale para o padrão de respiração do item 3.10. (MAPA-DE-LACUNAS-E-CONFLITOS-20261030.md, 30/10 — conflito 7)

## 8. EM DISPUTA (conflitos abertos no mapa — não resolver aqui)

- **8.1.** **Teto de True Peak — duas leituras:** (a) −0,3 dBTP ao masterizar (REGUA-DE-AUDIO-20261025.md, 25/10 — §5.4); (b) Spotify pede <−2 dBTP para master >−14 LUFS e o estado −0,6 falha esse critério em 1,4 dB (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10). O mapa marca masterização como lacuna crítica (duplo limiter contamina medidas do render); a leitura completa das três leituras está na régua-mixagem-e-master §6.1. (MAPA-DE-LACUNAS-E-CONFLITOS-20261030.md, 30/10 — conflito 5)
- **8.2.** **BPM da régua temporal — duas leituras:** cânon 128 BPM (16º = 117,19 ms; ESTUDO 17/10) × estado atual do set a 130 BPM (16º ≈ 115,4 ms; aritmética derivada). O mapa manda tratar 130 como estado, não como lei nova. (MAPA-DE-LACUNAS-E-CONFLITOS-20261030.md, 30/10 — conflito 3)
- **8.3.** **Sidechain no set do autor (Kickstart 2 / `SUBS A/B` / `SUB NOVO`) — duas leituras:** nomes de canal do set do autor — referência, não régua. O plano de 29/10 relata Kickstart 2 ligado em `SUBS A/B` e `SUB NOVO` mudo; a reconciliação de 30/10 relata Kickstart desligado e `SUB NOVO` ativo. Verificação pendente no Live (read-back dos canais), sem escolher versão. (MAPA-DE-LACUNAS-E-CONFLITOS-20261030.md, 30/10 — conflito 4)
- **8.4.** **Padrão de respiração do baixo (Fox, item 3.10) — duas leituras:** usar como ilustração de fraseado × não usar como prova — o stem é estimativa de separação. (MAPA-DE-LACUNAS-E-CONFLITOS-20261030.md, 30/10 — conflito 7)

## 9. Casos (contraste com o set do autor — referência, não régua)

- **9.1.** Caso medido de 17/10: sub−kick = −2,64 dB (dentro do corpus), mas `(55–75)−(40–55)` = +4,0 dB (FORA, limite +2), densidade 7,57 onsets/s (FORA, teto 6,99) e 8 kHz+ com déficit de 6,3 dB contra a média das refs. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10)
- **9.2.** Kick principal do set mediu 52,5 Hz ≈ G#1 (+20 cents, 5ª justa de C#) e o alternativo 46,4 Hz ≈ F#1 (4ª justa) — ambos consonantes; o rack se intitulava "Organic 48Hz" (erro de ~90 cents se ajustado pelo nome). (REGUA-DE-AUDIO-20261025.md, 25/10 — §7.2)
- **9.3.** O briefing chamava o rolling de "C#2 ≈ 103,8 Hz"; C#2 = 69,3 Hz e 103,8 Hz ≈ G#2 — a auditoria confirmou o canal em G#2. (ESTUDO-BATERIA-E-BAIXO-20261017.md, 17/10)
- **9.4.** No render de 25/10, o bass ficou idêntico à família (36,9 vs 37,1%) e o grave 9 dB mais mono que a mediana — o desejado com cânon low-end mono. (REGUA-DE-AUDIO-20261025.md, 25/10 — §2)

---

*Contraste numérico pronto para virar experimento (EXP-03/04, SYN-02, mapa 30/10 §6): separação kick×cada grave por janelas pós-kick (§7.2) e trigger de sidechain 1 vs N cópias (§5.5). Método de medição: taxa original, estéreo, janela declarada (REGUA-DE-AUDIO-20261025.md, 25/10 — §6).*
