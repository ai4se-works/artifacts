# Contributing

This repository publishes anonymized AI4SE practice materials for the global community. Maintainers and invited collaborators may open pull requests.

## What belongs here

- Anonymized academic manuscripts and their **data packs** (`papers/<slug>/`)
- Industry talks and keynotes (`talks/<slug>/`)
- Non-academic practice reports (`reports/<slug>/`)

## What must never be committed

- Legal client names, unredacted org charts, raw engagement dumps, photos, credentials
- Internal path pointers that reveal client identity
- Secrets (API keys, tokens, `.env` files)

## Anonymization

Before publishing any engagement-derived evidence:

1. Replace org identifiers with stable aliases (e.g. Org-A) consistently across prose and data.
2. Publish only **derived** metrics and protocols needed to inspect claims—not raw operational extracts.
3. Document in `data/README.md` what is included, how to reproduce tables/figures, and what is explicitly excluded.
4. Have a maintainer confirm the pack is safe for a public repository.

## Language

English is the default. Chinese materials should be clearly labeled or placed under a `zh/` subpath within the entry folder.

## Adding a paper entry

1. Choose a **topic-based** slug: lowercase, hyphenated (e.g. `stage-gated-ai4se-path`). Do not encode a venue name in the slug while under review.
2. Create `papers/<slug>/README.md` with: title, short summary, status (`draft` | `under review` | `published`), authors (omit or anonymize if double-blind rules require it), and links to `paper/` / `data/` if present.
3. If providing Data Availability materials, add `papers/<slug>/data/` with a `README.md` and derived files only.
4. Open a PR describing what changed and confirming anonymization review.

## Venue silence while under review

Do **not** list conference or journal names in folder names, entry READMEs, or the root index until the work is accepted or publicly presented. Status may say `under review` without naming where.

## Talks and reports

Use the same slug and README patterns under `talks/` and `reports/`. Event names for talks may be added once the talk has been delivered publicly.
