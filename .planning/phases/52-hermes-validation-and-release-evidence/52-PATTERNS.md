# Phase 52: Hermes Validation and Release Evidence - Pattern Map

**Mapped:** 2026-06-18
**Files analyzed:** 3 implementation/release files
**Analogs found:** 3 / 3

## File Classification

| New/Modified File | Role | Data Flow | Closest Analog | Match Quality |
|-------------------|------|-----------|----------------|---------------|
| `scripts/validate-skill-package.mjs` | utility / validator | batch, file-I/O, transform | Go Gopher + Cai Xukun validator families in `scripts/validate-skill-package.mjs` | exact |
| `scripts/validate-skill-package.test.mjs` | test | batch, fixture mutation | Go Gopher + Cai Xukun fixture families in `scripts/validate-skill-package.test.mjs` | exact |
| `.planning/phases/52-hermes-validation-and-release-evidence/52-RELEASE-EVIDENCE.md` | release evidence | batch, command evidence | `.planning/phases/47-cai-xukun-validation-and-release-evidence/47-RELEASE-EVIDENCE.md` and Phase 42 evidence | exact |

## Pattern Assignments

### `scripts/validate-skill-package.mjs` (validator utility, batch/file-I/O)

**Analogs:** Go Gopher, OpenClaw, and Cai Xukun route-specific validators in the same file.

**Route/output path helpers** (lines 709-756):

```javascript
export function outputPathTokens() {
  return {
    raw: [
      "assets/<article-slug>-illustrations/",
      "assets/<article-slug>-littlebox/",
      "assets/<article-slug>-tom/",
      "assets/<article-slug>-ferris/",
      "assets/<article-slug>-seal/",
      "assets/<article-slug>-openclaw/",
      "assets/<article-slug>-gopher/",
      "assets/<article-slug>-caixukun/",
    ],
    escaped: [
      "assets/&lt;article-slug&gt;-illustrations/",
      "assets/&lt;article-slug&gt;-littlebox/",
      "assets/&lt;article-slug&gt;-tom/",
      "assets/&lt;article-slug&gt;-ferris/",
      "assets/&lt;article-slug&gt;-seal/",
      "assets/&lt;article-slug&gt;-openclaw/",
      "assets/&lt;article-slug&gt;-gopher/",
      "assets/&lt;article-slug&gt;-caixukun/",
    ],
  };
}
```

Add `assets/<article-slug>-hermes/` and `assets/&lt;article-slug&gt;-hermes/` to both `outputPathTokens()` and `publicDocsOutputPathTokens()`.

**Approval parser family** (lines 781-864):

```javascript
export function parsePublicOpenClawSampleApproval(releaseChecklistText) {
  const approvalLine = releaseChecklistText
    .split("\n")
    .map((line) => line.trim())
    .find((line) => line.includes("OpenClaw public asset policy for"));

  return parseOpenClawApprovalLine(approvalLine, "public");
}

export function parseGeneratedCaiXukunSampleApproval(releaseChecklistText) {
  const caiXukunSection = releaseChecklistText
    .split("## Cai Xukun Source Boundary and Public Sample Gate")[1]
    ?.split("## Installable Package Boundary")[0] ?? "";
  const approvalLine = caiXukunSection
    .split("\n")
    .map((line) => line.trim())
    .find((line) => line.includes("Record generated sample review:"));

  return parseCaiXukunApprovalLine(approvalLine, "generated");
}
```

Copy this route-specific parser shape for `parsePublicHermesSampleApproval()`, `parseGeneratedHermesSampleApproval()`, and a `parseHermesApprovalLine()` helper near the OpenClaw/Gopher/Cai Xukun approval-line helpers. Hermes public approval must require reviewer, valid date, status, allowed directories, release channels, uploaded-image identity outcome, source/MIT outcome, mythology-drift outcome, product-poster boundary outcome, route-isolation outcome, article-metaphor quality outcome, and public-sample decision.

**Reference inventory helpers** (lines 1941-1959, 2289-2335):

```javascript
function requiredPackageFiles() {
  return [
    SKILL_FILE,
    OPENAI_AGENT_FILE,
    ROUTING_FILE,
    ...
    ...openclawOperationalRefs(),
    ...gopherOperationalRefs(),
    ...caixukunOperationalRefs(),
    ...legacyXiaoheiRefs().map((item) => item.root),
    "README.md",
    "examples/prompts.md",
    "NOTICE.md",
    "LICENSE",
  ];
}

function gopherPlannedReferences() {
  return [
    "references/ips/gopher/index.md",
    "references/ips/gopher/source.md",
    "references/ips/gopher/style-dna.md",
    "references/ips/gopher/gopher-ip.md",
    "references/ips/gopher/composition-patterns.md",
    "references/ips/gopher/prompt-template.md",
    "references/ips/gopher/qa-checklist.md",
  ];
}
```

Add `hermesPlannedReferences()` and `hermesOperationalRefs()` directly after Cai Xukun or adjacent to the source-reviewed route helpers. Required Hermes files are `index.md`, `source.md`, `style-dna.md`, `hermes-ip.md`, `composition-patterns.md`, `prompt-template.md`, and `qa-checklist.md` under `references/ips/hermes/`. Add `...hermesOperationalRefs()` to `requiredPackageFiles()`.

**Route-order and stale eight-route normalization** (lines 2159-2225, 2364-2395, 2433):

```javascript
function assertPhase28CompatibilitySurface() {
  assertRebrandRouteTable();
  const combinedRuntimeDocs = combinedText([
    SKILL_FILE,
    OPENAI_AGENT_FILE,
    "README.md",
    "examples/prompts.md",
    LANGUAGE_POLICY_FILE,
    ROUTING_FILE,
  ]);
  assertIncludes(combinedRuntimeDocs, "runtime + docs + policy + routing surfaces", [
    "$visual-ip-illustrations",
    "$ian-xiaohei-illustrations",
    ...
    "Cai Xukun",
    "蔡徐坤",
    "caixukun",
    "cxk",
    "gated-public-figure",
  ], "canonical and legacy invocations, Chinese aliases, and visible-label behavior");
}
```

Extend `rebrandRouteExpectations()`, `assertRebrandRouteTable()`, `assertPhase28CompatibilitySurface()`, `REBRAND-CANON-004`, `REBRAND-ROUTE-001`, `REBRAND-DOCS-001`, route table checks, mixed-IP checks, and public docs path checks from eight routes to nine. The stable order is `xiaohei`, `littlebox`, `tom`, `ferris`, `seal`, `openclaw`, `gopher`, `caixukun`, `hermes`. Hermes remains `default=false`, `status=source-reviewed`, `outputSuffix=hermes`, `referenceCount=7`.

**Route-specific check family insertion areas** (line anchors):

| Family | Existing analog IDs | Insert Hermes sibling near |
|--------|---------------------|----------------------------|
| Agent metadata | `AGENT-OPENCLAW-001`, `AGENT-GOPHER-001`, `AGENT-CAIXUKUN-001` | lines 2824-2848 |
| Route contract | `ROUTE-GOPHER-001`, `ROUTE-CAIXUKUN-001` | lines 3074-3107 |
| Reference pack | `REFS-OPENCLAW-001`, `REFS-GOPHER-001`, `REFS-CAIXUKUN-001` | lines 3395-3468 |
| Prompt template | `PROMPT-OPENCLAW-001`, `PROMPT-GOPHER-001`, `PROMPT-CAIXUKUN-001` | lines 3645-3697 |
| IP identity | `IP-OPENCLAW-001`, `IP-GOPHER-001`, `IP-CAIXUKUN-001` | lines 3856-3929 |
| QA checklist | `QA-OPENCLAW-001`, `QA-GOPHER-001`, `QA-CAIXUKUN-001` | lines 4069-4139 |
| Source/license | `SOURCE-OPENCLAW-001`, `SOURCE-GOPHER-001`, `SOURCE-CAIXUKUN-001` | lines 4250-4325 |
| Public docs | `DOC-OPENCLAW-001`, `DOC-GOPHER-001`, `DOC-CAIXUKUN-001` | lines 4591-4702 |
| NOTICE | `NOTICE-OPENCLAW-001`, `NOTICE-GOPHER-001`, `NOTICE-CAIXUKUN-001` | lines 4846-4882 |
| Smoke prompts | `SMOKE-OPENCLAW-001`, `SMOKE-GOPHER-001`, `SMOKE-CAIXUKUN-001` | lines 4994-5033 |
| Mixed-IP smoke | `SMOKE-MIXED-OPENCLAW-001`, `SMOKE-MIXED-GOPHER-001`, `SMOKE-MIXED-CAIXUKUN-001` | lines 5081-5121 |
| Release checklist | `RELEASE-OPENCLAW-001`, `RELEASE-GOPHER-001`, `RELEASE-CAIXUKUN-001` | lines 5242-5299 |

Use Hermes IDs from the context: `AGENT-HERMES-001`, `ROUTE-HERMES-001`, `REFS-HERMES-001`, `PROMPT-HERMES-001`, `IP-HERMES-001`, `QA-HERMES-001`, `SOURCE-HERMES-001`, `DOC-HERMES-001`, `NOTICE-HERMES-001`, `SMOKE-HERMES-001`, `SMOKE-MIXED-HERMES-001`, and `RELEASE-HERMES-001`.

**Release evidence checks** (lines 5567-5657):

```javascript
defineCheck("VAL-CAIXUKUN-EVIDENCE-001", "Phase 47 records Cai Xukun validation and release evidence", () => {
  const evidencePath = path.join(
    ".planning",
    "phases",
    "47-cai-xukun-validation-and-release-evidence",
    "47-RELEASE-EVIDENCE.md",
  );
  assertIncludes(requireFile(evidencePath), evidencePath, [
    "# Phase 47 Release Evidence: Cai Xukun Validation",
    "node scripts/validate-skill-package.mjs",
    "node --test scripts/validate-skill-package.test.mjs",
    "git diff --check",
    "Cai Xukun route smoke",
    "uploaded-image smoke",
    "docs consistency",
    "BOUNDARY-CAIXUKUN-LEAK-001",
    "BOUNDARY-CAIXUKUN-IMG-001",
    "BOUNDARY-CAIXUKUN-GEN-001",
    "VAL-01",
    "VAL-02",
    "VAL-03",
    "VAL-04",
    "VAL-05",
  ], "Phase 47 exact command summaries, route smoke, uploaded-image smoke, docs consistency, leakage, sample gates, scope evidence, and requirement traceability");
})
```

Add `VAL-HERMES-EVIDENCE-001` after the Phase 52 release evidence exists. Required markers: `# Phase 52 Release Evidence: Hermes Validation`, validator command, Node test command, `git diff --check`, Hermes route smoke, uploaded-image smoke, source/MIT boundary smoke, mythology-drift scan, public sample gate, generated sample gate, dirty-worktree scope, `BOUNDARY-HERMES-LEAK-001`, `BOUNDARY-HERMES-IMG-001`, `BOUNDARY-HERMES-GEN-001`, and `VAL-01` through `VAL-05`.

**Leakage and sample gates** (lines 5746-5994):

```javascript
defineCheck("BOUNDARY-GOPHER-LEAK-001", "non-Go-Gopher route references keep Go Gopher source-reviewed markers isolated", () => {
  const leakMarkers = [
    "Go Gopher",
    "Gopher mascot",
    "gopher.png",
    "Renee French",
    "Creative Commons Attribution 4.0",
    "references/ips/gopher",
    "assets/<article-slug>-gopher/",
    "assets/&lt;article-slug&gt;-gopher/",
  ];
  const scannedPaths = [
    path.join(REFERENCES_DIR, "ips", "xiaohei", "index.md"),
    ...xiaoheiOperationalRefs(),
    ...
    ...legacyXiaoheiRefs().map((item) => item.root),
  ];
  for (const relativePath of scannedPaths) {
    assertNoMarkers(requireFile(relativePath), relativePath, leakMarkers, "no Go Gopher route text leakage");
  }
})
```

For Hermes, scan every non-Hermes route-local pack plus legacy root Xiaohei references. Include markers from Phase 52 context: `Hermes Agent`, `hermes-agent`, `references/ips/hermes`, raw/escaped output paths, `Generated image 1 (16).jpeg`, uploaded-image authority, black bob haircut, headset or earpiece, black sleeveless dress, white collar tag, thigh-high stockings, platform heels, slender fashion-figure posture, mythology-drift boundary, and product-poster boundary.

Copy the public sample gate shape from `BOUNDARY-GOPHER-IMG-001` and `BOUNDARY-CAIXUKUN-IMG-001`: parse approval, scan `imageAssetPaths()`, fail on `hermes|hermes-agent` public filenames when approval is incomplete, and include field-by-field missing diagnostics. Copy generated sample distinction from `BOUNDARY-GOPHER-GEN-001` and `BOUNDARY-CAIXUKUN-GEN-001`, with `assets/<article-slug>-hermes/` and the Hermes-specific review fields.

### `scripts/validate-skill-package.test.mjs` (test, fixture mutation)

**Analogs:** Cai Xukun and Go Gopher parser, route-order, public sample, generated sample, and leakage tests.

**Required check order list** (lines 10-155):

```javascript
const requiredCheckIds = [
  "PKG-SHAPE-001",
  ...
  "AGENT-GOPHER-001",
  "AGENT-CAIXUKUN-001",
  ...
  "BOUNDARY-GOPHER-GEN-001",
  "BOUNDARY-CAIXUKUN-GEN-001",
  "BOUNDARY-P5-001",
];
```

Insert Hermes IDs immediately after the comparable Cai Xukun or source-reviewed route IDs in each family. Update all summary assertions from the current Phase 47 total to the final Phase 52 total after the new matrix is stable.

**Fixture helper pattern** (lines 158-180):

```javascript
function runValidator(extraEnv = {}) {
  return spawnSync(process.execPath, [scriptPath], {
    cwd: repoRoot,
    env: { ...process.env, ...extraEnv },
    encoding: "utf8",
  });
}

function copyFixture(name) {
  const fixtureRoot = fixturePath(name);
  cpSync(repoRoot, fixtureRoot, {
    recursive: true,
    filter(source) {
      const relative = path.relative(repoRoot, source);
      return relative !== ".git" && !relative.startsWith(`.git${path.sep}`);
    },
  });
```

Reuse `copyFixture`, `runFixtureValidator`, `replaceInFixture`, and `replaceAllInFixture`. Hermes fixture tests should mutate copied files and assert exact failing check IDs.

**Approval line builders** (lines 267-378):

```javascript
function pendingGopherPublicAssetApprovalLine() {
  return "- [ ] Go Gopher public asset policy for `examples/images/`, `examples/images-en/`, and `skills/visual-ip-illustrations/assets/examples/`: PENDING / reviewer / date / approval status / allowed directories / release channels / Go blog source outcome / Renee French attribution outcome / Creative Commons Attribution 4.0 outcome / local visual marker outcome / route-isolation outcome / Go logo boundary outcome / official endorsement boundary outcome / article-metaphor quality outcome / public-sample decision.";
}

function pendingCaiXukunPublicAssetApprovalLine() {
  return "- [ ] Cai Xukun public asset policy for `examples/images/`, `examples/images-en/`, and `skills/visual-ip-illustrations/assets/examples/`: PENDING / reviewer / date / approval status / allowed directories / release channels / uploaded-image identity outcome / public-figure likeness boundary outcome / source-image context boundary outcome / route-isolation outcome / stylized mascot-only output outcome / article-metaphor quality outcome / public-sample decision.";
}
```

Create `pendingHermesPublicAssetApprovalLine()`, `completeHermesPublicAssetApprovalLine()`, `pendingGeneratedHermesSampleLine()`, and `completeGeneratedHermesSampleLine()` with fields from Phase 52 D-24/D-26.

**Route parser primitives** (lines 1112-1261):

```javascript
const routes = validators.parseMarkdownTable(routingText, "IP Routes");
assert.equal(routes.length, 8);
assert.deepEqual(routes.map((route) => route.id), [
  "xiaohei",
  "littlebox",
  "tom",
  "ferris",
  "seal",
  "openclaw",
  "gopher",
  "caixukun",
]);
...
assert.ok(validators.outputPathTokens().raw.includes("assets/<article-slug>-caixukun/"));
assert.ok(validators.outputPathTokens().escaped.includes("assets/&lt;article-slug&gt;-caixukun/"));
```

Normalize route count/order to nine and assert Hermes aliases, `output_suffix=hermes`, `default=false`, `status=source-reviewed`, seven references, and raw/escaped output paths.

**Leakage fixture pattern** (lines 2958-3007):

```javascript
test("validator fixture reports Cai Xukun leakage in non-Cai-Xukun packs", () => {
  for (const [name, relativePath, marker] of [
    ["xiaohei", path.join("skills", "visual-ip-illustrations", "references", "ips", "xiaohei", "xiaohei-ip.md"), "Cai Xukun"],
    ["littlebox", path.join("skills", "visual-ip-illustrations", "references", "ips", "littlebox", "littlebox-ip.md"), "references/ips/caixukun"],
    ...
  ]) {
    const fixtureRoot = copyFixture(`caixukun-leak-${name}`);
    ...
    assert.match(result.stdout, /\[FAIL\] BOUNDARY-CAIXUKUN-LEAK-001 /);
  }
});
```

Copy this loop for Hermes across Xiaohei, Littlebox, Tom, Ferris, Seal, OpenClaw, Go Gopher, Cai Xukun, and legacy root references. Use distinct Hermes markers per target so the check proves broad marker coverage.

**Public sample fixture pattern** (lines 3241-3297 and 3602-3648):

```javascript
test("validator fixture enforces public Go Gopher sample approval parsing", async () => {
  const validators = await import(`${scriptPath}?gopherApproval=${Date.now()}`);
  const fixtureRoot = copyFixture("gopher-public-asset");
  try {
    replaceInFixture(
      fixtureRoot,
      "RELEASE_CHECKLIST.md",
      currentGopherPublicAssetApprovalLine(),
      pendingGopherPublicAssetApprovalLine(),
    );
    writeFileSync(path.join(fixtureRoot, "examples", "images", "99-gopher-test.png"), "fixture", "utf8");
    const pendingResult = runFixtureValidator(fixtureRoot);
    assert.equal(pendingResult.status, 1);
    assert.match(pendingResult.stdout, /\[FAIL\] BOUNDARY-GOPHER-IMG-001 /);
    ...
  } finally {
    rmSync(fixtureRoot, { recursive: true, force: true });
  }
});
```

Copy this for Hermes with `99-hermes-test.png`, `BOUNDARY-HERMES-IMG-001`, pending/complete approval replacement, and assertions for uploaded-image identity, source/MIT, mythology-drift, product-poster, route-isolation, article-metaphor, and public-sample decision fields.

**Generated sample fixture pattern** (lines 3985-4149 and 4153-4280):

```javascript
test("validator fixture distinguishes Generated Sample Go Gopher review outputs from public samples", async () => {
  const validators = await import(`${scriptPath}?generatedGopherApproval=${Date.now()}`);
  const releaseChecklistText = readFileSync(path.join(repoRoot, "RELEASE_CHECKLIST.md"), "utf8");
  const currentApproval = validators.parseGeneratedGopherSampleApproval(releaseChecklistText);
  assert.equal(currentApproval.complete, true);
  ...
  const fixtureRoot = copyFixture("gopher-generated-sample");
  try {
    const workspaceOutputDir = path.join(fixtureRoot, "assets", "article-gopher");
    mkdirSync(workspaceOutputDir, { recursive: true });
    writeFileSync(path.join(workspaceOutputDir, "99-gopher-test.png"), "fixture", "utf8");
    const result = runFixtureValidator(fixtureRoot);
    assert.equal(result.status, 0);
    assert.match(result.stdout, /\[PASS\] BOUNDARY-GOPHER-GEN-001 /);
    assert.match(result.stdout, /\[PASS\] BOUNDARY-GOPHER-IMG-001 /);
  } finally {
    rmSync(fixtureRoot, { recursive: true, force: true });
  }
});
```

Copy this for Hermes with an internal `assets/article-hermes/99-hermes-test.png` fixture. The generated sample gate should pass for internal workspace assets while the public image gate remains independent.

### `.planning/phases/52-hermes-validation-and-release-evidence/52-RELEASE-EVIDENCE.md` (release evidence, batch)

**Analogs:** Phase 47 release evidence for uploaded-image/public-gate/scope shape, plus Phase 42 evidence for source-reviewed route release style.

**Phase 47 structure** (`47-RELEASE-EVIDENCE.md`, full file):

```markdown
---
phase: 47
status: pass
created: 2026-06-18T06:00:00Z
requirements:
  - VAL-01
  - VAL-02
  - VAL-03
  - VAL-04
  - VAL-05
---

# Phase 47 Release Evidence: Cai Xukun Validation

## Verdict

PASS.

## Command Evidence

```bash
node scripts/validate-skill-package.mjs
# Summary: total=145 passed=145 failed=0 skipped=0
```
```

Use the same sections: frontmatter, `## Verdict`, `## Command Evidence`, route smoke, uploaded-image smoke, source/MIT boundary smoke, docs consistency, leakage scan, public sample gate, generated sample gate, dirty-worktree scope, and requirement traceability.

**Phase 42 evidence additions:** include exact command snippets for public sample directory `find`, release evidence marker `rg -q 'VAL-01|...'`, and any Hermes-specific source/marker `rg` scans. Phase 42 also shows route-specific source/license smoke and a concrete untracked-file check; for Hermes, replace this with uploaded attachment/source/MIT/public-sample boundary evidence.

## Shared Patterns

### Deterministic Validator Matrix

Source: `scripts/validate-skill-package.mjs` lines 2581-2583 and all `defineCheck(...)` entries.

Apply stable ordered checks. Add Hermes siblings inside existing route-family clusters, update `requiredCheckIds`, and adjust final exact summary totals after implementation. Avoid introducing package scripts, dependencies, or generated manifests.

### Route Count and Order

Source: `scripts/validate-skill-package.test.mjs` lines 1112-1123 and `scripts/validate-skill-package.mjs` route expectation helpers.

Normalize all stale eight-route assumptions before adding Hermes assertions. Any checks that currently derive from `rebrandRouteExpectations()`, `assertRebrandRouteTable()`, `ROUTE-REFS-001`, `REBRAND-CANON-004`, `REBRAND-ROUTE-001`, or `VAL-COMPAT-001` must see Hermes as the ninth route.

### Public Docs and README Variant Gate

Source: `scripts/validate-skill-package.mjs` lines 1614, 4591-4702, and 5453-5461.

Reuse `readmeVariantFiles()` and `assertIncludes()` over `README.md`, `readmes/README.*.md`, `examples/prompts.md`, `NOTICE.md`, `RELEASE_CHECKLIST.md`, `skills/visual-ip-illustrations/agents/openai.yaml`, `skills/visual-ip-illustrations/SKILL.md`, `routing.md`, and route-local Hermes references.

### Approval Parsing and Placeholder Dates

Source: `scripts/validate-skill-package.mjs` lines 759-864 and `scripts/validate-skill-package.test.mjs` lines 3303-3759.

Parsers return field booleans such as `reviewerPresent`, `datePresent`, `allowedDirectoriesPresent`, and route-specific outcome flags. Tests should mutate approval lines with `TBD`, `pending`, empty date, and placeholder outcome wording, then prove parser `complete=false` and gate failure.

### Leakage Scope

Source: `scripts/validate-skill-package.mjs` lines 5746-5850 and `scripts/validate-skill-package.test.mjs` lines 2958-3007.

Public docs may list all route inventory. Leakage scans target route-local packs and legacy shared Xiaohei references where Hermes identity would contaminate another route.

## No Analog Found

| File / Pattern | Role | Data Flow | Reason |
|----------------|------|-----------|--------|
| Hermes-specific mythology-drift and product-poster marker list | validator/test markers | batch scan | No prior route uses mythology/product-poster language. Implement by copying Cai Xukun uploaded-image/public-boundary pattern and substituting Hermes marker vocabulary from Phase 52 context. |
| Hermes uploaded attachment filename marker `Generated image 1 (16).jpeg` | validator marker | file-I/O / text scan | OpenClaw and Cai Xukun cover uploaded image authority, but Hermes is the first route that locks this exact uploaded conversation attachment marker. |

## Metadata

**Analog search scope:** `scripts/validate-skill-package.mjs`, `scripts/validate-skill-package.test.mjs`, Phase 42 and Phase 47 release evidence/context files, project skill index.
**Files scanned:** 9 required files plus targeted line ranges in 2 large scripts.
**Pattern extraction date:** 2026-06-18
