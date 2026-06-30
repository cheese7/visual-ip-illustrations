---
phase: 57-linux-mascot-validation-and-release-evidence
plan: 01
subsystem: validation
tags: [node, validator, linux-mascot, release-evidence, codex-skill]
requires:
  - phase: 56-linux-mascot-public-documentation-and-release-surface
    provides: Linux Mascot public docs, NOTICE, release checklist, skill metadata, and route surfaces
provides:
  - Linux Mascot validator matrix covering route, source, docs, NOTICE, release, smoke, leakage, public sample, and generated sample gates
  - Node regression coverage for Linux Mascot parser, drift fixtures, approval parsing, and generated sample distinction
  - Phase 57 release evidence with validator, Node test, diff-check, smoke, source-boundary, docs, leakage, sample-gate, and readiness proof
affects: [validator, release-evidence, linux-mascot, visual-ip-routes]
tech-stack:
  added: []
  patterns:
    - dependency-free Node validator checks
    - route-local Linux Mascot drift fixtures
    - release evidence freshness gate
key-files:
  created:
    - .planning/phases/57-linux-mascot-validation-and-release-evidence/57-RELEASE-EVIDENCE.md
  modified:
    - scripts/validate-skill-package.mjs
    - scripts/validate-skill-package.test.mjs
    - RELEASE_CHECKLIST.md
key-decisions:
  - "Keep Linux Mascot public rendered assets gated until complete release checklist approval exists."
  - "Use VAL-LINUX-EVIDENCE-001 to keep Phase 57 release evidence fresh and machine-checked."
patterns-established:
  - "Linux route validation mirrors Hermes/Gopher evidence structure with route-specific source, trademark, and sample gates."
  - "Public and generated Linux sample approvals are parsed separately so workspace outputs do not imply public release approval."
requirements-completed: [VAL-01, VAL-02, VAL-03, VAL-04, VAL-05]
duration: 1h
completed: 2026-06-30
---

# Phase 57 Plan 01: Linux Mascot Validation Hardening and Release Evidence Summary

**Linux Mascot validation now has deterministic route, docs, leakage, sample-gate, Node regression, and release-evidence coverage.**

## Performance

- **Duration:** ~1h
- **Started:** 2026-06-30T22:00:00Z
- **Completed:** 2026-06-30T23:02:08Z
- **Tasks:** 3
- **Files modified:** 5

## Accomplishments

- Added Linux Mascot validator checks for route metadata, required references, prompt/IP/QA/source markers, public docs, NOTICE, release checklist, route smoke, mixed-route smoke, leakage, public sample gate, generated sample gate, and final evidence.
- Added Node fixture coverage for Linux route parsing, ordering, default preservation, output path markers, source/trademark markers, release surface drift, leakage, approval placeholders, public sample gates, and generated sample separation.
- Recorded Phase 57 release evidence and added `VAL-LINUX-EVIDENCE-001` so the validator checks the evidence file itself.

## Task Commits

1. **Task 1: Validator matrix** - `2ddc732` (`feat`)
2. **Task 2: Node tests and release checklist alignment** - `bf2886d` (`test`)
3. **Task 3: Release evidence and evidence freshness gate** - `d35c20b` (`docs`)

## Files Created/Modified

- `scripts/validate-skill-package.mjs` - Linux Mascot validator checks, approval parsers, boundary gates, and Phase 57 evidence gate.
- `scripts/validate-skill-package.test.mjs` - Linux Mascot parser assertions, drift fixtures, approval fixtures, generated sample fixtures, and final matrix totals.
- `RELEASE_CHECKLIST.md` - Linux public asset approval template now includes the article-metaphor quality outcome required by the Phase 57 plan.
- `.planning/phases/57-linux-mascot-validation-and-release-evidence/57-RELEASE-EVIDENCE.md` - Final release evidence for VAL-01 through VAL-05.
- `.planning/phases/57-linux-mascot-validation-and-release-evidence/57-01-SUMMARY.md` - This execution summary.

## Verification

- `node scripts/validate-skill-package.mjs` -> `Summary: total=180 passed=180 failed=0 skipped=0`
- `node --test scripts/validate-skill-package.test.mjs` -> `tests 126`, `pass 126`, `fail 0`
- `git diff --check` -> exit 0
- Evidence marker grep passed for VAL-01 through VAL-05, route smoke, uploaded-image/source-boundary smoke, docs consistency, leakage scan, trademark-boundary scan, public sample gate status, generated sample gate status, public asset absence, and release readiness.

## Decisions Made

- Linux public approval parsing remains route-specific and requires source, GIMP attribution, Linux trademark, uploaded-image identity, distro-logo boundary, endorsement/certification boundary, product-output boundary, route isolation, uploaded-image-only output, article-metaphor quality, and public-sample decision fields.
- Generated Linux sample review stays separate from public rendered sample approval, with internal review paths under `assets/<article-slug>-linux/` and public directories checked independently.

## Deviations from Plan

### Auto-fixed Issues

**1. [Rule 2 - Missing Critical] Added article-metaphor outcome to Linux public asset approval template**
- **Found during:** Task 2
- **Issue:** The Phase 57 D-15 field list required article-metaphor quality outcome for public Linux sample approval, while `RELEASE_CHECKLIST.md` only had uploaded-image-only and public-sample fields.
- **Fix:** Added the article-metaphor quality outcome to the Linux public asset policy line and aligned Node approval builders and parser tests.
- **Files modified:** `RELEASE_CHECKLIST.md`, `scripts/validate-skill-package.test.mjs`
- **Verification:** `node scripts/validate-skill-package.mjs`, `node --test scripts/validate-skill-package.test.mjs`
- **Committed in:** `bf2886d`

**Total deviations:** 1 auto-fixed Rule 2 item.

## Issues Encountered

- Initial Linux public approval parser/test alignment exposed a field-position mismatch. The final implementation keeps the public and generated approval paths explicit and independently tested.
- `gsd-tools` was not on PATH, so state updates used the local GSD core entrypoint `node /Users/longnv/.codex/gsd-core/bin/gsd-tools.cjs`.

## Known Stubs

None.

## Threat Flags

None.

## User Setup Required

None.

## Next Phase Readiness

Phase 57 closes the v1.11 Linux Mascot validation milestone: validator, tests, release evidence, and sample gates are green. `.omo/` remains unrelated untracked local workspace state and was preserved.

## Self-Check: PASSED

- Summary file exists.
- Release evidence file exists.
- Task commits exist: `2ddc732`, `bf2886d`, `d35c20b`.
- Final verification commands passed.

---
*Phase: 57-linux-mascot-validation-and-release-evidence*
*Completed: 2026-06-30*
