# Feature Landscape: Hermes Agent Visual IP Integration

**Domain:** Visual IP Illustrations Codex Skill
**Milestone:** v1.10 Hermes Agent Visual IP Integration
**Researched:** 2026-06-18
**Scope:** Hermes Agent route only; Xiaohei, Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, and Cai Xukun behavior are baseline dependencies.

## Recommendation

Add Hermes Agent as an explicit source-reviewed uploaded-image route. Users should be able to request Hermes Agent and receive 16:9 article illustrations where the uploaded black-and-white headset character performs the cognitive action. Maintainers should be able to audit official Hermes Agent source context, MIT license context, uploaded-image visual authority, output path, route isolation, public sample policy, and validator evidence.

Hermes should behave like other explicit routes structurally: route aliases, isolated references, route-specific output suffix, prompt template, QA checklist, docs, examples, NOTICE, release checklist, validator checks, and Node tests. It should differ by preserving a monochrome logo-style human character: full-body black-and-white illustration, black bob haircut with bright highlights, headset or earpiece, black sleeveless dress, white collar tag with an `A`-like mark, black thigh-high stockings, platform heels, and slender fashion-figure posture.

## Table Stakes

| Feature | Expected User Behavior | Expected Maintainer Behavior | Complexity |
|---------|------------------------|------------------------------|------------|
| Explicit Hermes route selection | User can write `Hermes Agent` or `Hermes Agent logo` and get `selected IP: Hermes Agent`. | Add `hermes` route metadata with aliases, `default=false`, output suffix, required references, attribution context, and status. | Medium |
| Xiaohei default preservation | User omits IP and still gets Xiaohei. | Validator confirms Xiaohei is the sole default route. | Low |
| Source and license record | User and redistributor can inspect official Hermes Agent naming/source context. | Add `source.md` with official site, repository, MIT license, uploaded-image authority, sample policy, and review owner. | Medium |
| Canonical Hermes pack | User receives Hermes-consistent planning, prompt, edits, and QA. | Create route-local files under `references/ips/hermes/`. | High |
| Uploaded-image character identity | User sees the black-and-white Hermes figure as the action subject. | Define stable visual markers from the attachment and reject generic anime or assistant drift. | High |
| Article-illustration fit | Output explains one cognitive action rather than becoming a product poster or fashion pose sheet. | Prompt and QA require one idea, sparse layout, white background, sparse labels, and active Hermes participation. | Medium |
| Route-specific output path | Hermes outputs save under `assets/<article-slug>-hermes/`. | Docs and validator include raw and escaped path markers. | Low |
| Mixed-IP grouping | User can request Hermes alongside existing routes for the same idea. | Mixed requests create separate route groups with independent references, prompts, QA, and output directories. | Medium |
| Public docs and examples | User can copy Hermes prompts and understand route scope. | README, examples, metadata, NOTICE, and release checklist include Hermes wording and sample policy. | Medium |
| Local validation | Maintainer gets deterministic failures for route drift. | Extend validator and tests with Hermes route, pack, source, docs, path, smoke, leakage, and release checks. | Medium |

## Differentiators

| Feature | Value Proposition | Implementation Note |
|---------|-------------------|---------------------|
| Monochrome logo character | The uploaded image creates a distinctive high-contrast visual IP. | Preserve black-and-white line/fill contrast and the headset fashion silhouette. |
| Agent/workflow metaphor fit | Hermes Agent product context supports memory, skills, gateway, delegation, terminal, and scheduling metaphors. | Use these as optional article metaphors while keeping the image a general article illustration. |
| Strong silhouette | The dress, headset, stockings, and platform heels make route recognition possible even in sparse scenes. | QA should reject generic office assistant, robot, cyberpunk agent, and unrelated anime output. |
| Open-source source context | MIT source record can be audited locally. | Keep official site, repository, and license links in `source.md`, NOTICE, and validator markers. |

## Anti-Features

| Anti-Feature | Recommended Behavior |
|--------------|----------------------|
| Making Hermes the default IP | Keep Hermes explicit-only. |
| Replacing the uploaded character with a winged Greek god, messenger icon, robot, or generic anime girl | QA requires all uploaded-image identity markers together. |
| Turning illustrations into Hermes product ads | Use article-metaphor scenes, with product context only when the user's article needs it. |
| Copying visible brand/logotype text by default | Use the uploaded character identity; visible labels follow user content. |
| Mixing Hermes identity into other route packs | Keep Hermes constraints route-local. |
| Public generated sample assets before release review | Gate public examples through release checklist approval. |

## Required User Flows

1. **Planning only**
   - User asks for Hermes route planning.
   - Skill returns selected IP, route references, output path, shot list, Hermes state, Hermes action, objects, labels, and stability notes.

2. **Direct generation**
   - User explicitly requests Hermes image generation.
   - Skill loads only Hermes references, generates one image per prompt, applies Hermes QA, saves to `assets/<article-slug>-hermes/`, and reports delivery details.

3. **Mixed-IP variants**
   - User requests Hermes with Xiaohei, Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, or Cai Xukun variants.
   - Skill creates separate route groups and avoids blended visual rules.

4. **Editing**
   - User asks to strengthen Hermes participation, repair off-model identity, remove titles, reduce labels, or preserve unaffected content.
   - Skill uses Hermes edit prompts and retains output path and uploaded-image authority.

## Requirements Implications

- Hermes route acceptance requires official source/license evidence and uploaded-image visual authority.
- Visual markers should be testable through text prompts and QA rules.
- Source and public sample policy should appear before public generated Hermes examples.
- Existing Xiaohei default, existing explicit routes, and legacy skill aliases stay stable.
- Validation should cover route metadata, pack files, output path, docs, source record, NOTICE, release checklist, public asset gate, and non-Hermes leakage.

## Sources

- Hermes Agent official website: https://hermes-agent.nousresearch.com/
- Hermes Agent official repository: https://github.com/NousResearch/hermes-agent
- Hermes Agent MIT license: https://github.com/NousResearch/hermes-agent/blob/main/LICENSE
- Hermes Agent documentation: https://hermes-agent.nousresearch.com/docs/
- User-provided uploaded image: conversation attachment `Generated image 1 (16).jpeg`.
