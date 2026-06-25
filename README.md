# LUDUS

Dílna výukových her.

## Aktuální stav

Verze: **1.9.9**

- build: `npm run build`
- zdroj dílny: `src/index.html`
- samostatné enginy: `engines/*.html`
- kanonický katalog enginů: `engines/manifest.json`
- manuály: `docs/manualy/`

## Manifest enginů

`engines/manifest.json` je hlavní místo pro běžná metadata enginů. LUDUS z něj po načtení přebírá zejména:

- `status` hry (`ready`, `draft`, `planned`),
- `gameId`, `skinId`, `mechanicId` a `gameKey`,
- soubor enginu (`file` / `url`),
- `flowModel`, podporované typy cvičení, jazyky, brand režimy,
- `capabilities` a kontrolní smlouvu enginu.

`src/index.html` obsahuje ještě fallback registr pro případ, kdy se manifest nenačte, například při lokálním otevření přes `file://`.

## PWA verze

LUDUS obsahuje instalovatelnou PWA vrstvu: manifest, service worker a vlastní ikony. Build kopíruje složku `public/` do `dist/`.

## Dokumentace

Závazná sada manuálů 00–07 je v `docs/manualy/`. Build ji kopíruje také do `dist/docs/manualy/`.
