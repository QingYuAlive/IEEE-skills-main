# IEEE Caption And Legend Conventions

## Caption Structure

Use this compact structure:

```text
Fig. 3. Bounded accuracy improvement under held-out force evaluation. (a) Mean macro-F1 under LODO evaluation with 95% bootstrap confidence intervals. (b) Ablation of $\\mathcal{L}_{\\mathrm{con}}$ and $\\lambda_{\\mathrm{SD}}$ under the same split. (c) Runtime scaling with sequence length and $O(BTC)$ reference slope. Stars denote paired Wilcoxon tests with Holm correction; the source/target protocol is LODO.
```

Every caption must include enough information for a reviewer to understand the plotted protocol without searching the experiments section.

## Legend Rules

- Legends identify methods, domains, or loss variants, not prose descriptions.
- Use manuscript notation when relevant, such as `$\\mathcal{L}_{\\mathrm{con}}$` or `$G_\\theta$`.
- Keep legend labels short enough to fit at `8 pt`.
- Use one shared legend for repeated method sets across panels.

## Panel Labels

- Use `(a)`, `(b)`, `(c)` in normal weight.
- Place labels consistently at the upper-left of each axis or just outside the axis when space is tight.
- Do not use labels as decorative titles; the axis title should remain technical.

## Statistical Notes

State:

- Test name.
- Number of seeds, subjects, folds, or trials.
- Definition of interval.
- Multiple-comparison correction when used.

Example:

```text
Error bars denote 95% bootstrap confidence intervals across subjects; * and ** denote paired Wilcoxon tests with Holm correction at p<0.05 and p<0.01.
```
