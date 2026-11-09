# START HERE

## Beyond Static Computation and Structural Evolution

**A reader's guide to object-native intelligence, residual-first computation, persistent structural discovery, and evidence-governed capability relay**

**Status:** Research framework and experimental program; not a claim of demonstrated superiority or a production-ready runtime.  
**Version:** 0.1.0  
**Date:** 2026-11-08

---

## 1. What Is This Repository?

This repository is a synthesis and validation-oriented research program connecting five complementary lines of work:

1. **ASSI — Adversarial Structural Security Intelligence:** evolving identities, evidence, trust, authority, incentives, and adversarial dependencies.
2. **D-BTP — Dynamic Bucket Tree of Permutation:** directional candidate generation, path-sensitive structural search, and hypothesis evolution.
3. **CDE — Constrained Delta Evolution:** constrained state transitions, composable deltas, path memory, adaptive branching, and generator evolution.
4. **WE-SIO — World Entity and Structural Intelligence Operations:** persistent object identity, state, relations, history, residuals, capabilities, and extensible operations.
5. **OCSRE — Object-Centric Structural Reasoning and Evolution:** object-centered reasoning, in-situ learning, differential computation, constrained evolution, and capability spillover.

The central question is not whether computation can be dynamic—many established disciplines already address dynamic systems—but whether **persistent structural context, first-class residuals, constrained evolution, and evidence-bearing relay** can produce measurable advantages over appropriately selected existing methods.

This is a **research map**, not a replacement proposal for databases, dynamic programming, streaming systems, online learning, control theory, or optimization.

## 2. The Research Idea in One Minute

A system observes changing world entities and computational objects. It retains identity, state, relations, and history rather than repeatedly reconstructing context. It represents unresolved differences, conflicts, surprises, and opportunities as durable **Residual** records. These residuals help localize candidate discoveries and actions. **Delta** operators propose constrained changes; sandboxes and evaluators test them. Validated findings can be packaged with interfaces, provenance, evidence, limits, and unresolved questions for reuse by other agents, domains, or research groups.

A compact conceptual loop is:

```text
World / Data / Agents
        |
        v
Persistent WE Objects + Events + History
        |
        v
Residual Capture and Opportunity Localization
        |
        v
CCC / Two-Way CCC / Pattern and Hypothesis Generation
        |
        v
Constrained Delta Generation (CDE / OCSRE)
        |
        v
Sandbox -> Evaluation -> Independent Validation
        |                         |
        |                         +--> Rejected / Inconclusive
        |                               (retain evidence and leftovers)
        v
Evidence-Bound Capability Package
        |
        v
Relay / Cross-Domain Testing / Collective Learning
        |
        +------------ feedback to observation and generators
```

Every arrow is a proposed interface or workflow to specify and test—not evidence that the entire stack is already implemented.

## 3. Choose a Reading Path

### Path A — Executive and cross-disciplinary readers (20–30 minutes)

1. [`README.md`](README.md): scope, motivation, claims, and repository navigation.
2. [`docs/001-Five-DOI-Peaks.md`](docs/001-Five-DOI-Peaks.md): how the five source programs complement each other.
3. [`docs/005-Persistent-Structural-Discovery.md`](docs/005-Persistent-Structural-Discovery.md): persistent discovery and the SEFL research idea.
4. [`docs/006-Intelligence-Spillover-and-Relay.md`](docs/006-Intelligence-Spillover-and-Relay.md): how evidence-bearing capabilities may transfer.
5. [`research/OPEN-QUESTIONS.md`](research/OPEN-QUESTIONS.md): what remains unknown.

### Path B — Systems and software architects (45–60 minutes)

1. [`docs/002-WE-SIO-Object-Native-Intelligence.md`](docs/002-WE-SIO-Object-Native-Intelligence.md).
2. [`specifications/SPEC-001-Object-Residual-Delta-Interfaces.md`](specifications/SPEC-001-Object-Residual-Delta-Interfaces.md).
3. [`docs/003-Structural-Evolution-Computing.md`](docs/003-Structural-Evolution-Computing.md).
4. [`docs/004-Residual-First-In-Situ-Intelligence.md`](docs/004-Residual-First-In-Situ-Intelligence.md).
5. [`specifications/SPEC-002-Persistent-Discovery-Loop.md`](specifications/SPEC-002-Persistent-Discovery-Loop.md).
6. [`specifications/SPEC-003-Validation-and-Relay-Contracts.md`](specifications/SPEC-003-Validation-and-Relay-Contracts.md).

Focus on object lifecycle, versioning, provenance, constraint semantics, state transitions, evaluator contracts, and replayability. A conceptual interface does not imply a reference implementation.

### Path C — Experimental researchers (60–90 minutes)

1. [`research/STRUCTURAL-CLAIMS-REGISTRY.md`](research/STRUCTURAL-CLAIMS-REGISTRY.md): trace claims to tests and evidence, when available.
2. [`research/RESEARCH-DIVERGENCES.md`](research/RESEARCH-DIVERGENCES.md): competing interpretations and unresolved design choices.
3. [`research/TESTABLE-HYPOTHESES.md`](research/TESTABLE-HYPOTHESES.md): falsifiable hypotheses TH-001–TH-018.
4. [`research/VALIDATION-ROADMAP.md`](research/VALIDATION-ROADMAP.md): staged validation and gates.
5. Select an experimental laboratory from Section 5 below.

Pre-register metrics and evaluation splits before tuning. Preserve unsuccessful, null, and contradictory findings.

### Path D — Contributors and reviewers

Start with the specific claim you wish to challenge or extend. Identify its corresponding hypothesis, contract, baseline, experimental dataset, and validation status. Submit a reproducible counterexample, alternative explanation, improved contract, or independently checked result. Do not promote exploratory patterns to validated capabilities without the required evidence.

## 4. Six Core Papers at a Glance

| Paper | Question addressed | Principal contribution proposed |
|---|---|---|
| [`001 — Five DOI Peaks`](docs/001-Five-DOI-Peaks.md) | Why synthesize these five lines? | Complementarity, interfaces, and unresolved integration questions |
| [`002 — WE-SIO Object-Native Intelligence`](docs/002-WE-SIO-Object-Native-Intelligence.md) | What persists across computation? | Object identity, state, relations, history, capabilities, and plugins |
| [`003 — Structural Evolution Computing`](docs/003-Structural-Evolution-Computing.md) | How do constrained changes evolve? | Delta semantics, candidate generation, path memory, evaluation, and strategy evolution |
| [`004 — Residual-First In-Situ Intelligence`](docs/004-Residual-First-In-Situ-Intelligence.md) | What happens to unresolved differences? | Durable residual records that remain available for inference and learning |
| [`005 — Persistent Structural Discovery`](docs/005-Persistent-Structural-Discovery.md) | How can discovery continue under finite resources? | Adaptive observation, CCC, Two-Way CCC, pattern triggers, and SEFL |
| [`006 — Intelligence Spillover and Relay`](docs/006-Intelligence-Spillover-and-Relay.md) | How can validated capabilities travel? | Evidence-, contract-, and boundary-aware relay and collective learning |

## 5. Three Experimental Laboratories

### EXP-001 — SQL Discovery

[`experiments/EXP-001-SQL-Discovery-Lab.md`](experiments/EXP-001-SQL-Discovery-Lab.md)

**Setting:** SQL tables, rows, columns, relationships, and change-data-capture events.  
**Primary test:** Can persistent object and residual context improve the quality, reproducibility, or cost-efficiency of structural discovery compared with incremental and adaptive baselines?  
**Critical controls:** semantic alignment, leakage prevention, provenance, independent validation, and equal computational budgets.

### EXP-002 — Dynamic Scheduling

[`experiments/EXP-002-Dynamic-Scheduling-Lab.md`](experiments/EXP-002-Dynamic-Scheduling-Lab.md)

**Setting:** school transportation scheduling with changing students, stops, vehicles, routes, and time windows.  
**Primary test:** Can CDE/OCSRE produce feasible, high-quality repairs and learn transferable repair operators under dynamic constraints?  
**Critical controls:** safety and capacity as hard constraints; comparisons with re-optimization, rolling-horizon methods, incremental repair, and adaptive large-neighborhood search.

### EXP-003 — Stock Pattern Discovery

[`experiments/EXP-003-Stock-Pattern-Lab.md`](experiments/EXP-003-Stock-Pattern-Lab.md)

**Setting:** non-stationary market data, cross-asset relationships, events, and regime changes.  
**Primary test:** Can persistent structural discovery improve out-of-sample evidence quality or net decision utility after full costs and risks?  
**Critical controls:** walk-forward evaluation, data vintage, survivorship bias, multiple testing, transaction costs, slippage, liquidity, and regime robustness.

**Important:** A discovered market pattern is not a trading edge; statistical association does not establish causality. This laboratory is a research design, not investment advice or evidence of profitability.

## 6. The Three Specification Contracts

| Contract | What to inspect |
|---|---|
| [`SPEC-001 — Object, Residual, Delta Interfaces`](specifications/SPEC-001-Object-Residual-Delta-Interfaces.md) | Required fields, identities, versions, provenance, change semantics, and lifecycle invariants |
| [`SPEC-002 — Persistent Discovery Loop`](specifications/SPEC-002-Persistent-Discovery-Loop.md) | Observation budgets, triggers, candidate states, sandbox isolation, and feedback |
| [`SPEC-003 — Validation and Relay Contracts`](specifications/SPEC-003-Validation-and-Relay-Contracts.md) | Evidence gates, reproducibility, applicability limits, permissions, and relay eligibility |

The intended order is **specification → conformance tests → controlled experiments → evaluated runtime behavior**. Specifications alone do not establish performance.

## 7. What Counts as Evidence?

A defensible result should identify:

- **Claim and hypothesis:** a stable identifier and an outcome that could falsify the claim.
- **Comparison:** credible baselines, including established techniques appropriate to the domain.
- **Protocol:** dataset version, split, seeds, resource budget, hyperparameters, and stopping rules.
- **Metrics:** validity, quality, cost, latency, robustness, transfer, and safety where relevant.
- **Ablations:** isolate the effect of object persistence, residual retention, constrained delta evolution, discovery adaptation, and relay.
- **Limitations:** failures, null results, adverse conditions, unresolved alternatives, and threats to validity.
- **Replay package:** code/configuration or a sufficiently precise procedure, checksums where appropriate, and provenance.

**Evidence states must remain distinct:** proposed, exploratory, tested, replicated, contradicted, and unresolved. A capability may be relayed as an *experimental candidate* with explicit limitations, but must not be represented as independently validated without passing the relevant gates.

## 8. Recommended Validation Order

```text
M0  Claims, contracts, datasets, and baseline registry
M1  Object / Residual / Delta conformance and replay
M2  SQL discovery and residual ablations
M3  Dynamic scheduling and generator-evolution tests
M4  Persistent discovery, non-stationarity, and cross-domain transfer
M5  Independent replication, security review, and evidence-governed relay
```

Milestones are **proposed checkpoints**, not completed results. See [`research/VALIDATION-ROADMAP.md`](research/VALIDATION-ROADMAP.md) for dependencies and acceptance criteria.

## 9. Figures and Visual Navigation

The figures align with the six papers, three laboratories, and validation program:

| Figure | Subject | Primary location |
|---|---|---|
| Fig-001 | Five DOI Peaks and Structural Convergence | Paper 001 |
| Fig-002 | WE-SIO Object-Native Intelligence Architecture | Paper 002 |
| Fig-003 | Structural Evolution Computing Architecture | Paper 003 |
| Fig-004 | Residual-First In-Situ Intelligence Loop | Paper 004 |
| Fig-005 | Persistent Structural Discovery and SEFL | Paper 005 |
| Fig-006 | Intelligence Spillover and Collective Relay | Paper 006 |
| Fig-007 | SQL Discovery Laboratory | EXP-001 |
| Fig-008 | Dynamic Scheduling Evolution Laboratory | EXP-002 |
| Fig-009 | Stock Pattern Discovery Laboratory | EXP-003 |
| Fig-010 | Structural Claims, Validation, and Relay Roadmap | Validation roadmap |

See [`FIGURE-INDEX.md`](FIGURE-INDEX.md) for final figure names and insertion guidance. A figure is a conceptual illustration, not an experimental result.

## 10. Common Misreadings to Avoid

**“This replaces SQL.”** No. WE-SIO proposes an object-native intelligence layer that can align with and build upon SQL systems.

**“Dynamic computation is new.”** No. The proposed novelty, if demonstrated, lies in particular combinations of persistent context, residuals, constrained evolution, discovery policies, and relay contracts.

**“Residuals are only errors.”** No. They can include constraint violations, model discrepancies, missing explanations, evaluation disagreements, and candidate opportunities. Not all residuals are informative.

**“Two-Way CCC proves causality.”** No. Bidirectional conditional evidence may strengthen a hypothesis or expose asymmetry; causal inference requires additional assumptions and designs.

**“Every discovered pattern becomes intelligence.”** No. Candidates must pass relevance, reproducibility, robustness, cost, and governance checks.

**“Relay means automatic trust.”** No. Relay must preserve provenance, evidence, permissions, applicability boundaries, and failure history; receiving systems must revalidate as needed.

## 11. Source Research Repositories

- [Adversarial Structural Security Intelligence (ASSI)](https://github.com/sizhet/Adversarial-Structural-Security-Intelligence)
- [Dynamic Bucket Tree of Permutation (D-BTP)](https://github.com/sizhet/Dynamic-Bucket-Tree-of-Permutation-and-Directional-Structural-Evolution)
- [Constrained Delta Evolution (CDE)](https://github.com/sizhet/Constrained-Delta-Evolution)
- [World Entity and Structural Intelligence Operations (WE-SIO)](https://github.com/sizhet/World-Entity-and-Structural-Intelligence-Operations)
- [Object-Centric Structural Reasoning and Evolution (OCSRE)](https://github.com/sizhet/Object-Centric-Structural-Reasoning-and-Evolution)

These source repositories contain the broader research programs. This overview repository synthesizes questions and interfaces without superseding their detailed specifications.

## 12. A Practical First Contribution

Choose one claim from the claims registry or one hypothesis from [`research/TESTABLE-HYPOTHESES.md`](research/TESTABLE-HYPOTHESES.md). Then:

1. State a counterfactual and select a credible existing baseline.
2. Define a minimal dataset or reproducible synthetic case with realistic constraints.
3. Implement the smallest conformance surface needed for the test.
4. Pre-register metrics, failure thresholds, resource budgets, and stopping rules.
5. Run baselines, full-system treatment, and targeted ablations.
6. Record positive, negative, inconclusive, and contradictory outcomes.
7. Package evidence and limitations for independent review or controlled relay.

A well-supported **negative result** can be more valuable than an attractive but unverified architecture diagram.

---

## Closing Principle

> Preserve structure, preserve residuals, evolve under constraints, validate before promotion, and relay evidence rather than confidence.

The goal is to make the proposed structural-intelligence program **understandable, falsifiable, extensible, and collectively improvable**.
