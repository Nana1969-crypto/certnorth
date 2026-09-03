# Workflow: Audit Existing Site

**Purpose:** produce a complete, evidence-based picture of the site before any change.
**Destructive actions:** none. This workflow never modifies live content.

## Sequence
1. **Inspect** — stack, content location, format, configuration, institutional pages
2. **Inventory** — every article with id, URL, cluster, dates, word count, sources,
   official-source share, outbound and inbound links, primary keyword, content type
3. **Classify** — assign 🟢 / 🔵 / 🟡 / 🔴 / ⚫ with rationale and confidence
4. **Detect overlap** — by reader intent, not topic similarity
5. **Detect outdated facts** — check volatile fields against their source dates
6. **Detect repetitive structures** — run `skills/anti-template/SKILL.md` across the
   whole corpus, not article by article
7. **Evaluate originality** — what each page adds beyond its sources
8. **Evaluate evidence** — traceability, source tier, false precision
9. **Detect orphans** — articles with zero inbound internal links
10. **Produce recommendations** — ordered by impact, not by ease
11. **Portuguese executive briefing** — via `skills/editor-brief-ptbr/SKILL.md`

## Outputs
- `reports/INITIAL_REPOSITORY_INSPECTION.md`
- `reports/CERTNORTH_INITIAL_CONTENT_AUDIT.md`
- `reports/DISCLOSURE_AUDIT.md`
- A Portuguese briefing to the Editor-in-Chief

## Stop condition
Present findings and **wait**. Do not begin remediation.
