# port-db

Base de dados em JSON extraída de [https://github.com/deivid22srk/port-droid](https://github.com/deivid22srk/port-droid), com metadados dos jogos e seus recursos visuais associados.

## Conteúdo

- `data/games.json` — catálogo completo na estrutura original (`site` e lista `games`).
- `data/index.json` — índice compacto de registros e caminhos de imagens.
- `games/<id>.json` — um arquivo JSON por jogo, com nome, descrições, requisitos, links, créditos e metadados.
- `assets/img/games/<id>/` — capas, banners e screenshots referenciados pelos JSONs.

## Jogos incluídos

- `sonic-unleashed` — Sonic Unleashed
- `skate-3` — Skate 3
- `csgo-mobile` — Counter-Strike: Global Offensive
- `lost-odyssey-recomp` — Lost Odyssey
- `woodyre` — Woody Woodpecker: Escape from Buzz Buzzard Park
- `simpsons-hit-and-run` — The Simpsons: Hit & Run
- `halo-ce` — Halo: Combat Evolved

## Uso rápido

```js
const catalog = await fetch('./data/games.json').then(r => r.json());
const games = catalog.games;
const sonic = await fetch('./games/sonic-unleashed.json').then(r => r.json());
```

Os campos `cover`, `banner` e `screenshots` são caminhos relativos à raiz deste repositório. Os arquivos estão preservados em `assets/img/games/`.

## Escopo e direitos

Este repositório contém **metadados e arte/imagens de apresentação** já publicados no projeto de origem. Não inclui APKs, ROMs, ISOs, dumps nem dados executáveis dos jogos. Os direitos das marcas e imagens de jogos pertencem a seus respectivos titulares; os campos `credit`, `license` e links de cada registro devem ser consultados para atribuição e termos específicos. A licença MIT do código do site de origem não é aqui declarada como licença universal para imagens ou marcas.
