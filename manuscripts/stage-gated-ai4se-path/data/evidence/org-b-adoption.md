# Org-B adoption & engagement scope (anonymous)

**Client label in paper:** Org-B  
**Sector (Anon portrait):** Manufacturing enterprise (制造业).  
**Access constraint:** No consultant-side workspace mirror; client work stays on **client intranet only**. Facts below are author-supplied for Paper B §V — mark delivery status carefully.

**Phase (as of 2026-08-30 author briefing):** **Pilot exploration in progress.** Calendar target: **mid-July 2026 → mid-September 2026**. Do **not** write Org-B as consolidation-complete or organization-wide scaled.

**Internal only:** Legal entity name must not appear in `main.tex` / public packs until disclosure checklist allows.

---

## Timeline & adoption arc (decision facts)

| Window | What happened (Anon-safe) | Paper use |
|---|---|---|
| ~mid-Jul → ~mid-Aug (first ~month) | Other on-site consulting approaches led early exploration | Context only; **no firm names** |
| Transition | Client concluded those AI4SE transformation approaches were **not feasible** for their setting; **switched to this path as primary** | RQ3 adoption / method recognition |
| Recent (into late Aug) | This team is guiding **multiple pilot teams** through product R&D process梳理 under the AI4SE path | Explore evidence: multi-mode pilots underway |
| Target end | ~**mid-Sep 2026** close of exploration | Phase boundary |

**Suggested manuscript one-liner (editable):**  
> After an initial month of co-located alternative approaches proved infeasible for Org-B’s setting, the organization selected and is now executing the stage-gated AI4SE exploration path described here, with multiple pilot teams spanning distinct software delivery modes.

**Hard rule:** Never name other consultancies; never write a win/loss table; “infeasible” is a **client decision outcome**, not an author attack.

---

## Multi-mode pilot teams (explore design)

Org-B intentionally samples **heterogeneous software modes** in the same explore wave (representative teams, not full scale-out):

1. **Embedded** software teams  
2. **Internal-use** application development  
3. **Large, complex enterprise business** systems (external / customer-facing class)  
4. **AI Agent–oriented** software development teams  

**Paper B use:** Strengthens external validity *within* one org (mode diversity) while staying honest that this is still exploration, not enterprise rollout.

---

## Process context: IPD fit requirement

- Org-B’s incumbent product development regime follows **IPD (Integrated Product Development)** — the IBM-originated model widely taught/adapted in Chinese manufacturing enterprises (e.g., well-known Huawei-associated practice lineage).  
- Author note: spoken “Integrated Production Development” → standardize in English prose as **Integrated Product Development (IPD)**.  
- **Design constraint for the AI4SE path here:** the paradigm and playbook must be **adapted to IPD**, not assume a greenfield Agile-only org.

**Paper B use:** Industrial problem richness — stage gates / role model / human–AI split must map onto IPD decision and lifecycle structure.  
**Must not claim:** That Org-B has completed an IPD×AI4SE full process rewrite org-wide.

---

## User-harness AI Assets architecture constraints (method, not vendor lock-in)

The **user-harness AI Assets** framework is **SDD-oriented** with explicit non-goals:

| Requirement | Meaning for paper |
|---|---|
| **Open multi-SDD compatibility** | Harness must work with Spec-Driven Development stacks **of the OpenSpec / Superpowers / Spec Kit class** — these are **illustrative examples**, not an exhaustive allow-list |
| **Extensibility** | Architecture must remain able to support **future similar SDD frameworks** without redesigning the harness from scratch |
| **No single-framework lock-in** | Toolkit is a harness layer, not “Org-B must adopt only one SDD brand” |
| **Internal tool integration** | Must support **MCP** and **CLI** integration paths to Org-B’s internal engineering toolchain |

**Paper B use:** Explains *what* explore is inventing (a portable, extensible harness + playbook) vs buying a single IDE/plugin or single-SDD story.  
**Must not:** Dump proprietary MCP endpoint names, internal product brands, or claim production-complete integration; must not imply the three named stacks are the only supported ones.

**Naming policy:** Prefer phrasing like *“SDD frameworks such as OpenSpec, Superpowers, and Spec Kit, among others / and future peers”*.

---

## Stated engagement goals (explore-phase scope)

| # | Goal | Status note (2026-08-30) | Path mapping |
| ---: | --- | --- | --- |
| 1 | Explore AI4SE method/process + user-harness AI asset toolkit; define roles + human–AI division of labor | **In progress** — multi-team process梳理 underway | Stage 1 |
| 2 | End-to-end AI4SE operations playbook (Org-A–analog) + AI Assets toolkit (multi-SDD + MCP/CLI) | Explore deliverable target by ~mid-Sep; not marked accepted | Stage 1 → feeds 2 |
| 3 | Training outline/materials + certification system for later rollout | Scale-**prep**; in SOW | Stage 2/3 prep |
| 4 | Internal **seed coaches** for later scale-out | Scale-**prep**; in SOW | Stage 2 |
| 5 | Measurement scheme for the AI4SE paradigm | In SOW; **no Org-B numbers in Paper B** | Companion to Paper C |

---

## Honest claim boundaries (hard)

**May claim:**

- Explore window mid-Jul→mid-Sep 2026; still in explore as of late Aug.  
- Prior co-present approaches deemed infeasible → **this path selected as primary** (decision fact).  
- Multiple pilot teams across embedded / internal / complex enterprise / agentic modes; process梳理 in progress under IPD-fit constraint.  
- Harness designed for **open multi-SDD compatibility** (e.g. OpenSpec / Superpowers / Spec Kit **class**, extensible to future peers) + MCP/CLI to internal tools.  
- Sector: manufacturing enterprise (Anon).  
- SOW includes playbook, assets, training/cert, seed coaches, measurement scheme design.

**Must not claim without new evidence:**

- Explore closed successfully / all deliverables accepted.  
- Consolidation or org-wide scale started.  
- Named competitor comparison or “we beat X.”  
- Any Org-B ROI / maturity deltas.  
- Fingerprinting internal systems or full IPD transformation complete.

---

## Contrast with Org-A (for Discussion)

| | Org-A | Org-B |
|---|---|---|
| Calendar | ~6-week explore finished; consolidation started | ~2-month explore mid-Jul→mid-Sep; in progress |
| Process heritage | (see Org-A context) | **IPD** incumbent; AI4SE must adapt |
| Pilot shape | Enablement + vehicle | **Multi-mode** team sample in one wave |
| Adoption story | Deep gate + assets | **Method switch after infeasible alternatives** + ongoing pilots |
| Harness story | Plugins / playbook in handoff | Extensible multi-SDD harness (not locked to one stack) + MCP/CLI |
| Evidence depth | In-repo ledger | Author briefing only (no intranet mirror) |

---

## Remaining open questions

1. ~~Any Org-B co-author / stricter red lines?~~ **Closed 2026-09:** no Org-B co-authors; Anon pack locked.  
2. After mid-Sep: which of goals 1–5 will be safe to mark `delivered` for camera-ready (update this file then)?

**Provenance:** Author briefings 2026-08-30 (goals; timeline / IPD / multi-mode / harness; manufacturing sector; open SDD compatibility) · no client-repo pointers.
