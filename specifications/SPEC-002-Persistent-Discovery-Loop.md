# SPEC-002 — Persistent Structural Discovery Loop

**Status:** Research specification / proposed contract (v0.1.0)  
**Scope:** Object-centric, residual-first, continuously operating structural discovery  
**Companion:** `SPEC-001-Object-Residual-Delta-Interfaces.md`  
**Research context:** ASSI → D-BTP → CDE → WE-SIO → OCSRE  
**Normative language:** MUST, SHOULD, MAY indicate proposed conformance obligations, not claims of implemented functionality.

## Abstract

This specification defines a persistent discovery loop for systems that observe changing World Entities / Structural Intelligence Objects (WE-SIO), retain actionable Residuals, generate and evaluate structural hypotheses, propose constrained Deltas, and relay validated capabilities. The loop is intended to discover useful relations and improvements rather than merely detect anomalies. It provides explicit state transitions, contracts, safety and resource boundaries, provenance requirements, and conformance tests. It does not assume that persistent observation necessarily produces emergent intelligence or comparative advantage; those are hypotheses to be tested.

## 1. Purpose and boundaries

The loop aims to preserve the continuity between observation, structural interpretation, hypothesis generation, experimentation, decision, and learning. It SHOULD support SQL/CDC streams, time-series data, event logs, and object graphs without replacing their native storage or compute engines.

It does **not** require every object to execute code locally, every anomaly to trigger a hypothesis, or every validated pattern to be deployed. Logical *in-situ* continuity means maintaining identity, evidence, state versions, and feedback at the originating object or relationship; computation MAY be delegated to remote plugins.

## 2. Architectural roles

| Role | Responsibility | Key contract |
|---|---|---|
| Source adapter | Ingest snapshots, CDC changes, or events | Source identity, offset, timestamp, schema version |
| WE-SIO registry | Maintain object identities, typed relations, state versions | Immutable references to observed versions |
| Residual detector | Compare observations with expectations, constraints, or models | Typed residual with evidence and uncertainty |
| Opportunity localizer | Rank investigation targets under budgets | Explicit selection score and exploration allocation |
| Discovery engine | Generate CCC, Two-Way CCC, pattern, and causal candidates | Hypothesis lineage and declared semantics |
| CDE generator | Propose constrained state, policy, or structural Deltas | Preconditions, constraints, reversibility, path history |
| OCSRE evaluator | Reason, simulate, test, and compare candidates | Independent evidence and reproducible evaluation |
| Control plane | Enforce authority, risk, compute budgets, and deployment gates | Deny-by-default on unsafe or unverified actions |
| Relay registry | Preserve validated findings and negative results | Versioned capability package and provenance |

## 3. Canonical records

The loop uses the Object, Residual, and Delta interfaces defined in SPEC-001. It additionally introduces three logical records.

### 3.1 ObservationEvent

```yaml
observation_id: obs-1042
source_id: sql-cdc-orders
source_offset: "partition-2:83041"
observed_at: "2026-11-08T20:00:00Z"
event_time: "2026-11-08T19:59:57Z"
object_id: order-817
object_version_before: 21
object_version_after: 22
schema_version: 3
payload_ref: immutable://observations/obs-1042
quality_flags: []
```

Adapters MUST distinguish event time from processing time when both are available; replay MUST not silently duplicate effects.

### 3.2 DiscoveryCandidate

```yaml
candidate_id: cand-301
kind: two_way_ccc             # ccc | two_way_ccc | pattern_trigger | other
origin_object_refs: [order-817@22]
origin_residual_refs: [res-099]
hypothesis: "A and B jointly predict condition C within window W"
assumptions: ["stable units", "complete source window"]
features_and_windows: ["A@W", "B@W"]
proposed_test: test-019
multiple_testing_family: family-2026-11-08-a
state: proposed
provenance_ref: immutable://lineage/cand-301
```

Candidates MUST be distinguishable from validated knowledge. A two-way association MUST NOT be labeled causal solely because evidence is available in both directions.

### 3.3 OpportunityRecord

```yaml
opportunity_id: opp-072
candidate_refs: [cand-301]
expected_value: 0.6          # example normalized score, not money
information_gain_estimate: 0.4
compute_cost_estimate: 0.1
risk_estimate: 0.2
uncertainty: 0.35
selection_policy_version: select-v2
state: queued
```

Scoring scales, uncertainty calibration, and missing-value behavior MUST be documented. Opportunity scores are resource-allocation estimates, not proof of real-world value.

## 4. Persistent loop and state machine

The canonical loop is:

```text
OBSERVE → ALIGN → DETECT → LOCALIZE → GENERATE → TEST
                                            ↓
                           REJECT / DEFER / VALIDATE
                                            ↓
                               APPROVE → ACT / RELAY
                                            ↓
                                  FEEDBACK → OBSERVE
```

Each transition MUST produce an auditable record or a documented no-op. The following table specifies minimum transition gates.

| Transition | Preconditions | Output | Failure path |
|---|---|---|---|
| Observe → Align | Source authentication, offset and schema | Versioned observation | Quarantine malformed event |
| Align → Detect | Object mapping and temporal validity | Residual or no-residual result | Mark unresolved semantics |
| Detect → Localize | Residual evidence and priority inputs | Selected/deferred investigation | Retain with expiration/revisit policy |
| Localize → Generate | Budget and permitted generators | Candidate(s) with lineage | Record no-candidate outcome |
| Generate → Test | Test plan, split strategy, risk approval | Test results and uncertainty | Reject, revise, or defer |
| Test → Validate | Predeclared acceptance criteria met | Versioned validated finding | Record falsification and limitations |
| Validate → Act | Deployment authority, impact/risk gate | Controlled action and rollback plan | Relay only; no action |
| Validate → Relay | Portable contract and evidence | Capability package | Retain local-only finding |
| Act/Relay → Feedback | Outcome and monitoring window | Updated evidence and residuals | Flag missing feedback |

No candidate MAY move directly from `proposed` to `deployed` without validation and authorization. Emergency safety actions MAY use separate predefined operational rules, but MUST NOT be misrepresented as discoveries validated by this loop.

## 5. Detection and Residual semantics

Detectors SHOULD recognize prediction, constraint, explanation, capability, and evaluation residuals, with extension points for other types. Each residual MUST preserve its originating object/state version, expected or required condition, observed evidence, uncertainty, time scope, and resolution status. Noise filtering MUST NOT silently erase counterexamples: dropped or suppressed items SHOULD be represented in aggregate audit statistics, with sampling for inspection.

Residuals are not all scalar errors. Systems SHOULD support structured, relational, and qualitative residual payloads and MUST avoid meaningless cross-type numerical comparisons.

## 6. Discovery operators

### 6.1 CCC candidates

A CCC candidate represents a proposed common concept or condition distilled from multiple observations or relationships. The generator MUST specify its inputs, equivalence criteria, supporting examples, and counterexamples.

### 6.2 Two-Way CCC candidates

A Two-Way CCC candidate records directional evidence from A toward B and B toward A, potentially with different strengths, contexts, and confounders. Both directions MUST retain separate provenance and evaluation results. Bidirectionality alone does not establish symmetry, causality, or generality.

### 6.3 Pattern Triggering

A pattern trigger is an executable condition associated with a proposed action, question, or capability invocation. Trigger specifications MUST declare window semantics, thresholds, hysteresis or cooldown behavior, duplicate suppression, and consequences of false positives/negatives. Any consequential action requires an independent policy gate.

## 7. CDE and OCSRE integration

CDE MAY generate Deltas to object states, candidate representations, search operators, or strategies. Every proposed Delta MUST include versioned preconditions, constraint checks, a sandbox or equivalent validation plan, and path-memory semantics. Non-reusable path Deltas and loop-back restrictions MUST be interpreted within an explicit search scope; they are not universal laws for all possible state transitions.

OCSRE MAY coordinate object-centric reasoning, evaluation plugins, and learning. When the evaluation policy itself changes, the system MUST retain an independent reference metric or holdout evaluator to detect reward hacking and metric drift.

## 8. Localization and compute budgeting

A proposed prioritization objective is:

\[
\operatorname{priority}(o)=\frac{\mathbb E[\text{information gain}+\lambda\,\text{utility gain}\mid o]-\rho\,\text{risk}(o)}{\epsilon+\text{estimated cost}(o)}
\]

This is an illustrative policy, **not** a universal scoring law. The control plane SHOULD reserve a measurable exploration budget for under-observed objects, maintain per-object and global quotas, and document why investigations are deferred. Broad logical coverage does not imply continuous full-rate physical monitoring of every object.

## 9. Temporal and distributed correctness

Implementations MUST define handling for late/out-of-order events, duplicate delivery, schema evolution, clock uncertainty, source corrections, and replay. State commits SHOULD use compare-and-swap or equivalent version checks. Exactly-once processing MUST NOT be claimed without a corresponding end-to-end guarantee; idempotent processing with durable offsets is an acceptable design.

Cross-object conclusions MUST specify join windows and consistency assumptions. Findings based on incompatible snapshots MUST be flagged rather than silently merged.

## 10. Validation and discovery quality

The laboratory MUST distinguish:

1. **Candidate pattern:** an unverified relation.
2. **Replicated finding:** repeated under a defined replication protocol.
3. **Validated structural knowledge:** passes predeclared evidence thresholds and appropriate holdout tests.
4. **Transferable capability:** validated in at least one additional context with a declared adaptation contract.
5. **Discovery-mechanism improvement:** measurable improvement in future discovery efficiency or quality relative to baselines.

Testing SHOULD use temporal holdouts for streaming data, family-wise or false-discovery-rate controls for large hypothesis searches, leakage checks, negative controls, and independent replications where feasible. Financial strategies MUST be evaluated after transaction costs, latency, slippage, and regime changes, and SHOULD begin in paper trading rather than live execution.

## 11. Security, privacy, and authority

The loop MUST implement least-privilege source access, plugin sandboxing, authenticated capability calls, data minimization, retention rules, and an auditable deployment boundary. Untrusted source data and generated hypotheses MUST NOT be treated as instructions. Adversarial manipulation of evidence, identities, or triggers SHOULD be tested using ASSI-style threat models. Automated actions with financial, security, or safety consequences MUST require explicit risk policy and authorization.

## 12. Relay package contract

A validated discovery MAY be exported as:

```yaml
relay_id: relay-018
finding_id: finding-031
version: 1.0.0
semantic_contract: contracts/pattern-031.yaml
required_object_types: [order]
required_plugins: [temporal-join-v2]
evidence_refs: [test-019, replication-004]
known_failures: ["unstable under missing timestamps"]
applicability_limits: ["window <= 1 day"]
conformance_tests: [test-trigger-031]
license: Apache-2.0
status: validated_not_deployed
```

Relay MUST preserve provenance, scope limits, and unresolved residuals. Repeated execution and negative results MAY contribute useful learning records even when they yield no new capability.

## 13. Conformance profiles

- **P0 — Observable:** versioned objects, events, source offsets, and replay tests.
- **P1 — Residual-aware:** P0 plus typed residuals, evidence, uncertainty, and lifecycle tests.
- **P2 — Discovering:** P1 plus candidate generation, hypothesis lineage, and controlled statistical evaluation.
- **P3 — Evolvable:** P2 plus sandboxed CDE proposals, versioned policies, and safe rollback.
- **P4 — Relay-capable:** P3 plus portable capability contracts, transfer tests, and longitudinal outcome monitoring.

Profiles are cumulative. Conformance describes interface and process compliance; it does **not** establish intelligence emergence or economic superiority.

## 14. Minimal conformance test suite

| ID | Test | Expected behavior |
|---|---|---|
| PDL-T01 | Replay identical CDC event twice | No duplicated committed state change |
| PDL-T02 | Out-of-order observation | Version conflict detected or correctly reconciled |
| PDL-T03 | Missing units in SQL field | Semantic alignment deferred or quarantined |
| PDL-T04 | Uncertain residual | Uncertainty retained; not auto-validated |
| PDL-T05 | Multiple hypothesis search | Correction family and test count recorded |
| PDL-T06 | Bidirectional association | No unsupported causal assertion |
| PDL-T07 | Unsafe proposed Delta | Sandbox/policy gate blocks commit |
| PDL-T08 | Changed evaluator | Independent holdout/reference metric preserved |
| PDL-T09 | Budget exhaustion | Graceful deferral with recorded reason |
| PDL-T10 | Invalid relay contract | Export rejected with actionable diagnostics |
| PDL-T11 | Source poisoning attempt | Data remains untrusted; authority boundary intact |
| PDL-T12 | Post-deployment degradation | Monitoring triggers review, rollback, or retirement |

## 15. Research hypotheses

- **H1:** Persistent object/residual continuity improves useful discovery yield per compute unit compared with stateless periodic scans.
- **H2:** Two-Way CCC operators identify reproducible relations not found by equivalent one-way baselines at matched false-discovery rates.
- **H3:** CDE-guided hypothesis/operator evolution improves sample efficiency over fixed generators on selected dynamic tasks.
- **H4:** In-situ lineage reduces time-to-explanation and evidence reconstruction cost.
- **H5:** Relay packages improve cross-domain adaptation time while preserving quality and failure transparency.
- **H6:** Budget-aware opportunity localization outperforms uniform scanning without systematically neglecting rare high-value discoveries.

These are proposed falsifiable hypotheses, not empirical findings.

## 16. Reference experiments

**Experiment A — SQL discovery:** Use a versioned multi-table dataset with CDC. Compare static SQL rules, streaming anomaly detection, and the proposed loop at equal compute budgets. Measure precision, discovery novelty, latency, and provenance completeness.

**Experiment B — Dynamic scheduling:** Introduce changing routes, demand, and vehicle constraints. Compare fixed heuristics, online optimization, and CDE-guided proposals. Measure feasibility, fleet size, travel burden, compute cost, and retained learning.

**Experiment C — Financial time series:** Use walk-forward splits and strictly lagged information. Compare fixed features, online learning, and persistent discovery. Measure calibrated predictive gain and risk-adjusted net utility after realistic costs. No live trading is required.

## 17. Open issues and extension points

1. What constitutes a genuinely novel CCC versus a reformulation of an existing feature?
2. How should structured and qualitative Residuals be ranked without false precision?
3. What is the minimum persistent state required for cross-session learning?
4. Which operations should be local to an object, and which delegated to shared plugins?
5. How should exploration budgets adapt to drift and adversarial sources?
6. When is a new plugin justified rather than a new configuration of an existing plugin?
7. How can discoveries be compared when domains have different utility measures?
8. What evidence is sufficient to claim evolution of the *discovery mechanism* itself?

## 18. Relationship to the research series

This specification operationalizes the persistent discovery direction of `005-Persistent-Structural-Discovery.md`, building on `002-WE-SIO-Object-Native-Intelligence.md`, `003-Structural-Evolution-Computing.md`, and `004-Residual-First-In-Situ-Intelligence.md`. `SPEC-001` defines the underlying object/residual/delta interfaces; the planned `SPEC-003-Validation-and-Relay-Contracts.md` should formalize evidence gates, capability packaging, and transfer validation in greater detail.

### Foundational repositories

- [ASSI — Adversarial Structural Security Intelligence](https://github.com/sizhet/Adversarial-Structural-Security-Intelligence)
- [D-BTP — Dynamic Bucket Tree of Permutation](https://github.com/sizhet/Dynamic-Bucket-Tree-of-Permutation-and-Directional-Structural-Evolution)
- [CDE — Constrained Delta Evolution](https://github.com/sizhet/Constrained-Delta-Evolution)
- [WE-SIO — World Entity and Structural Intelligence Operations](https://github.com/sizhet/World-Entity-and-Structural-Intelligence-Operations)
- [OCSRE — Object-Centric Structural Reasoning and Evolution](https://github.com/sizhet/Object-Centric-Structural-Reasoning-and-Evolution)

---

**Specification principle:** Preserve what was observed, what remains unexplained, what was proposed, how it was tested, who may act, and what can be relayed. A persistent discovery loop is valuable only insofar as these distinctions remain inspectable and testable.
