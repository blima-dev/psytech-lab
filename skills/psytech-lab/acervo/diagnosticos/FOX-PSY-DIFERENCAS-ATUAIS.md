# Fox × projeto de referência — diferenças e correções da escuta (07/09/2026)

> Estudo do acervo psytech-lab, anonimizado. Referência externa: **Fox (Artemis AR Remix)**. O lado pessoal
> do original (quem acompanhou, decisões de captura canceladas) foi neutralizado; a técnica fica.

| Elemento | Evidência | Correção aplicada | Limite / próximo teste |
|---|---|---|---|
| Stabs | EQ Eight passava ~137–345 Hz, cortes de 48 dB/oitava. | Corte superior aberto para 2,80 kHz. | A/B: faixa de ataque ganhou ~18,7 dB relativo ao corpo; mudança perceptível confirmada por escuta. Não é medição de qualidade. |
| Kick: ataque | Drum Buss Damping 971 Hz. | Damping 3,99 kHz. | A/B: grave 30–120 Hz praticamente igual; ataque 1,5–6 kHz +12,46 dB relativo, pico menor. |
| Kick: corpo | Cru desce de ~178 a 50 Hz; capturado ~128 a 61,5 Hz. Não há oitava dobrada. Nota MIDI .24 beat, release ~50 ms. | Teste .36 beat nos clips 192 e 208; boom preservado. | Hipótese: o gate curto corta parte da cauda grave. Escuta atual, sem nova gravação. |
| Subgrave | Três notas por beat; ouvido como acelerado. | 47 clips passaram a notas em .5 do beat, duração .30 e velocidades 87/90; pausas anteriores preservadas. | Contratempo é decisão candidata para o projeto, não transcrição exata do stem Fox. |
| Hats | Sustain integral, decay 600 ms nos dois Simplers; rejeitados por escuta. | Aberto decay 120/release 20 ms; fechado 55/12 ms; sustain −inf em ambos. | Mudança de envelope; os samples continuam os mesmos. A escuta decide se trocar timbre. |
| Atmosfera | Grupo desligado e relatado "menos melodia". | Atmosferas permanece mutado. | Não reativar automaticamente; o projeto conserva o material até decidir a remoção. |
| Frase curta | Clip em 416 usa sequência 61/64/68/71/73, notas ~.28–.34 beat. | Teste com duas notas 61/64 e duração .14 no clip 416. | Teste local; demais frases ainda podem soar melódicas. |
| Retorno | Kick ausente em 387 na leitura anterior. | Kick 387 inserido, 16 notas em 384–400. | Nova leitura com 16 notas é resultado da correção; não erro do relatório anterior. |
| Construção | Riser terminava 336, drop 384; hats 4 notas por 16 beats. | Riser 374–382; hat fechado 352 = 8 notas, 368 = 18 notas. | Pausa final preservada; posições serão remapeadas no molde Fox. |

## Estrutura

Grade candidata da referência (mapa reverso): **132 BPM**. Intro 1–16; drop 1 17–72; preparação 73–80;
break 81–112; drop 2 113–192; saída 193–216. No projeto anterior o segundo drop começava no compasso 97:
alterar apenas locators não atende ao pedido — clips e automações precisam mudar juntos. Aplicação do molde
ainda pendente.

## Fontes e limitações (regras de método)

- Comparação kick/baixo e A/Bs (stabs, damping) documentados em arquivos de medição do projeto (stems Demucs
  e JSONs de A/B).
- Capturas existentes em `/tmp` são temporárias e anteriores a ajustes mais recentes.
- Fox drums/bass/other são **separações Demucs do edit de 3 min**, não os canais originais e não a timeline
  integral.
- **Não equiparar picos/níveis absolutos do MP3 masterizado aos sinais isolados pre-limiter do set.**

Principal ainda em desenvolvimento: avaliação integral, caudas, mono e aplicação da estrutura pendentes.
Não há variantes concluídas.
