# Phase 54: Linux Mascot Canonical Pack - Discussion Log

> **Audit trail only.** Do not use as input to planning, research, or execution agents.
> Decisions are captured in CONTEXT.md. This log preserves the alternatives considered.

**Date:** 2026-07-01
**Phase:** 54-Linux Mascot Canonical Pack
**Areas discussed:** Pack file set, route reference expansion, source authority preservation, prompt/edit/QA behavior, sample and scope boundaries, execution mode

---

## Pack File Set

| Option | Description | Selected |
|--------|-------------|----------|
| Full Linux route-local pack | Create `index.md`, preserve/refine `source.md`, and add `style-dna.md`, `linux-ip.md`, `composition-patterns.md`, `prompt-template.md`, and `qa-checklist.md` under `skills/visual-ip-illustrations/references/ips/linux/`. | yes |
| Source-only continuation | Keep Phase 54 limited to the existing source record and leave operational files for later. | |
| Shared global references | Reuse generic route references instead of Linux-specific operational files. | |

**User's choice:** Full Linux route-local pack.
**Notes:** User explicitly locked the seven-file Linux pack shape. Existing `source.md` remains the authority record and can receive only useful pack-navigation or status refinement.

---

## Route Reference Expansion

| Option | Description | Selected |
|--------|-------------|----------|
| Expand Linux `required_references` after files exist | Update `routing.md` from `references/ips/linux/source.md` to the full Linux pack list after pack creation. | yes |
| Keep source-only `required_references` | Leave Linux routing in the Phase 53 source-only state. | |
| Expand before file creation | Add missing file paths before creating the pack. | |

**User's choice:** Expand after files exist.
**Notes:** This preserves Phase 53's handoff and avoids route references pointing at missing files during implementation.

---

## Source Authority Preservation

| Option | Description | Selected |
|--------|-------------|----------|
| Preserve Phase 53 source authority exactly | Carry forward `/Users/longnv/Downloads/Linux-logo.jpg`, SHA-256, uploaded marker list, Larry Ewing, The GIMP, Linux Foundation trademark guidance, Linux mark ownership, and public sample policy. | yes |
| Derive a looser Tux identity | Use broader Tux or penguin cues without the uploaded image marker contract. | |
| Replace with external samples | Use unrelated penguin images, distro imagery, or generic Linux imagery as visual authority. | |

**User's choice:** Preserve Phase 53 source authority exactly.
**Notes:** The uploaded file and Phase 53 source record stay canonical for identity, attribution, source, trademark, and public sample gating.

---

## Prompt, Edit, and QA Behavior

| Option | Description | Selected |
|--------|-------------|----------|
| Tux as central cognitive action subject | Prompts and QA require Tux to perform the main article action in a sparse 16:9 visual metaphor. | yes |
| Tux as mascot decoration | Let Tux appear near a diagram or object while the props carry the meaning. | |
| Linux system poster framing | Use terminal, kernel, distro, or product visuals as the main visual frame. | |

**User's choice:** Tux as central cognitive action subject.
**Notes:** QA must reject generic penguin drift, distro-logo drift, missing white belly, missing yellow-orange beak, missing oversized yellow-orange webbed feet, missing seated Tux posture, official endorsement claims, passive placement, route leakage, excessive text, and copied composition. Visible labels follow the user's requested language; prompt instructions remain English.

---

## Sample and Scope Boundaries

| Option | Description | Selected |
|--------|-------------|----------|
| Gate public generated samples | Keep public generated Linux Mascot sample approval gated and create no sample images in Phase 54. | yes |
| Add public samples now | Create README or skill-local public sample images in this phase. | |
| Treat internal samples as release-approved | Allow internal generation to appear in public examples automatically. | |

**User's choice:** Gate public generated samples.
**Notes:** Phase 54 is a route-local pack discussion and planning input stage. Public samples belong behind release review and later-phase evidence.

---

## Execution Mode and Delegation Evidence

| Option | Description | Selected |
|--------|-------------|----------|
| Use subagents where available | Follow the user's subagent preference when `spawn_agent`, `wait`, and `close_agent` are exposed. | |
| Inline stage roles when subagent tools are unavailable | Use the same stage roles inline and record the runtime limitation. | yes |

**User's choice:** User requested subagents for every stage and authorized autonomous choices.
**Parent Codex thread evidence:** The parent Codex thread delegated Phase 54 stage work to subagents as part of the phases 53-57 staged rollout.
**Nested GSD runtime limitation:** Inside the Phase 54 stage agent, tool discovery exposed GitHub and CodeGraph tools but no callable `spawn_agent`, `wait`, or `close_agent`. The nested GSD role split for discussion, planning, and checking therefore ran inline inside that already-delegated stage agent.
**Notes:** The inline statements in this Phase 54 artifact describe nested role execution within the delegated stage agent. The parent thread's stage-level subagent delegation remains the outer execution context.

---

## the agent's Discretion

- Exact Markdown section ordering inside the future Linux pack files is left to the planner and executor.
- Deterministic validation marker phrasing may be added when it stays Linux route-local and English-default.
- Hermes Phase 49, Go Gopher, and OpenClaw pack files are the reusable analogs for the planner.

## Deferred Ideas

- Phase 55 owns runtime controller integration and mixed-IP dispatch.
- Phase 56 owns public docs, NOTICE, release checklist, examples, and agent metadata.
- Phase 57 owns validator hardening, Node tests, smoke prompts, public sample gates, generated sample gates, route leakage checks, trademark-boundary checks, and release evidence.
- Public generated Linux Mascot samples require release review before publication.
