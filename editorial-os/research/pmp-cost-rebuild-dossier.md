# Rebuild Dossier — `pmp-cost`

**Date:** 2026-09-04
**Operation:** REBUILD 01, the first reconstruction under the new CertNorth standard
**Draft:** `editorial-os/drafts/pmp-cost-rebuilt.json`
**Production article:** unchanged, and retained as rollback reference
**Published:** nothing

---

## 1. What changed the research

The research phase ended blocked: PMI is unreachable from this environment, and every
external source available was a training vendor. **The Editor-in-Chief then verified the
core figures at PMI directly, outside this environment**, and supplied them.

That converts the largest open questions from unanswerable to answered, and it changes
three conclusions the earlier research had reached.

### Figures now verified at primary source

| Fact | Value | Status |
|---|---|---|
| PMP exam fee, PMI member | **US$405** | **VERIFIED** — PMI, checked by the Editor-in-Chief |
| PMP exam fee, non-member | **US$655** | **VERIFIED** — same |
| PMI membership | **US$139 per year** | **VERIFIED** — same |
| PDUs per three-year cycle | **60** | **VERIFIED** — same |
| Minimum from Education | **35** | **VERIFIED** — same |
| Maximum from Giving Back | **25** | **VERIFIED** — same |

### Still not established

| Fact | Status |
|---|---|
| Renewal fee amount | **PRIMARY-SOURCE VERIFICATION REQUIRED.** Separate from membership renewal, and subject to membership status and regional pricing |
| Retake fee and retake rules | **PRIMARY-SOURCE VERIFICATION REQUIRED** |
| How far exam pricing varies by country or account | **PARTIALLY VERIFIED** — that it can vary is established; the extent is not |
| Any market price for the 35 contact hours | **Not establishable by anyone.** No neutral source exists |
| Membership application fee amount | **PRIMARY-SOURCE VERIFICATION REQUIRED** |

---

## 2. Three conclusions that changed

### 2.1 The site's published exam fee was wrong

The repository states **~$425 member / ~$675 non-member** in five places — `pmp-cost`,
`is-pmp-worth-it`, `pmp-vs-capm`, `is-pmi-membership-worth-it` and `certifications.json`.

**The verified figures are $405 and $655.** The site was internally consistent and
externally incorrect, on both numbers, by $20.

**The draft uses the verified figures. The other four locations still carry the old ones**
and are outside the scope of this rebuild — recorded in §6.

This also settles a question the earlier research left open: the search-discovered "$445
effective 6 August 2026" was **not** correct. Refusing to adopt it on the strength of
vendor repetition was the right call.

### 2.2 The ten-year total has been dropped

The earlier plan proposed a ten-year cost-of-ownership model, and an earlier version of the
cost model published one.

**It has been removed.** The renewal fee could not be established, and it recurs three
times inside ten years — so any total would be built on an unverified number multiplied by
three, with regional variation on top. That is manufactured precision.

**The article now explains why it will not give a ten-year figure**, which is a weaker
deliverable and an honest one. The explanation itself carries analytical value: it names
the three specific things that make the number unavailable.

### 2.3 The membership analysis got smaller and firmer

The earlier model compared scenarios across a decade using an unverified membership figure
and an unverified renewal fee.

**The draft now does one calculation, on three verified inputs**, and states plainly that
it answers only the narrow question:

```
Non-member route:  $655
Member route:      $139 + $405 = $544
CertNorth calculation:  $111 in favour of joining, for a single first attempt
```

Whether membership is worth *keeping* is explicitly left to
`is-pmi-membership-worth-it`, because answering it requires the renewal fee.

---

## 3. What the rebuild fixes in the existing article

| # | Problem in the production article | Fixed how |
|---|---|---|
| 1 | **States three times that "every figure comes from PMI" while publishing third-party training prices** | Claim removed. The draft states the opposite explicitly: PMI sets the exam fee, other providers price the education |
| 2 | Exam fee ~$425/~$675 | Replaced with the verified $405/$655 |
| 3 | Membership "~$140 a year" | Replaced with the verified $139 |
| 4 | *"a retake adds another exam fee"* — unsourced | Removed. The draft says the amount is not confirmed and quotes no figure |
| 5 | Publishes renewal rules without citing the CCR Handbook | The Handbook is now in the sources; so is the PMP Handbook |
| 6 | Recommends a self-paced course with no mention of the late-2026 rule change | A dedicated section covers it, marked as upcoming and not in force |
| 7 | Training priced at "$0–$600 depending on provider" and an all-in range of "$700–$2,500" | **Both removed.** No range is published, and the article explains why |
| 8 | Stops at the purchase | Extends to maintenance, PDU composition, and the time budget |

**Problem 1 was the most serious, and it required no external access to find.**

---

## 4. The new analytical content

Six things the article now does that PMI's pricing page does not:

1. **Classifies costs by behaviour** — required, conditional, optional, recurring — and
   identifies who prices each.
2. **Runs the membership break-even** on verified numbers, and separates the exam-only
   question from overall membership value.
3. **Analyses the PDU composition rather than the total.** The 35/25 split means working in
   your certified role — a Giving Back activity — can cover **at most 25 of 60**, and none
   of the 35 that must be Education. The widely repeated idea that doing the job covers
   renewal is wrong by construction.
4. **Separates financial cost from time commitment** without monetising hours.
5. **Refuses to publish a ten-year total, and explains the three reasons.**
6. **Treats the late-2026 training change as a budgeting variable**, distinguishing the
   current rule from the announced one.

Item 3 is the strongest, because it is derived from newly verified numbers and it corrects
something both the wider internet and **CertNorth's own `pmp-renewal-pdus` dek** currently
imply.

---

## 5. Word count — and why it is not the point

| | Words |
|---|---|
| Production article | 477 |
| Draft | **1,594** |

**The draft must not be approved because it is longer.** The test is whether each section
carries something the reader cannot get from PMI. Section by section:

| Section | Earns its place because |
|---|---|
| Opening | States the thesis: PMI sets one line of the bill |
| What PMI charges, and what it doesn't | Carries the verified figures **and** the sourcing correction |
| Four kinds of cost | The classification — new, and independent of every price |
| Membership is a $111 question | The only calculation, on verified inputs |
| Sixty PDUs, and why 25 matters | The strongest original analysis |
| Money and time are separate budgets | The framework, and the refusal to monetise hours |
| Why we won't give you a ten-year total | The refusal, with its three reasons |
| What changes at the end of 2026 | The forward-looking budget variable |
| Pricing this for yourself | Converts the analysis into an action |

**If the Editor-in-Chief judges it long, the most compressible section is "Money and time
are separate budgets"** — its list restates timings owned by other articles. Cutting it
would cost roughly 180 words and lose the least.

---

## 6. Problems found in OTHER articles — recorded, not fixed

**No other article was modified.** These need separate approval.

| Article | Problem |
|---|---|
| `is-pmp-worth-it` | Exam fee ~$425/~$675 — now known to be wrong |
| `pmp-vs-capm` | Same |
| `is-pmi-membership-worth-it` | Exam fee ~$425/~$675, and membership ~$150 — now known to be wrong. Its "~$100 in your favour" becomes **$111** on verified figures |
| `certifications.json` | `examCost: "~$425 member / ~$675 non-member"`, `verifiedOn: 2026-07` — wrong, and it feeds the `certTable` on `best-pm-certifications-beginners`, so the error appears on a second page |
| `pmp-renewal-pdus` | Its dek says PDUs can be earned "including by doing your own job". With the 35/25 split now verified, that route caps at 25 of 60 and the dek overstates it |
| `how-to-become-project-manager` | "PMP path… $1,000–$3,000" — an unsourced training range of the kind this rebuild removes |
| `is-safe-certification-worth-it` | Its ten-year comparison gives the PMP as "exam plus ~$180–$450 in fees" while every other row is a full total. The renewal figures behind it are unverified |
| All 50 articles | No source entry carries a date — ~160 citations, zero dates |

**The exam-fee error is now known to be live on four pages plus a data file.** That is the
most urgent item on this list, and it is larger than this rebuild.
