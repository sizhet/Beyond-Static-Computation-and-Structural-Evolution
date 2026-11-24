# GLOSSARY — Structural Evolution and Persistent Intelligence

**Repository:** Beyond Static Computation: Object-Centric Structural Evolution and Persistent Intelligence  
**Version:** 1.0.0  
**Date:** 2026-11-08  
**Status:** Working research terminology; definitions and interfaces remain subject to validation

> **Reading rule.** This glossary standardizes how terms are used *within this research program*. Some labels are proposed constructs rather than established terms of art. Definitions do not establish empirical superiority, implementation readiness, or scientific validation. For normative interface requirements, consult the corresponding `SPEC-*` document rather than treating this glossary as a contract.

## 1. How to use this glossary

Terms are grouped by research function rather than alphabetically. An alphabetical index appears at the end. Each entry distinguishes the concept from adjacent ideas where ambiguity matters. Cross-references point to repository-relative paths. In particular, **object**, **residual**, **delta**, **discovery**, **validation**, and **relay** should not be treated as interchangeable abstractions.

**Research maturity vocabulary**

| Label | Meaning |
| --- | --- |
| **Concept** | A proposed interpretation or organizing abstraction, not necessarily an implemented mechanism. |
| **Specification** | A proposed set of interface and behavioral requirements, to be tested for conformance. |
| **Hypothesis** | A falsifiable prediction with measurable outcomes and comparators. |
| **Candidate** | An unverified pattern, method, action, or capability awaiting evaluation. |
| **Validated (scoped)** | Supported by specified evidence under explicit conditions; not universally proven. |
| **Relayed** | Transferred with relevant evidence, contracts, limitations, and provenance; not necessarily effective in the target domain. |

## 2. The five contributing DOI research lines

**ASSI — Adversarial Structural Security Intelligence.** Research on security when identities, authority, evidence, incentives, and dependencies change. It treats trust, provenance, permissions, and adversarial contamination as structural concerns. Security claims still require threat models and tests.

**D-BTP — Dynamic Bucket Tree of Permutation.** A directional, dynamically generated candidate-tree approach associated with combinatorial inference and structural search. Its research emphasis includes changing candidate sets, path semantics, and hypothesis evolution; it is not a generic claim to replace existing search algorithms.

**CDE — Constrained Delta Evolution.** A proposed framework for evolving a state through feasible, traceable deltas under constraints, path rules, feedback, and potentially adaptive generators. In the broader SIF program, CDE is also proposed as a Localization/addressing method for finding promising moves in constrained state spaces.

**WE-SIO — World Entity and Structural Intelligence Operations.** The object-native representation and operations research line: persistent entities, relations, state, history, residuals, capabilities, and extensibility. It is intended to interoperate with databases and other systems, not require their replacement.

**OCSRE — Object-Centric Structural Reasoning and Evolution.** A proposed integration of object-centric reasoning, differential computation, in-situ learning, constrained state evolution, and capability spillover. It connects representation to adaptive computation and learning.

**Structural Intelligence (SI).** The larger research approach that organizes intelligence around explicit structures, relationships, scoring, localization, control, learning, and evolution. This is a program-level framing, not a universally agreed scientific definition of intelligence.

**SIF — Structural Intelligence Framework.** The broader architecture coordinating problem/capability maps, localization and addressing, per-node intelligence, and control/governance. CDE and object-native methods are proposed complements to existing SIF localization mechanisms.

## 3. Object-native representation and interfaces

**World Entity (WE).** A modeled entity in a data, computational, organizational, or physical world, with stable reference semantics and potentially evolving state. A WE may correspond to a SQL row, a route, an event, a hypothesis, or another bounded unit, depending on its schema.

**Object-Native Intelligence.** An architectural approach in which objects and their identities, relationships, histories, and operations are first-class contexts for reasoning and adaptation. It does not imply that all computation must be object-oriented programming.

**WE Core Frame.** The minimal common envelope for identifying, locating, relating, and operating on world entities. Domain-specific details should be introduced through typed extensions or plugins rather than an unlimited monolithic core.

**Core Frame + Plugins.** A separation between stable shared semantics and optional domain-specific capabilities, policies, data adapters, and algorithms. Its extensibility advantage is a hypothesis to be tested against alternative architectures.

**Object Identity.** The persistent reference by which an object can be distinguished across updates, versions, and contexts. Identity should not be confused with a mutable label or with verified real-world identity.

**Object State.** A versioned description of the attributes and conditions relevant to an object at a particular logical or physical time.

**Object Relations.** Typed links among objects, potentially including direction, provenance, temporal validity, and confidence. A relation is not automatically causal.

**Object History.** An auditable sequence or summary of changes, observations, decisions, and associated evidence. History retention may be bounded by privacy, cost, and policy.

**Object Capability.** A bounded operation, skill, or method that an object or component can invoke or offer, subject to contracts, permissions, and preconditions.

**StructuralRecord.** A proposed common record envelope for typed identity, timestamps or versions, provenance, references, and governance fields. See [SPEC-001](specifications/SPEC-001-Object-Residual-Delta-Interfaces.md).

**ObjectRecord.** A typed representation of a persistent object and its current structural context; it is not necessarily a complete copy of all underlying data.

**Plugin Contract.** The interface, compatibility requirements, permissions, side-effect boundaries, and evidence obligations for an extension to a core frame.

**Three-Level SQL Alignment.** The mapping between object-native and relational systems at (1) **structure**—tables, rows, columns, keys; (2) **semantics**—entity meaning and relations; and (3) **operations**—queries, transactions, updates, and events. Semantic alignment must be tested rather than inferred from schema similarity.

**CDC — Change Data Capture.** Mechanisms for obtaining database change events. CDC can support incremental observation, but delivery guarantees, ordering, duplicates, and schema changes must be handled explicitly.

**Event Time / Processing Time.** Respectively, when an event occurred and when a system processed it. Confusing them can introduce leakage, incorrect histories, and invalid discovery claims.

**Provenance / Lineage.** Evidence of where a record, candidate, or capability came from and how it was transformed. Provenance supports audit but does not alone prove truth.

## 4. Residual-first and in-situ computation

**Residual.** A structured difference, gap, conflict, unexplained observation, violated expectation, or opportunity remaining after a computation or observation. It may be informative, spurious, or unresolvable.

**Residual-First Computing.** A research stance that treats residuals as durable inputs to subsequent inference, learning, and evolution instead of automatically discarding them as temporary error signals.

**Residual-Native Representation.** Encoding a residual with its own identity, source, context, history, status, and next-action possibilities, rather than only as an untyped numeric difference.

**ResidualRecord.** The typed record carrying a residual's semantics, lineage, lifecycle state, and relevant object references. See [SPEC-001](specifications/SPEC-001-Object-Residual-Delta-Interfaces.md).

**Residual Lifecycle.** The transitions through which a residual is created, triaged, investigated, tested, resolved, retained, rejected, or reopened. Rejection should preserve the evidence needed to understand why.

**Explicit Leftover.** An unresolved difference, assumption, disagreement, or unfinished task preserved for later work and relay, rather than hidden by a premature closure claim.

**Computational Boundary Loss.** Information or unresolved structure lost when a computation, task, context window, or organizational boundary is crossed. The program investigates whether persistent records can reduce some such losses.

**In-Situ Intelligence.** Reasoning, learning, or decision-making performed with access to the relevant live or persistent object context, instead of repeatedly reconstructing context from detached snapshots. It does not guarantee lower latency or better results.

**Residual Localization.** Mapping a residual to the objects, relations, state regions, capabilities, and decisions that might explain or resolve it.

**Opportunity Residual.** A residual interpreted as a possible beneficial action or new capability, not merely a failure. Opportunity classification requires validation against costs, alternatives, and false positives.

**Structural Correction.** A justified update to a model, relationship, rule, workflow, or object state in response to evidence. Correction is distinct from merely suppressing a warning.

**Residual Feedback Loop.** Observe discrepancy → preserve context → localize → form hypotheses → test → act or retain → update future observation and learning.

## 5. Delta evolution and adaptive computation

**State Container.** A bounded, versioned representation of the relevant objects, constraints, and history on which candidate changes operate.

**Delta (Δ).** A specified change between states, with preconditions, affected objects, effects, and potentially an inverse or replay record. A delta is not synonymous with a gradient or a scalar error.

**DeltaRecord.** A typed proposal or execution record for a state transition, including constraints, provenance, validation, and path context.

**Atomic Delta.** A single bounded change under a specified transaction or transition model.

**Composite Delta.** A combination of compatible changes, potentially across multiple objects or scales. Composition requires conflict checks and cannot be assumed commutative.

**Delta Composition.** Applying or combining deltas according to explicit ordering and consistency rules. `ΔA ∘ ΔB` may differ from `ΔB ∘ ΔA`.

**Reversible Delta.** A delta with a valid, defined undo operation under stated assumptions; external side effects and irreversible events may prevent reversibility.

**Constraint.** A rule defining permissible states, transitions, resources, or policies. **Hard constraints** must hold for feasibility; **soft constraints** enter preference or penalty evaluation.

**Feasibility Check.** A determination that a candidate state or transition satisfies applicable hard constraints. Feasibility is separate from quality or desirability.

**Candidate Generation.** Production of proposed deltas, states, hypotheses, or methods for evaluation; generation alone is not discovery or validation.

**Directional Field.** A structured collection of signals or scores guiding which candidate changes to explore. It is a search aid, not necessarily a physical or mathematical vector field.

**Path Memory.** Records of prior deltas, states, decisions, and rejected branches used to prevent invalid reuse, control loops, and support learning.

**Path-Local Non-Reuse.** A CDE/D-BTP rule that a delta may not be reused within the same path when the defined path semantics prohibit it. This does not automatically forbid reuse across independent branches or new episodes.

**NoSubtree / No-Branch.** A negative branching decision that excludes a defined descendant search region. It should record the reason, scope, and any conditions under which exclusion may be reconsidered.

**Loop-Back Control.** Mechanisms for detecting and managing repeated states, cycles, or revisits in an evolving search, including explicit termination and resource limits.

**M→N Adaptive Branching.** A proposed search design in which the number and structure of successor candidates can vary with state, evidence, constraints, and budget rather than remaining fixed.

**Generator Evolution.** Adaptation of the policy or operators that produce candidates, based on validated feedback. This is distinct from selecting a better candidate from a fixed generator.

**Structural Evolution Computing.** The research framing for computations that explicitly maintain state, feasible deltas, candidate generators, path histories, evaluation, and learning across repeated transitions. It overlaps with existing online optimization, control, dynamic programming, incremental computation, and evolutionary search; distinct value must be established experimentally.

**Sandbox.** An isolated or controlled environment for evaluating a candidate without immediately changing the authoritative state. Isolation strength and side-effect controls must be specified.

**Commit / Rollback.** Respectively, promotion of an approved candidate to authoritative state and reversal or compensation of a failed or withdrawn change, where supported.

## 6. Persistent discovery and SEFL

**Persistent Structural Discovery.** A repeated, evidence-driven process that maintains context and candidate histories while seeking useful new relations, patterns, methods, or opportunities over time.

**SEFL — Structural Emergence Fishing Laboratory.** A proposed experimental framework for selectively observing evolving environments, locating promising residuals, testing candidate structures, and improving discovery policy. “Fishing” is a metaphor for resource-aware opportunity search, not a claim of spontaneous intelligence emergence.

**Persistent Structural Presence.** Maintaining enough durable context and observation coverage to revisit opportunities as conditions change. It does **not** mean observing every signal continuously.

**Adaptive Observation.** Allocation of limited monitoring attention, frequency, and compute according to evidence, uncertainty, cost, and potential value.

**Opportunity Localization.** Identifying where, when, and under what conditions additional observation or experimentation may be valuable.

**CCC — Cross-Context Connection.** A proposed operation for relating signals, objects, or patterns across different contexts. A connection is a candidate relation, not automatically a causal finding.

**Two-Way CCC.** Testing a proposed connection from more than one direction or perspective, including reverse conditional evidence or reciprocal checks. Bidirectional association does not establish causality.

**Pattern Triggering.** Rules or learned policies that nominate a pattern or hypothesis for further investigation when specified structural conditions arise.

**DiscoveryCandidate.** A proposed relation, explanation, method, or capability awaiting independent evaluation.

**ObservationEvent.** A timestamped and provenance-bearing record of something observed, including the distinction between event time and processing time where applicable.

**Persistent Discovery Loop.** Observe → localize → generate candidates → evaluate in a sandbox → validate or reject → update policy and records → observe again. See [SPEC-002](specifications/SPEC-002-Persistent-Discovery-Loop.md).

**Discovery Policy.** The strategy for deciding what to monitor, which candidates to test, and how to allocate limited resources.

**Discovery Yield.** The number or value of independently validated findings relative to time, compute, data, or other specified budgets. Raw candidate count is not an adequate proxy.

**False Discovery.** A pattern that appears promising but fails an appropriate independent test or results from leakage, chance, selection effects, or confounding.

**Emergence (research usage).** A candidate system-level behavior or capability not adequately characterized by the immediately inspected local mechanisms. Claims of emergence require operational definitions, controls, and alternative explanations.

## 7. Evidence, validation, and scientific governance

**Research Claim.** A precisely scoped assertion about a mechanism, property, or comparative advantage that can be tied to evidence and counterevidence.

**Structural Claims Registry.** A proposed inventory of claims, assumptions, source documents, evidence status, limitations, and responsible experiments. It is a governance instrument, not a certificate of truth.

**Research Divergence.** A documented disagreement between plausible interpretations, architectures, or experimental approaches, preserved until evidence warrants resolution.

**Testable Hypothesis.** A prediction stating a measurable outcome, comparator, boundary conditions, and failure criteria. See [TESTABLE-HYPOTHESES](research/TESTABLE-HYPOTHESES.md).

**Baseline.** A specified existing or simpler method against which a proposed system is compared under matched data, budgets, and evaluation conditions.

**Ablation.** A controlled removal or alteration of a system component to estimate its contribution to measured outcomes.

**Conformance.** Demonstrated compliance with a specified interface, invariant, lifecycle, or behavioral contract. Conformance does not imply superior performance.

**ValidationRecord.** A typed record of protocol, data, conditions, measurements, results, reviewer or system identity, and decision status.

**Independent Validation.** Evaluation separated appropriately from candidate generation, training, and model selection, reducing circular confirmation.

**Pre-registration.** Recording hypotheses, outcomes, splits, decision rules, and analyses before inspecting confirmatory results.

**Evidence Package.** The data descriptions, code or procedure references, metrics, negative results, provenance, and environmental details needed to inspect or reproduce a claim.

**Reproducibility.** Ability to obtain materially consistent results with the specified artifacts and conditions; **replicability** may involve independently produced data or implementation. Exact standards depend on the experiment.

**Promotion Gate.** A rule preventing a candidate from being labeled validated or released as a reusable capability until its required tests, provenance, permissions, and boundary checks pass.

**Applicability Boundary.** The stated assumptions, operating regimes, constraints, populations, or environments within which evidence supports a claim.

**Negative Result.** A valid test that does not support a hypothesis, including regressions or infeasibility. Such results should remain accessible for later learning.

**Total Cost Accounting.** Measurement that includes observation, storage, computation, validation, integration, maintenance, and relay overhead—not only core algorithm runtime.

**Temporal Leakage.** Using information not legitimately available at a prediction or decision time. This is particularly important in SQL/CDC and financial time-series studies.

**Walk-Forward Validation.** Sequential evaluation using past information to make decisions about later periods, with appropriate retraining and selection boundaries.

**Multiple-Testing Correction.** Statistical procedures addressing the increased false-positive risk when many patterns, parameters, or hypotheses are screened.

**Net Utility.** Benefit after accounting for specified costs and risks. In the stock laboratory, this includes transaction costs, slippage, liquidity limits, and risk exposure; positive backtest returns alone are insufficient.

**Threat Model.** An explicit description of adversaries, capabilities, assets, trust boundaries, and attack surfaces against which security controls are evaluated.

## 8. Spillover, relay, and collective learning

**Intelligence Spillover.** A hypothesized transfer of useful structure, methods, or capability from one problem, context, or domain to another. Transfer is not established merely by shared terminology.

**Capability Relay.** The transfer of a bounded, evidence-described capability to another agent, system, task, or domain for independent assessment and potential reuse.

**Capability Relay Package (CRP).** A proposed bundle containing interface and contract definitions, provenance, validation evidence, applicability limits, permissions, failure experience, open questions, and reusable methods or artifacts.

**RelayPackage.** The typed machine-readable or document-level representation of a relayable capability and its supporting materials.

**Evidence-Bound Relay.** A policy that the strength of a relayed claim must not exceed the strength and scope of its supporting evidence.

**Collective Learning.** Improvement through sharing and evaluating knowledge, capabilities, failures, and residuals across participants. It requires mechanisms for provenance, disagreement, access control, and quality assurance.

**Cross-Domain Transfer.** Testing whether a method developed in one domain retains value in another after accounting for differences in data, constraints, incentives, and evaluation.

**Failure Relay.** Transferring unsuccessful approaches and their conditions to prevent repeated dead ends and support better future hypotheses.

**Capability Spillover vs. Capability Relay.** **Spillover** describes the possible emergence of usefulness outside the original setting; **relay** describes the governed process for packaging, transferring, testing, and potentially adopting that usefulness.

**Relay Feedback.** Evidence from target-domain reuse that updates the source capability's applicability, limitations, and subsequent versions.

**Governed Reuse.** Reuse conditioned on authorization, safety constraints, provenance, evidence, and local validation rather than automatic acceptance.

## 9. The three experimental laboratories

**EXP-001 — SQL Discovery Laboratory.** Tests SQL/CDC-to-object alignment, residual persistence, cross-context discovery, and evidence-backed relay in changing data environments. See [EXP-001](experiments/EXP-001-SQL-Discovery-Lab.md).

**EXP-002 — Dynamic Scheduling Evolution Laboratory.** Uses dynamic school transportation as a constrained optimization testbed for delta repair, evolving generators, path memory, feasibility, and transfer. The primary objective of fewer vehicles is subordinate to safety and other hard constraints. See [EXP-002](experiments/EXP-002-Dynamic-Scheduling-Lab.md).

**EXP-003 — Stock Pattern Discovery Laboratory.** Tests persistent pattern discovery under non-stationarity with strict temporal integrity, out-of-sample validation, cost and risk accounting, and adaptive baselines. It is a research protocol, not an investment recommendation. See [EXP-003](experiments/EXP-003-Stock-Pattern-Lab.md).

**Non-Stationarity.** Change over time in the data-generating process, relationships, or operating regime, potentially invalidating patterns learned from earlier periods.

**Dynamic Repair.** Updating a feasible plan after new events while minimizing disruption and respecting current constraints; its quality must be compared with established replanning methods.

**Rolling-Horizon Optimization.** Repeatedly solving or updating a planning problem over a moving time window; an important baseline for dynamic scheduling.

**Adaptive Large-Neighborhood Search (ALNS).** An optimization technique that adaptively selects destroy-and-repair operators; a strong comparator for claims about evolving delta generators.

**Comparative Advantage (experimental).** A measured, repeatable improvement over appropriate alternatives under stated data, cost, risk, and resource assumptions; not an unqualified statement of market profitability.

## 10. Important distinctions and non-claims

| Do not conflate | Necessary distinction |
| --- | --- |
| Object vs. SQL row | An object may be mapped to a row, but may also have history, behavior, relationships, and domain semantics not captured by a row alone. |
| Residual vs. error | A residual may be a gap, conflict, surprise, or opportunity; not all residuals signal faults. |
| Delta vs. residual | A residual describes what remains or differs; a delta describes a proposed or executed change. |
| Candidate vs. validated finding | A generated hypothesis is not evidence of its truth or usefulness. |
| Conformance vs. efficacy | Correct interface behavior does not establish improved discovery or optimization outcomes. |
| Two-Way CCC vs. causality | Reciprocal association is not a causal identification strategy. |
| Pattern discovery vs. trading edge | Statistical patterns need out-of-sample, cost-adjusted and risk-aware evaluation. |
| CDE vs. established optimization | CDE is a proposed organizing framework; superiority to DP, ALNS, control, or online optimization is unproven. |
| Persistence vs. exhaustive monitoring | Persistent context can coexist with selective and budget-limited observation. |
| Relay vs. validation | Transfer is not proof of effectiveness in a new environment. |
| Scientific hypothesis vs. demonstrated system | This repository chiefly contains proposals and protocols, not an already validated integrated runtime. |

## 11. Alphabetical quick index

**A:** Ablation; Adaptive Large-Neighborhood Search; Adaptive Observation; Applicability Boundary; ASSI; Atomic Delta.  
**B:** Baseline.  
**C:** Candidate Generation; Capability Relay; Capability Relay Package; CCC; CDC; CDE; Collective Learning; Comparative Advantage; Composite Delta; Computational Boundary Loss; Conformance; Constraint; Core Frame + Plugins; Cross-Domain Transfer.  
**D:** D-BTP; Delta; Delta Composition; DeltaRecord; Directional Field; DiscoveryCandidate; Discovery Policy; Discovery Yield; Dynamic Repair.  
**E:** Emergence; Evidence-Bound Relay; Evidence Package; Event Time; Explicit Leftover; EXP-001/002/003.  
**F:** Failure Relay; False Discovery; Feasibility Check.  
**G:** Generator Evolution; Governed Reuse.  
**I:** Independent Validation; In-Situ Intelligence; Intelligence Spillover.  
**L:** Loop-Back Control.  
**M:** M→N Adaptive Branching; Multiple-Testing Correction.  
**N:** Negative Result; Net Utility; NoSubtree; Non-Stationarity.  
**O:** Object Capability; Object History; Object Identity; Object Relations; Object State; Object-Native Intelligence; ObjectRecord; ObservationEvent; OCSRE; Opportunity Localization; Opportunity Residual.  
**P:** Path Memory; Path-Local Non-Reuse; Pattern Triggering; Persistent Discovery Loop; Persistent Structural Discovery; Persistent Structural Presence; Plugin Contract; Pre-registration; Processing Time; Promotion Gate; Provenance.  
**R:** Relay Feedback; RelayPackage; Reproducibility; Research Claim; Research Divergence; Residual; Residual Feedback Loop; Residual Lifecycle; Residual Localization; Residual-Native Representation; ResidualRecord; Residual-First Computing; Reversible Delta; Rolling-Horizon Optimization.  
**S:** Sandbox; SEFL; SIF; SI; State Container; Structural Claims Registry; Structural Correction; Structural Evolution Computing; StructuralRecord.  
**T:** Temporal Leakage; Testable Hypothesis; Threat Model; Three-Level SQL Alignment; Total Cost Accounting; Two-Way CCC.  
**V:** Validated (scoped); ValidationRecord.  
**W:** Walk-Forward Validation; WE Core Frame; WE-SIO; World Entity.

## 12. Primary cross-references

- **Research synthesis:** [001](docs/001-Five-DOI-Peaks.md), [002](docs/002-WE-SIO-Object-Native-Intelligence.md), [003](docs/003-Structural-Evolution-Computing.md), [004](docs/004-Residual-First-In-Situ-Intelligence.md), [005](docs/005-Persistent-Structural-Discovery.md), [006](docs/006-Intelligence-Spillover-and-Relay.md).
- **Interfaces and governance:** [SPEC-001](specifications/SPEC-001-Object-Residual-Delta-Interfaces.md), [SPEC-002](specifications/SPEC-002-Persistent-Discovery-Loop.md), [SPEC-003](specifications/SPEC-003-Validation-and-Relay-Contracts.md).
- **Scientific discipline:** [Research Divergences](research/RESEARCH-DIVERGENCES.md), [Open Questions](research/OPEN-QUESTIONS.md), [Testable Hypotheses](research/TESTABLE-HYPOTHESES.md), [Validation Roadmap](research/VALIDATION-ROADMAP.md).
- **Experiments:** [SQL Discovery](experiments/EXP-001-SQL-Discovery-Lab.md), [Dynamic Scheduling](experiments/EXP-002-Dynamic-Scheduling-Lab.md), [Stock Pattern](experiments/EXP-003-Stock-Pattern-Lab.md).
- **Navigation:** [README](README.md), [START-HERE](START-HERE.md), [CONTENTS](CONTENTS.md).

### Source DOI repositories

1. [Adversarial Structural Security Intelligence (ASSI)](https://github.com/sizhet/Adversarial-Structural-Security-Intelligence)
2. [Dynamic Bucket Tree of Permutation (D-BTP)](https://github.com/sizhet/Dynamic-Bucket-Tree-of-Permutation-and-Directional-Structural-Evolution)
3. [Constrained Delta Evolution (CDE)](https://github.com/sizhet/Constrained-Delta-Evolution)
4. [World Entity and Structural Intelligence Operations (WE-SIO)](https://github.com/sizhet/World-Entity-and-Structural-Intelligence-Operations)
5. [Object-Centric Structural Reasoning and Evolution (OCSRE)](https://github.com/sizhet/Object-Centric-Structural-Reasoning-and-Evolution)

---

**Maintenance policy.** When a concept changes, update this glossary, the normative specification (if applicable), the claims registry, and the affected experiment protocols together. Preserve competing definitions in `RESEARCH-DIVERGENCES.md` when the research has not yet resolved them. A term becoming familiar does not make its associated hypothesis true.
