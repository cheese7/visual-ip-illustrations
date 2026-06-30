# Phase 57: Linux Mascot Validation and Release Evidence - Context

**Gathered:** 2026-07-01
**Status:** Ready for planning

<domain>
## Phase Boundary

Phase 57 hardens deterministic local validation for the completed Linux Mascot route and records final release evidence. Maintainers should be able to run the validator and Node regression suite and see Linux Mascot route metadata, route-local pack markers, uploaded-image authority, Tux attribution, Linux trademark-boundary markers, output paths, docs, prompt examples, public asset gates, leakage scans, route smoke, and release readiness verified locally.

In scope:

- Extend `scripts/validate-skill-package.mjs` for the tenth route, Linux Mascot check IDs, route parsing, source/pack/docs/metadata checks, public asset gates, generated sample gates, leakage checks, docs consistency, route smoke, and final evidence checks.
- Extend `scripts/validate-skill-package.test.mjs` for Linux Mascot route parsing, stable ordering, default preservation, output path markers, uploaded-image markers, Tux attribution markers, Linux trademark-boundary markers, smoke prompts, leakage fixtures, public asset gates, generated sample gates, and full-pass output.
- Add Phase 57 release evidence under `.planning/phases/57-linux-mascot-validation-and-release-evidence/`.
- Preserve `.omo/` and avoid generated Linux Mascot sample assets unless a later release-review decision explicitly approves them.

Out of scope:

- Changing Linux Mascot route selection, source authority, pack behavior, runtime controller behavior, README variants, examples, NOTICE, release checklist wording, or public route copy except for narrow fixes required by deterministic validation.
- Adding public generated Linux Mascot sample images or gallery assets.
- Changing Xiaohei default behavior or non-Linux route behavior.

</domain>

<decisions>
## Implementation Decisions

### Validator Matrix

- **D-01:** Phase 57 should update the validator from the current pre-Linux 164-check matrix to a Linux-aware matrix that passes with ten routes and includes Linux-specific check IDs.
- **D-02:** Keep the validator dependency-free Node and local-only. The repository has no package manager, build runtime, or CI harness for this phase.
- **D-03:** Add Linux Mascot to route expectations after Hermes Agent: `xiaohei`, `littlebox`, `tom`, `ferris`, `seal`, `openclaw`, `gopher`, `caixukun`, `hermes`, `linux`.
- **D-04:** Preserve Xiaohei as the only `default=true` route and require Linux Mascot to remain `default=false`, `source-reviewed`, `output_suffix=linux`, and `assets/<article-slug>-linux/`.
- **D-05:** Linux route checks must validate all seven required references in order: `index.md`, `source.md`, `style-dna.md`, `linux-ip.md`, `composition-patterns.md`, `prompt-template.md`, and `qa-checklist.md`.
- **D-06:** Update shared route/path/doc token helpers so raw and escaped Linux output markers are covered wherever existing helpers enumerate route output paths.
- **D-07:** Add Linux-specific checks for `openai.yaml`, `routing.md`, route-local references, prompt template, QA checklist, source record, public docs, NOTICE, release checklist, smoke prompts, release evidence, leakage, public assets, generated samples, and live package output boundaries.

### Linux Marker Coverage

- **D-08:** Source checks must preserve `/Users/longnv/Downloads/Linux-logo.jpg`, SHA-256 `071bc327e4a2814864f9e2fcdea99aa50482a92ef4e816de9d9ce5f40e17bb2a`, Larry Ewing, Linux 2.0 Penguins source, The GIMP attribution condition, Linux Foundation trademark guidance, Linux mark ownership context, and the Linux registered-trademark attribution pattern.
- **D-09:** Uploaded-image marker checks must preserve the full Tux marker set together: glossy black rounded penguin head and body, white face eye patches, large oval eyes with dark pupils and small highlights, yellow-orange beak with two nostril dots, white oval belly, long black flippers, seated rounded posture, and oversized yellow-orange webbed feet.
- **D-10:** Trademark-boundary checks must cover distro-logo drift, Linux Foundation logo use, official endorsement, affiliation, sponsorship, approval, certification, compatibility, Linux Foundation campaign framing, product-poster output, CLI screenshots, web hero graphics, kernel dashboard screenshots, and operating-system marketing graphics.
- **D-11:** Linux prompt and QA checks should use route-local marker phrases already present in `references/ips/linux/prompt-template.md` and `references/ips/linux/qa-checklist.md`.

### Route Parsing and Mixed-IP Smoke

- **D-12:** Route parser helper tests should expect ten route rows, Linux as the final route, and stable route ordering from Xiaohei through Linux Mascot.
- **D-13:** Existing nine-route mixed-IP smoke assertions should become ten-route assertions, while older route-specific fixtures for Cai Xukun and Hermes should be updated so their fixture markers match the current ten-route public prompt text.
- **D-14:** Existing failure fixtures that intentionally remove earlier routes should keep testing meaningful route-drift behavior after Linux is added; expected messages should match current route expectation text.

### Public Asset and Generated Sample Gates

- **D-15:** Add a Linux Mascot public asset approval parser following the route-specific parser style used by Hermes, Go Gopher, OpenClaw, Cai Xukun, Seal, Ferris, and Tom.
- **D-16:** Add a Linux Mascot generated sample approval parser scoped to the Linux Mascot release checklist section.
- **D-17:** Public asset gate must fail when any Linux/Tux rendered asset appears in `examples/images/`, `examples/images-en/`, or `skills/visual-ip-illustrations/assets/examples/` before release checklist approval is complete.
- **D-18:** Generated sample gate must distinguish internal review samples under `assets/<article-slug>-linux/` from public release into public sample directories.
- **D-19:** Gate completion should require route-specific outcomes: Tux source, GIMP attribution, Linux trademark, uploaded-image identity, distro-logo boundary, endorsement/certification boundary, product-output boundary, route-isolation, uploaded-image-only Tux article illustration, public-sample decision, and article-metaphor quality where relevant.

### Leakage and Boundary Scans

- **D-20:** Add a Linux Mascot leakage gate that scans Xiaohei, Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, and Hermes Agent route-local packs for Linux Mascot-only markers.
- **D-21:** Leakage patterns should include `Linux Mascot`, `Tux`, `Linux-logo`, `/Users/longnv/Downloads/Linux-logo.jpg`, `references/ips/linux`, `assets/<article-slug>-linux/`, `assets/&lt;article-slug&gt;-linux/`, Linux trademark-boundary phrases, distro-logo boundary phrases, and Linux Foundation logo phrases where route-local context makes them Linux-only.
- **D-22:** Keep public README and release checklist Linux mentions outside leakage scope because those files intentionally list all public routes.

### Release Evidence

- **D-23:** Create final Phase 57 evidence after implementation as `57-RELEASE-EVIDENCE.md` or the existing phase evidence pattern selected by the planner.
- **D-24:** Evidence must include exact command outputs or concise transcripts for `node scripts/validate-skill-package.mjs`, `node --test scripts/validate-skill-package.test.mjs`, `git diff --check`, Linux route smoke, uploaded-image/source-boundary smoke, docs consistency, leakage scan, trademark-boundary scan, public sample gate status, generated sample gate status, and public asset absence.
- **D-25:** Evidence should record the final validator total, Node test count, pass count, fail count, skipped count, and the final release readiness judgment.
- **D-26:** The current pre-implementation baseline is intentionally failing: validator `Summary: total=164 passed=156 failed=8 skipped=0`; Node tests `tests 117`, `pass 94`, `fail 23`, `cancelled 0`, `skipped 0`, `todo 0`. Phase 57 should close these failures.

### the agent's Discretion

- The planner may choose exact check IDs and final matrix count, provided Linux-specific checks are stable, ordered, actionable, and covered by Node tests.
- The planner may refactor repeated route expectation helpers only when it reduces real duplication and keeps existing fixture failure behavior readable.
- The planner may update release evidence check names from older milestone labels, provided existing OpenClaw, Go Gopher, Cai Xukun, Hermes, language, rebrand, and boundary evidence remains covered.

</decisions>

<canonical_refs>
## Canonical References

**Downstream agents MUST read these before planning or implementing.**

### Phase Scope

- `.planning/PROJECT.md` - v1.11 Linux Mascot constraints, route authority, uploaded-image markers, trademark boundary, no-build-runtime rule, and English-default documentation policy.
- `.planning/REQUIREMENTS.md` - VAL-01 through VAL-05 and future requirements explicitly out of this phase.
- `.planning/ROADMAP.md` - Phase 57 goal, success criteria, dependency on Phase 56, and validation/release evidence ownership.
- `.planning/STATE.md` - current milestone state, accumulated validator history, and latest route compatibility decisions.

### Prior Linux Phase Decisions

- `.planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md` - locked route, source, uploaded-image, Tux attribution, trademark-boundary, public sample, and default-route decisions.
- `.planning/phases/53-linux-mascot-source-and-route-contract/53-01-SUMMARY.md` - route/source implementation evidence.
- `.planning/phases/53-linux-mascot-source-and-route-contract/53-VERIFICATION.md` - Phase 53 verification evidence and deferred Phase 57 ownership.
- `.planning/phases/54-linux-mascot-canonical-pack/54-CONTEXT.md` - locked seven-file Linux pack, prompt, edit, QA, sample gate, and route expansion decisions.
- `.planning/phases/54-linux-mascot-canonical-pack/54-01-SUMMARY.md` - Linux pack implementation evidence.
- `.planning/phases/54-linux-mascot-canonical-pack/54-VERIFICATION.md` - Phase 54 verification evidence and current validator deferral.
- `.planning/phases/55-linux-mascot-skill-controller-integration/55-CONTEXT.md` - locked controller, mixed-IP, delivery, and metadata decisions.
- `.planning/phases/55-linux-mascot-skill-controller-integration/55-01-SUMMARY.md` - runtime/metadata implementation evidence.
- `.planning/phases/55-linux-mascot-skill-controller-integration/55-VERIFICATION.md` - Phase 55 verification evidence and current validator deferral.
- `.planning/phases/56-linux-mascot-public-documentation-and-release-surface/56-CONTEXT.md` - locked public docs, prompt examples, NOTICE, release checklist, and Phase 57 ownership decisions.
- `.planning/phases/56-linux-mascot-public-documentation-and-release-surface/56-01-SUMMARY.md` - public docs implementation evidence.
- `.planning/phases/56-linux-mascot-public-documentation-and-release-surface/56-VERIFICATION.md` - Phase 56 verification evidence and current validator/Node deferral.

### Validator and Test Targets

- `scripts/validate-skill-package.mjs` - dependency-free validator to harden for Linux Mascot route metadata, docs, pack markers, leakage, public assets, generated samples, and final evidence.
- `scripts/validate-skill-package.test.mjs` - Node regression suite to update for ten-route parser behavior, Linux fixtures, approval parsers, full-pass output, and route-specific gate failures.

### Runtime and Public Surfaces

- `skills/visual-ip-illustrations/references/routing.md` - canonical route table, Linux route row, mixed-IP route grouping, output paths, aliases, and attribution context.
- `skills/visual-ip-illustrations/SKILL.md` - runtime controller route selection, progressive loading, planning, generation, edit, QA, save, delivery, and leakage guard wording.
- `skills/visual-ip-illustrations/agents/openai.yaml` - Linux route discovery metadata and implicit invocation policy.
- `README.md` - root public docs with Linux route, output paths, public sample gate, and Phase 57 ownership.
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
- `examples/prompts.md` - Linux planning/generation/edit/smoke examples and ten-route mixed-IP prompts.
- `NOTICE.md` - Linux Mascot attribution and public sample gate.
- `RELEASE_CHECKLIST.md` - Linux Mascot source/trademark/uploaded-image gate, public asset policy, generated sample policy, and final release review.

### Linux Mascot Pack

- `skills/visual-ip-illustrations/references/ips/linux/index.md`
- `skills/visual-ip-illustrations/references/ips/linux/source.md`
- `skills/visual-ip-illustrations/references/ips/linux/style-dna.md`
- `skills/visual-ip-illustrations/references/ips/linux/linux-ip.md`
- `skills/visual-ip-illustrations/references/ips/linux/composition-patterns.md`
- `skills/visual-ip-illustrations/references/ips/linux/prompt-template.md`
- `skills/visual-ip-illustrations/references/ips/linux/qa-checklist.md`

### Evidence Precedents

- `.planning/phases/52-hermes-validation-and-release-evidence/52-CONTEXT.md` - closest validator/evidence precedent for a source-reviewed uploaded-image route.
- `.planning/phases/52-hermes-validation-and-release-evidence/52-01-SUMMARY.md` - Hermes validator hardening summary.
- `.planning/phases/52-hermes-validation-and-release-evidence/52-RELEASE-EVIDENCE.md` - Hermes final release evidence format and command set.
- `.planning/phases/47-cai-xukun-validation-and-release-evidence/47-RELEASE-EVIDENCE.md` - public-figure route validation evidence precedent.
- `.planning/phases/42-go-gopher-validation-and-release-evidence/42-RELEASE-EVIDENCE.md` - source-reviewed mascot validator evidence precedent.
- `.planning/phases/37-openclaw-validation-and-release-evidence/37-RELEASE-EVIDENCE.md` - uploaded-logo route validator evidence precedent.

</canonical_refs>

<code_context>
## Existing Code Insights

### Reusable Assets

- `scripts/validate-skill-package.mjs` already has reusable route table parsers, route reference path checks, output token helpers, public asset scans, leakage scans, approval parsers, generated sample parsers, final evidence checks, and CLI scan modes.
- `scripts/validate-skill-package.test.mjs` already has fixture-copy helpers, fixture mutation helpers, route approval line builders, full matrix assertions, parser helper assertions, public asset gate fixtures, generated sample gate fixtures, leakage fixtures, and release evidence drift tests.
- `RELEASE_CHECKLIST.md` already contains Linux Mascot public asset policy and generated sample policy lines with all required outcome slots.
- Linux route-local pack files already repeat deterministic route markers that validators can assert directly.

### Established Patterns

- Route-specific validator checks are added as explicit check IDs rather than hidden under generic catch-all checks.
- Public asset gates scan `examples/images`, `examples/images-en`, and `skills/visual-ip-illustrations/assets/examples`.
- Internal generated samples are allowed under route-specific `assets/<article-slug>-<suffix>/` paths when source/review context stays attached.
- Existing source-reviewed routes use route-local leakage checks that scan all other route packs.
- Final evidence checks live with validation checks and boundary checks, then Node tests assert stable check ordering and full summary output.

### Current Baseline Failures

- `node scripts/validate-skill-package.mjs` exits 1 with `Summary: total=164 passed=156 failed=8 skipped=0`.
- Validator failures are current-route drift from old expectations: Linux reference count expectation missing, stale nine-route route assumptions, mixed-IP prompt expectations still naming nine routes, and compatibility checks expecting exactly nine route rows.
- `timeout 90s node --test scripts/validate-skill-package.test.mjs` exits 1 with `tests 117`, `pass 94`, `fail 23`, `cancelled 0`, `skipped 0`, `todo 0`.
- Node failures include full-matrix tests depending on the failing validator, parser helper route count `10 !== 9`, stale fixture markers for nine-route mixed prompts, public approval parser fixtures for several existing routes, and generated sample parser fixtures for existing routes.

### Integration Points

- Add Linux planned references and operational reference helpers next to Hermes/Gopher/Cai Xukun helpers in `scripts/validate-skill-package.mjs`.
- Extend `rebrandRouteExpectations()`, `outputPathTokens()`, `publicDocsOutputPathTokens()`, route compatibility scans, and public docs marker checks for Linux.
- Add `parsePublicLinuxSampleApproval()` and `parseGeneratedLinuxSampleApproval()` alongside existing route-specific approval parsers.
- Add Linux check definitions near adjacent Hermes/source-reviewed route checks while keeping legacy check order stable.
- Add Linux fixture builder helpers and update `requiredCheckIds` in `scripts/validate-skill-package.test.mjs`.
- Add Phase 57 evidence file after implementation and update any validator evidence check that asserts final release evidence markers.

</code_context>

<specifics>
## Specific Ideas

- Linux Mascot final evidence should say whether the public Linux/Tux sample asset count is `0` when approval remains pending.
- Linux route smoke should parse `routing.md` and confirm `linux:Linux Mascot:false:linux:source-reviewed`, seven required references, and Linux appearing after Hermes Agent.
- Uploaded-image/source-boundary smoke should confirm `/Users/longnv/Downloads/Linux-logo.jpg`, SHA-256, Larry Ewing, The GIMP, Linux Foundation trademark URLs, ownership attribution, sample policy, and marker list.
- Trademark-boundary scan should use the Linux route pack and public release surfaces to confirm required boundary markers are present, then use non-Linux route packs to confirm Linux-only boundary language is isolated.
- Public sample gate tests should exercise both pending approval with no assets and approved approval with Linux assets, using fixture filenames that match `/linux|tux/i`.

</specifics>

<deferred>
## Deferred Ideas

- Future machine-readable route manifests and validator generation remain future requirements `MNF-01` and `MNF-02`.
- Public generated Linux Mascot gallery assets remain deferred until release checklist approval is complete.
- Uploaded source-image storage and hashing automation remain future requirements `AST-01` and visual regression/comparison sheets remain `AST-02` and `AST-03`.
- Distribution scripts for selected IP variants remain future requirements `DIST-01` and `DIST-02`.

</deferred>

---

*Phase: 57-Linux Mascot Validation and Release Evidence*
*Context gathered: 2026-07-01*
