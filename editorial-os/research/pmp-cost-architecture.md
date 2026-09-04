# Proposed Article Architecture — `pmp-cost`

**Date:** 2026-09-04
**Status:** proposal. Nothing drafted, nothing published.

---

## 1. Identity

| Field | Value |
|---|---|
| **Working title (H1)** | What the PMP Really Costs — and What Nobody Can Confirm |
| **`seo.metaTitle`** | `What the PMP Really Costs (And What Nobody Can Confirm)` — 55 chars, unique |
| **`intent.primaryKeyword`** | `pmp certification cost` — **unchanged**, so no cannibalisation risk |
| **URL** | `/certifications/guides/pmp-certification-cost/` — **unchanged** |
| **`clusterId`** | `cl_guides` — unchanged |
| **`publishedAt`** | **unchanged** (2026-07-25) |
| **`updatedAt`** | set to the real rebuild date — this *is* a genuine revision |
| **Content type** | RESEARCH, not DECISION. A deliberate shift: the site is 34% DECISION and near its threshold |

**Search intent:** commercial investigation. The reader is close to spending money and
wants to know the real total, not the sticker price.

**Editorial question:** *"What will I realistically spend to obtain and keep the PMP, and
which of those costs am I most likely to underestimate?"*

**Unique angle:** the page states openly that the headline fee cannot be confirmed —
because PMI appears to price by region, because the fee changed in August 2026, and
because every confident figure online comes from a company selling PMP training — and
then supplies the complete cost structure anyway, including a ten-year model the reader
can run with their own numbers.

---

## 2. Anti-template compliance

The site's measured habits and what this article does instead:

| Site-wide pattern | Frequency | This article |
|---|---|---|
| Block 1 paragraph → block 2 callout | 50 / 50 | **Paragraph → H2 → table.** The second block is a heading |
| Contains an FAQ block | 50 / 50 | **No FAQ** — see §6 |
| Leads with a price/comparison table | common | Leads with an **uncertainty ledger**: claim, evidence, confidence |
| "The case for it / against it / The honest bottom line" | 8 articles | Not used |
| Multiple callouts per article | typical | **One** callout in the whole piece, carrying the CERTNORTH CALCULATION |
| Title contains "2026" | 24 / 50 | **No year in the title** — the page argues that fixed figures go stale |

All eight proposed H2 headings were checked against the 215 distinct level-2 headings
already on the site. **Zero collisions.**

---

## 3. Section plan

| # | Block | Section | Evidence needed | Original analysis contributed |
|---|---|---|---|---|
| 0 | paragraph | Opens on the finding: the confident numbers online come from companies selling PMP training, PMI's price appears to vary by country, and it changed in August 2026 | Dossier §1, §3.1, §3.5 | Frames uncertainty as the subject, not a disclaimer |
| 1 | H2 | *What can be confirmed, and what can't* | — | — |
| 2 | **table** | Claim · best available evidence · confidence. Exam fee, membership, renewal, retake, regional pricing, ATP rule | Dossier §3, §4 | **The uncertainty ledger.** No competitor publishes one |
| 3 | paragraph | Why: PMI is the only tier-2 source and it is not reachable from here; every other source sells training | Dossier §1 | Names the conflict of interest in the evidence base |
| 4 | H2 | *Four kinds of cost, and only two are unavoidable* | — | — |
| 5 | **table** | Required / conditional / optional / recurring — what triggers each, whether it recurs, whether it varies by country | Cost model §1 | The taxonomy. PMI has no reason to publish it |
| 6 | paragraph | The two genuinely unavoidable costs, and why the 35 contact hours are required but nearly free today | Cost model §1A, §3 | |
| 7 | H2 | *Joining PMI pays once. It does not keep paying.* | — | — |
| 8 | paragraph | Exam-time arithmetic | Cost model §2.1 | |
| 9 | **callout (info)** | **CERTNORTH CALCULATION** — break-even in both directions, with sensitivity across the membership figures found | Cost model §2 | The only calculation block in the article |
| 10 | paragraph | Correction: "non-members pay $90 more to renew, so membership pays for itself" is false. Links `is-pmi-membership-worth-it` | Dossier §6 | **Corrects a claim the industry repeats** |
| 11 | H2 | *A retake is not another exam fee* | — | — |
| 12 | paragraph | Reduced retake fee, three attempts in a one-year eligibility window, 30-day wait, one-year lockout after three failures | Dossier §3.4 | **Corrects CertNorth's own current article** |
| 13 | paragraph | Why no expected-cost calculation: no reliable pass rate exists. Links `pmp-pass-rate` | Dossier §5 | A refusal, explained — itself a differentiator |
| 14 | H2 | *Ten years of ownership, with the assumptions on the table* | — | — |
| 15 | **table** | Scenarios A / B / C at 5 and 10 years, assumptions in the caption | Original value plan §3 | The model |
| 16 | paragraph | The counterintuitive result: keeping membership ten years costs ~$1,071 more and saves $270 in renewals | Original value plan §3 | |
| 17 | H2 | *Sixty PDUs can cost nothing and still cost sixty hours* | — | — |
| 18 | paragraph | Financial cost vs time commitment, never monetised. The 35-Education floor means "your job covers it" is wrong. Links `pmp-renewal-pdus` | Cost model §4 | **Corrects an implication in CertNorth's own renewal article** |
| 19 | H2 | *The change that could move your budget most* | — | — |
| 20 | paragraph | The late-Q4-2026 ATP requirement, both possible scopes and what each does to the education floor. Links `pmp-eligibility` | Dossier §3.7, cost model §3 | Names the largest live variable; no source found states its scope |
| 21 | H2 | *How to work out your own number* | — | — |
| 22 | **list (ordered)** | The procedure: check the price in your own PMI account, decide membership before booking, confirm the training provider qualifies, budget renewals not just the exam, treat retakes as a time risk | All | Turns the analysis into an action the reader can complete |
| 23 | paragraph | Close. Links `is-pmp-worth-it` (whether to spend at all) and `pmp-vs-capm` (the cheaper route) | — | |

**8 level-2 headings** (GATE minimum 2). **5 internal links** (GATE minimum 1).
**Sources: 4+** (GATE minimum 1).

---

## 4. What must NOT go in this article

| Excluded | Because |
|---|---|
| A confident single "the PMP costs $X" | Regional pricing is disputed and unresolved |
| An "average" or "typical" training cost | No neutral data exists; every source quoting one sells training |
| A pass-rate-weighted expected cost | No reliable pass rate exists |
| A monetary value assigned to study hours | Arbitrary, and the prompt correctly forbids it |
| Full PDU mechanics — Talent Triangle areas, category caps, the free-routes list | Owned by `pmp-renewal-pdus`. Summarise and link |
| Full eligibility rules — the 36/60-month pathways | Owned by `pmp-eligibility`. Link only |
| Exam format, domain weights, study method | Owned by `how-to-prepare-for-pmp-exam` |
| The pass-rate argument in full | Owned by `pmp-pass-rate`. One sentence and a link |
| The complete membership-benefits case | Owned by `is-pmi-membership-worth-it`. Only the money belongs here |
| Whether the PMP is worth getting at all | Owned by `is-pmp-worth-it` |
| A "related articles" block | Prohibited. Links go inside sentences that already raise the subject |

---

## 5. Consolidation map (Phase 12)

`pmp-cost` becomes the definitive CertNorth page for **the economics of getting and
keeping the PMP** — and nothing else.

| Information | Decision |
|---|---|
| Exam fee, membership fee, renewal fee, retake fee | **Retained** — this is the page's subject |
| Cost taxonomy, break-even, 5/10-year model, time-vs-money | **Retained** — new, and belongs nowhere else |
| Uncertainty ledger | **Retained** — new |
| PDU mechanics | **Summarised + linked** to `pmp-renewal-pdus` |
| Eligibility pathways | **Removed + linked** to `pmp-eligibility` |
| Pass-rate reasoning | **One sentence + linked** to `pmp-pass-rate` |
| Membership benefits beyond money | **Removed + linked** to `is-pmi-membership-worth-it` |
| Study time and exam preparation | **Removed + linked** to `how-to-prepare-for-pmp-exam` |
| "Is it worth it" verdict | **Removed + linked** to `is-pmp-worth-it` |

**Inbound links are unaffected.** The URL, slug and primary keyword do not change, so all
11 existing inbound links continue to resolve.

**One outbound link is added** that does not exist today: `pmp-pass-rate`, which the
current article does not link. It is the evidence for the article's refusal to compute an
expected cost.

---

## 6. Two decisions the Editor-in-Chief should make

### 6.1 Dropping the FAQ block

The GATE was read directly (`platform/src/build.js`, `runGate`). It requires: valid
cluster, unique primary keyword, unique slug, metaTitle ≤60, metaDescription ≤155, an
author with a bio ≥40 chars, `publishedAt`, a dek ≥40 chars, **≥2 level-2 headings**, ≥1
internal link, ≥1 source. **An FAQ block is not required.** Dropping it will not break
the build.

**Trade-off:** the FAQ block feeds `FAQPage` structured data. Whether that still produces
any visible search benefit could not be verified from this environment. What is certain
is that every one of the 50 articles currently carries one, and that an FAQ here would
restate what the body already says — which is padding.

**Recommendation: drop it**, and let this article be the first structural exception. If
the loss of `FAQPage` schema matters to you, say so and it stays.

### 6.2 The unverified fee

The article can be built either way:

| Option | What the page says |
|---|---|
| **A — publish with the uncertainty stated** | "Reported at $445 member / $675 non-member effective 6 August 2026, from secondary sources. We could not confirm this with PMI, and PMI appears to price by country — check your own account." |
| **B — hold until a human verifies at PMI** | The page waits. Someone opens pmi.org, reads the current fee, and the figure ships verified |

**Recommendation: B, if you can spare ten minutes.** Option A is honest and publishable,
but this is the one number the previous audit singled out as failing the site's own
standard, and the rebuild is the natural moment to fix it rather than document it again.

If B is chosen, the same visit should also confirm the membership fee, the renewal fee,
the retake fee, the PDU category split, and the scope of the ATP rule — see
`pmp-cost-fact-check-plan.md`.
