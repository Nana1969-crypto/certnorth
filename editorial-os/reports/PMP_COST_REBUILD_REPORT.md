# Rebuild Report — REBUILD 01: `pmp-cost`

**Date:** 2026-09-04
**Article:** `pmp-cost` · `/certifications/guides/pmp-certification-cost/`
**Draft:** `editorial-os/drafts/pmp-cost-rebuilt.json`
**Production article:** **unchanged**, retained as rollback reference
**Published:** nothing · **Merged:** nothing · **Deleted:** nothing · **Other articles modified:** none

---

## 1. Verdict

## READY FOR HUMAN REVIEW

with one item to confirm before publication, identified in §7.

---

## 2. What was rebuilt

| | Production | Draft |
|---|---|---|
| Body words | 477 | **1,594** |
| Level-2 headings (authored) | 3 | 8 |
| Internal links | 3 | **8**, to 7 distinct articles |
| Sources | 2 | **5** — both PMI handbooks added |
| Callouts | 2 | **1** |
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
| **Fact Check Gate** | **PASS with one flag** | All prices VERIFIED; all rules at least PARTIALLY VERIFIED; all 5 calculations labelled CertNorth with assumptions visible. **One load-bearing PARTIALLY VERIFIED premise** — see §7 |
| **Pattern Gate** | **PASS** | Zero heading collisions against 215 existing H2s; zero consecutive-pair sequence overlap; below the corpus minimum on callouts; first article on the site without an FAQ. **Three self-findings acted on** — see §5 |
| **SEO Gate** | **PASS** | metaTitle 52/60 unique · metaDescription 137/155 unique · dek 275 chars answer-first · primary keyword unchanged so no cannibalisation · no keyword stuffing, no sections created for keywords |
| **AdSense Quality Gate** | **PASS on substance** | Substantially more useful, no padding, no fabrication, sources named, limitations stated. **No editorial change guarantees approval, and this report does not claim otherwise** |
| **Build GATE + `check.js`** | **PASS** | Validated in an isolated copy of `platform/`; production content never touched |

### Build validation

```
node src/build.js --force → ✓ 50 articles, 60 sitemap URLs, quality GATE passed
node src/check.js         → ✓ 61 pages, links intact, alt ok, heading order ok,
                              JSON-LD valid, unique titles, WCAG AA in both themes
```

Rendered in Chromium at 375 px: no horizontal overflow, 8 authored H2s, 1 table,
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

## 5. Pattern Guardian — three findings against the draft itself

| # | Finding | Action |
|---|---|---|
| 1 | The opening used a house rhetorical formula — *"Most pages about the cost of the PMP…"*, the same "most other articles get this wrong" move as `project-manager-salary` and `best-pm-certifications-beginners`; "Most" already opens 4 of 50 articles | Rewritten to open on substance |
| 2 | The eligibility sentence was **verbatim across four articles** (10 shared 6-word spans each with `how-long-to-get-pmp`, `is-pmp-worth-it`, `pmp-vs-capm`) | Rephrased; overlap now **0** in all three |
| 3 | The 2026 training paragraph restated `pmp-eligibility` almost word for word (7 shared spans) | Rewritten as a budgeting summary pointing to the owning article; overlap now **2** |

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

## 7. The one flag before publication

**Confirm in PMI's CCR Handbook that working in your certified role is a Giving Back
activity.**

The section *"Sixty PDUs, and why 25 is the number that matters"* is the article's
strongest original analysis. Its inputs — 60 PDUs, ≥35 Education, ≤25 Giving Back — are
verified. Its conclusion depends on one premise that is only **PARTIALLY VERIFIED**: that
working in the role counts as Giving Back. That comes from `pmp-renewal-pdus`, which cites
the CCR Handbook but transcribes no category list.

**If the premise is wrong, cut the section rather than soften it.**

Nothing else blocks publication. The remaining unverified items — renewal fee, retake fee,
application fee, rule scope, extent of regional variation — would let the article say
*more*, not make what it says wrong.

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
| 1 | Confirm the Giving Back categorisation | **Do this first.** One handbook lookup |
| 2 | Approve the draft to replace the production article | Your call. The draft is ready subject to 1 |
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
