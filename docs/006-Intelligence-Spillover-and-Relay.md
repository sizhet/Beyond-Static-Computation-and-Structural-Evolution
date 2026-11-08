# 006 — Intelligence Spillover and Relay

## From Object-Native Structural Capabilities to Cross-Domain Engineering, Validated Transfer, and Collective Learning

**Status:** Research synthesis, architectural proposal, and falsifiable research program  
**Series:** Beyond Static Computation — Five DOI Peaks  
**Version:** 0.1.0 (research draft)  
**Date:** 2026-11-08

> **Central thesis.** The most consequential possible outcome of the ASSI → D-BTP → CDE → WE-SIO → OCSRE research sequence is not a universal algorithm that solves every task. It is an open, governed mechanism through which representations, residuals, discovery methods, evaluation contracts, and verified capabilities can move between tasks and domains. *Intelligence spillover* is the generation of useful capability beyond the original task boundary; *Relay* is the disciplined handoff that makes such capability inspectable, reproducible, and improvable by others. Neither transfer nor its economic value should be assumed: both require evidence.

## Abstract

Research systems frequently develop valuable local techniques that remain trapped in their originating task, implementation, or research group. This article investigates whether object-native representations, constrained structural evolution, residual-first computation, and persistent discovery can reduce the cost of transferring those techniques across domains. It synthesizes five connected research programs: Adversarial Structural Security Intelligence (ASSI), Dynamic Bucket Tree of Permutation (D-BTP), Constrained Delta Evolution (CDE), World Entity and Structural Intelligence Operations (WE-SIO), and Object-Centric Structural Reasoning and Evolution (OCSRE). It distinguishes representational, computational, learning, discovery, and organizational spillover; proposes a Core Frame/Plugin/Contract transfer model; specifies capability packages and a staged Relay protocol; and outlines tests across SQL change data, scheduling, security analysis, financial time series, and AI-generated code governance. The proposed approach does not presume that structural uniformity guarantees semantic transfer. Its central empirical question is whether independently validated capabilities can be transferred, adapted, and improved more reliably and economically than with strong conventional baselines. Collective Learning is treated as an evidence-bearing, governed process rather than a slogan for unrestricted sharing.

**Keywords:** intelligence spillover; capability relay; collective learning; WE-SIO; CDE; OCSRE; residual-first; object-native intelligence; structural transfer; reusable contracts; conformance; provenance; cross-domain validation.

---

## 1. Why a Sixth Article Is Necessary

The preceding five articles in this synthesis series establish a progression: observe the five research peaks; consider WE-SIO as a durable object and capability substrate; examine structural evolution computation; elevate residuals and in-situ intelligence; and propose persistent structural discovery. A remaining question is decisive: **what can leave the original system and remain useful elsewhere?**

A discovery that works only in one dataset may be valuable but is not yet a generalizable capability. A Plugin that can be called by another program is interoperable but not necessarily semantically transferable. A theory that can be read by another researcher has been communicated but not necessarily verified. This article treats these as distinct stages of Relay.

The research motivation is practical. Many intelligence-related advances are expensive to rediscover because they are entangled with private state, implicit assumptions, undocumented metrics, or a single team's workflow. If the structural parts of a discovery can be isolated and their assumptions made explicit, downstream researchers may be able to reuse or challenge them without recreating the entire originating system.

The ambition is **open-ended, evidence-preserving transfer**, not an assertion of unlimited general intelligence.

## 2. Five Research Peaks as Complementary Sources of Transfer

| Research program | Transferable structural contribution | Transfer limitation to test |
|---|---|---|
| **ASSI** | Changing identities, evidence, authority, adversarial dependencies, compositional subjects | Security evidence may be incomplete, manipulated, or unsafe to expose |
| **D-BTP** | Dynamic candidate generation, directional search, branching, path constraints | Candidate and path semantics may be highly domain-specific |
| **CDE** | State containers, Delta transitions, constraints, loop-back governance, adaptive branching | A valid Delta in one domain may not be meaningful in another |
| **WE-SIO** | Persistent entities, typed state, relations, Core Frame, extensible Plugins | Shared object interfaces do not imply shared ontology or causal meaning |
| **OCSRE** | Object-centric reasoning, in-situ computation and learning, capability evolution | Self-modifying strategies and evaluators require independent oversight |

The five are not a completed, integrated runtime by virtue of being connected conceptually. Their value for Relay must be established through explicit mappings, executable conformance tests, and measurable downstream outcomes.

### 2.1 Connection to the Earlier SI Lineage

The earlier Scoring Tree and Control Plane work supplies selection and governance; the Structural Intelligence Framework (SIF) supplies problem/capability localization; AQSI supplies autonomous questioning; UIERU and related Relay work supply multi-agent or multi-unit coordination; and Collective Learning supplies the longer-term accumulation objective. The new five-peak sequence potentially adds **dynamic state and capability evolution carried by durable objects**.

This connection matters because an object substrate without governance risks uncontrolled complexity, while a Relay architecture without explicit object and Delta semantics risks passing ambiguous artifacts between units.

## 3. A Precise Taxonomy of Intelligence Spillover

The term *spillover* should not be treated as a single scalar. At least six different mechanisms deserve separate measurement.

1. **Representational spillover:** a useful object schema, relation type, or state model can describe a new domain with limited adaptation.
2. **Computational spillover:** an operator, constraint solver, Delta generator, or optimization pattern works on another task.
3. **Residual spillover:** a failure, unexplained discrepancy, or unclosed constraint from one task supplies a useful question or hypothesis elsewhere.
4. **Discovery spillover:** a method for generating and validating CCC, Two-Way CCC, or Pattern Trigger candidates improves discovery in another domain.
5. **Governance spillover:** a conformance test, provenance requirement, sandbox, or evaluator-independence rule can be reused across systems.
6. **Collective spillover:** independent participants can improve, combine, or invalidate an artifact and return those results to a shared knowledge lineage.

These categories interact but must not be conflated. For example, reusing a JSON schema is representational reuse; demonstrating improved out-of-domain decisions is a stronger claim.

### 3.1 Spillover Versus Transfer Versus Relay

- **Spillover** describes the emergence or availability of utility outside an originating boundary.
- **Transfer** describes adaptation and use of a candidate capability in a target setting.
- **Relay** describes the structured handoff of artifacts, contracts, evidence, and unresolved issues that enables transfer and subsequent learning.

A Relay can succeed as documentation even if a proposed capability fails in the target domain. Such a negative result is itself useful evidence if it is recorded with its conditions.

## 4. WE-SIO as an Interoperability Substrate, Not a Universal Ontology

A candidate WE-SIO Core Frame may expose:

```text
WorldEntity {
    entity_id
    entity_type
    schema_version
    state_ref
    relation_refs
    temporal_scope
    provenance_refs
    residual_refs
    capability_refs
    constraint_refs
    access_policy
}
```

The core should be stable and intentionally small. Domain-specific meaning belongs in typed schemas, adapters, Plugins, and Contracts. SQL rows, a school bus, a security principal, and a financial instrument should not be forced into an identical substantive ontology merely because they share a Core Frame.

### 4.1 Three Levels of Alignment

**Structural alignment** maps entities, fields, keys, relations, and versions. **Semantic alignment** resolves units, time, missingness, identity, causal assumptions, and domain constraints. **Operational alignment** specifies how changes, transactions, Plugins, and residual updates behave under concurrency and failure.

A SQL primitive column may provide a convenient structural anchor, but a column name alone is not a complete semantic contract. For instance, a `price` field requires currency, adjustment policy, timestamp, and source conventions before a transferred financial Plugin can interpret it safely.

### 4.2 Core Frame + Plugins as an Engineering Hypothesis

A narrow Core Frame with independently replaceable Plugins may reduce integration friction. Yet extra indirection, serialization, governance checks, and synchronization can increase latency and maintenance cost. The engineering question is not whether this architecture looks elegant, but **whether total lifecycle cost and transfer reliability improve** relative to ordinary services, libraries, database views, event buses, and typed APIs.

## 5. The Transferable Unit: A Capability Relay Package

The proposed Relay unit is more than a model weight file, prompt, or executable function. It is an inspectable package with an explicit contract and evidence envelope.

```yaml
capability_id: example.directional-delta-search
version: 0.1.0
origin:
  repository: <source-repository>
  artifact: <specific-source-reference>
  license: <declared-license>
interface:
  input_schema: <versioned-schema>
  output_schema: <versioned-schema>
  preconditions: <machine-checkable-conditions>
  invariants: <machine-checkable-conditions>
  failure_modes: <documented-failures>
semantics:
  state_model: <state-contract>
  delta_model: <delta-contract>
  residual_model: <residual-contract>
evidence:
  baseline_results: <reproducible-record>
  validation_status: candidate
  limitations: <known-boundaries>
execution:
  resource_budget: <limits>
  permissions: <least-privilege-policy>
  rollback: <rollback-procedure>
relay:
  dependencies: <versioned-dependencies>
  open_questions: <explicit-leftovers>
  feedback_channel: <issue-or-review-mechanism>
```

Angle-bracketed fields are placeholders, not assertions that such packages currently exist. A production specification must define the canonical schemas, integrity hashes, version rules, and validation procedure.

The package separates four questions: **Can it be invoked? Is its behavior conformant? Is its claim empirically supported? Is it safe and useful in the target setting?** Passing the first question does not imply passing the other three.

## 6. Relay as a Staged Protocol

A proposed transfer process is:

**R0 — Capture.** Preserve the original discovery, provenance, context, negative evidence, and the residual that motivated it.

**R1 — Distill.** Identify the smallest reusable capability, pattern, contract, or hypothesis; remove accidental task-specific dependencies.

**R2 — Specify.** Publish input/output types, preconditions, invariants, failure semantics, permissions, and version compatibility.

**R3 — Conformance.** Test the package against its own specification, including invalid inputs, resource limits, rollback, and edge cases.

**R4 — Cross-domain sandbox.** Map source semantics to a target domain, run matched baselines, and record adaptations and failures.

**R5 — Independent validation.** Reproduce results with held-out data or independent evaluators; estimate uncertainty and costs.

**R6 — Governed deployment.** Permit controlled use only after satisfying domain-specific safety, privacy, and authorization requirements.

**R7 — Feedback Relay.** Return improvements, incompatibilities, counterexamples, new residuals, and deprecated assumptions to the originating lineage.

The crucial principle is **conformance before runtime claims, and independent evidence before broad transfer claims**. Repeated execution also contributes to Relay when it yields traceable evidence, not merely repeated outputs.

## 7. Residuals as Transferable Research Assets

A residual may be a prediction error, violated constraint, explanation gap, capability gap, or disagreement among evaluators. Its usefulness depends on the preserved context.

A residual record should identify its originating entity, expected and observed conditions, evidence quality, uncertainty, time window, candidate explanations, attempted repairs, and validation state. Without this context, a residual transferred to another domain can become misleading.

The most interesting possibility is **residual-to-question transfer**: an unresolved pattern in one domain suggests a new experiment in another. For example, a failed scheduling heuristic might expose a general path-memory problem relevant to D-BTP; a security identity ambiguity might suggest a compositional-state representation that is useful in other multi-actor systems. Such analogies are hypotheses, not proofs of transfer.

A strong Collective Learning repository should preserve unsuccessful transfers. A well-characterized failure prevents downstream researchers from rediscovering the same dead end and helps refine the applicability boundary.

## 8. CDE and OCSRE: Transfer of Methods Versus Transfer of Outcomes

CDE may allow a target system to reuse a constrained state-transition *pattern* without reusing the source system's state variables. The transferable contract could require:

- State transitions are explicit and versioned.
- Candidate Deltas are checked against constraints before commitment.
- Path-memory and loop-back rules are stated and testable.
- Rejected candidates and reasons can be retained for learning.
- Evaluation and generator updates are separately governed.

OCSRE adds the possibility that the object holding state and evidence also organizes reasoning, local learning, and capability calls. A transferred reasoning Plugin should still be evaluated against the target's semantics and decision objectives.

**Method transfer** means that a structural procedure can be instantiated in another domain. **Outcome transfer** means that it actually produces better results there. The former is a prerequisite for the latter, not evidence of it.

## 9. Persistent Discovery and the Relay of Newly Found Capabilities

The preceding article proposed the Structural Emergence Fishing Laboratory (SEFL), a candidate persistent discovery system. Its discovery loop can feed a Relay pipeline:

```text
World change / Object state
          |
          v
Residual and candidate opportunity
          |
          v
CCC / Two-Way CCC / Pattern Trigger hypotheses
          |
          v
CDE candidate generation + OCSRE evaluation
          |
          v
Independent validation and novelty checks
          |
          v
Capability Relay Package
          |
          v
Target-domain sandbox and replication
          |
          v
Collective feedback, revision, or retirement
          |
          +------> Updated objects / residual registry
```

The loop should not equate an increasing number of patterns with intelligence growth. Stronger evidence would be a rising rate of **validated, nonredundant, transferable improvements per unit of total resource** under prospective testing.

### 9.1 Opportunity Localization

A persistent system cannot investigate everything at equal depth. It can maintain low-cost coverage while allocating expensive analysis according to estimated evidence quality, potential utility, novelty, risk, and computational cost. The policy must also reserve an exploration budget for neglected regions; otherwise the system can lock itself into previously successful patterns and miss new opportunities.

The metaphor “wherever the rain falls, I am there” is therefore best treated as a target of *logical readiness*, not literal omnipresent computation.

## 10. Engineering Spillover: Five Candidate Testbeds

### 10.1 SQL and Change-Data-Capture Systems

**Transfer candidate:** WE-SIO object mapping, event-linked residuals, schema-aware pattern discovery, reusable triggers.  
**Baseline:** database-native queries, CDC pipelines, stream processing, and conventional anomaly detection.  
**Success evidence:** lower integration effort or more independently validated structural discoveries at comparable latency and cost.  
**Critical boundary:** transactional semantics, access controls, schema drift, and temporal consistency.

### 10.2 Dynamic School-Bus Scheduling

**Transfer candidate:** CDE Delta generation, constraint checks, path-memory policies, reusable search strategies.  
**Baseline:** mixed-integer optimization, constraint programming, local search, and established routing heuristics.  
**Success evidence:** improved feasible vehicle counts, travel burden, or adaptation speed under matched constraints and budgets.  
**Critical boundary:** student safety, maximum ride times, route feasibility, and fairness constraints must never be sacrificed for a headline score.

### 10.3 Adversarial Security and Compositional Identity

**Transfer candidate:** ASSI evidence models, dynamic actor composition, directional hypothesis evaluation, provenance-aware Relay.  
**Baseline:** graph analytics, entity resolution, established threat modeling, and forensic workflows.  
**Success evidence:** better-calibrated, auditable hypotheses with fewer unsupported identity inferences.  
**Critical boundary:** adversarial contamination, privacy, false attribution, and authorization. Structural similarity is not proof of real-world identity.

### 10.4 Financial Time Series

**Transfer candidate:** persistent object histories, residual and pattern discovery, regime-aware validation.  
**Baseline:** time-series forecasting, statistical factor models, online learning, and rule-based strategies.  
**Success evidence:** prospective, out-of-sample decision improvement after fees, slippage, risk, and multiple-testing correction.  
**Critical boundary:** nonstationarity, look-ahead bias, data snooping, and capacity limits. No market advantage is established by historical pattern discovery alone.

### 10.5 AI-Generated Code Governance

**Transfer candidate:** calling-graph localization, contract checking, object-linked residuals, and capability feedback; integration with UTN-related governance questions.  
**Baseline:** static analysis, type checking, tests, dependency analysis, and existing software supply-chain tools.  
**Success evidence:** fewer escaped defects, more precise impact localization, or lower review cost without degrading security.  
**Critical boundary:** generated explanations are not executable proofs; sandbox isolation and human authorization remain necessary.

These domains are selected to test distinct structural properties. Success in one should not be generalized to all.

## 11. Collective Learning as a Governed Evidence Network

Collective Learning should be designed as an accumulation of *reviewable claims and artifacts*, not an undifferentiated pool of agent outputs. A proposed network contains:

1. **Source registries** for papers, specifications, and provenance.
2. **Capability registries** for versioned Plugins and contracts.
3. **Residual registries** for failures, open gaps, and unresolved evidence.
4. **Validation registries** for benchmarks, replication attempts, and counterexamples.
5. **Relay portfolios** for deciding which artifacts deserve adaptation or further testing.

Governance must specify who can publish, verify, promote, deprecate, or revoke an artifact. Different participants may use different evaluators and objectives; disagreement should be represented explicitly rather than erased by a single global score.

### 11.1 Credit, Licensing, and Provenance

Each Relay should preserve authorship, citation, version, declared license, derivative lineage, and evidence provenance. Apache-2.0 may be suitable for software and specification artifacts when selected by their rights holders; third-party datasets, model weights, and publications require their own rights checks. A shared object interface does not override licensing or privacy constraints.

### 11.2 The Value of Explicit Leftovers

A high-quality Relay package should state what remains unknown: untested environments, suspected failure modes, unresolved conceptual disagreements, and incomplete validation. These leftovers are not editorial defects; they are actionable starting points for the next research unit.

## 12. A Quantitative Research Agenda

Transfer claims need metrics that cannot be improved simply by producing more artifacts. Candidate measures include:

| Measure | Meaning | Caveat |
|---|---|---|
| Validated discovery yield | Independently supported nonredundant findings / total resource | Novelty and validity require external criteria |
| Transfer success rate | Target tasks meeting preregistered success criteria / attempted transfers | Report all attempted transfers, not only successes |
| Adaptation cost | Engineering time, compute, and data needed to port a capability | Compare against strong conventional reuse |
| Capability durability | Performance retained across time, versions, or regime changes | Requires prospective observation |
| Relay reproducibility | Fraction of artifacts independently reproduced | Requires sufficient access and precise protocols |
| Residual reuse value | Improvement attributable to preserved residual evidence | Requires ablation against no-residual baselines |
| Governance overhead | Latency, compute, and review cost added by contracts and validation | May outweigh gains for simple tasks |

A possible research score is a vector rather than a single optimized number:

\[
M=(Y_{validated}, T_{success}, C_{adapt}, D_{durability}, R_{reproduce}, G_{overhead}).
\]

Any scalar aggregation should disclose stakeholder weights and constraints. Otherwise a system can appear to improve by optimizing a narrow metric while worsening reliability, safety, or transfer cost.

## 13. Falsifiable Hypotheses

**H1 — Object-substrate portability.** Under matched tasks and engineering budgets, WE-SIO-style object contracts reduce median cross-domain integration effort relative to well-designed conventional APIs. *Possible falsifier:* no improvement or increased maintenance cost.

**H2 — Residual-preserving transfer.** Transfer packages containing structured residual history yield more validated target-domain improvements than otherwise identical packages without that history. *Possible falsifier:* no incremental benefit after controlling for additional context volume.

**H3 — Constrained Delta reuse.** A common CDE transition contract can be instantiated in at least two substantially different problem families without sacrificing correctness or competitive performance. *Possible falsifier:* domain-specific adaptation dominates all common structure.

**H4 — Discovery-to-capability conversion.** A governed persistent discovery pipeline produces more independently replicated, reusable capabilities per unit resource than static rule or anomaly-detection pipelines. *Possible falsifier:* discovery counts rise but replicated utility does not.

**H5 — Relay feedback learning.** Recording negative transfers and counterexamples improves subsequent candidate selection and reduces wasted adaptation effort. *Possible falsifier:* no prospective improvement against a registry without such feedback.

**H6 — Collective improvement.** Independently contributed, conformance-tested Relay artifacts produce measurable gains over isolated development under matched budgets. *Possible falsifier:* coordination, incompatibility, and review overhead eliminate the gains.

**H7 — Governed evaluator evolution.** Allowing candidate evaluators to evolve under fixed independent holdouts improves durable target performance without reward hacking. *Possible falsifier:* gains disappear under independent testing or evaluator drift increases.

All hypotheses require preregistered outcomes, ablations, uncertainty estimates, and publication of negative results.

## 14. Minimal Specifications and Conformance Contracts

The following are candidate specification boundaries for a future implementation; they are not claims of completed software.

**CONTRACT-001 — Identity and Versioning:** object and capability identities must be stable or explicitly remapped; schema and contract versions must be recorded.

**CONTRACT-002 — Semantic Mapping:** transferred fields and relations require declared units, time semantics, missing-value handling, and domain assumptions.

**CONTRACT-003 — Delta Safety:** proposed transitions must be checked against invariants, authorization, loop-back rules, and rollback conditions before commitment.

**CONTRACT-004 — Residual Provenance:** residuals must retain evidence sources, uncertainty, time scope, and attempted resolutions.

**CONTRACT-005 — Evaluation Independence:** a capability may not certify its own improvement solely using an evaluator that it can modify.

**CONTRACT-006 — Relay Completeness:** packages must include dependencies, preconditions, known limitations, validation status, and explicit leftovers.

**CONTRACT-007 — Sandbox Isolation:** untrusted or unvalidated Plugins must not gain production privileges through discovery or transfer.

**CONTRACT-008 — Feedback Integrity:** downstream replication, failures, and revisions must be linked to the precise source version and conditions.

Conformance should be checked before broad runtime deployment; conformance alone does not establish domain utility.

## 15. Validation Roadmap

**Phase A — Preserve and specify.** Finalize the conceptual glossary, claim registry, divergence record, and the minimal Core Frame/Capability/Residual contracts. Identify exact source documents for each claim.

**Phase B — Single-domain baselines.** Implement or select strong conventional solutions for SQL discovery and scheduling; record performance, cost, and failure modes before adding the proposed structural layer.

**Phase C — Controlled transfer.** Transfer a narrowly scoped capability between two distinct task families. Report every semantic adaptation and failed mapping.

**Phase D — Persistent discovery.** Introduce governed CCC and Pattern Trigger candidate generation, residual retention, and independent novelty validation. Measure net discovery yield.

**Phase E — Collective Relay.** Have independent teams or agents reproduce and adapt packages using only published artifacts. Capture counterexamples and revisions.

**Phase F — Longitudinal assessment.** Test durability, governance overhead, version compatibility, and whether feedback measurably improves subsequent transfers.

At every phase, retain a no-Relay or no-Residual ablation and a strong non-SI baseline. A positive case study without those comparisons should be reported as feasibility evidence, not a general superiority claim.

## 16. Critical Boundaries and Failure Modes

**Uniform syntax can hide divergent semantics.** Two systems may serialize the same object shape while disagreeing on identity, time, units, or permissible actions.

**More Plugins can create more coupling.** Dependency chains, contract versions, and trust boundaries can become more difficult to govern than a simpler service architecture.

**Residual accumulation can become noise accumulation.** Retention needs relevance filtering, privacy limits, expiration, and deletion policies.

**Relay can amplify errors.** A false but plausible structural claim can spread quickly through a shared capability registry. Independent replication and revocation must be first-class mechanisms.

**Local gains can fail to transfer.** A capability may depend on hidden data distributions, incentive structures, or evaluation choices.

**Adaptive evaluators can game themselves.** Changes to scoring and objective functions need protected benchmarks and external accountability.

**Persistent observation is not free.** Storage, compute, latency, energy, security, and privacy costs must be included in net-value estimates.

**Economic value is not guaranteed.** Better pattern discovery may be offset by implementation costs, market competition, operational risk, or the absence of actionable decisions.

These boundaries are integral to the research, not qualifications to be removed from its final presentation.

## 17. Open Questions for Downstream Researchers

1. What is the smallest semantically sufficient WE-SIO Core Frame for meaningful transfer?
2. Which kinds of residuals provide positive cross-domain value, and which are noise?
3. How can a system detect when two apparently similar object types have incompatible semantics?
4. Can a CDE Delta generator transfer without transferring its domain-specific evaluator?
5. What is the correct unit of a transferable CCC or Two-Way CCC discovery?
6. How should a Relay registry represent incompatible yet legitimate stakeholder objectives?
7. What evidence distinguishes capability emergence from composition of known capabilities?
8. How should negative results and failed transfers influence future exploration budgets?
9. What is the minimum independent validation needed before a Plugin is promoted?
10. Can persistent discovery remain economically beneficial when full lifecycle costs are counted?
11. How should capability revocation propagate through dependent Relay chains?
12. What longitudinal evidence would justify calling this an evolving discovery mechanism rather than an adaptive workflow?

## 18. Conclusion: Relay the Road, the Evidence, and the Unfinished Work

The five DOI peaks reveal a plausible architectural convergence: ASSI contributes adversarially changing evidence and actors; D-BTP contributes directional candidate generation; CDE generalizes constrained Delta evolution; WE-SIO provides persistent object and capability semantics; and OCSRE integrates object-centric reasoning, computation, and learning. The wider SI lineage contributes scoring, localization, questioning, governance, and Relay.

The strongest research proposition is not that this convergence has already produced a universally superior intelligence engine. It is that **explicit object semantics, residual retention, constrained evolution, and governed Relay may make useful discoveries more portable, testable, and cumulatively improvable**.

The responsibility of a research Relay is therefore broader than publishing an attractive vision. It must preserve what was observed, what was proposed, what remains disputed, which assumptions were necessary, which experiments failed, and what another researcher can try next. The road between the peaks—including the gaps and uncertain crossings—is part of the scientific contribution.

> **Final proposition:** The most valuable intelligence spillover may be not a single transferred answer, but a reproducible improvement in the ability of different systems and researchers to discover, validate, adapt, and relay useful structural capabilities.

---

## Source Repositories and Research Lineage

The five primary research anchors are listed below. Their inclusion establishes conceptual lineage, not independent verification of the integrated architecture or its performance.

1. **ASSI — Adversarial Structural Security Intelligence:** https://github.com/sizhet/Adversarial-Structural-Security-Intelligence
2. **D-BTP — Dynamic Bucket Tree of Permutation:** https://github.com/sizhet/Dynamic-Bucket-Tree-of-Permutation-and-Directional-Structural-Evolution
3. **CDE — Constrained Delta Evolution:** https://github.com/sizhet/Constrained-Delta-Evolution
4. **WE-SIO — World Entity and Structural Intelligence Operations:** https://github.com/sizhet/World-Entity-and-Structural-Intelligence-Operations
5. **OCSRE — Object-Centric Structural Reasoning and Evolution:** https://github.com/sizhet/Object-Centric-Structural-Reasoning-and-Evolution

**Related SI lineage:** Structural Intelligence Framework (SIF); Scoring Tree and Universal Control Planes; Autonomous Questioning Structural Intelligence (AQSI); CCC and Two-Way CCC; UIERU and Relay; Collective Learning; UTN and calling-graph governance.

**Previous in series:** `005-Persistent-Structural-Discovery.md`  
**Series entry point:** `001-Five-DOI-Peaks.md`
