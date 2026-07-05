# Ablation and Feature Visualization

Use this reference for common IEEE Transactions figure types.

## Ablation Bar or Line Plot

Required:

- Full model and each variant.
- Same split and metric as main comparison.
- Error bars when repeated runs exist.
- Clear naming of removed or replaced component.
- Metric direction indicator.

Interpretation:

```text
The drop caused by removing [component] is largest under [target split],
which supports the role of [component] in [mechanism]. The smaller change
under [source/in-domain split] suggests that the component mainly affects
generalization rather than source-domain fitting.
```

## Sensitivity Plot

Required:

- Hyperparameter range.
- Default value marker.
- Mean and variance.
- Stable interval.
- Failure at extremes if present.

Use for temperature, loss weights, perturbation ratio, sparsity coefficient, mix ratio, pretraining epochs, pair count.

## t-SNE/PCA/UMAP

Required:

- Feature source and checkpoint.
- Sample selection policy.
- Projection method and seed.
- Coloring by class, domain, subject, force, or modality.
- Same number of samples per group when feasible.

Safe interpretation:

- Compact class clusters support discriminability.
- Reduced visible domain separation supports alignment only qualitatively.
- Overlap alone does not prove invariance.
- Pair with accuracy/F1/domain-classifier/ablation evidence.

## Confusion Matrix

Required:

- Normalization policy.
- Same class order across panels.
- Per-class labels.
- Macro metric in caption or surrounding text.

Use the figure to identify hard classes, not merely to show a colorful square.

## Signal, Spectrum, and Time-Frequency Plots

Required:

- Units, sampling rate, preprocessing, and window length.
- Same scale across compared panels.
- Quantitative metric such as RMSE, MMD, DTW, or classification transfer when making fidelity claims.
- For generated signals, show both temporal and spectral evidence when possible.

## Topographic or Channel-Importance Maps

Required:

- How importance is computed.
- Channel montage or sensor layout.
- Colorbar and scale.
- Statistical or repeated-subject summary if making group-level claims.

Use bounded language when linking maps to physiology.

## Method Overview Figure

Required panels:

- Input and domain/source structure.
- Encoder and projection spaces.
- Losses attached to the correct representations.
- Training-only modules distinguished from inference modules.
- Stage boundary if two-stage.

Avoid decorative architecture boxes that do not show where the objective acts.
