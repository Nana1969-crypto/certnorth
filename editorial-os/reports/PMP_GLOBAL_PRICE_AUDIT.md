# Global PMP Price Audit

**Date:** 2026-09-04
**Scope:** entire repository — every file, not only the six briefed locations
**Method:** numeric search for `425`, `675`, `445` plus contextual search for PMP exam fee,
member/non-member exam, membership discount, PMP certification cost
**Verified values in force:** exam **$405** member / **$655** non-member · membership
**$139**/year · difference **$250**

---

## 1. Contextual classification key

| Code | Meaning |
|---|---|
| **A** | PMP exam fee — outdated, must change |
| **B** | Another fee entirely — must not change |
| **C** | Historical record of the correction itself — must not change |
| **D** | Illustrative calculation depending on the exam fee |
| **E** | Citation or formatting example |
| **F** | Unrelated content |

---

## 2. Occurrences in published site content — `platform/content/`

| # | File | Article / page | Old value | Context | Class | Change? |
|---|---|---|---|---|---|---|
| 1 | `certifications.json` | **source of truth**, record `pmp` | `~$425 member / ~$675 non-member (verify for your country)` | `examCost` field | **A** | **Yes — done** |
| 2 | `certifications.json` | record `pmp` | `verifiedOn: 2026-07` | verification date | **A** | **Yes — done**, see §5 |
| 3 | `articles/is-pmp-worth-it.json` | Is the PMP Worth It | `around $425 … and $675` | `body[3]` paragraph | **A** | **Yes — done** |
| 4 | `articles/pmp-vs-capm.json` | PMP vs CAPM | `~$425 member / ~$675 non-member` | `body[3]` table, PMP column | **A** | **Yes — done** |
| 5 | `articles/pmp-vs-capm.json` | PMP vs CAPM | `around $425 … and $675` | `body[12]` FAQ | **A** | **Yes — done** |
| 6 | **`articles/pmp-vs-prince2.json`** | PMP vs PRINCE2 | `~$425 member / ~$675 non-member` | `body[5]` table, PMP column | **A** | **Yes — done. NOT in the briefed list** |
| 7 | `articles/is-pmi-membership-worth-it.json` | Is PMI Membership Worth It | `~$675` | `body[4]` table | **A** | **Yes — done** |
| 8 | same | same | `~$150 + ~$425 = ~$575` | `body[4]` table | **A + D** | **Yes — recalculated** |
| 9 | same | same | `~$100 in your favour` | `body[4]` table | **D** | **Yes — recalculated to $111** |
| 10 | same | same | `$425 … $675 … $150 … $100` | `body[19]` FAQ | **A + D** | **Yes — recalculated** |
| 11 | same | same | membership `~$150` in dek, callout, tables and two FAQs | 7 places | **A** | **Yes — all to $139** |
| 12 | same | same | `~$150 per year = ~$450 over 3 years` | `body[11]` table | **D** | **Yes — recalculated to $417** |
| 13 | same | same | `roughly $450 of membership` | `body[19]` FAQ | **D** | **Yes — recalculated to $417** |
| 14 | **`articles/pmp-cost.json`** | **PMP Certification Cost — production** | `$425` ×3, `$675` ×3 | dek, `body[3]` table, `body[12]` FAQ | **A** | **NO — see §4. Requires your decision** |

## 3. Occurrences correctly left alone

| # | File | Value | Context | Class | Why untouched |
|---|---|---|---|---|---|
| 15 | `articles/is-pmi-membership-worth-it.json` | `about $60 instead of $150` | **Certification renewal fee**, not membership or exam | **B** | A different fee. Changing it would introduce an error |
| 16 | same | `~$90 once every 3 years` · `$30 a year` | Renewal-discount arithmetic ($150 − $60) | **B** | Does not depend on the exam fee. Verified still correct |
| 17 | `articles/is-prince2-worth-it.json` | `~£445 / ~$565` | **PRINCE2 Practitioner** exam | **B** | Different certification, different body |
| 18 | `articles/pmp-vs-prince2.json` | `roughly $600+ in the US` | **PRINCE2** column of the same row we corrected | **B** | Only the PMP column was changed |
| 19 | `articles/pmp-vs-capm.json` | `$225 member / $300 non-member` | **CAPM** fee | **B** | Unaffected |
| 20 | `platform/src/blocks.js:80` | `b.height \|\| 675` | Default image height in pixels | **F** | Engine code, and not a price |
| 21 | `platform/.build-manifest.json` | `3bf9fed91090b675` | Build hash fragment | **F** | Generated artefact |
| 22 | `editorial-os/skills/data-analysis/SKILL.md` | `"approximately $425"` | Formatting example for rounding | **E** | Editorial OS — explicitly out of scope, and it is an example not a claim |
| 23 | `editorial-os/skills/source-verification/SKILL.md` | `"approximately $425" → "$425"` | Formatting example | **E** | Same |
| 24 | `editorial-os/research/*.md`, `editorial-os/reports/*.md` | `$425`, `$675`, `$445` in ~20 places | The audit trail of this very correction | **C** | Deleting these would destroy the record of what was wrong and why |

---

## 4. The one occurrence not corrected, and why

**`platform/content/articles/pmp-cost.json` — the production article.**

It still carries `$425` and `$675` in three places. **This was a deliberate decision, not an
oversight**, and it needs yours.

**Why it was not patched:** that file is superseded in full by the approved rebuild in
`editorial-os/drafts/pmp-cost-rebuilt.json`, which already carries $405/$655. Patching only
its exam fee would leave the page's three worse problems intact while making it *look*
corrected:

- the unsupported training range `$0–$600 depending on provider`
- the unsupported all-in range `$700 to $2,500`
- the **false claim, stated three times, that every figure comes from PMI**

A page that quotes the right exam fee while still claiming a sourcing standard it does not
meet is arguably worse than one that is visibly out of date.

**Downstream effect while it stands.** The stale dek propagates to **three generated
pages**, not one:

| Generated page | Why |
|---|---|
| `/certifications/guides/pmp-certification-cost/` | The article itself |
| `/certifications/` | Pillar index — renders the article dek |
| `/authors/certnorth-team/` | Author index — renders the article dek |

**Two ways to close it, both yours to choose:**

| Option | Effect |
|---|---|
| **A — promote the approved draft** *(recommended)* | Fixes the price and the three other problems in one action. One approval, not two |
| **B — patch the price in production now** | Removes the wrong figure from three pages immediately, but leaves the false sourcing claim and both unsupported ranges live until the draft is promoted |

---

## 5. `certifications.json` — the source of truth

**Role.** `certifications.json` is the single source for certification facts. The comment at
the top of the file states the intent: *"update a number ONCE and every page follows on the
next build."*

**Consumers, measured rather than assumed.** Every article was scanned for `certTable`
blocks. **Exactly one article consumes it:**

| Consumer | Block | Certifications pulled | Fields pulled |
|---|---|---|---|
| `best-pm-certifications-beginners` | `body[12]` | `google-pm`, `capm`, `psm`, `csm`, **`pmp`** | `examCost`, `training`, `experience`, `renewal` |

**Result.** Correcting the `pmp` record fixed `best-pm-certifications-beginners`
**without editing that article at all.** Confirmed in the built output:

```
PMP row → $405 member / $655 non-member (verify for your country)
```

**`verifiedOn` was advanced from `2026-07` to `2026-09`.** This is not a cosmetic refresh:
a real verification took place at PMI in September, and the field exists to record when a
value was last checked. Leaving it at `2026-07` would have misstated when the current
figure was confirmed. The build's six-month staleness warning now runs from the correct
date.

---

## 6. Article dates

`updatedAt` was advanced to `2026-09-04` on the four articles whose factual content changed:
`is-pmp-worth-it`, `pmp-vs-capm`, `pmp-vs-prince2`, `is-pmi-membership-worth-it`.

**Reason, documented as required.** `CLAUDE.md` prohibits cosmetic date changes, and the
site's own editorial policy promises *"we never bump a date without actually revising the
content."* Correcting a published price is a real revision of factual content — precisely
what the field is for. No `publishedAt` was touched, and no date was advanced on any article
whose content did not change.

---

## 7. Summary

| | Count |
|---|---|
| Occurrences found across the repository | 24 |
| Classified **A** (outdated PMP exam fee) | 14 |
| **Corrected** | **13** |
| **Deliberately not corrected** (production `pmp-cost`, pending draft promotion) | **1** |
| Left alone as another fee, example, historical record or unrelated | 10 |
| Locations found that were **not** in the briefed list | **1** — `pmp-vs-prince2` |
| Articles edited | 4 |
| Data files edited | 1 |
| Articles fixed **without being edited**, via the source of truth | 1 |
