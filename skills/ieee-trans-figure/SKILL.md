---
name: ieee-trans-figure
description: >-
  Design, generate, revise, or audit IEEE Transactions manuscript figures for TCYB, THMS, and TNNLS, including ablation plots, performance comparisons, feature-space visualizations, t-SNE/PCA, confusion matrices, time-frequency/spectral plots, topographic maps, method diagrams, and multi-panel figures. Use for requests about IEEE论文图, 科研绘图, 消融图, t-SNE图, 混淆矩阵, 特征可视化, figure caption, or journal-ready vector export.
---

# IEEE Transactions Figure

Use this skill for IEEE Transactions-style manuscript figures and figure critique.

## Mandatory First Read

Read `../_shared/ieee-trans-guidelines.md` before figure work. It defines visualization as bounded evidence and gives the interpretation rules for feature plots, confusion matrices, spectra, and topographic maps.

## Backend Gate

If the user asks you to generate code or files and has not specified a backend, ask one concise question: `Python, R, MATLAB, or existing script?` Stop after asking. If the user only asks for design, caption, audit, or guidance, proceed without a backend.

Do not create mock scientific data unless the user explicitly asks for a schematic or template and the output is clearly labeled as schematic.

## Figure Contract

Before drawing or rewriting a caption, define:

- Core conclusion.
- Evidence type: main comparison, ablation, sensitivity, feature space, signal morphology, method overview, or complexity.
- Data/protocol: dataset, split, metric, seeds/folds, target condition.
- Panel map.
- Statistical or uncertainty display.
- Export target: single-column, double-column, or supplementary.
- Claim boundary.

Load `references/ieee-figure-contract.md` for the detailed contract and plotting constraints.

Load `references/ablation-and-feature-visualization.md` for ablation bars, t-SNE/PCA, confusion matrices, spectra, topographic maps, and sensitivity plots.

## IEEE Plotting Constraints

Use these as drafting defaults and verify against the target IEEE template before final submission:

- Single-column figure width: 3.5 in.
- Double-column figure width: 7.16 in.
- Keep panel lettering and tick labels legible after scaling.
- Prefer vector PDF/SVG/EPS for line art; use high-resolution TIFF/PNG only for raster images or heatmaps.
- Use colorblind-aware palettes and redundant encodings such as markers, line styles, or hatching.
- Avoid rainbow colormaps for quantitative heatmaps.
- Use consistent metric direction indicators, for example higher-is-better or lower-is-better.
- Keep captions self-contained: what, data/protocol, metric, panel meaning, statistical summary.

## Workflow

1. Determine whether the task is design, generation, audit, caption, or revision.
2. Build the figure contract.
3. Select the figure archetype.
4. Specify dimensions, palette, fonts, legends, axes, and export format.
5. Generate or revise using user data only.
6. Inspect for claim-evidence match, readability, and scaling.
7. Provide caption and reviewer-risk notes.

## Output Contract

For design/audit:

```text
Figure Contract
Panel Layout
Visual Encoding
Caption Draft
Reviewer Risks
```

For code generation:

```text
Figure Contract
Files Created
How To Reproduce
Export Checks
Caption Draft
```

## Red Lines

- Do not plot fabricated results as if they are experimental.
- Do not use t-SNE/PCA to claim proof of invariance.
- Do not hide error bars or variance when comparing repeated experiments.
- Do not use color alone to distinguish critical groups.
- Do not make legends, labels, or panels unreadable at IEEE column width.
- Do not let a caption imply an experiment not shown in the figure.
