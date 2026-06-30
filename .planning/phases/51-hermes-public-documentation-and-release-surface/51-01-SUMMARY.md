---
phase: 51-hermes-public-documentation-and-release-surface
plan: 51-01
status: complete
subsystem: public-documentation
tags:
  - hermes-agent
  - public-docs
  - release-surface
requirements:
  - DOC-01
  - DOC-02
  - DOC-03
  - DOC-04
  - DOC-05
completed_at: 2026-06-18
key_files:
  - README.md
  - readmes/README.*.md
  - examples/prompts.md
  - NOTICE.md
  - RELEASE_CHECKLIST.md
---

# Phase 51 Plan 51-01: Hermes Public Documentation and Release Surface Summary

Hermes Agent public release documentation now covers route discovery, prompt usage, attribution, sample gates, and Phase 52 validator ownership without adding generated Hermes images or public Hermes sample assets.

## Status

status: complete

## Files Changed

- `README.md`
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
- `examples/prompts.md`
- `NOTICE.md`
- `RELEASE_CHECKLIST.md`
- `.planning/phases/51-hermes-public-documentation-and-release-surface/51-01-SUMMARY.md`

## Requirement Coverage

- DOC-01: README surfaces now list Hermes Agent as route id `hermes`, status `source-reviewed`, aliases, source pointer, raw and escaped output paths, uploaded-image authority, MIT license context, public sample review gate, mythology-drift boundary, product-poster boundary, route isolation, and uploaded-character-only article illustration output.
- DOC-02: `examples/prompts.md` now includes canonical Hermes planning, generation, edit, explicit route smoke, mixed-IP ninth variant group, and maintainer smoke examples with required Hermes fields.
- DOC-03: `NOTICE.md` now records Hermes Agent source attribution, official website, official repository, MIT license URL, docs URL, source authority, uploaded-image authority from `Generated image 1 (16).jpeg`, public sample gate, and review terms.
- DOC-04: `RELEASE_CHECKLIST.md` now includes Phase 52 ownership, explicit Hermes smoke, attribution review, dedicated Hermes source/MIT/uploaded-image/public-sample gate, installable package boundary notes, path marker checks, and final Hermes release review.
- DOC-05: Public docs explicitly keep generated Hermes image publication behind release review and leave generated/public sample assets absent.

## Verification Results

- PASS: `rg -n "Hermes Agent|assets/<article-slug>-hermes/|assets/&lt;article-slug&gt;-hermes/|references/ips/hermes/source.md|source-reviewed|Generated image 1 \\(16\\)\\.jpeg|MIT license|mythology|product-poster|public sample review" README.md readmes/README.*.md`
- PASS: `rg -n "hermes/|hermes-ip.md|assets/<article-slug>-hermes|assets/&lt;article-slug&gt;-hermes|Phase 52 owns Hermes" README.md readmes/README.*.md`
- PASS: `rg -n "Hermes Agent state|Hermes Agent action|Source context note|Mythology-drift note|Product-poster boundary note|assets/<article-slug>-hermes|assets/&lt;article-slug&gt;-hermes|Generated image 1 \\(16\\)\\.jpeg|MIT license context|public sample review gate" examples/prompts.md`
- PASS: `rg -n "nine separate variant groups|Hermes Agent variant group|Route Smoke: Explicit Hermes Agent|Smoke: Hermes Agent source-reviewed route status" examples/prompts.md`
- PASS: `rg -n "Hermes Agent Source|https://hermes-agent.nousresearch.com/|https://github.com/NousResearch/hermes-agent|https://github.com/NousResearch/hermes-agent/blob/main/LICENSE|https://hermes-agent.nousresearch.com/docs/|Generated image 1 \\(16\\)\\.jpeg|public generated Hermes samples|mythology-drift|product-poster" NOTICE.md RELEASE_CHECKLIST.md`
- PASS: `find examples/images examples/images-en skills/visual-ip-illustrations/assets/examples -path '*hermes*' -print`
- PASS: `git diff --check -- README.md readmes/README.*.md examples/prompts.md NOTICE.md RELEASE_CHECKLIST.md`

## Asset Counts

Generated Hermes image count: 0

Public Hermes sample asset count: 0

## Deviations from Plan

### Auto-fixed Issues

**1. [Rule 1 - Bug] Fixed README directory tree indentation after Hermes insertion**
- **Found during:** Task 1 verification
- **Issue:** The generated `hermes/` directory tree made the preceding `caixukun/` subtree lose tree-line indentation.
- **Fix:** Normalized the `caixukun/` and `hermes/` tree entries across README variants.
- **Files modified:** `README.md`, `readmes/README.*.md`

### Tooling Notes

- `gsd-tools` was unavailable in the shell PATH during execution, so SDK state helpers could not be used from this environment. The requested plan artifacts, verification, and commit were still completed in the repository.

## Known Stubs

None.

## Threat Flags

None.

## Phase 52 Ownership

Phase 52 owns Hermes validator hardening, Node tests, final release evidence, leakage scan, and public sample gate automation.

## Self-Check: PASSED

- Summary file exists.
- Hermes public README, prompt, NOTICE, and release checklist markers are present.
- Generated Hermes image count remains 0.
- Public Hermes sample asset count remains 0.
