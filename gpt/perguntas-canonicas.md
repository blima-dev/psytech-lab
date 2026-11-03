# Perguntas canonicas — psytech, techno e minimal progressivo (multi-tempo)

> As 10 perguntas que um produtor do genero faz de verdade numa sessao, e o arquivo do pacote psytech-lab
> que responde cada uma. Caminhos relativos a pasta da skill (`plugins/psytech-lab/skills/psytech-lab/`).
> Compiladas em 01/11/2026 a partir da leitura das 6 reguas e do arquivo de casos — nada aqui e opiniao de fora.
>
> **Como usar:**
> - **Regua** (`reguas/`) = resposta destilada, com numero e fonte citada (arquivo + data) em cada item.
> - **Acervo** (`acervo/`) = fonte profunda, citada pela propria regua no cabecalho "Fontes".
> - **Casos** (`casos/`) = porta de entrada por sintoma, quando algo quebrou ou o numero briga com o ouvido.
> - **EM DISPUTA** dentro das reguas = conflito aberto do mapa de 30/10 (`acervo/raiz/MAPA-DE-LACUNAS-E-CONFLITOS-20261030.md`)
>   — a regua registra as leituras, nao decide; decidir e do ouvido do produtor.
> - Contexto dos estudos de origem: maioria medida a 128 BPM (semicolcheia = 117,19 ms); o DNA do genero aponta 130–134 — leia as duas leituras em `reguas/regua-baixo-kick.md` §8.2. C# frigio e do set de referencia, nao lei do genero. Low-end mono ≤ 120 Hz.

---

## 1. "Meu grave embola com o kick. Quem e dono de qual banda, quanto de sidechain e de verdade — e em que nota afino cada um?"

**Responde:** `reguas/regua-baixo-kick.md`
- §1 — balanca: `(sub 25–40 Hz) − (kick 40–55 Hz)` entre −3 e +0,5 dB; kick 2–3 dB acima do bassline no fader.
- §2 + §4.2 — afinar kick e bass em grau consonante da tonalidade, medindo por FFT (o nome do sample mente).
- §4 — divisao de bandas: kick dono de 30–90 Hz, bass dono de 90–250 Hz; bass 5–15 ms atras do kick; mono-sum com correlacao ≥0,98 ate 120 Hz.
- §5 — sidechain como meio: attack 0–0,2 ms, ratio 4:1–8:1, GR 8–12 dB, release <50 ms ou 80–100 ms; 0 dB de ducking e valido quando a separacao fisica funciona.

**Aprofunda:** `acervo/knowledge-base/anti-mascaramento-kick-bass.md` (08/09) · `acervo/pesquisas/ESTUDO-BATERIA-E-BAIXO-20261017.md` (17/10)

## 2. "Como desenho o baixo rolling — duracao da nota, envelope, filtro, saturacao, velocity — e como calculo as celulas no MEU BPM?"

**Responde:** `reguas/regua-baixo-kick.md` §3
- Celula de 16 avos = 117,19 ms @128; duracao de nota em 64–94 ms (55–80% de um 16º).
- Filtro fechado em ~120–250 Hz com envelope curto de cutoff (+15–25%); as referencias tem quase nada acima de 300–400 Hz.
- Pressao no sub (~69 Hz = C#1), corpo no 2º harmonico (~138 Hz), saturacao quente concentrada em 140–250 Hz, sub mono puro <120 Hz.
- "Barriga" no envelope, release 40–80 ms; velocity em escadinha 45/95/118/80 modulando cutoff/drive; baixo respira com o kick (pico de pressao no offbeat).

**Aprofunda:** `acervo/knowledge-base/PME_EXPERTS_PSYTECH_BASS_BIBLE.md` (s.d.) · `acervo/pesquisas/ESTUDO-BATERIA-E-BAIXO-20261017.md` (17/10)

## 3. "Quando e como tiro o kick para o grave respirar, sem esvaziar a faixa?"

**Responde:** `reguas/regua-baixo-kick.md` §6
- Tirar o kick por blocos longos: a referencia Gazolla tira por ~30 s e o bass sobe no intervalo.
- Abertura por pulso de grave 1× por compasso (furos de LF de 0,80 s espacados 1 compasso).
- Dois polos ritmicos (tempo 1 + ultimo 16º) e pergunta-resposta em vez de somar onsets.
- Densidade da marcha: 6,0–6,8 onsets/s, teto ≤6,99/s; saida do outro por erosao vertical (topo sai antes do sub); grave cortado a seco nas quebras, sem reverb no low-end.

**Aprofunda:** `acervo/knowledge-base/gazolla-analise-faixas.md` (08/09) · `acervo/pesquisas/refs-artistas/ANALISE-SLIPPERY-SLOPE-LUISM-20261016.md` (16/10)

## 4. "O que escrevo no lead? Quantas notas, qual registro, quando entra a b2 — e como faco a conversa com a percussao?"

**Responde:** `reguas/regua-melodia-e-harmonia.md`
- Motivo de 2–3 notas: tonica, b2 e 5ª (em C#: C#, D, G#); harmonia ancorada em centro modal menor com drone de tonica (§1–2).
- Lead ancorado na tonica 65–95% das notas; a b2 quase nao aparece no lead (0–5%) — a cor frigia mora no grave (item 6).
- Staccato de 0,1–0,3 s; registro C#3–C#4 (C#3 e corpo, nao sub) (itens 17 e 26).
- Conversa com a percussao: ~50% simultaneo, buraco ~16%, resposta atrasada como minoria; pergunta-resposta com 1 compasso de silencio escrito (itens 10–12).
- b2 como inflexao, nao cama: bend de +1 semitom (~120 ms) ou 1 dissonancia por frase (itens 7 e 18); voicing de quintas/oitavas sem terca para solene (item 23).
- **EM DISPUTA** (§8): C#5 como excecao no registro; b2 no lead por timbre/funcao.

**Aprofunda:** `acervo/pesquisas/ESTUDO-ARRANJO-FX-DESENHO-20261025.md` (25/10) · `acervo/pesquisas/tutoriais/MELODIA.md` (s.d.)

## 5. "A faixa esta reta e parada. Quando entra camada nova, quanto dura cada estado, o que subtraio e quando?"

**Responde:** `reguas/regua-arranjo-e-transicao.md` §1–2
- 1 track nova a cada ~16 bars; elemento entra e fica (mediana 48 bars); refresh de versao a cada ~60 bars com stitch-ponte (§1.4–1.7).
- Fundacao imortal: kick e baixo correm do primeiro ao ultimo compasso; energia se administra removendo camadas de cima, nunca a base (§1.5).
- Regua de 8 bars: 1–8 base + hook, 9–16 camada forte, 17–24 remove algo, 25–32 fill, 33 mudanca de secao (§1.10).
- Turnover saudavel: 3–4 compassos por estado de camada e 2,8–6,7 mudancas/min; algo audivel muda a cada ~15 s (§2.15–2.16).
- Variar sem compor novo: mesmo MIDI com outro timbre ou ritmo vira secao diferente que ainda encaixa (§2.21).

**Aprofunda:** `acervo/pesquisas/refs-artistas/PROFESSOR-ARRANJO-UNDERTOW-2026-09-08.md` (08/09) · `acervo/knowledge-base/arranjo-anti-estase.md` (08/09)

## 6. "O que ponho na fronteira do drop — riser tonal, succao, silencio? E qual a dose certa de vacuo?"

**Responde:** `reguas/regua-arranjo-e-transicao.md` §3–5
- Um dono por fronteira: um gesto por corte; se ja existe reverse/crash/sweep, substitui em vez de somar (§3.27).
- Usar o proprio alvo como subida (invertido com fade); FX de transicao fora do grave (HP ≥120 Hz); master conta a historia: 1–2 dB de GR no drop, nao 6 (§3.28, 3.30, 3.34).
- Vacuo: silencio total reservado a 1–3 momentos por faixa, quase sempre no ultimo terco; dose da familia 0,11–0,80 gaps/min; puxar o sub nos 1–2 bars finais antes do drop (§4.37–4.39).
- Riser/downlifter em pares; riser de referencia em 8 bars e 3 camadas (tonal 0 dB + noise −12/−15 + ritmica −6/−9); sweep de ruido filtrado como alternativa (§5.44–5.47).
- **EM DISPUTA** (§6 D3): riser tonal de 8 compassos e conteudo normal do genero × diretriz que o aposenta — a regua registra, nao decide.

**Aprofunda:** `acervo/pesquisas/ESTUDO-ARRANJO-FX-DESENHO-20261025.md` (25/10) · `acervo/pesquisas/tutoriais/TRANSICOES.md` (27/10)

## 7. "Como desenho o timbre no Serum 2 — camadas, envelope, distorcao — e onde entra madeira organica e granular sem virar enfeite?"

**Responde:** `reguas/regua-texturas-e-sounddesign.md`
- Economia por funcao (pack Drift, 152 presets): baixo 2 camadas/2 FX · lead e pluck 3 camadas/5 FX · pad 2 camadas; resolver o timbre dentro do patch (§B, itens 7–8).
- ENV1 de referencia: attack 0,5 ms · decay 1,0 s · sustain 0,79 · release 76 ms; distorcao identica antes e depois do filtro; phase distortion como sujeira controlada (§B, itens 9–11).
- Madeira por funcao: acento/resposta em one-shots 0,2–1,0 s · topo percussivo continuo em loops · madeira melodica (marimba/woodwinds) · cama granular (~1,5 s por grao); reafinar o pack para a tonica e tratar madeira como lado secundario (§C, itens 18–22).
- Granular por funcao: grao de drone 150–300 ms, resposta percussiva 60–120 ms, madeira 100–160 ms; cama nasce de fonte acustica e entra/sai por secao (§D, itens 23–28).
- Espaco: Side real so acima de ~150–250 Hz; mono ≤120 Hz (§F, itens 46–47).
- **EM DISPUTA** (§H): HPF do drone 90 × 160 Hz; topo percussivo continuo × G16/G17/G18 provisorias.

**Aprofunda:** `acervo/pesquisas/cursos/PRESETS-SERUM-20261025.md` (25/10) · `acervo/pesquisas/AUDITORIA-PACKS-ORGANICOS-20261029.md` (29/10)

## 8. "Que numeros miro no master — LUFS, true peak, crest, mono do low-end — e como meco sem me enganar?"

**Responde:** `reguas/regua-mixagem-e-master.md`
- Regua da familia masterizada: LUFS-I −8,7 (−11,7 a −6,9) · crest 11,1 dB (9,2 a 15,7) · sub 47,5% · bass 37,1% (§1.5).
- Medir em taxa nativa e estereo; limiter de escuta ligado no master contamina qualquer numero (§1.1, §1.7).
- Gain staging: canais e grupos em 0,0 dB; low-cut do master LC12 @ 18–20 Hz (§2.2, §2.7).
- Dinamica: Glue com GR maximo 1,5–2,0 dB; um limiter so com 2–3 dB de GR; distribuir a reducao com clipper antes (§3.1–3.3).
- Low-end: monoizar abaixo de 100–120 Hz; uma camada so de BassMono (§4.1–4.2).
- Alvos por destino: streaming ≤ −1,0 dBTP com Spotify −14 LUFS; clube −8 a −6 LUFS (§5.1–5.2).
- **EM DISPUTA** (§6.1): tres leituras coexistem de true peak (−1,0 / −0,3 / exigencia de −2) — investigar a cadeia antes de cravar numero.

**Aprofunda:** `acervo/pesquisas/estudo_master_20261017.md` (17/10) · `acervo/pesquisas/estudo_mix_20261017.md` (17/10) · `acervo/diagnosticos/REGUA-DE-AUDIO-20261025.md` (25/10)

## 9. "Como o Gazolla, o Kaled, a Akari e a AIO fazem groove, build e drop — com numeros, nao de cabeca?"

**Responde:** `reguas/regua-referencias-artistas.md`
- Consenso transversal: 127–132 BPM; grave 20–120 Hz = 56–78% da energia; estrutura quantizada em 8 compassos; primeiro impacto ≤0:35 (§1.1, 1.2, 1.8, 1.9).
- Swing no topo, nao no kick: hats adiantados 13–27 ms com kick/bass quantizados (§1.7).
- Kick com cauda tonal (decay −20 dB em 140–200 ms) e master da cena −7 a −6 LUFS com clipper antes do limiter (§1.6, §1.11).
- Fichas por artista (§2): Gazolla — grid cirurgico, drops por degrau (+52 a +62 dB), pre-drop com micro-cuts e roll de kick; Kaled — camada organica permanente a ~4 clicks/s, build sem riser tonal; Yao — pleno com todas as camadas a 9–12 onsets/s, rolling "KBBB"; Akari — rolling 16ths planos 19–20 onsets/compasso sem pausa; AIO — dinamica por filtro e vacuo filtrado pre-drop; Discretion — corte de downbeat a cada 16 compassos.

**Aprofunda:** `acervo/pesquisas/refs-artistas/ANALISE-COMPARATIVA-REFS-2026-09-08.md` (08/09) · `acervo/pesquisas/refs-artistas/AUDIOMETRIA-FISICA-PSYTECH-2026-09-09.md` (09/09)

## 10. "Um elemento sumiu, o numero nao bate com o ouvido, o timbre mudou sozinho — por onde comeco o diagnostico?"

**Responde:** `casos/cicatrizes-como-caso.md`
- Check de 60 segundos em 5 passos, sem pular: Alvo → Existencia (mute de grupo/canal/clipe, janela) → Sinal (device, sidechain, fader × automacao) → Numero (render com hash, unidade) → Mudanca pequena e reversivel (§1).
- 86 casos reais em 6 familias, cada um com sintoma → causa medida → correcao que funcionou: silencio/sinal (§3), preset/timbre/clipe (§4), medicao e grade (§5), grave (§6), arranjo e orquestra (§7), pedido e processo (§8).
- Padrao recorrente: o estado real nao era o que o documento/nome dizia; o numero era de outro objeto ou unidade; a correcao atacou a camada errada (§2).
- Regra das duas falhas: se a mesma correcao falhar duas vezes, a premissa esta errada — nao a dose.

**Aprofunda:** `acervo/raiz/CICATRIZES-20261030.md` (30/10) — corpus original das licoes, com custo documentado por caso

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

*Fontes consultadas (caminho + data): as 6 reguas de `plugins/psytech-lab/skills/psytech-lab/reguas/` (destiladas 01/11/2026) · `plugins/psytech-lab/skills/psytech-lab/casos/cicatrizes-como-caso.md` (casos reescritos, lido 01/11/2026) · `acervo/raiz/CICATRIZES-20261030.md` e `acervo/raiz/MAPA-DE-LACUNAS-E-CONFLITOS-20261030.md` (30/10, lidos 01/11/2026) · varredura do inventario de `acervo/` (01/11/2026). Consulta ao Live: nenhuma — tarefa de documentacao, sem mutacao.*
