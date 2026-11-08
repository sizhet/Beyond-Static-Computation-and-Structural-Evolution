# CONTENTS — Repository Guide and Research Cross-Index

**Beyond Static Computation: Object-Centric Structural Evolution and Persistent Intelligence**  
**Version:** 0.1.0 · **Date:** 2026-11-08 · **Status:** Research synthesis, proposed specifications, and experimental protocols

> **Interpretation note.** This index describes research documents and planned validation activities. A specification is not an implementation; a laboratory design is not a completed experiment; a hypothesis is not a validated result. Links are repository-relative and assume the directory layout below.

## 1. Begin Here

| Document | Purpose | Reader |
| --- | --- | --- |
| [README.md](README.md) | Research thesis, scope, architecture, source repositories, and entry points | All readers |
| [START-HERE.md](START-HERE.md) | Guided reading paths and first steps | New readers and contributors |
| **CONTENTS.md** | Complete document map, research traceability, and navigation | All readers |

**Fast route:** [001](docs/001-Five-DOI-Peaks.md) → [002](docs/002-WE-SIO-Object-Native-Intelligence.md) → [003](docs/003-Structural-Evolution-Computing.md) → [004](docs/004-Residual-First-In-Situ-Intelligence.md) → [005](docs/005-Persistent-Structural-Discovery.md) → [006](docs/006-Intelligence-Spillover-and-Relay.md).

## 2. Six Core Research Papers (`docs/`)

| ID | Document | Central research question | Figure |
| --- | --- | --- | --- |
| 001 | [Five DOI Peaks](docs/001-Five-DOI-Peaks.md) | How do ASSI, D-BTP, CDE, WE-SIO, and OCSRE converge without losing their distinct scopes? | Fig-001 |
| 002 | [WE-SIO Object-Native Intelligence](docs/002-WE-SIO-Object-Native-Intelligence.md) | How should persistent identity, state, relations, history, residuals, and capabilities interoperate with SQL and plugins? | Fig-002 |
| 003 | [Structural Evolution Computing](docs/003-Structural-Evolution-Computing.md) | How can constrained deltas, path memory, adaptive search, and evolving candidate generators be specified and compared? | Fig-003 |
| 004 | [Residual-First In-Situ Intelligence](docs/004-Residual-First-In-Situ-Intelligence.md) | Can persistent, actionable residual objects improve learning and reasoning at computational boundaries? | Fig-004 |
| 005 | [Persistent Structural Discovery](docs/005-Persistent-Structural-Discovery.md) | Can selective observation, CCC, Two-Way CCC, triggering, and sandbox validation sustain valuable discoveries? | Fig-005 |
| 006 | [Intelligence Spillover and Relay](docs/006-Intelligence-Spillover-and-Relay.md) | What makes a capability transferable, independently verifiable, and safe to reuse? | Fig-006 |

### Suggested conceptual sequence

```text
Five DOI research lines
    ↓
WE-SIO: persistent object-native structural context
    ↓
Residual-first: preserve unresolved differences and opportunities
    ↓
Persistent discovery: observe → localize → hypothesize → test
    ↕
CDE / OCSRE: constrained delta generation, evaluation, and evolution
    ↓
Evidence-bound validation and capability relay
    ↓
Collective learning, cross-domain feedback, and new residuals
```

This is an explanatory dependency map, not a claim that the research program already operates as an integrated runtime.

## 3. Proposed Technical Specifications (`specifications/`)

| ID | Document | Contract coverage | Key relationship |
| --- | --- | --- | --- |
| SPEC-001 | [Object–Residual–Delta Interfaces](specifications/SPEC-001-Object-Residual-Delta-Interfaces.md) | Typed records, identity, provenance, state versions, residual lifecycle, delta feasibility and replay | Papers 002–004; EXP-001/002 |
| SPEC-002 | [Persistent Discovery Loop](specifications/SPEC-002-Persistent-Discovery-Loop.md) | Observation, prioritization, candidate creation, CCC/Two-Way CCC, sandbox evaluation, budget control, feedback | Papers 004–005; EXP-001/003 |
| SPEC-003 | [Validation and Relay Contracts](specifications/SPEC-003-Validation-and-Relay-Contracts.md) | Evidence status, conformance, reproducibility, permissions, applicability boundaries, promotion and relay | Paper 006; all laboratories |

**Normative language** (MUST, SHOULD, MAY) in these files governs a hypothetical conforming implementation. Conformance and effectiveness must be established separately.

## 4. Research Governance and Falsification (`research/`)

| Document | Function | Status |
| --- | --- | --- |
| [RESEARCH-DIVERGENCES.md](research/RESEARCH-DIVERGENCES.md) | Records alternative explanations, disagreements, and research forks (RD-001–RD-012) | Drafted |
| [OPEN-QUESTIONS.md](research/OPEN-QUESTIONS.md) | Unresolved theoretical, engineering, and validation questions | Drafted |
| [TESTABLE-HYPOTHESES.md](research/TESTABLE-HYPOTHESES.md) | Falsifiable claims TH-001–TH-018, baselines, ablations, and measurement plans | Drafted |
| [VALIDATION-ROADMAP.md](research/VALIDATION-ROADMAP.md) | Staged validation, phase gates, evidence requirements, and research milestones | Drafted |
| [STRUCTURAL-CLAIMS-REGISTRY.md](research/STRUCTURAL-CLAIMS-REGISTRY.md) | Planned claim-to-source-to-evidence registry; must not imply unverified claims are established | **Planned** |

**Evidence rule:** Retain negative results, inconclusive tests, failed transfer attempts, and unresolved residuals. No candidate capability should be labeled *validated* without meeting its applicable contract and evidence gate.

## 5. Three Experimental Laboratories (`experiments/`)

| ID | Document | Test environment | What is actually being tested | Figure |
| --- | --- | --- | --- | --- |
| EXP-001 | [SQL Discovery Lab](experiments/EXP-001-SQL-Discovery-Lab.md) | SQL tables, rows, relations, and change-data capture | Semantic alignment, persistent residuals, discovery quality, and validated reusable patterns | Fig-007 |
| EXP-002 | [Dynamic Scheduling Lab](experiments/EXP-002-Dynamic-Scheduling-Lab.md) | Dynamic school-bus scheduling | Feasibility, vehicle minimization, ride-time and service constraints, adaptation, and operator evolution | Fig-008 |
| EXP-003 | [Stock Pattern Lab](experiments/EXP-003-Stock-Pattern-Lab.md) | Nonstationary market time series | Pattern validity, walk-forward generalization, leakage control, net utility after costs, and robustness | Fig-009 |

These are **proposed experimental designs**. No performance figures, market returns, validated discoveries, or generalization results are claimed by their inclusion.

### Comparison discipline

- Use conventional and strong adaptive baselines, not only a weak static baseline.
- Match compute, observation, tuning, and information budgets where possible.
- Preregister metrics, temporal splits, failure thresholds, and ablations.
- Separate schema conformance, experimental feasibility, statistical evidence, practical value, and cross-domain transfer.
- Preserve both successful and failed evidence packages for future Relay.

## 6. Figures (`figures/`)

The ten planned official figures and their primary insertion points are:

| Figure | File | Primary document |
| --- | --- | --- |
| Fig-001 | `Fig-001-Five-DOI-Peaks-and-Structural-Convergence.png` | `docs/001-Five-DOI-Peaks.md` |
| Fig-002 | `Fig-002-WE-SIO-Object-Native-Intelligence-Architecture.png` | `docs/002-WE-SIO-Object-Native-Intelligence.md` |
| Fig-003 | `Fig-003-Structural-Evolution-Computing-Architecture.png` | `docs/003-Structural-Evolution-Computing.md` |
| Fig-004 | `Fig-004-Residual-First-In-Situ-Intelligence-Loop.png` | `docs/004-Residual-First-In-Situ-Intelligence.md` |
| Fig-005 | `Fig-005-Persistent-Structural-Discovery-and-SEFL.png` | `docs/005-Persistent-Structural-Discovery.md` |
| Fig-006 | `Fig-006-Intelligence-Spillover-and-Collective-Relay.png` | `docs/006-Intelligence-Spillover-and-Relay.md` |
| Fig-007 | `Fig-007-SQL-Discovery-Laboratory.png` | `experiments/EXP-001-SQL-Discovery-Lab.md` |
| Fig-008 | `Fig-008-Dynamic-Scheduling-Evolution-Laboratory.png` | `experiments/EXP-002-Dynamic-Scheduling-Lab.md` |
| Fig-009 | `Fig-009-Stock-Pattern-Discovery-Laboratory.png` | `experiments/EXP-003-Stock-Pattern-Lab.md` |
| Fig-010 | `Fig-010-Structural-Claims-Validation-and-Relay-Roadmap.png` | `research/VALIDATION-ROADMAP.md` |

Figure titles are the **canonical target filenames**. Before publication, confirm that the corresponding PNG files have been copied or renamed into `figures/`, and that captions, internal labels, and figure links match the final files. A figure illustrates a proposed mechanism; it does not constitute validation evidence.

## 7. Cross-Index: From Research Question to Experiment

| Research focus | Main paper | Specification | Research record | Proposed experiment |
| --- | --- | --- | --- | --- |
| Persistent identity and SQL compatibility | 002 | SPEC-001 | TH-001–TH-003 | EXP-001 |
| Constrained state and delta evolution | 003 | SPEC-001 | TH-004–TH-006 | EXP-002 |
| Residual persistence and actionable localization | 004 | SPEC-001/002 | TH-007–TH-009 | EXP-001/002 |
| Selective observation and structural discovery | 005 | SPEC-002 | TH-010–TH-014 | EXP-001/003 |
| Evidence-bearing capability transfer | 006 | SPEC-003 | TH-015–TH-017 | EXP-001/002/003 |
| End-to-end system value after costs | 001–006 | SPEC-001–003 | TH-018 | Integrated evaluation, if implemented |

Hypothesis IDs refer to [`TESTABLE-HYPOTHESES.md`](research/TESTABLE-HYPOTHESES.md). This matrix provides **planned traceability**, not experimental outcomes.

## 8. Research Lifecycle and Evidence States

```text
Research claim / open question
          ↓
Testable hypothesis + alternative explanation
          ↓
Specification and conformance checks
          ↓
Preregistered experiment and baseline comparison
          ↓
Observed evidence + uncertainty + negative results
          ↓
Independent validation / replication
          ↓
Scoped capability package (only if supported)
          ↓
Controlled relay and cross-domain revalidation
          ↘
       New residuals, questions, and research divergences
```

Suggested evidence labels: `proposed`, `specified`, `conformance-tested`, `experimentally-supported`, `replicated`, `rejected`, and `inconclusive`. These are not interchangeable; a result may also be domain- or version-limited.

## 9. Source DOI Research Lines

The synthesis is informed by the following separately scoped repositories:

1. **ASSI:** [Adversarial Structural Security Intelligence](https://github.com/sizhet/Adversarial-Structural-Security-Intelligence)
2. **D-BTP:** [Dynamic Bucket Tree of Permutation and Directional Structural Evolution](https://github.com/sizhet/Dynamic-Bucket-Tree-of-Permutation-and-Directional-Structural-Evolution)
3. **CDE:** [Constrained Delta Evolution](https://github.com/sizhet/Constrained-Delta-Evolution)
4. **WE-SIO:** [World Entity and Structural Intelligence Operations](https://github.com/sizhet/World-Entity-and-Structural-Intelligence-Operations)
5. **OCSRE:** [Object-Centric Structural Reasoning and Evolution](https://github.com/sizhet/Object-Centric-Structural-Reasoning-and-Evolution)

These repositories provide conceptual provenance; their existence does not independently establish the validity of the integrated research claims.

## 10. Additional Repository Assets

The following navigational, publication, and metadata files are part of the intended repository layout; some may still need drafting or assembly:

| File | Role |
| --- | --- |
| `GLOSSARY.md` | Definitions and acronym consistency |
| `FIGURE-INDEX.md` | Figure descriptions, captions, and insertion guidance |
| `FUTURE-DIRECTIONS.md` | Long-term research branches and engineering priorities |
| `CHANGELOG.md` | Versioned research-document changes |
| `CITATION.cff` | Machine-readable citation metadata |
| `.zenodo.json` | Zenodo deposit metadata, with correct leading dot |
| `LICENSE` | Repository license (Apache-2.0 intended; verify the actual file) |

**Publication hygiene:** Ensure every referenced document exists at its canonical path, each figure has the canonical filename, metadata is syntactically valid, and DOI fields are not invented or filled before issuance.

## 11. Intended Repository Tree

```text
Beyond-Static-Computation-and-Structural-Evolution/
├── README.md
├── START-HERE.md
├── CONTENTS.md
├── docs/
│   ├── 001-Five-DOI-Peaks.md
│   ├── 002-WE-SIO-Object-Native-Intelligence.md
│   ├── 003-Structural-Evolution-Computing.md
│   ├── 004-Residual-First-In-Situ-Intelligence.md
│   ├── 005-Persistent-Structural-Discovery.md
│   └── 006-Intelligence-Spillover-and-Relay.md
├── specifications/
│   ├── SPEC-001-Object-Residual-Delta-Interfaces.md
│   ├── SPEC-002-Persistent-Discovery-Loop.md
│   └── SPEC-003-Validation-and-Relay-Contracts.md
├── research/
│   ├── STRUCTURAL-CLAIMS-REGISTRY.md       # planned
│   ├── RESEARCH-DIVERGENCES.md
│   ├── OPEN-QUESTIONS.md
│   ├── TESTABLE-HYPOTHESES.md
│   └── VALIDATION-ROADMAP.md
├── experiments/
│   ├── EXP-001-SQL-Discovery-Lab.md
│   ├── EXP-002-Dynamic-Scheduling-Lab.md
│   └── EXP-003-Stock-Pattern-Lab.md
├── figures/
│   └── Fig-001-...png through Fig-010-...png
├── GLOSSARY.md                              # planned
├── FIGURE-INDEX.md                          # planned
├── FUTURE-DIRECTIONS.md                     # planned
├── CHANGELOG.md                             # planned
├── CITATION.cff                             # planned
├── .zenodo.json                             # planned
└── LICENSE                                  # verify before release
```

## 12. Contribution and Maintenance Rules

1. **Link claims to evidence:** distinguish assumptions, proposals, measurements, and replicated results.
2. **Preserve leftovers:** record failed tests, rejected hypotheses, unresolved discrepancies, and alternative interpretations.
3. **Keep interfaces auditable:** version object schemas, delta semantics, evaluation contracts, and evidence provenance.
4. **Compare fairly:** retain strong existing methods as baselines and account for total costs.
5. **Constrain relay:** a transferred capability inherits its limits and requires renewed validation in a new context.
6. **Maintain the index:** update this file when adding, renaming, or relocating a paper, specification, experiment, figure, or research artifact.

---

**Navigation:** [README](README.md) · [START HERE](START-HERE.md) · [Core papers](docs/001-Five-DOI-Peaks.md) · [Testable hypotheses](research/TESTABLE-HYPOTHESES.md) · [Validation roadmap](research/VALIDATION-ROADMAP.md)

*Research principle: Preserve structure and residuals; evolve under constraints; validate before promotion; relay evidence, limitations, and open questions rather than confidence alone.*
