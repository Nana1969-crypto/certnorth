# Cost Model — `pmp-cost`

**Built:** 2026-09-04
**Revised:** 2026-09-04 (third revision) — rebuilt on primary-source-verified inputs; the
ten-year total has been **removed**
**Status:** this model is implemented in `editorial-os/drafts/pmp-cost-rebuilt.json`

---

## 0. Revision history, stated openly

| Version | Inputs | Ten-year total | Why it changed |
|---|---|---|---|
| 1 | Search-discovered figures ($445/$675/$149) | Published | **Wrong method.** Vendor repetition treated as evidence |
| 2 | Repository figures ($425/$675/$140–150) | Published as a range | Protocol corrected; inputs were still unverified |
| 3 — current | **PMI-verified figures ($405/$655/$139)** | **Removed** | Renewal fee still unverified, and it recurs three times inside ten years |

**Version 3 makes fewer claims than version 1 and is the only one that is defensible.**

---

## 1. Inputs

| Input | Value | Status |
|---|---|---|
| Exam fee, PMI member | **$405** | **VERIFIED** at PMI by the Editor-in-Chief |
| Exam fee, non-member | **$655** | **VERIFIED** |
| PMI membership, annual | **$139** | **VERIFIED** |
| PDUs per 3-year cycle | **60** | **VERIFIED** |
| Minimum Education PDUs | **35** | **VERIFIED** |
| Maximum Giving Back PDUs | **25** | **VERIFIED** |
| Renewal fee | — | **PRIMARY-SOURCE VERIFICATION REQUIRED.** Separate from membership renewal; subject to membership status and regional pricing |
| Retake fee and rules | — | **PRIMARY-SOURCE VERIFICATION REQUIRED** |
| Membership application fee | — | **PRIMARY-SOURCE VERIFICATION REQUIRED**; excluded from all arithmetic |
| Cost of the 35 contact hours | — | **Not modelled.** No neutral source exists |
| Regional variation | — | **PARTIALLY VERIFIED** — that pricing can depend on account and location is established; the extent is not |

---

## 2. Taxonomy

Independent of every price. This survives any input being revised.

| Category | What it covers | Trigger | Recurring | Who prices it |
|---|---|---|---|---|
| **Required** | Exam fee; 35 contact hours of education | Applying and sitting | No | PMI sets the exam fee; providers price the education |
| **Conditional** | A further exam fee after a failed attempt | Not passing | Per attempt | PMI — **amount unverified** |
| **Optional** | Membership; prep courses; question banks; books; PDU bundles | Choice | Varies | PMI and third parties |
| **Recurring** | Renewal every 3 years; 60 PDUs per cycle | Holding the credential | Yes | PMI sets the requirement; spending is largely the holder's choice |

**Only part of one row is both required and priced by the issuing body.** That is the
article's organising insight.

---

## 3. CERTNORTH CALCULATION — membership at exam time

**All three inputs verified.**

```
Non-member route:   exam                        $655
Member route:       membership $139 + exam $405 $544
                                    Difference  $111 in favour of joining
```

**Assumptions, all stated in the article:** PMI's current published fees; **one** exam
attempt; no regional variation; the one-time application fee **excluded** because its
amount is unverified.

**Sensitivity.** The exam-fee gap is `$655 − $405 = $250`. Joining is cheaper for a first
attempt while membership costs less than $250. At $139 the margin is comfortable.

**What this calculation does NOT establish:**

- **It is not "membership is worth it."** It answers the exam-only question. Overall
  membership value depends on the renewal fee (unverified) and on benefits whose worth
  depends entirely on use. That analysis belongs to `is-pmi-membership-worth-it`.
- **It does not assume renewal of membership.**
- **It puts no value on the library, webinars or chapter access.**

The article carries this distinction explicitly: **EXAM-ONLY BREAK-EVEN** is not
**OVERALL MEMBERSHIP VALUE**.

---

## 4. CERTNORTH CALCULATION — PDU composition

**All three inputs verified: 60 total, ≥35 Education, ≤25 Giving Back.**

```
Maximum share of a cycle that Giving Back can cover:  25 / 60 = 41.7%
Minimum deliberate learning per cycle:                35 hours
Annualised total commitment:                          60 / 3 = 20 hours per year
```

**The consequence.** Working in the certified role is a Giving Back activity. It is
therefore capped at 25 PDUs and can contribute **nothing** to the 35 that must be
Education. The common claim that simply doing the job covers renewal is wrong by
construction — not approximately, but structurally.

**Financially this changes little**, because Education PDUs can be earned from free
webinars and qualifying self-directed learning. **For the calendar it changes a great
deal**: at least 35 hours per cycle of deliberate learning is not optional.

*(Note: that working in the certified role counts as Giving Back is stated by
`pmp-renewal-pdus`, which cites the CCR Handbook. It is **PARTIALLY VERIFIED** —
the category cap is verified, the category assignment is repository-sourced.)*

---

## 5. Why there is no ten-year total

**Three reasons, all published in the article rather than hidden.**

1. **The renewal fee is not a single universal number.** It depends on membership status at
   the moment of renewal and, like the exam fee, on how PMI prices for the holder's
   location. Multiplying an unverified figure by three renewal cycles would manufacture
   precision.
2. **The education requirement is priced by third parties**, and no neutral average exists.
3. **Any total weighting a retake by the probability of failure needs a pass rate**, and
   PMI has not published one for around two decades — established in `pmp-pass-rate`.

**What the article gives instead:** the *shape* — one exam fee, one education requirement,
then a renewal event every three years for as long as the credential is held — plus the
instruction to price those three against the reader's own PMI account.

**A transparent limitation is preferable to a false precise number.** This is the single
biggest change from earlier versions of this model, and it makes the deliverable smaller.

---

## 6. Why there is no retake scenario

The retake fee and the retake rules are **PRIMARY-SOURCE VERIFICATION REQUIRED**. The
production article's claim that *"a retake adds another exam fee"* is unsourced, and search
material suggesting a reduced fee is vendor-sourced and was not adopted.

**The article states that a further attempt costs a further fee and that we have not
confirmed the amount.** No number is quoted, in either direction.

**No expected-cost calculation exists anywhere in this model**, because it would require a
pass rate that does not exist.

---

## 7. Money and time

The model never assigns an hourly monetary value to the reader's time.

| Financial cost | Time commitment |
|---|---|
| Exam fee | 36 or 60 months of qualifying experience, depending on degree |
| Education, priced by providers | 35 contact hours before applying |
| Optional preparation materials | Preparation, variable with experience |
| Renewal fee, every 3 years | 180 questions in 240 minutes |
| PDU purchases, if any — avoidable | 60 PDUs per cycle, ≥35 Education, ~20 hours a year |

**These are different budgets with different constraints.** Money for a course can be
borrowed; the hours cannot.

---

## 8. What this model must not be used to claim

- **Not** a universal country-independent price. Regional variation is established, its
  extent is not.
- **Not** a ten-year or five-year total.
- **Not** a retake cost, in either direction.
- **Not** an average or typical training cost.
- **Not** an expected cost weighted by any pass probability.
- **Not** "membership is worth it" — only that joining is $111 cheaper for a first attempt.
- **Not** a monetary value for study or PDU time.
