# Phase 50: Hermes Skill Controller Integration - Research

**Researched:** 2026-06-18 [VERIFIED: system date]
**Domain:** Documentation-driven Codex Skill runtime controller integration for a Visual IP route [VERIFIED: AGENTS.md]
**Confidence:** HIGH [VERIFIED: repo grep]

<user_constraints>
## User Constraints (from CONTEXT.md)

### Locked Decisions

## Implementation Decisions

### Scope Ownership

- **D-01:** Phase 50 owns runtime controller behavior in `skills/visual-ip-illustrations/SKILL.md`.
- **D-02:** Phase 50 owns the agent metadata slice required by RUN-04 in `skills/visual-ip-illustrations/agents/openai.yaml` because RUN-04 explicitly names agent metadata for Hermes.
- **D-03:** Preserve all existing route behavior for omitted-IP Xiaohei and explicit Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, and Cai Xukun.
- **D-04:** Public docs and validation remain deferred to Phases 51 and 52.

### RUN-01 Decisions

- **D-05:** Add Hermes Agent to `SKILL.md` frontmatter description, Visual IP Routes, Reference Loading, Select the Visual IP Route, shot-list fields, generation context, edit routing, QA dispatch, save paths, and delivery reporting.
- **D-06:** Hermes route selection must use aliases `Hermes Agent`, `Hermes`, `hermes`, `hermes-agent`, `Hermes logo`, and `Hermes Agent logo`; broad assistant, AI agent, logo, anime, monochrome girl, fashion figure, Greek messenger, winged sandals, and caduceus terms remain outside Hermes route selection.
- **D-07:** Hermes progressive loading must point to the Phase 49 seven-file pack: `index.md`, `source.md`, `style-dna.md`, `hermes-ip.md`, `composition-patterns.md`, `prompt-template.md`, and `qa-checklist.md`.
- **D-08:** Hermes runtime wording must carry uploaded-image authority, official source context, MIT license context, source context note, mythology-drift boundary, product-poster boundary, public sample review boundary, route isolation, and source pointer `references/ips/hermes/source.md`.

### RUN-02 Decisions

- **D-09:** Mixed-IP workflows must add Hermes Agent as a separate route group alongside Xiaohei, Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, and Cai Xukun.
- **D-10:** Each mixed-IP group must load only its own required references, use its own prompt template, QA checklist, edit gates, route note, output suffix, and output directory.
- **D-11:** Hermes mixed-IP groups must write to `assets/<article-slug>-hermes/` and include route status `source-reviewed`, source pointer, uploaded-image authority status, source-context note, mythology-drift boundary status, product-poster boundary status, public sample review boundary, and route isolation status.

### RUN-03 Decisions

- **D-12:** Hermes delivery reports must include selected visual IP, image count, purpose per image, saved path under `assets/<article-slug>-hermes/`, uploaded-image authority note, source-context note, route status `source-reviewed`, source pointer `references/ips/hermes/source.md`, public sample review boundary when relevant, and route stability notes.
- **D-13:** The route-leakage delivery guard must include Hermes and require source-reviewed status, source pointer, uploaded-image authority note, route-local QA, original article-metaphor status, mythology-drift boundary, product-poster boundary, public sample review boundary, route isolation status, and `assets/<article-slug>-hermes/`.

### RUN-04 Decisions

- **D-14:** `SKILL.md` must present Hermes Agent as a selectable source-reviewed uploaded-image route while preserving Visual IP Illustrations identity, canonical `$visual-ip-illustrations`, and legacy `$ian-xiaohei-illustrations` compatibility alias.
- **D-15:** `agents/openai.yaml` must add Hermes Agent to display name, short description, and default prompt without removing existing route descriptions.

### the agent's Discretion

- The planner may choose exact `SKILL.md` paragraph placement by following the Cai Xukun, Go Gopher, and OpenClaw route-specific pattern.
- The planner may keep Hermes runtime text compact because detailed style, prompt, edit, and QA rules live in `references/ips/hermes/`.
- The planner should use targeted `rg` checks and `git diff --check` as Phase 50 acceptance proof; full validator and Node tests remain Phase 52.

### Deferred Ideas (OUT OF SCOPE)

- README variants, `examples/prompts.md`, NOTICE, release checklist, public release copy, and public sample surfaces. Phase 51 owns these.
- Validator hardening, Node regression tests, smoke prompts, leakage fixtures, public sample gates, and final release evidence. Phase 52 owns these.
- Generated Hermes images or public sample assets.
</user_constraints>

<phase_requirements>
## Phase Requirements

| ID | Description | Research Support |
|----|-------------|------------------|
| RUN-01 | User can invoke Hermes through the skill controller, route selection rules, progressive reference loading, planning fields, generation dispatch, edit routing, QA dispatch, and delivery reports. [VERIFIED: .planning/REQUIREMENTS.md] | Add Hermes to every `SKILL.md` controller surface listed in the Implementation Surface table. [VERIFIED: SKILL.md grep] |
| RUN-02 | User can request mixed-IP output where Hermes and all existing routes create separate route groups with their own references, prompts, QA rules, and output paths. [VERIFIED: .planning/REQUIREMENTS.md] | Extend mixed-IP shot-list, generation, save, and delivery blocks with a Hermes group using only `references/ips/hermes/`. [VERIFIED: SKILL.md grep; routing.md] |
| RUN-03 | User receives Hermes delivery reports with selected visual IP, image count, purpose per image, saved path under `assets/<article-slug>-hermes/`, uploaded-image authority note, source-context note, and route stability notes. [VERIFIED: .planning/REQUIREMENTS.md] | Add single-route and mixed-route Hermes delivery blocks plus the delivery guard fields from `prompt-template.md`. [VERIFIED: prompt-template.md] |
| RUN-04 | Agent metadata and skill instructions present Hermes as a selectable source-reviewed route while preserving Visual IP Illustrations identity and the legacy `$ian-xiaohei-illustrations` alias. [VERIFIED: .planning/REQUIREMENTS.md] | Update `SKILL.md` route copy and `agents/openai.yaml` display/short/default prompt strings while retaining existing identity text. [VERIFIED: CONTEXT.md; openai.yaml] |
</phase_requirements>

## Summary

Phase 50 is a surgical controller-integration phase. `routing.md` already defines the `hermes` route, aliases, `default=false`, `output_suffix: hermes`, output path, escaped marker, source-reviewed status, and all seven required references. [VERIFIED: routing.md] Phase 49 already created the Hermes seven-file route-local pack and verified planning, prompt, edit, QA, output path, public sample boundary, mythology-drift boundary, and product-poster boundary behavior. [VERIFIED: 49-VERIFICATION.md]

The runtime gap is in `skills/visual-ip-illustrations/SKILL.md` and `skills/visual-ip-illustrations/agents/openai.yaml`. [VERIFIED: repo grep] `SKILL.md` currently has full route-controller parity through Cai Xukun, while Hermes appears only in `routing.md` and `references/ips/hermes/`. [VERIFIED: SKILL.md grep; routing.md grep] `agents/openai.yaml` currently lists routes through Cai Xukun and has no Hermes metadata. [VERIFIED: openai.yaml]

**Primary recommendation:** Implement one plan that updates only `SKILL.md` and `agents/openai.yaml`, mirroring the Cai Xukun and Go Gopher controller pattern with Hermes-specific source-reviewed uploaded-image wording. [VERIFIED: CONTEXT.md; SKILL.md]

## Architectural Responsibility Map

| Capability | Primary Tier | Secondary Tier | Rationale |
|------------|-------------|----------------|-----------|
| Route selection for Hermes aliases | Skill runtime controller | Route metadata reference | `SKILL.md` is the runtime controller, while `routing.md` is the canonical route metadata source. [VERIFIED: AGENTS.md; routing.md] |
| Progressive reference loading | Skill runtime controller | Hermes route pack | `SKILL.md` instructs agents to read `routing.md` first and load selected-route references. [VERIFIED: SKILL.md] |
| Hermes planning/generation/edit/QA dispatch | Skill runtime controller | Hermes route-local pack | `SKILL.md` owns dispatch text; `references/ips/hermes/*.md` owns detailed prompt, edit, composition, and QA rules. [VERIFIED: SKILL.md; prompt-template.md; qa-checklist.md] |
| Agent discovery metadata | Agent metadata YAML | Skill runtime controller | `agents/openai.yaml` exposes display name, short description, default prompt, and implicit invocation policy. [VERIFIED: AGENTS.md; openai.yaml] |
| Generated asset persistence | Workspace filesystem | Route metadata | Output paths are route-derived `assets/<article-slug>-<suffix>/` paths with `hermes` already defined in `routing.md`. [VERIFIED: routing.md] |

## Project Constraints (from AGENTS.md)

- Every user-facing reply must begin with `爸爸`; assistant replies must use Simplified Chinese. [VERIFIED: AGENTS.md]
- Code, code comments, commit messages, and PR copy stay English. [VERIFIED: AGENTS.md]
- Before source edits, work should run through GSD; this research file is a planning artifact requested directly by the user, and source files must remain untouched in this turn. [VERIFIED: AGENTS.md; user request]
- Preserve Codex Skill compatibility through Markdown `SKILL.md`, local reference files, and `agents/openai.yaml`. [VERIFIED: AGENTS.md]
- Existing `$ian-xiaohei-illustrations` behavior and documented Xiaohei prompts must keep working. [VERIFIED: AGENTS.md]
- IP rules must remain separately readable, testable, and routable. [VERIFIED: AGENTS.md]
- The package remains lightweight; no app framework or build runtime should be introduced. [VERIFIED: AGENTS.md]
- Final image generation depends on the host `image_gen` capability. [VERIFIED: AGENTS.md]
- Markdown style uses ATX headings, compact sections, short bullets, and fenced code blocks with language hints. [VERIFIED: AGENTS.md]
- `SKILL.md` is the central controller and reference files load progressively on demand. [VERIFIED: AGENTS.md]

## Standard Stack

### Core

| Library | Version | Purpose | Why Standard |
|---------|---------|---------|--------------|
| Markdown files | repository-native | Runtime skill instructions, route packs, prompt templates, QA rules | The installable skill is documentation-driven. [VERIFIED: AGENTS.md] |
| YAML metadata | repository-native | Agent discovery metadata in `agents/openai.yaml` | The OpenAI agent metadata file defines display and default prompt fields. [VERIFIED: AGENTS.md; openai.yaml] |
| Node.js | v24.13.0 | Optional local validation runner for existing scripts | Node is available in the environment; Phase 52 owns full validator repair. [VERIFIED: command output] |
| ripgrep | 15.1.0 | Targeted verification over Markdown/YAML surfaces | Phase 50 context explicitly recommends targeted `rg` checks. [VERIFIED: command output; CONTEXT.md] |
| Git | 2.50.1 | Diff hygiene with `git diff --check` | Phase 50 verification target includes `git diff --check`. [VERIFIED: command output; CONTEXT.md] |

### Supporting

| Library | Version | Purpose | When to Use |
|---------|---------|---------|-------------|
| `scripts/validate-skill-package.mjs` | repository script | Full package validation | Defer green-gate ownership to Phase 52; use only as optional diagnostic if the planner wants to record known baseline debt. [VERIFIED: 49-VERIFICATION.md; CONTEXT.md] |
| `scripts/validate-skill-package.test.mjs` | repository script | Node regression suite | Defer green-gate ownership to Phase 52. [VERIFIED: 49-VERIFICATION.md; CONTEXT.md] |

### Alternatives Considered

| Instead of | Could Use | Tradeoff |
|------------|-----------|----------|
| Manual `SKILL.md` route-controller edit | Generated route manifest | Manifest generation is a future idea in prior phases; current architecture is Markdown-driven. [VERIFIED: Phase 40 context; AGENTS.md] |
| Targeted grep verification | Full validator repair | Full validator and Node repair are explicitly deferred to Phase 52. [VERIFIED: CONTEXT.md] |
| Runtime controller only | Runtime controller plus `agents/openai.yaml` | Phase 50 owns `agents/openai.yaml` because RUN-04 names agent metadata. [VERIFIED: CONTEXT.md] |

**Installation:** No external package installation is required. [VERIFIED: AGENTS.md]

## Package Legitimacy Audit

No external package will be installed for Phase 50. [VERIFIED: CONTEXT.md; AGENTS.md]

| Package | Registry | Age | Downloads | Source Repo | slopcheck | Disposition |
|---------|----------|-----|-----------|-------------|-----------|-------------|
| none | none | none | none | none | not run | No install surface. [VERIFIED: repo files] |

**Packages removed due to slopcheck [SLOP] verdict:** none. [VERIFIED: no packages]
**Packages flagged as suspicious [SUS]:** none. [VERIFIED: no packages]

## Architecture Patterns

### System Architecture Diagram

```text
User prompt
  |
  v
SKILL.md route selection
  |-- omitted IP ---------------------> xiaohei route
  |-- Hermes aliases -----------------> hermes route
  |-- existing explicit aliases ------> existing route groups
  |
  v
Read references/routing.md
  |
  v
Selected route required_references
  |
  v
Route-local pack under references/ips/hermes/
  |-- prompt-template.md -> planning, generation, edit gates
  |-- composition-patterns.md -> metaphor/action patterns
  |-- qa-checklist.md -> QA and repair judgment
  |-- source.md -> source, MIT, uploaded-image, sample boundaries
  |
  v
One image-generation call per image
  |
  v
Route-local QA / repair loop
  |
  v
Save accepted output to assets/<article-slug>-hermes/
  |
  v
Delivery report with selected IP, count, purposes, path, source context, authority, boundaries, and stability notes
```

### Recommended Project Structure

```text
skills/visual-ip-illustrations/
├── SKILL.md                     # runtime controller surface to update [VERIFIED: repo]
├── agents/openai.yaml           # metadata surface to update [VERIFIED: repo]
└── references/
    ├── routing.md               # existing Hermes route metadata source [VERIFIED: repo]
    └── ips/hermes/              # existing seven-file Hermes pack [VERIFIED: repo]
```

### Pattern 1: Route-Local Controller Parity

**What:** Every explicit route appears in `SKILL.md` route overview, reference loading, selection, planning, generation/edit, QA, save, mixed-IP, and delivery sections. [VERIFIED: SKILL.md]

**When to use:** Add Hermes wherever Cai Xukun, Go Gopher, and OpenClaw already have runtime controller surfaces. [VERIFIED: SKILL.md; 45-CONTEXT.md; 40-CONTEXT.md; 35-CONTEXT.md]

**Example:**

```markdown
Hermes Agent loads only Hermes Agent `required_references`, uses `references/ips/hermes/prompt-template.md` plus `references/ips/hermes/composition-patterns.md`, then checks output with `references/ips/hermes/qa-checklist.md`. [VERIFIED: prompt-template.md; qa-checklist.md]
```

### Pattern 2: Compact Controller, Detailed Route Pack

**What:** Keep `SKILL.md` compact and route-dispatch oriented; rely on `references/ips/hermes/` for detailed prompt, edit, QA, and style rules. [VERIFIED: CONTEXT.md; SKILL.md]

**When to use:** Use short Hermes bullets in `SKILL.md` that name required status, source pointer, uploaded-image authority, route boundaries, output path, and dispatch files. [VERIFIED: CONTEXT.md]

### Pattern 3: Mixed-IP Separate Route Groups

**What:** Mixed-IP requests state one shared core idea, then split into independent route groups with separate references, prompt templates, QA, edit gates, suffixes, and output directories. [VERIFIED: SKILL.md]

**When to use:** Add Hermes to every mixed-IP list after Cai Xukun or at the end of current route ordering. [VERIFIED: SKILL.md]

### Anti-Patterns to Avoid

- **Editing public docs in Phase 50:** README variants, examples, NOTICE, release checklist, public release copy, and samples are Phase 51-owned. [VERIFIED: CONTEXT.md]
- **Repairing full validator baselines in Phase 50:** validator hardening and Node regression expansion are Phase 52-owned. [VERIFIED: CONTEXT.md]
- **Making Hermes a generic assistant route:** Hermes route matching is limited to the six explicit aliases, while broad assistant, AI agent, logo, anime, monochrome girl, fashion figure, Greek messenger, winged sandals, and caduceus terms stay outside the Hermes alias set. [VERIFIED: CONTEXT.md; routing.md]
- **Product-poster or mythology drift:** Hermes output is a sparse article-illustration route, with product-poster output and mythological Hermes imagery treated as route failures. [VERIFIED: prompt-template.md; qa-checklist.md]

## Implementation Surface

| Surface | Current State | Required Phase 50 Edit |
|---------|---------------|------------------------|
| `SKILL.md` frontmatter description, current line 3 | Explicit routes end at Cai Xukun. [VERIFIED: nl SKILL.md] | Add Hermes Agent to the explicit route list while preserving existing route names and Xiaohei default wording. [VERIFIED: CONTEXT.md] |
| `## Visual IP Routes`, current lines 25-51 | Route overview includes Cai Xukun as the newest explicit route. [VERIFIED: nl SKILL.md] | Insert Hermes Agent route overview after Cai Xukun: route id `hermes`, display name Hermes Agent, `default=false`, `output_suffix: hermes`, `source-reviewed`, source pointer, uploaded-image authority, official source context, MIT license context, public sample boundary, mythology/product boundaries, and `assets/<article-slug>-hermes/`. [VERIFIED: routing.md; source.md] |
| `## Reference Loading`, current lines 53-114 | Hermes seven references are absent. [VERIFIED: nl SKILL.md] | Add `index.md`, `source.md`, `style-dna.md`, `hermes-ip.md`, `composition-patterns.md`, `prompt-template.md`, and `qa-checklist.md` with compact responsibilities. [VERIFIED: routing.md; 49-VERIFICATION.md] |
| `### 1. Select the Visual IP Route`, current lines 118-150 | Hermes selection, output path, and required references are absent. [VERIFIED: nl SKILL.md] | Add alias rule, exclusion rule, mixed-IP list membership, output path rule, required references rule, and route-local loading rule for Hermes. [VERIFIED: CONTEXT.md; routing.md] |
| `### 3. Plan the Shot List First`, current lines 163-284 | Hermes shot-list fields are absent. [VERIFIED: nl SKILL.md] | Add Hermes planning fields from `prompt-template.md`: Placement, Core idea, Structure type, Hermes Agent state/action, Supporting objects, Visible labels, Source context note, Mythology-drift note, Product-poster boundary note, Output path. [VERIFIED: prompt-template.md] |
| Mixed-IP shot-list list, current lines 273-282 | Route groups end at Cai Xukun. [VERIFIED: nl SKILL.md] | Add Hermes variant group with required references, prompt/composition/QA/edit paths, output suffix, route status, source pointer, uploaded-image authority, source-context note, mythology/product boundary status, public sample review boundary, and route isolation status. [VERIFIED: CONTEXT.md; prompt-template.md] |
| `### 4. Generate One Image at a Time`, current lines 286-432 | Hermes generation and edit dispatch are absent. [VERIFIED: nl SKILL.md] | Add Hermes generation context using `prompt-template.md`, `composition-patterns.md`, and `qa-checklist.md`; add prompt marker bullets and edit behavior with all Hermes edit gate names. [VERIFIED: prompt-template.md; composition-patterns.md; qa-checklist.md] |
| Mixed-IP generation sentence, current line 432 | Route loading list ends at Cai Xukun. [VERIFIED: nl SKILL.md] | Add Hermes to route loading list and add Hermes-specific mixed generation sentence with `assets/<article-slug>-hermes/`. [VERIFIED: CONTEXT.md] |
| `### 5. QA and Iteration`, current line 436 | QA dispatch sentence lacks Hermes. [VERIFIED: nl SKILL.md] | Add Hermes QA dispatch to `references/ips/hermes/qa-checklist.md`. [VERIFIED: qa-checklist.md] |
| High-risk failure lists, current lines 438-593 | Hermes failure list is absent. [VERIFIED: nl SKILL.md] | Add Hermes high-risk failures: generic anime or assistant drift, mythological Hermes imagery, missing headset, missing bob-hair highlight silhouette, missing black sleeveless dress, missing collar tag, missing stockings/platform heels, product-poster drift, passive placement, route leakage, excessive text, copied composition, official endorsement/affiliation/sponsorship/approval/impersonation, and missing output/source markers. [VERIFIED: qa-checklist.md] |
| Repair paragraph, current line 595 | Hermes repair routing is absent. [VERIFIED: nl SKILL.md] | Add Hermes repair behavior using `references/ips/hermes/prompt-template.md` gates: Stronger Hermes Participation, Uploaded-Image Identity Repair, Title Removal, Text Reduction, Mythology-Drift Repair, Product-Poster Repair, Route Leakage Repair, Unaffected-Content Preservation. [VERIFIED: prompt-template.md] |
| `### 6. Save and Deliver`, current lines 601-633 | Hermes output path and escaped marker are absent. [VERIFIED: nl SKILL.md] | Add raw path, output suffix mapping, escaped marker, filename sentence, and mixed-IP output directory for Hermes. [VERIFIED: routing.md] |
| `## Output Contract`, current lines 637-660 | Hermes delivery block and guard are absent. [VERIFIED: nl SKILL.md] | Add single-route Hermes delivery rule, mixed-IP Hermes block, and Hermes route-leakage guard. [VERIFIED: CONTEXT.md; prompt-template.md] |
| `agents/openai.yaml`, current lines 2-4 | Metadata route list ends at Cai Xukun. [VERIFIED: nl openai.yaml] | Add Hermes Agent to display name, short description, and default prompt with aliases, status, output path, escaped marker, source pointer, uploaded-image authority, source/MIT context, mythology/product boundaries, public sample gate, and route isolation. [VERIFIED: CONTEXT.md; routing.md] |

## Don't Hand-Roll

| Problem | Don't Build | Use Instead | Why |
|---------|-------------|-------------|-----|
| Route truth | A second Hermes route table inside `SKILL.md` | Existing `references/routing.md` row | `routing.md` already stores aliases, default flag, output suffix, references, attribution, status, output paths, and mixed-IP behavior. [VERIFIED: routing.md] |
| Hermes prompt/edit/QA rules | New prompt wording from scratch | `references/ips/hermes/prompt-template.md`, `composition-patterns.md`, `qa-checklist.md` | Phase 49 verified those files for planning, generation, edits, QA, and delivery judgment. [VERIFIED: 49-VERIFICATION.md] |
| Validation framework | New test runner or package | Targeted `rg` plus `git diff --check` | Phase 50 context assigns full validator/Node hardening to Phase 52. [VERIFIED: CONTEXT.md] |
| Public samples | Generated image assets | No generated samples in Phase 50 | Public generated Hermes samples require release review. [VERIFIED: source.md] |

**Key insight:** Phase 50 should consume the Hermes route and pack contracts, then expose them through the two runtime surfaces. [VERIFIED: CONTEXT.md]

## Common Pitfalls

### Pitfall 1: Missing One Controller Surface

**What goes wrong:** Hermes is selectable but planning, QA, save, or delivery still lacks Hermes behavior. [VERIFIED: Phase 35/40/45 summaries]
**Why it happens:** `SKILL.md` repeats route-specific text across many sections. [VERIFIED: SKILL.md]
**How to avoid:** Patch by section using the Implementation Surface table and verify with grouped `rg` commands. [VERIFIED: CONTEXT.md]
**Warning signs:** Hermes appears in route selection but is absent from `Active route paths`, `Output Contract`, or QA dispatch. [VERIFIED: SKILL.md]

### Pitfall 2: Metadata Scope Creep

**What goes wrong:** Phase 50 expands README, examples, NOTICE, release checklist, validators, or public samples. [VERIFIED: CONTEXT.md]
**Why it happens:** Prior phases sometimes defer metadata to public-doc phases, while Phase 50 has a narrow RUN-04 metadata exception for `agents/openai.yaml`. [VERIFIED: 45-CONTEXT.md; 50-CONTEXT.md]
**How to avoid:** Limit production edits to `SKILL.md` and `agents/openai.yaml`. [VERIFIED: CONTEXT.md]
**Warning signs:** `git status --short` shows README, examples, NOTICE, release checklist, validator scripts, test files, or generated assets after implementation. [VERIFIED: CONTEXT.md]

### Pitfall 3: Mythology and Product Drift

**What goes wrong:** Runtime prompts treat Hermes as Greek-myth Hermes or as product marketing material. [VERIFIED: prompt-template.md; qa-checklist.md]
**Why it happens:** The route name has mythology ambiguity and official product source context. [VERIFIED: routing.md; source.md]
**How to avoid:** Include mythology-drift and product-poster boundary notes in planning, generation, edit, QA, and delivery guard surfaces. [VERIFIED: CONTEXT.md]
**Warning signs:** Runtime text mentions winged sandals, winged helmet, caduceus, web hero graphics, CLI screenshots, or official endorsement as positive route behavior. [VERIFIED: prompt-template.md]

### Pitfall 4: Output Path Drift

**What goes wrong:** Hermes delivery saves under a wrong directory or lacks the escaped validation marker. [VERIFIED: routing.md]
**Why it happens:** `SKILL.md` has raw path, output suffix, validation marker, accepted filename, mixed-IP, and delivery contract sections. [VERIFIED: SKILL.md]
**How to avoid:** Add both `assets/<article-slug>-hermes/` and `assets/&lt;article-slug&gt;-hermes/` wherever peer route path markers appear. [VERIFIED: routing.md]
**Warning signs:** `rg` finds only raw path or only escaped marker. [VERIFIED: routing.md]

## Code Examples

### Hermes Shot-List Controller Block

```markdown
Hermes Agent shot-list entries use `references/ips/hermes/prompt-template.md` and include:

- Placement
- Core idea
- Structure type
- Hermes Agent state
- Hermes Agent action
- Supporting objects
- Visible labels
- Source context note
- Mythology-drift note
- Product-poster boundary note
- Output path: `assets/<article-slug>-hermes/`
```

Source: `skills/visual-ip-illustrations/references/ips/hermes/prompt-template.md` lines 15-39. [VERIFIED: prompt-template.md]

### Hermes Generation Dispatch Block

```markdown
Hermes Agent loads only Hermes Agent `required_references`, uses `references/ips/hermes/prompt-template.md` plus `references/ips/hermes/composition-patterns.md`, then checks output with `references/ips/hermes/qa-checklist.md`.
```

Source: mirrors current Go Gopher/Cai Xukun controller dispatch and Hermes pack file responsibilities. [VERIFIED: SKILL.md; prompt-template.md; composition-patterns.md; qa-checklist.md]

### Hermes Delivery Block

```markdown
- Hermes Agent block: selected IP `Hermes Agent`, shared core idea, image purposes, save path `assets/<article-slug>-hermes/`, route status `source-reviewed`, source context note, MIT license context, source pointer `references/ips/hermes/source.md`, uploaded-image identity status, mythology-drift boundary status, product-poster boundary status, public sample review boundary when relevant, route isolation status, stability notes
```

Source: `prompt-template.md` output reminder and Phase 50 D-12/D-13. [VERIFIED: prompt-template.md; CONTEXT.md]

## State of the Art

| Old Approach | Current Approach | When Changed | Impact |
|--------------|------------------|--------------|--------|
| Controller edits per new route only in `SKILL.md` | Phase 50 updates `SKILL.md` plus `agents/openai.yaml` because RUN-04 explicitly names metadata | Phase 50 context, 2026-06-18 | Planner should include both files and no public-doc expansion. [VERIFIED: CONTEXT.md] |
| Source-only route row before full pack | Hermes route row now has seven required references | Phase 49, 2026-06-18 | Planner should consume full pack and avoid editing `routing.md`. [VERIFIED: 49-02-SUMMARY.md; routing.md] |
| Route-specific controller ending at Cai Xukun | Hermes should become the next route-controller entry | Phase 50 | Planner should mirror the Cai Xukun, Go Gopher, and OpenClaw integration pattern. [VERIFIED: SKILL.md; 45-CONTEXT.md; 40-CONTEXT.md; 35-CONTEXT.md] |

**Deprecated/outdated:**

- Hermes `routing.md` source-only loading: superseded by Phase 49 seven-file required-reference row. [VERIFIED: 49-02-SUMMARY.md]
- Phase 45-style metadata deferral for RUN-04: Phase 50 explicitly owns `agents/openai.yaml`. [VERIFIED: 45-CONTEXT.md; 50-CONTEXT.md]

## Assumptions Log

| # | Claim | Section | Risk if Wrong |
|---|-------|---------|---------------|
| A1 | Full validator and Node suites may still fail until Phase 52. [ASSUMED] | Verification Commands | If current baseline changed to green, optional diagnostic wording could understate available validation. |

## Open Questions

None. Phase 50 target, implementation surface, and ownership are resolved by `50-CONTEXT.md`, `routing.md`, and the Phase 49 pack evidence. [VERIFIED: CONTEXT.md; routing.md; 49-VERIFICATION.md]

## Environment Availability

| Dependency | Required By | Available | Version | Fallback |
|------------|-------------|-----------|---------|----------|
| Node.js | Optional validator diagnostics | yes | v24.13.0 | Skip full validator because Phase 52 owns green repair. [VERIFIED: command output; CONTEXT.md] |
| Git | `git diff --check` | yes | 2.50.1 | none needed. [VERIFIED: command output] |
| ripgrep | Phase 50 targeted verification | yes | 15.1.0 | POSIX grep with noisier commands. [VERIFIED: command output] |
| `gsd-tools` shell shim | Optional workflow helper | no in shell PATH | unavailable | Use `/Users/longnv/.codex/gsd-core/bin/gsd-tools.cjs` for init/status when needed. [VERIFIED: command output] |
| slopcheck | Package legitimacy gate | yes | command available | No package installs in this phase. [VERIFIED: command output] |

**Missing dependencies with no fallback:** none. [VERIFIED: environment audit]

**Missing dependencies with fallback:**

- `gsd-tools` shell shim is missing from PATH; the core Node script path works for init queries. [VERIFIED: command output]

## Verification Commands

Run these after implementation. [VERIFIED: CONTEXT.md]

```bash
rg -n "Hermes Agent|hermes|assets/<article-slug>-hermes|assets/&lt;article-slug&gt;-hermes|references/ips/hermes|source-reviewed|Generated image 1 \\(16\\)\\.jpeg|mythological Hermes|product-poster" skills/visual-ip-illustrations/SKILL.md skills/visual-ip-illustrations/agents/openai.yaml
```

Expected: matches frontmatter, route overview, reference loading, selection, planning, generation/edit, QA, save, delivery, route guard, and metadata surfaces. [VERIFIED: SKILL.md pattern; openai.yaml]

```bash
rg -n "Hermes Agent shot-list entries|Hermes Agent loads only|Hermes Agent high-risk failures|Hermes Agent repair behavior|Hermes Agent block|route-leakage delivery guard" skills/visual-ip-illustrations/SKILL.md
```

Expected: matches planning, generation dispatch, QA failures, repair dispatch, mixed/single delivery, and guard surfaces. [VERIFIED: SKILL.md pattern]

```bash
rg -n "Hermes Agent|Hermes|hermes-agent|Hermes logo|Hermes Agent logo|broad assistant|AI agent|Greek messenger|winged sandals|caduceus" skills/visual-ip-illustrations/SKILL.md
```

Expected: matches Hermes alias and exclusion wording. [VERIFIED: CONTEXT.md; routing.md]

```bash
rg -n "references/ips/hermes/index\\.md|references/ips/hermes/source\\.md|references/ips/hermes/style-dna\\.md|references/ips/hermes/hermes-ip\\.md|references/ips/hermes/composition-patterns\\.md|references/ips/hermes/prompt-template\\.md|references/ips/hermes/qa-checklist\\.md" skills/visual-ip-illustrations/SKILL.md
```

Expected: every Hermes required reference appears in `SKILL.md`. [VERIFIED: routing.md]

```bash
rg -n "Visual IP Illustrations|\\$visual-ip-illustrations|\\$ian-xiaohei-illustrations|Xiaohei|Littlebox|Tom|Ferris|Seal|OpenClaw|Go Gopher|Cai Xukun|Hermes Agent" skills/visual-ip-illustrations/SKILL.md skills/visual-ip-illustrations/agents/openai.yaml
```

Expected: identity, legacy alias, existing routes, and Hermes route all remain visible. [VERIFIED: CONTEXT.md]

```bash
git diff --check -- skills/visual-ip-illustrations/SKILL.md skills/visual-ip-illustrations/agents/openai.yaml
```

Expected: exit 0. [VERIFIED: CONTEXT.md]

```bash
git status --short -- README.md readmes examples NOTICE.md RELEASE_CHECKLIST.md scripts skills/visual-ip-illustrations/SKILL.md skills/visual-ip-illustrations/agents/openai.yaml
```

Expected: only `SKILL.md` and `agents/openai.yaml` are modified among source/public surfaces for Phase 50. [VERIFIED: CONTEXT.md]

## Security Domain

### Applicable ASVS Categories

| ASVS Category | Applies | Standard Control |
|---------------|---------|------------------|
| V2 Authentication | no | No auth surface exists in this documentation-only skill phase. [VERIFIED: AGENTS.md] |
| V3 Session Management | no | No session surface exists in this documentation-only skill phase. [VERIFIED: AGENTS.md] |
| V4 Access Control | no | No API/backend access-control surface exists in this phase. [VERIFIED: AGENTS.md] |
| V5 Input Validation | yes | Route aliases and exclusion wording constrain Hermes selection; route-local QA constrains prompt output. [VERIFIED: routing.md; qa-checklist.md] |
| V6 Cryptography | no | No cryptographic implementation exists in this phase. [VERIFIED: AGENTS.md] |

### Known Threat Patterns for Documentation-Driven Image Prompt Routing

| Pattern | STRIDE | Standard Mitigation |
|---------|--------|---------------------|
| Route spoofing through broad aliases | Spoofing | Keep Hermes aliases limited to the six explicit strings and state broad-term exclusions. [VERIFIED: CONTEXT.md; routing.md] |
| Route leakage in mixed-IP output | Information Disclosure / Tampering | Each route group loads only its own required references and has its own delivery guard. [VERIFIED: SKILL.md; CONTEXT.md] |
| Official endorsement or impersonation claims | Spoofing | Keep official endorsement, affiliation, sponsorship, approval, and impersonation outside route identity. [VERIFIED: source.md; prompt-template.md] |
| Product-poster prompt drift | Tampering | Product-poster repair and boundary wording stay in planning, generation, edit, QA, and delivery surfaces. [VERIFIED: prompt-template.md; qa-checklist.md] |
| Mythology-drift prompt injection | Tampering | Mythology-drift repair and boundary wording stay in planning, generation, edit, QA, and delivery surfaces. [VERIFIED: prompt-template.md; qa-checklist.md] |

## Sources

### Primary (HIGH confidence)

- `.planning/phases/50-hermes-skill-controller-integration/50-CONTEXT.md` - locked Phase 50 decisions, scope, deferred work, and verification targets. [VERIFIED: file read]
- `.planning/REQUIREMENTS.md` - RUN-01 through RUN-04 and phase ownership. [VERIFIED: repo grep]
- `.planning/ROADMAP.md` - Phase 50 success criteria and Phase 51/52 boundaries. [VERIFIED: repo grep]
- `skills/visual-ip-illustrations/SKILL.md` - current controller surfaces and insertion points. [VERIFIED: nl/grep]
- `skills/visual-ip-illustrations/agents/openai.yaml` - current metadata fields. [VERIFIED: nl/grep]
- `skills/visual-ip-illustrations/references/routing.md` - Hermes route metadata, aliases, references, output path, and boundaries. [VERIFIED: nl/grep]
- `skills/visual-ip-illustrations/references/ips/hermes/*.md` - Hermes source, style, identity, composition, prompt, edit, QA, and delivery contract. [VERIFIED: nl/grep]
- `.planning/phases/49-hermes-canonical-pack/49-VERIFICATION.md` and summaries - Phase 49 pack completion and known Phase 52 validation boundary. [VERIFIED: file read]
- `.planning/phases/45-*`, `.planning/phases/40-*`, `.planning/phases/35-*` controller artifacts - analogous runtime-controller patterns. [VERIFIED: file read]

### Secondary (MEDIUM confidence)

- `/Users/longnv/.codex/memories/MEMORY.md` - prior repo context and caution about current GSD planning state; used only for orientation and rechecked against live repo files. [VERIFIED: memory grep]

### Tertiary (LOW confidence)

- None. [VERIFIED: research process]

## Metadata

**Confidence breakdown:**

- Standard stack: HIGH - repo has no app dependency manifests; Markdown/YAML/Node/ripgrep/Git availability was checked locally. [VERIFIED: AGENTS.md; command output]
- Architecture: HIGH - `SKILL.md`, `routing.md`, and Hermes pack responsibilities are explicit in repo files. [VERIFIED: file read]
- Pitfalls: HIGH - pitfalls come from current controller repetition, locked Phase 50 scope, and Phase 35/40/45 precedents. [VERIFIED: SKILL.md; phase artifacts]

**Research date:** 2026-06-18 [VERIFIED: system date]
**Valid until:** 2026-07-18 for this codebase-local planning artifact, unless Phase 50 source files change first. [ASSUMED]
