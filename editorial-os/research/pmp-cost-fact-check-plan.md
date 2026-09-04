# Fact-Check Plan — `pmp-cost`

**Date:** 2026-09-04
**Rule:** no statement below may be published as fact until its status reads VERIFIED, or
until the article labels it explicitly as unverified in the body text — not in a footnote
and not in a caveat at the end.

**Confidence key:** HIGH = inspectable or primary · MEDIUM = converging independent
secondary sources · LOW = single or conflicting secondary sources · UNKNOWABLE = no
reliable source exists anywhere.

---

## 1. Prices — every one requires human verification at PMI

| # | Fact the article needs | Best current source | Status | Confidence | Re-verify |
|---|---|---|---|---|---|
| 1 | PMP exam fee, member | Vendor consensus: **$445**, effective 2026-08-06 | **UNVERIFIED** | MEDIUM | Every 6 months + on any PMI announcement |
| 2 | PMP exam fee, non-member | Vendor consensus: **$675** | **UNVERIFIED** | MEDIUM | Same |
| 3 | Whether a fee change took effect 2026-08-06 | Multiple unaffiliated vendors state it consistently | **UNVERIFIED** | MEDIUM | Once |
| 4 | PMI membership, annual | Sources disagree: $129 / $139 / $149 / $154 / $159 | **UNVERIFIED — sources conflict** | **LOW** | Every 6 months |
| 5 | PMI membership application fee | ~$10 one-time, consistent | **UNVERIFIED** | MEDIUM | Every 6 months |
| 6 | Renewal fee, member | **$60** | **UNVERIFIED** | MEDIUM | Every 6 months |
| 7 | Renewal fee, non-member | **$150** | **UNVERIFIED** | MEDIUM | Every 6 months |
| 8 | Retake fee, member | **$275** | **UNVERIFIED — may predate the August increase** | **LOW–MEDIUM** | Before publication |
| 9 | Retake fee, non-member | **$375** | **UNVERIFIED — same risk** | **LOW–MEDIUM** | Before publication |

**Facts 8 and 9 are load-bearing.** The article corrects CertNorth's own claim that a
retake costs another full exam fee. **If the reduced retake fee cannot be verified, that
section must be cut, not softened.**

**Fact 4 is load-bearing for the calculation.** The membership break-even is stated with a
sensitivity range precisely because the figure is unreliable. If PMI publishes one number,
the range should be replaced by it.

---

## 2. Rules and requirements

| # | Fact | Source | Status | Confidence | Re-verify |
|---|---|---|---|---|---|
| 10 | 60 PDUs per 3-year cycle | Already published in `pmp-renewal-pdus`; externally corroborated | Consistent | MEDIUM–HIGH | Annually |
| 11 | Minimum 8 PDUs in each Talent Triangle area | `pmp-renewal-pdus` | **UNVERIFIED at source** | MEDIUM | Annually |
| 12 | **Minimum 35 of the 60 PDUs from Education** | One secondary source; consistent with the commonly described structure | **UNVERIFIED** | **LOW–MEDIUM** | Before publication |
| 13 | Giving Back is capped | `pmp-renewal-pdus` says caps exist without numbers | **UNVERIFIED, and the number is missing** | LOW | Before publication |
| 14 | 3 exam attempts within a 1-year eligibility period | Secondary | **UNVERIFIED** | MEDIUM | Before publication |
| 15 | 30-day wait between attempts | Secondary | **UNVERIFIED** | LOW–MEDIUM | Before publication |
| 16 | 1-year lockout after 3 failures, then a new application | Secondary | **UNVERIFIED** | LOW–MEDIUM | Before publication |
| 17 | 35 contact hours required for the application | `pmp-eligibility`, widely corroborated | Consistent | MEDIUM–HIGH | Annually |
| 18 | An active CAPM can satisfy the 35 hours | `pmp-eligibility` | **UNVERIFIED at source** | MEDIUM | Before publication |
| 19 | Membership is optional, never required | No source disputes it | Consistent | HIGH | — |

**Fact 12 is load-bearing.** The claim that "your job does not cover your PDUs" depends on
it. Without verification, that paragraph must be rewritten to state only what
`pmp-renewal-pdus` already supports — that caps exist — or cut.

---

## 3. The ATP change — the most important open question

| # | Fact | Status | Confidence | Action |
|---|---|---|---|---|
| 20 | A change to how the 35 contact hours may be delivered takes effect **late Q4 2026** | **UNVERIFIED** | MEDIUM | Verify at PMI |
| 21 | Approved routes include PMI Authorized Training Partners | **UNVERIFIED** | MEDIUM | Verify |
| 22 | GAC-accredited academic programmes qualify | **UNVERIFIED** | LOW–MEDIUM | Verify |
| 23 | China Registered Education Providers qualify | From `pmp-eligibility`; not corroborated externally | **UNVERIFIED** | Verify |
| 24 | An active CAPM waiver qualifies | **UNVERIFIED** | LOW–MEDIUM | Verify |
| 25 | **Whether the restriction covers all 35 hours or only live instructor-led training** | **UNVERIFIED — sources directly contradict each other** | **LOW** | **Verify before publication. This is the single most consequential unknown in the article** |

If fact 25 cannot be resolved, the article must present **both** readings and their
different consequences for the education floor — which is what the architecture already
proposes. That is publishable. Asserting either one is not.

---

## 4. Facts that are settled, and one that never will be

| # | Fact | Status | Confidence |
|---|---|---|---|
| 26 | **No reliable PMP pass rate exists.** PMI has not published one in ~20 years; the circulating "61%" is a passing score retired around 2006 | Established in `pmp-pass-rate` | **UNKNOWABLE — permanently** |
| 27 | PMI scores psychometrically and reports performance bands, not a percentage | `pmp-pass-rate` | MEDIUM–HIGH |
| 28 | The exam was updated 9 July 2026; People 33% / Process 41% / Business Environment 26% | `how-to-prepare-for-pmp-exam` | MEDIUM–HIGH |
| 29 | Eligibility: 36 months with a four-year degree, 60 months with a secondary diploma | `pmp-eligibility` | MEDIUM–HIGH |

**Fact 26 licenses the article's refusal to compute an expected cost.** It needs no
further verification — the absence of the data *is* the verified finding.

---

## 5. Internal contradictions to resolve before publishing

These are CertNorth disagreeing with itself. All four must be settled, and the fix may
touch files beyond `pmp-cost`.

| # | Contradiction | Files affected | Resolution |
|---|---|---|---|
| 30 | Membership is "about $140/yr" in `pmp-cost` but "roughly $150/yr" in `is-pmi-membership-worth-it` | 2 articles | Verify at PMI, then make both say the same thing |
| 31 | `pmp-cost` implies a retake costs another full exam fee | `pmp-cost` | Correct if fact 8 verifies; cut if it does not |
| 32 | `certifications.json` carries `~$425 / ~$675` with `verifiedOn: 2026-07`. If the August increase is real this is stale — **and it feeds the `certTable` in `best-pm-certifications-beginners`** | `certifications.json`, and one further page | **Update the single source of truth, not the article.** Requires `verifiedOn` to be advanced honestly, which means someone actually checked |
| 33 | `pmp-renewal-pdus` leads its free-PDU list with "working in your certified role", which is Giving Back and therefore capped | `pmp-renewal-pdus` | Only if fact 12 verifies. **Requires approval — it is a second article** |

**Contradictions 32 and 33 are outside `pmp-cost`.** They are recorded here, not fixed.
Touching `certifications.json` changes a second published page and needs explicit
approval.

---

## 6. Recurring re-verification schedule

If this article ships, it creates an ongoing obligation the editorial policy already
promises:

| Cadence | Items |
|---|---|
| Every 6 months | Facts 1, 2, 4, 5, 6, 7, 8, 9 — all prices |
| Annually | Facts 10, 11, 17 — PDU and education requirements |
| On any PMI announcement | Facts 1–3, 20–25 |
| Once, then closed | Fact 3 (did the August 2026 change happen), fact 25 (ATP scope) |

`certifications.json` currently carries `verifiedOn: 2026-07` for all six certifications.
The build warns at six months, so the first automatic alert is due **January 2027**. This
article's publication is the natural moment to run the first real pass — which would make
the editorial policy's promise demonstrable rather than merely stated.

---

## 7. The single instruction for whoever verifies

Open `pmi.org` **logged in from the country the reader is being advised for**, and record,
with the date and a screenshot reference:

1. PMP exam fee, member and non-member, **as displayed at checkout**
2. Whether the displayed currency and amount differ from the USD figure published on the
   general certification page — this settles the regional-pricing question
3. PMI membership fee and application fee
4. Certification renewal fee, member and non-member
5. Retake / re-examination fee
6. The PDU category minimums and maximums in the current CCR Handbook
7. The exact wording of the late-2026 training-provider requirement — **specifically
   whether it applies to all 35 contact hours or only to live instructor-led training**

Item 2 is the one that decides whether this article can state any universal number at all.
