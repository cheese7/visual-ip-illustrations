# Phase 55: Linux Mascot Skill Controller Integration - Discussion Log

> **Audit trail only.** Do not use as input to planning, research, or execution agents.
> Decisions are captured in CONTEXT.md - this log preserves the alternatives considered.

**Date:** 2026-07-01
**Phase:** 55-Linux Mascot Skill Controller Integration
**Areas discussed:** Runtime controller surface, Linux route invocation and dispatch, Mixed-IP isolation, Delivery and metadata

---

## Runtime Controller Surface

| Option | Description | Selected |
|--------|-------------|----------|
| `SKILL.md` only | Match Phase 45 style and leave agent metadata to the public docs phase. | |
| `SKILL.md` plus `agents/openai.yaml` | Match Phase 50 Hermes style because RUN-04 explicitly names agent metadata. | yes |
| Broader public docs pass | Include README, examples, NOTICE, and release checklist in controller integration. | |

**User's choice:** Inferred from Phase 55 RUN-04 and Hermes Phase 50 precedent.
**Notes:** Phase 56 owns public docs and release surfaces. Phase 55 should update `agents/openai.yaml` only for route discovery metadata required by RUN-04.

---

## Linux Route Invocation and Dispatch

| Option | Description | Selected |
|--------|-------------|----------|
| Minimal route mention | Add Linux Mascot only to route overview and save paths. | |
| Full controller parity | Add Linux Mascot to selection, progressive loading, planning, generation, edit, QA, save, delivery, and route-leakage guard. | yes |
| Rework route loading model | Introduce a new generic route controller abstraction. | |

**User's choice:** Inferred from RUN-01 and established route-controller pattern.
**Notes:** Phase 55 should consume the Phase 54 seven-file Linux pack instead of redefining detailed style, identity, prompt, and QA rules in `SKILL.md`.

---

## Mixed-IP Isolation

| Option | Description | Selected |
|--------|-------------|----------|
| Append Linux to existing mixed-IP list | Add Linux Mascot as another route group with its own references and output path. | yes |
| Merge Linux with generic mascot handling | Treat Linux Mascot through broad mascot words or shared mascot rules. | |
| Defer mixed-IP wording | Keep single-route Linux behavior first and leave mixed-IP to later docs. | |

**User's choice:** Inferred from RUN-02 and routing.md mixed-IP contract.
**Notes:** Linux Mascot must stay explicit. Broad penguin, server, kernel, distro, Linux Foundation, operating-system, CLI, terminal, product, brand-campaign, and generic mascot terms stay outside the alias set.

---

## Delivery and Metadata

| Option | Description | Selected |
|--------|-------------|----------|
| Basic delivery fields | Report selected IP, image count, purpose, saved path, and stability notes only. | |
| Linux source/trademark delivery fields | Add uploaded-image authority, source/trademark note, source pointer, public sample boundary, route isolation, and route stability. | yes |
| Public release copy | Add README and release-checklist language together with delivery fields. | |

**User's choice:** Inferred from RUN-03 and RUN-04.
**Notes:** Linux Mascot delivery should preserve `source-reviewed`, `/Users/longnv/Downloads/Linux-logo.jpg`, `references/ips/linux/source.md`, Larry Ewing Tux attribution, The GIMP attribution condition, Linux trademark-boundary context, and `assets/<article-slug>-linux/`.

---

## the agent's Discretion

- The planner may choose exact paragraph placement by following Hermes Agent, Cai Xukun, Go Gopher, and OpenClaw controller precedents.
- The planner may keep runtime wording compact because Linux route-local references carry detailed style, prompt, edit, and QA rules.
- The planner should use targeted `rg` checks and `git diff --check`; full validator and Node updates stay in Phase 57.

## Deferred Ideas

- Phase 56 public documentation and release surfaces.
- Phase 57 validator hardening, Node tests, leakage scans, public sample gates, and release evidence.
- Public generated Linux Mascot gallery after release approval.
