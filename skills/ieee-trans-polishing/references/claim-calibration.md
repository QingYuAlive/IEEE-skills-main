# Claim Calibration

Use this reference to repair overclaiming, weak hedging, or unsupported novelty statements.

## Claim Strength Ladder

| Strength | Use When | Example Verb Set |
|---|---|---|
| Observation | Single table/figure or limited split | observe, find, show |
| Support | Result aligns with mechanism and ablation | support, indicate, suggest |
| Validation | Controlled experiment directly tests claim | validate, verify under this setting |
| Establishment | Multiple datasets, baselines, stats, ablations | demonstrate, establish |
| Proof | Formal theorem under assumptions | prove, guarantee |

Do not use a stronger level than the evidence allows.

## Common Repairs

Overclaim:

```text
The proposed method solves domain shift.
```

Repair:

```text
The proposed method improves recognition accuracy under the held-out force protocol, suggesting better tolerance to the force-induced distribution shift.
```

Overclaim:

```text
The t-SNE proves that the features are domain invariant.
```

Repair:

```text
The t-SNE projection shows more compact class-wise clusters and reduced visible separation across force levels, which is consistent with the quantitative improvements in the held-out-force results.
```

Weak novelty:

```text
We combine contrastive learning and regularization.
```

Repair:

```text
We define cross-force positive pairs at the window level and couple the resulting contrastive objective with logit regularization, so that class-discriminative features are smoothed across force-induced variations.
```

## Verbs for IEEE Prose

Use:

- formulate, derive, optimize, constrain, regularize, align, decouple, perturb, reconstruct, calibrate, evaluate.

Use carefully:

- demonstrate, validate, significant, robust, invariant, generalizable, state of the art.

Avoid unless proven:

- solve, eliminate, guarantee, fully, universally, unprecedented.

## Boundary Phrases

- under the evaluated protocol
- in the held-out target domains
- for the considered datasets
- relative to the selected baselines
- consistent with the ablation results
- suggesting rather than proving

Use boundary phrases to protect honest claims, not to weaken well-supported results.
