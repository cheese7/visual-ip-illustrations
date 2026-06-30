# Quick Summary: Refine Hermes Uploaded-Image Identity Markers

## Status

Completed on 2026-06-24.

## What Changed

- Tightened Hermes Agent source-image identity markers across routing, source, style, IP, composition, prompt, and QA references.
- Replaced broad identity cues with the visible uploaded-reference markers: three-quarter side-facing pose, blunt straight bangs, outward curled shoulder-length black hair, bright white highlights, wide white over-head headset band, visible small black circular ear cup, fitted black spaghetti-strap mini dress, flared pleated skirt, small white A-like neck/collar tag, black thigh-high stockings, black Mary Jane platform high heels, very long slim legs, and reserved fashion-model posture.
- Updated Hermes validator markers, route leakage markers, and regression fixtures so future route drift is caught by automated checks.

## Evidence

The local attachment path `/Users/carson/Downloads/User attachment.jpeg` was unavailable in this workspace, so the visible image embedded in the user message was used as the visual reference.

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
- `.planning/quick/260624-khz-refine-hermes-uploaded-image-identity-ma/260624-khz-PLAN.md`
- `.planning/quick/260624-khz-refine-hermes-uploaded-image-identity-ma/260624-khz-SUMMARY.md`
- `skills/visual-ip-illustrations/references/routing.md`
- `skills/visual-ip-illustrations/references/ips/hermes/source.md`
- `skills/visual-ip-illustrations/references/ips/hermes/index.md`
- `skills/visual-ip-illustrations/references/ips/hermes/style-dna.md`
- `skills/visual-ip-illustrations/references/ips/hermes/hermes-ip.md`
- `skills/visual-ip-illustrations/references/ips/hermes/composition-patterns.md`
- `skills/visual-ip-illustrations/references/ips/hermes/prompt-template.md`
- `skills/visual-ip-illustrations/references/ips/hermes/qa-checklist.md`
- `scripts/validate-skill-package.mjs`
- `scripts/validate-skill-package.test.mjs`
