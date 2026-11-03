# 05 — Lab EXP + SYN: protocolos (sem execução)

> Nenhum experimento foi executado ainda. Cada EXP/SYN só existe quando entregar os 7 itens. Saída como artefato de medição isolado — nunca aplicada direto no projeto em produção.

## Template obrigatório por experimento
1. Hipótese + mecanismo físico. 2. Arquivos original/processado. 3. Parâmetros, SR, duração, janela e ponto de captura. 4. Gráfico temporal/espectral/fase. 5. A/B auditivo nivelado. 6. Resultado, hipótese rejeitada, limitações. 7. Implicação de mix. Registrar também quando a intervenção **não melhora**.

## EXP-01…10 (mistura/fase/dinâmica)
* 01: senoides 50 Hz a 0°/90°/180°, amplitudes controladas.
* 02: senoide + cópia atrasada → pente por frequência.
* 03: kick+sub com deslocamento gradual → transiente vs energia.
* 04: kick+rolling, envelopes diferentes, mesmas notas/volumes.
* 05: original vs paralelo (latência/filtros/compensação).
* 06: mesma mix estéreo vs mono, perdas por banda.
* 07: EQ fase mínima vs linear em transiente, A/B cego.
* 08: saturação/clipping por nível → harmônicos, aliasing, crest.
* 09: compressão/limitação progressiva a loudness igualado.
* 10: overlap espectral resolvido por arranjo vs volume vs EQ estático vs dinâmico.

## SYN-01…10 (síntese)
* 01: seno vs seno+harmônicos (tradução do sub). 02: fase fixa vs random (estabilidade ataque). 03: unison/detune no grave (soma mono). 04: FM razões/intensidades. 05: pitch-env + amplitude (kick). 06: distorção pré/pós-filtro. 07: glide/duração MIDI (bassline). 08: mod sync vs free. 09: granular/spectral (transientes/artefatos). 10: mesma receita em instrumentos diferentes.

Prioridade de execução futura: EXP-03/04 + SYN-02/05 (estabilidade sub + kick). Motor: render offline do synth (ex.: Serum), >100×, no BPM do projeto.
