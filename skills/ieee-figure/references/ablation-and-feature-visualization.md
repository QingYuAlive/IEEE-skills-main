# Ablation And Feature Visualization Rules

## Ablation Panels

Ablation panels must defend a specific mathematical or algorithmic component. The x-axis should name the removed term, altered hyperparameter, or replaced module. The y-axis should state the metric, unit, and evaluation protocol.

Required elements:

- Mean performance over folds, seeds, subjects, or trials.
- Error bars with a declared interval type.
- Significance marks only with a named statistical test.
- Labels tied to manuscript notation, such as `$\\mathcal{L}_{\\mathrm{con}}$`, `$\\lambda_{\\mathrm{SD}}$`, or `$\\tau$`.

The panel is invalid if it merely shows that the final method is higher without isolating the proposed mechanism.

## Feature Visualization Panels

t-SNE and PCA panels are diagnostic, not standalone proof. They must be paired with numeric compactness or separation evidence.

Required elements:

- Fixed random state for stochastic reduction.
- Domain color when the claim concerns invariance or OOD behavior.
- Class or gesture marker only when readable at IEEE width.
- Printed silhouette score or intra-class variance.
- Caption statement linking the visualization to the exact protocol.

Do not use feature scatterplots to imply robustness beyond the tested domains.
