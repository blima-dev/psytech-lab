# Pesquisa — automação do Ableton Live: o que a API oficial (LOM) cobre e como operar com segurança

**Data:** 13/10/2026
**Escopo:** inspeção de referências oficiais (documentação LOM/Cycling '74, manual do Live) e de código de ponte MCP existente; sem chamadas ao Live/LOM/CUA e sem alterações no Set.

## Resumo executivo

- **VERIFICADO:** uma ponte MCP típica cobre leitura do Set, execução Python via bridge, assinatura do Set, auditoria offline, escrita de lotes de automação em cópia nova, captura/medição de áudio e presets. Ferramentas de alto nível de curadoria podem não estar registradas — o caminho para rotinas recorrentes é promovê-las a tools tipadas.
- **INFERÊNCIA:** o menor caminho para reduzir scripts one-off é promover rotinas recorrentes a ferramentas tipadas, mantendo execução de código livre como escape para código novo autorizado. O modelo pode continuar escrevendo; a barreira contra um falso "pronto" deve ser evidência mecânica, read-back e gate — não proibição do executor.
- **VERIFICADO:** criar/duplicar/deletar tracks e clips tem suporte documentado no LOM; as páginas oficiais consultadas não documentam mover/reordenar tracks nem criar/agrupar Group Tracks. A via documentada para agrupamento é a interface nativa do Live.

## Capacidade oficial do LOM, limite e recomendação

| Área | Capacidade documentada | Limite | Recomendação |
|---|---|---|---|
| Tracks e clips | LOM documenta `create_audio_track`, `create_midi_track`, `duplicate_track`, `delete_track`; `ClipSlot` cria/deleta/duplica clips; `Track` duplica clip para Arrangement e deleta clip. | As referências oficiais não documentam mover track/clip nem criar grupo. | Envolver operações em tools com alvo por nome/identidade, beat, validação e read-back; grupos só pela UI. ([Song](https://docs.cycling74.com/apiref/lom/song/), [Track](https://docs.cycling74.com/apiref/lom/track/), [ClipSlot](https://docs.cycling74.com/apiref/lom/clipslot/), [Clip](https://docs.cycling74.com/apiref/lom/clip/)) |
| Automação de Arrangement | Escrita de envelopes em cópia nova do `.als`, com hash, validação/read-back e auditoria do arquivo. | Escritores comuns aceitam apenas envelope `FloatEvent` existente; não criam envelope novo e não cobrem `BoolEvent`/`EnumEvent`. | Usar a escrita em lote onde o contrato coincide; ampliar a API só para casos recorrentes testados, sem tentar substituir um script inteiro quando ele também altera clips/notas. |
| Leitura de grupos | Listagem de grupos/filhos existentes e tracks fora de pasta; execução arbitrária de código no Live com assinatura exigida pelo cliente. | Agrupamento em si não é operação de API. | Pré-criar grupo/pista-modelo via UI; operar variantes por código depois, sempre com read-back. |

## LOM oficial e Group Tracks

**VERIFICADO — escopo da referência:** a página `Song` documenta criação, duplicação e exclusão de tracks e a propriedade `tracks` como leitura/observação; não lista operação de mover/reordenar nem criar/agrupar tracks. Na página `Track`, `group_track` é **get-only**; `clip_slots` e `arrangement_clips` também são propriedades de leitura/observação. A página `Application.View` consultada não lista comando Group/Ungroup. Na API de clips, a cópia de um clip de Arrangement tem beat de destino; a API não apresenta um método direto de "mover clip". Essas conclusões limitam-se às páginas oficiais citadas — **não** provam que não existam APIs privadas/não documentadas.

**VERIFICADO:** o manual oficial orienta selecionar as tracks e usar **Edit → Group Tracks** ou **Edit → Ungroup Tracks** ([Ableton Live Manual, §18.3](https://www.ableton.com/en/live-manual/12/mixing/#group-tracks)).

**Alternativas para agrupamento:**

1. **UI nativa — recomendada.** Usar seleção exata de tracks e o comando nativo; em seguida conferir a estrutura (grupos/filhos) antes de continuar. É a menor rota apoiada pelo manual. Requer Live aberto e operador serializado; qualquer automação aqui deve ser testada antes de adoção.
2. **Extensão via Remote Script/ponte — parcial.** Dá para envolver operações LOM documentadas em ferramentas com parâmetros e validação. Para criar/mover grupos, não há método público documentado nas referências consultadas; não assumir um `create_group_track` oculto. Investigar implementação privada somente em Set descartável e exigir teste load→read-back antes de adotar.
3. **Patch offline de `.als` para criar grupos — NÃO VERIFICADO e não recomendado.** Correções offline servem para consertar arquivos *já agrupados* que falham no load (sends, cadeia herdada, IDs); não são criadoras de grupos. A auditoria detecta referências a grupos inexistentes, mas não valida que uma nova estrutura carregará ou terá comportamento correto. Regra de ouro da escrita de `.als`: nunca usar biblioteca XML para escrever; patch por string; auditoria sempre.

**Context7 — evidência complementar:** a consulta ao catálogo da API LOM confirmou `Song.create_audio_track/create_midi_track/duplicate_track/delete_track`; `Track` trouxe propriedades de grupo somente leitura. A busca específica de métodos de agrupamento retornou "No documentation matched". Isso é resultado de indexação, não prova de inexistência; a conclusão se apoia no escopo explícito das páginas oficiais Cycling '74.

## Rota priorizada para centralização

1. **Sem Live:** usar as ferramentas offline existentes para inventário/preview/escrita em cópia de automação e auditoria; escrever contratos e testes unitários puros para as operações de curadoria. A escrita de automação confere hash, preserva o fonte, escreve cópia e audita, mas não prova que o Live carrega essa cópia.
2. **Com Live disponível:** criar o grupo e a pista-modelo pela UI. Duplicar o modelo, posicionar o material e manter a track ligada; read-back deve confirmar nome, grupo, clips e beats. Promoções copiam MIDI para o destino aprovado e preservam a origem para comparação; limpezas devem operar apenas sobre itens explicitamente marcados/selecionados, com preview da lista, backup e confirmação — **nunca por inferência estética automática**.
3. **Detecção de buracos no arranjo:** começar como leitura (snapshot do Arrangement); depois separar o cálculo puro para teste offline. Limites conhecidos: snapshot aceita um conjunto limitado de tracks por chamada e não expande eventos repetidos de clips MIDI em loop; roteamento/dispositivos/automação/solo podem deixar audibilidade não verificada. Portanto, "gap encontrado" precisa declarar janela, tracks e limite de loop; não deve virar avaliação musical automática.
4. **Reduzir scripts redundantes com escopo preciso:** cada script one-off novo deve se classificar (ferramenta do catálogo, comando da ponte, ou caso único justificado). Não afirmar que um batch substitui toda a lógica de um script que também altera clips/notas.

## Gates mecânicos e pendências de prova

**VERIFICADO:** código executado no Live deve exigir assinatura recente do Set (token); a ponte encaminha o token no RPC. Se houver timeout/falha depois do início do envio, o resultado deve ser tratado como incerto e o estado relido, sem retry automático.

**NÃO VERIFICADO (neste estudo):** a validação ponta a ponta da assinatura no Live; carga/roundtrip de uma cópia editada do `.als`; execução real das operações de curadoria.

**Gate recomendado para qualquer mutação:** backup do Set antes da mutação; um escritor por vez; assinatura recente por operação; read-back por identidade/contagem/conteúdo; salvar no Live e comprovar com mtime; auditoria offline no `.als` salvo; captura + medição DSP para prova de áudio. A tabela de provas deve apontar alvo, comando e saída crua. Medições não são julgamento estético — a curadoria final é do ouvido.

**Status desta pesquisa:** fontes oficiais e código local consultados; nenhuma alteração em código, Set ou documentação; nenhum teste ou operação Live executada. As validações ponta a ponta permanecem pendentes de uma sessão com Live disponível.
