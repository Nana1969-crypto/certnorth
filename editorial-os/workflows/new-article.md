# Workflow: New Article

**Purpose:** take a reader question to a publishable article.
**Publication:** requires explicit human approval at the final gate.

## Sequence
1. **Research question** — one sentence, in the reader's terms. Not a keyword.
2. **Source discovery** — `config/source-hierarchy.yaml`; highest tier available
3. **Research** — `agents/research-agent.md` → Research Dossier
4. **Verification** — `agents/source-verifier.md`; mark anything UNVERIFIED
5. **Data analysis** — `agents/data-analyst.md`; label SOURCE vs CERTNORTH CALCULATION
6. **Original value** — `agents/originality-strategist.md`. **Mandatory gate.** If
   nothing original exists, change the question, merge, or stop here.
7. **Editorial strategy** — `agents/editorial-strategist.md` → Article Brief,
   including which existing pages will link *to* this one
8. **Draft** — `agents/writer.md`
9. **Fact check** — `agents/fact-checker.md`; resolve every blocking claim
10. **Pattern check** — `agents/pattern-guardian.md` against the corpus
11. **SEO check** — `agents/seo-editor.md`
12. **Quality check** — `agents/adsense-quality-auditor.md`
13. **Portuguese editor brief** — `skills/editor-brief-ptbr/SKILL.md`
14. **Human approval** — stop and wait
15. **Publish** — build, check, browser-verify, commit, PR, merge; then add the
    planned inbound links from existing articles

## Hard stops
- No original value → do not proceed to drafting
- Unresolved UNSUPPORTED / MISLEADING / INCORRECT / OUTDATED claim → no approval gate
- Pattern thresholds breached → redesign before approval
- No approval → no publication
