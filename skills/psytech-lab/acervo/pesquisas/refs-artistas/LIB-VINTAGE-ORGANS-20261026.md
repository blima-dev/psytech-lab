# LIB — NI Vintage Organs 1.5.3 (Kontakt) — pesquisa de referência (26/10/2026)

## O que é (VERIFICADO: página oficial NI, aberta 26/10)

Sample library (não físico-modelado) de **5 órgãos clássicos**: Hammond B-3, C-3 e M-3, Vox Continental II
e Farfisa Compact — gravações cromáticas dos instrumentos reais; rotator/Leslie, cabinets e reverb são
emulação em tempo real. Controles: **drawbars, percussion, chorus/vibrato** (página Organ) + envelope,
drive, EQ, 8 cabinets, reverb por convolução (IRs plate/spring) e speaker rotativo (página Amp).
Manuais superior/inferior/pedal via keysplit ou canais MIDI. Ainda vendida (US$ 99), compatível com
**Kontakt 8 (Player ou full)**.

## Conteúdo do pacote (VERIFICADO: find/ls)

**1,4 GB** · 100 `.nki` em 9 categorias:
Default 5 · Jazz 15 · Classic Rock 13 · Transistor 12 · Gospel & Church 14 · Funk & Reggae 14 ·
**House & Disco 12** · Theater & Entertainer 5 · Special 10.
Extras: `Vintage Organs.nicnt` (library **licenciada do Kontakt Player**), Samples/, Documentation/,
e **`.previews/*.ogg` para cada patch** — os 100 timbres são **audíveis sem abrir o Kontakt**.

## Lições de licenciamento (Kontakt Player — vale para qualquer lib com .nicnt)

- **`.nicnt` = biblioteca licenciada do Kontakt Player**: exige entitlement no **Native Access** —
  sem ele, qualquer `.nki` falha com *"This instrument belongs to a library that is not installed
  currently!"* **Mesmo no Kontakt full** (o full tem Batch resave, mas .nicnt exige licença do mesmo jeito).
- O caminho da pasta **não** é o problema: bibliotecas de fábrica do app carregam porque vêm
  pré-entituladas; e bibliotecas **não-Player** (sem .nicnt) carregam de qualquer pasta no full.
- Samples são contêineres `.nkc/.nkr` (não WAV solto) — uso musical é dentro do Kontakt/Live.
- **Caminhos legítimos:** (a) serial no Native Access (US$ 99) → "Locate" apontando para a pasta
  montada; (b) escuta pelos `.previews/*.ogg` (funciona sem instalar nada); (c) alternativa free
  SEM `.nicnt` (non-Player carrega de qualquer pasta no full). Falsificar registro de licença da NI
  não se faz.

## Serventia num projeto minimal psytech

- **Não resolve** madeira/orgânicos percussivos nem camada orquestral — é órgão, não madeira.
- **Papel realista: COR/TEXTURA** — o Leslie/rotator é movimento embutido (não precisa LFO); os
  presets "House & Disco" apontam para o uso dance; um drawbar sustentado em **2–3 notas
  (tônica/quinta), oitava 3–4**, com HP ~200 Hz entra como cama/eco sem brigar com o mono do grave.
- **NUNCA no grave**: drawbars 16'/sub do órgão podem sujar o low-end mono — qualquer uso com HP e
  sem dobrar o sub do projeto.
- Timbre gospel/disco pode brigar com o dark zenon: é **decisão de ouvido** (soberania da escuta).

## A/B proposto (o mais barato — sem instalar nada)

1. Ouvir 3–4 `.previews/*.ogg` das categorias `7 - House & Disco`, `4 - Transistor` e `9 - Special`
   (escuta direta, zero setup).
2. Se gostar: resolver licença/scan e testar 8 compassos de cama (ou cauda no echo do breakdown),
   HP 200 Hz, contra o trecho atual.

## Referências usadas

- Web: https://www.native-instruments.com/en/products/komplete/keys/vintage-organs/ (26/10).
- Disco: find/ls/du na pasta do download (26/10).

`NÃO VERIFICADO`: comportamento do scan de plugins varia por máquina; som renderizado (nenhum .nki
foi aberto — a escuta possível é pelos .previews).
