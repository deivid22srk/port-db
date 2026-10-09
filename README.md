# port-db

Base de dados em JSON extraída de [https://github.com/deivid22srk/port-droid](https://github.com/deivid22srk/port-droid), com metadados dos jogos e seus recursos visuais associados.

## Conteúdo

- `data/games.json` — catálogo completo na estrutura original (`site` e lista `games`).
- `data/index.json` — índice compacto de registros e caminhos de imagens.
- `games/<id>.json` — um arquivo JSON por jogo, com nome, pacote Android quando informado, descrições, requisitos, links e créditos.
- `assets/img/games/<id>/` — capas, banners e screenshots referenciados pelos JSONs.

## Jogos incluídos

- `sonic-unleashed` — Sonic Unleashed
- `skate-3` — Skate 3
- `csgo-mobile` — Counter-Strike: Global Offensive
- `lost-odyssey-recomp` — Lost Odyssey
- `woodyre` — Woody Woodpecker: Escape from Buzz Buzzard Park
- `simpsons-hit-and-run` — The Simpsons: Hit & Run
- `halo-ce` — Halo: Combat Evolved
- `gta-iv` — Grand Theft Auto IV

## Uso rápido

```js
const catalog = await fetch('./data/games.json').then(r => r.json());
const games = catalog.games;
const sonic = await fetch('./games/sonic-unleashed.json').then(r => r.json());
```

Os registros incluem `packageName` quando informado. O campo `version` não é usado. Os campos `cover`, `banner` e `screenshots` são caminhos relativos à raiz deste repositório. Os arquivos estão preservados em `assets/img/games/`.

## Imagens

As imagens de GTA IV seguem a resolução indicada no README do projeto de origem: capa WebP **720×960 (3:4)** e banner/screenshots WebP **1280×720 (16:9)**. Os screenshots enviados em 1200×540 foram encaixados no canvas 1280×720 preservando o conteúdo completo.

## Escopo e direitos

Este repositório contém **metadados e arte/imagens de apresentação** já publicados no projeto de origem. Não inclui APKs, ROMs, ISOs, dumps nem dados executáveis dos jogos. Os direitos das marcas e imagens de jogos pertencem a seus respectivos titulares; os campos `credit`, `license` e links de cada registro devem ser consultados para atribuição e termos específicos. A licença MIT do código do site de origem não é aqui declarada como licença universal para imagens ou marcas.
