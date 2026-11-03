# Mapa de sessão de um set de referência — material de estudo extraído (12/09/2026)

> Estudo do acervo psytech-lab, anonimizado. O original é um mapa de sessão do set (tabelas de mutes por
> canal, backups, rollbacks, estado não salvo) — essa parte é estado puro e foi removida. Fica o material
> transferível: hipóteses de teste, o design system de resposta, o tratamento medido de transições, o mapa
> espacial da profundidade e as lições operacionais do Live.

Contexto: set a 128 BPM, C# frígio, loop de trabalho no drop 1 (beats 192–304), retornos A-Reverb (0.85) e
B-Delay (0.85).

## 1. Hipóteses de teste (canais de teste, todos mutados por padrão, clipes 192–304)

| Hipótese | Pergunta que responde | Implementação |
|---|---|---|
| **Micro-hats 16th sintopado** — velocidade no topo | O 16th sintopado deixa a faixa mais rápida sem virar metralhadora? | 16ths com pocket no 4º beat (silêncio .75); Serum 2 |
| **Ear ticklers 3D órbita** — movimento ao redor da cabeça | Os micro-ticks ×.772 orbitando dão profundidade sem Auto Pan em tudo? | Simpler wood + Delay + AutoPan |
| **Perc orgânica sincopada** — corpo no centro | A perc sincopada dá malandragem sem encher o groove? | perc de pack (BLACKBOX) sincopada, sem AutoPan |
| **Wood click resposta** — conversa | O wood respondendo nos gaps cria diálogo ou fica espalhado? | wood só responde nos gaps dos bars pares |
| **Shaker swing malandro** — atraso sensual | O shaker com +0.02 beat traz o swing do tech house antigo ou fica datado? | 8ths com +0.02 beat no contratempo; Operator |

Volumes 0,75–0,9; densidade crescente (ghost notes nos blocos finais). **Padrão ×.772** (atraso ~10 ms no
micro) = linguagem de swing já usada no material original.

## 2. Design system de resposta (duelo de personagens)

- **Resposta em duelo (−1 oitava):** duplicar o personagem A com patch/FX intactos; a resposta espelha TODAS
  as frases do A −1 oitava (ex.: 61→49, 62→50, 56→44, 68→56), shift +2.0/1.5/2.5 beats onde couber sem
  colisão, velocity −10~14, fecho na quinta (44). Anti-colisão: resposta nunca toca junto com o A.
- **Tema nos cortes:** célula malandra que entra nos cortes REAIS do kick (espera o kick e não vem — a
  surpresa). Vocabulário descendente 68→62→56→50 com "mordida" no bII (a nota frígia) + ghosts vel 52.
  Auto Pan-Tremolo em modo Panning (Sine, 68%, synced 1 bar, Phase 180°) = varredura 3D de um lado pro outro
  (linguagem Greenwolve/Ear Ticklers).
- **Regra anti-colisão:** cada célula nunca sobrepõe A, B ou outra C — a varredura pula posições ocupadas.
- **Regra de dono:** 1 dono por corte (janela de FX exclui célula melódica, e vice-versa).

**O sistema da conversa:** A pergunta → B responde grave no vácuo → kick corta → C entra inesperado rasgando
em 3D → subs complementam. Papéis por artista de referência: **Akari** = chão quase reto; **Gazolla** = corte
seco e PUSH; **Desert Nomads / Tiger Eyes** = retorno deslizante; **Greenwolve** = malandragem lateral;
**Rolling** = PULL sensual.

## 3. Tratamento medido de transições (FX pack e tape rewind)

- Auto Filter HP no canal de FX (**111 Hz**) e no tape rewind (**151 Hz**) — calibrado por bissecção no display.
- Sends medidos: FX pack A-Reverb 0,25 / B-Delay 0,15; tape rewind A-Reverb 0,40 / B-Delay 0,30 (cauda do
  corte seco Oziris).
- Base: dicionário de 232 FX das referências — a transição das refs vive no **topo** (centro 3–3,5 kHz,
  ~1/3 >4 kHz) e **NUNCA no grave**; o FX pack medido tinha **37% da energia <100 Hz** → HPF obrigatório.

## 4. Mapa espacial da profundidade (molde de organização)

- **Centro/chão:** kick + sub ground (senoidal + saturador) + camas de médio (150–400 Hz no centro).
- **Frente:** personagem melódico (synth + delay + filtro, sends de reverb/delay).
- **Laterais:** madeiras (delay ping-pong + auto pan), glitches, ear ticklers.
- **Fundo/altura:** camas atmosféricas com filtro fechado, drones, chants, swells, caudas reversas.
- **Movimento ao redor da cabeça:** auto pan-tremolo das madeiras (binaural), micro-hats.
- **Silêncio:** vácuos programados (bars 24/32), corte seco no estilo da referência, caudas reversas.

## 5. Lições operacionais (Live 12, verificadas na sessão)

- `set_notes` legacy via bridge **ADICIONA**, não reconstrói — sempre `remove_notes` antes, ou usar
  `add_notes clear=true` pela ponte.
- `get_notes_extended` retorna tempos **RELATIVOS ao clip** — misturar com absolutos dobra as posições.
- Popups de permissão do script aparecem na GUI do Live e travam a chamada até alguém aceitar.
- Filtro de pistas por nome: buscar "kick" (não "ick", que pega Wood Click).
- `AudioClip.file_path` EXISTE no Live 12 — dá para medir o WAV real de cada clipe.
- Um corte de kick no meio do arranjo pode ser intencional (duelo de personagens sem kick) — checar o desenho
  antes de "consertar".
- Clipes de transição de biblioteca têm o tratamento certo no topo (HPF + sends) e errado no grave — medir
  a energia <100 Hz antes de mandar o FX para a frente.
