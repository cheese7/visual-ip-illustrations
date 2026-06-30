# Phase 52: Hermes Validation and Release Evidence - Research

**Researched:** 2026-06-18
**Domain:** dependency-free Node.js validator hardening, built-in `node:test` regression coverage, release evidence
**Confidence:** HIGH

<user_constraints>
## User Constraints (from CONTEXT.md)

### Locked Decisions

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

### Deferred Ideas (OUT OF SCOPE)

None - discussion stayed within Phase 52 validation and release-evidence scope.
</user_constraints>

<phase_requirements>
## Phase Requirements

| ID | Description | Research Support |
|----|-------------|------------------|
| VAL-01 | Validator fails when Hermes route metadata, source record, required references, output paths, docs, examples, NOTICE, release checklist, or agent metadata drift from the v1.10 contract. | Add route, refs, source, prompt, identity, QA, docs, NOTICE, release, agent, smoke, and evidence checks in `scripts/validate-skill-package.mjs`. |
| VAL-02 | Validator fails when Hermes identity markers leak into Xiaohei, Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, or Cai Xukun route-local packs. | Add `BOUNDARY-HERMES-LEAK-001` over non-Hermes route-local refs plus shared legacy refs. |
| VAL-03 | Validator fails when public generated Hermes samples appear without explicit release checklist approval. | Add `parsePublicHermesSampleApproval`, `BOUNDARY-HERMES-IMG-001`, `parseGeneratedHermesSampleApproval`, and `BOUNDARY-HERMES-GEN-001`. |
| VAL-04 | Node tests cover Hermes route parsing, route ordering, default preservation, output path markers, uploaded-image markers, source/license markers, mythology-drift markers, smoke prompts, leakage fixtures, public asset gates, and full-pass output. | Extend `scripts/validate-skill-package.test.mjs` helpers, fixtures, stable order expectations, parser primitive tests, sample gate tests, and summary assertions. |
| VAL-05 | Final release evidence records validator output, Node test output, `git diff --check`, Hermes route smoke, uploaded-image and source-boundary smoke, docs consistency, leakage scan, mythology-drift scan, and public sample gate status. | Create `52-RELEASE-EVIDENCE.md` after green commands and add `VAL-HERMES-EVIDENCE-001` to enforce its markers. |
</phase_requirements>

## Summary

Phase 52 is a codebase-internal validation hardening phase, not a library-selection phase. The standard path is to extend the existing dependency-free Node ESM validator and the existing built-in `node:test` suite, then record release evidence in the same shape as Phase 42 and Phase 47. [VERIFIED: codebase grep, scripts/validate-skill-package.mjs] [VERIFIED: codebase grep, scripts/validate-skill-package.test.mjs] [VERIFIED: .planning/phases/42-go-gopher-validation-and-release-evidence/42-RELEASE-EVIDENCE.md] [VERIFIED: .planning/phases/47-cai-xukun-validation-and-release-evidence/47-RELEASE-EVIDENCE.md]

The current failure state is expected after Phase 51: Hermes is already present in route/docs/runtime surfaces, while the validator and test suite still encode an eight-route baseline and some stale Cai Xukun phrase expectations. The planner should schedule repairs first for route baseline helpers and existing stale expectations, then add Hermes-specific validator gates, then add Node fixtures, then create release evidence and add the evidence validator check. [VERIFIED: command `node scripts/validate-skill-package.mjs`] [VERIFIED: command `node --test scripts/validate-skill-package.test.mjs`] [VERIFIED: .planning/phases/52-hermes-validation-and-release-evidence/52-CONTEXT.md]

**Primary recommendation:** Use one ordered plan: baseline normalization -> Hermes validator matrix -> Node regression fixtures -> green commands -> release evidence -> `VAL-HERMES-EVIDENCE-001`.

## Project Constraints (from AGENTS.md)

| Directive | Planning Impact |
|-----------|-----------------|
| Every user-facing reply begins with `爸爸`; replies use Simplified Chinese. | Planner/executor final and progress responses must follow this, while code/comments/docs in repo remain English. |
| Code, comments, commit messages, PR copy use English. | Future source/test/release artifact content should be English. |
| Start from first principles and keep edits surgical. | Phase 52 tasks should touch only validator, validator tests, phase release evidence, and phase-owned planning artifacts unless a real drift fix is required. |
| Use GSD workflow before file-changing tools. | Execution should use planned phase workflow; this research was explicitly authorized to write only `52-RESEARCH.md`. |
| Prefer durable root-cause fixes and verifiable goals. | Plan should require reproducing current baseline, then validating each check family. |
| No build runtime. | Use direct `node` commands and `git diff --check`; avoid package manager or framework setup. |
| Do not use negation-based contrastive phrasing in user-facing replies. | Planner/executor responses should avoid contrastive negation phrasing. |

## Architectural Responsibility Map

| Capability | Primary Tier | Secondary Tier | Rationale |
|------------|--------------|----------------|-----------|
| Hermes route validation | Local validation script | Markdown/YAML skill package | `scripts/validate-skill-package.mjs` owns deterministic assertions over route metadata, references, docs, examples, NOTICE, checklist, and metadata. [VERIFIED: codebase grep] |
| Hermes regression tests | Node built-in test runner | Temporary fixture copies | `scripts/validate-skill-package.test.mjs` owns mutation fixtures and parser primitive assertions. [VERIFIED: codebase grep] |
| Public sample gate | Local validation script | Release checklist | Validator parses checklist approval records and scans public sample directories. [VERIFIED: codebase grep] |
| Generated sample distinction | Local validation script | Workspace `assets/` convention | Existing route gates distinguish internal `assets/<article-slug>-route/` outputs from public directories. [VERIFIED: codebase grep] |
| Release evidence | Phase planning artifact | Validator evidence check | `52-RELEASE-EVIDENCE.md` records exact command evidence, and `VAL-HERMES-EVIDENCE-001` should enforce it after creation. [VERIFIED: Phase 42/47 evidence] |
| Runtime skill behavior | Markdown skill controller | Route-local references | Phase 52 validates behavior already delivered in Phases 48-51; it should avoid changing route behavior unless drift is proven. [VERIFIED: 52-CONTEXT.md] |

## Standard Stack

### Core

| Library / Tool | Version | Purpose | Why Standard |
|----------------|---------|---------|--------------|
| Node.js runtime | v24.13.0 available locally | Run validator and built-in tests | Existing scripts are ESM and run directly with `node`. [VERIFIED: command `node --version`] |
| `node:test` | bundled with Node.js | Regression suite | Current test file imports `node:test` and `node:assert/strict` directly. [VERIFIED: scripts/validate-skill-package.test.mjs] |
| Node core modules | bundled with Node.js | Filesystem, path, child process, temp fixtures | Validator/test use `node:fs`, `node:path`, `node:child_process`, `node:os`; no external dependencies. [VERIFIED: codebase grep] |
| ripgrep `rg` | 15.1.0 available locally | Evidence scans and targeted release checks | Existing verification evidence uses `rg`; it is available in this environment. [VERIFIED: command `rg --version`] |
| Git | 2.50.1 Apple Git | Diff hygiene and dirty-worktree scope | Final command set includes `git diff --check`; Phase 47 evidence uses scoped dirty-worktree checks. [VERIFIED: command `git --version`] |

### Supporting

| Tool | Version | Purpose | When to Use |
|------|---------|---------|-------------|
| `find` | system tool [ASSUMED] | Public sample and internal generated sample scans | Use in release evidence for filename gates. |
| `git status --short` | Git 2.50.1 | Dirty-worktree scope baseline/evidence | Use before and after Phase 52 edits to prove owned file scope. |

### Alternatives Considered

| Instead of | Could Use | Tradeoff |
|------------|-----------|----------|
| Direct Node script | Package manager script | Adds package manifest/build shape to a no-build-runtime repo. Keep direct commands. [VERIFIED: .planning/PROJECT.md] |
| Built-in `node:test` | Jest/Vitest | Adds dependencies and config. Keep existing test runner. [VERIFIED: scripts/validate-skill-package.test.mjs] |
| Generated route manifest | Machine-readable manifest | Future `MNF-01`/`MNF-02`; out of scope for Phase 52. [VERIFIED: .planning/REQUIREMENTS.md] |

**Installation:** none.

## Package Legitimacy Audit

No external packages are required or recommended. Phase 52 should use Node core modules and existing repository scripts only. [VERIFIED: .planning/PROJECT.md] [VERIFIED: scripts/validate-skill-package.mjs]

## Current Validation Architecture and Extension Points

### Validator Structure

`scripts/validate-skill-package.mjs` is a single dependency-free ESM script. It defines repo/package constants, file/path helpers, Markdown/YAML parsers, route table readers, approval parsers, assertion helpers, route reference helper arrays, and one ordered `checks` array made of `defineCheck(id, message, run)` entries. The CLI runs all checks and prints `[PASS]`, `[FAIL]`, and `Summary: total=... passed=... failed=... skipped=...`. [VERIFIED: scripts/validate-skill-package.mjs]

### Exact Validator Extension Points

| Area | Current Hook | Hermes Planning Action |
|------|--------------|------------------------|
| Output paths | `outputPathTokens()` and `publicDocsOutputPathTokens()` | Add raw and escaped Hermes path tokens. |
| Public sample approval | `parsePublic*SampleApproval()` exports and route-specific approval line parsers | Add `parsePublicHermesSampleApproval()` and likely `parseHermesApprovalLine()`. |
| Generated sample approval | `parseGenerated*SampleApproval()` section slicing by release checklist heading | Add Hermes section slicing for `## Hermes Agent Source, MIT License, Uploaded-Image Authority, and Public Sample Gate`. |
| Package file inventory | `requiredPackageFiles()` | Include Hermes planned references if absent from dynamic route coverage. |
| Route refs | `hermesPlannedReferences()` missing today | Add planned refs and operational refs for the seven Hermes files. |
| Route contract | `rebrandRouteExpectations()` | Append Hermes as ninth route with seven references. |
| Route table checks | `ROUTE-TABLE-001`, `ROUTE-DEFAULT-001`, `ROUTE-REFS-001`, `ROUTE-PATHS-001`, `ROUTE-MIXED-001` | Add Hermes id/default/path/ref count and nine-route mixed wording. |
| Route-specific checks | `AGENT-*`, `ROUTE-*`, `REFS-*`, `PROMPT-*`, `IP-*`, `QA-*`, `SOURCE-*`, `DOC-*`, `NOTICE-*`, `SMOKE-*`, `RELEASE-*` | Add Hermes variants with uploaded-image, source/MIT, mythology, product-poster, and sample-gate markers. |
| Evidence checks | `VAL-OPENCLAW-EVIDENCE-001`, `VAL-GOPHER-EVIDENCE-001`, `VAL-CAIXUKUN-EVIDENCE-001` | Add `VAL-HERMES-EVIDENCE-001` after `52-RELEASE-EVIDENCE.md` is written. |
| Boundary checks | `BOUNDARY-*-LEAK`, `BOUNDARY-*-IMG`, `BOUNDARY-*-GEN` | Add Hermes leakage, public sample, and generated sample gates. |
| Exports | final `export { ... }` block | Export Hermes approval parsers for Node tests. |

### Test Suite Structure

`scripts/validate-skill-package.test.mjs` uses Node core only: `node:test`, `node:assert/strict`, `node:fs`, `node:path`, `node:child_process`, and `node:os`. It has a `requiredCheckIds` ordered list, `runValidator`, `copyFixture`, `runFixtureValidator`, mutation helpers, approval-line builders, parser primitive tests, route drift tests, release surface drift tests, leakage fixtures, public sample fixtures, generated sample fixtures, placeholder approval tests, and full-pass output assertions. [VERIFIED: scripts/validate-skill-package.test.mjs]

## Current Failing Baseline and Root-Cause Grouping

### Command Baseline

| Command | Exit | Observed |
|---------|------|----------|
| `node scripts/validate-skill-package.mjs` | 1 | `Summary: total=145 passed=137 failed=8 skipped=0` |
| `node --test scripts/validate-skill-package.test.mjs` | 1 | `tests 105`, `pass 83`, `fail 22` |

### Validator Failures

| Failure ID | Root Cause Group | Planning Note |
|------------|------------------|---------------|
| `AGENT-CAIXUKUN-001` | Stale Cai Xukun metadata expectation | Existing test/validator expectation requires older public-figure marker set in `openai.yaml`; fix only if needed to unblock nine-route baseline. |
| `ROUTE-REFS-001` | Missing Hermes route reference expectation | Add `hermes: 7`, `references/ips/hermes/` resolution rules, and Hermes file existence. |
| `DOC-CAIXUKUN-001` | Stale mixed-IP phrase expectation after Hermes wording | Update Cai Xukun docs check to tolerate/expect nine-route wording. |
| `SMOKE-MIXED-GOPHER-001` | Stale mixed-IP phrase expectation | Update Go Gopher mixed smoke expectation from eight-route adjacency to nine-route Hermes wording. |
| `SMOKE-MIXED-CAIXUKUN-001` | Stale mixed-IP phrase expectation | Update from “eight separate variant groups” to nine-route Hermes wording. |
| `REBRAND-CANON-004` | Eight-route route table baseline | Update `rebrandRouteExpectations()` to include Hermes. |
| `REBRAND-ROUTE-001` | Eight-route route table baseline | Same as above. |
| `VAL-COMPAT-001` | Compatibility helper delegates to eight-route baseline | Update compatibility helper after route expectation update. |

### Node Test Failures

The 22 failing Node tests group into these workstreams:

| Group | Examples | Root Cause |
|-------|----------|------------|
| Green-run expectations blocked by validator failure | Harness smoke, stable order tests, full matrix test, language enforce fixture, public/generated sample “approved” fixture runs | Fixture validators inherit current global validator failures, so expected `status 0` fails. |
| Route-count/order primitives | `parser helpers expose current package contract primitives` | Parser test expects 8 routes; live table has 9. |
| Fixture marker drift | Cai Xukun release surface drift, Go Gopher/Cai Xukun mixed markers, Seal route metadata regex | Tests look for old phrase strings or old observed route-list text. |
| Full-pass summary drift | Multiple assertions still expect `Summary: total=145 passed=145 failed=0 skipped=0` | New Hermes checks will change totals; update after final matrix lands. |
| Sample parser fixture green assertions | Tom/Ferris/Seal/OpenClaw/Go Gopher/Cai Xukun public and generated sample tests | These become green after the base validator passes and summary totals are updated. |

## Recommended Hermes Validator Check Matrix

Add Hermes checks in the existing ordered route-family positions. Exact count depends on whether helpers consolidate checks, but the matrix should cover every requirement below.

| Suggested ID | Capability | Required Markers / Behavior |
|--------------|------------|-----------------------------|
| `AGENT-HERMES-001` | Agent metadata | `Hermes Agent`, aliases, `source-reviewed`, source pointer, raw/escaped path, uploaded-image authority, MIT/source context, mythology/product-poster/public sample boundaries. |
| `ROUTE-HERMES-001` | Route table | id `hermes`, display `Hermes Agent`, aliases, `default=false`, `output_suffix=hermes`, status `source-reviewed`, official source/license/docs URLs, uploaded attachment, sample gate. |
| `REFS-HERMES-001` | Seven-file pack | `index.md`, `source.md`, `style-dna.md`, `hermes-ip.md`, `composition-patterns.md`, `prompt-template.md`, `qa-checklist.md` exist and share route/path/source markers. |
| `PROMPT-HERMES-001` | Prompt template | Planning fields, generation prompt, edit prompts, uploaded-image repair, mythology-drift repair, product-poster repair, output path, delivery report. |
| `IP-HERMES-001` | Identity pack | Black bob haircut, bright highlights, headset/earpiece, black sleeveless dress, white collar tag with `A`-like mark, thigh-high stockings, platform heels, slender posture, action-subject rule. |
| `QA-HERMES-001` | QA checklist | Reject generic anime assistant, mythological Hermes, missing identity markers, product-poster drift, passive placement, route leakage, excessive text, copied composition. |
| `SOURCE-HERMES-001` | Source record | Official website, GitHub repo, MIT license URL, docs URL, uploaded conversation attachment, sample policy, route status, allowed/restricted use, distribution boundary, review owner. |
| `DOC-HERMES-001` | Public docs | All README variants, examples, release checklist, routing, metadata, source/MIT, raw/escaped path, uploaded-image authority, mythology/product-poster boundaries. |
| `NOTICE-HERMES-001` | NOTICE | Hermes source attribution, MIT context, uploaded-image authority, public sample gate, boundary wording. |
| `SMOKE-HERMES-001` | Explicit route smoke | `examples/prompts.md` route smoke for Hermes planning/generation/edit/source/MIT/uploaded-image/path/sample gate. |
| `SMOKE-MIXED-HERMES-001` | Mixed-IP smoke | Nine variant groups and Hermes route-local group with own refs, QA, output path, source note, mythology/product-poster notes. |
| `RELEASE-HERMES-001` | Release checklist | Source/MIT review, uploaded-image/boundary review, leakage scan, public asset policy, generated sample policy, final review. |
| `VAL-HERMES-EVIDENCE-001` | Release evidence | `52-RELEASE-EVIDENCE.md` exact command summaries, route smoke, uploaded-image/source/MIT docs, leakage, mythology, sample gates, dirty scope, VAL traceability. |
| `BOUNDARY-HERMES-LEAK-001` | Route leakage | Scan non-Hermes packs and legacy refs for Hermes-only identity/source/path/mythology/product-poster markers. |
| `BOUNDARY-HERMES-IMG-001` | Public sample gate | Fail if public sample dirs contain Hermes assets without complete approval record. |
| `BOUNDARY-HERMES-GEN-001` | Generated sample distinction | Enforce `assets/<article-slug>-hermes/` internal review distinction and checklist review fields. |

## Node Test and Fixture Recommendations

Update these test surfaces in order:

1. Extend `requiredCheckIds` with the final Hermes check IDs in exact validator order.
2. Update green-run tests to expect the new final summary count after the check matrix lands.
3. Update parser primitive tests to expect 9 routes and route order `xiaohei`, `littlebox`, `tom`, `ferris`, `seal`, `openclaw`, `gopher`, `caixukun`, `hermes`.
4. Add approval-line builders: `pendingHermesPublicAssetApprovalLine`, `completeHermesPublicAssetApprovalLine`, `pendingGeneratedHermesSampleLine`, `completeGeneratedHermesSampleLine`.
5. Add parser tests for `parsePublicHermesSampleApproval` and `parseGeneratedHermesSampleApproval`, including placeholder date and missing outcome fields.
6. Add route metadata drift fixture by mutating the Hermes row in `routing.md`.
7. Add required-reference drift fixture by removing or renaming a Hermes required reference.
8. Add source marker drift fixture against `references/ips/hermes/source.md`.
9. Add pack/prompt/QA/identity drift fixtures against `references/ips/hermes/*.md`.
10. Add release surface drift fixture across README variant, `examples/prompts.md`, `NOTICE.md`, `RELEASE_CHECKLIST.md`, `openai.yaml`, and `SKILL.md` only where markers are required.
11. Add leakage fixtures that append Hermes markers into each non-Hermes route-local pack family.
12. Add public asset fixture by writing `examples/images/99-hermes-test.png` under pending approval, then proving a complete approval line passes.
13. Add generated sample fixture by writing `assets/article-hermes/99-hermes-test.png` and proving it does not trip the public sample gate.
14. Add release evidence drift fixture once `52-RELEASE-EVIDENCE.md` exists.

## Public Sample / Generated Sample Parser Strategy for Hermes

Hermes should follow the Cai Xukun/OpenClaw style parser because it has route-specific outcome fields beyond simple reviewer/date/allowed directories. The public approval parser should find:

```text
Hermes Agent public asset policy for `examples/images/`, `examples/images-en/`, and `skills/visual-ip-illustrations/assets/examples/`
```

The generated approval parser should slice the release checklist section:

```text
## Hermes Agent Source, MIT License, Uploaded-Image Authority, and Public Sample Gate
```

and find:

```text
Record generated sample review:
```

Recommended public fields:

```text
status / reviewer / date / approval status / allowed directories / release channels / official source outcome / MIT license outcome / uploaded-image identity outcome / mythology-drift outcome / product-poster boundary outcome / route-isolation outcome / uploaded-character-only article illustration outcome / public-sample decision
```

Recommended generated fields:

```text
status / reviewer / date / approval status / internal review directories / public directories / release channels / official source outcome / MIT license outcome / uploaded-image identity outcome / mythology-drift outcome / product-poster boundary outcome / route-isolation outcome / endorsement, affiliation, sponsorship, approval, impersonation review outcome / article-metaphor quality outcome
```

The planner should require tests for placeholder dates (`TBD`, `pending`, blank), placeholder outcome labels, incomplete directory fields, incomplete release channels, and public Hermes file names under pending approval.

## Release Evidence Artifact Strategy

Mirror Phase 47, with Hermes-specific sections:

| Section | Required Content |
|---------|------------------|
| Frontmatter | `phase: 52`, `status: pass`, creation timestamp, requirements `VAL-01` to `VAL-05`. |
| Verdict | PASS statement naming ninth route, uploaded-image authority, source/MIT, mythology/product-poster boundaries, sample gates, release evidence, dirty scope. |
| Command Evidence | Exact outputs for validator, Node tests, scoped `git diff --check`, README/docs marker loop, sample asset scan, VAL traceability scan, boundary/evidence grep, dirty scope check. |
| Hermes Route Smoke | `SMOKE-HERMES-001` and `SMOKE-MIXED-HERMES-001` details. |
| Uploaded-Image Smoke | `SOURCE-HERMES-001`, `REFS-HERMES-001`, `PROMPT-HERMES-001`, `IP-HERMES-001`, `QA-HERMES-001`. |
| Source/MIT Boundary Smoke | Official website, repository, MIT URL, docs URL, route status, distribution/review owner. |
| Mythology/Product-Poster Scan | Evidence that default route excludes Greek messenger symbols and product-poster/advertising framing. |
| Docs Consistency | README variants, examples, NOTICE, checklist, routing, `SKILL.md`, `openai.yaml`. |
| Leakage Scan | `BOUNDARY-HERMES-LEAK-001` result and scan target description. |
| Public Sample Gate | Public directories scanned, approval pending by design, no public assets present. |
| Generated Sample Gate | Internal `assets/<article-slug>-hermes/` distinction and checklist fields. |
| Dirty-Worktree Scope | Baseline and final comparison allowing only Phase 52-owned files. |
| Requirement Traceability | Map VAL-01 through VAL-05 to check IDs and evidence. |

Use the scoped diff hygiene command from Phase 47 style:

```bash
git diff --check -- scripts/validate-skill-package.mjs scripts/validate-skill-package.test.mjs .planning/phases/52-hermes-validation-and-release-evidence/52-*.md
```

## Architecture Patterns

### System Architecture Diagram

```text
Markdown/YAML source surfaces
  -> validator file readers and parsers
  -> ordered defineCheck matrix
  -> PASS/FAIL summary
  -> node:test fixture mutations
  -> final release evidence artifact
  -> VAL-HERMES-EVIDENCE-001 enforces evidence freshness
```

### Recommended Project Structure

```text
scripts/
├── validate-skill-package.mjs       # validator checks and exported parsers
└── validate-skill-package.test.mjs  # node:test regression fixtures

.planning/phases/52-hermes-validation-and-release-evidence/
├── 52-RESEARCH.md                   # this research artifact
├── 52-01-PLAN.md                    # future planner output
└── 52-RELEASE-EVIDENCE.md           # future execution output after green commands
```

### Pattern 1: Ordered Check Registration

**What:** Add stable `defineCheck(id, message, run)` entries near adjacent route families.
**When to use:** Every new Hermes validation capability.
**Example:**

```javascript
defineCheck("SOURCE-HERMES-001", "Hermes Agent source record preserves source, MIT, uploaded-image, and sample gate markers", () => {
  const relativePath = path.join(REFERENCES_DIR, "ips", "hermes", "source.md");
  assertIncludes(requireFile(relativePath), relativePath, [
    "https://hermes-agent.nousresearch.com/",
    "https://github.com/NousResearch/hermes-agent",
    "https://github.com/NousResearch/hermes-agent/blob/main/LICENSE",
    "Generated image 1 (16).jpeg",
    "assets/<article-slug>-hermes/",
  ], "Hermes source, MIT, uploaded-image authority, output path, and sample gate");
});
```

### Pattern 2: Fixture Mutation

**What:** Copy the repo to a temp fixture, mutate one marker, run validator, assert specific check failure.
**When to use:** Every Hermes drift behavior in Node tests.
**Example:**

```javascript
const fixtureRoot = copyFixture("hermes-source-drift");
try {
  replaceInFixture(
    fixtureRoot,
    path.join("skills", "visual-ip-illustrations", "references", "ips", "hermes", "source.md"),
    "https://hermes-agent.nousresearch.com/",
    "https://example.invalid/",
  );
  const result = runFixtureValidator(fixtureRoot);
  assert.equal(result.status, 1);
  assert.match(result.stdout, /\[FAIL\] SOURCE-HERMES-001 /);
} finally {
  rmSync(fixtureRoot, { recursive: true, force: true });
}
```

### Anti-Patterns to Avoid

- **Manifest generator creep:** Future requirements reserve generated manifests; Phase 52 should use helper arrays.
- **Broad docs rewrites:** Phase 51 already passed docs verification; use surgical drift repairs only.
- **Sample approval shortcuts:** Pending checklist lines should remain incomplete and block public sample files.
- **Evidence before green commands:** `52-RELEASE-EVIDENCE.md` should be written after final validator/test/diff commands pass, then enforced.
- **Route leakage over-scan:** Public docs can list Hermes; leakage scan should target route-local packs and shared legacy references.

## Don't Hand-Roll

| Problem | Don't Build | Use Instead | Why |
|---------|-------------|-------------|-----|
| Test runner | Custom test harness | built-in `node:test` | Existing suite uses it and avoids dependencies. |
| Markdown parsing | New parser dependency | Existing `parseMarkdownTable`, `bodyAfterHeading`, `parseMarkdownLinks` helpers | Keeps validator dependency-free. |
| YAML parsing | YAML package | Existing simple YAML parser | `openai.yaml` shape is simple and already covered. |
| Sample approval parsing | Ad hoc one-off regex per assertion | Route-specific parser function plus fixture tests | Existing pattern exposes parser primitives to tests. |
| Release proof | Prose-only claim | Exact command blocks plus validator evidence check | Phase 42/47 precedent makes evidence auditable. |

**Key insight:** The risky part is not implementing complex algorithms; it is keeping many duplicated prose surfaces synchronized through deterministic checks.

## Common Pitfalls

### Pitfall 1: Updating Hermes Checks Before Route Baseline Helpers

**What goes wrong:** New Hermes checks fail behind existing route-count failures.
**Why it happens:** `rebrandRouteExpectations()`, `ROUTE-REFS-001`, and parser primitive tests still expect 8 routes.
**How to avoid:** Normalize nine-route helpers first.
**Warning signs:** `expected exactly 8 rebrand route rows; observed 9`.

### Pitfall 2: Public Sample Parser Accepts Placeholders

**What goes wrong:** Public Hermes sample files pass with `PENDING / reviewer / date`.
**Why it happens:** Parser only checks line existence.
**How to avoid:** Require checked box, approved/complete/granted status, valid ISO date, real reviewer, all directories, channels, and all outcome fields.
**Warning signs:** A fixture with `99-hermes-test.png` under `examples/images/` passes while approval is pending.

### Pitfall 3: Existing Route Fixture Failures Hide Hermes Failures

**What goes wrong:** Approved sample fixture tests for other routes stay red because base validator remains red.
**Why it happens:** The fixture copies inherit global validator failures.
**How to avoid:** Repair stale route/mixed phrase expectations before adding broad fixture assertions.
**Warning signs:** Tom/Ferris/Seal/OpenClaw/Gopher/Cai Xukun sample tests fail on `status 1` after approval line is complete.

### Pitfall 4: Leakage Scan Targets Public Docs

**What goes wrong:** Validator fails because README legitimately lists Hermes.
**Why it happens:** Leakage scan uses all docs instead of route-local packs.
**How to avoid:** Scan `references/ips/xiaohei`, `littlebox`, `tom`, `ferris`, `seal`, `openclaw`, `gopher`, `caixukun`, and shared legacy refs.
**Warning signs:** `README.md` or `examples/prompts.md` appear in leakage failure output.

### Pitfall 5: Evidence Goes Stale After Adding Evidence Check

**What goes wrong:** `VAL-HERMES-EVIDENCE-001` expects old summary totals.
**Why it happens:** Evidence file written before final check matrix stabilizes.
**How to avoid:** Stabilize validator/test totals, run final commands, write evidence, add or update evidence check, rerun final commands.
**Warning signs:** Evidence check fails on missing summary or old test count.

## Code Examples

### Approval Parser Shape

```javascript
export function parsePublicHermesSampleApproval(releaseChecklistText) {
  const approvalLine = releaseChecklistText
    .split("\n")
    .map((line) => line.trim())
    .find((line) => line.includes("Hermes Agent public asset policy for"));

  return parseHermesApprovalLine(approvalLine, "public");
}
```

### Public Asset Gate Shape

```javascript
defineCheck("BOUNDARY-HERMES-IMG-001", "example asset directories keep Hermes Agent rendered assets behind release approval", () => {
  const releaseChecklist = requireFile("RELEASE_CHECKLIST.md");
  const approval = parsePublicHermesSampleApproval(releaseChecklist);
  if (!approval.found) {
    throw new Error("RELEASE_CHECKLIST.md expected Hermes Agent public asset policy approval record; observed missing line");
  }
  const matches = imageAssetPaths().filter((relativePath) => /hermes|hermes-agent/i.test(relativePath));
  if (!approval.complete && matches.length > 0) {
    throw new Error(`examples/images, examples/images-en, and ${PACKAGE_DIR}/assets/examples expected no rendered Hermes Agent assets until public-sample approval is complete; observed ${matches.join(", ")}`);
  }
});
```

## State of the Art

| Old Approach | Current Approach | When Changed | Impact |
|--------------|------------------|--------------|--------|
| Manual QA only | Dependency-free Node validator plus `node:test` fixtures | Multi-IP milestones through Phase 47 | Phase 52 should extend validator/test parity. |
| Route docs hardcoded to one README | `readmeVariantFiles()` discovers `README.md` plus `readmes/README.*.md` | OpenClaw/README migration work | Hermes docs checks should scan variants. |
| Simple public sample approval | Route-specific approval parsers with outcome fields | OpenClaw/Gopher/Cai Xukun validators | Hermes needs source/MIT/uploaded-image/mythology/product-poster outcomes. |
| Seven/eight route baselines | Nine-route Hermes baseline | Phase 52 target | Route order and summary counts must update. |

**Deprecated/outdated:**
- Eight-route route count in `rebrandRouteExpectations()` and parser primitive tests.
- Mixed-IP wording that names only eight variant groups.
- Full-pass summary `Summary: total=145 passed=145 failed=0 skipped=0` after Hermes checks land.

## Runtime State Inventory

This is not a rename/refactor/migration phase. Runtime state inventory is skipped. [VERIFIED: .planning/ROADMAP.md]

## Environment Availability

| Dependency | Required By | Available | Version | Fallback |
|------------|-------------|-----------|---------|----------|
| Node.js | Validator and `node:test` | yes | v24.13.0 | none needed |
| Git | diff hygiene and scope checks | yes | 2.50.1 Apple Git | none needed |
| ripgrep | targeted evidence scans | yes | 15.1.0 | `grep`/`find` if needed |

**Missing dependencies with no fallback:** none.

**Missing dependencies with fallback:** none.

## Validation Architecture

Skipped because `.planning/config.json` has `workflow.nyquist_validation` explicitly set to `false`. [VERIFIED: .planning/config.json]

## Security Domain

Security enforcement is enabled in `.planning/config.json`; Phase 52 is local validation tooling and Markdown/YAML release evidence with no API, browser session, database, credentials, authentication, or networked runtime. [VERIFIED: .planning/config.json] [VERIFIED: .planning/PROJECT.md]

### Applicable ASVS Categories

| ASVS Category | Applies | Standard Control |
|---------------|---------|------------------|
| V2 Authentication | no | No auth surface in scope. |
| V3 Session Management | no | No session surface in scope. |
| V4 Access Control | no | Local repo files only. |
| V5 Input Validation | yes | Validate static Markdown/YAML marker content through deterministic assertions and safe path helpers. |
| V6 Cryptography | no | No crypto surface in scope. |

### Known Threat Patterns for This Stack

| Pattern | STRIDE | Standard Mitigation |
|---------|--------|---------------------|
| Path traversal in reference paths | Tampering | Existing `safeReferencePath()` and `safePackagePath()` should remain in use. |
| False release approval from placeholder text | Spoofing | Approval parsers require checked status, real reviewer/date, directories, channels, and outcome fields. |
| Public asset publication without approval | Information Disclosure / Repudiation | Public asset directory scan plus release checklist parser. |

## Planning Risks and Ordering Recommendations

Recommended ordering:

1. Capture dirty scope baseline and rerun current validator/test failures.
2. Normalize route baseline helpers to nine routes and repair stale Cai Xukun/Go Gopher mixed wording expectations.
3. Add Hermes route helper arrays and output path tokens.
4. Add Hermes validator checks from metadata/source/pack/docs through smoke/release.
5. Add Hermes boundary checks and approval parsers.
6. Extend Node `requiredCheckIds`, parser primitives, fixture builders, drift tests, leakage tests, public sample tests, generated sample tests, and summary assertions.
7. Run validator and Node tests until green.
8. Write `52-RELEASE-EVIDENCE.md` from exact final outputs.
9. Add or finalize `VAL-HERMES-EVIDENCE-001`, rerun validator, Node tests, and `git diff --check`.

Planning risks:

- Summary totals are unknown until final check matrix stabilizes.
- Existing failing fixture tests can mask Hermes-specific fixture failures.
- Release evidence check must be last or near-last.
- Dirty worktree may contain previous phase artifacts; execution should stage/touch only Phase 52-owned files plus minimal drift fixes.

## Concrete File Ownership for Future Plan

| File | Owner Task | Allowed Change |
|------|------------|----------------|
| `scripts/validate-skill-package.mjs` | Validator matrix task | Add Hermes helpers/checks/parsers/exports and minimal stale route expectation repairs. |
| `scripts/validate-skill-package.test.mjs` | Node regression task | Add Hermes check IDs, helpers, fixtures, parser tests, and update final totals/order. |
| `.planning/phases/52-hermes-validation-and-release-evidence/52-RELEASE-EVIDENCE.md` | Evidence task | Create after green validator/test/diff commands. |
| `.planning/phases/52-hermes-validation-and-release-evidence/52-01-PLAN.md` | Planner output | Future plan artifact. |
| README variants / examples / NOTICE / checklist / `SKILL.md` / `openai.yaml` / Hermes refs | Drift repair only | Touch only if final validation proves actual marker drift that cannot be fixed in stale validator/test expectations. |

## Assumptions Log

| # | Claim | Section | Risk if Wrong |
|---|-------|---------|---------------|
| A1 | System `find` is available. | Environment Availability | Release evidence scan command may need a shell alternative. |

## Open Questions (RESOLVED)

1. **Final validator total**
   - What we know: current matrix has 145 checks and fails 8; Hermes will add multiple checks.
   - Resolution: final validator and Node test totals are implementation-derived. The executor updates summary assertions and release evidence only after the Hermes matrix, Node fixtures, and evidence check stabilize.
2. **Cai Xukun metadata drift**
   - What we know: `AGENT-CAIXUKUN-001` is currently red.
   - Resolution: Cai Xukun metadata and docs drift handling is bounded stale-expectation repair aligned with Phase 47 and Phase 51 intent unless validator or Node fixture evidence proves source drift. Public surface edits stay limited to proven source drift.

## Sources

### Primary (HIGH confidence)

- `.planning/phases/52-hermes-validation-and-release-evidence/52-CONTEXT.md` - locked Phase 52 scope and decisions.
- `.planning/REQUIREMENTS.md` - VAL-01 through VAL-05.
- `.planning/ROADMAP.md` - Phase 52 goal and success criteria.
- `.planning/PROJECT.md` - no-build-runtime and Hermes constraints.
- `.planning/STATE.md` - current phase focus and milestone state.
- `scripts/validate-skill-package.mjs` - current validator architecture and extension points.
- `scripts/validate-skill-package.test.mjs` - current Node test architecture and fixture patterns.
- `.planning/phases/42-go-gopher-validation-and-release-evidence/42-CONTEXT.md` - analogous final validation context.
- `.planning/phases/42-go-gopher-validation-and-release-evidence/42-RELEASE-EVIDENCE.md` - release evidence artifact precedent.
- `.planning/phases/47-cai-xukun-validation-and-release-evidence/47-CONTEXT.md` - latest uploaded-image route validation context.
- `.planning/phases/47-cai-xukun-validation-and-release-evidence/47-RELEASE-EVIDENCE.md` - latest release evidence precedent.
- `.planning/phases/51-hermes-public-documentation-and-release-surface/51-VERIFICATION.md` - Phase 51 docs and sample absence evidence.
- `.planning/codebase/TESTING.md` and `.planning/codebase/CONVENTIONS.md` - project testing and documentation conventions.

### Secondary (MEDIUM confidence)

- Local command outputs from `node scripts/validate-skill-package.mjs`, `node --test scripts/validate-skill-package.test.mjs`, `node --version`, `git --version`, and `rg --version`.

### Tertiary (LOW confidence)

- None.

## Metadata

**Confidence breakdown:**
- Standard stack: HIGH - direct project scripts and local command versions verified.
- Architecture: HIGH - validator and test extension points inspected directly.
- Pitfalls: HIGH - based on current failing command output and Phase 42/47 precedents.

**Research date:** 2026-06-18
**Valid until:** 2026-07-18 for this phase unless validator/test files change first.

## RESEARCH COMPLETE
