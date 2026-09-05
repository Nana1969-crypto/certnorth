# Source Verification — `best-pm-certifications-beginners` (REBUILD 03)

**Status:** consolidated with the Editor-in-Chief's primary-source evidence package.
**Package supplied:** September 4, 2026
**Input:** `editorial-os/research/best-pm-certifications-beginners-diagnostic.md` (commit `3d7cada`)
**Phase:** verification only. No article written, no draft created, production untouched.

---

## 1. Verification summary

### 1.1 How the evidence was obtained

Route D1 was approved. **This session could not execute it**: the environment has no outbound
web access at all — every external host returns `403 CONNECT tunnel failed` at the proxy,
including control hosts unrelated to certification bodies. The proxy documentation directs
that such denials be reported, not retried or routed around, and they were not.

**The Editor-in-Chief therefore performed the primary-source verification externally and
supplied the results.** Everything classified as verified below rests on that package and on
nothing else. No web access was attempted in this phase. No figure was completed from general
knowledge, memory, search snippets, caches or secondary sources.

### 1.2 Status of the tracked items

The seven items from the diagnostic, plus the conditionally approved PRINCE2 eighth, plus one
item the package settles that was not on the original list (CAPM education hours).

| # | Item | Before | **Now** |
|---|---|---|---|
| 1 | CAPM exam fee $225 / $300 | NOT VERIFIED | **NOT VERIFIED** |
| 2 | CAPM renewal cycle | **CONTRADICTORY** | **VERIFIED** — and expanded |
| 3 | Google price | NOT VERIFIED | **VERIFIED WITH CONDITIONS** |
| 4 | Google hours → CAPM's 23 | NOT VERIFIED | **NOT VERIFIED** |
| 5 | Google duration | NOT VERIFIED | **VERIFIED WITH CONDITIONS** |
| 6 | PSM I fee | NOT VERIFIED | **VERIFIED** — as a per-attempt fee |
| 7 | CSM cost and renewal | NOT VERIFIED | **PARTIALLY VERIFIED** — renewal yes, acquisition no |
| 8 | PRINCE2 | NOT VERIFIED | **VERIFIED WITH CONDITIONS** |
| 9 | CAPM education hours *(new)* | — | **VERIFIED** |

**VERIFIED: 3 · VERIFIED WITH CONDITIONS: 3 · PARTIALLY VERIFIED: 1 · NOT VERIFIED: 2**

At the level of discrete facts rather than tracked items: **15 VERIFIED · 10 VERIFIED WITH
CONDITIONS**, enumerated in §2.

### 1.3 What changed most

**The one real contradiction is resolved, and in the repository's favour.** §8.1 of the
previous version recorded the CAPM renewal cycle as three years (CertNorth) against five years
(in circulation), and deliberately refused to choose. **The package settles it: the cycle is
three years.** The five-year figure is incorrect as a statement of the current rule.

Two things follow. CertNorth was right, and would have been wrong to "correct" itself toward
the more widely repeated number — which is precisely what the standing protocol against
secondary convergence exists to prevent. And CertNorth's record, while right, was
**incomplete**: it carried the cycle and the total, and omitted the composition limits that
determine whether a holder actually satisfies it.

### 1.4 What did not change

**No price for acquiring the CAPM or the CSM is verified.** Those were the two figures most
widely repeated across the site, and both remain unusable. §3 sets out why this matters more
than it appears: after consolidation, **there is still no comparable "cost to obtain" figure
across the five credentials** — and that is now an evidenced finding rather than an
editorial suspicion.

---

## 2. Credential-by-credential verification

Recorded strictly as the package states it. Where the package is silent, the entry is
**NOT VERIFIED** and the silence is stated rather than filled.

---

### 2.1 CAPM — maintenance and renewal · **VERIFIED**

| Fact | Status |
|---|---|
| Renewal cycle of **3 years** | **VERIFIED** |
| **15 PDUs** per cycle | **VERIFIED** |
| Minimum **9 Education** PDUs | **VERIFIED** |
| Maximum **6 Giving Back** PDUs | **VERIFIED** |
| Minimum **2 PDUs in each area of the PMI Talent Triangle** | **VERIFIED** |

**Source:** PMI, via the Editor-in-Chief's package · **Date:** 2026-09-04

**The five-year validity figure is incorrect as a statement of the current rule.** The package
establishes it as wrong for the rule in force; it does not establish whether it was ever
correct historically, and this file does not claim either way.

**CERTNORTH CALCULATION — the composition is fully determined.** Minimum 9 Education plus
maximum 6 Giving Back is exactly 15, which is the total. So a holder taking the maximum 6
Giving Back must take exactly 9 Education, and any reduction in Giving Back must be matched
one-for-one by additional Education. **There is no discretionary remainder.** Inputs verified
above; arithmetic performed here.

**What this does NOT establish:**
- **How many areas the PMI Talent Triangle has.** The package says "each area" without
  enumerating them. The minimum spread implied by the 2-PDU-per-area rule therefore
  **cannot be calculated**, and the areas must not be named in the article.
- Whether a **renewal fee** applies to the CAPM. The package is silent. `certifications.json`
  records none; that remains unverified either way.
- What the renewal costs in time or money.
- Any comparison with the PMP's cycle. *(The PMP's own PDU rules were verified separately on
  2026-09-04: 60 PDUs / 3 years, ≥35 Education, ≤25 Giving Back, ≤8 Work as a Practitioner.
  The two rule sets must not be conflated or presented as one system.)*

**Effect on CertNorth's record.** `certifications.json` publishes `15 PDUs every 3 years`.
That is **correct but incomplete** — it omits all three composition limits, which are the part
that determines whether a holder can actually satisfy the requirement. **No change is made to
that file in this phase.**

---

### 2.2 CAPM — education requirement · **VERIFIED**

| Fact | Status |
|---|---|
| **23 hours** of education are required | **VERIFIED** |
| **PMI's official training satisfies those 23 hours** | **VERIFIED** |

**Source:** PMI, via the package · **Date:** 2026-09-04

**What this does NOT establish — and the distinction is load-bearing:**
- That **any other provider's** training satisfies the 23 hours. The package verifies PMI's own
  training only.
- **Specifically, it does not establish that the Google Project Management Certificate
  satisfies them.** See §2.4.
- What PMI's official training costs, or how long it takes.
- Whether other routes to the 23 hours exist.

---

### 2.3 CAPM — exam fee · **NOT VERIFIED**

| | |
|---|---|
| **CertNorth publishes** | `$225 member / $300 non-member` — `certifications.json` (`verifiedOn: 2026-07`), article block 27, `pmp-vs-capm` table and FAQ, `is-capm-worth-it` body and table |
| **Package** | **Does not verify this figure** |
| **Status** | **NOT VERIFIED — do not reuse** |

**Explicitly instructed not to reuse.** The figure appears in **four articles** and must not be
stated as a verified price in the rebuild.

**What remains unknown:** the fee itself; whether it varies by country; the retake fee. PMI is
known to price the PMP regionally, and nothing establishes that the CAPM is uniform.

---

### 2.4 Google Project Management Certificate — price and duration · **VERIFIED WITH CONDITIONS**

| Fact | Status |
|---|---|
| **US$49 per month** in the **US and Canada**, per the source | **VERIFIED WITH CONDITIONS** |
| Many learners complete in **3–6 months** | **VERIFIED WITH CONDITIONS** |
| Coursera states completion in **under 6 months** is possible | **VERIFIED WITH CONDITIONS** |
| **Most learners can complete for under US$300** in the US and Canada | **VERIFIED WITH CONDITIONS** |
| **Prices may differ in other countries** | **VERIFIED** |
| **No prior knowledge required** | **VERIFIED WITH CONDITIONS** |

**Source:** Coursera, via the package · **Date:** 2026-09-04
**Condition on every price figure: US and Canada only.**

**US$49 is a monthly subscription, not the price of the certificate.** It must never be
labelled as a certificate price, an exam fee, or a total. What a learner pays depends on how
long they take, which is why the under-US$300 figure is expressed as what most learners *can*
achieve rather than what the certificate costs.

**What this does NOT establish:**
- The price in any country outside the US and Canada. The package states they may differ; it
  does not say what they are.
- What any **individual** learner pays — the subscription makes the total pace-dependent.
- How long learners **actually** take. "Many complete in 3–6 months" and "completion in under
  6 months is possible" are both statements about what happens or is achievable, not a
  completion rate.
- Any completion or outcome rate.
- Whether the certificate expires. **The package is silent.** `certifications.json` records
  "None — does not expire"; that remains **NOT VERIFIED**.

---

### 2.5 Google → CAPM education credit · **NOT VERIFIED**

| | |
|---|---|
| **CertNorth publishes** | *"even counts toward the education requirement for the CAPM"* (article block 25) · *"Counts toward the 23 education hours the CAPM requires"* (`google-pm-certificate-worth-it`) · asserted twice more in `capm-vs-google-pm-certificate` |
| **Package** | Verifies that **PMI's official training** satisfies the 23 hours (§2.2). **It does not verify that the Google certificate does** |
| **Status** | **NOT VERIFIED — must not be written as fact** |

This is the item with the widest blast radius. **The site's "do the Google certificate first,
then the CAPM" recommendation appears in three articles and rests entirely on this
mechanism.** With the mechanism unverified, the recommendation loses its stated basis.

**The original sourcing defect also stands, independently of the answer.** The claim is cited
to Google/Coursera, but the rule belongs to PMI. A provider is not an authority on another
body's eligibility criteria, and has a direct commercial interest in the claim being believed.

**Absence of evidence is not evidence of absence.** This file does not assert that the Google
certificate fails to qualify. It asserts that nothing available establishes that it does.

---

### 2.6 PSM I · **VERIFIED**

| Fact | Status |
|---|---|
| **US$200 per assessment attempt** | **VERIFIED** |
| **80 questions** | **VERIFIED** |
| **60 minutes** | **VERIFIED** |
| Passing score **85%** | **VERIFIED** |
| The test password **does not expire until used** | **VERIFIED** |

**Source:** Scrum.org, via the package · **Date:** 2026-09-04

**The figure must be described as US$200 per assessment attempt** — not as the cost of the
certification, and not as a guaranteed total. With an 85% pass mark, a second attempt is a
real possibility, and a reader told "$200" without "per attempt" has been given a floor
presented as a price.

**What this does NOT establish:**
- **Whether the certification expires.** The package is silent. `certifications.json` records
  "None — never expires", and `best-agile-certifications` says "you own it for life with no
  renewal fees". **Both remain NOT VERIFIED.**
- The cost of preparing, which for a self-study credential is the larger variable.
- Whether training is required or optional.
- That US$200 is the cheapest of anything. See §6, claim C5.

---

### 2.7 CSM · **PARTIALLY VERIFIED**

| Fact | Status |
|---|---|
| **2-year** validity / renewal cycle | **VERIFIED** |
| **20 SEUs** per cycle | **VERIFIED** |
| **US$100** renewal fee | **VERIFIED** |
| ~US$800–US$1,500 to obtain initially | **NOT VERIFIED — do not publish as a current verified price** |

**Source:** Scrum Alliance, via the package · **Date:** 2026-09-04

**The item is split.** Everything verified concerns **keeping** the credential. Nothing
verified concerns **getting** it.

**What this does NOT establish:**
- **Any acquisition cost.** Explicitly refused.
- **Whether the two-day course is mandatory.** The package is silent, and this is not a minor
  omission: it is the article's stated explanation for the CSM's price (*"The CSM looks
  expensive because a two-day course is mandatory"*), and it is `certifications.json`'s
  `training` value. **NOT VERIFIED.**
- Whether an exam exists or what it involves.
- What SEUs cost to obtain, in money or time.

---

### 2.8 PRINCE2 · **VERIFIED WITH CONDITIONS**

| Fact | Status |
|---|---|
| Official name: **PRINCE2 Project Management Foundation (Version 7)** | **VERIFIED** |
| Renewal every **3 years** | **VERIFIED WITH CONDITIONS** |
| **60 CPD points** | **VERIFIED WITH CONDITIONS** |
| **US$701** for the option/package displayed on the page consulted | **VERIFIED WITH CONDITIONS** |

**Source:** PeopleCert, via the package · **Date:** 2026-09-04

**US$701 is a displayed package price, not a universal price and not an exam fee.** The
package identifies it as the price of the option shown on the page consulted. It must never be
presented as *the* price of PRINCE2.

**The naming risk flagged in the previous version was real.** CertNorth publishes
`PRINCE2 Foundation & Practitioner (7th edition)`. The verified official name of the
qualification is **PRINCE2 Project Management Foundation (Version 7)**. These are not the same
label. **The CertNorth name field is NOT VERIFIED and appears superseded** — and the blueprint's
single approved PRINCE2 sentence could not have been written correctly without this.

**What this does NOT establish:**
- What the US$701 package **contains** — whether training, exam, materials, or a combination.
- The price of any other option, or the price in any other region.
- Prerequisites, or whether training is mandatory.
- Exam format.
- That a combined "Foundation & Practitioner" product exists under the name CertNorth
  publishes.
- Recognition or usage outside the markets where PRINCE2 is established.
- Whether the 3-year / 60-CPD obligation attaches to the **Foundation** qualification, the
  Practitioner, or both. See §8.1.

---

## 3. Pricing verification

### 3.1 The five figures, after consolidation

| # | Credential | Verified figure | **What kind of quantity it is** | Currency | Region | Status |
|---|---|---|---|---|---|---|
| 1 | CAPM | — | **exam fee** | — | — | **NOT VERIFIED** |
| 3 | Google | US$49 / month | **monthly subscription** | USD | **US & Canada** | VERIFIED WITH CONDITIONS |
| 6 | PSM I | US$200 | **per assessment attempt** | USD | not stated | VERIFIED |
| 7 | CSM | US$100 | **renewal fee** | USD | not stated | VERIFIED |
| 8 | PRINCE2 | US$701 | **displayed package price** | USD | page consulted | VERIFIED WITH CONDITIONS |

Rules held: no currency converted · no price estimated · no figure rounded · no course price
presented as a credential price · no variable price presented as universal.

### 3.2 The comparability finding — now evidenced

**These are five different quantities.** They cannot be placed in one column, and a table
headed `examCost` containing all five is invalid regardless of how accurate each cell is.

Stronger, and this is the finding of the whole phase:

> **After primary-source verification, there is still no comparable "cost to obtain" figure
> across the five credentials.**

- **CAPM** — acquisition cost **NOT VERIFIED**
- **CSM** — acquisition cost **NOT VERIFIED**; only the renewal fee is verified
- **Google** — a subscription, so the total is pace-dependent by construction
- **PSM I** — verified, but per attempt, not per certification
- **PRINCE2** — verified, but for one displayed package of unknown contents

**Two of five have no verified acquisition figure at all, and the remaining three are three
different kinds of number.** The current article's `certTable` places all five under
`examCost`. That column cannot be made valid by better data, because the underlying quantities
are not the same quantity.

**This is the diagnostic's central thesis, confirmed by evidence rather than by argument.**
It is also a constraint on the rebuild, not a licence: it says the comparison must be
restructured, not that any credential is better than another.

---

## 4. Eligibility verification

| Credential | CertNorth publishes | Package | Status |
|---|---|---|---|
| CAPM — education | 23 contact hours | **23 hours required; PMI's official training satisfies them** | **VERIFIED** |
| CAPM — experience | None — secondary diploma only | **silent** | **NOT VERIFIED** |
| CAPM — via Google hours | asserted in 3 articles | **not established** | **NOT VERIFIED** (§2.5) |
| Google | No prerequisites | **No prior knowledge required** | **VERIFIED WITH CONDITIONS** |
| PSM I | No prerequisites; training not required | **silent** | **NOT VERIFIED** |
| CSM | No prerequisites; training **mandatory** | **silent** | **NOT VERIFIED** |
| PRINCE2 Foundation | None | **silent** | **NOT VERIFIED** |
| PMP | 36 months (bachelor's) / 60 (secondary) + 35 contact hours | **not in package** | **NOT VERIFIED at source** |

**Consequence for the approved architecture.** The blueprint's structural claim — that four of
the five require no experience and the fifth requires years — **is not verified.** Only the
Google certificate's "no prior knowledge required" is established, and the CAPM's, PSM I's,
CSM's and PRINCE2's experience requirements are all unconfirmed.

**The classification the article is built on therefore cannot be stated as verified fact for
four of five rows.** §10 records what this permits and forbids. It does not invalidate the
architecture — the *kinds* of product differ regardless — but it does forbid the sentence
"four of these five require no experience".

---

## 5. Maintenance and renewal verification

| Credential | CertNorth publishes | Package | Status |
|---|---|---|---|
| **CAPM** | 15 PDUs every 3 years | **3-year cycle · 15 PDUs · ≥9 Education · ≤6 Giving Back · ≥2 per Talent Triangle area** | **VERIFIED** — CertNorth correct but incomplete |
| **CSM** | Every 2 years (SEUs + fee) | **2 years · 20 SEUs · US$100** | **VERIFIED** — CertNorth correct but unquantified |
| **PRINCE2** | Practitioner every 3 years | **3 years · 60 CPD points** | **VERIFIED WITH CONDITIONS** — attribution unclear, §8.1 |
| **Google** | None — does not expire | **silent** | **NOT VERIFIED** |
| **PSM I** | None — never expires | **silent** | **NOT VERIFIED** |
| PMP | 60 PDUs / 3 yrs + $60/$150 fee | verified separately 2026-09-04 (rules); **fee NOT ESTABLISHED** | out of scope — PMP leaves the table |

### 5.1 The obligation asymmetry — partially evidenced, and the gap is where it hurts

The diagnostic's Thesis 2 held that the recurring obligation is the real long-run difference.
After consolidation:

- **Three credentials have verified renewal obligations** — CAPM (3 yrs / 15 PDUs), CSM
  (2 yrs / 20 SEUs / US$100), PRINCE2 (3 yrs / 60 CPD).
- **The two claimed to have none — Google and PSM I — are exactly the two the package does not
  address.**

So the asymmetry can be stated in one direction and not the other. **CertNorth can say these
three renew, and on what terms. It cannot say the other two never expire.** The absence of a
renewal statement in the package is not evidence that no renewal exists.

This vindicates the diagnostic's decision to demote Thesis 2 from frame to section: had the
article's spine been the obligation asymmetry, half of it would now be unusable.

---

## 6. Claim verification

### 6.1 Group A — closed decisions, unchanged

These were never verification problems. No primary source could settle them, because they are
evaluative or concern employer behaviour no available source measures. **The package does not
alter any of them.**

| # | Claim | Action |
|---|---|---|
| C1 | *"2026 figures, **verified with each provider**"* (table caption) | **REMOVE** — false as written. Highest priority |
| C2 | *"the **best** first certification is the CAPM or the Google Certificate"* (dek) | **REWRITE** |
| C3 | *"the PMP is the **gold standard**"* (dek, H3) | **REMOVE** |
| C4 | *"the **most respected credential** in the field"* | **REMOVE** |
| C5 | *"PSM I is the **cheapest real certification**"* | **REWRITE** |
| C6 | *"which **recruiters recognize**"* (CAPM) | **REMOVE** |
| C7 | *"**best recognized** entry-level credential"* (H3) | **REMOVE** |
| C8 | *"the **gentlest** on-ramp"* (Google) | **QUALIFY** |

**Note on C1.** The consolidation strengthens the case for removal rather than weakening it.
The verification that has now occurred was performed **by the Editor-in-Chief, externally, on
2026-09-04** — not by the process the caption describes, and not covering the CAPM fee or the
CSM acquisition price at all. The caption would remain false even if every figure in it were
right.

**Note on C5.** "Cheapest" rested on ~US$200 against ~US$225. **The CAPM figure is
unverified**, so the comparison has no second term and cannot be made at all. Separately, the
verified PSM I figure is **per attempt**, which is not a total. The claim is not merely
unsupported — it is now unconstructable.

### 6.2 Group B — items the package addresses

| # | Claim | Status | Action |
|---|---|---|---|
| C9 | CAPM US$225 / US$300 | **NOT VERIFIED** | **Do not use** |
| C10 | CAPM 23 contact hours | **VERIFIED** | **KEEP** |
| C10b | CAPM — no experience required | **NOT VERIFIED** | Do not state |
| C11 | CAPM renewal | **VERIFIED** — 3 yrs · 15 PDUs · ≥9 Ed · ≤6 GB · ≥2 per TT area | **KEEP** — may now be stated, with composition |
| C12 | Google US$49/month | **VERIFIED WITH CONDITIONS** | **QUALIFY** — monthly subscription, US & Canada |
| C13 | Google "under six months" | **VERIFIED WITH CONDITIONS** | **QUALIFY** — as Coursera's statement of what is possible; pair with "many complete in 3–6 months" |
| C14 | Google hours count toward CAPM's 23 | **NOT VERIFIED** | **Do not state as fact** |
| C15 | PSM I US$200 | **VERIFIED** | **KEEP** — as "per assessment attempt" |
| C15b | PSM I never expires | **NOT VERIFIED** | Do not state |
| C16 | CSM US$800–US$1,500 | **NOT VERIFIED** | **Do not use** |
| C16b | CSM two-day course mandatory | **NOT VERIFIED** | Do not state |
| C16c | CSM renewal — 2 yrs · 20 SEUs · US$100 | **VERIFIED** | **KEEP** |
| C17 | PRINCE2 name and figures | **VERIFIED WITH CONDITIONS** | **REWRITE** — official name differs from CertNorth's; US$701 is a displayed package price |

---

## 7. Evidence chain

| Claim | Source | Evidence | Status | Date | Conditions | **What the source does NOT show** |
|---|---|---|---|---|---|---|
| CAPM renewal cycle 3 years, 15 PDUs, ≥9 Education, ≤6 Giving Back, ≥2 per Talent Triangle area | PMI, via Editor-in-Chief | Package | **VERIFIED** | 2026-09-04 | none stated | How many areas the Talent Triangle has, so the minimum spread cannot be computed · whether a renewal fee applies · what renewal costs in time or money · anything about the PMP's separate rules |
| CAPM 5-year validity | — | Package states it is incorrect for the current rule | **OUTDATED** | 2026-09-04 | applies to the current rule | Whether it was ever correct historically |
| CAPM 23 education hours required; PMI's official training satisfies them | PMI, via Editor-in-Chief | Package | **VERIFIED** | 2026-09-04 | PMI's own training only | That **any other provider** qualifies — **specifically not the Google certificate** · what PMI's training costs or how long it takes · whether other routes exist |
| CAPM exam fee US$225 / US$300 | — | **none** | **NOT VERIFIED** | 2026-09-04 | — | Everything. The fee, regional variation, and the retake fee are all unknown |
| Google US$49/month | Coursera, via Editor-in-Chief | Package | **VERIFIED WITH CONDITIONS** | 2026-09-04 | **US & Canada** · monthly subscription, not a certificate price | The price in any other country · what an individual learner pays, which is pace-dependent · whether the price is stable |
| Google — most can complete for under US$300 | Coursera, via Editor-in-Chief | Package | **VERIFIED WITH CONDITIONS** | 2026-09-04 | **US & Canada** · "most learners can", not "the certificate costs" | What any individual pays · the completion rate · the total in other countries |
| Google — many complete in 3–6 months; under 6 months possible | Coursera, via Editor-in-Chief | Package | **VERIFIED WITH CONDITIONS** | 2026-09-04 | Coursera's statement | How long learners **actually** take · any completion rate · that finishing yields any outcome |
| Google — no prior knowledge required | Coursera, via Editor-in-Chief | Package | **VERIFIED WITH CONDITIONS** | 2026-09-04 | — | Whether the certificate expires · what it is accepted for |
| Google hours count toward CAPM's 23 | — | **none** | **NOT VERIFIED** | 2026-09-04 | — | Google could not show it in any case — **it is not PMI.** And confirmation would show only that the route is permitted, not that it is advisable |
| PSM I US$200 per assessment attempt · 80 questions · 60 minutes · 85% pass · password does not expire until used | Scrum.org, via Editor-in-Chief | Package | **VERIFIED** | 2026-09-04 | **per attempt**, not a guaranteed total | Whether the certification expires · the cost of preparing · whether training is required · that it is cheapest |
| CSM 2-year cycle · 20 SEUs · US$100 renewal | Scrum Alliance, via Editor-in-Chief | Package | **VERIFIED** | 2026-09-04 | renewal only | **Any acquisition cost** · whether the two-day course is mandatory · whether an exam exists · what SEUs cost to obtain |
| CSM US$800–US$1,500 to obtain | — | **none** | **NOT VERIFIED** | 2026-09-04 | — | Everything about the cost of obtaining the credential |
| PRINCE2 Project Management Foundation (Version 7) · 3-year renewal · 60 CPD points · US$701 | PeopleCert, via Editor-in-Chief | Package | **VERIFIED WITH CONDITIONS** | 2026-09-04 | US$701 is **the displayed package price on the page consulted** | What the package contains · other options or regions · prerequisites · whether training is mandatory · exam format · whether the renewal attaches to Foundation, Practitioner or both · that a combined "Foundation & Practitioner" product exists under CertNorth's published name |
| Certification is not required for the occupation (BLS) | — | repository record only; page unreachable | **NOT VERIFIED at source** | 2026-09-04 | — | **Nothing about which certification** · nothing about any individual employer · nothing about entry-level hiring. **This limit holds even if the page is reached** |
| How employers treat entry-level certifications | — | **none available** | **EVIDENCE INSUFFICIENT** | 2026-09-04 | — | No reachable source measures it. Every source that speaks to it is the issuer or a training seller |

---

## 8. Contradictions

### 8.1 Open — PRINCE2 renewal attribution

The package records **3-year renewal and 60 CPD points** under the heading naming
**PRINCE2 Project Management Foundation (Version 7)**. CertNorth's `certifications.json`
records `Practitioner every 3 years`, which implies the Foundation carries **no** renewal
obligation.

These do not agree about whether the Foundation renews. **Not resolved, and not resolved
silently.** Both are recorded; neither is chosen. This needs one clarification from PeopleCert,
and it matters because the Foundation is the beginner-relevant level.

### 8.2 Resolved — CAPM renewal cycle

**Closed in the repository's favour.** Three years, 15 PDUs, with composition limits.
The five-year figure is incorrect for the current rule.

Worth recording as method: the previous version refused to choose between the repository value
and a more widely repeated secondary figure. **The widely repeated figure was wrong.** Had
convergence been treated as evidence, the site would have replaced a correct value with an
incorrect one.

### 8.3 Resolved — Google price divergence

The $49 / $51 / $62 spread across secondary pages was never a conflict between official
sources. The package establishes **US$49/month for the US and Canada**, with prices possibly
differing elsewhere — which is consistent with a spread appearing across pages describing
different plans or regions. **No secondary figure is adopted.**

### 8.4 New — CertNorth's PRINCE2 product name

CertNorth publishes `PRINCE2 Foundation & Practitioner (7th edition)`. The verified official
name is **PRINCE2 Project Management Foundation (Version 7)**. Recorded as a discrepancy in
CertNorth's own data. **`certifications.json` is not modified in this phase.**

---

## 9. Remaining unknowns

| # | Unknown | Consequence |
|---|---|---|
| 1 | **CAPM exam fee** | No price for the credential the article recommends most often |
| 2 | **CSM acquisition cost** | Only the renewal fee is available |
| 3 | **Whether the CSM's two-day course is mandatory** | The article's stated explanation for the CSM's price is unverified |
| 4 | **Whether Google hours satisfy PMI's 23** | A recommendation in three articles loses its mechanism |
| 5 | **Whether the Google certificate expires** | Half of the obligation asymmetry |
| 6 | **Whether PSM I expires** | The other half |
| 7 | **Experience requirements for CAPM, PSM I, CSM, PRINCE2** | The "no experience required" grouping cannot be stated |
| 8 | **What the PRINCE2 US$701 package contains** | The figure cannot be described, only quoted |
| 9 | **Whether PRINCE2 Foundation itself renews** | §8.1 |
| 10 | **Number of PMI Talent Triangle areas** | The minimum PDU spread cannot be computed |
| 11 | **Regional variation** for CAPM, PSM I, CSM | Only Google's regional caveat is verified |
| 12 | **How employers treat entry-level certifications** | **EVIDENCE INSUFFICIENT — permanently, for CertNorth** |

### 9.1 On item 12

No job-posting research was performed and none is possible: no job board is reachable, and the
package does not address employer behaviour. Constructing a sample from memory or from search
results would be fabricating job postings — prohibited absolutely.

**This remains a finding rather than a gap.** The beginner's central question — *will this get
me hired?* — has no source CertNorth can reach, and every source that speaks to it is either
the issuer or someone selling training for it. The approved architecture already routes this
into a section that says so and hands the reader a check for their own market. That section is
unaffected by anything in this phase, because it never depended on data we do not have.

---

## 10. Drafting Constraints

**For the writer of the rebuild. Binding.**

### 10.1 Numbers that may be used

| Figure | How it must be described |
|---|---|
| CAPM renewal: **3 years · 15 PDUs · ≥9 Education · ≤6 Giving Back · ≥2 per Talent Triangle area** | May be stated. **State the composition, not just the total** — that is what the previous record omitted |
| CAPM: **23 hours of education required** | May be stated |
| CAPM: **PMI's official training satisfies the 23 hours** | May be stated **only about PMI's own training** |
| Google: **US$49 per month** | **"a monthly subscription of US$49 in the US and Canada."** Never "the price of the certificate", never an exam fee, never a total |
| Google: **most learners can complete for under US$300** | With the US/Canada condition, and as what most learners *can* do — not what it costs |
| Google: **many complete in 3–6 months; Coursera states under 6 months is possible** | Attributed. Both statements together, not the flattering one alone |
| Google: **no prior knowledge required** | May be stated |
| Google: **prices may differ in other countries** | **Must accompany any Google price** |
| PSM I: **US$200 per assessment attempt** · 80 questions · 60 minutes · 85% pass · password does not expire until used | **"Per attempt" is mandatory.** With an 85% pass mark, a bare "US$200" presents a floor as a price |
| CSM renewal: **2 years · 20 SEUs · US$100** | May be stated **as renewal only** |
| PRINCE2: **PRINCE2 Project Management Foundation (Version 7)** · 3-year renewal · 60 CPD points | Use the official name. Renewal attribution is unresolved (§8.1) — **do not state which level it applies to** |
| PRINCE2: **US$701** | **"the displayed price of the package shown on PeopleCert's page."** Never "the price of PRINCE2" |

### 10.2 Numbers that must NOT be used

- **CAPM US$225 / US$300** — NOT VERIFIED, explicitly not to be reused. Appears in four articles
- **CSM US$800–US$1,500** — NOT VERIFIED
- Any Google price presented as universal, as a total, or as a certificate price
- Any PSM I figure without "per attempt"
- Any PRINCE2 figure presented as universal
- Any figure for the PMP — **it leaves the comparison**
- The **five-year** CAPM validity — OUTDATED
- Any renewal fee for the CAPM — none is verified
- Any number naming the PMI Talent Triangle areas or a minimum spread — not computable

### 10.3 Statements requiring qualification

| Statement | Required qualification |
|---|---|
| Google duration | "Coursera states…" / "many learners…" — never flat |
| Google price | "monthly subscription" + "US and Canada" |
| Google → CAPM credit | **Do not state it.** If mentioned at all, attributed to the provider and marked unconfirmed |
| PSM I price | "per assessment attempt" |
| CSM figures | "to renew", never "to obtain" |
| PRINCE2 price | "the package displayed on the page consulted" |
| PMI training satisfying 23 hours | "PMI's own training" — never generalised to other providers |
| "Gentlest on-ramp" | CertNorth's assessment, not a property of the product |

### 10.4 Comparisons that are NOT valid

1. **A single price column across the five.** They are five different quantities: exam fee ·
   monthly subscription · assessment attempt · renewal fee · displayed package price. **No data
   improvement can fix this** — it is a category error, not a gap. **This is the finding the
   article is built on.**
2. **Any "cost to obtain" comparison.** Two of five have no verified acquisition figure.
3. **Cheapest / most expensive.** Requires a comparison that cannot be constructed.
4. **"Four of five require no experience."** Only Google's prerequisite is verified.
5. **"Two never expire."** Neither Google's nor PSM I's non-expiry is verified.
6. **Any recognition or employer-preference ranking.** No source exists.
7. **CAPM and PMP renewal presented as one system.** Different totals, different limits,
   verified separately.

### 10.5 Claims removed — final

**REMOVE:** "verified with each provider" · "gold standard" · "most respected credential" ·
"recruiters recognize" · "best recognized"
**REWRITE:** "the best first certification is…" · "cheapest real certification"
**QUALIFY:** "gentlest on-ramp"

### 10.6 Questions that remain unknown

The twelve in §9. Items 1–3 and 7 bear directly on what the article can say; item 12 is
permanent and is handled by an approved section rather than by data.

### 10.7 The editorial rule that governs all of the above

> **"Not the same kind of thing" must not become "therefore this is the best one."**

Nothing in this phase produces a ranking, and the verified data makes ranking **less**
constructible than before, not more: the two comparisons a ranking would need — acquisition
cost and recognition — are precisely the two that remain unavailable.

The article must help a beginner choose by **objective, career stage and type of investment**.
It must not order these credentials.

---

## 11. Source register

### 11.1 Primary sources — verified externally by the Editor-in-Chief

| Organisation | Covers | Items | Date supplied |
|---|---|---|---|
| **PMI** | CAPM maintenance; CAPM education requirement | 2, 9 | 2026-09-04 |
| **Coursera** | Google certificate price, duration, prerequisites | 3, 5 | 2026-09-04 |
| **Scrum.org** | PSM I fee, format, pass mark, password validity | 6 | 2026-09-04 |
| **Scrum Alliance** | CSM renewal cycle, SEUs, renewal fee | 7 (part) | 2026-09-04 |
| **PeopleCert** | PRINCE2 official name, renewal, CPD, displayed price | 8 | 2026-09-04 |

**Two limitations of the package, recorded for the audit trail and not as criticism:**

1. **No per-item URLs.** Sources are identified by organisation and, for PRINCE2, by "the page
   consulted". A future re-check will need to locate the pages again.
2. **No per-item consultation dates.** All entries are dated to the day the package was
   supplied. `CLAUDE.md` requires date sensitivity for prices and rules; without a consultation
   date per figure, drift cannot be measured against a known baseline.

Neither affects any classification above. Both are worth capturing at source next time.

### 11.2 Attempted by this session — all blocked

`pmi.org` · `coursera.org` · `grow.google` · `scrum.org` · `scrumalliance.org` ·
`peoplecert.org` · `bls.gov` — all **403 CONNECT tunnel failed**, as were the control hosts
`example.com` and `en.wikipedia.org`. **Primary sources reached by this session: 0.**
**No web access was attempted in this phase.**

### 11.3 Secondary material

None used. The three searches from the research phase are recorded in the research dossier
§18.2. They surfaced the CAPM contradiction and the Google price divergence, both of which the
package has now settled. **No secondary figure was adopted at any point, and the CAPM outcome
shows why: the widely repeated figure was the wrong one.**

### 11.4 Repository sources

`platform/content/certifications.json` ·
`platform/content/articles/best-pm-certifications-beginners.json` · `is-capm-worth-it` ·
`capm-vs-google-pm-certificate` · `google-pm-certificate-worth-it` · `pmp-vs-capm` ·
`best-agile-certifications` · the Rebuild 03 dossier and diagnostic ·
`editorial-os/reports/PMP_GLOBAL_PRICE_CORRECTION_REPORT.md` · `CLAUDE.md`

### 11.5 CertNorth data discrepancies recorded — **no file modified**

| File · field | Published | Verified | Status |
|---|---|---|---|
| `certifications.json` · `capm.renewal` | 15 PDUs every 3 years | 3 yrs · 15 PDUs · ≥9 Ed · ≤6 GB · ≥2 per TT area | Correct, **incomplete** |
| `certifications.json` · `csm.renewal` | Every 2 years (SEUs + fee) | 2 yrs · 20 SEUs · US$100 | Correct, **unquantified** |
| `certifications.json` · `prince2.fullName` | PRINCE2 Foundation & Practitioner (7th edition) | PRINCE2 Project Management Foundation (Version 7) | **Does not match** |
| `certifications.json` · `prince2.renewal` | Practitioner every 3 years | 3 yrs · 60 CPD, level unresolved | **§8.1** |
| `certifications.json` · `capm.examCost` | $225 / $300 | — | **NOT VERIFIED** |
| `certifications.json` · `csm.examCost` | ~$800–$1,500 all-in | — | **NOT VERIFIED** |
| `certifications.json` · `psm.renewal` | None — never expires | — | **NOT VERIFIED** |
| `certifications.json` · `google-pm.renewal` | None — does not expire | — | **NOT VERIFIED** |

**Recorded only. `certifications.json` was not modified**, per this phase's instructions.
These require a separate decision from the Editor-in-Chief.

### 11.6 No ranking produced

Nothing in this file orders these credentials. §3.2's finding is a **classification** — five
different kinds of quantity — not an ordering, and no price, difficulty, format or renewal
difference has been converted into a verdict.

---

**Production untouched.** `platform/content/articles/best-pm-certifications-beginners.json`
read, not modified. `certifications.json` not modified. No other article modified. No
`platform/src/*` modified. No infrastructure. Nothing drafted, published, merged or deployed.
One file changed: this one.
