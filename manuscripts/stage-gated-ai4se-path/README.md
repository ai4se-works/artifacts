# Manuscript: AI4SE operating stack

**Title:** From Pilot Evidence to Conditional Scale: An AI4SE Operating Stack for Mid-to-Large Organizations  
**Status:** `under review`  
**Authors:** Juan Qiu, Qilong Yan (Inspire Group)  
**Partners:** anonymized as Org-A, Org-B (no client co-authors)

## Contents

| Path | Description |
|------|-------------|
| [`paper/`](paper/) | LaTeX sources, IEEE class files, compiled PDF |
| [`data/`](data/) | Reviewer-facing evidence pack (gate rubric, ledger, themes, L3 map, timeline) |

## Data Availability URL

https://github.com/ai4se-works/artifacts/tree/main/manuscripts/stage-gated-ai4se-path/data

## Build PDF

```bash
cd paper
latexmk -pdf -interaction=nonstopmode main.tex
```

## Submission notes

- Upload `paper/main.pdf` (or a fresh `latexmk` build) as the manuscript PDF.
- Venue-specific cover letters / portal forms stay in the private consulting workspace (not published here while under review).
- Do not add target venue names to this README until acceptance.
