---
status: complete
phase: 48-hermes-source-and-route-contract
source:
  - .planning/phases/48-hermes-source-and-route-contract/48-01-SUMMARY.md
started: 2026-06-18T10:45:00Z
updated: 2026-06-18T10:45:00Z
---

## Current Test

[testing complete]

## Tests

### 1. Select Hermes Agent Route
expected: Hermes Agent appears as an explicit route with aliases `Hermes Agent`, `Hermes`, `hermes`, `hermes-agent`, `Hermes logo`, and `Hermes Agent logo`.
result: pass

### 2. Preserve Default Route
expected: Xiaohei remains the only route with `default=true`, while Hermes uses `default=false`.
result: pass

### 3. Inspect Hermes Source Record
expected: Maintainer can inspect `references/ips/hermes/source.md` and see official Hermes Agent website, repository, MIT license URL, docs URL, uploaded attachment authority, public sample policy, review owner, and route status.
result: pass

### 4. Confirm Uploaded Image Markers
expected: Source record contains `Generated image 1 (16).jpeg` plus the fixed uploaded Hermes visual marker list.
result: pass

### 5. Confirm Output Path
expected: Routing metadata and source record expose `assets/<article-slug>-hermes/` as the Hermes output path.
result: pass

## Summary

total: 5
passed: 5
issues: 0
pending: 0
skipped: 0
blocked: 0

## Gaps

None.
