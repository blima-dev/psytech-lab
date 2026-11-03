# Fox → projeto de referência: mapa de continuidade (07/09/2026)

> Estudo do acervo psytech-lab, anonimizado. O original trazia o inventário completo de 36 pistas/grupos do
> set (cadeias por pista, nomes de canal) e a infraestrutura de automação do autor — essa parte é
> estado/infra pessoal e foi removida. Ficam as referências Fox (externas), as medições, o mapa por função,
> o contrato de trabalho e as limitações metodológicas do uso de stems Demucs.

**DECISÃO registrada:** Fox (Artemis (AR) Remix) é a referência; manter o método de separação por elemento
para aprender de ouvido.

**VERIFICADO (leitura do Live):** 132 BPM, 36 pistas/grupos (30 pistas + 6 grupos) e 3 retornos; nenhuma
alteração no set nesta rodada. Inventário das cadeias no nível principal; parâmetros internos, automações e
presets não foram auditados.
**NÃO VERIFICADO:** correspondência auditiva, qualidade dos timbres, BPM/tom da referência e alinhamento do
edit à faixa integral. Nomes de clips indicam intenção; não provam resultado sonoro.

## 1. Referências Fox disponíveis (tabela de estudo)

| Arquivo | Duração medida | Uso |
|---|---:|---|
| `Fox (Artemis (AR) Remix).mp3` | 393,744 s | Referência integral: arco, densidade e balanço geral |
| `Fox (Artemis (AR) Remix) - Instrumental 3min ref.mp3` | 180,036 s | Apoio para ouvir instrumentação |
| `Fox - Bass oitava-acima ref.mp3` | 180,016 s | Apoio para perceber ritmo/notas; NÃO usar como régua de subgrave |
| `Fox (Artemis (AR) Remix) - Edit Drop Maior 3min.mp3` | 180,000 s | Edit curto: comparação de energia; não presumir timestamps da integral |
| `htdemucs/…/other.mp3` | 180,036 s | Restante extraído: synths, atmosfera e efeitos possivelmente misturados |
| `htdemucs/…/bass.mp3` | 180,036 s | Baixo extraído do edit: ritmo, duração e movimento |
| `htdemucs/…/drums.mp3` | 180,036 s | Bateria extraída do edit: groove e ataques |
| `htdemucs/…/vocals.mp3` | 180,036 s | Vozes/resíduos extraídos; presença do arquivo não exige adicionar vocal |

Medição (ffmpeg volumedetect; **não é LUFS**): média no arquivo inteiro −8,7 dB na integral, −15,8 dB em
bass, −12,9 dB em drums, −18,6 dB em other e −30,3 dB em vocals. **Não comparar esses números diretamente
com o volume das pistas do set.** Métricas antigas em trechos não substituem esta medição integral.

## 2. Limitações dos stems Demucs (regra de leitura)

- Os quatro stems são **separações do edit de 3 min**, não pistas originais de produção, e não a timeline
  integral.
- **Não há kick, hat e clap isolados** nesses quatro arquivos.
- O bass "oitava acima" é uma referência **alterada** — nunca régua de sub.
- Samples de outros packs na mesma pasta não são elementos de Fox.
- **Não equiparar picos/níveis absolutos do MP3 masterizado aos sinais isolados pre-limiter do set.**

## 3. Mapa por função — onde ouvir e onde trabalhar

As correspondências abaixo são **INFERÊNCIAS funcionais** pelos stems. A coluna de escuta define perguntas,
não defeitos já diagnosticados.

| Elemento em linguagem simples | Referência Fox | O que comparar / intervenção mínima possível |
|---|---|---|
| Kick / bumbo: batida que dá o impacto | drums + integral | Ataque e duração; avaliar Simpler/Drum Buss existentes antes de trocar instrumento |
| Hi-hat aberto: abertura entre batidas | drums | Cauda e espaço; envelope do Simpler e EQ existentes |
| Hi-hat fechado: pequenos impulsos do groove | drums | Pausas e intensidade; distinguir ritmo de problema de timbre |
| Clap / palma e percussão: balanço | drums | Resposta ao kick; Simpler no clap e áudio já pronto na percussão |
| Ride / prato: brilho sustentado | drums | Entrada e duração; Drum Rack 909 existente |
| Subgrave: peso mais profundo | bass + integral | Relação com kick e cauda; Serum 2, filtro e Utility existentes |
| Baixo médio: parte do baixo que "fala" | bass; other como apoio | Movimento e presença; Serum 2, filtro, EQ, Saturator e Chorus existentes |
| Acordes curtos: ataques de synth | other + integral | Timbre, pausa e resposta; cada variante já pode receber tratamento próprio |
| Melodias e respostas: conversa entre synths | other + integral | Escolher uma voz por vez; não preencher todas as pistas com novos VSTs |
| Atmosfera: som de fundo sustentado | other + integral | Profundidade e espaço; áudio com Serum 2 FX e filtro — não falta instrumento gerador |
| Transições e cortes: anunciam ou interrompem a volta | other, drums e integral | Contraste na entrada/saída; distinguir efeitos em áudio de notas do Serum |
| Voz | vocals + integral | Adicionar só se houver intenção musical e necessidade auditiva |

## 4. Forma de trabalho preservada (contrato por rodada)

O produtor define intenção e aprova pelo ouvido → escolhe-se uma pergunta → coleta só os fatos ausentes →
1–2 análises apenas quando existir decisão material → um executor escreve no Live → leitura real confirma →
áudio A/B → manter ou desfazer.

Contrato por rodada: **TARGET / REGION / CHANGE / DO-NOT-CHANGE / ACCEPTANCE**. Uma hipótese e uma mudança
material. Nomes claros, variantes em linhas próprias e subgrupos. Não adicionar camadas ou trocar VSTs em
massa. **Não copiar melodia, hook ou composição da referência.**

## 5. Próxima rodada concreta (método do caso)

1. Comparar **other + integral de Fox** com um canal de stabs já separado (região existente de 4 compassos,
   beats 192–208). É um candidato curto por já estar separado e usar Serum; não é diagnóstico de que seja o
   maior defeito.
2. Ouvir e identificar UMA diferença material (por exemplo duração ou movimento), em volume percebido
   comparável. Localizar um trecho correspondente em Fox por função musical; não alinhar automaticamente os
   tempos do edit e da integral.
3. Só então escolher um parâmetro/efeito ou mudança de preset que teste essa diferença. Priorizar controle já
   disponível se suficiente; se exigir interior do Serum, validar a ligação real do host nesse elemento antes
   de substituir a instância atual.
4. Guardar A/B curto, confirmar estado final e obter decisão estética do produtor. A seleção definitiva da
   intervenção depende da escuta — métricas e consenso de agentes não aprovam música.

## 6. Evidência e limites

- Snapshot do Live (pistas, grupos, cadeias e posições) e inventário dos oito arquivos de referência
  (duração, canais, sample rate, volume integral) registrados no projeto.
- Nenhuma audição simulada: esta rodada entrega mapeamento operacional, não análise estética concluída.
- Nenhuma mutação no Ableton, preset, áudio ou configuração global nesta rodada.
