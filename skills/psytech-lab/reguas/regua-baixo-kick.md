# Regua: baixo e kick

**Sub · Kick · Sidechain · Jogo de ausencia do kick · Anti-mascaramento kick × baixo**

> Conflitos abertos ficam marcados EM DISPUTA; o contexto do set de referencia aparece so em Casos (§9).
> **Fontes:**
> `acervo/pesquisas/ESTUDO-BATERIA-E-BAIXO-20261017.md`
> `acervo/diagnosticos/REGUA-DE-AUDIO-20261025.md`
> `acervo/knowledge-base/PME_EXPERTS_PSYTECH_BASS_BIBLE.md`
> `acervo/knowledge-base/anti-mascaramento-kick-bass.md`
> `acervo/knowledge-base/gazolla-analise-faixas.md`
> `acervo/knowledge-base/andre-gazolla.md`
> `MAPA-DE-LACUNAS-E-CONFLITOS-20261030.md` (so para os pontos EM DISPUTA)
>
> Classes do estudo de bateria e baixo: C = consenso tecnico · R = medido em referencias externas · E = faixa de engenharia recomendada. Fontes sem classe (PME, compilacoes de aula) sao receita de instrutor, nao medicao.

## 1. Fundamento e balanca dos graves

- **1.1.** Equilibre o peso entre as camadas do grave: `(sub 25–40 Hz) − (kick 40–55 Hz)` fica bem entre `−3 e +0,5 dB`; o corpus medido (Kaled/Gazolla/ISMAIL/Slippery) vai de `−6,77 a +0,34 dB`; abaixo de ~−7 dB o bloco fica magro, acima de ~+1 dB exige validacao de headroom.
- **1.2.** Mantenha um so "andar" dominante: `(55–75) − (40–55)` ≤ `+1,5 dB`; o corpus mede `−1,2…+1,4 dB` e da alerta forte acima de `+2 dB`.
- **1.3.** Deixe o kick 2–3 dB acima do bassline no fader; o metodo objetivo e igualar os dois por LUFS no solo e ajustar de la.
- **1.4.** Regua de banda da familia (mediana de 15 referencias masterizadas; min–max): sub 47,5% (13,5–59,0) · bass 37,1% (22,8–52,7) · side/mid do grave −32,7 dB (−48,6 a −12,9).
- **1.5.** Kick psytrance: fundamental 50–70 Hz e click 2–5 kHz; fundamentos de bass/kick moram tipicamente em 40–80 Hz.

## 2. Kick: afinacao, cauda, ataque, timing

- **2.1.** Afine o kick em grau consonante da tonalidade, nao necessariamente na tonica: a familia de 53 kicks (pack Drift) mede fundamental mediana 49,1 Hz (25,6–68,0), com classes G1 (15) · G#1 (11) · A1 (6) · F#1 (5) · E1 (5).
- **2.2.** Cauda de referencia do pack: decay −20 dB mediano 0,19 s (0,08–0,39); duracao do arquivo mediana 0,48 s.
- **2.3.** Meca a fundamental por FFT e trate o nome do sample/rack como suspeito, porque o ajuste "pelo nome" erra cents.
- **2.4.** Reserve o "ombro" do kick (~150 Hz) para o baixo: havendo acumulo, corte em sino Q 2–3, −3 a −6 dB.
- **2.5.** De altas frequencias ao ataque/click para o kick sobreviver sobre o baixo e em sistemas menores; click fraco pede +2–3 dB em 2–5 kHz.
- **2.6.** Mantenha o kick na grade: 0–5 ms de microtiming como alvo de engenharia; offsets aleatorios grandes (>25 ms) passam o limiar de deteccao (JND 19–24 ms para bateria) e descoordenam o motor.

## 3. Baixo rolling: envelope, timbre, saturacao

- **3.1.** Calcule a celula pelo BPM vigente: 16 avos a 128 BPM = 117,19 ms por celula; envelope efetivo acima disso invade a proxima celula por construcao (BPM em disputa, §8.2).
- **3.2.** Comece a duracao da nota em 64–94 ms (55–80% de um 16º a 128 BPM); ~50–105 ms continua plausivel conforme o envelope.
- **3.3.** Feche o filtro do baixo em ~120–250 Hz e module o cutoff com envelope curto (+15% a +25%); as referencias Fox/AlpaKa/Zenon tem quase nenhuma energia de bass acima de 300–400 Hz.
- **3.4.** Deixe a pressao no sub (~69 Hz = C#1) e o corpo no 2º harmonico (~138 Hz = C#2); essa regiao fraca soa como subwoofer sem peso, e o 3º harmonico (~207 Hz) da definicao.
- **3.5.** Sature de forma cirurgica: Tube/Soft Sine concentrado em 140–250 Hz, sub mono abaixo de 120 Hz 100% puro e agudos acima de 400 Hz cortados no canal de bass.
- **3.6.** De "barriga" ao envelope (hold/decay sustentado pela fracao da semicolcheia) e ajuste release em 40–80 ms; a cauda respira ate o proximo kick em vez de cortar seca.
- **3.7.** Ordene os harmonicos: fundamental (sub) como mais alta, seguida de perto pelo 2º harmonico, a relacao mais importante do timbre do baixo.
- **3.8.** Humanize por velocity em escadinha (45/95/118/80 por 4 notas) e module cutoff/drive pelo velocity.
- **3.9.** Valorize as casas menos acentuadas (2ª e 4ª semicolcheias) no baixo sincopado; no rolling, deixe a 1ª nota fraca/duckada pelo sidechain.
- **3.10.** Faca o baixo respirar com o kick: pocket no tempo do kick → subida → pico de pressao no offbeat → cauda sustentada que entrega ao proximo kick; mono legato com portamento sutil (padrao medido em stem: `ESTIMATIVA`, ver §8.4).

## 4. Anti-mascaramento kick × baixo

- **4.1.** Divida o espectro: kick dono de 30–90 Hz e bass dono de 90–250 Hz; HP 90 Hz/24 dB-oct no bass e HP 30 Hz no master (rumble).
- **4.2.** Garanta ~30 Hz minimos entre as fundamentais e afine o bass contra o pitch REAL do kick (63 Hz vs C2 = 65,4 Hz da batimento de 2,4 Hz).
- **4.3.** Atrase o bass 5–15 ms apos o kick, offset tipico psytrance.
- **4.4.** Corrija fase nesta ordem: nudge em ms → inverter polaridade → EQ linear-phase apenas em crossovers ingremes.
- **4.5.** Cheque mono na zona 80–120 Hz a cada nota e sample: a combinacao que perde >3 dB no mono-sum repetidamente em 25–120 Hz reprova o trecho.
- **4.6.** Mantenha o low-end mono ate 120 Hz com correlacao ≥0,98 no render (gate pratico do corpus); heuristicas do genero vao ate 150–200 Hz, entao 120 e conservador.
- **4.7.** Abra o conflito "boxy" em ~300 Hz com incrementos pequenos acima de 250 Hz.
- **4.8.** Cole o bus kick+bass com Glue 2:1, attack ~20 ms, release ~80 ms e 1–2 dB de GR.
- **4.9.** Sature o BASS (nao o sub do kick): harmonicos 300 Hz–3 kHz fazem o baixo aparecer em sistemas pequenos.

## 5. Sidechain

- **5.1.** Resolva kick × baixo primeiro por arranjo + envelope curto + fase coerente: a ordem Zenon e phase alignment → kick EQ → bass articulation; 0 dB de ducking e valido quando a separacao fisica funciona, e nao existe justificativa para impor 2–6 dB so por genero (a pratica complementar de duckar todo elemento que colide com o ataque do kick esta na regua de mixagem e master, §4.4–4.5).
- **5.2.** Quando usar sidechain: attack 0–0,2 ms (ou ~4 ms anti-clique), ratio 4:1 a 8:1+, threshold calibrado em 8–12 dB de gain reduction, release <50 ms ou 80–100 ms afinado na cauda; o release e o dial decisivo.
- **5.3.** Cuidado com o ataque rapido em fonte grave: <50 ms pode seguir ciclos individuais da onda e distorcer o low-end.
- **5.4.** Sem plugins: ducking por automacao de gain do Utility (cai no beat, segura 30–50 ms, volta em 60–80 ms) ou Multiband Dynamics duckando so a banda low do bass.
- **5.5.** Valide o trigger com 1 copia vs N copias antes de decidir: 8 eventos identicos somariam ate ~+18 dB no limite teorico e mudam thresholds invisivelmente.
- **5.6.** Trate sidechain como meio, nao resultado: a pergunta final e "o render prova que kick e baixo coexistem sem mascaramento/cancelamento?".

## 6. Jogo de ausencia do kick

- **6.1.** Tire o kick por blocos longos e deixe o grave respirar: a referencia Gazolla (Mayuri) tira o kick por ~30 s em duas secoes e o bass sobe nesse intervalo (34,1 dB, maximo ate entao).
- **6.2.** Abra a faixa com pulso de grave 1× por compasso: furos de LF de 0,80 s espacados exatamente 1 compasso, 16 seguidos.
- **6.3.** Va ao zero de transientes no break: a Slippery Slope mede ~15 s sem transientes e o onset do break pode chegar a 0/s; intro com ou sem kick sao igualmente validas.
- **6.4.** Desenhe dois polos ritmicos: primeiro tempo + ultimo 16º antes do proximo pulso.
- **6.5.** Faca pergunta e resposta: kick limpo no tempo 1 e, em ciclos especificos, resposta do rolling no ultimo 16º, sem somar onsets totais.
- **6.6.** Transforme os vacuos da cama de sub em eventos formais: sub em zero nos dois tempos vazios e uma unica resposta seca de wood/hat/glitch no ultimo 16º.
- **6.7.** Saia por erosao vertical no outro: retire topo em etapas mantendo kick/rolling/sub e o centro por ultimo; a curva 8k+ cai antes da de 25–75 Hz.
- **6.8.** Corte o grave a seco nas quebras, sem reverb no low-end (INFERENCIA do padrao da lane do artista: Black Belt, cena low-BPM psy nacional).
- **6.9.** Segure a densidade da marcha: corpus forte = 6,0–6,8 onsets/s, gate interno ≤6,99/s.
- **6.10.** Calibre microtiming de hats/percussao em 5–20 ms intencionais; a assinatura Gazolla adianta contratempos de hats 12–14 ms e mantem os 16ths no grid.
- **6.11.** Entre no drop por degrau, nao por fade: saltos medidos de +52 a +62 dB no envelope LF nos drops principais.

## 7. Diagnostico do bloco grave

- **7.1.** Trate cancelamento recorrente kick×sub como problema critico: mono-sum ou combinacao kick+bass perdendo >3 dB repetidamente em 25–120 Hz reprova o trecho em hits equivalentes.
- **7.2.** Prove a separacao no render: meca envelope/energia em janelas 0–30 / 30–60 / 60–90 / 90–117 ms apos cada kick, conferindo polaridade e mono-sum.
- **7.3.** Vigie o limiter: reducao reaparecendo a cada kick/16º com crest dos drops abaixo de 6 dB indica que o limiter virou o envelope ritmico.
- **7.4.** Etiquete como `ESTIMATIVA` toda leitura que dependa de stem separado por IA (Demucs e similares); vale para o padrao de respiracao do item 3.10 (conflito 7).

## 8. EM DISPUTA (conflitos abertos no mapa; nao resolver aqui)

- **8.1.** **Teto de True Peak (duas leituras):** (a) −0,3 dBTP ao masterizar; (b) Spotify pede <−2 dBTP para master >−14 LUFS e o estado −0,6 falha esse criterio em 1,4 dB. O mapa marca masterizacao como lacuna critica (duplo limiter contamina medidas do render); a leitura completa das tres leituras esta na regua de mixagem e master (§6.1). (conflito 5)
- **8.2.** **BPM da regua temporal (duas leituras):** canon 128 BPM (16º = 117,19 ms) × estado atual do set a 130 BPM (16º ≈ 115,4 ms, aritmetica derivada). O mapa manda tratar 130 como estado, nao como lei nova. (conflito 3)
- **8.3.** **Sidechain no set do autor (Kickstart 2 / `SUBS A/B` / `SUB NOVO`), duas leituras:** nomes de canal do set do autor (referencia, nao regua). O plano relata Kickstart 2 ligado em `SUBS A/B` e `SUB NOVO` mudo; a reconciliacao relata Kickstart desligado e `SUB NOVO` ativo. Verificacao pendente no Live (read-back dos canais), sem escolher versao. (conflito 4)
- **8.4.** **Padrao de respiracao do baixo (Fox, item 3.10), duas leituras:** usar como ilustracao de fraseado × nao usar como prova, pois o stem e estimativa de separacao. (conflito 7)

## 9. Casos (contraste com o set do autor; referencia, nao regua)

- **9.1.** Caso medido no estudo de bateria e baixo: sub−kick = −2,64 dB (dentro do corpus), mas `(55–75)−(40–55)` = +4,0 dB (FORA, limite +2), densidade 7,57 onsets/s (FORA, teto 6,99) e 8 kHz+ com deficit de 6,3 dB contra a media das refs.
- **9.2.** Kick principal do set mediu 52,5 Hz ≈ G#1 (+20 cents, 5ª justa de C#) e o alternativo 46,4 Hz ≈ F#1 (4ª justa), ambos consonantes; o rack se intitulava "Organic 48Hz" (erro de ~90 cents se ajustado pelo nome).
- **9.3.** O briefing chamava o rolling de "C#2 ≈ 103,8 Hz"; C#2 = 69,3 Hz e 103,8 Hz ≈ G#2; a auditoria confirmou o canal em G#2.
- **9.4.** No render medido, o bass ficou identico a familia (36,9 vs 37,1%) e o grave 9 dB mais mono que a mediana, o desejado com canon low-end mono.

---

*Contraste numerico pronto para virar experimento (EXP-03/04, SYN-02, §6 do mapa): separacao kick×cada grave por janelas pos-kick (§7.2) e trigger de sidechain 1 vs N copias (§5.5). Metodo de medicao: taxa original, estereo, janela declarada.*
