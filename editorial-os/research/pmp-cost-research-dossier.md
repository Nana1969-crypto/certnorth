# Research Dossier — `pmp-cost`

**Article:** `pmp-cost` · `/certifications/guides/pmp-certification-cost/`
**Researched:** 2026-09-04
**Revised:** 2026-09-04 — verification protocol corrected (see §0)
**Live article modified:** none

---

## 0. Protocol correction

An earlier version of this dossier assigned **MEDIUM confidence** to the exam fee on the
grounds that several unaffiliated vendor pages agreed with each other. **That was wrong
and has been removed.**

Repetition is not verification. A figure copied between commercial sites is one claim
appearing many times, not many independent confirmations — and when the sites concerned
all sell PMP training, agreement between them is weak evidence about PMI's prices and no
evidence at all about which figure is current.

The revised protocol, applied throughout:

| Label | Meaning | May be published as fact? |
|---|---|---|
| **VERIFIED FROM CERTNORTH REPOSITORY** | The repository demonstrably contains this. Says nothing about whether it is *true* | Only as "what CertNorth currently states" |
| **PRIMARY SOURCE VERIFICATION REQUIRED** | Settleable only at the issuing body. Not settled here | **No** |
| **SECONDARY/SEARCH DISCOVERY ONLY** | Found via search. A lead — a question to ask PMI | **No.** Never, regardless of how many sources repeat it |
| **CERTNORTH CALCULATION** | Our arithmetic from stated inputs. Valid only if the inputs are | Only with inputs and their labels attached |
| **EDITORIAL INFERENCE** | A judgement drawn from the above | Only as clearly-marked reasoning |

**No figure in this dossier is verified.** Section 2 is the only section resting on
inspectable evidence, and even there the evidence is *what the site says*, not whether the
site is right.

---

## 1. The blocking constraint

**PMI cannot be reached from this environment.**

```
WebFetch https://www.pmi.org/certifications/project-management-pmp
→ EGRESS_BLOCKED: Access to www.pmi.org is blocked by the network egress proxy.
```

The same block applied to every other external domain tested. The only external channel is
web search, which returns **summaries of third-party pages** — never the page, never the
primary source.

Under `editorial-os/config/source-hierarchy.yaml`, PMI is **tier 2** (official
certification organisation). Every external source obtained here is **tier 10**
(secondary) *and* a training or exam-prep vendor — the exact category the hierarchy says
must never be cited as neutral evidence about its own product.

**Conclusion: the external verification layer is unavailable.** Not degraded —
unavailable. Nothing in §3 may reach the published article as fact.

---

## 2. What the repository establishes

Full extraction, with locations and cited sources, is in
**`pmp-cost-internal-claims-map.md`**. Summary of what that map found:

### 2.1 Where the site is internally consistent

**Label: VERIFIED FROM CERTNORTH REPOSITORY** — meaning the site says this consistently,
not that it is correct.

| Claim | Locations agreeing |
|---|---|
| PMP exam ~$425 member / ~$675 non-member | **5** — `pmp-cost`, `is-pmp-worth-it`, `pmp-vs-capm`, `is-pmi-membership-worth-it`, `certifications.json` |
| Renewal $60 member / $150 non-member, 60 PDUs per 3 years, ≥8 PDUs per Talent Triangle area | **3+** — `pmp-renewal-pdus`, `pmp-cost`, `certifications.json` |
| Eligibility 36 months (degree) / 60 months (secondary) + 35 contact hours | **7** — site-wide |
| CAPM $225 / $300, 23 contact hours | **4** |
| PMI-ACP $435 / $495, 21 contact hours, 30 PDUs per 3 years | **2** |

### 2.2 Where the site contradicts itself

| # | Contradiction | Severity |
|---|---|---|
| 1 | **`pmp-cost` claims "every figure sourced from PMI" three times while publishing training prices PMI does not publish** | **High** |
| 2 | PMI membership: **~$140** (`pmp-cost`) vs **~$150** (`is-pmi-membership-worth-it`) — both citing the same URL | Medium-high |
| 3 | All-in cost: **$700–$2,500** (`pmp-cost`) vs **$1,000–$3,000** (`how-to-become-project-manager`) | Medium |
| 4 | The only 10-year PMP figure on the site is renewal fees alone, in a table where every other row is a full total (`is-safe-certification-worth-it`) | Medium |
| 5 | `pmp-renewal-pdus` leads its dek with "doing your own job" while its body says that route is capped, and never gives the cap | Medium |
| 6 | Retake described as "another exam fee" — unsourced, and the only mention on the site | Medium |
| 7 | `pmp-cost` publishes renewal rules without citing the CCR Handbook that supports them | Low-medium |
| 8 | `pmp-cost` advises self-paced training with no reference to the late-2026 rule change `pmp-eligibility` documents | Low-medium |
| 9 | **No source entry anywhere in the repository carries a date** — ~160 citations, zero dates | Medium, systemic |

**Contradiction 1 is the most consequential finding of this entire research phase**, and it
required no external access. The article makes a claim about its own sourcing integrity
that its own content disproves.

### 2.3 What the repository settles permanently

**No reliable PMP pass rate exists.** `pmp-pass-rate` establishes that PMI has not
published one for roughly two decades, that the circulating "61%" is a passing score
retired around 2006, and that PMI now scores psychometrically and reports performance
bands rather than a percentage.

**Label: VERIFIED FROM CERTNORTH REPOSITORY**, and the underlying situation is not going to
change. **This is the one thing that needs no further verification**, because the *absence*
of the data is the finding.

**Consequence:** no expected-cost calculation weighted by pass probability may be built.
Scenario analysis only, with attempt counts as reader-chosen assumptions.

---

## 3. External research — DISCOVERY ONLY

**Everything in this section is SECONDARY/SEARCH DISCOVERY ONLY and
PRIMARY SOURCE VERIFICATION REQUIRED. None of it may be published as fact. None of it is
treated as competing with, or correcting, the repository values in §2.1.**

These are recorded as **questions to put to PMI**, not as answers.

| # | Question raised by search | What search returned | Status |
|---|---|---|---|
| Q1 | Did the PMP exam fee change in August 2026? | Several vendor pages state a change effective 2026-08-06 to different figures | **Question only.** Not adopted. Frequency of repetition deliberately disregarded |
| Q2 | What is the current member exam fee? | Vendor pages variously state $405, $425, $445 | **Unresolved.** Three values, no adjudication possible |
| Q3 | What is the current non-member exam fee? | Vendor pages variously state $555, $655, $675 | **Unresolved** |
| Q4 | What is the PMI membership fee? | Vendor pages variously state $129, $139, $149, $154, $159, plus a ~$10 application fee | **Unresolved.** ~20% spread |
| Q5 | **Does PMI price the exam by country?** | **Sources directly contradict each other.** One states fees are adjusted for local purchasing power in India, Brazil and APAC. Another states PMI fees are globally fixed in USD | **Unresolved, and this is the question that matters most** |
| Q6 | Is there a reduced retake fee, and how many attempts are allowed? | Vendor pages describe a reduced re-examination fee and a limited number of attempts within an eligibility period | **Unresolved.** Would contradict `pmp-cost` if true; not treated as a correction |
| Q7 | Is there a minimum number of Education PDUs within the 60? | One vendor page states a minimum | **Unresolved.** Would bear on contradiction 5 above |
| Q8 | **What is the scope of the late-2026 training-provider rule?** | One source reads it as covering all 35 contact hours; another as covering only live instructor-led training. `pmp-eligibility` says live only | **Unresolved.** Materially different rules with materially different cost consequences |

### Why no figure was selected

Protocol item 7: *do not choose between contradictory search results merely because one
appears more frequently.* Applied literally. Q2 has three candidate values and Q4 has five;
no ranking has been imposed on any of them, and the repository's existing ~$425/~$675 has
**not** been treated as refuted.

One numeric observation is recorded because it bears on Q5 rather than on a price: a
figure reported as PMI's checkout price in India converts to well under the USD figures
in circulation. If accurate it would indicate regional pricing. **It is a lead for Q5, not
a price.**

---

## 4. What cannot be verified in this environment

| Item | Why |
|---|---|
| Any PMI price — exam, membership, renewal, retake | PMI unreachable; no primary source available |
| Whether PMI prices regionally | Unreachable, and secondary sources contradict each other |
| Retake policy and fee | Unreachable; the PMP Handbook is not readable from here |
| PDU category minimums and maximums | Unreachable; the CCR Handbook is not readable from here |
| Scope of the late-2026 training-provider rule | Unreachable; secondary readings conflict |
| Whether the repository's ~$425/~$675 is currently correct | Unreachable |
| Any market-average training price | **Not establishable by anyone.** No neutral data exists; every source quoting one sells training |
| The PMP pass rate | **Unknowable permanently** — already established, needs no verification |

---

## 5. Assessment

**The research phase is partially complete.**

**Complete:** the repository layer. Every PMP cost claim on the site has been located,
attributed to its article and its cited source, and cross-checked against every other
claim. Nine contradictions were found, one of them serious and fixable by the rebuild
alone.

**Not complete, and not completable here:** the primary-source layer. No PMI figure has
been verified, and none can be from this environment.

**What this does not block:** the article's architecture, its cost taxonomy, its analytical
approach, its structural design, its internal-link plan, and its consolidation map are all
derivable from the repository and from reasoning. They are complete — see
`pmp-cost-architecture.md`.

**What it does block:** publishing any figure as verified fact, and publishing any
calculation whose inputs are not labelled.

**One human, logged in to PMI from the relevant country, resolves Q1 through Q8 in a single
sitting** — and Q5 is the one that determines whether this article can state a universal
number at all.
