# IEEE Article Architecture

Use this reference when rebuilding a full manuscript argument or checking whether a section sequence can survive IEEE Transactions review.

## Full-Paper Argument

```text
formal task -> source-target difficulty -> mathematical mechanism -> algorithmic implementation -> protocol-bound evidence -> ablation defense -> complexity and limitation
```

If one link is missing, report the missing link before drafting prose.

## Section Sequence

| Section | Required job |
|---|---|
| Abstract | Compress task, limitation, mechanism, algorithmic innovation, and verified evidence. |
| Introduction | Define the task, explain OOD failure, introduce the technical mechanism, and list categorized contributions. |
| Related Work | Synthesize prior work by technical obstacle and end each group with the unresolved formal boundary. |
| Method | Define notation, mappings, objectives, algorithm, inference path, and complexity. |
| Experiments | Defend protocol, fairness, OOD coverage, ablations, mechanism evidence, and cost. |
| Discussion | Explain why the mechanism helps, where it fails, and what evidence limits the claim. |
| Conclusion | Restate the bounded contribution, decisive evidence, and remaining boundary. |

## Reviewer Defense Ladder

1. Protocol: source domains, target domains, split, seeds or folds, checkpoint rule, and metrics.
2. Fairness: baseline families, input parity, architecture capacity, training budget, and tuning disclosure.
3. Mechanism: each loss or module has an ablation and an interpretation metric.
4. Scope: claims remain tied to domains, subjects, sessions, force levels, or operating conditions.
5. Cost: added modules justify their parameters, FLOPs, memory, latency, or training overhead.

## Output JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["argument_chain", "section_plan", "defense_ladder", "missing_links"],
  "properties": {
    "argument_chain": {"type": "array", "items": {"type": "string"}},
    "section_plan": {"type": "array", "items": {"type": "object"}},
    "defense_ladder": {"type": "array", "items": {"type": "object"}},
    "missing_links": {"type": "array", "items": {"type": "string"}}
  }
}
```
