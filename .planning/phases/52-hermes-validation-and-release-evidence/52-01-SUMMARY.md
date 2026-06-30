---
phase: 52-hermes-validation-and-release-evidence
plan: 52-01
status: complete
subsystem: validation-release-evidence
tags:
  - hermes-agent
  - validator
  - release-evidence
  - node-test
requirements:
  - VAL-01
  - VAL-02
  - VAL-03
  - VAL-04
  - VAL-05
completed_at: 2026-06-18T13:57:38Z
dependency_graph:
  requires:
    - Phase 51 public documentation and release surfaces
  provides:
    - Hermes deterministic validator matrix
    - Hermes Node regression coverage
    - Phase 52 release evidence
  affects:
    - scripts/validate-skill-package.mjs
    - scripts/validate-skill-package.test.mjs
    - .planning/phases/52-hermes-validation-and-release-evidence/52-RELEASE-EVIDENCE.md
tech_stack:
  added:
    - none
  patterns:
    - dependency-free Node core validator
    - built-in node:test fixtures
    - Markdown release evidence
key_files:
  created:
    - .planning/phases/52-hermes-validation-and-release-evidence/52-RELEASE-EVIDENCE.md
  modified:
    - scripts/validate-skill-package.mjs
    - scripts/validate-skill-package.test.mjs
decisions:
  - Hermes release readiness is enforced through VAL-HERMES-EVIDENCE-001 after evidence exists.
  - Public Hermes samples remain gated while internal generated samples stay allowed under workspace output semantics.
metrics:
  duration: ~1h
  tasks: 3
  files: 3
  validator_checks: 161
  node_tests: 114
---

# Phase 52 Plan 52-01: Hermes Validation and Release Evidence Summary

Hermes Agent release readiness is now deterministic: the validator covers the ninth route, source/MIT boundary, uploaded-image markers, docs, leakage, mythology drift, sample gates, and fresh release evidence, with Node regression coverage proving the drift cases.

## Status

status: complete

## Files Changed

- `scripts/validate-skill-package.mjs`
- `scripts/validate-skill-package.test.mjs`
- `.planning/phases/52-hermes-validation-and-release-evidence/52-RELEASE-EVIDENCE.md`
- `.planning/phases/52-hermes-validation-and-release-evidence/52-01-SUMMARY.md`

## Task Commits

| Task | Name | Commit | Files |
|------|------|--------|-------|
| 1 | Normalize nine-route baseline and add Hermes validator matrix | `2c92997` | `scripts/validate-skill-package.mjs` |
| 2 | Add Hermes Node regression coverage | `51e6b15` | `scripts/validate-skill-package.test.mjs` |
| 3 | Record release evidence and enforce evidence freshness | `f67249a` | `scripts/validate-skill-package.mjs`, `scripts/validate-skill-package.test.mjs`, `52-RELEASE-EVIDENCE.md` |

## Requirement Coverage

- VAL-01: `AGENT-HERMES-001`, `ROUTE-HERMES-001`, `REFS-HERMES-001`, `PROMPT-HERMES-001`, `IP-HERMES-001`, `QA-HERMES-001`, `SOURCE-HERMES-001`, `DOC-HERMES-001`, `NOTICE-HERMES-001`, `SMOKE-HERMES-001`, `SMOKE-MIXED-HERMES-001`, `RELEASE-HERMES-001`, and `VAL-HERMES-EVIDENCE-001` cover route, source, pack, output, docs, metadata, examples, release, and evidence drift.
- VAL-02: `BOUNDARY-HERMES-LEAK-001` scans non-Hermes route-local references and legacy shared references for Hermes leakage markers.
- VAL-03: `BOUNDARY-HERMES-IMG-001` gates public generated Hermes sample assets, and `BOUNDARY-HERMES-GEN-001` preserves internal generated sample review separation.
- VAL-04: `scripts/validate-skill-package.test.mjs` covers Hermes parser primitives, route ordering, default preservation, output path markers, uploaded-image markers, source/MIT markers, mythology-drift markers, smoke prompts, leakage fixtures, public asset gates, generated sample gates, approval placeholder failures, release evidence drift, and full-pass output.
- VAL-05: `52-RELEASE-EVIDENCE.md` records validator output, Node test output, `git diff --check`, Hermes route smoke, uploaded-image smoke, source/MIT boundary smoke, docs consistency, leakage scan, mythology-drift scan, public sample gate, generated sample gate, and dirty-worktree scope.

## Verification Results

- PASS: `node scripts/validate-skill-package.mjs`
  - `Summary: total=161 passed=161 failed=0 skipped=0`
- PASS: `node --test scripts/validate-skill-package.test.mjs`
  - `tests 114`
  - `pass 114`
  - `fail 0`
- PASS: `git diff --check`
- PASS: `node scripts/validate-skill-package.mjs | rg 'VAL-HERMES-EVIDENCE-001|BOUNDARY-HERMES-(LEAK|IMG|GEN)-001|Summary:'`
- PASS: `rg -n 'VAL-01|VAL-02|VAL-03|VAL-04|VAL-05|Hermes route smoke|uploaded-image smoke|source/MIT boundary smoke|docs consistency|leakage scan|mythology-drift scan|public sample gate|generated sample gate|dirty-worktree scope' .planning/phases/52-hermes-validation-and-release-evidence/52-RELEASE-EVIDENCE.md`

## Deviations from Plan

None - plan executed as written.

## Tooling Notes

- `gsd-tools` was unavailable in the shell PATH during execution, so planning state updates were applied directly to Markdown tracking files.

## Known Stubs

None.

The stub-pattern scan found only negative parser tests for placeholder approval fields and existing prompt placeholder allowlist rules. These are validation fixtures and policy markers.

## Threat Flags

None.

## Self-Check: PASSED

- Found `scripts/validate-skill-package.mjs`.
- Found `scripts/validate-skill-package.test.mjs`.
- Found `.planning/phases/52-hermes-validation-and-release-evidence/52-RELEASE-EVIDENCE.md`.
- Found commit `2c92997`.
- Found commit `51e6b15`.
- Found commit `f67249a`.
- Final validator, Node test suite, and diff hygiene commands passed.
