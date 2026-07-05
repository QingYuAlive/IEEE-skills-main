# IEEE Experiments Reference Guide

Use this guide to plan or repair Results and Experiments sections for defensive IEEE review.

## Reviewer Question Matrix

| Reviewer question | Required experiment content |
|---|---|
| What exactly was tested? | Dataset, preprocessing, split, source domains, target domains, seeds or folds, checkpoint rule, and metric definitions |
| Was the comparison fair? | Baseline tiers, comparable input, comparable architecture capacity, comparable training budget, and disclosed tuning |
| Does the method generalize? | Unseen-domain protocol, cross-condition evaluation, target-held-out construction, and failure cases |
| Does each component matter? | Removal, replacement, and sensitivity ablations aligned to each loss or module |
| Is the mechanism plausible? | Representation metrics, discrepancy metrics, confusion analysis, and bounded visualization |
| Is the cost justified? | Parameters, FLOPs, memory, latency, throughput, or training overhead |

## Baseline Tiers

1. Classical feature or machine-learning baselines when field practice still uses them.
2. Plain deep baselines using comparable inputs and backbones.
3. Domain-generalization, invariant-learning, contrastive-learning, or robust-training baselines matching the claim type.
4. Recent specialized methods from the same signal, time-series, or industrial condition.
5. Internal ablations isolating every proposed mechanism.

## Result Paragraph Pattern

Use active defense:

```text
Under the named protocol, method A improves metric M relative to baseline B by the reported amount. The comparison is fair because the split, input, budget, and checkpoint rule are matched. The ablation or mechanism metric indicates that component C contributes through role R. The claim is bounded to condition D.
```

Do not output this pattern with generic variables. Replace it with the user's concrete protocol, method, metric, baseline, component, role, and boundary before drafting.

## Visualization Rules

- t-SNE and PCA support interpretation only when paired with quantitative representation metrics.
- Confusion matrices support class-level error analysis, not global robustness claims.
- Waveform and spectrum plots support signal preservation only when paired with temporal, spectral, or task metrics.
- Saliency and topographic maps support plausibility only when the sensor or physiology interpretation is bounded.

## Input JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["protocol", "baseline_tiers", "main_comparisons", "ablations", "mechanism_metrics", "complexity", "limitations"],
  "properties": {
    "protocol": {"type": "object"},
    "baseline_tiers": {"type": "array", "items": {"type": "object"}},
    "main_comparisons": {"type": "array", "items": {"type": "object"}},
    "ablations": {"type": "array", "items": {"type": "object"}},
    "mechanism_metrics": {"type": "array", "items": {"type": "object"}},
    "complexity": {"type": "array", "items": {"type": "string"}},
    "limitations": {"type": "array", "items": {"type": "string"}}
  }
}
```

## Output JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["experiments_text", "reviewer_question_matrix", "baseline_table", "ablation_table", "visualization_audit", "cost_audit"],
  "properties": {
    "experiments_text": {"type": "string"},
    "reviewer_question_matrix": {"type": "array", "items": {"type": "object"}},
    "baseline_table": {"type": "array", "items": {"type": "object"}},
    "ablation_table": {"type": "array", "items": {"type": "object"}},
    "visualization_audit": {"type": "array", "items": {"type": "object"}},
    "cost_audit": {"type": "array", "items": {"type": "object"}}
  }
}
```
