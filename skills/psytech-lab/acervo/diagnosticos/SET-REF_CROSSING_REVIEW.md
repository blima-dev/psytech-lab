# Cruzamento: o set de referência montado × o que as referências fazem (12/09/2026)

> Estudo do acervo psytech-lab, anonimizado. Estado medido após faxina (62 pistas); fontes comparadas:
> perfil de groove das 29 referências, medições Fox, bibliotecas de groove e estudo forense comparativo da
> Rolling Music. Os números das referências são externos e permanecem íntegros; o lado do set é tratado como
> "set de referência".

## 1. O que estava montado (verificado no Live)

- **Motor:** kick único ligado (a versão anterior foi removida, preservada em backup) · sub: **3 engines de
  sub simultâneas** · cama 4× (3 versões iguais + 1 em Serum, diferente de verdade).
- **Topo novo:** hat em Serum + closed hat em Gatelab + **acid FREAKAUDIO ACID** (Serum FX) + FX PACK 73 +
  tape rewind + 2× Serum FX (uma mutada).
- **Movimento:** wood editado (26 clipes), swells reeditada (16 clipes, vol 0.27), shaker de teste reciclado
  (26 clipes 96–495, cadeia Serum+Filter+Delay).
- Personagem 4× (B/E/D/C), glitch 5×, wood ~6 no ar.

## 2. O que ainda estava duplicado igual — para mexer

| Prioridade | Família | O que é | Overlap medido |
|---|---|---|---|
| **P0** | **Glitch 5×** | 5 pistas com os MESMOS 22 clipes + mesmo device | 407–408 beats (100% do tempo) |
| **P0** | **Sub A×D×C** | 3 engines de sub simultâneas | 287–333 beats — risco de fase/embolação no low-end (regra de método: sub mono e único) |
| P1 | **Swells** | 3× mesmos 7 clipes (a 4ª já reeditada) | 137 beats |
| P1 | **Yao A×B** | 2× mesmos 10 clipes (C/D/E já mudos) | 283 beats |
| P2 | **Personagem** | 4 simultâneas, clipes diferentes mas sobrepostos | 329–393 beats |
| P2 | **Cama** | 4 simultâneas (1 em Serum, diferente de verdade) | 236–411 beats |
| P2 | **Wood** | 4 + 2 de teste somando | 61–394 beats |

**Nota:** as somas múltiplas são parte da "profundidade cruda" aprovada de ouvido — a decisão
cruda × organizada fica em aberto. O que é objetivo: **glitch 5× e sub 3× são os dois pontos onde a soma
idêntica pesa mais** (glitch = 5× o mesmo evento; sub = risco de cancelamento de fase no grave).

## 3. Cruzamento com as referências — onde estava perto e onde faltava

### O que já estava parecido (os acertos de ouvido)
| O que o set fazia | A referência que isso imita |
|---|---|
| Ácido FREAKAUDIO + FX packs + tape rewind | **acelero narrativo Akari/Artemis** (eventos rápidos no midrange, transições marcadas) |
| Wood editado denso (26 clipes) + ticklers ×.772 | **Greenwolve/Rolling** (madeiras respondendo, micro-pocket) |
| Sub staccato + Desert Nomads | movimento de bass psy (Zenon/Desert Nomads são da linhagem certa) |
| Hat em Serum + Gatelab closed hat | topo aéreo da Fox (começado — faltava ganho) |
| Ghost notes nos canais de teste (vel 48/72) | **Petrix Allert 30/32 ghosts** — a técnica do selo |

### O que as referências têm e o set ainda não tinha (lacunas medidas)
1. **Topo aéreo com ganho real** — Fox: 4–10 kHz a −20 dBFS; o set: −47. Os hats existiam, mas o master
   continuava escuro no ar. Medir de novo no master após a mix.
2. **Rolling bass que "pega o bastão" a ~180 ms** — a referência Fox (60–120 Hz a −12) e os 29 GROOVE_BASS
   extraídos mostram o desenho; o sub do set ainda era 3 engines somadas, não um rolling único com
   harmônicos em 120–250 Hz.
3. **Pull sensual distribuído** — na Rolling é contínuo (offset 0.61 no breakdown); no set só nos canais de
   teste. Sugestão: 1 percussão lateral com o pull em todos os blocos, não só 192–304.
4. **Um elemento por função** — nenhuma ref soma 5 cópias do mesmo evento; elas variam timbre/pitch por
   bloco. É o desvio estrutural mais visível.

## 4. Plano mínimo sugerido (sem executar)

1. **Glitch 5× → 1×** (manter uma, mutar as outras 4) — ganho imediato de clareza no midrange, zero risco
   musical (são idênticas).
2. **Sub 3× → 1× + verificar fase** — testar cada um sozinho contra o kick antes de escolher.
3. Swells: manter só a reeditada.
4. Personagem/cama: testar a versão Serum vs as iguais, depois 1×.
5. Wood: decidir a duplicata parcial (apagar ou virar variação).
6. Depois da faxina: medir master vs Fox (4–10 kHz) para calibrar ganho do topo.

## 5. Camada 2 — presets dos Serums comparados (state binário do arquivo)

Todos os devices estavam **LIGADOS** (único device OFF = trem ghost pump, igual nos 3 subs). Hashes do
ProcessorState:

| Família | Pist. | Veredito |
|---|---|---|
| **Sub** (3 engines) | 3 | **MESMO PRESET EXATO** (hash 2a3764702c4e ×3) — os nomes são diferentes, o SOM é 3× idêntico. Duplicata real mais grave do set. |
| **Glitch** | 5 | 3 sons distintos: 2 próprios + **trio idêntico** (03f4291733cd). Redução correta: manter os 2 e 1 do trio. |
| **Personagem** | 4 | 1 próprio; **trio idêntico**. Redução: 1 + 1 do trio. |
| **Swells** | 4 | **4 presets DIFERENTES** — não são duplicatas sonoras; são 4 timbres somados (decisão artística, não faxina). |
| Cama em Serum | 1 | state único de 1,95 MB (com samples embutidos no Serum). |

**Correção ao mapa da seção 2:** sub ×3 é duplicata total (mesmo preset). Glitch/Personagem: redução segura =
manter as variações A/B e UMA cópia do trio idêntico. Swells: ouvir antes de cortar — são timbres diferentes
somados no mesmo tempo.

**Método (replicável):** comparar o hash do ProcessorState do Serum entre pistas "iguais" — hash idêntico =
mesmo som (faxina); hash diferente = timbres somados (decisão artística, ouvir antes de cortar).

## 6. Medição pós-faxina (janela mais energética da captura) — base da receita do bass

| Banda | Set | Fox (drop) | Gap |
|---|---|---|---|
| 20–60 | −16,7 | −10,0 | −6,7 |
| 60–120 | −17,6 | **−7,1** | **−10,5** |
| 120–300 | −18,9 | −14,4 | −4,5 |
| 300–1 k | −25,8 | −19,4 | −6,4 |
| 1–4 k | −35,9 | −19,9 | −16,1 |
| 4–10 k | −42,6 | −20,5 | −22,2 |

Faxina + elementos novos fecharam: 60–120 **+5,6 dB**, 120–300 **+9,3**, 1–4 k **+7,1**, 4–10 k **+4,6**
(direcional: kick/trecho diferentes entre as duas medições). Peak da janela: −0,7 dBFS (limiter no teto).

**Receita do bass novo derivada dos números:**
1. **60–120 Hz é o maior gap musical (−10,5)** — na Fox essa é a banda MAIS ALTA de todas (rolling bass
   domina). No set o grave ainda era sub-centrado (20–60 acima de 60–120).
2. **Arquitetura:** sub puro em C#1 (34,65 Hz, mono) + camada rolling cujos HARMÔNICOS 2º/3º (69,3 / 103,9 Hz)
   entregam o 60–120 — é assim que a Fox domina a banda sem subir o sub.
3. **Nível alvo:** 60–120 de −17,6 → ~−11 (fechar 6–7 dB com o rolling; limites: não subir 20–60 mais que
   ~1–2 dB; 120–300 já está a −4,5, harmônicos acima disso estragam).
4. **O resto do gap (1–4 k −16, 4–10 k −22) é GANHO DO TOPO**, não bass — por isso 120–300 deve parar em
   −4,5: mais mordida aí vira congestionamento, o ar vem dos hats.
