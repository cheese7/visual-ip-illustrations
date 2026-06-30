---
phase: 48-hermes-source-and-route-contract
plan: 48-01
subsystem: skill-routing
tags: [markdown, visual-ip, hermes, routing, source-record]

requires:
  - phase: 47
    provides: Cai Xukun route/source precedent and existing eight-route routing baseline
provides:
  - Hermes Agent explicit route metadata with `default=false`
  - Hermes Agent route-local source authority record
  - Phase 48 verification evidence for focused route/source checks
affects: [phase-49-hermes-pack, phase-50-controller, phase-51-docs, phase-52-validation]

tech-stack:
  added: []
  patterns:
    - route-first source contract
    - source-reviewed uploaded-image route authority
    - focused rg and diff hygiene verification

key-files:
  created:
    - skills/visual-ip-illustrations/references/ips/hermes/source.md
  modified:
    - skills/visual-ip-illustrations/references/routing.md
    - .planning/phases/48-hermes-source-and-route-contract/48-01-SUMMARY.md

key-decisions:
  - "Hermes Agent uses explicit route id `hermes`, display name `Hermes Agent`, status `source-reviewed`, output suffix `hermes`, and `default=false`."
  - "Phase 48 keeps Hermes required references limited to `references/ips/hermes/source.md`; Phase 49 owns the full route-local pack."
  - "Conversation attachment `Generated image 1 (16).jpeg` is the uploaded visual authority for the Hermes Agent route."

patterns-established:
  - "Hermes Agent follows the route-first source/source-only contract used by recent visual IP additions."
  - "Public generated Hermes samples require release review before publication."

requirements-completed: [ROUTE-01, ROUTE-02, ROUTE-03, SRC-01, SRC-02]

duration: 4min
completed: 2026-06-18
---

# Phase 48 Plan 48-01: Hermes Source and Route Contract Summary

**Hermes Agent now has an explicit source-reviewed route contract and route-local source authority record using the uploaded conversation attachment as visual authority.**

## Performance

- **Duration:** 4min
- **Started:** 2026-06-18T10:34:13Z
- **Completed:** 2026-06-18T10:37:58Z
- **Tasks:** 3
- **Files modified:** 3

## Accomplishments

- Added Hermes Agent route selection to `routing.md` with aliases `Hermes Agent`, `Hermes`, `hermes`, `hermes-agent`, `Hermes logo`, and `Hermes Agent logo`.
- Added route table metadata for `hermes`, `Hermes Agent`, `default=false`, output suffix `hermes`, `references/ips/hermes/source.md`, status `source-reviewed`, and output path `assets/<article-slug>-hermes/`.
- Created `references/ips/hermes/source.md` with official source URLs, MIT license URL, docs URL, uploaded image authority, visual markers, sample policy, route boundaries, distribution boundary, and review owner fields.
- Preserved Xiaohei as the only omitted-IP default and kept existing explicit routes isolated.

## Task Commits

1. **Task 1: Add Hermes Routing Contract** - `6d9c4c3` (feat)
2. **Task 2: Create Hermes Source Record** - `c4c9f01` (feat)
3. **Task 3: Verify Contract and Write Summary** - pending metadata commit

## Files Created/Modified

- `skills/visual-ip-illustrations/references/routing.md` - Hermes route selection rule, route table row, metadata section, output path markers, mixed-IP grouping, and alias/boundary copy.
- `skills/visual-ip-illustrations/references/ips/hermes/source.md` - Hermes official source/license context, uploaded-image authority, marker list, sample policy, route status, boundaries, distribution boundary, and review owner.
- `.planning/phases/48-hermes-source-and-route-contract/48-01-SUMMARY.md` - Execution evidence and Phase 48 boundary record.

## Requirements Covered

- **ROUTE-01:** Explicit Hermes aliases added while Xiaohei remains the omitted-IP default.
- **ROUTE-02:** Route id `hermes`, display name `Hermes Agent`, output suffix `hermes`, and `assets/<article-slug>-hermes/` recorded.
- **ROUTE-03:** Routing metadata includes source-only required reference, uploaded-image authority, official source context, `source-reviewed`, and `default=false`.
- **SRC-01:** Source record includes official website, repository, MIT license, documentation URL, third-party icon context, uploaded authority, sample policy, review owner, route status, and source-image context.
- **SRC-02:** Source record includes `Generated image 1 (16).jpeg` and the stable uploaded visual marker list.

## Verification Evidence

Commands run:

```bash
rg -n 'Hermes Agent|hermes-agent|Hermes logo|Hermes Agent logo|source-reviewed|assets/<article-slug>-hermes/|assets/&lt;article-slug&gt;-hermes/|references/ips/hermes/source\.md' skills/visual-ip-illustrations/references/routing.md skills/visual-ip-illustrations/references/ips/hermes/source.md
```

Outcome: PASS. Matches were found in route selection, route table row, Hermes metadata, output paths, and source record.

```bash
rg -n 'https://hermes-agent\.nousresearch\.com/|https://github\.com/NousResearch/hermes-agent|https://github\.com/NousResearch/hermes-agent/blob/main/LICENSE|https://hermes-agent\.nousresearch\.com/docs/|Generated image 1 \(16\)\.jpeg|monochrome full-body logo-style character|black bob haircut with bright highlights|headset or earpiece|black sleeveless dress|white collar tag with an `A`-like mark|black thigh-high stockings|platform heels|slender fashion-figure posture|winged sandals|caduceus|product-poster output|public generated Hermes samples require release review' skills/visual-ip-illustrations/references/ips/hermes/source.md
```

Outcome: PASS. Matches were found for official URLs, uploaded attachment marker, all visual markers, mythology-drift markers, product boundary, and public sample policy.

```bash
git diff --check -- skills/visual-ip-illustrations/references/routing.md skills/visual-ip-illustrations/references/ips/hermes/source.md .planning/phases/48-hermes-source-and-route-contract/48-01-SUMMARY.md
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
```

Outcome: PASS. Hermes appears after Cai Xukun, and Xiaohei remains the only `default=true` route.

## Decisions Made

- Hermes Agent is source-reviewed in Phase 48 because official Hermes Agent source context, MIT license context, and uploaded-image visual authority are now recorded for maintainer review.
- Required references stay source-only in Phase 48: `references/ips/hermes/source.md`.
- Broad assistant, AI agent, logo, anime, monochrome girl, fashion figure, Greek messenger, winged sandals, and caduceus terms remain outside the Phase 48 alias set.

## Deviations from Plan

None - plan executed exactly as written.

**Total deviations:** 0 auto-fixed.
**Impact on plan:** No scope expansion.

## Issues Encountered

None.

## Known Stubs

None. Phase 48 intentionally creates the route/source contract only; full Hermes pack, controller behavior, docs, release surfaces, validator expansion, and Node tests are owned by Phases 49-52.

## Threat Flags

None. The new trust-boundary surface was already covered by the plan threat model: explicit aliases, uploaded attachment authority, source/license context, public sample policy, claim boundaries, mythology-drift boundaries, and route-local isolation.

## User Setup Required

None - no external service configuration required.

## Phase Boundary Confirmation

Phase 48 changed only:

- `skills/visual-ip-illustrations/references/routing.md`
- `skills/visual-ip-illustrations/references/ips/hermes/source.md`
- `.planning/phases/48-hermes-source-and-route-contract/48-01-SUMMARY.md`

Deferred to later phases:

- Phase 49: Hermes route-local pack files.
- Phase 50: `SKILL.md` controller integration.
- Phase 51: public docs, NOTICE, release checklist, examples, and metadata.
- Phase 52: validator and Node test expansion.

## Next Phase Readiness

Phase 49 can use `routing.md` and `references/ips/hermes/source.md` as the source authority for the Hermes canonical pack. The route id, aliases, status, output path, official source URLs, uploaded visual markers, sample policy, and product/mythology boundaries are now explicit and grep-friendly.

## Self-Check: PASSED

- `skills/visual-ip-illustrations/references/ips/hermes/source.md` exists.
- `.planning/phases/48-hermes-source-and-route-contract/48-01-SUMMARY.md` exists.
- Task commits `6d9c4c3` and `c4c9f01` exist.
- Focused `rg` checks passed.
- `git diff --check` passed.
- Scoped file boundary confirmed.

---
*Phase: 48-hermes-source-and-route-contract*
*Completed: 2026-06-18*
