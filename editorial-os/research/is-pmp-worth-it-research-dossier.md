# Research Dossier — `is-pmp-worth-it` (REBUILD 02)

**Date:** 2026-09-04
**Article:** `is-pmp-worth-it` · `/certifications/worth-it/is-pmp-certification-worth-it/`
**Phase:** research only. Nothing drafted, nothing modified, nothing published.
**Method:** repository-only. No external source was used, and none is needed for the
findings below.

---

## 1. What the page is now

| Measure | Value |
|---|---|
| Body words | **687** |
| Inbound internal links | **17** — joint-highest on the site |
| Outbound internal links | 7 |
| Sources cited | 4 |
| Blocks | 4 paragraphs · 2 callouts · 5 headings · 2 lists · 1 table · 1 FAQ |
| Opens | paragraph → callout (the site's 50/50 pattern) |
| Closes | FAQ (the site's 50/50 pattern) |
| Content type | DECISION |
| `updatedAt` | 2026-09-04 (the price correction) |

**Heading spine:**

1. What it costs and demands
2. **The case for it (real pros)**
3. **The case against it (real cons)**
4. A myth worth correcting: the PMP is not "waterfall only"
5. **The honest bottom line**

**Headings 2, 3 and 5 are shared verbatim with seven other articles** — `is-capm-worth-it`,
`is-csm-worth-it`, `is-pmi-acp-worth-it`, `is-prince2-worth-it`, `is-psm-worth-it`,
`is-pspo-worth-it`, `is-safe-certification-worth-it`. `is-pmi-acp-worth-it` shares four,
including "What it costs and demands".

This is the template the audit identified as the site's highest-severity pattern, and this
article is one of its eight instances.

---

## 2. Finding 1 — a cited source that supports nothing

The article's source list includes:

> **U.S. Bureau of Labor Statistics — Project Management Specialists, Occupational Outlook Handbook**

**The body never uses it.** Searched for "Bureau", "BLS", "labor", "labour", "statistic",
"median", "100,750" and "occupation": **zero occurrences.** No claim in the article traces
to that source.

**Label: VERIFIED FROM CERTNORTH REPOSITORY.**

This is not a false claim — it is a citation doing no work. But it belongs to the same
family as the `pmp-cost` problem the last rebuild fixed: **the appearance of sourcing
without the substance of it.**

### And it is worse than decorative

The BLS Occupational Outlook Handbook is precisely the source that
`do-you-need-certification-project-manager` uses — with 5 inbound links — to argue the
opposite conclusion:

> *"The U.S. Bureau of Labor Statistics states that certification is not a requirement for
> the occupation — its wording is that certification 'may be beneficial'… Beneficial is not
> the same as necessary."*

**So the site's flagship "is it worth it" page cites the authority that undercuts it, and
never engages with what that authority says.** That is the single most interesting thing
found in this research.

---

## 3. Finding 2 — the strongest argument on this subject is not on this page

The article's case-for list says:

> *"It's widely associated with higher salaries for experienced PMs"*

That is the soft version. The site's own `does-pmp-increase-salary` does the real work:

> *"The famous 'PMP holders earn 17–33% more' comes from PMI's own survey of self-reported
> salaries, and it compares certified professionals against a group that includes…"*
> *"…the headline figure cannot be read as 'get the PMP and earn 17% more', because the
> people it compares are not otherwise similar. Expect a modest effect, not a
> transformation."*

**The rigorous analysis lives on a page with 2 inbound links. The flat assertion lives on
the page with 17.** The article does link to it from a FAQ answer, but its own body still
states the version the dedicated article spends 1,027 words qualifying.

**Label: VERIFIED FROM CERTNORTH REPOSITORY + EDITORIAL INFERENCE.**

---

## 4. Finding 3 — a duplicated table, and the other version is better

| Article | Table | Columns |
|---|---|---|
| `is-pmp-worth-it` `body[10]` | PMP exam domain weighting before and after 9 July 2026 | Domain · Previous · From July 2026 |
| `how-to-prepare-for-pmp-exam` `body[8]` | Roughly how many of the 180 questions each domain represents | Domain · Previous weight · Current weight · **Approx. questions now** |

Same three rows, same figures (42→33, 50→41, 8→26). **The preparation article's version adds
the question counts, which is what makes the shift concrete.**

The whole "A myth worth correcting" section — one paragraph plus this table — restates
material owned by `how-to-prepare-for-pmp-exam`. It is good material. It is in the wrong
article.

---

## 5. Finding 4 — an unverified claim about a price movement

`body[3]`: *"PMI adjusted its fees during 2026 and prices also vary by country."*

`pmp-vs-capm` carries a stronger form: *"PMI raised PMP exam fees in 2026, so the gap
between the two is now wider than older articles suggest."*

**Neither is supported.** The verified figures ($405 / $655) match no before-and-after pair
that this project has been able to establish, and the fee-increase narrative traces to
vendor pages that the last rebuild's protocol correction ruled out as evidence.

**Label: PRIMARY-SOURCE VERIFICATION REQUIRED.** Until verified, the rebuild should either
drop the claim or state that we could not confirm a change.

**Note:** this also affects `pmp-vs-capm`, which is out of scope here and is recorded, not
fixed.

---

## 6. What this article still owns, after everything else claims its subject

| Subject | Owner |
|---|---|
| What it costs | `pmp-cost` (rebuilt, 1,743 words) |
| Whether you qualify | `pmp-eligibility` |
| The July 2026 exam change | `how-to-prepare-for-pmp-exam` |
| Whether it raises pay | `does-pmp-increase-salary` |
| The cheaper alternative | `pmp-vs-capm` |
| The agile alternative | `psm-vs-csm`, `scrum-master-vs-project-manager` |
| Difficulty / pass rate | `pmp-pass-rate` |
| **Whether you need any certification at all** | `do-you-need-certification-project-manager` |
| Cost of keeping it | `pmp-renewal-pdus` |
| Membership economics | `is-pmi-membership-worth-it` |

**Almost nothing is left except the verdict itself** — which is exactly what the audit said
about all eight `is-X-worth-it` pages: *"what they add over the official source is the
verdict, and the verdict is formatted identically eight times."*

**Label: EDITORIAL INFERENCE.**

---

## 7. The original-value opportunity

The site has spent six weeks accumulating **four evidence-led arguments that complicate the
naive "yes, get the PMP"** — and none of them appears in the page that renders the verdict:

| Complication | Where it lives | Inbound links |
|---|---|---|
| BLS says certification is **not required** for the occupation | `do-you-need-certification-project-manager` | 5 |
| The salary premium comes from a **self-selected, non-comparable** survey | `does-pmp-increase-salary` | 2 |
| The **pass rate is unknowable** — every figure in circulation is a retired passing score or a vendor's own students | `pmp-pass-rate` | 1 |
| The cost **does not stop at the exam** — renewal recurs for as long as you hold it | `pmp-cost`, `pmp-renewal-pdus` | 11, 3 |

**The strongest possible version of this page is the one that assembles its own site's best
counter-arguments and still reaches a defensible verdict.** That is something no training
provider can publish, and something no PMI page has any reason to. It is also a genuinely
different job from a pros-and-cons list.

It is also structurally different from `pmp-cost`, which is the other constraint: the
rebuild must not import that article's shape either.

---

## 8. What needs primary-source verification

| # | Claim | Status |
|---|---|---|
| 1 | "PMI adjusted its fees during 2026" | **PRIMARY-SOURCE VERIFICATION REQUIRED** — see §5 |
| 2 | Domain weights 42/50/8 → 33/41/26 | PARTIALLY VERIFIED — repository, citing PMI's 2026 ECO |
| 3 | ~40% predictive, ~60% agile and hybrid | PARTIALLY VERIFIED — same |
| 4 | Eligibility 36 / 60 months + 35 contact hours | PARTIALLY VERIFIED — repository, 7 locations |
| 5 | Exam fee $405 / $655 | **VERIFIED** — PMI, checked by the Editor-in-Chief |
| 6 | Renewal 60 PDUs + fee every 3 years | VERIFIED (limits) / repository (fee) |

**No external research is required to proceed.** Every finding in this dossier came from the
repository, and the one unverified claim is a candidate for removal rather than
confirmation.

---

## 9. Assessment

**The research phase is complete and it did not need the outside world.**

The article is not wrong. It is **thin, template-bound, and outflanked by its own site** —
it renders a verdict without engaging any of the four arguments CertNorth has already
published that make the verdict hard.

Its 17 inbound links make it the joint most-linked page on the site. It is currently the
second-thinnest of the pages that carry that much internal traffic.

**Recommended next step per the pipeline: diagnosis, then fact-check, then its own
architecture.** The architecture must break the eight-article spine and must not borrow the
`pmp-cost` shape.
