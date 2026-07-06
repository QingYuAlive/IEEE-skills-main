# Output Format For IEEE Transactions Polishing

## Default Markdown Output

Return results in this order:

1. `Route:` paper type, section, language, journal, and formality-gate status.
2. `Polished Text:` revised prose, not in a code block unless the user asks for LaTeX source.
3. `Before And After:` a compact table for major edits.
4. `Reviewer Defense Rationale:` why each major edit reduces rejection risk.
5. `Notation And Terminology Changes:` symbols or terms standardized during polishing.
6. `Formalization Flags:` sentences that still require equations, algorithms, objectives, protocols, or evidence from the author.
7. `Unresolved Author Inputs:` only items that block a defensible final polish.

## Before And After Table

| Before | After | Edit Type |
|---|---|---|
| Original claim or phrase | Revised IEEE-style wording | notation, protocol binding, claim calibration, ablation defense, equation integration, grammar |

## Reviewer Defense Rationale Table

| Edit | Rejection risk reduced | Rationale |
|---|---|---|
| Bounded a robustness claim to the held-out target protocol | OOD overclaiming | The revised sentence names the target split and avoids implying untested generalization. |
| Replaced a workflow description with equation-aware wording | Underformalized method | The revised sentence exposes the mapping and test-time modules. |
| Downgraded `prove` to `support` | Evidence inflation | The available result is empirical and does not constitute a theorem. |
| Added ablation language | Unsubstantiated necessity claim | The claim now depends on the removal or replacement experiment. |

## JSON Output Schema

Use this schema when the user requests structured output or when the polish is extensive:

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": [
    "route",
    "polished_text",
    "before_after",
    "reviewer_defense_rationale",
    "notation_and_terminology_changes",
    "formalization_flags",
    "unresolved_author_inputs"
  ],
  "properties": {
    "route": {"type": "string"},
    "polished_text": {"type": "string"},
    "before_after": {
      "type": "array",
      "items": {
        "type": "object",
        "required": ["before", "after", "edit_type"],
        "properties": {
          "before": {"type": "string"},
          "after": {"type": "string"},
          "edit_type": {"type": "string"}
        }
      }
    },
    "reviewer_defense_rationale": {
      "type": "array",
      "items": {
        "type": "object",
        "required": ["edit", "rejection_risk_reduced", "rationale"],
        "properties": {
          "edit": {"type": "string"},
          "rejection_risk_reduced": {"type": "string"},
          "rationale": {"type": "string"}
        }
      }
    },
    "notation_and_terminology_changes": {"type": "array", "items": {"type": "string"}},
    "formalization_flags": {"type": "array", "items": {"type": "string"}},
    "unresolved_author_inputs": {"type": "array", "items": {"type": "string"}}
  }
}
```

## Blocked Output

If the formality gate fails, return:

```json
{
  "status": "blocked_by_formality_gate",
  "blocked_text": "The underformalized sentence or paragraph.",
  "missing_formal_objects": [
    "LaTeX equation",
    "objective term",
    "source-target protocol",
    "ablation evidence",
    "complexity metric"
  ],
  "polished_text": null
}
```
