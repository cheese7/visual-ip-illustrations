---
phase: 57-linux-mascot-validation-and-release-evidence
reviewed: 2026-06-30T23:31:02Z
depth: deep
files_reviewed: 4
files_reviewed_list:
  - scripts/validate-skill-package.mjs
  - scripts/validate-skill-package.test.mjs
  - RELEASE_CHECKLIST.md
  - .planning/phases/57-linux-mascot-validation-and-release-evidence/57-RELEASE-EVIDENCE.md
findings:
  critical: 1
  warning: 2
  info: 0
  total: 3
status: issues_found
verdict: BLOCKED
---

# Phase 57: Code Review Report

**Reviewed:** 2026-06-30T23:31:02Z
**Depth:** deep
**Files Reviewed:** 4
**Status:** issues_found
**Verdict:** BLOCKED

## Review Criteria

This review explicitly applied:

- `/Users/longnv/.codex/skills/gsd-code-review/SKILL.md`: adversarial source review for bugs, security vulnerabilities, code quality defects, concrete severity, line-numbered findings, and exact fix guidance.
- `/Users/longnv/.codex/plugins/cache/sisyphuslabs/omo/4.14.1/skills/remove-ai-slops/SKILL.md`: AI slop review for over-defensive code, excessive complexity, dead code, tautological tests, deletion-only tests, unnecessary parser/normalization, oversized maintenance burden, and behavior coverage gaps.
- `/Users/longnv/.codex/plugins/cache/sisyphuslabs/omo/4.14.1/skills/programming/SKILL.md`: strict JavaScript/TypeScript-style review principles, behavior-first tests, parse-at-boundary discipline, escape-hatch avoidance, and 250 pure LOC ceiling.

## Summary

Phase 57 adds useful Linux Mascot validator coverage and the current command gates are green, but the approval parser accepts semantically pending review outcomes as complete approvals. That can release Linux Mascot public/generated samples when checklist fields still say pending, so the phase should remain blocked until the approval parser and tests reject pending/placeholder semantics across every Linux review outcome field.

## Critical Issues

### CR-01: Linux approval parser accepts pending outcome text as complete

**File:** `scripts/validate-skill-package.mjs:1903`

**Issue:** `parseLinuxApprovalLine()` treats any non-empty outcome field as present unless it exactly matches the placeholder label. Lines `1903-1924` reject labels such as `Tux source outcome`, but they accept values such as `Tux source pending`, `Linux trademark pending`, or `public-sample decision pending`. The final `complete` expression at lines `1937-1948` then returns `true` for public approval, and returns `true` for generated approval through the same shared outcome checks. This undermines `BOUNDARY-LINUX-IMG-001` and `BOUNDARY-LINUX-GEN-001`: public assets can be considered approved while release checklist outcome fields still say pending.

**Evidence:** Read-only probe against current code:

```json
{
  "publicComplete": true,
  "publicSourceOutcomePresent": true,
  "publicSourceOutcome": "Tux source pending",
  "generatedComplete": true,
  "generatedSourceOutcomePresent": true,
  "generatedSourceOutcome": "Tux source pending"
}
```

**Fix:**

Require every outcome field to contain an affirmative approval/completion term and reject pending/TBD/placeholder language. Keep this as a shared helper so public and generated Linux approvals use identical semantics.

```javascript
function approvedOutcomePresent(value, placeholderPattern) {
  return (
    Boolean(value) &&
    !placeholderPattern.test(value) &&
    /(approved|complete|granted)/i.test(value) &&
    !/(pending|tbd|todo|reviewer|approval status)/i.test(value)
  );
}

const sourceOutcomePresent = approvedOutcomePresent(sourceOutcome, /^Tux source outcome\.?$/i);
const gimpAttributionOutcomePresent = approvedOutcomePresent(
  gimpAttributionOutcome,
  /^GIMP attribution outcome\.?$/i,
);
```

Add regression cases in `scripts/validate-skill-package.test.mjs` where each Linux outcome field is set to a realistic pending value, for both `completeLinuxPublicAssetApprovalLine()` and `completeGeneratedLinuxSampleLine()`, and assert `complete === false` plus a fixture failure for `BOUNDARY-LINUX-IMG-001` or `BOUNDARY-LINUX-GEN-001`.

## Warnings

### WR-01: Validator module is far beyond the 250 pure LOC ceiling

**File:** `scripts/validate-skill-package.mjs:1`

**Issue:** The validator now measures 7,613 pure LOC. Phase 57 added 847 lines in `2ddc732` and another 34 lines in `d35c20b`, growing an already oversized validator. This violates the OMO programming and remove-ai-slops 250 pure LOC rule and makes route-specific parser logic hard to review consistently. The CR-01 pending-outcome gap is a direct symptom: similar approval parsers are copied route-by-route, and review semantics drift across large repeated blocks.

**Evidence:** `awk '!/^[[:space:]]*$/ && !/^[[:space:]]*(\/\/|#|--)/' scripts/validate-skill-package.mjs | wc -l` returned `7613`.

**Fix:** Split route-specific validator ownership by responsibility before adding more route gates. A practical split:

- `scripts/validator/approval-parsers.mjs`: public/generated approval parsers and shared approval outcome semantics.
- `scripts/validator/route-contracts.mjs`: route metadata, references, output suffix, and route isolation checks.
- `scripts/validator/checks.mjs`: check registration and CLI rendering.

Keep `scripts/validate-skill-package.mjs` as a thin CLI wrapper that imports the check set.

### WR-02: Evidence freshness gate validates marker text rather than live command evidence

**File:** `scripts/validate-skill-package.mjs:7207`

**Issue:** `VAL-LINUX-EVIDENCE-001` only checks that `57-RELEASE-EVIDENCE.md` contains strings such as `Summary: total=180 passed=180 failed=0 skipped=0`, `tests 126`, `pass 126`, and `git diff --check`. The release evidence file can be stale or hand-edited while the validator still passes. This creates implementation-mirroring evidence validation: the check verifies that the report repeats expected text, not that the command output is current.

**Evidence:** The evidence check at lines `7214-7239` is a static `assertIncludes()` list. The actual validator and Node tests pass in this review, but the gate itself has no freshness binding to command execution time, command output artifact hashes, or a generated transcript.

**Fix:** Store command transcripts under the phase evidence directory and validate recorded metadata with deterministic fields: command, exit code, timestamp, relevant summary line, and hash. At minimum, require a generated evidence block with a timestamp newer than the last source change for `scripts/validate-skill-package.mjs`, `scripts/validate-skill-package.test.mjs`, and `RELEASE_CHECKLIST.md`.

## Verification Commands

Read-only commands run during review:

```text
node scripts/validate-skill-package.mjs
Summary: total=180 passed=180 failed=0 skipped=0

node --test scripts/validate-skill-package.test.mjs
tests 126
pass 126
fail 0
duration_ms 71873.225584

git diff --check
exit 0

awk pure LOC:
scripts/validate-skill-package.mjs -> 7613
scripts/validate-skill-package.test.mjs -> 5271
```

## Residual Risks

- `scripts/validate-skill-package.test.mjs` also exceeds the 250 pure LOC ceiling at 5,271 pure LOC. It has many real fixture tests, but the route-specific approval coverage is concentrated in large repeated blocks that miss semantic pending values.
- `.omo/` remained untracked local workspace state and was preserved.

---

_Reviewed: 2026-06-30T23:31:02Z_
_Reviewer: the agent (gsd-code-reviewer)_
_Depth: deep_
