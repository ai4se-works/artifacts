# Data pack — stage-gated AI4SE path (reviewer-facing)

Anonymized, **self-contained** evidence for the manuscript
*From Pilot toward Conditional Scale: A Stage-Gated AI4SE Path for Mid-to-Large Software Organizations*.

**Canonical URL:** https://github.com/ai4se-works/artifacts/tree/main/manuscripts/stage-gated-ai4se-path/data  
**License:** CC-BY-4.0 (repository root `LICENSE`)

This pack is written for external readers. Every file below is meant to be
readable without access to any private consulting repository.

## Claim → file map

| Manuscript claim (inspectable) | File |
|---|---|
| G1 (Explore) pass / G2 (Scale entry) hold at Org-A | [`gate-rubric.md`](gate-rubric.md) |
| Stage goals and exit tests (Explore / Consolidation / Scale) | [`gate-rubric.md`](gate-rubric.md) |
| L1 citable method kernel (principles, artifact chain, process gates, normative clauses, known gaps) | [`l1-method-extract.md`](l1-method-extract.md) |
| L1–L4 asset classes, outcomes, readiness boundaries | [`asset-ledger.csv`](asset-ledger.csv) |
| Twelve opportunity themes; #5/#9 observation; aggregate 11+11 L2 counts | [`theme-index.csv`](theme-index.csv) + [`asset-ledger.csv`](asset-ledger.csv) (L2 row) |
| L3 executable pack layout; stub vs ready on main chain | [`l3-stub-map.md`](l3-stub-map.md) |
| Org-A Explore timeline (~6 weeks; week-level windows, not day-exact) | [`timeline.csv`](timeline.csv) |
| Org-A sector-type portrait (anonymized) | [`org-a-context.md`](org-a-context.md) |
| Org-B recognition vignette bounds only | [`org-b-bounds.md`](org-b-bounds.md) |
| Threat / boundary notes aligned with the manuscript | [`threats-note.md`](threats-note.md) |

## What is NOT included

- Full playbook / operations handbook text (only the public method card in `l1-method-extract.md`)
- Opportunity Spec/BP bodies, or plugin source trees
- Client intranet materials, legal entity names, product brands, participant names
- Raw workshop transcripts, photos, or unredacted change records
- Companion measurement manuscript quantitative tables (see
  [`../ai4se-measurement-maturity/data/`](https://github.com/ai4se-works/artifacts/tree/main/manuscripts/ai4se-measurement-maturity/data))

## Aggregate L2 counts

The manuscript and [`asset-ledger.csv`](asset-ledger.csv) report **11 best practices + 11 specifications** in the Explore release index.
[`theme-index.csv`](theme-index.csv) lists all **twelve** named themes with `released` vs `observation` status (#5 and #9 observation).
Spec/BP file bodies are withheld; the CSV is for status inspection only.

1. Read [`gate-rubric.md`](gate-rubric.md) for the admission contract and Org-A gate outcomes.
2. Read [`l1-method-extract.md`](l1-method-extract.md) for the citable method kernel behind L1.
3. Cross-check Table “asset ledger” claims against [`asset-ledger.csv`](asset-ledger.csv) and [`l3-stub-map.md`](l3-stub-map.md).
4. Cross-check theme counts / observation flags against [`theme-index.csv`](theme-index.csv).
5. Cross-check the Org-A timeline figure against [`timeline.csv`](timeline.csv).

## Citation

Cite the manuscript and this repository path. After acceptance, prefer the camera-ready citation with DOI/proceedings link.
