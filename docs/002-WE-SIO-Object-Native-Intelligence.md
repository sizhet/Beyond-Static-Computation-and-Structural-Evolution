# 002 — WE-SIO and Object-Native Intelligence: Representation, Computation, and Engineering Spillover

**Research series:** Beyond Static Computation: Object-Centric Structural Evolution and Persistent Intelligence  
**Document type:** Integrative architectural research essay / testable engineering proposals  
**Status:** Proposed architecture and research hypotheses; not an experimentally established universal runtime  
**Version:** 0.1.0 — 2026-11-08  
**Companion:** [001 — Five DOI Peaks](001-Five-DOI-Peaks.md)

## Abstract

World Entity and Structural Intelligence Operations (WE-SIO) offers a promising bridge between object-centric representation and the execution of structural intelligence. Its potential is not limited to making data more readable for reasoning. A stable **Core Frame** with extensible **Plugins** could bind entity identity, typed state, relations, provenance, constraints, residuals, capabilities, and evolution history to a common semantic address. This, in turn, could reduce repeated context reconstruction across database queries, analytic models, optimization engines, reasoning agents, and persistent learning loops. The particularly practical opportunity is a disciplined mapping from relational tables and primitive columns into object-oriented semantic frames, while retaining the relational system's transactional, query, and performance strengths.

This paper proposes an object-native intelligence architecture, distinguishes logical locality from physical co-location, specifies the contracts needed for relational alignment and safe plugin execution, and traces the connections to Structural Intelligence Framework (SIF), Constrained Delta Evolution (CDE), and Object-Centric Structural Reasoning and Evolution (OCSRE). It also identifies failure modes—semantic mismatch, object inflation, stale state, plugin privilege escalation, provenance loss, and unjustified performance claims—and outlines experiments capable of separating actual engineering spillover from architectural elegance alone. The central proposition is that a world entity can become a **durable coordination unit for computation, learning, and evolution**, without requiring all computation to reside inside the entity itself.

**Keywords:** WE-SIO; world entity; object-native intelligence; Core Frame; plugins; SQL alignment; semantic contracts; structural intelligence; in-situ computation; residual-first learning; capability relay.

---

## 1. Why Object-Native Intelligence Matters

A typical computational workflow crosses several representational boundaries: a relational table is queried, rows are converted into application objects, features are assembled, models are invoked, results are interpreted, and downstream actions are issued. Each boundary may require the system to reconstruct identity, temporal scope, units, permissions, and the meaning of the result. Such separation is often justified by modularity and scalability; it becomes costly when a system must **continuously observe and learn from evolving entities** rather than answer one isolated query.

WE-SIO suggests a different organizing question:

> What if the persistent unit of intelligence were not merely a data record or an autonomous agent, but an identifiable world entity with explicit, governed connections to state, relations, residuals, computational capabilities, and evolution history?

This is a proposal about **semantic and operational coordination**, not a demand to abandon databases, functions, event streams, GPUs, or existing models. A WE-SIO object should be able to *refer to* these resources through well-defined contracts. The proposed advantage is continuity of meaning across them.

The five-DOI sequence supplies the context. ASSI exposes changing identities and evidence; D-BTP requires dynamic candidate structures; CDE generalizes constrained state transitions; WE-SIO supplies a possible common object carrier; and OCSRE investigates reasoning, differential computation, in-situ learning, and capability spillover on that carrier. The present paper concentrates on WE-SIO's architectural and engineering implications, leaving the full evolution loop to paper 003 and residual-native operation to paper 004.

### 1.1 Scope of the claim

Three levels must remain distinct:

1. **Representation claim:** a WE-SIO frame can express useful identity, state, relation, and capability metadata.
2. **Engineering claim:** the shared frame can lower integration, maintenance, and repeated-context costs for selected workloads.
3. **Intelligence claim:** persistent object-local context can improve the discovery, validation, and reuse of useful structural hypotheses.

The first is largely a design and conformance question. The second requires implementation benchmarks. The third requires controlled learning and discovery experiments. Success at one level does not prove the next.

## 2. From Object-Centric Representation to an Operational World Entity

An ordinary object groups fields and methods. A database row groups typed values under a schema. A knowledge-graph node identifies an entity and its edges. A WE-SIO object is proposed as a **semantically durable intersection** of these concerns, with explicit hooks for computational and learning processes.

A candidate world-entity frame can be modeled as:

\[
W_e = (I, S, R, H, C, P, A, X, V)
\]

where:

- **I — Identity:** stable identifier, type, namespace, aliases, entity-resolution confidence.
- **S — State:** typed attributes, units, temporal scope, version, and validity intervals.
- **R — Relations:** typed links to other entities, including direction and evidence.
- **H — History:** event references, state transitions, provenance, and lineage.
- **C — Constraints:** invariants, access rules, admissible state transitions, and validation contracts.
- **P — Plugins:** discoverable computational capabilities with declared inputs and outputs.
- **A — Attention and residuals:** unresolved differences, alerts, hypotheses, and prioritization references.
- **X — Execution references:** data stores, query engines, compute services, sandboxes, and relay endpoints.
- **V — Version and governance:** schema version, ownership, authority, audit, and compatibility metadata.

This tuple is a **proposed interface decomposition**, not a claim that the original WE-SIO repository already implements every field in precisely this form. An implementation may store most elements as references rather than embedding them physically.

### 2.1 Identity must outlive individual representations

One entity may appear as a SQL row, a time-series key, an API resource, and a graph node. A useful object-native system needs explicit identity-resolution rules and must preserve uncertainty when a match is ambiguous. In adversarial or financial settings, the apparent entity may represent a composite actor, a changing group, or a hypothesis rather than a known individual. Object identity must therefore not silently imply ground truth.

### 2.2 Time and provenance are part of semantics

A price without its currency, observation time, source, adjustment convention, and validity interval is not a fully specified value. Similarly, a relation inferred yesterday may be contradicted tomorrow. WE-SIO should distinguish **event time**, **processing time**, **effective time**, and **version time** where applicable. Provenance should accompany both observations and derived conclusions.

### 2.3 World modeling is open-ended, not unconstrained

New entity types, relations, metrics, and capabilities should be introducible without rewriting the entire core. Yet open-ended growth requires type validation, schema migration, compatibility checks, resource limits, and authority boundaries. Extensibility without governance can degrade into inconsistent metadata and uncontrolled execution.

## 3. The Core Frame + Plugins Dual Architecture

The central engineering proposition is a **small, stable Core Frame** paired with an open but contract-governed plugin ecosystem.

### 3.1 Core Frame: what should be stable

The core should supply the minimum interoperable machinery:

| Core responsibility | Minimum contract |
|---|---|
| Entity identity | Stable address, type, version, identity confidence where needed |
| State access | Typed reads, versioned updates, temporal qualifiers |
| Relations | Typed and directional edges with provenance |
| Constraint enforcement | Validation, authorization, invariant checking |
| Residual registration | Structured discrepancy records and lifecycle |
| Capability discovery | Plugin manifest, compatibility and permission checks |
| Event linkage | Change notification and event-to-state reconciliation |
| Audit and relay | Reproducible inputs, outputs, lineage, and handoff metadata |

The core should **not** include every algorithm, model, or domain-specific business rule. Otherwise the common runtime becomes a monolith and loses the openness that motivates WE-SIO.

### 3.2 Plugins: extensible capabilities, not unrestricted methods

A plugin can expose SQL queries, feature transforms, graph traversal, optimization, forecasting, constraint checking, CDE candidate generation, OCSRE reasoning, or external-agent assistance. Each plugin should publish a machine-checkable manifest containing at least:

```yaml
plugin_id: example.forecast.v1
contract_version: "1.0"
accepted_entity_types: [market.instrument]
inputs:
  - name: price_series
    type: timeseries.decimal
    required_metadata: [currency, event_time, source]
outputs:
  - name: forecast
    type: prediction.distribution
side_effects: none
permissions: [read:market.instrument]
execution:
  mode: sandboxed
  max_runtime_ms: 3000
  deterministic: false
provenance_required: true
validation_policy: forecast_oos_v1
```

This manifest is **illustrative**, not an existing standardized WE-SIO schema. The core should check compatibility, authority, and resource budgets before dispatch. Output must be validated before it can change a durable object state or become a relayed capability.

### 3.3 Logical in-situ versus physical in-situ

The phrase *in-situ computation* can be misunderstood. Three arrangements are possible:

- **Physically local:** the computation executes in the same process or storage node as the object.
- **Data-local:** computation is pushed toward the data store, such as SQL aggregation or a database-native operator.
- **Semantically local:** computation may run remotely but remains attached to the entity's identity, state version, constraints, and residual history.

The third is the most general and defensible WE-SIO proposition. A remote GPU or distributed database can remain fully compatible with object-native intelligence if the results are correctly bound to the object's semantic context. Physical locality should be selected by cost, privacy, latency, and reliability rather than assumed to be universally superior.

## 4. SQL Primitive-Column Alignment: A Practical Entry Point

Relational databases offer a compelling bridge into real-world systems because they already encode typed values, keys, constraints, indexes, and query semantics. WE-SIO could build an **object view** over these assets instead of requiring a wholesale migration.

### 4.1 Three levels of alignment

**Level 1 — Structural alignment.** Map database/table/row/column, primary keys, foreign keys, data types, nullability, and constraints into object identity and typed attributes.

**Level 2 — Semantic alignment.** Add units, domain meaning, source, temporal interpretation, uncertainty, and relation semantics. A column name alone is rarely sufficient.

**Level 3 — Operational alignment.** Support query pushdown, change-data capture (CDC), transactional consistency, incremental object updates, residual generation, and capability execution.

The first level makes mapping convenient. The second makes reasoning safer. The third creates the conditions for continuous engineering spillover.

### 4.2 Illustrative mapping

Suppose a database contains:

```sql
CREATE TABLE instrument_prices (
    instrument_id TEXT NOT NULL,
    event_time TIMESTAMP NOT NULL,
    currency CHAR(3) NOT NULL,
    close_price DECIMAL(18,6) NOT NULL,
    volume BIGINT,
    source_id TEXT NOT NULL,
    PRIMARY KEY (instrument_id, event_time, source_id)
);
```

A WE-SIO view might map `instrument_id` to an entity reference; `event_time` to the observation's temporal scope; `currency` to a unit/denomination qualifier; `close_price` and `volume` to typed observations; and `source_id` to provenance. The **composite primary key** identifies a price observation, not necessarily the instrument entity itself. That distinction is essential.

A minimal mapping declaration might look like:

```yaml
entity_type: market.instrument
identity:
  source: instrument_prices.instrument_id
observations:
  - field: close_price
    type: decimal
    time: event_time
    qualifiers: [currency]
    provenance: source_id
  - field: volume
    type: integer
    time: event_time
    provenance: source_id
update_mode: cdc
consistency: source_transaction_order
```

Again, this is an example contract, not an assertion of an implemented parser.

### 4.3 What must not be lost in translation

A robust alignment must preserve:

- **SQL NULL semantics** and distinctions among missing, unknown, invalid, and inapplicable values.
- **Composite keys, uniqueness, and referential integrity.**
- **Transaction boundaries and isolation levels**, especially for multi-table state.
- **Joins, aggregations, and window semantics** that do not map cleanly to one object field.
- **Late-arriving and corrected events**, including retractions and backfills.
- **Authorization and row-level security** from the underlying source.
- **Query planning and pushdown**, so an object layer does not cause avoidable full scans or N+1 queries.

The object frame should complement relational algebra, not pretend to replace it. Where SQL already performs a computation efficiently, WE-SIO should preserve that advantage and attach the result to a semantically explicit object context.

## 5. A Continuous Object-Native Computation Loop

Once objects are linked to live data and executable capabilities, the architecture can support a continuous loop:

```text
Relational / Stream / Graph / API Sources
                  |
        Typed mapping + CDC
                  v
       WE-SIO Object Frames
                  |
        State/version comparison
                  v
       Residual and Event Registry
                  |
    Scoring + Capability Localization
                  v
       Contracted Plugin Execution
                  |
     Reasoning / CDE / OCSRE / Tests
                  v
        Validated Commit or Reject
                  |
         Audit + Relay + Learning
                  |
             feedback
                  +------> Object Frames / Policies
```

This is not a claim that every object should execute every plugin on every update. It is a **governed opportunity-routing design**. A control plane should determine whether an event is relevant, which residual deserves attention, which plugin is admissible, and whether expected benefit justifies the compute budget.

### 5.1 Object-local residuals as durable research inputs

An observed-versus-expected mismatch, failed constraint, unexplained relation, or capability gap can be recorded as a structured residual tied to the entity, its state version, and evidence. Residuals should be typed rather than compressed into a single scalar error. They can then support later hypothesis generation, comparison, or relay.

### 5.2 Two-way evidence and cross-object reasoning

A local object may produce a candidate relation to another object; evidence from the second object can confirm, weaken, or contradict it. This is a natural place to explore CCC, Two-Way CCC, and Pattern Triggering mechanisms. The object fabric supplies persistent addresses and evidence lineage; the reasoning layer supplies the logic and tests. Correlation or co-occurrence alone must not be upgraded into a causal claim.

### 5.3 Controlled commits

Proposed updates should pass type checks, state-version checks, authorization, constraint validation, and domain-specific tests. Failed updates remain observable as residuals or rejected hypotheses, rather than disappearing. Retaining failure evidence supports learning but requires storage limits and retention policies.

## 6. Connections to SIF, CDE, OCSRE, and Relay

WE-SIO's role is clearer when it is not asked to solve every part of structural intelligence by itself.

| Research program | Distinct role in the proposed composition |
|---|---|
| **SIF** | Problem/capability localization, addressing, governance, structural coordination |
| **WE-SIO** | Persistent entity identity, state, relations, semantic interfaces, capability attachment |
| **CDE** | Constrained generation and evaluation of state/strategy/operator deltas |
| **OCSRE** | Object-centric reasoning, differential computation, in-situ learning, capability evolution |
| **UCPSF / Scoring** | Perspective-aware evaluation, attention, prioritization, control policies |
| **UIERU / Relay** | Packaging, transfer, validation, and reuse of discovered capabilities |
| **ASSI** | Adversarial test cases involving changing identity, evidence, and authority |

This table is a proposed division of responsibilities. Implementations may overlap, but overlaps should be resolved through explicit contracts rather than ambiguous ownership.

### 6.1 SIF localization and WE-SIO addressing

SIF asks where a problem or capability should be located and addressed. WE-SIO can provide concrete entity addresses, typed relation paths, and operational references. CDE extends localization into a dynamic question: which admissible state changes and candidate branches should be explored next? These are complementary roles, not interchangeable terms.

### 6.2 CDE changes the state; WE-SIO preserves its meaning

CDE can propose a delta against a state container. WE-SIO can specify which entity and version the delta targets, what constraints govern the transition, and how the result is recorded. An admissible delta must not silently rewrite identity or historical evidence. Where reversible deltas are supported, inverse operations and path memory need explicit semantics.

### 6.3 OCSRE adds reasoning and learning over the object fabric

OCSRE can orchestrate candidate hypotheses, compute differences, select capabilities, and learn from residuals. WE-SIO provides the durable object context that can make such learning reusable rather than ephemeral. Neither alone guarantees emergent intelligence: novelty, generalization, and net utility must be demonstrated.

### 6.4 Relay as a first-class output

A useful result should be exportable with its schema, prerequisites, evidence, failure cases, tests, and version. The object-native frame can make that packaging more systematic. A learned plugin without provenance or a validation contract is not yet a reliable relay artifact.

## 7. Engineering Spillover: Where the Architecture Could Matter

Potential application areas include:

**Operational SQL systems.** Persistent monitoring of entity changes, cross-table constraints, and recurring exceptions, with governed capability invocation.

**Market and time-series systems.** Event-time-aware objects, evolving relations, prediction residuals, and hypothesis testing. Financial patterns require walk-forward evaluation, transaction costs, and strict safeguards against look-ahead bias.

**Scheduling and logistics.** Vehicles, requests, routes, constraints, and candidate schedules represented as related entities; CDE proposes controlled changes while WE-SIO preserves state and evidence.

**Scientific discovery.** Instruments, measurements, hypotheses, and unexplained residuals share provenance-aware addresses. Hypotheses remain distinct from validated findings.

**AI-generated code governance.** Modules, interfaces, dependencies, call graphs, tests, and change requests become related objects. Critical-path and dependency analysis can route into existing UTN-oriented mechanisms; WE-SIO should integrate with, not replace, specialized code-analysis tools.

**Adversarial security.** Dynamic identities and conflicting evidence become explicit objects and relations. The design must guard against poisoned observations, forged provenance, privilege escalation, and overconfident attribution.

Across these domains, the claimed spillover is **reusable semantic and operational scaffolding**. Whether it outweighs additional abstraction and runtime overhead is an empirical question.

## 8. Architectural Risks and Critical Objections

### 8.1 Object inflation and accidental monoliths

A frame that absorbs all data, computation, and policy becomes difficult to scale or reason about. Keep the core narrow; use references, typed extensions, and plugin boundaries. Domain-specific fields should not automatically enter the universal core.

### 8.2 Semantic mismatch masquerading as alignment

Mapping a SQL column to an object attribute is easy; preserving the meaning of derived measures, temporal joins, NULL, provenance, and units is not. The architecture should report unmapped semantics explicitly rather than imply lossless conversion.

### 8.3 Distributed consistency and stale object views

CDC and event-driven updates are not automatically transactionally consistent. A WE-SIO view may lag behind source tables or combine incompatible snapshots. Every inference and action should state the source version, consistency guarantees, and acceptable staleness.

### 8.4 Plugin authority and supply-chain risk

An open plugin interface creates an attack surface. Signed manifests, least-privilege execution, sandboxing, quotas, dependency review, and audit logs are essential. A plugin must not acquire authority simply because an object advertises its capability.

### 8.5 Attention overload and residual noise

Persistent observation can produce too many low-value residuals. Deduplication, decay, prioritization, uncertainty calibration, and bounded retention are necessary. More observations do not necessarily yield more intelligence.

### 8.6 No automatic advantage over existing systems

Object-relational mappers, knowledge graphs, actor systems, event sourcing, streaming engines, and agent frameworks already solve overlapping problems. The WE-SIO proposal must demonstrate its **distinct integration benefits** rather than claim novelty for each component individually.

## 9. Testable Hypotheses

**H-WE-001 — Context reconstruction.** Under matched workloads, a WE-SIO object fabric reduces repeated identity/metadata reconstruction relative to a conventional service-and-table pipeline without degrading correctness.

**H-WE-002 — Relational alignment.** A contract-driven SQL mapping preserves a defined set of key, type, temporal, provenance, and authorization semantics across updates and backfills.

**H-WE-003 — Plugin interoperability.** Independently implemented plugins can exchange typed results through the Core Frame with fewer custom adapters than a baseline integration architecture.

**H-WE-004 — Residual continuity.** Persisting object-bound residuals improves the precision or time-to-validation of subsequent structural discoveries compared with stateless anomaly processing at matched budgets.

**H-WE-005 — Cross-domain relay.** A capability packaged with object contracts, evidence, and tests transfers to a second domain with less integration effort than a domain-specific pipeline, without unacceptable loss of validity.

**H-WE-006 — Governance overhead.** The incremental runtime, storage, and operational cost of the Core Frame remains within explicitly defined workload-specific thresholds; otherwise the architecture's net benefit is not established.

These are hypotheses, not reported experimental results.

## 10. Minimum Validation Program

### Experiment A — SQL-to-object conformance

Construct a relational dataset with composite keys, nullable columns, multi-table transactions, corrections, late events, and row-level access controls. Define mappings and measure semantic fidelity, missed or duplicated updates, staleness, query overhead, and audit completeness. Include adversarial cases and intentionally ambiguous entity identities.

### Experiment B — Core Frame + Plugins integration

Implement three independent capabilities—SQL aggregation, time-series residual detection, and constraint validation—behind the same manifests. Compare adapter count, engineering effort, execution latency, failure isolation, and maintenance complexity against an ordinary modular service design.

### Experiment C — Persistent discovery

Run matched pipelines with and without object-bound residual history. Evaluate validated discovery rate, false discovery rate, evidence reuse, time to verification, and compute cost. Include holdout data, pre-registered evaluation criteria, and a negative-results log.

### Experiment D — Cross-domain transfer

Transfer a constrained-delta or residual-scoring capability between two structurally similar but semantically different domains (for example, scheduling and inventory). Measure the amount of contract adaptation required and whether performance survives the transfer.

### Evaluation rules

- Publish baselines, workloads, budgets, and failure cases.
- Separate correctness from speed and novelty from utility.
- Use independent evaluation where the system may modify its own scoring rules.
- Report negative and inconclusive results rather than only successful discoveries.
- Do not infer general intelligence from isolated integration or benchmark wins.

## 11. A Proposed Minimal Interface Contract

The following pseudocode sketches a possible *logical* interface. It is intentionally smaller than a full runtime specification:

```text
EntityRef        = (namespace, entity_type, entity_id, version?)
Observation      = (field, typed_value, event_time, provenance, qualifiers)
ResidualRef      = (entity_ref, residual_type, evidence_ref, status)
CapabilityRef    = (plugin_id, contract_version, permissions, validation_policy)
DeltaProposal    = (target_entity, base_version, change_set, constraints, evidence)
ValidatedResult  = (output, provenance, tests, decision, audit_ref)

observe(entity_ref, observation) -> state_update_or_rejection
query(entity_ref, temporal_scope, consistency) -> typed_state
register_residual(entity_ref, evidence) -> residual_ref
resolve_capability(entity_ref, task, budget) -> admissible_capabilities
propose_delta(entity_ref, delta) -> candidate_ref
validate(candidate_ref, policy) -> validated_result
commit(validated_result, expected_version) -> new_version_or_conflict
relay(validated_result, destination_contract) -> relay_receipt
```

The core must distinguish **proposal**, **validation**, and **commit**. An LLM-generated hypothesis or plugin output should not automatically become a durable fact or authorized action.

## 12. Open Questions and Research Divergences

1. **How thin can the Core Frame remain?** Which responsibilities are universal, and which should be plugins or external services?
2. **What is the canonical unit of identity?** Entity, observation, relation, hypothesis, and composite actor may require distinct identity semantics.
3. **How much SQL alignment is lossless?** Which relational constructs demand explicit non-object-native representations?
4. **What does in-situ mean operationally?** Under which workloads is semantic locality enough, and when does physical data locality matter?
5. **Can residuals become universal first-class objects?** Or do heterogeneous residual types require multiple incompatible contracts?
6. **How should capability ownership and authority work?** Who may install, execute, revise, or relay a plugin?
7. **When is object-native integration economically superior?** What scale, change frequency, and cross-domain complexity justify its overhead?
8. **What qualifies as structural intelligence spillover?** Reuse of code, transfer of a pattern, transfer of a learning mechanism, and discovery of a new capability are different achievements.
9. **How should WE-SIO interoperate with knowledge graphs, actors, and event-sourced systems?** A practical architecture should reuse proven infrastructure wherever possible.
10. **How should self-referential updates be governed?** Any plugin that changes its own representation or evaluation criteria needs independent validation and rollback.

These questions should remain visible in the research record even when a particular implementation chooses a provisional answer.

## 13. Relay Guidance for Independent Researchers

A useful research relay should include:

- **Claim:** precisely what the architecture is expected to improve.
- **Contract:** typed interfaces, consistency guarantees, and authority boundaries.
- **Evidence:** source datasets, provenance, tests, and known limitations.
- **Counterexamples:** cases where mapping fails or abstraction overhead dominates.
- **Reproduction:** a minimal setup with baselines and measurement procedures.
- **Extension point:** how a new entity type, metric, plugin, or evaluator can be added without invalidating existing contracts.

This structure allows future researchers to adopt a small, testable subset of WE-SIO without committing to the entire SI research program. That openness is a feature, not a weakness.

## 14. Conclusion

WE-SIO's most promising contribution may be the **continuity of computation around a durable, semantically explicit world entity**. The proposed Core Frame + Plugins architecture offers a way to coordinate heterogeneous data, algorithms, and learning mechanisms while preserving identity, provenance, constraints, and versioned state. Alignment with SQL primitive columns and relational operations provides a practical route into existing engineering systems, provided the mapping does not erase transaction, temporal, or query semantics.

The larger opportunity appears when WE-SIO is combined with SIF localization, CDE constrained evolution, OCSRE reasoning, residual-first learning, and governed Relay. A changing entity can then become the address at which evidence accumulates, discrepancies remain available for future analysis, capabilities are invoked, hypotheses are tested, and validated improvements are passed onward. This is a plausible architecture for persistent structural discovery—not yet proof of a general intelligence engine.

The next paper, **003 — From Static Localization to Structural Evolution Computing**, examines how CDE and OCSRE can make these object-centered structures dynamically generative and evolvable.

---

## Source Research Repositories

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

**Research note:** The interfaces, pseudocode, example schemas, and experiments in this article are forward-looking synthesis proposals. Consult the original repositories for their own authoritative terminology, versioned specifications, and claims. No benchmark results are asserted here.
