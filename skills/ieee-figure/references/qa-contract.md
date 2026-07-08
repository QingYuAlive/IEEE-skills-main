# IEEE Figure QA Contract

## Pre-Submission Audit

Run this audit before final delivery:

```json
{
  "data_integrity": {
    "arrays_supplied": true,
    "no_mock_data": true,
    "shape_validation_present": true,
    "units_declared": true
  },
  "ieee_layout": {
    "width_is_exact": true,
    "font_family_allowed": true,
    "font_sizes_match_contract": true,
    "no_bold_axes": true
  },
  "math_rendering": {
    "usetex_enabled": true,
    "variables_match_manuscript": true,
    "latex_notation_in_labels": true
  },
  "empirical_defense": {
    "uncertainty_defined": true,
    "statistical_tests_declared": true,
    "ood_protocol_visible_when_claimed": true,
    "ablation_isolation_clear": true
  },
  "exports": {
    "pdf_saved": true,
    "png_600dpi_saved": true,
    "same_figure_object": true,
    "no_cropped_labels": true
  }
}
```

## Fatal QA Failures

Block final delivery when any item is true:

- The code constructs artificial result arrays without user authorization.
- A robustness or generalization claim lacks explicit source/target protocol.
- Error bars are drawn but their definition is absent.
- Significance marks appear without a named test.
- Variables in labels do not match manuscript notation.
- The figure reads or writes image/PDF files under `assets/`.
- The script omits `ieee_style_setup()` or sets `rcParams["text.usetex"]` to `False`.

## Reviewer Defense Rationale

For every substantial plot decision, include one sentence explaining rejection-risk reduction:

- "Error bars are confidence intervals across subject folds, reducing the risk that the accuracy gain is read as a single-run artifact."
- "The LODO protocol is printed in the legend, preventing an unsupported domain-generalization claim."
- "The ablation isolates `$\\mathcal{L}_{\\mathrm{con}}$`, so the visual evidence maps to the proposed loss term."
- "Silhouette score is printed with the embedding, preventing a purely qualitative feature-clustering argument."
