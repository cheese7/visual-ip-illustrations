---
phase: 51-hermes-public-documentation-and-release-surface
tested: 2026-06-18T12:34:44Z
status: passed
mode: auto
tester: gsd-verifier
---

# Phase 51 UAT: Hermes Public Documentation and Release Surface

## Scope

Auto-UAT for the documentation release surface after the README.zh.md Hermes parity gap closure. This phase has no running application, so UAT is command-backed documentation verification.

## Test Results

| # | Test | Command | Expected | Result | Status |
| --- | --- | --- | --- | --- | --- |
| 1 | README variants include Hermes operational route facts | `rg --files-without-match -F -- '- Hermes Agent: route id \`hermes\`; default=false; status \`source-reviewed\`' README.md readmes/README.*.md` | Empty output. | Empty output. | PASS |
| 2 | README variants include Hermes escaped marker | `rg --files-without-match -F -- 'Docs validation also keeps Hermes Agent escaped marker: \`assets/&lt;article-slug&gt;-hermes/\`' README.md readmes/README.*.md` | Empty output. | Empty output. | PASS |
| 3 | README variants include Hermes canonical pack/source authority line | `rg --files-without-match -F -- '- Hermes Agent: \`skills/visual-ip-illustrations/references/ips/hermes/\`, source authority \`skills/visual-ip-illustrations/references/ips/hermes/source.md\`' README.md readmes/README.*.md` | Empty output. | Empty output. | PASS |
| 4 | Public Hermes generated sample assets remain absent | `find examples/images examples/images-en skills/visual-ip-illustrations/assets/examples -type f \( -iname '*hermes*' -o -iname '*Hermes*' \) -print` | Empty output. | Empty output. | PASS |
| 5 | Prompt examples carry Hermes planning, generation, edit, mixed-IP, smoke, and output markers | `rg -n "Hermes Agent state\|Hermes Agent action\|Source context note\|Mythology-drift note\|Product-poster boundary note\|nine separate variant groups\|Hermes Agent variant group\|Route Smoke: Explicit Hermes Agent\|Smoke: Hermes Agent source-reviewed route status\|assets/<article-slug>-hermes\|assets/&lt;article-slug&gt;-hermes" examples/prompts.md` | Required markers found. | Required markers found. | PASS |
| 6 | NOTICE and release checklist carry Hermes source, MIT, uploaded-image, public-sample, and release markers | `rg -n "Hermes Agent Source\|https://hermes-agent.nousresearch.com/\|https://github.com/NousResearch/hermes-agent\|https://github.com/NousResearch/hermes-agent/blob/main/LICENSE\|https://hermes-agent.nousresearch.com/docs/\|Generated image 1 \(16\)\.jpeg\|public generated Hermes samples\|mythology-drift\|product-poster\|Phase 52 owns Hermes\|Explicit Hermes Agent smoke\|Hermes Agent Source, MIT License, Uploaded-Image Authority, and Public Sample Gate\|Final Hermes release review\|assets/&lt;article-slug&gt;-hermes" NOTICE.md RELEASE_CHECKLIST.md` | Required markers found. | Required markers found. | PASS |
| 7 | Skill instructions and agent metadata carry Hermes route/source/output/boundary markers | `rg -n "Hermes\|hermes\|source-reviewed\|MIT\|Generated image 1 \(16\)\.jpeg\|public sample\|mythology\|product-poster\|route isolation\|uploaded-character-only\|assets/<article-slug>-hermes\|assets/&lt;article-slug&gt;-hermes" skills/visual-ip-illustrations/SKILL.md skills/visual-ip-illustrations/agents/openai.yaml` | Required markers found. | Required markers found. | PASS |
| 8 | Public documentation diff is whitespace-clean | `git diff --check -- README.md readmes/README.*.md examples/prompts.md NOTICE.md RELEASE_CHECKLIST.md skills/visual-ip-illustrations/agents/openai.yaml skills/visual-ip-illustrations/SKILL.md .planning/phases/51-hermes-public-documentation-and-release-surface/51-01-SUMMARY.md .planning/phases/51-hermes-public-documentation-and-release-surface/51-VERIFICATION.md .planning/phases/51-hermes-public-documentation-and-release-surface/51-UAT.md` | Exit code 0. | Exit code 0. | PASS |

## UAT Decision

PASS. Phase 51 documentation behavior is verified through command-backed checks. The previous README.zh.md parity gap is closed, and no public Hermes generated sample assets are present.
