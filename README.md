# Babel

**Localization Tool** — Crowdsourcing portal for translating pet dialogue and UI across locales without flattening character.

Part of the [ComputerPets](https://github.com/RicheyWorks/computerpets) ecosystem. Index: [computerpets-ecosystem](https://github.com/RicheyWorks/computerpets-ecosystem).

> Status: **design scaffold**. This repository ships the contract, README, and layout so implementation can start without renaming the organ later.

## Why it exists

Rui's English is short. Japanese must stay short. Babel ships string kits to Cortex + Companion + desktop, with reviewer gates.

The flagship overlay already puts a living sticker on the real desktop (Rui first, 210 kinds). Babel does not replace that. It is one organ.

## Stack

TypeScript · React 19 · crowdin-style workflow · ICU messages · species-aware tone guides

GroupId / namespace: `com.enterprisepet.babel`  
Default listen: `8080`

## Talks to

- computerpets-cortex
- computerpets-vox
- computerpets-companion
- computerpets-lore

## Contract

### Data

`StringKey(id, source, tone) · Suggestion(locale, text, user) · Kit(locale, completePct)`

### Surface

- GET /v1/kits/{locale} — pending strings
- POST /v1/suggest — translator proposal
- POST /v1/approve — reviewer
- GET /v1/export/{locale} — json for clients

### Failure doctrine

Machine-only translation → flagged, not shipped. Missing locale → English fallback. Tone lint fail → stay pending.

## Layout

```
computerpets-babel/
  README.md           this file
  LICENSE             MIT
  docs/CONTRACT.md    the same contract, frozen for implementers
  src/                implementation lands here
```

## Run (Windows)

PowerShell, from this folder, after the flagship helpers (Git, Node LTS 22+, JDK 21 as needed):

```powershell
cd app; npm install; npm run dev
```

You do not need this service to meet Rui. The [flagship start-here](https://github.com/RicheyWorks/computerpets/blob/main/docs/START-HERE.md) is still the first pet.

## Ecosystem

| Organ | Repo |
| --- | --- |
| Flagship desktop + Spring | [RicheyWorks/computerpets](https://github.com/RicheyWorks/computerpets) |
| This organ | [RicheyWorks/computerpets-babel](https://github.com/RicheyWorks/computerpets-babel) |
| Full map | [RicheyWorks/computerpets-ecosystem](https://github.com/RicheyWorks/computerpets-ecosystem) |

## License

MIT. See [LICENSE](LICENSE).

---

*Two hundred ten living kinds. Keep them so a line does not go quiet.*
