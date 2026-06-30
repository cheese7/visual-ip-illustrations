# Phase 55: Linux Mascot Skill Controller Integration - Context

**Gathered:** 2026-07-01
**Status:** Ready for planning

<domain>
## Phase Boundary

Phase 55 wires the already-defined `linux` route into the Visual IP Illustrations runtime controller. Users should be able to select Linux Mascot, load the Linux seven-file pack, plan Linux Mascot shots, generate and edit Linux Mascot images, run Linux Mascot QA, save under `assets/<article-slug>-linux/`, receive Linux Mascot delivery reports, and request mixed-IP output where Linux Mascot is a separate route group.

Implementation scope centers on:

- `skills/visual-ip-illustrations/SKILL.md`
- `skills/visual-ip-illustrations/agents/openai.yaml`

The route metadata and Linux Mascot pack were completed in Phases 53 and 54:

- `skills/visual-ip-illustrations/references/routing.md`
- `skills/visual-ip-illustrations/references/ips/linux/index.md`
- `skills/visual-ip-illustrations/references/ips/linux/source.md`
- `skills/visual-ip-illustrations/references/ips/linux/style-dna.md`
- `skills/visual-ip-illustrations/references/ips/linux/linux-ip.md`
- `skills/visual-ip-illustrations/references/ips/linux/composition-patterns.md`
- `skills/visual-ip-illustrations/references/ips/linux/prompt-template.md`
- `skills/visual-ip-illustrations/references/ips/linux/qa-checklist.md`

Out of scope:

- README variants, `examples/prompts.md`, NOTICE, release checklist, public release copy, and public sample surfaces. Phase 56 owns these.
- Validator hardening, Node regression tests, smoke prompts, leakage fixtures, public sample gates, and final release evidence. Phase 57 owns these.
- Generated Linux Mascot images or public sample assets.

</domain>

<decisions>
## Implementation Decisions

### Scope Ownership

- **D-01:** Phase 55 owns runtime controller behavior in `skills/visual-ip-illustrations/SKILL.md`.
- **D-02:** Phase 55 owns the agent metadata slice required by RUN-04 in `skills/visual-ip-illustrations/agents/openai.yaml` because RUN-04 explicitly names agent metadata for Linux Mascot.
- **D-03:** Preserve all existing route behavior for omitted-IP Xiaohei and explicit Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, and Hermes Agent.
- **D-04:** Public docs and validation remain deferred to Phases 56 and 57.

### RUN-01 Decisions

- **D-05:** Add Linux Mascot to `SKILL.md` frontmatter description, Visual IP Routes, Reference Loading, Select the Visual IP Route, shot-list fields, generation context, edit routing, QA dispatch, save paths, and delivery reporting.
- **D-06:** Linux Mascot route selection must use aliases `Linux Mascot`, `Linux mascot`, `Linux`, `linux`, `Tux`, `tux`, `Linux penguin`, and `Tux penguin`; broad penguin, server, kernel, distro, distro-logo, Linux Foundation, operating-system, CLI, terminal, product, brand-campaign, and generic mascot terms remain outside Linux Mascot selection.
- **D-07:** Linux Mascot progressive loading must point to the Phase 54 seven-file pack: `index.md`, `source.md`, `style-dna.md`, `linux-ip.md`, `composition-patterns.md`, `prompt-template.md`, and `qa-checklist.md`.
- **D-08:** Linux Mascot runtime wording must carry uploaded-image authority from `/Users/longnv/Downloads/Linux-logo.jpg`, Larry Ewing Tux attribution, The GIMP attribution condition, Linux trademark-boundary context, source pointer `references/ips/linux/source.md`, public sample review boundary, route isolation, and output path `assets/<article-slug>-linux/`.
- **D-09:** Linux Mascot planning entries must mirror `references/ips/linux/prompt-template.md` and include Placement, Core idea, Structure type, Linux Mascot state, Linux Mascot action, Supporting objects, Visible labels, Source context note, Trademark-boundary note, and Output path.
- **D-10:** Linux Mascot generation and edit dispatch must use `references/ips/linux/prompt-template.md` plus `references/ips/linux/composition-patterns.md`, then check outputs with `references/ips/linux/qa-checklist.md`.

### RUN-02 Decisions

- **D-11:** Mixed-IP workflows must add Linux Mascot as a separate route group alongside Xiaohei, Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, and Hermes Agent.
- **D-12:** Each mixed-IP group must load only its own required references, use its own prompt template, QA checklist, edit gates, route note, output suffix, and output directory.
- **D-13:** Linux Mascot mixed-IP groups must write to `assets/<article-slug>-linux/` and include route status `source-reviewed`, source pointer, uploaded-image authority note, Tux source attribution note, Linux trademark-boundary note, public sample review boundary when relevant, and route isolation status.

### RUN-03 Decisions

- **D-14:** Linux Mascot delivery reports must include selected visual IP, image count, purpose per image, saved path under `assets/<article-slug>-linux/`, uploaded-image authority note, source/trademark note, route status `source-reviewed`, source pointer `references/ips/linux/source.md`, public sample review boundary when relevant, and route stability notes.
- **D-15:** The route-leakage delivery guard must include Linux Mascot and require source-reviewed status, source pointer, uploaded-image authority note, route-local QA, original article-metaphor status, trademark-boundary status, distro-logo boundary status, product-output boundary status, public sample review boundary, route isolation status, and `assets/<article-slug>-linux/`.

### RUN-04 Decisions

- **D-16:** `SKILL.md` must present Linux Mascot as a selectable source-reviewed uploaded-image route while preserving Visual IP Illustrations identity, canonical `$visual-ip-illustrations`, and legacy `$ian-xiaohei-illustrations` compatibility alias.
- **D-17:** `agents/openai.yaml` must add Linux Mascot to display name, short description, and default prompt without removing existing route descriptions.

### the agent's Discretion

- The planner may choose exact `SKILL.md` paragraph placement by following the Hermes Agent, Cai Xukun, Go Gopher, and OpenClaw route-specific pattern.
- The planner may keep Linux Mascot runtime text compact because detailed style, prompt, edit, and QA rules live in `references/ips/linux/`.
- The planner should use targeted `rg` checks and `git diff --check` as Phase 55 acceptance proof; full validator and Node tests remain Phase 57.

</decisions>

<canonical_refs>
## Canonical References

**Downstream agents MUST read these before planning or implementing.**

### Phase Scope

- `.planning/ROADMAP.md` - Phase 55 goal, success criteria, and Phase 56/57 boundaries.
- `.planning/REQUIREMENTS.md` - RUN-01 through RUN-04.
- `.planning/STATE.md` - current milestone state and Phase 55 readiness.

### Prior Phase Evidence

- `.planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md` - locked route, alias, source, uploaded-image, Tux attribution, trademark-boundary, and default-route decisions.
- `.planning/phases/53-linux-mascot-source-and-route-contract/53-01-SUMMARY.md` - implementation evidence for the Linux route row and source record.
- `.planning/phases/53-linux-mascot-source-and-route-contract/53-VERIFICATION.md` - verified route/source contract and later-phase ownership.
- `.planning/phases/54-linux-mascot-canonical-pack/54-CONTEXT.md` - locked Linux Mascot pack, prompt, edit, QA, source-preservation, and routing-expansion decisions.
- `.planning/phases/54-linux-mascot-canonical-pack/54-01-SUMMARY.md` - implementation evidence for the Linux seven-file route-local pack and routing required-reference expansion.
- `.planning/phases/54-linux-mascot-canonical-pack/54-VERIFICATION.md` - verified Linux Mascot operational pack behavior and deferred validator ownership.

### Runtime Targets

- `skills/visual-ip-illustrations/SKILL.md` - central runtime controller for route selection, progressive loading, planning, generation, edit routing, QA, save paths, delivery reporting, and route-leakage guard.
- `skills/visual-ip-illustrations/agents/openai.yaml` - agent metadata required by RUN-04.
- `skills/visual-ip-illustrations/references/routing.md` - route metadata, aliases, required references, output suffix, mixed-IP behavior, output paths, and delivery fields.

### Linux Mascot Route Pack

- `skills/visual-ip-illustrations/references/ips/linux/index.md`
- `skills/visual-ip-illustrations/references/ips/linux/source.md`
- `skills/visual-ip-illustrations/references/ips/linux/style-dna.md`
- `skills/visual-ip-illustrations/references/ips/linux/linux-ip.md`
- `skills/visual-ip-illustrations/references/ips/linux/composition-patterns.md`
- `skills/visual-ip-illustrations/references/ips/linux/prompt-template.md`
- `skills/visual-ip-illustrations/references/ips/linux/qa-checklist.md`

### Controller Precedents

- `.planning/phases/50-hermes-skill-controller-integration/50-CONTEXT.md`
- `.planning/phases/50-hermes-skill-controller-integration/50-01-SUMMARY.md`
- `.planning/phases/45-cai-xukun-skill-controller-integration/45-CONTEXT.md`
- `.planning/phases/40-go-gopher-skill-controller-integration/40-CONTEXT.md`
- `.planning/phases/35-openclaw-skill-controller-integration/35-CONTEXT.md`

</canonical_refs>

<code_context>
## Existing Code Insights

### Reusable Assets

- `skills/visual-ip-illustrations/SKILL.md` already has repeated runtime-controller blocks for Hermes Agent, Cai Xukun, Go Gopher, OpenClaw, Seal, Ferris, Tom, Littlebox, and Xiaohei across route overview, reference loading, selection, planning, generation, QA, repair, save, and delivery.
- `skills/visual-ip-illustrations/references/routing.md` already contains the verified Linux Mascot route row, alias boundaries, seven-file `required_references`, output suffix `linux`, output path markers, source/trademark context, and mixed-IP path entry.
- `skills/visual-ip-illustrations/references/ips/linux/prompt-template.md` and `qa-checklist.md` already define the exact Linux Mascot planning, generation, edit, QA, delivery, and route-leakage wording to mirror into runtime-controller guidance.
- `skills/visual-ip-illustrations/agents/openai.yaml` currently lists routes through Hermes Agent and should be extended for Linux Mascot as the RUN-04 discovery surface.

### Established Patterns

- `SKILL.md` functions as the runtime controller and should stay concise; detailed identity, prompt, and QA rules live in route-local reference files.
- Each explicit route has entries in Visual IP Routes, Reference Loading, Select the Visual IP Route, shot-list planning, generation context, mixed-IP grouping, QA, save paths, Output Contract, and route-leakage delivery guard.
- Existing route output paths follow `assets/<article-slug>-<output_suffix>/`, except Xiaohei compatibility uses `assets/<article-slug>-illustrations/`.
- Public generated samples for source-reviewed, uploaded-image, local-reference, public-figure, protected, or brand-sensitive routes require release review.

### Integration Points

- Frontmatter description: add Linux Mascot to explicit selectable routes.
- `## Visual IP Routes`: add Linux Mascot status, source pointer, output path, uploaded-image authority, Tux attribution, Linux trademark boundary, distro-logo boundary, public sample review boundary, and product-output boundary.
- `## Reference Loading`: add all seven Linux Mascot route-local references.
- `### 1. Select the Visual IP Route`: add aliases, route metadata, broad-term exclusions, output path, required references, and mixed-IP grouping.
- `### 3. Plan the Shot List First`: add Linux Mascot shot-list fields and mixed-IP group entry.
- `### 4. Generate One Image at a Time`: add Linux Mascot generation context and repair behavior.
- `### 5. QA and Iteration`: add Linux Mascot QA checklist and high-risk failure list.
- `### 6. Save and Deliver`: add `assets/<article-slug>-linux/` active path and escaped validation marker.
- `## Output Contract`: add Linux Mascot delivery block and route-leakage delivery guard.
- `agents/openai.yaml`: add Linux Mascot route discovery wording while preserving Visual IP Illustrations identity and `$ian-xiaohei-illustrations` compatibility.

</code_context>

<specifics>
## Specific Ideas

- Preserve omitted-IP Xiaohei default exactly.
- Preserve existing Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, and Hermes Agent route behavior exactly.
- Keep Linux Mascot as an explicit selectable source-reviewed uploaded-image route with aliases `Linux Mascot`, `Linux mascot`, `Linux`, `linux`, `Tux`, `tux`, `Linux penguin`, and `Tux penguin`.
- Preserve uploaded-image authority from `/Users/longnv/Downloads/Linux-logo.jpg`.
- Preserve the Tux marker set in runtime text when marker detail is useful: glossy black rounded penguin head and body, white face eye patches, large oval eyes with dark pupils and small highlights, yellow-orange beak with two nostril dots, white oval belly, long black flippers, seated rounded posture, and oversized yellow-orange webbed feet.
- Keep Linux Mascot route outputs as sparse 16:9 article illustrations and keep official endorsement, certification, compatibility, distro-logo, Linux Foundation logo, product-poster, CLI screenshot, web hero graphic, kernel dashboard screenshot, and operating-system marketing graphic drift outside route identity.
- Keep public generated Linux Mascot samples behind release review.

</specifics>

<deferred>
## Deferred Ideas

- Phase 56: README variants, `examples/prompts.md`, NOTICE, RELEASE_CHECKLIST, public release surfaces, broad public docs, and any wider release-copy parity for Linux Mascot.
- Phase 57: validator coverage, Node tests, leakage scans, trademark-boundary scans, public sample gates, generated sample gates, route smoke, uploaded-image and source-boundary smoke, docs consistency, and release evidence.
- Future requirements: public generated Linux Mascot sample gallery after release approval, machine-readable route manifests, uploaded source-image hashing automation, visual regression, public comparison sheets, release packaging, and selected-IP installation variants.

</deferred>

---

*Phase: 55-Linux Mascot Skill Controller Integration*
*Context gathered: 2026-07-01*
