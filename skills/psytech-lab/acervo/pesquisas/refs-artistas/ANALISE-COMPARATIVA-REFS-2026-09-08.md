# ANÁLISE COMPARATIVA — REFERÊNCIAS PSY-TECHNO: Akari System, André Gazolla, Yao Ofosu, Kaled Nasser
**Data:** 2026-09-08 · **Método:** medições de áudio (ffmpeg/FFT, bandas 20–120/120–300/300–1k/1–5k Hz) + 4 pesquisas web profundas.

---

## 1. RESUMO EXECUTIVO

O gênero que o Beatport chama oficialmente de **Psy-Techno** (128–138 BPM, "pulso hipnótico do techno + sound design psicodélico") é o território medido: as referências abaixo marcam 125–132 BPM reais e as 4 pesquisas convergem nesse território. A régua da cena é **grave = 56–78% da energia do groove, médios = 1–3%**. Os requisitos para chegar à "experiência" Akari/Gazolla/Yao/Kaled, em ordem: **(1)** duração 6:30–8:21 da cena, **(2)** percussão orgânica com swing (groove pool 54–58%), **(3)** "momento psy" com acid 303 em tom frígio, **(4)** sidechain bass→kick, **(5)** master alvo −7 a −6 LUFS.

## 2. MEDIÇÕES (verificadas)

### 2.1 BPM e entrada do low-end

| Referência | BPM (medido) | Primeiro corpo | Low-end pleno |
|---|---:|---:|---:|
| Akari — Segments | ~127,8 | estável 0–70 s | patamar contínuo |
| Akari — Slippery Slope (Luis M) | ~127,8 | 25–30 s | 30–35 s |
| Gazolla — Mayuri | ~128 (IBI 470 ms) | 29,7 s | 60,9 s |
| Gazolla — Breakdown | ~128 | 30–35 s | 55–65 s |
| Yao — Limbo | ~130,8 (458,7 ms) | LF estável 0–70 s | +9,1 dB ataque até 70–90 s |
| Yao — Demons | ~125 (480 ms) | corpo estável | ataque +7,1 dB 70–90 s |
| Kaled — Bush | ~128–132 | **5–10 s** | escala contínua até 60–65 s |
| Kaled — Sonar (AdrenaZ) | ~128–132 | 25–30 s | 30–35 s |
| Kaled — Karmacobra | ~132 | 15–20 s | respiro 45–55 s, 2º patamar 60–75 s |

**Leitura:** nenhuma referência sustenta vazio inicial; primeiro impacto ≤0:35 em todas. O padrão Yao/Gazolla é corpo → degraus → impacto ~1:00.

### 2.2 Balanço de energia por banda no groove (60–120 s)

| Referência | Grave 20–120 Hz | Corpo 120–300 | Médios 0,3–1k | Ataque 1–5k |
|---|---:|---:|---:|---:|
| Akari — Segments | 74,0% | 22,2% | 3,3% | 0,5% |
| Akari — Slippery Slope | 60,1% | 37,4% | 2,4% | 0,1% |
| Gazolla — Mayuri | 72,4% | 24,7% | 2,7% | 0,2% |
| Gazolla — Breakdown | 56,4% | 40,3% | 2,8% | 0,5% |
| Kaled — Bush | **78,4%** | 20,2% | 1,3% | 0,1% |
| **Consenso** | **56–78%** | **20–40%** | **1–3%** | **<1%** |

A proporção estrutural da cena: a base grave é a soma mais pesada da mix e os médios melódicos não competem.

### 2.3 Timings de kick

| Faixa | IBI p10/mediana/p90 | Cauda do kick |
|---|---|---:|
| Fox/Artemis | 433/455/490 ms | +0,5 dB |
| Dark Voices | 435/460/490 ms | −9,1 dB |
| Gazolla — Mayuri | 465/470/480 ms | **+1,5 dB** |

O IBI ~455–470 ms confirma 128–132 BPM. A cauda do kick é a diferença tátil: Mayuri mantém cauda viva — um gate agressivo no kick deixa a "batida forte" sem o arredondamento final.

## 3. CONSENSO DAS 4 PESQUISAS (o que o gênero exige)

1. **Gênero oficial**: Psy-Techno (Beatport, dentro de Peak Time/Driving), 128–138 BPM — "pulso hipnótico + sound design psicodélico, basslines dirigidas, layering intrincado".
2. **Duração**: cena opera 6:30–8:21 (Gazolla ~6–8 min; Akari 5:30–7:00; Kaled 6:30–8:21; Yao 6:31–7:00). Faixas curtas demais ficam fora do padrão.
3. **Estrutura**: arranjo evolutivo, camada nova a cada 8–16 compassos, breakdowns contidos (30–45 s), intro/outro DJ-friendly de 16–32 bars, 1–2 "momentos psy" por faixa.
4. **Groove**: kick/bass quantizados e retos; o swing humano (54–58%) entra SÓ na percussão/shakers — nunca no kick.
5. **Low-end**: sub mono <~100–120 Hz; kick tuned (C# ideal); sidechain do bass pelo kick é canônico; glue compressor no bus kick+bass.
6. **Glitch metálico (Akari/hi-tech)**: FM inarmônico (Operator ratios 3.7:1/5.1:1), resampling em cadeia, Beat Repeat 1/32–1/64, pitch-down com artefato, granular 20–30 ms. Uso como ACENTO (2–4 hits/8 bars), não como melodia contínua de hi-tech.
7. **Rolling bass (Yao/Gazolla/Black Belt)**: saw mono phase-locked, LP 24 dB com envelope (decay ~30%, release 0), resample por nota em Drum Rack, cortar mud ~300 Hz, velocity variando nota a nota.
8. **Master**: alvo −7 a −6 LUFS integrado com clipper antes do limiter; aspereza 4–7 kHz tratada com corte estreito/de-ess; low-end mono.
9. **Cena BR**: bush tech moderno = esse psy-techno groovado com DNA percussivo orgânico; black belt/Atípic/AlpaKa = o ecossistema do estilo (Gazolla e Yao lançam na Black Belt; Akari/Kaled na AlpaKa/Atípic).

## 4. POR ARTISTA — identidade e o que aplicar

### Akari System (Rinkadink + Airi, AlpaKa)
**Identidade:** stabs metálicos cristalinos, glitch de precisão, energia limpa de peak-time.
**Como aplicar:** pipeline de glitch (resampling+Beat Repeat) para os FX; stabs band-pass ressonantes como pergunta-resposta; de-ess dinâmico 5–8 kHz nos metálicos.

### André Gazolla / AdrenaZ (Black Belt)
**Identidade:** "psytechno grooves, atmosferas densas dark e o fluxo hipnótico do rolling bass"; gingado house-brasileiro nas percussões; quebras com corte de grave seco.
**Como aplicar:** ghost notes de percussão nos 16ths "e" (deslocadas 10–25 ms); rolls pré-drop acelerando; intro percussiva longa; 1º tema ~bar 32.

### Yao Ofosu (Black Belt + AlpaKa, Berlim)
**Identidade:** "psychedelic techno + dark minimal, late-night"; baixo com pocket e silêncios deliberados; curva em degraus.
**Como aplicar:** frases de baixo 1–2 compassos com silêncio no 1º 16th (pocket empurrado); resample das notas de baixo em Drum Rack com EQ por nota; automações de filtro de 16–32 bars nos synths.

### Kaled Nasser (Atípic, Cuiabá)
**Identidade:** bush tech moderno: "sustained heavy low-end", percussão orgânica brasileira, 128–132 BPM.
**Como aplicar:** percussão orgânica contínua com swing 54–58%; motivo de 2–3 notas (tônica–sétima–quinta em menor) sobre drone; low-end que entra cedo e não sai (padrão da cena).

## 5. FONTES E LIMITES

- Medições: VERIFICADO (ffmpeg/FFT sobre MP3s; % de energia interna a cada master — não comparar níveis absolutos).
- Pesquisas web: VERIFICADO nas fontes dos dossiês de pesquisa; INFERÊNCIAS marcadas; BPM/key de várias faixas dos artistas: NÃO ENCONTRADO (Beatport/Spotify bloqueiam).
- Nenhuma escuta humana automatizada: tudo aguarda validação por escuta.
