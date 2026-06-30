# Requirements: Hermes Agent Visual IP Integration

**Defined:** 2026-06-18
**Core Value:** Users can choose a visual IP and receive article illustrations whose character, style rules, prompts, QA gates, and saved outputs stay consistent with that IP.

## v1.10 Requirements

### Route and Source

- [x] **ROUTE-01**: User can select Hermes Agent as an explicit visual IP route through clear aliases including `Hermes Agent`, `Hermes`, `hermes`, `hermes-agent`, `Hermes logo`, and `Hermes Agent logo` while Xiaohei remains the omitted-IP default.
- [x] **ROUTE-02**: User can rely on route id `hermes`, display name `Hermes Agent`, output suffix `hermes`, and output directory `assets/<article-slug>-hermes/`.
- [x] **ROUTE-03**: Maintainer can inspect Hermes routing metadata and see all required references, uploaded-image authority, official source context, route status `source-reviewed`, and `default=false`.
- [x] **SRC-01**: Maintainer can inspect `references/ips/hermes/source.md` and see the official website, official repository, MIT license, documentation URL, third-party icon context when confirmed, uploaded conversation attachment authority, public sample policy, review owner, route status, and source-image context.
- [x] **SRC-02**: User and maintainer can see that the conversation attachment `Generated image 1 (16).jpeg` is the route visual authority, with stable markers for a monochrome full-body logo-style character, black bob haircut with bright highlights, headset or earpiece, black sleeveless dress, white collar tag with an `A`-like mark, black thigh-high stockings, platform heels, and slender fashion-figure posture.

### Hermes IP Pack

- [x] **PACK-01**: User can read a Hermes route-local pack that isolates style, identity, composition, prompt, QA, source, mythology-drift guardrails, sample policy, and output behavior from other IP routes.
- [x] **PACK-02**: User can plan Hermes shots with route-specific fields for character state, character action, core article idea, structure type, objects, labels, source context notes, mythology-drift notes, and output path.
- [x] **PACK-03**: User can generate Hermes prompts where the uploaded character performs the central cognitive article action in a sparse 16:9 illustration.
- [x] **PACK-04**: User can apply Hermes edit prompts for stronger participation, uploaded-image identity repair, title removal, text reduction, mythology-drift repair, and unaffected-content preservation.
- [x] **PACK-05**: User can use Hermes QA gates that reject generic anime or assistant drift, mythological Hermes imagery, missing headset, missing bob-hair highlight silhouette, missing black sleeveless dress, missing collar tag, missing stockings or platform heels, product-poster drift, passive placement, route leakage, excessive text, and copied composition.

### Runtime Integration

- [x] **RUN-01**: User can invoke Hermes through the skill controller, route selection rules, progressive reference loading, planning fields, generation dispatch, edit routing, QA dispatch, and delivery reports.
- [x] **RUN-02**: User can request mixed-IP output where Hermes and all existing routes create separate route groups with their own references, prompts, QA rules, and output paths.
- [x] **RUN-03**: User receives Hermes delivery reports with selected visual IP, image count, purpose per image, saved path under `assets/<article-slug>-hermes/`, uploaded-image authority note, source-context note, and route stability notes.
- [x] **RUN-04**: Agent metadata and skill instructions present Hermes as a selectable source-reviewed route while preserving Visual IP Illustrations identity and the legacy `$ian-xiaohei-illustrations` alias.

### Public Documentation

- [x] **DOC-01**: User can read README route selection, workflow, output path, and route descriptions with Hermes Agent as an explicit source-reviewed uploaded-image route.
- [x] **DOC-02**: User can copy examples for Hermes planning, generation, editing, and mixed-IP variants with `assets/<article-slug>-hermes/` paths.
- [x] **DOC-03**: Maintainer can read NOTICE and release checklist entries that include official Hermes Agent source context, MIT license, uploaded-image authority, public sample policy, and release review gates.
- [x] **DOC-04**: User and maintainer can see Hermes docs preserve default-route behavior, route isolation, source-reviewed route status, no endorsement claims, no product-poster drift, and uploaded-character-only output.
- [x] **DOC-05**: Public release surfaces stay consistent across README variants, prompt examples, agent metadata, NOTICE, and release checklist when Hermes is introduced.

### Validation and Release Evidence

- [x] **VAL-01**: Validator fails when Hermes route metadata, source record, required references, output paths, docs, examples, NOTICE, release checklist, or agent metadata drift from the v1.10 contract.
- [x] **VAL-02**: Validator fails when Hermes identity markers leak into Xiaohei, Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, or Cai Xukun route-local packs.
- [x] **VAL-03**: Validator fails when public generated Hermes samples appear without explicit release checklist approval.
- [x] **VAL-04**: Node tests cover Hermes route parsing, route ordering, default preservation, output path markers, uploaded-image markers, source/license markers, mythology-drift markers, smoke prompts, leakage fixtures, public asset gates, and full-pass output.
- [x] **VAL-05**: Final release evidence records validator output, Node test output, `git diff --check`, Hermes route smoke, uploaded-image and source-boundary smoke, docs consistency, leakage scan, mythology-drift scan, and public sample gate status.

## Future Requirements

### Route Manifests

- **MNF-01**: Maintainer can track all route source, license, trademark, uploaded-image, local-reference, public-sample, output-path, likeness-boundary, and validation metadata through a machine-readable visual-IP manifest.
- **MNF-02**: Maintainer can generate route tables and validator expectations from the manifest.

### Assets

- **AST-01**: Maintainer can store and hash canonical local or uploaded source images for every visual-reference route.
- **AST-02**: User can generate a public-approved comparison sheet across active routes after sample review.
- **AST-03**: Maintainer can run automated visual regression checks against approved calibration images.

### Distribution

- **DIST-01**: Maintainer can package selected IP variants through a release script.
- **DIST-02**: User can install selected IP routes through a CLI-level selector.

## Out of Scope

Explicitly excluded. Documented to prevent scope creep.

| Feature | Reason |
|---------|--------|
| Making Hermes the default IP | Xiaohei remains the compatibility baseline and omitted-IP default. |
| Generic custom-IP import | v1.10 adds one concrete Hermes route. |
| Replacing the uploaded attachment as route authority | The user-uploaded conversation attachment is the visual authority for this milestone. |
| Mythological Hermes route behavior | This route is Hermes Agent by Nous Research and uses the uploaded character authority. |
| Product advertising or CLI screenshot output | The route remains an article-illustration route. |
| Official endorsement or affiliation claims | The route records official source context and requires release review. |
| Public generated Hermes gallery before approval | Public samples require release review. |
| Changing Xiaohei, Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, or Cai Xukun behavior | The milestone is scoped to Hermes. |
| Renaming the whole package | Visual IP Illustrations remains the product identity. |
| Removing legacy skill invocation | `$ian-xiaohei-illustrations` remains a validated compatibility alias. |
| Forcing visible labels into English | Visible labels continue to follow the user's requested language. |
| Hosted app, UI, API, database, or build runtime | The product remains a lightweight Codex Skill package. |

## Traceability

Which phases cover which requirements. Updated during roadmap creation.

| Requirement | Phase | Status |
|-------------|-------|--------|
| ROUTE-01 | Phase 48 | Complete |
| ROUTE-02 | Phase 48 | Complete |
| ROUTE-03 | Phase 48 | Complete |
| SRC-01 | Phase 48 | Complete |
| SRC-02 | Phase 48 | Complete |
| PACK-01 | Phase 49 | Complete |
| PACK-02 | Phase 49 | Complete |
| PACK-03 | Phase 49 | Complete |
| PACK-04 | Phase 49 | Complete |
| PACK-05 | Phase 49 | Complete |
| RUN-01 | Phase 50 | Complete |
| RUN-02 | Phase 50 | Complete |
| RUN-03 | Phase 50 | Complete |
| RUN-04 | Phase 50 | Complete |
| DOC-01 | Phase 51 | Complete |
| DOC-02 | Phase 51 | Complete |
| DOC-03 | Phase 51 | Complete |
| DOC-04 | Phase 51 | Complete |
| DOC-05 | Phase 51 | Complete |
| VAL-01 | Phase 52 | Complete |
| VAL-02 | Phase 52 | Complete |
| VAL-03 | Phase 52 | Complete |
| VAL-04 | Phase 52 | Complete |
| VAL-05 | Phase 52 | Complete |
| MNF-01 | Future | Future |
| MNF-02 | Future | Future |
| AST-01 | Future | Future |
| AST-02 | Future | Future |
| AST-03 | Future | Future |
| DIST-01 | Future | Future |
| DIST-02 | Future | Future |

**Coverage:**

- v1.10 requirements: 24 total
- Mapped to phases: 24
- Unmapped: 0

---
*Requirements defined: 2026-06-18*
*Last updated: 2026-06-18 after completing Phase 52 Hermes validation and release evidence*
