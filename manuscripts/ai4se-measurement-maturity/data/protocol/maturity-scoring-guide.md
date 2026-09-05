# Maturity scoring guide (Org-A instrument)

**Signal type:** `process_signal` (facilitator-guided consensus; **not** platform-measured)  
**Instrument:** 6 domains × 18 capabilities (3 per domain), levels L1–L5  
**Derived scores:** `../derived/maturity_capabilities.csv`, `../derived/maturity_domain_scores.csv`

This guide packages the industrial rubric used for Paper C. It is a program-local checklist for repeated enablement phases, **not** a psychometrically validated scale and **not** a claim of inter-rater reliability.

## Who scores

- A consulting facilitator walks sponsors and delivery leads through each capability.
- Consensus level is recorded after short discussion against the anchors below.
- Same facilitation team should run Before and After when possible (Org-A: start and end of ~6-week pilot).
- The effectiveness workshop is a **separate** session; do not mix workshop pair IDs into maturity scores.

## Level anchors (L1–L5)

| Level | Label | Observable cue (short) |
|-------|--------|-------------------------|
| L1 | Initial | Ad hoc / absent practice; no shared ritual or artifact |
| L2 | Toolized | Tools or templates exist for some people; uneven use |
| L3 | Engineered | Defined workflow/recipe with named owners; used on the pilot vehicle |
| L4 | Systematized | Cross-team standard with review/gate; measured or audited |
| L5 | Autonomous | Self-improving loop; org can extend without external facilitation |

Domain means = arithmetic mean of the three capability levels in that domain (1–5 encoding). Treat means as **convenience summaries of ordinal levels**, not interval measurements.

## Domains (English labels)

| ID | Domain |
|----|--------|
| D1 | Efficiency Foundation |
| D2 | Process Layer |
| D3 | Engineering Methods & Discipline |
| D4 | Tooling Layer |
| D5 | Human–Agent Collaboration |
| D6 | Organization & Culture |

Full capability IDs and Before/After levels: see `maturity_capabilities.csv`.

## Facilitation notes

1. Score what is **observable now**, not aspirational roadmap slides.
2. Prefer under-claiming when evidence is thin (default to lower level).
3. A one-level lift on a single capability with two unchanged → domain mean Δ ≈ 0.33.
4. Short pilots (~6 weeks) should be expected to move only a subset of capabilities; modest Δ is news, not automatic failure.
5. Never promote maturity scores to delivery ROI or `req_measured`.

## Limits (publish with scores)

- No IRR / kappa study claimed.
- Ordinal levels averaged for narrative tables only.
- Not interchangeable with AASD-OMM, AI4SE-MM, or ACMM without remapping.
- Client-specific product names and participant identities stay out of public derived files.
