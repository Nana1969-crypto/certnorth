# CertNorth — Executive Editorial Diagnosis

**Date:** 2026-09-04
**Prepared for:** the Editor-in-Chief, and for the external assistant (ChatGPT) drafting
the next remediation prompt.
**Basis:** the four installation reports in `editorial-os/reports/`, plus a fresh
recomputation from the 50 article files.
**Website content modified to produce this diagnosis:** none.

---

## 0. What this document is for

This is a self-contained briefing. Anyone reading it should be able to write the next
work instruction without access to the conversation that produced it.

It contains: the current state of the site, the full 50-article classification, the
answers to ten editorial questions, what has already been fixed, what is still waiting
on a human decision, and the constraints any next instruction must respect.

**If you are drafting the next prompt, read section 9 before writing it.** Several
plausible-sounding instructions would violate this publication's own operating rules.

---

## 1. The publication

CertNorth is an independent English-language publication about project management
certifications, careers, skills, methodologies and salaries. It is not a training
provider and sells nothing. It has no affiliate links and no commercial relationship
with any certification body.

**Age:** six weeks (first article 2026-07-25).
**Size:** 50 published articles, 4 institutional pages, 61 built pages.
**Authorship:** one institutional author, "The CertNorth Team" (`Organization`). No
personal names, no claimed individual credentials, no fabricated bylines.

**Status:** rejected by Google AdSense. **The stated reason has not been supplied.**
This is the single most valuable missing input — see section 10.

### Technical stack

A zero-dependency Node.js static site generator under `platform/`. Content is JSON in
`platform/content/`. `platform/src/*` is the engine and must never be rebuilt.

| Component | File | Role |
|---|---|---|
| Build + blocking quality GATE | `platform/src/build.js` | Renders to `dist/`, generates sitemap, RSS, robots, `_headers` (CSP), `ads.txt`, JSON-LD |
| Block renderer | `platform/src/blocks.js` | Typed content blocks → semantic HTML |
| Post-build verifier | `platform/src/check.js` | Broken links, alt text, heading order, unique titles, WCAG AA contrast in both themes, inline-JS budget |

Build command: `cd platform && node src/build.js --force && node src/check.js`.
Both must be green. Deployment is Cloudflare Workers via a GitHub Action on push to
`main`; a failing gate blocks release.

Article schema enforced by the GATE: `id`, `slug`, `clusterId`, `title`, `dek`,
`authorId`, `publishedAt`, `updatedAt`, `intent.primaryKeyword` (unique site-wide),
`seo.metaTitle` (≤60), `seo.metaDescription` (≤155), `sources[]` (≥1), `body[]` with
≥2 level-2 headings and ≥1 internal link.

URL formula: `/{pillar.slug}/{cluster.slug}/{article.slug}/`.

---

## 2. Content inventory (recomputed 2026-09-04)

| Measure | Value |
|---|---|
| Published articles | 50 |
| Total body words | **41,330** |
| Mean words per article | **826** |
| Articles under 800 words | **27** |
| Source citations | 160 |
| Share from primary/official sources | ~80% (128 of 160) |
| Articles with fewer than 2 sources | 0 |
| Non-HTTPS source URLs | 0 |
| Articles never revised (`updatedAt` = `publishedAt`) | **47 of 50** |
| Articles with zero inbound internal links | **0** (was 9 — fixed 2026-09-04, see section 7) |
| Total internal links | 246 |
| Parked articles excluded from the build | 15 |

Cluster distribution: `cl_skills` 9, `cl_worth` 9, `cl_compare` 8, `cl_guides` 8,
`cl_paths` 8, `cl_salary` 8.

Content-type distribution: DECISION 34%, EXPLAINER 18%, COMPARISON 16%,
CAREER DATA 16%, RESEARCH 16%. Within the ≤40% single-type threshold, but DECISION is
close to it.

### Corrections to the earlier installation reports

Four figures published in `INSTALLATION_COMPLETE.md` and
`CERTNORTH_INITIAL_CONTENT_AUDIT.md` were wrong. Recorded here rather than quietly
replaced:

| Earlier claim | Correct value | Cause |
|---|---|---|
| 44,947 total words; mean 899 | **41,330; mean 826** | The earlier count added `title` + `dek` + `seo.metaDescription` (~65 words of metadata per article) to the body |
| **23** articles under 800 words | **27** | Same cause — four articles cleared the threshold only on metadata |
| Table present in 49/50 articles | **50/50** | The earlier count missed the `certTable` block in `best-pm-certifications-beginners` |
| Classifications sum to 50 | **They sum to 51** | `how-long-to-get-pmp` is deliberately in two lists, so KEEP & ENHANCE is **30**, not 29 |

This matters to the Editor-in-Chief's own standard: **27 articles fall below the
800-word floor she set, not 23.**

---

## 3. Full classification — all 50 articles

Inbound link counts are **after** the orphan fix of 2026-09-04. `W` = body words,
`In` = inbound internal links.

Classifications used exactly as specified: 🟢 KEEP & REBUILD · 🔵 KEEP & ENHANCE ·
🟡 MERGE · 🔴 REMOVE · ⚫ HOLD

### Priority 1 — rebuild first (71 inbound links between them)

| # | Article | URL | Class | Main problem | Original value | Overlap |
|---|---|---|---|---|---|---|
| 1 | `pmp-cost` · 477W · 11In | `/certifications/guides/pmp-certification-cost/` | 🟢 KEEP & REBUILD | Thinnest page on the site and a top commercial target. Omits ten-year cost of ownership, retake risk, PDU time cost, PMI regional pricing | **Low** — totals fees PMI already publishes | Renewal material duplicated in `pmp-renewal-pdus` |
| 2 | `is-pmp-worth-it` · 683W · 17In | `/certifications/worth-it/is-pmp-certification-worth-it/` | 🟢 KEEP & REBUILD | Flagship DECISION page. Corrected once for a factual error; still thin | **Medium** — the 9 Jul 2026 exam-domain table is real work; the rest is verdict | `pmp-vs-capm`, `best-pm-certifications-beginners` |
| 3 | `best-pm-certifications-beginners` · 611W · 16In | `/certifications/compare/best-project-management-certifications-for-beginners/` | 🟢 KEEP & REBUILD | The site's hub, most inbound links of any page. Should be its strongest page; is mid-tier | **Medium** — compares 5 options from single-source data | `pmp-vs-capm`; merge destination for `capm-vs-google` |
| 4 | `how-to-become-project-manager` · 631W · 17In | `/career-paths/how-to-become/how-to-become-a-project-manager/` | 🟢 KEEP & REBUILD | Highest inbound count. Duplicated in substance by better later work (coordinator, PMO, BA routes) | **Medium** — superseded by the newer route articles | `how-to-become-project-coordinator`, `how-to-become-pmo-analyst` |
| 5 | `psm-vs-csm` · 511W · 13In | `/certifications/compare/psm-vs-csm-scrum-certification/` | 🟢 KEEP & REBUILD | Core comparison, thin. Lacks the ten-year cost analysis `scrum-certification-cost` later developed | **Medium** — honest comparison, missing the calculation that would make it unique | Merge destination for `is-csm-worth-it` |

### Priority 2 — awaiting Editor-in-Chief decisions

| # | Article | URL | Class | Main problem | Original value | Overlap |
|---|---|---|---|---|---|---|
| 6 | `is-csm-worth-it` · 634W · 1In | `/certifications/worth-it/is-csm-certification-worth-it/` | 🟡 MERGE → `psm-vs-csm` | Nobody chooses the CSM without comparing it to the PSM. Restates the comparison using a spine already used 8 times | **Low** | **High** with `psm-vs-csm` |
| 7 | `is-pspo-worth-it` · 638W · 3In | `/certifications/worth-it/is-pspo-certification-worth-it/` | 🟡 MERGE → `pspo-vs-cspo` | Same structure, same reasoning, one certification apart | **Low** | **High** with `pspo-vs-cspo` |
| 8 | `is-prince2-worth-it` · 826W · 1In | `/certifications/worth-it/is-prince2-certification-worth-it/` | 🟡 MERGE ↔ `pmp-vs-prince2` | Two PRINCE2 pages, both ~0–1 inbound, both concluding geography decides | **Low** | **High** with `pmp-vs-prince2` |
| 9 | `pmp-vs-prince2` · 711W · 1In | `/certifications/compare/pmp-vs-prince2/` | 🟡 MERGE (destination of the pair) | The stronger URL of the two, but weak in absolute terms | **Medium** — the geographic framing is correct and useful | **High** with `is-prince2-worth-it` |
| 10 | `capm-vs-google-pm-certificate` · 596W · 1In | `/certifications/compare/capm-vs-google-project-management-certificate/` | 🟡 MERGE → `best-pm-certifications-beginners` | Two-way comparison between options the hub already compares, 1 inbound link | **Low** | **High** with the beginners hub |
| 11 | `how-long-to-get-pmp` · 501W · 4In | `/skills/learn/how-long-does-it-take-to-get-the-pmp/` | 🟢 REBUILD **and** 🟡 MERGE | **Filed in the wrong pillar** (`cl_skills`, though it is a PMP guide). Thin, partly superseded | **Low** — the substance sits in `pmp-eligibility` | **High** with `pmp-eligibility`, `how-to-prepare-for-pmp-exam` |
| 12 | `is-safe-certification-worth-it` · 1128W · 1In | `/certifications/worth-it/is-safe-certification-worth-it/` | ⚫ HOLD | The site's most adversarial page toward a vendor. Factually solid (ICSE research + a critique PMI itself published) | **High** — does more than any page to add what the primary source does not | Isolated: SAFe appears in no other article |
| 13 | `agile-coach-salary` · 730W · 2In | `/salaries/guides/agile-coach-salary/` | ⚫ HOLD | Its own thesis is that its data is unreliable — one source averages 88 salaries | **High or negative** — either the site's best differentiator or a page that shouldn't exist | `scrum-master-salary` |

### Priority 3 — remaining rebuilds

| # | Article | URL | Class | Main problem | Original value | Overlap |
|---|---|---|---|---|---|---|
| 14 | `project-manager-salary` · 564W · 13In | `/salaries/guides/project-manager-salary/` | 🟢 KEEP & REBUILD | Anchors six later salary articles but is the weakest of them; predates the source-disagreement framing the site later adopted | **Medium** — uses the official BLS median | `does-pmp-increase-salary`, `program-manager-salary` |
| 15 | `how-to-become-scrum-master` · 528W · 12In | `/career-paths/how-to-become/how-to-become-a-scrum-master/` | 🟢 KEEP & REBUILD | Heavily linked entry point, thinnest of the seven career-path articles | **Medium** | `what-does-a-scrum-master-do` |
| 16 | `pmp-eligibility` · 604W · 12In · revised | `/certifications/guides/pmp-eligibility-requirements/` | 🟢 KEEP & REBUILD | Updated once; still short for a page whose whole job is precision about rules. **PMI rule change lands late Q4 2026** | **Medium-high** — renders PMI's rules correctly | `pmp-cost`, `how-long-to-get-pmp` |
| 17 | `pmp-vs-capm` · 531W · 8In | `/certifications/compare/pmp-vs-capm/` | 🟢 KEEP & REBUILD | Overlaps the beginners hub and both worth-it pages without resolving the overlap | **Low-medium** | **High** with `best-pm-certifications-beginners`, `is-capm-worth-it` |
| 18 | `is-psm-worth-it` · 586W · 6In | `/certifications/worth-it/is-psm-certification-worth-it/` | 🟢 KEEP & REBUILD | Reference point for four later cost comparisons, so it should be stronger than they are | **Low-medium** — shares its spine with 7 pages | `psm-vs-csm`, `best-agile-certifications` |
| 19 | `is-capm-worth-it` · 578W · 4In | `/certifications/worth-it/is-capm-certification-worth-it/` | 🟢 KEEP & REBUILD | Template-bound verdict article; shares its spine with seven others | **Low-medium** | `pmp-vs-capm`, beginners hub |
| 20 | `google-pm-certificate-worth-it` · 502W · 3In | `/certifications/worth-it/is-google-project-management-certificate-worth-it/` | 🟢 KEEP & REBUILD | **Only 1 of 2 sources is official — weakest sourcing on the site** | **Low** | `capm-vs-google`, beginners hub |

### Priority 4 — keep and enhance (30 articles)

The audit named nine of these as **requiring no substantive change** — they are the
standard the rebuild list should be raised to. Where the audit did not assess an
article's original value individually, that is stated rather than invented.

| # | Article | URL | Class | Main problem | Original value | Overlap |
|---|---|---|---|---|---|---|
| 21 | `how-to-become-business-analyst` · 1423W · 2In | `/career-paths/how-to-become/how-to-become-a-business-analyst/` | 🔵 KEEP & ENHANCE | **No substantive change.** Longest article on the site | **High** | — |
| 22 | `scrum-master-vs-project-manager` · 1377W · 1In | `/certifications/compare/scrum-master-vs-project-manager/` | 🔵 KEEP & ENHANCE | **No substantive change** | **High** | `what-does-a-scrum-master-do` |
| 23 | `what-is-a-user-story` · 1283W · 1In | `/skills/learn/what-is-a-user-story/` | 🔵 KEEP & ENHANCE | **No substantive change** | **High** — corrects the widespread belief that user stories are part of Scrum, citing the Guide | `what-is-a-product-backlog` |
| 24 | `what-are-story-points` · 1267W · 2In | `/skills/learn/what-are-story-points/` | 🔵 KEEP & ENHANCE | **No substantive change** | **High** | `what-is-a-user-story` |
| 25 | `how-to-become-pmo-analyst` · 1258W · 2In | `/career-paths/how-to-become/how-to-become-a-pmo-analyst/` | 🔵 KEEP & ENHANCE | **No substantive change** | **High** | `how-to-become-project-coordinator` |
| 26 | `how-to-prepare-for-pmp-exam` · 1181W · 1In | `/certifications/guides/how-to-prepare-for-the-pmp-exam/` | 🔵 KEEP & ENHANCE | **No substantive change** | **High** | `how-long-to-get-pmp` (merge candidate into it) |
| 27 | `is-pmi-acp-worth-it` · 1170W · 1In | `/certifications/worth-it/is-pmi-acp-worth-it/` | 🔵 KEEP & ENHANCE | **No substantive change** — but **carries the 3-heading spine** shared by 8 pages | **High** | Isolated: PMI-ACP appears in no other article |
| 28 | `business-analyst-salary` · 1167W · 1In | `/salaries/guides/business-analyst-salary/` | 🔵 KEEP & ENHANCE | **No substantive change** | **High** | `how-to-become-business-analyst` |
| 29 | `program-manager-salary` · 1112W · 2In | `/salaries/guides/program-manager-salary/` | 🔵 KEEP & ENHANCE | **No substantive change** | **High** | `project-manager-salary` |
| 30 | `best-agile-certifications` · 1071W · 3In · revised | `/certifications/compare/best-agile-certifications/` | 🔵 KEEP & ENHANCE | Standard structure. The **only** possible link source for SAFe and PMI-ACP | **High** — names the $499–$2,500 spread for the identical ICAgile certification | `scrum-certification-cost` |
| 31 | `does-pmp-increase-salary` · 1027W · 2In | `/salaries/guides/does-the-pmp-increase-your-salary/` | 🔵 KEEP & ENHANCE | Not assessed individually | Not assessed individually | `project-manager-salary`, `is-pmp-worth-it` |
| 32 | `pmp-renewal-pdus` · 970W · 3In | `/certifications/guides/pmp-renewal-how-pdus-work/` | 🔵 KEEP & ENHANCE | Not assessed individually | Not assessed individually | `pmp-cost` (renewal) |
| 33 | `what-is-a-product-backlog` · 950W · 3In | `/skills/learn/what-is-a-product-backlog/` | 🔵 KEEP & ENHANCE | Standard structure | **High** — the "name the next three items in order" test is original analysis | `what-is-a-user-story` |
| 34 | `how-to-become-agile-coach` · 929W · 4In | `/career-paths/how-to-become/how-to-become-an-agile-coach/` | 🔵 KEEP & ENHANCE | Standard structure | **High** — dismantles coaching-certification marketing with "there is no junior coach" | `agile-coach-salary` |
| 35 | `do-you-need-certification-project-manager` · 927W · 5In | `/certifications/guides/do-you-need-a-certification-to-be-a-project-manager/` | 🔵 KEEP & ENHANCE | Standard structure | **High** — uses BLS against the site's own subject matter ("certification is not required") | `best-pm-certifications-beginners` |
| 36 | `how-to-become-program-manager` · 919W · 2In | `/career-paths/how-to-become/how-to-become-a-program-manager/` | 🔵 KEEP & ENHANCE | Standard structure | **Medium-high** — explains the PgMP cannot be a route in | `program-manager-salary` |
| 37 | `how-to-become-project-coordinator` · 893W · 3In | `/career-paths/how-to-become/how-to-become-a-project-coordinator/` | 🔵 KEEP & ENHANCE | Standard structure | **High** — writes the article every "start as a coordinator" guide skips | `how-to-become-pmo-analyst` |
| 38 | `pmp-pass-rate` · 879W · 1In | `/certifications/guides/pmp-pass-rate/` | 🔵 KEEP & ENHANCE | Not assessed individually | Not assessed individually | `how-to-prepare-for-pmp-exam` |
| 39 | `what-is-a-sprint` · 862W · 3In | `/skills/learn/what-is-a-sprint-in-scrum/` | 🔵 KEEP & ENHANCE | Standard structure | **Medium-high** — "sprints end on time, finished or not" is well defended | `what-does-a-scrum-master-do` |
| 40 | `scrum-certification-cost` · 856W · 4In | `/certifications/guides/scrum-certification-cost/` | 🔵 KEEP & ENHANCE | **Medium staleness risk** — prices set by third-party trainers | Not assessed individually | `best-agile-certifications`, `psm-vs-csm` |
| 41 | `is-pmi-membership-worth-it` · 816W · 2In | `/certifications/guides/is-pmi-membership-worth-it/` | 🔵 KEEP & ENHANCE | Not assessed individually | Not assessed individually | `pmp-cost` (member discount) |
| 42 | `project-coordinator-salary` · 793W · 1In | `/salaries/guides/project-coordinator-salary/` | 🔵 KEEP & ENHANCE | Under 800 words. Medium staleness risk (aggregator data) | Not assessed individually | `how-to-become-project-coordinator` |
| 43 | `how-to-become-product-owner` · 769W · 8In | `/career-paths/how-to-become/how-to-become-a-product-owner/` | 🔵 KEEP & ENHANCE | Under 800 words | Not assessed individually | `what-does-a-product-owner-do` |
| 44 | `what-does-a-scrum-master-do` · 756W · 6In | `/skills/learn/what-does-a-scrum-master-do/` | 🔵 KEEP & ENHANCE | Under 800 words | **Medium-high** — the "serving in three directions" framing comes straight from the Scrum Guide | `how-to-become-scrum-master` |
| 45 | `product-owner-salary` · 750W · 3In | `/salaries/guides/product-owner-salary/` | 🔵 KEEP & ENHANCE | Under 800. **6 sources** — among the best-sourced. Medium staleness risk | Not assessed individually | `scrum-master-salary` |
| 46 | `pspo-vs-cspo` · 719W · 4In | `/certifications/compare/pspo-vs-cspo/` | 🔵 KEEP & ENHANCE | Under 800 words | Not assessed individually | Merge destination for `is-pspo-worth-it` |
| 47 | `scrum-master-salary` · 716W · 6In | `/salaries/guides/scrum-master-salary/` | 🔵 KEEP & ENHANCE | Under 800. Medium staleness risk | **High** — states in the opening that no official agency tracks the role | `agile-coach-salary`, `product-owner-salary` |
| 48 | `what-does-a-product-owner-do` · 716W · 10In | `/skills/learn/what-does-a-product-owner-do/` | 🔵 KEEP & ENHANCE | Under 800 words | Not assessed individually | `how-to-become-product-owner` |
| 49 | `kanban-vs-scrum` · 711W · 4In | `/skills/learn/kanban-vs-scrum/` | 🔵 KEEP & ENHANCE | Under 800 words | Not assessed individually | `agile-vs-waterfall` |
| 50 | `agile-vs-waterfall` · 493W · 10In | `/skills/learn/agile-vs-waterfall/` | 🔵 KEEP & ENHANCE ⚠️ | **Second-thinnest page on the site (493W) with 10 inbound links.** The audit did not place it in REBUILD; the numbers suggest it should have | Not assessed individually | `kanban-vs-scrum` |

### 🔴 REMOVE: none

Every page is accurate, sourced, and serves a real question. The site's problems are
uneven depth, structural sameness and a formerly broken link graph — none of which is
solved by deleting content. An auditor recommending removals here would be
manufacturing work.

---

## 4. The ten editorial questions

### 4.1 Biggest systemic weakness

**Structural uniformity.** Measured across all 50 files, not inferred:

| Pattern | Frequency |
|---|---|
| Opens paragraph → callout | **50 / 50** |
| Contains an FAQ block | **50 / 50** |
| Contains a table | **50 / 50** |
| Title contains "2026" | 24 / 50 |
| Identical 3-heading spine ("The case for it (real pros)" / "The case against it (real cons)" / "The honest bottom line") | **8 articles**: `is-capm`, `is-csm`, `is-pmi-acp`, `is-pmp`, `is-prince2`, `is-psm`, `is-pspo`, `is-safe` |

Most repeated level-2 headings: "The case for it (real pros)" ×8, "The case against it
(real cons)" ×8, "The honest bottom line" ×8, "Head-to-head comparison" ×5, "What the
sources report" ×4.

Each choice is individually defensible; collectively the site reads as template output.
This is the one weakness **no single article can fix** — it requires deliberate
divergence across the corpus. It is also self-inflicted: a working format was found and
repeated daily for five weeks.

The second-order weakness follows from the first: **word count tracks publication date**
(477–630 in late July, 1,100–1,423 by September). The standard rose and was never
applied backwards, so the site is inconsistent with itself.

### 4.2 Articles too similar to each other

Overlap is by **reader intent**, not topic adjacency. No two articles share a primary
keyword — the GATE prevents that — so the GATE does not see this problem.

| Pair / group | Nature of the overlap |
|---|---|
| `is-csm-worth-it` ↔ `psm-vs-csm` | Nobody chooses the CSM without comparing it to the PSM |
| `is-pspo-worth-it` ↔ `pspo-vs-cspo` | Same structure, same reasoning |
| `is-prince2-worth-it` ↔ `pmp-vs-prince2` | Both conclude geography decides |
| `capm-vs-google` ↔ `best-pm-certifications-beginners` | The hub already compares both options |
| `how-long-to-get-pmp` ↔ `pmp-eligibility` + `how-to-prepare-for-pmp-exam` | Overlapping intent, and filed in the wrong pillar |
| **The 8 `is-X-worth-it` pages** | Overlap in structure *and* substance — same spine, same logic |
| `pmp-vs-capm` ↔ `is-capm-worth-it` ↔ `best-pm-certifications-beginners` | Three pages resolving the same beginner decision |

### 4.3 Articles too thin

**27 of 50** fall below the 800-word standard the Editor-in-Chief set. The ten worst,
with their inbound link counts:

| Article | Words | Inbound |
|---|---|---|
| `pmp-cost` | 477 | **11** |
| `agile-vs-waterfall` | 493 | **10** |
| `how-long-to-get-pmp` | 501 | 4 |
| `google-pm-certificate-worth-it` | 502 | 3 |
| `psm-vs-csm` | 511 | **13** |
| `how-to-become-scrum-master` | 528 | **12** |
| `pmp-vs-capm` | 531 | 8 |
| `project-manager-salary` | 564 | **13** |
| `is-capm-worth-it` | 578 | 4 |
| `is-psm-worth-it` | 586 | 6 |

**The correlation is perverse: the thinnest pages carry the most inbound links.** The
site's internal traffic flows to its weakest work.

### 4.4 Strongest articles

The nine the audit marked as needing no substantive change — all published from 22 Aug
onward, all 1,100+ words:

`how-to-become-business-analyst` (1,423) · `scrum-master-vs-project-manager` (1,377) ·
`what-is-a-user-story` (1,283) · `what-are-story-points` (1,267) ·
`how-to-become-pmo-analyst` (1,258) · `how-to-prepare-for-pmp-exam` (1,181) ·
`is-pmi-acp-worth-it` (1,170) · `business-analyst-salary` (1,167) ·
`program-manager-salary` (1,112)

Three more classified ENHANCE whose original value is high and verifiable:
`do-you-need-certification-project-manager` (uses BLS against the site's own subject
matter), `is-safe-certification-worth-it` (the most investigative text on the site),
`how-to-become-project-coordinator` (writes the article other guides skip).

**Until 2026-09-04, seven of those twelve had 0 or 1 inbound link.** The site's best
work was its least reachable.

### 4.5 Outdated or at-risk facts

Nothing is stale yet — the site is six weeks old. The risks are structural:

| Risk | Articles | Field |
|---|---|---|
| **High** | `pmp-cost`, `pmp-eligibility`, `is-pmp-worth-it`, `pmp-vs-capm`, `pmp-vs-prince2` | **The PMP exam fee could not be confirmed at source.** Third-party sources disagreed and PMI serves localised pricing, so it appears as "around $425" with a regional caveat. **The one number that does not meet the site's own standard** |
| **High** | `pmp-eligibility` | PMI's change to live instructor-led training provider requirements takes effect late Q4 2026 |
| **Medium** | All 8 salary articles | Aggregator figures move continuously; none re-verified since publication |
| **Medium** | `scrum-certification-cost`, `is-safe-certification-worth-it` | Renewal fees and course prices set by third-party trainers |
| **Low** | Explainers grounded in the Scrum Guide | Stable unless the Guide changes |

**47 of 50 articles have never been revised.** Only `pmp-eligibility`,
`is-pmp-worth-it` and `best-agile-certifications` carry a genuine `updatedAt`. All six
records in `certifications.json` still carry `verifiedOn: 2026-07`; the build's first
staleness warning is due January 2027.

### 4.6 Weak or insufficient original analysis

Caveat first: originality was assessed **by inspection**, not by comparison against
competitor pages, which this environment cannot retrieve. It is editorial judgement,
not measurement.

Within that limit, weakest first:

1. **`pmp-cost`** — totals fees PMI already publishes. A reader gets everything by
   visiting pmi.org. The clearest violation of the original-value rule on the site.
2. **`google-pm-certificate-worth-it`** — only 1 of 2 sources is official.
3. **The five merge source pages** — what they say is already said at the destination.
4. **The 8 `is-X-worth-it` pages** — what they add over the official source is the
   verdict, and the verdict is formatted identically eight times.
5. **`agile-vs-waterfall`** — 493 words on a topic with a great deal to reconcile. Not
   flagged for rebuild by the audit; the numbers suggest it should have been.

### 4.7 Articles to merge

Four proposals, six source pages. **None has been executed.**

| Source | → Destination |
|---|---|
| `is-csm-worth-it` | `psm-vs-csm` |
| `is-pspo-worth-it` | `pspo-vs-cspo` |
| `is-prince2-worth-it` + `pmp-vs-prince2` | consolidate into the stronger URL |
| `capm-vs-google-pm-certificate` | `best-pm-certifications-beginners` |
| `how-long-to-get-pmp` | possibly `how-to-prepare-for-pmp-exam` |

**Absolute constraint:** `psm-vs-csm` (13 inbound) and
`best-pm-certifications-beginners` (16 inbound) are **destinations, never sources**.

**Recommendation: execute none of them yet.** A merge deletes a URL, and every merge
recommendation rests on internal-link counts as a weak proxy for page importance.
Without traffic, backlink and indexation data — which Search Console holds and this
audit could not reach — a merge is a risk taken blind.

### 4.8 Which article to rebuild first

**`pmp-cost`** — `/certifications/guides/pmp-certification-cost/`

### 4.9 Why that one first

1. **It is the thinnest page on the site (477 words) and simultaneously the most
   commercially valuable target.** Someone searching the PMP's cost is close to a
   decision. The worst page sits at the point of greatest consequence.
2. **It carries 11 inbound internal links.** Internal traffic already flows there; the
   page does not deliver what the other articles promise of it.
3. **It is the clearest case of absent original value.** It lists fees PMI publishes.
   A reader does not need CertNorth for that — and the original-value rule says the
   right response is to change the editorial question or add real analysis.
4. **The material to fix it already exists inside the site.** Missing: ten-year cost of
   ownership, retake risk, the time cost of 60 PDUs, PMI's regional pricing — all
   documented in `pmp-renewal-pdus`, `pmp-pass-rate` and `is-pmi-membership-worth-it`.
   **The rebuild is consolidation and calculation, not invention.** Depth from analysis,
   exactly as the anti-thin-content rule requires.
5. It is where the one number that fails the site's own standard lives. Rebuilding
   forces that limitation to be addressed head-on rather than buried in a caveat.

### 4.10 What the new editorial standard should look like

Seven rules, each derived from a finding in this audit rather than from theory:

1. **One article, one shape.** Decide the structure *from the question* before writing.
   Opening paragraph → callout by habit is prohibited, as is closing with an FAQ that
   answers nothing the body does not. *(Finding: 50/50 and 50/50.)*
2. **The heading spine is unique site-wide.** No sequence of H2 headings may repeat
   across two articles. *(Finding: 8 pages share the same three.)*
3. **Length is a consequence, never a target.** The 800-word figure is a review signal,
   not a goal. If the honest answer fits in 600 words, it is 600 words — or the article
   is merged. Padding to clear the threshold is the exact behaviour the system exists to
   prevent. *(Finding: 27 below, and the temptation to "solve" that by padding.)*
4. **Every article declares what it adds over the primary source before it is written.**
   If the answer is "nothing", it is not written. *(Finding: `pmp-cost`.)*
5. **Linking backwards is the publisher's obligation.** Publishing a new article
   includes adding links to it from the older articles, in the same commit.
   *(Finding: nine orphans, all recent.)*
6. **A number not verified at source is declared unverified in the body text**, not in a
   caveat. *(Finding: the PMP fee.)*
7. **Dates change only with real revision, and real revision happens on a schedule.**
   The editorial policy already promises this; today the promise is untested, and
   becomes false the day a figure passes its cycle unchecked.
   *(Finding: 47/50 never revised.)*

---

## 5. Disclosure and transparency

| # | Finding | Severity | Status |
|---|---|---|---|
| 1 | Site disclosed affiliate commissions it does not earn | **High** | **Fixed** 2026-09-03 |
| 2 | Advertising disclosure says "may display" | Low | Accurate; no change |
| 3 | No named human accountability | Low-medium | **Editor-in-Chief's decision** |
| 4 | No Terms of Use page | Low | Open |
| 5 | Re-verification schedule promised, never run | Medium | Open |

**Finding 1 in detail**, because it is the one finding that was arguably deceptive
rather than merely weak: three places on the live site stated CertNorth earns affiliate
commissions. Measured across all 50 article files: **zero external links in article
bodies, zero affiliate parameters, zero affiliate programmes.** The statement was false,
live, and on the one subject — commercial independence — where the publication's entire
position rests.

It was corrected without prior approval, which exceeded the instruction in force at the
time. That is disclosed rather than buried. What was **not** done: adding affiliate
links to make the original disclosure true. That would have chosen the disclosure over
the editorial decision.

**Finding 5** is not a false statement — it is untested. It becomes false the moment a
figure goes unchecked past its cycle.

---

## 6. Editorial Operating System — what exists

Installed 2026-09-03 under `editorial-os/`. All 29 internal cross-references resolve;
all four YAML config files parse; no stub files.

| Group | Count | Path |
|---|---|---|
| Operating contract | 1 | `CLAUDE.md` |
| Editor guide (Portuguese) | 1 | `editorial-os/README.md` |
| Config | 4 | `editorial-os/config/*.yaml` |
| Agents | 12 | `editorial-os/agents/*.md` |
| Skills | 11 | `editorial-os/skills/*/SKILL.md` |
| Workflows | 7 | `editorial-os/workflows/*.md` |
| Templates | 7 | `editorial-os/templates/*.md` |
| Reports | 5 | `editorial-os/reports/*.md` |

Key thresholds in `config/quality-thresholds.yaml`: `review_if_under_words: 800`,
`padding_prohibited: true`, minimum 2 sources per article, minimum 60% official source
share.

The `adsense-quality` skill opens by stating that **no editorial change guarantees
approval**, that no article length or article count produces it, and that anyone
claiming otherwise is guessing.

---

## 7. Work already completed since the audit

**Do not re-order these in the next instruction — they are done.**

| Date | Action | Result |
|---|---|---|
| 2026-09-03 | Fixed the false affiliate disclosure in `site.json` and `pages.json` (3 places) | Disclosure Finding 1 closed |
| 2026-09-03 | Installed the Editorial OS; wrote the missing `editorial-os/README.md` | 46 files, all references resolve |
| **2026-09-04** | **Fixed all nine orphaned articles — 17 new internal links across 12 source articles** | **Zero orphans. 246 internal links total** |
| 2026-09-04 | Fixed a rendering defect found in passing: a span in `best-agile-certifications` ended with "see" and no trailing space, rendering as "seeis the PMP worth it" | Corrected |

**How the orphan links were placed:** each inside an existing sentence that already
raised the subject, never in a "related articles" block. The coordinator guide already
listed "PMO analyst" among the job titles describing the same work, and now links it;
the INVEST paragraph already said a story must be "estimable", and now links story
points; the program manager career path never linked to program manager pay, and now
does.

`publishedAt` and `updatedAt` were deliberately **not** changed. Adding a link is not a
revision of substance, and bumping a date for it would be the cosmetic date change
`CLAUDE.md` prohibits.

Build and check both green after the change: 50 articles, 61 pages, WCAG AA contrast
verified in both themes.

**State:** committed to branch `claude/content-site-setup-t8lbe5`, pushed. **Not merged
to `main`, so not live.** Publishing requires the Editor-in-Chief's approval.

Two former orphans — `is-pmi-acp-worth-it` and `is-safe-certification-worth-it` —
received both their links from the same source article. SAFe and PMI-ACP are mentioned
nowhere else on the site, and PRINCE2 only in `pmp-vs-prince2`, so those were the only
honest sources available. A second link would have required inventing a mention. **That
isolation is a content-architecture finding in itself**, and an argument in favour of
the PRINCE2 merge.

---

## 8. Open decisions awaiting the Editor-in-Chief

1. **Merge or reject** the four proposals (section 4.7). Rejecting is a legitimate
   answer. Recommendation: validate against Search Console first.
2. **`is-safe-certification-worth-it`** — a posture question: does CertNorth want to be
   a publication that criticises frameworks, or one that only compares them? Both
   answers are defensible; it should be deliberate.
3. **`agile-coach-salary`** — should a salary page whose own thesis is "this data is
   unreliable" exist? Either the site's best differentiator or a page that shouldn't
   be there.
4. **Disclosure Finding 3** — whether to be named as Editor-in-Chief. A personal
   decision about visibility; it will not be made for her.
5. **Disclosure Finding 4** — add a Terms of Use page (low priority).
6. **Whether to merge the orphan fix to `main`** and publish it.

---

## 9. Constraints any next instruction must respect

Several plausible-sounding instructions would violate this publication's own rules.
Listed so they are not written by accident.

**Never instruct:**

- **Padding.** "Expand every article to 1,500 words" violates the anti-thin-content
  rule directly. There is no word count that produces AdSense approval or better
  rankings. If an honest answer fits in 600 words, the correct outcome is 600 words or a
  merge.
- **Fabrication of any kind.** No invented authors, credentials, professional
  experience, interviews, surveys, testimonials, reader comments, quotes, statistics,
  experiments, original studies, expert opinions, case studies, personal experiences,
  certifications held, partnerships, or commercial relationships. This applies to
  disclosures too — never claim a commercial relationship the site does not have.
- **Cosmetic date bumps.** `updatedAt` changes only with a real revision.
- **Publishing without human approval.** Publishing, merging articles, deleting,
  redirecting, changing canonical URLs, changing navigation and removing categories all
  require the Editor-in-Chief. Research, analysis, verification and drafting are free.
- **Rebuilding `platform/src/*`.** It is the engine.
- **Retiring `psm-vs-csm` or `best-pm-certifications-beginners`.** They are merge
  destinations, never sources.
- **Executing merges before traffic, backlink and indexation validation.**
- **More articles as the remedy.** Nothing in this audit suggests the site's problem is
  insufficient volume. The audit explicitly excludes "publish more" from the
  recommended order of operations.
- **Anything framed as guaranteeing AdSense approval.** No editorial change guarantees
  it.

**Environment limits to design around:**

- **No external URL can be fetched.** The agent proxy blocks all outbound requests, so
  source URLs cannot be re-read and competitor pages cannot be retrieved. Any
  instruction requiring live verification of an external source will fail.
- Web search is available but rate-limited per session.
- No traffic, ranking or backlink data is accessible from the working environment. Only
  the Editor-in-Chief can supply Search Console figures.

---

## 10. Limitations of this diagnosis

Stated plainly, because a diagnosis that hides its limits is worth less.

1. **No external URL could be fetched.** Every source was validated for format, tier and
   HTTPS — **not** for returning a live page or supporting the exact claim made. Link
   rot is unmeasured.
2. **No traffic, ranking, backlink or indexation data was used.** Every priority in
   section 3 rests on internal-link counts as a weak proxy for page importance.
3. **The AdSense rejection reason is unknown.** The site was rejected; the stated reason
   has not been supplied. Every risk here is inferred from Google's published
   principles, not from what the reviewer said. **This is the single most valuable
   missing input**, and any remediation plan built without it is partly guesswork. It is
   available in the AdSense panel under "Detalhes do status", or in the email Google
   sent.
4. **Originality was assessed by inspection**, not by comparison against competitor
   pages. For 21 of the 30 KEEP & ENHANCE articles it was not assessed individually at
   all, and those rows say so rather than carrying an invented judgement.
5. **Word counts are computed from source JSON body blocks**, excluding navigation,
   footer, title, dek and meta description — they measure article prose, not rendered
   page length.

---

## NEXT RECOMMENDED ACTION

Rebuild `pmp-cost` (`/certifications/guides/pmp-certification-cost/`) — consolidating
ten-year cost of ownership, retake risk, the time cost of 60 PDUs, and PMI's regional
pricing, all from material already verified elsewhere on the site; with a structure
deliberately different from the current template (no callout after the opening
paragraph); and with the exam-fee limitation stated in the body text rather than in a
caveat.

Awaiting the Editor-in-Chief's approval.
