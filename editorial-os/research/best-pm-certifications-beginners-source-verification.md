# Source Verification — `best-pm-certifications-beginners` (REBUILD 03, route D1)

**Verification date attempted:** September 4, 2026
**Input:** `editorial-os/research/best-pm-certifications-beginners-diagnostic.md` (commit `3d7cada`)
**Phase:** factual verification only. No article written, no draft created, production untouched.

---

## 1. Verification summary

**D1 could not be executed in this environment. Zero primary sources were reached.**

This must be stated before anything else, because every classification below follows from it.

### 1.1 What was attempted

| Organisation | URL | Method | Result |
|---|---|---|---|
| PMI | `https://www.pmi.org/certifications/certified-associate-capm` | WebFetch, then curl | **403 — CONNECT tunnel failed** |
| PMI | `https://www.pmi.org` | curl | **403** |
| PMI | `https://pmi.org` | curl | **403** |
| Coursera / Google | `https://www.coursera.org/professional-certificates/google-project-management` | WebFetch, then curl | **403** |
| Grow with Google | `https://grow.google/certificates/project-management/` | curl | **403** |
| Scrum.org | `https://www.scrum.org/assessments/professional-scrum-master-i-certification` | WebFetch, then curl | **403** |
| Scrum Alliance | `https://www.scrumalliance.org/get-certified/scrum-master-track/certified-scrummaster` | WebFetch, then curl | **403** |
| PeopleCert | `https://www.peoplecert.org/` | curl | **403** |
| U.S. BLS | `https://www.bls.gov/ooh/business-and-financial/project-management-specialists.htm` | WebFetch, then curl | **403** |

### 1.2 Why — and it is not what the earlier dossier implied

The research dossier reported that four issuing-body domains were blocked. That was accurate
but incomplete, and the incomplete version invited a wrong inference — that specific
certification bodies were being refused.

**This session has no general outbound web access at all.** A control test:

```
https://example.com        → 403 CONNECT tunnel failed
https://en.wikipedia.org   → 403 CONNECT tunnel failed
```

Every external host tested returns 403 at the CONNECT stage. The environment's proxy
documentation (`/root/.ccr/README.md`) describes this class explicitly:

> **403 / 407 from the proxy** — The destination host is not allowed by your organization's
> egress policy for this session. **Do not retry or route around it — report the blocked
> host.**

I did not retry beyond establishing the pattern, and did not attempt to route around it.

**Consequence: no environment-side action can complete D1.** This is not a matter of trying
harder or finding a different URL. The seven items require a human with a browser.

### 1.3 Classification totals

| Status | Count | Which |
|---|---|---|
| **VERIFIED** | **0** | — |
| **PARTIALLY VERIFIED** | **0** | — |
| **NOT VERIFIED** | **7 of 7** | all items in §2 |
| **OUTDATED** | 0 confirmed | *cannot be determined without the source; item 2 is a candidate* |
| **CONTRADICTORY** | **1** | item 2 — CAPM renewal cycle (§8.1) |
| **NOT APPLICABLE** | — | noted per field in §2 |

**No number in this file may be treated as verified.** Everything recorded as a CertNorth
value is what the repository currently publishes, with the date the repository claims it was
checked — which is a record of an assertion, not a verification.

### 1.4 What *was* completed, and it is not nothing

D1's premise was that the seven items block drafting. **That is only half true, and
establishing which half is the useful outcome of this phase.**

The claims in the current article divide cleanly:

| Group | Claims | Needs a provider? | Status now |
|---|---|---|---|
| **A — evaluative and market claims** | 6 | **No** | **Resolved. §6 gives a final action for each** |
| **B — factual figures and rules** | 7 | **Yes** | NOT VERIFIED. §2–§5 give the Editor an executable worksheet |

Six of the thirteen problems in this article were never verification problems. They are
unsupported superlatives and claims about employer behaviour that **no source could establish
even if every provider page were reachable** — "most respected credential in the field" has no
possible primary source. Those are settled here, permanently, and do not depend on D1.

§10 states precisely what can and cannot be drafted on that basis.

---

## 2. Credential-by-credential verification

The seven items are carried over from the diagnostic exactly as listed. **The list was not
re-selected.** PRINCE2 appears as a conditional eighth, per the Editor-in-Chief's approval
("PRINCE2 citado conforme o blueprint → APROVADO, condicionado à verificação oficial") — it is
an addition to the approved seven, not a substitution for any of them.

Each entry gives: what CertNorth currently publishes · the exact question for the official
source · the URL to ask it at · status.

---

### 2.1 CAPM — item 1: exam fee

| | |
|---|---|
| **CertNorth currently publishes** | `$225 member / $300 non-member` (`certifications.json`, `verifiedOn: 2026-07`; also article body block 27, `pmp-vs-capm` table and FAQ, `is-capm-worth-it` body and table) |
| **Ask the source** | Current CAPM exam fee for members and non-members. **Also: does PMI show a different fee for the account's country?** The PMP record already carries "(verify for your country)"; the CAPM record does not, and nothing establishes that CAPM pricing is uniform |
| **Where** | `https://www.pmi.org/certifications/certified-associate-capm` and the CAPM Handbook PDF |
| **Record** | value · currency · member/non-member · country the price was shown for · what is included · retake fee if shown · date · URL |
| **Status** | **NOT VERIFIED** |
| **Risk if wrong** | Appears in **four** articles. The identical failure occurred with the PMP fee, which stood at `~$425/~$675` across five files until Phase 2 corrected it on 2026-09-04 |

---

### 2.2 CAPM — item 2: renewal cycle and validity ⚠️ **CONTRADICTORY**

| | |
|---|---|
| **CertNorth currently publishes** | `15 PDUs every 3 years` (`certifications.json`) · *"the credential now requires ongoing renewal, so check PMI for the current maintenance requirement"* (`is-capm-worth-it`) — the site is already hedging here |
| **In circulation elsewhere** | A **5-year** validity period, renewable by 15 PDUs **or** re-examination |
| **The conflict** | Three years vs five years. These are not reconcilable readings of one rule. **One of them is wrong** |
| **Ask the source** | The CAPM's validity period; the renewal requirement; whether re-examination is an alternative to PDUs; whether a renewal fee applies |
| **Where** | `https://www.pmi.org/certifications/certified-associate-capm` and the **CCR Handbook** — the same document that settled the PMP's PDU category limits |
| **Status** | **NOT VERIFIED · CONTRADICTORY.** See §8.1 |
| **Note** | The 5-year figure comes from vendor pages surfaced in search. **It is not evidence and is not preferred over the repository value.** Both are recorded; neither is chosen |

---

### 2.3 Google Project Management Certificate — item 3: price

| | |
|---|---|
| **CertNorth currently publishes** | `~$49/month on Coursera (under $300 total)` (`certifications.json`, `verifiedOn: 2026-07`); *"about $49/month"* (article block 25); *"~$49/month (typically under $300 total)"* (`google-pm-certificate-worth-it`, `capm-vs-google-pm-certificate`) |
| **Ask the source** | The current subscription price; **which country that price is shown for**; whether a free trial applies; whether Coursera Plus is a separate price; whether financial aid is offered |
| **Where** | `https://www.coursera.org/professional-certificates/google-project-management` (Coursera sets the price) and `https://grow.google/certificates/project-management/` |
| **Record** | value · currency · **billing basis — this is a recurring subscription, not a fee** · region · what is included · date · URL |
| **Status** | **NOT VERIFIED** |
| **Known divergence** | Search results returned **$49**, **$51**, and **$62** (Coursera Plus) in a single result set. Not used to verify anything — recorded because it shows the figure is unstable, plan-dependent and region-dependent, and should probably not be published as a single number at all |
| **Editorial note** | Per §4, a subscription price must not be presented in the same column as an exam fee. This is the clearest instance of the category error the rebuild exists to fix |

---

### 2.4 Google Project Management Certificate — item 4: CAPM education credit

| | |
|---|---|
| **CertNorth currently publishes** | *"even counts toward the education requirement for the CAPM"* (article block 25) · *"Counts toward the 23 education hours the CAPM requires"* (`google-pm-certificate-worth-it`) · asserted twice more in `capm-vs-google-pm-certificate` |
| **The sourcing defect** | The claim is cited to **Google/Coursera**. The rule it describes belongs to **PMI**. An organisation cannot be the authority on another body's eligibility criteria — `CLAUDE.md`: *"Never cite a training provider as neutral evidence about its own product."* Google has a direct commercial interest in this claim being believed |
| **Ask the source** | **PMI**, not Google: what satisfies the CAPM's 23 contact hours; whether a Coursera/Google professional certificate qualifies; whether PMI names accepted providers |
| **Where** | `https://www.pmi.org/certifications/certified-associate-capm` and the CAPM Handbook |
| **Status** | **NOT VERIFIED — and mis-sourced regardless of the answer** |
| **Note** | This is load-bearing. It is the basis of the site's "do Google first, then CAPM" recommendation in three articles. If PMI does not confirm it, that recommendation loses its mechanism |

---

### 2.5 Google Project Management Certificate — item 5: duration

| | |
|---|---|
| **CertNorth currently publishes** | *"finishable in under six months"* (article block 25) · *"Google estimates most learners finish in under six months at roughly 10 hours per week"* (`google-pm-certificate-worth-it`) |
| **The defect** | `google-pm-certificate-worth-it` attributes it correctly — *"Google estimates"*. **This article states it flat, as fact.** The same claim, one page apart, at two different evidential standards |
| **Ask the source** | The stated duration and weekly hours, **and whether it is presented as an estimate** |
| **Where** | `https://www.coursera.org/professional-certificates/google-project-management` |
| **Status** | **NOT VERIFIED as fact.** Provider estimate, never independent evidence |
| **Action regardless of verification** | **QUALIFY.** Even if the source confirms the wording, the ceiling is *"Google estimates"* — a provider's completion estimate for its own paid course is marketing about its own product |

---

### 2.6 PSM I — item 6: assessment fee

| | |
|---|---|
| **CertNorth currently publishes** | `~$200 (voucher)` (`certifications.json`, `verifiedOn: 2026-07`) · *"roughly $200"*, *"about $200"*, *"around $200"* (`best-agile-certifications`, three places) |
| **Ask the source** | The current PSM I assessment fee; whether the price is a voucher; whether a retake requires a new voucher; the pass mark; **whether the certification expires** |
| **Where** | `https://www.scrum.org/assessments/professional-scrum-master-i-certification` |
| **Status** | **NOT VERIFIED** |
| **Depends on it** | The article's claim that *"PSM I is the cheapest real certification"* rests on ~$200 vs the CAPM's $225 — **a $25 gap between two figures, neither verified.** See §6, claim C5 |

---

### 2.7 CSM — item 7: cost and renewal

| | |
|---|---|
| **CertNorth currently publishes** | `~$800–$1,500 all-in (course included)` · `Mandatory two-day course` · `Every 2 years (SEUs + fee)` (`certifications.json`) · *"$100 plus 20 hours of learning every two years"* (`best-agile-certifications`) |
| **Ask the source** | Whether the two-day course is mandatory; whether an exam is included; the price range and what sets it; the renewal period; the renewal fee; the SEU requirement |
| **Where** | `https://www.scrumalliance.org/get-certified/scrum-master-track/certified-scrummaster` |
| **Status** | **NOT VERIFIED** |
| **Additional defect — independent of verification** | **The article cites no Scrum Alliance source at all.** Five certifications, three sources, and the CSM has none. This is a sourcing gap the rebuild must close whether or not the figures change |
| **Note** | Price is set largely by independent training partners, so a single range may not be publishable as a provider figure. Record what Scrum Alliance itself states versus what partners charge |

---

### 2.8 PRINCE2 — conditional eighth item

Approved conditionally. **This is an addition to the seven, not a replacement for any of them.**

| | |
|---|---|
| **CertNorth currently publishes** | `PRINCE2 Foundation & Practitioner (7th edition)` · body `PeopleCert` · level `intermediate` · `Varies by region (roughly $600+ in the US)` · `Not required for Foundation` · `None for Foundation` · `Practitioner every 3 years` (`certifications.json`, `verifiedOn: 2026-07`) |
| **Ask the source** | **The current official qualification name** · whether "7th edition" is current · Foundation prerequisites · whether training is mandatory · exam format · price and by which region · validity and renewal for Foundation specifically, separately from Practitioner |
| **Where** | `https://www.peoplecert.org/` |
| **Status** | **NOT VERIFIED** |
| **Naming risk** | Search results asserted a **January 2026 qualification rename** and a pass-mark change. **SECONDARY / SEARCH DISCOVERY ONLY — not used, not relied on.** But it means the site may be publishing a superseded product name, and a rename is exactly the kind of thing that cannot be inferred |
| **Blueprint dependency** | The approved narrow form is one sentence naming PRINCE2 and its position, plus a link. **Even that sentence needs the current name.** Naming a renamed qualification wrongly is worse than the current silence |

---

## 3. Pricing verification

Required fields per the brief. **Nothing in the "verified" columns can be filled from this
environment.** This is the worksheet.

| # | Item | CertNorth value | Currency | Condition | Region | Member / non-member | What's included | Verified value | Date | URL |
|---|---|---|---|---|---|---|---|---|---|---|
| 1 | CAPM exam | $225 / $300 | USD | exam fee | **unstated — assumed US** | yes | exam only | — | — | pmi.org/certifications/certified-associate-capm |
| 3 | Google certificate | ~$49/month, under $300 total | USD | **subscription, recurring** | **unstated — assumed US** | n/a | all course content | — | — | coursera.org/professional-certificates/google-project-management |
| 6 | PSM I | ~$200 | USD | voucher, per attempt | **unstated** | n/a | assessment only, no training | — | — | scrum.org/assessments/professional-scrum-master-i-certification |
| 7 | CSM | ~$800–$1,500 | USD | **course + credential bundled** | **unstated — assumed US** | n/a | mandatory 2-day course | — | — | scrumalliance.org/get-certified/scrum-master-track/certified-scrummaster |
| 8 | PRINCE2 | roughly $600+ in the US | USD | **already flagged region-variable** | US, stated | n/a | unclear — Foundation, Practitioner, or both | — | — | peoplecert.org |

**Rules held.** No currency converted. No price estimated. No figure rounded. No course price
presented as a credential price. No variable price presented as universal.

**Three observations that do not require the sources**, and that the rebuild must act on:

1. **Four of five prices carry no stated region.** Only PRINCE2 and the PMP are marked
   region-variable. There is no basis for assuming the other four are uniform — and PMI's own
   PMP record proves PMI at minimum prices regionally.
2. **The five values are not the same kind of quantity.** A per-attempt exam fee · a recurring
   monthly subscription · a per-attempt voucher · a bundled course-plus-credential range · an
   unclear regional range. **Placing them in one column headed `examCost` is the category
   error the rebuild exists to correct**, and it is visible in the data model itself.
3. **The Google figure may not be publishable as a single number at all.** A subscription's
   total depends on how fast the learner finishes. "Under $300 total" already embeds an
   assumption about the learner's pace.

---

## 4. Eligibility verification

| # | Credential | CertNorth value | Status | Note |
|---|---|---|---|---|
| 1 | CAPM | Secondary diploma + 23 contact hours · **no experience** | **NOT VERIFIED** | Consistent across four articles. Almost certainly right; consistency is not verification |
| 4 | Google → CAPM credit | Google hours count toward the 23 | **NOT VERIFIED · mis-sourced** | §2.4. Must come from PMI |
| 3/5 | Google certificate | No prerequisites | **NOT VERIFIED** | Low risk |
| 6 | PSM I | No prerequisites; training not required | **NOT VERIFIED** | The "training not required" point is load-bearing for the price comparison |
| 7 | CSM | No prerequisites; **training mandatory** | **NOT VERIFIED** | Mandatory training is what makes the price meaningful |
| 8 | PRINCE2 Foundation | None | **NOT VERIFIED** | The basis on which the blueprint calls it beginner-accessible |
| — | PMP | 36 months (bachelor's) / 60 months (secondary) + 35 contact hours | **NOT VERIFIED at source by this project** | Repository-consistent across seven locations. **The Editor-in-Chief verified PMI's fees and PDU rules on 2026-09-04, not the eligibility months** — do not carry over that verification |

**One structural finding, verifiable without any source:** four of the five options require **no
experience**, and the fifth requires three to five years. That is not a spectrum — it is a
binary, and it is the fact that removes the PMP from a beginners' comparison. **The
architecture does not depend on any unverified number.**

---

## 5. Maintenance and renewal verification

| # | Credential | CertNorth value | Status |
|---|---|---|---|
| 2 | CAPM | 15 PDUs every 3 years | **NOT VERIFIED · CONTRADICTORY** — §8.1 |
| 3 | Google certificate | None — does not expire | **NOT VERIFIED** |
| 6 | PSM I | None — never expires | **NOT VERIFIED** |
| 7 | CSM | Every 2 years, SEUs + fee | **NOT VERIFIED** |
| 8 | PRINCE2 | Practitioner every 3 years | **NOT VERIFIED** · Foundation's own validity is **not recorded at all** |
| — | PMP | 60 PDUs / 3 years · ≥35 Education · ≤25 Giving Back · ≤8 Work as a Practitioner | **VERIFIED** — Editor-in-Chief, PMI, 2026-09-04 |
| — | PMP renewal **fee** | `$60/$150` in `certifications.json` | **NOT ESTABLISHED** — explicitly unresolved since Rebuild 01 |

**This section is the most exposed in the file.** The blueprint's Thesis 2 — that the
recurring obligation is the real long-run difference — rests entirely on data of which
**exactly one row is verified, and that row belongs to the credential being removed from the
table.**

The diagnostic anticipated this (§B, "building the article's backbone on the least verified
data on the page is the wrong risk") and demoted Thesis 2 from frame to section. **That
judgment is confirmed by this verification attempt.** The obligation asymmetry can be
*described* qualitatively — some expire, some do not — long before the exact cycles are
confirmed.

---

## 6. Claim verification

Claims carried from the diagnostic §H and the dossier §7.

### 6.1 Group A — resolvable without any provider. **These are final.**

No primary source could settle these, because they are evaluative or concern employer
behaviour that no available source measures. **They do not depend on D1 and are closed.**

| # | Claim | Source | Evidence | Status | Action |
|---|---|---|---|---|---|
| C1 | *"2026 figures, **verified with each provider**"* (table caption) | — | **Contradicted.** `certifications.json` carried `~$425/~$675` for the PMP until Phase 2 corrected it on 2026-09-04. **This verification attempt is itself further evidence: no provider has ever been reached by this project for any of these five records** | **NOT VERIFIED — false as written** | **REMOVE.** Highest priority in the rebuild |
| C2 | *"the **best** first certification is the CAPM or the Google Certificate"* (dek) | none | No criteria stated; contradicted by the article's own four "best for X" headings | OPINION | **REWRITE** |
| C3 | *"the PMP is the **gold standard**"* (dek, H3) | none | Marketing register; `CLAUDE.md` prohibits empty superlatives by name | OPINION | **REMOVE** |
| C4 | *"the **most respected credential** in the field"* | none | Unmeasurable. **No source could establish it** | NOT VERIFIED | **REMOVE** |
| C5 | *"PSM I is the **cheapest real certification**"* | none | "Cheapest" rests on a $25 gap between two unverified figures (§2.6). "**Real**" disqualifies the Google certificate without argument | NOT VERIFIED | **REWRITE** — and note the "real" judgment is the article's own category insight, smuggled in as a dismissal instead of stated as analysis |
| C6 | *"which **recruiters recognize**"* (CAPM) | none | Employer-behaviour claim. Same class as the claims cut from the `is-pmp-worth-it` draft in Rebuild 02 review | NOT VERIFIED | **REMOVE** |
| C7 | *"**best recognized** entry-level credential"* (H3) | none | Comparative recognition claim, unmeasured | NOT VERIFIED | **REMOVE** |
| C8 | *"the **gentlest** on-ramp"* (Google) | none | Subjective, criterion unstated | OPINION | **QUALIFY** — permissible as CertNorth's stated assessment, not as a property of the product |

**Eight claims closed. Six removed or rewritten, two qualified. None required a provider.**

### 6.2 Group B — blocked on D1

| # | Claim | Source cited | Evidence | Status | Action |
|---|---|---|---|---|---|
| C9 | CAPM $225 / $300 | PMI index page (generic) | Not on the cited page | **NOT VERIFIED** | Hold — §10 |
| C10 | CAPM 23 contact hours, no experience | PMI index page (generic) | Not on the cited page | **NOT VERIFIED** | Hold |
| C11 | CAPM renewal cycle | none | **Contradictory** — §8.1 | **CONTRADICTORY** | **Do not state a cycle under either route** |
| C12 | Google ~$49/month | Coursera page | Unreachable; figure unstable across plans and regions | **NOT VERIFIED** | Hold |
| C13 | Google "under six months" | Coursera page | Provider's own estimate | **NOT VERIFIED as fact** | **QUALIFY regardless** — attribute to Google |
| C14 | Google hours count toward CAPM | Coursera page | **Wrong body.** The rule is PMI's | **NOT VERIFIED · mis-sourced** | **QUALIFY or hold** — attribute, never state flat |
| C15 | PSM I ~$200 | Scrum.org page | Unreachable | **NOT VERIFIED** | Hold |
| C16 | CSM 2-day course mandatory, ~$800–$1,500, 2-year renewal | **none cited** | No Scrum Alliance source anywhere in the article | **NOT VERIFIED** | Hold · **add a source regardless** |
| C17 | PRINCE2 name, edition, figures | none in this article | Possible rename in circulation | **NOT VERIFIED** | Hold — name required before even a passing mention |

---

## 7. Evidence chain

The final column is mandatory and is the point of the table.

| # | Claim | Official source | Evidence obtained | Status | Date | **What the source does NOT show** |
|---|---|---|---|---|---|---|
| 1 | CAPM fee $225/$300 | PMI — CAPM page | **none — 403** | NOT VERIFIED | 2026-09-04 | Even if confirmed: not that the price applies outside the US; not what training costs on top; not that the fee is stable |
| 2 | CAPM renewal 15 PDUs / 3 yrs | PMI — CAPM page, CCR Handbook | **none — 403** | CONTRADICTORY | 2026-09-04 | Not what renewal costs in time or money; not how many holders let it lapse |
| 3 | Google ~$49/month | Coursera | **none — 403** | NOT VERIFIED | 2026-09-04 | Not the total a given learner pays — that depends on their pace; not the price in any other country; not whether the price is stable |
| 4 | Google hours → CAPM's 23 | **PMI** (currently cited to Google) | **none — 403** | NOT VERIFIED | 2026-09-04 | Google could not show it even if reached — **it is not PMI**. And confirmation would not show that the route is a good idea, only that it is permitted |
| 5 | Google "under six months" | Coursera / Grow with Google | **none — 403** | NOT VERIFIED | 2026-09-04 | Not how long learners actually take; not the completion rate. A provider's estimate for its own paid course |
| 6 | PSM I ~$200 | Scrum.org | **none — 403** | NOT VERIFIED | 2026-09-04 | Not the cost of preparing, which is the larger variable for self-study; not that it is cheapest |
| 7 | CSM ~$800–$1,500, 2-yr renewal | Scrum Alliance | **none — 403** | NOT VERIFIED | 2026-09-04 | Not what any particular trainer charges — the range is set by partners; not what the credential is worth |
| 8 | PRINCE2 name / edition / fees | PeopleCert | **none — 403** | NOT VERIFIED | 2026-09-04 | Not regional availability; not recognition outside the UK and Europe |
| — | Certification not required for the occupation | U.S. BLS OOH | **none — 403.** Repository record only | NOT VERIFIED at source | 2026-09-04 | **Nothing about which certification**; nothing about any individual employer; nothing about entry-level hiring specifically. **This limit holds regardless of whether the page is ever reached** |

---

## 8. Contradictions

### 8.1 CAPM renewal — three years or five

| Position | Where |
|---|---|
| **15 PDUs every 3 years** | `platform/content/certifications.json`, `verifiedOn: 2026-07` |
| **Valid 5 years, renewable by 15 PDUs or re-examination** | Multiple exam-prep and training pages surfaced in search |
| **"check PMI for the current maintenance requirement"** | `is-capm-worth-it` — the site already declining to commit |

**Not resolved, and deliberately not resolved.** Per the brief: *"Se houver contradição, NÃO
escolha uma versão silenciosamente."*

Both are recorded. **Neither is preferred.** The repository value is not privileged merely for
being ours, and the search value is not privileged for being more recent — it is not evidence
at all. This needs PMI, and it is the **highest-value item on the Editor's worksheet**,
because it is the only one where the site may be publishing something actively wrong rather
than merely unconfirmed.

### 8.2 Google certificate price — three figures

$49 / $51 / $62 (Coursera Plus) across one search result set. Not a contradiction between
official sources — a contradiction among secondary ones, which is why **secondary convergence
was rejected as a method in the first place.** Recorded as evidence that the figure is
plan- and region-dependent, not as a challenge to the repository value.

### 8.3 An internal inconsistency, resolvable now

The Google duration claim is stated as **fact** in this article (*"finishable in under six
months"*) and correctly **attributed** one page away in `google-pm-certificate-worth-it`
(*"Google estimates most learners finish in under six months"*).

**Two evidential standards for one claim, inside one site.** This does not need PMI, Google or
anyone else. **Action: adopt the stricter of the two.** Recorded as fixed in Group A terms
even though the underlying figure sits in Group B.

---

## 9. Remaining unknowns

| # | Unknown | Blocking? |
|---|---|---|
| 1 | Every price in §3 | Blocks stating figures as fact; **does not block the architecture** |
| 2 | The CAPM renewal cycle | **Blocks any statement of a cycle**, under either route |
| 3 | Whether Google hours satisfy PMI's 23 | Blocks a flat statement; the site's three-article "Google then CAPM" recommendation depends on it |
| 4 | PRINCE2's current official name | **Blocks even the one approved sentence** |
| 5 | Whether four of the five prices are region-specific | Blocks presenting any as universal |
| 6 | Whether a CSM exam exists and what it involves | Minor |
| 7 | PMP renewal fee | Unresolved since Rebuild 01. **Out of scope — the PMP is leaving the table** |
| 8 | **How employers treat entry-level certifications** | **EVIDENCE INSUFFICIENT — permanently, for CertNorth** |

### 9.1 On item 8 — the job-market question

The brief allowed a limited, transparent check distinguishing *requirement · preference ·
differentiator · mention*.

**No such check was performed, because none is possible.** The egress block is total; no job
board is reachable. There is no sample, and constructing one from memory or from search
snippets would be fabricating job postings — prohibited by the brief, and by `CLAUDE.md`
absolutely.

**This is not a gap awaiting a better session. It is a finding.** The beginner's central
question — *will this get me hired?* — has no source CertNorth can reach, and the honest
answer available is that **every source that speaks to it is either the issuer or someone
selling training for it.** The blueprint already routes this into a section that says so and
hands the reader a check for their own market (§E, section 9). That section is unaffected by
D1's failure — it never depended on data we do not have.

---

## 10. Drafting constraints

**The central finding of this phase: D1's failure does not block the rebuild. It constrains
it, and the constraints are enumerable.**

### 10.1 What can be drafted now, with no further verification

| Element | Basis |
|---|---|
| **The classification** — course completion · exam credential · bundled-course credential · experience-gated credential | Product *types*, not figures. §2, §4 |
| **The decomposition** — teaching · credential · assessment · recurring obligation | Same |
| **The PMP's removal from the comparison, and why** | The 36/60-month bar; four of five require no experience and the fifth requires years (§4) |
| **The recognition section and the reader's market check** | Depends on the *absence* of evidence, which is established (§9.1) |
| **All eight Group A claim fixes** | §6.1 — closed |
| **The corrected table caption** | Removing a false claim requires no verification |
| **Resolution by goal, with criteria stated** | Qualitative: what you want to do → what kind of product serves it |
| **"Three numbers to check before you pay"** | **Strengthened, not weakened, by this phase** — §10.4 |

**That is the entire architecture in §E of the blueprint.** Not one of its seven sections
depends on a number that is currently unverified.

### 10.2 What must not be drafted

| Prohibited | Because |
|---|---|
| Any price stated as fact | §3 — zero verified |
| The CAPM renewal cycle, in any form | §8.1 — contradictory |
| *"counts toward the CAPM"* stated flat | §2.4 — mis-sourced |
| *"under six months"* stated flat | §2.5 — provider estimate |
| Any "cheapest" / "best" / "most recognised" claim | §6.1 — closed as removals |
| Any figure presented as universal rather than regional | §3, observation 1 |
| Any PRINCE2 sentence naming the qualification | §2.8 — the name itself is unconfirmed |
| Any statement about employer behaviour | §9.1 |

### 10.3 Route decision, returned to the Editor-in-Chief

D1 was chosen and **cannot be completed by me**. Three ways forward:

| | Route | What it needs | Result |
|---|---|---|---|
| **D1-H** | **You run the worksheet** — §2 gives every URL and the exact question | ~20–30 minutes with a browser | The strongest page. Figures stated plainly, `verifiedOn` advances across five records |
| **D2** | **Draft on recorded values** | Nothing | Publishable and honest: every figure carries its date and its status, and §10.4 becomes the reader's instrument |
| **D1-partial** | **Draft the seven sections that need no figures; leave the table pending** | Nothing now, your verification later | Preserves momentum; the table is filled in before publication |

**Recommendation: D1-H if you can spare the half hour**, because item 2 (the CAPM renewal
contradiction) is the one place the site may be publishing something wrong, and only you can
settle it. **Otherwise D1-partial** — it is strictly better than waiting, and the architecture
is already proven independent of the figures.

**D2 remains defensible and remains more honest than the live page**, which asserts
verification that never happened.

### 10.4 The one thing this phase improved

The blueprint's closing section — *"Three numbers to check before you pay"* — was designed as
a reader service. **This verification attempt makes it the most defensible section in the
article**, because CertNorth will be telling readers to verify precisely the figures CertNorth
could not verify itself, and saying so.

That is not a weakness dressed up. A page that says *"here is what we recorded, here is when,
here is what moves, go and check these three"* is doing something no training provider will
ever do — and it is exactly what `CLAUDE.md` means by original value coming from stating a
limitation others hide.

---

## 11. Source register

### 11.1 Primary sources — attempted, September 4, 2026

| Organisation | Page | URL | Method | Result | Would have settled |
|---|---|---|---|---|---|
| PMI | CAPM | `https://www.pmi.org/certifications/certified-associate-capm` | WebFetch + curl | **403** | Items 1, 2, 4 |
| PMI | root | `https://www.pmi.org` · `https://pmi.org` | curl | **403** | — |
| Coursera | Google PM Certificate | `https://www.coursera.org/professional-certificates/google-project-management` | WebFetch + curl | **403** | Items 3, 5 |
| Grow with Google | PM Certificate | `https://grow.google/certificates/project-management/` | curl | **403** | Items 3, 5 |
| Scrum.org | PSM I | `https://www.scrum.org/assessments/professional-scrum-master-i-certification` | WebFetch + curl | **403** | Item 6 |
| Scrum Alliance | CSM | `https://www.scrumalliance.org/get-certified/scrum-master-track/certified-scrummaster` | WebFetch + curl | **403** | Item 7 |
| PeopleCert | root | `https://www.peoplecert.org/` | curl | **403** | Item 8 |
| U.S. BLS | Project Management Specialists, OOH | `https://www.bls.gov/ooh/business-and-financial/project-management-specialists.htm` | WebFetch + curl | **403** | Occupational framing |

**Control tests** — establishing that this is not specific to certification bodies:

| Host | Result |
|---|---|
| `https://example.com` | **403 CONNECT tunnel failed** |
| `https://en.wikipedia.org` | **403 CONNECT tunnel failed** |

**Primary sources successfully consulted: 0 of 8.**

### 11.2 Secondary material — recorded, not used

No web search was run in this phase. The three searches from the research phase are recorded
in the dossier §18.2 and were used only to surface the contradiction in §8.1 and the price
divergence in §8.2 — never to verify. **No claim in this file rests on any of them.**

### 11.3 Repository sources — read directly

`platform/content/certifications.json` · `platform/content/articles/best-pm-certifications-beginners.json` ·
`is-capm-worth-it` · `capm-vs-google-pm-certificate` · `google-pm-certificate-worth-it` ·
`pmp-vs-capm` · `best-agile-certifications` ·
`editorial-os/research/best-pm-certifications-beginners-diagnostic.md` ·
`editorial-os/research/best-pm-certifications-beginners-research-dossier.md` ·
`editorial-os/reports/PMP_GLOBAL_PRICE_CORRECTION_REPORT.md` · `CLAUDE.md`

### 11.4 Verified figures available to this rebuild

| Item | Value | Verified by | Date |
|---|---|---|---|
| PMP exam | $405 member / $655 non-member | Editor-in-Chief, at PMI | 2026-09-04 |
| PMI membership | $139 / year | Editor-in-Chief, at PMI | 2026-09-04 |
| PMP PDU rules | 60 / 3 yrs · ≥35 Education · ≤25 Giving Back · ≤8 Work as a Practitioner | Editor-in-Chief, at PMI | 2026-09-04 |
| PMP renewal fee | **NOT ESTABLISHED** | — | — |

**All four concern the PMP, which the approved architecture removes from the comparison. In
practical terms, the rebuild has zero verified figures for the credentials it will actually
compare** — and that is the fact §10 is built to handle.

### 11.5 No ranking has been produced

Per the approved principle: **"Not the same kind of thing" must not become "therefore this is
the best one."**

Nothing in this file ranks these credentials. §4's finding — four require no experience, one
requires years — is a **classification**, not an ordering, and no price, difficulty or
recognition difference has been converted into a verdict. The eight Group A actions in §6.1
**remove** ranking language; they do not replace it with better-sourced ranking language.

---

**Production untouched.** `platform/content/articles/best-pm-certifications-beginners.json`
was read and not modified. No other article modified · no `platform/src/*` modified · no
infrastructure, Actions, Cloudflare, sitemap, canonical, robots or AdSense configuration
touched · nothing drafted, published, merged or deployed. One file added: this one.
