# Empirical Defense Checklist

Use this for reviewing experiments, tables, figures, and result claims.

## Protocol

- Are datasets named and described?
- Are preprocessing, normalization, filtering, windowing, and trial handling explicit?
- Are train/validation/test or source/target splits clear?
- Are seeds, folds, repeats, and checkpoint selection reported?
- Is target data unavailable during training when claiming DG?

## Baselines

Check for:

- Classical or feature-based baselines where field-relevant.
- Plain neural baselines with comparable input.
- Mechanism-specific baselines: DG, contrastive, uncertainty, IRM, adversarial, mixup, reconstruction, perturbation.
- Recent specialized methods.
- Fair hyperparameters and training budgets.

## Metrics

Classification:

- Accuracy plus macro-F1 or class-balanced metric when classes may be imbalanced.
- Confusion matrix for class-specific errors.

Domain generalization:

- Per-target-domain scores.
- Mean/std across targets or seeds.

Generation:

- Distribution metric.
- Temporal metric.
- Spectral metric.
- Task-transfer metric when possible.

Regression:

- RMSE/MAE and domain-specific score if standard.

## Ablations

Each proposed component should have:

- Removal.
- Replacement or simpler alternative.
- Hyperparameter sensitivity if governed by a weight/temperature/ratio.
- Same evaluation protocol as the main result.

## Visualization

Flag if:

- t-SNE/PCA is interpreted as proof.
- No seed or feature source is given.
- Colors encode too many variables.
- Confusion matrix lacks normalization policy.
- Spectral plots lack units or preprocessing.
- Topographic maps lack importance definition.

## Complexity

Require at least one:

- Parameters.
- FLOPs or asymptotic complexity.
- Memory.
- Throughput.
- Latency.
- Training overhead.

For real-time HMI or diagnosis, latency and inference path matter.
