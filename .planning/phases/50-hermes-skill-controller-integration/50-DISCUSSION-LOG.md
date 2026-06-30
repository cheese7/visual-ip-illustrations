# Phase 50: Hermes Skill Controller Integration - Discussion Log

> **Audit trail only.** Do not use as input to planning, research, or execution agents.
> Decisions are captured in CONTEXT.md. This log preserves the alternatives considered.

**Date:** 2026-06-18
**Phase:** 50-Hermes Skill Controller Integration
**Areas discussed:** runtime controller scope, agent metadata scope, route selection, progressive loading, planning fields, generation/edit/QA dispatch, mixed-IP grouping, delivery reporting, deferred docs and validation

---

## Implementation Surface

| Option | Description | Selected |
|--------|-------------|----------|
| Runtime controller plus agent metadata | Update `SKILL.md` and `agents/openai.yaml` because RUN-04 explicitly includes agent metadata. | yes |
| Runtime controller only | Update `SKILL.md` and defer all agent metadata to Phase 51. | |
| Broad public surface update | Include README, examples, NOTICE, release checklist, and validators now. | |

**Decision:** Phase 50 updates `SKILL.md` and `agents/openai.yaml`.
**Notes:** Public docs stay Phase 51. Validator and Node work stay Phase 52.

---

## Hermes Route Activation

| Option | Description | Selected |
|--------|-------------|----------|
| Full runtime parity | Add Hermes to every runtime route surface where Cai Xukun, Go Gopher, and OpenClaw already appear. | yes |
| Minimal route selection only | Add aliases without planning, generation, QA, delivery, or mixed-IP integration. | |
| Route pack only | Rely on `routing.md` required references without controller text. | |

**Decision:** Hermes needs full runtime parity because RUN-01 through RUN-03 name route selection, progressive loading, planning, generation/edit, QA, mixed-IP, save path, and delivery behavior.

---

## Boundary Handling

| Option | Description | Selected |
|--------|-------------|----------|
| Source-reviewed uploaded-image article route | Preserve official source context, MIT license context, uploaded visual authority, product-poster boundary, mythology-drift boundary, and public sample review boundary. | yes |
| Product route | Present Hermes through product screenshots, launch graphics, web hero graphics, or CLI UI surfaces. | |
| Mythology route | Treat Greek Hermes imagery as the default visual language. | |

**Decision:** Hermes remains a source-reviewed uploaded-image article-illustration route.
**Notes:** Product-poster and mythology-drift terms must appear in generation, QA, edit, and delivery surfaces.

---

## Existing Route Compatibility

| Option | Description | Selected |
|--------|-------------|----------|
| Preserve all existing route wording | Add Hermes around current controller patterns while leaving Xiaohei default and existing explicit routes stable. | yes |
| Rename the whole skill | Change product identity from Visual IP Illustrations to Hermes-inclusive naming. | |
| Make Hermes the default | Make omitted-IP selection choose Hermes. | |

**Decision:** Visual IP Illustrations identity, `$visual-ip-illustrations`, `$ian-xiaohei-illustrations`, and omitted-IP Xiaohei behavior remain stable.

---

## Verification Architecture

| Option | Description | Selected |
|--------|-------------|----------|
| Targeted runtime checks | Use `rg` groups for route activation, loading, planning, generation/edit, QA, mixed-IP, save/delivery, metadata, and diff health. | yes |
| Full validator green gate | Repair validator and Node tests now. | |
| Visual generation smoke | Generate Hermes images in Phase 50. | |

**Decision:** Phase 50 uses targeted deterministic checks and `git diff --check`.
**Notes:** Phase 52 owns validator/Node green and release evidence. Phase 50 adds no generated images.

## Deferred Ideas

- README variants, public examples, NOTICE, release checklist, and public release copy in Phase 51.
- Validator hardening, Node tests, smoke prompts, leakage fixtures, public sample gates, and final evidence in Phase 52.
