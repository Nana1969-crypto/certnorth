# Workflow: Audit Content (single article)

**Purpose:** assess one article and recommend an action.
**Destructive actions:** none.

## Sequence
1. **Read** the article in full, including its sources list
2. **Identify intent** — what question does a reader arrive with?
3. **Verify sources** — `skills/source-verification/SKILL.md`; check dates and scope
4. **Identify unsupported claims** — anything not traceable, and any false precision
5. **Compare with the site** — does another page serve this intent? Does this
   contradict another page?
6. **Assess originality** — `skills/original-value/SKILL.md`
7. **Assess structure** — `skills/anti-template/SKILL.md` against the corpus
8. **Assess SEO** — title honesty, metadata, inbound and outbound links
9. **Assess quality risk** — `skills/adsense-quality/SKILL.md`
10. **Recommend** — one action, with rationale and confidence

## Output
One row via `templates/content-audit-row.md`, plus notes on any blocking factual
problem found.

## Note
If the article is already strong, say so and recommend no action. Do not manufacture
work.
