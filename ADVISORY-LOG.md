# Advisory log

Record of the npm security advisory triage board, pulled from GitHub's public security advisory database (npm ecosystem) as of 2026-10-21. Covers the first two critical-severity and first two high-severity advisories currently listed, plus an exposure check on the top critical advisory's affected package.

## Critical advisories

- **GHSA-f2ph-cmg5-wxc8** — package: storybook — severity: critical — CVSS: no CVSS published
- **GHSA-qx66-fv34-fjm8** — package: @tanstack/start-server-core — severity: critical — CVSS: 9.3

## High advisories

- **GHSA-86wm-68pq-5jwq** — package: @apostrophecms/import-export — severity: high — CVSS: 7.5
- **GHSA-gfr2-rv44-r23c** — package: markdown-it — severity: high — CVSS: 7.5

## Exposure check

- **Package searched on:** `storybook` (the affected package of the first critical advisory, GHSA-f2ph-cmg5-wxc8)
- **What the manifest search turned up:** A GitHub code search for public repositories whose `package.json` lists `storybook` as a dependency returned 136,704 results; refining to the exact `"storybook":` dependency-entry form returned 114,944 results, so real-world public exposure is widespread.
- **Repositories whose manifests were opened and confirmed:**
  - [epicmaxco/vuestic-admin](https://github.com/epicmaxco/vuestic-admin) — confirmed `"storybook": "^7.4.6"` in devDependencies
  - [trevoreyre/autocomplete](https://github.com/trevoreyre/autocomplete) — confirmed `"storybook": "^8.2.9"` in devDependencies, inside the advisory's vulnerable `>= 8.0.0, < 8.6.19` range
