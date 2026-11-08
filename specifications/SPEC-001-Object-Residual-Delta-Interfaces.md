# SPEC-001 — Object, Residual, and Delta Interfaces

**Status:** Proposed research specification (v0.1.0)  
**Scope:** WE-SIO / CDE / OCSRE interoperability  
**Normative language:** MUST, SHOULD, MAY describe proposed conformance requirements, not claims of existing implementations.

## Abstract

This specification defines minimal, interoperable contracts for three first-class structural entities: persistent **Objects**, actionable **Residuals**, and constrained **Deltas**. It is intended to connect object-native representation (WE-SIO), residual-first in-situ intelligence, constrained state evolution (CDE), and object-centric reasoning and evolution (OCSRE). It separates stable semantics from optional computation plugins and establishes identity, provenance, versioning, validation, governance, and replay requirements. The objective is not to replace SQL databases, stream processors, or optimization engines, but to make their outputs and unfinished work addressable and reusable across intelligent workflows.

## 1. Purpose and non-goals

The interface must support (1) persistent identity across observations; (2) typed state and relation references; (3) explicit unresolved differences; (4) candidate transformations with constraints; (5) independent evaluation; and (6) transferable evidence and learning artifacts.

Non-goals include prescribing a universal ontology, requiring every computation to execute physically inside an object, guaranteeing intelligence emergence, or treating any detected correlation as causal knowledge.

## 2. Conceptual model

An **Object** represents a versioned entity or structural unit. A **Residual** is a typed, evidence-linked mismatch, unexplained observation, unmet constraint, or capability gap relative to an explicit reference. A **Delta** is a proposed transformation of a declared target state or, under stronger governance, a proposal to modify a generator, evaluator, or policy.

The canonical lifecycle is:

```text
Observe → Resolve Object → Compare / Evaluate → Register Residual
        → Generate Delta Candidate → Check Constraints → Sandbox
        → Independently Validate → Commit / Reject / Defer
        → Update Object and Residual Histories → Relay
```

Residual detection need not always generate a Delta; an inconclusive or low-value residual can remain open or be retired with justification. A Delta may also originate from a goal or explicit user request rather than a residual.

## 3. Common envelope: StructuralRecord

Every Object, Residual, and Delta record MUST provide:

| Field | Type | Requirement | Meaning |
|---|---|---|---|
| `record_id` | URI or namespaced string | MUST | Stable globally scoped identity |
| `record_type` | enum | MUST | `object`, `residual`, or `delta` |
| `schema_version` | semver string | MUST | Contract version |
| `revision` | monotonically increasing integer | MUST | Optimistic concurrency / history |
| `created_at`, `updated_at` | RFC 3339 timestamps | MUST | Audit times |
| `provenance` | structured reference | MUST | Origin system, actor, method, evidence pointers |
| `access_policy_ref` | reference | MUST | Authorization and sensitivity policy |
| `status` | type-specific enum | MUST | Lifecycle state |
| `extensions` | namespaced object | MAY | Non-core plugin-specific metadata |

Implementations MUST NOT silently overwrite prior revisions. They SHOULD use content hashes or signed event logs when stronger auditability is required. A missing field is not equivalent to a known null value.

## 4. Object interface

### 4.1 Required fields

```yaml
record_type: object
record_id: "we://inventory/item-42"
schema_version: "0.1.0"
revision: 7
created_at: "2026-11-08T12:00:00Z"
updated_at: "2026-11-08T12:05:00Z"
provenance:
  source: "inventory-db"
  method: "cdc-ingestion"
access_policy_ref: "policy://inventory/read"
status: active
object_kind: "inventory.item"
state:
  quantity:
    value: 14
    datatype: integer
    unit: count
relations:
  - predicate: "stored_at"
    target_ref: "we://warehouse/3"
capability_refs:
  - "cap://inventory/reorder-evaluator@1.2.0"
constraint_refs:
  - "constraint://inventory/nonnegative"
```

The object MUST expose a typed `state`, a declared `object_kind`, and an explicit `revision`. Relations MUST identify their targets and predicate semantics. Historical values MAY remain in an external time-series or SQL store, provided stable versioned references are retained. Capabilities are discoverable by contract, not assumed to be embedded executable code.

### 4.2 Core operations

- `get_object(id, revision?)` returns a versioned snapshot or a typed not-found/unauthorized result.
- `query_relations(id, predicate?, as_of?)` returns typed relation references.
- `list_capabilities(id)` returns authorized capability contracts.
- `subscribe_changes(id, cursor)` yields ordered, resumable change events, with deduplication support.

An implementation MUST declare its consistency model, including whether a snapshot is transactionally consistent across related objects.

## 5. Residual interface

### 5.1 Semantics

A residual MUST specify **what was observed**, **what reference was used**, **how the mismatch was assessed**, and **what uncertainty remains**. The reference may be a prediction, constraint, explanation, expected capability, or evaluation contract. A residual without a reference is an unclassified observation, not a validated discrepancy.

Recommended `residual_kind` values are `prediction`, `constraint`, `explanation`, `capability`, `evaluation`, `relation`, and `operational`. Types are extensible; they MUST NOT be reduced to a single universal scalar without a declared normalization policy.

### 5.2 Example

```yaml
record_type: residual
record_id: "res://inventory/shortfall-104"
schema_version: "0.1.0"
revision: 1
created_at: "2026-11-08T12:06:00Z"
updated_at: "2026-11-08T12:06:00Z"
provenance:
  source: "reorder-evaluator"
  method: "threshold-check@1.2.0"
access_policy_ref: "policy://inventory/read"
status: candidate
residual_kind: constraint
object_refs:
  - id: "we://inventory/item-42"
    revision: 7
reference:
  constraint_ref: "constraint://inventory/minimum-stock"
observed:
  quantity: 14
expected:
  minimum_quantity: 20
mismatch:
  value: 6
  unit: count
uncertainty:
  level: low
  basis: "transactional stock snapshot"
evidence_refs:
  - "event://inventory/txn-8831"
priority:
  score: 0.72
  scoring_contract_ref: "score://inventory/triage-v1"
```

### 5.3 Residual lifecycle

`candidate → corroborated → actionable → resolved | retired | disputed`.

A residual MAY remain `corroborated` indefinitely if no safe action is known. `resolved` MUST link to a state change or new evidence and a resolution criterion. `retired` MUST retain a reason (e.g., noise, duplicate, obsolete reference). `disputed` MUST preserve conflicting evidence rather than erase it.

### 5.4 Core operations

- `register_residual(record)` validates evidence, provenance, and reference semantics.
- `link_residuals(ids, relation_type)` records typed associations and possible shared causes.
- `triage_residual(id, policy_ref)` assigns attention without implying truth.
- `resolve_residual(id, evidence_refs, object_revision)` records the closure basis.

## 6. Delta interface

### 6.1 Semantics

A Delta is a **proposal**, not a committed mutation. It MUST declare its target, expected base revision, transformation, preconditions, constraints, and validation plan. Deltas affecting generators, evaluators, or governance policies MUST be labeled `meta_delta` and require independent approval.

### 6.2 Example

```yaml
record_type: delta
record_id: "delta://inventory/reorder-22"
schema_version: "0.1.0"
revision: 1
created_at: "2026-11-08T12:07:00Z"
updated_at: "2026-11-08T12:07:00Z"
provenance:
  source: "reorder-planner"
  method: "candidate-generator@0.3.0"
access_policy_ref: "policy://inventory/propose"
status: proposed
delta_kind: state_delta
target:
  object_id: "we://inventory/item-42"
  expected_revision: 7
motivation_residual_refs:
  - "res://inventory/shortfall-104"
operation:
  op: "propose_purchase_order"
  parameters:
    quantity: 12
preconditions:
  - "constraint://supplier/available"
constraint_refs:
  - "constraint://budget/purchase-limit"
validation_plan_ref: "validation://purchase-order/sandbox-v1"
rollback_plan_ref: "rollback://purchase-order/cancel-v1"
idempotency_key: "item-42-reorder-20261108"
```

### 6.3 Delta lifecycle

`proposed → checked → simulated → validated → approved → committed`, with terminal branches `rejected`, `expired`, or `rolled_back`. A successful simulation does not authorize commitment. `commit_delta` MUST verify preconditions, policy, and target revision at commit time. External side effects MUST use explicit idempotency and compensating-action policies; a rollback plan is not a guarantee of perfect reversibility.

### 6.4 CDE path semantics

A CDE execution context SHOULD track `(path_id, state_revision, applied_delta_ids, forbidden_reuse_rules, constraint_set_version, termination_budget)`. Path-local non-reuse MUST be enforced where specified by the search contract; it is not a universal prohibition on applying the same logical operation in unrelated paths. Loop-back transitions MUST declare a cycle policy, termination condition, or resource bound. Branching may be adaptive (`M → N`) but MUST remain auditable.

## 7. Cross-record invariants

1. **Referential integrity:** references MUST resolve to a record, a documented external locator, or an explicit unavailable state.
2. **Version safety:** evaluation and commit MUST identify the exact state and constraint versions considered.
3. **Evidence separation:** observed data, hypotheses, scores, and verified conclusions MUST be distinguishable.
4. **No automatic promotion:** a candidate pattern or residual MUST NOT automatically become a validated capability.
5. **Governed side effects:** observation and sandbox evaluation MUST be separable from production actions.
6. **Traceability:** committed Deltas MUST link to their evaluation, approval, resulting state, and associated residuals where applicable.
7. **Privacy and security:** access policy applies to derived residuals and relay artifacts, not only source objects.
8. **Failure preservation:** rejected candidates and failed validations SHOULD be retained within privacy and retention limits for collective learning.

## 8. Plugin and capability contract

A capability contract SHOULD declare:

```yaml
capability_id: "cap://inventory/reorder-evaluator@1.2.0"
input_schema_ref: "schema://inventory/object-v1"
output_schema_ref: "schema://inventory/residual-v1"
preconditions: ["snapshot-consistent"]
side_effect_class: "read_only"
resource_budget: {cpu_ms: 500, memory_mb: 128}
authorization_ref: "policy://inventory/read"
determinism: "versioned-input-deterministic"
conformance_suite_ref: "tests://inventory/reorder-evaluator-v1"
```

The Core Frame MUST NOT assume a plugin's trustworthiness merely because its schema is valid. Plugin provenance, execution sandbox, authorization, and independent evaluation remain separate concerns.

## 9. SQL and stream alignment

SQL alignment SHOULD proceed in three stages: **structural** (table/row/column, keys, types), **semantic** (units, temporal meaning, null semantics, business constraints), and **operational** (CDC ordering, transaction boundaries, snapshot consistency, deduplication, and update semantics).

A row may map to an Object; a column may map to a typed property; a join may map to a relation; a constraint violation may produce a Residual; and an authorized change proposal may map to a Delta. These are mapping conventions, not one-to-one equivalences. A single world entity may span multiple rows or systems.

Event consumers MUST document at-least-once versus exactly-once guarantees and handle late, duplicate, and out-of-order events. Source-system timestamps MUST NOT be treated as a universal total order.

## 10. Two-Way CCC and pattern-trigger interoperability

A pattern discovery plugin MAY emit a candidate relation linking multiple objects or residuals. Two-Way CCC evidence SHOULD represent both directions explicitly, with separate conditioning assumptions, evidence provenance, and confidence estimates. Bidirectional association MUST NOT be silently promoted to causality.

A Pattern Trigger contract MUST specify: input scope, temporal window, trigger predicate, suppression/debounce policy, expected action class, false-positive handling, validation state, and expiry/revalidation criteria. Production triggers that cause side effects MUST pass the same Delta governance boundary as other actions.

## 11. Minimal API surface

```text
ObjectStore.get(id, revision?) -> ObjectSnapshot | Error
ObjectStore.subscribe(id_or_query, cursor?) -> ChangeEventStream
ResidualRegistry.register(residual) -> ResidualRef | Error
ResidualRegistry.query(object_ref?, status?, kind?) -> ResidualRefs
DeltaEngine.propose(delta) -> DeltaRef | Error
DeltaEngine.check(delta_ref, context) -> CheckReport
DeltaEngine.simulate(delta_ref, snapshot_ref) -> SimulationReport
Validator.validate(delta_ref, evidence_refs) -> ValidationReport
Governance.approve(delta_ref, principal_ref) -> ApprovalRef
DeltaEngine.commit(delta_ref, approval_ref, expected_revision) -> CommitReceipt
Relay.export(record_refs, policy_ref) -> RelayPackage
```

Each operation MUST return typed errors, including invalid schema, unresolved reference, stale revision, constraint violation, insufficient evidence, unauthorized action, budget exhaustion, and external side-effect failure. Retries MUST be safe or explicitly documented as unsafe.

## 12. Conformance profiles

| Profile | Required behavior | Intended test |
|---|---|---|
| **P0 — Representation** | Stable Object/Residual/Delta schemas, references, versions | Serialization and round-trip tests |
| **P1 — Observation** | Object change subscriptions and residual provenance | CDC replay, duplicate/out-of-order events |
| **P2 — Evolution** | Delta preconditions, simulation, path constraints, commit checks | Stale-state and cycle tests |
| **P3 — Governance** | Authorization, approvals, side-effect boundaries, audit | Denied action and rollback tests |
| **P4 — Relay** | Portable packages with provenance, evidence, unresolved limits | Cross-runtime import and independent reproduction |

Conformance to a lower profile does not imply higher-profile compliance. Claims of learning, discovery advantage, or emergence require separate empirical evaluation and are not conformance properties.

## 13. Testable hypotheses

- **H1 — Context retention:** preserving object-linked residual history improves validated discovery yield compared with stateless pipelines at equal compute budget.
- **H2 — Update safety:** revision-checked Deltas reduce invalid commits relative to unversioned mutation proposals.
- **H3 — Reuse:** Core Frame + Plugin contracts reduce cross-domain adaptation effort relative to bespoke integration, without unacceptable runtime overhead.
- **H4 — Discovery quality:** bidirectionally evaluated CCC candidates have lower false-discovery rates than one-direction pattern promotion under controlled conditions.
- **H5 — Relayability:** evidence-bearing packages improve independent reproduction rates relative to result-only exports.

Each hypothesis requires predefined baselines, datasets, uncertainty intervals, failure reporting, and explicit cost accounting. No hypothesis is asserted as established by this specification.

## 14. Known limitations and open questions

- Can a minimal shared envelope avoid becoming an overly broad universal object model?
- How should incompatible ontologies, units, and object identity policies be reconciled?
- What is the minimal evidence threshold for promoting a residual to an actionable opportunity?
- Which Delta transformations are reversible, and how are irreversible effects governed?
- How should meta-Deltas that modify evaluators be independently benchmarked?
- How can path non-reuse and loop-back semantics remain tractable at scale?
- What privacy constraints should prevent residual histories from leaking sensitive source information?
- When does in-situ persistence outperform stateless recomputation after full infrastructure costs?

## 15. Relation to the five DOI research peaks

- **ASSI:** supplies adversarial identity, evidence, trust, and authority challenges that stress provenance and governance.
- **D-BTP:** motivates dynamic candidate generation, directional scoring, and path-aware search.
- **CDE:** provides the constrained Delta evolution perspective and state/path semantics.
- **WE-SIO:** motivates object-native identity, state, relations, and Core Frame + Plugins.
- **OCSRE:** connects object-centric reasoning, differential computation, in-situ learning, and capability evolution.

The present specification is a proposed interoperability layer above those research contributions; it does not assert that the source repositories implement this exact contract.

## 16. Source repositories

1. [Adversarial Structural Security Intelligence (ASSI)](https://github.com/sizhet/Adversarial-Structural-Security-Intelligence)
2. [Dynamic Bucket Tree of Permutation (D-BTP)](https://github.com/sizhet/Dynamic-Bucket-Tree-of-Permutation-and-Directional-Structural-Evolution)
3. [Constrained Delta Evolution (CDE)](https://github.com/sizhet/Constrained-Delta-Evolution)
4. [World Entity and Structural Intelligence Operations (WE-SIO)](https://github.com/sizhet/World-Entity-and-Structural-Intelligence-Operations)
5. [Object-Centric Structural Reasoning and Evolution (OCSRE)](https://github.com/sizhet/Object-Centric-Structural-Reasoning-and-Evolution)

## 17. Suggested next specifications

- `SPEC-002-Persistent-Discovery-Loop.md`: observation, opportunity localization, pattern generation, validation, and resource allocation.
- `SPEC-003-Validation-and-Relay-Contracts.md`: independent replication, claim lifecycle, capability packaging, and collective learning governance.

---

**Research note:** This document is a specification proposal for falsifiable engineering research. Its schemas are illustrative v0.1 contracts, not a claim of standardization or deployed compatibility.
