# Disclosure Audit

**Date:** 2026-09-03
**Pages inspected:** About, Privacy Policy, Contact, Editorial Policy, footer,
article templates, `site.json`, `pages.json`, all 50 article files
**Changes made:** none. Every finding below awaits human decision.

---

## Finding 1 — The site discloses affiliate commissions it does not earn

**Severity: high.** This is the only finding in the entire audit that is arguably
deceptive rather than merely weak.

### What the site says

Three separate places state that CertNorth earns affiliate commissions.

**Editorial Policy** (`platform/content/site.json`):
> **On affiliates:** some links to courses and exam-prep tools earn us a commission
> at no cost to you. That never changes a ranking or a verdict — when we say skip
> something, it stays "skip it" whether or not there's a commission attached.

**About page** (`platform/content/pages.json`):
> Some links to courses and exam-prep tools earn us a commission at no extra cost to
> you, and the site may display advertising. Neither ever changes a ranking or a
> verdict.

**Privacy Policy** (`platform/content/pages.json`):
> References affiliate links in its description and in its disclosure section.

### What is actually true

Measured across all 50 article files:

| Measure | Count |
|---|---|
| External links in article bodies | **0** |
| Links carrying an affiliate or tracking parameter | **0** |
| Affiliate programmes joined | **0** (no evidence in the repository) |

Every external URL on the site sits in a `sources` list and points at PMI,
Scrum.org, the Scrum Guide, Scrum Alliance, BLS, IIBA, Scaled Agile, ICAgile,
PeopleCert or ACM. There is not one commercial link anywhere on CertNorth.

### Why this matters

The disclosure was written in good faith, in anticipation of monetisation that never
happened. But its effect is that the site tells readers it has a commercial interest
in its own recommendations when it does not.

That is backwards from the usual failure. Most sites hide commercial relationships;
this one invents one. It is still a false statement about how the publication
operates, and for a site whose entire positioning is independence, it is the most
damaging possible thing to be wrong about.

It also creates a specific quality risk: a reviewer who checks the disclosure against
the site will find no affiliate links, which reads as a disclosure copied from a
template rather than written for this publication.

### Recommended action

**Rewrite all three statements to describe reality.** Two honest options:

**Option A — state the current position plainly.**
> CertNorth currently earns nothing. We use no affiliate links and have no
> commercial relationship with any certification body or training provider. If that
> changes, we will say so here before it appears anywhere else on the site.

This is accurate today and is a stronger claim than the current text.

**Option B — state the position and the intent.**
> CertNorth has no affiliate links today and no commercial relationship with any
> certification body or training provider. We may add affiliate links in future,
> and we will disclose them here and on any page that carries them. A commission
> will never change a ranking or a verdict.

Option B preserves the forward-looking promise without claiming a present-tense
relationship that does not exist.

**What must not happen:** adding affiliate links in order to make the existing
disclosure true. That would be choosing the disclosure over the editorial decision.

### Requires your approval
Yes — this changes the About page, the Privacy Policy and the Editorial Policy. It is
a small edit with a large meaning, and it should be your wording, not mine.

---

## Finding 2 — Advertising disclosure describes ads that are not running

**Severity: low.** Accurate as written, worth checking.

The Privacy Policy and About page state that the site "may display advertising" and
the Privacy Policy has a dedicated Google AdSense section covering cookies,
third-party vendors, and how readers can opt out.

The AdSense verification script **is** present on all pages and `ads.txt` **is**
correct, so the infrastructure is real. No ads are currently served because the
account was not approved.

The wording "may display" is honest — it does not claim ads are running. No change
required, but if you adopt Option A above, keep this section: it will be accurate
again the moment ads serve.

---

## Finding 3 — Institutional authorship is honest but carries no named accountability

**Severity: low-medium.** Not deceptive. Worth a decision.

`authors.json` contains one author: "The CertNorth Team", type `Organization`, with
this bio position stated in the Editorial Policy:

> **About authorship:** this is an early build of CertNorth, published under our
> editorial team. We compile and verify from official primary sources rather than
> claiming personal credentials we don't have — and we tell you exactly where every
> fact comes from so you can check it yourself.

**This is honest and I recommend keeping it.** It claims no credentials, invents no
byline, and explains the basis of authority it does have. That is the correct
handling and it is rarer than it should be.

The observation is that no human name appears anywhere on the site. A reader cannot
identify who is accountable for a correction. Options, all legitimate:

| Option | Trade-off |
|---|---|
| Keep as is | Honest, but anonymous |
| Add your name as Editor-in-Chief | Real accountability, no invented credentials, and you genuinely hold the role |
| Add a named contact for corrections | Middle ground; `contact@certnorth.com` already exists |

**Never acceptable:** inventing a named author, or attributing credentials or
experience to anyone who does not have them.

### Requires your approval
Yes, if you want to be named. This is a personal decision about visibility and I will
not make it for you.

---

## Finding 4 — No Terms of Use page

**Severity: low.**

Present: About, Privacy Policy, Contact, Editorial Policy — all four linked from the
footer of every page.

Absent: Terms of Use. Not required for a content site with no accounts, no payments
and no user submissions, but conventional and cheap to add. It would also be the
natural place for a limitation-of-liability statement about acting on certification
advice.

**Recommendation:** add it, low priority.

---

## Finding 5 — The editorial policy promises a re-verification schedule that has not run

**Severity: medium.** Not a false statement, but an unmet commitment.

The Editorial Policy states:
> **These figures change.** [...] We re-verify the volatile numbers on a regular
> schedule and update the guide — we do not leave stale figures online, and we never
> bump a date without actually revising the content.

The second half is true and well-honoured: 47 of 50 articles have `updatedAt` equal
to `publishedAt`, which is exactly what "never bump a date without revising" looks
like in practice. No cosmetic date bumps exist anywhere.

The first half is not yet evidenced. No scheduled re-verification pass has run. All
six certifications in `certifications.json` still carry `verifiedOn: 2026-07`.

The site is six weeks old, so nothing is stale yet — the promise is not broken, it is
untested. But it becomes false the moment a figure goes unchecked past its cycle.

**Recommendation:** either run the first re-verification pass, or soften "on a
regular schedule" to describe what actually happens. The build already warns after
six months, so the mechanism exists; it needs to be used once for the claim to be
demonstrable.

---

## Summary

| # | Finding | Severity | Needs your approval |
|---|---|---|---|
| 1 | Affiliate commissions disclosed but not earned | **High** | **Yes** |
| 2 | Advertising disclosure ("may display") | Low | No |
| 3 | No named human accountability | Low-medium | Yes, if naming yourself |
| 4 | No Terms of Use page | Low | No |
| 5 | Re-verification schedule promised, not yet run | Medium | No |

**Nothing in this report has been changed.** Finding 1 is the one I would fix today
if you approve it, and I would use your wording rather than mine.

I have not invented an affiliate relationship to make the disclosure true, and I will
not.
