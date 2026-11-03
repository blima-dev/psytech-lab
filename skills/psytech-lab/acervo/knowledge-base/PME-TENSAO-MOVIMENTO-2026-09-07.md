# PME Experts — tensão e movimento

Consulta em 2026-09-07 ao notebook de fontes PME Experts. UI: 300 fontes cadastradas, 295 selecionáveis e cinco com erro. Não tratar a contagem como 300 transcrições validadas.

## Trechos originais conferidos na UI

- **Como Criar Movimento com Automações - by Dharana (Zenon)**, citação 20: controle X/Y associa ressonância à vertical e cutoff à horizontal. O autor relata variar automações para atenuar a atenção de um synth marcante. Aplicação candidata: dar foco e depois recuar, em vez de abrir tudo continuamente.
- **WORKSHOP: TRANSIÇÕES CRIATIVAS**, citação 8: retirar kick e baixo cria silêncio de transição; o autor alerta contra repetir a pausa a cada 32 tempos, pois a música pode parecer incompleta. Aplicação candidata: reservar cortes fortes às chegadas principais e variar outras transições.
- **FOREST AMBIENCES Aula Completa**, transcrição no acervo `FOREST_AMBIENCES_Aula_Completa.md`: derivar atmosferas da própria conversa dos leads, usando processamento e planos de profundidade; rotas nativas e externas são alternativas. Não exige adicionar VST ou nova camada se a atmosfera atual já cumprir a função.

## Síntese retornada pelo Notebook — ainda não é fonte primária verificada

Seis ideias recuperadas: arranjo em atos e subtração; silêncio antes de retorno; deslocamento melódico de tensão; transição com release/noise do próprio lead; movimento de cutoff/ressonância; diálogo frente/fundo com reverbs diferentes. As sugestões específicas de notas, frequências e compassos da resposta são hipóteses de aplicação do modelo.

## Correções antes de reutilizar

- A 132 BPM em 4/4, 16 compassos duram **29,0909 s**, não exatamente 30 s. 224 compassos = **407,2727 s** sem caudas.
- C#1 = **34,6478 Hz**, C#2 = **69,2957 Hz** sob MIDI convencional com C4 = 60. O texto anterior do Notebook cita 62 Hz como C#: incorreto. O Live pode usar numeração de oitava diferente; registrar MIDI/frequência.
- A quinta justa de C# é **G#**, não G natural. Ré natural é empréstimo cromático/frígio; não faz parte da escala natural de C# menor.
- Um pico de kick em −10 dBFS e de baixo em −12 dBFS não garante 10 dB de margem no master: conferir a soma real.
- Não aplicar a um filtro passa-altas a automação de abertura de um passa-baixas (confundir os dois tipos de filtro corrompe o movimento de abertura pretendido).

## Uso

Uma mudança material por rodada, trecho curto, leitura do estado real e escuta. Fontes orientam hipóteses; não comprovam melhoria musical.
