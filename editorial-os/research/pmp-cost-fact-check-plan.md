# Fact-Check Plan — `pmp-cost`

**Date:** 2026-09-04
**Revised:** 2026-09-04 — relabelled under the corrected verification protocol

**Rule:** nothing below may be published as fact while its status reads
PRIMARY SOURCE VERIFICATION REQUIRED. It may be published only as *"what CertNorth
currently states, not yet confirmed at source"*, in the body text — never in a footnote.

---

## 1. Labels

| Label | May be published as fact? |
|---|---|
| **VERIFIED FROM CERTNORTH REPOSITORY** | Only as "what the site currently claims" |
| **PRIMARY SOURCE VERIFICATION REQUIRED** | **No** |
| **SECONDARY/SEARCH DISCOVERY ONLY** | **No** — regardless of how many sources repeat it |
| **CERTNORTH CALCULATION** | Only with inputs and their labels attached |
| **EDITORIAL INFERENCE** | Only as clearly-marked reasoning |

---

## 2. Prices — all require verification at PMI

| # | Fact the article needs | Repository value | Label | Re-verify |
|---|---|---|---|---|
| 1 | PMP exam fee, member | **~$425** — 5 locations agree | REPOSITORY + **PRIMARY VERIFICATION REQUIRED** | Every 6 months |
| 2 | PMP exam fee, non-member | **~$675** — 5 locations agree | REPOSITORY + **PRIMARY VERIFICATION REQUIRED** | Every 6 months |
| 3 | PMI membership, annual | **$140 or $150 — the site contradicts itself** | REPOSITORY (both) + **PRIMARY VERIFICATION REQUIRED** | Every 6 months |
| 4 | Membership application fee | *"a small one-time fee"* — **never quantified on the site** | REPOSITORY + **PRIMARY VERIFICATION REQUIRED** | Every 6 months |
| 5 | Renewal fee, member | **$60** — 3 locations | REPOSITORY + **PRIMARY VERIFICATION REQUIRED** | Every 6 months |
| 6 | Renewal fee, non-member | **$150** — 3 locations | REPOSITORY + **PRIMARY VERIFICATION REQUIRED** | Every 6 months |
| 7 | Whether PMI changed fees during 2026 | Asserted by 3 articles, undated | REPOSITORY + **PRIMARY VERIFICATION REQUIRED** | Once |
| 8 | **Whether PMI prices the exam by country** | `is-pmp-worth-it` says prices "vary by country"; `certifications.json` says "verify for your country" | REPOSITORY + **PRIMARY VERIFICATION REQUIRED** | **Before publication — decides whether any universal figure may be stated** |

**Fact 3 is load-bearing.** The membership break-even is published as a range precisely
because the site disagrees with itself. One verified number collapses the range.

**Fact 8 is the gate on the whole article.** If PMI prices regionally, no universal number
may be stated at all — only a method.

---

## 3. Rules and requirements

| # | Fact | Repository value | Label | Action |
|---|---|---|---|---|
| 9 | 60 PDUs per 3-year cycle | Stated in 3 locations | REPOSITORY + **PRIMARY VERIFICATION REQUIRED** | Annually |
| 10 | Minimum 8 PDUs per Talent Triangle area | `pmp-renewal-pdus` | REPOSITORY + **PRIMARY VERIFICATION REQUIRED** | Annually |
| 11 | **The Giving Back cap** | **Site says a cap exists; never states the number** | **PRIMARY VERIFICATION REQUIRED** | **Before publication** |
| 12 | Whether a minimum share of PDUs must be Education | **Not stated anywhere on the site** | **PRIMARY VERIFICATION REQUIRED**; a search lead exists but is **SECONDARY/SEARCH DISCOVERY ONLY** | Before publication |
| 13 | 35 contact hours required | 7 locations agree | REPOSITORY + **PRIMARY VERIFICATION REQUIRED** | Annually |
| 14 | An active CAPM covers the 35 hours | `pmp-eligibility`, `pmp-vs-capm` | REPOSITORY + **PRIMARY VERIFICATION REQUIRED** | Before publication |
| 15 | Membership is optional, never required | Consistent site-wide | REPOSITORY | — |

**Facts 11 and 12 together decide** whether the article may say anything about how easily
PDUs are earned. Without them, it may say only that free routes exist —
which `pmp-renewal-pdus` supports — and **not** that doing your job covers them.

---

## 4. Retake — currently unpublishable

| # | Fact | Status |
|---|---|---|
| 16 | Retake fee | **Unknown.** The site's only claim (*"a retake adds another exam fee"*) is **unsourced**; `pmp-cost` does not cite the PMP Handbook. A search lead suggests a reduced fee, but that is **SECONDARY/SEARCH DISCOVERY ONLY** |
| 17 | Number of attempts permitted, and over what period | **Not stated anywhere on the site.** **PRIMARY VERIFICATION REQUIRED** |
| 18 | Waiting period between attempts | Same |
| 19 | What happens after the permitted attempts are exhausted | Same |

**The rebuilt article may not assert any retake figure, in either direction.** It may state
that a failed attempt has a cost, that we could not verify what it is, and that our current
page's wording is unsourced.

**Correcting our own article on the strength of vendor pages would repeat the exact error
that made the current article weak.**

---

## 5. The training rule — the largest live variable

| # | Fact | Status |
|---|---|---|
| 20 | A change takes effect late Q4 2026 | REPOSITORY (`pmp-eligibility`) + **PRIMARY VERIFICATION REQUIRED** |
| 21 | Approved routes: ATPs, China REPs, eligible academic programmes | REPOSITORY + **PRIMARY VERIFICATION REQUIRED** |
| 22 | **Scope — all 35 contact hours, or only live instructor-led training?** | `pmp-eligibility` says **live only**. A search lead offers a broader reading — **SECONDARY/SEARCH DISCOVERY ONLY**. **Unresolved** |

If fact 22 cannot be resolved, the article presents **both readings and their different
consequences**, which is publishable. Asserting either is not.

---

## 6. Settled, and one settled permanently

| # | Fact | Status |
|---|---|---|
| 23 | **No reliable PMP pass rate exists.** PMI has not published one for ~20 years; the circulating "61%" is a passing score retired around 2006 | REPOSITORY (`pmp-pass-rate`). **Needs no verification — the absence of data is the finding** |
| 24 | PMI scores psychometrically, reporting performance bands | REPOSITORY + PRIMARY VERIFICATION REQUIRED |
| 25 | Exam updated 9 July 2026; People 33% / Process 41% / Business Environment 26% | REPOSITORY (`how-to-prepare-for-pmp-exam`, which cites the 2026 ECO) |

**Fact 23 licenses the article's refusal to compute an expected cost.**

---

## 7. Internal contradictions to resolve

Full detail in `pmp-cost-internal-claims-map.md`.

| # | Contradiction | Files | Fixable by this rebuild alone? |
|---|---|---|---|
| 26 | **"Every figure sourced from PMI"** while publishing training prices PMI does not publish | `pmp-cost` | **Yes — and it needs no verification** |
| 27 | Renewal rules published without citing the CCR Handbook | `pmp-cost` | **Yes** — add the source |
| 28 | Retake claim unsourced | `pmp-cost` | **Yes** — remove or qualify |
| 29 | Self-paced training advised with no mention of the late-2026 change | `pmp-cost` | **Yes** |
| 30 | Membership **$140** vs **$150** | `pmp-cost`, `is-pmi-membership-worth-it` | **No — second article. Needs approval** |
| 31 | All-in cost **$700–$2,500** vs **$1,000–$3,000** | `pmp-cost`, `how-to-become-project-manager` | **No — second article. Needs approval** |
| 32 | The site's only 10-year PMP figure is renewal fees alone, in a comparison table of full totals | `is-safe-certification-worth-it` | **No — second article. Needs approval** |
| 33 | `certifications.json` `verifiedOn: 2026-07`, feeding a `certTable` on `best-pm-certifications-beginners` | `certifications.json` + 1 page | **No — changes a second page. Needs approval** |
| 34 | `pmp-renewal-pdus` dek promises what its body caps | `pmp-renewal-pdus` | **No — second article. Needs approval** |
| 35 | **No source entry anywhere carries a date** — ~160 citations | All 50 articles, and the content schema | **No — systemic. Needs a decision, not a fix** |

---

## 8. Re-verification schedule

| Cadence | Items |
|---|---|
| Every 6 months | 1–6 — all prices |
| Annually | 9, 10, 13 — PDU and education requirements |
| On any PMI announcement | 1–8, 20–22 |
| Once, then closed | 7, 22 |

`certifications.json` carries `verifiedOn: 2026-07` for all six certifications; the build
warns at six months, so the first automatic alert is due **January 2027**. Publishing this
article is the natural moment to run the first real pass — which would make the editorial
policy's re-verification promise demonstrable rather than merely stated.

---

## 9. The verification instruction

Open `pmi.org` **logged in from the country the reader is being advised for**, and record
each item with the date checked:

1. PMP exam fee, member and non-member, **as displayed at checkout**
2. **Whether that displayed amount and currency differ from the USD figure on the general
   certification page** — this settles fact 8, and fact 8 gates the article
3. PMI membership fee **and the application fee amount**
4. Certification renewal fee, member and non-member
5. **Re-examination fee, number of attempts permitted, and the eligibility period** — PMP
   Handbook
6. **PDU category minimums and maximums** — CCR Handbook
7. **The exact wording of the late-2026 training requirement**, specifically whether it
   covers all 35 contact hours or only live instructor-led training

Items 2, 5, 6 and 7 are the ones that change what the article can say. Items 1, 3 and 4
change only the numbers inside it.
