# Domain Pitfalls: Hermes Agent Visual IP Integration

**Project:** Visual IP Illustrations
**Milestone:** v1.10 Hermes Agent Visual IP Integration
**Researched:** 2026-06-18

## Scope

This file covers risks when adding Hermes Agent as a source-reviewed uploaded-image route. The main challenge is preserving the exact uploaded monochrome character identity while turning it into article-illustration behavior that stays route-local, source-auditable, and compatible with existing route contracts.

## Critical Pitfalls

### 1. Treating the Uploaded Image as a Vague Anime Style Hint

**What goes wrong:** Prompts say "black-and-white anime agent" and the generated route drifts into a generic assistant, secretary, idol, or cyberpunk character.
**Warning signs:** Missing exact marker list; QA accepts any headset character; source record lacks uploaded-image authority.
**Prevention:** Record the uploaded image as visual authority and repeat stable markers: monochrome full-body logo-style character, black bob haircut with bright highlights, headset or earpiece, black sleeveless dress, white collar tag with an `A`-like mark, thigh-high stockings, platform heels, and slender fashion-figure posture.
**Automate:** Validator checks source, identity, prompt, and QA files for uploaded-image authority and marker strings.

### 2. Confusing Hermes Agent With Mythological Hermes

**What goes wrong:** Outputs become winged sandals, Greek messenger imagery, caduceus symbols, or classical mythology scenes.
**Warning signs:** Aliases include generic `Hermes`; prompts mention wings or Greek messenger unless the user explicitly asks for mythology.
**Prevention:** Route copy anchors the route to Hermes Agent by Nous Research and the uploaded character. Alias handling can accept `Hermes` only in contexts that mention article illustrations or visual IP routing.
**Automate:** Validator checks prompt and QA for mythology drift vetoes.

### 3. Making Hermes a Product Poster Route

**What goes wrong:** Hermes images become product ads, CLI screenshots, web hero graphics, or promotional logo lockups.
**Warning signs:** Prompt asks for large Hermes wordmark; README examples center brand copy; QA lacks article-metaphor requirements.
**Prevention:** Require one article idea, one cognitive action, sparse labels, white background, and character-as-actor composition.
**Automate:** Validator checks prompt and QA for article-illustration, cognitive-action, and sparse-label markers.

### 4. Omitting Source and License Context

**What goes wrong:** The route ships without official website, official repository, MIT license, or Nous Research attribution in NOTICE and source record.
**Warning signs:** Route row says only "uploaded image"; NOTICE lacks Hermes; release checklist has no source/license review.
**Prevention:** Add `source.md`, NOTICE, and release checklist markers for official site, repository, MIT license, Nous Research copyright, uploaded-image authority, and release review.
**Automate:** Validator adds `SOURCE-HERMES-001`, `NOTICE-HERMES-001`, and `RELEASE-HERMES-001`.

### 5. Accidental Default Route Expansion

**What goes wrong:** Hermes becomes default for generic "agent", "AI assistant", "black-and-white character", or "headset" prompts.
**Warning signs:** `default=true`; aliases include generic `agent`, `assistant`, `anime girl`, or `headset`.
**Prevention:** Keep Hermes explicit-only, with direct Hermes Agent aliases.
**Automate:** Validator enforces exactly one default route and rejects generic Hermes aliases.

### 6. Route Leakage Into Xiaohei, Tom, or Cai Xukun

**What goes wrong:** Headset, black dress, platform heels, or Hermes source terms appear in other route packs.
**Warning signs:** Xiaohei prompt mentions headset; Tom QA references Hermes; shared prompts include route-specific fashion anatomy.
**Prevention:** Keep Hermes identity under `references/ips/hermes/` plus bounded route/docs/release sections.
**Automate:** Add non-Hermes leakage scan for `Hermes Agent`, `Nous Research`, `black sleeveless dress`, `platform heels`, and `headset character`.

### 7. Public Sample Assets Ship Before Review

**What goes wrong:** Generated Hermes assets enter README galleries or skill example assets before identity and source review.
**Warning signs:** Public example directories contain Hermes filenames; release checklist lacks approval line.
**Prevention:** Keep generated Hermes public samples gated until release review records approval.
**Automate:** Public asset scan blocks Hermes rendered assets without explicit approval marker.

### 8. Weak Edit Prompts

**What goes wrong:** Editing a generated image fixes one issue while losing the headset, hair silhouette, dress, stockings, platform heels, or article readability.
**Warning signs:** Edit prompts lack unaffected-content preservation; QA has no repair prompts.
**Prevention:** Add edit prompt families for stronger participation, identity repair, title removal, text reduction, mythology-drift repair, and unaffected-content preservation.
**Automate:** Validator checks `prompt-template.md` and `qa-checklist.md` for edit gate names.

### 9. Output Path Ambiguity

**What goes wrong:** Hermes outputs save into `assets/<article-slug>-illustrations/` or a generic agent folder.
**Warning signs:** Missing `output_suffix`; README lacks raw/escaped path tokens; examples copy Gopher or OpenClaw path.
**Prevention:** Use `assets/<article-slug>-hermes/` consistently.
**Automate:** Validator checks raw and escaped Hermes output tokens.

## Recommended Automated Checks

1. `ROUTE-HERMES-001`: route row contains aliases, `default=false`, `output_suffix=hermes`, required references, source context, and status.
2. `REFS-HERMES-001`: seven route-local files exist.
3. `SOURCE-HERMES-001`: `source.md` records official site, official repository, MIT license, uploaded-image authority, sample policy, and review owner.
4. `PROMPT-HERMES-001`: prompt template includes planning fields, one-image gate, identity markers, edit gates, and output path.
5. `QA-HERMES-001`: QA checklist includes identity, action, article-metaphor, source-isolation, text, mythology-drift, and delivery gates.
6. `DOC-HERMES-001`: README, examples, skill metadata, and agent metadata describe the Hermes route consistently.
7. `NOTICE-HERMES-001`: NOTICE includes source and MIT attribution.
8. `SMOKE-HERMES-001`: smoke prompts cover explicit Hermes and mixed-IP route groups.
9. `BOUNDARY-HERMES-LEAK-001`: non-Hermes packs avoid Hermes identity markers.
10. `BOUNDARY-HERMES-IMG-001`: public sample assets require release approval.

## Sources

- Hermes Agent official website: https://hermes-agent.nousresearch.com/
- Hermes Agent official repository: https://github.com/NousResearch/hermes-agent
- Hermes Agent MIT license: https://github.com/NousResearch/hermes-agent/blob/main/LICENSE
- Hermes Agent documentation: https://hermes-agent.nousresearch.com/docs/
- User-provided uploaded image: conversation attachment `Generated image 1 (16).jpeg`.
