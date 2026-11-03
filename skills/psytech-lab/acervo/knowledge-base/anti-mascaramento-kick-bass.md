# Anti-mascaramento Kick × Bass em psytech — Pesquisa profunda (2026-09-08)

> Fonte: pesquisa web nativa (14 buscas + fetch completo do Myloops). Todos os números com fonte URL; generalizações marcadas [INFERÊNCIA].

## 1. EQ — mapa e cortes de referência

- Kick psytrance: fundamental **50–70 Hz**, click **2–5 kHz** ([Myloops kick+bass guide](https://www.myloops.net/how-to-make-psytrance-kick-and-bass-work-together)).
- Divisão dura: kick dono de **30–90 Hz**, bass dono de **90–250 Hz** — HP no bass **90 Hz/24 dB-oct**, HP **30 Hz** no master (rumble).
- Alternativa: low cut suave **45–60 Hz** no kick — "mais importante que micro-alinhamento de fase" ([Music StackExchange](https://music.stackexchange.com/questions/96962/kick-bass-phase-alignment)).
- "Ombro" do kick ~150 Hz: sino Q 2–3, −3 a −6 dB só se houver acúmulo.
- **"Boxy" em ~300 Hz = conflito clássico**; acima de 250 Hz, mexer em incrementos pequenos.
- Click fraco: **+2–3 dB em 2–5 kHz** no kick.
- M/S: low-end **mono** (clubes somam em mono) — Armada University/Myloops.
- Separação tonal: ~30 Hz mín. entre fundamentais; afinar bass contra o pitch REAL do kick (63 Hz vs C2=65,4 Hz = batimento 2,4 Hz) — Sokolovskiy.

## 2. Sidechain (nativo Ableton)

| Param | Valor típico |
|---|---|
| Attack | 0–0,2 ms (FB Ableton) / ~4 ms anti-clique (EDMProd) |
| Ratio | 4:1 a 8:1+ |
| Threshold | 8–12 dB de gain reduction (Myloops); −25 dB ponto de partida (Abletunes) |
| Release | **<50 ms** ou 80–100 ms afinado na cauda — "o dial decisivo" |

Sem plugins: **ducking por automação de gain do Utility** (cai ao silêncio no beat, segura 30–50 ms, volta em 60–80 ms); **Multiband Dynamics** nativo (duck só a banda low do bass) — Abletunes/Gearspace.

## 3. Phase/timing

- Bass atrasado **5–15 ms** após o kick = offset típico psytrance (Myloops).
- Ordem de correção: nudge ms → inverter polaridade → EQ linear-phase em crossovers íngremes.
- Delay de 1 ciclo da fundamental (~23 ms @43 Hz) resolve cancelamento (Hainbach).
- Checagem em **mono** na zona 80–120 Hz obrigatória; varia por nota e sample.

## 4. Transient design

- Psytrance clássico: **reduzir attack + aumentar sustain** ("kick com corpo") — inverso do techno punch (KVR).
- Techno punch: aumentar attack; shaper > compressor (Reddit/MasteringBOX); attack 15–30 ms.
- No Ableton sem plugin: aproximar com Compressor (attack 1–10 ms, release curto, GR 2–4 dB) + Saturator para densidade.

## 5. Bus

- Glue no bus kick+bass: **2:1, attack ~20 ms, release ~80 ms, 1–2 dB GR** (Myloops).
- Multiband ducking só <350 Hz mantém harmônicos do bass contínuos (Gearspace).
- **Clipper antes do limiter no master**: aparar só o topo (transientes do kick) rende 1–2 dB de loudness com menos pumping (Newfangled Audio, Mastering The Mix, Reddit).
- **Saturar o BASS (não o sub do kick)**: harmônicos 300 Hz–3 kHz fazem o bass "aparecer" em sistemas pequenos.

## 6. Faders (alvo master −6/−7 LUFS)

- **Kick 2–3 dB acima do bassline** (Sokolovskiy); método objetivo: igualar por LUFS solo (UJAM).
- −6/−7 LUFS = alvo competitivo de clube; loudness vem de arranjo+EQ+ducking+low-end, "não de empurrar o limiter" (Glow Mastering, Ghost Production).
- Hierarquia [INFERÊNCIA]: kick no topo; bass −2/−3; synths −6/−10; sub sintético curto tunado no kick, disparado pelo MIDI do kick.
- Comparar sempre level-matched com a referência (Myloops).

## Fontes

Myloops kick+bass · Music StackExchange phase · Armada University · Sokolovskiy (fit kick&bass) · Hainbach phase vs delay · KVR transient psytrance · Reddit r/edmproduction transient · MasteringBOX · FB Ableton Users · Abletunes sidechain · Gearspace multiband ducking/phase · Ableton blog sidechain 2 · Newfangled Audio clip vs limit · Mastering The Mix · Reddit clipping before limiting · Glow Mastering EDM · Ghost Production LUFS · UJAM bass balance.
