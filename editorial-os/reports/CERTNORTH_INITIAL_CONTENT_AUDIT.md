# CertNorth Initial Content Audit

**Date:** 2026-09-03
**Articles audited:** 50 (all published articles)
**Live content modified:** none
**Articles deleted, merged, redirected or rewritten:** none

---

## Summary of recommendations

| Action | Count |
|---|---|
| 🟢 KEEP & REBUILD | 13 |
| 🔵 KEEP & ENHANCE | 29 |
| 🟡 MERGE | 6 |
| 🔴 REMOVE | **0** |
| ⚫ HOLD | 2 |

**No article is recommended for removal.** Every page is accurate, sourced, and
serves a real question. The site's problems are uneven depth, structural sameness,
a broken internal link graph and one false disclosure — none of which is solved by
deleting content. An auditor that recommended removals here would be manufacturing
work.

---

## The finding that explains most of the others

Word count correlates almost perfectly with publication date.

| Published | Typical length |
|---|---|
| 25–31 July | 515–790 words |
| 1–15 August | 780–1,050 words |
| 16 August – 2 September | 890–1,522 words |

The editorial standard rose steadily over five weeks and was never applied backwards.
The result is a site that is **inconsistent with itself**: a reader landing on
`pmp-cost` (515 words) and a reader landing on `how-to-become-business-analyst`
(1,522 words) encounter two different publications.

The internal link graph shows the mirror image of the same problem. New articles link
back to old ones; nobody returned to link forward.

| Published | Typical inbound links |
|---|---|
| July | 8–17 |
| Late August – September | 0–3 |

**Nine articles have zero inbound links.** All nine are recent, and several are the
strongest work on the site.

---

## Site-wide patterns

### Structural uniformity — highest-severity pattern

| Pattern | Frequency |
|---|---|
| Opens paragraph → callout | **50 / 50** |
| Contains an FAQ block | **50 / 50** |
| Contains a table | **49 / 50** |
| Title contains "2026" | 24 / 50 |

Shared level-2 heading spines:

| Heading | Articles |
|---|---|
| "The case for it (real pros)" | 8 |
| "The case against it (real cons)" | 8 |
| "The honest bottom line" | 8 |
| "Head-to-head comparison" | 5 |
| "What the sources report" | 4 |

Eight articles share an identical three-heading spine. Every article on the site
opens with the same two-block sequence and closes with an FAQ. Individually each is
defensible; collectively the site reads as template output. This is the single most
visible quality signal against the site and it is not fixable article by article — it
requires deliberate divergence across the corpus.

### Content-type imbalance

| Type | Articles | Share |
|---|---|---|
| DECISION ("is X worth it", "should I") | 17 | 34% |
| COMPARISON ("X vs Y") | 8 | 16% |
| CAREER DATA (salary) | 8 | 16% |
| EXPLAINER ("what is X") | 9 | 18% |
| RESEARCH | 8 | 16% |

Within threshold (≤40% single type), but DECISION is close to the limit and the nine
`is-X-worth-it` articles are the most template-bound group on the site.

### Sources — the site's strongest dimension

- 160 citations across 50 articles; **128 (80%) primary or official**
- Zero non-HTTPS URLs; zero articles with fewer than two sources
- Salary articles necessarily lean on commercial aggregators, and generally label
  them as self-reported

### Freshness

**47 of 50 articles have never been revised.** Only `pmp-eligibility`,
`is-pmp-worth-it` and `best-agile-certifications` carry a genuine `updatedAt`. The
editorial policy promises scheduled re-verification of volatile figures; that promise
is currently unevidenced.

---

## 🟢 KEEP & REBUILD (13)

Right topic, high value, execution below current standard. These carry the most
inbound links on the site, so they are also the highest-leverage fixes.

| Article | Words | In | Rationale | Confidence |
|---|---|---|---|---|
| `pmp-cost` | 515 | 11 | Thinnest page on the site and a top commercial target. Omits ten-year cost of ownership, retake risk, PDU time cost and PMI's regional pricing — all of which the site now documents elsewhere | high |
| `is-pmp-worth-it` | 709 | 17 | Flagship DECISION page. Already corrected once for a factual error; still thin relative to the material available | high |
| `best-pm-certifications-beginners` | 681 | 16 | The site's hub, with the most inbound links. Should be its strongest page and is currently mid-tier | high |
| `how-to-become-project-manager` | 689 | 17 | Highest inbound count. Now duplicated in substance by better later work on coordinator, PMO and BA routes without linking to it | high |
| `psm-vs-csm` | 563 | 13 | Core comparison, thin. Lacks the ten-year cost analysis the later `scrum-certification-cost` article developed | high |
| `project-manager-salary` | 600 | 13 | Anchors six later salary articles but is the weakest of them; predates the source-disagreement framing the site later adopted | high |
| `how-to-become-scrum-master` | 588 | 12 | Heavily linked entry point, thinnest of the seven career-path articles | high |
| `pmp-eligibility` | 662 | 12 | Was updated once; still short for a page whose whole job is precision about rules | medium |
| `pmp-vs-capm` | 586 | 8 | Core comparison; overlaps `best-pm-certifications-beginners` and both worth-it pages without resolving the overlap | medium |
| `how-long-to-get-pmp` | 556 | 4 | Misfiled in `cl_skills` when it is a PMP guide. Thin, and superseded in part by `how-to-prepare-for-pmp-exam` | high |
| `is-capm-worth-it` | 635 | 4 | Template-bound verdict article; shares its spine with seven others | medium |
| `is-psm-worth-it` | 643 | 6 | Same. Also the reference point for four later cost comparisons, so it should be stronger than they are | medium |
| `google-pm-certificate-worth-it` | 552 | 3 | Only 1 of 2 sources is official — weakest sourcing on the site | medium |

## 🟡 MERGE (6 source pages, 4 proposals)

Recommended for consolidation because **reader intent overlaps**, not because topics
are adjacent. All require validation and approval before implementation.

| Source page | Words | In | Proposed destination | Rationale |
|---|---|---|---|---|
| `is-csm-worth-it` | 701 | 1 | `psm-vs-csm` | Nobody choosing the CSM does so without comparing it to the PSM. The verdict page restates the comparison and adds a spine already used eight times |
| `is-pspo-worth-it` | 702 | 3 | `pspo-vs-cspo` | Same structure, same reasoning, one certification apart |
| `is-prince2-worth-it` | 897 | 0 | merge with `pmp-vs-prince2` | Two PRINCE2 pages, both with ~0–1 inbound links, both concluding that geography decides it |
| `pmp-vs-prince2` | 775 | 1 | (destination of the above) | The stronger URL of the pair |
| `capm-vs-google-pm-certificate` | 655 | 1 | `best-pm-certifications-beginners` | A two-way comparison between options the hub already compares, with 1 inbound link |
| `how-long-to-get-pmp` | 556 | 4 | consider folding into `how-to-prepare-for-pmp-exam` | Overlapping intent; also currently misfiled in the wrong pillar. Alternatively rebuild in place — flagged in both lists deliberately |

**Before implementing any merge:** check traffic, backlinks, indexation status, and
every inbound internal link to the retiring URL. `psm-vs-csm` (13 inbound) and
`best-pm-certifications-beginners` (16 inbound) are destinations, not sources — do
not retire them.

## ⚫ HOLD (2)

Both need the Editor-in-Chief's judgment, not an auditor's.

| Article | Question for you |
|---|---|
| `is-safe-certification-worth-it` | The site's most adversarial page toward a vendor. It publishes criticism of the SAFe framework sourced to ICSE research and a critique PMI itself published — factually solid and properly attributed. But it is a posture decision: does CertNorth want to be a publication that criticises frameworks, or one that only compares them? Either answer is defensible; it should be deliberate |
| `agile-coach-salary` | The article's own thesis is that its data is unreliable — one source averages 88 salaries. It is honest, and it may be *too* honest to be useful. Publishing a salary page that says "these numbers are shaky" is either the site's best differentiator or a page that shouldn't exist. Your call |

## 🔵 KEEP & ENHANCE (29)

Fundamentally sound. Enhancement here means targeted work, not rebuilding.

**The nine orphans need inbound links before anything else** — they are the site's
best content and nothing points to them:

`agile-coach-salary` (also on HOLD), `does-pmp-increase-salary`,
`how-to-become-pmo-analyst`, `is-pmi-acp-worth-it`, `is-pmi-membership-worth-it`,
`is-prince2-worth-it` (also a merge candidate), `is-safe-certification-worth-it`
(also on HOLD), `program-manager-salary`, `what-are-story-points`

The remaining articles in this group are at or above current standard. Their common
needs, in priority order:

1. **Inbound links** from the older, heavily-linked articles
2. **Structural divergence** — several still open paragraph → callout and close with
   an FAQ purely by habit
3. **`updatedAt` discipline** — a genuine re-verification pass on volatile figures

Articles in this group requiring no substantive change: `how-to-become-business-analyst`,
`scrum-master-vs-project-manager`, `what-is-a-user-story`, `what-are-story-points`,
`how-to-prepare-for-pmp-exam`, `is-pmi-acp-worth-it`, `how-to-become-pmo-analyst`,
`business-analyst-salary`, `program-manager-salary`. These represent the standard the
rebuild list should be brought up to.

---

## Outdated-information risk

| Risk | Articles | Field |
|---|---|---|
| High | `pmp-cost`, `pmp-eligibility`, `is-pmp-worth-it`, `pmp-vs-capm`, `pmp-vs-prince2` | PMP exam fee — could not be confirmed at source; softened to "around $425" across the site. PMI prices regionally, which the site now documents but these pages predate |
| High | `pmp-eligibility` | PMI's late-Q4-2026 change to live-training provider requirements takes effect soon |
| Medium | All 8 salary articles | Aggregator figures move continuously; none has been re-verified since publication |
| Medium | `scrum-certification-cost`, `is-safe-certification-worth-it` | Renewal fees and course prices set by third-party trainers |
| Low | Explainers grounded in the Scrum Guide | Stable unless the Guide changes |

`platform/content/certifications.json` carries `verifiedOn: 2026-07` for all six
certifications. The build warns after six months, so the first alert is due
**January 2027**.

---

## Recommended order of operations

Ordered by impact per unit of effort.

1. **Fix the affiliate disclosure** — see `DISCLOSURE_AUDIT.md`. This is the only
   finding that is arguably deceptive rather than merely weak, and it is a
   ten-minute fix.
2. **Fix the nine orphans** — add inbound links from the heavily-linked older
   articles. Cheap, and it makes the site's best work reachable.
3. **Break the template** — divergence in openings, closings and heading spines
   across the corpus. Highest-severity pattern; requires corpus-level planning.
4. **Rebuild the top five** — `pmp-cost`, `is-pmp-worth-it`,
   `best-pm-certifications-beginners`, `how-to-become-project-manager`,
   `psm-vs-csm`. These carry 70+ inbound links between them.
5. **Decide the two HOLD questions** — posture on vendor criticism, and whether to
   keep a salary page that undermines its own data.
6. **Validate and execute the merges** — after traffic, backlink and indexation
   checks.
7. **Rebuild the remaining eight** on the rebuild list.
8. **Run a genuine re-verification pass** on volatile figures and set `updatedAt`
   honestly.

Deliberately **not** on this list: publishing more articles. Nothing in this audit
suggests the site's problem is insufficient volume.

---

## Limitations of this audit

- **Depth was assessed from content, but word count was the only quantitative
  proxy available.** A short article that fully answers its question is adequate;
  the audit flags length and then applies judgment, but that judgment is fallible.
- **No traffic, ranking, backlink or indexation data was available.** All merge and
  removal reasoning rests on internal-link counts as a weak proxy for page
  importance. Every merge recommendation must be validated against real data before
  implementation.
- **The AdSense rejection reason was not supplied.** Nothing in this audit should be
  read as identifying the cause of that decision. The findings here are quality
  problems that are worth fixing regardless of what Google cited.
- **External sources were not re-fetched.** Source URLs were checked for format,
  tier and HTTPS, not re-read. Currency assessments are based on known change dates,
  not fresh verification.
- **Overlap was assessed by reading intent, not by measuring text similarity.** Two
  pages could share more passages than this audit detected.
