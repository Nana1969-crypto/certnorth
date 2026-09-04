# Proposed Article Architecture — `pmp-cost`

**Date:** 2026-09-04
**Revised:** 2026-09-04 — retake section removed, sourcing-claim fix added (see §7)
**Status:** proposal. Nothing drafted, nothing published, no article modified.

---

## 1. Identity

| Field | Value |
|---|---|
| **Working title (H1)** | What the PMP Really Costs — and What Nobody Can Confirm |
| **`seo.metaTitle`** | `What the PMP Really Costs (And What Nobody Can Confirm)` — 55 chars, unique |
| **`intent.primaryKeyword`** | `pmp certification cost` — **unchanged**, no cannibalisation risk |
| **URL** | `/certifications/guides/pmp-certification-cost/` — **unchanged** |
| **`clusterId`** | `cl_guides` — unchanged |
| **`publishedAt`** | **unchanged** (2026-07-25) |
| **`updatedAt`** | set to the real rebuild date — this is a genuine revision |
| **Content type** | RESEARCH, not DECISION — a deliberate shift; the site sits at 34% DECISION |

**Search intent:** commercial investigation. The reader is close to spending and wants the
real total, not the sticker price.

**Editorial question:** *"What will I realistically spend to obtain and keep the PMP, and
which costs am I most likely to underestimate?"*

**Unique angle:** the page states openly which figures can be confirmed and which cannot —
and supplies the complete cost structure anyway, including a ten-year model the reader can
re-run with their own numbers.

---

## 2. Anti-template compliance

| Site-wide pattern | Frequency | This article |
|---|---|---|
| Block 1 paragraph → block 2 callout | 50 / 50 | **Paragraph → H2 → table.** Second block is a heading |
| Contains an FAQ block | 50 / 50 | **No FAQ** — see §6.1 |
| Leads with a price table | common | Leads with an **uncertainty ledger** |
| "The case for it / against it / The honest bottom line" | 8 articles | Not used |
| Several callouts per article | typical | **One**, carrying the CERTNORTH CALCULATION |
| Title contains "2026" | 24 / 50 | **No year** — the page argues that fixed figures go stale |

All eight proposed H2 headings checked against the **215 distinct level-2 headings** on the
site: **zero collisions.**

---

## 3. Section plan

Every section is labelled with the evidence class it rests on.

| # | Block | Section | Evidence class | Original analysis |
|---|---|---|---|---|
| 0 | paragraph | Opens on what this page can and cannot tell you, and why | EDITORIAL INFERENCE | Frames uncertainty as subject, not disclaimer |
| 1 | H2 | *What we can confirm, and what we can't* | — | — |
| 2 | **table** | Claim · what we can say about it · what still needs checking. Covers exam fee, membership, renewal, PDUs, training, regional pricing | REPOSITORY + PRIMARY VERIFICATION REQUIRED | **The uncertainty ledger.** No competitor publishes one |
| 3 | paragraph | Why: PMI is the only source that settles this, and every other page you'll find sells PMP training | EDITORIAL INFERENCE | Names the conflict of interest in the evidence base |
| 4 | H2 | *Four kinds of cost, and only two are unavoidable* | — | — |
| 5 | **table** | Required / conditional / optional / recurring — trigger, recurrence, who sets the price | REPOSITORY + EDITORIAL INFERENCE | The taxonomy. Survives every figure being wrong |
| 6 | paragraph | The two unavoidable costs; the 35 hours are required but the amount is candidate-dependent | REPOSITORY | |
| 7 | H2 | *Joining PMI pays once. It does not keep paying.* | — | — |
| 8 | paragraph | Exam-time arithmetic | CERTNORTH CALCULATION | |
| 9 | **callout (info)** | **CERTNORTH CALCULATION**, inputs and their status stated inline | CERTNORTH CALCULATION | The only callout in the article |
| 10 | paragraph | Why the renewal discount does not justify membership. Links `is-pmi-membership-worth-it` | CERTNORTH CALCULATION | **Corrects a claim the industry repeats** |
| 11 | H2 | *Ten years of ownership, with the assumptions on the table* | — | — |
| 12 | **table** | Scenarios A and B at 5 and 10 years; assumptions in the caption | CERTNORTH CALCULATION | The model |
| 13 | paragraph | Keeping membership ten years costs ~$990–$1,080 more and saves $270 | CERTNORTH CALCULATION | Counterintuitive, checkable |
| 14 | H2 | *Sixty PDUs can cost nothing and still cost sixty hours* | — | — |
| 15 | paragraph | Financial cost vs time commitment, never monetised. Links `pmp-renewal-pdus` | REPOSITORY + CERTNORTH CALCULATION | Separation most pages collapse |
| 16 | H2 | *Three costs we could not price, and why we are not guessing* | — | — |
| 17 | paragraph | Training, retakes, and regional pricing — what we could not establish, and the refusal to compute an expected cost. Links `pmp-pass-rate` | PRIMARY VERIFICATION REQUIRED | **A refusal, explained.** Distinctive on its own |
| 18 | H2 | *The change that could move your budget most* | — | — |
| 19 | paragraph | The late-Q4-2026 training rule, its unresolved scope, and both consequences. Links `pmp-eligibility` | REPOSITORY + PRIMARY VERIFICATION REQUIRED | Names the largest live variable |
| 20 | H2 | *How to work out your own number* | — | — |
| 21 | **list (ordered)** | Check the price in your own PMI account; decide membership before booking; confirm your training provider qualifies; budget renewals, not just the exam | EDITORIAL INFERENCE | Turns analysis into an action |
| 22 | paragraph | Close. Links `is-pmp-worth-it` and `pmp-vs-capm` | — | |

**8 level-2 headings** (GATE minimum 2) · **5 internal links** (minimum 1) ·
**sources: 4+** (minimum 1), and they must now include the **CCR Handbook** and the
**PMP Handbook**, which the current article omits.

---

## 4. What changed in this revision, and why

| Earlier plan | Now | Reason |
|---|---|---|
| A dedicated section: *"A retake is not another exam fee"* | **Removed.** Retakes appear only in §16–17 as a cost we could not price | The reduced-fee figure was SECONDARY/SEARCH DISCOVERY ONLY. We cannot assert it, and correcting our own article on unverified evidence would repeat the original error |
| Scenario C, one retake, $275 | **Removed** | Same reason |
| Membership modelled at $149 | **$140–$150 range** | The range is the site's own internal contradiction, shown rather than resolved |
| Exam modelled at $445/$675 | **~$425/~$675** | Repository values. Search figures are questions, not corrections |
| — | **New: remove the "every figure sourced from PMI" claim** | See §7 |

---

## 5. What must NOT go in this article

| Excluded | Because |
|---|---|
| A confident single "the PMP costs $X" | Regional pricing unresolved |
| An average or typical training cost | No neutral data exists |
| A pass-rate-weighted expected cost | No reliable pass rate exists |
| A retake fee, in either direction | Unverified; the site's own claim is unsourced |
| A monetary value for study hours | Arbitrary |
| **"Every figure sourced from PMI"** | **Untrue** — see §7 |
| Full PDU mechanics | Owned by `pmp-renewal-pdus` — summarise and link |
| Eligibility pathways | Owned by `pmp-eligibility` — link only |
| Exam format and study method | Owned by `how-to-prepare-for-pmp-exam` |
| The pass-rate argument in full | Owned by `pmp-pass-rate` — one sentence and a link |
| Membership benefits beyond money | Owned by `is-pmi-membership-worth-it` |
| Whether the PMP is worth getting | Owned by `is-pmp-worth-it` |
| A "related articles" block | Prohibited. Links go inside sentences that already raise the subject |

---

## 6. Consolidation map

`pmp-cost` becomes the definitive CertNorth page for **the economics of getting and keeping
the PMP** — and nothing else.

| Information | Decision |
|---|---|
| Exam, membership, renewal fees | **Retained** — the page's subject |
| Cost taxonomy, break-even, 5/10-year model, time-vs-money | **Retained** — new, belongs nowhere else |
| Uncertainty ledger | **Retained** — new |
| PDU mechanics | **Summarised + linked** to `pmp-renewal-pdus` |
| Eligibility pathways | **Removed + linked** to `pmp-eligibility` |
| Pass-rate reasoning | **One sentence + linked** to `pmp-pass-rate` |
| Membership benefits beyond money | **Removed + linked** to `is-pmi-membership-worth-it` |
| Study time and preparation | **Removed + linked** to `how-to-prepare-for-pmp-exam` |
| "Is it worth it" verdict | **Removed + linked** to `is-pmp-worth-it` |

**Inbound links unaffected.** URL, slug and primary keyword unchanged, so all 11 existing
inbound links continue to resolve.

**One new outbound link:** `pmp-pass-rate`, which the current article does not link. It is
the evidence for the refusal to compute an expected cost.

### 6.1 Dropping the FAQ

`platform/src/build.js` `runGate()` was read directly. It requires a valid cluster, unique
primary keyword, unique slug, metaTitle ≤60, metaDescription ≤155, an author bio ≥40
chars, `publishedAt`, a dek ≥40 chars, **≥2 level-2 headings**, ≥1 internal link, ≥1
source. **An FAQ block is not required.** Dropping it will not break the build.

**Trade-off:** the FAQ block feeds `FAQPage` structured data. Whether that still yields any
visible search benefit could not be verified from this environment. What is certain is that
all 50 articles currently carry one, and that an FAQ here would restate the body — which is
padding.

**Recommendation: drop it.** If the loss of `FAQPage` schema matters to you, it stays.

---

## 7. The one change that should happen regardless

`pmp-cost` states three times that its figures come from PMI:

- `body[0]`: *"with every fee sourced from PMI"*
- `body[3]` table caption: *"(source: PMI)"*
- `seo.metaDescription`: *"Every figure sourced from PMI."*

**The same table contains "Required education (35 contact hours) | $0–$600 depending on
provider", and the article's second table prices third-party training at $700–$2,500+.
PMI does not sell PMP training and does not publish its price.**

**Label: VERIFIED FROM CERTNORTH REPOSITORY.** The claim and the content that disproves it
are in the same file.

This is a statement about our own sourcing integrity, on a site whose entire position is
independence and verifiability. **It should be corrected whether or not the rebuild
proceeds**, and it is the one change in this whole plan that requires no external
verification at all.

---

## 8. Can the architecture be finalised despite the unresolved facts?

**Yes — with one dependency.**

| Element | Status |
|---|---|
| Editorial question and angle | **Final** |
| Section order and headings | **Final** — collision-checked |
| Cost taxonomy | **Final** — independent of every price |
| Structural anti-template decisions | **Final** |
| Internal links and consolidation map | **Final** |
| Sources list | **Final** — must add the CCR Handbook and the PMP Handbook |
| Time-vs-money framework | **Final** |
| Refusal to compute an expected cost | **Final** — rests on a permanent finding |
| **Every monetary figure** | **Blocked** on primary-source verification |
| **The uncertainty ledger's contents** | **Partly blocked** — its shape is final, its rows change depending on what verification finds |

**The article cannot be drafted to publication standard until a human reads PMI's current
prices.** It *can* be drafted as a complete structure with figures held as placeholders,
if you want to see the shape before committing to the verification work.
