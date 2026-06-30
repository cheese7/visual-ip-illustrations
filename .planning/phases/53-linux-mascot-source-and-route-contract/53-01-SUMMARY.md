---
phase: 53-linux-mascot-source-and-route-contract
plan: 53-01
subsystem: skill-routing
tags: [markdown, visual-ip, linux-mascot, routing, source-record]

requires:
  - phase: 52
    provides: Hermes Agent route/source, controller, docs, validation, and release evidence baseline
provides:
  - Linux Mascot explicit route metadata with `default=false`
  - Linux Mascot route-local source authority record
  - Phase 53 verification evidence for focused route/source checks
affects: [phase-54-linux-pack, phase-55-controller, phase-56-docs, phase-57-validation]

tech-stack:
  added: []
  patterns:
    - route-first source contract
    - source-reviewed uploaded-image route authority
    - focused rg and diff hygiene verification

key-files:
  created:
    - skills/visual-ip-illustrations/references/ips/linux/source.md
  modified:
    - skills/visual-ip-illustrations/references/routing.md
    - .planning/phases/53-linux-mascot-source-and-route-contract/53-01-SUMMARY.md

key-decisions:
  - "Linux Mascot uses explicit route id `linux`, display name `Linux Mascot`, status `source-reviewed`, output suffix `linux`, and `default=false`."
  - "Phase 53 keeps Linux Mascot required references limited to `references/ips/linux/source.md`; Phase 54 owns the full route-local pack."
  - "`/Users/longnv/Downloads/Linux-logo.jpg` is the uploaded visual authority for the Linux Mascot route."

patterns-established:
  - "Linux Mascot follows the route-first source/source-only contract used by recent visual IP additions."
  - "Public generated Linux Mascot samples require release review before publication."

requirements-completed: [ROUTE-01, ROUTE-02, ROUTE-03, SRC-01, SRC-02]

duration: 4min
completed: 2026-07-01
---

# Phase 53 Plan 53-01: Linux Mascot Source and Route Contract Summary

**Linux Mascot now has an explicit source-reviewed route contract and route-local source authority record using the uploaded Tux image as visual authority.**

## Performance

- **Duration:** 4min
- **Started:** 2026-06-30T19:13:01Z
- **Completed:** 2026-06-30T19:17:04Z
- **Tasks:** 3
- **Files modified:** 3

## Accomplishments

- Added Linux Mascot route selection to `routing.md` with aliases `Linux Mascot`, `Linux mascot`, `Linux`, `linux`, `Tux`, `tux`, `Linux penguin`, and `Tux penguin`.
- Added route table metadata for `linux`, `Linux Mascot`, `default=false`, output suffix `linux`, `references/ips/linux/source.md`, status `source-reviewed`, and output path `assets/<article-slug>-linux/`.
- Created `references/ips/linux/source.md` with Larry Ewing Tux attribution, The GIMP attribution condition, Linux Foundation trademark guidance, Linux mark ownership context, uploaded local image authority, visual markers, sample policy, route boundaries, distribution boundary, and review owner fields.
- Preserved Xiaohei as the only omitted-IP default and kept existing explicit routes isolated.

## Task Commits

1. **Task 1: Add Linux Mascot Routing Contract** - `a623470` (feat)
2. **Task 2: Create Linux Mascot Source Record** - `ed7d8ab` (feat)
3. **Task 3: Verify Contract and Write Summary** - pending metadata commit

## Files Created/Modified

- `skills/visual-ip-illustrations/references/routing.md` - Linux Mascot route selection rule, route table row, metadata section, output path markers, mixed-IP grouping, alias boundary copy, source/trademark context, and route boundary copy.
- `skills/visual-ip-illustrations/references/ips/linux/source.md` - Linux Mascot Tux attribution, GIMP attribution condition, Linux trademark context, uploaded-image authority, marker list, sample policy, route status, boundaries, distribution boundary, and review owner.
- `.planning/phases/53-linux-mascot-source-and-route-contract/53-01-SUMMARY.md` - Execution evidence and Phase 53 boundary record.

## Requirements Covered

- **ROUTE-01:** Explicit Linux Mascot aliases added while Xiaohei remains the omitted-IP default.
- **ROUTE-02:** Route id `linux`, display name `Linux Mascot`, output suffix `linux`, and `assets/<article-slug>-linux/` recorded.
- **ROUTE-03:** Routing metadata includes source-only required reference, uploaded-image authority, Tux source context, Linux trademark-boundary context, `source-reviewed`, and `default=false`.
- **SRC-01:** Source record includes Larry Ewing attribution, The GIMP attribution condition, Linux Foundation trademark usage URL, Linux mark URL, ownership attribution, uploaded authority, sample policy, review owner, route status, and source-image context.
- **SRC-02:** Source record includes `/Users/longnv/Downloads/Linux-logo.jpg`, SHA-256 `071bc327e4a2814864f9e2fcdea99aa50482a92ef4e816de9d9ce5f40e17bb2a`, and the stable uploaded visual marker list.

## Verification Evidence

Commands run:

```bash
rg -n 'Linux Mascot|Linux mascot|Tux penguin|source-reviewed|assets/<article-slug>-linux/|assets/&lt;article-slug&gt;-linux/|references/ips/linux/source\.md' skills/visual-ip-illustrations/references/routing.md skills/visual-ip-illustrations/references/ips/linux/source.md
```

Outcome: PASS. Matches were found in route selection, route table row, Linux Mascot metadata, output paths, and source record.

```bash
rg -n 'Larry Ewing|The GIMP|https://isc\.tamu\.edu/~lewing/linux/|https://www\.linuxfoundation\.org/legal/trademark-usage|https://www\.linuxfoundation\.org/legal/the-linux-mark|Linux is the registered trademark of Linus Torvalds in the U\.S\. and other countries|/Users/longnv/Downloads/Linux-logo\.jpg|071bc327e4a2814864f9e2fcdea99aa50482a92ef4e816de9d9ce5f40e17bb2a|glossy black rounded penguin head and body|yellow-orange beak with two nostril dots|oversized yellow-orange webbed feet|public generated Linux Mascot samples require release review|Linux Foundation logo use|distro-logo|kernel dashboard screenshots|operating-system marketing graphics' skills/visual-ip-illustrations/references/ips/linux/source.md
```

Outcome: PASS. Matches were found for Tux attribution, GIMP attribution, Linux trademark URLs, ownership attribution, uploaded local path, SHA-256, key visual markers, sample policy, distro/logo boundary, and product-output boundary.

```bash
git diff --check -- skills/visual-ip-illustrations/references/routing.md skills/visual-ip-illustrations/references/ips/linux/source.md .planning/phases/53-linux-mascot-source-and-route-contract/53-01-SUMMARY.md
```

Outcome: PASS. No whitespace errors reported.

Route inspection output:

```text
xiaohei:Xiaohei:true:illustrations:active
littlebox:Littlebox:false:littlebox:active
tom:Tom:false:tom:gated-authorized
ferris:Ferris:false:ferris:source-reviewed
seal:Seal:false:seal:active
openclaw:OpenClaw:false:openclaw:source-reviewed
gopher:Go Gopher:false:gopher:source-reviewed
caixukun:Cai Xukun:false:caixukun:gated-public-figure
hermes:Hermes Agent:false:hermes:source-reviewed
linux:Linux Mascot:false:linux:source-reviewed
```

Outcome: PASS. Linux Mascot appears after Hermes Agent, and Xiaohei remains the only `default=true` route.

Quick route smoke:

```text
PASS quick route smoke
```

Outcome: PASS. The Linux route row includes `linux`, `Linux Mascot`, `default=false`, `source-reviewed`, `references/ips/linux/source.md`, and `assets/<article-slug>-linux/`; the source file includes Larry Ewing, The GIMP, the Linux Foundation URLs, local path, SHA-256, visual markers, and sample policy.

## Decisions Made

- Linux Mascot is source-reviewed in Phase 53 because Tux source context, Linux trademark context, and uploaded local image visual authority are now recorded for maintainer review.
- Required references stay source-only in Phase 53: `references/ips/linux/source.md`.
- Broad penguin, server, kernel, distro, distro-logo, Linux Foundation, operating-system, CLI, terminal, product, brand-campaign, and generic mascot terms remain outside the Phase 53 alias set.

## Deviations from Plan

None - plan executed exactly as written.

**Total deviations:** 0 auto-fixed.
**Impact on plan:** No scope expansion.

## Issues Encountered

None.

## Known Stubs

None. Phase 53 intentionally creates the route/source contract only; full Linux Mascot pack, controller behavior, docs, release surfaces, validator expansion, and Node tests are owned by Phases 54-57.

## Threat Flags

None. The new trust-boundary surface was already covered by the plan threat model: explicit aliases, uploaded local image authority, Tux attribution, GIMP attribution, Linux trademark context, public sample policy, endorsement/certification boundaries, distro/product-output boundaries, and route-local isolation.

## User Setup Required

None - no external service configuration required.

## Phase Boundary Confirmation

Phase 53 changed only:

- `skills/visual-ip-illustrations/references/routing.md`
- `skills/visual-ip-illustrations/references/ips/linux/source.md`
- `.planning/phases/53-linux-mascot-source-and-route-contract/53-01-SUMMARY.md`

Deferred to later phases:

- Phase 54: Linux Mascot route-local pack files.
- Phase 55: `SKILL.md` controller integration.
- Phase 56: public docs, NOTICE, release checklist, examples, and metadata.
- Phase 57: validator and Node test expansion.

## Next Phase Readiness

Phase 54 can use `routing.md` and `references/ips/linux/source.md` as the source authority for the Linux Mascot canonical pack. The route id, aliases, status, output path, Tux attribution, Linux trademark context, uploaded visual markers, sample policy, and trademark/distro/product boundaries are now explicit and grep-friendly.

## Self-Check: PASSED

- `skills/visual-ip-illustrations/references/ips/linux/source.md` exists.
- `.planning/phases/53-linux-mascot-source-and-route-contract/53-01-SUMMARY.md` exists.
- Task commits `a623470` and `ed7d8ab` exist.
- Focused `rg` checks passed.
- `git diff --check` passed.
- Route order/default smoke passed.
- Quick route smoke passed.
- Scoped file boundary confirmed, with `.omo/` left untracked and unstaged.

---
*Phase: 53-linux-mascot-source-and-route-contract*
*Completed: 2026-07-01*
