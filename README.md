# LUDUS

Dílna výukových her.

## Aktuální stav

Verze: **1.10.1**

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


## 1.10.1

- Sjednoceno ukládání rozehraných her napříč hotovými enginy.
- Každý hotový engine teď deklaruje LUDUS progress API v1: `saveProgress`, `loadProgress`, `resumeProgress`, `clearProgress`, `getProgressSummary`.
- Pas hry a `engines/manifest.json` nově ukazují schopnost save/load/resume.

## 1.10.0
- Přidány plánované světy Banánová parta (Mimoni) a Továrna na smích (Příšerky s.r.o.).
- Panel API klíče podporuje trvalé uložení v tomto prohlížeči i dočasné uložení pro relaci.
