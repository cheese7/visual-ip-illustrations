---
phase: 57-linux-mascot-validation-and-release-evidence
status: complete
created: 2026-06-30T22:09:02Z
research_level: level-0-codebase-patterns
requirements:
  - VAL-01
  - VAL-02
  - VAL-03
  - VAL-04
  - VAL-05
---

# Phase 57 Research: Linux Mascot Validation and Release Evidence

## Scope

Phase 57 closes the deterministic validator and Node regression gaps left by Phases 53-56 for the Linux Mascot route. The phase owns local validation, fixture coverage, public/generated sample gates, leakage scans, route smoke, and release evidence for the tenth route.

Discovery level is Level 0. The repository already has the dependency-free validator, built-in `node:test` suite, prior validation-evidence phases, and all Linux route/source/pack/docs inputs. No package install, new runtime, external API, or library selection is involved.

## Inputs Read

- `.planning/phases/57-linux-mascot-validation-and-release-evidence/57-CONTEXT.md`
- `.planning/phases/57-linux-mascot-validation-and-release-evidence/57-DISCUSSION-LOG.md`
- `.planning/phases/53-linux-mascot-source-and-route-contract/53-VERIFICATION.md`
- `.planning/phases/54-linux-mascot-canonical-pack/54-VERIFICATION.md`
- `.planning/phases/55-linux-mascot-skill-controller-integration/55-VERIFICATION.md`
- `.planning/phases/56-linux-mascot-public-documentation-and-release-surface/56-VERIFICATION.md`
- `scripts/validate-skill-package.mjs`
- `scripts/validate-skill-package.test.mjs`
- `skills/visual-ip-illustrations/references/routing.md`
- `skills/visual-ip-illustrations/references/ips/linux/*.md`
- `README.md`, `examples/prompts.md`, `NOTICE.md`, `RELEASE_CHECKLIST.md`
- `skills/visual-ip-illustrations/SKILL.md`
- `skills/visual-ip-illustrations/agents/openai.yaml`
- `.planning/phases/52-hermes-validation-and-release-evidence/52-01-PLAN.md`
- `.planning/phases/52-hermes-validation-and-release-evidence/52-RELEASE-EVIDENCE.md`
- `.planning/phases/42-go-gopher-validation-and-release-evidence/42-RELEASE-EVIDENCE.md`
- `.planning/phases/37-openclaw-validation-and-release-evidence/37-RELEASE-EVIDENCE.md`

## Current Baseline

`node scripts/validate-skill-package.mjs` exits 1:

- `Summary: total=164 passed=156 failed=8 skipped=0`
- Failing checks are stale route/reference/doc/smoke compatibility expectations:
  - `ROUTE-REFS-001`
  - `DOC-CAIXUKUN-001`
  - `SMOKE-MIXED-GOPHER-001`
  - `SMOKE-MIXED-CAIXUKUN-001`
  - `SMOKE-MIXED-HERMES-001`
  - `REBRAND-CANON-004`
  - `REBRAND-ROUTE-001`
  - `VAL-COMPAT-001`

`timeout 90s node --test scripts/validate-skill-package.test.mjs` exits 1:

- `tests 117`
- `pass 94`
- `fail 23`
- `cancelled 0`
- `skipped 0`
- `todo 0`

Primary failing groups:

- Full-matrix tests expect the validator to exit 0 while current validator exits 1.
- Parser primitive test expects 9 routes while routing now has 10.
- Mixed-IP fixtures still expect nine-route text for Cai Xukun and Hermes surfaces.
- Route drift fixtures assert old route-count failure messages.
- Public asset and generated sample fixtures for existing routes inherit the current validator failures.

## Confirmed Linux Contract

`routing.md` already contains Linux Mascot after Hermes Agent with:

- id `linux`
- display name `Linux Mascot`
- aliases `Linux Mascot`, `Linux mascot`, `Linux`, `linux`, `Tux`, `tux`, `Linux penguin`, `Tux penguin`
- `default=false`
- `output_suffix=linux`
- seven ordered required references under `references/ips/linux/`
- `source-reviewed`
- raw path `assets/<article-slug>-linux/`
- escaped path `assets/&lt;article-slug&gt;-linux/`

The Linux route-local pack already contains deterministic markers for:

- `/Users/longnv/Downloads/Linux-logo.jpg`
- SHA-256 `071bc327e4a2814864f9e2fcdea99aa50482a92ef4e816de9d9ce5f40e17bb2a`
- Larry Ewing
- Linux 2.0 Penguins source URL
- The GIMP attribution condition
- Linux Foundation trademark guidance
- Linux mark ownership context
- glossy black rounded penguin head and body
- white face eye patches
- large oval eyes with dark pupils and small highlights
- yellow-orange beak with two nostril dots
- white oval belly
- long black flippers
- seated rounded posture
- oversized yellow-orange webbed feet
- distro-logo boundary
- Linux Foundation logo boundary
- official endorsement, certification, and compatibility boundaries
- product-output boundaries for poster, CLI screenshot, web hero, kernel dashboard, and operating-system marketing output

## Reusable Implementation Patterns

- `outputPathTokens()` and `publicDocsOutputPathTokens()` enumerate raw and escaped route paths.
- `routeRows()` and `routeReferencePaths(row)` parse `routing.md`.
- `rebrandRouteExpectations()`, `assertRebrandRouteTable()`, and `assertPhase28CompatibilitySurface()` encode stable route ordering and compatibility checks.
- Existing route helpers use `openclawPlannedReferences()`, `gopherPlannedReferences()`, `caixukunPlannedReferences()`, and `hermesPlannedReferences()` patterns.
- Public sample gates use route-specific `parsePublic*SampleApproval()` helpers.
- Generated sample gates use route-specific `parseGenerated*SampleApproval()` helpers.
- Boundary checks scan `examples/images`, `examples/images-en`, and `skills/visual-ip-illustrations/assets/examples`.
- Release evidence checks use `VAL-*-EVIDENCE-001` IDs and assert command, smoke, docs, leakage, sample gate, and requirement markers.

## Recommended Plan Shape

Use one execution plan with three tasks:

1. Update the dependency-free validator for the ten-route Linux contract.
2. Update Node regression fixtures and parser tests for Linux and the refreshed ten-route matrix.
3. Create Phase 57 release evidence and add validator/test coverage for evidence freshness.

This mirrors Phase 52 Hermes validation hardening and keeps the hardest constraint first: making the local validator green against the live ten-route package.

## Package Legitimacy Audit

No npm, pip, or cargo installs are planned. The phase uses only local Node built-ins already used by the repository.

## Out-of-Scope Items Excluded From Planning

- Machine-readable route manifest generation.
- Public Linux/Tux gallery assets.
- Uploaded source-image storage and hashing automation.
- Visual regression or comparison sheets.
- Distribution scripts for selected IP variants.
