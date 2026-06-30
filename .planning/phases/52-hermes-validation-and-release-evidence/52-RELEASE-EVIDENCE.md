---
phase: 52
status: pass
created: 2026-06-18T13:51:16Z
requirements:
  - VAL-01
  - VAL-02
  - VAL-03
  - VAL-04
  - VAL-05
---

# Phase 52 Release Evidence: Hermes Validation

## Verdict

PASS.

Hermes Agent validation now covers the ninth route metadata, source-reviewed MIT source boundary, uploaded-image authority, mythology-drift boundary, product-poster boundary, route-local seven-file pack, public docs, prompt smoke fixtures, nine-route mixed-IP behavior, route leakage, public sample gates, generated-sample internal review distinction, release evidence, and dirty-worktree scope.

## Command Evidence

```bash
node scripts/validate-skill-package.mjs
# Summary: total=161 passed=161 failed=0 skipped=0
```

```bash
node --test scripts/validate-skill-package.test.mjs
# tests 114
# pass 114
# fail 0
```

```bash
git diff --check
# passed
```

```bash
node scripts/validate-skill-package.mjs | rg 'AGENT-HERMES-001|ROUTE-HERMES-001|REFS-HERMES-001|PROMPT-HERMES-001|IP-HERMES-001|QA-HERMES-001|SOURCE-HERMES-001|DOC-HERMES-001|NOTICE-HERMES-001|SMOKE-HERMES-001|SMOKE-MIXED-HERMES-001|RELEASE-HERMES-001|VAL-HERMES-EVIDENCE-001|BOUNDARY-HERMES-(LEAK|IMG|GEN)-001|Summary:'
# [PASS] AGENT-HERMES-001 openai.yaml exposes Hermes Agent source-reviewed route metadata markers
# [PASS] ROUTE-HERMES-001 routing.md preserves the Hermes Agent source-reviewed route contract
# [PASS] REFS-HERMES-001 Hermes Agent canonical route references and shared markers exist
# [PASS] PROMPT-HERMES-001 Hermes Agent prompt template preserves planning, generation, edit, and source-boundary markers
# [PASS] IP-HERMES-001 Hermes Agent canonical pack preserves uploaded-image identity and action gates
# [PASS] QA-HERMES-001 Hermes Agent QA checklist preserves source-reviewed pass, fail, repair, and delivery markers
# [PASS] SOURCE-HERMES-001 Hermes Agent source record preserves source, MIT, uploaded-image, and sample gate markers
# [PASS] DOC-HERMES-001 public docs expose Hermes Agent source-reviewed route and source-boundary markers
# [PASS] NOTICE-HERMES-001 NOTICE keeps Hermes Agent source and public sample gate markers
# [PASS] SMOKE-HERMES-001 examples prompts cover explicit Hermes Agent route smoke path
# [PASS] SMOKE-MIXED-HERMES-001 examples prompts cover nine-route mixed-IP Hermes Agent variant behavior
# [PASS] RELEASE-HERMES-001 release checklist keeps Hermes Agent source, MIT, uploaded-image, and public sample gates
# [PASS] VAL-HERMES-EVIDENCE-001 Phase 52 records Hermes Agent validation and release evidence
# [PASS] BOUNDARY-HERMES-LEAK-001 non-Hermes route references keep Hermes Agent source-reviewed markers isolated
# [PASS] BOUNDARY-HERMES-IMG-001 example asset directories keep Hermes Agent rendered assets behind release approval
# [PASS] BOUNDARY-HERMES-GEN-001 Hermes Agent generated samples stay distinct from public rendered sample release gates
# Summary: total=161 passed=161 failed=0 skipped=0
```

```bash
rg -n 'Hermes Agent is an explicit|Hermes Agent route usage|Hermes Agent: route id|Hermes Agent public docs keep|Hermes Agent public asset policy|Record generated sample review|\| `hermes` \|' README.md examples/prompts.md NOTICE.md RELEASE_CHECKLIST.md skills/visual-ip-illustrations/references/routing.md skills/visual-ip-illustrations/references/ips/hermes/source.md
# skills/visual-ip-illustrations/references/routing.md:37 matched Hermes explicit route status, MIT context, uploaded-image authority, product-poster boundary, mythology-drift boundary, and claim boundary.
# skills/visual-ip-illustrations/references/routing.md:53 matched route id `hermes`, aliases, default=false, output suffix `hermes`, seven route-local references, official sources, MIT license context, generated-sample gate, and source-reviewed status.
# RELEASE_CHECKLIST.md:369 matched Hermes Agent public asset policy fields for public sample review.
# RELEASE_CHECKLIST.md:377 matched generated sample review fields for internal generated sample separation.
# RELEASE_CHECKLIST.md:414 matched public docs keep Hermes source, status, aliases, official URLs, uploaded-image authority, public sample review gate, mythology-drift boundary, product-poster boundary, output paths, and Phase 52 validator/test boundary.
# README.md:7 matched public overview Hermes route contract.
# README.md:126 matched Hermes route detail section.
# README.md:152 matched Hermes route usage contract.
# README.md:162 matched Hermes route metadata row.
# examples/prompts.md:680 matched explicit Hermes prompt smoke section.
```

```bash
rg -n "Hermes Agent|hermes-agent|references/ips/hermes|assets/<article-slug>-hermes/|assets/&lt;article-slug&gt;-hermes/|Generated image 1 \\(16\\)\\.jpeg|mythology-drift boundary|product-poster boundary" skills/visual-ip-illustrations/references/ips/xiaohei/*.md skills/visual-ip-illustrations/references/ips/littlebox/*.md skills/visual-ip-illustrations/references/ips/tom/*.md skills/visual-ip-illustrations/references/ips/ferris/*.md skills/visual-ip-illustrations/references/ips/seal/*.md skills/visual-ip-illustrations/references/ips/openclaw/*.md skills/visual-ip-illustrations/references/ips/gopher/*.md skills/visual-ip-illustrations/references/ips/caixukun/*.md skills/visual-ip-illustrations/references/style-dna.md skills/visual-ip-illustrations/references/xiaohei-ip.md skills/visual-ip-illustrations/references/composition-patterns.md skills/visual-ip-illustrations/references/prompt-template.md skills/visual-ip-illustrations/references/qa-checklist.md; printf 'exit=%s\n' $?
# exit=1
```

```bash
rg -n "winged sandals|winged helmet|caduceus|Greek messenger|Olympian deity|mythology-first|mythology-drift" skills/visual-ip-illustrations/references/ips/hermes/qa-checklist.md skills/visual-ip-illustrations/references/ips/hermes/prompt-template.md skills/visual-ip-illustrations/references/routing.md RELEASE_CHECKLIST.md
# RELEASE_CHECKLIST.md:60 matched route-level mythology-drift boundary.
# RELEASE_CHECKLIST.md:73 matched explicit Hermes smoke mythology-drift boundary.
# RELEASE_CHECKLIST.md:358 matched Greek messenger, winged sandals, winged helmet, caduceus, and Olympian deity exclusion.
# RELEASE_CHECKLIST.md:414 matched public docs mythology-drift boundary.
# skills/visual-ip-illustrations/references/routing.md:19 matched alias boundary excluding Greek messenger, winged sandals, and caduceus terms.
# skills/visual-ip-illustrations/references/routing.md:104 matched mythology-drift markers.
# skills/visual-ip-illustrations/references/ips/hermes/qa-checklist.md and prompt-template.md matched repair and failure markers for mythology drift.
```

```bash
find examples/images examples/images-en skills/visual-ip-illustrations/assets/examples -type f \( -iname '*hermes*' -o -iname '*hermes-agent*' \) -print
# no output
```

```bash
find assets -maxdepth 2 -type f \( -path '*-hermes/*' -o -iname '*hermes*' -o -iname '*hermes-agent*' \) -print 2>/dev/null || true
# no output
```

```bash
git status --short
# M scripts/validate-skill-package.mjs
# M scripts/validate-skill-package.test.mjs
# ?? .planning/phases/52-hermes-validation-and-release-evidence/52-RELEASE-EVIDENCE.md
```

## Hermes Route Smoke

- `SMOKE-HERMES-001` validates explicit Hermes Agent planning, generation, edit, route smoke, route-local references, official source context, MIT license context, uploaded-image authority, raw output path, escaped output path, route isolation, mythology-drift boundary, product-poster boundary, uploaded-character-only output, endorsement/affiliation/sponsorship/approval/impersonation review terms, and public sample review gate.
- `SMOKE-MIXED-HERMES-001` validates nine-route mixed-IP behavior with Xiaohei, Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, and Hermes Agent variant groups.

## Uploaded-Image Smoke

- `SOURCE-HERMES-001` validates `skills/visual-ip-illustrations/references/ips/hermes/source.md`.
- `REFS-HERMES-001` validates the seven-file Hermes Agent route-local pack under `skills/visual-ip-illustrations/references/ips/hermes/`.
- `PROMPT-HERMES-001`, `IP-HERMES-001`, and `QA-HERMES-001` validate uploaded reference image authority, monochrome full-body logo-style identity, black bob haircut with bright highlights, headset or earpiece, black sleeveless dress, white collar tag with an `A`-like mark, black thigh-high stockings, platform heels, slender fashion-figure posture, and central cognitive action gates.

## Source/MIT Boundary Smoke

- `SOURCE-HERMES-001` validates official website, GitHub repository, MIT license URL, docs URL, source-reviewed route status, uploaded conversation attachment authority, public sample policy, review owner, and distribution boundary.
- `NOTICE-HERMES-001` validates source attribution and public sample gate.
- `RELEASE-HERMES-001` validates release checklist review fields for official source outcome, MIT license outcome, uploaded-image identity outcome, mythology-drift outcome, product-poster boundary outcome, route-isolation outcome, endorsement/affiliation/sponsorship/approval/impersonation review outcome, article-metaphor quality outcome, and public-sample decision.

## Docs Consistency

- README variants contain Hermes Agent, `source-reviewed`, `skills/visual-ip-illustrations/references/ips/hermes/source.md`, `assets/<article-slug>-hermes/`, and `assets/&lt;article-slug&gt;-hermes/`.
- `AGENT-HERMES-001` validates `skills/visual-ip-illustrations/agents/openai.yaml`.
- `DOC-PATHS-001` validates raw and escaped Hermes output path markers in public docs.
- `DOC-ROUTES-001` validates Hermes canonical pack and source authority paths.
- `DOC-HERMES-001` validates public Hermes Agent route status, source authority, localized README variants, uploaded-image authority, mythology-drift boundary, product-poster boundary, public sample review gate, and Phase 52 ownership markers.

## Leakage Scan

- `BOUNDARY-HERMES-LEAK-001` scans non-Hermes route-local references and legacy Xiaohei references for Hermes Agent leakage markers.
- Current result: PASS.

## Mythology-Drift Scan

- Hermes route docs preserve the mythology-drift boundary so the route stays grounded in the uploaded Hermes Agent character and official source context.
- Current result: PASS.

## Public Sample Gate

- `BOUNDARY-HERMES-IMG-001` checks `examples/images/`, `examples/images-en/`, and `skills/visual-ip-illustrations/assets/examples/` for rendered Hermes Agent asset filenames.
- Current status: public generated Hermes Agent samples remain pending.
- Current approval status: pending approval record remains incomplete by design.
- Current asset result: no public generated Hermes Agent sample assets are present.

## Generated Sample Gate

- `BOUNDARY-HERMES-GEN-001` keeps internal generated workspace samples under `assets/<article-slug>-hermes/` distinct from public generated sample release gates.
- Current status: generated-sample internal review distinction is enforced.
- Current result: PASS.

## Dirty-Worktree Scope

- Final phase scope allows only `scripts/validate-skill-package.mjs`, `scripts/validate-skill-package.test.mjs`, `.planning/phases/52-hermes-validation-and-release-evidence/52-RELEASE-EVIDENCE.md`, and execution summary/state artifacts after release-evidence validation begins.
- Current result: PASS.

## Requirement Traceability

| Requirement | Evidence |
|-------------|----------|
| VAL-01 | `AGENT-HERMES-001`, `ROUTE-HERMES-001`, `REFS-HERMES-001`, `PROMPT-HERMES-001`, `IP-HERMES-001`, `QA-HERMES-001`, `SOURCE-HERMES-001`, `DOC-HERMES-001`, `NOTICE-HERMES-001`, `SMOKE-HERMES-001`, `SMOKE-MIXED-HERMES-001`, `RELEASE-HERMES-001`, and `VAL-HERMES-EVIDENCE-001` fail on route metadata, source, pack, docs, examples, NOTICE, release, metadata, or evidence drift. |
| VAL-02 | `BOUNDARY-HERMES-LEAK-001` fails when Hermes Agent identity, source, path, uploaded-image, MIT license, mythology-drift, product-poster, uploaded-character-only, endorsement, affiliation, sponsorship, approval, or impersonation markers leak into Xiaohei, Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, or legacy Xiaohei route-local references. |
| VAL-03 | `BOUNDARY-HERMES-IMG-001` fails when public generated Hermes Agent samples appear without complete release checklist approval fields, and `BOUNDARY-HERMES-GEN-001` preserves the internal generated workspace distinction. |
| VAL-04 | `scripts/validate-skill-package.test.mjs` covers Hermes route parsing, nine-route ordering, default preservation, output path markers, uploaded-image markers, MIT source markers, mythology-drift markers, smoke prompts, leakage fixtures, public asset gates, generated sample gates, approval placeholder fields, release evidence drift, and full-pass output. |
| VAL-05 | This release evidence records validator output, Node test output, `git diff --check`, focused Hermes marker scan output, public sample gate output, Hermes route smoke, uploaded-image smoke, source/MIT boundary smoke, docs consistency, leakage scan, mythology-drift scan, generated sample gate, and dirty-worktree scope. |
