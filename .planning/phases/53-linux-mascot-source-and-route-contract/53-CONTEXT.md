# Phase 53: Linux Mascot Source and Route Contract - Context

**Gathered:** 2026-07-01
**Status:** Ready for planning

<domain>
## Phase Boundary

Phase 53 delivers the Linux Mascot route and source authority contract for v1.11. The phase locks only route selection metadata, source-record authority, output path contract, uploaded-image authority, public sample policy, Tux attribution, Linux trademark-boundary context, review ownership, route status, and existing-route compatibility.

In scope:

- Add Linux Mascot to `skills/visual-ip-illustrations/references/routing.md` as an explicit selectable visual IP route.
- Create the Linux Mascot source record at `skills/visual-ip-illustrations/references/ips/linux/source.md`.
- Lock the Linux Mascot route id, display name, aliases, `default=false`, output suffix, output path, source authority, uploaded-image authority, public sample policy, Linux trademark boundary, distro-logo boundary, review owner, and route status.
- Preserve Xiaohei as the omitted-IP default while Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, Hermes Agent, and Linux Mascot remain explicit isolated routes.

Later phases own the full Linux Mascot route-local pack, skill controller dispatch, public docs, metadata, validation, tests, and release evidence.

</domain>

<decisions>
## Implementation Decisions

### Route Contract

- **D-01:** Linux Mascot route id is `linux`.
- **D-02:** Linux Mascot display name is `Linux Mascot`.
- **D-03:** Linux Mascot route metadata uses `default=false`.
- **D-04:** Linux Mascot route status is `source-reviewed`.
- **D-05:** Linux Mascot output suffix is `linux`.
- **D-06:** Linux Mascot output path is `assets/<article-slug>-linux/`.
- **D-07:** Documentation and validation surfaces should preserve the escaped marker `assets/&lt;article-slug&gt;-linux/` when escaped path markers are relevant.
- **D-08:** The route table should follow the existing `routing.md` shape: `id`, `display_name`, `aliases`, `default`, `output_suffix`, `required_references`, `attribution_context`, and `status`.
- **D-09:** Phase 53 should keep Linux Mascot `required_references` limited to `references/ips/linux/source.md`. Phase 54 can expand the row after the full Linux Mascot pack exists.

### Alias Boundary

- **D-10:** Linux Mascot aliases include `Linux Mascot`, `Linux mascot`, `Linux`, `linux`, `Tux`, `tux`, `Linux penguin`, and `Tux penguin`.
- **D-11:** Alias matching should stay limited to the explicit aliases in D-10 for Phase 53.
- **D-12:** Broad penguin, server, kernel, distro, distro-logo, Linux Foundation, operating-system, CLI, terminal, product, brand-campaign, and generic mascot terms stay outside the Phase 53 alias set.

### Source Record Contract

- **D-13:** The source record path is `skills/visual-ip-illustrations/references/ips/linux/source.md`.
- **D-14:** The source record must record Larry Ewing Tux attribution, GIMP attribution condition, Linux Foundation trademark guidance, Linux trademark ownership context, uploaded local image authority, source-image context, public sample policy, review owner, route status, and distribution boundary.
- **D-15:** Tux creator attribution is Larry Ewing.
- **D-16:** Tux permission context should cite Larry Ewing's Linux 2.0 Penguins page: `https://isc.tamu.edu/~lewing/linux/`.
- **D-17:** GIMP attribution condition should preserve the Ewing permission wording in route-local source context: acknowledge Larry Ewing and The GIMP if someone asks.
- **D-18:** Linux Foundation trademark guidance should cite `https://www.linuxfoundation.org/legal/trademark-usage` and keep trademark uses factual, adjective-style, ownership-attributed, and free of endorsement or certification claims.
- **D-19:** Linux mark ownership context should cite `https://www.linuxfoundation.org/legal/the-linux-mark` and preserve the required ownership attribution pattern: Linux is the registered trademark of Linus Torvalds in the U.S. and other countries.
- **D-20:** The source record should note that Tux the Penguin is an image created by Larry Ewing and is outside Linux Foundation ownership, while Linux word-mark usage remains governed by Linux trademark guidance.
- **D-21:** Public generated Linux Mascot samples require release review before publication.
- **D-22:** Source wording should treat Linux Mascot as a source-reviewed uploaded-image article-illustration route with Tux source context, Linux trademark context, and uploaded-image authority.

### Uploaded Visual Authority

- **D-23:** Uploaded visual authority is `/Users/longnv/Downloads/Linux-logo.jpg`.
- **D-24:** The uploaded file metadata recorded during discussion is: JPEG image data, JFIF 1.01, progressive, 8-bit precision, 3500x2300 pixels, 3 components, SHA-256 `071bc327e4a2814864f9e2fcdea99aa50482a92ef4e816de9d9ce5f40e17bb2a`.
- **D-25:** The uploaded local image is the visual authority for this route. Downstream work should preserve the local path in source context and treat it as a user-provided visual reference.
- **D-26:** Fixed uploaded-image markers are glossy black rounded penguin head and body, white face eye patches, large oval eyes with dark pupils and small highlights, yellow-orange beak with two nostril dots, white oval belly, long black flippers, seated rounded posture, and oversized yellow-orange webbed feet.
- **D-27:** Phase 53 records the marker list as source and route authority. Phase 54 turns the same markers into detailed identity, style, prompt, edit, and QA behavior.

### Source and Usage Boundary

- **D-28:** Generated Linux Mascot route outputs stay sparse 16:9 article illustrations.
- **D-29:** Official Linux endorsement, affiliation, sponsorship, approval, certification, compatibility, Linux Foundation campaign framing, Linux Foundation logo use, distro-logo use, and distro branding stay outside this route.
- **D-30:** Product advertising, product-poster output, CLI screenshots, web hero graphics, kernel dashboard screenshots, and operating-system marketing graphics stay outside this route.
- **D-31:** Generic penguin drift, generic server mascot drift, distro-logo drift, passive placement, route leakage, excessive text, and copied composition stay outside positive route identity.
- **D-32:** Linux Mascot public sample copy should present the subject as a source-reviewed uploaded-image article-illustration route with Tux attribution, Linux trademark-boundary context, and uploaded local image authority.

### Existing Route Compatibility

- **D-33:** Xiaohei remains the omitted-IP default.
- **D-34:** Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, Hermes Agent, and Linux Mascot remain explicit routes with isolated references.
- **D-35:** Linux Mascot source/route work stays under `skills/visual-ip-illustrations/references/ips/linux/` and preserves the route-local isolation pattern used by the existing routes.
- **D-36:** Phase 53 preserves route behavior for Xiaohei, Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, and Hermes Agent.

### the agent's Discretion

- The implementation planner may choose exact Markdown section ordering inside `source.md`, provided D-13 through D-32 remain explicit and grep-friendly.
- The implementation planner should append Linux Mascot after Hermes Agent in `routing.md` to preserve existing route order while adding the v1.11 route.
- The implementation planner should create only `source.md` in Phase 53; Phase 54 owns the pack index and the full route-local reference set.

</decisions>

<canonical_refs>
## Canonical References

**Downstream agents MUST read these before planning or implementing.**

### Planning Scope

- `.planning/PROJECT.md` - v1.11 milestone goal, Linux Mascot constraints, uploaded-image authority, Tux attribution, Linux trademark boundary, and source-reviewed route intent.
- `.planning/REQUIREMENTS.md` - Phase 53 requirement IDs `ROUTE-01`, `ROUTE-02`, `ROUTE-03`, `SRC-01`, and `SRC-02`.
- `.planning/ROADMAP.md` - Phase 53 goal, success criteria, dependencies, and phase boundaries for Phases 54-57.
- `.planning/STATE.md` - current v1.11 state, accumulated default-route decisions, route-isolation history, and Linux Mascot milestone notes.

### Codebase Maps

- `.planning/codebase/ARCHITECTURE.md` - documentation-first skill architecture, progressive reference loading, route-local reference policy, and no build runtime.
- `.planning/codebase/CONVENTIONS.md` - Markdown conventions, repository-relative paths, English-default content, and route reference style.
- `.planning/codebase/STRUCTURE.md` - package layout, route-local reference placement, public docs placement, and generated asset path rules.

### Existing Public and Runtime Surfaces

- `skills/visual-ip-illustrations/references/routing.md` - live route table, selection rules, output path markers, mixed-IP route grouping, attribution context, route statuses, and delivery fields.
- `skills/visual-ip-illustrations/SKILL.md` - runtime skill entrypoint, route selection, progressive reference loading, delivery report, and save-path contract.
- `skills/visual-ip-illustrations/agents/openai.yaml` - agent metadata surface for route discovery and default prompt copy.
- `README.md` - public install, route selection, workflow, examples, and route description surface.
- `examples/prompts.md` - copyable planning, generation, editing, and mixed-IP prompt surface.
- `NOTICE.md` - attribution and legal notice surface for source-reviewed and gated routes.
- `RELEASE_CHECKLIST.md` - release review, public sample, generated sample, docs, and evidence gates.

### Existing Route Contracts

- `skills/visual-ip-illustrations/references/ips/hermes/source.md` - closest source-reviewed uploaded-image route precedent with source record, marker list, sample policy, review owner, route status, distribution boundary, and later-phase handoff.
- `skills/visual-ip-illustrations/references/ips/gopher/source.md` - source-reviewed mascot route precedent with creator attribution, license boundary, local visual authority, public sample policy, and review owner.
- `skills/visual-ip-illustrations/references/ips/openclaw/source.md` - source-reviewed uploaded-logo authority precedent with source record, marker list, sample policy, review owner, and distribution boundary.
- `skills/visual-ip-illustrations/references/ips/caixukun/source.md` - uploaded-image authority precedent with route status, output path, source-image context, boundary wording, and later-phase handoff.
- `.planning/phases/48-hermes-source-and-route-contract/48-CONTEXT.md` - analogous source and route contract decisions.
- `.planning/phases/48-hermes-source-and-route-contract/48-DISCUSSION-LOG.md` - analogous autonomous discussion audit trail.

### Planned Phase 53 Artifacts

- `skills/visual-ip-illustrations/references/ips/linux/source.md` - planned Tux attribution, GIMP attribution condition, Linux trademark guidance, uploaded-image authority, source-image context, sample policy, review owner, route status, and distribution boundary record.
- `/Users/longnv/Downloads/Linux-logo.jpg` - uploaded visual authority. Local metadata: JPEG, 3500x2300, SHA-256 `071bc327e4a2814864f9e2fcdea99aa50482a92ef4e816de9d9ce5f40e17bb2a`.

### External Source Anchors

- `https://isc.tamu.edu/~lewing/linux/` - Larry Ewing Linux 2.0 Penguins page, Tux image permission, and GIMP attribution condition.
- `https://www.linuxfoundation.org/legal/the-linux-mark` - Linux mark ownership attribution, Linux Foundation sublicensing context, and statement that Tux is created by Larry Ewing and outside Linux Foundation ownership.
- `https://www.linuxfoundation.org/legal/trademark-usage` - Linux Foundation trademark usage guidance for factual use, attribution, and endorsement-safe wording.

### Validation Surfaces

- `scripts/validate-skill-package.mjs` - dependency-free validator surface that Phase 57 should extend for Linux Mascot route/source/docs/sample markers.
- `scripts/validate-skill-package.test.mjs` - Node regression test surface that Phase 57 should extend for Linux Mascot route parsing, marker drift, trademark-boundary gates, leakage fixtures, public sample gates, generated sample gates, and full-pass output.

</canonical_refs>

<code_context>
## Existing Code Insights

### Reusable Assets

- `skills/visual-ip-illustrations/references/routing.md` already centralizes route metadata, aliases, default flags, output suffixes, required references, attribution context, route statuses, mixed-IP grouping, output paths, and delivery fields.
- `skills/visual-ip-illustrations/references/ips/hermes/source.md` is the strongest precedent for a source-reviewed uploaded-image route with source context, visual markers, sample policy, review owner, and distribution boundary.
- `skills/visual-ip-illustrations/references/ips/gopher/source.md` is the strongest precedent for mascot source attribution, license or trademark boundary language, local visual authority, and public sample review.
- `scripts/validate-skill-package.mjs` already contains route metadata parsers, output path token checks, source marker checks, public asset gates, generated sample gates, route leakage gates, and release evidence checks.

### Established Patterns

- Xiaohei is the only omitted-IP default.
- Additional IPs are explicit routes with `default=false`, route-specific aliases, route-local references, route-specific output suffixes, route-specific output directories, and route status.
- Source, rights, local visual authority, or uploaded-image authority is recorded route-locally before broad docs, controller integration, validation, and public generated samples expand the route.
- Public generated samples for protected, source-reviewed, uploaded-image, local-reference, public-figure, or brand-sensitive routes require release review.
- Route-specific style, identity, composition, prompt, edit, and QA rules stay isolated under `skills/visual-ip-illustrations/references/ips/<route>/`.

### Integration Points

- Phase 53 connects to `skills/visual-ip-illustrations/references/routing.md` and `skills/visual-ip-illustrations/references/ips/linux/source.md`.
- Phase 54 expands Linux Mascot into the full route-local pack.
- Phase 55 wires Linux Mascot into `skills/visual-ip-illustrations/SKILL.md` runtime route selection and mixed-IP dispatch.
- Phase 56 updates README variants, examples, NOTICE, release checklist, broad skill docs, and `agents/openai.yaml`.
- Phase 57 extends the validator, Node regression tests, leakage checks, trademark-boundary checks, public sample gates, generated sample gates, and release evidence.

</code_context>

<specifics>
## Specific Ideas

- Linux Mascot route metadata should use `source-reviewed` to keep Tux attribution, GIMP attribution condition, Linux trademark context, uploaded-image authority, and public-sample review visible from the first source/route phase.
- The source record should name Larry Ewing, The GIMP attribution condition, Linux Foundation trademark usage guidance, Linux trademark ownership context, and the uploaded file path exactly.
- The marker list should appear together in `source.md`: glossy black rounded penguin head and body, white face eye patches, large oval eyes with dark pupils and small highlights, yellow-orange beak with two nostril dots, white oval belly, long black flippers, seated rounded posture, and oversized yellow-orange webbed feet.
- Trademark-boundary language should cover Linux word-mark attribution, Linux Foundation guidance, official endorsement, affiliation, sponsorship, approval, certification, compatibility, distro branding, Linux Foundation logo use, and Linux Foundation campaign drift.
- Product advertising, product-poster output, CLI screenshots, kernel dashboard screenshots, web hero graphics, generic server mascot drift, passive placement, route leakage, excessive text, and copied composition should stay outside Linux Mascot route identity and sample copy.
- Mixed-IP requests should treat Linux Mascot as its own route group with its own source record and output directory.

</specifics>

<deferred>
## Deferred Ideas

- Phase 54: Linux Mascot style DNA, identity rules, composition patterns, prompt template, edit prompts, QA checklist, sample-policy wording, full route-local pack navigation, and expanded `required_references`.
- Phase 55: Linux Mascot skill controller integration, selected-IP reference loading, mixed-IP grouping, generation/edit routing, QA dispatch, and delivery reporting.
- Phase 56: README variants, examples, NOTICE, RELEASE_CHECKLIST, broad `SKILL.md` docs, and `agents/openai.yaml` Linux Mascot discovery wording.
- Phase 57: validator coverage, Node tests, leakage scans, trademark-boundary scans, public sample gates, generated sample gates, route smoke, uploaded-image and source-boundary smoke, docs consistency, and release evidence.
- Future requirements: machine-readable route manifests, uploaded source-image hashing, visual regression, public comparison sheets, release packaging, and selected-IP installation variants.

</deferred>

---

*Phase: 53-Linux Mascot Source and Route Contract*
*Context gathered: 2026-07-01*
