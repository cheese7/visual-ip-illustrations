---
status: complete
phase: 53-linux-mascot-source-and-route-contract
source:
  - 53-01-SUMMARY.md
  - 53-VERIFICATION.md
started: 2026-06-30T19:25:46Z
updated: 2026-06-30T19:25:46Z
---

## Current Test

[testing complete]

## Tests

### 1. Explicit Linux Mascot Route Selection
expected: Linux Mascot aliases `Linux Mascot`, `Linux mascot`, `Linux`, `linux`, `Tux`, `tux`, `Linux penguin`, and `Tux penguin` select the `linux` route, while omitted visual-IP requests select Xiaohei.
result: pass
evidence: `routing.md:7` keeps omitted visual IP on `xiaohei`; `routing.md:20-21` lists the exact Linux Mascot aliases and alias boundary.

### 2. Linux Route Metadata Contract
expected: Route metadata exposes id `linux`, display name `Linux Mascot`, `default=false`, output suffix `linux`, status `source-reviewed`, source reference `references/ips/linux/source.md`, and output path `assets/<article-slug>-linux/`.
result: pass
evidence: `routing.md:59`, `routing.md:113-121`, `routing.md:170`, and route-table smoke output all matched the expected metadata.

### 3. Linux Source and Trademark Record
expected: The Linux source record exposes Larry Ewing Tux attribution, The GIMP attribution condition, Linux Foundation trademark guidance, Linux trademark ownership context, uploaded-image authority, public sample policy, review owner, route status, and source-image context.
result: pass
evidence: `source.md:18-30`, `source.md:34-38`, `source.md:55-72`, and `source.md:100-104` contain the required source and review contract.

### 4. Uploaded Image Authority and Marker Set
expected: `/Users/longnv/Downloads/Linux-logo.jpg`, SHA-256 `071bc327e4a2814864f9e2fcdea99aa50482a92ef4e816de9d9ce5f40e17bb2a`, and the full Linux Mascot visual marker list are visible.
result: pass
evidence: `source.md:34-51` contains the uploaded image path, file metadata, SHA-256, and fixed marker list.

### 5. Route Order and Default Preservation
expected: Xiaohei is the only `default=true` route; Linux Mascot appears after Hermes Agent with `default=false` and `source-reviewed`; existing explicit routes remain present.
result: pass
evidence: Node route-table smoke output matched `xiaohei:Xiaohei:true:illustrations:active` through `linux:Linux Mascot:false:linux:source-reviewed`.

### 6. Diff Hygiene and Phase Boundary
expected: Focused `rg` checks pass, `git diff --check` succeeds, and Phase 53 production scope stays limited to routing/source contract files.
result: pass
evidence: Focused route/source `rg` checks passed; `git diff --check` exited 0; verification confirmed no debt/stub markers in Phase 53 touched files.

## Summary

total: 6
passed: 6
issues: 0
pending: 0
skipped: 0
blocked: 0

## Gaps

[]
