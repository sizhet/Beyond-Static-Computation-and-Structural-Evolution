# Research Divergences: Open Positions, Boundaries, and Resolution Paths

**Project:** Beyond Static Computation: Object-Centric Structural Evolution and Persistent Intelligence  
**Document:** `research/RESEARCH-DIVERGENCES.md`  
**Status:** Living research record — discussion positions, not settled consensus  
**Version:** 1.0.0 (2026-11-08)  
**Research context:** ASSI → D-BTP → CDE → WE-SIO → OCSRE

## Abstract

This document preserves consequential disagreements, alternative interpretations, and unresolved design choices arising from the five-DOI research sequence and its synthesis. Divergence is not treated as an error to eliminate. A useful divergence identifies assumptions, exposes a boundary, suggests a discriminating experiment, and leaves a traceable path for subsequent researchers. The positions below are *reconstructed research alternatives*, not attributed quotations or a claim that the collaborators have endorsed every formulation. In particular, proposals introduced during synthesis must not be silently promoted into consensus or validated fact.

## 1. Purpose and recording discipline

The companion papers propose object-native intelligence, structural evolution computing, residual-first and in-situ intelligence, persistent structural discovery, and intelligence spillover through relay. These are related but not identical claims. A coherent architecture can conceal meaningful uncertainty about its scope, feasibility, or value.

For each divergence, record: (i) shared observations; (ii) distinct positions; (iii) what is at stake; (iv) evidence that would discriminate between positions; (v) provisional disposition; and (vi) links to claims and specifications. The record should be updated when new evidence appears, retaining superseded positions in revision history.

**Evidence vocabulary:** `OBSERVATION` (documented phenomenon), `DESIGN` (specified proposal), `HYPOTHESIS` (testable expectation), `VALIDATED` (supported in a stated experimental domain), `OPEN` (not resolved), and `REJECTED-IN-SCOPE` (failed under stated conditions). These labels are not maturity guarantees.

## 2. Divergence index

| ID | Question | Main alternatives | Current disposition |
|---|---|---|---|
| RD-001 | Is residual-first a design priority or a general computing paradigm? | Architecture principle / paradigm hypothesis | OPEN |
| RD-002 | Should intelligence be present everywhere or selectively deployed? | Logical coverage / physical selective allocation | OPEN; potentially compatible |
| RD-003 | What counts as in-situ computation? | Physical co-location / semantic-state continuity | OPEN |
| RD-004 | Does CDE establish a new computational class? | Unifying specification / distinct computational paradigm | OPEN |
| RD-005 | How much intelligence belongs in the WE-SIO Core Frame? | Minimal kernel / richer native semantics | OPEN |
| RD-006 | How directly can SQL primitives map into WE-SIO? | Structural mapping / semantic-operational mapping | OPEN |
| RD-007 | Is the fishing system an experimental discovery engine or a broader evolving intelligence? | Narrow falsifiable lab / open-ended system ambition | OPEN |
| RD-008 | When does pattern discovery become emergent intelligence? | Utility threshold / reusable meta-capability threshold | OPEN |
| RD-009 | Can evaluation mechanisms evolve without corrupting evidence? | Fixed external anchors / governed evaluator co-evolution | OPEN |
| RD-010 | What constitutes a transferable capability? | Interface portability / demonstrated destination-domain utility | OPEN |
| RD-011 | What is the right first experimental domain? | SQL / scheduling / financial streams | OPEN |
| RD-012 | How should the synthesis be published? | Immediate theory DOI / staged validation-first release | OPEN |

## 3. RD-001 — Residual-first: architectural principle or computing paradigm?

**Shared ground.** Residuals can contain useful information about prediction error, unsatisfied constraints, unexplained observations, capability gaps, and evaluator disagreement. Conventional processing boundaries sometimes discard that information.

**Position A — Architecture principle.** Treat Residual as a first-class record with identity, provenance, lifecycle, and links to originating objects. This is a practical design commitment that can be implemented and measured without asserting a novel class of computation.

**Position B — Paradigm hypothesis.** Organize computation and resource allocation around persistent residuals so that discovery, generation, evaluation, and learning are driven by unresolved structure. This might constitute a distinctive systems paradigm if it delivers capabilities not reproducible by ordinary pipelines at comparable cost.

**Discriminating test.** Compare otherwise equivalent systems with and without persistent residual registries, matched for compute, model capacity, data access, and feedback. Measure verified discoveries, error reduction, reuse, and total cost—not residual count alone.

**Disposition.** Adopt A as the specification baseline; retain B as an explicit hypothesis. **Related:** paper 004; SPEC-001, SPEC-002.

## 4. RD-002 — “Wherever the rain falls, I am there”: universal presence or selective presence?

**Shared ground.** Persistent observation can preserve context and shorten the interval from change to response. The phrase describes an aspiration to be structurally ready wherever useful opportunities arise.

**Position A — Broad logical coverage.** Maintain a continuously addressable object and relation fabric, capable of recognizing signals across many domains and time scales.

**Position B — Selective physical computation.** Allocate finite sensing, inference, and validation resources dynamically, concentrating on promising residuals while preserving exploration of neglected regions.

**Potential reconciliation.** Logical presence does not require full computation at every location. A tiered architecture may combine low-cost coverage, event-triggered escalation, and targeted high-cost analysis. This reconciliation remains an engineering proposal, not a proven equivalence.

**Discriminating test.** Under fixed compute and latency budgets, compare uniform scanning, fixed priorities, and adaptive localization on recall of valuable events, false positives, latency, and missed discoveries. **Related:** papers 004–005; SPEC-002.

## 5. RD-003 — What does “in-situ” mean?

**Position A — Physical locality.** Computation executes close to the data source or object storage, reducing movement and latency.

**Position B — Semantic locality.** Computation may execute remotely, but object identity, state version, residual history, permissions, and result attribution remain continuously linked.

**Risk.** Treating these as synonyms hides network costs, consistency problems, and data-governance constraints.

**Proposed resolution.** Define two orthogonal properties: `execution_locality` and `semantic_continuity`. Benchmark each independently. A system may be semantically in-situ while physically distributed. **Related:** papers 002, 004; SPEC-001.

## 6. RD-004 — CDE: unifying language or distinct computation paradigm?

**Shared ground.** Dynamic programming, incremental algorithms, control, evolutionary computation, reinforcement learning, and search already address changing states and strategies.

**Position A — Integrative framework.** CDE supplies common contracts for state containers, constrained deltas, path memory, candidate generation, evaluator governance, and feedback across heterogeneous algorithms.

**Position B — Structural evolution paradigm.** When the generator, representation, and controlled evaluator can themselves evolve, CDE/OCSRE may enable a more general form of computation than ordinary fixed-problem solvers.

**Discriminating test.** Compare against strong established methods, including online optimization and adaptive control. Report novelty as an architectural or empirical contribution unless formal separation or repeatable performance advantages are established. **Related:** paper 003; SPEC-001.

## 7. RD-005 — Minimal WE-SIO Core Frame versus richer object-native intelligence

**Position A — Minimal core.** Identity, versioned state, relations, provenance, contracts, and plugin discovery belong in the kernel. Domain-specific reasoning, learning, and optimization remain plugins.

**Position B — Rich native object.** Residual handling, capability selection, and basic reasoning should be native, enabling uniform object behavior and reduced orchestration overhead.

**Tradeoff.** A rich core can improve consistency but risks rigidity, hidden coupling, and implementation burden. A thin core may push too much semantic responsibility into incompatible plugins.

**Discriminating test.** Implement both profiles across SQL, graph, and time-series use cases. Measure semantic interoperability, plugin portability, update cost, and failure isolation. **Related:** paper 002; SPEC-001.

## 8. RD-006 — SQL primitive alignment: structural convenience versus semantic completeness

**Shared ground.** SQL tables, rows, columns, types, keys, and change streams provide a large practical entry point for WE-SIO.

**Position A — Direct structural mapping.** Primitive columns can efficiently seed object attributes and enable low-friction adoption.

**Position B — Multi-layer mapping.** Reliable intelligence requires semantic and operational alignment: units, time, source, constraints, joins, transaction boundaries, null semantics, and incremental consistency.

**Discriminating test.** Run a schema evolution and CDC benchmark with joins, late-arriving events, inconsistent units, and transaction rollback. Measure mapping correctness and downstream false discoveries. **Related:** paper 002; SPEC-001.

## 9. RD-007 — Discovery laboratory or general evolving intelligence system?

**Position A — Bounded SEFL.** Build a falsifiable Structural Emergence Fishing Laboratory that discovers, tests, and relays candidate structures in defined domains.

**Position B — Open-ended intelligence ecology.** Treat the laboratory as an initial implementation of a persistent system that evolves its own discovery mechanisms and capabilities.

**Tradeoff.** A narrow scope yields clearer evidence; a broad scope better expresses the research vision but risks untestable success criteria.

**Disposition.** Specify and validate the bounded laboratory first without discarding the broader research objective. **Related:** paper 005; SPEC-002.

## 10. RD-008 — Pattern, capability, and emergence: where is the boundary?

**Position A — Practical utility criterion.** A new pattern that repeatedly improves a decision is a useful intelligence gain.

**Position B — Structural emergence criterion.** Stronger evidence is required: a new reusable capability, new problem representation, or improved discovery process that generalizes beyond its discovery context.

**Proposed taxonomy.** `Candidate Pattern → Replicated Relation → Validated Decision Benefit → Reusable Capability → Improved Discovery Mechanism`. This is a research classification, not a universal definition of emergence.

**Discriminating test.** Use held-out periods and domains, novelty baselines, and ablations; record failed transfers. **Related:** papers 005–006; SPEC-003.

## 11. RD-009 — Evaluator evolution versus stable truth anchors

**Position A — Fixed evaluation anchors.** Keep outcome metrics and validation rules external to the evolving system to prevent reward hacking.

**Position B — Governed evaluator evolution.** Permit new metrics and evaluators when old ones miss meaningful structures, but require independent approval and backward comparison.

**Potential reconciliation.** Separate `candidate_evaluator` from `release_evaluator`, preserve frozen benchmark suites, and require audit trails for every metric change. Evaluate whether this actually prevents self-serving metric drift. **Related:** papers 003–005; SPEC-003.

## 12. RD-010 — Relay: packaging or demonstrated transfer?

**Position A — Contract portability.** A capability is relay-ready when its inputs, outputs, constraints, evidence, and dependencies are fully specified.

**Position B — Empirical transferability.** Relay succeeds only after the recipient domain independently validates usefulness and safety.

**Proposed resolution.** Distinguish `relay-packaged`, `relay-reproduced`, and `relay-validated-in-destination`. A portable package is not proof of transfer. **Related:** paper 006; SPEC-003.

## 13. RD-011 — Which experimental pool should come first?

**SQL discovery.** Strong for schema alignment, CDC, traceability, and controlled anomaly injection; weaker for demonstrating higher-order strategy evolution.

**Dynamic scheduling.** Strong for explicit objectives, constraints, and reproducible improvement; less direct for open-ended relation discovery.

**Stock time series.** Strong real-world nonstationarity and potential decision relevance; vulnerable to data leakage, multiple testing, transaction costs, and selection bias.

**Provisional sequencing proposal.** SQL for interface conformance; scheduling for structural evolution; financial data last for stringent out-of-sample testing. This is a pragmatic proposal, not a settled priority. **Related:** papers 005–006; SPEC-002, SPEC-003.

## 14. RD-012 — Publication now or after experiments?

**Position A — Publish the theory synthesis early.** A versioned DOI preserves the research timestamp, exposes assumptions, and invites collective learning.

**Position B — Delay broad claims until validation.** Early publication can make provisional ideas appear empirically established.

**Potential reconciliation.** Publish as a specification-first research program, mark unvalidated claims clearly, release test protocols, and update evidence in later versions. DOI registration should not be described as scientific validation. **Related:** paper 001; SPEC-003.

## 15. Cross-cutting unresolved questions

1. What minimum evidence warrants creating a persistent Residual object rather than dropping a transient error?
2. Can Opportunity objects be prioritized without embedding unexamined value judgments or creating feedback loops?
3. How can object identity and provenance survive cross-database joins, aggregation, and changing schemas?
4. What safeguards prevent recursive discovery from generating unbounded hypotheses and compute costs?
5. Which aspects of CCC and Two-Way CCC are domain-independent, and which require specialized semantics?
6. How should negative results, abandoned candidates, and evaluator disagreement be preserved without overwhelming the registry?
7. What qualifies as a *new* structural capability rather than a recombination of known operations?
8. Can discovery improvements persist under distribution shift and adversarial manipulation?
9. How should permission, sovereignty, and evidence contamination risks be handled when plugins and agents exchange capabilities?
10. Which claims survive ablation of WE-SIO, Residual persistence, CDE, or Relay individually?

## 16. Evidence and experiment requirements

A divergence should not be closed solely by verbal agreement. Closure should cite a reproducible artifact: experiment specification, dataset or generator, baseline, resource budget, protocol, quantitative and qualitative outcomes, limitations, and independently inspectable provenance. Results must distinguish (a) feasibility, (b) advantage over baseline, (c) cross-domain transfer, and (d) generality.

For time-series and financial tests, enforce chronological splits, leakage checks, multiple-comparison controls, and realistic costs. For adaptive systems, freeze a validation track independent of the evolving policy. For security-related claims, include adversarial or corrupted-evidence cases. Report null and negative results as relayable knowledge.

## 17. Proposed divergence-record template

```yaml
id: RD-013
question: "A precise unresolved question"
shared_observations: []
positions:
  - label: A
    statement: "..."
    assumptions: []
  - label: B
    statement: "..."
    assumptions: []
status: OPEN
stakes: []
discriminating_evidence: []
related_claims: []
related_documents: []
resolution_history: []
last_reviewed: YYYY-MM-DD
```

A record may remain `OPEN` indefinitely. A resolved record should retain its original alternatives and evidence trail rather than being deleted.

## 18. Relationship to the repository

- `docs/001-Five-DOI-Peaks.md`: overall synthesis and the five research sources.
- `docs/002-WE-SIO-Object-Native-Intelligence.md`: object and SQL mapping questions.
- `docs/003-Structural-Evolution-Computing.md`: CDE, computation, and evaluator questions.
- `docs/004-Residual-First-In-Situ-Intelligence.md`: residual-first and locality questions.
- `docs/005-Persistent-Structural-Discovery.md`: discovery, opportunity, and emergence questions.
- `docs/006-Intelligence-Spillover-and-Relay.md`: portability and collective learning.
- `specifications/SPEC-001-Object-Residual-Delta-Interfaces.md`: record-level contracts.
- `specifications/SPEC-002-Persistent-Discovery-Loop.md`: operational discovery contracts.
- `specifications/SPEC-003-Validation-and-Relay-Contracts.md`: evidence and transfer contracts.
- `research/STRUCTURAL-CLAIMS-REGISTRY.md`: companion claim inventory; cross-reference divergence IDs when created.

## 19. Five originating DOI repositories

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

## 20. Closing principle: relay the disagreement, not just the conclusion

The purpose of this document is not to manufacture unanimity. The useful research artifact is a set of inspectable alternatives, explicit assumptions, failure modes, and experiments that future collaborators can improve. Structural intelligence advances not only by preserving what worked, but also by retaining what remains uncertain, what was contested, and what evidence would change the research direction.

---

*This document is a research-position record, not an empirical validation report. It should evolve alongside the claims registry, specifications, and reproducible experiments.*
