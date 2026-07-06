# Python Backend: Mandatory IEEE Plotting Template

Use Python only. Generated code must be executable and must not depend on files in `assets/`. Every script must include `ieee_style_setup()` and call it before creating any figure.

## Required Imports And Style Block

```python
from __future__ import annotations

from pathlib import Path
from typing import Mapping, Sequence

import matplotlib as mpl
import matplotlib.pyplot as plt
import numpy as np
import pandas as pd
import seaborn as sns


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


def ieee_style_setup() -> None:
    """Configure Matplotlib for IEEE Transactions figures."""
    mpl.rcParams.update({
        "text.usetex": True,
        "font.family": "serif",
        "font.serif": ["Times New Roman"],
        "font.sans-serif": ["Arial", "Helvetica"],
        "axes.titlesize": 10,
        "axes.labelsize": 9,
        "xtick.labelsize": 8,
        "ytick.labelsize": 8,
        "legend.fontsize": 8,
        "font.weight": "normal",
        "axes.titleweight": "normal",
        "axes.labelweight": "normal",
        "axes.linewidth": 0.8,
        "lines.linewidth": 1.2,
        "lines.markersize": 4.0,
        "patch.linewidth": 0.8,
        "legend.frameon": False,
        "figure.dpi": 300,
        "savefig.dpi": 600,
        "savefig.bbox": "tight",
        "savefig.pad_inches": 0.02,
        "pdf.fonttype": 42,
        "ps.fonttype": 42,
        "svg.fonttype": "none",
    })
    sns.set_theme(context="paper", style="whitegrid", rc={
        "font.family": "serif",
        "font.serif": ["Times New Roman"],
        "axes.edgecolor": IEEE_COLORS["black"],
        "grid.color": "#D9D9D9",
        "grid.linewidth": 0.5,
    })


def ieee_figure_size(width: str, height: float | None = None) -> tuple[float, float]:
    """Return IEEE figure size in inches."""
    widths = {
        "single": 3.5,
        "single-column": 3.5,
        "double": 7.16,
        "double-column": 7.16,
    }
    if width not in widths:
        raise ValueError("width must be 'single-column' or 'double-column'")
    fig_width = widths[width]
    fig_height = height if height is not None else fig_width * 0.62
    return fig_width, fig_height


def save_ieee_figure(fig: plt.Figure, output_stem: str | Path) -> None:
    """Save vector and inspection copies with IEEE-compatible settings."""
    output_stem = Path(output_stem)
    output_stem.parent.mkdir(parents=True, exist_ok=True)
    fig.savefig(output_stem.with_suffix(".pdf"), format="pdf")
    fig.savefig(output_stem.with_suffix(".png"), format="png", dpi=600)
```

## Ablation Bar Chart Requirements

Ablation bars must include uncertainty and significance marks whenever repeated runs, folds, or subjects are available. The plotted comparison must isolate a named mechanism such as `$\\mathcal{L}_{\\mathrm{con}}$`, `$\\lambda_{\\mathrm{SD}}$`, temperature `$\\tau$`, or a negative-sampling policy.

```python
def add_significance_bar(
    ax: plt.Axes,
    x0: float,
    x1: float,
    y: float,
    text: str,
    height: float,
) -> None:
    ax.plot([x0, x0, x1, x1], [y, y + height, y + height, y],
            color=IEEE_COLORS["black"], linewidth=0.8)
    ax.text((x0 + x1) / 2.0, y + height, text, ha="center", va="bottom",
            fontsize=8, fontweight="normal")


def plot_ablation_bar(
    labels: Sequence[str],
    means: Sequence[float],
    errors: Sequence[float],
    ylabel: str,
    output_stem: str | Path,
    significance: Mapping[tuple[int, int], str] | None = None,
    width: str = "single-column",
) -> None:
    ieee_style_setup()
    labels = list(labels)
    means = np.asarray(means, dtype=float)
    errors = np.asarray(errors, dtype=float)
    if len(labels) != means.size or means.size != errors.size:
        raise ValueError("labels, means, and errors must have the same length")

    fig, ax = plt.subplots(figsize=ieee_figure_size(width))
    x = np.arange(means.size)
    colors = [IEEE_COLORS["gray"]] * means.size
    colors[-1] = IEEE_COLORS["blue"]
    ax.bar(x, means, yerr=errors, capsize=3, color=colors,
           edgecolor=IEEE_COLORS["black"], linewidth=0.8)
    ax.set_xticks(x)
    ax.set_xticklabels(labels, rotation=25, ha="right")
    ax.set_ylabel(ylabel)
    ax.set_xlabel("Ablation setting")

    if significance:
        top = float(np.max(means + errors))
        span = max(float(np.ptp(means)), 1.0)
        for level, ((i, j), stars) in enumerate(significance.items(), start=1):
            add_significance_bar(ax, i, j, top + 0.05 * span * level, stars, 0.02 * span)

    ax.margins(x=0.04)
    fig.tight_layout()
    save_ieee_figure(fig, output_stem)
```

## Feature Visualization Requirements

t-SNE/PCA plots must compute and print a numerical compactness or separation diagnostic. Use silhouette score when at least two classes are present. Also report mean intra-class variance in the plotted space.

```python
def summarize_embedding_quality(embedding: np.ndarray, labels: Sequence[int | str]) -> dict[str, float]:
    from sklearn.metrics import silhouette_score

    embedding = np.asarray(embedding, dtype=float)
    labels = np.asarray(labels)
    if embedding.ndim != 2 or embedding.shape[1] != 2:
        raise ValueError("embedding must have shape (n_samples, 2)")

    unique_labels = np.unique(labels)
    variances = []
    for value in unique_labels:
        points = embedding[labels == value]
        if points.shape[0] > 1:
            variances.append(float(np.mean(np.var(points, axis=0))))
    intra_class_variance = float(np.mean(variances)) if variances else float("nan")

    if unique_labels.size > 1 and embedding.shape[0] > unique_labels.size:
        silhouette = float(silhouette_score(embedding, labels))
    else:
        silhouette = float("nan")
    metrics = {"silhouette": silhouette, "intra_class_variance": intra_class_variance}
    print(metrics)
    return metrics


def plot_embedding(
    features: np.ndarray,
    labels: Sequence[int | str],
    domains: Sequence[int | str],
    output_stem: str | Path,
    reducer: str = "tsne",
    width: str = "double-column",
) -> None:
    from sklearn.decomposition import PCA
    from sklearn.manifold import TSNE

    ieee_style_setup()
    features = np.asarray(features, dtype=float)
    labels = np.asarray(labels)
    domains = np.asarray(domains)
    if reducer == "tsne":
        model = TSNE(n_components=2, perplexity=30, init="pca", learning_rate="auto", random_state=7)
    elif reducer == "pca":
        model = PCA(n_components=2, random_state=7)
    else:
        raise ValueError("reducer must be 'tsne' or 'pca'")

    embedding = model.fit_transform(features)
    summarize_embedding_quality(embedding, labels)

    fig, ax = plt.subplots(figsize=ieee_figure_size(width, height=3.2))
    palette = [IEEE_COLORS["blue"], IEEE_COLORS["red"], IEEE_COLORS["green"],
               IEEE_COLORS["orange"], IEEE_COLORS["purple"], IEEE_COLORS["black"]]
    for k, value in enumerate(np.unique(domains)):
        mask = domains == value
        ax.scatter(embedding[mask, 0], embedding[mask, 1], s=12, alpha=0.80,
                   color=palette[k % len(palette)], label=fr"domain ${value}$",
                   edgecolors="none")
    ax.set_xlabel(fr"{reducer.upper()}-1")
    ax.set_ylabel(fr"{reducer.upper()}-2")
    ax.legend(loc="best", ncol=2)
    fig.tight_layout()
    save_ieee_figure(fig, output_stem)
```

## Radar Chart Requirements

Radar charts are allowed only for normalized multi-metric comparison under clearly defined domain-generalization protocols. They must not replace the main numerical table.

```python
def plot_domain_radar(
    metrics: Sequence[str],
    series: Mapping[str, Sequence[float]],
    output_stem: str | Path,
    width: str = "single-column",
) -> None:
    ieee_style_setup()
    metrics = list(metrics)
    if len(metrics) < 3:
        raise ValueError("radar charts require at least three metrics")
    angles = np.linspace(0, 2 * np.pi, len(metrics), endpoint=False)
    closed_angles = np.r_[angles, angles[0]]

    fig, ax = plt.subplots(figsize=ieee_figure_size(width), subplot_kw={"projection": "polar"})
    colors = list(IEEE_COLORS.values())
    for idx, (name, values) in enumerate(series.items()):
        values = np.asarray(values, dtype=float)
        if values.size != len(metrics):
            raise ValueError(f"{name} has {values.size} values but {len(metrics)} metrics were provided")
        if np.any(values < 0.0) or np.any(values > 1.0):
            raise ValueError("radar values must be normalized to [0, 1]")
        closed_values = np.r_[values, values[0]]
        ax.plot(closed_angles, closed_values, color=colors[idx % len(colors)],
                linewidth=1.2, marker="o", label=name)
        ax.fill(closed_angles, closed_values, color=colors[idx % len(colors)], alpha=0.08)

    ax.set_xticks(angles)
    ax.set_xticklabels(metrics)
    ax.set_ylim(0.0, 1.0)
    ax.set_yticks([0.25, 0.50, 0.75, 1.00])
    ax.legend(loc="upper center", bbox_to_anchor=(0.5, -0.10), ncol=2)
    fig.tight_layout()
    save_ieee_figure(fig, output_stem)
```

## Code Generation Rules

- Validate array shapes before plotting.
- Keep all variable names and labels consistent with manuscript notation.
- Use hatches or markers when color alone carries an important comparison.
- Print summary statistics used to create the plot.
- Use `random_state` for stochastic reducers and bootstraps.
- Export PDF and PNG from the same figure object.
- Avoid notebook-only state, hidden global data, or interactive GUI calls.
