# IEEE Figure Implementation Tutorials

## Ablation Figure Workflow

1. Confirm labels name exact mechanisms, such as `$\\mathcal{L}_{\\mathrm{con}}$`, `$\\lambda_{\\mathrm{SD}}$`, or negative sampling.
2. Confirm mean values and uncertainty values have matching lengths.
3. Confirm the uncertainty definition is available.
4. Add significance markers only when a named test and paired measurements are supplied.
5. Export a single-column figure unless more than six settings require a double-column width.

## OOD Result Workflow

1. Identify source and held-out target domains.
2. Choose a heatmap for transfer matrices or grouped point ranges for per-target comparisons.
3. Print the protocol name in the caption: LODO, unseen subject, unseen force, unseen session, or another explicitly defined split.
4. Use identical color scaling across comparable panels.
5. Include uncertainty across folds, seeds, or subjects.

## Feature Visualization Workflow

1. Validate the feature matrix shape.
2. Reduce with PCA or t-SNE using a fixed `random_state`.
3. Color by domain when arguing domain invariance.
4. Mark class or gesture with shape only if the plot remains legible.
5. Print silhouette score and intra-class variance from the reduced embedding.

## Radar Workflow

1. Use only normalized metrics in `[0, 1]`.
2. Use at least three metrics.
3. Keep method count low enough for a readable legend.
4. State normalization in the caption.
5. Pair the radar with a table or bar chart for primary numerical claims.
