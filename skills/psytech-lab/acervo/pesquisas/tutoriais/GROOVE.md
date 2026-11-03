# Groove — tutoriais traduzidos

**Data do levantamento:** 27/10/2026 · **frente:** groove (9 mapas) · **bolso de referência:** a faixa "Shadows", trecho 1:30–3:00 — referência de ouvido, não grade para copiar.

## Use quando

For propor ou mexer em síncope, hats/shaker, ghost notes, microtiming, swing, percussão de resposta, stab de resposta ou hipnose do motor (primeiros 64 compassos). **Não use** para decidir kick/sub/baixo: essas funções têm documento próprio (`PRESSAO-GRAVE.md`) e aqui só aparecem como limite.

## Regras

1. **proteger o bolso .27/.77** — o bolso de referência é microtiming (uma camada de sub em .27 e o baixo em .50/.77; +0,02 beat ≈ 9,4 ms) e não se mexe. A síncope dos tutoriais é grade macro: entra só em madeira, percussão de resposta, stab e modulação de filtro — nunca em kick, sub, baixo/rolling ou na camada que carrega o deslocamento (`iWOPUHKbJjI`, `ejNHFdtYrw0`, `cVtnGIFGYss`).
2. **troca, não soma** — a hipnose vem de trocar, omitir e microvariar, não de camada contínua nova. A densidade de transientes já está no teto medido: cada evento novo remove um existente (`A6XjjwGUkA8`, `VSYCY__WVQ8`, `ejNHFdtYrw0`).
3. **um dono por fronteira** — uma mudança por bloco de 8 compassos, 2–3 micro-gestos, não 6–8; efeito de transição é evento mutado depois, não camada (`VSYCY__WVQ8`).
4. **tempo e velocity antes de EQ** — groove se faz com posição, velocity e LFO. Hat/shaker não consertam o déficit de médio, e saturação/EQ "para combinar" com groove é o caminho do brilho metálico (`cVtnGIFGYss`, `A6XjjwGUkA8`, `G4Tsj5or6A8`).
5. **provisório não é lei** — o corte uníssono de 8 compassos e o shaker contínuo em 16avos são diretrizes do projeto de referência ainda em aberto. Testar polimetria com o corte ligado **e** desligado; até decisão, o topo contínuo continua valendo.

## Receitas traduzidas

| Tutorial | Receita traduzida | Onde / valor de partida |
|---|---|---|
| `iWOPUHKbJjI` — síncope sem nota nova | Madeira ou percussão de resposta tipo bongo: mover **uma** resposta por frase de 16º para 3/16 (colcheia pontuada = 0,75 beat), mesmas notas e mesmo timbre. Baixo: LFO 1/8D ou 1/8T no filtro de uma **via paralela HP ≥300 Hz**, nota única, LFO mono. Shaker: polimetria 7/16 ou 13/16 no loop do clipe, sem nota nova. | Resposta em c9–16 e c25–32; offsets .27/.77 intactos. LFO ≈2,84 Hz (1/8D) e ≈6,4 Hz (1/8T) a 128 BPM (aritmética do mapa). Prova: 06:59 ("single note… filter outside the beat"), 07:39–07:53 (polimetria). |
| `ejNHFdtYrw0` — humanização | Claps/respostas: micro-delay +15/−10 ms, **uma direção por bloco** (atrás do kick = relaxed; à frente = rushed). Shaker: random position 1–8 ms, velocity ±10–15, pitch random só para baixo. Round robin de 3 para não metralhar. Madeira: fatiar loop gravado no Simpler (Slice) e montar o padrão com fatias diferentes. | Só hats/shaker/resposta/madeira; no Live o delay é **por track** — nota individual exige nudge. Prova: 00:02:11–00:02:22 (dragged × rushed), 00:09:11–00:09:20 (round robin ímpar desalinha, par realinha). |
| `xuHSPaCHjvo` — peso por camada | Camada média do baixo com Env2 curto (0,08–0,12 s — valor do estudo de origem, não do vídeo). Rumble **opcional** em return novo: send do kick → Hybrid Reverb 100% wet (150–300 ms) → HP 120 → LP 300–500 Q≤1,2 → compressor com sidechain do kick → −18/−24 dB; retorno mono <150 Hz. | Não copiar 3/16 com feedback 50% (00:01:53): a 1ª repetição cai 9,4 ms antes do baixo. O próprio mapa lembra que rumble é base hard techno — descartar se o motor soar tech house. Detalhe de grave em `PRESSAO-GRAVE.md`. |
| `C3x8o9Krfc0` — stab de resposta | Saw posição 0%, band pass 24 com drive 5–6 dB, centro **250–400 Hz** (o vídeo usa ~100 Hz), res ~50, Env2 amount 25, amp sem sustain e release 600 ms; Utility Bass Mono 120; delay/reverb em send com HP ~300. | Centro deslocado para o miolo; cauda não pode cair sobre os offsets .27/.77 nem no contratempo 0,5 do open hat (04:05). Prova: 01:09 (100 Hz), 01:19 (res 50), 02:17 (env rápido). |
| `A6XjjwGUkA8` — ruído como hat/resposta | Clique do início de um one-shot = hat fechado (5–15 ms). Recorte 100–400 ms com LFO no attack/decay por nota. HP 1 kHz em hat, ≥300 Hz em textura. Corpus tube afinado na tônica/quinta/quarta de referência. Auto Filter com pico em 700–900 Hz. LP 7–8 kHz no hat de ruído. Glue keyed no kick. | Substituir evento existente; pico não estaciona em 2–4 kHz; ruído nunca em sub/baixo. Prova: 02:49 (corta até 1 kHz + Corpus), 03:47–03:54 (≈800 Hz), 03:34 (LFO no attack). |
| `G4Tsj5or6A8` — camadas e velocity | Hats/shaker: velocity desenhada é o groove; Simpler com LFO lento em volume/pan; ressonância estreita em vez de boost; percussão média curta com velocity randomizada para dar corpo a 300–1.200 Hz; bus só de bateria, tone escurecido e level match. | Não copiar afinação de kick nem boost 55 Hz de tutorial. Ghost/rumble sempre filtrados e fora dos respiros; sem ghost kick novo. Prova: 00:06:46–00:06:55 ("the velocities are responsible for the swing"), 00:08:31–00:08:49 (LFO do Simpler). |
| `VSYCY__WVQ8` — portas de 8 e falso release | c33: sair com o open hat. c41: voltar **trocado** (outro sample do mesmo padrão). c49: acento de open hat nos offsets do bolso. c57: trocar de novo ou omitir 1 tempo a cada 2 compassos. Falso release c33–c40: só open hat e stab saem, chão idêntico. Madeira entra no compasso 5 de cada bloco de 8 (cola das duas metades). Banco de 4–6 eventos band-limited 300 Hz–6 kHz, um por fronteira, 2–4 compassos e mutado. | Shaker existente intocado; não copiar 16avos contínuos nem o tempo do autor (134 BPM). Prova: 00:06:59 (falso release), 00:02:18 (cola de 4 compassos), 00:04:45–00:05:00 (troca de open hat). |
| `cVtnGIFGYss` — Groove Pool | Swing de 16ª só em hats/shaker/resposta: Amount 10–20% (partida do estudo; o vídeo não dá número) e Random pequeno. Separar timing de velocity. Printar 2–3 variações e alternar por bloco de 8. | Kick/sub/rolling fora. Procedimento: 00:03:11 (arrastar o groove), 00:04:08 ("it only applies to timing"), 00:08:15 (printar). No Live 12 o recurso aparece como groove files. |
| `aK2tKYe8yCI` — ghost e 5/16 | Ghost notes realmente baixas nos hats ("splashing"). Hat fechado em 5 semicolcheias com curva de dinâmica. Chance por nota nas respostas. Madeira em loops de 2–4 compassos com Shifter/notch lento. Echo+reverb no hat só a cada 2 compassos. | 5/16 só na resposta, nunca nos offsets do bolso. Não copiar afinação de kick nem de tom do vídeo. Não resolver 1,2–4 kHz subindo hat. Prova: 00:15:48, 00:16:54, 00:20:10. |

**Preservar ao aplicar**

- Sub e baixo: posições, durações e fontes atuais do bolso de referência; nada de síncope, swing, micro-delay, reverb ou camada duplicada neles.
- Kick 4x4 preservando os respiros já escritos no arranjo de referência: 0:44–0:45, 0:59,5–1:00, 1:29,5, 1:44,1–1:45 e 1:59,5.
- Shaker no nível medido do projeto de referência; o déficit de médio não se corrige subindo topo.
- Camadas desligadas no projeto de referência (meio/ruído) não religar para "subir energia".
- Uma direção de micro-timing por bloco — nunca atrasado e adiantado juntos (`ejNHFdtYrw0`).

## Conflitos e cautelas

| Tutorial | O que o vídeo faz | Como adaptar |
|---|---|---|
| `G4Tsj5or6A8` — kick em 3 camadas, boost de 55 Hz, rumble/ghost desde bars 1–16 | Afinação e densidade próprias do vídeo | O kick de referência é G#0 (~52,4 Hz) — medir antes de retunar, nunca transplantar; boost ~51 Hz só se 40–55 Hz estiver baixo; rumble e ghost mudos nos respiros escritos (c.24 e c.32 dentro do motor, c.44/48/56 além de 2:00). |
| `aK2tKYe8yCI` — kick em C#, tom em G1, 5/16 no hat | Afinação do vídeo | Kick na fundamental medida (G#0 na referência); tom em G#1/A1; 5/16 só na resposta. |
| `iWOPUHKbJjI` — polimetria 7/16 e 13/16 no shaker; 7/8, 13/16, 15/16 na atmosfera | Polimetria rotativa | Testar com o corte de 8 compassos ligado/desligado (diretriz provisória do projeto de referência); só em A/B. |
| `cVtnGIFGYss` — swing impresso em blocos de 8 | Swing em percussão | Swing só na percussão e em Amount baixo; as variações precisam respeitar o corte de 8 se ele estiver ativo. A legalidade do shaker contínuo em 16avos é decisão em aberto. |
| `xuHSPaCHjvo` — rumble contínuo sobre o kick | Rumble como cama | Rumble só onde há kick, HP 120, mono, fora dos respiros; nunca somar sub; medir 55–75 Hz antes/depois. |
| `A6XjjwGUkA8` — textura "sem EQ"; pico ressonante | Ruído como camada | HP obrigatório (1 kHz hat, ≥300 Hz textura); pico em 700–900 Hz; low-end mono; ruído não sobe o topo. |
| `VSYCY__WVQ8` — 6–8 efeitos de transição | Densidade de FX | 2–3 micro-gestos, um dono por fronteira, evento mutado depois; sem riser/snare roll; cauda só em return. |
| `ejNHFdtYrw0` — drum bus com saturação em todos os drums | Bus saturado | Kick/sub fora do bus (ou bus que preserve mono); drive baixo e conferência auditiva de brilho. |
| `C3x8o9Krfc0` — centro em 100 Hz, low shelf 300 Hz, high shelf ~1 kHz | EQ do vídeo | Centro em 250–400 Hz; Bass Mono 120; sem high shelf amplo; cauda fora dos offsets do bolso. |

## A/B

**A/B 1 — portas de 8 e falso release (8 compassos, c33–c40 x c41–c48).** Sair com o open hat em c33, voltar trocado em c41; no bloco c33–c40 retirar também o stab, mantendo kick, sub, baixo, hats fechados e percussão idênticos. **Critério:** posições de onset do bolso de referência idênticas antes/depois (diferença 0 ms); energia e correlação em 20–120 Hz sem mudança mensurável; 5–12 kHz sem subir; contagem de eventos igual ou menor. Reprovado se o chão perder peso, se o topo subir ou se algum onset se mover.

**A/B 2 — síncope macro na resposta (8 compassos, c9–16).** Mover uma resposta por frase de 16º para 3/16 (0,75 beat), mesmas notas e timbre, sem evento novo. **Critério:** contagem de eventos idêntica; onsets da camada de resposta em 3/16; onsets de sub/baixo/shaker inalterados; 20–120 Hz sem mudança; 300–1.200 e 1.200–4.000 Hz sem cair. Reprovado se o bolso .27/.77 se mover ou se a frase ganhar movimento só por volume. O julgamento artístico é do produtor; estes números só protegem fase, mono e densidade.

## Evidência

Os mapas completos por vídeo (um por ID, com timestamps) não acompanham este pacote; os IDs listados identificam cada fonte. Proveniência: leitura de legenda automática ou ASR local.

## NÃO VERIFICADO / pendências

- **Nenhum A/B foi executado**; nenhum áudio foi medido; nada foi aplicado num projeto real.
- **Shaker contínuo em 16avos e corte uníssono de 8 compassos em aberto** — bloqueiam o desenho de shaker e a polimetria até decisão no projeto de referência.
- **Fundamental do kick** — as receitas que tocam kick estão reduzidas a guardrails; sem medir a fundamental real no projeto de destino, não há retune nem boost de fundamental.
- **`VSYCY__WVQ8`** — fala obtida por ASR local, não legenda; posições, nomes de camada e contagens são reconstrução, não o projeto de Rene Wise.
- **`iWOPUHKbJjI`** — rótulos exatos de dotted/triplet no Auto Filter do Live 12 não confirmados; usar os Hz equivalentes (2,84 / 6,4 Hz).
- **`A6XjjwGUkA8`** — Corpus, Auto Filter, Phaser, Amp e Glue no Live não conferidos nesta sessão; LFO→attack no Sampler não verificado (no Serum o destino `env0.attack` existe no schema).
- **`aK2tKYe8yCI` e `G4Tsj5or6A8`** — BPM (135), tonalidade (F#/G/C#) e valores de kick/tom são do vídeo e não se traduzem; só a regra vale.
- **Nível de bolso** — o quanto o 3/16 ou o Amount de swing "cola" no bolso de referência não foi medido; só A/B de ouvido resolve.
