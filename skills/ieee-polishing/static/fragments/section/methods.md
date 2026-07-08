# Section: Methods

## IEEE Polishing Contract

Methods prose must expose computational objects:

```text
notation -> input processing -> mapping -> objective -> optimization -> inference -> complexity
```

## Required Checks

- Inputs, labels, domains, and target conditions are defined.
- Encoders, projectors, classifiers, or generators are expressed as mappings.
- Positive pairs are defined before contrastive loss.
- Loss terms have coefficients, roles, and ablation hooks.
- Stage-wise methods state trainable and frozen modules.
- Test-time modules are distinguished from training-only modules.
- Complexity or deployment cost is included when claimed.

## Forbidden Vague Phrases

- `the signal passes through the network`
- `features are extracted automatically`
- `the model learns robust representations`
- `the method is validated`
- `standard preprocessing is applied`

Replace these with formal mappings, preprocessing parameters, objectives, protocols, and evidence.
