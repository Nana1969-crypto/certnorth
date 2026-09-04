# Rebuild Recommendation — `pmp-cost`

**Date:** 2026-09-04
**Article:** `pmp-cost` · `/certifications/guides/pmp-certification-cost/`
**Phase:** research complete, drafting not started
**Live content modified:** none

---

## 1. Recommendation

**Rebuild — but resolve the exam fee at PMI first, or publish it explicitly labelled as
unverified.**

The research supports a rebuild that genuinely changes the page's editorial value. It does
**not** support publishing any fee as verified fact.

---

## 2. The finding that shapes everything

**PMI could not be reached.** The environment's egress proxy blocks all outbound requests,
including `pmi.org`. The only external channel is web search, which returns summaries of
third-party pages.

**Every external source obtained is a training provider or exam-prep vendor** — tier 10 in
`source-hierarchy.yaml`, and specifically the category the hierarchy says must never be
cited as neutral evidence about its own product.

They also disagree with each other:

| Fact | Disagreement found |
|---|---|
| Exam fee, member | $405 · $425 (CertNorth) · $445 |
| Exam fee, non-member | $555 · $655 · $675 |
| PMI membership | $129 · $139 · $149 · $154 · $159 |
| **Regional pricing** | One source: PMI adjusts fees for local purchasing power in India, Brazil and APAC. Another: PMI fees are globally fixed in USD. **Direct contradiction** |
| **ATP rule scope** | One source: all 35 contact hours must come from an ATP. Another: only live instructor-led training is restricted. **Materially different rules** |

An India figure reported as PMI's own checkout price — ₹24,708, about **$281** — is far
below $445 and inconsistent with a straight USD conversion. If accurate, it is evidence
that PMI prices by region.

**Conclusion: no universal global PMP price can be responsibly stated from the evidence
available.** That is the finding, not a failure of the research.

---

## 3. What CertNorth is currently publishing, and what is wrong with it

| Issue | Severity | Detail |
|---|---|---|
| The member exam fee matches nothing | **High** | The site says ~$425. That is neither the reported old price ($405) nor the reported new one ($445). The non-member figure ($675) matches the *new* price. **The site carries a mixed pair** |
| `certifications.json` is probably stale | **High** | `examCost: "~$425 member / ~$675 non-member"`, `verifiedOn: 2026-07`. If the 2026-08-06 increase is real, this is out of date — **and it feeds the `certTable` on `best-pm-certifications-beginners`**, so the error appears on a second page |
| Retake cost is misdescribed | **Medium-high** | The article says a retake "adds another exam fee". Secondary sources report a **reduced** retake fee ($275 member / $375 non-member). If correct, CertNorth overstates it by roughly $170 — and omits the real risk, a **one-year lockout after three failed attempts** |
| The site contradicts itself on membership | **Medium** | `pmp-cost` says ~$140/yr; `is-pmi-membership-worth-it` says ~$150/yr |
| The membership benefit is overstated | **Medium** | The site's ~$100 net benefit rests on a $250 exam-fee gap. The reported post-August gap is **$230**, giving $61–$91 depending on the membership figure |
| No renewal economics | **Medium** | The page stops at the purchase. It never models what keeping the credential costs |

**Five of these six are corrections, not enhancements.** That alone justifies the rebuild
independently of length.

---

## 4. Original value — the Phase 10 test

> *What does this article give the reader that the PMI pricing page does not?*

1. A taxonomy of costs by behaviour — required, conditional, optional, recurring.
2. The membership break-even run **in both directions**; it reverses at renewal.
3. A correction of an industry claim: "the renewal discount means membership pays for
   itself" is false — ~$90 saved per cycle against ~$447 of membership.
4. The retake mechanism described correctly, including the one-year lockout.
5. A **refusal** to compute a pass-rate-weighted expected cost, with the reason — because
   no reliable pass rate exists, as `pmp-pass-rate` already establishes.
6. Financial cost and time commitment held apart, never monetised — plus the point that
   **at least 35 of the 60 PDUs must be Education, so "your job covers it" is wrong.**
7. An explicit account of what cannot be verified and why.

**None of these is "we explain PMI's prices better."** The test passes.

---

## 5. The result worth publishing

**CERTNORTH CALCULATION**, all inputs unverified and stated, US pricing, PDUs and the 35
contact hours obtained free, no purchased materials:

| Scenario | 5-year | 10-year |
|---|---|---|
| **A** — pass first time, membership for the exam year only | $754 | **$1,054** |
| **B** — same, membership maintained throughout | $1,260 | **$2,125** |
| **C** — A plus one retake | — | **$1,329** |

Over ten years, **keeping PMI membership costs about $1,071 more than letting it lapse,
while saving $270 in renewal fees.** A failed attempt adds about 26% to a bare-bones
ten-year cost — considerably less than "another exam fee" implies.

These are three explicitly assumed paths. **Not "typical". Not "average".**

---

## 6. Structure

Full plan in `pmp-cost-architecture.md`. The template-breaking moves:

- **Second block is a heading, not a callout** — breaking a 50/50 site-wide pattern
- **Leads with an uncertainty ledger**, not a price table
- **One callout in the whole article**, carrying the CERTNORTH CALCULATION
- **No FAQ block.** The GATE was read directly and does not require one
- **No year in the title**, on a page arguing that fixed figures go stale
- All eight proposed H2s checked against the site's 215 existing level-2 headings: **zero
  collisions**
- Content type shifts from DECISION to **RESEARCH**, easing a distribution that sits at
  34% DECISION

URL, slug, `clusterId`, `primaryKeyword` and `publishedAt` all unchanged. All 11 inbound
links continue to resolve.

---

## 7. What needs approval

| # | Decision | Recommendation |
|---|---|---|
| 1 | **Verify the fee at PMI, or publish it labelled unverified?** | **Verify.** This is the number the audit singled out as failing the site's own standard. Ten minutes in a browser fixes it |
| 2 | Drop the FAQ block? | **Yes.** It would restate the body, which is padding. Trade-off: the article loses `FAQPage` structured data, and it would be the site's first article without one |
| 3 | Update `certifications.json`? | **Needs approval — it changes a second live page.** Only after real verification, and `verifiedOn` must be advanced honestly |
| 4 | Fix the membership figure in `is-pmi-membership-worth-it` too? | **Needs approval — second article.** Two pages currently give different numbers for the same fee |
| 5 | Correct the free-PDU framing in `pmp-renewal-pdus`? | **Needs approval — second article.** Only if the 35-Education minimum verifies |
| 6 | Proceed to drafting? | **Yes**, once 1 and 2 are answered |

---

## 8. Risks

| Risk | Mitigation |
|---|---|
| The retake correction rests on an unverified figure | If it does not verify, **cut the section — do not soften it** |
| The 35-PDU Education floor is single-sourced | If it does not verify, state only what `pmp-renewal-pdus` supports — that caps exist |
| Prices go stale again | The fact-check plan sets a six-month cadence; the build already warns at six months |
| The uncertainty angle could read as an excuse | Mitigated by pairing it with the ten-year model — the page proves it did the work anyway |
| Scope creep into five other articles | The consolidation map defines what belongs here and what is linked |

---

## 9. Assessment

**The research is sufficient to proceed to drafting**, provided the article is built
around cost structure and uncertainty rather than a headline price.

**It is not sufficient to publish any specific fee as verified fact.** One human visit to
PMI, logged in from the relevant country, resolves nine of the open items at once — and
would also answer the regional-pricing question that currently prevents the site from
stating any universal number.
