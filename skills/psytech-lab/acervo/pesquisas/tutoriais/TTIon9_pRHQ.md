# How to Make Organic House Bass Warm & Wide (All Day I Dream style)

**Canal:** Dowden Production Academy · **ID:** `TTIon9_pRHQ` · **Duração:** 12:00 (720 s)
**Fonte:** legenda automática em inglês do vídeo. **Método:** leitura por janelas (linhas 1–600 de 784 limpas) — fim `NÃO VERIFICADO`. **O áudio não foi ouvido.**

## Técnica ensinada

Baixo "warm" do All Day I Dream em 3 passos, só Wavetable (synth do Live) + stock: **(1) Calor por overtones controlados** — sine → saw no oscilador (overtones = harmônicos extras), duplicar a camada e **cortar com low-pass 24 dB em ~150 Hz (depois ~135 Hz)** mantendo "só um pouco" dos harmônicos ("we're adding all these octaves and harmonies and then we're cutting almost all of them out so that we're still getting just a little bit of them"); rota alternativa: **Saturator ANTES do EQ** ("very important because we don't want to saturate after our EQing because we want to cut out the high-end") — duas camadas com calor de sabores diferentes. **(2) Movimento** — filtro dentro do wavetable 24 dB @ 135–150 Hz com **LFO no topo da frequência: amount 30–40% afinado para ~15%, re-trigger OFF** (o LFO flui pela nota inteira, não reinicia a cada nota), rate baixo — "very subtle, but it's adding a bit of depth". **(3) Largura sem sujar o sub** — duplicar para camada "wide bass": **desligar o oscilador do sub**, subir uma oitava, filtro ~265–280 Hz + ressonância, uníssono (amount ~25) com attack ~50 ms e release ~1,18 s, LFO também na posição da wavetable. A largura mora na camada de médio, nunca no sub.

## Ferramenta usada no vídeo

Live stock: Wavetable, Saturator, EQ, Compressor (sidechain do kick já presente). Zero plugin pago.

## Tradução para um arsenal compatível

Direta para **Serum 2** (wavetable + LFO interno + uníssono) — mesma arquitetura de um baixo em camadas. É a mesma família da receita de outro tutorial da mesma fonte (YouTube: `kGfIx2d4oEI` — sub carrega fundamental; harmônicos em camada separada) e da conclusão de um diagnóstico do set de referência (o corpo 300–1.200 Hz vem de conteúdo e movimento, não de gain): aqui o "conteúdo" é a fatia de harmônicos que sobrevive ao LP em 135–150 Hz. O **re-trigger OFF** do LFO é o detalhe que preserva groove contínuo — mesmo princípio de outro tutorial (`iWOPUHKbJjI` — LFO fora do beat).

## Aplicação concreta em um baixo rolling minimal (set de referência)

Teste no baixo (Serum 2) em A/B de 8–16 compassos: camada de harmônicos do saw com LP ~150 Hz (não subir o corte — o rolling do set de referência já tem seu corte), LFO sutil no topo (amount ~15%, re-trigger off), e camada "wide" só em 265–280 Hz com uníssono — medir que 20–120 Hz não muda (low-end mono é regra do material) e que 300–1.200 Hz sobe na direção da média das referências externas.

## Conflitos com o material de referência

- **Ordem de cadeia em conflito aparente:** outro tutorial analisado (`xZW3lTHRCxs`) registra **EQ antes da distorção** para kick; o vídeo diz **Saturator antes do EQ**. Não são a mesma tarefa (ele satura e depois corta o agudo gerado; o outro caso equaliza para não saturar lama) — mas a ordem tem de ser decidida por A/B no baixo, não copiada.
- LP em 135–150 Hz na camada de harmônicos é do sub-bass DELE (organic house é mais sub-contínuo); o rolling de referência vive acima (~200 Hz) — não transplantar o corte.
- Sidechain do kick já presente no canal dele: no material de referência o duck é só <150 Hz (ver tutorial `TwZk8Gcyl1E`, incluído no acervo).

## Trechos de prova (legenda)

1. "We're going to actually filter out almost all of that harmonic content… we're still getting just a little bit of them, but we're cutting so much of it out that it doesn't sound very high-end." — linhas ~172–195
2. "We're going to put the saturator before the EQ. That's very important because we don't want to saturate after our EQing because we want to cut out the high-end." — linhas ~266–278
3. "I want to turn the re-trigger off. The re-trigger is going to reset the parameter to the beginning of the LFO every time a note is played. And I don't want that." — linhas ~372–385

## Limites

Fim do vídeo (após linha 600: detalhes do LFO da wavetable, mix final) não lido. Sem dB/threshold numéricos; "amount 25" do uníssono e "10 or 15" do LFO são valores da UI dele. Áudio não escutado.
