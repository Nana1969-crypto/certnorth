# Internal Claims Map — every PMP cost claim in the CertNorth repository

**Date:** 2026-09-04
**Method:** programmatic extraction from `platform/content/` — all 50 article files plus
`certifications.json`. Every text-bearing element (paragraphs, callouts, list items,
table captions, table rows, FAQ questions and answers, dek, meta description, title) was
scanned for PMI/PMP/CAPM/PgMP/PMI-ACP together with a currency amount or a cost keyword.
**No external source was used in this document.**
**No file was modified.**

---

## Label definitions used throughout

| Label | Meaning |
|---|---|
| **VERIFIED FROM CERTNORTH REPOSITORY** | The repository demonstrably contains this. It says nothing about whether the claim is *true* — only that this is what the site publishes |
| **PRIMARY SOURCE VERIFICATION REQUIRED** | The truth of this claim can only be settled at the issuing body. Not settled here |
| **SECONDARY/SEARCH DISCOVERY ONLY** | Encountered via web search. Discovery lead. **Never** treated as verification |
| **CERTNORTH CALCULATION** | Arithmetic performed by us from stated inputs. Valid only if its inputs are |
| **EDITORIAL INFERENCE** | A judgement drawn from the above. Reasoning, not fact |

---

## 1. A structural finding that affects every claim below

**No source entry anywhere in the repository carries a date.**

The source schema across all 50 articles is `{label, url}` — nothing else. There is no
publication date, no access date, no "as of" field. Approximately 160 citations, zero
dates.

**Label: VERIFIED FROM CERTNORTH REPOSITORY.**

The only dated field in the entire content layer is `certifications.json`, where all six
records carry `verifiedOn: 2026-07`.

**Consequence:** the protocol asks for "date of that source if available". For every
article the answer is **not available**. No CertNorth cost claim can currently be tied to
a moment in time. This is a schema gap, not an oversight in one article, and it is why
figures can drift without anything in the system noticing.

**Label: EDITORIAL INFERENCE.**

---

## 2. The PMP exam fee

### What the repository says

| Article | Value stated | Location | Source cited by that article | Source date |
|---|---|---|---|---|
| `pmp-cost` | **~$425 member / ~$675 non-member** | `body[3]` table rows 0–1, `dek`, `body[12].faq[0].a` | PMI — PMP page; PMI — Membership | **none** |
| `is-pmp-worth-it` | ~$425 / ~$675 | `body[3]` | PMI — PMP page; BLS; PMI — new exam; PMI — ECO 2026 | **none** |
| `pmp-vs-capm` | ~$425 / ~$675 | `body[3]` table, `body[12].faq[2].a` | PMI — PMP page; PMI — CAPM page | **none** |
| `is-pmi-membership-worth-it` | ~$425 / ~$675 | `body[4]` table, `body[19].faq[1].a` | PMI — Membership; PMI — PMP page; PMI — maintain | **none** |
| `certifications.json` | `~$425 member / ~$675 non-member (verify for your country)` | record `pmp` | PMI — PMP page | `verifiedOn: 2026-07` |

**Internal contradiction: NONE.** Five locations agree exactly.
**Label: VERIFIED FROM CERTNORTH REPOSITORY** — the site is internally consistent here.

### What is not settled

Whether ~$425/~$675 is *correct* cannot be determined from the repository.
**Label: PRIMARY SOURCE VERIFICATION REQUIRED.**

A search lead exists suggesting a change effective August 2026 to different figures.
**Label: SECONDARY/SEARCH DISCOVERY ONLY.** It is recorded as a question to ask PMI, not
as a competing value. Repetition across vendor pages is not evidence and has not been
treated as such.

### A related claim the repository makes about itself

Two articles assert that PMI raised fees during 2026:

- `pmp-cost` `body[1]`: *"PMI raised its exam fees in 2026."*
- `pmp-vs-capm` `body[4]`: *"PMI raised PMP exam fees in 2026, so the gap between the two is now wider than older articles suggest."*
- `is-pmp-worth-it` `body[3]`: *"PMI adjusted its fees during 2026 and prices also vary by country."*

**Label: VERIFIED FROM CERTNORTH REPOSITORY** (the site says this) **+ PRIMARY SOURCE
VERIFICATION REQUIRED** (whether it is so, and whether ~$425 is the pre- or post-increase
figure).

---

## 3. PMI membership fee — **CONTRADICTION**

| Article | Value stated | Location | Source cited | Source date |
|---|---|---|---|---|
| `pmp-cost` | **~$140 a year** | `body[3]` row 2, `body[4]` | PMI — Membership | **none** |
| `is-pmi-membership-worth-it` | **~$150 a year** | `body[1]`, `body[4]` table, `body[11]` table, `body[19].faq[0].a`, `dek` | PMI — Membership | **none** |

**Both articles cite the same URL and state different numbers.**

**Label: VERIFIED FROM CERTNORTH REPOSITORY** — the contradiction is real and present in
published content.

Both mention a "small one-time application fee" without quantifying it.

### Downstream effect on published arithmetic

| Article | Published net benefit of joining | Derivation |
|---|---|---|
| `is-pmi-membership-worth-it` `body[4]` | "~$100 in your favour" | $675 − ($150 + $425) = $100 |
| `pmp-cost` `body[4]` | not stated, but implied | $250 saving − $140 membership = $110 |

**CERTNORTH CALCULATION** — both are arithmetically correct *given their own inputs*. They
produce different answers because the inputs disagree. **The two pages cannot both be
right.**

**Also:** `is-pmi-membership-worth-it` `body[4]` omits the one-time application fee that
the same article's callout and FAQ both mention, so its $100 figure is slightly
overstated by that fee. **Label: CERTNORTH CALCULATION** (an error in our own table).

---

## 4. Renewal fee and PDU requirement

| Article | Value stated | Location | Source cited | Source date |
|---|---|---|---|---|
| `pmp-renewal-pdus` | **$60 member / $150 non-member**, 60 PDUs / 3 years, ≥8 PDUs in each of 3 Talent Triangle areas | `body[1]`, `body[3]` table, `body[19]`, `body[22].faq[1].a`, `dek` | PMI — maintain; PMI — earn PDUs; **PMI — CCR Handbook**; PMI — Talent Triangle | **none** |
| `pmp-cost` | $60 / $150, 60 PDUs / 3 years | `body[3]` row 4, `body[10]`, `body[12].faq[2].a` | PMI — PMP page; PMI — Membership | **none** |
| `certifications.json` | `60 PDUs every 3 years + $60/$150 fee` | record `pmp` | PMI — PMP page | `verifiedOn: 2026-07` |
| `is-safe-certification-worth-it` | `body[9]` row 2 | see §5 | — | — |

**Internal contradiction on the figures: NONE.**
**Label: VERIFIED FROM CERTNORTH REPOSITORY.**

### But there is a sourcing gap

`pmp-renewal-pdus` cites the **CCR Handbook**, which is the document that would actually
support these requirements. `pmp-cost` states the same requirements while citing only the
PMP landing page and the Membership page — **neither of which is the source for renewal
rules**.

**Label: EDITORIAL INFERENCE.** `pmp-cost` publishes claims its own citation list does not
support. The rebuild must carry the CCR Handbook in its sources.

---

## 5. Ten-year cost — **METHODOLOGICAL INCONSISTENCY**

`is-safe-certification-worth-it` `body[9]`, caption: *"Ten-year cost of keeping one
credential current, across the certifications we cover."*

| Certification | Renewal cycle | Approximate 10-year total |
|---|---|---|
| PSM I / PSPO I | Never expires | ~$200 |
| CSM | Every 2 years | ~$1,200–$1,900 |
| **PMP** | Every 3 years | **"Exam plus ~$180–$450 in fees"** |
| SAFe (foundational) | Every year | ~$2,755 |

**Every other row is a single total. The PMP row is not a total at all** — it is renewal
fees only ($60 × 3 = $180; $150 × 3 = $450), with the exam left as an unpriced "plus" and
membership excluded entirely.

**Label: VERIFIED FROM CERTNORTH REPOSITORY** (the table is published this way)
**+ EDITORIAL INFERENCE** (that this makes the PMP look cheaper than the comparison
intends, in a table whose whole purpose is comparison).

**This is the only ten-year PMP figure the site currently publishes, and it lives in an
article about SAFe.** If the rebuilt `pmp-cost` publishes a proper ten-year model, this
row must be reconciled with it — which means touching a second article.

---

## 6. All-in cost range — **CONTRADICTION**

| Article | Value stated | Location |
|---|---|---|
| `pmp-cost` | **$700–$2,500** | `dek`, `body[12].faq[0].a` |
| `pmp-cost` | $700–$1,000 / $1,200–$1,800 / $2,000–$2,500+ by study approach | `body[7]` table |
| `how-to-become-project-manager` | **$1,000–$3,000** for the "PMP path" | `body[15]` table row 2 |

`pmp-cost`'s own dek and its own table are consistent with each other. **They are not
consistent with `how-to-become-project-manager`**, which puts the same journey at
$1,000–$3,000.

**Label: VERIFIED FROM CERTNORTH REPOSITORY.**

Neither range is traceable to any cited source. `how-to-become-project-manager` cites only
BLS and the PMI certifications index; `pmp-cost` cites the PMP page and the Membership
page. **No cited source publishes third-party training prices, because none of them sells
training.**

**Label: EDITORIAL INFERENCE** — both ranges appear to be estimates presented without
being labelled as estimates.

---

## 7. **A false claim inside `pmp-cost` itself**

This is the most serious finding in this map, and it is fully verifiable without leaving
the repository.

`pmp-cost` `body[0]`:
> *"Here's the full picture, **with every fee sourced from PMI**."*

`pmp-cost` `seo.metaDescription`:
> *"...plus how to keep the total down. **Every figure sourced from PMI.**"*

`pmp-cost` `body[3]` table caption:
> *"PMP core costs in 2026 **(source: PMI)**."*

**But that same table contains a row PMI does not and cannot publish:**

| Item | Cost |
|---|---|
| Required education (35 contact hours) | **$0–$600 depending on provider** |

And the article's second table, `body[7]` — "Typical all-in PMP budget by study approach",
ranging $700 to $2,500+ — is entirely third-party training pricing.

**PMI does not sell PMP training and does not publish its price.** Neither figure can be
sourced to PMI. The article states three times that every figure comes from PMI, and at
least two of its figures do not.

**Label: VERIFIED FROM CERTNORTH REPOSITORY.** This is not a matter of interpretation: the
claim and the contradicting content are in the same file.

**Severity: high.** It is a claim about our own sourcing integrity, on the page the audit
already identified as the site's weakest. The rebuild must remove it. **It should be
removed whether or not the rebuild proceeds.**

---

## 8. Retake policy — **UNSOURCED, AND THE ONLY MENTION ON THE SITE**

| Article | Claim | Location | Source cited |
|---|---|---|---|
| `pmp-cost` | *"pass on the first try — **a retake adds another exam fee**"* | `body[8]` callout | PMI — PMP page; PMI — Membership |

**No other article on the site mentions retakes.** There is no second value, so there is no
internal contradiction — but there is no internal support either.

**Neither cited source is a handbook**, and retake policy would live in the PMP Handbook,
which `pmp-cost` does not cite. (`pmp-eligibility` and `how-long-to-get-pmp` both cite
"PMI — PMP Handbook"; `pmp-cost` does not.)

**Label: PRIMARY SOURCE VERIFICATION REQUIRED.** Search discovery suggests a *reduced*
retake fee and a limited number of attempts, which would make the current wording wrong in
both directions — but that is **SECONDARY/SEARCH DISCOVERY ONLY** and is recorded as a
question, not a correction.

**Until verified at PMI, the rebuilt article may not assert either version.** The honest
options are to omit retakes or to describe only what is verifiable.

---

## 9. PDU sourcing — **INTERNAL TENSION INSIDE ONE ARTICLE**

All within `pmp-renewal-pdus`:

| Location | Statement |
|---|---|
| `dek` | *"a large share of those PDUs can be earned without paying for anything, **including by doing your own job**"* |
| `body[22].faq[2].a` | *"most people can cover a large share of a cycle at no cost. **Working in your certified role counts as giving back**"* |
| `body[11]` | *"Education — this is the required category, and PMI places **no cap** on how many PDUs you can earn this way"* |
| `body[12]` | *"Giving Back — This is optional, and **PMI limits how much of your total can come from it**, so treat it as a supplement rather than a strategy"* |
| `body[17]` callout | *"Category caps do apply — PMI limits how many PDUs certain activities can contribute in a cycle, and those limits change from time to time"* |

**The dek leads with the route the body then describes as capped.** Working in your role is
Giving Back; Giving Back is limited; the article never states the limit.

**Label: VERIFIED FROM CERTNORTH REPOSITORY** (both statements are published)
**+ EDITORIAL INFERENCE** (that the dek promises more than the body supports).

**The cap value is PRIMARY SOURCE VERIFICATION REQUIRED** — it is in the CCR Handbook,
which the article cites but from which no number was transcribed.

**Consequence for the rebuild:** `pmp-cost` cannot claim PDUs are effectively free on the
strength of "you already do the job", because our own article says that route is capped
and does not say by how much.

---

## 10. Training / 35 contact hours requirement

| Article | Claim | Location | Source cited |
|---|---|---|---|
| `pmp-eligibility` | 35 contact hours for every pathway; **"can come from any eligible course or provider — PMI doesn't require a specific one"**; live or on demand | `body[3]` caption, `body[10]` | PMI — PMP page; PMI — PMP Handbook; PMI — new exam |
| `pmp-eligibility` | **From late Q4 2026, live instructor-led training must be delivered through an approved provider pathway** (ATPs, China REPs, eligible academic programmes) | `body[11]` callout | same |
| `pmp-eligibility` | An active CAPM can cover the requirement | `body[10]`, `body[14].faq[1].a` | same |
| `pmp-cost` | *"choose a self-paced course for your 35 education hours"* | `body[8]` callout | PMI — PMP page; PMI — Membership |
| `pmp-vs-capm` | PMP requires 35 contact hours; CAPM 23 | `body[3]` table, `body[8]` | PMI pages |
| `best-pm-certifications-beginners` | The Google certificate counts toward the CAPM education requirement | `body[4]` | PMI certifications; Coursera |

**Internal contradiction on the requirement itself: NONE.**

**But `pmp-cost` gives cost-saving advice ("choose a self-paced course") without any
reference to the rule change that `pmp-eligibility` documents.** The two articles are not
in conflict on facts; they are in conflict on what a reader should do next.

**Label: EDITORIAL INFERENCE.** The advice is not future-proofed. Whether the change
affects on-demand training or only live instructor-led training is
**PRIMARY SOURCE VERIFICATION REQUIRED** — `pmp-eligibility` says live only; search
discovery offers a broader reading; neither is settled here.

---

## 11. Adjacent PMI figures (context, not contradictions)

| Fact | Articles | Consistent? |
|---|---|---|
| CAPM exam $225 member / $300 non-member | `is-capm-worth-it`, `pmp-vs-capm`, `best-pm-certifications-beginners`, `certifications.json` | **Yes**, 4 locations |
| CAPM 23 contact hours, no experience | `is-capm-worth-it`, `pmp-vs-capm`, `certifications.json` | **Yes** |
| PMI-ACP $435 member / $495 non-member, 21 contact hours | `best-agile-certifications`, `is-pmi-acp-worth-it` | **Yes**, 2 locations |
| PMI-ACP renewal 30 PDUs / 3 yrs, min 4 per area | `is-pmi-acp-worth-it` | Single source; consistent with PMP's 8 per area |
| PgMP ~$800 member / ~$1,000 non-member | `how-to-become-program-manager` | Single location |
| PMP eligibility 36 months (degree) / 60 months (secondary) | `pmp-eligibility`, `is-pmp-worth-it`, `pmp-vs-capm`, `certifications.json`, and 3 more | **Yes**, consistent site-wide |

All **VERIFIED FROM CERTNORTH REPOSITORY** as to what the site says;
all **PRIMARY SOURCE VERIFICATION REQUIRED** as to whether it is correct.

---

## 12. Summary — the contradiction ledger

| # | Contradiction | Type | Articles affected | Severity |
|---|---|---|---|---|
| 1 | **"Every figure sourced from PMI"** while publishing training prices PMI does not publish | Claim contradicts own content | `pmp-cost` | **High** |
| 2 | Membership **~$140** vs **~$150** — same cited URL | Value conflict | `pmp-cost`, `is-pmi-membership-worth-it` | **Medium-high** |
| 3 | All-in cost **$700–$2,500** vs **$1,000–$3,000** | Value conflict | `pmp-cost`, `how-to-become-project-manager` | **Medium** |
| 4 | Ten-year PMP row is renewal fees only, while every other row in the same table is a full total | Methodological | `is-safe-certification-worth-it` | **Medium** |
| 5 | Dek leads with "doing your own job" for PDUs; body says that route is capped and never gives the cap | Internal tension | `pmp-renewal-pdus` | **Medium** |
| 6 | Retake described as "another exam fee" — unsourced, single mention, handbook not cited | Unsourced claim | `pmp-cost` | **Medium** |
| 7 | Renewal rules published without citing the CCR Handbook that supports them | Sourcing gap | `pmp-cost` | **Low-medium** |
| 8 | Self-paced training advised with no reference to the late-2026 rule change | Advice not future-proofed | `pmp-cost` vs `pmp-eligibility` | **Low-medium** |
| 9 | **No source anywhere carries a date** | Schema gap | All 50 articles | **Medium**, systemic |

**Contradictions 1, 6, 7 and 8 live inside `pmp-cost` and can be fixed by the rebuild
alone.**

**Contradictions 2, 3, 4, 5 and 9 require touching other articles or the content schema,
and therefore require the Editor-in-Chief's approval.** They are recorded here, not fixed.

---

## 13. What this map establishes

**The repository is more internally consistent on the headline exam fee than expected** —
five locations agree — and **less consistent than expected on everything around it**.

More importantly: **`pmp-cost` currently claims a standard of sourcing it does not meet.**
That finding required no external access at all, and it is arguably a more serious problem
than the unverified price, because the price is merely unconfirmed while the sourcing
claim is demonstrably untrue.
