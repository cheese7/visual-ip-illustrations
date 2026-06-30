---
phase: 56-linux-mascot-public-documentation-and-release-surface
plan: 01
subsystem: public-documentation
tags: [linux-mascot, tux, public-docs, release-surface, markdown]

requires:
  - phase: 55-linux-mascot-skill-controller-integration
    provides: Linux Mascot runtime controller integration and OpenAI metadata parity
provides:
  - Linux Mascot public README coverage across root and localized variants
  - Linux Mascot copyable planning, generation, edit, mixed-IP, and smoke prompt examples
  - Linux Mascot NOTICE attribution and public sample gate
  - Linux Mascot release checklist gates and Phase 57 validation ownership
affects: [phase-57-validation, public-docs, release-checklist]

tech-stack:
  added: []
  patterns:
    - Markdown public route documentation following the Hermes public-doc pattern
    - Release-gated source-reviewed uploaded-image route surface

key-files:
  created:
    - .planning/phases/56-linux-mascot-public-documentation-and-release-surface/56-01-SUMMARY.md
  modified:
    - README.md
    - readmes/README.ar.md
    - readmes/README.de.md
    - readmes/README.es.md
    - readmes/README.fr.md
    - readmes/README.ja.md
    - readmes/README.ko.md
    - readmes/README.pt.md
    - readmes/README.ru.md
    - readmes/README.tr.md
    - readmes/README.uk.md
    - readmes/README.zh-Hant.md
    - readmes/README.zh.md
    - examples/prompts.md
    - NOTICE.md
    - RELEASE_CHECKLIST.md

key-decisions:
  - "Linux Mascot public docs follow the Hermes uploaded-image route pattern while keeping public Linux/Tux samples pending behind release review."
  - "Linux Mascot source attribution separates Tux source context from Linux word-mark and trademark guidance."
  - "Phase 57 owns validator, Node, leakage, smoke, public sample gate, generated sample gate, and final release evidence."

patterns-established:
  - "README variants use deterministic Linux Mascot route markers, raw and escaped output paths, source pointer, and public sample gate wording."
  - "Prompt examples expose Linux Mascot as the tenth mixed-IP route group with route-local references and assets/<article-slug>-linux/ output."

requirements-completed: [DOC-01, DOC-02, DOC-03, DOC-04, DOC-05]

duration: 10m
completed: 2026-06-30
---

# Phase 56 Plan 01: Linux Mascot Public Documentation and Release Surface Summary

**Linux Mascot is now visible across public docs, copyable prompts, attribution notices, and release gates as a source-reviewed Tux route without adding generated Linux/Tux public assets.**

## Performance

- **Duration:** 10m
- **Started:** 2026-06-30T21:26:14Z
- **Completed:** 2026-06-30T21:35:49Z
- **Tasks:** 3
- **Files modified:** 17

## Status

status: complete

## Accomplishments

- Added Linux Mascot route discovery, output path, escaped marker, source pointer, source-reviewed status, uploaded-image authority, attribution, trademark boundary, route isolation, product-output boundary, and public sample gate wording to `README.md` and every localized README variant.
- Added Linux Mascot canonical planning, generation, edit, route smoke, mixed-IP planning, and mixed-IP generation examples to `examples/prompts.md`, with `assets/<article-slug>-linux/` and `assets/&lt;article-slug&gt;-linux/`.
- Added Linux Mascot NOTICE attribution and release checklist gates covering Larry Ewing Tux attribution, Linux 2.0 Penguins source, The GIMP attribution condition, Linux Foundation trademark guidance, Linux mark ownership context, uploaded-image authority, public sample policy, and Phase 57 ownership.

## Requirement Coverage

- **DOC-01:** README route selection, workflow, output path, route descriptions, route reference, route facts, and maintainer validation now include Linux Mascot as explicit `source-reviewed` route id `linux`.
- **DOC-02:** `examples/prompts.md` now includes Linux Mascot planning, generation, edit, explicit route smoke, route-status smoke, mixed-IP tenth group, and `assets/<article-slug>-linux/` paths.
- **DOC-03:** `NOTICE.md` and `RELEASE_CHECKLIST.md` now include Tux source attribution, The GIMP attribution condition, Linux trademark guidance, uploaded-image authority, public sample policy, and review gates.
- **DOC-04:** Public docs preserve Xiaohei omitted-IP default, route isolation, source-reviewed status, endorsement/certification/distro-logo/product-output boundaries, and uploaded-image-only Tux output.
- **DOC-05:** Public release surfaces stay consistent across README variants, prompt examples, agent metadata parity checks, NOTICE, and release checklist.

## Task Commits

1. **Task 1: Add Linux Mascot to README Variants** - `683cca9` (docs)
2. **Task 2: Add Linux Mascot Prompt Examples** - `4486ca5` (docs)
3. **Task 3: Add Linux Notice, Release Gates, Parity Checks, and Summary** - pending at summary creation

## Files Created/Modified

- `README.md` and `readmes/README.*.md` - Linux Mascot public route inventory, output paths, escaped markers, route section, route reference, operational facts, gallery pending boundary, quick examples, workflow, directory tree, and validation ownership.
- `examples/prompts.md` - Linux Mascot canonical prompts, edit prompt, explicit smoke prompts, route-status smoke, and tenth mixed-IP route group.
- `NOTICE.md` - Linux Mascot source attribution and public sample gate.
- `RELEASE_CHECKLIST.md` - Linux Mascot Phase 57 ownership, route smoke, attribution review, public asset policy, generated sample policy, and final release review.
- `.planning/phases/56-linux-mascot-public-documentation-and-release-surface/56-01-SUMMARY.md` - Execution summary and verification evidence.

## Decisions Made

- Followed the Hermes Phase 51 public documentation pattern because Linux Mascot is also a source-reviewed uploaded-image route.
- Kept public Linux/Tux generated samples pending behind release review and added no gallery columns or image links.
- Kept Tux source attribution and Linux word-mark guidance as separate release-review contexts.

## Verification Results

All planned verification commands passed:

```bash
rg -n 'Linux Mascot|Tux|assets/<article-slug>-linux/|assets/&lt;article-slug&gt;-linux/|skills/visual-ip-illustrations/references/ips/linux/source.md|source-reviewed|Larry Ewing|The GIMP|Linux trademark|public sample review gate|route isolation|product-output boundary|distro-logo boundary' README.md readmes/README.*.md
for f in README.md readmes/README.*.md; do rg -q 'Linux Mascot' "$f" && rg -q 'assets/<article-slug>-linux/' "$f" && rg -q 'assets/&lt;article-slug&gt;-linux/' "$f" && rg -q 'skills/visual-ip-illustrations/references/ips/linux/source.md' "$f"; done
rg -n 'Xiaohei|Littlebox|Tom|Ferris|Seal|OpenClaw|Go Gopher|Cai Xukun|Hermes Agent|\$visual-ip-illustrations|\$ian-xiaohei-illustrations|Omitted visual IP|omitted IP|implicit default' README.md readmes/README.*.md
find examples/images examples/images-en skills/visual-ip-illustrations/assets/examples assets -iname '*linux*' -o -iname '*tux*'
rg -n 'Linux Mascot: canonical planning|Linux Mascot: canonical generation|Linux Mascot: edit existing image|Route Smoke: Explicit Linux Mascot|ten separate variant groups|Linux Mascot group' examples/prompts.md
rg -n 'Linux Mascot state|Linux Mascot action|Source context note|Trademark-boundary note|assets/<article-slug>-linux|assets/&lt;article-slug&gt;-linux|skills/visual-ip-illustrations/references/ips/linux/source.md|/Users/longnv/Downloads/Linux-logo.jpg|Larry Ewing|The GIMP|Linux Foundation trademark|public sample review gate|route isolation' examples/prompts.md
rg -n 'glossy black rounded penguin head and body|white face eye patches|yellow-orange beak with two nostril dots|white oval belly|oversized yellow-orange webbed feet|distro-logo|Linux Foundation logo|product-poster|CLI screenshots|web hero graphics|kernel dashboard screenshots|operating-system marketing graphics' examples/prompts.md
rg -n "Visible labels are copied exactly in the user's requested language|visible labels copied exactly in the user's requested language" examples/prompts.md
rg -n 'Linux Mascot Source Attribution|Linux Mascot Source, Trademark, Uploaded-Image Authority|Linux 2.0 Penguins|Larry Ewing|The GIMP|Linux Foundation trademark|Linux mark ownership|Linus Torvalds|assets/<article-slug>-linux/|assets/&lt;article-slug&gt;-linux/|public generated Linux Mascot samples' NOTICE.md RELEASE_CHECKLIST.md
rg -n 'Phase 57 owns|Linux Mascot route smoke|Linux Mascot Public Asset Policy|Linux Mascot Generated Sample Policy|Final Linux Mascot Release Review|Tux source outcome|GIMP attribution outcome|Linux trademark outcome|uploaded-image identity outcome|distro-logo boundary outcome|endorsement/certification boundary outcome|product-output outcome' RELEASE_CHECKLIST.md
rg -n 'Linux Mascot|Tux|assets/<article-slug>-linux|assets/&lt;article-slug&gt;-linux|source-reviewed|Larry Ewing|The GIMP|Linux trademark|references/ips/linux/source.md|\$ian-xiaohei-illustrations|\$visual-ip-illustrations|allow_implicit_invocation: true' skills/visual-ip-illustrations/SKILL.md skills/visual-ip-illustrations/agents/openai.yaml
git diff --check -- README.md readmes/README.*.md examples/prompts.md NOTICE.md RELEASE_CHECKLIST.md .planning/phases/56-linux-mascot-public-documentation-and-release-surface/56-01-SUMMARY.md
```

Public asset check result:

- Generated Linux Mascot image count: 0
- Public Linux Mascot sample asset count: 0

## Deviations from Plan

### Auto-fixed Issues

**1. [Rule 1 - Bug] Fixed mixed-IP prompt list count mismatch**
- **Found during:** Task 2 verification
- **Issue:** Two mixed-IP prompt headers said ten route groups while the inline route list still ended at Hermes Agent.
- **Fix:** Added Linux Mascot variant group to both route lists.
- **Files modified:** `examples/prompts.md`
- **Verification:** `rg -n 'ten separate variant groups|Linux Mascot variant group' examples/prompts.md`
- **Committed in:** `4486ca5`

**2. [Rule 1 - Bug] Added exact release-checklist smoke phrase**
- **Found during:** Task 3 verification
- **Issue:** The release checklist described explicit Linux smoke and Phase 57 smoke ownership, but the plan verification expected the exact phrase `Linux Mascot route smoke`.
- **Fix:** Added a Phase 57 ownership sentence with `Linux Mascot route smoke automation`.
- **Files modified:** `RELEASE_CHECKLIST.md`
- **Verification:** `rg -n 'Phase 57 owns|Linux Mascot route smoke' RELEASE_CHECKLIST.md`
- **Committed in:** pending Task 3 commit

**Total deviations:** 2 auto-fixed (Rule 1)

## Issues Encountered

- `gsd-tools` was not available as `gsd-tools` in the shell PATH. The SDK was available through `node /Users/longnv/.codex/gsd-core/bin/gsd-tools.cjs`, which was used for state loading and later metadata updates.
- `.omo/` was already untracked and was preserved unstaged.

## User Setup Required

None - no external service configuration required.

## Known Stubs

None. Stub scan found only the existing `prompt placeholders` phrase inside `RELEASE_CHECKLIST.md` release review instructions.

## Threat Flags

None. This phase changes public documentation and release-review surfaces only; it adds no runtime endpoint, auth path, schema, network behavior, or file-access implementation.

## Phase 57 Ownership

Phase 57 owns Linux Mascot validator parity, Node tests, final release evidence, docs consistency, leakage scan, route smoke, public sample gate automation, generated sample gate automation, and release evidence.

## Next Phase Readiness

Phase 57 can validate the Linux Mascot public route surface against deterministic README, prompt, NOTICE, release checklist, `SKILL.md`, `openai.yaml`, routing, and Linux pack markers.

## Self-Check: PASSED

- FOUND: `README.md`
- FOUND: `readmes/README.zh.md`
- FOUND: `examples/prompts.md`
- FOUND: `NOTICE.md`
- FOUND: `RELEASE_CHECKLIST.md`
- FOUND: `.planning/phases/56-linux-mascot-public-documentation-and-release-surface/56-01-SUMMARY.md`
- FOUND: production commits `683cca9` and `4486ca5`
- Generated Linux Mascot image count: 0
- Public Linux Mascot sample asset count: 0
- Intentional deletions: none

---
*Phase: 56-linux-mascot-public-documentation-and-release-surface*
*Completed: 2026-06-30*
