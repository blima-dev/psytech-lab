# Advanced Synthesis with Will O Wisp — Future Media Academy (webinar, 3h11)

**Instrutor:** apresenta-se como Gaston Willowisp (aliases Willowisp, Gizmo, Mysterion) · **Formato:** webinar Future Media Academy · **Duração:** 3h11
**Estudo:** mapa de 27/10/2026 — transcrição ASR (3.812 linhas; 31% são loop de ASR e dois trechos, ~24 min no total, se perderam); áudio não escutado.

## Técnicas-chave

- **Categorizar antes de abrir o synth** — todo som se decide por três fatores: timbre (método/waveform), tuning (nota e registro) e amplitude (envelope/intensidade); a experimentação só vale guiada por um alvo declarado.
- **Subtrativa e FM** — subtrativa (osc + filtro + envelope) para corpo; FM: carrier + modulator com ratio em oitavas mantém a nota, semitons criam inarmônicos; wavetable é bom modulador de FM; LFO só vira timbre acima de 20 Hz.
- **Wavetable: posição é o parâmetro central** — mudar a posição altera só o timbre, a nota fica igual; trocar de wavetable a cada disparo (random por gate) gera percussão sempre diferente — a técnica mais barata para movimento sem mexer no groove.
- **Modulação complexa** — depth (atenuação), polaridade (unipolar 0→+10 vs bipolar −5→+5) e offset; unipolar numa macro move só para cima, preservando o estado salvo; mixar dois moduladores no mesmo destino (LFO + random) cria movimento composto sem camada nova.
- **Random MIDI + Scale no fim da cadeia** — o device Random escolhe entre N opções e o Scale, no FIM, restringe tudo ao modo/tonalidade; gravar o MIDI gerado transforma o aleatório em nota editável.
- **Efeito como parte da síntese** — delay curto em kick+bass (assinatura hi-tech) exige cortar os lows; beat repeat duplo (um gera textura, outro corta); três sends (reverb longo, curto, outro); nunca dois sons empilhados; gravar áudio e salvar preset no mesmo instante. Teoria granular: grão de 1–50 ms; grain freeze no kick+bass serve a breaks.

## Conflitos com minimal psytech (uso restrito)

- FM "bell" e saw somado ao sine do SUB são vetados como corpo (em C#, o 2º harmônico do saw cai em ~69,3 Hz); FM só como acento curto com LP.
- Random de pitch sem Scale sai do modo; registro de melodia gerada citado até C6 — em oitavas 3–4, teto na 4ª e vocabulário de 2–3 notas.
- Grain freeze de kick+bass sustenta o grave e mata o vácuo — oposto do jogo de ausência; usar só em resposta/textura com HP.
- Delay em kick+bass só em transição/resposta com HP ≥120 Hz, fora dos vácuos.
