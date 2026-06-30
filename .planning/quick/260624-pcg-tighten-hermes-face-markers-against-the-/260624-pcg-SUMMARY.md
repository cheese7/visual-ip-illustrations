# Quick Summary: Tighten Hermes Face Markers

## Status

Completed on 2026-06-24.

## What Changed

- Added face-specific Hermes Agent markers from the uploaded reference: three-quarter left-facing manga face, large almond eyes with dark upper lashes, slim pointed nose, small slightly parted lips, pointed chin, and cool reserved expression.
- Updated Hermes identity notes, marker lists, prompt templates, repair prompts, QA pass checks, and failure signals to preserve face consistency.
- Updated validator marker checks and leakage checks so face drift is enforced by the main validation matrix.

## Reference Read

The visible uploaded reference shows a three-quarter left-facing manga-style face with large almond eyes, dark upper lashes, a slim pointed nose, small slightly parted lips, a pointed chin, and a cool reserved expression.

## Validation

```bash
node scripts/validate-skill-package.mjs
# Summary: total=161 passed=161 failed=0 skipped=0

node --test scripts/validate-skill-package.test.mjs
# tests 114
# pass 114
# fail 0

git diff --check
# pass
```

## Files Changed

- `.planning/STATE.md`
- `.planning/quick/260624-pcg-tighten-hermes-face-markers-against-the-/260624-pcg-PLAN.md`
- `.planning/quick/260624-pcg-tighten-hermes-face-markers-against-the-/260624-pcg-SUMMARY.md`
- `skills/visual-ip-illustrations/references/routing.md`
- `skills/visual-ip-illustrations/references/ips/hermes/source.md`
- `skills/visual-ip-illustrations/references/ips/hermes/index.md`
- `skills/visual-ip-illustrations/references/ips/hermes/style-dna.md`
- `skills/visual-ip-illustrations/references/ips/hermes/hermes-ip.md`
- `skills/visual-ip-illustrations/references/ips/hermes/composition-patterns.md`
- `skills/visual-ip-illustrations/references/ips/hermes/prompt-template.md`
- `skills/visual-ip-illustrations/references/ips/hermes/qa-checklist.md`
- `scripts/validate-skill-package.mjs`
