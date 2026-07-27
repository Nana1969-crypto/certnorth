# CertNorth — project management certifications, decoded

CertNorth is an English-language content site covering **project management
certifications and careers** — honest, officially-sourced guides (real exam
costs, real requirements, honest "is it worth it" verdicts, and salary data
from official labour-market sources). Built on the **Blog OS** static engine.

## What's here

- `platform/src/*` — the engine: build with a blocking quality gate, typed
  block renderer, tokens-driven templates (light/dark, WCAG AA validated),
  and post-build checks. **Do not rebuild this.**
- `platform/content/{site,taxonomy,authors,pages}.json` — the site config.
- `platform/content/articles/*.json` — the published articles.
- `platform/parked-articles/*.json` — earlier drafts kept out of the build.
- `platform/wrangler.jsonc` — Cloudflare deploy config (`name: "certnorth"`).
- `.github/workflows/deploy.yml` — auto-deploy on push to `main` (needs repo
  secrets `CLOUDFLARE_API_TOKEN` + `CLOUDFLARE_ACCOUNT_ID`).

## Build locally

```
node platform/src/build.js --force && node platform/src/check.js
```

The gate blocks the build on quality violations (cannibalization, over-length
meta, missing sources, weak structure); `check.js` verifies the output
(broken links, alt text, heading order, unique titles, AA contrast in both
themes, inline-JS budget).

## Deploy

Push to `main` and the GitHub Action builds, runs the gate + checks, and
deploys to Cloudflare Workers via `npx wrangler@4 deploy`. Configure the two
repo secrets first (Settings → Secrets and variables → Actions).
