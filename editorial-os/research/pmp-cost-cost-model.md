# Cost Model — `pmp-cost`

**Built:** 2026-09-04
**Input:** `pmp-cost-research-dossier.md`
**Status:** model design. No figure below is verified at source — see §6.

---

## 0. The rule this model follows

Every amount in this document is **secondary-sourced and unverified**. The model is
therefore built to survive being wrong about any individual number: it classifies costs
by *behaviour* (mandatory, conditional, optional, recurring, candidate-dependent) rather
than resting on a total. A reader whose local price differs can still use the structure.

Any figure that reaches the published article must be labelled with its confidence, and
any calculation must be labelled **CERTNORTH CALCULATION** — never "PMI says".

---

## 1. Cost taxonomy

### A. REQUIRED — you cannot obtain the PMP without paying these

| Cost | Trigger | Amount (unverified) | Recurring | Varies by geography | PMI publishes a fixed amount? |
|---|---|---|---|---|---|
| PMP exam fee | Sitting the exam | **$445 member / $675 non-member** (reported effective 2026-08-06) | No — once per attempt | **Disputed.** Sources contradict each other; an India figure of ₹24,708 (~$281) is inconsistent with a straight USD conversion | Yes, but possibly per-region |
| 35 contact hours of project management education | Application | **Not establishable.** CertNorth currently says $0–$600; unsourced | No | Yes — training markets differ sharply by country | No — third-party pricing |

**Note on the second row:** this is required, but the *amount* is candidate-dependent and
can be near zero today. See §3 — that may change in late 2026.

### B. CONDITIONAL — required only if something happens

| Cost | Trigger | Amount (unverified) | Recurring | Notes |
|---|---|---|---|---|
| Retake fee | Failing an attempt | **$275 member / $375 non-member**, per additional attempt | Up to 2 additional attempts within the 1-year eligibility period | **Lower than a full exam fee** — the current CertNorth article implies otherwise |
| New application after 3 failures | Failing all three attempts | Full exam fee again, after a **1-year wait** | — | The real exposure here is time, not money |
| Higher non-member renewal fee | Letting membership lapse before renewal | $150 instead of $60 | Every 3 years | Often still cheaper than a year of membership — already covered in `is-pmi-membership-worth-it` |

### C. OPTIONAL — genuinely avoidable

| Cost | Trigger | Amount | Notes |
|---|---|---|---|
| PMI membership | Choosing to join | **$129–$159/yr** depending on source, **+ ~$10 one-time application fee** | Optional. Never required. See §2 for whether it pays |
| Prep course beyond the 35 hours | Choosing to buy | No defensible figure | **Do not publish an average.** Every source quoting one is selling one |
| Exam simulators, question banks, books | Choosing to buy | No defensible figure | Same |
| Purchased PDU bundles | Choosing to buy | Several hundred per cycle | Largely avoidable — `pmp-renewal-pdus` documents the free routes |

### D. RECURRING — the cost of keeping it, not getting it

| Cost | Frequency | Amount (unverified) | Avoidable? |
|---|---|---|---|
| Certification renewal fee | Every 3 years | **$60 member / $150 non-member** | No |
| 60 PDUs | Every 3 years | **$0 financially achievable** — but see §4 | The money, yes. The time, no |
| PMI membership, if maintained | Annual | $129–$159 | Yes — and after certification the renewal discount does not justify it |

### E. CANDIDATE-DEPENDENT — the variables that actually move the number

| Variable | Range of effect |
|---|---|
| Member or non-member at the moment of booking | ~$230 on the exam fee alone |
| Country / PMI account region | Potentially very large, and unquantifiable from here |
| Whether an active CAPM already covers the 35 hours | Removes a required cost entirely |
| Whether the employer pays | Removes most of it |
| Number of attempts | $275–$375 per additional attempt |
| Whether PDUs are earned or bought | $0 vs several hundred per cycle |
| How many renewal cycles you keep it for | The dominant factor over 10 years |

---

## 2. CERTNORTH CALCULATION — membership break-even, done twice

The industry states this once, in the direction that favours joining. It has two
directions and they point opposite ways.

### 2.1 At exam time — membership wins

```
Non-member route:  exam $675                                    = $675
Member route:      membership ~$149 + $10 application + exam $445 = $604
                                                        Difference = $71 in favour of joining
```

**CERTNORTH CALCULATION.** Assumptions stated: member exam $445, non-member exam $675,
membership $149/yr, one-time application fee $10, single attempt, US pricing, figures
reported effective 2026-08-06 and **not verified at source**.

**Sensitivity — this is why the assumption matters:**

| If membership is… | Net benefit of joining |
|---|---|
| $129 | **+$91** |
| $149 | **+$71** |
| $159 | **+$61** |

Joining wins under every membership figure found, but by **$61–$91, not the ~$100 the
current CertNorth article implies**. The site's current text says "a saving of about
$250 against a membership of about $150, so joining first leaves you around $100 better
off" — that rests on a $250 gap. The reported post-August gap is **$230**.

### 2.2 At renewal time — membership loses

```
Membership over one 3-year cycle:   ~$149 × 3        = ~$447
Renewal discount over that cycle:   $150 − $60       =   $90
                                              Net    = −$357
```

**CERTNORTH CALCULATION.** The renewal discount does **not** pay for membership. It
recovers about a fifth of it.

This directly contradicts a claim repeated across vendor pages ("non-members pay $90
more to renew, so membership pays for itself"). CertNorth's `is-pmi-membership-worth-it`
already makes this argument and is correct; the rebuilt `pmp-cost` should reference it
rather than restate it.

**Break-even statement, honest form:** join before the exam; after that, keep membership
only for things you will actually use, never on the renewal arithmetic.

---

## 3. The education cost, and the change that could break this model

The 35 contact hours are **required**, but today the amount is close to
candidate-dependent: self-paced options exist at low cost, and an active CAPM covers the
requirement outright.

**From late Q4 2026 that may stop being true.** PMI is reported to be restricting how the
35 hours may be delivered — to Authorized Training Partners, GAC-accredited academic
programmes, or the CAPM waiver. **Sources disagree on whether this covers all 35 hours or
only live instructor-led training.**

| If the restriction covers… | Effect on the budget |
|---|---|
| Live instructor-led training only | Self-paced on-demand still qualifies. The current low-cost floor survives |
| All 35 contact hours | The cheap route disappears. The education floor rises to ATP pricing, which is set by commercial providers |

**This is the single largest unresolved variable in a 2026 PMP budget, and no source
found states the scope unambiguously.** The model cannot resolve it. The article must
present it as an open question with both consequences, and tell the reader to confirm
before buying training.

---

## 4. PDUs — financial cost and time commitment, kept separate

The prompt is right that converting 60 PDUs into money would be arbitrary. This model
therefore never assigns an hourly rate. It reports two independent quantities.

### Financial cost of 60 PDUs

**Can be $0.** `pmp-renewal-pdus` documents the free routes: free webinars, chapter
events, qualifying self-directed learning, mentoring, teaching, volunteering, and working
in the certified role.

### Time commitment of 60 PDUs

**60 hours over three years — about 20 hours a year, roughly two hours a month.**

### The qualification the current site article misses

One PDU generally represents one hour. But the 60 are not interchangeable:

- **At least 35 must come from Education** (reported; unverified).
- **Working in your certified role is *Giving Back*, not Education** — and Giving Back is
  capped.

So "your job covers your PDUs" is **wrong**. Working in the role can contribute at most
the Giving Back allowance; the remaining 35+ require deliberate learning activity. That
activity can still be free, so the *financial* conclusion is unchanged — but the *time*
conclusion is not, and CertNorth's own renewal article currently leads its free-routes
list with the role-based option.

**This distinction is original analysis and belongs in the rebuilt article**, with a link
to `pmp-renewal-pdus` for the mechanics.

---

## 5. Which costs are fixed, variable, and candidate-dependent

| Behaviour | Costs |
|---|---|
| **Fixed by PMI** (but possibly per-region, and revised 2026-08-06) | Exam fee, retake fee, renewal fee, membership fee |
| **Variable, set by third parties** | 35 contact hours, prep materials, PDU bundles |
| **Determined by the candidate** | Membership yes/no, number of attempts, buy vs earn PDUs, how many cycles to maintain, whether an employer pays |
| **Not a money cost at all** | Study time, PDU time, eligibility time |

---

## 6. What this model must not be used to claim

- **Not** a single global "the PMP costs $X". Regional pricing is disputed and
  unresolved.
- **Not** an expected cost weighted by pass probability. No reliable pass rate exists —
  `pmp-pass-rate` establishes this.
- **Not** a "typical candidate" scenario. Every scenario must be labelled with its
  assumptions and presented as one path, not as the average.
- **Not** an average training cost. No neutral data exists.
- **Not** a monetised value of study time.
- **Not** a claim that any figure here is confirmed. Nothing was verified at source.
