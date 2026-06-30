# Architecture Research: Hermes Agent Visual IP Integration

**Project:** Visual IP Illustrations
**Milestone:** v1.10 Hermes Agent Visual IP Integration
**Researched:** 2026-06-18
**Scope:** Add Hermes Agent as a new explicit route while preserving all existing route behavior.

## Recommendation

Integrate Hermes Agent as a vertical route slice:

```text
SKILL.md
  -> references/routing.md
    -> references/ips/xiaohei/*
    -> references/ips/littlebox/*
    -> references/ips/tom/*
    -> references/ips/ferris/*
    -> references/ips/seal/*
    -> references/ips/openclaw/*
    -> references/ips/gopher/*
    -> references/ips/caixukun/*
    -> references/ips/hermes/*
  -> image_gen runtime
  -> assets/<article-slug>-<route-suffix>/
```

`SKILL.md` should select the route, load Hermes references, dispatch planning/generation/QA/editing, and report output paths. The uploaded-image identity, official source/license record, composition rules, prompt wording, QA failures, and sample policy belong inside `references/ips/hermes/`.

## New Components

| File | Responsibility |
|------|----------------|
| `references/ips/hermes/index.md` | Pack navigation, route status, source authority, output path, shared failure categories. |
| `references/ips/hermes/source.md` | Official Hermes Agent source links, MIT license, uploaded-image authority, public sample policy, review owner. |
| `references/ips/hermes/style-dna.md` | Sparse article-illustration style, monochrome identity, white background, visual vetoes. |
| `references/ips/hermes/hermes-ip.md` | Character identity, visual markers, action responsibility, recognition gates, failure modes. |
| `references/ips/hermes/composition-patterns.md` | Composition families and Hermes-appropriate article metaphors. |
| `references/ips/hermes/prompt-template.md` | Shot-list fields, one-image generation prompt, edit prompts, output reminder. |
| `references/ips/hermes/qa-checklist.md` | Pass/fail criteria, uploaded-image identity gates, source isolation, iteration moves, delivery judgment. |

## Modified Components

| File | Change |
|------|--------|
| `references/routing.md` | Add Hermes route row, selection rules, metadata block, output paths, mixed-IP wording. |
| `SKILL.md` | Add Hermes route selection, reference loading, planning fields, generation prompt dispatch, QA dispatch, edit routing, delivery report. |
| `agents/openai.yaml` | Mention Hermes Agent as an explicit source-reviewed route while preserving Xiaohei default. |
| `README.md` and localized docs | Add Hermes route summary, output path, source/license note, uploaded-image authority, sample policy. |
| `examples/prompts.md` | Add explicit Hermes planning, generation, edit, and mixed-IP prompts. |
| `NOTICE.md` | Add Hermes Agent source attribution and MIT license note. |
| `RELEASE_CHECKLIST.md` | Add Hermes route, uploaded-image, public sample, validation, and release evidence gates. |
| `scripts/validate-skill-package.mjs` | Add Hermes route/pack/docs/source/path/smoke/leakage/release checks. |
| `scripts/validate-skill-package.test.mjs` | Add Hermes check IDs, parser expectations, failure fixtures, and summary counts. |

## Data Flow

### Explicit Hermes Request

```text
User asks for Hermes Agent article illustration
  -> SKILL.md reads references/routing.md
  -> routing.md selects route id hermes
  -> agent loads only references/ips/hermes/ required references
  -> shared workflow extracts article anchors
  -> Hermes shot list maps one core idea to character action
  -> Hermes prompt-template.md creates one prompt per image
  -> host image_gen generates one image per prompt
  -> Hermes QA decides pass, edit, or regenerate
  -> accepted PNGs save under assets/<article-slug>-hermes/
  -> delivery report states selected IP, count, purpose, path, and stability notes
```

### Mixed-IP Request

```text
User asks for variants across Hermes and other routes
  -> SKILL.md extracts one shared core idea
  -> routing.md resolves route groups
  -> each route group loads only its required references
  -> each route group produces an independent shot list, prompt, QA result, and output directory
```

## Build Order

1. **Source and route contract**
   - Add source/license authority, route metadata, output suffix, aliases, and uploaded-image visual authority.

2. **Hermes canonical pack**
   - Add identity, style, composition, prompt, QA, and edit references.

3. **Skill controller integration**
   - Add Hermes to route selection, reference loading, shot-list fields, generation/editing/QA dispatch, and mixed-IP delivery.

4. **Docs and release surface**
   - Add README variants, prompt examples, NOTICE, release checklist, and agent metadata.

5. **Validation hardening**
   - Extend validator and tests, add source/path/smoke/leakage/public asset gates, and record final evidence.

## Architecture Risks

| Risk | Impact | Mitigation |
|------|--------|------------|
| Uploaded-image identity lives only in prompts | Future edits drift into generic black-and-white anime output. | Store identity markers in `source.md`, `hermes-ip.md`, prompt, and QA. |
| Product copy dominates prompts | Images become Hermes Agent ads rather than article illustrations. | Route pack requires one cognitive action and sparse article-metaphor scenes. |
| Source/license omitted from public docs | Maintainers cannot audit redistribution context. | NOTICE, source record, and validator require official site, repository, and MIT markers. |
| Hermes becomes a generic AI-agent default | Omitted-IP behavior changes unexpectedly. | Keep Hermes explicit-only and reject generic aliases. |
| Mixed-IP requests load all references | Route leakage becomes likely. | Keep one route group per selected IP with independent references and paths. |
| Validator remains eight-route specific | Partial Hermes integration can pass. | Add Hermes route checks and update parser expectations. |

## Sources

- Hermes Agent official website: https://hermes-agent.nousresearch.com/
- Hermes Agent official repository: https://github.com/NousResearch/hermes-agent
- Hermes Agent MIT license: https://github.com/NousResearch/hermes-agent/blob/main/LICENSE
- Hermes Agent documentation: https://hermes-agent.nousresearch.com/docs/
- User-provided uploaded image: conversation attachment `Generated image 1 (16).jpeg`.
