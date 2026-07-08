# IEEE Python Helper API

Use these helper contracts when generating plotting scripts. Implementations live in `static/fragments/backend/python.md`.

## Style And Export

```python
ieee_style_setup() -> None
ieee_figure_size(width: str, height: float | None = None) -> tuple[float, float]
save_ieee_figure(fig: matplotlib.figure.Figure, output_stem: str | pathlib.Path) -> None
```

Rules:

- `ieee_style_setup()` must be called before `plt.subplots`.
- `width` must be `single-column` or `double-column`.
- `save_ieee_figure()` must save both `.pdf` and `.png`.

## Ablation API

```python
plot_ablation_bar(
    labels: Sequence[str],
    means: Sequence[float],
    errors: Sequence[float],
    ylabel: str,
    output_stem: str | pathlib.Path,
    significance: Mapping[tuple[int, int], str] | None = None,
    width: str = "single-column",
) -> None
```

Use for mechanism isolation. Labels should name the removed or retained term, such as `w/o $\\mathcal{L}_{\\mathrm{con}}$` or `full objective`.

## Embedding API

```python
plot_embedding(
    features: numpy.ndarray,
    labels: Sequence[int | str],
    domains: Sequence[int | str],
    output_stem: str | pathlib.Path,
    reducer: str = "tsne",
    width: str = "double-column",
) -> None
```

Use for feature-space diagnostics. The script must print silhouette score and intra-class variance.

## Radar API

```python
plot_domain_radar(
    metrics: Sequence[str],
    series: Mapping[str, Sequence[float]],
    output_stem: str | pathlib.Path,
    width: str = "single-column",
) -> None
```

Use only for normalized multi-metric summaries. Keep numerical tables as the primary quantitative evidence.

## Validation Requirements

- Assert compatible lengths for labels, means, errors, and metric names.
- Assert radar values are in `[0, 1]`.
- Assert embeddings have shape `(n_samples, n_features)` before reduction and `(n_samples, 2)` after reduction.
- Print the exact output paths after saving.
