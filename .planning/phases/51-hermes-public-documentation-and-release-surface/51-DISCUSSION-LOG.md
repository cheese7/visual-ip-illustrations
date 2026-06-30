---
phase: 51-hermes-public-documentation-and-release-surface
status: complete
date: 2026-06-18
---

# Phase 51 Discussion Log

## Decision

Proceed with one documentation-focused plan that adds Hermes Agent to all public and release-facing docs while keeping validator hardening and release evidence for Phase 52.

## Discussion Findings

- All README surfaces currently stop at Go Gopher and Cai Xukun for public route documentation.
- `examples/prompts.md` needs Hermes planning, generation, edit, smoke, and mixed-IP examples.
- `NOTICE.md` needs Hermes official source, MIT license, uploaded-image authority, route status, and public sample gate text.
- `RELEASE_CHECKLIST.md` needs Hermes smoke, attribution, source/MIT/uploaded-image review, public sample policy, and Phase 52 evidence ownership.
- `agents/openai.yaml` already includes Hermes from Phase 50 and should receive a parity check during Phase 51.
- `SKILL.md` already includes Hermes from Phase 50 and should remain the runtime authority.

## Implementation Direction

Use the existing Go Gopher and Cai Xukun public-doc pattern:

- Add Hermes as an explicit route in first-view README route summaries.
- Add Hermes to route inventory, outputs, escaped markers, route reference packs, operational facts, workflow, quick examples, mixed-IP wording, and maintainer validation notes.
- Add Hermes to every README variant with the same stable technical markers, even where surrounding prose remains localized.
- Add Hermes copyable examples to `examples/prompts.md`.
- Add Hermes source attribution and public sample gate to `NOTICE.md`.
- Add Hermes release gates to `RELEASE_CHECKLIST.md`.

## Out of Scope

- Generated Hermes sample images.
- Public Hermes gallery assets.
- Validator implementation changes.
- Node test changes.
- Leakage fixtures.
- Mythology-drift automation.
- Final release evidence.

## Acceptance

- Public docs contain Hermes raw and escaped output markers.
- Public docs contain Hermes source pointer, official source context, MIT license context, uploaded-image authority, public sample gate, mythology boundary, product-poster boundary, and route isolation wording.
- Mixed-IP examples include Hermes as a separate ninth route group.
- Public sample asset search for `*hermes*` returns no files.
- `git diff --check` passes.
