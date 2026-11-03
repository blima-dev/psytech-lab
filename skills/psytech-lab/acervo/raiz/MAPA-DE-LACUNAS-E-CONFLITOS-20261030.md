# MAPA DE LACUNAS E CONFLITOS — PESQUISA PSYTECH

> Roteiro de lacunas de pesquisa (levantamento de 30/10/2026). Só leitura.
> Sem origem identificada = `NÃO VERIFICADO`. O estado do set e os números de contraste da produção em
> curso não acompanham este roteiro — estão no repositório de origem.

## 1. Cobertura por frente (P0–P2)

* **P0 ondas/fase/kick-bass/mascaramento/dinâmica/medição:** **parcial**. Teoria coberta em estudos com
  Zenon/FabFilter/iZotope como fontes; faltam experimentos controlados com prova sintética + null-test na
  cadeia real.
* **P0 kick×bass, 4 mecanismos (envelope/interferência/mascaramento/bombeamento):** **lacuna**. Existe
  contraste numérico com a referência externa, mas sem teste discriminante aplicado no material real.
* **P1 EQ/filtros/estéreo/saturação/espaço/master:** **parcial**. Achados pontuais (enum de filtro corrigido,
  mono ≤120 Hz, true peak −0,6 PASS) sem experimentos controlados em série.
* **P1 masterização (ordem/limiter/true peak/transcode):** **lacuna crítica** — limiter duplo na produção
  contamina qualquer medida de LUFS/TP do render; e −0,6 dBTP não atende plataformas que pedem −2 dBTP.
* **P2 percepção/arranjo-identidade:** **parcial**. Respiro por subtração medido (contagem de camadas por
  bloco de 8, não RMS) e vazio proposital no 1º minuto; falta matriz por perfil psytech.
* **Síntese:** **parcial-baixa**. Já coberto: bass-rip (saw + uníssono + wavetable-LFO + FM com filtro final),
  split SUB/HIGH, square uma oitava abaixo em mono, ghost kick, note-length; bancos de presets curados;
  renderer offline de síntese. Faltam: série sistemática de experimentos, fase fixa vs random, unison no
  grave somado em mono, razões de FM, pitch-env de kick, distorção pré/pós-filtro.

## 2. Lacunas restantes (priorizadas)

1. **Matriz de corpus psytech por perfil** (minimal/groove/dark/orgânico/agressivo) com janelas e método
   declarados, sem inventar padrão único de LUFS.
2. **Receitas por função** (kick/sub/bass-rip/perc/madeiras/drone/riser) com instrumento + versão + controle
   acessível provado (sintetizador atual vs alternativas do DAW), cada uma com alternativa sem plugin pago.
3. **Biblioteca offline modular:** `FUNDAMENTOS/ INSTRUMENTOS/ RECEITAS/ DIAGNOSTICOS/ REFERENCIAS/` com
   índice pequeno e gatilhos por sintoma, sem duplicar índices já existentes.
4. **Experimentos e síntese como pacotes reproduzíveis:** hipótese + arquivos + parâmetros + janela + gráfico +
   A/B nivelado + limite declarado — nenhum entregue nesse formato ainda.

## 3. Regras do levantamento

- Medição de áudio na taxa original e em estéreo — nunca medir topo (>8 kHz) ou estéreo depois de reamostrar
  para 22.050 Hz ou somar em mono.
- Stems separados por IA (Demucs e similares) são estimativa: não servem de prova de instrumento isolado sem
  etiqueta `ESTIMATIVA`.
- Pesquisa externa alimenta a biblioteca versionada; operação diária = arquivos locais + rotina sob demanda.
  Ausente = `NÃO COMPROVADO`, nunca inventar parâmetro.

---
*Nota de higienização: este roteiro é a parte genérica de um levantamento maior cujas seções de estado
(baseline de set, hashes, conflitos de estado, configuração de host) não acompanham o pacote.*
