# IEEE Figure Design Theory

## Principle

An IEEE Transactions figure is an engineering proof surface. Its design must make the measurement protocol, mathematical object, and empirical defense visible with minimum decorative load.

## Visual Hierarchy

Rank visual emphasis in this order:

1. Quantity being measured.
2. Protocol under which it is measured.
3. Method or mechanism being compared.
4. Uncertainty and statistical relation.
5. Secondary annotations.

Use color only after axes, labels, line styles, markers, and grouping already encode the comparison.

## Panel Composition

Use rectangular grids with aligned axes whenever panels share metrics. Use separate axes only when scales differ. Maintain consistent x-ordering across ablation, baseline, and sensitivity panels so the reader can compare without re-parsing the figure.

Recommended composites:

- `Method comparison + ablation + OOD split`: double-column, three panels.
- `Signal trace + feature embedding + confusion matrix`: double-column, three panels.
- `Sensitivity to $\\lambda$ + sensitivity to $\\tau$`: single-row double-column or two single-column figures.
- `Runtime + memory`: paired line charts with shared x-axis.

## Spacing

- Keep outer margins tight but never crop math.
- Prefer `constrained_layout=True` for multi-panel figures when LaTeX labels are long.
- Keep legends inside unused whitespace only when they do not obscure data.
- Use one global legend for multi-panel comparisons with identical methods.

## Axes

- Label every axis with metric and unit.
- Avoid unlabeled normalized scores. State the normalization interval or equation.
- Use linear scales unless the data or theory requires log scale.
- For log axes, mark powers clearly and state whether zeros were excluded or shifted.

## Lines, Markers, And Bars

- Use line width near `1.2 pt` and axis spine width near `0.8 pt`.
- Use markers for method curves in addition to color.
- Use hatches on bars when grayscale readability matters.
- Error bars must have caps and must identify whether they are `std`, `sem`, confidence intervals, or bootstrap intervals.

## Mathematical Labels

Equations and operators in the manuscript should map directly to visual encodings:

- Loss curves: `$\\mathcal{L}_{\\mathrm{ERM}}$`, `$\\mathcal{L}_{\\mathrm{con}}$`, `$\\mathcal{L}_{\\mathrm{IRM}}$`.
- Hyperparameters: `$\\lambda$`, `$\\tau$`, `$\\rho$`.
- Spaces and mappings: `$\\mathcal{X}$`, `$\\mathcal{Y}$`, `$\\mathcal{Z}$`, `$G_\\theta$`, `$h_\\phi$`.
- Domains: `$\\mathcal{E}_{s}$`, `$\\mathcal{E}_{t}$`, `$\\mathcal{D}_{\\mathrm{test}}$`.

## Rejection-Risk Controls

- Do not let a feature plot stand alone as proof of generalization.
- Do not show only best-seed curves.
- Do not hide weak baselines by changing axis limits.
- Do not claim practical efficiency without runtime or parameter counts.
- Do not claim robustness without showing the exact perturbation, subject, force, or domain protocol.
