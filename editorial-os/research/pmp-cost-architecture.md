# Article Architecture — `pmp-cost` (as built)

**Date:** 2026-09-04
**Status:** implemented in `editorial-os/drafts/pmp-cost-rebuilt.json`. Not published.

---

## 1. Identity

| Field | Value | Changed? |
|---|---|---|
| **H1** | What the PMP Costs, and Which Costs PMI Doesn't Set | New |
| **`seo.metaTitle`** | `What the PMP Costs (And Which Costs PMI Doesn't Set)` — **52 chars**, unique site-wide | New |
| **`seo.metaDescription`** | 137 chars, unique | New |
| **`dek`** | 275 chars, answer-first, leads with the verified fees | New |
| **`intent.primaryKeyword`** | `pmp certification cost` | **Unchanged** |
| **URL / slug** | `/certifications/guides/pmp-certification-cost/` | **Unchanged** |
| **`clusterId`** | `cl_guides` | **Unchanged** |
| **`publishedAt`** | `2026-07-25` | **Unchanged** |
| **`updatedAt`** | `2026-09-04` | Set to the real revision date |
| **Content type** | RESEARCH (was DECISION) | Eases a corpus at 34% DECISION |

**Title rationale.** The suggested direction was *"How Much Does the PMP Really Cost in
2026?"* The title chosen instead states the article's actual finding — that PMI sets one
line of the bill — and avoids "2026", which 24 of 50 existing titles already carry and
which dates a page whose own argument is that fixed figures go stale.

---

## 2. Structure as built

24 blocks. **8 authored level-2 headings** (the template adds "Sources and references" and
"Next step" to every article).

| # | Block | Section |
|---|---|---|
| 0 | paragraph | Opening — PMI sets one line of the bill |
| 1–3 | H2 + 2 paragraphs | **What PMI charges, and what it doesn't** — verified fees; the education is priced elsewhere |
| 4–6 | H2 + table + paragraph | **Four kinds of cost, and PMI sets only one** |
| 7–10 | H2 + paragraph + callout + paragraph | **Membership is a $111 question at exam time** |
| 11–13 | H2 + 2 paragraphs | **Sixty PDUs, and why 25 is the number that matters** |
| 14–16 | H2 + paragraph + list | **Money and time are separate budgets** |
| 17–18 | H2 + paragraph | **Why we won't give you a ten-year total** |
| 19–20 | H2 + paragraph | **What changes at the end of 2026** |
| 21–23 | H2 + ordered list + paragraph | **Pricing this for yourself** |

Block inventory: 12 paragraphs · 8 headings · 1 table · 1 callout · 2 lists · **0 FAQ**.

---

## 3. Pattern Guardian — measured against the corpus

| Pattern | Corpus | Draft |
|---|---|---|
| Second block is a callout | **50 / 50** | **Heading** |
| Contains an FAQ block | **50 / 50** | **None** |
| Last block is an FAQ | **50 / 50** | **Paragraph** |
| Callouts per article | 2 to 5 (min 2) | **1** — below the corpus minimum |
| Tables per article | 1 to 3 | 1 |
| Title contains "2026" | 24 / 50 | **No** |
| Shared 3-heading "worth it" spine | 8 articles | Not used |

**Heading collisions:** all 8 checked against the **215 distinct level-2 headings** on the
site — **zero**. Consecutive-pair sequence overlap with any existing article — **none**.

**Verbatim phrasing (6-word spans):**

| Comparison | Before fixes | After fixes |
|---|---|---|
| vs the production `pmp-cost` | 0 | **0** — fully rewritten |
| vs `how-long-to-get-pmp` | 10 | **0** |
| vs `is-pmp-worth-it` | 10 | **0** |
| vs `pmp-vs-capm` | 10 | **0** |
| vs `pmp-eligibility` | 7 | **2** |

**Three Pattern Guardian findings were acted on**, all against the draft itself:

1. **The opening used a house rhetorical formula.** It began *"Most pages about the cost of
   the PMP…"* — the same "most other articles get this wrong" move used by
   `project-manager-salary` and `best-pm-certifications-beginners`, and "Most" already
   opens 4 of 50 articles. Rewritten to open on substance.
2. **The eligibility sentence was verbatim across four articles.** Rephrased to keep the
   36/60-month precision without the shared span.
3. **The 2026 training paragraph restated `pmp-eligibility` almost word for word.**
   Rewritten as a budgeting summary that points to the owning article for the exact wording.

---

## 4. Internal links

**8 links to 7 distinct articles**, each inside a sentence that already raises the subject.
No "related articles" block.

| Target | Placed in | Why there |
|---|---|---|
| `pmp-eligibility` | §What PMI charges; §What changes at the end of 2026 | Owns the CAPM waiver and the exact rule wording |
| `is-pmi-membership-worth-it` | §Membership | Owns overall membership value, which this article deliberately does not answer |
| `pmp-renewal-pdus` | §Sixty PDUs | Owns PDU mechanics and which activities count |
| `pmp-pass-rate` | §Why we won't give you a ten-year total | The evidence for refusing an expected-cost calculation |
| `is-pmp-worth-it` | §Pricing this for yourself | Owns whether to spend at all |
| `pmp-vs-capm` | §Pricing this for yourself | The cheaper credential while qualifying |
| `how-to-prepare-for-pmp-exam` | §Pricing this for yourself | Where the time budget becomes a plan |

**Inbound links unaffected** — URL, slug and primary keyword unchanged, so all 11 continue
to resolve.

---

## 5. Sources

Five, all PMI, all HTTPS. **Two are new** and fix a sourcing gap in the production article,
which published renewal rules while citing neither handbook:

- PMI — Project Management Professional (PMP)
- PMI — Membership
- PMI — How to maintain your certification
- **PMI — Continuing Certification Requirements (CCR) Handbook** *(new)*
- **PMI — PMP Handbook** *(new)*

**Note:** the source schema is `{label, url}` with no date field, so these citations carry
no "as of" date — a site-wide gap affecting ~160 citations. Recorded, not fixed here.

---

## 6. Ownership boundaries respected

`pmp-cost` becomes the reference page for **the economics of getting and keeping the PMP**,
and nothing else.

| Subject | Kept out, and linked to |
|---|---|
| Eligibility pathways | `pmp-eligibility` |
| Exam format and study method | `how-to-prepare-for-pmp-exam` — one line about 180 questions in 240 minutes, in the time budget only |
| Pass rate reasoning | `pmp-pass-rate` — one sentence |
| PDU mechanics and which activities count | `pmp-renewal-pdus` — the composition rule is used, the mechanics are not restated |
| Overall membership value | `is-pmi-membership-worth-it` |
| Whether the PMP is worth having | `is-pmp-worth-it` |

---

## 7. Validation performed

The draft was built and checked in an **isolated copy** of `platform/` in a scratch
directory, with the draft substituted for the production article.
**`platform/content/` was never modified.**

```
node src/build.js --force → ✓ 50 articles, 60 sitemap URLs, GATE passed
node src/check.js         → ✓ 61 pages, links intact, headings ok, JSON-LD valid,
                              unique titles, WCAG AA contrast in both themes
```

Rendered page inspected in Chromium at 375 px: no horizontal overflow, 8 authored H2s
present, 1 table, **0 `<details>` elements** confirming the FAQ removal renders cleanly, all
9 internal links resolving. The single console error is the AdSense script blocked by this
environment's proxy — pre-existing on every page.

**GATE compliance:** metaTitle 52 ≤ 60 and unique · metaDescription 137 ≤ 155 and unique ·
dek 275 ≥ 40 · 8 h2 ≥ 2 · 8 internal links ≥ 1 · 5 sources ≥ 1 · primaryKeyword unchanged
and still unique.
