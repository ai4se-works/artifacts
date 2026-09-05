# Manuscript: Boundary-aware AI4SE measurement

**Title:** Beyond Multiplier Myths: A Boundary-Aware Dual-Lens Reporting Scheme for Industrial AI4SE Pilots  
**Status:** `under review`  
**Authors:** Juan Qiu, Qilong Yan (Inspire Group)  
**Partners:** anonymized as Org-A (no client co-authors)

## Contents

| Path | Description |
|------|-------------|
| [`paper/`](paper/) | LaTeX sources, figures, IEEE class files, compiled PDF |
| [`data/`](data/) | Anonymized derived tables, protocols, scoring guide |

## Data Availability URL

https://github.com/ai4se-works/artifacts/tree/main/manuscripts/ai4se-measurement-maturity/data

## Build PDF

```bash
cd paper
latexmk -pdf -interaction=nonstopmode main.tex
```

## Submission notes

- Upload `paper/main.pdf` (or a fresh `latexmk` build) as the manuscript PDF.
- Venue-specific cover letters / portal forms stay in the private consulting workspace (not published here while under review).
- Do not add target venue names to this README until acceptance.
- Every quantitative table cell must match `data/derived/*.csv`.
