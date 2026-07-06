# IEEE Diction Calibration

Use this file during the sentence-level polish pass when verbs, hedges, boosters, and claim strength need reviewer-facing calibration.

## Verb Strength

| Verb | Use when |
|---|---|
| `demonstrate` | Direct empirical evidence under a clearly stated protocol supports the claim. |
| `show` | A table, metric, or controlled experiment directly reports the effect. |
| `indicate` | The evidence is measured but not decisive or not fully isolating. |
| `suggest` | The sentence interprets a pattern beyond direct measurement. |
| `support` | Evidence is consistent with a mechanism, ablation, or claim. |
| `validate under this protocol` | The claim is true only for the stated split, metric, and checkpoint rule. |

## Booster Control

Avoid boosters unless tied to numbers or statistical tests.

- Replace `significantly improves` with `improves` unless a statistical test is supplied.
- Replace `substantially improves` with the actual delta when available.
- Replace `superior` with `higher macro-F1 under the reported split` when the metric and protocol are known.
- Replace `state of the art` with `outperforms the compared baselines under the matched protocol` unless the comparison is broad, current, and fair.

## Hedge Placement

- Results sentences should report measured effects directly.
- Interpretation sentences may use `may`, `can`, `is consistent with`, or `suggests`.
- Theorem statements should not be hedged if the assumptions are satisfied; instead state the assumptions.
- Limitation sentences should be explicit, not ceremonial.

## IEEE Preferred Repairs

| Risky wording | Calibrated wording |
|---|---|
| `This proves the effectiveness of the module.` | `The removal ablation supports the contribution of the module under the stated protocol.` |
| `The method generalizes well.` | `The method improves target-domain performance under the held-out evaluation protocol.` |
| `The visualization clearly verifies invariance.` | `The visualization is consistent with the discrepancy metric and supports the representation analysis.` |
| `The model is efficient.` | `The model adds the reported parameter, memory, or latency cost relative to the baseline.` |
