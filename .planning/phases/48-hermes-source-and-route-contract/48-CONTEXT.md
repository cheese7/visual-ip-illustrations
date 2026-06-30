# Phase 48: Hermes Source and Route Contract - Context

**Gathered:** 2026-06-18
**Status:** Ready for planning

<domain>
## Phase Boundary

Phase 48 delivers the Hermes Agent route and source authority contract for v1.10. The phase locks only route selection metadata, source-record authority, output path contract, uploaded-image authority, public sample policy, official source and MIT license context, review ownership, route status, and existing-route compatibility.

In scope:

- Add Hermes Agent to `skills/visual-ip-illustrations/references/routing.md` as an explicit selectable visual IP route.
- Create the Hermes Agent source record at `skills/visual-ip-illustrations/references/ips/hermes/source.md`.
- Lock the Hermes route id, display name, aliases, `default=false`, output suffix, output path, source authority, uploaded-image authority, public sample policy, mythology-drift boundary, product-poster boundary, review owner, and route status.
- Preserve Xiaohei as the omitted-IP default while Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, and Hermes remain explicit isolated routes.

Later phases own the full Hermes route-local pack, skill controller dispatch, public docs, metadata, validation, tests, and release evidence.

</domain>

<decisions>
## Implementation Decisions

### Route Contract

- **D-01:** Hermes route id is `hermes`.
- **D-02:** Hermes display name is `Hermes Agent`.
- **D-03:** Hermes route metadata uses `default=false`.
- **D-04:** Hermes route status is `source-reviewed`.
- **D-05:** Hermes output suffix is `hermes`.
- **D-06:** Hermes output path is `assets/<article-slug>-hermes/`.
- **D-07:** Documentation and validation surfaces should preserve the escaped marker `assets/&lt;article-slug&gt;-hermes/` when escaped path markers are relevant.
- **D-08:** The route table should follow the existing `routing.md` shape: `id`, `display_name`, `aliases`, `default`, `output_suffix`, `required_references`, `attribution_context`, and `status`.
- **D-09:** Phase 48 should keep Hermes `required_references` limited to `references/ips/hermes/source.md`. Phase 49 can expand the row after the full Hermes pack exists.

### Alias Boundary

- **D-10:** Hermes aliases include `Hermes Agent`, `Hermes`, `hermes`, `hermes-agent`, `Hermes logo`, and `Hermes Agent logo`.
- **D-11:** Alias matching should stay limited to the explicit aliases in D-10 for Phase 48.
- **D-12:** Broad assistant, AI agent, logo, anime, monochrome girl, fashion figure, Greek messenger, winged sandals, and caduceus terms stay outside the Phase 48 alias set.

### Source Record Contract

- **D-13:** The source record path is `skills/visual-ip-illustrations/references/ips/hermes/source.md`.
- **D-14:** The source record must record official Hermes Agent website, Nous Research repository, MIT license URL, documentation URL, user-uploaded conversation attachment authority, source-image context, public sample policy, review owner, route status, and distribution boundary.
- **D-15:** Official website is `https://hermes-agent.nousresearch.com/`.
- **D-16:** Official repository is `https://github.com/NousResearch/hermes-agent`.
- **D-17:** MIT license URL is `https://github.com/NousResearch/hermes-agent/blob/main/LICENSE`.
- **D-18:** Documentation URL is `https://hermes-agent.nousresearch.com/docs/`.
- **D-19:** Uploaded visual authority is the conversation attachment named `Generated image 1 (16).jpeg`; the local `/Users/carson/Downloads/Generated image 1 (16).jpeg` path is unavailable from this workspace and should not be treated as a repository dependency.
- **D-20:** Source wording should treat Hermes Agent as a source-reviewed uploaded-image article-illustration route with official Hermes Agent context and MIT license context.
- **D-21:** Public generated Hermes samples require release review before publication.

### Uploaded Visual Authority

- **D-22:** The uploaded conversation attachment is the visual authority for the route.
- **D-23:** Fixed uploaded-image markers are monochrome full-body logo-style character, black bob haircut with bright highlights, headset or earpiece, black sleeveless dress, white collar tag with an `A`-like mark, black thigh-high stockings, platform heels, and slender fashion-figure posture.
- **D-24:** Phase 48 records the marker list as source and route authority. Phase 49 turns the same markers into detailed identity, style, prompt, edit, and QA behavior.

### Source and Usage Boundary

- **D-25:** Generated Hermes route outputs stay sparse 16:9 article illustrations.
- **D-26:** Product advertising, product-poster output, CLI screenshots, web hero graphics, official endorsement, affiliation, sponsorship, approval, or impersonation claims stay outside this route.
- **D-27:** Mythological Hermes imagery stays outside default route behavior. Default outputs should not use winged sandals, winged helmet, caduceus, Greek messenger scenes, Olympian deity framing, or mythology-first symbols.
- **D-28:** Generic anime assistant drift, generic logo mascot drift, passive placement, route leakage, excessive text, and copied composition stay outside positive route identity.
- **D-29:** Hermes public sample copy should present the subject as a source-reviewed uploaded-image article-illustration route with official source and MIT license context.

### Existing Route Compatibility

- **D-30:** Xiaohei remains the omitted-IP default.
- **D-31:** Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, and Hermes remain explicit routes with isolated references.
- **D-32:** Hermes source/route work stays under `skills/visual-ip-illustrations/references/ips/hermes/` and preserves the route-local isolation pattern used by the existing routes.
- **D-33:** Phase 48 preserves route behavior for Xiaohei, Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, and Cai Xukun.

### the agent's Discretion

- The implementation planner may choose exact Markdown section ordering inside `source.md`, provided D-13 through D-29 remain explicit and grep-friendly.
- The implementation planner should append Hermes after Cai Xukun in `routing.md` to preserve existing route order while adding the v1.10 route.
- The implementation planner should create only `source.md` in Phase 48; Phase 49 owns the pack index and the full route-local reference set.

</decisions>

<canonical_refs>
## Canonical References

**Downstream agents MUST read these before planning or implementing.**

### Planning Scope

- `.planning/PROJECT.md` - v1.10 milestone goal, Hermes constraints, uploaded-image authority, and source-reviewed route intent.
- `.planning/REQUIREMENTS.md` - Phase 48 requirement IDs `ROUTE-01`, `ROUTE-02`, `ROUTE-03`, `SRC-01`, and `SRC-02`.
- `.planning/ROADMAP.md` - Phase 48 goal, success criteria, dependencies, and phase boundaries for Phases 49-52.
- `.planning/STATE.md` - current v1.10 state, accumulated default-route decisions, route-isolation history, and Hermes milestone notes.

### Codebase Maps

- `.planning/codebase/ARCHITECTURE.md` - documentation-first skill architecture, progressive reference loading, and route-local reference policy.
- `.planning/codebase/CONVENTIONS.md` - Markdown conventions, repository-relative paths, English-default content, and route reference style.
- `.planning/codebase/STRUCTURE.md` - package layout, route-local reference placement, public docs placement, and generated asset path rules.

### Existing Public and Runtime Surfaces

- `skills/visual-ip-illustrations/references/routing.md` - live route table, selection rules, output path markers, mixed-IP route grouping, attribution context, and delivery fields.
- `skills/visual-ip-illustrations/SKILL.md` - runtime skill entrypoint, route selection, progressive reference loading, delivery report, and save-path contract.
- `README.md` - public install, route selection, workflow, examples, and route description surface.
- `examples/prompts.md` - copyable planning, generation, editing, and mixed-IP prompt surface.
- `NOTICE.md` - attribution and legal notice surface for source-reviewed and gated routes.
- `RELEASE_CHECKLIST.md` - release review, public sample, generated sample, docs, and evidence gates.

### Existing Route Contracts

- `skills/visual-ip-illustrations/references/ips/gopher/source.md` - source-reviewed route/source precedent with official source, license, visual authority, public sample policy, and review owner.
- `skills/visual-ip-illustrations/references/ips/openclaw/source.md` - uploaded visual authority precedent with source record, marker list, sample policy, review owner, and distribution boundary.
- `skills/visual-ip-illustrations/references/ips/caixukun/source.md` - recent route/source-only precedent with uploaded-image authority, route status, output path, boundary wording, and later-phase handoff.
- `.planning/phases/43-cai-xukun-source-and-route-contract/43-CONTEXT.md` - analogous source and route contract decisions.
- `.planning/phases/43-cai-xukun-source-and-route-contract/43-01-SUMMARY.md` - analogous execution evidence and scope boundary.

### Planned Phase 48 Artifacts

- `skills/visual-ip-illustrations/references/ips/hermes/source.md` - planned official source, MIT license, uploaded-image authority, source-image context, sample policy, review owner, and route status record.
- `Generated image 1 (16).jpeg` conversation attachment - uploaded visual authority. Local file path is unavailable from this workspace.

### Validation Surfaces

- `scripts/validate-skill-package.mjs` - dependency-free validator surface that Phase 52 should extend for Hermes route/source/docs/sample markers.
- `scripts/validate-skill-package.test.mjs` - Node regression test surface that Phase 52 should extend for Hermes route parsing, marker drift, mythology-drift gates, leakage fixtures, public sample gates, and full-pass output.

</canonical_refs>

<code_context>
## Existing Code Insights

### Reusable Assets

- `skills/visual-ip-illustrations/references/routing.md` already centralizes route metadata, aliases, default flags, output suffixes, required references, attribution context, route statuses, mixed-IP grouping, output paths, and delivery fields.
- `skills/visual-ip-illustrations/references/ips/gopher/source.md` is a strong precedent for source-reviewed route authority and license context.
- `skills/visual-ip-illustrations/references/ips/openclaw/source.md` and `skills/visual-ip-illustrations/references/ips/caixukun/source.md` are strong uploaded-image authority precedents.

### Established Patterns

- Xiaohei is the only omitted-IP default.
- Additional IPs are explicit routes with `default=false`, route-specific aliases, route-local references, route-specific output suffixes, route-specific output directories, and route status.
- Source, rights, local visual authority, or uploaded-image authority is recorded route-locally before broad docs, controller integration, validation, and public generated samples expand the route.
- Public generated samples for protected, source-reviewed, uploaded-image, local-reference, public-figure, or brand-sensitive routes require release review.
- Route-specific style, identity, composition, prompt, edit, and QA rules stay isolated under `skills/visual-ip-illustrations/references/ips/<route>/`.

### Integration Points

- Phase 48 connects to `skills/visual-ip-illustrations/references/routing.md` and `skills/visual-ip-illustrations/references/ips/hermes/source.md`.
- Phase 49 expands Hermes into the full route-local pack.
- Phase 50 wires Hermes into `skills/visual-ip-illustrations/SKILL.md` runtime route selection and mixed-IP dispatch.
- Phase 51 updates README variants, examples, NOTICE, release checklist, broad skill docs, and `agents/openai.yaml`.
- Phase 52 extends the validator, Node regression tests, leakage checks, mythology-drift checks, public sample gates, generated sample gates, and release evidence.

</code_context>

<specifics>
## Specific Ideas

- Hermes route metadata should use `source-reviewed` to keep official source, MIT license, uploaded-image authority, and public-sample review visible from the first source/route phase.
- The source record should name the official website, repository, license URL, docs URL, and conversation attachment authority exactly.
- The marker list should appear together in `source.md`: monochrome full-body logo-style character, black bob haircut with bright highlights, headset or earpiece, black sleeveless dress, white collar tag with an `A`-like mark, black thigh-high stockings, platform heels, and slender fashion-figure posture.
- Mythological Hermes default behavior should be blocked with exact drift markers: winged sandals, winged helmet, caduceus, Greek messenger scenes, Olympian deity framing, and mythology-first symbols.
- Product advertising, product-poster output, CLI screenshots, web hero graphics, official endorsement, affiliation, sponsorship, approval, and impersonation should stay outside Hermes route identity and sample copy.
- Mixed-IP requests should treat Hermes as its own route group with its own source record and output directory.

</specifics>

<deferred>
## Deferred Ideas

- Phase 49: Hermes style DNA, identity rules, composition patterns, prompt template, edit prompts, QA checklist, sample-policy wording, full route-local pack navigation, and expanded `required_references`.
- Phase 50: Hermes skill controller integration, selected-IP reference loading, mixed-IP grouping, generation/edit routing, QA dispatch, and delivery reporting.
- Phase 51: README variants, examples, NOTICE, RELEASE_CHECKLIST, broad `SKILL.md` docs, and `agents/openai.yaml` Hermes discovery wording.
- Phase 52: validator coverage, Node tests, leakage scans, mythology-drift scans, public sample gates, generated sample gates, route smoke, uploaded-image and source-boundary smoke, docs consistency, and release evidence.
- Future requirements: machine-readable route manifests, uploaded source-image hashing, visual regression, public comparison sheets, release packaging, and selected-IP installation variants.

</deferred>

---

*Phase: 48-Hermes Source and Route Contract*
*Context gathered: 2026-06-18*
