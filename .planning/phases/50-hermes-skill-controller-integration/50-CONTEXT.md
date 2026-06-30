# Phase 50: Hermes Skill Controller Integration - Context

**Gathered:** 2026-06-18
**Status:** Ready for planning

<domain>
## Phase Boundary

Phase 50 wires the already-defined `hermes` route into the Visual IP Illustrations runtime controller. Users should be able to select Hermes Agent, load the Hermes seven-file pack, plan Hermes shots, generate/edit Hermes images, run Hermes QA, save under `assets/<article-slug>-hermes/`, receive Hermes delivery reports, and request mixed-IP output where Hermes is a separate route group.

Implementation scope centers on:

- `skills/visual-ip-illustrations/SKILL.md`
- `skills/visual-ip-illustrations/agents/openai.yaml`

The route metadata and Hermes pack were completed in Phases 48 and 49:

- `skills/visual-ip-illustrations/references/routing.md`
- `skills/visual-ip-illustrations/references/ips/hermes/index.md`
- `skills/visual-ip-illustrations/references/ips/hermes/source.md`
- `skills/visual-ip-illustrations/references/ips/hermes/style-dna.md`
- `skills/visual-ip-illustrations/references/ips/hermes/hermes-ip.md`
- `skills/visual-ip-illustrations/references/ips/hermes/composition-patterns.md`
- `skills/visual-ip-illustrations/references/ips/hermes/prompt-template.md`
- `skills/visual-ip-illustrations/references/ips/hermes/qa-checklist.md`

Out of scope:

- README variants, `examples/prompts.md`, NOTICE, release checklist, public release copy, and public sample surfaces. Phase 51 owns these.
- Validator hardening, Node regression tests, smoke prompts, leakage fixtures, public sample gates, and final release evidence. Phase 52 owns these.
- Generated Hermes images or public sample assets.

</domain>

<decisions>
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

### Agent Discretion

- The planner may choose exact `SKILL.md` paragraph placement by following the Cai Xukun, Go Gopher, and OpenClaw route-specific pattern.
- The planner may keep Hermes runtime text compact because detailed style, prompt, edit, and QA rules live in `references/ips/hermes/`.
- The planner should use targeted `rg` checks and `git diff --check` as Phase 50 acceptance proof; full validator and Node tests remain Phase 52.

</decisions>

<canonical_refs>
## Canonical References

**Downstream agents MUST read these before planning or implementing.**

### Phase Scope

- `.planning/ROADMAP.md` - Phase 50 goal, success criteria, and Phase 51/52 boundaries.
- `.planning/REQUIREMENTS.md` - RUN-01 through RUN-04.
- `.planning/STATE.md` - current milestone state.

### Prior Phase Evidence

- `.planning/phases/48-hermes-source-and-route-contract/48-VERIFICATION.md` - verified route/source contract.
- `.planning/phases/49-hermes-canonical-pack/49-VERIFICATION.md` - verified seven-file Hermes pack.
- `.planning/phases/49-hermes-canonical-pack/49-01-SUMMARY.md` - operational pack creation evidence.
- `.planning/phases/49-hermes-canonical-pack/49-02-SUMMARY.md` - routing expansion and phase-level verification evidence.

### Runtime Targets

- `skills/visual-ip-illustrations/SKILL.md` - central runtime controller.
- `skills/visual-ip-illustrations/agents/openai.yaml` - agent metadata required by RUN-04.
- `skills/visual-ip-illustrations/references/routing.md` - route metadata, aliases, required references, output suffix, and mixed-IP behavior.

### Hermes Route Pack

- `skills/visual-ip-illustrations/references/ips/hermes/index.md`
- `skills/visual-ip-illustrations/references/ips/hermes/source.md`
- `skills/visual-ip-illustrations/references/ips/hermes/style-dna.md`
- `skills/visual-ip-illustrations/references/ips/hermes/hermes-ip.md`
- `skills/visual-ip-illustrations/references/ips/hermes/composition-patterns.md`
- `skills/visual-ip-illustrations/references/ips/hermes/prompt-template.md`
- `skills/visual-ip-illustrations/references/ips/hermes/qa-checklist.md`

### Controller Precedents

- `.planning/phases/45-cai-xukun-skill-controller-integration/45-CONTEXT.md`
- `.planning/phases/45-cai-xukun-skill-controller-integration/45-01-SUMMARY.md`
- `.planning/phases/40-go-gopher-skill-controller-integration/40-CONTEXT.md`
- `.planning/phases/35-openclaw-skill-controller-integration/35-CONTEXT.md`

</canonical_refs>

<verification_targets>
## Phase 50 Verification Targets

- `SKILL.md` frontmatter description mentions Hermes Agent while preserving existing routes.
- `SKILL.md` Visual IP Routes includes route id `hermes`, display name Hermes Agent, `default=false`, output suffix `hermes`, route status `source-reviewed`, source pointer, uploaded-image authority, official source context, MIT license context, public sample review boundary, mythology-drift boundary, product-poster boundary, and output path.
- `SKILL.md` Reference Loading lists all seven Hermes route-local references.
- `SKILL.md` route selection includes Hermes aliases and broad-term exclusions.
- `SKILL.md` planning fields include Hermes Agent state/action, source context note, mythology-drift note, product-poster boundary note, and output path.
- `SKILL.md` generation/edit/QA sections dispatch to Hermes prompt, composition, and QA references.
- `SKILL.md` mixed-IP sections include Hermes as a separate route group.
- `SKILL.md` save path and output contract include `assets/<article-slug>-hermes/` and escaped marker `assets/&lt;article-slug&gt;-hermes/`.
- `agents/openai.yaml` includes Hermes Agent in display name, short description, and default prompt while preserving existing route text and `$ian-xiaohei-illustrations`.
- `git diff --check` passes.

</verification_targets>

<open_questions>
## Open Questions

None. Phase 50 target and implementation surface are determined by RUN-01 through RUN-04 and the current runtime-controller gap.

</open_questions>
