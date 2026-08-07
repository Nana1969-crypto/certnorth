# CertNorth — Content Plan & Editorial Priorities

Living note for the daily-article cadence. Update as pillars fill out.

## Standing priority (as of 2026-07-31)

Reinforce the **thinner pillars** while keeping the commercial certification cluster healthy:

1. **Salaries** (`cl_salary`) — was the thinnest pillar; every salary article must cite a real, named source per figure and anchor to official data (US BLS) where it exists. Be honest when no official figure exists (e.g. Scrum Master has no BLS occupation code).
2. **Career Paths** (`cl_paths`) & **Skills / Methods** (`cl_skills`) — "how to become / how to learn" content that ranks fast and funnels readers into the commercial cluster via internal links.
3. Keep the **commercial cluster** (`cl_compare`, `cl_worth`, `cl_guides`) fed — it's the money cluster (affiliate) — but don't let it crowd out 1–2.

## Pillar coverage snapshot

| Pillar | Cluster | Articles |
|---|---|---|
| Certifications | cl_compare, cl_worth, cl_guides | pmp-vs-capm, psm-vs-csm, pmp-vs-prince2, capm-vs-google-pm-certificate, pspo-vs-cspo, is-pmp-worth-it, is-capm-worth-it, is-psm-worth-it, is-csm-worth-it, is-pspo-worth-it, google-pm-certificate-worth-it, best-pm-certifications-beginners, pmp-cost, pmp-eligibility, how-long-to-get-pmp, agile-vs-waterfall |
| Career Paths | cl_paths | how-to-become-project-manager, how-to-become-scrum-master, how-to-become-product-owner, how-to-become-agile-coach |
| Salaries | cl_salary | project-manager-salary, scrum-master-salary, product-owner-salary |
| Skills & Methods | cl_skills | what-does-a-scrum-master-do, kanban-vs-scrum, what-does-a-product-owner-do |

## Candidate next articles (by priority)

- **Skills/Methods (3 articles as of 2026-08-01):** next → "What is a product backlog", "How to learn Agile", "What is a sprint", "Scrum roles explained".
- **Salaries:** "Product Owner salary", "Agile Coach salary", "PMP salary premium (does PMP raise pay?)".
- **Career Paths:** "How to become a Product Owner", "How to become an Agile Coach", "Project coordinator to project manager".
- **Certifications (commercial):** "PMP vs PMI-ACP", "Best Agile certifications", "SAFe certification worth it", "CAPM vs PMP for beginners".

## Publishing workflow (owner's standing decision, 2026-08-07)

The owner has explicitly authorised Claude to **merge its own pull requests**, so
publishing no longer waits on her. The flow per article stays:

1. Write on `claude/content-site-setup-t8lbe5`.
2. `node src/build.js --force` (GATE) + `node src/check.js` must both be green.
3. Browser-verify: correct title, zero console errors, no horizontal scroll at 375px.
4. Push, open a PR, then merge it. Cloudflare deploys from `main` automatically.

Keep opening a PR per publication rather than pushing straight to `main` — it is
what makes a single bad change cheap to revert. Never merge a PR whose build or
check is red, and never skip the browser step to save time. If a fact could not
be verified at its source, do not publish the number; say so to the owner instead.

## Non-negotiables (from the mission)

- Never publish through a disabled gate; never fabricate data.
- One intent → one URL. `intent.primaryKeyword` unique site-wide.
- Institutional authorship labeled honestly (author_team).
- updatedAt = publishedAt for new posts; no cosmetic date bumps.
- Every article: ≥2 h2, ≥1 internal link, faq block, ≥1 real source.
