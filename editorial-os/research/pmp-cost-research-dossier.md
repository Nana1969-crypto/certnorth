# Research Dossier — `pmp-cost`

**Article:** `pmp-cost` · `/certifications/guides/pmp-certification-cost/`
**Researched:** 2026-09-04
**Live article modified:** none
**Researcher note:** this dossier records what could and could not be verified. Its most
important section is §4.

---

## 1. The blocking constraint, stated first

**PMI's website could not be reached.** The environment's egress proxy blocks all
outbound HTTP requests, including `pmi.org`:

```
WebFetch https://www.pmi.org/certifications/project-management-pmp
→ EGRESS_BLOCKED: Access to www.pmi.org is blocked by the network egress proxy.
```

The same block applies to every other external domain tested. The only external channel
available is web search, which returns **summaries of third-party pages**, not the pages
themselves and never the primary source.

### What that means under CertNorth's own source hierarchy

`editorial-os/config/source-hierarchy.yaml` ranks sources 1–10. PMI is **tier 2**
(official certification organisation). Every external source obtained for this dossier
is **tier 10** (secondary) *and* is a **training provider or exam-prep vendor** — the
exact category the hierarchy says must never be cited as neutral evidence about its own
product.

Sources encountered, all commercial training or prep vendors: StormWind Studios, PMTI
(4pmti.com), Simpliaxis, BePM Academy, Boost eLearning, PrepSolution, TechCertGuide,
ExamCert, PM Study Circle, Master of Project, ShriLearning, iCert Global, Gururo,
Woloyem, 3Fold Training, StarAgile, Invensis Learning, Kavita Sharma, CertScope,
Projeric, PMP Journey, Certsqill, Study.com, Learning Mudra, PrepSaret,
The Career Accelerators, IMT-PM, Spoclearn, EduHubSpot, PM Exam Study.

**No figure in section 3 has been verified at source.** Confidence levels are assigned
accordingly and none rises above MEDIUM.

---

## 2. What CertNorth already owns (Phase 1) — HIGH confidence

These are internal, inspectable facts. They are the strongest material available, and
most of what the rebuilt article needs already exists on the site.

| Fact | Owning article | Notes |
|---|---|---|
| 60 PDUs per 3-year cycle; renewal fee $60 member / $150 non-member; minimum 8 PDUs in each of the three Talent Triangle areas | `pmp-renewal-pdus` | Also documents free PDU routes and warns that category caps exist and change |
| **The PMP pass rate is unknowable.** PMI has not published it for ~20 years. The circulating "61%" is a *passing score* retired around 2006, not a pass rate | `pmp-pass-rate` | **Decisive for Phase 6** — see §5 |
| PMI now scores psychometrically and reports performance bands, not a percentage | `pmp-pass-rate` | |
| Eligibility: 36 months experience with a four-year degree, or 60 months with a secondary diploma, plus 35 contact hours; qualifying experience may come from the last 10 years | `pmp-eligibility` | |
| An active CAPM can cover the 35-contact-hour requirement | `pmp-eligibility`, `pmp-vs-capm` | A real cost lever |
| **PMI rule change from late Q4 2026** on how the 35 hours may be delivered | `pmp-eligibility` | See §3.7 — scope is disputed |
| Membership exam discount pays for itself once; **the renewal discount does not** — ~$90 saved per cycle against ~$450 of membership over the same period | `is-pmi-membership-worth-it` | CertNorth is right and the vendor pages are wrong; see §6 |
| Exam updated 9 July 2026: People 33% / Process 41% / Business Environment 26%; ~60% agile and hybrid; 180 questions in 240 min, 10 unscored | `how-to-prepare-for-pmp-exam` | Business Environment more than tripled |
| Most working professionals need ~2–3 months of part-time study once eligible | `how-to-prepare-for-pmp-exam` | Time, not money |

### `certifications.json` — the single source of truth

```
id: pmp
examCost:  "~$425 member / ~$675 non-member (verify for your country)"
training:  "35 contact hours required"
renewal:   "60 PDUs every 3 years + $60/$150 fee"
verifiedOn: 2026-07
source:     https://www.pmi.org/certifications/project-management-pmp
```

This record feeds the `certTable` in `best-pm-certifications-beginners`. **If the August
2026 increase is real, this one file is stale and the error propagates to another page.**

---

## 3. External research (Phase 2) — LOW to MEDIUM confidence, secondary only

Format: claim · best available source type · date researched · explicit or inferred ·
confidence.

### 3.1 Exam fee — the contested number

| Figure | Reported as | Appears in |
|---|---|---|
| $405 member / $555 non-member | pre-August-2026 | several vendor pages |
| **$445 member / $675 non-member** | effective **2026-08-06** | multiple independent vendor pages, converging |
| $405 member / $655 non-member | "usually around" | one vendor page |
| ~$425 member / ~$675 non-member | current CertNorth figure | `certifications.json`, `verifiedOn: 2026-07` |

**Convergent claim:** PMI implemented a global fee increase effective **6 August 2026**,
raising the member fee from $405 to **$445** and the non-member fee from $555 to
**$675**. Several unrelated vendors state this independently and consistently.

**Confidence: MEDIUM.** Convergence across many unaffiliated commercial sources is
meaningful evidence, but every one of them has a commercial interest in PMP pricing
content and none is PMI. Explicit, not inferred.

**Consequence for CertNorth:** the site's current member figure (~$425) matches neither
the old price ($405) nor the reported new price ($445). It appears to be an
approximation that was never anchored to either. The non-member figure ($675) matches
the reported *new* price. **The site is currently carrying a mixed pair.**

**This is the number the previous audit flagged as failing the site's own standard. It
still fails it. It is now also probably wrong.**

### 3.2 PMI membership

| Figure | Source position |
|---|---|
| $129/yr | one vendor |
| $139/yr | one vendor |
| $149/yr renewal rate | one vendor |
| $154/yr for new members | one vendor |
| $139–$159/yr | one vendor's range |
| **+ ~$10 one-time application fee** | consistent across sources |

**Confidence: LOW.** Sources disagree by ~20%. The $10 application fee is the most
consistent element. Membership is **optional**, never required — no source disputes this.

**Internal contradiction found:** `pmp-cost` states membership is "about $140 a year";
`is-pmi-membership-worth-it` states "roughly $150 a year". **Two CertNorth pages give
different numbers for the same fee.** Neither is sourced to PMI.

### 3.3 Renewal

| Claim | Confidence |
|---|---|
| Renewal fee $60 member / $150 non-member, every 3 years | **MEDIUM** — the most consistent external figure found, and it matches what CertNorth already publishes |
| 60 PDUs per 3-year cycle | **MEDIUM–HIGH** — universally agreed |
| **Minimum 35 of the 60 PDUs must come from Education** | **LOW–MEDIUM** — stated by one source; consistent with the widely-described 35-Education-minimum / 25-Giving-Back-maximum structure, but not verified |

**The 35-PDU Education floor matters analytically.** CertNorth's `pmp-renewal-pdus`
says category caps exist without giving the numbers, and its list of free routes leads
with "working in your certified role", which is a *Giving Back* activity. If Giving Back
is capped at 25, then **working in the role cannot cover more than 25 of the 60 PDUs**,
and at least 35 must come from deliberate learning activity. That does not make renewal
expensive — free Education PDUs exist — but it does mean "your job covers it" is wrong.

### 3.4 Retake — a likely error in the current article

| Claim | Confidence |
|---|---|
| Eligibility period is 1 year, allowing up to **3 exam attempts** | MEDIUM |
| Retake fee **$275 member / $375 non-member**, per additional attempt | **LOW–MEDIUM** — consistently reported, but the figures may predate the August 2026 increase |
| 30-day waiting period between attempts | LOW–MEDIUM |
| After 3 failed attempts: wait **1 year** from the last attempt, then a new application | LOW–MEDIUM |

**The current CertNorth article says:** *"pass on the first try — a retake adds another
exam fee."* If the reduced retake fee is real, **CertNorth is currently overstating
retake cost by roughly $170**, and misdescribing the mechanism. The bigger exposure is
not money but the **1-year lockout** after three failures — which the article does not
mention at all.

### 3.5 Regional pricing — a direct contradiction

Two search results, from different vendors, state opposite things:

> "In countries like India, Brazil, and parts of the Asia-Pacific region, fees are
> adjusted to align with local purchasing power."

> "PMI exam fees are globally fixed in USD; local training costs fluctuate."

A third gives an India-specific figure presented as the price shown at PMI checkout for
Indian members: **₹24,708**. At roughly ₹88/USD that is about **$281** — far below $445.
If that figure is accurate, it is evidence *for* regional pricing and *against* a fixed
global USD fee.

**Confidence: LOW on any specific number. MEDIUM–HIGH that a universal global price
cannot be responsibly stated**, because the sources contradict each other and at least
one country figure is inconsistent with a straight USD conversion.

**This is the finding that should shape the article.** See §7.

### 3.6 Training / 35 contact hours

No defensible market-average price could be established. Vendor pages quote wide ranges,
and every page quoting a price is selling the thing it prices. CertNorth's current
"$0–$600 depending on provider" is a reasonable range but is not sourced.

**Do not publish an "average preparation cost".** The prompt forbids it and the evidence
would not support it anyway.

### 3.7 The ATP rule — scope disputed, and it is a cost question

| Version | Source position |
|---|---|
| From late Q4 2026, PMI will accept the 35 contact hours **only** from a PMI Authorized Training Partner, a GAC-accredited academic programme, or an active CAPM waiver | one vendor, stated broadly |
| The restriction applies to **live instructor-led training** (virtual or in person) delivered by unauthorised institutes, trainers, consultants or bootcamps | another vendor, and CertNorth's own `pmp-eligibility` |

**These are materially different rules.** If *all* 35 hours must come from an ATP, the
cheap self-paced route disappears and the education floor rises to ATP pricing. If only
*live* training is restricted, on-demand self-study still qualifies and the floor holds.

**Confidence: MEDIUM that the change is happening. LOW on its scope.**

**This is the largest live variable in a 2026 PMP budget**, and no page found states the
scope unambiguously.

---

## 4. What could NOT be verified

Stated plainly, because this determines what the article may claim.

| Item | Status |
|---|---|
| Current PMP exam fee at PMI | **UNVERIFIED at source.** Best evidence: $445/$675 from 2026-08-06, secondary only |
| PMI membership fee | **UNVERIFIED.** Sources disagree ($129–$159) |
| Whether PMI prices the exam regionally | **UNVERIFIED — sources actively contradict each other** |
| Retake fee | **UNVERIFIED.** $275/$375 reported; may predate the August increase |
| Whether 35 of 60 PDUs must be Education | **UNVERIFIED.** Plausible and consistent, not confirmed |
| Scope of the late-2026 ATP requirement | **UNVERIFIED — the central open question** |
| Any "average" or "typical" training cost | **Not establishable.** No neutral data exists |
| PMP pass rate | **Unknowable.** PMI does not publish it — already established in `pmp-pass-rate` |

---

## 5. Consequence for Phase 6 (retake risk)

The prompt says: *"Do not create a probabilistic expected cost unless the necessary
probability data is sufficiently reliable."*

**It is not, and CertNorth has already published why.** `pmp-pass-rate` establishes that
no reliable pass-rate figure exists anywhere. Therefore:

- No expected-value calculation. Not "if the pass rate is 60%, expected cost is…".
- **Scenario analysis only**, with the number of attempts as an explicit assumption
  chosen by the reader, never a probability supplied by CertNorth.
- The article should say *why* it refuses to compute an expected cost, and link
  `pmp-pass-rate`. That refusal is itself original value: every competitor page that
  quotes a pass rate is quoting a retired passing score.

---

## 6. A claim CertNorth can correct

Multiple vendor pages assert some version of:

> "Non-members pay $90 more just to renew, so PMI membership often pays for itself."

CertNorth's `is-pmi-membership-worth-it` already demonstrates this is false: ~$90 saved
once per three-year cycle against ~$450 of membership across the same period is a losing
trade. **The renewal discount does not pay for membership.** The exam discount does — but
only once.

This is a correction of a claim widely repeated by the industry, backed by arithmetic the
reader can check. It qualifies as original value under the rule in `CLAUDE.md`:
*"correcting a claim everyone repeats."*

---

## 7. Research conclusion

The research did not produce a reliable price. **That is the finding, not a failure of
the research.**

Three independent facts point the same way:

1. The headline fee apparently changed on 2026-08-06 and CertNorth's figure matches
   neither the old nor the new number.
2. Sources contradict each other on whether a universal USD price even exists.
3. Every source available is a vendor with an interest in the answer.

A page that responds by stating a confident number would be doing exactly what the audit
criticised. A page that gives the reader a method, a taxonomy of costs, two honest
calculations and a clear account of what nobody can currently confirm is doing something
no PMI page and no vendor page does.

**Assessment: the research is sufficient to proceed to structure design and drafting,
provided the article is built around cost structure and uncertainty rather than around a
headline price.** It is *not* sufficient to publish any specific fee as verified fact.

---

## 8. Re-verification requirement

Every figure in §3 must be re-checked against PMI directly before publication, by a human
with browser access, or published with an explicit unverified label. See
`pmp-cost-fact-check-plan.md`.
