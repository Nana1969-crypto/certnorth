# Global PMP Price Correction — Change Report

**Date:** 2026-09-04
**Phase:** 2 — factual consistency only. No rebuild, no editorial optimisation, no new content.
**Verified values applied:** exam **$405** member / **$655** non-member · membership **$139**/year
**Published:** nothing · **Merged:** nothing · **Deployed:** nothing

---

## 1. Occurrences found

24 across the repository. Full classification in `PMP_GLOBAL_PRICE_AUDIT.md`.

| Class | Meaning | Count |
|---|---|---|
| **A** | Outdated PMP exam fee | 14 |
| **B** | A different fee — renewal, CAPM, PRINCE2 | 5 |
| **C** | Historical record of this correction, in `editorial-os/` | ~20 spans across 6 files |
| **E** | Formatting examples in Editorial OS skills | 2 |
| **F** | Unrelated — image height default, build hash | 2 |

**One location was found that the brief did not list: `pmp-vs-prince2`.** Its comparison
table carried `~$425 member / ~$675 non-member` in the PMP column. The instruction not to
assume the six known locations were exhaustive was correct.

---

## 2. Occurrences corrected

**5 files. 16 individual edits.** Each was an exact-match replacement asserted to occur
exactly once; no global find-and-replace was used anywhere.

### `platform/content/certifications.json` — source of truth

| Field | Before | After |
|---|---|---|
| `examCost` (record `pmp`) | `~$425 member / ~$675 non-member (verify for your country)` | `$405 member / $655 non-member (verify for your country)` |
| `verifiedOn` (record `pmp`) | `2026-07` | `2026-09` |

### `platform/content/articles/is-pmp-worth-it.json`

| Location | Before | After |
|---|---|---|
| `body[3]` | `costs around $425 for PMI members and $675 for non-members` | `costs $405 for PMI members and $655 for non-members` |

The existing caveat — *"prices also vary by country, so confirm the current figure for your
region on PMI's site"* — was **retained unchanged**.

### `platform/content/articles/pmp-vs-capm.json`

| Location | Before | After |
|---|---|---|
| `body[3]` table, PMP column | `~$425 member / ~$675 non-member` | `$405 member / $655 non-member` |
| `body[12]` FAQ | `around $425 … and $675` | `$405 … and $655` |

The CAPM column (`$225 / $300`) was not touched.

### `platform/content/articles/pmp-vs-prince2.json` — not in the briefed list

| Location | Before | After |
|---|---|---|
| `body[5]` table, PMP column | `~$425 member / ~$675 non-member` | `$405 member / $655 non-member` |

The PRINCE2 column (`Varies by region (roughly $600+ in the US)`) was not touched.

### `platform/content/articles/is-pmi-membership-worth-it.json`

Ten edits — the exam fees, the membership price in seven places, and three calculations.

| Location | Before | After |
|---|---|---|
| `dek` | membership `around $150` | `$139` |
| `body[1]` callout | `roughly $150 a year` | `$139 a year` |
| `body[4]` table | `Non-member exam fee ~$675` | `$655` |
| `body[4]` table | `~$150 + ~$425 = ~$575` | `$139 + $405 = $544` |
| `body[4]` table | `Difference ~$100 in your favour` | `$111 in your favour` |
| `body[11]` table | `~$150 per year = ~$450 over 3 years` | `$139 per year = ~$417 over 3 years` |
| `body[12]` | `against roughly $150 a year of cost` | `against $139 a year of cost` |
| `body[19]` FAQ 0 | `Around $150 a year` | `$139 a year` |
| `body[19]` FAQ 1 | `$425 … $675 … about $150 … around $100` | `$405 … $655 … $139 … $111` |
| `body[19]` FAQ 2 | `roughly $450 of membership` | `roughly $417 of membership` |

**The article's editorial thesis was not altered.** Both of its conclusions survive on the
new numbers, and were re-tested:

| Thesis | Test | Holds? |
|---|---|---|
| "Join before the exam — it pays for itself" | $111 net benefit > 0 | **Yes** |
| "The renewal discount alone is not a reason to keep paying" | $90 saved per cycle vs $417 of membership | **Yes** |

### `updatedAt` advanced to `2026-09-04`

On the four articles whose factual content changed: `is-pmp-worth-it`, `pmp-vs-capm`,
`pmp-vs-prince2`, `is-pmi-membership-worth-it`. **Reason documented in the audit §6:**
correcting a published price is a real content revision, which is what the field records.
No `publishedAt` was touched. No date was moved on any article whose content did not change.

---

## 3. Calculations recalculated

Every calculation that depends on the exam fee or the membership price, re-derived and
independently verified:

| # | Calculation | Old | New | Check |
|---|---|---|---|---|
| 1 | Member route: membership + member exam | $150 + $425 = $575 | **$139 + $405 = $544** | ✓ |
| 2 | Net benefit of joining: non-member − member route | $675 − $575 = $100 | **$655 − $544 = $111** | ✓ |
| 3 | Exam-fee gap | $675 − $425 = $250 | **$655 − $405 = $250** | ✓ **unchanged by coincidence** |
| 4 | Membership over one renewal cycle | $150 × 3 = $450 | **$139 × 3 = $417** | ✓ |

**Calculations deliberately not changed**, because they do not depend on the exam fee or the
membership price:

| Calculation | Value | Why unchanged |
|---|---|---|
| Renewal discount | $150 − $60 = $90 per cycle | Renewal fees, unrelated to the exam |
| Renewal discount annualised | $90 ÷ 3 = $30 a year | Same |

**Note on #3.** The $250 gap survived the correction by coincidence — both figures moved by
$20. It was re-derived rather than assumed, and the text stating "$250" is still correct.

---

## 4. Source of truth

`certifications.json` is the single source for certification facts. Its own header states
the intent: *"update a number ONCE and every page follows on the next build."*

**Consumers were measured, not assumed.** All 50 articles were scanned for `certTable`
blocks. **Exactly one consumes the data:**

| Consumer | Block | Certifications | Fields |
|---|---|---|---|
| `best-pm-certifications-beginners` | `body[12]` | `google-pm`, `capm`, `psm`, `csm`, **`pmp`** | `examCost`, `training`, `experience`, `renewal` |

**The source was corrected rather than the generated output patched.**

---

## 5. Generated pages affected

Confirmed in the built output after the correction.

**Now showing the corrected figures — five pages:**

| Page | How it was fixed |
|---|---|
| `/certifications/worth-it/is-pmp-certification-worth-it/` | Article edited |
| `/certifications/compare/pmp-vs-capm/` | Article edited |
| `/certifications/compare/pmp-vs-prince2/` | Article edited |
| `/certifications/guides/is-pmi-membership-worth-it/` | Article edited |
| `/certifications/compare/best-project-management-certifications-for-beginners/` | **Not edited — inherited from `certifications.json`** |

Rendered PMP row on the last of those:

```
PMP | $405 member / $655 non-member (verify for your country) | 35 contact hours required
    | 36 months (bachelor's) or 60 months (secondary) | 60 PDUs every 3 years + $60/$150 fee
```

---

## 6. Remaining occurrences

### In published content — one, and it needs your decision

**`platform/content/articles/pmp-cost.json`** still carries `$425`/`$675` in three places:
its dek, its cost table, and one FAQ answer.

**This was deliberate.** That file is superseded in full by the approved rebuild in
`editorial-os/drafts/pmp-cost-rebuilt.json`, which already carries $405/$655. Patching only
its exam fee would leave the page's three worse problems intact while making it look
corrected: the unsupported `$0–$600` training range, the unsupported `$700 to $2,500` total,
and the **false claim, made three times, that every figure comes from PMI**.

**While it stands, the stale figure appears on three generated pages**, because the dek is
rendered in listings:

- `/certifications/guides/pmp-certification-cost/`
- `/certifications/` — pillar index
- `/authors/certnorth-team/` — author index

**Your options:**

| Option | Effect |
|---|---|
| **A — promote the approved draft** *(recommended)* | Fixes the price and the three other problems in one action |
| **B — patch the price in production now** | Removes the wrong figure from three pages immediately, but leaves the false sourcing claim and both unsupported ranges live |

Say which and it takes one edit either way.

### Elsewhere — legitimate, and deliberately preserved

| Location | Value | Why it stays |
|---|---|---|
| `is-pmi-membership-worth-it` | `$60 instead of $150` | **Renewal fee**, not the exam fee |
| `is-prince2-worth-it` | `~£445 / ~$565` | **PRINCE2 Practitioner** exam |
| `pmp-vs-prince2` | `roughly $600+ in the US` | The **PRINCE2** column of the row we corrected |
| `pmp-vs-capm` | `$225 / $300` | **CAPM** fee |
| `platform/src/blocks.js` | `b.height \|\| 675` | Default image height in pixels — engine code |
| `platform/.build-manifest.json` | `…675` | Build hash fragment |
| `editorial-os/skills/data-analysis`, `source-verification` | `"approximately $425"` | Formatting examples. The Editorial OS is out of scope, and these are examples not claims |
| `editorial-os/research/*`, `editorial-os/reports/*` | ~20 spans | **The audit trail of this correction.** Removing them would destroy the record of what was wrong and why |

**No `$445` remains anywhere in published content.** The only `445` in the repository is
PRINCE2's `~£445`, which is a different currency and a different certification.

---

## 7. Validation

| Check | Result |
|---|---|
| `node src/build.js --force` | ✓ 50 articles, 60 sitemap URLs, quality GATE passed |
| `node src/check.js` | ✓ 61 pages — links intact, alt text, heading order, **JSON-LD valid**, **unique titles**, **WCAG AA contrast in both themes** |
| All content JSON parses | ✓ |
| Second global search for `$425`, `$675`, `$445` | ✓ Only the documented production `pmp-cost` occurrences remain |
| Affected calculations re-derived | ✓ All four verified independently |
| `certTable` propagation | ✓ Confirmed in the built HTML |
| `pmp-cost` draft unchanged | ✓ No reference dependency required touching it |
| No unrelated article modified | ✓ 5 files changed, all listed above |

---

## 8. Production safety

| | |
|---|---|
| Deployed | **No** |
| Merged | **No** |
| Pushed to main | **No** — work is on `claude/content-site-setup-t8lbe5` |
| Published | **No** |
| `platform/src/*` modified | **No** |
| Editorial OS modified | **No** — only two new report files added under `editorial-os/reports/` |
| Approved `pmp-cost` draft modified | **No** |

---

## 9. What this leaves

**Corrected and ready for your review:** the exam fee and membership price across four
articles and the source-of-truth data file, with one further page fixed automatically
through that data file, and every dependent calculation re-derived.

**Open, and requiring one word from you:** whether the production `pmp-cost` article is
fixed by promoting the approved draft, or by a price-only patch in the meantime.
