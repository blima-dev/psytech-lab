# How to make a Full On Psy bassline (Ableton Live)

**Canal:** Tom Cosm (cosmcosm) · **ID:** `etRN4sAiCbI` · **Duração:** 28:43 (1723 s) · **Tema:** bassline full-on psy (pressão de grave).
**Fonte:** legenda automática ASR em inglês, obtida via yt-dlp e lida integralmente (0–28:43). **Não ouvi o áudio** — análise só da legenda. Parte 4 da série "Bassline sound design" do canal.

## Técnica ensinada

Bassline full-on psy ("bouncy funky", não dark 150+) construída **inteira no Operator (Live nativo)**, do sine ao groove:

1. **Base**: MIDI clip de 1 bar, 16ths iguais numa nota só (G), osc único saw ("the standard baseline... they use a saw wave").
2. **Envelope no filtro**: LPF com envelope amount no máximo, peak 100%, decay encurtado (parte de 600 ms), freq de sustain bem baixa → "sharp sweep" por nota. A tese central: **"é tudo sobre fazer alguns elementos dançarem juntos — decay do envelope, frequência e ressonância — é uma mistura perfeita deles"** (04:14). A **curva** do envelope (dot azul) muda o caráter: corta rápido e desacelera.
3. **Notas**: notas longas encadeadas = sub contínuo; encurtar todas (Cmd+A + drag) → levada "definitive" (05:22–05:49).
4. **Kick × bass**: conflito de fase/lama quando o bass soa junto do kick. Duas soluções: **apagar a primeira nota de cada beat** ("when the kick plays there's no note") ou **sidechain** (compressor no bass escutando o kick, attack e release curtos = "ducking the bassline out of the way of the kick").
5. **Widening da parte alta**: Filter Delay com o canal do meio desligado, L/R em **time (ms)** com valores curtíssimos e diferentes (1 ms vs 10 ms) → "amazing spatial effect... widening sound"; band-pass por canal para caráter. Ele avisa: isso **duplica o bass e cria lama no sub**.
6. **Split SUB/HIGH**: agrupar tudo num Instrument Rack com 2 chains — **HIGH** = Operator + Filter Delay + EQ8 com o 1º pole em **HPF cortando TODO o sub**; **SUB** = Operator **sine** com **pitch envelope** (peak +36 st = 3 oitavas, decay curtíssimo) = "really quick punch at the start of that sub". Compressor fica FORA do rack (afeta as duas chains).
7. **Oitava**: tudo uma oitava alto demais → Cmd+A + Shift+↓ → "much more fat, you can hear that sub coming through" (15:09–15:29).
8. **Groove**: "very computer sounding" → arrastar o próprio MIDI clip para o **Groove Pool**, aplicar de volta, trocar Base Note para 16 → shuffle triplet; dosar com o knob **Timing** — "maybe 50 is perfect" (16:51–17:00); aplicar o mesmo groove nos hats.
9. **Variação**: 3º 16th de cada beat +1 oitava (full-on padrão); notas longas "funk notes"; −2 st para "fun feeling".
10. **Velocity como modulador** (só na chain HIGH): velocity → filter frequency (amount 100) = cada nota abre o filtro diferente, "quite expressive"; velocity → pan, sutil, "really nice groove".
11. **EQ "sweet spot" por ressonância**: pole 6 com Q máximo + gain máximo → o resonance "canta" uma nota; varrer até achar a nota **harmônica compatível com o baixo (G)**; depois alargar o Q e baixar o gain → "adds a little bit of character" (21:56–23:00).
12. **Automação desenhada** de cutoff nas notas longas ("swooping" com curvas); começar a frase com nota alta e velocity alta (filtro aberto) (25:07–26:24).
13. Fechamento: testa square vs saw no high; duplica o rack como camada "synth" (sem sub, +1 oitava, square, ping-pong delay).

## Ferramenta usada no vídeo

**Ableton Live nativo**: Operator, EQ8, Compressor (sidechain), Filter Delay, Instrument Rack, Groove Pool. Zero plugin externo.

## Tradução (Live 12 nativo — tradução direta)

Direta (Operator é Live 12 nativo). Os gestos que interessam ao **motor de grave** do estilo minimal psytech: (a) **split SUB/HIGH com HPF na chain alta** — implementação exata do "low-end mono, espacialidade só acima"; (b) **sub sine com pitch-env curtíssimo no ataque** — punch por envelope, sem sample extra; (c) **envelope de filtro por nota com decay/freq/res balanceados** — o "punch" sem bateria extra; (d) **Filter Delay L/R em ms curtos** como widening SÓ da parte alta. O groove do vídeo (shuffle triplet) não é o groove deslocado típico do minimal — é outro idioma rítmico.

## Aplicação sugerida

No canal de grave: separar sub (sine puro, mono, pitch-env de punch) da camada alta (HP ~150–200 Hz, filtro por nota, widening permitido). Ajustar decay do envelope de filtro até o sweep caber entre as posições deslocadas do groove sem preencher o espaço negativo — alvo ~2–2,5 onsets/s, não 16ths contínuos. Quando o kick coexistir com o baixo, escolher entre apagar a nota do beat ou sidechain curto. A/B de 8–16 compassos antes de propagar; medir mono do grave após aplicar.

## Ressalvas

- **16ths contínuos a 145 BPM não são o idioma do minimal**: alvo típico é 128 com jogo de ausência de kick e offsets deslocados; onsets/s moderados, não metralha.
- **Groove shuffle/Base Note 16**: outra escola de groove — só o gesto "dosar com Timing e achar sweet spot" é aproveitável; o desenho deslocado do groove prevalece.
- **Velocity → pan**: ok ACIMA de ~200 Hz; **jamais no sub** (low-end mono). O vídeo aplica na chain HIGH — mesma fronteira.
- **Sidechain**: ferramenta opcional, não lei — o motor do estilo usa ausência de kick como jogo; quando ambos coexistirem, sidechain curto é válido.
- **"I like to boost, it's a bit naughty"**: método oposto ao princípio de cortar a causa antes do boost; o "sweet spot por ressonância" dele é diagnóstico de nota harmônica, útil, mas o boost final merece A/B e medição.
- **Resonância alta no filtro do bass**: ele mesmo mostra que "toma o fundamental" — no grave, moderação e conferência em mono/medição.
- Pitch-env de +36 st é ponto de partida do punch, não regra numérica.

## Trechos de prova (legenda)

1. "the standard baseline from what I hear and I think I'm safe to say they use a saw wave" — 02:01–02:06
2. "the filter will play a kind of a Sharp sweep every time a notes played" — 03:02–03:05
3. "it's all about making um a few elements dance together specifically the Decay time of the envelope the frequency and the resonance and it's a it's a perfect mix" — 04:14–04:24
4. "the sub of that note it's just pretty much continuously going... let's just click and drag them all back a notch... that's much more definitive" — 05:22–05:49
5. "they're conflicting with each other... you're getting into phase cancellation and muddiness" — 08:14–08:25
6. "delete the first note from Every Beat So when the kick plays there's no note" — 08:29–08:37
7. "it's effectively ducking the Baseline out of the way of the kick each time the kick is playing" — 09:23–09:31
8. "we get this amazing spatial effect it's a really quick way of getting a really nice sounding a widening sound" — 10:52–11:00
9. "we're making the Baseline double itself up... we're going to get some really muddy stuff happening in the sub" — 12:01–12:11
10. "turn this first pole into a high pass filter this means it's going to cut all the sub end out of this base" — 13:01–13:05
11. "it's going to start three octaves above and then it's going to quickly go back down... a really quick punch at the start of that sub" — 14:38–14:55
12. "we've done everything in octave too high... down one octave... much more fat and you can hear that sub coming through" — 15:09–15:29
13. "if we bring it up slowly we'll find a sweet spot maybe 50 is perfect" — 16:47–17:00
14. "we can actually go into the operator... put it on say the filter frequency... each one of these notes" — 18:44–19:03
15. "if it's up very very high it actually produces a note... find a note which matches the Baseline which is G" — 21:56–22:16
16. "I just like to have some long notes call them Funk notes" — 23:51–23:56
17. "draw some automation lines in here on that long note just to make them really really funky" — 25:06–25:09

## Limites

Legenda automática ASR; áudio não escutado. Valores exibidos na tela (decay final do filtro, freq de sustain, res, corte do HPF, tempos finais do delay) não são todos verbalizados — só 600 ms (decay inicial), 100% (peak), +36 st, 1 ms/10 ms, Timing 50 e −2 st aparecem falados. BPM do projeto dele: 145 (07:49–07:52 "Tempo back up to 145 BPM") — distante do 128 típico do minimal; nenhum valor de EQ é dado. Título/lógica "full-on" é deliberadamente bouncy/funky, fronteira estética do dark minimal — vale pelos gestos de síntese/arranjo do grave, não pelo idioma rítmico.
