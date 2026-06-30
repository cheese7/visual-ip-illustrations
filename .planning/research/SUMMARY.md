# Project Research Summary

**Project:** Visual IP Illustrations
**Milestone:** v1.10 Hermes Agent Visual IP Integration
**Domain:** Codex Skill package for route-isolated article illustration IPs
**Researched:** 2026-06-18
**Confidence:** HIGH for repository integration; MEDIUM-HIGH for uploaded-image handling because the image is available in the conversation but the original `/Users/carson/Downloads/Generated image 1 (16).jpeg` path is unavailable from this workspace.

## Executive Summary

Hermes Agent should be added as an explicit source-reviewed uploaded-image route. The project stack should remain unchanged: Markdown reference packs, `SKILL.md` route dispatch, YAML agent metadata, static examples, host-provided `image_gen`, and dependency-free Node validation.

The route authority has two parts. Official Hermes Agent surfaces from Nous Research provide source, naming, and MIT license context. The user-uploaded conversation attachment provides the visual identity authority for the route: a monochrome full-body logo-style character with black bob haircut and bright highlights, headset or earpiece, black sleeveless dress, white collar tag with an `A`-like mark, black thigh-high stockings, platform heels, and slender fashion-figure posture.

The recommended implementation is a vertical route slice: add `references/ips/hermes/`, register `hermes` in `references/routing.md`, update skill controller behavior, update public docs and release surfaces, then extend validator and Node tests. Hermes-specific identity, prompt, QA, source, mythology-drift, and sample-policy rules should stay route-local.

## Stack Additions

- `references/ips/hermes/` canonical pack with `index.md`, `source.md`, `style-dna.md`, `hermes-ip.md`, `composition-patterns.md`, `prompt-template.md`, and `qa-checklist.md`.
- `references/routing.md` Hermes row with aliases, `default=false`, `output_suffix=hermes`, required references, source context, and status.
- `SKILL.md` route selection, reference loading, planning, generation, edit, QA, mixed-IP, and delivery updates.
- README variants, examples, NOTICE, release checklist, and agent metadata updates.
- Validator and Node test extensions for Hermes route, source, docs, paths, smoke, leakage, public assets, and release evidence.

## Feature Table Stakes

- Explicit Hermes Agent route selection.
- Xiaohei remains the sole omitted-IP default.
- Hermes output path is `assets/<article-slug>-hermes/`.
- The uploaded conversation attachment is the visual authority.
- Source record includes official website, official repository, MIT license, uploaded-image authority, sample policy, and review owner.
- Hermes prompts make the uploaded character perform the central cognitive article action.
- QA rejects generic anime/assistant drift, mythology drift, missing headset, missing bob-hair highlight silhouette, missing black sleeveless dress, missing collar tag, missing stockings/platform heels, product-poster drift, passive placement, excessive text, route leakage, and copied composition.
- Mixed-IP requests create separate route groups.
- Public Hermes samples require release review.
- Local validation covers the full route contract.

## Roadmap Recommendation

### Phase 48: Hermes Source and Route Contract

Add source/license authority, route metadata, aliases, output suffix, output path, uploaded-image visual authority, and explicit-only route-selection boundaries.

### Phase 49: Hermes Canonical Pack

Create the Hermes route-local reference pack with identity, style, composition, prompt, edit, QA, source, mythology-drift, and sample-policy rules.

### Phase 50: Hermes Skill Controller Integration

Wire Hermes into `SKILL.md`, route selection, progressive reference loading, planning fields, generation dispatch, edit routing, QA dispatch, mixed-IP grouping, and delivery reports.

### Phase 51: Public Documentation and Release Surface

Update README variants, examples, NOTICE, release checklist, agent metadata, and public route descriptions with Hermes source and output path behavior.

### Phase 52: Hermes Validation and Release Evidence

Extend validator and Node tests, add leakage and public asset gates, record final evidence, and verify existing routes remain stable.

## Watch Out For

- Uploaded-image identity drift into a generic monochrome anime character.
- Mythological Hermes drift into wings, sandals, caduceus, or Greek messenger imagery.
- Hermes prompt wording turning into product advertising or CLI screenshots.
- Missing MIT/source attribution.
- Hermes becoming default through generic aliases.
- Hermes visual markers leaking into Xiaohei, Tom, Cai Xukun, or shared prompts.
- Public generated Hermes assets shipping before release review.
- Output path drift away from `assets/<article-slug>-hermes/`.

## Sources

- Hermes Agent official website: https://hermes-agent.nousresearch.com/
- Hermes Agent official repository: https://github.com/NousResearch/hermes-agent
- Hermes Agent MIT license: https://github.com/NousResearch/hermes-agent/blob/main/LICENSE
- Hermes Agent documentation: https://hermes-agent.nousresearch.com/docs/
- User-provided uploaded image: conversation attachment `Generated image 1 (16).jpeg`.

---
*Research completed: 2026-06-18*
*Ready for roadmap: yes*
