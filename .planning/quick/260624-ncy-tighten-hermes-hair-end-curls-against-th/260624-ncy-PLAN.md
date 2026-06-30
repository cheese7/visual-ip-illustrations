---
quick_id: 260624-ncy
slug: tighten-hermes-hair-end-curls-against-th
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
  - scripts/validate-skill-package.test.mjs
---

# Quick Plan: Tighten Hermes Hair-End Curls

## Goal

Refine the Hermes Agent uploaded-image identity contract so hair-end curls match the reference image more closely.

## Reference Read

The visible uploaded reference shows shoulder-length black hair with blunt bangs and clearly curled hair ends. The left and right hair tips curve into large C-shaped hooks, creating a curled bob silhouette.

## Tasks

### Task 1: Refine Hermes hair marker wording

**Files:**

- `skills/visual-ip-illustrations/references/ips/hermes/index.md`
- `skills/visual-ip-illustrations/references/ips/hermes/source.md`
- `skills/visual-ip-illustrations/references/ips/hermes/style-dna.md`
- `skills/visual-ip-illustrations/references/ips/hermes/hermes-ip.md`
- `skills/visual-ip-illustrations/references/ips/hermes/composition-patterns.md`
- `skills/visual-ip-illustrations/references/ips/hermes/prompt-template.md`
- `skills/visual-ip-illustrations/references/ips/hermes/qa-checklist.md`
- `skills/visual-ip-illustrations/references/routing.md`

**Action:** Replace broad `outward curled shoulder-length hair` wording with explicit C-shaped curled hair-end wording across Hermes route-local references.

**Verify:**

```bash
rg -n "large C-shaped curled ends on both sides|missing large C-shaped curled hair ends" skills/visual-ip-illustrations/references/ips/hermes skills/visual-ip-illustrations/references/routing.md
```

### Task 2: Update validator and regression coverage

**Files:**

- `scripts/validate-skill-package.mjs`
- `scripts/validate-skill-package.test.mjs`

**Action:** Update Hermes visual marker arrays, route-block markers, leakage markers, and regression fixture expectations to enforce the curled hair-end detail.

**Verify:**

```bash
node scripts/validate-skill-package.mjs
node --test scripts/validate-skill-package.test.mjs
git diff --check
```

### Task 3: Record quick completion

**Files:**

- `.planning/STATE.md`
- `.planning/quick/260624-ncy-tighten-hermes-hair-end-curls-against-th/260624-ncy-PLAN.md`
- `.planning/quick/260624-ncy-tighten-hermes-hair-end-curls-against-th/260624-ncy-SUMMARY.md`

**Action:** Record the completed quick task, validation results, and final commit evidence.

**Verify:**

```bash
rg -n "260624-ncy|Tighten Hermes hair-end curls" .planning/STATE.md .planning/quick/260624-ncy-tighten-hermes-hair-end-curls-against-th
```
