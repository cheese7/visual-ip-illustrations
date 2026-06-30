# Phase 53: Linux Mascot Source and Route Contract - Discussion Log

> **Audit trail only.** Do not use as input to planning, research, or execution agents.
> Decisions are captured in CONTEXT.md; this log preserves the alternatives considered.

**Date:** 2026-07-01
**Phase:** 53-Linux Mascot Source and Route Contract
**Areas discussed:** Route contract, source record, uploaded visual authority, trademark and usage boundary, existing route compatibility

---

## Route Contract

| Option | Description | Selected |
|--------|-------------|----------|
| Minimal source route | Add `linux` route with `source.md` only in Phase 53, expand the full pack in Phase 54. | ✓ |
| Full route pack now | Add route metadata and every route-local pack file in Phase 53. | |

**User's choice:** Agent-selected from the user's locked autonomous decisions and existing source/route phase precedent.
**Notes:** Phase 53 success criteria cover route/source only. Phase 54 owns the full canonical pack.

---

## Source Record

| Option | Description | Selected |
|--------|-------------|----------|
| Tux source plus trademark boundary | Record Larry Ewing attribution, GIMP attribution condition, Linux Foundation trademark guidance, Linux trademark ownership context, uploaded image authority, source-image context, public sample policy, review owner, and route status. | ✓ |
| Uploaded authority only | Record only the uploaded image marker list. | |

**User's choice:** Agent-selected per explicit Phase 53 instructions, `.planning/PROJECT.md`, and `.planning/REQUIREMENTS.md`.
**Notes:** Linux Mascot is a source-reviewed route, so Tux attribution and Linux trademark-boundary context are part of the route contract.

---

## Uploaded Visual Authority

| Option | Description | Selected |
|--------|-------------|----------|
| Local uploaded image authority | Treat `/Users/longnv/Downloads/Linux-logo.jpg` as the visual authority and record local metadata plus SHA-256 in source context. | ✓ |
| Generic Tux reference | Use a general Tux web image or broad penguin description as route authority. | |

**User's choice:** Agent-selected from the user's locked decision.
**Notes:** File metadata verified during discussion: JPEG, JFIF 1.01, progressive, 8-bit, 3500x2300 pixels, 3 components, SHA-256 `071bc327e4a2814864f9e2fcdea99aa50482a92ef4e816de9d9ce5f40e17bb2a`.

---

## Trademark and Usage Boundary

| Option | Description | Selected |
|--------|-------------|----------|
| Article-illustration mascot route | Keep Linux Mascot outputs as sparse article illustrations with Tux attribution, Linux trademark attribution, uploaded-image authority, and release-review gates. | ✓ |
| Product or distro route | Treat Linux Mascot as distro branding, Linux Foundation campaign output, CLI screenshot output, web hero output, or official Linux endorsement material. | |

**User's choice:** Agent-selected per milestone out-of-scope constraints.
**Notes:** Linux Foundation trademark guidance and Linux mark ownership context are source-record requirements for downstream planning.

---

## Existing Route Compatibility

| Option | Description | Selected |
|--------|-------------|----------|
| Append explicit Linux Mascot route | Add Linux Mascot after Hermes Agent, keep Xiaohei as the only omitted-IP default, preserve existing route behavior. | ✓ |
| Reorder or broaden route matching | Rework route ordering or add broad penguin/server/kernel/distro aliases. | |

**User's choice:** Agent-selected from route-isolation history and explicit user instructions.
**Notes:** Route order and alias boundaries are compatibility-sensitive. Existing explicit routes stay intact.

## the agent's Discretion

- Exact `source.md` section ordering can follow existing source-record style.
- Linux Mascot should append after Hermes Agent in route ordering.
- Phase 53 can leave docs, controller, pack expansion, validator, and public sample evidence to Phases 54-57.

## Deferred Ideas

- Full Linux Mascot canonical pack belongs to Phase 54.
- Runtime controller and mixed-IP dispatch belong to Phase 55.
- Public docs, metadata, NOTICE, and release checklist belong to Phase 56.
- Validator, Node tests, leakage scans, trademark-boundary scans, sample gates, and release evidence belong to Phase 57.
