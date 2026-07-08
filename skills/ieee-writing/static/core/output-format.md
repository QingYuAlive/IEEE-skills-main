# Output Format For IEEE Transactions Writing

Return successful drafts in this order:

1. `Route:` detected paper type, section, language, journal, and gate status.
2. `Draft:` the requested manuscript prose.
3. `Section Outline:` compact bullets or numbered paragraph jobs.
4. `Notation Used:` symbols from the Notation Ledger that appear in the draft.
5. `Claim-Evidence Map:` claims mapped to protocol, table, figure, ablation, bound, or limitation.
6. `Reviewer Defense Notes:` concise notes on protocol fairness, OOD scope, ablation coverage, visualization limits, and complexity.
7. `Missing Inputs:` only material gaps that affect correctness or defensibility.

For Chinese-author notes, provide polished English first, then brief Chinese notes explaining only structural or claim-calibration decisions.

If the math gate fails, return only the blocked-gate report from `SKILL.md` plus one concise sentence explaining that drafting is suspended until the missing formal objects are supplied.

## Successful Output JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": [
    "route",
    "draft",
    "section_outline",
    "notation_used",
    "claim_evidence_map",
    "reviewer_defense_notes",
    "missing_inputs"
  ],
  "properties": {
    "route": {"type": "string"},
    "draft": {"type": "string"},
    "section_outline": {"type": "array", "items": {"type": "string"}},
    "notation_used": {"type": "array", "items": {"type": "string"}},
    "claim_evidence_map": {
      "type": "array",
      "items": {
        "type": "object",
        "required": ["claim", "support", "status"],
        "properties": {
          "claim": {"type": "string"},
          "support": {"type": "string"},
          "status": {"type": "string", "enum": ["supported", "bounded", "needs_evidence"]}
        }
      }
    },
    "reviewer_defense_notes": {"type": "array", "items": {"type": "string"}},
    "missing_inputs": {"type": "array", "items": {"type": "string"}}
  }
}
```
