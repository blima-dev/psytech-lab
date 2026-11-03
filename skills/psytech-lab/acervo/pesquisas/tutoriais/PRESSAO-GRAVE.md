# Pressão de grave — tutoriais traduzidos

**Frente:** `pressao-grave` · 16 mapas · **escopo:** motor de um arranjo de referência de 2 minutos a 128 BPM (C# frígio no projeto de referência) · **levantado em:** 27/10/2026.
**Público:** produtor que vai executar. **Nada aqui foi aplicado, renderizado ou medido num projeto real.**

**Use quando** o pedido for:
- "quero mais peso / mais chão sem subir volume";
- "kick e baixo se encavalando" ou "o kick sumiu quando o baixo entrou";
- "uma nota do baixo cancela" / "o grave some no mono ou no clube";
- "o kick tá sem punch e o limiter tá bombeando";
- "quero pressão de sub sem tapete" / "o sub tá ligado o tempo todo";
- "o corpo do baixo não aparece" (sem pedir EQ de médio).

**Números de régua não se repetem aqui.** As medições ficam no projeto que usa este estudo; os parâmetros abaixo são o mínimo para executar.

## Antes de aplicar

1. **Mapear o estado real do projeto de destino** antes de mapear receitas: qual canal é kick, qual é sub, qual é baixo, quais returns existem. Nunca confiar no nome do canal.
2. **Backup antes de qualquer mutação** do projeto.
3. **Reconferir o estado citado.** A leitura original (26/10) descrevia um motor com sub em Operator + Saturator, baixo em Serum 2 + EQ Eight, dois returns (reverb e delay) e sem canal de rolling dedicado — nada disso vale sem conferência atual.

## Regras

- **Bolso, não ganho** — o encaixe kick×grave se resolve em fase, envelope e omissão; fader e EQ vêm depois, e o kick não recebe ganho empilhado para "engordar".
- **Uma fundamental só** — sub, corpo e acento são camadas com funções distintas; o fundamental existe em uma camada e nunca se soma um segundo sub "para engrossar".
- **Evento, não cama** — pressão vem de eventos curtos, filtrados e mono que respeitam os respiros; camada contínua de grave é tapete, não pressão.
- **Fase na fonte, nunca no tempo** — alinhamento é polaridade e fase do oscilador por nota; Track Delay, nudge ou delay no bus destroem o bolso de microtiming (.27/.77).
- **O sub fica seco** — nenhum clipper, drive, widener, reverb ou delay no ramo do sub; drive só band-limited acima de 150 Hz e low-end mono abaixo de 120–150 Hz.

## Receitas traduzidas

Ordem de execução: segurança/fase → kick → fundamental e corpo → bus → pressão pontual → arco.

| Técnica | Fonte/ID | Device/encaixe | Parâmetros | Limite |
|---|---|---|---|---|
| Fase kick×sub×baixo por nota | `nS7CHBL-Bzs` | Utility `Ph` no bus de grave + `Phase`/retrigger do oscilador (Operator no sub, Serum 2 no baixo) | Kick sozinho → kick+sub (`Ph` A/B) → +baixo, por nota, em passos de 45–90°; `Rand` em zero | Sem Track Delay/nudge/delay no bus; nivelar **para baixo** quando a soma subir; onde o kick não toca não há fase a resolver (00:17:05) |
| Mono do low-end sem cortar o Mid | `w1WsSkRLyrU` | EQ Eight M/S no bus de bateria e no master (último insert); Utility `Width 0` no kick e no sub | Low-cut **só no Side** a 120 Hz, 12 dB/oct; auditar subindo até 150 Hz e voltar | Não cortar o Mid; não usar widener/chorus para "recuperar" largura; acima do corte o topo fica como está |
| Kick: EQ subtrativo antes da distorção; Roar multibanda com grave limpo | `xZW3lTHRCxs` | kick: EQ Eight → Roar → Compressor → Utility (gain staging) | EQ só cortando, Q alto; Roar low "soft and clean", tube **só no mid**; compressor 4:1, attack 100 ms, release mínimo | Medir a fundamental do kick antes; sem click de filtro; sem boost 55–75 Hz; não cortar os médios de caráter madeira |
| Kick: ataque por LP24 + envelope de filtro, reverb curto paralelo | `IbeXMrvWAew` | Simpler/Sampler do kick com LP24 + envelope de filtro; rack paralelo EQ Eight + Hybrid Reverb | Varrer o corte 380–550 Hz; ressonância 40–55% (não os ~80% do vídeo); reverb 100% wet com HPF, send só até começar a ouvir | **Pular o rumble**; ressonância larga (Q baixo) para não brigar com a madeira; não inserir segundo limiter às cegas |
| Kick curto + sine sequenciado fora do 1 | `iteUJHS5YNE` | kick (fonte atual) + sub (Operator sine) | Corpo do kick ≤117–130 ms; sine mono; LFO só como modulação de amplitude/posição; glue ataque longo/release curto no bus; compressor de pico no return | LFO não pode criar onset; sem reverb no sub; o kick do vídeo é G — medir a fundamental do kick do projeto antes de copiar afinação |
| Fundamental em uma camada só | `kGfIx2d4oEI` | baixo (Serum 2): Sub + Osc A saw | Sub uma oitava abaixo; saw com 1º harmônico removido (`custom_harmonics`, índice 0 = 0); LFO1 modo envelope unipolar → cutoff; velocity → cutoff | O sub do patch **substitui** o sub existente ou fica mudo — nunca soma; random phase 0 na UI; não usar o 1/16 reto da demo |
| Rolling com articulação de 1/16 | `_W_mwJVDhqA` | baixo (Wavetable/Serum 2); duck por Compressor com sidechain do kick | Saw mono, LP ~200 Hz, Env2 → cutoff +55%, sustain 0, decay = 1/16 a 128 BPM, release 10 ms | Não copiar o corte de médios-baixos/1,2–4 k; não quantizar para 16º reto; tocar nos offsets .27/.77 do bolso de referência |
| Camada média psy (o grave vira articulação de médio) | `Mix6rW9AHgE` | baixo (Serum 2/Wavetable) ou canal novo; HP decidido pela nota | Saw → LPF → Saturator → Multiband Dynamics (só médios) → EQ ~1 kHz → soft clip → reverb curto; Env2 sustain 0 | Máx. 2 estágios de cor; sem o "add sub" do mapa; se houver rumble, só onde há kick e mudo nos respiros |
| Camadas com funções, não 4 instâncias | `yZ-q1H6KaME` | sub (sine, Width 0) + baixo (sine+saw) + camada de corpo no baixo | HP 100–120 entre sub e corpo; saw em volume menor; saturação só no médio; apagar notas cujo onset coincide com o kick | Não dobrar a fundamental; não transpor o sub para buscar médio; LP no saw (~2,5–3,5 kHz) |
| Bassline por LFO/pitch-envelope (sem eventos novos) | `Dcs7r1b6RwI` | sub (Operator sine) + camada de baixo-médio (Serum 2) | Baixo-médio: LFO → WT Pos em Retrig; Env2 → cutoff; velocity e keytrack → cutoff | Saw só no baixo-médio com HP 120–150; sub sine puro; loop de 3 tempos só na resposta, fora de sub/kick |
| Drive band-limited + clipper no bus kick+baixo | `I__tWZTk5-Q` | grupo kick+baixo | EQ8 → drive paralelo HP 150 Hz/LP 1,8 kHz, 20–35% wet → EQ8 pós → Glue 1–2 dB → clipper 1–3 dB → Limiter | Hats/resposta/madeira/stab/subida/atmosfera **fora** do bus; sem Bass Low Extender; medir 55–75 antes/depois |
| Clipper só no ramo de ataque | `R6xwYFH5SSY` | percussão de resposta e ramo de click do kick (Saturator em paralelo) | Digital Clip (hard) ou Soft Sine; HP antes e LP depois (6–8 kHz); blend 10–25%; oversampling | Nunca no sub nem no baixo inteiro; não usar em hats para "abrir" 1,2–4 k; true peak sob controle |
| Noise deslocado como pressão pontual | `h39gdHGGo-c` | camada nova ou percussão de resposta, **fora** do sub | Noise sem grave → Shifter (Frequency Shifter) para baixo → HP 45–60/LP 200–300 → envelope espelhado ao kick → sidechain | Eventos mono 60–200 Hz, curtos, nos offsets do bolso de referência; sem ring mod; Echo só em camada de movimento separada |
| Vazio de kick com duck congelado | `NCY0r4q-QcM` | automação de volume do kick + automação do duck do sub | Rampa de 1/16; kick fora 53–56, volta em 57; sub no mesmo nível ou abaixo; hats caem em 49–52 | Sem delay no shaker/rolling; sem ganho de compensação no retorno; resolver uma oitava abaixo da resolução do vídeo; no respiro do compasso 56 o sub também sai |
| Rampa de 8 compassos (pressão sem volume) | `bOEc9c3pGi8` | EQ Eight em ramo paralelo do kick; Auto Filter no baixo; send da atmosfera | Low-cut automatizado 150–300 Hz no ramo paralelo; cutoff do rolling 300 Hz–1,2 kHz; pontuar em 9/17/25/33/41/49 | Jamais no kick inteiro; não descer o cutoff abaixo de ~250 Hz; não modular o fundamental do sub; ±1–2 dB é adaptação do projeto de referência, não do vídeo |

**Não é técnica de grave:** `NXWjMYYYHGw` (Operator parallel + Shifter ring) é lead/sino inarmônico — usar como resposta/stab de meio com HP 200–300, ring baixo e decay curto; nunca em kick/sub/baixo (00:04:05, 00:05:01).

## Conflitos e cautelas

| Tutorial | O que o vídeo faz | Como adaptar |
|---|---|---|
| `Mix6rW9AHgE` — kick com rumble de reverb + "add a bit of sub"; baixo psy em G0 | Rumble contínuo + sub extra | Rumble só onde há kick e **mudo** nos respiros escritos (compassos 24/32/44/48/56); transpor G0→tônica do projeto; o "add sub" não entra — se o rumble existir, ele **substitui** uma camada, não soma (`Mix6r:158-159`) |
| `_W_mwJVDhqA` — rolling em C#2/G (69,3 Hz), 16º reto | Fundamental em 69,3 Hz | Tocar a articulação em **C#3** (138,6 Hz) com HP 100–120; não empilhar sub; não copiar o corte de 300–4 kHz. A própria nuance do mapa: HP 80–100 "comeria" o C#2 (`_W:147`) — por isso a rota é C#3 |
| `Dcs7r1b6RwI` — saw no sub para gerar harmônicos | Saw no sub | Saw **só no baixo-médio**, com HP 120–150; o sub fica sine puro — o 2º harmônico de C#1 cai em 69,3 Hz, banda sensível do grave (`Dcs7:64`) |
| `NCY0r4q-QcM` — resolver em C#5; LP do stab em 1,2–2 kHz | Registro agudo como resolução | Resolver uma oitava abaixo (C#4 na tonalidade de referência) (`NCY0:71`); manter a lógica de subtração; LP do stab em 3–4 kHz ou automatizado por seção — LP estático ≤3 kHz em canal vivo fecha o topo |
| `bOEc9c3pGi8` — curva de pitch/oitava acima sem teto; Shepard | Subida sem teto | Cap na oitava 4; Shepard só como micro-gesto; não usar pitch de ride como riser (`bOEc:48`) |
| `NXWjMYYYHGw` — ring mod/bell como corpo | Ring mod como corpo | Ring mod só como tempero curto e com LP; madeira com ring off; bell não é corpo; a camada é resposta/stab, não grave (`NXWj:101-103`) |
| `kGfIx2d4oEI` (`:131`) e `iteUJHS5YNE` — "kick afinado em C#" | Afinação do vídeo | O C#2/C#3 é registro do **baixo**; não retunar o kick pela escala do tutorial — medir a fundamental real primeiro |
| `h39gdHGGo-c` — Echo no grupo inteiro do grave | Echo serial no grave | Echo só em camada de movimento separada, com retorno HP acima de ~200 Hz; o núcleo 60–200 Hz fica seco (`h39:82`) |

**Diretrizes provisórias:** o projeto de referência tem regras ainda provisórias sobre cauda em return, corte de 8 compassos e rampa de pressão; onde a provisoriedade muda o veredito, trate como decisão em aberto e confirme com o produtor.

## A/B

Dois blocos de 16 compassos, em volume casado, no contexto da mix. Medir no **export** (não no monitor); captura ao vivo é pista, não prova. Registrar comando e janela.

### A/B 1 — Fase e mono (segurança)

**Alvo:** `nS7CHBL-Bzs` + `w1WsSkRLyrU` + fundamental única de `kGfIx2d4oEI`, em bars 1–16 (0:00–0:30).
**Passos:** (1) baseline; (2) só `Ph`/`Phase` por nota, nivelando para baixo; (3) EQ Eight M/S com low-cut 120 Hz só no Side no bus de bateria e no master; (4) reexportar.

**Aceite:**
- 20–120 Hz idêntico ao baseline (tolerância ±0,2 dB); se cair, havia conteúdo side/fora de fase — investigar fase, **não** subir ganho.
- Correlação sub/baixo abaixo de 120 Hz ≥0,98, pelo mesmo método da medição de referência.
- 30–100 Hz estável entre as 2–3 notas do baixo (nenhuma nota cancela sozinha).
- Onsets `.27/.77` do bolso de referência nas mesmas posições; nenhum Track Delay/nudge.

**Invalida:** qualquer ganho novo no kick/sub; qualquer mudança acima de 150 Hz.

### A/B 2 — Corpo do baixo sem engordar o sub

**Alvo:** `kGfIx2d4oEI` (substituindo, não somando) ou `_W_mwJVDhqA` / `Mix6rW9AHgE`, em um bloco de 16 compassos com kick+sub+baixo tocando juntos (sugestão: bars 33–48, 1:00–1:30; confirmar com o produtor).
**Passos:** (1) baseline; (2) aplicar **uma** receita; (3) reexportar; (4) repetir para a segunda receita só depois de fechar a primeira.

**Aceite:**
- 20–60 Hz idêntico (±0,2 dB) — sub intocado.
- 55–75 Hz não sobe.
- 300–1.200 e 1.200–4.000 Hz sobem contra o baseline.
- 5–12 kHz não salta.
- Onsets `.50/.77` e `.27` idênticos.

**Invalida:** critério de parada: sem ganho no médio, sem mexer em 20–120 Hz e sem apagar o groove, a receita é descartada; não se compensa com EQ.

## Evidência

Os mapas completos por vídeo (um por ID, com timestamps) não acompanham este pacote; os IDs listados identificam cada fonte:

- Fase: `nS7CHBL-Bzs` — alinhamento por nota, sem mover tempo (00:16:10–00:20:35).
- Mono: `w1WsSkRLyrU` — low-cut só no Side (00:02:44–00:03:05).
- Kick (encaixe): `xZW3lTHRCxs` — EQ subtrativo antes da distorção (00:03:38), Roar multibanda (00:04:45).
- Kick (ataque): `IbeXMrvWAew` — LP24 + envelope, res 80% em 485 Hz (00:01:58), reverb curto paralelo (00:04:34).
- Kick/sub (meta-análise): `iteUJHS5YNE` — 10 tutoriais, veredito por fonte e LFO como modulação (16:47, 18:25).
- Fundamental única: `kGfIx2d4oEI` — 1º harmônico cortado (00:04:51), random phase 0 (00:05:04).
- Camadas: `yZ-q1H6KaME` — 4 instâncias, sub isolado, width 0 (00:00:18–00:07:38).
- Bassline por LFO: `Dcs7r1b6RwI` — sine + saw com sustain 0, LFO→WT (02:33–08:28).
- Rolling: `_W_mwJVDhqA` — decay = 1/16 (00:03:47), slot do kick vazio (00:01:24).
- Corpo psy: `Mix6rW9AHgE` — grave vira médio (00:05:20), Env2 sustain 0 (00:08:02).
- Bus: `I__tWZTk5-Q` — cadeia kick+baixo (sem legenda; capítulos/descrição).
- Clipper: `R6xwYFH5SSY` — clip sem envelope, limiter quando não quer distorcer (00:02:37, 00:08:58).
- Pressão pontual: `h39gdHGGo-c` — noise deslocado, envelope espelhado (00:03:03–00:03:43).
- Arco/vazio: `NCY0r4q-QcM` — kick fora, resolução no groove (00:02:42–00:07:59).
- Rampas: `bOEc9c3pGi8` — low-cut de 8 compassos no kick (00:07:47).
- Fora do grave: `NXWjMYYYHGw` — lead/sino; ring mod (00:03:41).

## NÃO VERIFICADO / pendências

**Não verificado:** estado atual do projeto de destino (a leitura citada é da data do levantamento); fundamental real do kick; o que o patch do baixo produz de fato; se o sub é ducked pelo kick; se existe grupo de graves nomeado; nenhum A/B, render, escuta ou medição de áudio. `kSpectralShift` (h39) não foi testado em áudio; random phase 0 e splitter/Hyper Dimension do Serum 2 ficam na UI (kGf); o "Roar" de `I__t` pode não ser o device nativo, e Soothe 2 não tem equivalente nativo exato — a cadeia do bus é proposta, não transcrição.

**Decisões em aberto no projeto de referência** (fundamental do kick, alvo de relação sub×kick, régua de medição, registro agudo, cauda em return e corte de 8 compassos) não vêm aqui como critério fechado: meça no projeto de destino e decida com o produtor.
