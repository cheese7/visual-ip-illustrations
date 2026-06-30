# Phase 48: Hermes Source and Route Contract - Discussion Log

> **Audit trail only.** Do not use as input to planning, research, or execution agents.
> Decisions are captured in CONTEXT.md; this log preserves the alternatives considered.

**Date:** 2026-06-18
**Phase:** 48-Hermes Source and Route Contract
**Areas discussed:** Route contract, source record, uploaded visual authority, source and usage boundary, existing route compatibility

---

## Route Contract

| Option | Description | Selected |
|--------|-------------|----------|
| Minimal source route | Add `hermes` route with `source.md` only in Phase 48, expand the full pack in Phase 49. | ✓ |
| Full route pack now | Add route metadata and every route-local pack file in Phase 48. | |

**User's choice:** Agent-selected per ordered workflow and existing phase precedent.
**Notes:** Phase 48 success criteria cover route/source only. Phase 49 owns the full canonical pack.

---

## Source Record

| Option | Description | Selected |
|--------|-------------|----------|
| Official source plus uploaded authority | Record official Hermes Agent website, repository, MIT license, docs, and conversation attachment authority. | ✓ |
| Uploaded authority only | Record only the uploaded image marker list. | |

**User's choice:** Agent-selected per `.planning/PROJECT.md` and `.planning/REQUIREMENTS.md`.
**Notes:** Hermes is a source-reviewed route, so official source and MIT license context are part of the route contract.

---

## Uploaded Visual Authority

| Option | Description | Selected |
|--------|-------------|----------|
| Conversation attachment authority | Treat `Generated image 1 (16).jpeg` conversation attachment as the visual authority and avoid a local path dependency. | ✓ |
| Local path authority | Depend on `/Users/carson/Downloads/Generated image 1 (16).jpeg`. | |

**User's choice:** Agent-selected from project context.
**Notes:** The local path was unavailable from this workspace. The conversation attachment remains the authority.

---

## Source and Usage Boundary

| Option | Description | Selected |
|--------|-------------|----------|
| Article-illustration route | Keep Hermes outputs as sparse article illustrations with uploaded-character authority and official source context. | ✓ |
| Product or mythology route | Treat Hermes as product-poster, CLI screenshot, web hero, or mythological Hermes imagery by default. | |

**User's choice:** Agent-selected per milestone out-of-scope constraints.
**Notes:** Product-poster drift and mythological Hermes drift are explicit risks for later prompt and QA phases.

---

## Existing Route Compatibility

| Option | Description | Selected |
|--------|-------------|----------|
| Append explicit Hermes route | Add Hermes after Cai Xukun, keep Xiaohei as the only omitted-IP default, preserve existing route behavior. | ✓ |
| Reorder or broaden route matching | Rework route ordering or add broad assistant/logo aliases. | |

**User's choice:** Agent-selected from route-isolation history.
**Notes:** Route order and alias boundaries are compatibility-sensitive.

## the agent's Discretion

- Exact `source.md` section ordering can follow existing source-record style.
- Hermes should append after Cai Xukun in route ordering.
- Phase 48 can leave docs, controller, pack expansion, validator, and public sample evidence to Phases 49-52.

## Deferred Ideas

- Full Hermes canonical pack belongs to Phase 49.
- Runtime controller and mixed-IP dispatch belong to Phase 50.
- Public docs, metadata, NOTICE, and release checklist belong to Phase 51.
- Validator, Node tests, leakage scans, mythology-drift scans, sample gates, and release evidence belong to Phase 52.
