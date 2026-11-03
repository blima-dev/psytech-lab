# Perguntas canônicas — psytech, techno e minimal progressivo (multi-tempo)

> As 10 perguntas que um produtor do gênero faz de verdade numa sessão, e o arquivo do pacote psytech-lab
> que responde cada uma. Caminhos relativos à pasta da skill (`plugins/psytech-lab/skills/psytech-lab/`).
> Compiladas em 01/11/2026 a partir da leitura das 6 réguas e do arquivo de casos — nada aqui é opinião de fora.
>
> **Como usar:**
> - **Régua** (`reguas/`) = resposta destilada, com número e fonte citada (arquivo + data) em cada item.
> - **Acervo** (`acervo/`) = fonte profunda, citada pela própria régua no cabeçalho "Fontes".
> - **Casos** (`casos/`) = porta de entrada por sintoma, quando algo quebrou ou o número briga com o ouvido.
> - **EM DISPUTA** dentro das réguas = conflito aberto do mapa de 30/10 (`acervo/raiz/MAPA-DE-LACUNAS-E-CONFLITOS-20261030.md`)
>   — a régua registra as leituras, não decide; decidir é do ouvido do produtor.
> - Contexto dos estudos de origem: maioria medida a 128 BPM (semicolcheia = 117,19 ms); o DNA do gênero aponta 130–134 — leia as duas leituras em `reguas/regua-baixo-kick.md` §8.2. C# frígio é do set de referência, não lei do gênero. Low-end mono ≤ 120 Hz.

---

## 1. "Meu grave embola com o kick. Quem é dono de qual banda, quanto de sidechain é de verdade — e em que nota afino cada um?"

**Responde:** `reguas/regua-baixo-kick.md`
- §1 — balança: `(sub 25–40 Hz) − (kick 40–55 Hz)` entre −3 e +0,5 dB; kick 2–3 dB acima do bassline no fader.
- §2 + §4.2 — afinar kick e bass em grau consonante da tonalidade, medindo por FFT (o nome do sample mente).
- §4 — divisão de bandas: kick dono de 30–90 Hz, bass dono de 90–250 Hz; bass 5–15 ms atrás do kick; mono-sum com correlação ≥0,98 até 120 Hz.
- §5 — sidechain como meio: attack 0–0,2 ms, ratio 4:1–8:1, GR 8–12 dB, release <50 ms ou 80–100 ms; 0 dB de ducking é válido quando a separação física funciona.

**Aprofunda:** `acervo/knowledge-base/anti-mascaramento-kick-bass.md` (08/09) · `acervo/pesquisas/ESTUDO-BATERIA-E-BAIXO-20261017.md` (17/10)

## 2. "Como desenho o baixo rolling — duração da nota, envelope, filtro, saturação, velocity — e como calculo as células no MEU BPM?"

**Responde:** `reguas/regua-baixo-kick.md` §3
- Célula de 16 avos = 117,19 ms @128; duração de nota em 64–94 ms (55–80% de um 16º).
- Filtro fechado em ~120–250 Hz com envelope curto de cutoff (+15–25%); as referências têm quase nada acima de 300–400 Hz.
- Pressão no sub (~69 Hz = C#1), corpo no 2º harmônico (~138 Hz), saturação quente concentrada em 140–250 Hz, sub mono puro <120 Hz.
- "Barriga" no envelope, release 40–80 ms; velocity em escadinha 45/95/118/80 modulando cutoff/drive; baixo respira com o kick (pico de pressão no offbeat).

**Aprofunda:** `acervo/knowledge-base/PME_EXPERTS_PSYTECH_BASS_BIBLE.md` (s.d.) · `acervo/pesquisas/ESTUDO-BATERIA-E-BAIXO-20261017.md` (17/10)

## 3. "Quando e como tiro o kick para o grave respirar, sem esvaziar a faixa?"

**Responde:** `reguas/regua-baixo-kick.md` §6
- Tirar o kick por blocos longos: a referência Gazolla tira por ~30 s e o bass sobe no intervalo.
- Abertura por pulso de grave 1× por compasso (furos de LF de 0,80 s espaçados 1 compasso).
- Dois polos rítmicos (tempo 1 + último 16º) e pergunta-resposta em vez de somar onsets.
- Densidade da marcha: 6,0–6,8 onsets/s, teto ≤6,99/s; saída do outro por erosão vertical (topo sai antes do sub); grave cortado a seco nas quebras, sem reverb no low-end.

**Aprofunda:** `acervo/knowledge-base/gazolla-analise-faixas.md` (08/09) · `acervo/pesquisas/refs-artistas/ANALISE-SLIPPERY-SLOPE-LUISM-20261016.md` (16/10)

## 4. "O que escrevo no lead? Quantas notas, qual registro, quando entra a b2 — e como faço a conversa com a percussão?"

**Responde:** `reguas/regua-melodia-e-harmonia.md`
- Motivo de 2–3 notas: tônica, b2 e 5ª (em C#: C#, D, G#); harmonia ancorada em centro modal menor com drone de tônica (§1–2).
- Lead ancorado na tônica 65–95% das notas; a b2 quase não aparece no lead (0–5%) — a cor frígia mora no grave (item 6).
- Staccato de 0,1–0,3 s; registro C#3–C#4 (C#3 é corpo, não sub) (itens 17 e 26).
- Conversa com a percussão: ~50% simultâneo, buraco ~16%, resposta atrasada como minoria; pergunta-resposta com 1 compasso de silêncio escrito (itens 10–12).
- b2 como inflexão, não cama: bend de +1 semitom (~120 ms) ou 1 dissonância por frase (itens 7 e 18); voicing de quintas/oitavas sem terça para solene (item 23).
- **EM DISPUTA** (§8): C#5 como exceção no registro; b2 no lead por timbre/função.

**Aprofunda:** `acervo/pesquisas/ESTUDO-ARRANJO-FX-DESENHO-20261025.md` (25/10) · `acervo/pesquisas/tutoriais/MELODIA.md` (s.d.)

## 5. "A faixa está reta e parada. Quando entra camada nova, quanto dura cada estado, o que subtraio e quando?"

**Responde:** `reguas/regua-arranjo-e-transicao.md` §1–2
- 1 track nova a cada ~16 bars; elemento entra e fica (mediana 48 bars); refresh de versão a cada ~60 bars com stitch-ponte (§1.4–1.7).
- Fundação imortal: kick e baixo correm do primeiro ao último compasso; energia se administra removendo camadas de cima, nunca a base (§1.5).
- Régua de 8 bars: 1–8 base + hook, 9–16 camada forte, 17–24 remove algo, 25–32 fill, 33 mudança de seção (§1.10).
- Turnover saudável: 3–4 compassos por estado de camada e 2,8–6,7 mudanças/min; algo audível muda a cada ~15 s (§2.15–2.16).
- Variar sem compor novo: mesmo MIDI com outro timbre ou ritmo vira seção diferente que ainda encaixa (§2.21).

**Aprofunda:** `acervo/pesquisas/refs-artistas/PROFESSOR-ARRANJO-UNDERTOW-2026-09-08.md` (08/09) · `acervo/knowledge-base/arranjo-anti-estase.md` (08/09)

## 6. "O que ponho na fronteira do drop — riser tonal, sucção, silêncio? E qual a dose certa de vácuo?"

**Responde:** `reguas/regua-arranjo-e-transicao.md` §3–5
- Um dono por fronteira: um gesto por corte; se já existe reverse/crash/sweep, substitui em vez de somar (§3.27).
- Usar o próprio alvo como subida (invertido com fade); FX de transição fora do grave (HP ≥120 Hz); master conta a história: 1–2 dB de GR no drop, não 6 (§3.28, 3.30, 3.34).
- Vácuo: silêncio total reservado a 1–3 momentos por faixa, quase sempre no último terço; dose da família 0,11–0,80 gaps/min; puxar o sub nos 1–2 bars finais antes do drop (§4.37–4.39).
- Riser/downlifter em pares; riser de referência em 8 bars e 3 camadas (tonal 0 dB + noise −12/−15 + rítmica −6/−9); sweep de ruído filtrado como alternativa (§5.44–5.47).
- **EM DISPUTA** (§6 D3): riser tonal de 8 compassos é conteúdo normal do gênero × diretriz que o aposenta — a régua registra, não decide.

**Aprofunda:** `acervo/pesquisas/ESTUDO-ARRANJO-FX-DESENHO-20261025.md` (25/10) · `acervo/pesquisas/tutoriais/TRANSICOES.md` (27/10)

## 7. "Como desenho o timbre no Serum 2 — camadas, envelope, distorção — e onde entra madeira orgânica e granular sem virar enfeite?"

**Responde:** `reguas/regua-texturas-e-sounddesign.md`
- Economia por função (pack Drift, 152 presets): baixo 2 camadas/2 FX · lead e pluck 3 camadas/5 FX · pad 2 camadas; resolver o timbre dentro do patch (§B, itens 7–8).
- ENV1 de referência: attack 0,5 ms · decay 1,0 s · sustain 0,79 · release 76 ms; distorção idêntica antes e depois do filtro; phase distortion como sujeira controlada (§B, itens 9–11).
- Madeira por função: acento/resposta em one-shots 0,2–1,0 s · topo percussivo contínuo em loops · madeira melódica (marimba/woodwinds) · cama granular (~1,5 s por grão); reafinar o pack para a tônica e tratar madeira como lado secundário (§C, itens 18–22).
- Granular por função: grão de drone 150–300 ms, resposta percussiva 60–120 ms, madeira 100–160 ms; cama nasce de fonte acústica e entra/sai por seção (§D, itens 23–28).
- Espaço: Side real só acima de ~150–250 Hz; mono ≤120 Hz (§F, itens 46–47).
- **EM DISPUTA** (§H): HPF do drone 90 × 160 Hz; topo percussivo contínuo × G16/G17/G18 provisórias.

**Aprofunda:** `acervo/pesquisas/cursos/PRESETS-SERUM-20261025.md` (25/10) · `acervo/pesquisas/AUDITORIA-PACKS-ORGANICOS-20261029.md` (29/10)

## 8. "Que números miro no master — LUFS, true peak, crest, mono do low-end — e como meço sem me enganar?"

**Responde:** `reguas/regua-mixagem-e-master.md`
- Régua da família masterizada: LUFS-I −8,7 (−11,7 a −6,9) · crest 11,1 dB (9,2 a 15,7) · sub 47,5% · bass 37,1% (§1.5).
- Medir em taxa nativa e estéreo; limiter de escuta ligado no master contamina qualquer número (§1.1, §1.7).
- Gain staging: canais e grupos em 0,0 dB; low-cut do master LC12 @ 18–20 Hz (§2.2, §2.7).
- Dinâmica: Glue com GR máximo 1,5–2,0 dB; um limiter só com 2–3 dB de GR; distribuir a redução com clipper antes (§3.1–3.3).
- Low-end: monoizar abaixo de 100–120 Hz; uma camada só de BassMono (§4.1–4.2).
- Alvos por destino: streaming ≤ −1,0 dBTP com Spotify −14 LUFS; clube −8 a −6 LUFS (§5.1–5.2).
- **EM DISPUTA** (§6.1): três leituras coexistem de true peak (−1,0 / −0,3 / exigência de −2) — investigar a cadeia antes de cravar número.

**Aprofunda:** `acervo/pesquisas/estudo_master_20261017.md` (17/10) · `acervo/pesquisas/estudo_mix_20261017.md` (17/10) · `acervo/diagnosticos/REGUA-DE-AUDIO-20261025.md` (25/10)

## 9. "Como o Gazolla, o Kaled, a Akari e a AIO fazem groove, build e drop — com números, não de cabeça?"

**Responde:** `reguas/regua-referencias-artistas.md`
- Consenso transversal: 127–132 BPM; grave 20–120 Hz = 56–78% da energia; estrutura quantizada em 8 compassos; primeiro impacto ≤0:35 (§1.1, 1.2, 1.8, 1.9).
- Swing no topo, não no kick: hats adiantados 13–27 ms com kick/bass quantizados (§1.7).
- Kick com cauda tonal (decay −20 dB em 140–200 ms) e master da cena −7 a −6 LUFS com clipper antes do limiter (§1.6, §1.11).
- Fichas por artista (§2): Gazolla — grid cirúrgico, drops por degrau (+52 a +62 dB), pré-drop com micro-cuts e roll de kick; Kaled — camada orgânica permanente a ~4 clicks/s, build sem riser tonal; Yao — pleno com todas as camadas a 9–12 onsets/s, rolling "KBBB"; Akari — rolling 16ths planos 19–20 onsets/compasso sem pausa; AIO — dinâmica por filtro e vácuo filtrado pré-drop; Discretion — corte de downbeat a cada 16 compassos.

**Aprofunda:** `acervo/pesquisas/refs-artistas/ANALISE-COMPARATIVA-REFS-2026-09-08.md` (08/09) · `acervo/pesquisas/refs-artistas/AUDIOMETRIA-FISICA-PSYTECH-2026-09-09.md` (09/09)

## 10. "Um elemento sumiu, o número não bate com o ouvido, o timbre mudou sozinho — por onde começo o diagnóstico?"

**Responde:** `casos/cicatrizes-como-caso.md`
- Check de 60 segundos em 5 passos, sem pular: Alvo → Existência (mute de grupo/canal/clipe, janela) → Sinal (device, sidechain, fader × automação) → Número (render com hash, unidade) → Mudança pequena e reversível (§1).
- 86 casos reais em 6 famílias, cada um com sintoma → causa medida → correção que funcionou: silêncio/sinal (§3), preset/timbre/clipe (§4), medição e grade (§5), grave (§6), arranjo e orquestra (§7), pedido e processo (§8).
- Padrão recorrente: o estado real não era o que o documento/nome dizia; o número era de outro objeto ou unidade; a correção atacou a camada errada (§2).
- Regra das duas falhas: se a mesma correção falhar duas vezes, a premissa está errada — não a dose.

**Aprofunda:** `acervo/raiz/CICATRIZES-20261030.md` (30/10) — corpus original das lições, com custo documentado por caso

---

## Cobertura do pacote

| Arquivo | Perguntas |
|---|---|
| `reguas/regua-baixo-kick.md` | 1, 2, 3 |
| `reguas/regua-melodia-e-harmonia.md` | 4 |
| `reguas/regua-arranjo-e-transicao.md` | 5, 6 |
| `reguas/regua-texturas-e-sounddesign.md` | 7 |
| `reguas/regua-mixagem-e-master.md` | 8 |
| `reguas/regua-referencias-artistas.md` | 9 |
| `casos/cicatrizes-como-caso.md` | 10 |

---

*Fontes consultadas (caminho + data): as 6 réguas de `plugins/psytech-lab/skills/psytech-lab/reguas/` (destiladas 01/11/2026) · `plugins/psytech-lab/skills/psytech-lab/casos/cicatrizes-como-caso.md` (casos reescritos, lido 01/11/2026) · `acervo/raiz/CICATRIZES-20261030.md` e `acervo/raiz/MAPA-DE-LACUNAS-E-CONFLITOS-20261030.md` (30/10, lidos 01/11/2026) · varredura do inventário de `acervo/` (01/11/2026). Consulta ao Live: nenhuma — tarefa de documentação, sem mutação.*
