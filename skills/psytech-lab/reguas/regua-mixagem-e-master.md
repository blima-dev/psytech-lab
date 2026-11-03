# Regua: mixagem e master

**Headroom · Dinamica · Low-end mono · Medicao e unidades**

> Destilada do acervo psytech-lab (limpo, sem vestigios do autor) contra o mapa de conflitos. Contraste com o set do autor mora em "Casos", nao na regua.
> **Fontes:**
> `acervo/pesquisas/estudo_mix_20261017.md`
> `acervo/pesquisas/estudo_master_20261017.md`
> `acervo/diagnosticos/REGUA-DE-AUDIO-20261025.md`
> `acervo/knowledge-base/My_Complete_Psytrance_Mixing_Method_2026.md`
> `MAPA-DE-LACUNAS-E-CONFLITOS-20261030.md` (so para os pontos EM DISPUTA)

## 1. Medicao e unidades

- **1.1.** Mede em taxa nativa do arquivo e em estereo; ferramenta que reamostre declara o limite em voz alta.
- **1.2.** LUFS-I e true peak saem do ebur128 (`ffmpeg -filter_complex ebur128=peak=true`); crest = pico − RMS; bandas de energia e side/mid na janela de 60 s de maior RMS, com a janela declarada.
- **1.3.** No `.als`, `Mixer/Speaker Manual=true` significa pista **ATIVA**; audite com `active` e `mute` separados: um leitor antigo invertia esse campo em 186 sets.
- **1.4.** Conte audibilidade, nao clipe: a medida honesta contou bateria audivel = 5 pistas, contra 18+ infladas por contagem de clip.
- **1.5.** Regua da familia psytech (mediana; min–max das 15 referencias masterizadas): LUFS-I −8,7 (−11,7 a −6,9) · TP +2,3 dBTP (+0,6 a +6,3) · crest 11,1 dB (9,2 a 15,7) · sub 47,5% (13,5 a 59,0) · bass 37,1% (22,8 a 52,7) · low-mid 9,4% (4,9 a 22,3) · mid 2,7% (0,9 a 7,9) · presence 1,2% (0,4 a 8,3) · air 1,6% (0,3 a 6,9) · side/mid −14,8 dB (−24,6 a −10,9) · side/mid do grave −32,7 dB (−48,6 a −12,9).
- **1.6.** LUFS/TP de referencias masterizadas medem estagio de masterizacao; as partes comparaveis com render cru sao bandas de energia e estereo.
- **1.7.** Meca com a cadeia de master documentada: limiter de escuta ligado no master contamina qualquer numero de LUFS/TP.

## 2. Headroom e gain staging

- **2.1.** Mixa top-down: comece pelo master, depois grupos, canais individuais por ultimo, com a excecao do grupo kick+bass, que se acerta canal a canal.
- **2.2.** Base de ganho: grupos e canais cravados em 0,0 dB; automacao de `Mixer.Volume` que sobe grupo a +3/+4 dB rouba o headroom que o master precisa.
- **2.3.** Boost de EQ em canal de mix fica em +1,5 a +2,5 dB; no caso medido, boosts de +10 a +15,6 dB em 130–700 Hz em 6+ canais entupiam o master.
- **2.4.** Cada acao de mix tem custo de fase; com o minimo de acoes o mix chega natural e rapido: o que ja foi cortado no grupo fica cortado, sem repetir EQ no canal.
- **2.5.** A cadeia mantem ganho plano entre estagios: leia o medidor pos-plugin a cada etapa e compense o output quando o processamento subir o volume.
- **2.6.** Auto Filter com Resonance > 50% gera picos estreitos de +6 a +12 dB; HP/LP com Dry/Wet < 100% vira comb filtering (filtro parcial a 35% em 9+ canais do caso).
- **2.7.** Low-cut do master em LC12 @ 18–20 Hz (Q ~0,6) preserva a oitava sub 25–40 Hz; o LC48 @ 25,2 Hz medido no caso matava essa oitava e girava fase.
- **2.8.** Um high-shelf por regiao de topo no master, em +1,5 a +2,0 dB; tres shelves em serie somavam +15 dB acima de 11 kHz e empurravam Glue e limiter.
- **2.9.** Placa do metodo no master: EQ suave @ 20 Hz (reduz DC offset), Glue com EQ no detector para nao bombear com o sub, clipper suave (modo digital) com macro drive↔output compensado, medidor TP+LUFS apos os plugins, Utility para teste mono e referencia nivelada.
- **2.10.** Caudas longas vivem em retornos (o metodo usa tres: sala curta pre-EQ, espaco medio, cauda ~6 s com damping) e nao em insert no canal; 9 reverbs insert de 3,09 a 11,76 s vazavam no caso.
- **2.11.** Ancore o fader do kick (~−10 dB no metodo) antes de encaixar o baixo em fase com ele.

## 3. Dinamica (Glue, limiter, crest)

- **3.1.** Glue como cola: threshold com GR maximo 1,5–2,0 dB, attack 30 ms, release 0,1 s (ou Auto), Dry/Wet 60–65% (paralelo) e sidechain-EQ HP 150–200 Hz para o detector desconsiderar o sub.
- **3.2.** Um unico limiter trabalha com ate 2–3 dB de GR; acima disso perde transiente e estreita a imagem com link estereo em 100%.
- **3.3.** Para loudness de pista, distribua a reducao: clipper/soft-clip antes do limiter, ou dois limiters em serie com ~1 dB de GR cada.
- **3.4.** Limiter: AutoRelease ligado (40–50 ms) e Stereo Link 60–65%, para o kick nao fechar os Sides nem segurar a atenuacao por uma semicolcheia (117 ms a 128 BPM).
- **3.5.** Alvos de dinamica pos-ajuste do estudo (`INFERENCIA` do estudo): LRA 9–11,5 LU e crest 8–9,5 dB nos drops (clube); LRA 10,5–12,5 LU e crest 9–10,5 dB (streaming).
- **3.6.** Crest da familia: 11,1 dB de mediana (9,2 a 15,7).
- **3.7.** Nao existe "o master do genero": o continuum medido nas escolas vai de master = trim de −3,33 dB (uma escola) a dois limiters em serie (outra); a mediana de FX por pista e 2,88, e 5+ e extremo maximalista.

## 4. Low-end mono e kick × sub

- **4.1.** Monoize o sub: subs de PA de clube reproduzem <80–120 Hz em mono e conteudo estereo nessa regiao cancela em fase; a pratica padrao e monoizar abaixo de 100–120 Hz.
- **4.2.** Uma camada so de BassMono: quatro cascatas de minimum-phase (canais 120–140 Hz → grupos 120/140/144 Hz → master 121,3 Hz) estreitavam a imagem ate 1–5 kHz; a alternativa e side LC12 @ 110–115 Hz no EQ M/S do master.
- **4.3.** O sub ocupa 32–45 Hz e o corpo do kick 48–65 Hz; em C# frigio a fundamental sub e C#0 Ableton = MIDI 25 = 34,65 Hz, com 2º harmonico em 69,30 Hz.
- **4.4.** Kick e sub dividem o grave com ducking: volume-shaping (LFO 1/4 com fase travada) ou compressor ultrarrapido (attack <1 ms, release 120–180 ms); band-splitting aplica o duck so no grave e preserva o resto do baixo.
- **4.5.** Todo elemento que colide com o ataque do kick carrega sidechain, e caudas de reverb/delay duckam contra o sinal dry ou o kick.
- **4.6.** O kick afina em grau consonante da tonalidade: a familia de 53 kicks mede fundamental mediana 49,1 Hz (25,6–68,0) com decay −20 dB de 0,19 s (0,08–0,39); audite por FFT, porque o nome do arquivo mente.
- **4.7.** Mono-compatibilidade medida: correlacao L/R 200–2k Hz alvo 0,38–0,52 (abertura 0,35–0,55), graves 20–120 Hz ≥ +0,95, faixa de seguranca geral +0,5..+1,0.
- **4.8.** M/S sutil no master: movimentos abaixo de ~4 dB com Q largo; lama dos sides sai em 240–480 Hz (−1,5 a −3 dB), corpo abre nos sides em ~620 Hz (+2,2 a +2,5 dB), ar nos sides com shelf @ ~11,5 kHz (+2,5 a +3 dB).
- **4.9.** Na referencia psytrance, bass e agudos aparecem em volume aproximado no espectro; use a referencia nivelada para calibrar essa balanca.

## 5. Alvos por destino (master)

- **5.1.** Streaming: teto ≤ −1,0 dBTP com limiter true peak (a transcodificacao Ogg/AAC cria inter-sample peaks de +1 a +3 dB); uma variante usa clipper @ −1 dBFS + TP limiter @ −0,3 dBTP. Normalizacao: Spotify −14, Apple Music −16, Deezer −15, Amazon/YouTube/Tidal −14 LUFS.
- **5.2.** Beatport/clube: sem normalizacao de loudness; alvos do guia: techno −8 a −6 LUFS, trance −9 a −7, melodic house −11 a −8; TP −1 dBTP; crest 6–9 dB.
- **5.3.** Ao masterizar contra a familia: mire −9 a −8 LUFS com teto proprio da secao 6; os +2,3 dBTP de mediana sao das referencias clipadas.

## 6. EM DISPUTA (conflitos abertos no mapa; nao resolver aqui)

- **6.1.** **Teto de True Peak (tres leituras coexistem):** (a) ≤ −1,0 dBTP streaming / −0,8 hibrido / −0,5 clube; (b) −0,3 dBTP ao masterizar; (c) o mapa marca a masterizacao como lacuna critica, com o estado atual em −0,6 dBTP contra uma exigencia citada de "Spotify −2 dBTP". O mapa manda investigar a cadeia (duplo limiter) antes de declarar numero de master.
- **6.2.** **Estado do low-end no Set, duas leituras:** o plano relata Kickstart 2 ligado nos SUBS A/B e SUB NOVO mudo; a reconciliacao relata Kickstart desligado e SUB NOVO ativo. Decisao pendente de read-back no Live via `live_run_code`, sem escolher versao.

## 7. Casos (contraste com o set do autor; referencia, nao regua)

- **7.1.** Render analisado (janela 80–140 s): LUFS −10,9, TP −0,6, crest 10,5, bass 36,9% (identico a familia), sub −3,9 pp, low-mid +4,3 pp, air −1,1 pp (≈3× menos), side/mid +0,7 dB, grave 9 dB mais mono que a mediana, o desejado com canon low-end mono.
- **7.2.** Correcao do baseline: os numeros "ar 0,5% / low-mid 13,7%" vinham de render anterior; no estado novo, Drop 1 mede air 1,0% / low-mid 23,9% / bass 22,6% e Drop 2 air 1,7% / low-mid 30,5% / bass 15,5%, e o gap real migrou para low-mid/bass.
- **7.3.** Kick principal mediu 52,5 Hz ≈ G#1 (+20 cents, 5ª justa) e o alternativo 46,4 Hz ≈ F#1 (+81 cents, 4ª justa), ambos consonantes com C#; o rack se intitulava "Organic 48Hz".
- **7.4.** A escola de referencia Tim mede 0,71/1,04/0,78 s de drum room, sala curta para bateria em retorno, contra reverbs insert de 3,09–11,76 s no caso.
- **7.5.** Acoes propostas a partir do gap do render: high shelf 8–12 kHz (+1,5 a +2 dB) no master ou no bus de madeiras e corte 120–400 Hz (−1 a −2 dB) nos buses que acumulam low-mid, agindo acima de 6 kHz; bass e estereo ja estavam na regua da familia.
