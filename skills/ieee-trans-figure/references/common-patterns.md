# Common IEEE Plot Patterns

## Method Comparison With Uncertainty

Use grouped bars or point-range plots for method comparison across folds, subjects, or domains. Sort methods by experimental role: classical baseline, recent baseline, proposed variants, final method. Do not sort by result value when it hides the experimental design.

Required encodings:

- Mean or median.
- Error interval definition.
- Number of folds, seeds, or subjects.
- Statistical test when stars are used.

## Ablation Defense

Use ablation bars when the manuscript claims a loss, module, temperature, sampling policy, or normalization is necessary. The x-axis must name each removal or replacement precisely. The y-axis must state the metric and protocol.

Examples of precise labels:

- `w/o $\\mathcal{L}_{\\mathrm{SD}}$`
- `w/o positive-pair alignment`
- `$\\tau=0.05$`
- `full objective`

## Domain-Generalization Grid

Use a heatmap or grouped point plot when evaluating source-to-target transfer. Rows should be source domains and columns should be held-out target domains, or the reverse. The caption must state whether the protocol is LODO, unseen subject, unseen force, or unseen session.

## Feature Alignment Visualization

Use t-SNE or PCA only as supporting evidence. Pair the scatter with printed silhouette score or intra-class variance. Color by domain when the claim concerns invariance; use marker shape for class when both domain and label must be visible.

## Signal-Processing Trace

For sEMG, EEG, industrial time-series, or sensor traces:

- State sampling rate.
- Mark window boundaries if classification windows are plotted.
- Use consistent amplitude units.
- Overlay only a small number of traces; use summary bands for many trials.

## Complexity And Efficiency

Use line plots for runtime, memory, FLOPs, or parameter count against sequence length, channels, classes, or domains. Include asymptotic notation in the legend or caption, such as `$O(BTC)$` or `$O(N^2d)$`.
