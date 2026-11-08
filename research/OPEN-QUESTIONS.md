# Open Questions

**Project:** Beyond Static Computation: Object-Centric Structural Evolution and Persistent Intelligence  
**Document:** `OPEN-QUESTIONS.md`  
**Status:** Open research agenda — hypotheses and architectural proposals, not established results  
**Version:** 0.1.0  
**Date:** 2026-11-08

## 1. Purpose and Scope

This document preserves unresolved questions arising from the synthesis of five research programs:

1. [ASSI — Adversarial Structural Security Intelligence](https://github.com/sizhet/Adversarial-Structural-Security-Intelligence)
2. [D-BTP — Dynamic Bucket Tree of Permutation](https://github.com/sizhet/Dynamic-Bucket-Tree-of-Permutation-and-Directional-Structural-Evolution)
3. [CDE — Constrained Delta Evolution](https://github.com/sizhet/Constrained-Delta-Evolution)
4. [WE-SIO — World Entity and Structural Intelligence Operations](https://github.com/sizhet/World-Entity-and-Structural-Intelligence-Operations)
5. [OCSRE — Object-Centric Structural Reasoning and Evolution](https://github.com/sizhet/Object-Centric-Structural-Reasoning-and-Evolution)

The objective is **relayability**: future researchers should be able to identify a precise unknown, understand its dependencies, devise discriminating tests, and preserve negative findings. Questions are deliberately not disguised as claims of proven novelty. Existing work in databases, incremental computation, streaming, online learning, control, program synthesis, and evolutionary optimization provides necessary baselines.

### Question record convention

Each question has an ID, a research question, a suggested way to discriminate competing answers, and a relevant dependency. The test sketches are invitations to build protocols, not reports of completed experiments. Priority tags are **P0** (needed for a minimal integrated demonstrator), **P1** (needed for defensible generalization), and **P2** (longer-horizon exploration).

## 2. WE-SIO: Object-Native Expression and Engineering Spillover

### OQ-001 — What is the minimal sufficient WE-SIO Core Frame? [P0]
Can identity, versioned state, relations, provenance, capabilities, constraints, and residual references be represented without making the core monolithic? **Discriminator:** compare a minimal core plus plugins against enriched-core variants on interoperability, upgrade complexity, latency, and schema churn. **Dependency:** SPEC-001.

### OQ-002 — What makes an object *intelligence-native* rather than merely data-rich? [P1]
Is persistent identity plus executable contracts sufficient, or are feedback and learning semantics necessary? **Discriminator:** define operational conformance levels and compare observable capabilities, not labels. **Dependency:** article 002.

### OQ-003 — How far can SQL primitive-column alignment extend? [P0]
Which table/row/column structures map losslessly, and where do joins, aggregates, units, temporal validity, nulls, and transactions require richer semantics? **Discriminator:** round-trip benchmark with schema evolution and temporal queries. **Dependency:** SPEC-001.

### OQ-004 — How should CDC events become object-state changes? [P0]
How are duplicate, late, reordered, and missing events handled while retaining causality and auditability? **Discriminator:** replay event streams with fault injection and compare reconstructed states to database snapshots. **Dependency:** SPEC-001 and SPEC-002.

### OQ-005 — How can plugins preserve portability without flattening semantics? [P1]
What is the smallest shared contract for capability discovery, inputs, outputs, authority, resource budgets, and failure reporting? **Discriminator:** implement the same capability in SQL, Python, and remote-service adapters. **Dependency:** SPEC-003.

## 3. From Localization to Structural Evolution Computing

### OQ-006 — What is genuinely unified by CDE? [P0]
Does a common State–Delta–Constraint–History interface enable reusable search and adaptation across distinct domains, or only rename existing algorithms? **Discriminator:** compare cross-domain implementation effort and performance with dynamic programming, constraint programming, incremental optimization, and evolutionary search. **Dependency:** article 003.

### OQ-007 — What are the precise semantics of a Delta? [P0]
When can deltas be composed, reversed, commuted, replayed, or forbidden from reuse along a path? **Discriminator:** property-based tests for preconditions, conflict detection, rollback, and history constraints. **Dependency:** SPEC-001.

### OQ-008 — How are termination and loop-back controlled? [P0]
Can bounded search and convergence be guaranteed for particular state classes without excluding productive revisitation? **Discriminator:** formal invariants and adversarial cycle tests. **Dependency:** CDE.

### OQ-009 — When should the generator itself evolve? [P1]
What evidence justifies changing the candidate generator rather than simply searching longer? **Discriminator:** hold compute budget constant and compare fixed versus adaptive generators on nonstationary problems. **Dependency:** OCSRE.

### OQ-010 — What must remain invariant when evaluators evolve? [P0]
How can a system improve its metrics without rewarding itself for lowering standards? **Discriminator:** independent holdout evaluators, immutable external objectives, and evaluator-drift audits. **Dependency:** SPEC-003.

### OQ-011 — Where is the boundary between simulation and structural evolution? [P1]
Which systems require explicit simulation, and which benefit from event-driven state updates, local deltas, or hybrid methods? **Discriminator:** compare predictive fidelity, cost, and adaptation speed. **Dependency:** article 003.

## 4. Residual-First and In-Situ Intelligence

### OQ-012 — What counts as a first-class Residual? [P0]
How should prediction errors, unmet constraints, explanatory gaps, capability deficits, and evaluator conflicts share an interface without pretending to share a single metric? **Discriminator:** typed residual schemas and cross-domain conformance cases. **Dependency:** SPEC-001.

### OQ-013 — Which computational-boundary losses matter? [P0]
When do discarded failures, intermediate states, or conflicting explanations contain actionable information? **Discriminator:** instrument conventional pipelines and compare discovery quality with and without retained residual histories. **Dependency:** article 004.

### OQ-014 — How can useful residuals be separated from noise? [P0]
What scoring policy combines reliability, novelty, expected information gain, expected utility, and investigation cost? **Discriminator:** precision–recall and net-value curves under fixed budgets. **Dependency:** SPEC-002.

### OQ-015 — What exactly does *in situ* mean? [P1]
Must compute execute physically near data, or is continuity of object identity, state, and evidence sufficient? **Discriminator:** compare local execution, remote execution with preserved context, and detached batch processing. **Dependency:** RESEARCH-DIVERGENCES.md.

### OQ-016 — Is persistent presence better than selective observation? [P1]
Can broad logical coverage coexist with adaptive allocation of finite compute and storage? **Discriminator:** measure missed opportunities, detection delay, and cost under always-on, sampled, and priority-driven policies. **Dependency:** article 004.

### OQ-017 — Can residuals recursively generate useful research objects? [P2]
When does a residual-of-a-residual yield new explanatory structure rather than unbounded metadata proliferation? **Discriminator:** bounded recursion experiments with novelty and utility thresholds. **Dependency:** WE-SIO and OCSRE.

## 5. Persistent Structural Discovery and Emergence Fishing

### OQ-018 — What constitutes a new CCC or Two-Way CCC? [P0]
What evidence establishes a novel conditional relationship, and how are directionality, confounding, leakage, and multiple testing controlled? **Discriminator:** pre-registered candidate criteria, independent data, null models, and false-discovery-rate controls. **Dependency:** SPEC-002.

### OQ-019 — When should a pattern become a trigger? [P0]
Which validation, stability, authority, and rollback requirements must precede deployment? **Discriminator:** shadow-mode evaluation followed by constrained deployment with audit logs. **Dependency:** SPEC-003.

### OQ-020 — Is Opportunity a useful first-class object? [P1]
Does explicitly tracking opportunity identity, evidence, cost, expected benefit, expiry, and outcome improve scheduling and learning? **Discriminator:** compare an Opportunity Registry against ad hoc alert queues. **Dependency:** article 005.

### OQ-021 — How is genuine discovery distinguished from rediscovery? [P1]
What novelty criterion accounts for equivalent rules, transformed representations, and prior known methods? **Discriminator:** deduplicate against a curated rule library and evaluate semantic equivalence. **Dependency:** Structural Claims Registry.

### OQ-022 — What evidence warrants the term *emergent intelligence*? [P1]
Is better detection sufficient, or must the system demonstrate new reusable abilities or improvement in its own discovery process? **Discriminator:** blinded, longitudinal tests of transfer and discovery efficiency. **Dependency:** article 005.

### OQ-023 — How should exploration and exploitation be balanced? [P0]
How much budget belongs to novel low-confidence structures versus established high-return capabilities? **Discriminator:** compare fixed allocations, bandit policies, and control-plane scoring under the same budget. **Dependency:** UCPSF/SIF and SPEC-002.

### OQ-024 — Can an intelligence-discovery system avoid self-confirmation? [P0]
How are feedback loops between data collection, hypothesis generation, evaluation, and action detected? **Discriminator:** delayed holdouts, blinded replication, counterfactual tests, and provenance audits. **Dependency:** SPEC-003.

## 6. Security, Governance, and Relay

### OQ-025 — What authority can a discovered capability inherit? [P0]
How are data access, plugin execution, and external action permissions separated from scientific validation? **Discriminator:** deny-by-default authorization tests and adversarial plugin cases. **Dependency:** ASSI and SPEC-003.

### OQ-026 — What makes a Capability Relay Package genuinely portable? [P1]
Are syntax-compatible contracts enough, or is receiver-side semantic alignment and local replication mandatory? **Discriminator:** transfer packages between SQL, scheduling, and time-series environments. **Dependency:** article 006.

### OQ-027 — How should failed or unfinished work be relayed? [P1]
What minimum negative evidence, unresolved residuals, rejected deltas, and known limitations should accompany a transfer? **Discriminator:** compare receiver progress with and without structured failure records. **Dependency:** SPEC-003.

### OQ-028 — How can adversarial evidence contaminate structural learning? [P0]
Can manipulated observations, identity ambiguity, poisoned plugins, or strategic feedback produce false residuals and spurious opportunities? **Discriminator:** red-team injection, provenance checks, and recovery measurements. **Dependency:** ASSI.

### OQ-029 — How are credit, versioning, and conflicting claims maintained across Relay? [P2]
How should competing results coexist without collapsing provenance or overstating consensus? **Discriminator:** multi-party versioning and claim-conflict exercises. **Dependency:** RESEARCH-DIVERGENCES.md and SPEC-003.

## 7. Comparative Evaluation and Experimental Priority

### OQ-030 — Which testbed best discriminates architectural value? [P0]
Should the first integrated demonstration use SQL/CDC, dynamic school-bus scheduling, or stock time series? **Provisional sequence:** SQL/CDC for alignment and discovery, scheduling for constrained evolution, and stock data for difficult nonstationary validation. **Discriminator:** feasibility, ground truth, reproducibility, and measurable net benefit. **Dependency:** experiments EXP-001–003.

### OQ-031 — What are the fair baselines? [P0]
How should the full architecture be compared with rule engines, stream processors, incremental computation, online learning, AutoML, and domain-specific optimizers? **Discriminator:** matched data, compute, latency, and engineering effort, plus component ablations. **Dependency:** VALIDATION-ROADMAP.md.

### OQ-032 — Which metrics demonstrate structural spillover? [P1]
Is success measured by discovery precision, time-to-validation, transferable capability count, adaptation cost, or net operational value? **Discriminator:** publish a multidimensional scorecard and avoid collapsing all outcomes into one scalar. **Dependency:** article 006.

### OQ-033 — How much overhead is acceptable? [P0]
When do object provenance, residual persistence, and discovery loops cost more than their benefits? **Discriminator:** throughput, storage, memory, and energy profiling against minimal baselines. **Dependency:** WE-SIO and SPEC-001.

### OQ-034 — What does longitudinal improvement look like? [P1]
Can a system become better at discovering and validating useful structures without simply accumulating more rules or spending more compute? **Discriminator:** frozen-budget evaluations across time with independent test tasks. **Dependency:** SEFL and article 005.

## 8. Cross-Cutting Research Tensions

The following tensions should remain explicitly open rather than be resolved by terminology alone:

- **Universality versus domain-specific advantage:** a common interface may improve interoperability while losing performance or semantic precision.
- **Persistence versus resource limits:** logical coverage does not imply unlimited physical monitoring.
- **Adaptation versus stable validation:** a changing evaluator cannot be its own sole judge.
- **Discovery versus action:** a validated finding does not automatically confer authority to act.
- **Open-ended growth versus termination:** recursive candidate generation needs budgets, stopping rules, and rollback.
- **Novelty versus prior art:** similar ideas exist in established disciplines; the research contribution must be demonstrated through precise combinations and results.
- **Collective learning versus evidence contamination:** Relay must preserve provenance, dissent, failures, and local validation requirements.

See `RESEARCH-DIVERGENCES.md` for alternative positions and provisional dispositions. An open question need not imply a disagreement; a disagreement need not be resolvable by a single experiment.

## 9. Suggested First Research Milestones

**M1 — Interface conformance.** Implement a small WE-SIO adapter and typed Object/Residual/Delta records; test identity, versioning, referential integrity, and replay. Targets: OQ-001, 003, 004, 007, 012.

**M2 — Residual value.** Compare event-driven SQL discovery with and without preserved residual histories; report false discoveries and overhead. Targets: OQ-013, 014, 018, 031, 033.

**M3 — Constrained evolution.** Run matched-budget dynamic scheduling experiments with fixed and adaptive candidate generators; independently evaluate objective improvement and constraint violations. Targets: OQ-006, 008, 009, 010.

**M4 — Discovery-to-relay.** Package a validated capability, transfer it to a semantically different setting, and measure adaptation effort, local replication, and failures. Targets: OQ-022, 026, 027, 032.

**M5 — Longitudinal study.** Test whether discovery efficiency improves across unseen tasks at constant compute and with blinded evaluation. Targets: OQ-023, 024, 034.

No milestone should be marked successful without published protocol, baselines, negative results, and reproducible evidence.

## 10. How to Contribute an Answer

A proposed answer should provide:

```yaml
question_id: OQ-XXX
position: "A concise falsifiable answer"
assumptions: []
related_claim_ids: []
related_specs: []
prior_art: []
protocol_or_argument: ""
comparison_baselines: []
evidence_links: []
negative_results: []
known_limitations: []
replication_status: proposed
next_residuals: []
```

Suggested states are `open`, `under_test`, `partially_resolved`, `supported`, `refuted`, and `superseded`. A `supported` result is always scoped to stated assumptions and tests. A question can be reopened when new evidence arrives. Preserve superseded records for audit and collective learning.

## 11. Related Documents

- `docs/001-Five-DOI-Peaks.md` — synthesis and research landscape.
- `docs/002-WE-SIO-Object-Native-Intelligence.md` — object representation and engineering interfaces.
- `docs/003-Structural-Evolution-Computing.md` — state/delta evolution and localization.
- `docs/004-Residual-First-In-Situ-Intelligence.md` — residuals and persistent computation.
- `docs/005-Persistent-Structural-Discovery.md` — structural discovery and SEFL.
- `docs/006-Intelligence-Spillover-and-Relay.md` — cross-domain reuse and collective learning.
- `specifications/SPEC-001-Object-Residual-Delta-Interfaces.md` — record contracts.
- `specifications/SPEC-002-Persistent-Discovery-Loop.md` — discovery-loop contracts.
- `specifications/SPEC-003-Validation-and-Relay-Contracts.md` — evidence and transfer contracts.
- `research/RESEARCH-DIVERGENCES.md` — competing interpretations.
- `research/TESTABLE-HYPOTHESES.md` — formal hypotheses and measurable criteria.
- `research/VALIDATION-ROADMAP.md` — execution plan and benchmarks.

## 12. Closing Perspective

The central open question is not whether object models, dynamic algorithms, residual analysis, or online learning exist—they do. It is whether their **specification-first integration** can produce measurable, reproducible, transferable improvements in the discovery and evolution of useful capabilities. This document is intended to keep that question, and its many component questions, available for critical examination and future Relay.
