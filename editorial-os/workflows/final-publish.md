# Workflow: Final Publish

**Purpose:** the publication gate. Nothing reaches `main` except through this.

## Gates, in order
```
Research Gate        — question answered, sources adequate and current
      ↓
Source Gate          — every significant claim traceable and verified
      ↓
Original Value Gate  — a specific, non-duplicative contribution exists
      ↓
Editorial Gate       — coherent, correctly typed, in voice
      ↓
Fact Check Gate      — no UNSUPPORTED / MISLEADING / INCORRECT / OUTDATED claims
      ↓
Pattern Gate         — structural repetition within thresholds
      ↓
SEO Gate             — natural; inbound links planned
      ↓
Quality Gate         — publisher-quality risks acceptable
      ↓
Portuguese Editor Brief
      ↓
HUMAN APPROVAL       ← hard stop
      ↓
Publish
```

## Technical publication steps (after approval)
1. `cd platform && node src/build.js --force` — GATE must pass
2. `node src/check.js` — must be green
3. Browser-verify: correct title, zero console errors, no horizontal scroll at 375px
4. Verify internal links resolve
5. Commit with a message stating what was verified and what was not
6. Open a PR describing the editorial reasoning, then merge
7. **Add the planned inbound links** from existing articles — the article is not
   finished until it is not an orphan

## Any gate fails
Return to the responsible agent with the specific defect. Do not proceed. Do not
soften a gate because the article is otherwise good.

## No approval
No publication. There is no exception to this.
