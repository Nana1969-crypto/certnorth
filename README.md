# blogcareer — Blog OS engine (Careers, Skills & Certifications)

This repository is a fresh copy of the **Blog OS** static content engine, ready
to build site #2 in the **Careers, Skills & Certifications** niche (English).

It contains the engine only — **no articles yet**.

## What's here

- `platform/src/*` — the engine (build with quality gate, block renderer,
  templates, post-build checks). **Do not rebuild this.**
- `platform/wrangler.jsonc` — Cloudflare deploy config (`name: "blogcareer"`).
- `.github/workflows/deploy.yml` — auto-deploy on push to `main`
  (needs repo secrets `CLOUDFLARE_API_TOKEN` + `CLOUDFLARE_ACCOUNT_ID`).
- `platform/content/{site,taxonomy,authors,pages}.json` — **Sheetlift templates,
  kept only as schema reference. Overwrite them for the Careers site.**
- `platform/content/articles/` — empty. The new session creates the articles here.
- `docs/handoff-careers-site.md` — the build prompt.

## How to start

1. Open a **new session** on this repository.
2. Paste the contents of `docs/handoff-careers-site.md` (from "You are…").
3. Add the two repo secrets in GitHub (Settings → Secrets and variables →
   Actions): `CLOUDFLARE_API_TOKEN` (the same account-wide token as Sheetlift)
   and `CLOUDFLARE_ACCOUNT_ID`.

## Build locally

```
node platform/src/build.js --force && node platform/src/check.js
```
