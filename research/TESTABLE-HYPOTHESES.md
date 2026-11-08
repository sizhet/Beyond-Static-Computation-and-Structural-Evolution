# Testable Hypotheses: Object-Native Structural Evolution and Persistent Intelligence

**Status:** Research hypotheses; not validated findings  
**Version:** 0.1.0  
**Date:** 2026-11-08  
**Scope:** Cross-cutting research program connecting ASSI, D-BTP, CDE, WE-SIO, and OCSRE

## Abstract

This document turns architectural claims about object-native intelligence, structural evolution computing, residual-first in-situ learning, persistent discovery, and capability relay into falsifiable experiments. The goal is not to assume that a unified structural-intelligence stack outperforms established methods. It is to identify where, under which constraints, and at what cost the proposed components add measurable value. All hypotheses require preregistered baselines, explicit budgets, versioned datasets, and publication of negative results.

## 1. Epistemic and Experimental Rules

- **Hypothesis is not evidence.** No claim below is considered established merely because it is architecturally plausible.
- **Equal-budget comparisons.** Match compute, memory, engineering effort where practical, observation windows, and access to data.
- **Temporal integrity.** For streaming and financial experiments, enforce event-time availability and prevent look-ahead leakage.
- **Predeclared metrics.** Specify primary metrics, minimum meaningful effect sizes, and stopping rules before evaluation.
- **Ablations.** Remove one structural component at a time to test attribution.
- **Adverse cases.** Include drift, missing data, schema changes, adversarial inputs, and resource pressure.
- **Relay the leftovers.** Preserve rejected hypotheses, residuals, failed experiments, and unresolved semantic mappings.

A result counts as supportive only when it passes a preregistered acceptance criterion and survives a held-out replication. A null result is not automatically a refutation outside the tested conditions.

## 2. Experimental Infrastructure

### 2.1 Shared record types

Each experiment should log `ObjectRecord`, `ResidualRecord`, `DeltaRecord`, `ObservationEvent`, `DiscoveryCandidate`, `ValidationRecord`, and `RelayPackage` identifiers, with immutable timestamps, provenance, versioned schemas, and permission scope. These records are proposed interfaces, not claims of an existing implementation.

### 2.2 Baseline families

- **B0 — Conventional pipeline:** SQL or domain-specific code with fixed rules and batch processing.
- **B1 — Incremental pipeline:** change-data capture, streaming analytics, online anomaly detection, or dynamic optimization.
- **B2 — Adaptive pipeline:** online learning, AutoML, reinforcement learning, or established evolutionary search as appropriate.
- **B3 — Object-centric without evolution:** persistent object representation and plugin invocation, but no CDE/OCSRE discovery loop.
- **S — Proposed structural stack:** WE-SIO + residual records + constrained delta generation + validated discovery + relay, with scoped components per test.

Do not force all baselines into every experiment; choose the strongest relevant alternatives and document omissions.

### 2.3 Shared evaluation axes

Measure predictive or optimization utility; discovery precision; reproducibility; time-to-detection; semantic correctness; runtime cost; state consistency; transfer performance; human review burden; and safety violations. Report confidence intervals, seeds, failed runs, and sensitivity to resource budgets.

## 3. Hypotheses: Object-Native Representation and Engineering Spillover

### TH-001 — Persistent object context reduces reconstruction overhead

**Claim.** For repeated queries and decisions over changing relational entities, a WE-SIO representation reduces repeated context reconstruction relative to a stateless pipeline without decreasing semantic correctness.

**Test.** Run identical multi-step workflows on a versioned SQL dataset with joins, entity histories, and schema changes. Compare B0/B1 to B3/S.  
**Primary metrics.** Median end-to-end latency and number of repeated data/semantic joins per workflow.  
**Guardrail.** Correctness of entity identity, temporal joins, and results must remain non-inferior.  
**Falsifier.** No overhead reduction at matched correctness and resources, or higher consistency error rates.

### TH-002 — Core Frame + Plugins improves extensibility

**Claim.** A small stable object core plus contract-bound plugins reduces the cost of adding heterogeneous analytical capabilities compared with tightly coupled alternatives.

**Test.** Independently implement and integrate SQL, graph, time-series, and optimization capabilities using both designs.  
**Primary metrics.** Engineer-hours to integrate, regression failures, and interface changes required.  
**Guardrail.** Equivalent functionality, security review, and performance envelope.  
**Falsifier.** Plugin approach adds complexity without measurable integration or maintenance benefit.

### TH-003 — Three-level SQL alignment improves semantic reliability

**Claim.** Structural, semantic, and operational alignment together reduce incorrect object interpretations versus column-name/type mapping alone.

**Test.** Benchmark entity resolution and computations involving units, time zones, slowly changing dimensions, missing values, transactions, and derived columns.  
**Primary metrics.** Semantic mapping error rate and correctness under updates.  
**Falsifier.** Rich alignment produces no reproducible correctness benefit after accounting for annotation cost.

## 4. Hypotheses: Structural Evolution Computing

### TH-004 — Constrained delta search improves adaptive optimization

**Claim.** In selected changing constraint systems, CDE's typed deltas, path memory, and adaptive branching improve solution quality per unit compute over relevant dynamic search baselines.

**Test.** Use dynamic school-bus routing/scheduling instances with changing demand, vehicle availability, and hard service constraints. Compare against established local search, mixed-integer optimization with warm starts, and evolutionary methods.  
**Primary metrics.** Feasible objective value at fixed wall-clock/compute budget.  
**Guardrail.** Zero unapproved hard-constraint violations.  
**Falsifier.** No advantage across preregistered instance families or improvements disappear when budgets are matched.

### TH-005 — Explicit delta provenance improves auditability

**Claim.** Versioned delta and constraint records make structural search results easier to reproduce and explain than opaque state replacement.

**Test.** Ask independent reviewers to reconstruct why accepted states were reached and identify the first invalid transition in seeded failure cases.  
**Primary metrics.** Reconstruction success, diagnostic time, and audit completeness.  
**Falsifier.** No improvement or excessive logging overhead relative to trace-enabled baselines.

### TH-006 — Controlled generator evolution outperforms fixed generators

**Claim.** Under drift, governed evolution of candidate generators improves long-run performance relative to fixed generators with comparable tuning resources.

**Test.** Compare fixed, periodically retrained, and evolving generators on held-out sequential problem episodes. Freeze an external evaluator.  
**Primary metrics.** Cumulative regret or normalized optimization utility on future episodes.  
**Guardrail.** No unauthorized evaluator or constraint changes.  
**Falsifier.** Apparent gains vanish on future episodes or come from changing evaluation standards.

## 5. Hypotheses: Residual-First and In-Situ Intelligence

### TH-007 — Structured residual retention improves subsequent learning

**Claim.** Retaining typed residuals with context and provenance improves later diagnosis or adaptation compared with retaining scalar errors or discarding failures.

**Test.** Replay recurrent failures, changed constraints, and explanatory gaps with equivalent storage budgets.  
**Primary metrics.** Time or samples needed to resolve recurring issues; held-out diagnosis accuracy.  
**Falsifier.** Structured residual records add storage and processing without meaningful improvement.

### TH-008 — Residual localization improves discovery efficiency

**Claim.** Prioritizing objects and relations by calibrated residual-based opportunity scores increases validated discoveries per unit compute compared with uniform scanning and anomaly-only ranking.

**Test.** Use a streaming SQL/graph benchmark with planted and naturally occurring structural changes.  
**Primary metrics.** Independently validated discoveries per compute-hour.  
**Guardrail.** Coverage of rare but consequential events.  
**Falsifier.** Ranking yields no advantage or systematically misses high-impact low-frequency discoveries.

### TH-009 — Persistent context reduces adaptation latency

**Claim.** In-situ object histories and state-local capabilities reduce time from a meaningful change to a correct adaptive response versus reconstruct-on-trigger approaches.

**Test.** Inject timed changes into dynamic scheduling and data-integrity tasks.  
**Primary metrics.** Event-to-validated-response latency.  
**Guardrail.** False-trigger rate and memory/compute cost.  
**Falsifier.** Latency gains disappear after accounting for resident-resource costs or correctness degrades.

### TH-010 — Selective presence can approximate broad coverage at lower cost

**Claim.** A governed selective in-situ strategy can preserve most of the discovery utility of dense monitoring at substantially lower cost.

**Test.** Compare full monitoring, fixed sampling, random exploration, and adaptive localization under identical streams.  
**Primary metrics.** Utility-versus-cost frontier; missed critical events.  
**Falsifier.** Selective monitoring loses essential coverage or is dominated by simple fixed schedules.

## 6. Hypotheses: Persistent Structural Discovery

### TH-011 — Two-way CCC validation reduces spurious patterns

**Claim.** Bidirectional conditional-evidence checks reduce false discoveries relative to one-direction pattern triggering, given matched discovery power and multiplicity control.

**Test.** Use synthetic ground-truth causal/conditional graphs plus realistic observational data. Distinguish bidirectional association from causality.  
**Primary metrics.** False discovery rate at matched recall; calibration.  
**Falsifier.** Two-way checks add no precision or systematically suppress valid asymmetric relationships.

### TH-012 — Discovery loops yield reusable capabilities, not merely more patterns

**Claim.** A validated discovery loop yields a higher rate of independently reusable triggers, rules, or plugins than conventional anomaly/pattern mining.

**Test.** Blindly evaluate candidate outputs on fresh tasks and objects not used in discovery.  
**Primary metrics.** Accepted transferable capabilities per 1,000 candidates and per compute-hour.  
**Falsifier.** Candidate volume grows but transfer-qualified capability yield does not.

### TH-013 — Learning the discovery policy improves future discovery

**Claim.** Updating the discovery policy from validated and rejected findings improves future held-out discovery efficiency over a frozen policy.

**Test.** Sequential train/validation/test periods; compare frozen, retrained, and structurally evolving discovery policies. Keep the final test set untouched until evaluation.  
**Primary metrics.** Future validated discoveries per compute-hour, adjusted for false discoveries.  
**Falsifier.** Gains appear only in reused evaluation data or are explained by larger search budgets.

### TH-014 — Opportunity records improve resource allocation

**Claim.** Explicit opportunity objects linking expected utility, evidence, uncertainty, and cost improve allocation over severity-only or recency-only queues.

**Test.** Simulate competing residuals and live-like streams under hard compute and review budgets.  
**Primary metrics.** Realized utility, regret, and calibration of predicted value.  
**Falsifier.** Added opportunity metadata fails to improve decisions or causes unstable allocation.

## 7. Hypotheses: Validation, Security, and Relay

### TH-015 — Evidence-bound relay improves cross-domain reuse

**Claim.** Capability packages carrying contracts, evidence, provenance, limitations, and test cases transfer more reliably than code-only or prose-only handoffs.

**Test.** Independent teams adapt the same capabilities across SQL, scheduling, and graph-analysis tasks.  
**Primary metrics.** Successful conformance rate, integration time, and semantic failures.  
**Falsifier.** Packages do not improve reuse after accounting for preparation effort.

### TH-016 — Relay of failed attempts reduces repeated dead ends

**Claim.** Sharing rejected hypotheses and residual evidence reduces duplicate failed experiments without suppressing useful exploration.

**Test.** Randomize teams to access positive results only versus positive and negative evidence.  
**Primary metrics.** Repeated failed trials, novel valid discoveries, and total research cost.  
**Falsifier.** No reduction in duplication, or negative-result exposure discourages productive exploration.

### TH-017 — Security contracts contain adversarial contamination

**Claim.** Provenance checks, plugin isolation, authorization, and independent validation reduce successful malicious or erroneous relay acceptance compared with ungoverned exchange.

**Test.** Red-team fabricated evidence, poisoned candidate rules, compromised plugins, and authority spoofing in a controlled sandbox.  
**Primary metrics.** Unauthorized acceptance rate, time-to-detection, and legitimate throughput.  
**Falsifier.** Controls fail to reduce accepted attacks or impose disproportionate operational cost.

### TH-018 — The integrated stack has positive net value

**Claim.** On at least one preregistered task family, the complete stack achieves higher validated utility per total cost than the strongest applicable baseline, with acceptable reliability.

**Test.** End-to-end benchmark on streaming SQL and dynamic scheduling, with component ablations and independent replication.  
**Primary metrics.** Net validated utility per total compute, storage, engineering, and human-review cost.  
**Falsifier.** Benefits vanish under full cost accounting or are not attributable to proposed components.

## 8. Priority Experiments

| Phase | Experiment | Principal hypotheses | Deliverable |
|---|---|---|---|
| E1 | SQL / CDC semantic alignment and residual registry | TH-001, 003, 007, 008 | Reproducible dataset, mappings, traces, baseline comparison |
| E2 | Dynamic school-bus scheduling and CDE ablations | TH-004, 005, 006, 009 | Feasibility-constrained benchmark and solver traces |
| E3 | CCC / Two-Way CCC and persistent discovery | TH-011, 012, 013, 014 | Discovery registry with held-out validation |
| E4 | Cross-domain capability relay and adversarial review | TH-015, 016, 017 | Versioned relay packages and conformance report |
| E5 | End-to-end integrated evaluation | TH-010, 018 and earlier | Cost-normalized independent replication |

A stock-data study may follow E3 as a stress test, but it requires walk-forward evaluation, realistic transaction costs, market impact assumptions, and strict separation of research from live trading. Historical profitability alone is insufficient evidence of generalizable discovery.

## 9. Preregistration Template

```yaml
hypothesis_id: TH-XXX
status: proposed
research_question: ""
primary_outcome: ""
minimum_meaningful_effect: null
baselines: []
dataset_version: ""
time_split_policy: ""
resource_budget:
  compute: ""
  memory: ""
  engineering_hours: ""
  human_review: ""
random_seeds: []
acceptance_rule: ""
falsification_rule: ""
robustness_checks: []
security_constraints: []
replication_owner: ""
evidence_artifacts: []
negative_results: []
```

## 10. Interpreting Results

A positive result supports only the specified hypothesis, task distribution, budget, and evaluation regime. It does not establish general intelligence, consciousness, autonomous scientific discovery, or universal superiority. A negative result should distinguish conceptual failure, implementation limitations, insufficient statistical power, and inappropriate benchmark selection. Claims of **emergence** require evidence of new, transferable capability beyond recombination or memorization, using a predeclared operational definition.

## 11. Connections to the Repository

- `docs/001-Five-DOI-Peaks.md` — the cross-repository research perspective.
- `docs/002-WE-SIO-Object-Native-Intelligence.md` — object-native representation and plugins.
- `docs/003-Structural-Evolution-Computing.md` — constrained delta and adaptive computation.
- `docs/004-Residual-First-In-Situ-Intelligence.md` — persistent residuals and in-situ learning.
- `docs/005-Persistent-Structural-Discovery.md` — opportunity localization and discovery loops.
- `docs/006-Intelligence-Spillover-and-Relay.md` — reusable capabilities and collective learning.
- `specifications/SPEC-001-Object-Residual-Delta-Interfaces.md` — record interfaces.
- `specifications/SPEC-002-Persistent-Discovery-Loop.md` — discovery lifecycle.
- `specifications/SPEC-003-Validation-and-Relay-Contracts.md` — evidence and relay contracts.
- `research/RESEARCH-DIVERGENCES.md` — unresolved competing positions.
- `research/OPEN-QUESTIONS.md` — broader unanswered questions.
- `research/VALIDATION-ROADMAP.md` — future experimental execution plan.

## 12. Foundational DOI Repositories

1. **ASSI — Adversarial Structural Security Intelligence**  
   https://github.com/sizhet/Adversarial-Structural-Security-Intelligence
2. **D-BTP — Dynamic Bucket Tree of Permutation**  
   https://github.com/sizhet/Dynamic-Bucket-Tree-of-Permutation-and-Directional-Structural-Evolution
3. **CDE — Constrained Delta Evolution**  
   https://github.com/sizhet/Constrained-Delta-Evolution
4. **WE-SIO — World Entity and Structural Intelligence Operations**  
   https://github.com/sizhet/World-Entity-and-Structural-Intelligence-Operations
5. **OCSRE — Object-Centric Structural Reasoning and Evolution**  
   https://github.com/sizhet/Object-Centric-Structural-Reasoning-and-Evolution

## 13. Closing Principle

The objective is not to accumulate confirmations of a preferred architecture. It is to produce an auditable sequence of hypotheses, discriminating tests, and transferable evidence. A structural-intelligence research program advances when it can identify both **where its structures create real advantage** and **where established approaches remain superior**. Both outcomes should be relayed.
