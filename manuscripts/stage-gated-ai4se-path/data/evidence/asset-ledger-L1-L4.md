# Org-A asset ledger (L1–L4)

**Paper B use:** §IV case outcomes — method-asset inventory with honest readiness.  
**Client label:** Org-A only.  
**Authority:** Handoff package `99-archive/handoff/` (L1–L4 ledger in `README.md`).

---

## Layer inventory

| Layer | What | Org-A status (honest) | Pointer |
|---|---|---|---|
| **L1** | Method playbook / operations handbook | **Frozen v1.0, citable.** SDD end-to-end handbook passed explore gate (“Playbook citable”); consolidation target is v2 (remove “reads right but doesn’t run” clauses). Not yet v2. | `99-archive/handoff/01-playbook/SDD 端到端软件开发方法与实践指导手册（V1.0）.md` |
| **L2** | Opportunity Spec / Best Practice assets | **Release set countable.** 11 Best Practices + 11 Specs in release index; `#5` and `#9` remain **observation items** (not fully converged). | `99-archive/handoff/02-opportunity-assets/` (`README-release-index.md`) |
| **L3** | Executable plugins / skills / recipes (`/sdd`, etc.) | **Catalogued, largely stub on main chain.** Formal plugin pack exists (`/sdd`, skills, recipes, adapters); explore gate recorded honest readiness as **stub ≠ production-ready**. Consolidation work: stub → ready on primary execution path. | `99-archive/handoff/01-playbook/ai4se-plugins/` (also `ai4se-plugins.zip`) |
| **L4** | Evidence pack pointers (maturity / effectiveness) | **Exists with stated boundaries.** Maturity before/after and effectiveness workshop materials present; signals are **process / expert-estimate**, not platform-measured ROI. Quantitative claims → Paper C / `public-data/derived/` only — **do not paste C numbers here.** | `99-archive/handoff/03-evidence/` (maturity/, metrics/) |

---

## Readiness discipline

Frozen ledgers or stubs are **not** production-ready. Paper B must not equate “catalogued” with “runnable at scale.”

---

## Claim boundaries

- **L1:** cite v1.0 existence and gate pass; do not imply v2 consolidation complete.  
- **L2:** inventory counts and observation flags only; do not overstate convergence.  
- **L3:** presence of `/sdd` and plugin tree ≠ org-wide executable readiness.  
- **L4:** cite pack existence and signal-type limits; defer numbers to Paper C evidence chain.

**Related:** `phase1-gate.md` (executable-asset honesty criterion); `scale-path.md` (Stage 2 hardening goals).
