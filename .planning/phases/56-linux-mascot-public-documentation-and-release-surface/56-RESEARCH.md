# Phase 56: Linux Mascot Public Documentation and Release Surface - Research

**Researched:** 2026-07-01  
**Domain:** Public documentation, prompt examples, source attribution, release gates, and parity checks for the Linux Mascot route  
**Confidence:** HIGH

## Summary

Phase 56 should expose the already-built Linux Mascot route across public and maintainer-facing documentation. Phases 53-55 already established the route/source contract, seven-file Linux route-local pack, runtime controller behavior, and OpenAI metadata. The public gap is limited to README variants, copyable prompt examples, NOTICE attribution, release checklist gates, and targeted parity checks against `SKILL.md`, `agents/openai.yaml`, `routing.md`, and the Linux pack.

Primary recommendation: create one execution plan with three ordered documentation tasks. Task 1 updates `README.md` plus all localized README variants. Task 2 updates `examples/prompts.md`. Task 3 updates `NOTICE.md`, `RELEASE_CHECKLIST.md`, runs parity/asset-absence checks, and writes the execution summary. The task order follows the Hermes Phase 51 precedent and keeps generated Linux Mascot assets absent from this phase.

## User Constraints From CONTEXT.md

### Locked Decisions

- D-01: Add Linux Mascot to the root README and every localized README variant where the current route inventory lists Hermes Agent and other explicit routes.
- D-02: README updates must cover route selection, route description, aliases, source pointer, output path `assets/<article-slug>-linux/`, escaped marker `assets/&lt;article-slug&gt;-linux/`, `source-reviewed` status, uploaded-image authority, Tux attribution, The GIMP attribution condition, Linux trademark-boundary context, public sample review boundary, route isolation, and product-output boundary.
- D-03: README gallery sections keep Linux Mascot documented as pending public sample review, with Linux gallery columns and generated assets absent.
- D-04: Localized README variants may keep the existing mixed-language style, while deterministic Linux markers, paths, aliases, source pointer, status, and review-gate language stay exact enough for Phase 57 validation.
- D-05: `examples/prompts.md` adds Linux Mascot planning, generation, and edit examples with route-local references under `skills/visual-ip-illustrations/references/ips/linux/`.
- D-06: Linux prompt examples require route status `source-reviewed`, source authority `skills/visual-ip-illustrations/references/ips/linux/source.md`, uploaded-image authority from `/Users/longnv/Downloads/Linux-logo.jpg`, Larry Ewing Tux attribution, The GIMP attribution condition, Linux trademark-boundary note, public sample review gate, route isolation, and output path `assets/<article-slug>-linux/`.
- D-07: Multi-IP prompt examples move from nine groups to ten groups by adding Linux Mascot after Hermes Agent.
- D-08: Linux Mascot visible labels continue to be copied exactly in the user's requested language; prompt and maintainer-facing prose stays English-default.
- D-09: `NOTICE.md` adds Linux Mascot source attribution and public sample gate details for route id, display name, status, source authority, uploaded local image authority, Tux source, Linux trademark context, output paths, and release-review terms.
- D-10: `RELEASE_CHECKLIST.md` adds Phase 57 ownership for Linux validation, route smoke coverage, attribution review, Linux source/trademark/uploaded-image/public-sample gates, generated sample policy, and final release review.
- D-11: Release checklist wording keeps public generated Linux Mascot samples pending until reviewer, date, approval status, allowed directories, release channels, Tux source outcome, GIMP attribution outcome, Linux trademark outcome, uploaded-image identity outcome, route-isolation outcome, distro-logo boundary outcome, endorsement/certification boundary outcome, product-output outcome, and public-sample decision are recorded.
- D-12: `SKILL.md` and `agents/openai.yaml` already include Linux Mascot from Phase 55; Phase 56 performs parity checks and makes only narrow documentation-discovery edits if public surfaces reveal inconsistent markers.
- D-13: Preserve Visual IP Illustrations identity, canonical `$visual-ip-illustrations`, legacy `$ian-xiaohei-illustrations`, `allow_implicit_invocation: true`, and omitted-IP Xiaohei default behavior.
- D-14: Preserve Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, and Hermes Agent public documentation and route behavior while adding Linux Mascot.
- D-15: Public copy presents Linux Mascot as a source-reviewed uploaded-image article-illustration route where Tux performs the central cognitive action in sparse 16:9 article illustrations.
- D-16: Public copy keeps Tux source context separate from Linux word-mark guidance: Larry Ewing and The GIMP attach to Tux source context; Linux Foundation trademark guidance and Linux mark ownership context attach to Linux word-mark usage.
- D-17: Public and release copy keeps official endorsement, affiliation, sponsorship, approval, certification, compatibility, Linux Foundation logo use, distro-logo use, distro branding, product advertising, product-poster output, CLI screenshots, web hero graphics, kernel dashboard screenshots, and operating-system marketing graphics outside the Linux Mascot route.
- D-18: Public copy preserves the uploaded marker set when marker detail is needed.
- D-19: Phase 56 verification uses targeted `rg` checks across README variants, prompt examples, NOTICE, release checklist, `SKILL.md`, and `openai.yaml`, plus a public sample asset absence check and `git diff --check`.
- D-20: Full validator and Node regression updates remain Phase 57 work, so current validator route-count drift is not a Phase 56 documentation blocker.

### Deferred Scope

- Phase 57 owns validator coverage, Node tests, leakage scans, trademark-boundary scans, public sample gates, generated sample gates, route smoke automation, uploaded-image and source-boundary smoke, docs consistency automation, and release evidence.
- Public generated Linux Mascot sample gallery work belongs after release review approval.
- Machine-readable route manifests, uploaded source-image hashing, visual regression, public comparison sheets, release packaging, and selected-IP installation variants remain future requirements.

## Phase Requirements

| ID | Requirement | Research Support |
|----|-------------|------------------|
| DOC-01 | README route selection, workflow, output path, and route descriptions include Linux Mascot as an explicit source-reviewed Tux route. | Update README root and every localized variant in the same sections Hermes currently occupies. |
| DOC-02 | Copyable Linux Mascot planning, generation, editing, and mixed-IP examples use `assets/<article-slug>-linux/`. | Add Linux canonical examples, edit example, smoke prompt, and tenth mixed-IP group in `examples/prompts.md`. |
| DOC-03 | NOTICE and release checklist include Larry Ewing Tux attribution, The GIMP attribution condition, Linux trademark guidance, uploaded-image authority, public sample policy, and review gates. | Add a dedicated Linux NOTICE section and a dedicated Linux release checklist gate modeled on Hermes. |
| DOC-04 | Docs preserve default-route behavior, route isolation, source-reviewed status, endorsement and distro-logo boundaries, and uploaded-image-only output. | README, examples, NOTICE, and release checklist all repeat route isolation, Xiaohei default preservation, public-sample gate, and claim boundaries. |
| DOC-05 | Public release surfaces stay consistent across README variants, prompt examples, agent metadata, NOTICE, and release checklist. | Targeted parity checks compare public docs with `SKILL.md`, `openai.yaml`, `routing.md`, and Linux pack markers. |

## Existing Baseline

- `README.md` and all `readmes/README.*.md` currently describe routes through Hermes Agent and contain no Linux Mascot public route markers.
- `examples/prompts.md` currently has canonical Hermes planning/generation/edit prompts and a nine-group mixed-IP prompt; it has no Linux Mascot examples.
- `NOTICE.md` currently ends route-specific attribution sections at Hermes Agent.
- `RELEASE_CHECKLIST.md` currently has route gates through Hermes Agent and Phase 52 ownership; it has no Phase 57 Linux release gate.
- `skills/visual-ip-illustrations/SKILL.md` and `skills/visual-ip-illustrations/agents/openai.yaml` already contain Linux Mascot runtime and metadata markers from Phase 55.
- `skills/visual-ip-illustrations/references/routing.md` and `skills/visual-ip-illustrations/references/ips/linux/` already provide canonical Linux route facts.

## Standard Stack

| Surface | Current Standard | Phase 56 Use |
|---------|------------------|--------------|
| Public docs | `README.md`, `readmes/README.*.md` | Add Linux route inventory, output paths, route section, route reference, operational facts, gallery pending note, quick examples, workflow, directory/validation wording. |
| Prompt examples | `examples/prompts.md` | Add Linux planning, generation, edit, route smoke, and mixed-IP tenth group examples. |
| Source attribution | `NOTICE.md` | Add Linux source attribution and public sample gate section. |
| Release gates | `RELEASE_CHECKLIST.md` | Add Linux Phase 57 ownership, source/trademark/uploaded-image/sample gates, and final release review. |
| Runtime parity | `SKILL.md`, `agents/openai.yaml`, `routing.md`, `references/ips/linux/` | Check Linux markers and preserve Phase 55 behavior. |
| Verification | `rg`, `find`, `git diff --check`, `gsd-tools` plan validators | Use targeted checks; Phase 57 owns full validator and Node expansion. |

## Package Legitimacy Audit

No external package installation is required for Phase 56.

| Package | Registry | Source Repo | slopcheck | Disposition |
|---------|----------|-------------|-----------|-------------|
| none | none | none | not run | No install surface. |

## Implementation Surface

| File | Action | Key Markers |
|------|--------|-------------|
| `README.md` and `readmes/README.*.md` | Add Linux Mascot to route inventory, outputs, Visual IP Routes, Route Reference, operational facts, gallery pending wording, quick examples, workflow, and maintainer validation. | `Linux Mascot`, `Tux`, `source-reviewed`, `assets/<article-slug>-linux/`, `assets/&lt;article-slug&gt;-linux/`, `skills/visual-ip-illustrations/references/ips/linux/source.md`. |
| `examples/prompts.md` | Add Linux planning, generation, edit, route smoke, maintainer smoke, and mixed-IP tenth group examples. | Linux route-local directory, source authority, uploaded-image authority, Tux markers, trademark-boundary note, output path. |
| `NOTICE.md` | Add Linux Mascot source attribution and public sample gate. | Larry Ewing, Linux 2.0 Penguins, The GIMP, Linux Foundation trademark guidance, Linux mark ownership context. |
| `RELEASE_CHECKLIST.md` | Add Linux release gates and Phase 57 ownership. | Route smoke, attribution review, public/generated sample policy, final Linux release review, validator ownership. |
| `SKILL.md`, `agents/openai.yaml` | Parity check only unless marker drift is found during execution. | Existing Phase 55 Linux runtime and metadata markers. |

## Verification Guidance

Use focused checks that prove public documentation coverage without expanding Phase 57 validator ownership:

```bash
rg -n 'Linux Mascot|Tux|assets/<article-slug>-linux/|assets/&lt;article-slug&gt;-linux/|skills/visual-ip-illustrations/references/ips/linux/source.md|source-reviewed|Larry Ewing|The GIMP|Linux trademark|public sample review gate|route isolation' README.md readmes/README.*.md examples/prompts.md NOTICE.md RELEASE_CHECKLIST.md
```

```bash
rg -n 'ten separate variant groups|Linux Mascot group|Linux Mascot state|Linux Mascot action|Trademark-boundary note|Route Smoke: Explicit Linux Mascot|assets/<article-slug>-linux|assets/&lt;article-slug&gt;-linux' examples/prompts.md
```

```bash
rg -n 'Linux Mascot|Tux|assets/<article-slug>-linux|assets/&lt;article-slug&gt;-linux|source-reviewed|Larry Ewing|The GIMP|Linux trademark|references/ips/linux/source.md|\$ian-xiaohei-illustrations' skills/visual-ip-illustrations/SKILL.md skills/visual-ip-illustrations/agents/openai.yaml
```

```bash
find examples/images examples/images-en skills/visual-ip-illustrations/assets/examples assets -iname '*linux*' -o -iname '*tux*'
git diff --check -- README.md readmes/README.*.md examples/prompts.md NOTICE.md RELEASE_CHECKLIST.md .planning/phases/56-linux-mascot-public-documentation-and-release-surface/56-01-SUMMARY.md
```

Expected public sample asset check output: empty.

## Risks And Mitigations

| Risk | Mitigation |
|------|------------|
| README variant drift | Task 1 edits every README variant and verifies Linux markers across `README.md readmes/README.*.md`. |
| Public sample wording overpublishes Linux assets | Task 1 and Task 3 keep Linux samples pending behind release review and verify Linux/Tux asset absence. |
| Tux attribution and Linux word-mark guidance merge into one claim | Task 3 separates Larry Ewing/The GIMP Tux source context from Linux Foundation trademark guidance and Linux mark ownership context. |
| Existing routes drift during bulk README updates | Task verification requires existing route names and output paths to remain present. |
| Full validator failure blocks documentation work | D-20 assigns validator and Node updates to Phase 57; Phase 56 records targeted checks and `git diff --check`. |

