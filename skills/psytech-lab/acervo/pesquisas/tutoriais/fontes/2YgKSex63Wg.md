# How to Make Gnarly Bass Rips in Serum (Psytech Tutorial)

**Canal:** Scionaugh · **ID:** `2YgKSex63Wg` · **Duração:** 2:59 (179 s) · **Frente:** pressao-grave / stab-resposta · **Perna:** BUSH PROG
**Fonte:** transcrição completa via web reader, 29/10 — yt-dlp bloqueado (HTTP 429). **Não ouvi o áudio.**
**Contexto:** o som é o "bass rip" de **Crab Soup**, collab com Mezzle, lançado na **Alpaka Muzik** (Fault In The Formula Pt.2) — mesmo selo das referências do projeto de referência (AlpaKa).

## Técnica ensinada

Bass rip psytech no Serum 2, construído em camadas de movimento e não de onsets novos: sawtooth com **unison 5** e detune para largura; wavetable "evolution" com **posição automatizada pelo LFO 1**; "a little bit of FM". FX: distortion, phaser, compressão ~5 dB, reverb mínimo. O truque central: **a automação não está no filtro, está no CO (cutoff)** — e o cutoff controla **três coisas ao mesmo tempo**: o cutoff em si, **a quantidade de FM** ("that's going to add a bit of extra grit") e **um segundo filtro no FIM da cadeia** (depois de reverb/compressão/distortion), ambos em 18. O segundo filtro existe para que, com o cutoff fechado, **não escape o buzz da distorção**: "we get all the texture from using the distortion, but none of the buzz".

## Ferramenta usada no vídeo

Serum 2 + Valhalla VintageVerb (externo). Tradução para o Live: usar o retorno de reverb nativo (Hybrid Reverb) no lugar do VintageVerb.

## Tradução para o Live/Serum 2

Direta (Serum 2). Encaixes no fluxo de referência:
- **Um macro (cutoff) modulando FM + filtro principal + filtro final** = movimento sem onsets novos — a mesma filosofia de macros/automação embutidos no som.
- **Filtro DEPOIS da distorção** para tirar o buzz: converge com a receita de clipper/saturator (clip gera HF; filtrar depois) e com a regra de não deixar a saturação comer o kick (EQ antes da distorção no kick; aqui a tarefa é outra: a distorção é desejada e o filtro final é o limpador).
- **Unison 5 = ímpar**, confirma a regra do mesmo canal citada em outro vídeo ("only the odd numbers, three, five, or seven").
- É um **rip** (registro de lead/baixo-médio), não baixo de fundamentais — casa no stab/resposta, não no sub/baixo de fundamental.

## Aplicação de referência

1. Camada de stab/resposta em Serum 2: saw + unison 5, FM leve, e **CO macro** → cutoff + FM amount + filtro final em série depois da distorção.
2. Automatir o CO em rampa de 8 compassos na subida de seção (pontuação 9/17/25/33…).
3. HP ≥250 Hz na camada (não é dona de grave); largura do detune fica acima do low-end mono.

## Cautelas

- Distorção + filtros em stab/resposta: OK; **no sub nunca** — a mesma distorção no sub engordaria o grave (sub limpo).
- Buzz de distorção tem de morrer no filtro final — não resolver no master (nenhuma receita desta leva autoriza boost/filtro no master).
- BPM/tonalidade não citados no vídeo — definir pela tonalidade do projeto de destino (a referência trabalha em C# frígio).

## Trechos de prova (transcrição)

1. "the automation is not on the filter, it's on this thing called CO, which is cutoff. So… we can see cutoff is controlling the FM amount, so that's going to add a bit of extra grit."
2. "why would I have a filter at the end of the chain when we've already got one filter? … when I've got that cutoff right down, we don't hear any of the buzz. So, we get all the texture from using the distortion, but none of the buzz."
3. "we've got a sawtooth here. Uh we've got the unison on five. Increase that detune to give it some width."

## Limites

Transcrição via web reader não traz timestamps por frase (só o fluxo); duração curta (2:59) minimiza perda. Valores de UI não citados além do unison 5, compressão ~5 dB e filtros "both on 18". Áudio não escutado.
