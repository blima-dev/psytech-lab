# A malandragem dos cortes — André Gazolla / Petrix (medido, 21/10/2026)

> Método: taxa original, estéreo, grave no mid; grade por `librosa.beat`. Corte = tempo cuja energia
> cai ≥ 10 dB abaixo da mediana dos 16 tempos vizinhos. **grave** = só kick+baixo somem (o topo segue);
> **total** = vácuo da faixa inteira.

## Faixas (5, MP3 de artista)

| Faixa | BPM medido | compassos | cortes | 1 corte a cada |
|---|---|---|---|---|
| Gazolla — Eastern Thesis | 126,0 | ~247 | 9 | 27 c |
| Gazolla — Boogie Box | 120,2 (`HIPÓTESE`: grade errada) | ~175 | 2 | 88 c |
| Petrix — Enigma (Gazolla rmx) | 123,0 | ~75 | 9 | 8 c |
| Gazolla & Petrix — Breakdown Intro | 123,0 | ~199 | 19 | 11 c |
| Petrix — Groove Work | 123,0 | ~86 | 10 | 9 c |

## As regras que os números sustentam (49 cortes)

1. **O corte mora no fim da frase.** 34/49 (69%) caem no **compasso 7 ou 8** de cada 8. Ao acaso seriam 25%.
   O corte não decora: ele **anuncia** que a frase vai virar.
2. **É curto.** 32/49 duram **1 tempo**, 14 duram 2. Só 3 passam de 2 tempos. Vácuo de compasso inteiro não é a
   malandragem: é breakdown.
3. **Cai no fim do compasso.** 35/49 nos **tempos 3–4** (23 no tempo 4). O corte "puxa" a cabeça do próximo
   compasso. Exceção típica (Breakdown Intro 176/184/192/200): grave sai no **tempo 1 do compasso 8**, por 2 tempos.
4. **Tira o chão, não a música.** 30/49 são de **grave** (kick + baixo juntos); o topo continua. O vácuo total
   (19/49) é o golpe forte, guardado para portas de seção.
5. **Kick e baixo cortam JUNTOS.** Medido no mid em 30–150 Hz: o "grave" cai inteiro, não só o kick.
6. **Escadinha antes da entrada** (Enigma 47·48·49, tempo 4): o mesmo corte de 1 tempo em compassos seguidos
   cria expectativa crescente antes do drop.
7. **Intro com respiração curta** (Breakdown Intro c1·3·5, tempo 4, total): vácuo de 1 tempo a cada 2 compassos.
8. **Dose.** 1 corte a cada 8–27 compassos nas faixas de groove. Não é toda frase: é quando a frase precisa virar.

## Limites

- mp3: o grave é confiável; o topo não foi usado aqui.
- A grade do `beat_track` erra em faixas com pouco kick (Boogie Box saiu 120,2): confira o BPM antes de confiar
  na posição.
- Mede a **ausência**, não o gesto que a cerca (filtro, reverse, eco). O "como" do corte (cortar seco vs. fade)
  precisa de escuta.
