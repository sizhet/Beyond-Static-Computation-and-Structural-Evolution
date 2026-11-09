# Structural Claims Registry

**Repository:** Beyond Static Computation and Structural Evolution  
**Version:** 1.0.0 (initial research registry)  
**Date:** 2026-11-09  
**Status:** Research claims; no experimental confirmation asserted  
**Maintainers:** Sizhe Tan & GPT-Obot

## 1. Purpose and scope

This registry is the central traceability index for the research program connecting **ASSI**, **D-BTP**, **CDE**, **WE-SIO**, and **OCSRE**. It records what the program proposes, what would count as evidence, which specifications and experiments can test each claim, and what remains unresolved. A registry entry is **not** evidence of truth. Nor does a specification or a successful conformance test, by itself, establish comparative performance.

The intended evidence path is:

`Research claim → contract/specification → falsifiable hypothesis → controlled experiment → evidence review → qualified capability → relay`

Claims can remain open, be narrowed, be rejected, or be split into more precise claims. Negative results and boundary conditions are first-class research outputs.

## 2. Status vocabulary and promotion rules

| Status | Meaning | Minimum evidence |
|---|---|---|
| **Proposed** | A defined research proposition awaiting relevant evaluation | Traceable statement and falsification conditions |
| **Specified** | Interfaces or operational behavior have a testable contract | Versioned specification and conformance criteria |
| **Under Test** | A preregistered evaluation is actively underway | Frozen protocol, baselines, datasets, metrics |
| **Supported (Scoped)** | Evidence supports a claim only within explicitly stated conditions | Reproducible results, uncertainty, scope and limitations |
| **Not Supported** | Tests failed to show the predicted effect | Complete results, including statistical and practical interpretation |
| **Refuted (Scoped)** | Evidence contradicts a sufficiently precise claim in its tested scope | Replicable counterevidence and documented scope |
| **Inconclusive** | Evidence is insufficient or ambiguous | Reasons, missing information and next tests |
| **Superseded** | Replaced by a revised or decomposed claim | Link to successor claim(s) |

**Initial status:** Every claim in this version is **Proposed**. Some related interfaces have been drafted, but no claim is promoted merely because the corresponding document exists. “Supported (Scoped)” requires an independently reviewable evidence package, not an author judgment alone. Relay eligibility is separately assessed; a supported result is not automatically portable to a new domain.

## 3. Claim registration schema

Each claim record should maintain these fields as it matures:

```yaml
claim_id: SCR-001
statement: "A falsifiable, scoped proposition"
claim_type: comparative | mechanism | interoperability | governance | security
scope: "Systems, workloads, assumptions, and exclusions"
source_documents: []
specifications: []
hypotheses: []
experiments: []
baselines: []
primary_metrics: []
falsification_conditions: []
status: Proposed
evidence_records: []
negative_results: []
explicit_leftovers: []
relay_eligibility: Not assessed
last_reviewed: 2026-11-09
```

Stable IDs are never recycled. Changes in wording that materially alter the proposition require a revision note; incompatible changes should receive a new ID and link to the predecessor.

## 4. Master registry

**Document keys:** `D001`–`D006` denote `docs/001-...md` through `docs/006-...md`; `S1`–`S3` denote `specifications/SPEC-001` through `SPEC-003`; `E1`–`E3` denote `experiments/EXP-001` through `EXP-003`. `TH-nnn` refers to the corresponding entry in `research/TESTABLE-HYPOTHESES.md`. All listed mappings are *planned test coverage*, not completed verification.

| ID | Research claim (testable interpretation) | Primary source | Contract | Hypothesis | Lab | Status |
|---|---|---|---|---|---|---|
| SCR-001 | Persistent object context reduces repeated reconstruction effort versus matched conventional pipelines. | D002 | S1 | TH-001 | E1 | Proposed |
| SCR-002 | Core Frame + Plugins reduces the cost of safe extension without unacceptable runtime or semantic overhead. | D002 | S1 | TH-002 | E1 | Proposed |
| SCR-003 | Explicit SQL structural, semantic and operational alignment reduces meaning-changing transformations. | D002 | S1 | TH-003 | E1 | Proposed |
| SCR-004 | Constraint-aware Delta evolution improves feasible dynamic scheduling outcomes under equal resource budgets. | D003 | S1 | TH-004 | E2 | Proposed |
| SCR-005 | Delta provenance and path memory improve auditability and reduce invalid repeated exploration. | D003 | S1 | TH-005 | E2 | Proposed |
| SCR-006 | Controlled evolution of candidate generators improves search performance across changed workloads. | D003 | S1 | TH-006 | E2 | Proposed |
| SCR-007 | Persistently recorded residuals improve subsequent learning or diagnosis over discard-and-recompute baselines. | D004 | S1 | TH-007 | E1, E2 | Proposed |
| SCR-008 | Residual localization improves useful-discovery yield per unit of observation or computation. | D004, D005 | S1, S2 | TH-008 | E1, E3 | Proposed |
| SCR-009 | Persistent structural context reduces response latency after meaningful environmental changes. | D004, D005 | S2 | TH-009 | E1, E2 | Proposed |
| SCR-010 | Selective adaptive observation retains most useful discovery coverage at lower cost than exhaustive observation. | D005 | S2 | TH-010 | E1, E3 | Proposed |
| SCR-011 | Two-Way CCC checks reduce spurious pattern promotion relative to one-direction checks, without implying causality. | D005 | S2, S3 | TH-011 | E1, E3 | Proposed |
| SCR-012 | A persistent discovery loop produces more reusable validated capabilities, not merely more candidate patterns. | D005, D006 | S2, S3 | TH-012 | E1, E2, E3 | Proposed |
| SCR-013 | Learning observation and discovery policies improves later validated-discovery efficiency under matched budgets. | D005 | S2 | TH-013 | E1, E3 | Proposed |
| SCR-014 | Explicit opportunity records improve allocation of limited monitoring and experimental resources. | D005 | S2 | TH-014 | E1, E3 | Proposed |
| SCR-015 | Evidence-bound capability packages improve safe reuse across domains compared with unqualified result sharing. | D006 | S3 | TH-015 | E1, E2, E3 | Proposed |
| SCR-016 | Relaying failed attempts and applicability limits reduces repeated dead ends in downstream research. | D006 | S3 | TH-016 | E1, E2, E3 | Proposed |
| SCR-017 | Permission, provenance and validation contracts reduce adversarial contamination during structural relay. | D001, D006 | S3 | TH-017 | E1, E2, E3 | Proposed |
| SCR-018 | The integrated stack provides positive net utility after full compute, maintenance, validation and relay costs. | D001–D006 | S1–S3 | TH-018 | E1, E2, E3 | Proposed |

## 5. Scope, baselines and disconfirmation criteria

The table below sets the **minimum distinguishing test** for each claim. Experimental protocols must additionally specify datasets, splits, random seeds, power or precision targets, practical-effect thresholds, and total resource budgets before outcome inspection.

| Claim | Primary comparator | Principal measure | A result that challenges the claim |
|---|---|---|---|
| SCR-001 | Stateless or rebuilt-context pipeline | Reconstruction time and total cost | No material improvement after persistence overhead |
| SCR-002 | Monolithic extension or conventional plugin system | Extension effort, breakage, overhead | No improvement or greater integration risk |
| SCR-003 | Direct SQL mapping without explicit semantic contract | Semantic violations and mapping cost | Equivalent accuracy at lower complexity |
| SCR-004 | Rolling horizon, incremental repair, ALNS | Feasibility, fleet count, ride time, compute | No advantage over tuned baselines under hard constraints |
| SCR-005 | Logging-only and no-path-memory variants | Repeated invalid states, trace completeness | Extra memory with no audit or search benefit |
| SCR-006 | Fixed candidate generator | Held-out search quality per unit cost | Adaptation overfits or yields no generalizable gain |
| SCR-007 | Residual discard or summary-only baseline | Downstream validated task improvement | Retention adds noise or cost without benefit |
| SCR-008 | Random/uniform and conventional prioritization | Valid discoveries per observation budget | No higher yield on blind evaluation |
| SCR-009 | Restart/recompute and incremental baseline | Post-change adaptation latency | No gain when maintenance overhead is included |
| SCR-010 | Exhaustive and fixed-rate monitoring | Discovery recall at matched cost | Missed important events outweigh savings |
| SCR-011 | One-way CCC and standard statistical checks | False discovery rate, precision | No reduction after multiple-testing control |
| SCR-012 | One-shot pattern mining | Independently validated reusable capabilities | More patterns but no more useful capabilities |
| SCR-013 | Fixed discovery policy | Future-period validated yield | Improvement disappears in held-out periods |
| SCR-014 | Conventional resource scheduling | Net value per resource unit | Opportunity metadata adds no decision benefit |
| SCR-015 | Unstructured transfer and conventional model packaging | Successful independent transfer rate | Evidence package adds cost without safer reuse |
| SCR-016 | Success-only relay | Repeated failures and wasted search | No reduction or negative transfer |
| SCR-017 | Relay without provenance/permission gates | Contamination and unauthorized promotion rate | Attack success unchanged or legitimate reuse unduly blocked |
| SCR-018 | Best feasible combination of established methods | Total net utility, reliability, lifecycle cost | No robust positive net advantage |

**No straw-man baselines:** Conventional incremental databases, online learning, dynamic programming, model-predictive control, adaptive large-neighborhood search, anomaly detection and provenance systems must be represented where relevant. An integrated system is not novel solely because it combines familiar components.

## 6. Cross-cutting architectural propositions

The following propositions organize the research but are **not additional empirical claims** unless operationalized with new IDs:

- **Object-native continuity:** identity, state, relations, history and capabilities may be maintained together without forcing all data into one universal physical store.
- **Residual-first in-situ intelligence:** unresolved differences remain addressable and actionable instead of disappearing at component boundaries.
- **Constrained structural evolution:** both state and, when explicitly permitted, the constraint/policy representation may evolve; safety invariants must remain enforceable.
- **Persistent selective presence:** broad potential coverage must be reconciled with finite attention, storage and compute.
- **Evidence-bound relay:** a transfer artifact carries claims, provenance, contracts, known failures, unresolved questions and restrictions.

A separate open research question concerns **CDE as a dynamic Localization pillar within SIF**. This is an architectural positioning proposal, not an experimentally established superiority claim; see `FUTURE-DIRECTIONS.md` and `research/OPEN-QUESTIONS.md`. It should receive a new claim ID only after an operational definition and comparative test are agreed.

## 7. Experiment-to-claim traceability

### E1 — SQL Discovery Laboratory

Primary coverage: SCR-001–003, SCR-007–009, SCR-010–015. Use temporal integrity for CDC streams, explicit semantic ground truth where available, matched database/incremental baselines, and independent review of discovered relationships. Record storage and maintenance costs. Avoid promoting correlations to causal claims.

### E2 — Dynamic Scheduling Laboratory

Primary coverage: SCR-004–007, SCR-009, SCR-012, SCR-015–018. Hard safety, capacity and service constraints precede optimization. Compare with well-tuned rolling-horizon, incremental-repair and ALNS systems. Evaluate under demand shifts and distribution changes; prevent reuse of forbidden path deltas, and establish loop termination or bounded computation.

### E3 — Stock Pattern Laboratory

Primary coverage: SCR-008, SCR-010–015, SCR-018. Use point-in-time universes, delisting-aware data, walk-forward testing, multiple-hypothesis correction, embargo where appropriate, transaction costs, slippage, liquidity and risk controls. Separate statistical pattern validity from deployable economic value. This lab is research-only and is not evidence of investment performance.

### Cross-domain relay and adversarial tests

SCR-015–018 require dedicated transfer and security protocols spanning at least two environments, with independently executed recipient-side conformance and validation. A source-domain result cannot be counted as successful transfer by itself.

## 8. Evidence package and review contract

A claim may be reviewed for scoped support only when an evidence package includes:

1. Immutable claim ID and exact versioned wording.
2. Protocol registration timestamp and deviations log.
3. Dataset provenance, licensing, temporal boundaries and access restrictions.
4. Implementations, baselines, tuning budgets, environment and seeds.
5. Primary metrics, effect sizes, uncertainty intervals and cost accounting.
6. Ablations, sensitivity tests, negative outcomes and failure cases.
7. Threats to validity, leakage checks and scope limitations.
8. Reproduction instructions and an independent review record where feasible.
9. Links to specification-conformance outcomes, which remain distinct from empirical outcomes.
10. Relay eligibility decision, with conditions, permissions and expiration/revalidation triggers.

Recommended evidence path: `research/evidence/SCR-###/<study-id>/`. This path is **proposed**, not a claim that evidence files already exist.

## 9. Relay eligibility and trust boundaries

Use the following independent decision labels: **Not Assessed**, **Not Eligible**, **Eligible for Experimental Relay**, and **Eligible for Scoped Validated Relay**. Eligibility must be explicitly approved, not inferred from claim status.

- **Experimental Relay** may distribute a proposed method with conspicuous unvalidated labeling, restrictions and reproducible tests.
- **Scoped Validated Relay** requires reviewed evidence, versioned interfaces, provenance, permissions, recipient-side checks and a clearly stated validity domain.
- Failed, refuted or inconclusive claims may still be relayed as **research findings**, never as validated operational capabilities.
- Changes in domain, data distribution, policy, threat model or implementation invalidate automatic portability and may trigger revalidation.

The security perspective of ASSI is especially important: a plausible evidence trail can itself be adversarially constructed. Validate signatures, provenance, permissions and independent measurements where applicable; do not treat a relay package as trusted merely because it is structurally well formed.

## 10. Explicit leftovers and unresolved divergences

| ID | Unresolved issue | Related claims | Required next step |
|---|---|---|---|
| L-001 | Object persistence may impose prohibitive storage or maintenance cost. | 001, 007, 009, 018 | Cost-aware ablation |
| L-002 | Plugin modularity may trade simplicity for semantic drift. | 002, 003 | Contract stress tests |
| L-003 | Evolving constraints may create unsafe or incomparable objectives. | 004, 006 | Invariant and policy governance tests |
| L-004 | Residual accumulation may amplify noise and spurious discoveries. | 007, 008, 011 | Retention/forgetting controls |
| L-005 | Selective observation can miss rare but decisive events. | 010, 014 | Worst-case and recall evaluation |
| L-006 | Bidirectional consistency is not causal identification. | 011 | Confounding and negative-control tests |
| L-007 | Candidate generation may improve benchmarks but not transferable capabilities. | 006, 012, 013, 015 | Out-of-domain tests |
| L-008 | Relay may propagate compromised or obsolete evidence. | 015–017 | Adversarial provenance tests |
| L-009 | Integrated overhead may outweigh gains from individual mechanisms. | 018 | Full lifecycle accounting |
| L-010 | CDE/SIF Localization relation lacks a comparative operational benchmark. | Cross-cutting | Define localization metrics and baselines |

Do not silently close leftovers. Each closure requires a rationale and a link to a supporting record; unresolved items should remain visible through releases.

## 11. Maintenance and change control

- **Before a new release:** reconcile claim wording with papers, specifications, testable hypotheses and experiment plans; verify links and statuses; publish known negative results.
- **When a protocol changes:** preserve the earlier version and record the reason, especially if outcomes were already observed.
- **When evidence arrives:** update only the supported scope, include uncertainty and competing explanations, and assign a reviewer.
- **When a claim fails:** preserve the failure and evaluate whether a narrower successor claim is scientifically warranted; do not erase the original.
- **When a capability is relayed:** attach the evidence and boundary conditions; monitor for drift and revalidation needs.

Suggested change-log line: `YYYY-MM-DD | SCR-### | previous → new status | evidence ref | reviewer | scope note`.

## 12. Canonical document map

**Core papers**

- [`docs/001-Five-DOI-Peaks.md`](../docs/001-Five-DOI-Peaks.md)
- [`docs/002-WE-SIO-Object-Native-Intelligence.md`](../docs/002-WE-SIO-Object-Native-Intelligence.md)
- [`docs/003-Structural-Evolution-Computing.md`](../docs/003-Structural-Evolution-Computing.md)
- [`docs/004-Residual-First-In-Situ-Intelligence.md`](../docs/004-Residual-First-In-Situ-Intelligence.md)
- [`docs/005-Persistent-Structural-Discovery.md`](../docs/005-Persistent-Structural-Discovery.md)
- [`docs/006-Intelligence-Spillover-and-Relay.md`](../docs/006-Intelligence-Spillover-and-Relay.md)

**Specifications**

- [`SPEC-001-Object-Residual-Delta-Interfaces.md`](../specifications/SPEC-001-Object-Residual-Delta-Interfaces.md)
- [`SPEC-002-Persistent-Discovery-Loop.md`](../specifications/SPEC-002-Persistent-Discovery-Loop.md)
- [`SPEC-003-Validation-and-Relay-Contracts.md`](../specifications/SPEC-003-Validation-and-Relay-Contracts.md)

**Research and experimental verification**

- [`TESTABLE-HYPOTHESES.md`](TESTABLE-HYPOTHESES.md)
- [`VALIDATION-ROADMAP.md`](VALIDATION-ROADMAP.md)
- [`OPEN-QUESTIONS.md`](OPEN-QUESTIONS.md)
- [`RESEARCH-DIVERGENCES.md`](RESEARCH-DIVERGENCES.md)
- [`EXP-001-SQL-Discovery-Lab.md`](../experiments/EXP-001-SQL-Discovery-Lab.md)
- [`EXP-002-Dynamic-Scheduling-Lab.md`](../experiments/EXP-002-Dynamic-Scheduling-Lab.md)
- [`EXP-003-Stock-Pattern-Lab.md`](../experiments/EXP-003-Stock-Pattern-Lab.md)

**Research foundations**

- [ASSI](https://github.com/sizhet/Adversarial-Structural-Security-Intelligence)
- [D-BTP](https://github.com/sizhet/Dynamic-Bucket-Tree-of-Permutation-and-Directional-Structural-Evolution)
- [CDE](https://github.com/sizhet/Constrained-Delta-Evolution)
- [WE-SIO](https://github.com/sizhet/World-Entity-and-Structural-Intelligence-Operations)
- [OCSRE](https://github.com/sizhet/Object-Centric-Structural-Reasoning-and-Evolution)

## 13. Closing principle

> A structural claim is not a capability; a specification is not an experiment; an experiment is not a universal proof; and relay is not validation. Preserve the distinction, the evidence, and the unresolved residuals.

This registry is intentionally open to correction. Its value lies in making structural-intelligence research **traceable, falsifiable, comparable, and reusable without overstating maturity**.
