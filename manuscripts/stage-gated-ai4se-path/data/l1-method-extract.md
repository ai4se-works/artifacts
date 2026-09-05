# L1 method extract (public inspection card)

**Purpose.** This file is a **self-contained method card** for external readers of the stage-gated AI4SE path manuscript. It supports inspection of the claim that Explore produced a **citable L1 method** (handbook v1.0 frozen at gate), without publishing the full client-facing deliverable.

**What this is**

- A **rewritten academic extract** of a consulting-authored Spec-Driven Development (SDD) end-to-end method guide (v1.0), as instantiated during Org-A Explore.
- Framed for gate inspection: principles, artifact chain, process stages, quality gates, and a few **normative clauses**.

**What this is not**

- Not the full playbook / operations handbook text.
- Not Org-A–branded customization chapters, intranet tool recipes, workshop transcripts, or opportunity Spec/BP bodies.
- Not permission to treat catalogued L3 stubs as production-ready (see [`l3-stub-map.md`](l3-stub-map.md)).

**Ownership / disclosure.** Full handbook text remains confidential under partner constraints. This extract is released under the repository CC-BY-4.0 license for manuscript inspection only.

---

## 1. Why a method card (maps to G1 “playbook citable”)

At Explore closeout, G1 asks whether a method can be **shown and referenced with gaps visible**. A brochure slogan is not enough; neither is an unreadable private dump. This card gives reviewers:

1. Proof of **depth** (chapter map of the frozen v1.0 guide).
2. The **transferable kernel** (principles + artifact flow + 5+1 stages + three quality gates).
3. **Normative clauses** aligned with the manuscript’s paraphrased L1 extract.
4. Explicit **known gaps** assigned to Consolidation (v2), matching “read right but did not run.”

---

## 2. Structure of the frozen v1.0 guide (chapter map)

The frozen L1 handbook is organized as follows (titles only; bodies withheld):

| Part | Chapters (titles) |
|---|---|
| Foreword | From Implementation Scarcity to Definition Scarcity |
| I — Paradigm and Principles | Ch.1 Agile → Spec-Driven; Ch.2 Five First Principles |
| II — System Framework | Ch.3 Role System; Ch.4 Artifact System (Living Spec); Ch.5 Process System (5+1 + three gates) |
| III — Practice and Adoption | Ch.6 Human–AI Collaboration; Ch.7 Verification System; Ch.8 Metrics (trust); Ch.9 AI Capability Assets; Ch.10 Rollout / Scaling; Ch.11 Pitfalls and Anti-Patterns |
| IV — Organization and Future | Ch.12 Organizational / Talent Evolution; Ch.13 Outlook |
| Appendices | Supporting reference material |

This map is the inspectable answer to “was there a real handbook, or only slides?”

---

## 3. Five first principles (transferable kernel)

| # | Principle | One-line meaning for gate inspection |
|---|---|---|
| 1 | **Spec as Source of Truth** | One authoritative Living Spec; disputes about “what the system should do” are settled there; code is a derived snapshot |
| 2 | **Precision over Consensus** | Intent must be precise enough for machine execution; vague specs force model guessing |
| 3 | **Verification over Trust** | Non-determinism ⇒ every AI output needs systematic verification; past success does not license this run |
| 4 | **Delta over Rewrite** | Brownfield change is expressed as ADDED / MODIFIED / REMOVED deltas, not a full-system rewrite |
| 5 | **Human Accountability** | Final outcomes, architecture decisions, and risk acceptance remain human-owned |

**Independence corollary (from principle 3).** The executor must not be the sole verifier. AI-generated output must not be self-attested by the same generating session as “verified.”

---

## 4. Artifact chain (Living Spec centered)

Durable vs transitional artifacts:

```text
Intent → Change Proposal
       → Delta Spec (ADDED / MODIFIED / REMOVED)
       → Design & Task Plan
       → [generation + independent verification]
       → Verified Increment
       → merge back into Living Spec (sole durable endpoint)
```

| Artifact | Role |
|---|---|
| **Living Spec** | Sole durable Source of Truth; continuously updated; never “finished” |
| **Change Proposal** | Human-facing why/what/scope |
| **Delta Spec** | Precise change unit for execution and verification design |
| **Design & Task Plan** | How + atomic AI-executable tasks linked to delta items |
| **Verified Increment** | Trustworthy deliverable: working software + verification evidence + spec conformance—not “code that compiled” |

**DoV replaces DoD.** Completion means *spec-verified*, not merely *code written / tests green by convention*.

---

## 5. 5+1 end-to-end stages and three quality gates

| Stage | Name | Core question | Gate |
|---|---|---|---|
| 0 | Project baseline / harness bootstrap | By what rules does this project run? | — (checklist DoV) |
| 1 | Intent discovery & proposal | What are we building; what is out of scope? | — |
| 2 | Spec definition & align | What does “correct” look like? | **Align Gate (process G1)** |
| 3 | Design planning & breakdown | How do we implement it? | — |
| 4 | Implementation, verification & feedback | Built to plan—is it right? | **Verify Gate (process G2)** |
| 5 | Codify, archive & evolve | How do we retain learning / keep Living Spec consistent? | **Merge & Archive Gate (process G3)** |

| Process gate | Intercepts | Pass intuition |
|---|---|---|
| Align (G1) | Directional / spec ambiguity errors | Spec complete, precise, verifiable; no conflict with Living Spec |
| Verify (G2) | Execution / fidelity errors | Implementation matches Spec; independent verification evidence complete |
| Merge & Archive (G3) | Consistency / drift errors | Delta merged; Living Spec self-consistent; lessons codified |

**Note on gate vocabulary.** These *process* gates (Align / Verify / Merge) live inside the method guide. The manuscript’s *transformation* gates (Explore closeout G1 / Scale-entry G2) are organizational admission controls defined in [`gate-rubric.md`](gate-rubric.md). Both layers matter; they must not be conflated.

---

## 6. Normative clauses (inspection-facing)

The following clauses are **paraphrased / redacted** for public release. They illustrate the kind of normative content that made L1 *citable* at Explore—not a verbatim dump of client handbook text.

| ID | Normative expectation | Why it matters at Explore G1 |
|---|---|---|
| N1 | Every accepted increment must cite a Living Spec **delta identifier** (traceable change unit) | Makes the method chain auditable; blocks “code without a spec delta” |
| N2 | A **human verifier** distinct from the apply/generation agent must be named for acceptance | Enforces human accountability + separation of duties |
| N3 | **Refuse** “generated output equals verified” shortcuts (no AI self-attestation as the sole verification) | Blocks theater verification; aligns with Verification-over-Trust |
| N4 | Until Align-gate (process G1) passes, implementation generation must not proceed as if the Spec were approved | Precision-before-speed; reduces rework economics |
| N5 | Unmapped critical code (no Spec/delta linkage) is treated as suspect for hallucination review | Traceability as a quality skeleton |

These clauses are the public counterpart of the manuscript’s illustrative L1 extract.

---

## 7. Known v1 gaps → Consolidation (honesty for G1)

Explore G1 can pass with a citable v1 **and** visible gaps. Gaps recorded for Stage-2 (not claimed fixed at closeout):

| Gap class | Public description | Consolidation intent |
|---|---|---|
| Runnable fidelity | Some handbook clauses “read right” but were not yet backed by a hardened primary L3 path | Playbook v2 + L3 stub→ready (see [`l3-stub-map.md`](l3-stub-map.md)) |
| Teachability | v1 was showable/citable; org-wide teach-the-teacher not yet demonstrated | Seed coaches; “team can teach” exit |
| Observation themes | Themes #5 and #9 remained observation in the L2 index | Converge or keep explicitly flagged ([`theme-index.csv`](theme-index.csv)) |

---

## 8. How to use this card with the rest of the pack

| If you want to check… | Open |
|---|---|
| Organizational Explore/Scale admission | [`gate-rubric.md`](gate-rubric.md) |
| L1–L4 readiness summary | [`asset-ledger.csv`](asset-ledger.csv) |
| Theme release vs observation | [`theme-index.csv`](theme-index.csv) |
| Executable stub honesty | [`l3-stub-map.md`](l3-stub-map.md) |
| This method kernel | **this file** |

**Reader takeaway.** The Explore gate did not require open-sourcing a client deliverable. It required a **citable method with inspectable structure, normative constraints, and declared gaps**—which this card is intended to demonstrate.
