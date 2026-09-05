# Workshop protocol (public)

Anonymized English distillation of the internal effectiveness-measurement workshop design (evidence E2). Enough to reproduce the comparison structure behind `effectiveness_pair_summary.csv` and `effectiveness_aggregate.csv`.

## Proposition

Under a **fixed** Product Backlog, team size, and iteration window, independent expert pairs estimate Throughput and Cycle Time for **Before** (traditional delivery) vs **After** (spec-driven / SDD method pack at high consensus). Cross-pair results are summarized with **median and IQR**.

**Positioning:** promissory expectation under high consensus — **not** landed platform-measured ROI. Later platform measurement should validate or refute the expectation.

## Three anchors

1. **Comparability** — only the development method may change between Before and After.  
2. **Separability** — freeze story points after Stage 1; After must not re-estimate points.  
3. **Honesty** — publish estimates as estimates; prefer “promissory expectation” over “best case” hype or fake ROI.

### Fixed conditions

| Condition | Workshop setting | Why fixed |
|-----------|------------------|-----------|
| Product Backlog | Identical PBI list for all pairs | Complexity mix must not drift |
| Team size | Fixed roster (example used in study: 5 Dev + shared BA/QA fractions) | Parallelism confounder |
| Iteration window | 2 weeks / 10 working days | Completion probability confounder |

## Metrics used on the floor

- **Throughput (primary):** Σ story points completable in the window (PersonDays ≈ constant ⇒ equivalent ranking to points/person-day). Completion endpoint = QA testing completed (aligned with CT2).
- **CT1:** DEV accept → last commit (maps to `CT_code`); within-pair summary = **P75** over stories in the throughput set.
- **CT2:** DEV accept → QA testing completed (maps to `CT_delivery`); **P75** likewise.
- After work may be planned as Changes, but **statistics stay at story grain** (fold Changes back to stories before P75).

### Paired improve Δ (positive = better)

```text
Δ_TP      = (TP_after − TP_before) / TP_before
speedup   = CT_before / CT_after
Δ_CT_speed = (CT_before − CT_after) / CT_after = speedup − 1
reduction = (CT_before − CT_after) / CT_before
```

Do not mix reduction % with speed-improve % as if they were different facts.

## Participants and independence

- Twelve participants → **six pairs** of two.  
- Pairs estimate independently (no sharing mid-workshop) to limit anchoring.  
- Public data labels pairs `Pair-1`…`Pair-6` only.

## Three stages

1. **Clarify backlog & estimate SP** — joint understanding of PBIs; freeze SP table (read-only thereafter).  
2. **Before** — traditional delivery: which stories finish in the window → `TP_before`; CT1/CT2 per counted story → P75.  
3. **After** — SDD method at high consensus: scope as Changes, map to stories, sum **frozen** SP → `TP_after`; story-level CT → P75; compute pair Δs.

Facilitator aggregates six Δs into median / IQR (and optionally min/max). **Do not** average all Before then all After then one global Δ. **Do not** drop pairs for ugly numbers (disqualify only for protocol violations, and document).

## Reading for management

Report central tendency as **median** of pair Δs with **IQR** as disagreement. State signal type `expert_estimate`. Close the loop later with `req_measured` under `metrics-definitions.md`.
