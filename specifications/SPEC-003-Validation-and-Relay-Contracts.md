# SPEC-003 — Validation and Relay Contracts

**Status:** Research specification / proposed contract (v1.0.0)  
**Scope:** Evidence governance, independent validation, capability packaging, cross-context transfer, and Collective Learning Relay  
**Companions:** `SPEC-001-Object-Residual-Delta-Interfaces.md`; `SPEC-002-Persistent-Discovery-Loop.md`  
**Research context:** ASSI → D-BTP → CDE → WE-SIO → OCSRE  
**Normative language:** MUST, SHOULD, and MAY describe obligations for an implementation claiming conformance to this *proposed* specification; they do not imply an established standard or deployed implementation.

## Abstract

A persistent structural discovery system is useful only if its discoveries can be distinguished from noise, reproduced, safely acted upon, and transferred without silently changing their meaning. This specification defines contracts for turning observations, Residuals, CCC / Two-Way CCC hypotheses, Pattern Triggers, and constrained Deltas into evidence-backed claims and portable capability packages. It separates **discovery**, **validation**, **deployment authorization**, and **Relay**. It also preserves negative findings, disagreements, and unresolved limitations as first-class research assets. The specification is intentionally implementation-neutral and does not presume that a discovered pattern constitutes causal knowledge, emergent intelligence, or economic advantage.

## 1. Goals and non-goals

### 1.1 Goals

1. Establish traceable links from source observations and WE-SIO state versions to a claim, its tests, and its decisions.
2. Require independent evaluation before a candidate is promoted to validated knowledge.
3. Define explicit claim and capability lifecycles, including failure, retraction, and retirement.
4. Permit a finding to be relayed across teams, agents, runtimes, and domains without erasing assumptions or negative evidence.
5. Separate evidence strength from authorization to take consequential action.
6. Support specification-first conformance tests prior to any full runtime implementation.

### 1.2 Non-goals

This specification does not define a universal scientific truth metric, a universal ontology, a mandatory statistical method, an automatic trading strategy, or an unrestricted self-modifying agent. It does not guarantee successful transfer, autonomous discovery, or positive return on investment. The receiving environment remains responsible for local validation and governance.

## 2. Terms and distinctions

| Term | Meaning | Important boundary |
|---|---|---|
| **DiscoveryCandidate** | Proposed relationship, trigger, explanation, or improvement | Not yet verified |
| **Claim** | Precisely scoped assertion with evidence and test conditions | Not automatically actionable |
| **EvidenceBundle** | Immutable or content-addressed references to observations, procedures, and outcomes | Evidence may be incomplete or restricted |
| **ValidationRun** | Reproducible evaluation under a declared protocol | One successful run is not universal validity |
| **CapabilityPackage** | Portable interface, procedure, policy, or plugin with contracts and evidence | Portability is not equivalence |
| **RelayEvent** | Recorded transfer of a package or claim to another context | Transfer is not deployment |
| **LocalAcceptance** | Receiving context's independent compatibility and validation decision | Cannot be inherited blindly |
| **Comparative advantage** | Measured net improvement over a declared baseline and budget | Not implied by pattern discovery |

A claim MAY describe correlation, prediction, causal mechanism, optimization benefit, or transferability, but MUST declare which. A statistical association MUST NOT be relabeled causal without an appropriate identification and validation design.

## 3. Canonical evidence and claim records

Records MAY be represented in YAML, JSON, database tables, or another lossless encoding. Identifiers, schema versions, source references, and lifecycle transitions MUST remain stable and auditable.

### 3.1 ClaimRecord

```yaml
claim_id: claim-0042
schema_version: "0.1"
claim_type: predictive_pattern  # association | predictive_pattern | causal | optimization | capability
statement: "Pattern P improves 1-step prediction under protocol V"
scope:
  object_types: [market-series]
  source_domains: [research-sandbox]
  time_window: "2024-01-01/2025-12-31"
  excluded_contexts: [live-trading]
source_refs:
  object_versions: ["asset-17@v83"]
  residual_ids: [res-201]
  discovery_candidate_ids: [candidate-018]
  delta_ids: [delta-093]
evidence_bundle_id: evidence-0042
protocol_id: protocol-007
status: candidate
uncertainty: "Requires out-of-sample replication"
limitations: ["Possible regime dependence", "Multiple-testing exposure"]
owner_or_steward: research-team-a
created_at: "2026-11-08T20:00:00Z"
```

**Contract C-CLAIM-01:** Every claim MUST have a falsifiable or explicitly bounded statement, claim type, declared scope, evidence references, limitations, and status. Missing evidence MUST be represented as missing, not inferred as successful.

### 3.2 EvidenceBundle

```yaml
evidence_bundle_id: evidence-0042
schema_version: "0.1"
source_manifest:
  - source_id: dataset-a
    snapshot_id: snapshot-2026-11-08
    digest: "sha256:<actual-digest-at-publication>"
    access_class: restricted
    schema_version: "3"
observation_refs: [obs-1042]
procedure:
  code_revision: "git:<actual-commit>"
  environment_digest: "sha256:<actual-digest>"
  parameters_ref: params-007
  random_seed: 1729
  split_policy: chronological_holdout
results:
  validation_run_ids: [run-007]
  negative_run_ids: [run-006]
provenance:
  collected_by: source-adapter-a
  transformation_log_ref: transform-log-12
privacy_policy_ref: privacy-01
```

Placeholder digests above MUST be replaced by real verifiable values in any published conformance artifact. Restricted source data MAY remain private, but the restriction and the consequent replication limits MUST be declared. No claim of fully independent reproduction is permitted if necessary materials are unavailable to the reproducer.

**Contract C-EVID-01:** Evidence MUST retain data lineage, event/observation time where relevant, transformations, test procedure, negative outcomes, and access constraints. Changes MUST create new versions rather than silently rewriting historical evidence.

## 4. Claim lifecycle and state transitions

```text
candidate
   |
   v
screened -----> rejected
   |
   v
replication_pending -----> inconclusive
   |
   v
replicated -----> validated -----> deployable_candidate
   |                  |                    |
   |                  v                    v
   +--------------> challenged          authorized
                          |                 |
                          v                 v
                      revised/retired    deployed
                                            |
                                            v
                                      monitored/retired
```

The diagram is illustrative, not a mandatory single workflow. `rejected`, `inconclusive`, `challenged`, and `retired` MUST remain queryable. A `validated` claim is not automatically `authorized`, and a `deployed` capability can later be `retired` or rolled back. A revision MUST link to its predecessor and explain what changed.

**Contract C-LIFE-01:** Every status transition MUST record actor/authority, timestamp, previous status, reason, evidence, and policy version. The system MUST reject unsupported promotion or unauthorized deployment transitions.

## 5. Validation protocol contract

Each `ValidationProtocol` MUST specify:

- **Question and estimand:** what is being measured, for which population or state distribution.
- **Baseline(s):** fixed rules, existing algorithms, and other appropriate competitors.
- **Data separation:** training, selection, validation, and final test boundaries; chronological or group-aware splitting when needed.
- **Discovery accounting:** candidate search space, number of tests, selection history, and leakage controls.
- **Metrics:** primary and secondary measures, uncertainty intervals, failure rates, and computational cost.
- **Stopping rule:** preregistered or versioned success/failure criteria and budget limits.
- **Replication:** who can rerun the test, with what artifacts, and how independence is assessed.
- **Negative results:** what constitutes non-replication, regression, or inconclusiveness.
- **Threat model:** adversarial manipulation, dataset shift, privacy, and operational risk where applicable.

Example:

```yaml
protocol_id: protocol-007
claim_type: predictive_pattern
primary_metric: net_predictive_gain
baselines: [fixed-rule, online-learning]
data_split: chronological
holdout_locked_before_selection: true
multiple_testing_control: declared-and-audited
compute_budget: "100 GPU-hours maximum"
minimum_effect: "Predeclared domain-specific threshold"
replication_requirement: independent_run_on_unseen_period
promotion_policy: require_positive_effect_and_no_critical_violation
```

**Contract C-VAL-01:** Evaluation MUST distinguish in-sample discovery from untouched evaluation. For an adaptive discovery engine, repeated access to the same holdout MUST be logged and treated as selection exposure.

**Contract C-VAL-02:** Validation MUST include at least one meaningful baseline and a cost-aware result; raw accuracy or raw discovery count alone is insufficient to establish comparative advantage.

**Contract C-VAL-03:** Evidence of transfer requires testing in a receiving context, not merely renaming objects or reusing a schema.

## 6. Special validation rules for structural discovery

### 6.1 CCC, Two-Way CCC, and Pattern Triggers

A candidate MUST declare the conditions, direction(s), temporal ordering, observed support, counterexamples, and expected trigger consequence. Two-way evidence MUST distinguish independent reverse-direction support from circular restatement of the same evidence. Trigger execution MUST have an explicit action policy and MUST NOT be authorized solely because a pattern was replicated.

### 6.2 Residual-First mechanisms

Residual detection quality MUST be evaluated against noise, duplicate alerts, missed consequential differences, and investigation cost. A system MUST NOT use total residual count as a proxy for intelligence growth. Evaluation SHOULD compare the value of retaining residual histories against stateless recomputation and against ordinary event-stream processing.

### 6.3 CDE and evaluator-changing Deltas

Deltas that change the evaluator, reward function, admissible constraints, or validation procedure are **meta-Deltas**. They MUST be evaluated against an external, versioned reference criterion that the candidate cannot alter. Path-memory and non-reuse constraints MUST be checked within their declared scope. Irreversible or high-impact actions MUST be sandboxed or subject to additional authorization.

### 6.4 Claimed emergence

An emergent-capability claim MUST specify the capability, a nontrivial baseline composition, generalization tests, and a criterion that distinguishes new functional competence from increased search volume or compute expenditure. The label *emergent* MUST NOT be inferred merely from an unexpected pattern or a new plugin registration.

## 7. Capability Relay Package (CRP)

A Relay package SHOULD be compact enough for independent evaluation, yet complete enough to preserve the conditions of its validity.

```yaml
package_id: crp-0031
package_version: "1.0.0"
schema_version: "0.1"
capability_kind: pattern-trigger-plugin
purpose: "Detect and score candidate relationship P"
interface:
  input_schema_ref: schemas/input-v1.json
  output_schema_ref: schemas/output-v1.json
  contract_ref: contracts/trigger-v1.md
semantics:
  object_types: [market-series]
  units_and_time_semantics_ref: semantics/time-and-units.md
  preconditions: ["Timestamped observations", "Stable object identity"]
  exclusions: ["No causal interpretation", "No autonomous live orders"]
execution:
  implementation_ref: "git:<actual-commit>"
  dependencies_ref: dependencies.lock
  resource_budget: "Declared by deployment context"
  permission_profile: read-only
validation:
  claim_ids: [claim-0042]
  evidence_bundle_ids: [evidence-0042]
  known_failures: ["Nonstationary regime sensitivity"]
  validation_status: replicated
provenance:
  origin_project: SEFL-research
  steward: research-team-a
  license: Apache-2.0
relay_policy:
  local_revalidation_required: true
  allowed_actions: [evaluate, simulate]
  forbidden_actions: [autonomous-live-trading]
```

**Contract C-CRP-01:** Every Relay package MUST declare identity/version, interface, semantic assumptions, permissions, evidence status, provenance, limitations, and receiver obligations. A code artifact without these declarations is not a conformant CRP.

**Contract C-CRP-02:** Packages MUST preserve explicit leftover work: unresolved Residuals, failed tests, contested claims, and open questions SHOULD accompany the validated capability when relevant.

## 8. Relay handshake and receiving-context acceptance

A conformant Relay follows a staged handshake:

1. **Offer:** sender provides package manifest, evidence status, restrictions, and integrity references.
2. **Inspect:** receiver checks provenance, schema compatibility, licensing, and authority.
3. **Map:** receiver declares object/ontology/unit/time mappings and any semantic loss.
4. **Sandbox:** receiver runs contract tests and local replication under a bounded budget.
5. **Decide:** receiver records `accepted_for_research`, `accepted_for_deployment`, `rejected`, or `needs_adaptation`.
6. **Monitor:** receiver tracks performance drift, incidents, and deprecation; results MAY relay back.

```yaml
relay_event_id: relay-008
package_id: crp-0031
sender_context: lab-a
receiver_context: lab-b
mapping_version: map-04
compatibility_result: partial
local_validation_run_ids: [run-local-12]
decision: accepted_for_research
permissions_granted: [evaluate, simulate]
restrictions: ["Deployment prohibited pending new validation"]
feedback_channel: relay-feedback-08
```

**Contract C-RELAY-01:** Relay MUST NOT automatically transfer authority, secrets, credentials, production permissions, or claims of validity. The receiver MUST make and record its own acceptance decision.

**Contract C-RELAY-02:** Semantic mismatches MUST be recorded, not silently coerced. If time units, identities, objectives, or constraints cannot be reconciled, the package MUST be rejected or restricted to research-only evaluation.

## 9. Collective Learning feedback and conflict handling

Feedback MAY contain successful replication, failed replication, discovered counterexamples, improved baselines, new Residuals, or a proposed successor package. All feedback MUST reference the package and context versions being assessed.

Conflicting findings MUST coexist as separately attributable evidence until reconciled. A receiving team MUST NOT overwrite the original author's claim or erase negative evidence. Conflict resolution MAY produce a narrower scoped claim, a revised hypothesis, or a retirement decision. An append-only audit log or equivalently tamper-evident record SHOULD preserve this history.

This supports **Relay of the unfinished**: a failed transfer or unresolved discrepancy can still become a productive research object for a subsequent team.

## 10. Governance, security, and privacy

ASSI-style adversarial considerations apply to every boundary: source identity, evidence provenance, package integrity, evaluator independence, plugin supply chain, and receiving authority. Systems SHOULD use least privilege, signature or digest verification, sandbox isolation, revocation, and separation of duties for consequential actions.

- Restricted or personal data MUST NOT be copied into public Relay packages without appropriate authorization and protection.
- A successful sandbox result MUST NOT grant production permission.
- Evaluation and authorization roles SHOULD be separated for high-impact decisions.
- Packages MUST declare dependencies and externally callable effects.
- Revocation and rollback procedures MUST exist for deployed packages.
- Untrusted findings, package documentation, and model-generated instructions MUST be treated as data, not operational authority.

## 11. Conformance profiles

| Profile | Required capability | Excluded assumption |
|---|---|---|
| **V0 — Traceable Claim** | ClaimRecord, source references, status and limitations | No replication claim |
| **V1 — Reproducible Evidence** | V0 + evidence bundle and versioned protocol | No independent validation claim |
| **V2 — Independently Validated** | V1 + independent run and baseline comparison | No deployment authority |
| **V3 — Relay-Ready Capability** | V2 + CRP, handshake, receiver-local acceptance | No automatic cross-domain equivalence |
| **V4 — Governed Operational Relay** | V3 + authorization, monitoring, rollback, drift response | No guarantee of persistent advantage |

A profile MUST be claimed only if all lower profiles' obligations are satisfied. Implementations MAY support different profiles for different claims or packages.

## 12. Minimum conformance tests

| Test ID | Test | Expected outcome |
|---|---|---|
| VT-001 | Claim missing scope or evidence reference | Reject as conformant claim |
| VT-002 | Evidence changes without version update | Reject or flag integrity violation |
| VT-003 | Candidate attempts direct `validated` promotion | Reject unsupported transition |
| VT-004 | Adaptive search reuses holdout without disclosure | Flag evaluation contamination |
| VT-005 | No baseline or cost accounting for advantage claim | Reject advantage assertion |
| VT-006 | CCC reverse-direction support is circular | Reject independent two-way evidence claim |
| VT-007 | Meta-Delta modifies its own sole success criterion | Reject independent validation |
| VT-008 | Relay package omits known failure or permissions | Reject CRP conformance |
| VT-009 | Receiver changes units without declared mapping | Reject or restrict transfer |
| VT-010 | Sender marks package validated; receiver has not tested | Permit research-only, not deployment |
| VT-011 | Independent replication fails | Preserve failure; challenge or narrow claim |
| VT-012 | Revoked package remains deployable | Block deployment and trigger response |
| VT-013 | Restricted evidence appears in public manifest | Block publication or redact with audit trail |
| VT-014 | New runtime version regresses against reference baseline | Record regression; deny unqualified promotion |
| VT-015 | Discovery count rises while net validated utility falls | Do not report intelligence improvement |

A conformance report SHOULD include test IDs, inputs, expected/actual outcomes, implementation revision, evaluator identity, and unresolved deviations.

## 13. Reference validation studies

### 13.1 SQL / CDC structural discovery

Compare fixed SQL rules, stream anomaly detection, and the full WE-SIO / Residual / discovery loop under matched data access and compute budgets. Evaluate novel validated relationships, false discoveries, detection delay, investigation burden, and transfer to another schema. Preserve mapping failures and data-quality Residuals.

### 13.2 Dynamic scheduling

Compare conventional heuristics and online reoptimization with CDE/OCSRE structural evolution under changing route, demand, and capacity constraints. Measure objective improvement, constraint violations, decision latency, compute cost, and transfer across districts. Do not treat a simulated gain as an authorized real-world schedule.

### 13.3 Financial time series

Use chronological evaluation, transaction costs, slippage, regime shifts, and multiple-testing controls. Keep research simulation separate from live trading. A discovered pattern is not evidence of durable profitability until it survives appropriately designed out-of-sample and prospective testing.

### 13.4 Cross-domain Relay

Transfer a CRP between two domains with an explicit semantic mapping. Measure adaptation effort, preserved validity, new failures, and whether receiving-context performance exceeds an independently tuned local baseline. A failed transfer is informative when its boundary conditions are preserved.

## 14. Testable research hypotheses

- **H-VR-01:** Versioned evidence and explicit claim lifecycles reduce false promotion relative to untracked discovery pipelines.
- **H-VR-02:** Preserving negative results and Residual histories improves subsequent hypothesis selection under matched budgets.
- **H-VR-03:** CRPs with semantic contracts reduce transfer debugging cost compared with code-only handoffs.
- **H-VR-04:** Receiver-local revalidation detects harmful context mismatch more reliably than sender-side validation alone.
- **H-VR-05:** Independent evaluation of meta-Deltas reduces evaluator gaming and false self-improvement claims.
- **H-VR-06:** Persistent discovery with governed Relay increases *validated net utility per unit compute* over suitable baseline systems in at least some domains.
- **H-VR-07:** Explicit unresolved-question Relay produces more useful follow-on experiments than publishing positive results alone.

Each hypothesis requires prespecified metrics, representative tasks, appropriate baselines, and publication of negative outcomes. None is treated as established by this specification.

## 15. Open research questions

1. What minimum evidence envelope permits replication without disclosing sensitive source data?
2. How should provenance be maintained across probabilistic object identity resolution?
3. Which validation standards are portable across predictive, causal, and optimization claims?
4. How should evidence quality be aggregated without hiding disagreement between evaluators?
5. What is the most useful representation of semantic loss during cross-domain transfer?
6. How can Relay avoid accumulating obsolete, contradictory, or unsafe capabilities?
7. Which mechanisms prevent discovery engines from overfitting their own evaluation procedures?
8. How should benefits from a new discovery be attributed to WE-SIO, Residual, CDE, or Relay components?
9. When is retaining all Residual history less effective than selective summarization or forgetting?
10. Can collective learning improve *discovery methods* rather than only sharing discovered results?

## 16. Relationship to SPEC-001 and SPEC-002

- **SPEC-001** defines the **Object / Residual / Delta** interfaces and cross-record integrity rules.
- **SPEC-002** defines the **persistent discovery loop**, opportunity localization, candidate generation, and operational control points.
- **SPEC-003** defines the **evidence-to-claim-to-capability-to-Relay** boundary, independent verification, and receiving-context governance.

The three specifications are complementary, not a claim that the five source repositories already implement these exact records or APIs. Implementers SHOULD map their existing contracts explicitly rather than assume wire-level compatibility.

## 17. Source research repositories

1. [Adversarial Structural Security Intelligence (ASSI)](https://github.com/sizhet/Adversarial-Structural-Security-Intelligence)
2. [Dynamic Bucket Tree of Permutation (D-BTP)](https://github.com/sizhet/Dynamic-Bucket-Tree-of-Permutation-and-Directional-Structural-Evolution)
3. [Constrained Delta Evolution (CDE)](https://github.com/sizhet/Constrained-Delta-Evolution)
4. [World Entity and Structural Intelligence Operations (WE-SIO)](https://github.com/sizhet/World-Entity-and-Structural-Intelligence-Operations)
5. [Object-Centric Structural Reasoning and Evolution (OCSRE)](https://github.com/sizhet/Object-Centric-Structural-Reasoning-and-Evolution)

## 18. Closing principle

**A discovery is not yet a validated claim; a validated claim is not yet an authorized action; an authorized local capability is not automatically a transferable capability.**

The purpose of this specification is to preserve those distinctions while enabling productive Relay. Collective Learning becomes stronger when future researchers inherit not only a result, but also its evidence, limits, failed attempts, executable contracts, and unanswered questions.

---

**Research note:** Proposed v1.0.0 research contracts. No claim of external standardization, deployed conformance, or demonstrated general intelligence emergence is made.
