# Understanding Reverb — fundamentos e controles

> **Fonte:** [Sonic Academy — Understanding Reverb](https://www.youtube.com/watch?v=9jkbBQW11qA), publicado em 05/11/2021, duração 13:51. Consulta em 27/10/2026. Legenda automática em inglês obtida e lida na sessão original. Legendas podem transcrever termos incorretamente; não substituem a escuta ou a leitura da interface.
>
> **Escopo:** a descrição do próprio vídeo anuncia um curso de nove vídeos e aponta para [Understanding Reverb, Graham Ginty e Protoculture](https://www.sonicacademy.com/courses/understanding-reverb-graham-ginty-protoculture). A página do curso retornou HTTP 403 na consulta original. O link fornecido não contém identificador de playlist. **NÃO VERIFICADO:** relação completa de aulas, acesso e conteúdo das outras oito; este mapa cobre apenas o vídeo indicado.

## O que a aula ensina

Reverberação é o conjunto de reflexões que chegam depois do som direto; a absorção das superfícies altera sua duração e seu espectro (00:22–00:56). A aula apresenta room/hall, chamber, plate e spring; a seguir, distingue algoritmos que simulam espaços e convolução, que usa uma resposta ao impulso — registro da resposta acústica de um espaço ou outra fonte (01:10–05:22). Ela cita o Hybrid Reverb do Ableton como exemplo capaz de combinar convolução e algoritmo (05:15–05:22).

| Controle ou técnica | Evidência da aula | Nota de experimentação (não receita pronta) |
|---|---|---|
| Dry/wet e return | Em return, usar reverb 100% wet e dosar nos sends; um retorno compartilhado pode unificar os sons (06:29–06:46). | Preservar o sinal seco na pista e dosar o retorno. Um retorno único é uma escolha possível; não é a única (retornos distintos por tipo de cauda também são prática comum). |
| Decay | Tempo para a reverberação desaparecer; espaços maiores tendem a caudas maiores, dependendo da absorção (07:09–07:36). | Comparar caudas curtas e longas no contexto do groove; verificar se a cauda preenche pausas que deveriam respirar. |
| Early e late reflections | Reflexões iniciais ajudam a perceber o espaço; as tardias formam a cauda mais difusa (07:42–08:12). | Comparar sensação de sala com e sem cauda pronunciada; a aula não determina valores. |
| Diffusion/density | Menor difusão deixa ecos mais distinguíveis; maior difusão suaviza as reflexões (08:53–09:15). A aula alerta que nomes dos controles variam e chama `Density` o controle equivalente no Reverb do Ableton (09:32–09:45). | Conferir o device e a versão antes de equiparar parâmetros; não inferir que o controle homônimo de outro plugin seja idêntico. |
| Pre-delay | Intervalo entre som original e efeito; pode separar o ataque da cauda e aumentar clareza (09:52–10:00). | A/B com e sem separação audível, sem assumir um valor universal; demais parâmetros constantes. |
| EQ da reverb | Modela frequências do efeito (11:06–11:14). | Priorizar EQ da cauda no retorno para não alterar o corpo seco; frequências específicas dependem de contexto e teste. |
| Room size e decay | O tamanho virtual afeta o intervalo entre reflexões; alguns plugins o ligam ao decay. Na demonstração, o Reverb do Ableton permite ajustá-los separadamente (11:43–12:26). | Testar tamanho e duração separadamente se o device concreto permitir; conferir a interface real. |
| Modulação | Introduz movimento e pode suavizar ou adensar a cauda, frequentemente com efeito semelhante a chorus (13:00–13:09). | Comparar desligada e sutil na cauda; largura e compatibilidade mono não foram medidas nesta aula. |

## Hipótese de aplicação e limites

**HIPÓTESE:** para manter um motor minimalista definido e explorar sala em madeira ou resposta, um retorno paralelo dosado com comparação de pre-delay e decay pode ser um experimento útil. Não é decisão estética, alteração de Set ou recomendação de valor fixo. Fontes acústicas conservam o dry em primeiro plano (wet ≤25% ou paralelo); low-end permanece mono. A avaliação deve ocorrer na música inteira e com volume percebido equivalente.

**NÃO VERIFICADO:** escuta direta do vídeo ou de seus exemplos, interface visual e parâmetros demonstrados, efeito em sets concretos, estado de returns, compatibilidade mono e aprovação auditiva de quem escuta. Nada foi aplicado a Live. A duração e os timestamps vêm dos metadados e da legenda; demonstrações sem fala não foram interpretadas.

## Prova de extração (sessão original)

- `yt-dlp --skip-download --no-playlist --print '%(title)s | %(channel)s | %(channel_url)s | %(duration_string)s | %(playlist_url)s' URL` → `Understanding Reverb | Sonic Academy | ... | 13:51 | NA`.
- `yt-dlp --skip-download --write-auto-subs --sub-langs en-orig --sub-format vtt ... URL` → `Downloading subtitles: en-orig` (legenda gravada e lida).
- Página oficial do curso: consulta direta retornou `HTTP 403 Forbidden`; não há prova de acesso às demais aulas.
