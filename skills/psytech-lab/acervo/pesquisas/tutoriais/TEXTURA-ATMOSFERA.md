# Textura e atmosfera — tutoriais traduzidos

**Frente:** textura-atmosfera · **16 mapas** · **compactado em:** 27/10/2026.

**Natureza:** leitura dos mapas, que são leitura de legenda/ASR. Nenhum áudio de vídeo foi ouvido como fonte musical, nenhum A/B rodou e nada foi tocado num projeto real nesta sessão. Aqui só entram o parâmetro que decide o encaixe e o limite, sem repetir a régua numérica.

**Contexto fixo desta frente:** no projeto de referência (leitura de 27/10) havia 16 pistas MIDI + 2 returns e **nenhum canal granular**; a camada nasce em **canal novo** ou reaproveita as camadas de **madeira (Operator)** e **percussão de resposta (Simpler)**. Diretriz de caráter: granular de **sample acústico**, não sci-fi digital.

## Use quando

Consultar antes de propor qualquer coisa que ocupe o meio ou o fundo: cama granular, drone, pad, camada de ruído, resposta granular, throw/atmosfera em return, ou quando for decidir **em que canal** essa camada nasce. Também serve para barrar receita de tutorial que quebra a escala de referência (frígio sobre a tônica do projeto), o registro médio-grave, os respiros ou o bolso `.27/.77`.

## Regras

- **Textura com buraco.** Nenhuma cama é permanente: entra e sai por seção, e o silêncio faz parte. Preserva os respiros de kick já escritos no arranjo de referência perto de **0:44–0:45** e **0:59,5–1:00** e não cria hit nos acentos `.27/.77`. Base: QLPV1Wk5hoE estende o loop para não retriggerar o tempo todo (00:05:53.4) e usa o filtro como ferramenta de arranjo (00:05:32.6); lHGfb5Hlmuc desliga o LFO para criar tensão (00:06:19.8).
- **Fonte acústica primeiro.** O grão nasce de madeira, voz, guitarra ou gravação de campo; fonte escura vence filtro corretivo. Granular não entra em kick, sub, baixo ou hat — só acima do HP, em cama ou resposta. Base: JNAyJa_Dcx0 (grão é fatia de sample, 00:13:07–00:13:18), QLPV1Wk5hoE (voz/orgânico, 00:00:46.9), f4tdX3LsKj0 (escolher o sample é o ponto, 00:04:26.8).
- **Pitch travado.** `random_pitch` = 0 no drone e no máximo ±2 st na textura; a variação vem de posição, comprimento de grão e pan, nunca de afinação. vREN7ACIcFc é literal: não mexer no pitch porque o drone precisa servir melodicamente (00:00:59.5). Transpor oitava é decisão de registro, não de aleatoriedade.
- **Cauda em return, envio em pulso.** Reverb/delay 100% wet em return dedicado, alimentado por pulsos curtos de send na resposta ou no fim de frase; kick, sub e baixo com send zero. É a diretriz de cauda do projeto de referência (provisória) e é literal em sTizY7Qln78: "não posso mandar tudo estático" (00:03:29.1), "mandei bem curto" (00:04:10.5).
- **Uma cama, camadas dela.** As 3–4 camadas do li-Oed1DWck são camadas de **uma** cama, não três pads independentes; o QLPV1Wk5hoE pede uma fonte e silêncios. Empilhar camas independentes vira colchão e mascara madeira e resposta.

## Encaixe no projeto

- **Cama/drone:** canal novo (Serum 2 GranularOsc ou Granulator 3). Não existe canal granular por padrão — nome e grupo são decisão do produtor do projeto de destino.
- **Resposta granular:** percussão de resposta (Simpler, clipes de resposta já existentes) ou madeira (Operator), printando o material do próprio canal.
- **Dobra do motivo/baixo:** layer no **baixo** (Serum 2 + EQ Eight), com filtro e nível próprios. Não é canal granular.
- **Cauda:** usar o return de reverb existente para o throw; return dedicado só se o A/B mostrar que o return atual não serve.
- Nomes de canais/returns citados nos tutoriais (ATMOSBED, "Organic Atmos (Bed)", "05. ATMOS BUS", GRANULATOR, DRONEGRAN) **não existem por padrão** — o encaixe depende do projeto de destino.

**Escolha rápida:** cama contínua → playheads deslocados (li-Oed) ou drone de pitch travado (vREN); corpo tonal sem ataque → pad dark (Hzszjbt/90V) ou noise+drone (lHG); responder ao groove → granular percussivo (f4td); colar fronteira → return com pulsos (sTiz); engrossar o motivo sem criar ataque → dobra filtrada (BjDkk).

| técnica | fonte/ID | device | parâmetros | limite |
|---|---|---|---|---|
| **teoria do grão** (não é receita) | JNAyJa_Dcx0 | nenhum | grão = fatia curta com pitch/velocidade/direção/volume próprios; dezenas sobrepostas (00:12:14.7, 00:13:07.2) | aula conceitual, sem DAW e sem parâmetro demonstrado; não gera preset |
| **cama granular de playheads deslocados** | li-Oed1DWck | Serum 2 GranularOsc (canal novo) ou Granulator III | grão longo + densidade alta = liso (00:01:19.4); offsets por camada (00:04:02.4); pan 35–50%; HP 250–300; LP 7–9 kHz | o gerador **não escreve** SCAN/playhead; 4 playheads = GUI ou 2–3 instâncias; sem voz −1 oitava no motor (00:06:24.9) |
| **drone granular de pitch travado** | vREN7ACIcFc | GranularOsc / Granulator III | grão 150–300 ms; `random_pitch` 0 (00:00:59.5); reverse ~50/50 em duas camadas (00:02:38.4); HP **antes** do reverb (00:06:27.0) | `granular_reverse` é booleano, não mix; janela do grão só na GUI; nível −18/−24 dB é proposta do estudo, não fala do vídeo |
| **cama de fonte orgânica, 8 vozes** | QLPV1Wk5hoE | GranularOsc | 8 vozes/uníssono (00:02:55.1); start point diferente por voz (00:03:28.2); loop fwd/back (00:02:12.5); filtro automatizado por seção (00:05:32.6) | ping-pong do sample **não existe** no GranularOsc; "por voz" vira "por grão"; uma cama, não três |
| **granular falso por warp Texture + resample** | 4q6GrRSEfhI + 4TOQ-5mGpUY | clipe de áudio Live (Warp Texture) → resample → GranularOsc | Flux 0 e Grain Size 226 no Live (00:03:38.1); esticar ao máximo (00:04:02.7); +12 antes do scan (00:03:16.5); HP 180–250 | "226" é unidade do Live, **não ms**; esticamento tem teto (ZSv 00:15:27.4); artefato no topo (00:07:21.9) |
| **noise + drone com LFOs independentes** | lHGfb5Hlmuc | Serum 2 Noise (Pink/Brown) + drone | HP ~280–300; LP 4–5 kHz; rates lentos e diferentes (00:04:46.8); LFO no volume (00:04:30.4) | LFO não trava fase: dois renders não saem iguais; não é cama permanente; White tende a aspereza |
| **atmosfera em return com pulsos de send** | sTizY7Qln78 | return (reverb existente ou novo) | Hybrid Reverb 100% wet, decay longo (00:01:22.9); Shifter lento (00:01:19.1); send em pulso curto (00:04:10.5); kick/sub/baixo com send zero | sem Soothe; Redux desligado; os nomes de bus do vídeo não existem por padrão; diretriz provisória no projeto de referência |
| **pad tonal dark em duas camadas** | Hzszjbt_c9I + 90VpsmIaPuk | Live Wavetable ou Operator parallel | ataque longo (01:31.0); LFO pitch/filtro (02:31.4, 03:31.8); unison shimmer (04:40.5); ratios 1×/2×/3× → 0/+12/+19 sobre C#2 (00:03:22–03:52) | +6 sai da escala de referência; LP 2–3 kHz só por seção; HPF 90 vs 160 em aberto; feedback 50% não tem equivalente no Serum |
| **madeira plucky que preenche o meio** | Wmr4dnvhVkc | Serum 2 / madeira (Operator) | saw + camada de caráter (00:04:03.7); dois filtros em série (00:08:21.0); Env2 plucky (00:08:41.7); Q baixo; macro no decay (00:09:24.0) | −2 oitavas só no miolo com HP; não copiar a tônica D do vídeo (00:03:11.6); sem LPF ressonante de trance (00:06:29.3) |
| **granular como percussão de resposta** | f4tdX3LsKj0 | Granulator 3 (Suite) ou GranularOsc na percussão de resposta/madeira | loop on (00:03:21.6); grão 60–120 ms na resposta e 100–160 na madeira; LFO no grain size (00:04:16.9); 16avos staccato (00:06:33.6); 1 pergunta + 1 resposta a cada 2 compassos (00:08:13.5) | Granulator 3 **não verificado** no ambiente de origem; um hit por buraco, sem sobrepor as camadas (00:07:43.2); HP ~276 |
| **dobra filtrada do motivo/baixo** | BjDkkB8ElnY | duplicar a pista do baixo (mesmo clip) | cortar todo o grave (00:03:04.1); LP ~5–6 kHz; Roar leve (00:03:14.2); LFO lento (00:03:45.7); nível abaixo do original | herda os offsets do bolso por construção; bitcrush só no terceiro plano; não criar ataque novo |
| **drone por acorde 7(b5)** | nU3udPVlJGg | Chord / Operator / Serum | sem a nota de baixo (03:26); oitava 4; HP 250–350; sidechain lento do kick (09:07); dois AutoPan (09:36); reverb em return (11:18) | o acorde do vídeo sai da escala de referência — só em A/B rotulado; não sincronizar LFO ao grid; o "industrial metallic" do vídeo (07:43) não é o alvo |

## Conflitos e cautelas

Dos 16 mapas, 15 alinham e 1 é neutro; a tabela abaixo reúne o que **não pode ser copiado literalmente** e a conciliação.

| tutorial | o que o vídeo faz | como adaptar |
|---|---|---|
| **Hzszjbt_c9I** — segundo oscilador a +6 st, trítono (02:04.2–02:07.2) | +6 sobre a tônica sai da escala de referência | Usar **+1 (b2)** ou **+5 (5ª acima)**; o trítono b2–5 só em A/B rotulado, nunca como produção. |
| **nU3udPVlJGg** — acorde dominante 7(b5) (01:15–01:39) | Tensão dominante | Produção em acorde dentro da escala de referência; a versão do vídeo só no teste, como o próprio mapa avisa. |
| **v-mjY-Vlgv0** — padrão MIDI em 0/+6 st (07:47.0) | Intervalo fora do modo | Trocar +6 por **+7 (5ª)** ou **+1 (b2)**; o mapa já propõe. |
| **li-Oed1DWck** — voz −1 oitava (00:06:24.9) | Grave da cama | Fora do motor. Se usar em breakdown, HP 250–300; o mapa já recomenda evitar. |
| **li-Oed1DWck + 4TOQ-5mGpUY + 90VpsmIaPuk** — voz +1 oitava, +12 e ratio 4× | Registro agudo | Só se o root for **≤ oitava 3**, para o resultado ficar na oitava 4; nada acima. Nos ratios, base na oitava 2. |
| **ZSvJlc3LRqo** — gate de 1/8 do warp Beats (00:07:38.8–00:08:20.6) | Gate em grade reta | Só em camada independente; nunca no shaker nem em quem carrega o bolso. |
| **4q6GrRSEfhI** — cópias transpostas −5 e −8 st (00:06:50.1, 00:07:00.9) | Transposição fora do modo | Reafinar as cópias à escala de referência; o intervalo do vídeo é movimento, não tonalidade. |
| **Hzszjbt_c9I** — LP 2–3 kHz nos primeiros 16 compassos | LP estático | LP **por seção**, com abertura automatizada; LP estático ≤3 kHz em canal vivo fecha o topo. |
| **sTizY7Qln78 + BjDkkB8ElnY** — Redux 8-bit e bitcrush (sTiz 00:02:03.9; Bj 00:03:22.2) | Timbre digital | Desligado por padrão; se ligar, só terceiro plano, blend baixo, LP 6–8 kHz e A/B contra o dry. |
| **sTizY7Qln78** — cauda da atmosfera atravessa a virada (00:05:11.4) | Cauda sobre o drop | Só atmosfera **sem elemento de impacto**; automatizar o send a zero no downbeat do drop. Stab/lead/braam não atravessam. |
| **f4tdX3LsKj0** — hits granulares em 16avos (00:06:33.6) | Densidade percussiva | 1 hit por buraco a cada 2 compassos, como o mapa manda (00:08:13.5, 00:10:04.2); nada nos respiros; "não exagerar" é fala dele (00:09:57.8). |
| **BjDkkB8ElnY** — dobra do motivo (00:02:57.0) | Duplicata | A dobra herda o MIDI e fica em terceiro plano; não virar segunda melodia na mesma oitava. |

## A/B

Dois testes, 8 compassos cada, em contexto de Arrangement e com ganho percebido casado. Medir no export, não no monitor.

**A/B 1 — cama granular vs. sem cama (bars 17–24, 0:30–0:45).**
Ligar/desligar o canal novo por mute, mantendo o resto igual. Critério: com a cama ligada, 20–120 Hz e a correlação do grave **não se movem** dentro do erro de medição; 300–1.200 e 1.200–4.000 **sobem**; 5–12 kHz **não salta**; o respiro de 0:44–0:45 continua vazio. Reprovam os dois extremos: cama que não muda nada quando mutada (decoração) e cama que desmonta o trecho quando mutada (peso demais).

**A/B 2 — resposta granular na percussão de resposta vs. resposta seca (bars 25–32, 0:45–1:00).**
Printar 1–2 compassos do próprio canal de resposta, grão 60–120 ms, loop on, HP ~276; uma pergunta e uma resposta a cada 2 compassos, **substituindo** eventos. Critério: a contagem de transientes **não sobe**; nenhum hit cai nos acentos `.27/.77`; o último hit acontece **antes de 0:59,5**; 20–120 Hz idêntico. Se o desenho do groove borrar, reprovar mesmo que o médio suba.

## Evidência

Os mapas completos por vídeo (um por ID, com timestamps) não acompanham este pacote; os IDs listados identificam cada fonte: JNAyJa_Dcx0 (definição de grão), li-Oed1DWck (playheads deslocados), vREN7ACIcFc (drone pitch travado), QLPV1Wk5hoE (cama orgânica 8 vozes), ZSvJlc3LRqo (warp modes), 4q6GrRSEfhI (Texture + resample), 4TOQ-5mGpUY (resample→granular), nU3udPVlJGg (drone 7(b5)), 90VpsmIaPuk (Operator parallel ratios), v-mjY-Vlgv0 (stab/pluck Wavetable), lHGfb5Hlmuc (noise+drone), sTizY7Qln78 (atmosfera por sends), Wmr4dnvhVkc (madeira plucky), Hzszjbt_c9I (pad dark), f4tdX3LsKj0 (Granulator percussivo), BjDkkB8ElnY (dobra filtrada).

## NÃO VERIFICADO / pendências

- **Nenhum A/B foi executado** e nenhum áudio foi medido nesta sessão; todos os critérios acima são protocolo, não resultado.
- **Granulator 3 / Max for Live / Suite** não foram verificados no ambiente de origem. A rota existe no papel; confirmar no browser antes de prometer.
- **O gerador de presets não escreve o SCAN/playhead** do GranularOsc. Offset estático por playhead exige GUI ou 2–3 instâncias; não prometer preset com esse controle.
- **`granular_reverse` é incerto** no schema. Preferir reverter o WAV na fonte.
- **Ping-pong do sample não existe** no GranularOsc; `granular_loop` é loop dentro do grão.
- **"Grain Size 226" é unidade do Live, não ms**; não transportar o número para o Serum.
- **Preset granular depende do WAV**: o engine copia o arquivo para a Samples library do Serum; se o preset circular, o WAV tem de ir junto.
- **HPF do drone em aberto:** as fontes divergem entre 90 e 160 Hz. Decidir no projeto de destino.
- **Diretrizes provisórias no projeto de referência** (cauda em return, corte de 8 compassos) e a régua do médio em aberto: nada aqui as trata como homologadas.
- **Canal, nome e grupo da cama** são decisão do produtor do projeto de destino. Não criar pista, return ou automação sem OK.
- **LFOs não travam fase:** dois renders do mesmo estado não saem iguais. Para A/B, congelar em automação de volume ou comparar dentro do mesmo render.
- **O projeto de destino pode ter mudado** depois da leitura de 27/10. Reconferir antes de criar qualquer canal.
