# IEEE Transactions Figure Contract

## Required Deliverable

The figure deliverable is a reproducible Python script, not a hand-tuned visual. The script must load explicit user data, validate shapes and units, configure IEEE style, render variables through LaTeX, and export both vector and inspection formats.

## Layout Specification

| Target | Width | Use Case |
| --- | ---: | --- |
| Single column | `3.5 in` (`88.9 mm`) | One comparison, one ablation, one signal panel, compact embedding |
| Double column | `7.16 in` (`181.8 mm`) | Multi-panel evidence, source/target domain grid, method/ablation/feature composite |

Height is evidence-driven. Keep single-column panels near `2.1-2.8 in` and double-column composites near `3.0-4.6 in` unless the data density requires otherwise.

## Typography Rules

- Use only Arial, Helvetica, or Times New Roman.
- Figure title: `10 pt`.
- Axis labels: `9 pt`.
- Legend labels and tick labels: `8 pt`.
- Axis labels, ticks, legends, and panel letters use normal weight.
- Variables must be enclosed in LaTeX math delimiters, for example `$\\mathcal{X}$`, `$\\mathcal{Y}$`, `$G_\\theta$`, `$\\lambda$`, `$\\tau$`.

## Color Rules

Use high-contrast, colorblind-aware colors and redundant encodings:

```python
IEEE_COLORS = {
    "blue": "#005AB5",
    "red": "#DC3220",
    "green": "#009E73",
    "black": "#000000",
    "gray": "#666666",
    "orange": "#E69F00",
    "sky": "#56B4E9",
    "purple": "#7B3294",
}
```

Avoid soft, low-contrast, decorative palettes. Critical method distinctions must remain visible in grayscale through marker, hatch, line style, or direct label.

## Mathematical Integration

Set `rcParams["text.usetex"] = True` in every script. Match manuscript notation exactly: if the method section defines `$G_\\theta: \\mathcal{X} \\rightarrow \\mathcal{Z}$`, the figure label must not rename it to `Encoder` unless the caption explicitly maps the terms.

## Evidence Requirements By Claim

| Claim Type | Figure Must Show |
| --- | --- |
| Higher accuracy | Mean, uncertainty, sample count or fold count, and statistical comparison |
| Better OOD generalization | Source/target domains, held-out domain protocol, and unseen-domain metric |
| Robust feature alignment | Feature visualization plus silhouette score or intra-class variance |
| Necessary loss term | Ablation of each loss component, including error bars and significance marks |
| Efficient algorithm | Runtime or memory curve plus asymptotic notation |
| Stable training | Seed/fold variability and convergence trend |

## Final QA

Before delivery, verify:

- The code never fabricates arrays.
- All panel labels and legends fit at IEEE width.
- The plot uses exact dimensions.
- The figure can be regenerated from the script.
- PDF and PNG exports are generated from the same figure object.
- No operation reads image or PDF files from `assets/`.
