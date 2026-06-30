---
quick_id: 260624-pcg
slug: tighten-hermes-face-markers-against-the-
type: quick
status: completed
created: 2026-06-24
completed: 2026-06-24
autonomous: true
files_modified:
  - skills/visual-ip-illustrations/references/ips/hermes/index.md
  - skills/visual-ip-illustrations/references/ips/hermes/source.md
  - skills/visual-ip-illustrations/references/ips/hermes/style-dna.md
  - skills/visual-ip-illustrations/references/ips/hermes/hermes-ip.md
  - skills/visual-ip-illustrations/references/ips/hermes/composition-patterns.md
  - skills/visual-ip-illustrations/references/ips/hermes/prompt-template.md
  - skills/visual-ip-illustrations/references/ips/hermes/qa-checklist.md
  - skills/visual-ip-illustrations/references/routing.md
  - scripts/validate-skill-package.mjs
---

# Quick Plan: Tighten Hermes Face Markers

## Goal

Refine the Hermes Agent uploaded-image identity contract so the face stays aligned with the reference image.

## Reference Read

The visible uploaded reference shows a three-quarter left-facing manga-style face with large almond eyes, a slim pointed nose, small slightly parted lips, a pointed chin, and a cool reserved expression.

## Tasks

### Task 1: Add face markers to Hermes route-local references

**Files:**

- `skills/visual-ip-illustrations/references/ips/hermes/index.md`
- `skills/visual-ip-illustrations/references/ips/hermes/source.md`
- `skills/visual-ip-illustrations/references/ips/hermes/style-dna.md`
- `skills/visual-ip-illustrations/references/ips/hermes/hermes-ip.md`
- `skills/visual-ip-illustrations/references/ips/hermes/composition-patterns.md`
- `skills/visual-ip-illustrations/references/ips/hermes/prompt-template.md`
- `skills/visual-ip-illustrations/references/ips/hermes/qa-checklist.md`
- `skills/visual-ip-illustrations/references/routing.md`

**Action:** Add explicit face markers to identity notes, marker lists, prompt templates, repair prompts, QA pass checks, and failure signals.

**Verify:**

```bash
rg -n "three-quarter left-facing face|large almond eyes|slim pointed nose|small slightly parted lips|pointed chin|cool reserved expression" skills/visual-ip-illustrations/references/ips/hermes skills/visual-ip-illustrations/references/routing.md
```

### Task 2: Update validator coverage

**Files:**

- `scripts/validate-skill-package.mjs`

**Action:** Add face markers to Hermes uploaded visual markers and route leakage markers so face drift is enforced by the main validation matrix.

**Verify:**

```bash
node scripts/validate-skill-package.mjs
node --test scripts/validate-skill-package.test.mjs
git diff --check
```

### Task 3: Record quick completion

**Files:**

- `.planning/STATE.md`
- `.planning/quick/260624-pcg-tighten-hermes-face-markers-against-the-/260624-pcg-PLAN.md`
- `.planning/quick/260624-pcg-tighten-hermes-face-markers-against-the-/260624-pcg-SUMMARY.md`

**Action:** Record the completed quick task, validation results, and final commit evidence.

**Verify:**

```bash
rg -n "260624-pcg|Tighten Hermes face markers" .planning/STATE.md .planning/quick/260624-pcg-tighten-hermes-face-markers-against-the-
```
