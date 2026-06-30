# Phase 52: Hermes Validation and Release Evidence - Discussion Log

> **Audit trail only.** Do not use as input to planning, research, or execution agents.
> Decisions are captured in CONTEXT.md - this log preserves the alternatives considered.

**Date:** 2026-06-18
**Phase:** 52-hermes-validation-and-release-evidence
**Areas discussed:** Validator scope, Node test/fixture strategy, Public and generated sample gates, Release evidence format, Scope boundaries

---

## Validator Scope

| Option | Description | Selected |
|--------|-------------|----------|
| Extend existing dependency-free validator | Add Hermes checks to `scripts/validate-skill-package.mjs` using current helper patterns and direct Node execution. | Yes |
| Add a manifest generator or build runtime | Introduce a generated route manifest or package-level build step to produce validator expectations. | |
| Add external validation dependencies | Use a package manager or third-party validation/test framework. | |

**User's choice:** Auto-selected existing dependency-free validator.

**Notes:** This follows Phase 42 Go Gopher and Phase 47 Cai Xukun precedent. The repository has no package manager or build runtime, and `.planning/PROJECT.md` keeps the skill package lightweight. Current validator baseline is failing with `Summary: total=145 passed=137 failed=8 skipped=0`, showing Phase 52 should extend and repair the existing matrix instead of replacing it.

---

## Node Test/Fixture Strategy

| Option | Description | Selected |
|--------|-------------|----------|
| Mirror existing route precedents with Hermes-specific coverage | Extend `scripts/validate-skill-package.test.mjs` using built-in `node:test`, fixture-copy helpers, route parser assertions, approval parser tests, leakage fixtures, public/generated sample gates, and full-pass output assertions. | Yes |
| Write only high-level smoke tests | Add a smaller Hermes smoke layer without fixture failure coverage. | |
| Introduce a separate test runner | Add Jest, Vitest, or another framework for this phase. | |

**User's choice:** Auto-selected existing Node fixture strategy with Hermes-specific coverage.

**Notes:** Phase 42 and Phase 47 both use the current Node suite style. Current Node baseline exits with `tests 105`, `pass 83`, and `fail 22`, largely because existing tests still encode old route counts and full-pass expectations.

---

## Public And Generated Sample Gates

| Option | Description | Selected |
|--------|-------------|----------|
| Keep public Hermes samples blocked and internal generated samples distinct | Public samples require complete release checklist approval; internal `assets/<article-slug>-hermes/` outputs stay separate from public sample directories. | Yes |
| Allow public Hermes samples once files exist | Treat sample presence as enough if filenames are route-specific. | |
| Block all generated Hermes outputs everywhere | Reject both internal review outputs and public rendered samples. | |

**User's choice:** Auto-selected gated public samples with internal generated sample distinction.

**Notes:** This matches Go Gopher and Cai Xukun validation precedent and Phase 51 verification, which confirmed public Hermes sample assets are absent. Phase 52 should add Hermes public sample approval parsing and generated sample review parsing.

---

## Release Evidence Format

| Option | Description | Selected |
|--------|-------------|----------|
| Create Phase 52 release evidence with exact command outputs and route-specific smoke/gate scans | Write `52-RELEASE-EVIDENCE.md` after green validation, recording exact validator, Node, diff, smoke, docs, leakage, mythology, public sample, generated sample, and scope evidence. | Yes |
| Rely on verification/UAT reports only | Skip a dedicated release evidence artifact and let later workflow reports summarize the phase. | |
| Store evidence only in validator output | Use `VAL-HERMES-EVIDENCE-001` without a human-readable release artifact. | |

**User's choice:** Auto-selected dedicated Phase 52 release evidence artifact.

**Notes:** Phase 42 release evidence is the clearest format precedent. The release evidence should become validator-covered through a Hermes evidence check after it exists.

---

## Scope Boundaries

| Option | Description | Selected |
|--------|-------------|----------|
| Preserve existing route behavior and prior Hermes deliverables | Keep Phase 52 focused on validation, Node tests, and release evidence while preserving Xiaohei default, Visual IP identity, public docs from Phase 51, and Hermes pack/controller behavior from Phases 48-50. | Yes |
| Rework Hermes docs and route copy broadly | Use Phase 52 as a cleanup pass across public docs and runtime wording. | |
| Expand into route manifest or asset hashing future work | Start future manifest/source-image-hash requirements in this phase. | |

**User's choice:** Auto-selected strict Phase 52 boundary.

**Notes:** Phase 52 may repair stale validator/test assumptions and minimal real drift exposed by validation, but it should avoid broad docs rewrites and future manifest work.

---

## Agent's Discretion

- Exact helper names, check insertion points, and check ID numbering can be chosen during planning and execution.
- Local helper arrays for Hermes are acceptable if they reduce duplication while keeping the validator dependency-free.
- Existing Cai Xukun and eight-route assertions may be updated only where required for the nine-route Hermes matrix.

## Deferred Ideas

None.
