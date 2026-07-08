# IEEE Engineering Stance

## Visual Philosophy

IEEE Transactions figures are technical evidence, not visual persuasion. Optimize for reproducibility, compactness, auditability, and reviewer defense.

The figure should answer these questions immediately:

1. What quantity is measured?
2. Under which split, subject, source/target domain, force level, seed, or fold was it measured?
3. What uncertainty or statistical test supports the comparison?
4. Which mathematical operator, loss term, module, or constraint is being isolated?
5. Which claim in the manuscript does the panel defend?

## Default Figure Behavior

- Prefer dense, readable panels over decorative composition.
- Prefer direct labels, exact metric names, and defined units.
- Use equations in axis labels or captions when the plotted quantity is a loss, penalty, bound, or operator.
- Keep the palette restrained and high-contrast.
- Keep line widths, markers, hatches, and spacing consistent across panels.
- Make all code deterministic through fixed seeds when dimensionality reduction or bootstrapping is used.

## Prohibited Behavior

- Do not invent data.
- Do not draw data-free conceptual visuals.
- Do not hide weak uncertainty behind smoothed curves.
- Do not make robustness or generalization visually appear broader than the test protocol.
- Do not use decorative backgrounds, shaded flourishes, or ornamental panel framing.
- Do not inspect or modify files in `assets/`.

## Reviewer-Oriented Heuristic

For each panel, write one sentence before coding:

`Panel (x) supports claim C by plotting metric M under protocol P with uncertainty U and statistical comparison S.`

If the sentence cannot be completed using supplied data, block the plot and request the missing input.
