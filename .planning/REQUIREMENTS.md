# Requirements: Linux Mascot IP Integration

**Defined:** 2026-07-01
**Core Value:** Users can choose a visual IP and receive article illustrations whose character, style rules, prompts, QA gates, and saved outputs stay consistent with that IP.

## v1.11 Requirements

### Route and Source

- [ ] **ROUTE-01**: User can select Linux Mascot as an explicit visual IP route through clear aliases including `Linux Mascot`, `Linux mascot`, `Linux`, `linux`, `Tux`, `tux`, `Linux penguin`, and `Tux penguin` while Xiaohei remains the omitted-IP default.
- [ ] **ROUTE-02**: User can rely on route id `linux`, display name `Linux Mascot`, output suffix `linux`, and output directory `assets/<article-slug>-linux/`.
- [ ] **ROUTE-03**: Maintainer can inspect Linux Mascot routing metadata and see all required references, uploaded-image authority, Tux source context, Linux trademark-boundary context, route status `source-reviewed`, and `default=false`.
- [ ] **SRC-01**: Maintainer can inspect `references/ips/linux/source.md` and see Larry Ewing Tux attribution, GIMP attribution condition, Linux Foundation trademark guidance, Linux trademark ownership context, uploaded local image authority, public sample policy, review owner, route status, and source-image context.
- [ ] **SRC-02**: User and maintainer can see that `/Users/longnv/Downloads/Linux-logo.jpg` is the route visual authority, with stable markers for a glossy black rounded penguin head and body, white face eye patches, large oval eyes with dark pupils and small highlights, yellow-orange beak with two nostril dots, white oval belly, long black flippers, seated rounded posture, and oversized yellow-orange webbed feet.

### Linux Mascot IP Pack

- [ ] **PACK-01**: User can read a Linux Mascot route-local pack that isolates style, identity, composition, prompt, QA, source, trademark-boundary guardrails, sample policy, and output behavior from other IP routes.
- [ ] **PACK-02**: User can plan Linux Mascot shots with route-specific fields for mascot state, mascot action, core article idea, structure type, objects, labels, source context notes, trademark-boundary notes, and output path.
- [ ] **PACK-03**: User can generate Linux Mascot prompts where Tux performs the central cognitive article action in a sparse 16:9 illustration.
- [ ] **PACK-04**: User can apply Linux Mascot edit prompts for stronger participation, uploaded-image identity repair, title removal, text reduction, trademark-boundary repair, and unaffected-content preservation.
- [ ] **PACK-05**: User can use Linux Mascot QA gates that reject generic penguin drift, distro-logo drift, missing white belly, missing yellow-orange beak, missing oversized yellow-orange webbed feet, missing seated Tux posture, official endorsement claims, passive placement, route leakage, excessive text, and copied composition.

### Runtime Integration

- [ ] **RUN-01**: User can invoke Linux Mascot through the skill controller, route selection rules, progressive reference loading, planning fields, generation dispatch, edit routing, QA dispatch, and delivery reports.
- [ ] **RUN-02**: User can request mixed-IP output where Linux Mascot and all existing routes create separate route groups with their own references, prompts, QA rules, and output paths.
- [ ] **RUN-03**: User receives Linux Mascot delivery reports with selected visual IP, image count, purpose per image, saved path under `assets/<article-slug>-linux/`, uploaded-image authority note, source/trademark note, and route stability notes.
- [ ] **RUN-04**: Agent metadata and skill instructions present Linux Mascot as a selectable source-reviewed route while preserving Visual IP Illustrations identity and the legacy `$ian-xiaohei-illustrations` alias.

### Public Documentation

- [ ] **DOC-01**: User can read README route selection, workflow, output path, and route descriptions with Linux Mascot as an explicit source-reviewed Tux route.
- [ ] **DOC-02**: User can copy examples for Linux Mascot planning, generation, editing, and mixed-IP variants with `assets/<article-slug>-linux/` paths.
- [ ] **DOC-03**: Maintainer can read NOTICE and release checklist entries that include Larry Ewing Tux attribution, GIMP attribution condition, Linux trademark guidance, uploaded-image authority, public sample policy, and release review gates.
- [ ] **DOC-04**: User and maintainer can see Linux Mascot docs preserve default-route behavior, route isolation, source-reviewed route status, no endorsement claims, no distro-logo drift, and uploaded-image-only output.
- [ ] **DOC-05**: Public release surfaces stay consistent across README variants, prompt examples, agent metadata, NOTICE, and release checklist when Linux Mascot is introduced.

### Validation and Release Evidence

- [ ] **VAL-01**: Validator fails when Linux Mascot route metadata, source record, required references, output paths, docs, examples, NOTICE, release checklist, or agent metadata drift from the v1.11 contract.
- [ ] **VAL-02**: Validator fails when Linux Mascot identity markers leak into Xiaohei, Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, or Hermes Agent route-local packs.
- [ ] **VAL-03**: Validator fails when public generated Linux Mascot samples appear without explicit release checklist approval.
- [ ] **VAL-04**: Node tests cover Linux Mascot route parsing, route ordering, default preservation, output path markers, uploaded-image markers, Tux attribution markers, Linux trademark-boundary markers, smoke prompts, leakage fixtures, public asset gates, and full-pass output.
- [ ] **VAL-05**: Final release evidence records validator output, Node test output, `git diff --check`, Linux Mascot route smoke, uploaded-image and source-boundary smoke, docs consistency, leakage scan, trademark-boundary scan, and public sample gate status.

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
| Making Linux Mascot the default IP | Xiaohei remains the compatibility baseline and omitted-IP default. |
| Generic custom-IP import | v1.11 adds one concrete Linux Mascot route. |
| Replacing the uploaded local image as route authority | `/Users/longnv/Downloads/Linux-logo.jpg` is the visual authority for this milestone. |
| Linux distro branding or logo packs | The route is Tux-focused and does not add distro-specific marks. |
| Official endorsement or affiliation claims | The route records source and trademark context and requires release review. |
| Product advertising or CLI screenshot output | The route remains an article-illustration route. |
| Public generated Linux Mascot gallery before approval | Public samples require release review. |
| Changing Xiaohei, Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, or Hermes Agent behavior | The milestone is scoped to Linux Mascot. |
| Renaming the whole package | Visual IP Illustrations remains the product identity. |
| Removing legacy skill invocation | `$ian-xiaohei-illustrations` remains a validated compatibility alias. |
| Forcing visible labels into English | Visible labels continue to follow the user's requested language. |
| Hosted app, UI, API, database, or build runtime | The product remains a lightweight Codex Skill package. |

## Traceability

Which phases cover which requirements. Updated during roadmap creation.

| Requirement | Phase | Status |
|-------------|-------|--------|
| ROUTE-01 | Phase 53 | Pending |
| ROUTE-02 | Phase 53 | Pending |
| ROUTE-03 | Phase 53 | Pending |
| SRC-01 | Phase 53 | Pending |
| SRC-02 | Phase 53 | Pending |
| PACK-01 | Phase 54 | Pending |
| PACK-02 | Phase 54 | Pending |
| PACK-03 | Phase 54 | Pending |
| PACK-04 | Phase 54 | Pending |
| PACK-05 | Phase 54 | Pending |
| RUN-01 | Phase 55 | Pending |
| RUN-02 | Phase 55 | Pending |
| RUN-03 | Phase 55 | Pending |
| RUN-04 | Phase 55 | Pending |
| DOC-01 | Phase 56 | Pending |
| DOC-02 | Phase 56 | Pending |
| DOC-03 | Phase 56 | Pending |
| DOC-04 | Phase 56 | Pending |
| DOC-05 | Phase 56 | Pending |
| VAL-01 | Phase 57 | Pending |
| VAL-02 | Phase 57 | Pending |
| VAL-03 | Phase 57 | Pending |
| VAL-04 | Phase 57 | Pending |
| VAL-05 | Phase 57 | Pending |
| MNF-01 | Future | Future |
| MNF-02 | Future | Future |
| AST-01 | Future | Future |
| AST-02 | Future | Future |
| AST-03 | Future | Future |
| DIST-01 | Future | Future |
| DIST-02 | Future | Future |

**Coverage:**

- v1.11 requirements: 24 total
- Mapped to phases: 24
- Unmapped: 0

---
*Requirements defined: 2026-07-01*
*Last updated: 2026-07-01 after starting v1.11 Linux Mascot IP Integration*
