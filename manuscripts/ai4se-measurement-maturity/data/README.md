# Public data pack — AI4SE measurement × maturity

Open release pack accompanying the manuscript *Beyond Multiplier Myths: A Boundary-Aware Dual-Lens Reporting Scheme for Industrial AI4SE Pilots*.

**Canonical URL:** https://github.com/ai4se-works/artifacts/tree/main/manuscripts/ai4se-measurement-maturity/data  
**License:** [CC BY 4.0](LICENSE) · Cite via [`CITATION.cff`](CITATION.cff).

## Contents

| Path | Description |
|------|-------------|
| `derived/` | Summary CSVs / JSON used by paper tables and figures |
| `derived/maturity_domain_scores.csv` | D1–D6 before/after domain means |
| `derived/maturity_capabilities.csv` | 18 capability before/after levels |
| `derived/effectiveness_pair_summary.csv` | Anonymized Pair-1…Pair-6 workshop signals |
| `derived/effectiveness_aggregate.csv` | Cross-pair median / IQR (and related stats) |
| `derived/figure_sources.json` | Planned figures → CSV mapping |
| `protocol/` | Metrics definitions, workshop protocol, maturity scoring guide |
| `protocol/maturity-scoring-guide.md` | L1–L5 anchors, who scores, ordinal caveats |
| `scripts/extract_derived_from_xlsx.py` | Optional regenerator (needs authorized local xlsx; not in this pack) |
| `codebook.md` | Field definitions and signal-type notes |
| `LICENSE` | Creative Commons Attribution 4.0 International |
| `CITATION.cff` | Machine-readable citation stub |

## Signal-type legend

Every derived row carries `signal_type ∈ {expert_estimate, process_signal, req_measured}` (see `codebook.md`):

| Value | Meaning | Used in this pack |
|-------|---------|-------------------|
| `expert_estimate` | Facilitator / SME judgment from the effectiveness workshop; **not** platform-measured ROI | `effectiveness_*.csv` |
| `process_signal` | Expert-facilitated maturity assessment (capability / domain levels); **not** platform-measured telemetry | `maturity_*.csv` |
| `req_measured` | Values grounded in requirements platform (or equivalent) measurement systems | Reserved — unused in current derived tables |

Do not collapse these types when reproducing tables.

## What is NOT included

- Raw client spreadsheets (`.xlsx`) or workbook dumps
- Photos, logos, or branded workshop artifacts
- Real person names (workshop pairs are anonymized as `Pair-1` … `Pair-N`)
- Organizational identifiers beyond the paper’s `Org-A` anonymization

## How to reproduce table numbers

1. Prefer the committed files under `derived/` as the source of truth for published numbers.
2. With **authorized local** handoff xlsx present (not in this pack), regenerate via `scripts/extract_derived_from_xlsx.py` after pointing its output directory at this `derived/` folder.
3. Diff regenerated CSVs against the committed `derived/` files; they must match for paper table numbers.
4. Anonymity smoke (expect no matches for legal client names or participant names).

## Suggested citation

Cite the manuscript and this repository path (CC BY 4.0). Update `CITATION.cff` after camera-ready metadata is fixed.
