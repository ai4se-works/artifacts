# Threats to validity

Structured for Paper C §Threats. Keep Results and Threats symmetric: every strong quantitative claim has a matching boundary here.

## Construct validity

- **Story points under AI4SE.** SP are intended to capture inherent demand complexity independent of method. SDD may change how work *feels* complex; freezing SP is a design choice for separability, not proof that complexity is invariant.
- **Throughput / CT constructs.** Workshop Σ SP and P75 CT are operationalizations of delivery throughput and cycle time aligned to the metrics spec, but they are still **estimates of future delivery**, not observed platform histories for the After condition.
- **Maturity levels.** L1–L5 rubrics and domain means are process constructs; they do not measure product quality or business outcome directly.

## Internal validity

- **Estimation bias.** Expert pairs may be systematically optimistic (or conservative). Median/IQR reduce single-pair extremes but do not eliminate shared optimism.
- **Facilitator effects.** Protocol framing, fixed conditions, and high-consensus prompting can shape estimates; results are not a blind controlled experiment.
- **Maturity re-assessment.** Before/after maturity used the same facilitator-guided instrument; learning-to-the-test and social desirability may inflate small lifts.
- **No causal isolation beyond fixed conditions.** Backlog / team / window are held fixed, but other confounders (fatigue, concurrent org change, tool availability) remain.

## External validity

- **Single industrial case (Org-A).** One ~6-week enablement pilot in one software organization; not a multi-site sample.
- **High-consensus precondition.** After estimates assume teams already understand the SDD method pack; results do not generalize to cold-start adoption.
- **Workshop grain ≠ org grain.** Pair estimates under a fixed backlog do not license extrapolating to portfolio or enterprise productivity.

## Conclusion validity

- **Estimate ≠ platform-measured.** All workshop productivity rows are `expert_estimate`. Treating them as `req_measured` ROI would be an invalid conclusion.
- **Modest maturity Δ ≠ “no effect” / ≠ “transformation complete.”** Short pilots often show limited capability movement; overclaiming significance from small domain deltas would be invalid, as would dismissing the dual-lens scheme because maturity moved slowly.
- **Small n (6 pairs).** Median/IQR are appropriate descriptive summaries, not grounds for strong inferential claims or industry-wide multiplier law.

**Mitigations used in the scheme:** signal-type labels; fixed conditions + frozen SP; paired Δ then cross-pair median/IQR; explicit promissory-expectation wording; dual-lens dashboard rather than a single multiplier.

---

## Paper B–specific threats

- **Single deep case (Org-A) + early second case (Org-B).** Org-A supplies the primary longitudinal gate and asset narrative; Org-B is an in-progress explore pilot at manuscript freeze — not a balanced multi-site sample.
- **Participant-observer / consultant bias.** Authors facilitated enablement, gate framing, and asset authoring; consolidation and readiness judgments may reflect consultant–client alignment rather than independent audit.
- **Org-B facts from author briefing without intranet artifact mirror.** Org-B prose relies on SOW-aligned author briefing and `org-b-adoption.md`; no workspace mirror of client intranet artifacts — limits external verification of Org-B claims.
- **Adoption-after-alternatives narrative without naming firms.** Org-B’s “after alternatives” positioning is described at sector/pattern level without naming vendors or competitors — readers cannot independently reconcile competitive context.
- **Construct: “scale-ready” is gate-based, not ROI-based.** Paper B treats scale feasibility as stage-gate and asset-readiness constructs; absence of platform-measured ROI or completed rollout must not be read as proof of ineffectiveness, nor must bounded explore signals be read as scale completion.
