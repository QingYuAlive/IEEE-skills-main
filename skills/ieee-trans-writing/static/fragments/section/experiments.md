# Section: Experiments And Results

## Bulletproof Analysis Playbook

The Results section must actively defend the engineering claim. Do not write passive table narration such as "Table I shows our method is better." Each result paragraph must state the protocol, the comparison, the observed effect, the mechanism interpretation, and the claim boundary.

## Required Experiment Order

| Subsection | Required defense |
|---|---|
| Experimental Setup | Datasets, preprocessing, source-target splits, OOD protocol, metrics, seeds or folds, checkpoint rule, hardware, and implementation fairness. |
| Baseline Comparison | Classical baselines, backbone-matched deep baselines, domain-generalization or contrastive baselines, recent specialized methods, and internal variants. |
| OOD Generalization Analysis | Cross-subject, cross-session, cross-force, leave-one-domain-out, unseen-condition, or target-held-out evaluation tied to the claim. |
| Ablation Defense | Removal, replacement, and sensitivity tests for every proposed loss, operator, stage, pair construction, or reference component. |
| Mechanism Analysis | Quantitative representation metrics, confusion patterns, discrepancy measures, t-SNE or PCA with bounded interpretation, and class/domain compactness evidence. |
| Complexity And Practicality | Parameters, FLOPs, memory, latency, throughput, training overhead, and deployment path. |
| Failure Modes | Negative cases, weak domains, unstable hyperparameters, class confusions, and assumptions that limit transfer. |

## Paragraph Formula

Use this formula for each result paragraph:

```text
Protocol -> comparison -> measured effect -> mechanism interpretation -> boundary.
```

Example:

```text
Under leave-one-force-level-out evaluation, the full objective improves macro-F1 relative to the backbone-matched ERM baseline and the single-loss variants. The largest ablation drop occurs when the cross-force positive-pair loss is removed, which supports the role of `L_con` in reducing within-class force dispersion rather than merely increasing classifier capacity. This interpretation is limited to the tested force levels and checkpoint rule.
```

## Ablation Defense Rules

- A loss term is not necessary until removal or replacement reduces performance under the same protocol.
- A staged method needs stage-specific ablations, including reference source, frozen versus trainable components, and total budget fairness.
- A contrastive claim needs pair-construction ablations, temperature sensitivity, positive-count sensitivity, and negative-set policy when available.
- An invariant or robust claim needs the OOD protocol and failure cases.
- A visualization claim needs quantitative support such as silhouette score, Davies-Bouldin index, MMD, A-distance, intra-class variance, inter-class margin, or source-target discrepancy.

## t-SNE And Representation Analysis

Allowed interpretation:

```text
The t-SNE plot is consistent with tighter class-wise clustering on unseen domains because the same setting also reduces intra-class latent variance and improves target macro-F1.
```

Disallowed interpretation:

```text
The t-SNE plot proves that the learned representation is domain-invariant.
```

## Loss Alignment Documentation

For every loss term in the Method section, include one result-side defense:

| Loss term | Required result-side evidence |
|---|---|
| `L_cls` | Main task metric under the same split |
| `L_con` | Positive-pair or temperature ablation plus representation metric |
| `L_inv` | OOD target risk, domain discrepancy, or IRM penalty ablation |
| `L_dro` | Worst-domain or low-performing-domain improvement |
| `L_rec` | Reconstruction metric plus downstream utility |
| `L_reg` | Sensitivity curve and overfitting or calibration evidence |

## Input JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["setup", "baselines", "main_results", "ablation_results", "mechanism_results", "complexity_results", "failure_modes"],
  "properties": {
    "setup": {
      "type": "object",
      "required": ["datasets", "splits", "metrics", "checkpoint_rule", "seeds_or_folds"],
      "properties": {
        "datasets": {"type": "array", "items": {"type": "string"}},
        "splits": {"type": "array", "items": {"type": "string"}},
        "metrics": {"type": "array", "items": {"type": "string"}},
        "checkpoint_rule": {"type": "string"},
        "seeds_or_folds": {"type": "string"}
      }
    },
    "baselines": {"type": "array", "items": {"type": "string"}},
    "main_results": {"type": "array", "items": {"type": "object"}},
    "ablation_results": {"type": "array", "items": {"type": "object"}},
    "mechanism_results": {"type": "array", "items": {"type": "object"}},
    "complexity_results": {"type": "array", "items": {"type": "object"}},
    "failure_modes": {"type": "array", "items": {"type": "string"}}
  }
}
```

## Output JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["experiments_section", "result_claim_map", "ablation_defense_map", "visualization_limits", "complexity_claims", "missing_evidence"],
  "properties": {
    "experiments_section": {"type": "string"},
    "result_claim_map": {"type": "array", "items": {"type": "object"}},
    "ablation_defense_map": {"type": "array", "items": {"type": "object"}},
    "visualization_limits": {"type": "array", "items": {"type": "string"}},
    "complexity_claims": {"type": "array", "items": {"type": "string"}},
    "missing_evidence": {"type": "array", "items": {"type": "string"}}
  }
}
```

## Quality Gate

- Every table or figure is introduced by a claim, not by its label.
- Every comparison states dataset, split, metric, and checkpoint rule.
- Every proposed component has an ablation or is excluded from necessity claims.
- Every representation visualization is paired with a quantitative metric.
- Every robustness or generalization claim names the exact OOD target protocol.
- Every complexity claim includes measured or asymptotic cost.
