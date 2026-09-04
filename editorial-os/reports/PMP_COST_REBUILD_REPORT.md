# Rebuild Report — REBUILD 01: `pmp-cost`

**Date:** 2026-09-04
**Revised:** 2026-09-04 — PDU correction applied after human review (§4a); four editorial
corrections applied after the human review package (§4b)
**Article:** `pmp-cost` · `/certifications/guides/pmp-certification-cost/`
**Draft:** `editorial-os/drafts/pmp-cost-rebuilt.json`
**Production article:** **unchanged**, retained as rollback reference
**Published:** nothing · **Merged:** nothing · **Deleted:** nothing · **Other articles modified:** none

---

## 1. Verdict

## READY FOR HUMAN APPROVAL

The factual flag raised in human review has been corrected (§4a), and the four editorial
refinements requested afterwards have been applied (§4b). The Editor-in-Chief performs the
final reading.

---

## 2. What was rebuilt

| | Production | Draft |
|---|---|---|
| Body words | 477 | **1,743** |
| Level-2 headings (authored) | 3 | 8 |
| Internal links | 3 | **8**, to 7 distinct articles |
| Sources | 2 | **5** — both PMI handbooks added |
| Callouts | 2 | **1** |
| Tables | 2 | 2 |
| FAQ block | Yes | **No** |
| Second block | Callout | **Heading** |
| Verbatim overlap with the production text | — | **0** 6-word spans |

URL, slug, `clusterId`, `primaryKeyword` and `publishedAt` are **unchanged**. All 11
inbound internal links continue to resolve. `updatedAt` is set to 2026-09-04, which is a
real revision date.

---

## 3. Gates

| Gate | Result | Evidence |
|---|---|---|
| **Research Gate** | **PASS** | Repository layer fully mapped (`pmp-cost-internal-claims-map.md`); primary figures verified by the Editor-in-Chief at PMI |
| **Source Gate** | **PASS** | 5 sources, all PMI, all HTTPS. The CCR Handbook and PMP Handbook were added, fixing a gap where the production article published renewal rules citing neither. **No vendor source is cited anywhere** |
| **Original Value Gate** | **PASS** | 8 distinct contributions, none obtainable from PMI's pricing page. Strongest: the PDU composition analysis. See `pmp-cost-original-value-plan.md` |
| **Editorial Gate** | **PASS** | Independent, analytical, no marketing language, no superlatives, no manufactured urgency. Every refusal is explained rather than hedged |
| **Fact Check Gate** | **PASS** | All prices VERIFIED; all PDU limits now VERIFIED against the CCR Handbook; all 5 calculations labelled CertNorth with assumptions visible. **No claim classified INCORRECT or UNSUPPORTED remains.** Full classification in `pmp-cost-fact-check-plan.md` |
| **Pattern Gate** | **PASS, no regression** | Zero heading collisions against 215 existing H2s; zero consecutive-pair sequence overlap; below the corpus minimum on callouts; first article on the site without an FAQ. **Three self-findings acted on** — see §5. Re-run after the correction: **no new phrase overlap introduced** |
| **SEO Gate** | **PASS** | metaTitle 52/60 unique · metaDescription 137/155 unique · dek 275 chars answer-first · primary keyword unchanged so no cannibalisation · no keyword stuffing, no sections created for keywords |
| **AdSense Quality Gate** | **PASS on substance** | Substantially more useful, no padding, no fabrication, sources named, limitations stated. **No editorial change guarantees approval, and this report does not claim otherwise** |
| **Build GATE + `check.js`** | **PASS** | Validated in an isolated copy of `platform/`; production content never touched |

### Build validation

```
node src/build.js --force → ✓ 50 articles, 60 sitemap URLs, quality GATE passed
node src/check.js         → ✓ 61 pages, links intact, alt ok, heading order ok,
                              JSON-LD valid, unique titles, WCAG AA in both themes
```

Rendered in Chromium at 375 px: no horizontal overflow, 8 authored H2s, 2 tables,
**0 `<details>` elements** confirming the FAQ removal renders cleanly, all internal links
resolving. The one console error is this environment's proxy blocking the AdSense script —
present on every page of the site.

---

## 4. The correction that mattered most

The production article states **three times** that every figure comes from PMI — in the
opening paragraph, in a table caption, and in the meta description — while that same table
prices the 35 contact hours at "$0–$600 depending on provider" and a second table prices
third-party training at "$700–$2,500".

**PMI does not publish either figure.** The claim and the content disproving it were in the
same file.

**The draft removes the claim and states the opposite:** PMI sets the exam fee; the
education is priced by whoever sells it; and no range is published here, because every
source found for one was itself selling training.

This required no external access to find, and it is about our own sourcing integrity on a
site whose entire position is independence.

---

## 4a. The PDU correction (applied after human review)

**The draft was factually wrong, and the review caught it.**

| | |
|---|---|
| **Old interpretation** | *"Working in your certified role is a Giving Back activity, so… it can cover at most 25 of the 60, and none of the 35 that must be Education."* |
| **Why it was wrong** | It treated **25** — the maximum for the whole **Giving Back to the Profession** category — as though it were the maximum for **Work as a Practitioner**, which is one activity inside that category |
| **Corrected interpretation** | Work as a Practitioner is capped at **8 PDUs per three-year cycle** for PMP holders. Holding a project management job therefore contributes **at most 8 of the 60**, and nothing toward the 35 that must be Education |

**Source:** PMI — *Continuing Certification Requirements (CCR) Handbook, 2026 edition*. The
source label in the article was updated to name the edition. No commercial training
provider and no search snippet was used as authority for this claim.

**Why the distinction has to be explicit.** The two limits are nested, and the nesting is
where every casual summary of PMP renewal goes wrong:

```
60 PDUs per cycle
  ├─ at least 35 from Education        (a floor, not a ceiling)
  └─ up to 25 from Giving Back          (a category ceiling)
        └─ up to 8 from Work as a Practitioner   (one activity inside it)
```

The draft now carries this as a four-row table sourced to the CCR Handbook, so the
relationship is visible rather than asserted in prose.

**The editorial conclusion is preserved and is now stronger.** Having a project management
job does not satisfy PMP renewal — and the real figure makes the point more sharply than
the wrong one did: the job covers at most 8 of 60, roughly one PDU in eight, not 25.

**What the article does not say**, checked explicitly: that professional work yields 25
PDUs; that employment alone satisfies renewal; that the 25-PDU Giving Back maximum is the
Work as a Practitioner limit; or that all 60 can be earned through work.

### A second problem found while sweeping for the first

The article contains **two different "35 Education" requirements**: the **35 contact hours**
needed before sitting the exam, and the **35 Education PDUs** needed in each renewal cycle
afterwards. Both appear several times, and a reader could easily merge them.

A disambiguating sentence was added: they are separate requirements at different stages —
one a condition of applying, the other a condition of keeping the credential. This was not
in the brief; the sweep surfaced it.

**Correction cost:** +174 words (1,594 → 1,768), being the four-row table and the
disambiguation.

---

## 4b. Four editorial corrections (applied after the human review package)

Surgical edits to the draft only. No section added or removed, no architecture change, no
calculation touched, no verified price touched, no PDU conclusion touched.

| # | Correction | Section | Before → After |
|---|---|---|---|
| 1 | **"Every applicant" was too absolute**, since the same paragraph gives the CAPM exception | §What PMI charges | *"Every applicant needs 35 contact hours…"* → *"Most applicants need 35 contact hours of project management education before they can apply; if you already hold an active CAPM, that requirement is covered…"*. The exception now sits immediately after the rule |
| 2 | **Wording could be read as a claim about PMI's training business** | §heading + §What PMI charges | H2: *"Four kinds of cost, and PMI sets only one"* → **"Four kinds of cost, but only some are priced by PMI"**. Opening: *"What PMI does not set is the cost of qualifying"* → *"PMI requires qualifying education, but it does not publish a single price for the required 35 hours… Providers set their own prices, so there is no single 'PMP training cost' issued by PMI"* |
| 3 | **Unsupported free-PDU claim removed** | §Sixty PDUs | *"The financial consequence of this is limited, because Education PDUs can be earned from free webinars and qualifying self-directed learning."* → **deleted.** The following sentence was made grammatical without adding any cost claim: *"The consequence for your calendar is real: at least 35 Education PDUs is a floor, and no job clears it on its own."* |
| 4 | **PDU hierarchy preserved exactly** | §Sixty PDUs | **No change.** Verified unchanged: 60 total → ≥35 Education → ≤25 Giving Back → ≤8 Work as a Practitioner, with the category/activity distinction intact |

**Correction 2 is the one worth noting.** The article now makes only the claim the evidence
supports — that there is no single PMI-published price for the required 35 hours — and
makes no claim at all about whether PMI offers training products.

**Correction 3 removed the last unsupported cost claim in the article.** Nothing replaced
it: the section no longer says anything about what PDUs cost, only about what they demand
in time.

**Length:** 1,768 → **1,743 words**. The §"Money and time are separate budgets" section was
**retained** on the Editor-in-Chief's explicit instruction.

**Validation after the edits:** build green, `check.js` green, JSON-LD valid, headings
ordered, 8 internal links resolving, no overflow at 375 px. Pattern Guardian: zero heading
collisions against the 215 on the site, the new H2 unique, and **phrase overlap slightly
lower than before** (13 articles, down from 15) — no regression.

**Still pending, deliberately untouched:** the old exam prices in `is-pmp-worth-it`,
`pmp-vs-capm`, `is-pmi-membership-worth-it`, `certifications.json` and, through the
`certTable`, `best-pm-certifications-beginners`. That global correction is a separate task.

---

## 5. Pattern Guardian — three findings against the draft itself

| # | Finding | Action |
|---|---|---|
| 1 | The opening used a house rhetorical formula — *"Most pages about the cost of the PMP…"*, the same "most other articles get this wrong" move as `project-manager-salary` and `best-pm-certifications-beginners`; "Most" already opens 4 of 50 articles | Rewritten to open on substance |
| 2 | The eligibility sentence was **verbatim across four articles** (10 shared 6-word spans each with `how-long-to-get-pmp`, `is-pmp-worth-it`, `pmp-vs-capm`) | Rephrased; overlap now **0** in all three |
| 3 | The 2026 training paragraph restated `pmp-eligibility` almost word for word (7 shared spans) | Rewritten as a budgeting summary pointing to the owning article; overlap now **2** |

**Re-run after the PDU correction — no regression.** Heading collisions against 215
existing H2s: none. Consecutive-pair sequence overlap: none. Six-word phrase overlap
unchanged from before the correction, with no new article entering the list. The new
heading, *"Sixty PDUs, and why eight is the number that matters"*, is unique site-wide. The
correction added a second table, taking the article from 1 to 2 — still inside the corpus
range of 1–3, and the table earns its place by making a nested limit structure legible.
No FAQ was added, no callout was added, no house opening formula was reintroduced.

---

## 6. What the draft deliberately does not claim

Each omission is stated in the article, not left silent:

- **No ten-year total.** The renewal fee is unverified and recurs three times inside a
  decade; multiplying it would manufacture precision. The article gives the shape and the
  three reasons instead.
- **No retake fee**, in either direction. The production article's version was unsourced;
  vendor material suggesting a reduced fee was not adopted.
- **No training price or range.** No neutral source exists.
- **No expected cost** weighted by any pass probability — no reliable pass rate exists.
- **No monetary value for the reader's hours.**
- **No claim that membership is worth having** — only that joining is $111 cheaper for a
  first attempt, with the exam-only question kept separate from overall membership value.
- **No universal price.** The article says pricing can depend on account and location and
  tells the reader to check their own.

---

## 7. Flags — the previous one is closed

**Closed.** The PDU premise flagged in the first version of this report was checked against
the CCR Handbook and **turned out to be wrong**. It has been corrected in §4a. That is the
flag doing its job.

**Nothing now blocks publication.** The remaining unverified items would let the article say
*more*; none makes what it currently says wrong:

| Still unverified | Effect if verified later |
|---|---|
| Renewal fee, member and non-member | Would permit a long-term total — and would then oblige one |
| Retake fee and rules | Would let the conditional cost carry a figure |
| Membership application fee | Currently excluded from the $111 calculation, and the article says so |
| Exact scope of the late-2026 training rule | The article describes the timing implication without asserting scope |
| Extent of regional price variation | The article warns that it exists without quantifying it |

**A note on method.** Two of this rebuild's conclusions came from refusing to publish
something: the ten-year total and the retake fee. A third — the PDU analysis — came from
publishing something that was wrong and being corrected. The corrected version is sharper
than the original: 8 of 60 makes the point better than 25 of 60 did.

---

## 8. Problems in other articles — recorded, not fixed

**No other article was modified.** The verified fees reveal that the wrong exam fee is live
in four more places:

| Location | Problem |
|---|---|
| `is-pmp-worth-it` | Exam ~$425 / ~$675 — incorrect |
| `pmp-vs-capm` | Same |
| `is-pmi-membership-worth-it` | Same, plus membership "~$150"; its "~$100 in your favour" becomes **$111** |
| `certifications.json` | `examCost: "~$425 member / ~$675 non-member"`, `verifiedOn: 2026-07` — incorrect, **and it feeds the `certTable` on `best-pm-certifications-beginners`**, so a fifth page shows it |
| `pmp-renewal-pdus` | Its dek says PDUs can be earned "including by doing your own job" — with the 25-PDU cap now verified, that overstates the route |
| `how-to-become-project-manager` | "PMP path… $1,000–$3,000" — an unsourced range of exactly the kind removed here |
| `is-safe-certification-worth-it` | Its ten-year comparison gives the PMP as "exam plus ~$180–$450 in fees" while every other row is a full total |
| All 50 articles | **No source entry carries a date** — ~160 citations, zero dates |

**The exam-fee error is larger than this rebuild** and is the most urgent follow-up.

---

## 9. Needs approval

| # | Decision | Recommendation |
|---|---|---|
| 1 | ~~Confirm the Giving Back categorisation~~ | **Done.** Checked, found wrong, corrected — see §4a |
| 2 | Approve the draft to replace the production article | Your call. The draft is ready |
| 3 | Approve dropping the FAQ block | Recommended. It would restate the body. Cost: loses `FAQPage` schema; first article on the site without one |
| 4 | **Correct the exam fee in the four other locations** | **Strongly recommended and urgent** — the site is publishing an incorrect price on five pages |
| 5 | Correct `certifications.json` and advance `verifiedOn` honestly | Recommended, with 4 |
| 6 | Fix the `pmp-renewal-pdus` dek | Recommended |
| 7 | Remove the unsourced range in `how-to-become-project-manager` | Recommended |
| 8 | Reconcile the ten-year row in `is-safe-certification-worth-it` | Recommended |
| 9 | Add a date field to the source schema | Systemic decision |

---

## 10. Rollback

The production `platform/content/articles/pmp-cost.json` is untouched and remains live. The
draft exists only at `editorial-os/drafts/pmp-cost-rebuilt.json`, outside the build. Nothing
has been deployed, merged, redirected or deleted. Reverting requires deleting one draft
file.
