# Phase 56: Linux Mascot Public Documentation and Release Surface - Discussion Log

> **Audit trail only.** Do not use as input to planning, research, or execution agents.
> Decisions are captured in CONTEXT.md - this log preserves the alternatives considered.

**Date:** 2026-07-01
**Phase:** 56-Linux Mascot Public Documentation and Release Surface
**Areas discussed:** Public documentation surface, prompt examples, NOTICE and release gates, runtime and metadata parity, public sample boundary

---

## Public Documentation Surface

| Option | Description | Selected |
|--------|-------------|----------|
| Root README only | Add Linux Mascot only to `README.md`. | |
| README plus localized variants | Add Linux Mascot to `README.md` and every `readmes/README.*.md` surface where Hermes Agent and route inventory already appear. | yes |
| Metadata-only docs | Keep README variants unchanged because `SKILL.md` and `openai.yaml` already mention Linux. | |

**User's choice:** Inferred from DOC-01, DOC-05, public docs parity history, and the user's explicit instruction to read README variants.
**Notes:** Public docs currently have no Linux Mascot markers, while `SKILL.md`, `openai.yaml`, and `routing.md` already do. Phase 56 should close that public-surface gap.

---

## Prompt Examples

| Option | Description | Selected |
|--------|-------------|----------|
| Linux planning and generation only | Add two copyable Linux prompts. | |
| Linux planning, generation, edit, mixed-IP, and smoke prompts | Match Hermes Phase 51 pattern and cover DOC-02 plus release smoke copy. | yes |
| Defer examples to validation phase | Leave `examples/prompts.md` unchanged until validator hardening. | |

**User's choice:** Inferred from DOC-02 and Phase 51 Hermes precedent.
**Notes:** The examples should use `assets/<article-slug>-linux/`, the escaped marker, Linux source pointer, uploaded-image authority, Tux attribution, Linux trademark-boundary note, public sample review gate, and route isolation.

---

## NOTICE and Release Gates

| Option | Description | Selected |
|--------|-------------|----------|
| NOTICE attribution only | Add a Linux Mascot notice section without release checklist expansion. | |
| NOTICE plus release checklist gate | Add Linux attribution/source context and a dedicated release review gate with public/generated sample policy. | yes |
| Checklist only | Add release gates but leave NOTICE unchanged. | |

**User's choice:** Inferred from DOC-03 and existing source-reviewed route pattern.
**Notes:** Release checklist should record Phase 57 ownership and keep public Linux samples pending until review fields are recorded.

---

## Runtime and Metadata Parity

| Option | Description | Selected |
|--------|-------------|----------|
| Rework runtime controller | Change Linux route selection, dispatch, QA, or delivery behavior in Phase 56. | |
| Parity check with narrow metadata edits only | Treat `SKILL.md` and `openai.yaml` as Phase 55-complete, then adjust only if public docs reveal inconsistent discovery markers. | yes |
| Ignore runtime surfaces | Update only public prose and skip metadata verification. | |

**User's choice:** Inferred from Phase 55 verification and DOC-05 parity requirement.
**Notes:** `openai.yaml` already mentions Linux Mascot, and `SKILL.md` already contains Linux route selection, planning, generation, edit, QA, save, and delivery behavior.

---

## Public Sample Boundary

| Option | Description | Selected |
|--------|-------------|----------|
| Add Linux public gallery assets now | Create or publish Linux Mascot gallery samples in README and skill assets. | |
| Document pending public sample gate | Mention Linux Mascot as pending public sample review and keep gallery assets absent. | yes |
| Hide sample status | Add route docs without public sample policy language. | |

**User's choice:** Inferred from Phase 53, 54, and 55 decisions plus DOC-03 and DOC-04.
**Notes:** Public generated Linux Mascot samples require release review before appearing in `examples/images/`, `examples/images-en/`, `skills/visual-ip-illustrations/assets/examples/`, README previews, release galleries, agent metadata previews, or public release surfaces.

---

## the agent's Discretion

- The planner may choose exact README placement by following the Hermes Agent public-doc insertion pattern.
- The planner may keep localized README prose compact while preserving exact Linux route markers, paths, source pointer, and release-gate terms.
- The planner may add deterministic validation marker wording that remains Linux-scoped and public-doc appropriate.

## Deferred Ideas

- Phase 57 validator hardening, Node tests, leakage scans, docs consistency automation, public sample gate automation, and final release evidence.
- Public generated Linux Mascot sample gallery after release approval.
