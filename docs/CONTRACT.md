# Babel contract

Do not implement against folklore. Implement against this file.

## Identity

- Product: **Babel**
- Repo: `computerpets-babel`
- Category: Community
- Idea: Localization Tool
- Port / surface: `8080`

## Must

- Stay canon with 210 species. No illegal hybrids. No swapped voices.
- Treat the desktop overlay as the main quest. This organ is optional until wired.
- Fail soft: the overlay keeps walking if this service is down, unless this *is* the overlay.
- No PII in public artifacts (Steam id, wallet, home path, webcam frames).

## Data

StringKey(id, source, tone) · Suggestion(locale, text, user) · Kit(locale, completePct)

## Surface

- GET /v1/kits/{locale} — pending strings
- POST /v1/suggest — translator proposal
- POST /v1/approve — reviewer
- GET /v1/export/{locale} — json for clients

## Neighbors

- computerpets-cortex
- computerpets-vox
- computerpets-companion
- computerpets-lore

## Failure doctrine

Machine-only translation → flagged, not shipped. Missing locale → English fallback. Tone lint fail → stay pending.

## Stack

TypeScript · React 19 · crowdin-style workflow · ICU messages · species-aware tone guides
