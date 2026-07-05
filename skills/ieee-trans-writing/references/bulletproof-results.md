# Bulletproof Results

Use this reference for Experiments, Results, Discussion, and response to reviewer-style evidence concerns.

## Result Paragraph Formula

```text
Claim:
  What the table/figure tests.

Protocol:
  Dataset, split, metric, seeds/folds, checkpoint.

Observation:
  Direction and magnitude of the result.

Mechanism:
  Why the result matches or challenges the proposed mechanism.

Boundary:
  Where the evidence is limited.
```

## Main Comparison

A main comparison table should not stand alone. Surround it with:

- Why these baselines are the right tiers.
- Which baselines test architecture capacity.
- Which baselines test the same mechanism family.
- Whether all methods share preprocessing, training budget, and checkpoint selection.
- How many repeats or folds are averaged.

## Ablation Interpretation

Use an ablation table as a causal map, not as decoration.

Good sentence pattern:

```text
Removing the cross-domain contrastive term reduces performance mainly
on the held-out force split, which supports the claim that the term
acts on domain transfer rather than only in-domain discrimination.
```

Avoid:

```text
The ablation proves our module is effective.
```

## Sensitivity Analysis

For hyperparameters, report:

- Tested range.
- Stable interval.
- Failure behavior at extremes.
- Chosen default and whether it was tuned on validation data.

Use this for temperatures, loss weights, perturbation ratios, sparsity penalties, stage epochs, and pair counts.

## Visualization Paragraphs

t-SNE/PCA:

- State embedding source and samples.
- Interpret compactness/separation/alignment.
- Connect to a numeric metric or ablation.
- Avoid saying it proves invariance.

Confusion matrix:

- Name the hard classes.
- Relate errors to signal similarity, force/domain shift, or label ambiguity.
- Connect to macro-F1 or per-class accuracy.

Spectrum/waveform:

- State whether temporal morphology and frequency profile match.
- Add RMSE, MMD, DTW, or task transfer if available.

Topographic/importance map:

- Explain perturbation or importance computation.
- Tie patterns to physiological expectations only with bounded language.

## Complexity Paragraph

Include at least one of:

- Number of parameters.
- FLOPs or computational complexity.
- GPU memory.
- Throughput or latency.
- Training overhead.

Then explain why the cost is acceptable for the task.
