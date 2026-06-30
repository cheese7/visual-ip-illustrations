# Phase 49: Hermes Canonical Pack - Discussion Log

> **Audit trail only.** Do not use as input to planning, research, or execution agents.
> Decisions are captured in CONTEXT.md. This log preserves the alternatives considered.

**Date:** 2026-06-18
**Phase:** 49-Hermes Canonical Pack
**Areas discussed:** pack file set, route required references, uploaded-image authority, source/license boundary, mythology-drift boundary, product-poster boundary, deferred surfaces, verification architecture

---

## Pack File Set

| Option | Description | Selected |
|--------|-------------|----------|
| Route-local canonical pack | Create `index.md`, `style-dna.md`, `hermes-ip.md`, `composition-patterns.md`, `prompt-template.md`, and `qa-checklist.md` under `references/ips/hermes/`, preserving `source.md` as authority. | yes |
| Source-only continuation | Keep only `source.md` and postpone operational references. | |
| Broad runtime integration | Create pack files and wire `SKILL.md` in the same phase. | |

**Decision:** Phase 49 owns the route-local operational pack. Runtime wiring moves to Phase 50.
**Notes:** This phase follows Cai Xukun for uploaded-image authority and Go Gopher for source-reviewed operational pack shape.

---

## Route Required References

| Option | Description | Selected |
|--------|-------------|----------|
| Expand in Phase 49 | Update the Hermes `routing.md` row after the full route-local pack exists. | yes |
| Leave source-only | Keep `required_references` limited to `source.md` until runtime integration. | |
| Defer to validator phase | Wait for Phase 52 to expand route metadata. | |

**Decision:** Expand now because Phase 49 creates the files and Phase 50 needs a complete progressive-loading list.
**Notes:** The required reference list should include index, source, style DNA, identity, composition, prompt, and QA files.

---

## Uploaded-Image Authority

| Option | Description | Selected |
|--------|-------------|----------|
| Preserve Phase 48 authority | Carry conversation attachment `Generated image 1 (16).jpeg` and the full marker list into every operational file. | yes |
| Treat as generic anime assistant | Use broad assistant-character rules without the uploaded marker list. | |
| Use official product imagery as character authority | Promote official Hermes product or site imagery into the route identity. | |

**Decision:** The conversation attachment remains the visual authority. Official source context supports route metadata and release review.
**Notes:** The marker list is monochrome full-body logo-style character, black bob haircut with bright highlights, headset or earpiece, black sleeveless dress, white collar tag with an `A`-like mark, black thigh-high stockings, platform heels, and slender fashion-figure posture.

---

## Source, License, Product, and Mythology Boundaries

| Option | Description | Selected |
|--------|-------------|----------|
| Preserve Phase 48 boundaries | Carry official website, repository, MIT license URL, documentation URL, product-poster boundary, endorsement boundary, and mythology-drift boundary into operational files. | yes |
| Product-poster route | Make Hermes outputs look like product launch graphics, web heroes, CLI screenshots, or repository promotion. | |
| Mythology route | Use Greek Hermes symbols as a default visual language. | |

**Decision:** Hermes remains a source-reviewed uploaded-image article-illustration route.
**Notes:** Product-poster output, official endorsement claims, winged sandals, winged helmet, caduceus, Greek messenger scenes, Olympian deity framing, and mythology-first symbols fail the route.

---

## Planning, Prompt, Edit, and QA Fields

| Option | Description | Selected |
|--------|-------------|----------|
| Full operational pack fields | Include planning fields, one-image prompt, edit prompts, QA gates, delivery path, and route block. | yes |
| Minimal prose references | Add short style and identity notes with no operational prompt/edit/QA scaffolding. | |
| Test-first validator expansion | Update validator and tests before creating human-readable pack files. | |

**Decision:** Phase 49 delivers human-readable operational references that are deterministic enough for Phase 52 validation.
**Notes:** Required edit prompts are Stronger Hermes Participation, Uploaded-Image Identity Repair, Title Removal, Text Reduction, Mythology-Drift Repair, Product-Poster Repair, Route Leakage Repair, and Unaffected-Content Preservation.

---

## Deferred Surfaces

| Option | Description | Selected |
|--------|-------------|----------|
| Keep Phase 49 narrow | Defer runtime controller behavior, public docs/release surfaces, and validator/test hardening to Phases 50-52. | yes |
| Bundle runtime integration | Include `SKILL.md` selected-IP runtime work now. | |
| Bundle docs and tests | Include README, NOTICE, examples, release checklist, validator, and Node tests now. | |

**Decision:** Phase 49 creates only the canonical pack and route reference expansion.
**Notes:** The later phase split stays intact: Phase 50 runtime, Phase 51 docs/release surfaces, Phase 52 validation and release evidence.

---

## Verification Architecture

| Option | Description | Selected |
|--------|-------------|----------|
| Deterministic file checks | Grep every required file, marker, planning field, edit prompt, QA gate, route row, leakage boundary, and public sample gate; run `git diff --check`. | yes |
| Full validator update | Extend `scripts/validate-skill-package.mjs` and Node tests now. | |
| Visual generation smoke | Generate Hermes public sample images in this phase. | |

**Decision:** Phase 49 verification uses deterministic file checks and route leakage scans.
**Notes:** Phase 52 owns validator and Node regression expansion. Public generated Hermes samples remain behind release review.

## Agent Discretion

- Exact Markdown section ordering inside the new Hermes route-local files.
- Exact text density of prompt/edit/QA templates, provided PACK-01 through PACK-05 remain grep-friendly.
- Optional `source.md` wording updates for pack navigation and current-route-pack wording.

## Deferred Ideas

- Phase 50 runtime controller integration.
- Phase 51 public documentation and release surfaces.
- Phase 52 validator/test hardening and final release evidence.
