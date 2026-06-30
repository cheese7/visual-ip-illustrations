# Phase 52: Hermes Validation and Release Evidence - Context

**Gathered:** 2026-06-18
**Status:** Ready for planning

<domain>
## Phase Boundary

Phase 52 turns the Hermes Agent route delivered by Phases 48-51 into deterministic local release readiness.

This phase owns `VAL-01` through `VAL-05` from `.planning/REQUIREMENTS.md`: validator drift coverage, route-leakage checks, public generated sample gates, Node regression coverage, and final release evidence. The work should extend the existing dependency-free Node validator, extend the built-in `node:test` suite, run the final command set, and create the Phase 52 release evidence artifact.

In scope:

- Extend `scripts/validate-skill-package.mjs` for Hermes route metadata, route references, source/license markers, uploaded-image markers, output paths, public docs, examples, NOTICE, release checklist, OpenAI metadata, smoke prompts, leakage scans, mythology-drift scans, public sample gates, generated sample gates, and release evidence.
- Extend `scripts/validate-skill-package.test.mjs` with Hermes parser, route-order, fixture, approval parser, sample gate, leakage, evidence, and full-pass coverage.
- Create `.planning/phases/52-hermes-validation-and-release-evidence/52-RELEASE-EVIDENCE.md` during execution after the validator and Node suite are green.
- Preserve the Phase 48 route/source contract, Phase 49 route-local pack, Phase 50 controller integration, and Phase 51 public documentation behavior.

Out of scope:

- Changing Hermes route identity, visual authority, aliases, status, output suffix, output path, or route-local pack behavior from Phases 48-50.
- Changing public docs, examples, NOTICE, release checklist, `SKILL.md`, or `agents/openai.yaml` beyond minimal validator/test-driven repair if the final verification exposes actual drift.
- Publishing public generated Hermes samples before release checklist approval is complete.
- Moving internal generated samples from `assets/<article-slug>-hermes/` into public sample directories.
- Replacing the uploaded conversation attachment as Hermes visual authority.
- Adding a package manager, build runtime, external dependency, manifest generator, UI, hosted app, API, database, or CI system.
- Changing Xiaohei omitted-IP default behavior or Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, or Cai Xukun route behavior.

</domain>

<decisions>
## Implementation Decisions

### Validator Matrix

- **D-01:** Extend `scripts/validate-skill-package.mjs`; keep the validator dependency-free and runnable through direct `node scripts/validate-skill-package.mjs`.
- **D-02:** Treat Hermes as the ninth stable route in route table, route order, route count, output path, public docs, mixed-IP, rebrand-route, compatibility, and language-scan expectations.
- **D-03:** Add Hermes-specific validator checks for agent metadata, route metadata, route-local references, source record, prompt template, identity pack, QA checklist, public docs, NOTICE, release checklist, explicit smoke prompt, mixed-IP smoke prompt, public sample gate, generated sample gate, route leakage, mythology-drift leakage, and release evidence.
- **D-04:** Keep validator output deterministic with stable ordered `defineCheck(id, message, run)` entries and exact summary output.
- **D-05:** Current baseline diagnostics are part of the Phase 52 work surface: `node scripts/validate-skill-package.mjs` currently exits 1 with `Summary: total=145 passed=137 failed=8 skipped=0`, and the failure set shows old eight-route assumptions plus missing Hermes-aware route-reference expectations.

### Route Metadata

- **D-06:** Hermes route metadata authority comes from `skills/visual-ip-illustrations/references/routing.md`.
- **D-07:** Validator and tests must lock route id `hermes`, display name `Hermes Agent`, aliases `Hermes Agent`, `Hermes`, `hermes`, `hermes-agent`, `Hermes logo`, and `Hermes Agent logo`, `default=false`, output suffix `hermes`, status `source-reviewed`, and required references under `references/ips/hermes/`.
- **D-08:** Route ordering should become `xiaohei`, `littlebox`, `tom`, `ferris`, `seal`, `openclaw`, `gopher`, `caixukun`, `hermes`.
- **D-09:** Xiaohei remains the only omitted-IP default; Hermes remains explicit.

### Source And License Markers

- **D-10:** Add Hermes source-record validation against `skills/visual-ip-illustrations/references/ips/hermes/source.md`.
- **D-11:** Source/license checks must cover official website `https://hermes-agent.nousresearch.com/`, official repository `https://github.com/NousResearch/hermes-agent`, MIT license URL `https://github.com/NousResearch/hermes-agent/blob/main/LICENSE`, docs URL `https://hermes-agent.nousresearch.com/docs/`, route status `source-reviewed`, uploaded conversation attachment authority, public sample policy, review owner, and distribution boundary.
- **D-12:** Uploaded-image marker checks must preserve the Phase 48 marker set: monochrome full-body logo-style character, black bob haircut with bright highlights, headset or earpiece, black sleeveless dress, white collar tag with an `A`-like mark, black thigh-high stockings, platform heels, and slender fashion-figure posture.

### Output Path Markers

- **D-13:** Extend output path token helpers and assertions to include raw `assets/<article-slug>-hermes/` and escaped `assets/&lt;article-slug&gt;-hermes/`.
- **D-14:** Hermes output path markers must be checked in routing metadata, `SKILL.md`, public docs, examples, OpenAI metadata, release checklist, route-local prompt/QA references, and release evidence.

### Public Docs, Examples, NOTICE, Checklist, Metadata Drift

- **D-15:** Extend docs validation so README variants, `examples/prompts.md`, `NOTICE.md`, `RELEASE_CHECKLIST.md`, `skills/visual-ip-illustrations/agents/openai.yaml`, `skills/visual-ip-illustrations/SKILL.md`, and `skills/visual-ip-illustrations/references/routing.md` all preserve Hermes Agent route facts.
- **D-16:** Docs/examples checks must preserve Hermes source-reviewed status, uploaded-image authority, official source context, MIT license context, public sample review gate, mythology-drift boundary, product-poster boundary, uploaded-character-only output, route isolation, raw output path, escaped output path, and source pointer.
- **D-17:** Maintain README variant parity using the existing `readmes/README.*.md` scan pattern from Phase 51 verification.
- **D-18:** Keep Cai Xukun and existing-route drift fixes bounded to stale validator/test assumptions that block Phase 52 green status.

### Leakage Scan

- **D-19:** Add a Hermes leakage check that scans non-Hermes route-local packs and shared legacy references for Hermes-only route markers.
- **D-20:** Hermes leakage markers should include `Hermes Agent`, `hermes-agent`, `references/ips/hermes`, `assets/<article-slug>-hermes/`, `assets/&lt;article-slug&gt;-hermes/`, `Generated image 1 (16).jpeg`, uploaded-image authority, source-reviewed Hermes Agent context, black bob haircut, headset or earpiece, black sleeveless dress, white collar tag, thigh-high stockings, platform heels, slender fashion-figure posture, mythology-drift boundary, and product-poster boundary.
- **D-21:** Public docs may list Hermes in route inventory; the leakage scan should target route-local packs and shared legacy references where Hermes identity would contaminate another route.

### Public Sample Gates

- **D-22:** Public generated Hermes samples remain blocked unless `RELEASE_CHECKLIST.md` contains complete approval data.
- **D-23:** Public sample gates should scan `examples/images/`, `examples/images-en/`, and `skills/visual-ip-illustrations/assets/examples/` for Hermes filenames or rendered Hermes sample markers.
- **D-24:** Complete public-sample approval should require reviewer, valid date, approval status, allowed directories, release channels, uploaded-image identity outcome, source/MIT outcome, mythology-drift outcome, product-poster boundary outcome, route-isolation outcome, article-metaphor quality outcome, and public-sample decision.

### Generated Sample Gates

- **D-25:** Generated sample checks must keep internal workspace outputs under `assets/<article-slug>-hermes/` distinct from public rendered sample directories.
- **D-26:** Complete generated-sample review should require reviewer, valid date, approval status, internal review directories, public directories, release channels, uploaded-image identity outcome, source/MIT outcome, mythology-drift outcome, product-poster boundary outcome, route-isolation outcome, and article-metaphor quality outcome.
- **D-27:** Existing generated sample parser patterns for Ferris, Seal, OpenClaw, Go Gopher, and Cai Xukun are the model for Hermes approval parsing.

### Node Fixtures

- **D-28:** Extend `scripts/validate-skill-package.test.mjs` using the existing built-in `node:test` suite, fixture-copy helpers, validator runner helpers, route parser assertions, stable-order assertions, approval-line builders, placeholder approval tests, public sample fixtures, generated sample fixtures, leakage fixtures, and full-pass summary assertions.
- **D-29:** Add Hermes fixture tests that prove failure for route metadata drift, required-reference drift, source/license marker drift, uploaded-image marker drift, prompt/identity/QA drift, public docs drift, README variant drift, NOTICE drift, release checklist drift, smoke drift, mixed-IP drift, release evidence drift, leakage into non-Hermes packs, public sample approval gaps, generated sample review gaps, placeholder approval dates, and full-pass output drift.
- **D-30:** Current Node baseline diagnostics are part of the Phase 52 work surface: `node --test scripts/validate-skill-package.test.mjs` currently exits 1 with `tests 105`, `pass 83`, and `fail 22`.

### Release Evidence

- **D-31:** Produce `.planning/phases/52-hermes-validation-and-release-evidence/52-RELEASE-EVIDENCE.md` during execution after validator and Node tests pass.
- **D-32:** Add a validator evidence check for the release artifact after it exists, preferably `VAL-HERMES-EVIDENCE-001`.
- **D-33:** Release evidence must record exact command outputs for validator output, Node test output, `git diff --check`, Hermes route smoke, uploaded-image smoke, source/MIT boundary smoke, docs consistency, leakage scan, mythology-drift scan, public sample gate, generated sample gate, and dirty-worktree scope.
- **D-34:** Release evidence must trace `VAL-01` through `VAL-05` and state the release verdict in the Phase 42/47 release-evidence style.

### Final Command Set

- **D-35:** Final verification command set:

```bash
node scripts/validate-skill-package.mjs
node --test scripts/validate-skill-package.test.mjs
git diff --check
```

- **D-36:** Final route smoke commands should include focused scans for Hermes route/source/output/public markers across runtime, docs, routing, examples, NOTICE, release checklist, metadata, and route-local pack files.
- **D-37:** Final boundary commands should include a public sample asset scan, internal generated sample scan, non-Hermes route-local leakage scan, mythology-drift marker scan, and dirty-worktree scope check.

### Agent Discretion

- The planner may choose exact helper names, check insertion points, and check ID numbering, provided output order remains deterministic and readable.
- The planner may add small route-expectation helper arrays for Hermes and extend existing helper arrays, provided the validator stays script-only and dependency-free.
- The planner may repair stale Cai Xukun or eight-route test assertions only where required to make the nine-route Hermes validation matrix deterministic.

</decisions>

<canonical_refs>
## Canonical References

**Downstream agents MUST read these before planning or implementing.**

### Phase Scope

- `.planning/PROJECT.md` - v1.10 Hermes milestone goal, constraints, route boundaries, source context, and no-build-runtime policy.
- `.planning/REQUIREMENTS.md` - `VAL-01` through `VAL-05`, Hermes source/pack/runtime/docs requirements, and out-of-scope boundaries.
- `.planning/ROADMAP.md` - Phase 52 goal, dependency on Phase 51, success criteria, and planned `52-01-PLAN.md` title.
- `.planning/STATE.md` - current milestone state, Phase 52 current focus, recent Hermes phase sequence, and validation handoff.

### Prior Hermes Evidence

- `.planning/phases/48-hermes-source-and-route-contract/48-CONTEXT.md` - locked Hermes route/source decisions, source authority, uploaded-image marker list, and Phase 52 validation handoff.
- `.planning/phases/49-hermes-canonical-pack/49-CONTEXT.md` - locked seven-file Hermes pack, marker set, prompt/edit/QA gates, and Phase 52 verification targets.
- `.planning/phases/50-hermes-skill-controller-integration/50-CONTEXT.md` - locked runtime controller integration, mixed-IP routing, delivery reporting, metadata scope, and Phase 52 boundary.
- `.planning/phases/51-hermes-public-documentation-and-release-surface/51-CONTEXT.md` - public docs, examples, NOTICE, checklist, metadata markers, and Phase 52 validation boundary.
- `.planning/phases/51-hermes-public-documentation-and-release-surface/51-VERIFICATION.md` - Phase 51 green evidence, public sample absence evidence, and public docs parity evidence.

### Validator And Test Surfaces

- `scripts/validate-skill-package.mjs` - dependency-free validator to extend for Hermes route, docs, source/license, uploaded-image markers, leakage, mythology drift, sample gates, generated sample gates, and release evidence.
- `scripts/validate-skill-package.test.mjs` - built-in Node regression suite to extend for Hermes parser coverage, fixtures, gate parsers, release evidence drift, sample gates, leakage, and full green output.
- `.planning/codebase/TESTING.md` - project validation model and testing conventions.
- `.planning/codebase/CONVENTIONS.md` - Markdown, path, language, and validation conventions.
- `.planning/codebase/STRUCTURE.md` - repository layout and placement guide.
- `.planning/codebase/ARCHITECTURE.md` - documentation-first skill architecture and progressive reference loading.

### Public Docs And Release Surfaces

- `README.md` - canonical public route surface and validation documentation.
- `readmes/README.*.md` - localized README variants that need deterministic Hermes marker coverage.
- `examples/prompts.md` - Hermes planning, generation, edit, route smoke, mixed-IP, and maintainer smoke examples.
- `NOTICE.md` - Hermes source attribution, MIT context, uploaded-image authority, and public sample gate notice.
- `RELEASE_CHECKLIST.md` - Hermes release review, public sample, generated sample, final release review, and automated gate command surface.
- `skills/visual-ip-illustrations/agents/openai.yaml` - OpenAI/Codex metadata discovery copy.
- `skills/visual-ip-illustrations/SKILL.md` - runtime skill controller behavior, reference loading, output contract, and delivery reporting.

### Hermes Route Pack

- `skills/visual-ip-illustrations/references/routing.md` - route metadata, aliases, required references, output paths, mixed-IP groups, and delivery fields.
- `skills/visual-ip-illustrations/references/ips/hermes/index.md` - Hermes route-local pack navigation and shared route failure categories.
- `skills/visual-ip-illustrations/references/ips/hermes/source.md` - official website, Nous Research repository, MIT license URL, docs URL, uploaded conversation attachment authority, sample policy, review owner, and route status.
- `skills/visual-ip-illustrations/references/ips/hermes/style-dna.md` - Hermes style gates, uploaded-image marker preservation, mythology-drift boundary, product-poster boundary, and route isolation.
- `skills/visual-ip-illustrations/references/ips/hermes/hermes-ip.md` - Hermes identity markers, action-subject rule, mythology boundary, product boundary, and failure modes.
- `skills/visual-ip-illustrations/references/ips/hermes/composition-patterns.md` - article-metaphor patterns, action/object pools, anti-repeat rules, mythology-drift guardrails, and leakage boundary.
- `skills/visual-ip-illustrations/references/ips/hermes/prompt-template.md` - planning fields, generation prompt, edit prompts, uploaded-image identity repair, mythology-drift repair, product-poster repair, route leakage repair, and delivery report requirements.
- `skills/visual-ip-illustrations/references/ips/hermes/qa-checklist.md` - pass/fail gates, uploaded-image identity checks, mythology-drift repair, product-poster repair, public sample boundary, and delivery judgment.

### Route Precedents

- `.planning/phases/42-go-gopher-validation-and-release-evidence/42-CONTEXT.md` - analogous validation matrix, Node coverage, public sample gates, release evidence, and compatibility decisions.
- `.planning/phases/42-go-gopher-validation-and-release-evidence/42-RELEASE-EVIDENCE.md` - final release evidence artifact shape to mirror.
- `.planning/phases/47-cai-xukun-validation-and-release-evidence/47-CONTEXT.md` - latest validation context with uploaded-image/public-sample/generated-sample/leakage decisions.
- `skills/visual-ip-illustrations/references/ips/gopher/source.md` - source-reviewed source/license marker precedent.
- `skills/visual-ip-illustrations/references/ips/openclaw/source.md` - uploaded-logo source/license and public-sample gate precedent.
- `skills/visual-ip-illustrations/references/ips/caixukun/source.md` - uploaded-image authority and gated public sample precedent.

</canonical_refs>

<code_context>
## Existing Code Insights

### Reusable Assets

- `scripts/validate-skill-package.mjs` is dependency-free Node ESM and already contains filesystem helpers, Markdown table parsing, simple YAML parsing, route row lookup, reference path resolution, README variant discovery, image asset path discovery, approval-line parsers, language scan helpers, `assertIncludes`, `assertNoMarkers`, and ordered `defineCheck` entries.
- `scripts/validate-skill-package.test.mjs` uses the built-in `node:test` runner and direct `assert` APIs. No package manager or external test framework is present.
- Existing fixture-copy helpers (`copyFixture`, `runFixtureValidator`, `replaceInFixture`, `replaceAllInFixture`) already support mutation-based validator tests.
- Existing route expectation helpers include `rebrandRouteExpectations()`, route row parsing, route reference arrays, output path token helpers, and stable route-order assertions.
- Existing public/generated sample approval parsers cover Tom, Ferris, Seal, OpenClaw, Go Gopher, and Cai Xukun, with placeholder-date and missing-field tests.

### Established Patterns

- Validator checks are stable ordered `defineCheck(id, message, run)` entries in one matrix.
- Public sample gates scan `examples/images/`, `examples/images-en/`, and `skills/visual-ip-illustrations/assets/examples/`.
- Generated sample gates distinguish internal workspace outputs under `assets/<article-slug>-<route>/` from public rendered sample directories.
- Node tests assert exact stdout summaries, exact failure check IDs, parser primitive values, and route-order stability.
- Full-pass expectations currently name the Phase 47 matrix and `Summary: total=145 passed=145 failed=0 skipped=0`; Phase 52 should update these to the Hermes matrix after new checks land.
- Current validator failure IDs include `ROUTE-REFS-001`, `REBRAND-CANON-004`, `REBRAND-ROUTE-001`, and `VAL-COMPAT-001`, all tied to eight-route assumptions after Hermes became the ninth route.

### Integration Points

- Route constants and route-count expectations must include `hermes`.
- Output path token helpers must include `assets/<article-slug>-hermes/` and `assets/&lt;article-slug&gt;-hermes/`.
- Approval parser exports should add public and generated Hermes parsers if following the existing route-specific pattern.
- Public docs checks must include all README variants, `examples/prompts.md`, `NOTICE.md`, `RELEASE_CHECKLIST.md`, `routing.md`, `SKILL.md`, and `openai.yaml`.
- Final acceptance connects to `.planning/phases/52-hermes-validation-and-release-evidence/52-RELEASE-EVIDENCE.md`, then verification/UAT later in the phase.

</code_context>

<specifics>
## Specific Ideas

- Original need: maintainers need one local, deterministic proof that Hermes Agent is releasable after source, pack, controller, and public documentation work have landed.
- Core problem: validator and Node tests currently encode the pre-Hermes eight-route baseline and lack Hermes route-specific release gates.
- Acceptance truth: Phase 52 succeeds only when validator, Node tests, diff hygiene, route smoke, uploaded-image smoke, source/MIT smoke, docs consistency, leakage scan, mythology-drift scan, public sample gate, generated sample gate, release evidence, and dirty-worktree scope evidence all pass.
- Stable check IDs are preferred where they fit the existing matrix: `AGENT-HERMES-001`, `ROUTE-HERMES-001`, `REFS-HERMES-001`, `PROMPT-HERMES-001`, `IP-HERMES-001`, `QA-HERMES-001`, `SOURCE-HERMES-001`, `DOC-HERMES-001`, `NOTICE-HERMES-001`, `SMOKE-HERMES-001`, `SMOKE-MIXED-HERMES-001`, `RELEASE-HERMES-001`, `BOUNDARY-HERMES-LEAK-001`, `BOUNDARY-HERMES-IMG-001`, `BOUNDARY-HERMES-GEN-001`, and `VAL-HERMES-EVIDENCE-001`.
- Public generated Hermes samples stay pending behind explicit release checklist approval.
- Internal generated Hermes samples under `assets/<article-slug>-hermes/` stay separate from public rendered sample release gates.
- Route isolation policy: public docs may list Hermes in route inventory, while non-Hermes route-local packs must stay free of Hermes identity, source, path, mythology, and product-poster markers.
- Evidence freshness policy: `52-RELEASE-EVIDENCE.md` must contain exact command results from the final Phase 52 change set.

## Recommended Deterministic Command Strategy

Run these before implementation to preserve baseline diagnostics if needed:

```bash
node scripts/validate-skill-package.mjs
node --test scripts/validate-skill-package.test.mjs
```

Run these after implementation and before release evidence:

```bash
node scripts/validate-skill-package.mjs
node --test scripts/validate-skill-package.test.mjs
git diff --check
```

Run targeted checks for release evidence freshness:

```bash
rg -n "Hermes Agent|hermes|hermes-agent|source-reviewed|Generated image 1 \\(16\\)\\.jpeg|assets/<article-slug>-hermes/|assets/&lt;article-slug&gt;-hermes/|skills/visual-ip-illustrations/references/ips/hermes/source.md|MIT license|mythology-drift|product-poster|public sample review" README.md readmes/README.*.md examples/prompts.md NOTICE.md RELEASE_CHECKLIST.md skills/visual-ip-illustrations/agents/openai.yaml skills/visual-ip-illustrations/SKILL.md skills/visual-ip-illustrations/references/routing.md skills/visual-ip-illustrations/references/ips/hermes/*.md
rg -n "Hermes Agent|hermes-agent|references/ips/hermes|assets/<article-slug>-hermes/|assets/&lt;article-slug&gt;-hermes/|Generated image 1 \\(16\\)\\.jpeg|black bob haircut|headset or earpiece|black sleeveless dress|white collar tag|thigh-high stockings|platform heels|winged sandals|caduceus|Greek messenger|Olympian deity|product-poster" skills/visual-ip-illustrations/references/ips/xiaohei skills/visual-ip-illustrations/references/ips/littlebox skills/visual-ip-illustrations/references/ips/tom skills/visual-ip-illustrations/references/ips/ferris skills/visual-ip-illustrations/references/ips/seal skills/visual-ip-illustrations/references/ips/openclaw skills/visual-ip-illustrations/references/ips/gopher skills/visual-ip-illustrations/references/ips/caixukun skills/visual-ip-illustrations/references/*.md
find examples/images examples/images-en skills/visual-ip-illustrations/assets/examples -type f \( -iname '*hermes*' -o -iname '*hermes-agent*' \) -print
find assets -maxdepth 2 -type f \( -path '*-hermes/*' -o -iname '*hermes*' \) -print
```

</specifics>

<deferred>
## Deferred Ideas

None - discussion stayed within Phase 52 validation and release-evidence scope.

</deferred>

---

*Phase: 52-Hermes Validation and Release Evidence*
*Context gathered: 2026-06-18*
