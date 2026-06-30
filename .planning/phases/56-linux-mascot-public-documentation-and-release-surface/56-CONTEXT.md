# Phase 56: Linux Mascot Public Documentation and Release Surface - Context

**Gathered:** 2026-07-01
**Status:** Ready for planning

<domain>
## Phase Boundary

Phase 56 exposes the already-built Linux Mascot route to public and release-facing documentation. Users and maintainers should be able to learn, invoke, review, and release Linux Mascot through README variants, copyable prompt examples, NOTICE, release checklist, skill metadata parity, and runtime-facing documentation checks.

Implementation scope centers on:

- `README.md`
- `readmes/README.*.md`
- `examples/prompts.md`
- `NOTICE.md`
- `RELEASE_CHECKLIST.md`
- `skills/visual-ip-illustrations/agents/openai.yaml` parity checks
- `skills/visual-ip-illustrations/SKILL.md` parity checks
- `skills/visual-ip-illustrations/references/routing.md` and `skills/visual-ip-illustrations/references/ips/linux/` as source inputs

Out of scope:

- Changing Linux Mascot route selection, runtime dispatch, prompt behavior, QA behavior, save paths, or mixed-IP controller behavior. Phase 55 completed those surfaces.
- Expanding the Linux Mascot route-local pack. Phase 54 completed the seven-file pack.
- Adding generated Linux Mascot public sample images or gallery assets. Public samples stay behind release review.
- Extending `scripts/validate-skill-package.mjs`, Node tests, leakage fixtures, public sample gates, or final release evidence. Phase 57 owns those.

</domain>

<decisions>
## Implementation Decisions

### Public Documentation Surface

- **D-01:** Phase 56 should add Linux Mascot to the root README and all localized README variants wherever the latest route inventory already lists Hermes Agent, Go Gopher, Cai Xukun, and other explicit routes.
- **D-02:** README updates should cover route selection, route description, aliases, source pointer, output path `assets/<article-slug>-linux/`, escaped marker `assets/&lt;article-slug&gt;-linux/`, source-reviewed status, uploaded-image authority, Tux attribution, The GIMP attribution condition, Linux trademark-boundary context, public sample review boundary, route isolation, and product-output boundary.
- **D-03:** README gallery sections should keep Linux Mascot documented as pending public sample review rather than adding Linux Mascot gallery columns or generated assets.
- **D-04:** Localized README variants may follow the existing mixed-language style used for newer routes, but the deterministic Linux markers, paths, aliases, source pointer, status, and review-gate language must remain exact enough for Phase 57 validation.

### Prompt Examples

- **D-05:** `examples/prompts.md` should add Linux Mascot planning, generation, and edit examples with route-local references under `skills/visual-ip-illustrations/references/ips/linux/`.
- **D-06:** Linux prompt examples should require route status `source-reviewed`, source authority `skills/visual-ip-illustrations/references/ips/linux/source.md`, uploaded-image authority from `/Users/longnv/Downloads/Linux-logo.jpg`, Larry Ewing Tux attribution, The GIMP attribution condition, Linux trademark-boundary note, public sample review gate, route isolation, and output path `assets/<article-slug>-linux/`.
- **D-07:** Existing multi-IP prompt examples should move from nine groups to ten groups by adding Linux Mascot as its own variant group after Hermes Agent, with its own references, prompt template, QA checklist, output suffix, and output directory.
- **D-08:** Linux Mascot visible labels should continue to be copied exactly in the user's requested language; prompt and maintainer-facing prose stays English-default.

### NOTICE and Release Checklist

- **D-09:** `NOTICE.md` should add a Linux Mascot source attribution and public sample gate section that records route id `linux`, display name `Linux Mascot`, status `source-reviewed`, source authority, uploaded local image authority, Larry Ewing Tux attribution, Linux 2.0 Penguins source URL, The GIMP attribution condition, Linux Foundation trademark guidance, Linux mark ownership context, output path, escaped marker, and release-review terms.
- **D-10:** `RELEASE_CHECKLIST.md` should add Phase 57 ownership for Linux validation, route smoke coverage, attribution review, a dedicated Linux Mascot source/trademark/uploaded-image/public-sample gate, generated sample policy, and final release review.
- **D-11:** Release checklist wording must keep public generated Linux Mascot samples pending until reviewer, date, approval status, allowed directories, release channels, Tux source outcome, GIMP attribution outcome, Linux trademark outcome, uploaded-image identity outcome, route-isolation outcome, distro-logo boundary outcome, endorsement/certification boundary outcome, product-output outcome, and public-sample decision are recorded.

### Runtime and Metadata Parity

- **D-12:** `skills/visual-ip-illustrations/SKILL.md` and `skills/visual-ip-illustrations/agents/openai.yaml` already include Linux Mascot from Phase 55. Phase 56 should perform parity checks and make only narrow documentation-discovery edits if public surfaces reveal inconsistent markers.
- **D-13:** Preserve Visual IP Illustrations identity, canonical `$visual-ip-illustrations`, legacy `$ian-xiaohei-illustrations`, `allow_implicit_invocation: true`, and omitted-IP Xiaohei default behavior.
- **D-14:** Preserve existing Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, and Hermes Agent public documentation and route behavior while adding Linux Mascot.

### Linux Source and Boundary Language

- **D-15:** Linux Mascot public copy should present the route as a source-reviewed uploaded-image article-illustration route, with Tux performing the central cognitive action in sparse 16:9 article illustrations.
- **D-16:** Public copy should keep Tux source context separate from Linux word-mark guidance: Larry Ewing and The GIMP attach to Tux source context; Linux Foundation trademark guidance and Linux mark ownership context attach to Linux word-mark usage.
- **D-17:** Public and release copy should keep official endorsement, affiliation, sponsorship, approval, certification, compatibility, Linux Foundation logo use, distro-logo use, distro branding, product advertising, product-poster output, CLI screenshots, web hero graphics, kernel dashboard screenshots, and operating-system marketing graphics outside the Linux Mascot route.
- **D-18:** Public copy should preserve the uploaded marker set when marker detail is needed: glossy black rounded penguin head and body, white face eye patches, large oval eyes with dark pupils and small highlights, yellow-orange beak with two nostril dots, white oval belly, long black flippers, seated rounded posture, and oversized yellow-orange webbed feet.

### Verification Boundary

- **D-19:** Phase 56 verification should use targeted `rg` checks across README variants, prompt examples, NOTICE, release checklist, `SKILL.md`, and `openai.yaml`, plus a public sample asset absence check and `git diff --check`.
- **D-20:** Full validator and Node regression updates remain Phase 57 work, so Phase 56 should avoid treating current validator route-count drift as a documentation blocker.

### the agent's Discretion

- The planner may choose exact README paragraph placement by following the Hermes Phase 51 public-doc pattern.
- The planner may keep localized README Linux copy compact when deterministic route markers and release-gate terms remain present.
- The planner may add deterministic marker phrases that help Phase 57 validation, provided they stay Linux-scoped and public-doc appropriate.

</decisions>

<canonical_refs>
## Canonical References

**Downstream agents MUST read these before planning or implementing.**

### Phase Scope

- `.planning/ROADMAP.md` - Phase 56 goal, success criteria, Phase 55 dependency, and Phase 57 boundary.
- `.planning/REQUIREMENTS.md` - DOC-01 through DOC-05.
- `.planning/PROJECT.md` - v1.11 milestone goal, Linux Mascot constraints, uploaded-image authority, Tux attribution, Linux trademark boundary, no-build-runtime project rules, and English-default documentation policy.
- `.planning/STATE.md` - current milestone state and accumulated route compatibility decisions. Note: at context gathering time, STATE frontmatter still reported Phase 55 planned while Phase 55 roadmap and verification artifacts were complete.

### Prior Linux Phases

- `.planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md` - locked Linux route id, aliases, output suffix, output path, source record, uploaded-image authority, Tux attribution, Linux trademark boundary, public sample policy, and route compatibility decisions.
- `.planning/phases/53-linux-mascot-source-and-route-contract/53-DISCUSSION-LOG.md` - alternatives considered for the source/route contract.
- `.planning/phases/54-linux-mascot-canonical-pack/54-CONTEXT.md` - locked seven-file Linux route-local pack, prompt, edit, QA, source-preservation, sample gate, and route expansion decisions.
- `.planning/phases/54-linux-mascot-canonical-pack/54-DISCUSSION-LOG.md` - alternatives considered for the Linux canonical pack.
- `.planning/phases/55-linux-mascot-skill-controller-integration/55-CONTEXT.md` - locked runtime-controller, mixed-IP, delivery, and metadata decisions that Phase 56 must expose publicly.
- `.planning/phases/55-linux-mascot-skill-controller-integration/55-01-SUMMARY.md` - implementation evidence for Linux Mascot runtime and metadata surfaces.
- `.planning/phases/55-linux-mascot-skill-controller-integration/55-VERIFICATION.md` - verification evidence that Phase 55 passed and that public docs remain Phase 56 work.

### Public Documentation Targets

- `README.md` - root public install, route selection, workflow, examples, route descriptions, output paths, docs validation markers, and validation coverage notes.
- `readmes/README.ar.md`
- `readmes/README.de.md`
- `readmes/README.es.md`
- `readmes/README.fr.md`
- `readmes/README.ja.md`
- `readmes/README.ko.md`
- `readmes/README.pt.md`
- `readmes/README.ru.md`
- `readmes/README.tr.md`
- `readmes/README.uk.md`
- `readmes/README.zh-Hant.md`
- `readmes/README.zh.md`
- `examples/prompts.md` - copyable planning, generation, edit, mixed-IP, and route smoke examples.
- `NOTICE.md` - source attribution, legal notice, and public sample gate surface.
- `RELEASE_CHECKLIST.md` - release review, route smoke, attribution review, public sample, generated sample, docs, and evidence gates.

### Runtime and Metadata Inputs

- `skills/visual-ip-illustrations/SKILL.md` - current Linux runtime controller wording, reference loading, planning fields, generation/edit/QA dispatch, save path, delivery contract, and leakage guard.
- `skills/visual-ip-illustrations/agents/openai.yaml` - current Linux agent discovery copy and implicit invocation policy.
- `skills/visual-ip-illustrations/references/routing.md` - canonical Linux route metadata, aliases, required references, output path, source/trademark context, and route status.

### Linux Mascot Route Pack

- `skills/visual-ip-illustrations/references/ips/linux/index.md`
- `skills/visual-ip-illustrations/references/ips/linux/source.md`
- `skills/visual-ip-illustrations/references/ips/linux/style-dna.md`
- `skills/visual-ip-illustrations/references/ips/linux/linux-ip.md`
- `skills/visual-ip-illustrations/references/ips/linux/composition-patterns.md`
- `skills/visual-ip-illustrations/references/ips/linux/prompt-template.md`
- `skills/visual-ip-illustrations/references/ips/linux/qa-checklist.md`

### Public-Docs Precedent

- `.planning/phases/51-hermes-public-documentation-and-release-surface/51-CONTEXT.md` - closest public documentation and release surface precedent for a source-reviewed uploaded-image route.
- `.planning/phases/51-hermes-public-documentation-and-release-surface/51-01-SUMMARY.md` - concrete file list, markers, public sample absence policy, and verification commands for analogous docs rollout.
- `.planning/phases/46-cai-xukun-public-documentation-and-release-surface/46-CONTEXT.md` - public docs precedent for gated public sample and source-image boundary copy.
- `.planning/phases/41-go-gopher-public-documentation-and-release-surface/41-CONTEXT.md` - public docs precedent for source-reviewed mascot attribution and output path docs.

</canonical_refs>

<code_context>
## Existing Code Insights

### Reusable Assets

- `README.md` and all `readmes/README.*.md` already contain route inventory, Outputs, Visual IP Routes, Route Reference, Operational route facts, Example Gallery, copyable usage template, multi-IP guidance, Workflow, and Validation sections that should be extended for Linux Mascot.
- `examples/prompts.md` already contains canonical planning/generation/edit prompts and a multi-IP prompt for routes through Hermes Agent; Linux Mascot should be added using the Hermes/Go Gopher pattern.
- `NOTICE.md` already has route-specific attribution and sample-gate sections for Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, and Hermes Agent.
- `RELEASE_CHECKLIST.md` already has route smoke prompts, attribution review, public asset policy, generated sample policy, and final release review sections for prior routes.
- `skills/visual-ip-illustrations/SKILL.md`, `agents/openai.yaml`, `routing.md`, and `references/ips/linux/` already contain Linux route facts that public docs should mirror.

### Established Patterns

- Public docs lead with Visual IP Illustrations identity and keep `$visual-ip-illustrations` as canonical invocation while preserving `$ian-xiaohei-illustrations`.
- New explicit routes are added to public docs across README variants, prompt examples, NOTICE, release checklist, and metadata parity surfaces.
- Source-reviewed uploaded-image routes carry source pointer, uploaded-image authority, output path, escaped docs marker, public sample review boundary, route isolation, and claim-boundary wording.
- Public sample assets stay absent until release checklist approval records reviewer/date/status/allowed directories/release channels and route-specific quality outcomes.
- Localized README variants preserve deterministic route markers and paths even when prose remains partly English.

### Integration Points

- Add Linux Mascot public route copy near Hermes Agent in README route inventory and route sections.
- Add Linux Mascot output path bullets and escaped validation marker bullets.
- Add Linux Mascot canonical pack path and operational route facts.
- Add Linux Mascot to template route choices, mixed-IP groups, workflow route selection, QA/delivery notes, and validation coverage wording.
- Add Linux Mascot canonical planning, generation, edit, mixed-IP, and smoke examples to `examples/prompts.md`.
- Add Linux Mascot source and public sample gate to `NOTICE.md`.
- Add Linux Mascot Phase 57 ownership, smoke prompt, attribution review, public/generated sample policy, and final release review to `RELEASE_CHECKLIST.md`.

</code_context>

<specifics>
## Specific Ideas

- Linux Mascot public docs should say the route is explicit and source-reviewed, with aliases `Linux Mascot`, `Linux mascot`, `Linux`, `linux`, `Tux`, `tux`, `Linux penguin`, and `Tux penguin`.
- Public docs should point source-sensitive readers to `skills/visual-ip-illustrations/references/ips/linux/source.md`.
- Public docs should use `assets/<article-slug>-linux/` and `assets/&lt;article-slug&gt;-linux/` wherever output paths and docs validation markers are listed.
- Prompt examples should ask for Linux Mascot state, Linux Mascot action, Source context note, Trademark-boundary note, and Output path.
- Release checklist should include an explicit Linux Mascot smoke prompt and mixed-IP smoke expansion from nine route groups to ten route groups.
- No generated Linux Mascot images or public Linux Mascot samples should be added in Phase 56.

</specifics>

<deferred>
## Deferred Ideas

- Phase 57: validator coverage, Node tests, leakage scans, trademark-boundary scans, public sample gates, generated sample gates, route smoke, uploaded-image and source-boundary smoke, docs consistency, and release evidence.
- Future requirements: public generated Linux Mascot sample gallery after release approval, machine-readable route manifests, uploaded source-image hashing automation, visual regression, public comparison sheets, release packaging, and selected-IP installation variants.

</deferred>

---

*Phase: 56-Linux Mascot Public Documentation and Release Surface*
*Context gathered: 2026-07-01*
