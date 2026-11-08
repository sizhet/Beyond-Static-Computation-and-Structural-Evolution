# EXP-003 — Stock Pattern Discovery Laboratory

**Persistent Structural Discovery in Nonstationary Financial Markets**  
**Status:** Proposed experimental protocol; not empirical evidence  
**Version:** 0.1.0  
**Date:** 2026-11-08  
**Program:** Beyond Static Computation — Object-Centric Structural Evolution and Persistent Intelligence

## Abstract

This experiment tests whether a persistent, object-centric discovery system built from World Entity and Structural Intelligence Operations (WE-SIO), Residual-First computation, Constrained Delta Evolution (CDE), and Object-Centric Structural Reasoning and Evolution (OCSRE) can identify, independently validate, and responsibly exploit structural patterns in nonstationary equity-market data. It treats patterns as *hypotheses*, not trading signals until stringent point-in-time, out-of-sample, multiple-testing, execution-cost, and risk checks have been passed. The central question is whether a continuously learning discovery architecture improves the *quality, reproducibility, timeliness, and transferability* of discoveries at comparable total cost—not whether it can generate many correlations or attractive backtests.

This document specifies experiments rather than reporting results. No positive return, intelligence emergence, or superiority is assumed.

## 1. Research Context and Scope

The laboratory operationalizes the research sequence ASSI → D-BTP → CDE → WE-SIO → OCSRE and the program's six thematic papers. Financial markets are a demanding test bed because of regime changes, feedback effects, adversarial adaptation, data revisions, crowded strategies, and transaction costs. This makes them useful for testing the limits of persistent structural discovery, but unsuitable for inferring success from a single profitable simulation.

The laboratory is a research environment with simulated execution by default. It is not a recommendation to trade, an investment strategy, or a claim of expected profit. Live deployment requires separate authorization, controls, and compliance review.

### 1.1 Questions

1. Does object-native representation reduce semantic or operational errors relative to conventional market-data pipelines?
2. Does retaining structured residuals improve the efficiency of subsequent hypothesis generation?
3. Do CCC, Two-Way CCC, and pattern-trigger candidates yield independently replicated discoveries beyond standard statistical methods?
4. Can CDE/OCSRE adapt discovery operators without overfitting their own evaluation process?
5. Can validated discoveries transfer across securities, sectors, market regimes, or datasets?
6. Do any observed advantages survive realistic costs, capacity limits, and equal-budget comparisons?

### 1.2 Non-goals

The experiment does not attempt to prove universal market predictability, establish causality from correlation alone, guarantee alpha, replace market microstructure models, or establish AGI. A successful discovery need not be a profitable trading strategy: improved anomaly explanation, risk prediction, or data-quality diagnosis may also be valid outcomes when evaluated against a declared objective.

## 2. Experimental Architecture

```text
Licensed / permitted point-in-time market data
    |-- prices, volume, corporate actions, fundamentals, sector/index data
    v
Ingestion + temporal provenance + data-quality gates
    v
WE-SIO object fabric (instrument / event / relation / regime / observation)
    v
Residual registry + CCC / Two-Way CCC / Pattern Trigger discovery
    v
Opportunity localization and budgeted hypothesis generation
    v
CDE candidate evolution + OCSRE reasoning in isolated sandboxes
    v
Independent validation + statistical and operational risk gates
    |-- reject / archive / relay negative evidence
    |-- replicate / register validated knowledge
    v
Paper decisions or approved research actions
    v
Feedback, drift monitoring, retirement, and capability relay
```

A control plane allocates compute, enforces temporal and access boundaries, and prevents research-side feedback from contaminating held-out evaluation data.

## 3. WE-SIO Market Object Model

At minimum, the following objects have stable identities and versioned states:

| Object | Representative fields | Critical semantics |
|---|---|---|
| Instrument | instrument ID, venue, listing status, currency | Stable ID across ticker changes |
| Observation | event time, available time, source, OHLCV | Point-in-time availability and adjustments |
| CorporateAction | split, dividend, merger, effective time | Prevent backward-looking adjustment leakage |
| FundamentalRecord | fiscal period, filing time, restatement | Public availability vs. reporting period |
| Relation | sector, supply chain, index membership | Time-varying membership and evidence |
| MarketRegime | volatility, liquidity, macro context | Estimated, uncertain, not oracle-labeled |
| Residual | mismatch, expected state, evidence | Origin, version, confidence, lifecycle |
| DiscoveryCandidate | hypothesis, scope, trigger, tests | Immutable hypothesis registration |
| Delta | proposed operator or policy change | Preconditions, sandbox, rollback |
| Capability | validated transformation or trigger | Contract, provenance, domain limits |

Object identities must not be inferred solely from ticker strings. All joins and features must respect `available_at`, not merely observation or fiscal dates. Missing, delayed, corrected, and delisted observations are represented explicitly.

### 3.1 Illustrative record

```yaml
object_id: equity:example-001
object_type: MarketInstrument
state_version: 27
as_of: 2026-10-30T20:00:00Z
observations:
  - feature: daily_volume
    observed_at: 2026-10-30T20:00:00Z
    available_at: 2026-10-30T20:01:00Z
    source_id: feed-A
residual_refs: [residual:example-014]
capability_refs: [capability:liquidity-anomaly-v1]
permissions: [research_read]
```

All identifiers and values above are illustrative, not actual market observations.

## 4. Residual-First Discovery

Residuals may describe forecast errors, unexplained co-movement, regime breaks, cross-source disagreement, relation inconsistencies, risk-model failures, or capability gaps. A residual is a *typed, evidenced record*, not automatically a trading opportunity.

Minimum record:

```yaml
residual_id: residual:example-014
origin_object: equity:example-001
residual_type: unexplained_volume_shift
observed_at: 2026-10-30T20:00:00Z
available_at: 2026-10-30T20:01:00Z
reference_model_version: volume-baseline-v3
magnitude_definition: standardized_log_volume_difference
uncertainty: {method: rolling-bootstrap, status: pending}
source_evidence: [feed-A:record-123]
status: candidate
candidate_tests: [sector-adjustment, event-study, regime-split]
```

Residual retention is selective: deduplicate related events, track storage and compute costs, enforce retention policies, and preserve negative or failed tests as evidence. A budget-aware priority score may combine expected information gain, practical value, reliability, latency, and cost; the score must not be treated as a calibrated probability without validation.

## 5. CCC, Two-Way CCC, and Pattern Triggering

The lab treats CCC as a candidate structural relationship mechanism and Two-Way CCC as a bidirectional conditional-evidence process. Operational definitions and thresholds must be fixed in a registered protocol before the held-out test.

**Illustrative hypothesis:** An abnormal liquidity residual in one instrument precedes a temporary increase in sector-wide spread volatility, conditional on sector, market regime, and announcement timing. The reverse conditional direction is tested separately rather than inferred from the forward relationship.

Discovery stages:

1. Generate a typed candidate from observed residuals and relations.
2. Record directional conditions, lag windows, and eligible objects.
3. Compare against null models and common confounders.
4. Test both conditional directions when claiming Two-Way CCC.
5. Check stability across time, assets, regimes, and data providers.
6. Register a Pattern Trigger only after independent validation.
7. Monitor degradation and retire invalidated triggers.

A trigger is a reproducible predicate with an explicit action policy. Trigger firing alone does not authorize an order or other consequential action.

## 6. CDE and OCSRE Evolution Loop

CDE generates constrained candidate changes to features, relation hypotheses, trigger thresholds, search operators, and discovery strategies. OCSRE evaluates these changes in object context with evidence, cost, and governance constraints.

```text
observe → retain residual → localize opportunity → propose delta
       → check preconditions → sandbox test → independent validate
       → reject / register / relay → monitor → revise or retire
```

**Hard rules:** A candidate must declare its parent state, changed components, constraints, evidence, evaluation version, and rollback path. Path-memory and loop-control rules prevent uncontrolled replay. A model or evaluator may be evolved in the research sandbox, but it cannot grade its own promotion on a newly modified standard. Holdout ownership and evaluation policies remain externally controlled.

## 7. Preregistered Hypotheses

| ID | Hypothesis | Primary discriminating evidence |
|---|---|---|
| SPH-001 | WE-SIO reduces point-in-time and semantic mapping errors | Error rate under matched ingestion tasks |
| SPH-002 | Structured residual retention improves useful discovery yield | Validated discoveries per compute-hour |
| SPH-003 | Two-Way CCC adds signal beyond unidirectional and conventional conditional models | Held-out incremental predictive value |
| SPH-004 | CDE operator evolution improves discovery efficiency | Independent test performance at equal budget |
| SPH-005 | Persistent discovery detects regime change earlier | Detection delay at fixed false-alarm rate |
| SPH-006 | Capability Relay transfers discoveries with less redevelopment | Cross-dataset replication rate and adaptation cost |
| SPH-007 | Integrated architecture yields net practical value | Risk-adjusted utility after full costs and uncertainty |

Each hypothesis requires a predeclared minimum effect size, confidence or uncertainty method, test window, stopping rule, and rejection criterion. Failure to meet thresholds is reported as failure or inconclusive evidence, never reframed as confirmation.

## 8. Baselines and Ablations

| Group | Configuration | Purpose |
|---|---|---|
| B0 | Simple buy-and-hold or passive benchmark where applicable | Economic reference, not a discovery-system comparator |
| B1 | Fixed statistical features + preregistered tests | Conventional analysis baseline |
| B2 | Streaming anomaly detection + fixed triggers | Reactive continuous-monitoring baseline |
| B3 | Online learning / rolling retraining | Adaptive-model baseline |
| B4 | AutoML or adaptive search with equivalent compute budget | Automated-discovery baseline |
| B5 | WE-SIO without residual registry | Isolate object modeling |
| B6 | WE-SIO + residual registry, no CDE | Isolate residual retention |
| B7 | Full WE-SIO + CCC + CDE/OCSRE + Relay | Integrated hypothesis |
| B8 | Full system without Two-Way CCC or Relay | Component ablation |

All groups receive the same eligible information and comparable total resource budgets, including research, data engineering, inference, and review costs. Comparators must be tuned fairly on training/validation data without access to the final holdout.

## 9. Data Protocol and Leakage Prevention

1. Use licensed, timestamped, point-in-time data; document redistribution rights.
2. Include delisted securities and historically accurate universe membership to avoid survivorship bias.
3. Respect filing/publication latency, corporate-action effective times, revisions, and ticker histories.
4. Use chronological train/validation/test splits, rolling-origin evaluation, and purged/embargoed splits when labels overlap.
5. Lock the final holdout and restrict access until candidate selection is complete.
6. Log every tested candidate, including failed tests, to address selection bias and multiple comparisons.
7. Correct for multiple testing with a prespecified method (e.g., false discovery rate controls, reality-check style procedures, or a suitable sequential-testing design).
8. Repeat on independent time periods, market regimes, and—where feasible—data vendors.
9. Preserve event-time vs. knowledge-time distinctions throughout joins and backtests.
10. Treat historical revisions and provider outages as explicit stress cases.

The choice of statistical correction depends on the dependence structure and testing process; no single correction is universally sufficient.

## 10. Execution and Economic Evaluation

A predictive relationship is not automatically economically exploitable. Paper trading must include realistic bid–ask spreads, commissions, slippage, market impact, turnover, liquidity, borrowing or short-sale constraints where relevant, and capacity limits. Use conservative scenario bands rather than a single optimistic cost estimate.

Report separately:

- Predictive metrics: calibration, discrimination, effect stability, false-discovery rate.
- Discovery metrics: independently validated findings per compute-hour, time to validation, replication rate.
- Economic metrics: net return, risk-adjusted performance, drawdown, turnover, exposure, capacity, and uncertainty intervals.
- Operational metrics: ingestion latency, mapping errors, memory footprint, review time, and failure recovery.
- Evolution metrics: improvement in subsequent discovery quality on new data, operator survival, and rate of retired capabilities.

Use robust confidence intervals or resampling that accounts for time dependence. Evaluate economic utility against appropriate market, factor, and transaction-cost baselines; do not infer causality or sustainable alpha from backtest significance alone.

## 11. Opportunity Localization and Resource Governance

Opportunity candidates are registered with source objects, supporting residuals, expected value, uncertainty, estimated compute cost, and an expiration condition. The scheduler allocates a bounded budget across exploitation, replication, exploration, and negative-result review. A reserve for exploration prevents the system from reinforcing only previously rewarded patterns.

Stop or suspend a search branch when data quality is insufficient, test budget is exhausted, evidence is non-reproducible, or risk controls fail. Record the leftover unresolved hypothesis for later Relay.

## 12. Security, Integrity, and Action Boundaries

ASSI-inspired safeguards include provenance checks, permission-scoped plugins, sandbox isolation, signed or hash-addressed experiment artifacts, immutable evaluation records, and adversarial-data tests. No discovery component may silently change source observations, bypass an independent evaluator, or promote a strategy to live execution.

Any move beyond paper evaluation requires explicit human approval, risk limits, kill-switch design, operational monitoring, and applicable regulatory/compliance review. Research findings should not be presented as investment advice.

## 13. Conformance Tests

| Test | Expected result |
|---|---|
| CT-001 | Historical ticker rename | Identity remains consistent |
| CT-002 | Delisted-security replay | Universe retains eligible delisted members |
| CT-003 | Late filing revision | No pre-publication feature leakage |
| CT-004 | Adjusted-price replay | Corporate actions are temporally correct |
| CT-005 | Out-of-order feed event | State history remains auditable |
| CT-006 | Missing observation | Explicit missingness; no fabricated values |
| CT-007 | Residual provenance audit | Full evidence and baseline traceability |
| CT-008 | Bidirectional CCC test | Both directions tested independently |
| CT-009 | Duplicate hypothesis detection | Repeated tests counted and budgeted |
| CT-010 | Holdout access attempt | Unauthorized access denied and logged |
| CT-011 | Delta rollback | Prior state reproducibly restored |
| CT-012 | Trigger degradation | Trigger retired or downgraded |
| CT-013 | Cost shock | Economic utility recomputed conservatively |
| CT-014 | Cross-universe relay | Local revalidation required |
| CT-015 | Evaluation-rule modification | External approval and separate test required |

## 14. Experimental Phases and Exit Gates

**E0 — Protocol and dataset audit.** Deliver data dictionary, licensing record, historical universe, time semantics, preregistration, and locked holdout. *Gate:* no unresolved critical leakage path.

**E1 — Object and residual conformance.** Implement minimal WE-SIO records, CDC/stream replay, and provenance-preserving residual registry. *Gate:* pass applicable CT-001–007.

**E2 — Baseline discovery.** Run B1–B4 with fixed budgets and document false positives, costs, and latency. *Gate:* reproducible baseline reports.

**E3 — Structural discovery.** Evaluate CCC, Two-Way CCC, and residual-guided opportunity localization without evolving the evaluator. *Gate:* preregistered evidence on locked test windows.

**E4 — CDE/OCSRE evolution.** Permit bounded operator evolution in sandbox, with ablations and independent testing. *Gate:* measurable benefit or explicit negative finding.

**E5 — Paper decisions and Relay.** Run realistic cost-aware paper evaluation, independent replication, capability packaging, and retirement monitoring. *Gate:* publish complete results, including null findings and deployment restrictions.

A failed gate does not invalidate the research program; it blocks promotion of unsupported claims.

## 15. Deliverables and Reproducibility Package

Each completed run should produce:

```text
runs/<run-id>/
  protocol.yaml
  dataset-manifest.yaml
  code-and-environment-lock.yaml
  object-schema-version.yaml
  candidate-registry.jsonl
  residual-registry.jsonl
  delta-and-operator-history.jsonl
  evaluation-results.json
  costs-and-resource-ledger.csv
  leakage-and-integrity-audit.md
  negative-results.md
  capability-relay-package.yaml
  reproduction-instructions.md
```

If underlying market data cannot be redistributed, publish a synthetic fixture, dataset acquisition instructions, schema, code, hashes, and executable conformance tests within licensing constraints. A relay package must disclose domain limits, performance uncertainty, evidence status, known failure modes, and required local validation.

## 16. Failure Modes and Falsification

The program must explicitly watch for: data snooping; nonstationary effects; correlated multiple tests; selection bias; hidden vendor revisions; survivorship bias; unrealistic fills; crowding and market impact; evaluator overfitting; noncausal relationships; residual registry explosion; semantic mapping drift; and false claims of cross-market transfer.

A finding is **not validated** if its apparent benefit disappears on locked holdout, after realistic costs, or after appropriate multiple-testing adjustment; if it cannot be independently reproduced; or if required data provenance is unavailable. Where the evidence is insufficient, report *inconclusive* rather than forcing a binary result.

## 17. Open Research Questions

1. Which residual types yield the highest independently validated discovery rate per unit cost?
2. How should opportunity localization balance exploration, replication, and near-term utility?
3. When does Two-Way CCC add information beyond conditional dependence or causal-inference baselines?
4. Can discovery operators evolve without contaminating future evaluations?
5. Which WE-SIO abstractions remain stable across vendors and asset classes?
6. How rapidly do discovered triggers decay under market adaptation?
7. Can a capability transfer to a new market regime with less tuning than a conventional model?
8. What evidence would distinguish genuine discovery-mechanism improvement from increased search budget?
9. When is local in-situ computation preferable to centralized batch processing?
10. How should negative and inconclusive results be packaged for Collective Learning?

## 18. Integration with the Research Program

- **ASSI:** provenance, adversarial inputs, permissions, and evaluation integrity.
- **D-BTP:** directional candidate generation, branching, and hypothesis paths.
- **CDE:** constrained Delta semantics, adaptive operators, path memory, and rollback.
- **WE-SIO:** persistent market objects, typed relations, and plugin contracts.
- **OCSRE:** object-centered reasoning, in-situ learning, and governed evolution.
- **SPEC-001:** Object–Residual–Delta interfaces.
- **SPEC-002:** persistent discovery loop.
- **SPEC-003:** independent validation and Relay contracts.
- **EXP-001:** SQL/CDC structural discovery baseline.
- **EXP-002:** dynamic scheduling as a lower-ambiguity structural evolution test bed.

### Foundational repositories

1. [Adversarial Structural Security Intelligence (ASSI)](https://github.com/sizhet/Adversarial-Structural-Security-Intelligence)
2. [Dynamic Bucket Tree of Permutation (D-BTP)](https://github.com/sizhet/Dynamic-Bucket-Tree-of-Permutation-and-Directional-Structural-Evolution)
3. [Constrained Delta Evolution (CDE)](https://github.com/sizhet/Constrained-Delta-Evolution)
4. [World Entity and Structural Intelligence Operations (WE-SIO)](https://github.com/sizhet/World-Entity-and-Structural-Intelligence-Operations)
5. [Object-Centric Structural Reasoning and Evolution (OCSRE)](https://github.com/sizhet/Object-Centric-Structural-Reasoning-and-Evolution)

## 19. Closing Research Position

The Stock Pattern Lab is designed to test a strong claim under difficult conditions: a persistent structural discovery system may be more valuable than a sequence of isolated predictions if it improves the reproducible discovery process itself. This remains a hypothesis. The laboratory's scientific contribution is to make that hypothesis measurable, falsifiable, cost-aware, and relayable—including when the results are negative.

**Core principle:** *Discover, validate, account for costs, preserve failures, and relay only what the evidence supports.*
