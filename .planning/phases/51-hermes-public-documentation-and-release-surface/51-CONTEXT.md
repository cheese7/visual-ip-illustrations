---
phase: 51-hermes-public-documentation-and-release-surface
status: discussion
date: 2026-06-18
depends_on:
  - 50-hermes-skill-controller-integration
requirements:
  - DOC-01
  - DOC-02
  - DOC-03
  - DOC-04
  - DOC-05
---

# Phase 51 Context: Hermes Public Documentation and Release Surface

## Goal

Users and maintainers can learn, invoke, review, and release Hermes Agent through public and runtime-facing documentation with uploaded-image and source/license clarity.

## Phase Inputs

- Phase 48 completed Hermes routing and source contract.
- Phase 49 completed the Hermes seven-file route-local pack.
- Phase 50 completed `SKILL.md` controller integration and `agents/openai.yaml` metadata.

## Requirements

- DOC-01: User can read README route selection, workflow, output path, and route descriptions with Hermes Agent as an explicit source-reviewed uploaded-image route.
- DOC-02: User can copy examples for Hermes planning, generation, editing, and mixed-IP variants with `assets/<article-slug>-hermes/` paths.
- DOC-03: Maintainer can read NOTICE and release checklist entries that include official Hermes Agent source context, MIT license, uploaded-image authority, public sample policy, and release review gates.
- DOC-04: User and maintainer can see Hermes docs preserve default-route behavior, route isolation, source-reviewed route status, no endorsement claims, no product-poster drift, and uploaded-character-only output.
- DOC-05: Public release surfaces stay consistent across README variants, prompt examples, agent metadata, NOTICE, and release checklist when Hermes is introduced.

## Public Documentation Surfaces

- `README.md`
- `readmes/README.*.md`
- `examples/prompts.md`
- `NOTICE.md`
- `RELEASE_CHECKLIST.md`
- `skills/visual-ip-illustrations/agents/openai.yaml` parity check
- `skills/visual-ip-illustrations/SKILL.md` parity check

## Required Hermes Public Markers

- `Hermes Agent`
- route id `hermes`
- route status `source-reviewed`
- aliases `Hermes Agent`, `Hermes`, `hermes`, `hermes-agent`, `Hermes logo`, and `Hermes Agent logo`
- output path `assets/<article-slug>-hermes/`
- escaped marker `assets/&lt;article-slug&gt;-hermes/`
- source pointer `skills/visual-ip-illustrations/references/ips/hermes/source.md`
- uploaded-image authority from `Generated image 1 (16).jpeg`
- official source context
- MIT license context
- public sample review gate
- mythology-drift boundary
- product-poster boundary
- route isolation
- uploaded-character-only article illustration output

## Constraints

- Preserve Visual IP Illustrations identity.
- Preserve `$visual-ip-illustrations`.
- Preserve `$ian-xiaohei-illustrations` compatibility alias.
- Preserve omitted visual IP default as Xiaohei.
- Preserve existing route documentation for Xiaohei, Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, and Cai Xukun.
- Add no generated Hermes images or public Hermes sample assets.
- Keep validator and Node test hardening in Phase 52.

## Verification Targets

```bash
rg -n "Hermes Agent|assets/<article-slug>-hermes/|assets/&lt;article-slug&gt;-hermes/|references/ips/hermes/source.md|source-reviewed|Generated image 1 \\(16\\)\\.jpeg|MIT license|mythology|product-poster|public sample review" README.md readmes/README.*.md examples/prompts.md NOTICE.md RELEASE_CHECKLIST.md skills/visual-ip-illustrations/agents/openai.yaml
find examples/images examples/images-en skills/visual-ip-illustrations/assets/examples -path '*hermes*' -print
git diff --check
```

Expected public sample asset check output: empty.
