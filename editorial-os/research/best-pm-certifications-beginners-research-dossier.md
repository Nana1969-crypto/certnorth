# Research Dossier — `best-pm-certifications-beginners` (REBUILD 03)

**Date:** 2026-09-04
**Article:** `best-pm-certifications-beginners` ·
`/certifications/compare/best-project-management-certifications-for-beginners/`
**Phase:** research and diagnosis only. Nothing drafted, nothing modified in production,
nothing published.
**Branch:** `claude/content-site-setup-t8lbe5` · HEAD `8d9e691` · tree clean at start.

**Evidence labels used throughout** (the taxonomy established in Rebuild 01):

| Label | Meaning |
|---|---|
| **VERIFIED FROM CERTNORTH REPOSITORY** | Measured directly in the files. Certain about what the site says; says nothing about whether the site is right. |
| **PRIMARY-SOURCE VERIFICATION REQUIRED** | A factual claim that only the issuing body can settle, and which this environment cannot reach. |
| **SECONDARY / SEARCH DISCOVERY ONLY** | Surfaced by web search. **Not evidence.** Recorded to show what exists and where it disagrees, never to establish a fact. |
| **CERTNORTH CALCULATION** | Arithmetic performed here, with the inputs shown. |
| **EDITORIAL INFERENCE** | Judgment. Argued, not measured. |

---

## 1. Executive summary

The article is not badly written and it is not factually reckless. Its problem is more
fundamental than either: **its premise does not survive contact with its own contents.**

It promises a ranking of the best project management certifications for beginners. It then
does four things that contradict that promise:

1. It ranks five items that are **not the same kind of thing** — a course-completion
   certificate, two exam credentials with no experience bar, a credential whose price is
   mostly a mandatory course, and a credential beginners are barred from taking.
2. It includes the **PMP**, states in the same breath that it "requires substantial
   documented experience, so most beginners can't take it yet", and then puts it in the
   beginners' comparison table anyway.
3. It gives four separate "best for X" verdicts, which is an admission that there is no
   single best — while the title, dek, meta description and opening callout all promise
   exactly that.
4. It states **no criteria**. Nothing in the article explains what "best" is being measured
   against, so the ranking cannot be checked, argued with, or applied by a reader whose
   situation differs.

Three further findings matter as much:

- **It is a hub in the link graph and a stub in the content.** 20 inbound internal links —
  joint second-most-linked page on the site — carrying **622 words**. The two pages tied
  with or above it carry 1,746 and 636 words. It is also the **only** article on the site
  that consumes `certifications.json`, which makes it the site's certification data hub by
  construction.
- **It repeats the sourcing failure that Rebuild 01 was created to fix.** Its comparison
  table is captioned *"2026 figures, verified with each provider"*. That is a claim about
  CertNorth's own verification process, and it is not supported — the same data file was
  carrying a wrong PMP exam fee at the time, which Phase 2 corrected on 2026-09-04. This is
  the third instance of the same failure mode (`pmp-cost`, `is-pmp-worth-it`, this).
- **PRINCE2 is missing, and its absence is unexplained.** By the article's own working
  criterion — no experience required — PRINCE2 Foundation qualifies. The site holds two
  PRINCE2 articles and a PRINCE2 record in `certifications.json`. The omission is invisible
  to the reader and makes an implicitly US-centric list look like a global one.

**Recommendation: REBUILD WITH MAJOR RESTRUCTURE.** The reader intent is real, the internal
authority is real, and the page is worth having. The architecture is wrong, the promise in
the title is unsupportable as written, and the comparison compares incommensurable things.
Full reasoning in §16.

**External primary-source research was attempted and failed.** All four issuing-body domains
are blocked by this environment's egress proxy (§5). No claim in this dossier is upgraded
on search-result evidence.

---

## 2. Current article audit

Read in full from `platform/content/articles/best-pm-certifications-beginners.json`.
Nothing was modified.

### 2.1 Metadata

| Field | Value |
|---|---|
| `id` | `best-pm-certifications-beginners` |
| `slug` | `best-project-management-certifications-for-beginners` |
| `clusterId` | `cl_compare` |
| **H1 / `title`** | Best Project Management Certifications for Beginners (2026) |
| `seo.metaTitle` | Best PM Certifications for Beginners (2026) — 41 chars |
| `seo.metaDescription` | "An honest, vendor-neutral ranking of beginner project management certifications — real costs, requirements, and which one to pick for your situation." — 148 chars |
| `intent.primaryKeyword` | `best project management certifications for beginners` |
| `authorId` | `author_team` |
| `publishedAt` | 2026-07-25 |
| `updatedAt` | **2026-07-25 — never revised since publication** |
| Body words | **622** |
| Blocks | **18** |
| Sources | **3** |
| Content type | COMPARISON (per `content-types.yaml` definitions) |

**Label: VERIFIED FROM CERTNORTH REPOSITORY.**

### 2.2 dek

> "For most beginners the best first certification is the CAPM or the Google Project
> Management Certificate; the PMP is the gold standard but requires experience you probably
> don't have yet."

Two unsupported evaluative claims in one sentence — *"the best first certification is"* and
*"the PMP is the gold standard"*. Analysed in §7.

### 2.3 Opening

> "Most 'best project management certification' articles are written by the companies selling
> the training. This one isn't — so it can tell you the honest answer, which is that the right
> first certification depends on whether you already have project experience and what kind of
> work you want."

This is the article's strongest paragraph and it contains the seed of the rebuild: it says
plainly that the answer **depends**. The rest of the article then delivers a ranking anyway.
The independence claim itself is legitimate and verifiable — CertNorth sells nothing, per
`CLAUDE.md` — and it is the only genuine differentiator the page currently asserts.

### 2.4 Full block sequence

```
0  paragraph      intro
1  callout(tip)   "Quick answer: …"
2  H2             The honest shortlist
3  H3             Google Project Management Certificate — best for total beginners
4  paragraph
5  H3             CAPM — best recognized entry-level credential
6  paragraph
7  H3             Scrum (PSM I or CSM) — best for agile and software teams
8  paragraph
9  H3             PMP — the gold standard, but not a beginner cert
10 paragraph
11 H2             Side-by-side comparison
12 certTable      google-pm, capm, psm, csm, pmp
13 callout(warn)  "Watch the total cost, not just the exam fee…"
14 H2             How to choose in five minutes
15 list(ordered)  5 items
16 paragraph      pointer to how-to-become-project-manager
17 faq            3 questions
```

**3 H2 · 4 H3 · 2 callouts · 1 certTable · 1 ordered list · 1 FAQ · 0 plain tables.**
The corpus median is 5 H2s; this article has 3.

### 2.5 Callouts, verbatim

**Callout 1 — `tip`, block 1:**
> "Quick answer: no experience yet? Start with the Google Project Management Certificate or
> the CAPM. Work in software or agile teams? Start with a Scrum certification. Already have
> years of project experience? Skip straight to the PMP."

**Callout 2 — `warn`, block 13:**
> "Watch the total cost, not just the exam fee. The CSM looks expensive because a two-day
> course is mandatory; the PSM I looks cheap because you can self-study and just pay for the
> exam. The sticker price rarely tells the whole story."

**Callout 2 is the single most useful sentence in the article** and it is buried below the
table it corrects. It contains the beginning of the distinction the rebuild should be built
on — that these products bundle different things — and the article never develops it.

### 2.6 The table

The only table is a `certTable`, which renders from `certifications.json` rather than from
literal content:

```json
{ "type": "certTable",
  "caption": "Beginner-friendly project management certifications compared (2026 figures, verified with each provider).",
  "certs": ["google-pm", "capm", "psm", "csm", "pmp"],
  "fields": ["examCost", "training", "experience", "renewal"] }
```

Rendered values, read from `platform/content/certifications.json` as it stands today:

| Cert | `examCost` | `training` | `experience` | `renewal` | `verifiedOn` |
|---|---|---|---|---|---|
| Google PM Certificate | ~$49/month on Coursera (under $300 total) | Included — self-paced course | None | None — does not expire | 2026-07 |
| CAPM | $225 member / $300 non-member | 23 contact hours required | None — secondary diploma only | 15 PDUs every 3 years | 2026-07 |
| PSM I | ~$200 (voucher) | None required — self-study allowed | None | None — never expires | 2026-07 |
| CSM | ~$800–$1,500 all-in (course included) | Mandatory two-day course | None | Every 2 years (SEUs + fee) | 2026-07 |
| PMP | $405 member / $655 non-member (verify for your country) | 35 contact hours required | 36 months (bachelor's) or 60 months (secondary) | 60 PDUs every 3 years + $60/$150 fee | 2026-09 |

**Label: VERIFIED FROM CERTNORTH REPOSITORY** (this is what the site publishes, not a
statement that the figures are right).

### 2.7 The list

Block 15, "How to choose in five minutes", five ordered items:

1. No experience and unsure of your niche? Google Certificate or CAPM.
2. Targeting software / agile roles? PSM I (self-funded) or CSM (if your employer pays).
3. Already leading projects for years? Go straight for the PMP.
4. On a tight budget? PSM I is the cheapest real certification if you self-study.
5. Whatever you pick, check the current fee on the provider's official site before you pay.

Items 1–3 restate callout 1 almost exactly. **The article gives the same answer three
times** — in the dek, in the opening callout, and in this list — with no added information
on the second and third pass. That is 100+ words of the 622 spent on repetition.

**Label: VERIFIED FROM CERTNORTH REPOSITORY + EDITORIAL INFERENCE.**

### 2.8 FAQ

Three questions: *which is best for beginners with no experience* · *CAPM or PMP first* ·
*is Scrum better than PMP for beginners*. All three are answered identically in the body
above. The FAQ adds nothing but a fourth restatement and three internal links.

### 2.9 Internal links

Outbound, 7 links to 5 distinct articles: `google-pm-certificate-worth-it` (×2),
`psm-vs-csm`, `is-pmp-worth-it`, `pmp-vs-capm` (×2), `how-to-become-project-manager`.

Inbound: **20 links from 17 distinct articles** — `agile-vs-waterfall`,
`best-agile-certifications`, `capm-vs-google-pm-certificate`,
`do-you-need-certification-project-manager`, `google-pm-certificate-worth-it`,
`how-to-become-project-coordinator`, `how-to-become-project-manager`,
`how-to-become-scrum-master`, `is-capm-worth-it`, `is-csm-worth-it`, `is-pmp-worth-it`,
`is-prince2-worth-it`, `is-psm-worth-it`, `pmp-eligibility`, `pmp-vs-prince2`,
`project-manager-salary`, `psm-vs-csm`.

### 2.10 The link-authority asymmetry

| Rank | Article | Inbound | Words |
|---|---|---|---|
| 1 | `is-pmp-worth-it` | 21 | 1,746 |
| 2= | `how-to-become-project-manager` | 20 | 636 |
| **2=** | **`best-pm-certifications-beginners`** | **20** | **622** |
| 4 | `pmp-eligibility` | 18 | 609 |
| 5= | `psm-vs-csm` | 17 | 518 |
| 5= | `project-manager-salary` | 17 | 570 |

**Label: CERTNORTH CALCULATION** (link graph extracted programmatically from all 50 article
JSON files; word counts measured with a single consistent prose extractor that includes
headings, list items, table cells, captions, FAQ text and link anchor text).

The site directs a fifth of its internal link equity into a page that has not been revised
since the day it was published and is thinner than the average article it links out to.

### 2.11 Sources

Three, for claims about **five** certifications:

| # | Source | Covers |
|---|---|---|
| 1 | PMI — Certifications (index page) | CAPM, PMP — generically |
| 2 | Google Project Management Professional Certificate — Coursera | Google certificate |
| 3 | Scrum.org — Professional Scrum Master (PSM I) | PSM I |

**No source for the CSM.** No source for the PMP specifically. No occupational or labour-
market source of any kind — no BLS, no PMI salary survey, nothing. The article makes claims
about employer recognition and career value with no source that speaks to either.

Sibling comparison: `best-agile-certifications` cites **7** sources for the same job.

**Label: VERIFIED FROM CERTNORTH REPOSITORY.**

---

## 3. Search intent

### 3.1 What the keyword implies

`best project management certifications for beginners` is a **commercial-investigation**
query. The searcher has not decided anything. They are trying to work out what the options
are, whether any of them are open to them, and what a reasonable first purchase looks like.

### 3.2 What the searcher probably does not know

This is the substantive point, and it changes the architecture. A person typing this query
very likely does **not** yet know:

- that "certification" covers at least two different products — a **course you complete** and
  an **exam you pass** — which cost different amounts and mean different things;
- that the most famous credential in the field (PMP) is **closed to them** until they have
  three to five years of documented experience;
- that some credentials **expire and must be re-earned**, and some never expire;
- that the mandatory-course credentials are expensive because of the **course**, not because
  the credential is worth more;
- that Scrum credentials are for a **different role**, not a cheaper version of the same one.

Every one of those is answerable from `certifications.json` and the repository. **None of
them is currently stated as such.** The article assumes the reader already understands the
category system and just needs a ranking within it.

**Label: EDITORIAL INFERENCE**, argued from the data the site already holds.

### 3.3 Secondary intents the page should serve

- *Can I get a certification with no experience?* — yes for four of the five; the article
  says so only inside table cells.
- *Which one is cheapest?* — asked and answered, but with an unsupported superlative (§7).
- *Will it get me a job?* — asked constantly, and the article does not address it at all.
- *Should I get a certification or experience first?* — owned by
  `do-you-need-certification-project-manager` and `how-to-become-project-manager`; this page
  does not link to the first of those, which is the strongest answer the site has.
- *Which is best in my country?* — never addressed. See §4.4.

### 3.4 Does the article deliver on its title?

**Partially, and it undercuts itself.** The title promises a ranking; the body says the
answer depends; the callout then delivers a ranking with no criteria. A reader who does not
fit one of the three scenarios in the callout is left without a method.

---

## 4. Certification landscape

### 4.1 The category error — this is the central finding

Brief §6 asked for six categories to be separated explicitly. Applying them to the five
items the article compares in a single table:

| Item | Professional certification? | Course completion? | Training included? | Exam-based? | Requires experience? |
|---|---|---|---|---|---|
| **Google PM Certificate** | **No** | **Yes** | Yes — it *is* the training | No proctored exam | No |
| **CAPM** | Yes | No | No — 23 hours bought separately | Yes, proctored | **No** |
| **PSM I** | Yes | No | No — self-study permitted | Yes | No |
| **CSM** | Yes | No | **Yes — mandatory 2-day course** | Yes (light) | No |
| **PMP** | Yes | No | No — 35 hours bought separately | Yes, proctored | **Yes — 36 or 60 months** |

The rows are drawn from `certifications.json`; the classification is CertNorth's.
**Label: VERIFIED FROM CERTNORTH REPOSITORY (data) + EDITORIAL INFERENCE (classification).**

Read down the columns and the comparison collapses. The table's `examCost` column puts
"~$49/month on Coursera" beside "$405 member / $655 non-member" beside "~$800–$1,500 all-in
(course included)". Those three numbers measure three different things: a **subscription for
teaching**, a **fee to sit an exam**, and a **bundled course-plus-credential price**. Placing
them in one column labelled *Exam cost* invites a comparison that is not valid, and the
article's own warn callout at block 13 says as much four blocks later.

The article does notice the distinction elsewhere on the site —
`capm-vs-google-pm-certificate` states it cleanly: *"One proves you studied; the other is a
credential you hold."* **That sentence is the thesis this article needs and does not have.**

### 4.2 The PMP problem

The PMP is in the shortlist, in the H3s, and in the comparison table of an article about
**beginner** certifications, while the article itself says beginners cannot take it.

Two defensible treatments exist:
- **(a)** Remove it from the comparison and explain the exclusion — turning the omission into
  information: *here is the famous one, here is why it is not on this list, here is what to
  do instead.*
- **(b)** Keep it as an explicit destination rather than an option, visually separated from
  the things a beginner can actually buy today.

The current treatment is neither: it is listed as a fourth option with a "best for" framing
("the gold standard") and then contradicted in the same paragraph.

### 4.3 PRINCE2 — the unexplained absence

`certifications.json` holds a PRINCE2 record: level `intermediate`, training *"Not required
for Foundation"*, experience *"None for Foundation"*. **By the article's own operative
criterion — accessible without experience — PRINCE2 Foundation belongs in this comparison.**

The site has two PRINCE2 articles (`is-prince2-worth-it`, `pmp-vs-prince2`), and
`is-prince2-worth-it` links *into* this article. So the site tells readers this page ranks
the beginner options, and the page silently omits the one credential most likely to matter
to a reader outside the United States.

**Whether PRINCE2 should be added is a judgment for the Editor-in-Chief.** What is not
defensible is omitting it without a word.

### 4.4 The article is US-centric and does not say so

Every price is in US dollars. Coursera pricing is quoted at the US rate. PMI dominates the
list. `certifications.json` itself flags the problem in the PMP row — *"(verify for your
country)"* — and the article never surfaces it. `CLAUDE.md` requires exactly this care:
*"PMI shows different fees depending on the account's country, so a US dollar figure is not
universal."*

**Minimum fix: state the scope.** Better fix: make market a decision input, since it is one
of the few inputs that genuinely changes the answer.

### 4.5 Should other certifications be added?

**No.** Brief §5 warns against turning the page into a catalogue. PMI-ACP, SAFe, CSPO, PSPO
and ICP-ACC are all covered by `best-agile-certifications`, which does that job well at 1,078
words and 7 sources. Adding them here would create a second agile catalogue and cannibalise a
stronger page. PRINCE2 is the only candidate for addition, and only because it is the one
non-agile, non-PMI beginner-accessible credential the site already covers.

---

## 5. Primary-source research — attempted and unavailable

**This must be stated plainly, as it was in Rebuilds 01 and 02.**

The research protocol requires verification at the issuing body. Four fetches were attempted
on 2026-09-04:

| Target | Purpose | Result |
|---|---|---|
| `https://www.pmi.org/certifications/certified-associate-capm` | CAPM fee, contact hours, renewal cycle | **EGRESS_BLOCKED** |
| `https://www.coursera.org/professional-certificates/google-project-management` | Google certificate price, duration, what it confers | **EGRESS_BLOCKED** |
| `https://www.scrum.org/assessments/professional-scrum-master-i-certification` | PSM I fee, pass mark, expiry | **EGRESS_BLOCKED** |
| `https://www.bls.gov/ooh/business-and-financial/project-management-specialists.htm` | Occupational entry requirements and certification language | **EGRESS_BLOCKED** |

All four returned the environment's egress-proxy block. **Zero primary sources were reached
in this phase.** Scrum Alliance and PeopleCert were not attempted after the pattern was
established across four independent domains.

**Consequence:** no figure in the current article can be confirmed or refuted here. Every
price, hour count, renewal cycle and eligibility rule in §2.6 carries the status
**PRIMARY-SOURCE VERIFICATION REQUIRED**, except the PMP exam fee, which the Editor-in-Chief
verified directly at PMI on 2026-09-04 during Phase 2.

### 5.1 What search returned, and why it changes nothing

Three searches were run to establish **what exists**, not what is true. Per the standing
protocol correction — *"Search snippets are NOT evidence. Multiple commercial sites repeating
the same number are NOT independent verification"* — none of the following is used to
support any claim.

| Query | What the results were | Assessment |
|---|---|---|
| CAPM fee / contact hours / eligibility 2026 | Eight results, **all** exam-prep vendors and training blogs (rosemet.com, learnersink.com, projeric.com, capmquiz.com, flashgenius.net, spoto…). Zero pmi.org results. | **SECONDARY / SEARCH DISCOVERY ONLY.** Cannot verify. |
| Google PM Certificate cost / duration 2026 | Snippets stated **$49/month**, **$51/month**, and **$62/month via Coursera Plus** — three different prices in one result set. | **The secondary layer does not even agree with itself.** This is the clearest possible demonstration of why convergence-as-evidence was rejected. |
| PRINCE2 7 Foundation requirements 2026 | Mostly training providers. One peoplecert.org URL surfaced but **could not be fetched**. Snippets asserted a January 2026 qualification rename and a pass-mark change. | **SECONDARY / SEARCH DISCOVERY ONLY.** Flagged for the Editor-in-Chief in §17, not used. |

### 5.2 Two discrepancies the searches surfaced — flagged, not resolved

| # | Repository says | Secondary layer says | Status |
|---|---|---|---|
| 1 | CAPM `renewal`: "15 PDUs every 3 years" | Several vendor pages assert a **5-year** CAPM validity period renewable by 15 PDUs or re-examination | **PRIMARY-SOURCE VERIFICATION REQUIRED.** One of the two is wrong; this environment cannot say which. |
| 2 | Google `examCost`: "~$49/month on Coursera (under $300 total)" | $49 / $51 / $62 depending on the page | **PRIMARY-SOURCE VERIFICATION REQUIRED.** Also currency- and region-dependent. |

Neither should be edited on this evidence. Both are recorded because the rebuild will render
them and the Editor-in-Chief can check them in minutes at the source.

---

## 6. Market evidence

Brief §9 asked how real job postings describe certifications for beginner roles.

**EVIDENCE INSUFFICIENT. No job-posting research was performed, and none could be.**

This environment cannot reach job boards; the egress block that stopped four issuing bodies
applies generally. There is no sample. Constructing one from memory or from search snippets
would be fabricating job postings, which the brief prohibits explicitly and `CLAUDE.md`
prohibits absolutely.

**What follows from that is an editorial position, not a gap to be papered over.** Rebuild 02
established the discipline: where CertNorth cannot measure employer behaviour, it says so and
hands the reader the check. The same applies here, and more forcefully — the beginner's
central anxiety is *"will this get me hired?"*, and the honest answer available to CertNorth
is that **no source we can reach measures how employers treat entry-level certifications**,
followed by a method the reader can run in an afternoon against their own market.

That is not an evasion. It is the one thing on this subject that is both true and useful, and
no training provider will ever publish it.

### 6.1 What the article currently asserts about the market, without evidence

| Assertion | Block |
|---|---|
| "It carries the PMI name, which recruiters recognize" | 27 |
| "The PMP is the most respected credential in the field" | 31 |
| "the gold standard" | dek, H3 |
| "Strong entry-level learning signal" *(via the sibling article's table)* | — |

None is sourced. All four are claims about employer and recruiter behaviour. See §7.

### 6.2 Institutional sources — what may and may not be drawn from them

The BLS Occupational Outlook Handbook page could not be fetched (§5). What the repository
records it as saying, consistently across `do-you-need-certification-project-manager`,
`how-to-become-project-manager` and the rebuilt `is-pmp-worth-it`:

> certification is **not a requirement** for the occupation; it "may be beneficial" and
> demonstrates competency to employers and clients. Median annual wage $100,750
> (May 2024).

**What this supports:** that the profession has no certification barrier — directly relevant
to a beginner, and currently absent from this article.

**What it cannot support:** anything about which certification is best, anything about any
individual employer, and anything about entry-level hiring specifically. Rebuild 02 drew that
line and this rebuild must hold it. **Do not use an occupational source to argue the value of
a specific credential.**

**Note:** this article does not currently link to
`do-you-need-certification-project-manager` at all, despite that page holding the site's best
evidence-led answer to a question every reader of this page is implicitly asking.

---

## 7. Claim verification

Every evaluative, numeric and market claim in the article. Classification per brief §11.

| # | Claim (block) | Current source | Does the source support it? | Problem | Suggested action |
|---|---|---|---|---|---|
| 1 | "the **best** first certification is the CAPM or the Google Certificate" (dek) | None | No | Absolute superlative; no criteria stated; contradicted by the article's own four "best for X" H3s | **UNSUPPORTED** — replace with a conditional framing |
| 2 | "the PMP is the **gold standard**" (dek, H3) | None | No | Marketing register; `CLAUDE.md` prohibits empty superlatives explicitly | **OPINION** — remove or attribute |
| 3 | "The PMP is the **most respected credential in the field**" (31) | None | No | Unmeasurable as stated; no source could establish it | **UNSUPPORTED** — remove |
| 4 | "It carries the PMI name, which **recruiters recognize**" (27) | None | No | Employer-behaviour claim; the same class of claim removed from the `is-pmp-worth-it` draft during Rebuild 02 review | **UNSUPPORTED** — state as a plausible mechanism or drop |
| 5 | "PSM I is the **cheapest real certification**" (40) | None | Partly | "Cheapest" is arguable on the site's own data (~$200 vs CAPM $225 — a $25 gap on unverified figures); "**real**" silently disqualifies the Google certificate without argument | **REQUIRES QUALIFICATION** |
| 6 | "the **gentlest** on-ramp" (25) | None | No | Subjective, unstated criterion | **OPINION** — acceptable only if framed as CertNorth's assessment |
| 7 | "**best recognized** entry-level credential" (H3) | None | No | Comparative recognition claim, unmeasured | **UNSUPPORTED** |
| 8 | Google: "**about $49/month**" (25) | Coursera page (unfetchable) | Unverifiable here; secondary layer gives $49/$51/$62 | Single figure presented as settled; region-dependent | **PRIMARY-SOURCE VERIFICATION REQUIRED** |
| 9 | Google: "finishable in **under six months**" (25) | Coursera page | Unverifiable here | Provider's own estimate presented as fact — `CLAUDE.md`: never treat an organisation's marketing as independent evidence about its own product | **REQUIRES QUALIFICATION** — attribute to Google |
| 10 | Google "**counts toward** the education requirement for the CAPM" (25) | Coursera page | Unverifiable here | Eligibility rule set by PMI, not Google; sourced to the wrong body | **PRIMARY-SOURCE VERIFICATION REQUIRED** — must come from PMI |
| 11 | CAPM "$225 member / $300 non-member" (27) | PMI index page | Not specifically | Not on the cited page; unfetchable | **PRIMARY-SOURCE VERIFICATION REQUIRED** |
| 12 | CAPM "secondary diploma plus **23 hours**" (27) | PMI index page | Not specifically | Same | **PRIMARY-SOURCE VERIFICATION REQUIRED** |
| 13 | CAPM "needs **no work experience**" (27) | PMI index page | Not specifically | Almost certainly right; still not verified here | **PARTIALLY SUPPORTED** |
| 14 | PMP "requires substantial documented experience" (31) | None cited | Repository-consistent (36/60 months, 7 locations) | Sound, unsourced on this page | **PARTIALLY SUPPORTED** |
| 15 | "2026 figures, **verified with each provider**" (table caption) | — | **No** | A claim about CertNorth's own verification. The same data file carried a wrong PMP fee until 2026-09-04. **Same failure mode as the `pmp-cost` "every figure from PMI" claim removed in Rebuild 01.** | **UNSUPPORTED — remove.** Highest-priority fix in this dossier |
| 16 | CSM "two-day course is mandatory" (34) | **No CSM source cited** | n/a | Five certifications, three sources | **PRIMARY-SOURCE VERIFICATION REQUIRED** |
| 17 | "(2026)" in title | — | n/a | Freshness signal on a file with `updatedAt` = 2026-07-25, unrevised | **REQUIRES QUALIFICATION** — the year in the title must be earned by actual revision |

**Totals: 6 UNSUPPORTED · 5 PRIMARY-SOURCE VERIFICATION REQUIRED · 3 REQUIRES QUALIFICATION ·
2 OPINION · 2 PARTIALLY SUPPORTED.** (Claim 5 counted once, under REQUIRES QUALIFICATION.)

**Claim 15 is the one that matters most**, because it is not a claim about a certification —
it is a claim about CertNorth's own rigour, and it is false. It is the third instance of this
exact pattern found in this project. A site-wide sweep for sourcing-process claims is
recommended in §17.

---

## 8. Internal overlap analysis

Corpus scan across all 50 articles (`platform/content/articles/`), term frequency by article
count:

| Term | Articles mentioning |
|---|---|
| PMP | 28 |
| beginner / entry-level | 29 |
| "worth it" | 29 |
| PSM | 17 |
| CAPM | 15 |
| CSM | 15 |
| "best … certification" | 19 |
| Google certificate | 6 |
| **PRINCE2** | **2** |

**Label: VERIFIED FROM CERTNORTH REPOSITORY.**

### 8.1 Pairwise analysis

Brief §12 required demonstrated overlap, not assumed overlap. Each of the five priority
articles was read in full.

---

**vs `pmp-vs-capm`** (533 words · 13 inbound · cluster `cl_compare`)

| | |
|---|---|
| **This article asks** | Which of five options should a beginner start with? |
| **That article asks** | Between PMI's two credentials, which comes first? |
| **Duplicated** | CAPM cost ($225/$300) · CAPM 23 contact hours · PMP 36/60-month bar · "CAPM is the stepping stone to the PMP" · "go straight to the PMP if you qualify" |
| **Necessary?** | The CAPM figures, yes — a comparison table needs its cells. The *argument* about the ladder, no. |
| **Cannibalisation risk** | **Low.** Different keywords, different reader states. |
| **Should delegate** | The whole CAPM→PMP progression argument. This article should assert it in one sentence and link. |
| **Note** | `pmp-vs-capm` carries an unsupported claim — *"PMI raised PMP exam fees in 2026"* — recorded in the Rebuild 02 dossier and **still unfixed**. Out of scope here; re-flagged in §17. |

---

**vs `capm-vs-google-pm-certificate`** (602 words · 2 inbound · cluster `cl_compare`)

| | |
|---|---|
| **This article asks** | Which of five? |
| **That article asks** | Between the two entry options, which — and can you do both? |
| **Duplicated** | Google ~$49/month · under six months · Google hours count toward CAPM's 23 · CAPM $225/$300 · "do Google first, then CAPM" |
| **Necessary?** | **This is the heaviest overlap on the site for this article.** That page's whole thesis — the two are complementary, not rivals — is compressed into this article's H3s. |
| **Cannibalisation risk** | **Moderate.** Both target beginners choosing between the same two products. That page has 2 inbound links; this has 20. This page is out-competing it internally on its own subject. |
| **Should delegate** | The Google-vs-CAPM head-to-head in full. |
| **Critical** | That article contains the sentence this rebuild needs — *"One proves you studied; the other is a credential you hold."* **The idea should be developed here at the category level, not the product level**, so the two pages argue different things rather than the same thing at different lengths. |

---

**vs `is-capm-worth-it`** (580 words · 5 inbound · cluster `cl_worth`)

| | |
|---|---|
| **This article asks** | Which first? |
| **That article asks** | Is this specific one worth the money? |
| **Duplicated** | $225/$300 · 23 hours · no experience · "PMI credential carries more weight than a course certificate" · "if you qualify for the PMP, skip the CAPM" |
| **Necessary?** | Partly. A verdict article and a comparison article legitimately share facts. |
| **Cannibalisation risk** | **Low.** Genuinely different intents. |
| **Note** | That article carries the eight-article `is-X-worth-it` spine — *"The case for it (real pros)" / "The case against it (real cons)" / "The honest bottom line"* — identified in the site audit as the highest-severity structural pattern. **Out of scope for Rebuild 03.** |

---

**vs `is-pmp-worth-it`** (1,746 words · 21 inbound · rebuilt 2026-09-04)

| | |
|---|---|
| **This article asks** | Which first? |
| **That article asks** | Should *you* pursue the PMP, given four gates? |
| **Duplicated** | The 36/60-month bar; "not a beginner credential" |
| **Necessary?** | Yes, and minimal. |
| **Cannibalisation risk** | **None.** |
| **Critical** | The rebuilt article's **gate one** — *"if you cannot yet document the months, the question is not answered but premature"* — links here as the destination for readers who fail it. **This page is the landing site for traffic Rebuild 02 deliberately redirects to it, and it is not currently built to receive it.** That raises the priority of this rebuild. |
| **Constraint** | The rebuild **must not** reuse the four-gates architecture. Two rebuilds, two shapes; a third repetition would create the very pattern this project exists to break. |

---

**vs `how-to-become-project-manager`** (636 words · 20 inbound · cluster `cl_paths`)

| | |
|---|---|
| **This article asks** | Which certification first? |
| **That article asks** | How do I enter the profession at all? |
| **Duplicated** | "CAPM or Google for traditional, Scrum for agile" · "certification works best on top of real experience" · the beginner framing |
| **Necessary?** | Yes — its Step 3 is a one-paragraph summary that correctly hands off here. This is well-designed delegation, in the right direction. |
| **Cannibalisation risk** | **Low.** |
| **Note** | That article holds the site's only use of the BLS median wage ($100,750, May 2024). Relevant context; **not** evidence about certifications. |

---

### 8.2 Also examined

- **`best-agile-certifications`** (1,078 words · 7 sources): covers PSM I, PSPO I, CSM, CSPO,
  SAFe, PMI-ACP, ICP-ACC. **Overlaps on PSM I and CSM**, which are two of this article's five.
  It handles them better — with prices, renewal cycles, pass marks and an
  employer-pays/self-funded distinction this article lacks. **This article should cover the
  Scrum options thinly and delegate**, which is roughly what it does now via `psm-vs-csm`,
  though it should link to `best-agile-certifications` as well and currently does not.
- **`google-pm-certificate-worth-it`** (504 words): the fullest treatment of the Google
  certificate, including the honest limitation the hub omits — *"it maps to coordinator and
  junior roles, not manager titles"* and *"it's very widely held, so it no longer makes your
  application unique on its own."* **That second point is decision-relevant for a beginner
  and is absent from the page that ranks it first.**
- **`do-you-need-certification-project-manager`**: the site's best evidence-led answer to the
  prior question. **Not linked from this article.** Should be.

### 8.3 Verdict on merging

**Do not merge.** Six articles touch the beginner/first-certification intent, but each holds a
distinct question and a distinct keyword, and none of the pairwise overlaps is substantive
enough to justify consolidation under `content-consolidation` criteria. The overlap that does
exist is **redundant restatement inside this article**, not duplicated pages — which is fixed
by delegating, not by merging.

The one relationship worth watching is `capm-vs-google-pm-certificate` (§8.1). If, after the
rebuild, this page still contains a full Google-vs-CAPM head-to-head, that pair should be
re-examined for consolidation. **Recorded as a future check, not a recommendation now.**

---

## 9. Original value opportunities

The test from `CLAUDE.md`: *what can CertNorth investigate, calculate, compare, explain,
contextualise or analyse that the reader cannot obtain from the primary source?*

**Current answer: almost nothing.** Strip the article to what is not obtainable from PMI's,
Google's, Scrum.org's and Scrum Alliance's own pages, and what remains is the ordering of a
list and the sentence "most of these articles are written by the companies selling the
training". The comparison table has genuine assembly value — no single provider publishes the
other four — but assembly alone is a directory, not analysis.

### 9.1 Five legitimate opportunities

**A. The category correction — the strongest.**
No provider will ever tell a beginner that the thing it sells is a different *kind* of thing
from its competitor's. Google will not explain that its certificate is not a professional
certification. Scrum Alliance will not explain that most of its price is teaching. PMI will
not explain that its famous credential is closed to you. **CertNorth can state all three,
from data it already holds, and nobody selling anything can.** This is the article's
strongest possible contribution and it is currently one buried callout.

**B. What you are actually buying, made explicit.**
Decompose each option into: teaching · a credential · an assessment · a recurring obligation.
Straight from `certifications.json`:

| | Teaching | Credential | Proctored exam | Recurring obligation |
|---|---|---|---|---|
| Google PM Certificate | **Yes — the whole product** | Course completion | No | **None** |
| CAPM | No — bought separately | PMI certification | Yes | PDUs |
| PSM I | No — optional | Scrum.org certification | Yes | **None — never expires** |
| CSM | **Yes — mandatory, most of the price** | Scrum Alliance certification | Light | **Every 2 years** |
| PMP | No — bought separately | PMI certification | Yes | 60 PDUs / 3 years + fee |

*(Renewal cycles marked PRIMARY-SOURCE VERIFICATION REQUIRED — see §5.2.)*

This is comparison as analysis rather than as tabulation, and it is a **different table from
the one the article has**, not a longer one.

**C. The recurring-obligation asymmetry.**
Two of the five never expire. One must be renewed every two years. Two require PDUs. **No
beginner-facing article on this subject leads with this**, and it can invert the ranking: the
cheapest thing to acquire is not the cheapest thing to hold. This is where a CertNorth
calculation would be legitimate — but only once renewal cycles are verified at source.
**Not calculable today.**

**D. Naming the evidence gap honestly.**
Every source that answers *"which is best recognised?"* is either the issuer or someone
selling training for it. CertNorth can say so, and hand the reader a market check they can
run themselves. This is the Rebuild 02 discipline applied to a beginner audience.

**E. The cost of choosing wrong.**
Brief §7 raised it and no article on the site addresses it. What actually happens if you buy
the Scrum credential and then take a traditional PM job? On the site's own data: the money is
mostly not wasted, because none of these is expensive relative to a salary, and because the
Google certificate feeds CAPM eligibility. **That is a genuinely reassuring, evidence-based
finding and nobody publishes it** — because everyone publishing has an incentive to make the
choice feel high-stakes. *(The CAPM-credit claim needs PMI verification first — claim 10.)*

### 9.2 What must not be done

No invented salary data. No invented job-posting samples. No claimed testing of any course.
No "we surveyed". No pass rates that PMI does not publish. No manufactured length: if the
honest article is 900 words, it is 900 words.

---

## 10. Structural and pattern analysis — Pattern Guardian

Run per `editorial-os/agents/pattern-guardian.md` against all 50 articles.

### 10.1 Corpus fingerprint

| Pattern | Corpus | This article |
|---|---|---|
| Opens `paragraph → callout` | **48 / 50** | **Yes** |
| Closes with `faq` | **48 / 50** | **Yes** |
| Contains a table or certTable | **50 / 50** | Yes |
| Year in title | 22 / 50 | Yes — "(2026)" |
| Opening callout begins "Quick answer" / "Short version" / "The short answer" | **22 / 50** | **Yes — "Quick answer:"** |
| Median H2 count | 5 | **3** |

**The only two articles in the entire corpus that break the opening-and-FAQ mould are
`pmp-cost` and `is-pmp-worth-it` — the two articles rebuilt in this project.** The Pattern
Guardian's own notes record the baseline as 50/50 on both; it is now 48/50 because of those
two rebuilds. Everything else on the site still shares one skeleton.

**Label: CERTNORTH CALCULATION** (measured programmatically across all 50 files).

### 10.2 Repeated H2 text across the corpus

| Count | H2 |
|---|---|
| 7× | The case for it (real pros) |
| 7× | The case against it (real cons) |
| 7× | The honest bottom line |
| 5× | Head-to-head comparison |
| 4× | What the sources report |
| **3×** | **Side-by-side comparison** ← this article |
| 3× | What it is and what it costs |

This article does not carry the worst offender (the seven-article `is-X-worth-it` spine), but
"Side-by-side comparison" is shared with two others.

### 10.3 The "best X" mould — the specific breach

The site has exactly two "best X, ranked" articles. Their skeletons:

| | `best-pm-certifications-beginners` | `best-agile-certifications` |
|---|---|---|
| 1 | paragraph — "most of these lists are written by sellers" | paragraph — "the marketing is relentless" |
| 2 | **callout: "Quick answer: …"** | **callout: "Our overall pick for most people is…"** |
| 3 | H2 + per-cert H3 sections | H2 "The main options side by side" + table |
| 4 | H2 "Side-by-side comparison" + certTable | numbered H2 per certification |
| 5 | callout(warn) — cost caveat | callout(warn) — cost caveat |
| 6 | **H2 "How to choose in five minutes"** | **H2 "How to choose in one minute"** |
| 7 | list | list |
| 8 | closing paragraph + pointer | callout(tip) + closing paragraph |
| 9 | FAQ | FAQ |

**Same skeleton, two blocks transposed.** The opening rhetorical move is the same
("everyone else is compromised, we aren't"), the cost-caveat callout occupies the same slot,
and the closing H2 is the same formula with the number changed. **A reader who opens both in
sequence sees one template twice** — precisely the anti-template rule's failure condition.

### 10.4 Repeated rhetorical moves

- **"The honest…"** — "The honest shortlist", "The honest recommendation" (×2), "The honest
  bottom line" (×7), "an honest, vendor-neutral ranking", "honest cons". *Honest* is doing
  duty as a brand tic. Used often enough, it stops functioning as a signal of candour.
- **Three-scenario callout** — "no experience → X · agile → Y · experienced → Z" appears in
  this article, `pmp-vs-capm`, and `capm-vs-google-pm-certificate`.
- **"Whatever you pick, check the current fee on the provider's official site"** — near-
  identical closing advice in this article and `best-agile-certifications`.

### 10.5 Required divergence for the rebuild

Concrete, and each must serve the argument rather than novelty:

1. **Do not open `paragraph → callout`.** 48/50 do.
2. **Do not open with "Quick answer".** 22/50 do.
3. **Do not close with an FAQ** that restates the body a fourth time. If a FAQ survives, it
   must answer questions the body does not.
4. **Do not use "How to choose in N minutes"** as an H2.
5. **Do not reuse "Side-by-side comparison."**
6. **Do not import the Rebuild 02 four-gates spine** or the Rebuild 01 fixed/variable/unpriceable spine.
7. **Reduce "honest"** to at most one use, where it is load-bearing.
8. Reach the corpus median of 5 H2s **only if the argument needs them.**

---

## 11. SEO and search intent analysis

**No production SEO field was changed. These are recommendations only.**

### 11.1 Current state

| Field | Value | Assessment |
|---|---|---|
| `metaTitle` | Best PM Certifications for Beginners (2026) — 41 chars | Within the 60-char GATE limit. "PM" abbreviated; the full phrase is the primary keyword |
| `metaDescription` | 148 chars | Within the 155-char limit. **Contains "ranking", which the rebuild may make inaccurate** |
| `primaryKeyword` | best project management certifications for beginners | Unique site-wide; GATE-valid |
| H1 | Best Project Management Certifications for Beginners (2026) | Matches the keyword; promises a ranking |

### 11.2 The title question

Brief §16 asked whether this should be *"best X"* or *"which X should I choose?"*.

**Recommendation: keep the title's "best…for beginners" phrasing and change what the article
does under it.** Reasoning:

- The keyword is what people search. Abandoning it discards a page with 20 inbound internal
  links and an established URL for a phrasing with less search demand.
- The URL must not change. `CLAUDE.md` forbids redirects and canonical changes without
  explicit approval, and there is no reader benefit here that would justify one.
- **The fix is not in the title — it is in delivering something better than the title
  promises.** A reader arriving on "best" and receiving a clear-eyed account of what the
  options actually are is well served. A reader arriving and receiving an unsupported ranking
  is not.

**However:** the article must stop asserting a flat ranking in the dek and the opening
callout, because those are the parts that make an unsupportable promise in CertNorth's own
voice. The title poses a question the reader asked; the dek should signal the honest answer.

### 11.3 The "(2026)" problem

22 of 50 titles carry a year. This one carries "(2026)" while `updatedAt` has stood at
2026-07-25 since publication. A year in a title is a freshness claim. **Either the rebuild
earns it by genuine revision — which it will — or it should come out.** Recommend it stays,
and that `updatedAt` moves with the rebuild, as it did for the two previous rebuilds.

### 11.4 Semantically relevant territory currently unserved

Terms a comprehensive treatment of this intent would naturally cover, absent from the
article: *entry-level* (as a phrase) · *no experience* · *prerequisites* · *career change* ·
*renewal / expiry* · *PRINCE2* · *outside the US* · *coordinator* · *what employers ask for*.
Several are decision-relevant, not merely keyword-relevant — which is why they belong.

### 11.5 Not to be done

No keyword stuffing. No adding sections to capture terms. Any term above earns its place only
by answering a real reader question.

---

## 12. AdSense editorial quality assessment

Assessed against brief §17. **No claim is made that any change guarantees approval, and none
should be made to the Editor-in-Chief or anyone else.**

| Question | Verdict | Reasoning |
|---|---|---|
| Does it answer a real question? | **PASS** | The intent is genuine and high-volume |
| Is there enough analysis? | **FAIL** | Assembly and assertion. The one analytical sentence (callout 2) is undeveloped |
| Can the reader decide better after reading? | **CONCERN** | Only if they match one of three scenarios. No method, no criteria |
| Does it offer more than official pages? | **FAIL** | Strip the assembled table and the "we're independent" line and little remains |
| Are the comparisons justified? | **FAIL** | The central table compares incommensurable products in one column (§4.1) |
| Do important claims have evidence? | **FAIL** | 6 UNSUPPORTED, including 4 employer-behaviour claims and 1 false claim about CertNorth's own verification |
| Too much generic content? | **CONCERN** | The same answer is given three times in 622 words |
| Does it look mass-produced? | **FAIL** | Shares a skeleton with its only sibling, down to the closing H2 formula (§10.3) |
| Unnecessary overlap with other articles? | **CONCERN** | Heavy restatement of `capm-vs-google-pm-certificate`, delegable |
| Does it have its own editorial identity? | **FAIL** | Its identity is the site template plus a list |

**Overall: FAIL.** Not because it is short and not because it is dishonest, but because it
adds little a reader could not get from four provider pages, and what it does add — the
ranking — is asserted without criteria or evidence.

**The encouraging part:** everything needed to fix this is already in the repository. The
category distinction is in `capm-vs-google-pm-certificate`. The renewal asymmetry is in
`certifications.json`. The evidential discipline is in the two completed rebuilds. **The
material exists; it has never been assembled into an argument.**

---

## 13. Candidate editorial angles

Three were developed. Each is stated with what it would require and what it would cost.

### Angle A — "What you're actually buying" *(recommended)*

**Question:** *You have decided to spend money on a project management certification. What
are these five things, and which one matches what you are trying to do?*

**Thesis:** Beginners think they are choosing between five certifications. They are choosing
between **two different purchases — teaching and a credential** — and the standard list is
unhelpful because it prices them in the same column.

- **Original value:** the category correction (§9.1 A, B, C). Nobody selling any of these can
  publish it.
- **Evidence needed:** `certifications.json` + repository. **All present.**
- **Structural risk:** low. Naturally produces a different shape from both prior rebuilds.
- **Cost:** the flat ranking goes. The article stops promising a winner and starts supplying
  a method.
- **Weakness:** demands more of the reader than "get the CAPM". Mitigated by giving the
  answer for the common cases without pretending it is universal.

### Angle B — "The five options, honestly ranked, with criteria stated"

**Question:** the current one, done properly.

Keep the ranking, state the criteria, fix every unsupported claim, add PRINCE2, remove the
PMP from the comparison.

- **Original value:** moderate. Better than now; still fundamentally a list.
- **Evidence needed:** the same, plus a defensible criteria set.
- **Structural risk:** **high.** Keeping the "ranked list" form makes it very hard not to
  reproduce the `best-agile-certifications` skeleton (§10.3).
- **Weakness:** it does not resolve the category error. A criteria-based ranking of five items
  that are not the same kind of thing is a better-argued invalid comparison.

### Angle C — "Should you buy a certification at all yet?"

**Question:** *Before choosing one, is a certification the right purchase for you right now?*

- **Original value:** high — but **it is already owned** by
  `do-you-need-certification-project-manager`, which does it with a real source.
- **Weakness:** **fails the keyword promise.** A reader searching "best certifications for
  beginners" has already decided. Answering a question they did not ask, on a page with 20
  inbound links from articles that promise a comparison, would be a bait-and-switch.
- **Correct use:** as a link in the first 200 words, not as the article. Recommended either way.

---

## 14. Recommended editorial angle

**Angle A — "What you're actually buying."**

Four reasons.

**1. It resolves the article's central defect rather than tidying it.** The comparison is
currently invalid (§4.1). Angle B leaves it invalid; Angle C abandons the intent. Angle A
makes the invalidity itself the article's opening contribution.

**2. It is the only angle whose original value is unavailable from any primary source.**
PMI, Google, Scrum.org and Scrum Alliance each describe their own product accurately and none
has any reason to explain that it belongs to a different category than its competitor's.
`CLAUDE.md`'s original-value test is passed on the first section rather than argued for.

**3. It can be written entirely from verified material.** In an environment where no issuing
body is reachable (§5), an angle that depends on **relationships between facts the repository
already holds** is buildable now; one that depends on fresh price verification is not. Every
unverifiable figure can be presented as CertNorth's recorded value with an explicit
verification date — which is honest, and which the site's own data model already supports via
`verifiedOn`.

**4. It serves the reader Rebuild 02 sends here.** `is-pmp-worth-it` gate one now routes
not-yet-eligible readers to this page. They arrive having just learned they cannot buy the
famous credential. What they need is not a ranking — it is an account of what they *can* buy
and what each thing is. Angle A is that account.

**It also keeps the promise of the title.** A reader searching for the best beginner
certification gets a direct answer for their situation, plus the criteria to check it — which
is more than a ranking, not less.

---

## 15. Proposed architecture

**A proposal for human approval. Not a draft. No text has been written.**

Working H1 (unchanged, for the reasons in §11.2):
**Best Project Management Certifications for Beginners (2026)**

Proposed dek direction — replacing the two unsupported superlatives with the actual finding:
*there is no single best, and the reason is that these five things are not the same kind of
thing.*

| # | Proposed H2 | Job | Evidence status |
|---|---|---|---|
| 1 | *(no heading — opening, not a callout)* | State the finding immediately: you are choosing between two kinds of purchase, not five products | Repository |
| 2 | The five options are not the same kind of thing | The category correction. Course completion vs professional certification vs mandatory-course credential vs experience-gated credential | `certifications.json` + repository |
| 3 | What each one actually costs you — and for how long | The teaching / credential / assessment / recurring-obligation decomposition, incl. the two that never expire | `certifications.json`; **renewal cycles flagged for verification** |
| 4 | The one you have heard of is the one you cannot take | The PMP, treated as a destination and explicitly excluded from the comparison, with the reason | Repository (36/60 months, 7 locations) |
| 5 | The recognition question, and why nobody can answer it for you | The evidence gap stated plainly, plus a market check the reader can run | Rebuild 02 discipline; BLS framing via repository |
| 6 | Where this leaves you | Resolution **by situation**, with criteria stated — not a ranking | Editorial judgment, labelled as such |
| 7 | What we could not verify | Explicit: which figures are CertNorth's recorded values, when they were checked, what the reader should confirm | §5, §7 |

Plus the `certTable` — **retained and repositioned**, since it is the site's only rendering of
`certifications.json` and its assembly value is real. Its caption must lose *"verified with
each provider"* (claim 15) and gain an accurate statement of what CertNorth actually did.

**Open architectural questions for the Editor-in-Chief — §17.**

**Length:** wherever the argument lands. On this material, likely 1,100–1,400 words. **That is
an estimate, not a target.** The anti-thin-content rule cuts both ways: if section 5 is honest
in 150 words, it is 150 words.

**Structural divergence check against §10.5:** does not open `paragraph → callout`; no "Quick
answer"; no "How to choose in N minutes"; no "Side-by-side comparison"; not the four-gates
spine; not the fixed/variable/unpriceable spine; 6–7 H2s. **Passes all eight.**

---

## 16. Decision: KEEP / REBUILD / MERGE / HOLD / REMOVE

# → REBUILD WITH MAJOR RESTRUCTURE

**Why not KEEP & REBUILD (light):** a light rebuild fixes the six unsupported claims and the
false caption, and leaves the article comparing incommensurable products under a promise it
cannot keep. The defect is architectural.

**Why not MERGE:** demonstrated in §8, not assumed. Six articles touch this intent; each holds
a distinct question and keyword; no pairwise overlap meets the consolidation threshold. The
page carries 20 inbound links and is the site's only consumer of `certifications.json`.
Merging would destroy internal structure to solve a problem that is internal to one article.

**Why not HOLD:** the diagnosis does not depend on anything unavailable. The category error,
the unsupported claims, the false sourcing caption, the structural duplication and the
link-authority asymmetry are all measured from the repository. The unverifiable items are
**prices**, and the recommended angle does not rest on them.

**Why not REMOVE:** it answers a real question, holds 20 inbound links, and is the destination
Rebuild 02 routes ineligible readers to. Removing it would break the site's beginner path.

**Why REBUILD WITH MAJOR RESTRUCTURE:** the intent is valid and valuable; the architecture is
wrong; the central comparison is invalid as constructed; the promise in the dek is
unsupportable; and the material to fix all of it already exists in the repository.

**Priority: high** — higher than its word count suggests, because Rebuild 02 now depends on it.

---

## 17. Human editor decisions required

**Nothing below has been actioned. Each needs the Editor-in-Chief's word.**

### Blocking — the rebuild cannot be designed without these

| # | Decision | Options | Recommendation |
|---|---|---|---|
| 1 | **Editorial angle** | A (what you're buying) · B (ranking done properly) · C (should you buy at all) | **A** — §14 |
| 2 | **Does the PMP stay in the comparison table?** | Remove and explain · keep, visually separated · leave as is | **Remove and explain.** Its exclusion is more informative than its inclusion |
| 3 | **Is PRINCE2 added?** | Add as a sixth · keep out and say why · leave silently absent | **Say why, at minimum.** Adding it improves non-US coverage; silence is not defensible |
| 4 | **Is the title kept?** | Keep "Best…(2026)" · change to "Which…should you get first?" | **Keep** — §11.2. URL must not change |

### Verification — you can settle these at source in minutes; this environment cannot

| # | Item | Why it matters |
|---|---|---|
| 5 | **CAPM fee** — repository says $225/$300 | Rendered in the table; the same file was wrong about the PMP until 2026-09-04 |
| 6 | **CAPM renewal cycle** — repository says 15 PDUs / 3 years; secondary sources say 5-year validity | Direct contradiction (§5.2). One is wrong |
| 7 | **Google certificate price** — repository says ~$49/month | Secondary layer gives $49 / $51 / $62 (§5.2) |
| 8 | **Does the Google certificate count toward CAPM's 23 hours?** | Asserted twice; sourced to Google, but the rule is PMI's (claim 10) |
| 9 | **PSM I fee** — repository says ~$200 | Underpins the "cheapest" claim (claim 5) |
| 10 | **CSM cost and renewal** — repository says ~$800–$1,500, every 2 years | **No CSM source is cited anywhere in the article** |
| 11 | **PRINCE2 Foundation**, if added — incl. the reported January 2026 rename | Search-discovery only; unverified (§5.1) |

### Recorded, out of scope for Rebuild 03

| # | Item |
|---|---|
| 12 | **`pmp-vs-capm` still asserts *"PMI raised PMP exam fees in 2026"*** — unsupported, flagged in the Rebuild 02 dossier, still live |
| 13 | **The seven-article `is-X-worth-it` spine** — the site's highest-severity structural pattern, untouched |
| 14 | **48/50 articles still open `paragraph → callout` and close with an FAQ** — only the two rebuilds diverge |
| 15 | **~160 source citations site-wide carry no date field**, while `CLAUDE.md` requires date sensitivity |
| 16 | **Recommended: a site-wide sweep for claims about CertNorth's own sourcing process** — "verified with each provider", "all figures from X". Three instances found so far, all false or unsupported. This is a credibility risk of a different order from a wrong price |

---

## 18. Source register

### 18.1 External sources — attempted

| Organisation | Page | URL | Accessed | Would support | Result / limitation |
|---|---|---|---|---|---|
| PMI | Certified Associate in Project Management (CAPM) | `https://www.pmi.org/certifications/certified-associate-capm` | 2026-09-04 | Claims 11, 12, 13; decisions 5, 6, 8 | **EGRESS_BLOCKED — not reached** |
| Coursera / Google | Google Project Management Professional Certificate | `https://www.coursera.org/professional-certificates/google-project-management` | 2026-09-04 | Claims 8, 9, 10; decision 7 | **EGRESS_BLOCKED — not reached** |
| Scrum.org | Professional Scrum Master I | `https://www.scrum.org/assessments/professional-scrum-master-i-certification` | 2026-09-04 | Claim 5; decision 9 | **EGRESS_BLOCKED — not reached** |
| U.S. BLS | Project Management Specialists, OOH | `https://www.bls.gov/ooh/business-and-financial/project-management-specialists.htm` | 2026-09-04 | §6.2 occupational framing | **EGRESS_BLOCKED — not reached** |
| Scrum Alliance | Certified ScrumMaster | `https://www.scrumalliance.org/get-certified/scrum-master-track/certified-scrummaster` | not attempted | Claim 16; decision 10 | Not attempted after four consecutive blocks |
| PeopleCert | PRINCE2 Foundation (v7) | `https://www.peoplecert.org/` | not attempted | §4.3; decision 11 | Surfaced in search; not fetchable |

**Primary sources successfully consulted in this phase: 0.**

### 18.2 Search-discovery record — not evidence

Recorded so the Editor-in-Chief can see what the secondary layer looks like and why it was
refused. **No claim in this dossier rests on any of it.**

| Query | Domains returned | Use |
|---|---|---|
| CAPM exam fee / contact hours / eligibility 2026 | rosemet.com · olusholaoluyomi.com · learnersink.com · projeric.com · cciedump.spoto.net · capmquiz.com · flashgenius.net — **all training or exam-prep vendors; zero pmi.org** | Surfaced discrepancy 1 (§5.2). Not used to verify |
| Google PM Certificate cost / duration 2026 | coursera.org (unfetchable) · e-student.org · technologyadvice.com · googlepmcertguide.com · simputech.com · shortcourses.com · onlinecerthub.com · flashgenius.net | Surfaced discrepancy 2 — **three prices in one result set**. Not used to verify |
| PRINCE2 7 Foundation requirements 2026 | learningtree.com · qa.com · peoplecert.org (unfetchable) · open-exam-prep.com · olusholaoluyomi.com · prince2exam.com | Surfaced decision 11. Not used to verify |

Per the standing protocol correction: *"Multiple commercial sites repeating the same number
are NOT independent verification."* In the Google case the commercial sites did not even
repeat the same number.

### 18.3 Repository sources — measured directly

| Source | Used for |
|---|---|
| `platform/content/articles/best-pm-certifications-beginners.json` | §2 in full |
| `platform/content/certifications.json` | §2.6, §4.1, §4.3, §9.1 |
| `platform/content/articles/*.json` (all 50) | §8 corpus scan · §10 pattern analysis · §2.10 link graph |
| `pmp-vs-capm` · `capm-vs-google-pm-certificate` · `is-capm-worth-it` · `is-pmp-worth-it` · `how-to-become-project-manager` · `best-agile-certifications` · `google-pm-certificate-worth-it` | §8, read in full |
| `editorial-os/agents/pattern-guardian.md` | §10 method |
| `editorial-os/reports/PMP_GLOBAL_PRICE_CORRECTION_REPORT.md` | §7 claim 15 — the record that `certifications.json` carried a wrong PMP fee until 2026-09-04 |
| `editorial-os/research/is-pmp-worth-it-research-dossier.md` | §8.1 — the recorded `pmp-vs-capm` fee claim |
| `CLAUDE.md` | Source hierarchy · anti-template · original value · anti-thin-content · date sensitivity |

### 18.4 Verified figures carried forward

The only externally verified figures available to this rebuild, checked by the
Editor-in-Chief directly at PMI on 2026-09-04:

| Item | Value |
|---|---|
| PMP exam | $405 member / $655 non-member |
| PMI membership | $139 / year |
| PMP renewal | 60 PDUs per 3-year cycle · ≥35 Education · ≤25 Giving Back · ≤8 Work as a Practitioner |
| PMP renewal fee | **NOT ESTABLISHED** |

**No CAPM, Google, PSM I, CSM or PRINCE2 figure has been verified at source at any point in
this project.** Every such figure the rebuild renders will be a CertNorth recorded value, and
must be presented as one.

---

**Production untouched.** No article JSON modified · no `platform/src/*` modified · no build
run · nothing published, merged or deployed. The only file created is this dossier.
