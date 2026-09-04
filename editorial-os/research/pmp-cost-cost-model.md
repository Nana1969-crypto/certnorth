# Cost Model — `pmp-cost`

**Built:** 2026-09-04
**Revised:** 2026-09-04 — rebuilt on repository inputs only (see §0)
**Inputs:** `pmp-cost-internal-claims-map.md`, `pmp-cost-research-dossier.md`

---

## 0. Revision note

An earlier version of this model used figures obtained from web search as inputs. **It has
been rebuilt.** Search-discovered values are now excluded from the model entirely.

**Every input below is a value the CertNorth repository already publishes.** That gives it
one property and only one: **VERIFIED FROM CERTNORTH REPOSITORY** — we know this is what
the site claims. It does **not** mean the input is correct. Every one of them is also
**PRIMARY SOURCE VERIFICATION REQUIRED**.

The model is therefore built as a **structure with substitutable inputs**, not as a set of
answers. If PMI's real figures differ, the arithmetic is re-run; the taxonomy, the
break-even logic and the ten-year shape survive unchanged.

---

## 1. Model inputs

| Input | Value | Label | Notes |
|---|---|---|---|
| Exam, member | **~$425** | REPOSITORY (5 locations agree) | PRIMARY VERIFICATION REQUIRED |
| Exam, non-member | **~$675** | REPOSITORY (5 locations agree) | PRIMARY VERIFICATION REQUIRED |
| Membership, annual | **$140–$150** | REPOSITORY — **the site contradicts itself**; the range *is* the contradiction | PRIMARY VERIFICATION REQUIRED |
| Membership application fee | *"a small one-time fee"* | REPOSITORY — **never quantified anywhere on the site** | Excluded from totals; noted as an unpriced addition |
| Renewal, member | **$60** per 3 years | REPOSITORY (3 locations) | PRIMARY VERIFICATION REQUIRED |
| Renewal, non-member | **$150** per 3 years | REPOSITORY (3 locations) | PRIMARY VERIFICATION REQUIRED |
| PDU requirement | **60 per 3 years**, ≥8 per Talent Triangle area | REPOSITORY | PRIMARY VERIFICATION REQUIRED |
| 35 contact hours | Required | REPOSITORY (7 locations) | PRIMARY VERIFICATION REQUIRED |
| Cost of the 35 contact hours | **Not modelled** | — | No neutral data exists. See §4 |
| Retake fee | **Not modelled** | — | See §5 — the site's only claim is unsourced |

---

## 2. Cost taxonomy

Independent of any price. This survives every input being wrong.

### A. REQUIRED — cannot obtain the PMP without paying

| Cost | Trigger | Recurring | Varies by geography | Does the issuing body set it? |
|---|---|---|---|---|
| Exam fee | Sitting the exam | Once per attempt | **Unresolved** — see dossier Q5 | Yes |
| 35 contact hours of education | Application | No | Yes — training markets differ by country | **No** — third-party pricing |

### B. CONDITIONAL — required only if something happens

| Cost | Trigger | Status |
|---|---|---|
| Retake fee | Failing an attempt | **Amount and mechanism unverified.** See §5 |
| Higher non-member renewal fee | Membership lapsed at renewal | $150 instead of $60 — REPOSITORY |

### C. OPTIONAL — genuinely avoidable

| Cost | Notes |
|---|---|
| PMI membership | **Never required.** Consistent across the repository |
| Prep courses beyond the 35 hours | Not priceable — see §4 |
| Simulators, question banks, books | Not priceable |
| Purchased PDU bundles | `pmp-renewal-pdus` documents free alternatives |

### D. RECURRING — the cost of keeping it

| Cost | Frequency | Avoidable? |
|---|---|---|
| Renewal fee | Every 3 years | No |
| 60 PDUs | Every 3 years | The money largely yes; the **time** no — see §6 |
| Membership, if maintained | Annual | Yes |

### E. CANDIDATE-DEPENDENT — what actually moves the number

| Variable | Effect |
|---|---|
| Country of the PMI account | **Potentially large, unquantifiable from here** |
| Member or non-member when booking | ~$250 on the exam, using repository figures |
| Active CAPM already held | Removes a required cost entirely (REPOSITORY: `pmp-eligibility`) |
| Employer pays | Removes most of it |
| Number of attempts | Unquantified — see §5 |
| PDUs earned vs bought | $0 vs several hundred per cycle (REPOSITORY) |
| **Number of renewal cycles maintained** | **The dominant factor over 10 years** — see §3 |

---

## 3. CERTNORTH CALCULATION — cost of ownership

**All inputs are repository values requiring primary verification.** Assumptions stated in
full; substitute your own and re-run.

**Assumptions:** exam at member rate $425; membership $140–$150/yr (range = the site's
internal contradiction); renewal $60 member / $150 non-member every 3 years; PDUs earned at
no cost; the 35 contact hours obtained at no cost; **no** prep materials purchased; **no**
retake; membership application fee **excluded** because the site never quantifies it;
3 renewal events fall within 10 years, 1 within 5.

### Scenario A — join for the exam year, then let membership lapse

| Item | 5-year | 10-year |
|---|---|---|
| Membership, year 1 | $140–$150 | $140–$150 |
| Exam, member rate | $425 | $425 |
| 35 contact hours | not modelled | not modelled |
| Renewals at non-member rate | 1 × $150 | 3 × $150 = $450 |
| **Total** | **$715–$725** | **$1,015–$1,025** |

### Scenario B — maintain membership throughout

| Item | 5-year | 10-year |
|---|---|---|
| Membership | 5 × $140–150 = $700–$750 | 10 × $140–150 = $1,400–$1,500 |
| Exam, member rate | $425 | $425 |
| Renewals at member rate | 1 × $60 | 3 × $60 = $180 |
| **Total** | **$1,185–$1,235** | **$2,005–$2,105** |

### The result

**CERTNORTH CALCULATION.** Over ten years, maintaining PMI membership costs approximately
**$990–$1,080 more** than letting it lapse, while saving **$270** in renewal fees.

**EDITORIAL INFERENCE:** membership after certification should be judged on what you
actually use — the library, the webinars, a local chapter — never on the renewal discount,
which recovers roughly a quarter of its own cost. `is-pmi-membership-worth-it` already
reaches this conclusion; this model quantifies it over a decade.

### Scenario C — with a retake

**Not modelled.** See §5.

### Scenario D — with paid training

**Not modelled.** See §4.

### What these scenarios may never be called

Not "typical". Not "average". Not "what most people pay". They are **two explicitly assumed
paths built from figures the site itself has not verified**, published so a reader can
substitute their own.

---

## 4. Why training is not modelled

The 35 contact hours are **required**, but no defensible price exists for them.

- No source cited anywhere in the repository publishes third-party training prices —
  PMI does not sell training.
- Every external source that quotes an average is selling the thing it prices.
- The site currently publishes two mutually inconsistent all-in ranges
  (**$700–$2,500** in `pmp-cost`; **$1,000–$3,000** in `how-to-become-project-manager`),
  neither traceable to a cited source.

**The model excludes training and says so.** The article should instruct the reader to
insert their own quote.

**One forward-looking note, EDITORIAL INFERENCE:** `pmp-eligibility` documents a
late-Q4-2026 restriction on how the 35 hours may be delivered. If that restriction turns
out to cover more than live instructor-led training, the cheapest routes disappear and the
education floor rises. **The scope is unresolved** (dossier Q8) and the model takes no
position on it.

---

## 5. Why retakes are not modelled

Two independent reasons, and either alone would be sufficient.

**First — the fee is unknown.** The site's only statement is `pmp-cost` `body[8]`: *"a
retake adds another exam fee."* It is **unsourced**; the article does not cite the PMP
Handbook, which is where retake policy would live. Search raised a question about a
possible reduced fee (dossier Q6), but that is **SECONDARY/SEARCH DISCOVERY ONLY** and is
not adopted here. **We therefore do not know what a retake costs, and we may not assert
either version.**

**Second — the probability is unknowable, permanently.** `pmp-pass-rate` establishes that
PMI has not published a pass rate for roughly two decades and that the circulating "61%" is
a retired passing score. **No expected-cost calculation weighted by pass probability may be
built.**

**What the article can do instead:** state that a failed attempt has a cost, that we could
not verify what it is, and that any page presenting a probability-weighted expected cost is
using a number that does not exist. **That refusal, explained, is worth more than a
fabricated scenario.**

---

## 6. PDUs — financial cost and time commitment, held apart

The model never assigns an hourly monetary value to study or PDU time. Doing so would
require inventing a rate for the reader.

### Financial cost of 60 PDUs

**Can approach $0.** `pmp-renewal-pdus` documents free routes: webinars, chapter events,
qualifying self-directed learning, mentoring, teaching, volunteering.
**Label: VERIFIED FROM CERTNORTH REPOSITORY.**

### Time commitment of 60 PDUs

**60 hours over three years — about 20 hours a year, roughly two hours a month.**
**Label: CERTNORTH CALCULATION**, on the repository's stated basis that one PDU generally
represents one hour.

### The qualification our own article obscures

`pmp-renewal-pdus` leads its dek with earning PDUs *"including by doing your own job"*,
while its body states that working in the certified role is **Giving Back**, that Giving
Back is **capped**, and that the article does not say by how much.

**Label: EDITORIAL INFERENCE** — "your job covers your PDUs" is not supported by our own
article's body. **The cap value is PRIMARY SOURCE VERIFICATION REQUIRED** (CCR Handbook,
which `pmp-renewal-pdus` cites but from which no number was transcribed).

**Consequence:** the rebuilt `pmp-cost` may say PDUs can be earned without paying. It may
**not** say that working in the role covers them.

---

## 7. What this model must not be used to claim

- **Not** a single global "the PMP costs $X" — regional pricing is unresolved (Q5)
- **Not** a pass-rate-weighted expected cost — no such rate exists
- **Not** a retake scenario — the fee is unverified and the site's own claim is unsourced
- **Not** an average or typical training cost — no neutral data exists
- **Not** a monetary value for study time
- **Not** that any input here is confirmed — none is
- **Not** that the search-discovered figures are more current than the repository's. They
  are questions, not corrections
