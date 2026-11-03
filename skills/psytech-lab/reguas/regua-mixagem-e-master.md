# Régua: mixagem e master

**Headroom · Dinâmica · Low-end mono · Medição e unidades**

> Destilada do acervo psytech-lab (limpo, sem vestígios do autor) contra o mapa de conflitos. Contraste com o set do autor mora em "Casos", não na régua.
> **Fontes:**
> `acervo/pesquisas/estudo_mix_20261017.md`
> `acervo/pesquisas/estudo_master_20261017.md`
> `acervo/diagnosticos/REGUA-DE-AUDIO-20261025.md`
> `acervo/knowledge-base/My_Complete_Psytrance_Mixing_Method_2026.md`
> `MAPA-DE-LACUNAS-E-CONFLITOS-20261030.md` (só para os pontos EM DISPUTA)

## 1. Medição e unidades

- **1.1.** Mede em taxa nativa do arquivo e em estéreo; ferramenta que reamostre declara o limite em voz alta.
- **1.2.** LUFS-I e true peak saem do ebur128 (`ffmpeg -filter_complex ebur128=peak=true`); crest = pico − RMS; bandas de energia e side/mid na janela de 60 s de maior RMS, com a janela declarada.
- **1.3.** No `.als`, `Mixer/Speaker Manual=true` significa pista **ATIVA**; audite com `active` e `mute` separados: um leitor antigo invertia esse campo em 186 sets.
- **1.4.** Conte audibilidade, não clipe: a medida honesta contou bateria audível = 5 pistas, contra 18+ infladas por contagem de clip.
- **1.5.** Régua da família psytech (mediana; min–max das 15 referências masterizadas): LUFS-I −8,7 (−11,7 a −6,9) · TP +2,3 dBTP (+0,6 a +6,3) · crest 11,1 dB (9,2 a 15,7) · sub 47,5% (13,5 a 59,0) · bass 37,1% (22,8 a 52,7) · low-mid 9,4% (4,9 a 22,3) · mid 2,7% (0,9 a 7,9) · presence 1,2% (0,4 a 8,3) · air 1,6% (0,3 a 6,9) · side/mid −14,8 dB (−24,6 a −10,9) · side/mid do grave −32,7 dB (−48,6 a −12,9).
- **1.6.** LUFS/TP de referências masterizadas medem estágio de masterização; as partes comparáveis com render cru são bandas de energia e estéreo.
- **1.7.** Meça com a cadeia de master documentada: limiter de escuta ligado no master contamina qualquer número de LUFS/TP.

## 2. Headroom e gain staging

- **2.1.** Mixa top-down: comece pelo master, depois grupos, canais individuais por último, com a exceção do grupo kick+bass, que se acerta canal a canal.
- **2.2.** Base de ganho: grupos e canais cravados em 0,0 dB; automação de `Mixer.Volume` que sobe grupo a +3/+4 dB rouba o headroom que o master precisa.
- **2.3.** Boost de EQ em canal de mix fica em +1,5 a +2,5 dB; no caso medido, boosts de +10 a +15,6 dB em 130–700 Hz em 6+ canais entupiam o master.
- **2.4.** Cada ação de mix tem custo de fase; com o mínimo de ações o mix chega natural e rápido: o que já foi cortado no grupo fica cortado, sem repetir EQ no canal.
- **2.5.** A cadeia mantém ganho plano entre estágios: leia o medidor pós-plugin a cada etapa e compense o output quando o processamento subir o volume.
- **2.6.** Auto Filter com Resonance > 50% gera picos estreitos de +6 a +12 dB; HP/LP com Dry/Wet < 100% vira comb filtering (filtro parcial a 35% em 9+ canais do caso).
- **2.7.** Low-cut do master em LC12 @ 18–20 Hz (Q ~0,6) preserva a oitava sub 25–40 Hz; o LC48 @ 25,2 Hz medido no caso matava essa oitava e girava fase.
- **2.8.** Um high-shelf por região de topo no master, em +1,5 a +2,0 dB; três shelves em série somavam +15 dB acima de 11 kHz e empurravam Glue e limiter.
- **2.9.** Placa do método no master: EQ suave @ 20 Hz (reduz DC offset), Glue com EQ no detector para não bombear com o sub, clipper suave (modo digital) com macro drive↔output compensado, medidor TP+LUFS após os plugins, Utility para teste mono e referência nivelada.
- **2.10.** Caudas longas vivem em retornos (o método usa três: sala curta pré-EQ, espaço médio, cauda ~6 s com damping) e não em insert no canal; 9 reverbs insert de 3,09 a 11,76 s vazavam no caso.
- **2.11.** Ancore o fader do kick (~−10 dB no método) antes de encaixar o baixo em fase com ele.

## 3. Dinâmica (Glue, limiter, crest)

- **3.1.** Glue como cola: threshold com GR máximo 1,5–2,0 dB, attack 30 ms, release 0,1 s (ou Auto), Dry/Wet 60–65% (paralelo) e sidechain-EQ HP 150–200 Hz para o detector desconsiderar o sub.
- **3.2.** Um único limiter trabalha com até 2–3 dB de GR; acima disso perde transiente e estreita a imagem com link estéreo em 100%.
- **3.3.** Para loudness de pista, distribua a redução: clipper/soft-clip antes do limiter, ou dois limiters em série com ~1 dB de GR cada.
- **3.4.** Limiter: AutoRelease ligado (40–50 ms) e Stereo Link 60–65%, para o kick não fechar os Sides nem segurar a atenuação por uma semicolcheia (117 ms a 128 BPM).
- **3.5.** Alvos de dinâmica pós-ajuste do estudo (`INFERÊNCIA` do estudo): LRA 9–11,5 LU e crest 8–9,5 dB nos drops (clube); LRA 10,5–12,5 LU e crest 9–10,5 dB (streaming).
- **3.6.** Crest da família: 11,1 dB de mediana (9,2 a 15,7).
- **3.7.** Não existe "o master do gênero": o continuum medido nas escolas vai de master = trim de −3,33 dB (uma escola) a dois limiters em série (outra); a mediana de FX por pista é 2,88, e 5+ é extremo maximalista.

## 4. Low-end mono e kick × sub

- **4.1.** Monoize o sub: subs de PA de clube reproduzem <80–120 Hz em mono e conteúdo estéreo nessa região cancela em fase; a prática padrão é monoizar abaixo de 100–120 Hz.
- **4.2.** Uma camada só de BassMono: quatro cascatas de minimum-phase (canais 120–140 Hz → grupos 120/140/144 Hz → master 121,3 Hz) estreitavam a imagem até 1–5 kHz; a alternativa é side LC12 @ 110–115 Hz no EQ M/S do master.
- **4.3.** O sub ocupa 32–45 Hz e o corpo do kick 48–65 Hz; em C# frígio a fundamental sub é C#0 Ableton = MIDI 25 = 34,65 Hz, com 2º harmônico em 69,30 Hz.
- **4.4.** Kick e sub dividem o grave com ducking: volume-shaping (LFO 1/4 com fase travada) ou compressor ultrarrápido (attack <1 ms, release 120–180 ms); band-splitting aplica o duck só no grave e preserva o resto do baixo.
- **4.5.** Todo elemento que colide com o ataque do kick carrega sidechain, e caudas de reverb/delay duckam contra o sinal dry ou o kick.
- **4.6.** O kick afina em grau consonante da tonalidade: a família de 53 kicks mede fundamental mediana 49,1 Hz (25,6–68,0) com decay −20 dB de 0,19 s (0,08–0,39); audite por FFT, porque o nome do arquivo mente.
- **4.7.** Mono-compatibilidade medida: correlação L/R 200–2k Hz alvo 0,38–0,52 (abertura 0,35–0,55), graves 20–120 Hz ≥ +0,95, faixa de segurança geral +0,5..+1,0.
- **4.8.** M/S sutil no master: movimentos abaixo de ~4 dB com Q largo; lama dos sides sai em 240–480 Hz (−1,5 a −3 dB), corpo abre nos sides em ~620 Hz (+2,2 a +2,5 dB), ar nos sides com shelf @ ~11,5 kHz (+2,5 a +3 dB).
- **4.9.** Na referência psytrance, bass e agudos aparecem em volume aproximado no espectro; use a referência nivelada para calibrar essa balança.

## 5. Alvos por destino (master)

- **5.1.** Streaming: teto ≤ −1,0 dBTP com limiter true peak (a transcodificação Ogg/AAC cria inter-sample peaks de +1 a +3 dB); uma variante usa clipper @ −1 dBFS + TP limiter @ −0,3 dBTP. Normalização: Spotify −14, Apple Music −16, Deezer −15, Amazon/YouTube/Tidal −14 LUFS.
- **5.2.** Beatport/clube: sem normalização de loudness; alvos do guia: techno −8 a −6 LUFS, trance −9 a −7, melodic house −11 a −8; TP −1 dBTP; crest 6–9 dB.
- **5.3.** Ao masterizar contra a família: mire −9 a −8 LUFS com teto próprio da seção 6; os +2,3 dBTP de mediana são das referências clipadas.

## 6. EM DISPUTA (conflitos abertos no mapa; não resolver aqui)

- **6.1.** **Teto de True Peak (três leituras coexistem):** (a) ≤ −1,0 dBTP streaming / −0,8 híbrido / −0,5 clube; (b) −0,3 dBTP ao masterizar; (c) o mapa marca a masterização como lacuna crítica, com o estado atual em −0,6 dBTP contra uma exigência citada de "Spotify −2 dBTP". O mapa manda investigar a cadeia (duplo limiter) antes de declarar número de master.
- **6.2.** **Estado do low-end no Set, duas leituras:** o plano relata Kickstart 2 ligado nos SUBS A/B e SUB NOVO mudo; a reconciliação relata Kickstart desligado e SUB NOVO ativo. Decisão pendente de read-back no Live via `live_run_code`, sem escolher versão.

## 7. Casos (contraste com o set do autor; referência, não régua)

- **7.1.** Render analisado (janela 80–140 s): LUFS −10,9, TP −0,6, crest 10,5, bass 36,9% (idêntico à família), sub −3,9 pp, low-mid +4,3 pp, air −1,1 pp (≈3× menos), side/mid +0,7 dB, grave 9 dB mais mono que a mediana, o desejado com cânon low-end mono.
- **7.2.** Correção do baseline: os números "ar 0,5% / low-mid 13,7%" vinham de render anterior; no estado novo, Drop 1 mede air 1,0% / low-mid 23,9% / bass 22,6% e Drop 2 air 1,7% / low-mid 30,5% / bass 15,5%, e o gap real migrou para low-mid/bass.
- **7.3.** Kick principal mediu 52,5 Hz ≈ G#1 (+20 cents, 5ª justa) e o alternativo 46,4 Hz ≈ F#1 (+81 cents, 4ª justa), ambos consonantes com C#; o rack se intitulava "Organic 48Hz".
- **7.4.** A escola de referência Tim mede 0,71/1,04/0,78 s de drum room, sala curta para bateria em retorno, contra reverbs insert de 3,09–11,76 s no caso.
- **7.5.** Ações propostas a partir do gap do render: high shelf 8–12 kHz (+1,5 a +2 dB) no master ou no bus de madeiras e corte 120–400 Hz (−1 a −2 dB) nos buses que acumulam low-mid, agindo acima de 6 kHz; bass e estéreo já estavam na régua da família.
