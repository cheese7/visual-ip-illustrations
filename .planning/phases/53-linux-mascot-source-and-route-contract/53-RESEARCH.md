# Phase 53: Linux Mascot Source and Route Contract - Research

**Researched:** 2026-07-01
**Domain:** Codex Skill route/source contract for a source-reviewed uploaded-image Linux Mascot visual IP
**Confidence:** HIGH

## User Constraints

### Locked Decisions

- Phase 53 delivers only the Linux Mascot route/source authority: update `skills/visual-ip-illustrations/references/routing.md` and create `skills/visual-ip-illustrations/references/ips/linux/source.md`. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- Linux Mascot route metadata is locked to route id `linux`, display name `Linux Mascot`, `default=false`, route status `source-reviewed`, output suffix `linux`, and output path `assets/<article-slug>-linux/`. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- The escaped output marker `assets/&lt;article-slug&gt;-linux/` should be preserved where escaped docs path markers are relevant. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- The `routing.md` table shape stays `id`, `display_name`, `aliases`, `default`, `output_suffix`, `required_references`, `attribution_context`, and `status`. [VERIFIED: skills/visual-ip-illustrations/references/routing.md]
- Phase 53 `required_references` stays limited to `references/ips/linux/source.md`; Phase 54 expands the row after the full Linux Mascot pack exists. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- Linux Mascot aliases are exactly `Linux Mascot`, `Linux mascot`, `Linux`, `linux`, `Tux`, `tux`, `Linux penguin`, and `Tux penguin` for Phase 53. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- Broad penguin, server, kernel, distro, distro-logo, Linux Foundation, operating-system, CLI, terminal, product, brand-campaign, and generic mascot terms stay outside the Phase 53 alias set. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- The source record must record Larry Ewing Tux attribution, GIMP attribution condition, Linux Foundation trademark guidance, Linux trademark ownership context, uploaded local image authority, source-image context, public sample policy, review owner, route status, and distribution boundary. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- Source anchors are `https://isc.tamu.edu/~lewing/linux/`, `https://www.linuxfoundation.org/legal/trademark-usage`, and `https://www.linuxfoundation.org/legal/the-linux-mark`. The context already contains the URLs, so no web browsing is required for this planning stage. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- Uploaded visual authority is `/Users/longnv/Downloads/Linux-logo.jpg`; recorded metadata is JPEG image data, JFIF 1.01, progressive, 8-bit precision, 3500x2300 pixels, 3 components, SHA-256 `071bc327e4a2814864f9e2fcdea99aa50482a92ef4e816de9d9ce5f40e17bb2a`. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- Fixed uploaded-image markers are glossy black rounded penguin head and body, white face eye patches, large oval eyes with dark pupils and small highlights, yellow-orange beak with two nostril dots, white oval belly, long black flippers, seated rounded posture, and oversized yellow-orange webbed feet. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- Generated Linux Mascot route outputs stay sparse 16:9 article illustrations. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- Official Linux endorsement, affiliation, sponsorship, approval, certification, compatibility, Linux Foundation campaign framing, Linux Foundation logo use, distro-logo use, and distro branding stay outside this route. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- Product advertising, product-poster output, CLI screenshots, web hero graphics, kernel dashboard screenshots, and operating-system marketing graphics stay outside this route. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- Xiaohei remains the omitted-IP default; Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, Hermes Agent, and Linux Mascot remain explicit isolated routes. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]

### the agent's Discretion

- Use compact English Markdown with grep-friendly marker strings in `source.md`. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- Append Linux Mascot after Hermes Agent in `routing.md` to preserve existing route order while adding the v1.11 route. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- Create only `source.md` in Phase 53; Phase 54 owns the pack index and the full route-local reference set. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]

### Deferred Ideas

- Phase 54 owns Linux Mascot style DNA, identity rules, composition patterns, prompt template, edit prompts, QA checklist, sample-policy wording, full route-local pack navigation, and expanded `required_references`. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- Phase 55 owns Linux Mascot skill controller integration, selected-IP reference loading, mixed-IP grouping, generation/edit routing, QA dispatch, and delivery reporting. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- Phase 56 owns README variants, examples, NOTICE, RELEASE_CHECKLIST, broad `SKILL.md` docs, and `agents/openai.yaml` Linux Mascot discovery wording. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- Phase 57 owns validator coverage, Node tests, leakage scans, trademark-boundary scans, public sample gates, generated sample gates, route smoke, uploaded-image and source-boundary smoke, docs consistency, and release evidence. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- Future work may add machine-readable route manifests, uploaded source-image hashing, visual regression, public comparison sheets, release packaging, and selected-IP installation variants. [VERIFIED: .planning/REQUIREMENTS.md]

## Summary

Phase 53 should be planned as a narrow route/source slice: update `routing.md`, create `references/ips/linux/source.md`, and verify the contract with targeted `rg` checks plus diff hygiene. [VERIFIED: .planning/ROADMAP.md] [VERIFIED: .planning/REQUIREMENTS.md]

The closest precedent is Phase 48 Hermes because it added an uploaded-image source-reviewed route/source contract first, then deferred pack, controller, docs, and validation hardening. [VERIFIED: .planning/phases/48-hermes-source-and-route-contract/48-01-PLAN.md] Go Gopher is the closest mascot attribution and source-boundary source-record pattern. [VERIFIED: skills/visual-ip-illustrations/references/ips/gopher/source.md] OpenClaw is the closest uploaded visual authority and public-sample source-record pattern. [VERIFIED: skills/visual-ip-illustrations/references/ips/openclaw/source.md]

Primary recommendation: implement Phase 53 with the Phase 48 route-first/source-only structure, Go Gopher-style mascot attribution fields, and OpenClaw/Hermes-style uploaded visual authority sections. [VERIFIED: .planning/phases/48-hermes-source-and-route-contract/48-RESEARCH.md] [VERIFIED: skills/visual-ip-illustrations/references/ips/gopher/source.md] [VERIFIED: skills/visual-ip-illustrations/references/ips/openclaw/source.md]

## Phase Requirements

| ID | Description | Research Support |
|----|-------------|------------------|
| ROUTE-01 | User can select Linux Mascot through explicit aliases while Xiaohei remains omitted-IP default. | Add the exact eight aliases and keep Linux Mascot `default=false`. [VERIFIED: .planning/REQUIREMENTS.md] |
| ROUTE-02 | User can rely on id `linux`, display name `Linux Mascot`, suffix `linux`, and `assets/<article-slug>-linux/`. | Add row, metadata section, output path section, and escaped marker. [VERIFIED: .planning/ROADMAP.md] |
| ROUTE-03 | Maintainer can inspect routing metadata for references, uploaded-image authority, Tux source context, Linux trademark-boundary context, `source-reviewed`, and `default=false`. | Keep `required_references` as `references/ips/linux/source.md` and put source/trademark/uploaded authority in attribution context. [VERIFIED: .planning/REQUIREMENTS.md] |
| SRC-01 | Maintainer can inspect Linux Mascot `source.md` for Larry Ewing attribution, GIMP attribution condition, Linux Foundation trademark guidance, Linux trademark ownership context, uploaded authority, sample policy, review owner, route status, and source-image context. | Use the source record contract below. [VERIFIED: .planning/REQUIREMENTS.md] |
| SRC-02 | User and maintainer can see `/Users/longnv/Downloads/Linux-logo.jpg` and stable uploaded visual markers. | Add a grep-friendly uploaded marker list in `source.md`. [VERIFIED: .planning/REQUIREMENTS.md] |

## Project Constraints From AGENTS.md

- User-facing replies begin with `爸爸`; project planning artifacts, docs, code, comments, commit messages, and PR copy use English for this request. [VERIFIED: AGENTS.md]
- Repository work should go through GSD planning artifacts; this research artifact should avoid production implementation. [VERIFIED: AGENTS.md]
- Keep edits surgical and minimal. [VERIFIED: AGENTS.md]
- Markdown uses compact ATX sections and repository-relative paths. [VERIFIED: AGENTS.md]
- The package remains a lightweight Codex Skill package with Markdown/YAML/reference files and no app framework. [VERIFIED: AGENTS.md]
- Existing `$ian-xiaohei-illustrations` behavior and Xiaohei compatibility remain preserved. [VERIFIED: AGENTS.md]

## Architectural Responsibility Map

| Capability | Primary Tier | Secondary Tier | Rationale |
|------------|--------------|----------------|-----------|
| Linux Mascot route selection contract | Skill reference docs | Skill controller in Phase 55 | `routing.md` is the route metadata authority; `SKILL.md` consumes it later. [VERIFIED: skills/visual-ip-illustrations/references/routing.md] |
| Linux Mascot source authority | Route-local source record | Public docs in Phase 56 | Existing source-reviewed routes keep source/license/uploaded authority under `references/ips/<route>/source.md`. [VERIFIED: skills/visual-ip-illustrations/references/ips/hermes/source.md] |
| Uploaded-image marker contract | Route-local source record | Pack QA in Phase 54 | Phase 53 records identity markers; Phase 54 converts them into style, prompt, edit, and QA behavior. [VERIFIED: .planning/ROADMAP.md] |
| Public sample gate | Source record | Release checklist and validator later | Source records record sample policy before later docs and validation automate the gate. [VERIFIED: skills/visual-ip-illustrations/references/ips/openclaw/source.md] |
| Existing route compatibility | Routing metadata | Validator in Phase 57 | Xiaohei remains the only default route and all non-Linux route references remain isolated. [VERIFIED: skills/visual-ip-illustrations/references/routing.md] |

## Standard Stack

| Surface | Current Standard | Phase 53 Use |
|---------|------------------|--------------|
| Skill package | Markdown Codex Skill files under `skills/visual-ip-illustrations/` | Edit only route/source reference docs during execution. [VERIFIED: AGENTS.md] |
| Route registry | `skills/visual-ip-illustrations/references/routing.md` Markdown route table plus route notes | Append Linux Mascot route and metadata after Hermes Agent. [VERIFIED: skills/visual-ip-illustrations/references/routing.md] |
| Source records | `skills/visual-ip-illustrations/references/ips/<route>/source.md` | Create Linux Mascot `source.md` with source, authority, policy, status, boundary, and review sections. [VERIFIED: skills/visual-ip-illustrations/references/ips/hermes/source.md] |
| Validation | `rg`, `git diff --check`, `node scripts/validate-skill-package.mjs`, `node --test scripts/validate-skill-package.test.mjs` | Use grep/diff as Phase 53 gates; Phase 57 owns validator and Node expansion. [VERIFIED: scripts/validate-skill-package.mjs] |

No package installation is required for Phase 53. Package legitimacy audit is skipped because the phase uses Markdown-only edits and no package manager installs.

## Exact Files To Modify During Execution

| File | Action | Required Markers |
|------|--------|------------------|
| `skills/visual-ip-illustrations/references/routing.md` | Add Linux Mascot route selection bullet, mixed-IP group inclusion, source/route authority bullets, route table row, `## Linux Mascot Metadata`, output paths, and mixed output grouping. | `linux`, `Linux Mascot`, exact aliases, `default=false`, `source-reviewed`, `assets/<article-slug>-linux/`, `assets/&lt;article-slug&gt;-linux/`, `references/ips/linux/source.md`. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] |
| `skills/visual-ip-illustrations/references/ips/linux/source.md` | Create the Linux Mascot source record. | Larry Ewing, GIMP attribution condition, Linux Foundation trademark usage URL, Linux mark URL, Linux registered trademark ownership attribution, `/Users/longnv/Downloads/Linux-logo.jpg`, SHA-256, uploaded visual markers, public sample policy, trademark boundary, distro-logo boundary, review owner, route status, distribution boundary. [VERIFIED: .planning/REQUIREMENTS.md] |

Keep `skills/visual-ip-illustrations/SKILL.md`, README variants, examples, NOTICE, RELEASE_CHECKLIST, `agents/openai.yaml`, validators, tests, public images, and route-local Linux pack files for Phases 54-57. [VERIFIED: .planning/ROADMAP.md]

## Route Metadata Contract

| Field | Value |
|-------|-------|
| id | `linux` [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] |
| display_name | `Linux Mascot` [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] |
| aliases | `Linux Mascot`, `Linux mascot`, `Linux`, `linux`, `Tux`, `tux`, `Linux penguin`, `Tux penguin` [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] |
| default | `false` [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] |
| output_suffix | `linux` [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] |
| required_references | `references/ips/linux/source.md` [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] |
| status | `source-reviewed` [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] |
| raw output path | `assets/<article-slug>-linux/` [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] |
| escaped output marker | `assets/&lt;article-slug&gt;-linux/` [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] |

Recommended route row:

```markdown
| `linux` | Linux Mascot | `Linux Mascot`, `Linux mascot`, `Linux`, `linux`, `Tux`, `tux`, `Linux penguin`, `Tux penguin` | `false` | `linux` | `references/ips/linux/source.md` | Linux Mascot source-reviewed uploaded-image article-illustration route; Tux creator Larry Ewing; GIMP attribution condition; Linux Foundation trademark guidance https://www.linuxfoundation.org/legal/trademark-usage; Linux mark ownership context https://www.linuxfoundation.org/legal/the-linux-mark; uploaded local image `/Users/longnv/Downloads/Linux-logo.jpg` visual authority; public generated Linux Mascot samples require release review; official endorsement, certification, compatibility, Linux Foundation logo use, distro-logo drift, product-poster output, CLI screenshots, web hero graphics, kernel dashboard screenshots, and operating-system marketing graphics stay outside route identity | `source-reviewed` |
```

Source: current `routing.md` table shape and Phase 53 decisions. [VERIFIED: skills/visual-ip-illustrations/references/routing.md] [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]

## Source Record Contract

Create `skills/visual-ip-illustrations/references/ips/linux/source.md` with these sections. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]

| Section | Required Content |
|---------|------------------|
| `## Source` | Character route, display name, source context, route status `source-reviewed`, route id `linux`, `default=false`, output path, source authority path, and uploaded visual authority. [VERIFIED: .planning/REQUIREMENTS.md] |
| `## Tux Source Context` | Tux creator Larry Ewing, Linux 2.0 Penguins URL, GIMP attribution condition, and Tux as an image created by Larry Ewing. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] |
| `## Linux Trademark Context` | Linux Foundation trademark usage URL, Linux mark URL, Linux registered trademark ownership attribution pattern, factual/adjective-style use, and endorsement-safe wording. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] |
| `## Uploaded Image Authority` | `/Users/longnv/Downloads/Linux-logo.jpg`; JPEG metadata; SHA-256 `071bc327e4a2814864f9e2fcdea99aa50482a92ef4e816de9d9ce5f40e17bb2a`; user-provided visual reference status. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] |
| `## Uploaded Linux Mascot Visual Markers` | Glossy black rounded penguin head and body; white face eye patches; large oval eyes with dark pupils and small highlights; yellow-orange beak with two nostril dots; white oval belly; long black flippers; seated rounded posture; oversized yellow-orange webbed feet. [VERIFIED: .planning/REQUIREMENTS.md] |
| `## Source-Image Context` | Uploaded image is source authority; generated article illustrations keep sparse 16:9 article-illustration behavior; Phase 54 turns markers into operational style, prompt, edit, and QA behavior. [VERIFIED: .planning/ROADMAP.md] |
| `## Sample Policy` | Public generated Linux Mascot samples require release review before publication or placement under `examples/images/` or `skills/visual-ip-illustrations/assets/examples/`; internal review samples may use `assets/<article-slug>-linux/` with this source record attached. [VERIFIED: skills/visual-ip-illustrations/references/ips/hermes/source.md] |
| `## Route Status` | Current status `source-reviewed`; status meaning covers Tux attribution, GIMP attribution condition, Linux trademark context, uploaded-image authority, public-sample review boundary, distro-logo boundary, endorsement/certification boundary, and distribution boundary. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] |
| `## Allowed Use` | Document route metadata, Tux attribution, Linux trademark context, uploaded-image authority, internal review, and source-reviewed article-illustration route behavior. [VERIFIED: skills/visual-ip-illustrations/references/ips/gopher/source.md] |
| `## Restricted Use` | Official Linux endorsement, affiliation, sponsorship, approval, certification, compatibility, Linux Foundation campaign framing, Linux Foundation logo use, distro-logo use, distro branding, product advertising, product-poster output, CLI screenshots, web hero graphics, kernel dashboard screenshots, operating-system marketing graphics, generic penguin drift, generic server mascot drift, passive placement, route leakage, excessive text, and copied composition. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] |
| `## Distribution Boundary` | Public package distribution preserves this source record, Tux attribution, GIMP attribution condition, Linux trademark context, uploaded visual authority, sample policy, and `source-reviewed` status until release review changes it. [VERIFIED: skills/visual-ip-illustrations/references/ips/openclaw/source.md] |
| `## Review Owner` | Maintainer / release reviewer; fields include reviewer, date, approval status, Tux source outcome, GIMP attribution outcome, Linux trademark outcome, uploaded-image identity outcome, route isolation outcome, distro-logo boundary outcome, endorsement/certification boundary outcome, allowed directories, channels, and public-sample decision. [VERIFIED: skills/visual-ip-illustrations/references/ips/gopher/source.md] |

## Architecture Patterns

### Recommended Project Structure

```text
skills/visual-ip-illustrations/
└── references/
    ├── routing.md
    └── ips/
        └── linux/
            └── source.md
```

This matches the route-local source pattern used by Hermes, Go Gopher, and OpenClaw. [VERIFIED: skills/visual-ip-illustrations/references/ips/hermes/source.md] [VERIFIED: skills/visual-ip-illustrations/references/ips/gopher/source.md] [VERIFIED: skills/visual-ip-illustrations/references/ips/openclaw/source.md]

### Pattern 1: Route-First Source Contract

**What:** Add the route row and source record before adding pack files or controller behavior. [VERIFIED: .planning/phases/48-hermes-source-and-route-contract/48-01-SUMMARY.md]

**When to use:** Use this for new visual IPs that need source, uploaded-image, license, trademark, or likeness boundaries before runtime dispatch. [VERIFIED: .planning/ROADMAP.md]

### Pattern 2: Source Record As Grep-Friendly Authority

**What:** Use short Markdown sections with exact marker strings for source, status, visual markers, policy, distribution, and review ownership. [VERIFIED: skills/visual-ip-illustrations/references/ips/hermes/source.md]

**When to use:** Use this when later validators need deterministic token checks. [VERIFIED: scripts/validate-skill-package.mjs]

## Don't Hand-Roll

| Problem | Use Instead | Why |
|---------|-------------|-----|
| New manifest format | Existing `routing.md` table plus route-local `source.md` | Future route manifests are deferred. [VERIFIED: .planning/REQUIREMENTS.md] |
| Broad alias matching | Exact eight Linux Mascot aliases | Phase 53 alias boundary is locked. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] |
| Full Linux Mascot pack | Phase 54 route-local pack | Phase 53 creates only `source.md`. [VERIFIED: .planning/ROADMAP.md] |
| Runtime controller dispatch | Phase 55 `SKILL.md` integration | Phase 53 only records route/source metadata. [VERIFIED: .planning/ROADMAP.md] |
| Public docs and release surfaces | Phase 56 docs/release work | README, NOTICE, examples, metadata, and release checklist are later-phase scope. [VERIFIED: .planning/ROADMAP.md] |
| Validator overhaul | Phase 57 validation hardening | Current validator is calibrated to shipped routes; Linux changes need planned expansion after route, pack, controller, and docs exist. [VERIFIED: scripts/validate-skill-package.mjs] [VERIFIED: .planning/ROADMAP.md] |

## Common Pitfalls

| Pitfall | What Goes Wrong | Control |
|---------|-----------------|---------|
| Default-route drift | Omitted visual-IP requests stop mapping solely to Xiaohei. [VERIFIED: skills/visual-ip-illustrations/references/routing.md] | Keep only Xiaohei `default=true`; add Linux Mascot with `default=false`; manually inspect route table. |
| Alias overreach | Generic Linux, penguin, OS, terminal, or mascot terms select Linux Mascot accidentally. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] | Use only the exact eight aliases in Phase 53. |
| Trademark drift | Route copy implies official Linux endorsement, certification, compatibility, or Linux Foundation campaign framing. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] | Put factual source/trademark context and restricted-use markers in route and source records. |
| Distro/logo drift | Generated route becomes a distro logo pack or Linux Foundation logo route. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] | Record distro-logo and Linux Foundation logo use as restricted-use markers. |
| Product-poster drift | Route becomes OS marketing, kernel dashboard, CLI screenshot, or web hero output. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] | Record article-illustration-only, product-poster, CLI screenshot, kernel dashboard, and web hero boundaries in source and routing. |
| Source dependency leak | The uploaded local path becomes a generated asset output target or public package dependency. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] | Name `/Users/longnv/Downloads/Linux-logo.jpg` as user-provided visual authority and keep generated outputs under `assets/<article-slug>-linux/`. |
| Validator scope creep | Phase 53 tries to update all checks before docs/controller/pack exist. [VERIFIED: .planning/ROADMAP.md] | Use grep/diff gates now; leave validator and Node expansion to Phase 57. |

## Verification Commands

Phase 53 execution should run these focused checks after implementation:

```bash
rg -n 'Linux Mascot|Linux mascot|Tux penguin|source-reviewed|assets/<article-slug>-linux/|assets/&lt;article-slug&gt;-linux/|references/ips/linux/source\.md' \
  skills/visual-ip-illustrations/references/routing.md \
  skills/visual-ip-illustrations/references/ips/linux/source.md
```

```bash
rg -n 'Larry Ewing|The GIMP|https://isc\.tamu\.edu/~lewing/linux/|https://www\.linuxfoundation\.org/legal/trademark-usage|https://www\.linuxfoundation\.org/legal/the-linux-mark|Linux is the registered trademark of Linus Torvalds in the U\.S\. and other countries|/Users/longnv/Downloads/Linux-logo\.jpg|071bc327e4a2814864f9e2fcdea99aa50482a92ef4e816de9d9ce5f40e17bb2a' \
  skills/visual-ip-illustrations/references/ips/linux/source.md
```

```bash
rg -n 'glossy black rounded penguin head and body|white face eye patches|large oval eyes with dark pupils and small highlights|yellow-orange beak with two nostril dots|white oval belly|long black flippers|seated rounded posture|oversized yellow-orange webbed feet|public generated Linux Mascot samples require release review|official endorsement|certification|compatibility|Linux Foundation logo use|distro-logo|kernel dashboard screenshots|operating-system marketing graphics' \
  skills/visual-ip-illustrations/references/ips/linux/source.md
```

```bash
git diff --check -- \
  skills/visual-ip-illustrations/references/routing.md \
  skills/visual-ip-illustrations/references/ips/linux/source.md \
  .planning/phases/53-linux-mascot-source-and-route-contract/53-01-SUMMARY.md
```

Manual route inspection should show this order after implementation:

```text
xiaohei:Xiaohei:true:illustrations:active
littlebox:Littlebox:false:littlebox:active
tom:Tom:false:tom:gated-authorized
ferris:Ferris:false:ferris:source-reviewed
seal:Seal:false:seal:active
openclaw:OpenClaw:false:openclaw:source-reviewed
gopher:Go Gopher:false:gopher:source-reviewed
caixukun:Cai Xukun:false:caixukun:gated-public-figure
hermes:Hermes Agent:false:hermes:source-reviewed
linux:Linux Mascot:false:linux:source-reviewed
```

The current full validator and Node suite are Phase 57-owned for Linux Mascot expansion. Phase 53 should treat targeted route/source checks and `git diff --check` as the execution gate. [VERIFIED: .planning/ROADMAP.md]

## Environment Availability

| Dependency | Required By | Available | Fallback |
|------------|-------------|-----------|----------|
| `rg` | Marker verification | yes | `grep -R` |
| `git` | Diff hygiene | yes | manual whitespace review |
| Node.js | Existing validator/tests and GSD tools | yes | focused grep/diff for Phase 53 |

No external package, database, service, hosted runtime, or web lookup is required for Phase 53.

## Security Domain

| ASVS Category | Applies | Standard Control |
|---------------|---------|------------------|
| V2 Authentication | no | No auth surface in this documentation-only phase. [VERIFIED: .planning/PROJECT.md] |
| V3 Session Management | no | No session runtime exists. [VERIFIED: .planning/PROJECT.md] |
| V4 Access Control | no | File-based skill package only. [VERIFIED: .planning/PROJECT.md] |
| V5 Input Validation | yes | Exact alias set and route-local source/trademark constraints in `routing.md` and `source.md`. [VERIFIED: skills/visual-ip-illustrations/references/routing.md] |
| V6 Cryptography | no | No crypto surface in this phase. [VERIFIED: .planning/PROJECT.md] |

## Assumptions Log

| # | Claim | Section | Risk If Wrong |
|---|-------|---------|---------------|
| A1 | The provided source URLs in `53-CONTEXT.md` are sufficient for planning; release-time source availability can be rechecked in Phase 57. | Sources | If a URL changes before release, Phase 57 should update source evidence and validator expectations. [ASSUMED] |
| A2 | Phase 53 should avoid copying `/Users/longnv/Downloads/Linux-logo.jpg` into the repository. | Source Record Contract | Future asset hashing requirements may request a package-visible source image. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md] |

## Sources

### Primary

- `.planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md` - locked decisions, scope, aliases, source URLs, uploaded-image authority, boundaries, deferred phases. [VERIFIED: filesystem read]
- `.planning/REQUIREMENTS.md` - ROUTE-01, ROUTE-02, ROUTE-03, SRC-01, SRC-02. [VERIFIED: filesystem read]
- `.planning/ROADMAP.md` - Phase 53-57 boundaries and success criteria. [VERIFIED: filesystem read]
- `skills/visual-ip-illustrations/references/routing.md` - current route table, route order, metadata pattern, output path pattern. [VERIFIED: filesystem read]
- `skills/visual-ip-illustrations/references/ips/hermes/source.md` - uploaded-image source-reviewed route precedent. [VERIFIED: filesystem read]
- `skills/visual-ip-illustrations/references/ips/gopher/source.md` - mascot attribution and source-record precedent. [VERIFIED: filesystem read]
- `skills/visual-ip-illustrations/references/ips/openclaw/source.md` - uploaded authority and public-sample source-record precedent. [VERIFIED: filesystem read]
- `.planning/phases/48-hermes-source-and-route-contract/48-01-PLAN.md`, `48-01-SUMMARY.md`, and `48-RESEARCH.md` - analogous route/source-only plan, execution summary, and research artifact. [VERIFIED: filesystem read]

### Secondary

- `scripts/validate-skill-package.mjs` - current dependency-free validator surface and later-phase expansion target. [VERIFIED: filesystem read and CodeGraph]
- `.planning/STATE.md` - v1.11 state, prior milestone context, and current Phase 53 focus. [VERIFIED: filesystem read]
- AGENTS.md - repo constraints, language policy, and GSD workflow conventions. [VERIFIED: filesystem read]

## Metadata

**Confidence breakdown:**

- Route/source scope: HIGH - Phase 53 decisions and requirements are explicit. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- Architecture: HIGH - existing route/source patterns are implemented for Hermes, Go Gopher, and OpenClaw. [VERIFIED: skills/visual-ip-illustrations/references/ips/hermes/source.md] [VERIFIED: skills/visual-ip-illustrations/references/ips/gopher/source.md] [VERIFIED: skills/visual-ip-illustrations/references/ips/openclaw/source.md]
- Source/trademark context: MEDIUM-HIGH - the planning context contains canonical source URLs and exact source/trademark requirements; Phase 57 can recheck availability during release validation. [VERIFIED: .planning/phases/53-linux-mascot-source-and-route-contract/53-CONTEXT.md]
- Validation: HIGH for targeted Phase 53 checks, MEDIUM for post-Phase-53 full-suite expectation because Phase 57 owns Linux Mascot validator expansion. [VERIFIED: .planning/ROADMAP.md]

**Research date:** 2026-07-01
**Valid until:** 2026-08-01 for local route/source patterns; recheck external source URLs during release validation.

## RESEARCH COMPLETE
