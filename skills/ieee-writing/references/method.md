# IEEE Method Reference Guide

Use this guide when the Method section needs deeper equation planning, algorithm extraction, or complexity repair.

## Operator Ledger

Before prose, build an operator ledger:

| Operator type | Required definition |
|---|---|
| Input operator | Windowing, normalization, augmentation, transform, modality split, or graph construction |
| Encoder | Mapping from input tensor to representation with shape |
| Projector | Mapping from representation to contrastive or alignment space |
| Predictor | Mapping from representation to label or continuous output |
| Constraint | Loss, penalty, adversary, reconstruction objective, uncertainty term, or robust optimization objective |
| Optimizer | Update rule, training stage, frozen component, checkpoint rule, and inference path |

## Loss Alignment Table

Every objective term must have the following row:

| Field | Required content |
|---|---|
| Equation | Exact loss or penalty |
| Role | Mechanistic claim made by the paper |
| Coefficient | Weight, tuning policy, uncertainty parameter, or scheduling rule |
| Ablation | Removal, replacement, or sensitivity test |
| Inference impact | Whether the module remains, is discarded, or changes test-time cost |

## Stage-Wise Method Rule

If a method has pretraining, reference guidance, teacher-student learning, alternating updates, or fine-tuning, write each stage as a separate optimization problem:

1. Stage objective and trainable modules.
2. Checkpoint selection rule.
3. Reused or frozen components.
4. Stage interaction claim.
5. Ablation that isolates the stage interaction.

## Complexity Reporting

Report at least one of:

- Parameter count.
- FLOPs or multiply-adds.
- Memory footprint.
- Training overhead.
- Inference latency or throughput.
- Asymptotic complexity for pairwise, graph, attention, adversarial, or generative components.

## Input JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["operator_ledger", "loss_alignment_table", "training_stages", "complexity_items"],
  "properties": {
    "operator_ledger": {"type": "array", "items": {"type": "object"}},
    "loss_alignment_table": {"type": "array", "items": {"type": "object"}},
    "training_stages": {"type": "array", "items": {"type": "object"}},
    "complexity_items": {"type": "array", "items": {"type": "string"}}
  }
}
```

## Output JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["method_text", "operator_ledger", "loss_alignment_table", "algorithm_box", "complexity_note"],
  "properties": {
    "method_text": {"type": "string"},
    "operator_ledger": {"type": "array", "items": {"type": "object"}},
    "loss_alignment_table": {"type": "array", "items": {"type": "object"}},
    "algorithm_box": {"type": "array", "items": {"type": "string"}},
    "complexity_note": {"type": "string"}
  }
}
```
