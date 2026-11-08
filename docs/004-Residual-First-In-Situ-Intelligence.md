# 004 — Residual-First and In-Situ Structural Intelligence

## From Computational Boundary Loss to Persistent Local Reasoning, Learning, Decision, and Evolution

**Status:** Research synthesis, architectural proposal, and falsifiable hypotheses  
**Series:** Beyond Static Computation — Five DOI Peaks  
**Version:** 0.1.0 (research draft)  
**Date:** 2026-11-08

> **Central thesis.** A residual should not be treated solely as a disposable numerical error or a terminal failure report. In suitable systems, a residual can become a typed, persistent, first-class computational object that locates unfinished work, triggers situated reasoning, guides constrained delta generation, supports learning, and relays validated discoveries. *Residual-first* specifies an attention and organization principle; *in-situ intelligence* specifies a locality and continuity principle. Their conjunction is a research hypothesis, not a demonstrated universal superiority claim.

## Abstract

Computational pipelines routinely summarize discrepancies, failed constraints, unexplained observations, and capability gaps into scalar losses, status codes, or discarded candidates. This compression is often useful and sometimes necessary, but it can erase structure relevant to later discovery and adaptation. The five-repository progression—Adversarial Structural Security Intelligence (ASSI), Dynamic Bucket Tree of Permutation (D-BTP), Constrained Delta Evolution (CDE), World Entity and Structural Intelligence Operations (WE-SIO), and Object-Centric Structural Reasoning and Evolution (OCSRE)—suggests a different architectural possibility: retain selected residuals as durable, evidence-bearing objects associated with persistent world entities; use them to allocate attention, select capabilities, generate constrained changes, validate improvements, and propagate reusable results through Relay. This paper defines residual types and lifecycle contracts, distinguishes logical locality from physical execution, examines CCC, Two-Way CCC, and Pattern Triggering as candidate discovery mechanisms, and proposes comparative experiments. It addresses noise, selection bias, evaluator drift, feedback loops, security, and resource limits. The proposed contribution is an interoperable *residual-native* design pattern, not the invention of error-driven learning or online computation.

**Keywords:** residual-first; residual-native computing; in-situ intelligence; object-centric reasoning; WE-SIO; CDE; OCSRE; localization; structural learning; continual discovery; relay.

---

## 1. Why Residuals Deserve First-Class Attention

In many computational systems, the principal output is the solution, prediction, decision, or updated state. What remains unexplained is logged, averaged, dropped, or passed to a separate diagnostic workflow. Yet the remainder can carry information about a model's inadequacy, a violated constraint, a newly emerging relation, a missing capability, or an evaluator disagreement.

Consider four familiar cases:

1. A forecasting model reports an error but loses the context in which similar errors recur across related entities.
2. An optimizer discards infeasible candidates without preserving the specific constraint interactions that made them infeasible.
3. A data pipeline reports a schema mismatch while omitting the semantic difference that could reveal a new entity type.
4. An agent completes a task but leaves unresolved uncertainty that no later component can locate or revisit.

None of these examples proves that retaining more information is always beneficial. They motivate a narrower question: **when does preserving the structure of unresolved differences enable discoveries that conventional result-centric workflows would miss, delay, or reproduce at greater cost?**

The proposed answer is to make selected residuals addressable, typed, versioned, and actionable—without making every discrepancy permanent or important.

## 2. The Five DOI Peaks and the Residual Question

The following research lineage motivates the synthesis; it is not an assertion of experimental validation.

| Repository | Relevant contribution to residual-first in-situ intelligence |
|---|---|
| **ASSI** | Changing identities, evidence, incentives, and adversarial conditions require preserving unresolved and conflicting evidence, not merely issuing a final classification. |
| **D-BTP** | Directional candidate generation and path memory create opportunities to retain rejected hypotheses and informative search differences. |
| **CDE** | State containers, admissible deltas, constraints, and evaluation supply a formal setting for acting on residuals. |
| **WE-SIO** | Persistent object identity, state, relations, and Core Frame/Plugins provide a potential substrate for local residual registries and capability dispatch. |
| **OCSRE** | Object-centric reasoning, differential computation, in-situ learning, and capability evolution provide an integration path. |

The earlier Structural Intelligence Framework (SIF) supplies localization and addressing; Scoring/Control Plane mechanisms prioritize work; AQSI supplies autonomous questioning; Relay and Collective Learning offer a path for carrying validated results beyond their originating object.

The new point of convergence is **not** that these components each contain residuals. It is that residuals may organize a *persistent computational loop* across representation, detection, candidate generation, evaluation, learning, and capability reuse.

## 3. The Problem of Computational Boundary Loss

### 3.1 “Cut-cloth computation” as a research metaphor

The phrase *cut-cloth computation* describes a recurring architectural tradeoff: a rich evolving situation is cut into bounded tasks and interfaces, and each task exports only a narrow answer. The metaphor is not an argument against modularity. Modularity, abstraction, and compression are indispensable for reliability and performance.

The failure mode arises when a boundary discards information that would have been valuable for a later inference or decision. We call this **computational boundary loss**.

Examples include lost provenance, collapsed uncertainty, unrecorded rejected candidates, discarded constraint conflicts, and missing links between an error and its originating object or temporal context.

### 3.2 Boundary-loss hypothesis

Let a computation produce a result \(y\) and contextual remainder \(r\):

\[
F(x,c) \longrightarrow (y,r).
\]

A result-only interface transmits \(y\). A residual-aware interface may preserve a selected, compressed representation \(\hat r\) with provenance and explicit uncertainty. The testable question is whether downstream utility improves enough to justify storage, indexing, privacy, and compute costs.

This is **not** a claim that all discarded intermediate states should be retained. An effective system needs selective retention, summarization, expiry, and deletion contracts.

## 4. A Typed Residual Ontology

A residual is an *unclosed, evidence-bearing relation* between an observation or current state and some expectation, constraint, explanation, capability, or evaluation requirement. Not every residual is numeric, and different residual types should not be forced into one scalar.

| Type | Residual relation | Example | Candidate response |
|---|---|---|---|
| **Prediction** | Observed versus predicted | Recurrent forecast miss | Recalibrate or revise model |
| **Constraint** | Current or candidate state versus admissibility | Route exceeds time window | Generate feasible delta |
| **Explanation** | Evidence versus current hypothesis | Unexplained cross-object behavior | Generate competing hypotheses |
| **Capability** | Task requirement versus available operators | Missing temporal join | Discover or build plugin |
| **Evaluation** | Conflicting or insufficient assessments | Two scorers disagree | Request independent test |
| **Relational** | Expected versus observed object relation | New dependency appears | Update relation hypothesis |
| **Governance** | Proposed action versus authorization or safety contract | Unapproved capability escalation | Block, audit, or escalate |

A residual should declare its comparison basis. An unexplained observation without a defensible expectation may be an *observation requiring investigation*, not yet a well-defined residual. This distinction prevents the residual category from swallowing all data.

### 4.1 Minimum residual contract

```yaml
Residual:
  residual_id: immutable_identifier
  object_ref: stable_object_identifier
  object_version: version_or_snapshot
  kind: prediction | constraint | explanation | capability | evaluation | relational | governance
  observation_ref: evidence_or_event_reference
  comparison_basis: expectation_constraint_or_hypothesis_ref
  discrepancy: typed_value_or_structured_relation
  temporal_scope: event_and_validity_window
  provenance: source_and_transformation_chain
  uncertainty: calibrated_or_qualified_estimate
  severity: domain_specific_priority
  actionability: candidate_actions_or_none
  status: observed | triaged | hypothesized | tested | resolved | retired
  access_policy: visibility_and_retention_contract
```

This is a *candidate interoperability schema*, not a finalized WE-SIO specification. Fields such as severity and uncertainty must retain their domain-specific meaning; their numerical values are not universally comparable.

### 4.2 Residual as a WE-SIO object

A residual can itself be represented as an object with identity, links, history, evidence, and capabilities. This supports residual-to-residual relationships: recurrence, contradiction, shared cause, temporal sequence, or partial explanation. The resulting graph can generate higher-order questions without treating every cluster as a meaningful pattern.

## 5. Residual-First Is Not Residual-Only

*Residual-first* is a principle for **attention, prioritization, and follow-up**, not a requirement to replace normal data processing, objectives, or baseline computation.

The architecture must preserve:

- ordinary successful computations and stable operating modes;
- exploration of apparently normal states, since novel opportunities need not originate in visible errors;
- externally defined objectives and constraints;
- independent evaluations that do not reward merely making a residual score smaller.

A system that only hunts for residuals can become blind to quiet opportunities, self-created errors, and changing goals. Residual attention must therefore coexist with baseline monitoring, randomized exploration, and externally grounded task value.

## 6. In-Situ Intelligence: Locality, Continuity, and Ownership

**In-situ** means that reasoning and learning remain *logically anchored* to the relevant object, relation, state transition, and evidence history. It does **not** mean every computation runs physically inside a database row or on the same machine as the data.

A WE-SIO object may invoke a remote SQL engine, GPU service, optimization solver, or LLM plugin while maintaining:

1. stable identity and state-version linkage;
2. a record of the evidence and assumptions used;
3. explicit capability and authorization contracts;
4. attribution of results and residuals to the originating context;
5. validation before durable state or capability updates.

This distinction allows *object-local semantics with distributed execution*.

### 6.1 Four in-situ functions

**In-situ computation:** evaluate relevant functions against a versioned object state, using cached context and incremental updates when beneficial.

**In-situ learning:** update local models or statistics from a continuous history of evidence and residuals, with safeguards against drift and leakage.

**In-situ decision:** select bounded actions under object-specific constraints, risk limits, and approval requirements.

**In-situ evolution:** propose and test changes to state, relationships, plugins, heuristics, or candidate generators without silently rewriting the evaluator that judges them.

These functions can be deployed separately. A read-only observer is a legitimate first implementation; autonomous actuation is not required.

## 7. From Reactive Response to Persistent Structural Presence

The metaphor “wherever the cloud rains, I am there” expresses a goal of *persistent opportunity coverage*. It should not be interpreted as infinite sensors, universal prediction, or guaranteed advantage.

A reactive pipeline waits for a declared task or alert, reconstructs context, selects a tool, and produces a response. A persistent structural observer maintains relevant entity histories and candidate relationships, notices changes, and dispatches targeted computation without requiring every question to be manually restated.

Three potential sources of advantage are distinguishable:

| Advantage | Mechanism | Measurement |
|---|---|---|
| **Latency** | Less delay between meaningful change and useful response | Detection-to-decision time at fixed false-alert rate |
| **Context** | Preserved object history, relations, and residual provenance | Validated discovery yield at matched information access |
| **Learning** | Reusable patterns, strategies, and plugins | Out-of-sample improvement across tasks and time |

These advantages are hypotheses. They must be evaluated against strong streaming, incremental, and online-learning baselines, not merely against a batch-only system.

### 7.1 Selective presence rather than unlimited coverage

A scalable system maintains low-cost broad observation and concentrates expensive reasoning where expected value warrants it. A candidate attention score might be:

\[
A_i = \frac{\mathbb E[\Delta U_i] + \lambda\,\mathbb E[IG_i] - \rho\,Risk_i}{Cost_i+\epsilon},
\]

where \(\Delta U_i\) is incremental task utility, \(IG_i\) is information gain, and risk and cost are calibrated to the domain. This formula is illustrative, not a universal scoring law. Exploration quotas, uncertainty bounds, fairness constraints, and mandatory safety checks can override its ranking.

**Logical coverage can be broad while intensive computation remains selective.** This reconciles the ambition of persistent presence with finite resources.

## 8. The Residual-to-Delta-to-Learning Loop

A proposed minimal loop is:

```text
Versioned WE-SIO Object / Event Stream
                |
                v
       Residual Detection
                |
                v
     Typing + Provenance + Triage
                |
                v
   Localization + Capability Selection
                |
                v
  CCC / Two-Way CCC / Pattern Candidates
                |
                v
      CDE Delta / Hypothesis Generation
                |
                v
  OCSRE Sandbox + Independent Evaluation
                |
          +-----+-----+
          |           |
       Reject       Validate
          |           |
   Retain evidence    v
                  Controlled Commit
                       |
                       v
            Object Update / Relay Registry
                       |
                       +----> Subsequent observation
```

The arrows describe a governance loop, not a requirement that every event pass through all stages. Lightweight observations may be aggregated; some residuals may expire; some discoveries may require human review.

### 8.1 A constrained transition

For object state \(S_t\), residual set \(R_t\), and candidate delta \(\delta_t\):

\[
\delta_t \in G(S_t,R_t,H_t), \qquad
S_{t+1}=T(S_t,\delta_t)
\]

subject to explicit feasibility and authority checks:

\[
C(S_t,\delta_t)=\mathrm{true}, \qquad
V(S_t,\delta_t,E_t)\geq \tau.
\]

Here \(G\) is a generator, \(H_t\) is path/history memory, \(C\) is a constraint predicate, and \(V\) is an independently governed validation process. If evaluator \(E_t\) itself changes, the change must be tested against a held-out or external reference. Rejected deltas should retain useful evidence, not be promoted as successful learning.

### 8.2 Avoiding recursive self-confirmation

A system must not define success only by the residual measure that its own generator is optimizing. Use external outcomes, pre-registered tests, negative controls, independent evaluators, and rollback criteria. Where causal claims are made, require interventions or appropriately identified designs rather than correlations alone.

## 9. CCC, Two-Way CCC, and Pattern Triggering

The SI research lineage uses CCC, Two-Way CCC, and Pattern Triggering as candidate mechanisms for finding reusable structural relationships. In this synthesis, their precise formal semantics remain governed by their respective source specifications; the following are **operational roles**, not replacements for those definitions.

- **CCC discovery:** propose common structural concepts across multiple observations or objects, with explicit support and counterexamples.
- **Two-Way CCC:** test whether candidate structural relations provide informative evidence or mappings in both directions, without assuming reversibility or causality.
- **Pattern Triggering:** turn a validated, scoped relationship into an event or state-conditioned trigger for further analysis or bounded action.

A useful pipeline distinguishes **candidate pattern → replicated relation → validated trigger → deployed capability**. The two-way property must be empirically checked; a strong forward conditional does not imply an equally strong reverse conditional. All candidate mining must account for multiple testing and selection effects.

### 9.1 Illustrative SQL example

Suppose an order-processing database shows recurring fulfillment delays. A residual-aware system might preserve not only “late order” counts but object-level evidence linking warehouse, carrier, inventory changes, and time windows. It could propose a shared structural condition across orders, compare it against competing explanations, and test whether the condition predicts future delays. If validated, the result becomes a versioned monitoring trigger or scheduling recommendation.

The mere discovery of correlation is not proof of a causal mechanism or a transferable capability. Data leakage, confounding, seasonality, and operational interventions must be examined.

## 10. Core Frame, Plugins, and SQL Alignment

WE-SIO's Core Frame/Plugins separation is essential to prevent the residual-first proposal from becoming a monolithic intelligence engine.

**Core Frame responsibilities:** identity, state/version references, relationships, residual registry hooks, provenance, event subscriptions, permissions, capability discovery, and commit/rollback contracts.

**Plugin responsibilities:** SQL/CDC adapters, temporal analytics, graph reasoning, statistical tests, solvers, CDE generators, LLM reasoning, evaluators, and domain-specific actuators.

SQL alignment should be treated at three distinct levels:

1. **Structural:** tables, rows, columns, keys, types, and joins map to entity and relation references.
2. **Semantic:** units, event time, missing values, lineage, and domain constraints are preserved.
3. **Operational:** change-data capture, transaction boundaries, incremental queries, consistency, and access controls remain correct.

Primitive-column alignment is a promising engineering entry point, not proof that every column is a complete semantic primitive. The system should push computation into existing databases when appropriate and avoid needless replication of sensitive data.

## 11. Governance: Residual Attention, Cost, and Safety

Persistent observation can create substantial costs and risks. A credible architecture must specify:

- **Triage and retention:** deduplicate, summarize, expire, and delete low-value residuals; retain negative evidence when scientifically useful.
- **Budgets:** enforce per-object, per-plugin, and global limits on compute, memory, event volume, and exploration.
- **Isolation:** execute generated hypotheses and code in sandboxed environments with least-privilege access.
- **Versioning:** preserve the source snapshot, feature definitions, evaluator version, and model version for each claimed discovery.
- **Actuation controls:** separate observation, recommendation, simulation, and real-world action permissions.
- **Adversarial resilience:** handle poisoned events, forged identities, manipulated provenance, and feedback-induced behavior changes.
- **Human and external oversight:** use independent review for high-impact changes and self-modifying evaluation rules.

In security-sensitive systems, some residuals may expose confidential information or sensitive behavioral patterns. Persistence must never be assumed to justify unrestricted collection or sharing.

## 12. Failure Modes and Counterarguments

### 12.1 Noise accumulation

Persistent residuals can become an unbounded graveyard of false alerts. Mitigation: calibrated thresholds, expiry, deduplication, hierarchical summarization, and explicit measurement of discovery yield per resource unit.

### 12.2 Rediscovering known methods

Error-driven learning, continual learning, event-driven systems, active learning, incremental computation, and observability already implement parts of the proposal. The research claim must concern the **joint object–residual–delta–validation–relay contract**, not novelty of each constituent technique.

### 12.3 Locality can trap exploration

An in-situ system may overfit to local history and miss global patterns. Mitigation: cross-object comparison, exploration budgets, counterfactual probes, and periodic global evaluation.

### 12.4 Feedback can manufacture its own evidence

A deployed trigger changes behavior, which changes the observations used to validate the trigger. Mitigation: intervention logs, control cohorts, off-policy evaluation when appropriate, and separate pre- and post-deployment metrics.

### 12.5 Evaluator gaming

A generator may minimize the measured residual while degrading actual utility. Mitigation: independently specified objectives, locked benchmarks, multi-perspective scoring, and explicit change control for evaluators.

### 12.6 Persistent systems are not automatically intelligent

Continuous monitoring plus automation does not establish intelligence emergence. Evidence of genuinely new, reusable capability requires stronger tests than throughput, alert count, or local error reduction.

## 13. Falsifiable Research Hypotheses

| ID | Hypothesis | Falsifying or weakening evidence |
|---|---|---|
| **RFI-H01** | Typed residual persistence improves validated discovery yield at matched compute cost. | No improvement over event logs and conventional feature stores. |
| **RFI-H02** | Object-linked residual history reduces time to diagnose recurrent failures. | Equivalent or faster diagnosis with ordinary tracing and observability. |
| **RFI-H03** | In-situ context retention improves out-of-sample decision quality under changing conditions. | Gains vanish with equalized context windows and strong online baselines. |
| **RFI-H04** | Residual-guided CDE proposes more useful feasible deltas than unguided or heuristic search. | No gain after accounting for candidate-generation overhead. |
| **RFI-H05** | CCC and Two-Way CCC discovery yield transferable triggers beyond fixed rules. | Patterns fail replication or add no net value after multiple-testing correction. |
| **RFI-H06** | Validated Relay of local discoveries improves later tasks. | Transfer performance matches independent relearning or causes negative transfer. |
| **RFI-H07** | Selective in-situ attention outperforms uniform intensive scanning at a fixed budget. | Uniform or standard adaptive monitoring performs equally well or better. |
| **RFI-H08** | The combined architecture produces gains not explained by any single component. | Ablations show all gains attributable to one conventional technique. |

Each hypothesis requires a predefined population of tasks, time horizon, resource budget, evaluation procedure, and failure threshold. “More discoveries” alone is not an adequate success metric.

## 14. Experimental Program

### Experiment A — SQL residual discovery

**Environment:** versioned relational database with CDC, synthetic seeded anomalies, and real or realistically generated operational change streams.

**Baselines:** SQL rules, incremental materialized views, streaming anomaly detection, and conventional observability with comparable access to data.

**Treatments:** typed residual registry; object-linked history; CCC candidate generation; full residual-to-delta validation loop.

**Metrics:** precision of validated discoveries, false discovery rate, time-to-detection, compute/storage cost, reproducibility, and portability of learned triggers.

### Experiment B — Dynamic school-bus scheduling

**Environment:** time windows, vehicle capacities, travel-time uncertainty, student ride-time constraints, and changing demand.

**Baselines:** static optimization, rolling-horizon reoptimization, established local-search/metaheuristics, and a CDE implementation without residual prioritization.

**Metrics:** feasible vehicle count, total travel and ride time, violation rate, reoptimization latency, and generalization to unseen demand patterns. A solution is not an improvement if it violates student or safety constraints.

### Experiment C — Financial time-series observation

**Environment:** historical and forward paper-trading data, transaction-cost models, and time-consistent feature availability.

**Baselines:** fixed statistical signals, rolling models, online learners, and event-driven strategy pipelines.

**Metrics:** out-of-sample calibration, stability across regimes, risk-adjusted net returns after fees and slippage, turnover, drawdown, and discovery false-positive rates.

**Guardrail:** research findings are not evidence of guaranteed trading advantage; use paper trading and strictly separated training, validation, and prospective test windows before considering any deployment.

### Experiment D — Cross-domain Relay

Take a residual-handling strategy or trigger-discovery plugin validated in one environment and test its transfer to another. Record adaptation effort, failed transfers, and the extent to which the reusable *contract* rather than domain-specific data drives benefit.

### 14.1 Mandatory ablations

Remove or replace, one at a time: residual persistence, object identity linkage, in-situ context, CCC discovery, CDE candidate generation, and Relay. Match compute budgets and evaluator access. Without ablation, an integrated system's performance cannot establish which architectural idea contributed value.

## 15. Open Questions

1. What is the smallest interoperable residual ontology that retains useful structure without becoming vague?
2. Which residuals should be retained, summarized, forgotten, or legally deleted?
3. When is local object context more valuable than global batch computation?
4. How should cross-object residuals be owned and versioned?
5. Can a reliable attention policy balance exploitation, exploration, and safety?
6. How can Two-Way CCC be validated without confusing conditional evidence with causal direction?
7. Which evaluator properties must remain externally fixed during self-improvement?
8. What counts as a *new capability* rather than an additional trigger or rule?
9. Under what workloads do object-centric interfaces create unacceptable overhead?
10. How should negative results and failed deltas be relayed to prevent repeated mistakes?
11. How can an in-situ system discover opportunities without first observing a measurable failure?
12. What evidence would justify calling persistent structural discovery an emergent intelligence mechanism?

## 16. Conclusions: The Residual as a Place to Continue Thinking

The strongest claim of residual-first in-situ intelligence is architectural: **a useful remainder should be allowed to remain attached to its originating world, with sufficient evidence, identity, and executable context for future work to continue there.** This changes the lifecycle of a computation. Completion no longer requires the disappearance of all unfinished structure; selected residuals become organized starting points for subsequent reasoning, learning, and constrained evolution.

WE-SIO offers a candidate object substrate; SIF provides localization; CDE provides disciplined delta transitions; OCSRE coordinates reasoning and learning; Scoring/Control Plane mechanisms allocate attention; Relay carries validated knowledge onward. The architecture could support persistent discovery across SQL systems, scheduling, financial data, and other evolving domains—but its comparative advantage remains to be demonstrated.

The practical research program is therefore to preserve the structure of unfinished work **selectively**, validate its downstream value **independently**, and make successful discoveries **reusable**. This provides a concrete bridge from the five DOI peaks to the next article on persistent structural discovery and the proposed “intelligence fishing” laboratory.

---

## Source Repositories and Research Lineage

The following are the five primary repositories in the synthesis. Their links identify the research lineage; this document does not claim that all hypotheses above are already implemented or experimentally verified in those repositories.

1. **ASSI — Adversarial Structural Security Intelligence:** https://github.com/sizhet/Adversarial-Structural-Security-Intelligence
2. **D-BTP — Dynamic Bucket Tree of Permutation:** https://github.com/sizhet/Dynamic-Bucket-Tree-of-Permutation-and-Directional-Structural-Evolution
3. **CDE — Constrained Delta Evolution:** https://github.com/sizhet/Constrained-Delta-Evolution
4. **WE-SIO — World Entity and Structural Intelligence Operations:** https://github.com/sizhet/World-Entity-and-Structural-Intelligence-Operations
5. **OCSRE — Object-Centric Structural Reasoning and Evolution:** https://github.com/sizhet/Object-Centric-Structural-Reasoning-and-Evolution

**Related SI lineage:** Structural Intelligence Framework (SIF), Scoring/Control Plane, Autonomous Questioning Structural Intelligence (AQSI), UIERU/Relay, and Collective Learning.

**Next in series:** `005-Persistent-Structural-Discovery.md` — persistent observation, CCC/Two-Way CCC discovery, pattern-triggered hypothesis generation, controlled opportunity capture, and the Structural Emergence Fishing Laboratory.
