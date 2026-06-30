---
quick_id: 260624-khz
slug: refine-hermes-uploaded-image-identity-ma
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

# Quick Plan: Refine Hermes Uploaded-Image Identity Markers

## Goal

Refine the Hermes Agent uploaded-image identity rules so generated outputs match the user-provided reference more closely.

## Reference Read

The visible uploaded reference shows a monochrome full-body fashion figure with:

- three-quarter side-facing pose;
- blunt straight bangs;
- shoulder-length black hair with outward curled ends;
- bright white hair highlights;
- wide white over-head headset band;
- small black circular ear cup on the visible side;
- fitted black sleeveless spaghetti-strap mini dress;
- flared pleated skirt;
- small white neck/collar tag with an `A`-like mark;
- black thigh-high stockings;
- black Mary Jane platform high heels with strap and buckle;
- very long slim legs and reserved fashion-model posture.

## Problem

Current Hermes rules use broader markers such as `black bob haircut`, `headset or earpiece`, and `platform heels`. Those cues allow drift toward a generic anime assistant, ordinary bob haircut, small earpiece, or generic heels.

## Tasks

### Task 1: Refine Hermes route-local identity text

**Files:**

- `skills/visual-ip-illustrations/references/ips/hermes/index.md`
- `skills/visual-ip-illustrations/references/ips/hermes/source.md`
- `skills/visual-ip-illustrations/references/ips/hermes/style-dna.md`
- `skills/visual-ip-illustrations/references/ips/hermes/hermes-ip.md`
- `skills/visual-ip-illustrations/references/ips/hermes/composition-patterns.md`
- `skills/visual-ip-illustrations/references/ips/hermes/prompt-template.md`
- `skills/visual-ip-illustrations/references/ips/hermes/qa-checklist.md`
- `skills/visual-ip-illustrations/references/routing.md`

**Action:** Replace broad identity cues with stricter uploaded-reference cues while preserving route status, source/MIT boundaries, mythology boundary, product-poster boundary, output path, and sample gates.

**Verify:**

```bash
rg -n "wide white over-head headset band|small black circular ear cup|blunt straight bangs|shoulder-length black hair with outward curled ends|spaghetti-strap mini dress|flared pleated skirt|Mary Jane platform high heels" skills/visual-ip-illustrations/references/ips/hermes skills/visual-ip-illustrations/references/routing.md
```

**Done:** Hermes prompt, QA, source, style, identity, composition, index, and routing rules all name the stricter uploaded-reference markers.

### Task 2: Update validator and regression coverage

**Files:**

- `scripts/validate-skill-package.mjs`
- `scripts/validate-skill-package.test.mjs`

**Action:** Update Hermes marker arrays, route leakage markers, check descriptions, and regression expectations so the stricter identity markers are enforced.

**Verify:**

```bash
node scripts/validate-skill-package.mjs
node --test scripts/validate-skill-package.test.mjs
git diff --check
```

**Done:** Validator and Node tests pass with the stricter Hermes identity contract.

### Task 3: Record quick summary and state

**Files:**

- `.planning/quick/260624-khz-refine-hermes-uploaded-image-identity-ma/260624-khz-SUMMARY.md`
- `.planning/STATE.md`

**Action:** Record what changed, validation results, and add the quick task to STATE.md.

**Verify:**

```bash
rg -n "260624-khz|Refine Hermes uploaded-image identity markers" .planning/STATE.md .planning/quick/260624-khz-refine-hermes-uploaded-image-identity-ma/260624-khz-SUMMARY.md
```

**Done:** Quick task artifacts and STATE.md completion row are present.
