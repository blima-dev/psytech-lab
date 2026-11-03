# PML — TECH HOUSE "DRIFT" (TH3) — dissecação

**Fonte:** Production Music Live — "Tech House - Drift" (pack da Production Music Live)
**Análise:** 25/10/2026 · **Método:** contagem e leitura de nomes/caminhos, contagem de `.als` e MIDI. **Nada foi ouvido.**
**Tamanho:** 0,92 GB · **980 arquivos**

É o único pack desta coletânea que trabalha no **Serum** — synth de peso em psytech —, por isso o valor vai além do gênero tech house.

---

## 1. Conteúdo medido

| Material | Quanto |
|---|---|
| Projetos Ableton | **8** (Arson, Brain, Chaos, Ether, Far, Greed, Ring, Work) |
| `.als` totais | 16 (8 principais + 8 backups) |
| Presets **Serum 2** | **152** |
| Presets **Serum 1** (`.fxp`, bônus) | **112** |
| MIDI | **95** (57 no pack de presets + 38 loops melódicos) |
| Amostras WAV | **513** |
| MP3 de demonstração | 59 |
| Pack vocal | 1 pasta (bônus) |

---

## 2. Como os presets estão organizados — e por que isso é útil

Os presets estão **dentro de cada projeto**, na pasta `Presets/Serum 2 Presets`. Ou seja: dá para saber exatamente **qual som pertence a qual faixa**.

| Projeto | Presets próprios |
|---|---|
| Chaos | **20** |
| Arson | 15 |
| Greed | 15 |
| Ether | 13 |
| Brain | 10 |
| Work | 10 |
| Ring | 8 |
| Far | 4 |
| Banco geral `PML - TH3 - Serum2 Presets` | **57** |

### Nomenclatura — dois esquemas conviventes

- **Serum 2 (152):** `PML <FUNÇÃO> <nome> <projeto>` — exemplos reais: `PML BS Distortion Arson`, `PML LD Growl Greed`, `PML PD LFO Brain`, `PML STB Donk Ether`.
- **Serum 1 (112 `.fxp`):** numerado por projeto — `17 - Arson - Bass Pluck`, `18 - Arson - Bass Dist 2`, `19 - Arson - Bass Stab`.

Funções no nome: **BS** = bass, **LD** = lead, **PL** = pluck, **PD** = pad, **STB** = stab. Distribuição no banco geral: BS 22 · LD 16 · PL 11 · PD 6 · STB + numerados no restante.

**Consequência prática:** este pack é legível sem abrir o Live. O nome do preset já diz função, faixa e caráter ("bass distorcido da Arson", "pad com LFO da Brain").

---

## 3. MIDI — duas famílias

| Origem | Qtd | Para que serve |
|---|---|---|
| `Serum Presets/PML - TH3 - Serum Midis` | 57 | o motivo tocado por cada preset |
| `Sample Pack/Loops/Melodic Loops/Midi/Bass Loops` | 18 | loops de baixo |
| `.../Longer Synth Loops` | 11 | loops longos de synth |
| `.../Short Synth Loops` | 9 | loops curtos |

---

## 4. O que este pack ensina que os outros não ensinam

1. **Serum usado em faixa real**, com nome de função por track — para quem produz no Serum, qualquer receita é transferível sem tradução.
2. **Relação preset ↔ projeto:** como cada som foi usado, não só como foi programado. O Cercle e o Tim Engelhardt dão presets ou projetos separados; aqui os dois vêm juntos.
3. **Bônus de compatibilidade (com armadilha):** os 112 `.fxp` são formato Serum 1. Sem o Serum 1 instalado, eles não aparecem no browser — vira acervo morto; é por isso que cada projeto tem uma versão "(Live 11.1 and Serum)" e outra "(Live 11.1 and Serum 2)".

---

## 5. Como usar

1. **Estudar um projeto por função:** `Chaos` é o mais rico (20 presets próprios) e o melhor ponto de entrada.
2. **Importar presets de baixo (`BS`)** para comparar com o patch de sub/baixo do próprio projeto — quando o baixo de referência também é Serum, é o A/B de menor atrito de todos os packs.
3. **Usar os MIDI de bass loop (18)** como referência de ritmo de baixo contra o rolling do projeto.
4. **Ignorar o pack vocal**, salvo se o projeto usar vozes.

## 6. Limites

- Nada foi ouvido; nenhum projeto foi aberto.
- Os 152 presets Serum 2 não foram parseados em parâmetro (o formato é CBOR) — a análise é por nome, caminho e função declarada.
- Os 112 `.fxp` não são carregáveis sem o Serum 1.
- O gênero é tech house, não psytech: o valor está na **técnica de Serum**, não no groove.
