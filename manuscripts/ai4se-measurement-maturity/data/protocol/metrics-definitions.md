# Metrics definitions (public protocol)

Anonymized English distillation of the internal metrics specification (evidence E3). Sufficient to reproduce Throughput and Cycle Time definitions used in Paper C and `derived/` tables. Not a dump of internal client platform field catalogs.

## Scope

Core indicators: **Throughput** and **Cycle Time** (three variants in the full spec; workshop primary-reports two).

## Throughput

### Definition

Story-point volume completed per effective person-day in an observation window — team delivery rate.

### Formula

```text
Throughput = SUM(Story Points of Completed Stories in Observation Window) / PersonDays
```

Unit: **points / person-day**.

Relative change (Before / After):

```text
Δ_Throughput = (Throughput_after − Throughput_before) / Throughput_before
```

(Workshop field reporting often uses Σ SP alone when PersonDays is held constant; see workshop protocol.)

### Factors

**Story Points**

- Complexity points on a story card (Fibonacci or team scale).
- Use points recorded at completion (do not rewrite history for the metric).
- Include `type = Story`; exclude defect/bug/support/subtask/spike/epic unless a study explicitly extends scope.

**Completed in window**

- A story is completed when it first reaches **QA testing completed** (or platform-equivalent test-done state).
- Intermediate states (last commit, desk check, UAT entry) do **not** count as completed for Throughput.
- Attribute the story’s full SP to the window containing `T_qa_passed`.

**PersonDays**

```text
PersonDays = Σ_i (WorkingDays_i − LeaveDays_i)
```

Over team members in the window; calendar working days minus leave. No allocation-ratio partial FTE folding in the base definition.

**Observation window**

- Any closed interval; common baseline vs workshop windows are study-specific (e.g., trailing 90d baseline vs ~28d workshop period in field use).

## Cycle Time

### Definition

Calendar duration from **DEV accept** (first Backlog → Required Analysis) to a chosen delivery milestone.

| Variant | Spec id | End event |
|---------|---------|-----------|
| Code complete | `CT_code` | Latest related commit (`committer_date`) |
| Delivery / QA done | `CT_delivery` | QA testing completed |
| Production | `CT_prod` | Production release timestamp |

Same story: `CT_code ≤ CT_delivery ≤ CT_prod`.

### Formula (per story `s`)

```text
CT_code(s)     = T_last_commit(s)   − T_start(s)
CT_delivery(s) = T_qa_passed(s)     − T_start(s)
CT_prod(s)     = T_prod_released(s) − T_start(s)
```

Relative duration change (spec appendix / platform alignment form):

```text
Δ_CT_x = (CT_x_after − CT_x_before) / CT_x_before
```

(Negative means shorter.) Workshop **speed-improve** narrative uses a different denominator — see workshop protocol.

### Timestamp conventions

- **`T_start`:** first transition into Required Analysis; if bounced, keep **first** entry.
- **`T_last_commit`:** max committer_date among commits linked by story id; stories with no commits drop out of `CT_code`.
- **`T_qa_passed`:** same completion timestamp used for Throughput inclusion.
- **`T_prod_released`:** production deploy time (platform field as available).

## Signal types (when publishing numbers)

| Label | Use |
|-------|-----|
| `expert_estimate` | Facilitated judgment / workshop |
| `process_signal` | Maturity or other process assessment |
| `req_measured` | Computed from requirements platform/Git under these definitions |

This public pack’s Org-A effectiveness tables are **`expert_estimate` only**. Do not invent `req_measured` claims from workshop estimates.
