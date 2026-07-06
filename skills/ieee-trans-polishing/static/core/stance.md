# Default Stance For IEEE Transactions Polishing

## Governing Principle

Language optimization must serve mathematical clarity and logical defense. Do not make a weak technical sentence sound polished while leaving the equation, protocol, or evidence missing.

## What Polishing Must Preserve

- Author-provided facts, numbers, citations, datasets, protocols, and limitations.
- Notation Ledger entries and symbol meanings.
- The exact distinction between source domains, target domains, datasets, splits, subjects, sessions, force levels, and distributions.
- The evidence strength of each claim.

## What Polishing Must Improve

- Alignment between prose and equations.
- Consistency of mathematical symbols and terminology.
- Explicit protocol binding for OOD, robustness, invariance, and generalization claims.
- Reviewer-visible links between components, loss terms, ablations, and empirical claims.
- Sentence precision, grammar, and concision after the technical logic is correct.

## Formalization Gate

Before polishing, mark any sentence that needs formal replacement:

| Problem | Required action |
|---|---|
| Network described as a component list | Request mappings such as `$h_i = G_\theta(X_i)$` and `$p_i = C_\phi(h_i)$`. |
| Loss described only by name | Request the equation, coefficient, role, and ablation. |
| Domain shift described informally | Request source domains, target domains, unavailable target condition, and split policy. |
| Result stated without protocol | Request dataset, split, metric, baseline, checkpoint rule, and seed or fold policy. |
| Visualization used as proof | Request quantitative companion metric or controlled ablation. |

If a sentence fails this gate, flag it instead of polishing it into fluent but unscientific prose.

## Claim Calibration

Use verbs as evidence labels:

- `demonstrate`: direct evidence under the stated protocol.
- `show`: direct result, usually table or metric-backed.
- `indicate`: measured trend with limited scope.
- `suggest`: plausible interpretation beyond direct observation.
- `support`: evidence consistent with a mechanism or claim.
- `validate under this protocol`: evidence-bound validation only.

Do not use `prove`, `guarantee`, `universal`, `fully robust`, or `generalizable` unless a theorem or protocol explicitly supports the wording.
