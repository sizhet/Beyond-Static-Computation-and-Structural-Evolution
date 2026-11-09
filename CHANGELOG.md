# Changelog

All notable changes to **Beyond Static Computation and Structural Evolution** are documented here.

This repository is a specification-first research synthesis. A release denotes a versioned **research artifact**, not proof that its hypotheses have been experimentally confirmed or that a production runtime exists.

The format follows the principles of [Keep a Changelog](https://keepachangelog.com/en/1.1.0/) and [Semantic Versioning](https://semver.org/), adapted for research documents and validation contracts.

## [Unreleased]

### Planned

- Complete and cross-check `STRUCTURAL-CLAIMS-REGISTRY.md`, including stable claim identifiers, maturity levels, evidence links, and unresolved counterarguments.
- Audit links, figure names, captions, and the ten figure placements against the final repository contents.
- Publish versioned experimental preregistrations, data provenance statements, and reproducibility packages when experiments are actually conducted.
- Record independent replication attempts, counterexamples, failed experiments, and revisions to previously proposed claims.
- Consider executable reference implementations only after specifications and conformance criteria are stable enough to support meaningful comparison.

### Release-blocking checks

Before the first tagged release, verify that all referenced files and images exist, that links resolve, that `CITATION.cff` and `.zenodo.json` match the final title/authors/version, and that the LICENSE file is present. These checks are **not** represented as completed here.

## [1.0.0] — Proposed initial research release (2026-11-08)

**Status:** Draft release scope; not a declaration that a GitHub tag, Zenodo deposit, DOI, or independent validation has occurred.

### Added — Research synthesis

- `docs/001-Five-DOI-Peaks.md`: conceptual convergence of ASSI, D-BTP, CDE, WE-SIO, and OCSRE, with attention to their distinct scopes.
- `docs/002-WE-SIO-Object-Native-Intelligence.md`: persistent object identity, state, relations, history, residuals, capabilities, Core Frame + Plugins, and SQL alignment.
- `docs/003-Structural-Evolution-Computing.md`: constrained state evolution, delta semantics, path memory, candidate generation, evaluation, and generator adaptation.
- `docs/004-Residual-First-In-Situ-Intelligence.md`: residuals as persistent, traceable computational objects supporting discovery, learning, and correction.
- `docs/005-Persistent-Structural-Discovery.md`: resource-aware observation, opportunity localization, CCC, Two-Way CCC, pattern triggering, and SEFL.
- `docs/006-Intelligence-Spillover-and-Relay.md`: evidence-bound capability packaging, transfer, feedback, and collective learning.

### Added — Specifications

- `specifications/SPEC-001-Object-Residual-Delta-Interfaces.md`: proposed interfaces and invariants for object, residual, and delta records.
- `specifications/SPEC-002-Persistent-Discovery-Loop.md`: proposed lifecycle and control contracts for continuous discovery.
- `specifications/SPEC-003-Validation-and-Relay-Contracts.md`: evidence, validation, provenance, promotion, and relay requirements.

### Added — Research governance

- `research/RESEARCH-DIVERGENCES.md`: competing interpretations, unresolved distinctions, and areas where convergence is premature.
- `research/OPEN-QUESTIONS.md`: explicit unresolved research questions.
- `research/TESTABLE-HYPOTHESES.md`: falsifiable hypotheses TH-001–TH-018, baselines, and experimental considerations.
- `research/VALIDATION-ROADMAP.md`: staged evaluation, evidence requirements, and research gates.
- `research/STRUCTURAL-CLAIMS-REGISTRY.md`: designated claim-to-evidence registry; verify completion before release.

### Added — Experimental designs

- `experiments/EXP-001-SQL-Discovery-Lab.md`: SQL/CDC semantic alignment, residual tracking, and structural discovery study design.
- `experiments/EXP-002-Dynamic-Scheduling-Lab.md`: school transportation constraints, CDE repair operators, adaptive optimization, and transfer study design.
- `experiments/EXP-003-Stock-Pattern-Lab.md`: nonstationary pattern discovery, leakage controls, walk-forward testing, and cost-aware evaluation study design.

These are **experimental protocols**, not reports of successful completed experiments. Proposed benchmarks and metrics are not empirical findings.

### Added — Repository navigation and publication support

- `README.md`: research purpose, architecture, document map, and provenance.
- `START-HERE.md`: audience-specific reading paths and study entry points.
- `CONTENTS.md`: navigable inventory and research traceability map.
- `GLOSSARY.md`: terminology and distinctions across the five source programs and the synthesis.
- `FIGURE-INDEX.md`: figure filenames, captions, insertion points, and release checks.
- `FUTURE-DIRECTIONS.md`: prioritized research directions and validation dependencies.
- `CHANGELOG.md`: versioned record of research-artifact changes and release caveats.
- `CITATION.cff`, `.zenodo.json`, `LICENSE`, and release notes: publication metadata and licensing files to be finalized and verified for the tagged release.

### Figures — Planned release inventory

The intended figure set comprises ten numbered figures, from `Fig-001-Five-DOI-Peaks-and-Structural-Convergence.png` through `Fig-010-Structural-Claims-Validation-and-Relay-Roadmap.png`, covering the six core papers, three laboratories, and validation roadmap. Inclusion in this changelog is an **inventory target**, not a claim that every final named file is already present or visually verified.

### Research boundaries

- No claim of measured superiority over dynamic programming, online optimization, incremental systems, adaptive search, control methods, or existing learning systems.
- No claim that a detected pattern is causal, profitable, generalizable, or a validated capability without appropriate tests.
- No claim that capability transfer preserves performance, permissions, or safety automatically.
- No claim that the research program constitutes demonstrated AGI, autonomous self-improvement, or a deployed intelligent system.
- Negative results and unclosed residuals remain first-class research outputs.

## Versioning policy

- **MAJOR**: Changes to foundational research semantics, object/delta/residual contracts, or validation rules that make earlier interpretations incompatible.
- **MINOR**: New research directions, experiments, specifications, or substantive hypotheses that preserve existing contracts.
- **PATCH**: Corrections, clarification, cross-reference fixes, formatting, and nonsemantic figure updates.

When a claim changes status, record the claim identifier, prior and revised wording, evidence or counterevidence, affected specifications, and the effective version. Do not silently rewrite prior validation outcomes.

## Evidence and release integrity

A research claim may be labeled **proposed**, **specified**, **conformance-tested**, **experimentally supported**, **independently replicated**, **contradicted**, or **withdrawn**. A version number does not itself upgrade evidence status. Every empirical status change should point to an accessible protocol, dataset or dataset description, evaluation code where available, results, limitations, and provenance.

Release maintainers should ensure the DOI archive corresponds to the exact Git tag and that any post-release correction is documented in a new version rather than silently changing the archived record.

## Source research repositories

1. [ASSI — Adversarial Structural Security Intelligence](https://github.com/sizhet/Adversarial-Structural-Security-Intelligence)
2. [D-BTP — Dynamic Bucket Tree of Permutation](https://github.com/sizhet/Dynamic-Bucket-Tree-of-Permutation-and-Directional-Structural-Evolution)
3. [CDE — Constrained Delta Evolution](https://github.com/sizhet/Constrained-Delta-Evolution)
4. [WE-SIO — World Entity and Structural Intelligence Operations](https://github.com/sizhet/World-Entity-and-Structural-Intelligence-Operations)
5. [OCSRE — Object-Centric Structural Reasoning and Evolution](https://github.com/sizhet/Object-Centric-Structural-Reasoning-and-Evolution)

These links identify related source programs; this synthesis does not replace their versioned specifications or evidence.

---

*Maintainer note: Update this file at each release, distinguishing completed changes from planned work and verified results from hypotheses.*
