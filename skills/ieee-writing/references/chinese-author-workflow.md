# Chinese Author Workflow For IEEE Transactions

Use this reference for Chinese, mixed Chinese-English, or lab-note input.

## Principle

Translate intent into a formal IEEE argument. Do not translate sentence order literally. Convert notes into claim, symbol, equation, protocol, evidence, and boundary before drafting English prose.

## Drafting Sequence

1. Summarize the author's intended technical claim in Chinese.
2. Extract formal objects: input, output, domains, predictor, losses, metrics, and protocol variables.
3. Identify missing evidence or boundary before drafting.
4. Draft English prose using the relevant section fragment.
5. Add brief Chinese notes only for structural choices, claim calibration, and missing inputs.

## Common Repairs

| Chinese-draft pattern | IEEE repair |
|---|---|
| Method described as a workflow | Convert workflow steps into operators, mappings, and objectives. |
| Result described as better | Add dataset, split, metric, baseline, checkpoint rule, and numerical support. |
| Robustness claimed generally | Bind the claim to an explicit unseen-domain or perturbation protocol. |
| Figure used as proof | Pair the figure with a quantitative metric or ablation. |
| Long topic-comment sentence | Split into formal claim, condition, evidence, and limitation. |

## Output JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["english_draft", "chinese_notes", "formal_objects", "missing_inputs"],
  "properties": {
    "english_draft": {"type": "string"},
    "chinese_notes": {"type": "array", "items": {"type": "string"}},
    "formal_objects": {"type": "array", "items": {"type": "string"}},
    "missing_inputs": {"type": "array", "items": {"type": "string"}}
  }
}
```
