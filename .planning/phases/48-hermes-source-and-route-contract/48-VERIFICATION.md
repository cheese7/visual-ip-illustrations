---
phase: 48-hermes-source-and-route-contract
phase_number: 48
status: passed
verified: 2026-06-18
requirements:
  - ROUTE-01
  - ROUTE-02
  - ROUTE-03
  - SRC-01
  - SRC-02
---

# Phase 48 Verification: Hermes Source and Route Contract

## Verdict

PASSED.

Phase 48 delivers the Hermes Agent source-reviewed route/source contract. Hermes is now an explicit route with `default=false`, source-only required reference `references/ips/hermes/source.md`, official Hermes Agent source context, MIT license context, uploaded conversation attachment authority, output suffix `hermes`, and output path `assets/<article-slug>-hermes/`.

## Requirement Results

| Requirement | Result | Evidence |
|-------------|--------|----------|
| ROUTE-01 | PASS | `routing.md` contains the six Hermes aliases and route matching boundary; route inspection confirms Xiaohei remains the only `default=true` route. |
| ROUTE-02 | PASS | `routing.md` contains route id `hermes`, display name `Hermes Agent`, output suffix `hermes`, raw path `assets/<article-slug>-hermes/`, and escaped marker `assets/&lt;article-slug&gt;-hermes/`. |
| ROUTE-03 | PASS | `routing.md` contains `default=false`, status `source-reviewed`, required reference `references/ips/hermes/source.md`, uploaded-image authority, and official source context. |
| SRC-01 | PASS | `source.md` contains official website, repository, MIT license URL, docs URL, third-party icon context resolution, sample policy, review owner, route status, and source-image context. |
| SRC-02 | PASS | `source.md` contains `Generated image 1 (16).jpeg` and all uploaded Hermes visual markers. |

## Automated Evidence

```bash
rg -n 'Hermes Agent|hermes-agent|Hermes logo|Hermes Agent logo|source-reviewed|assets/<article-slug>-hermes/|assets/&lt;article-slug&gt;-hermes/|references/ips/hermes/source\.md' skills/visual-ip-illustrations/references/routing.md skills/visual-ip-illustrations/references/ips/hermes/source.md
```

Result: PASS.

```bash
rg -n 'https://hermes-agent\.nousresearch\.com/|https://github\.com/NousResearch/hermes-agent|https://github\.com/NousResearch/hermes-agent/blob/main/LICENSE|https://hermes-agent\.nousresearch\.com/docs/|Generated image 1 \(16\)\.jpeg|monochrome full-body logo-style character|black bob haircut with bright highlights|headset or earpiece|black sleeveless dress|white collar tag with an `A`-like mark|black thigh-high stockings|platform heels|slender fashion-figure posture|winged sandals|caduceus|product-poster output|public generated Hermes samples require release review' skills/visual-ip-illustrations/references/ips/hermes/source.md
```

Result: PASS.

```bash
git diff --check -- .planning/ROADMAP.md .planning/STATE.md .planning/phases/48-hermes-source-and-route-contract/48-01-PLAN.md .planning/phases/48-hermes-source-and-route-contract/48-CONTEXT.md .planning/phases/48-hermes-source-and-route-contract/48-DISCUSSION-LOG.md .planning/phases/48-hermes-source-and-route-contract/48-RESEARCH.md .planning/phases/48-hermes-source-and-route-contract/48-01-SUMMARY.md
```

Result: PASS.

## Route Inspection

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
```

Result: PASS. Hermes appears after Cai Xukun. Xiaohei remains the only omitted-IP default.

## Files Verified

- `skills/visual-ip-illustrations/references/routing.md`
- `skills/visual-ip-illustrations/references/ips/hermes/source.md`
- `.planning/phases/48-hermes-source-and-route-contract/48-01-SUMMARY.md`

## Scope Check

Phase 48 stayed within route/source scope. Full Hermes pack files remain Phase 49 ownership. `SKILL.md` controller integration remains Phase 50 ownership. Public docs, NOTICE, release checklist, examples, and metadata remain Phase 51 ownership. Validator, Node tests, leakage scans, mythology-drift scans, and release evidence remain Phase 52 ownership.

## Verification Complete
