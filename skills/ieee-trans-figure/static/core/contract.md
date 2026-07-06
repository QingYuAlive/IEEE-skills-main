# Core IEEE Figure Contract

## Mission

Generate executable Python figures that can survive IEEE Transactions review. Every figure must expose the underlying measurement, model comparison, uncertainty, domain split, and notation. Visual style serves technical verification.

## Blocking Input Schema

The agent must collect or infer this schema before writing code:

```json
{
  "figure_id": "Fig. 1",
  "target_width": "single-column or double-column",
  "panels": [
    {
      "panel_id": "(a)",
      "plot_type": "ablation_bar, line_trend, heatmap, embedding, radar, complexity, signal_trace, confusion_matrix",
      "data_source": "array, table path, dataframe columns, or mathematical function",
      "x_definition": "variable name, unit, and ordering",
      "y_definition": "metric name, unit, and aggregation rule",
      "uncertainty": "std, sem, confidence interval, bootstrap interval, or none with justification",
      "statistical_test": "paired t-test, Wilcoxon, bootstrap, permutation test, or not applicable",
      "domain_protocol": "LODO, unseen target, subject-wise split, force-level split, or not applicable",
      "math_notation": ["$\\mathcal{X}$", "$G_\\theta$", "$\\lambda$"]
    }
  ],
  "exports": ["PDF", "PNG"],
  "manuscript_claim_supported": "bounded claim stated in technical terms"
}
```

If `data_source`, `target_width`, or `y_definition` is missing, stop and request it.

## Required Dimensions

Use exact IEEE widths:

| Layout | Width | Typical Height Rule |
| --- | ---: | --- |
| Single column | `3.5 in` (`88.9 mm`) | `2.1-2.8 in` unless panel density requires more |
| Double column | `7.16 in` (`181.8 mm`) | `3.0-4.6 in` for multi-panel technical composites |

Never use slide, poster, square social-media, or arbitrary notebook dimensions.

## Typography

- Allowed fonts only: Arial, Helvetica, Times New Roman.
- Title size: `10 pt`.
- Axis label size: `9 pt`.
- Legend and tick label size: `8 pt`.
- Do not use bold font weight on axes, ticks, legends, or panel labels.
- Use LaTeX math for all variables: `$\\mathcal{X}$`, `$\\mathcal{Y}$`, `$G_\\theta$`, `$\\tau$`.

## Color And Encoding

Use high-contrast, colorblind-aware colors suitable for grayscale conversion:

- Deep blue `#005AB5`
- Red `#DC3220`
- Green `#009E73`
- Black `#000000`
- Gray `#666666`
- Orange `#E69F00`
- Sky blue `#56B4E9`
- Purple `#7B3294`

Do not use low-contrast soft editorial palettes. Encode critical comparisons with line style, marker, hatch, or direct labels in addition to color.

## Mathematical Rendering

Every generated script must set:

```python
rcParams["text.usetex"] = True
```

If the local LaTeX installation is unavailable, report the environment failure. Do not silently fall back to non-LaTeX math when the figure is intended for final IEEE submission.

## Statistical Defense

- Ablation bars require error bars and significance marks when multiple seeds, folds, or subjects exist.
- OOD/domain-generalization plots must show the split protocol, for example `LODO`, unseen target force, unseen subject, or source-to-target domain pair.
- Feature visualizations must print at least one numeric compactness/separation metric, such as silhouette score or intra-class variance.
- Complexity plots must state asymptotic time and memory notation in the caption or legend.

## Export Contract

Export `PDF` for vector submission and `PNG` at `600 dpi` for inspection. Use embedded fonts for vector files and a tight bounding box. Never crop axis labels, legends, panel labels, or math notation.
