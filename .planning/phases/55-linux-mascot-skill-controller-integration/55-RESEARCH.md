# Phase 55: Linux Mascot Skill Controller Integration - Research

**Researched:** 2026-07-01  
**Domain:** Documentation-driven Codex Skill runtime controller integration for a source-reviewed uploaded-image Linux Mascot visual IP route  
**Confidence:** HIGH

## Summary

Phase 55 should wire the already-complete Linux Mascot route metadata and seven-file route-local pack into the Visual IP Illustrations runtime controller.

The implementation surface is narrow:

- `skills/visual-ip-illustrations/SKILL.md`
- `skills/visual-ip-illustrations/agents/openai.yaml`

`routing.md` already defines the `linux` route, aliases, `default=false`, output suffix `linux`, output path `assets/<article-slug>-linux/`, escaped path marker, route status `source-reviewed`, source/trademark context, uploaded-image authority, and seven required references. Phase 54 already created the Linux route-local operational pack with planning fields, generation prompt, edit gates, QA gates, and delivery wording.

Primary recommendation: create one execution plan with three sequential tasks inside the same plan because all runtime behavior flows through `SKILL.md`. Task 1 activates route selection and progressive loading. Task 2 adds planning, generation, edit, QA, and mixed-IP dispatch. Task 3 adds save/delivery/reporting guards and `agents/openai.yaml` metadata.

## User Constraints From CONTEXT.md

### Locked Decisions

- D-01: Phase 55 owns runtime controller behavior in `skills/visual-ip-illustrations/SKILL.md`.
- D-02: Phase 55 owns the agent metadata slice required by RUN-04 in `skills/visual-ip-illustrations/agents/openai.yaml`.
- D-03: Existing route behavior for omitted-IP Xiaohei and explicit Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, and Hermes Agent must stay stable.
- D-04: Public docs and validation stay with Phases 56 and 57.
- D-05: Linux Mascot must be added across `SKILL.md` route overview, loading, selection, planning, generation, edit, QA, save, and delivery surfaces.
- D-06: Linux Mascot selection uses exactly the listed aliases and keeps broad penguin/server/kernel/distro/Linux Foundation/OS/CLI/terminal/product/brand/generic mascot terms outside Linux route selection.
- D-07: Linux progressive loading points to the Phase 54 seven-file pack.
- D-08: Runtime wording carries uploaded-image authority from `/Users/longnv/Downloads/Linux-logo.jpg`, Tux attribution, The GIMP attribution condition, Linux trademark-boundary context, source pointer, public sample review boundary, route isolation, and `assets/<article-slug>-linux/`.
- D-09: Linux Mascot planning entries mirror `references/ips/linux/prompt-template.md`.
- D-10: Generation and edit dispatch use Linux prompt, composition, and QA references.
- D-11: Mixed-IP workflows include Linux Mascot as a separate route group.
- D-12: Each mixed-IP route group loads only its own references, prompt template, QA checklist, edit gates, route note, suffix, and output directory.
- D-13: Linux mixed-IP groups use `assets/<article-slug>-linux/` and include source-reviewed status, source pointer, uploaded-image authority note, Tux source attribution note, Linux trademark-boundary note, public sample boundary, and route isolation.
- D-14: Linux delivery reports include selected visual IP, image count, purpose per image, saved path, uploaded-image authority note, source/trademark note, route status, source pointer, public sample boundary when relevant, and route stability notes.
- D-15: Route-leakage delivery guard includes Linux Mascot and the full source/trademark/output-path guard set.
- D-16: `SKILL.md` presents Linux Mascot as a selectable source-reviewed uploaded-image route while preserving Visual IP Illustrations identity and legacy `$ian-xiaohei-illustrations`.
- D-17: `agents/openai.yaml` adds Linux Mascot to display name, short description, and default prompt while preserving existing route descriptions.

### Deferred Scope

- Phase 56 owns README variants, `examples/prompts.md`, NOTICE, release checklist, public release copy, and public sample surfaces.
- Phase 57 owns validator coverage, Node tests, leakage scans, trademark-boundary scans, public sample gates, generated sample gates, route smoke, uploaded-image and source-boundary smoke, docs consistency, and release evidence.
- Generated Linux Mascot images and public sample assets stay outside Phase 55.

## Phase Requirements

| ID | Requirement | Research Support |
|----|-------------|------------------|
| RUN-01 | User can invoke Linux Mascot through controller route selection, progressive loading, planning fields, generation dispatch, edit routing, QA dispatch, and delivery reports. | Add Linux to every relevant `SKILL.md` controller section using the Phase 54 seven-file pack. |
| RUN-02 | User can request mixed-IP output where Linux Mascot and all existing routes create separate route groups with their own references, prompts, QA rules, and output paths. | Add Linux to mixed-IP shot-list, generation, save, and delivery blocks with route-local references and `assets/<article-slug>-linux/`. |
| RUN-03 | User receives Linux Mascot delivery reports with selected IP, image count, purpose per image, saved path, uploaded-image authority note, source/trademark note, and route stability notes. | Add single-route delivery rule, mixed-route delivery block, and route-leakage delivery guard. |
| RUN-04 | Agent metadata and skill instructions present Linux Mascot while preserving Visual IP Illustrations identity and legacy alias. | Update `SKILL.md` frontmatter and `agents/openai.yaml` display metadata while keeping existing route wording. |

## Architectural Responsibility Map

| Capability | Primary Tier | Secondary Tier | Rationale |
|------------|-------------|----------------|-----------|
| Linux route selection | `SKILL.md` runtime controller | `references/routing.md` route metadata | `SKILL.md` is the runtime route selection surface; `routing.md` is the canonical route metadata source. |
| Linux progressive reference loading | `SKILL.md` runtime controller | Linux route-local pack | The controller names selected-route references; the Phase 54 pack owns detailed rules. |
| Linux planning/generation/edit/QA dispatch | `SKILL.md` runtime controller | `references/ips/linux/*.md` | Controller dispatch should stay compact and route-local references carry prompt, edit, composition, and QA details. |
| Mixed-IP route isolation | `SKILL.md` runtime controller | `routing.md` output suffixes | Each route group gets its own references and output directory. |
| Agent discovery metadata | `agents/openai.yaml` | `SKILL.md` | RUN-04 requires route discovery through agent metadata and skill instructions. |

## Existing Baseline

- `SKILL.md` currently lists runtime controller behavior through Hermes Agent and lacks Linux Mascot wiring.
- `agents/openai.yaml` currently lists route discovery through Hermes Agent and lacks Linux Mascot metadata.
- `routing.md` already includes Linux Mascot route metadata, mixed-IP routing inclusion, output path, route-local references, and Linux Mascot metadata.
- `references/ips/linux/` already includes `index.md`, `source.md`, `style-dna.md`, `linux-ip.md`, `composition-patterns.md`, `prompt-template.md`, and `qa-checklist.md`.
- Phase 50 Hermes provides the closest controller-integration precedent for this phase shape.
- Phase 54 provides the direct Linux operational pack consumed by this phase.

## Standard Stack

| Surface | Current Standard | Phase 55 Use |
|---------|------------------|--------------|
| Markdown skill entrypoint | `skills/visual-ip-illustrations/SKILL.md` | Add Linux Mascot runtime controller dispatch. |
| YAML agent metadata | `skills/visual-ip-illustrations/agents/openai.yaml` | Add Linux Mascot route discovery wording. |
| Route metadata | `skills/visual-ip-illustrations/references/routing.md` | Read-only source for route ids, aliases, suffixes, required references, and boundaries. |
| Verification | `rg`, `find`, `git diff --check`, `gsd-tools` plan validators | Use targeted planning and execution checks; Phase 57 owns full validator and Node expansion. |

## Package Legitimacy Audit

No external package installation is required for Phase 55.

| Package | Registry | Source Repo | slopcheck | Disposition |
|---------|----------|-------------|-----------|-------------|
| none | none | none | not run | No install surface. |

## Implementation Surface

| File | Action | Key Markers |
|------|--------|-------------|
| `skills/visual-ip-illustrations/SKILL.md` | Add Linux Mascot to route overview, loading, selection, shot-list, generation, edit, QA, save, delivery, mixed-IP, and route-leakage guard sections. | `Linux Mascot`, `linux`, `Tux`, `source-reviewed`, `references/ips/linux/source.md`, `assets/<article-slug>-linux/`, `assets/&lt;article-slug&gt;-linux/`, `/Users/longnv/Downloads/Linux-logo.jpg`. |
| `skills/visual-ip-illustrations/agents/openai.yaml` | Add Linux Mascot to display name, short description, and default prompt. | Linux Mascot aliases, route status, output path, source pointer, uploaded-image authority, Tux attribution, The GIMP attribution condition, Linux trademark boundary, public sample review gate. |
| `.planning/phases/55-linux-mascot-skill-controller-integration/55-01-SUMMARY.md` | Execution summary target for the future executor. | RUN-01 through RUN-04 coverage and Phase 56/57 deferred scope notes. |

## Verification Guidance

Phase 55 execution should use focused checks that prove controller integration without expanding Phase 57 validator ownership:

```bash
rg -n 'Linux Mascot|Linux mascot|Tux penguin|source-reviewed|assets/<article-slug>-linux/|assets/&lt;article-slug&gt;-linux/|references/ips/linux/(index|source|style-dna|linux-ip|composition-patterns|prompt-template|qa-checklist)\.md' skills/visual-ip-illustrations/SKILL.md
```

```bash
rg -n 'Linux Mascot state|Linux Mascot action|Source context note|Trademark-boundary note|Stronger Linux Mascot Participation|Uploaded-Image Identity Repair|Trademark-Boundary Repair|Route Leakage Repair|Unaffected-Content Preservation|Linux Mascot loads only Linux Mascot `required_references`' skills/visual-ip-illustrations/SKILL.md
```

```bash
rg -n 'Linux Mascot|Tux|assets/<article-slug>-linux|assets/&lt;article-slug&gt;-linux|source-reviewed|Larry Ewing|The GIMP|Linux trademark|references/ips/linux/source.md|\$ian-xiaohei-illustrations' skills/visual-ip-illustrations/agents/openai.yaml
```

```bash
git diff --check -- skills/visual-ip-illustrations/SKILL.md skills/visual-ip-illustrations/agents/openai.yaml .planning/phases/55-linux-mascot-skill-controller-integration/55-01-SUMMARY.md
```

## Risks And Mitigations

| Risk | Mitigation |
|------|------------|
| Linux route activation misses a runtime controller section | Task actions enumerate every `SKILL.md` surface and verification greps route-selection, loading, planning, generation, QA, save, delivery, and guard markers. |
| Existing route behavior drifts | Verification requires Visual IP Illustrations identity, `$visual-ip-illustrations`, `$ian-xiaohei-illustrations`, Xiaohei default marker, and all existing route names in `SKILL.md` and `openai.yaml`. |
| Mixed-IP Linux group leaks other route references | Task 2 requires Linux as a separate route group with its own prompt template, composition rules, QA checklist, edit gates, route note, output suffix, and output directory. |
| Linux output reads as product marketing or official endorsement | Task 2 and Task 3 require trademark-boundary, distro-logo, product-output, public sample, and route-leakage guard language. |
| Phase 56/57 scope enters Phase 55 | Plan scope limits production edits to `SKILL.md` and `agents/openai.yaml`; public docs, examples, validators, tests, and samples remain deferred. |
