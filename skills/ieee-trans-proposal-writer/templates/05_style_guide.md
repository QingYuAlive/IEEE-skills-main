# IEEE Style Guide

- Language:
- Target venue:
- Target reader:
- Tone: formal / equation-first / conservative-claims / empirical-defense
- Citation style: IEEE numeric

## Required Style

- Define symbols before using them.
- Write modules as mappings before describing implementation.
- State pair construction before contrastive loss.
- State domain/environment definitions before DG objective.
- State OOD protocol before robustness/generalization claims.
- State ablation before claiming component necessity.
- State complexity before claiming lightweight or deployable.

## Forbidden Expressions Unless Proven

- robust
- invariant
- generalizable
- state of the art
- significant
- proves
- solves
- guarantees
- lightweight
- real-time

## Preferred Claim Boundaries

- under the evaluated held-out-domain protocol
- for the considered source and target environments
- relative to the selected baseline tiers
- consistent with the ablation results
- qualitatively supported by visualization and quantitatively supported by metrics

## Method Prose Rule

Do not write:

```text
We first use a CNN, then an LSTM, and finally a classifier.
```

Write:

```text
The encoder `G_\theta` maps each input window `X_i in R^{C x W}` to a representation `h_i`.
The classifier `C_\phi` predicts `\hat{y}_i`, while the auxiliary objective constrains `h_i`
across the specified source environments.
```
