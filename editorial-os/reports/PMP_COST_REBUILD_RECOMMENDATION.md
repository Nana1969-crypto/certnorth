# Rebuild Recommendation — `pmp-cost`

**Date:** 2026-09-04
**Revised:** 2026-09-04 — verification protocol corrected; conclusions changed accordingly
**Article:** `pmp-cost` · `/certifications/guides/pmp-certification-cost/`
**Phase:** research **partially complete** — repository layer done, primary-source layer blocked
**Live content modified:** none

---

## 1. Recommendation

**Rebuild the architecture now. Do not draft to publication standard until PMI's prices
have been read by a human.**

**One change should be made regardless of everything else: `pmp-cost` claims three times
that every figure comes from PMI, and that is not true.** See §4.

---

## 2. What changed since the first version of this report

The first version assigned **MEDIUM confidence** to an exam fee on the grounds that several
unaffiliated vendor pages agreed. **That reasoning was wrong and has been withdrawn.**

Repetition is not verification. A figure copied between commercial sites is one claim
appearing many times. When every site concerned sells PMP training, agreement between them
is weak evidence about PMI's prices and no evidence about which figure is current.

Consequences of the correction:

| First version | Now |
|---|---|
| Modelled the exam at $445/$675 | Models the repository's **~$425/~$675** |
| Modelled membership at $149 | Models **$140–$150** — the range *is* the site's internal contradiction |
| Proposed a section correcting our retake claim | **Withdrawn.** The correction rested on search results |
| Included a retake scenario at $275 | **Withdrawn** |
| Treated the August 2026 change as probable | Treated as **a question to ask PMI** |

**The research got weaker in claims and stronger in integrity.** That is the right
direction.

---

## 3. What the repository establishes

Full extraction in `pmp-cost-internal-claims-map.md`: every PMP cost claim on the site,
located, attributed to its article and its cited source, cross-checked against every other.

### Where the site agrees with itself

| Claim | Locations |
|---|---|
| PMP exam ~$425 member / ~$675 non-member | **5** |
| Renewal $60 / $150, 60 PDUs per 3 years, ≥8 per Talent Triangle area | **3+** |
| Eligibility 36/60 months + 35 contact hours | **7** |

**More internally consistent on the headline fee than expected.** Whether it is *correct*
is a separate question this environment cannot answer.

### Where it does not — nine contradictions

| # | Contradiction | Severity | Fixable by this rebuild alone? |
|---|---|---|---|
| 1 | **"Every figure sourced from PMI" while publishing training prices PMI does not publish** | **High** | **Yes — and needs no verification** |
| 2 | Membership **~$140** vs **~$150**, same cited URL | Medium-high | No — second article |
| 3 | All-in cost **$700–$2,500** vs **$1,000–$3,000** | Medium | No — second article |
| 4 | The site's only 10-year PMP figure is renewal fees alone, in a table where every other row is a full total | Medium | No — second article |
| 5 | `pmp-renewal-pdus` dek leads with "doing your own job"; its body says that route is capped and never gives the cap | Medium | No — second article |
| 6 | Retake described as "another exam fee" — unsourced, only mention on the site | Medium | **Yes** — remove or qualify |
| 7 | Renewal rules published without citing the CCR Handbook that supports them | Low-medium | **Yes** — add the source |
| 8 | Self-paced training advised with no reference to the late-2026 rule change | Low-medium | **Yes** |
| 9 | **No source entry anywhere carries a date** — ~160 citations, zero dates | Medium, systemic | No — schema decision |

---

## 4. The finding that needs no verification

`pmp-cost` says, three times:

- `body[0]`: *"Here's the full picture, with every fee sourced from PMI."*
- `body[3]` table caption: *"PMP core costs in 2026 (source: PMI)."*
- `seo.metaDescription`: *"Every figure sourced from PMI."*

**That same table contains "Required education (35 contact hours) | $0–$600 depending on
provider", and the article's second table prices third-party training at $700–$2,500+.**

PMI does not sell PMP training and does not publish its price. **Neither figure can be
sourced to PMI.**

This is a claim about our own sourcing integrity, on a site whose entire position is
independence and verifiability, on the page the audit already identified as the weakest.
The claim and the content disproving it are in the same file.

**Recommendation: remove it whether or not the rebuild proceeds.**

---

## 5. Original value — the Phase 10 test

1. A cost taxonomy by behaviour: required, conditional, optional, recurring.
2. The membership break-even **in both directions** — it reverses at renewal.
3. Cost of ownership over ten years, every assumption stated and substitutable.
4. A **refusal** to compute a pass-rate-weighted expected cost, with the reason.
5. Financial cost and time commitment held apart, never monetised.
6. An explicit account of what we could and could not confirm — including that our own page
   overstates its sourcing.

**The test passes.** Item 6 is the strongest and the cheapest.

---

## 6. The result worth publishing

**CERTNORTH CALCULATION**, inputs from the repository, all requiring primary verification.
Assumptions: exam ~$425 member; membership $140–$150/yr; renewal $60/$150 per three years;
PDUs and the 35 hours obtained free; no materials; no retake; application fee excluded
because the site never quantifies it.

| Scenario | 5-year | 10-year |
|---|---|---|
| **A** — join for the exam year, then lapse | $715–$725 | **$1,015–$1,025** |
| **B** — maintain membership throughout | $1,185–$1,235 | **$2,005–$2,105** |

Over ten years, keeping membership costs roughly **$990–$1,080 more** and saves **$270** in
renewal fees.

**Not modelled:** retakes (fee unverified, our own claim unsourced) and training (no
neutral data exists). The article says so rather than guessing.

---

## 7. Structure

Full plan in `pmp-cost-architecture.md`. Template-breaking moves:

- **Second block is a heading, not a callout** — breaking a 50/50 site-wide pattern
- **Leads with an uncertainty ledger**, not a price table
- **One callout in the whole article**
- **No FAQ block** — `build.js` `runGate()` was read directly and does not require one
- **No year in the title**, on a page arguing that fixed figures go stale
- All eight H2s checked against the site's 215 existing level-2 headings: **zero collisions**
- Content type shifts DECISION → **RESEARCH**

URL, slug, `clusterId`, `primaryKeyword` and `publishedAt` unchanged. All 11 inbound links
continue to resolve. Sources must now add the **CCR Handbook** and the **PMP Handbook**.

---

## 8. What needs approval

| # | Decision | Recommendation |
|---|---|---|
| 1 | **Remove the "every figure sourced from PMI" claim** | **Yes — independent of everything else.** It is untrue and needs no verification |
| 2 | Verify PMI prices before drafting? | **Yes.** One sitting resolves eight open questions. Without it, no figure may be published as fact |
| 3 | Drop the FAQ block? | **Yes.** It would restate the body. Cost: loses `FAQPage` schema; would be the site's first article without one |
| 4 | Fix the membership figure in `is-pmi-membership-worth-it`? | **Second article — needs approval.** Two pages give different numbers for the same fee |
| 5 | Fix the all-in range in `how-to-become-project-manager`? | **Second article — needs approval** |
| 6 | Reconcile the 10-year row in `is-safe-certification-worth-it`? | **Second article — needs approval** |
| 7 | Fix the dek in `pmp-renewal-pdus`? | **Second article — needs approval** |
| 8 | Update `certifications.json`? | **Changes a second published page — needs approval.** Only after real verification, with `verifiedOn` advanced honestly |
| 9 | **Add a date field to the source schema?** | **Systemic — needs a decision.** ~160 citations currently carry no date |

---

## 9. Assessment

**Repository layer: complete.** Every PMP cost claim mapped; nine contradictions found; one
serious and fixable without any external access.

**Primary-source layer: blocked, and not completable here.** PMI is unreachable. No figure
is verified.

**The architecture does not depend on the blocked layer** — the editorial question, the
angle, the taxonomy, the section order, the structural decisions, the internal links and
the consolidation map are all final. **Only the numbers are blocked.**

**The article can be designed. It cannot yet be published.**
