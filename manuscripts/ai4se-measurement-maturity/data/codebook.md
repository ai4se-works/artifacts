# Public-data codebook

Field definitions for CSVs under `derived/`. All workshop productivity numbers are **expert estimates** (facilitated promissory expectations under a fixed backlog/team/window), not platform-measured ROI. Maturity scores are **expert-facilitated process assessments** (`process_signal`), not platform telemetry.

Internal source workbooks are **not** shipped in this pack. Regenerate with `scripts/extract_derived_from_xlsx.py` when authorized local handoff xlsx are present.

## Signal types

| `signal_type` | Meaning |
|---------------|---------|
| `expert_estimate` | Facilitator / SME judgment from the effectiveness workshop |
| `process_signal` | Maturity model assessment (L1–L5 capability levels / domain means) |
| `req_measured` | Reserved; **not used** in the current derived tables |

## `maturity_domain_scores.csv`

| Column | Type | Description |
|--------|------|-------------|
| `domain_id` | string | `D1`…`D6` |
| `domain_name_en` | string | English domain label (see translation table below) |
| `before` | float | Domain mean maturity before intervention (mean of 3 capability numeric levels) |
| `after` | float | Domain mean maturity after re-assessment |
| `delta` | float | `after − before` |
| `signal_type` | string | Always `process_signal` |
| `notes` | string | Counts of L1 and L3+ capabilities before→after within the domain |

### Domain name translations

| ID | Chinese (source) | English |
|----|------------------|---------|
| D1 | 效能地基 | Efficiency Foundation |
| D2 | 流程层 | Process Layer |
| D3 | 工程方法与工作纪律 | Engineering Methods & Discipline |
| D4 | 工具层 | Tooling Layer |
| D5 | Harmony 人机/Agent 协作 | Human–Agent Collaboration |
| D6 | 组织与文化 | Organization & Culture |

## `maturity_capabilities.csv`

| Column | Type | Description |
|--------|------|-------------|
| `domain_id` | string | Parent domain `D1`…`D6` |
| `capability_id` | string | `D1.1`…`D6.3` (18 capabilities) |
| `capability_name_en` | string | English capability label |
| `before` | int | Numeric level before (1–5) |
| `after` | int | Numeric level after (1–5) |
| `delta` | int | `after − before` |
| `before_level` | string | Level code `L1`…`L5` (Chinese descriptors stripped) |
| `after_level` | string | Level code `L1`…`L5` |
| `signal_type` | string | Always `process_signal` |

Level scale (model): L1 Initial · L2 Toolized · L3 Engineered · L4 Systematized · L5 Autonomous.

## `effectiveness_pair_summary.csv`

Workshop pairs anonymized as `Pair-1`…`Pair-6`. Member-name columns from the source sheet are **never** copied.

| Column | Type | Description |
|--------|------|-------------|
| `pair_id` | string | `Pair-1`…`Pair-6` |
| `tp_before` | float | Throughput (Σ story points) before |
| `tp_after` | float | Throughput after (expert estimate) |
| `tp_delta_improve` | float | Throughput improve Δ = `(After−Before)/Before` |
| `ct1_p75_before` | float | CT1 (to last commit) P75 days before |
| `ct1_p75_after` | float | CT1 P75 days after |
| `ct1_speedup` | float | Speed multiple = `Before/After` |
| `ct1_reduction_pct` | float | Duration reduction = `(Before−After)/Before` |
| `ct2_p75_before` | float | CT2 (to QA test done) P75 days before |
| `ct2_p75_after` | float | CT2 P75 days after |
| `ct2_speedup` | float | Speed multiple = `Before/After` |
| `ct2_reduction_pct` | float | Duration reduction = `(Before−After)/Before` (**derived**; source xlsx has no CT2 缩短% column) |
| `signal_type` | string | Always `expert_estimate` |

**Schema note:** Source sheet `汇总对比报告` headers include CT1 缩短% but only CT2 速度倍数 (no CT2 缩短%). `ct2_reduction_pct` is computed in the extractor. CT “Δ提效” columns in the xlsx use speed-improve form `(Before−After)/After`; pair CSV exposes **speedup** and **reduction_pct** per the public schema rather than the raw Δ提效 CT columns.

## `effectiveness_aggregate.csv`

Cross-pair summary of **delta-improve** distributions (n=6), taken from the workbook’s section “跨组汇总”.

| Column | Type | Description |
|--------|------|-------------|
| `metric` | string | `tp_delta_improve`, `ct1_speed_delta_improve_p75`, or `ct2_speed_delta_improve_p75` |
| `stat` | string | `median`, `p25`, `p75`, `iqr`, `min`, `max` |
| `value` | float | Statistic value (fractional improve Δ, not percent display) |
| `signal_type` | string | Always `expert_estimate` |

Primary paper claims should prefer **median + IQR** of these deltas; do not cherry-pick max pair.

## `figure_sources.json`

Maps planned paper figures F1–F4 to derived files / columns. See that file for the authoritative figure→CSV binding.
