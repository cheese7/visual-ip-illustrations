# Stack Research: Hermes Agent Visual IP Integration

**Research type:** Project Research - Stack dimension
**Project:** Visual IP Illustrations
**Milestone:** v1.10 Hermes Agent Visual IP Integration
**Researched:** 2026-06-18
**Scope:** Add Hermes Agent as a selectable visual IP route using the user-uploaded black-and-white logo-style character as the visual authority.

## Recommendation

Keep the stack unchanged: Markdown route references, YAML agent metadata, static docs/examples, host-provided `image_gen`, and dependency-free Node validation. Hermes Agent should be added as another isolated route under `skills/visual-ip-illustrations/references/ips/hermes/`, with metadata in `references/routing.md`, public documentation, NOTICE attribution, release gates, validator checks, and Node regression tests.

The new stack concern is provenance layering. The user-uploaded conversation attachment is the visual authority for this route. Official Hermes Agent surfaces from Nous Research provide naming, product context, and open-source license context: `https://hermes-agent.nousresearch.com/`, `https://github.com/NousResearch/hermes-agent`, and the MIT license in the official repository. LobeHub icon/library references can be cited as third-party icon context only after implementation confirms the exact source path.

## Verified Hermes Agent Facts

| Fact | Evidence |
|------|----------|
| Hermes Agent is the self-improving AI agent built by Nous Research. | Official README and website copy. |
| Hermes Agent has official docs at `hermes-agent.nousresearch.com/docs/`. | Official README badge and site navigation. |
| Hermes Agent is distributed under MIT license. | Official repository `LICENSE`: MIT License, Copyright (c) 2025 Nous Research. |
| Hermes Agent supports CLI, messaging gateways, memory, skills, scheduling, subagents, and multiple terminal backends. | Official README feature table. |
| The requested route authority is the uploaded black-and-white character image. | User request attached `Generated image 1 (16).jpeg`; local `/Users/carson/Downloads/...` path was unavailable in this environment, so the route record should cite the conversation attachment. |

## Stack Additions

| Layer | Addition | Rationale |
|-------|----------|-----------|
| Source record | `references/ips/hermes/source.md` | Records official site, official repository, MIT license, uploaded-image authority, third-party icon context, public sample policy, and review owner. |
| IP pack | `references/ips/hermes/` | Keeps Hermes identity, style, composition, prompt, QA, and source boundaries route-local. |
| Routing | `references/routing.md` row for `hermes` | Adds deterministic aliases, output suffix, required references, source context, and status. |
| Skill runtime | `SKILL.md` route selection and dispatch updates | Lets users select Hermes Agent without affecting Xiaohei default behavior. |
| Public docs | README variants, prompt examples, NOTICE, release checklist, and agent metadata | Exposes the route, output path, source/license context, uploaded-image authority, and public sample gates. |
| Validation | `scripts/validate-skill-package.mjs` and tests | Makes route, source, docs, output path, leakage, public sample, and release gates deterministic. |

## Recommended Pack Shape

```text
skills/visual-ip-illustrations/references/ips/hermes/
├── index.md
├── source.md
├── style-dna.md
├── hermes-ip.md
├── composition-patterns.md
├── prompt-template.md
└── qa-checklist.md
```

Use the OpenClaw and Go Gopher pack shape because Hermes needs both official source/license context and uploaded-image visual authority. Keep route files in English and keep visible labels in the user's requested language.

## Routing Contract

| Field | Recommended value |
|-------|-------------------|
| `id` | `hermes` |
| `display_name` | `Hermes Agent` |
| `aliases` | `Hermes Agent`, `Hermes`, `hermes`, `hermes-agent`, `Hermes logo`, `Hermes Agent logo`, `Nous Hermes` |
| `default` | `false` |
| `output_suffix` | `hermes` |
| `required_references` | all seven Hermes route-local files |
| `attribution_context` | Hermes Agent official website, Nous Research repository, MIT license, uploaded conversation attachment visual authority, source record |
| `status` | `source-reviewed` during implementation; `active` after route, docs, validator, release evidence, and sample policy pass |

Output path:

```text
assets/<article-slug>-hermes/
assets/&lt;article-slug&gt;-hermes/
```

## What To Avoid

| Avoid | Reason |
|-------|--------|
| New app runtime, build system, package manager, database, or service | The project remains a lightweight Codex Skill package. |
| Generic custom-IP importer | The milestone target is one Hermes Agent route with a concrete uploaded visual authority. |
| Treating Hermes as the default AI-agent route | Xiaohei remains the omitted-IP default and Hermes is explicit-only. |
| Blending Hermes with generic anime, secretary, cyberpunk, or assistant tropes | The uploaded image defines the route identity. |
| Public generated Hermes sample gallery before release review | Public sample assets need identity, source, and license review. |

## Validation Commands

```bash
node scripts/validate-skill-package.mjs
node --test scripts/validate-skill-package.test.mjs
git diff --check
```

## Sources

- Hermes Agent official website: https://hermes-agent.nousresearch.com/
- Hermes Agent official repository: https://github.com/NousResearch/hermes-agent
- Hermes Agent MIT license: https://github.com/NousResearch/hermes-agent/blob/main/LICENSE
- Hermes Agent documentation: https://hermes-agent.nousresearch.com/docs/
- User-provided uploaded image: conversation attachment `Generated image 1 (16).jpeg`.

---
*Research completed: 2026-06-18*
