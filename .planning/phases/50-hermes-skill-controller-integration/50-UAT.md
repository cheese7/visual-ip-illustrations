---
phase: 50-hermes-skill-controller-integration
uat: manual
status: passed
date: 2026-06-18
---

# Phase 50 UAT: Hermes Skill Controller Integration

## Result

Passed.

## User-Facing Acceptance

- A user can select Hermes Agent with explicit aliases: `Hermes Agent`, `Hermes`, `hermes`, `hermes-agent`, `Hermes logo`, and `Hermes Agent logo`.
- Omitted visual IP still selects Xiaohei.
- Hermes Agent loads the route-local seven-file pack under `references/ips/hermes/`.
- Hermes Agent planning includes state, action, source context note, mythology-drift note, product-poster boundary note, and output path.
- Hermes Agent generation, edit, and QA dispatch use the Hermes route-local prompt, composition, and QA references.
- Mixed-IP requests include a separate Hermes Agent route group with its own references, prompt template, QA checklist, edit gates, output suffix, and output directory.
- Hermes Agent delivery reports include selected IP, image count, purpose per image, save path, uploaded-image authority status, source context note, MIT license context, mythology-drift status, product-poster boundary status, public sample boundary, route isolation, and route stability notes.
- OpenAI metadata presents Hermes Agent while preserving Visual IP Illustrations, `$visual-ip-illustrations`, `$ian-xiaohei-illustrations`, and existing route names.

## Evidence

- Source implementation commit: `526e953 feat(50-01): wire Hermes skill controller`
- Verification report: `.planning/phases/50-hermes-skill-controller-integration/50-VERIFICATION.md`
- Summary report: `.planning/phases/50-hermes-skill-controller-integration/50-01-SUMMARY.md`

## Commands

```bash
rg -n "Hermes Agent|hermes|source-reviewed|output_suffix: hermes|assets/<article-slug>-hermes|references/ips/hermes/(index|source|style-dna|hermes-ip|composition-patterns|prompt-template|qa-checklist)\\.md" skills/visual-ip-illustrations/SKILL.md
rg -n "Hermes Agent logo|hermes-agent|broad assistant|Greek messenger|winged sandals|caduceus" skills/visual-ip-illustrations/SKILL.md
rg -n 'Hermes Agent state|Hermes Agent action|Source context note|Mythology-drift note|Product-poster boundary note|Stronger Hermes Participation|Uploaded-Image Identity Repair|Mythology-Drift Repair|Product-Poster Repair|Route Leakage Repair|Unaffected-Content Preservation' skills/visual-ip-illustrations/SKILL.md
rg -n 'Hermes Agent uses `references/ips/hermes/qa-checklist.md`|Hermes high-risk failures|generic anime or assistant drift|mythological Hermes imagery|product-poster drift|missing headset|missing bob-hair highlight silhouette' skills/visual-ip-illustrations/SKILL.md
rg -n "Hermes Agent|assets/<article-slug>-hermes|source-reviewed|uploaded-image|mythology|product-poster|\\$ian-xiaohei-illustrations" skills/visual-ip-illustrations/agents/openai.yaml
git diff --check -- skills/visual-ip-illustrations/SKILL.md skills/visual-ip-illustrations/agents/openai.yaml .planning/phases/50-hermes-skill-controller-integration/50-01-SUMMARY.md .planning/phases/50-hermes-skill-controller-integration/50-VERIFICATION.md .planning/phases/50-hermes-skill-controller-integration/50-UAT.md
```

All commands exited 0 during Phase 50 verification.

## Scope Notes

- Generated Hermes image count: 0.
- Public docs/examples/NOTICE/validator changes: 0.
- Phase 51 owns public documentation and release surfaces.
- Phase 52 owns validation hardening and release evidence.
