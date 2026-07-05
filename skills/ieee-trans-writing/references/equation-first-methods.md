# Equation-First Method Writing

Use this reference when drafting Method, Proposed Approach, Algorithm, or technical proposal sections.

## Method Paragraph Skeleton

```text
Purpose sentence:
  Define what the subsection contributes to the objective.

Notation:
  Define input, domains, modules, and outputs.

Equation:
  Present the mapping or objective.

Design rationale:
  Explain why this mapping/loss addresses the failure mode.

Training/inference:
  State how it is optimized and whether it remains at test time.
```

## Recommended Section Order

1. Problem formulation.
2. Overview of the framework.
3. Feature extraction or representation module.
4. Alignment/regularization/contrastive/invariance module.
5. Total objective.
6. Optimization algorithm.
7. Inference and complexity.

## Problem Formulation Template

```text
Let D_s = {D_1,...,D_M} denote M source domains, where
D_m = {(x_i^m, y_i^m)}_{i=1}^{n_m}. The target domain D_t is
unavailable during training. The goal is to learn a predictor
q_phi(G_theta(x)) that minimizes the expected target risk under
domain shift while preserving class-discriminative information.
```

Adapt the domain variable to subject, force, session, dataset, or operating condition.

## Architecture Description Rule

Do not write:

```text
We first use a CNN and then feed the features into an MLP.
```

Write:

```text
The encoder G_theta maps each C-channel window X_i in R^{C x W}
to a latent representation h_i = G_theta(X_i). The classifier
C_phi then produces logits a_i = C_phi(h_i). This decomposition
separates signal representation from the supervised decision layer,
which allows the invariance constraint to act directly on h_i.
```

## Loss Assembly Rule

Introduce each loss in this order:

1. Pair or sample set definition.
2. Single-term objective.
3. Why the term is needed.
4. Total objective.
5. Optimization details.

Example structure:

```text
P(i) contains windows sharing class label y_i but sampled from
different force domains. The contrastive term L_cf pulls P(i)
toward anchor i while treating different-class windows as negatives.
The total objective is

L = L_cls + lambda_cf L_cf + lambda_reg L_reg.

Here L_cls preserves discriminability, L_cf enforces class-consistent
cross-force smoothness, and L_reg controls overconfidence.
```

## Algorithm Box Content

An IEEE-style algorithm should include:

- Required inputs: data, labels, domains, batch size, epochs, hyperparameters.
- Module initialization.
- Sampling rule, especially for domain or contrastive pairs.
- Forward pass and losses.
- Update order.
- Checkpoint or reference update.
- Output model.

For two-stage methods, use two algorithm blocks or clearly separate the loops.

## Inference Paragraph

Always state the inference path. If projectors, discriminators, generators, or reference encoders are used only during training, say so. If a reference encoder is frozen and used during inference, say so explicitly.
