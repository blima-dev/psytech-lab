# Receita: kick "Congela" (01/11/2026)

**Fonte:** sample externo de kick loop do pack de stems do **Music4Aliens** (pasta Minimal Techno; arquivo `Minimal techno 128 3-001 KICK LOOP 126 Bpm (Congela).wav`).
O nome do arquivo diz 126 BPM, mas a medida dá **128 BPM**. O arquivo tem 30 s e 64 golpes.

**Papel:** o sample substitui um kick sintetizado (Operator) como golpe principal; o kick sintetizado pode ficar mudo e continuar servindo apenas como fonte de sidechain.

**Medida:** média sincronizada de 64 golpes, na taxa original do sample.

## O golpe

| Medida | Congela |
|---|---|
| Nota do corpo | **F#1 −18 c (45,8 Hz)** |
| Queda de pitch | **144 Hz (0–8 ms) → 92 (10–30 ms) → 64 (30–60 ms) → 46** |
| Decay até −20 dB | **98 ms** |
| Pico do clique | **1,6 kHz** (2–8 kHz em −28 dB: quase sem estalo agudo) |
| 40–55 Hz | −1,7 dB (quase tudo está aqui) |
| 55–75 / 75–110 / 110–250 | −16 / −28 / −25 |
| 250 Hz–1 kHz | **−40,5 dB** (médio limpo) |

## Como refazer no Operator

Nota: em teste de escuta, a recriação no Operator ficou abaixo do sample; o resultado preferido foi usar o one-shot original do sample no Simpler. A receita abaixo descreve a anatomia do golpe.

- **Osc A:** seno afinado em F#1.
- **Pitch envelope:**
  - começa cerca de 1,6 oitava acima, uns +20 st (144 Hz);
  - cai pela metade em ~20 ms;
  - assenta em ~60 ms.
  - Ou seja: Pe Amount alto e Pe Decay de ~40–50 ms.
- **Amp envelope:** Attack 0 ms e Decay de ~100 ms. O decay curto faz o kick terminar antes de o sub responder no x.25, que fica 115 ms depois a 130 BPM.
- **Clique:** quem gera o clique é a própria queda de pitch, em torno de 1,6 kHz, sem oscilador de ruído. Não cortar 1,5 kHz.
- **Médio:** nenhum Osc B nem saturação no médio (250 Hz–1 kHz em −40 dB).

## Dicas de uso

- Warp **Re-Pitch** em vez de Beats (Beats estala no loop).
- EQ Eight com shelf de high ~5 kHz **−5 dB** para domar o estalo da ponta.
- Ao substituir o kick anterior por este sample, copiar para os clipes do sample as ausências/vácuos do kick anterior — os respiros de 1–2 tempos ficam preservados.
