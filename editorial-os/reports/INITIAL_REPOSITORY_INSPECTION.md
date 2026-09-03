# Initial Repository Inspection

**Date:** 2026-09-03
**Scope:** Full repository inspection performed before any files were created or modified.
**Live content modified during inspection:** none.

---

## 1. Technology stack

A **zero-dependency Node.js static site generator**, referred to internally as "Blog OS". `platform/package.json` declares no dependencies at all — only four scripts (`build`, `build:force`, `check`, `serve`).

| Component | File | Purpose |
|---|---|---|
| Build + quality gate | `platform/src/build.js` | Renders content to `dist/`, runs a blocking quality GATE, generates sitemap, RSS, robots.txt, `_headers` (CSP), `ads.txt`, JSON-LD |
| Block renderer | `platform/src/blocks.js` | Converts typed content blocks to semantic HTML |
| Templates | `platform/src/templates.js` | Layout, head, nav, footer, design tokens, light/dark themes |
| Post-build verifier | `platform/src/check.js` | Broken links, image alt text, heading order, unique titles, WCAG AA contrast (computed for both themes), inline-JS budget |
| Design tokens | `platform/src/tokens.js` | Three-layer token system |
| Local server | `platform/src/serve.js` | Static preview |

Deployment is via **Cloudflare Workers static assets** (`platform/wrangler.jsonc`, worker name `certnorth`), triggered by a GitHub Action on push to `main`. The Action runs `build.js` and `check.js` **before** deploying, so a failing gate blocks release.

## 2. Where content lives

All content is **JSON**, not Markdown, MDX, a CMS, or a database.

```
platform/content/
├── site.json            # name, baseUrl, tagline, promise, editorialPolicyHtml, adsensePublisherId
├── authors.json         # single institutional author
├── taxonomy.json        # 4 pillars, 6 clusters
├── pages.json           # about, privacy-policy, contact
├── certifications.json  # single source of data for prices/requirements
└── articles/*.json      # 50 published articles
platform/parked-articles/ # 15 articles from a previous niche, excluded from the build
```

Article schema (enforced by the GATE): `id`, `slug`, `clusterId`, `title`, `dek`, `authorId`, `publishedAt`, `updatedAt`, `intent.primaryKeyword`, `seo.metaTitle` (≤60), `seo.metaDescription` (≤155), `sources[]`, `body[]` (typed blocks).

## 3. Content inventory

- **50 published articles**, 60 sitemap URLs, 61 built pages
- **15 parked articles** from a previous niche (cybersecurity/data/UX) — confirmed excluded from the build and absent from `dist/`
- **4 pillars:** Certifications, Career Paths, Salaries, Skills & Methods
- **6 clusters:** `cl_compare`, `cl_worth`, `cl_guides`, `cl_paths`, `cl_salary`, `cl_skills` — currently 8–9 articles each

## 4. Authorship

`authors.json` contains **one** author: `author_team` — "The CertNorth Team", type `Organization`, with an institutional bio. No personal names, no claimed individual credentials, no fabricated bylines. This is honest as far as it goes, but it means the site presents **no named human accountability** anywhere.

## 5. SEO and technical configuration

| Item | State |
|---|---|
| `robots.txt` | `Allow: /`, sitemap declared |
| `sitemap.xml` | 60 URLs, generated |
| Canonical URLs | Self-referencing on all 61 pages, verified |
| JSON-LD | `Article`, `FAQPage`, `BreadcrumbList`, `Organization`, `WebSite` |
| `inLanguage` | `en` on all 36 markup blocks |
| `<html lang>` | `en` |
| `ads.txt` | Present, correct publisher ID |
| CSP (`_headers`) | Relaxed to permit Google ad domains |
| Broken internal links | Zero |

## 6. Institutional pages

Present: **About**, **Privacy Policy**, **Contact**, **Editorial Policy**. All four are linked from the footer of every page (verified).

**Absent:** Terms of Use.

## 7. Findings that need action

These are stated here as observations. Detailed analysis is in the companion reports.

### 7.1 Severe structural uniformity

The strongest signal found. Measured across all 50 articles:

| Pattern | Frequency |
|---|---|
| Opens with a paragraph block | **50 / 50** |
| Second block is a callout | **50 / 50** |
| Contains an FAQ block | **50 / 50** |
| Contains a table | **49 / 50** |
| Title contains "2026" | 24 / 50 |

Repeated level-2 headings:

| Heading | Articles |
|---|---|
| "The case for it (real pros)" | 8 |
| "The case against it (real cons)" | 8 |
| "The honest bottom line" | 8 |
| "Head-to-head comparison" | 5 |
| "What the sources report" | 4 |

Every article on the site follows the same opening sequence and closes with an FAQ. Eight articles share an identical three-heading spine. This is the pattern of a template applied repeatedly, not of independent editorial decisions — and it is visible to a reader browsing two pages in a row.

### 7.2 Thin articles

**23 of 50 articles fall below 800 words** of body text, including several of the most commercially important pages:

| Article | Words |
|---|---|
| `pmp-cost` | 515 |
| `google-pm-certificate-worth-it` | 552 |
| `how-long-to-get-pmp` | 556 |
| `psm-vs-csm` | 563 |
| `pmp-vs-capm` | 586 |
| `is-pmp-worth-it` | 709 |
| `best-pm-certifications-beginners` | 681 |

Site average is 899 words. The newest articles run 1,200–1,500 words; the oldest run 500–700. The site is **inconsistent with itself**, which reads as declining or uneven standards depending on which page is sampled.

### 7.3 Unverifiable affiliate disclosure — highest-priority finding

The site states in **at least three places** that it earns affiliate commissions:

> "some links to courses and exam-prep tools earn us a commission at no cost to you" — `site.json`, editorial policy
> "Some links to courses and exam-prep tools earn us a commission at no extra cost to you" — About page
> Privacy Policy references affiliate links and disclosure

Measured reality: **zero affiliate links exist.** Article bodies contain **no external links at all** — every external URL on the site sits in a `sources` list pointing at PMI, Scrum.org, BLS and similar. There are no tracking parameters, no partner links, no affiliate programme of any kind.

The site therefore discloses a commercial relationship it does not have. See `DISCLOSURE_AUDIT.md`.

### 7.4 Orphaned articles

**9 of 50 articles have zero inbound internal links** — nothing on the site links to them:

`agile-coach-salary`, `does-pmp-increase-salary`, `how-to-become-pmo-analyst`, `is-pmi-acp-worth-it`, `is-pmi-membership-worth-it`, `is-prince2-worth-it`, `is-safe-certification-worth-it`, `program-manager-salary`, `what-are-story-points`

All nine are recent. New articles link outward to older ones, but older articles were never updated to link back. Average inbound links across the site is 4.6.

### 7.5 Content never revisited

**47 of 50 articles have `updatedAt` equal to `publishedAt`** — they have never been revised since publication. Only three have been genuinely updated. For a site whose editorial policy promises to re-verify volatile figures on a schedule, that promise is currently unevidenced.

### 7.6 Near-duplication risk

No two articles share a primary keyword (the GATE prevents that). But several pairs cover adjacent intent closely enough to warrant review during the content audit — in particular the `is-X-worth-it` set (9 articles) and the `X-vs-Y` set (8 articles), which overlap in both structure and substance.

## 8. Sources

- **160 source citations** across 50 articles
- **128 (80%) from primary or official bodies** — PMI, Scrum.org, Scrum Guides, Scrum Alliance, US BLS, IIBA, Scaled Agile, ICAgile, PeopleCert, ACM
- Remaining 20% are commercial salary aggregators (Glassdoor, Indeed, Salary.com, Built In, ZipRecruiter, PayScale), used for roles that have no official data — a limitation the articles generally state
- Zero non-HTTPS source URLs
- Zero articles with fewer than 2 sources

Source quality is the strongest dimension of the existing site.

## 9. Automation and tooling

- No content-generation scripts exist in the repository
- No test suite; `check.js` serves as the verification layer
- Build commands: `npm run build`, `npm run build:force`, `npm run check`
- `docs/` contains `content-plan.md`, `manual-do-blog.md` (a Portuguese operating manual for the Editor-in-Chief), and a handoff document

## 10. CLAUDE.md

**Did not exist.** Created as part of this installation. No pre-existing project instructions were overwritten.

---

## Summary judgment

The site's **evidence base is strong** (80% official sources, no broken links, honest institutional authorship, no fabricated data). Its weaknesses are **structural and editorial**, not factual:

1. Every page is built from the same template — the most visible problem
2. Nearly half the articles are materially thinner than the rest
3. A commercial disclosure describes a relationship that does not exist
4. Recent articles are orphaned; old articles are never revisited

None of these require inventing anything. All four are fixable with editorial work.
