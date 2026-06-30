# Phase 54: Linux Mascot Canonical Pack - Context

**Gathered:** 2026-07-01
**Status:** Ready for planning

<domain>
## Phase Boundary

Phase 54 delivers the Linux Mascot route-local canonical pack. The phase creates the operational reference files that let users plan, prompt, edit, and QA Linux Mascot article illustrations while preserving the Phase 53 source-reviewed route contract, uploaded Tux visual authority, Larry Ewing attribution, The GIMP attribution condition, Linux trademark-boundary context, output path, and public sample review boundary.

In scope:

- Create the full Linux Mascot route-local pack under `skills/visual-ip-illustrations/references/ips/linux/`.
- Create `index.md`, `style-dna.md`, `linux-ip.md`, `composition-patterns.md`, `prompt-template.md`, and `qa-checklist.md`.
- Preserve `source.md` as the authority record, with refinement only when needed for pack navigation or current pack status.
- Update the Linux row in `skills/visual-ip-illustrations/references/routing.md` after pack files exist so `required_references` points to the full seven-file Linux pack.
- Keep Linux Mascot prompts and QA centered on Tux performing the central cognitive article action in sparse 16:9 article illustrations.
- Keep public generated Linux Mascot samples gated by release review. Phase 54 creates no public sample images.

Later phases own runtime controller integration, public docs, metadata, NOTICE, release checklist, validator expansion, Node tests, and release evidence.

</domain>

<decisions>
## Implementation Decisions

### Pack File Set

- **D-01:** Phase 54 creates the full Linux Mascot route-local pack under `skills/visual-ip-illustrations/references/ips/linux/`.
- **D-02:** Create `skills/visual-ip-illustrations/references/ips/linux/index.md` for pack navigation, route contract, references, uploaded marker set, failure categories, operational coherence, and scope boundary.
- **D-03:** Preserve `skills/visual-ip-illustrations/references/ips/linux/source.md` as the authority record; refine only when pack navigation or current route-local pack status needs a source-record update.
- **D-04:** Create `skills/visual-ip-illustrations/references/ips/linux/style-dna.md` for sparse 16:9 Linux Mascot article-illustration style, uploaded Tux marker preservation, trademark-boundary gates, visual vetoes, stable gates, and route isolation.
- **D-05:** Create `skills/visual-ip-illustrations/references/ips/linux/linux-ip.md` for Tux identity, recognition rules, cognitive-action responsibility, action verbs, source/trademark boundaries, route boundary, and failure modes.
- **D-06:** Create `skills/visual-ip-illustrations/references/ips/linux/composition-patterns.md` for composition families, original article-metaphor invention, Tux action patterns, supporting object pools, anti-repeat rules, trademark drift guardrails, and route leakage boundaries.
- **D-07:** Create `skills/visual-ip-illustrations/references/ips/linux/prompt-template.md` for planning fields, one-image generation prompt, edit prompts, uploaded-image identity repair, trademark-boundary repair, title removal, text reduction, route leakage repair, and unaffected-content preservation.
- **D-08:** Create `skills/visual-ip-illustrations/references/ips/linux/qa-checklist.md` for pass/fail gates, Tux identity checks, iteration moves, trademark-boundary repair, route leakage repair, public sample boundary, and delivery judgment.

### Route Reference Expansion

- **D-09:** Update `skills/visual-ip-illustrations/references/routing.md` after the Linux pack files exist so the Linux `required_references` cell expands from source-only to the full seven-file pack.
- **D-10:** The expanded Linux `required_references` list must include `references/ips/linux/index.md`; `references/ips/linux/source.md`; `references/ips/linux/style-dna.md`; `references/ips/linux/linux-ip.md`; `references/ips/linux/composition-patterns.md`; `references/ips/linux/prompt-template.md`; `references/ips/linux/qa-checklist.md`.
- **D-11:** Keep Linux Mascot route metadata unchanged: route id `linux`, display name `Linux Mascot`, aliases `Linux Mascot`, `Linux mascot`, `Linux`, `linux`, `Tux`, `tux`, `Linux penguin`, and `Tux penguin`, `default=false`, output suffix `linux`, output path `assets/<article-slug>-linux/`, and status `source-reviewed`.
- **D-12:** Preserve Xiaohei as the only omitted-IP default and preserve all existing non-Linux route behavior.

### Source Authority Preservation

- **D-13:** Preserve Phase 53 uploaded visual authority exactly: `/Users/longnv/Downloads/Linux-logo.jpg`.
- **D-14:** Preserve Phase 53 file metadata and SHA-256: JPEG image data, JFIF 1.01, progressive, 8-bit precision, 3500x2300 pixels, 3 components, SHA-256 `071bc327e4a2814864f9e2fcdea99aa50482a92ef4e816de9d9ce5f40e17bb2a`.
- **D-15:** Preserve the full uploaded visual marker set together: glossy black rounded penguin head and body, white face eye patches, large oval eyes with dark pupils and small highlights, yellow-orange beak with two nostril dots, white oval belly, long black flippers, seated rounded posture, and oversized yellow-orange webbed feet.
- **D-16:** Preserve Larry Ewing as Tux creator attribution.
- **D-17:** Preserve Larry Ewing's Linux 2.0 Penguins page as source context: `https://isc.tamu.edu/~lewing/linux/`.
- **D-18:** Preserve The GIMP attribution condition from Phase 53: acknowledge Larry Ewing and The GIMP if someone asks.
- **D-19:** Preserve Linux Foundation trademark usage guidance: `https://www.linuxfoundation.org/legal/trademark-usage`.
- **D-20:** Preserve Linux mark ownership context: `https://www.linuxfoundation.org/legal/the-linux-mark`.
- **D-21:** Preserve ownership attribution wording: Linux is the registered trademark of Linus Torvalds in the U.S. and other countries.
- **D-22:** Preserve the source distinction that Tux the Penguin is an image created by Larry Ewing and that Linux word-mark use follows Linux trademark guidance.
- **D-23:** Preserve public generated Linux Mascot sample approval gating before publication.

### Prompt, Edit, and QA Behavior

- **D-24:** Linux Mascot prompts must make Tux the central cognitive article-action subject in sparse 16:9 illustrations.
- **D-25:** The article metaphor should depend on Tux's physical action; removing Tux should break the metaphor.
- **D-26:** Planning fields must include Placement, Core idea, Structure type, Linux Mascot state, Linux Mascot action, Supporting objects, Visible labels, Source context note, Trademark-boundary note, and Output path.
- **D-27:** Visible labels follow the user's requested language. Prompt instructions and route reference prose remain English.
- **D-28:** Edit prompts must include stronger mascot participation, uploaded-image identity repair, title removal, text reduction, trademark-boundary repair, route leakage repair, and unaffected-content preservation.
- **D-29:** QA must reject generic penguin drift, distro-logo drift, missing white belly, missing yellow-orange beak, missing oversized yellow-orange webbed feet, missing seated Tux posture, official endorsement claims, passive placement, route leakage, excessive text, and copied composition.
- **D-30:** QA must also reject missing glossy black rounded penguin head and body, missing white face eye patches, missing large oval eyes with dark pupils and small highlights, missing yellow-orange beak with two nostril dots, missing long black flippers, source-image pose copying, product-poster drift, CLI screenshots, web hero graphics, kernel dashboard screenshots, operating-system marketing graphics, Linux Foundation logo use, distro branding, and certification or compatibility claims.
- **D-31:** Linux Mascot output remains a sparse article illustration route: one core idea, one composition family, generous whitespace, rough hand-drawn linework, 2-6 short visible labels, and article-metaphor supporting objects.

### Sample and Scope Boundaries

- **D-32:** Phase 54 creates no public generated Linux Mascot sample images.
- **D-33:** Public generated Linux Mascot samples remain behind release review before use in `examples/images/`, `examples/images-en/`, `skills/visual-ip-illustrations/assets/examples/`, README galleries, release galleries, agent metadata previews, or public release surfaces.
- **D-34:** Phase 54 stays limited to Linux route-local pack files, optional Linux `source.md` navigation/status refinement, and Linux `routing.md` `required_references` expansion.
- **D-35:** Linux Mascot markers and route wording stay route-local and should not leak into Xiaohei, Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, or Hermes Agent pack files.

### the agent's Discretion

- The planner may choose exact Markdown section ordering inside each Linux pack file, provided D-01 through D-35 remain explicit and grep-friendly.
- The planner should use Hermes Phase 49 as the closest source-reviewed uploaded-image pack precedent, Go Gopher as the strongest source-reviewed mascot pack precedent, and OpenClaw as the compact uploaded-logo repair precedent.
- The planner may add deterministic marker phrases that help Phase 57 validation, provided they stay Linux route-local and English-default.
- Subagent execution constraint: the user requested subagents for every stage. The parent Codex thread delegated Phase 54 stage work to subagents during the phases 53-57 rollout. Inside the Phase 54 stage agent, tool discovery exposed GitHub and CodeGraph tools but no callable `spawn_agent`, `wait`, or `close_agent`, so nested GSD discussion roles ran inline within that delegated agent and kept the same audit trail.

</decisions>

<canonical_refs>
## Canonical References

**Downstream agents MUST read these before planning or implementing.**

### Planning Scope

- `.planning/PROJECT.md` - v1.11 milestone goal, Linux Mascot source-reviewed route constraints, uploaded-image authority, Tux attribution, Linux trademark boundary, and no-build-runtime project rules.
- `.planning/REQUIREMENTS.md` - Phase 54 requirement IDs `PACK-01`, `PACK-02`, `PACK-03`, `PACK-04`, and `PACK-05`.
- `.planning/ROADMAP.md` - Phase 54 goal, success criteria, dependency on Phase 53, and Phase 55-57 boundaries.
- `.planning/STATE.md` - current milestone state, accumulated default-route decisions, route isolation history, Phase 53 completion notes, and pending Phase 54 state.

### Phase 53 Source and Route Contract

- `.planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md` - locked Phase 53 route, source, uploaded-image, Tux attribution, trademark-boundary, public sample policy, and later-phase handoff decisions.
- `.planning/phases/53-linux-mascot-source-and-route-contract/53-01-SUMMARY.md` - implementation evidence for the Linux route row and source record.
- `.planning/phases/53-linux-mascot-source-and-route-contract/53-VERIFICATION.md` - verification evidence that Phase 53 passed and that full route-local pack work belongs to Phase 54.

### Live Linux Route Files

- `skills/visual-ip-illustrations/references/routing.md` - live Linux route row, aliases, output path, `source-reviewed` status, mixed-IP route grouping, and current source-only `required_references`.
- `skills/visual-ip-illustrations/references/ips/linux/source.md` - Larry Ewing attribution, The GIMP attribution condition, Linux Foundation trademark guidance, Linux mark ownership context, uploaded local image authority, SHA-256, marker list, sample policy, route status, distribution boundary, and review owner.

### Analog Hermes Canonical Pack Artifacts

- `.planning/phases/49-hermes-canonical-pack/49-CONTEXT.md` - analogous source-reviewed uploaded-image canonical pack decisions, file set, route expansion, identity gates, and verification targets.
- `.planning/phases/49-hermes-canonical-pack/49-01-PLAN.md` - analogous operational pack file plan.
- `.planning/phases/49-hermes-canonical-pack/49-02-PLAN.md` - analogous route reference expansion and verification plan.
- `.planning/phases/49-hermes-canonical-pack/49-01-SUMMARY.md` - implementation summary for operational pack files.
- `.planning/phases/49-hermes-canonical-pack/49-02-SUMMARY.md` - implementation summary for route expansion and verification.
- `.planning/phases/49-hermes-canonical-pack/49-RESEARCH.md` - research summary for route-local pack patterns, current baseline notes, risks, and verification commands.

### Hermes Pack Precedent

- `skills/visual-ip-illustrations/references/ips/hermes/index.md` - closest uploaded-image route pack navigation and operational-coherence precedent.
- `skills/visual-ip-illustrations/references/ips/hermes/source.md` - source-reviewed uploaded-image source record precedent with public sample policy, review owner, and status handoff.
- `skills/visual-ip-illustrations/references/ips/hermes/style-dna.md` - uploaded-image marker preservation, article style, route isolation, and drift gates.
- `skills/visual-ip-illustrations/references/ips/hermes/hermes-ip.md` - uploaded-image identity, recognition, cognitive-action, route boundary, and failure-mode precedent.
- `skills/visual-ip-illustrations/references/ips/hermes/composition-patterns.md` - composition family, action pattern, supporting-object, and anti-repeat precedent.
- `skills/visual-ip-illustrations/references/ips/hermes/prompt-template.md` - planning fields, one-image prompt, edit repairs, route leakage repair, and unaffected-content preservation precedent.
- `skills/visual-ip-illustrations/references/ips/hermes/qa-checklist.md` - QA gates, identity checks, iteration moves, leakage repair, and delivery judgment precedent.

### Go Gopher Pack Precedent

- `skills/visual-ip-illustrations/references/ips/gopher/index.md` - source-reviewed mascot route pack navigation and operational-coherence precedent.
- `skills/visual-ip-illustrations/references/ips/gopher/source.md` - mascot source attribution, license boundary, local visual authority, public sample policy, and review owner precedent.
- `skills/visual-ip-illustrations/references/ips/gopher/style-dna.md` - mascot marker preservation, sparse article style, action-subject gate, and visual rejection pattern precedent.
- `skills/visual-ip-illustrations/references/ips/gopher/gopher-ip.md` - mascot identity, action verbs, route boundary, and failure-mode precedent.
- `skills/visual-ip-illustrations/references/ips/gopher/composition-patterns.md` - mascot composition family, supporting object pool, action pattern, and anti-repeat precedent.
- `skills/visual-ip-illustrations/references/ips/gopher/prompt-template.md` - mascot planning fields, generation prompt, source/license note, edit prompts, and delivery reminder precedent.
- `skills/visual-ip-illustrations/references/ips/gopher/qa-checklist.md` - mascot QA gates, route leakage repair, public sample boundary, and delivery judgment precedent.

### OpenClaw Pack Precedent

- `skills/visual-ip-illustrations/references/ips/openclaw/index.md` - compact source-reviewed route pack navigation and shared failure-category precedent.
- `skills/visual-ip-illustrations/references/ips/openclaw/source.md` - uploaded-logo authority, source/license context, public sample policy, and review owner precedent.
- `skills/visual-ip-illustrations/references/ips/openclaw/style-dna.md` - uploaded visual marker preservation and sparse article style precedent.
- `skills/visual-ip-illustrations/references/ips/openclaw/openclaw-ip.md` - route-local identity and active cognitive action precedent.
- `skills/visual-ip-illustrations/references/ips/openclaw/composition-patterns.md` - action pattern, supporting object pool, and anti-repeat precedent.
- `skills/visual-ip-illustrations/references/ips/openclaw/prompt-template.md` - compact edit prompt and uploaded identity repair precedent.
- `skills/visual-ip-illustrations/references/ips/openclaw/qa-checklist.md` - compact uploaded identity QA and product-poster repair precedent.

### Future Phase Boundaries

- `skills/visual-ip-illustrations/SKILL.md` - Phase 55 runtime controller integration target.
- `skills/visual-ip-illustrations/agents/openai.yaml` - Phase 56 agent metadata target.
- `README.md` - Phase 56 public documentation target.
- `examples/prompts.md` - Phase 56 public prompt examples target.
- `NOTICE.md` - Phase 56 legal/source notice target.
- `RELEASE_CHECKLIST.md` - Phase 56 release review target.
- `scripts/validate-skill-package.mjs` - Phase 57 validator target.
- `scripts/validate-skill-package.test.mjs` - Phase 57 regression test target.

### Uploaded and External Source Anchors

- `/Users/longnv/Downloads/Linux-logo.jpg` - uploaded visual authority; local metadata: JPEG, 3500x2300, SHA-256 `071bc327e4a2814864f9e2fcdea99aa50482a92ef4e816de9d9ce5f40e17bb2a`.
- `https://isc.tamu.edu/~lewing/linux/` - Larry Ewing Linux 2.0 Penguins page, Tux image permission, and The GIMP attribution condition.
- `https://www.linuxfoundation.org/legal/the-linux-mark` - Linux mark ownership attribution, Linux Foundation sublicensing context, and statement that Tux is created by Larry Ewing and outside Linux Foundation ownership.
- `https://www.linuxfoundation.org/legal/trademark-usage` - Linux Foundation trademark usage guidance for factual use, attribution, and endorsement-safe wording.

</canonical_refs>

<code_context>
## Existing Code Insights

### Reusable Assets

- `skills/visual-ip-illustrations/references/ips/linux/source.md` already records the Linux Mascot source authority, uploaded local path, SHA-256, marker list, sample policy, route status, distribution boundary, and review owner.
- `skills/visual-ip-illustrations/references/routing.md` already contains the Linux route selection rule, route table row, metadata block, output path markers, source/trademark context, route boundary, and current source-only `required_references`.
- `skills/visual-ip-illustrations/references/ips/hermes/` is the closest source-reviewed uploaded-image pack precedent because every operational file repeats route contract, uploaded visual authority, identity markers, action-subject rule, drift gates, edit repairs, and QA gates.
- `skills/visual-ip-illustrations/references/ips/gopher/` is the strongest mascot pack precedent because it combines source-reviewed route status, mascot identity, visual marker preservation, visible-label rules, action-subject gates, and public sample boundaries.
- `skills/visual-ip-illustrations/references/ips/openclaw/` is a compact uploaded-authority repair precedent for identity repair, product-poster repair, route leakage repair, and unaffected-content preservation.

### Established Patterns

- Xiaohei remains the only omitted-IP default.
- Additional IPs are explicit routes with `default=false`, route-specific aliases, route-local references, route-specific output suffixes, route-specific output directories, and route status.
- Route-local canonical packs use seven files when `source.md` is included: `index.md`, `source.md`, `style-dna.md`, `<route>-ip.md`, `composition-patterns.md`, `prompt-template.md`, and `qa-checklist.md`.
- Operational pack files repeat a compact route header so each file remains useful through progressive loading.
- `source.md` remains the authority for attribution, license or trademark context, uploaded visual authority, sample policy, review owner, distribution boundary, and route status.
- Prompt files keep image-generation instructions in English, while visible labels are copied exactly in the user's requested language.
- Public generated samples for source-reviewed, uploaded-image, local-reference, public-figure, protected, or brand-sensitive routes require release review.
- Sparse article illustration style uses 16:9 horizontal composition, white or very light background, rough hand-drawn linework, generous whitespace, one core idea, one structure family, and 2-6 short visible labels.

### Integration Points

- Phase 54 connects to `skills/visual-ip-illustrations/references/ips/linux/` by creating the operational pack around the existing `source.md`.
- Phase 54 connects to `skills/visual-ip-illustrations/references/routing.md` by expanding the Linux `required_references` cell after all pack files exist.
- Phase 55 will use the expanded route pack from `SKILL.md` for progressive reference loading, selected-IP dispatch, mixed-IP grouping, generation/edit routing, QA dispatch, save path, and delivery reporting.
- Phase 56 will expose the Linux Mascot route in README variants, `examples/prompts.md`, `NOTICE.md`, `RELEASE_CHECKLIST.md`, broad skill docs, and `agents/openai.yaml`.
- Phase 57 will add validator and Node regression coverage for Linux pack existence, route reference expansion, marker drift, trademark-boundary guardrails, public sample gates, generated sample gates, route leakage, docs consistency, and release evidence.

</code_context>

<specifics>
## Specific Ideas

- Linux Mascot should read as Tux from the uploaded image: glossy black rounded penguin head and body, white face eye patches, large oval eyes with dark pupils and small highlights, yellow-orange beak with two nostril dots, white oval belly, long black flippers, seated rounded posture, and oversized yellow-orange webbed feet.
- The positive route identity is a source-reviewed uploaded-image article-illustration route with Tux attribution, The GIMP attribution condition, Linux trademark-boundary context, and uploaded local image authority.
- Tux should perform article actions such as inspecting, sorting, bridging, carrying, marking, routing, shielding, comparing, weighing, repairing, mapping, untangling, stamping, guiding, assembling, or balancing.
- Supporting objects should be sparse physical article metaphors such as maps, bridges, knots, compasses, shelves, lamps, shields, stamps, keys, gates, scales, envelopes, source cards, license tags, review stamps, small terminals as abstract props, and small hand-built machines.
- Trademark-boundary wording should cover Linux word-mark attribution, Linux Foundation guidance, official endorsement, affiliation, sponsorship, approval, certification, compatibility, Linux Foundation logo use, distro-logo use, distro branding, and Linux Foundation campaign framing.
- Product-output boundary wording should cover product advertising, product-poster output, CLI screenshots, web hero graphics, kernel dashboard screenshots, operating-system marketing graphics, formal diagrams, dense PPT-like infographics, and clean digital typography.
- Mixed-IP requests should treat Linux Mascot as its own route group with its own route-local references and output directory.

</specifics>

<deferred>
## Deferred Ideas

- Phase 55: Linux Mascot runtime controller integration, selected-IP progressive reference loading, mixed-IP grouping, generation dispatch, edit routing, QA dispatch, save path, delivery reporting, and route-leakage guard coverage.
- Phase 56: README variants, examples, NOTICE, RELEASE_CHECKLIST, broad `SKILL.md` docs, and `agents/openai.yaml` Linux Mascot discovery wording.
- Phase 57: validator coverage, Node tests, leakage scans, trademark-boundary scans, public sample gates, generated sample gates, route smoke, uploaded-image and source-boundary smoke, docs consistency, and release evidence.
- Future requirements: public generated Linux Mascot sample gallery after release approval, machine-readable route manifests, uploaded source-image hashing automation, visual regression, public comparison sheets, release packaging, and selected-IP installation variants.

</deferred>

---

*Phase: 54-Linux Mascot Canonical Pack*
*Context gathered: 2026-07-01*
