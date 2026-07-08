# IEEE Evaluation Rubric

Compatibility file for the cloned proposal pipeline. Use `proposal-qa-rubric.md` as the primary rubric; this file mirrors the same IEEE Transactions readiness logic so older pipeline references do not fall back to generic narrative or non-IEEE scoring.

## Blocking Rule

If any of the following are missing, do not draft polished prose:

- Formal input space `\mathcal{X}` and label space `\mathcal{Y}`.
- Source environments and held-out OOD target environments.
- Predictor equations for encoder/projector/classifier.
- Empirical risk and total objective.
- Exact DG/contrastive/robustness constraint.
- OOD evaluation protocol.
- Ablation plan for every claimed module/loss.
- Complexity or deployment-cost plan when new modules are introduced.
- Theoretical assumptions and proof/convergence boundary if theory is claimed.

## 0-10 Dimensions

Score each dimension independently.

| Dimension | 3 | 5 | 7 | 9 |
|---|---|---|---|---|
| Formal problem | Narrative topic only | Dataset/task named | Spaces and domains mostly defined | `\mathcal{X}`, `\mathcal{Y}`, domains, target rule, assumptions complete |
| Equation-first method | Layer walkthrough | Module names only | Main mappings and losses present | All modules, objectives, weights, training, inference formalized |
| DG/OOD protocol | Random split | OOD implied | Held-out protocol present | Source/target, validation, seeds/folds, metrics, checkpoint and leakage rules explicit |
| Objective validity | CE only | Auxiliary losses named | Losses mostly defined | Empirical risk, IRM/GroupDRO/contrastive/etc., total objective and optimization complete |
| Theoretical support | Unsupported theory claim | Intuition only | Assumption/proposition partial | Assumptions, theorem/proof sketch, convergence/boundary tied to experiments |
| Empirical defense | Main accuracy only | Baselines listed | Baselines + some ablations | Baseline tiers, ablation matrix, sensitivity, stats, visualization and complexity |
| Claim calibration | Overclaims | Some hedging | Mostly protocol-bound | Every claim maps to formal object and evidence |

## Penalties

- Plain-English neural-network descriptions without equations: cap method score at 5.
- Robustness/generalization claim without OOD protocol: cap total readiness at internal sketch.
- Contrastive loss without pair definition: cap objective score at 5.
- No complexity discussion for added modules: cap empirical defense at 7.
- Theorem language without assumptions/proof boundary: cap theoretical support at 4.

## Recommendation Thresholds

```text
< 6.0    Blocked: formalization required
6.0-7.0  Internal method sketch
7.0-8.0  Draftable after targeted repairs
> 8.0    IEEE proposal foundation ready
```
