# IEEE Chart-Type Rules

## Bar And Point-Range Charts

Use for method comparison, ablation, and metric summaries. Include error bars for repeated measurements. Prefer point-range charts when many methods would make bars dense.

## Line Charts

Use for training convergence, sensitivity sweeps, runtime scaling, and perturbation severity. Show uncertainty bands when multiple seeds or folds exist. Do not smooth curves unless the smoothing equation and window are stated.

## Heatmaps

Use for source-to-target transfer matrices, confusion matrices, attention maps, or pairwise distances. Use a perceptually ordered colormap and print numerical values when the grid is small enough to read.

## Embedding Scatterplots

Use PCA or t-SNE for feature diagnostics. Always compute a quantitative companion metric. Use domain color and class marker only when both encodings remain legible at IEEE width.

## Radar Charts

Use for normalized multi-metric comparison across domain-generalization protocols. All values must lie in `[0, 1]`, and the caption must define the normalization. Do not use radar charts as the only evidence for a primary accuracy claim.

## Box, Violin, And Distribution Plots

Use when the distribution shape matters, for example subject-level variance or trial-level stability. State sample count. Do not replace error bars with distribution plots when the manuscript claim is about mean performance.

## Complexity Plots

Use log scale only when complexity spans orders of magnitude. Annotate theoretical slopes or asymptotic statements when comparing algorithms.
