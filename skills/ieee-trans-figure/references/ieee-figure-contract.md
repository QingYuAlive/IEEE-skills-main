# IEEE Figure Contract

Use this before drawing, revising, or auditing a figure.

## Contract Template

| Field | Required Answer |
|---|---|
| Core conclusion | What should the reader learn in one sentence? |
| Manuscript claim | Which claim does the figure support? |
| Evidence type | Main comparison, ablation, sensitivity, visualization, method, signal morphology, complexity |
| Data/protocol | Dataset, split, metric, repeats, target domain |
| Panel map | What each panel shows |
| Uncertainty | SD, SE, CI, p-value, repeated folds, or not applicable |
| Size | single-column, double-column, supplementary |
| Output | PDF/SVG/EPS/TIFF/PNG |
| Boundary | What the figure does not establish |

## Layout Defaults

- Single-column: 3.5 in wide.
- Double-column: 7.16 in wide.
- Common heights: 2.2-2.8 in for one-row single-column plots; 3.0-4.8 in for double-column multi-panel figures.
- Keep outer margins tight but not clipped.
- Use panel letters `(a)`, `(b)`, `(c)` consistently.
- Use shared axes when panels compare the same metric.
- Put legends outside dense plots when possible.

## Typography

- Use one sans-serif family consistently in generated plots.
- Axis labels should remain readable after scaling.
- Avoid tiny legends inside dense panels.
- Use mathematical symbols consistently with the manuscript notation.
- Do not overload titles; captions carry interpretation.

## Color and Encoding

- Use restrained, colorblind-aware palettes.
- For method comparison, keep the proposed method visually salient but not theatrical.
- Encode uncertainty with error bars, bands, or violin/box plots when repeated runs exist.
- For heatmaps, choose perceptually ordered maps and label colorbars with units.
- For confusion matrices, include class names or concise abbreviations and normalize policy.

## Export and Reproducibility

For generated figures, keep:

- Source data path or data-loading instruction.
- Plotting script.
- Exported vector/raster file.
- Random seed for dimensionality reduction.
- Notes on preprocessing used for visualization.

For final delivery, inspect:

- No clipped labels.
- No overlapping text.
- No unreadable tick labels.
- No inconsistent metric direction.
- No missing units.
- Caption matches the actual panels.
