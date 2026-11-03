# Motor completo — tutoriais traduzidos

**Data do levantamento:** 27/10/2026 · **frente:** motor-completo (7 mapas) · **nada foi aplicado num projeto real; nenhum A/B foi executado.**

## Use quando

Vai mexer no motor dos dois primeiros minutos — kick, sub, corpo e articulação do baixo, resposta percussiva, stab de apoio e entrada de seção — e precisa da técnica dos walkthroughs psytech/minimal já traduzida para Serum 2 + Live 12, sem refazer a pesquisa.

Não use esta frente para melodia, textura granular, arranjo dos 7 minutos ou master. O contexto medido que orienta tudo abaixo: no projeto de referência, o grave já é mono e correlacionado, e o déficit está no corpo — 300–1.200 Hz em −4,83 dB e 1.200–4.000 Hz em −5,76 dB contra a média de 6 referências externas. Por isso a receita é de **conteúdo e articulação**, não de mais sub nem de EQ estático.

## Regras

- **um dono de sub** — a camada de sub existente continua sendo a única dona do extremo grave; toda camada extra do baixo é harmônico/médio. Se um patch traz Sub próprio, ele substitui a camada de sub existente ou fica mudo; nunca soma.
- **fase antes de timbre** — antes de EQ, drive ou camada nova, conferir polaridade kick×sub×baixo e desligar randomização de fase no sub. O A/B é no áudio renderizado, não no clipe MIDI.
- **duck por banda** — sidechain só na faixa que colide com o kick; o médio do baixo fica seco e "fresco", sem o bombeamento óbvio do baixo inteiro.
- **substituir, nunca somar** — cada receita entra no lugar de um evento ou camada existente; não criar nota, hat ou camada nova só para preencher banda. Densidade já está acima do teto medido.
- **a arquitetura, não o timeline** — do Pspiralife copia-se a célula de 1 beat, os loops curtos×longos e a resposta rara; o "drop no compasso 17" do vídeo não é o drop do projeto de referência (correção na tabela de cautelas).

## Receitas traduzidas

Valores são **ponto de partida** (hipótese/inferência de tradução); só os timestamps são verificados no mapa.

| Função | Receita | Encaixe / valor de partida | Prova (mapa · timestamp) |
|---|---|---|---|
| Kick | Utility mono; EQ corta as duas pontas; Drum Buss `Transients` para o ataque; limiter como densidade, não volume. O bell de transiente é estreito, nunca shelf. | kick · mono <130 Hz; ataque ~1 kHz | Fx3jM4xdw4M 00:05:07–00:06:20; S0DRqIEXW_4 03:50–04:01 e 04:26–04:28 |
| Afinação do kick | Medir a fundamental com boost estreito + Spectrum e só então decidir; a escala se escolhe pela nota medida, não o contrário. Não copiar afinação de tutorial. | kick · leitura, sem retune | TwZk8Gcyl1E 03:41–04:20; n2rdb-8fQ9c 00:02:52–00:03:02 |
| Sub | Randomização de fase desligada; imprimir a camada low em áudio para repetição idêntica; HPF antes e depois de qualquer drive; nenhuma segunda sine. | camada de sub · Freeze & Flatten/Resample | GyhA92cfQgE 06:39–07:07; TwZk8Gcyl1E 05:11–06:26; n2rdb-8fQ9c 00:06:32–00:06:55 |
| Corpo do baixo | Sine carrega a fundamental + saw sem a fundamental (Serum 2 `custom_harmonics`, índice 0 = 0); reforço de presença no próprio baixo; cortar graves do baixo para não clashar com o sub. | baixo (Serum 2) · layer interno | GyhA92cfQgE 06:01–06:23; Fx3jM4xdw4M 00:13:14–00:13:30; TwZk8Gcyl1E 00:10:31–00:10:38 |
| Duck e grupo | Rack divisor no baixo: chain LOW com Compressor sidechain kick, chain HIGH seca. Grupo de graves: Glue + Bass Mono; duck só nas camadas que competem. | baixo e grupo de graves · duck 20–200 Hz; mono 178 Hz (valor do vídeo, ponto de partida) | Fx3jM4xdw4M 00:12:13–00:15:20; TwZk8Gcyl1E 00:12:23–00:13:17; ed5ODapIIBc 00:07:59–00:08:04 |
| Resposta | Ghost kick só de médio (mesmo sample, band-pass, sem grave) nos slots de resposta; resposta rara, não ping-pong por compasso; dois patches quase iguais chamando/respondendo. | percussão de resposta/madeira · 1 evento a cada 8 compassos | ed5ODapIIBc 00:04:34–00:05:05; ORj8Vgu2vNs 00:59:05–01:06:09; n2rdb-8fQ9c 00:14:22–00:15:20 |
| Stab | Curto e afiado, sem sustain; wavetable + Resonator + Auto Filter automatizado para "entrar" na track; band-pass perto da fundamental. Sem FM metálico/Shimmer e sem pitch envelope fora do modo (ver cautelas). | stab · 400–900 Hz | S0DRqIEXW_4 23:50–23:57; ed5ODapIIBc 10:22–11:24 |
| Subida | Reverse do próprio som que vai entrar (freeze+flatten/resample), alinhado no acento — não um riser novo; alternativa: automação de pitch ou de delay time descendente + feedback. | stab/madeira/atmosfera · antes do acento | S0DRqIEXW_4 33:09–33:40 e 34:21–34:50; ORj8Vgu2vNs 28:40–29:32; n2rdb-8fQ9c 19:47–20:15 e 26:04–26:32 |
| Hats | Closed com acentos de velocity, open no offbeat, um "tipo shaker"; par complementar L/R com padrões diferentes; cortar aspereza em vez de realçar. Hat como marcador de seção, não camada de brilho. | hats/shaker · ~6 kHz de corte; substituir evento, não somar | S0DRqIEXW_4 04:41–05:48; n2rdb-8fQ9c 30:03–31:03; ORj8Vgu2vNs 46:55–47:03 |
| Atmosfera | Em return: reverb com HP no médio do kick/baixo, wet automatizado por seção; low cut no sample e corte de graves do side. Não é cama de grave. | returns · HP/LP no retorno | ed5ODapIIBc 03:59–04:04 e 06:51–07:14; ORj8Vgu2vNs 19:26–20:19 e 15:40–15:44 |

**Ordem de ataque:** segurança (fase/mono) → duck por banda → corpo harmônico do baixo → resposta/articulação. Uma mudança por A/B; nada de aplicar Redux, delay e sidechain de uma vez.

## Conflitos e cautelas

| Tutorial | O que o vídeo faz | Como adaptar |
|---|---|---|
| **S0DRqIEXW_4** — pitch envelope de 33 st no stab (00:20:51–00:20:56) | Envelope de pitch atravessa quase 3 oitavas | Cortar para ≤12 st e terminar em nota da escala; se o gesto precisa de "queda", usar filtro/ruído, não pitch. |
| **S0DRqIEXW_4** — stab FM + Shimmer (00:24:18–24:35) | Timbre metálico digital | Stab analógico/curto com LP; Shimmer fora; FM só como tempero curto e filtrado. |
| **S0DRqIEXW_4** — rumble de delay sob o kick (00:02:22–02:34) | Rumble contínuo | Rumble só onde há kick e mudo nos respiros escritos; medir a janela, não confiar em "parece mudo". |
| **ORj8Vgu2vNs** — "drop no compasso 17" (00:06:24–06:31) | Timeline do vídeo | Usar a arquitetura (célula de 1 beat, loops curtos×longos, resposta a cada 8), não o timeline: o encaixe temporal do drop é do macro-arranjo de cada projeto. |
| **TwZk8Gcyl1E** — Auto Pan citado como sidechain do grupo (00:11:25–11:38) | AutoPan no grave | Não usar AutoPan no grave (o próprio mapa avisa); usar Compressor com sidechain ou rack de banda; AutoPan só em topo. |
| **TwZk8Gcyl1E** e **n2rdb-8fQ9c** — kick afinado pela escala / kick em A a 55 Hz (TwZk 03:52–04:16; n2rdb 00:02:52–00:03:02) | Afinações divergentes | Medir a fundamental real do kick do projeto antes de qualquer retune; não copiar 55 Hz nem "C#". |
| **GyhA92cfQgE** — trata o sub−kick como "dentro do envelope" | Régua de sub do vídeo | O alvo de relação sub×kick é decisão do projeto de destino; nenhuma régua citada vale universalmente — o A/B mede, não escolhe o alvo. |

## A/B

**A/B 1 — fase e mono do low end (GyhA + TwZk).** Em 8–16 compassos com kick+sub+baixo, cópias de audição em volume casado: A/B de polaridade (Utility `Ph` / fase do oscilador) e randomização de fase desligada no sub. Critério: perda ao somar em mono ≤3 dB em 25–120 Hz e correlação ≥0,98; onsets `.27/.77` do bolso de referência idênticos. Se não houver ganho — a medição de referência já encontrou o grave correlacionado —, registrar e não manter o flip.

**A/B 2 — corpo do baixo com uma fundamental (GyhA).** No baixo, A/B de 8–16 compassos: sine de fundamental + saw sem fundamental (`custom_harmonics`, índice 0 = 0), patch atual preservado. Critério: a faixa de corpo medida sobe; 20–60 Hz e 55–75 Hz não sobem; onsets `.50/.77` e contagem de notas idênticos. Se 55–75 subir ou a relação com o sub piorar, descartar.

## Evidência

Os mapas completos por vídeo (um por ID, com timestamps) não acompanham este pacote; os IDs listados identificam cada fonte: S0DRqIEXW_4 (Audioreakt, template peak time 100% stock), GyhA92cfQgE (Verschallt, low end em 3 camadas e fase), TwZk8Gcyl1E (Wachter & Böhm, 4 camadas em 2 subgrupos e duck por frequência), Fx3jM4xdw4M (SLUG, kick/baixo/bus de grave), ed5ODapIIBc (Michael Nox & Robin Mind, cadeias paralelas por banda), ORj8Vgu2vNs (Pspiralife, arquitetura de loops e colocação), n2rdb-8fQ9c (Durosai, kick, sub estéreo/HPF, call/response).

## NÃO VERIFICADO / pendências

- **Nenhum A/B executado e nenhum áudio dos vídeos escutado.** Os 7 mapas são leitura de legenda automática/ASR/descrição; "o vídeo diz" não é "o som funciona".
- **Cobertura incompleta da frente:** S0DR é parte 1 (arranjo/mix ficam para o próximo); Fx3j e TwZk cobrem só o grupo de graves; ed5O não trata hats/madeira/pad; GyhA não trata hats/percussão/madeira/stab/arranjo; ORj8 não desenha timbre. Nenhum vídeo sozinho fecha o motor.
- **Estrutura do kick não inspecionada no projeto de destino:** as duas camadas do TwZk seriam mudança estrutural, não preset.
- **Randomização de fase no Serum 2:** o controle é citado pelo GyhA, mas nome/caminho na UI não foram verificados; splitter e Hyperdimension do n2rdb também ficam para a UI do plugin.
- **"Low extender" e Auto Pan como sidechain:** o TwZk não dá valores; o preset não foi localizado na instalação.
- **OTT não é device nativo do Live** (citado pelo ed5O); Multiband Dynamics reproduz o conceito, não o algoritmo.
- **Os números de banda citados vêm da medição de referência da data do levantamento**, referentes àquela versão do projeto; não foram re-medidos nesta consulta.
