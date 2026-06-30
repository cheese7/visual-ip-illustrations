# Phase 57: Linux Mascot Validation and Release Evidence - Discussion Log

> **Audit trail only.** Do not use as input to planning, research, or execution agents.
> Decisions are captured in CONTEXT.md — this log preserves the alternatives considered.

**Date:** 2026-07-01
**Phase:** 57-linux-mascot-validation-and-release-evidence
**Areas discussed:** Validator matrix, Node regression suite, Route parsing and mixed-IP smoke, Public asset and generated sample gates, Release evidence

---

## Validator Matrix

| Option | Description | Selected |
|--------|-------------|----------|
| Linux-only additive checks | Add Linux-specific checks while updating shared route helpers for ten routes. | yes |
| Broad validator rewrite | Replace the per-route check matrix with a generated manifest-driven system. | |
| Defer generic manifest work | Keep manifest generation as future work and make this phase deterministic. | yes |

**User's choice:** Focus on final validator hardening for Phase 57.
**Notes:** The roadmap and requirements assign route metadata, source record, pack, docs, examples, NOTICE, release checklist, metadata drift, leakage, public sample gates, and release evidence to Phase 57. Existing manifest requirements are future scope.

---

## Node Regression Suite

| Option | Description | Selected |
|--------|-------------|----------|
| Update full matrix and fixtures | Extend current Node tests for ten-route parser behavior, Linux fixtures, public gates, generated sample gates, and full-pass output. | yes |
| Add a separate Linux-only test file | Keep existing full-matrix tests stale and test Linux separately. | |

**User's choice:** Focus on Node tests as part of Phase 57.
**Notes:** Current Node baseline fails with 94 passing and 23 failing tests because full-matrix, parser, mixed-IP, approval parser, and generated sample fixtures still reflect stale expectations.

---

## Route Parsing and Mixed-IP Smoke

| Option | Description | Selected |
|--------|-------------|----------|
| Ten-route route order | Treat Linux Mascot as the tenth route after Hermes Agent. | yes |
| Reorder routes by type | Group source-reviewed routes together or sort alphabetically. | |

**User's choice:** Preserve existing order and add Linux after Hermes Agent.
**Notes:** Phases 53-56 already implemented Linux after Hermes Agent. Phase 57 should update old nine-route and mixed-IP text expectations to ten-route expectations.

---

## Public Asset and Generated Sample Gates

| Option | Description | Selected |
|--------|-------------|----------|
| Pending-public-assets gate | Fail on Linux/Tux public assets while release checklist approval is pending. | yes |
| Approve sample assets now | Add or approve public Linux Mascot rendered samples during validation hardening. | |
| Internal/generated distinction | Keep `assets/<article-slug>-linux/` internal review separate from public sample directories. | yes |

**User's choice:** Focus on public asset gates and release evidence; public generated Linux Mascot samples remain gated.
**Notes:** Phase 56 added no Linux/Tux sample assets. Phase 57 should enforce that state and add approval parser coverage.

---

## Release Evidence

| Option | Description | Selected |
|--------|-------------|----------|
| Final evidence file | Record validator, Node, `git diff --check`, route smoke, source-boundary smoke, docs consistency, leakage scan, trademark-boundary scan, public sample gate, generated sample gate, and readiness. | yes |
| Minimal command transcript | Record only validator and Node command output. | |

**User's choice:** Produce release evidence for final readiness.
**Notes:** Evidence should include final counts and gate statuses, following Hermes, Go Gopher, Cai Xukun, and OpenClaw validation evidence precedents.

---

## the agent's Discretion

- Exact Linux check IDs and final validator matrix count may be selected during planning and implementation.
- Narrow refactors are acceptable when they reduce repeated route expectation logic and preserve readable fixture failures.

## Deferred Ideas

- Machine-readable route manifests and validator generation.
- Public generated Linux Mascot sample gallery after explicit release approval.
- Uploaded source-image hashing automation and visual regression.
- Distribution scripts for selected IP variants.
