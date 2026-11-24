# Future Directions: Beyond Static Computation and Structural Evolution

**Repository:** Beyond Static Computation and Structural Evolution  
**Document status:** Research agenda; proposals and hypotheses, not validated findings  
**Version:** 1.0.0  
**Date:** 2026-11-08

## 1. Purpose and Scope

This document identifies research directions emerging from the convergence of five research programs: **Adversarial Structural Security Intelligence (ASSI)**, **Dynamic Bucket Tree of Permutation (D-BTP)**, **Constrained Delta Evolution (CDE)**, **World Entity and Structural Intelligence Operations (WE-SIO)**, and **Object-Centric Structural Reasoning and Evolution (OCSRE)**.

The shared ambition is not to replace databases, optimization, statistical learning, control theory, or existing AI architectures. It is to investigate whether persistent object context, explicit residuals, constrained state evolution, continuous discovery, and evidence-governed capability relay can form a useful *additional computational organization*. Every proposed advantage requires a falsifiable comparison against credible existing methods.

The agenda distinguishes **conceptual extension**, **specification**, **prototype**, **controlled validation**, and **independent replication**. Movement between these stages is contingent on evidence, not publication or architectural elegance.

## 2. Direction FD-001 — Object-Native Computing as an Interoperable Substrate

**Question.** Can a compact WE-SIO Core Frame preserve object identity, state, relations, history, residuals, and capabilities across heterogeneous data and computational systems without creating an unmanageable universal object model?

**Research tasks.** Define versioned object identifiers, temporal semantics, relation types, provenance, and plugin contracts. Study bidirectional alignment with SQL tables, rows, columns, and change-data-capture (CDC) streams at the structural, semantic, and operational levels. Add adapters for event logs, graph stores, document systems, and simulations. Investigate when an object should remain a lightweight reference rather than an eagerly materialized record.

**Critical tests.** Measure semantic fidelity, reconstruction cost, storage overhead, update latency, schema evolution, and interoperability against normalized relational designs, event sourcing, and knowledge-graph baselines. Include adversarial schema changes and conflicting identity assignments.

**Open risk.** A universal representation may move complexity rather than remove it. Plugins can fragment semantics unless contracts and conformance tests are explicit.

## 3. Direction FD-002 — Residuals as First-Class, Persistent Computational Objects

**Question.** When does retaining unresolved differences produce more useful subsequent discoveries than discarding them, aggregating them into metrics, or handling them through conventional error logs and issue trackers?

**Research tasks.** Specify a ResidualRecord with stable identity, origin, affected objects, measurement context, uncertainty, severity, candidate explanations, validation state, expiry rules, and action links. Develop residual clustering, prioritization, deduplication, and lineage tracking. Distinguish prediction errors, constraint violations, missing capabilities, conflicting evidence, and opportunities not yet formalized as objectives.

**Critical tests.** Compare residual-native discovery with alerting, anomaly detection, error-driven learning, active learning, and issue-management baselines under equal observation and compute budgets. Track verified downstream value per retained residual and the cost of retaining irrelevant residuals.

**Open risk.** Unbounded residual persistence can become expensive, noisy, privacy-invasive, or misleading. Retention and deletion policies are part of the theory, not implementation afterthoughts.

## 4. Direction FD-003 — A General Calculus of Constrained Deltas

**Question.** Can CDE define a reusable delta algebra that supports composition, reversibility, path-dependent restrictions, and constraint-preserving transitions across substantially different domains?

**Research tasks.** Formalize state containers, typed deltas, preconditions, postconditions, invariants, conflict detection, partial composition, rollback, and path memory. Distinguish delta equivalence from path equivalence. Define termination and loop-back controls, including cases where revisiting a state is permissible but repeating a path action is not. Explore adaptive M-to-N branching and multi-scale deltas.

**Critical tests.** Compare against dynamic programming, constraint programming, branch-and-bound, incremental repair, large-neighborhood search, and online optimization on matched tasks. Separate gains from representation, search heuristics, memory, and evolving generators through ablation.

**Open risk.** No single delta semantics may cover all applications. A family of compatible calculi with explicit domain contracts may be preferable to a universal calculus.

## 5. Direction FD-004 — Evolution of Candidate Generators, Not Only Candidate Solutions

**Question.** Can a system improve the mechanisms that produce future hypotheses, repairs, and structural transformations rather than merely select among fixed candidates?

**Research tasks.** Represent candidate generators as versioned, testable capabilities. Allow constrained modifications to their operators, branching policies, retrieval strategies, and evaluation priorities. Track the provenance of each generator update and maintain rollback paths. Study multi-agent proposals and competitive relay under fixed compute budgets.

**Critical tests.** Compare fixed heuristics, tuned heuristics, adaptive search, and generator-evolution systems using held-out environments. Report improvements in solution quality, adaptation time, compute efficiency, and generalization. Require evidence that gains survive changes in workload and random seed.

**Open risk.** Generator evolution can overfit the evaluation process or create an unbounded meta-search problem. Governance and complexity budgets are essential.

## 6. Direction FD-005 — Persistent Structural Presence Under Finite Resources

**Question.** Can selective, adaptive observation approximate the value of broad monitoring while consuming substantially fewer resources?

**Research tasks.** Develop observation policies that allocate attention to objects, residuals, relation changes, and opportunities. Specify when a system samples, sleeps, resumes, escalates, or relinquishes monitoring. Model uncertainty about unobserved regions and the cost of missed events. Integrate temporal memory and changing priorities.

**Critical tests.** Compare periodic polling, fixed alerts, event-driven systems, adaptive sampling, and residual-guided monitoring. Evaluate detection delay, verified discovery yield, false discovery rate, resource cost, and missed-event regret.

**Open risk.** Selective presence can create blind spots and self-reinforcing attention biases. Randomized audits and coverage floors should be tested.

## 7. Direction FD-006 — CCC, Two-Way CCC, and Discovery Governance

**Question.** Can conditional-concept comparison and bidirectional evidence checks improve the quality of discovered structural relationships without mistaking association for causation?

**Research tasks.** Define explicit candidate-generation, comparison, contradiction, and counterevidence interfaces. Record assumptions, confounders, selection effects, and temporal direction. Use negative controls, permutation tests, interventions where feasible, and preregistered discovery criteria.

**Critical tests.** Measure the number of independently validated discoveries per unit cost, calibration, false discovery rates, and stability across domains. Compare against standard association mining, feature selection, causal discovery, and hypothesis-testing pipelines.

**Open risk.** Two-way support may reflect common causes, leakage, or circular construction. Bidirectional consistency is evidence, not proof of causality.

## 8. Direction FD-007 — A Structural Emergence Fishing Laboratory (SEFL)

**Question.** Can a common discovery protocol reveal transferable lessons across data systems, dynamic optimization, and nonstationary time series?

**Research tasks.** Operate three complementary laboratories:

- **EXP-001 — SQL Discovery Lab:** SQL/CDC alignment, semantic changes, residuals, relation discovery, and validated capability extraction.
- **EXP-002 — Dynamic Scheduling Lab:** changing student demand, route constraints, constrained delta repairs, and adaptive operator evolution.
- **EXP-003 — Stock Pattern Lab:** nonstationary market observations, pattern hypotheses, leakage-resistant evaluation, and cost-adjusted out-of-sample testing.

Use shared record schemas, preregistration templates, experiment identifiers, evidence bundles, and negative-result reporting. Preserve domain-specific metrics and do not collapse heterogeneous outcomes into an unjustified single intelligence score.

**Critical tests.** Evaluate each lab against its own strong baselines before claiming cross-domain transfer. For finance, require chronological walk-forward splits, realistic costs, multiple-testing controls, and an explicit distinction between predictive performance and investable advantage.

**Open risk.** A demonstration in one domain may not support a general theory. Cross-domain claims require independent evidence.

## 9. Direction FD-008 — From Discovery to Reusable Capability

**Question.** What additional conditions transform a discovered pattern into a capability that can be safely reused?

**Research tasks.** Introduce a staged lifecycle: observation → candidate → sandbox evaluation → validated finding → capability specification → constrained deployment → monitored reuse. Define executable interfaces, expected behavior, failure conditions, evidence provenance, and permissions. Distinguish descriptive knowledge, predictive models, decision policies, and operational actions.

**Critical tests.** Compare capability reuse rates, integration effort, regression frequency, and error propagation with ad hoc code reuse, workflow templates, and conventional model registries.

**Open risk.** Successful local experiments do not establish operational reliability or portability. Promotion gates must remain explicit.

## 10. Direction FD-009 — Evidence-Bound Collective Learning and Relay

**Question.** Can independent systems exchange not only successful capabilities but also uncertainty, failed attempts, contradictory evidence, and unresolved research questions in a way that improves collective progress?

**Research tasks.** Define a Capability Relay Package containing interface contract, provenance, environment, evidence, confidence or uncertainty calibration, constraints, safety permissions, failure lessons, and explicit leftovers. Explore interoperability with model cards, dataset cards, reproducibility packages, plugin registries, and scientific workflow systems.

**Critical tests.** Compare receiving systems with and without evidence-bound relay on integration time, repeated failure rates, validation cost, and cross-domain task performance. Measure whether negative-result relay avoids duplicated dead ends.

**Open risk.** Relay can amplify incorrect claims, security threats, and social consensus bias. Receiving systems must revalidate claims under their own conditions.

## 11. Direction FD-010 — Adversarial Structural Security and Trust Boundaries

**Question.** How should evolving identities, evidence, authority, dependencies, and capabilities be governed when parts of the environment or relay chain are adversarial?

**Research tasks.** Apply ASSI to provenance, compositional identities, permission boundaries, evidence contamination, malicious plugins, compromised agents, and poisoned relay packages. Separate *technical trust minimization* from *organizational trust elimination*. Specify revocation, quarantine, rollback, and audit procedures.

**Critical tests.** Run controlled red-team scenarios with identity spoofing, data poisoning, permission escalation attempts, and forged validation evidence. Measure containment, detection, recovery time, and false quarantine rates.

**Open risk.** More detailed object histories may increase the attack surface or expose sensitive information. Privacy-preserving provenance and least-privilege design are required.

## 12. Direction FD-011 — Structural Localization Within SIF

**Question.** Can CDE become a distinct, testable localization/addressing method within the Structural Intelligence Framework (SIF), complementing existing static addressing and scoring mechanisms?

**Research tasks.** Formalize localization over state-transition neighborhoods, candidate delta paths, residual neighborhoods, and evolving capability graphs. Compare *where an object or gap is located* with *which constrained evolution path can reach a better state*. Define interfaces to SIF's problem–capability mapping, node intelligence, scoring/control plane, and relay mechanisms.

**Critical tests.** Evaluate whether delta-based localization reduces search effort, improves repair quality, or identifies reachable opportunities that static localization misses. Include cases where dynamic localization is unnecessary or inferior.

**Open risk.** “Localization” may become too broad unless spatial, semantic, causal, and transition-path meanings are distinguished.

## 13. Direction FD-012 — Formal Methods, Contracts, and Conformance Before Runtime

**Question.** Which parts of the proposed framework can be specified and checked independently of a full implementation?

**Research tasks.** Develop machine-checkable schemas and invariants for ObjectRecord, ResidualRecord, DeltaRecord, ObservationEvent, DiscoveryCandidate, ValidationRecord, and RelayPackage. Add property-based testing, temporal invariants, trace replay, contract versioning, and compatibility matrices. Study proof obligations for safety-critical delta transitions and capability promotion.

**Critical tests.** Measure conformance coverage, defect detection, false acceptance, and cross-implementation interoperability. Include deliberately invalid traces and adversarial edge cases.

**Open risk.** Conformance to a specification is not evidence that the specification describes useful intelligence. Runtime performance and scientific validity require separate assessment.

## 14. Direction FD-013 — Efficiency, Scaling, and Boundary Conditions

**Question.** Under what workloads does persistent structural context pay for its own storage, update, validation, and coordination costs?

**Research tasks.** Build explicit cost models for memory, compute, bandwidth, energy, human review, and latency. Explore incremental recomputation, object caching, bounded residual retention, partial materialization, distributed state containers, and selective relay. Identify phase transitions where structural overhead exceeds benefit.

**Critical tests.** Use matched compute and memory budgets, scalability sweeps, stress tests, and ablations. Report absolute cost as well as relative improvement. Seek counterexamples where simpler systems win.

**Open risk.** Apparent improvements can be artifacts of unequal engineering effort, data access, or hidden manual curation.

## 15. Direction FD-014 — Evaluation of Intelligence Growth Without Circular Metrics

**Question.** How can the framework distinguish genuine improvement in discovery or adaptation capability from optimization of its own evaluation score?

**Research tasks.** Separate task outcomes, discovery yield, calibration, transfer, novelty, operational cost, and governance quality. Introduce external held-out tasks, independent validators, evaluator rotation, and precommitted acceptance thresholds. Track whether improvements persist after evaluation criteria change.

**Critical tests.** Use blinded or independent review, delayed outcome measurements, adversarial evaluation cases, and counterfactual ablations. Avoid declaring “emergence” solely because a system generates unexpected patterns.

**Open risk.** Any single score can be gamed. A portfolio of interpretable measures and documented disagreements is more defensible.

## 16. Prioritized Research Sequence

The following order prioritizes falsifiability and infrastructure reuse rather than architectural completeness.

| Horizon | Work package | Minimum evidence required | Promotion gate |
|---|---|---|---|
| P0 — Definitions | Canonical schemas, provenance, object/residual/delta semantics | Conformance tests and invalid-case fixtures | No unresolved critical contract contradictions |
| P1 — SQL substrate | EXP-001 object/CDC alignment and residual tracking | Reproducible semantic-fidelity and cost comparisons | Baselines and ablations completed |
| P2 — Dynamic evolution | EXP-002 CDE repair and generator evolution | Feasibility, objective quality, latency, and generalization | No safety-constraint regressions |
| P3 — Persistent discovery | Selective observation, CCC, Two-Way CCC, SEFL | Verified discovery yield under equal budgets | False-discovery controls satisfied |
| P4 — Transfer and security | Relay packages, ASSI controls, cross-domain tests | Independent receiving-system validation | Provenance, permission, and rollback gates passed |
| P5 — Integration | End-to-end OCSRE/WE-SIO/CDE stack | Net benefit after full cost accounting | Replication and limitations published |

These horizons are dependency stages, **not promised calendar dates**. Work may stop, branch, or reverse when evidence contradicts a hypothesis.

## 17. Research Artifacts and Reproducibility

Every major study should produce a compact evidence package:

1. **Claim ID and version:** precise statement, scope, and current epistemic status.
2. **Experiment registration:** dataset, environment, hypotheses, baselines, budget, metrics, and stopping rules.
3. **Conformance report:** schema versions, invariants, and failure cases.
4. **Execution record:** code/configuration hashes, random seeds, hardware, and dependency versions where applicable.
5. **Results and uncertainty:** primary outcomes, confidence intervals or appropriate uncertainty estimates, ablations, and sensitivity analyses.
6. **Counterevidence:** negative results, unresolved residuals, alternative explanations, and known failure modes.
7. **Relay decision:** reject, retain as exploratory, request replication, or promote with explicit applicability limits.

The **STRUCTURAL-CLAIMS-REGISTRY**, **RESEARCH-DIVERGENCES**, **OPEN-QUESTIONS**, **TESTABLE-HYPOTHESES**, and **VALIDATION-ROADMAP** documents should remain synchronized. A rejected hypothesis should remain discoverable as a research artifact, not silently disappear.

## 18. Cross-Document Traceability

| Direction | Primary paper | Specification / research asset | Initial validation venue |
|---|---|---|---|
| FD-001 | `docs/002-WE-SIO-Object-Native-Intelligence.md` | `specifications/SPEC-001-Object-Residual-Delta-Interfaces.md` | EXP-001 |
| FD-002 | `docs/004-Residual-First-In-Situ-Intelligence.md` | SPEC-001; `research/TESTABLE-HYPOTHESES.md` | EXP-001, EXP-002 |
| FD-003–004 | `docs/003-Structural-Evolution-Computing.md` | SPEC-001; validation roadmap | EXP-002 |
| FD-005–007 | `docs/005-Persistent-Structural-Discovery.md` | `specifications/SPEC-002-Persistent-Discovery-Loop.md` | EXP-001, EXP-003 |
| FD-008–010 | `docs/006-Intelligence-Spillover-and-Relay.md` | `specifications/SPEC-003-Validation-and-Relay-Contracts.md` | Cross-lab relay and security tests |
| FD-011–015 | `docs/001-Five-DOI-Peaks.md` and cross-cutting papers | Claims registry; divergences; roadmap | Cross-lab and independent replication |

The mappings identify proposed test venues, not completed evidence. Refer to `research/TESTABLE-HYPOTHESES.md` for TH-001–TH-018 and `research/VALIDATION-ROADMAP.md` for formal gates.

## 19. Open Strategic Choices

Several decisions should remain open until evidence is available:

- **Universal frame versus federation:** one shared object schema, or a minimal interoperable kernel with domain-specific extensions?
- **Residual retention versus bounded forgetting:** which unresolved differences deserve persistent identity, and when should they expire?
- **Generic delta calculus versus domain-specific operators:** what is genuinely reusable?
- **Autonomous discovery versus supervised promotion:** where should independent human or external review be mandatory?
- **Centralized governance versus distributed relay:** how can systems share capabilities without inheriting unverified trust?
- **Breadth versus depth:** is a small number of rigorous cross-domain replications more informative than many demonstrations?

These are design alternatives for comparative research, not choices already settled by the framework.

## 20. Source Research Programs

- **ASSI:** https://github.com/sizhet/Adversarial-Structural-Security-Intelligence
- **D-BTP:** https://github.com/sizhet/Dynamic-Bucket-Tree-of-Permutation-and-Directional-Structural-Evolution
- **CDE:** https://github.com/sizhet/Constrained-Delta-Evolution
- **WE-SIO:** https://github.com/sizhet/World-Entity-and-Structural-Intelligence-Operations
- **OCSRE:** https://github.com/sizhet/Object-Centric-Structural-Reasoning-and-Evolution

These repositories provide related research proposals and terminology; citing them does not imply that the present directions have been experimentally established.

## 21. Closing Research Principle

The long-term opportunity is a system that can **retain what it has not resolved, locate where further intelligence may be useful, generate constrained structural changes, test them, and relay validated capabilities with their evidence and limitations**.

The near-term obligation is narrower and more rigorous: build explicit contracts, choose credible baselines, preregister comparisons, preserve failures, and publish the boundaries of every claimed advantage. Structural intelligence becomes a stronger research program when its architecture is open to correction by evidence.
