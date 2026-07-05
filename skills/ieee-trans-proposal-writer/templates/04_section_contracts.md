# IEEE Section Contracts

Each section contract prevents narrative drift. Every section must state its mathematical inputs, empirical evidence, allowed claims, forbidden claims, and validation checks before prose drafting.

## Global Contract Gates

- No section may use an undefined symbol.
- No method section may describe a neural module only in plain English.
- No result section may claim robustness/generalization without an OOD protocol.
- No visualization may be used as proof without quantitative evidence.
- No theoretical claim may appear without assumptions, statement, proof sketch, and boundary.

## 1. Abstract

- Purpose: Summarize the OOD/signaling problem, formal method mechanism, evaluation protocol, and bounded contribution.
- Required inputs: central thesis, OOD protocol, method name, primary metric, strongest evidence.
- Required equations: none in final abstract, but the underlying objective must exist in `03_argument_map.md`.
- Allowed claims: protocol-bound improvement, component role if supported by ablation, complexity/deployment if measured.
- Forbidden claims: "solves domain shift", "guarantees robustness", "proves invariance", or "state of the art" without full baseline evidence.
- Validation checklist:
  - Names the target condition or OOD protocol.
  - Does not overstate t-SNE/PCA/confusion matrix.
  - Quantifies only verified results.

## 2. Introduction

- Purpose: Convert application pressure into a formal technical gap.
- Required inputs: source/target domains, failure mode, limitations of existing objectives, central thesis.
- Required equations: optional short problem notation; full equations deferred to Method.
- Allowed claims: why current CNN/RNN/Transformer, DG, or contrastive methods are insufficient for the defined OOD variable.
- Forbidden claims: broad "deep learning is powerful" openings; novelty slogans without formal difference.
- Validation checklist:
  - Gap is stated as a failure of representation, objective, pair construction, or protocol.
  - Contributions map to formal objects and experiments.

## 3. Related Work

- Purpose: Position the method by technical obstacle, not chronology.
- Required inputs: baseline tiers and mechanism families.
- Required equations: none required, but compare objective families accurately.
- Allowed claims: differences in assumptions, pair construction, domain availability, or optimization target.
- Forbidden claims: dismissing prior work without naming the precise missing condition.
- Validation checklist:
  - Covers signal architectures, DG/IRM/GroupDRO-type methods, contrastive learning, and robust/uncertainty methods when relevant.
  - Ends with the unresolved gap that the objective addresses.

## 4. Problem Formulation

- Purpose: Define the learning problem before the architecture.
- Required inputs: `\mathcal{X}`, `\mathcal{Y}`, domains `\mathcal{E}_{tr}`, target `\mathcal{E}_{te}`, training data, target availability rule.
- Required equations:

```text
D_e = {(x_i^e, y_i^e)}_{i=1}^{n_e}
R_e(\theta,\phi) = (1/n_e) \sum_i \ell(C_\phi(G_\theta(x_i^e)), y_i^e)
```

- Allowed claims: what distribution shift is addressed and what is excluded.
- Forbidden claims: DG/OOD language without held-out target definition.
- Validation checklist:
  - Every symbol appears in the notation ledger.
  - Category shift and label availability are stated.

## 5. Method / Proposed Framework

- Purpose: Define the model as mappings and objectives.
- Required inputs: modules, parameters, inputs/outputs, losses, training order, inference path.
- Required equations:

```text
h_i = G_\theta(x_i)
z_i = P_\psi(h_i)
\hat{y}_i = C_\phi(z_i)
L_total = L_cls + \lambda_1 L_DG + \lambda_2 L_con + \lambda_3 L_reg
```

- Allowed claims: each module's role as a mathematical constraint.
- Forbidden claims: layer-by-layer narration without formal input/output; "module improves robustness" without linked loss and ablation.
- Validation checklist:
  - Positive/negative pair sets are defined before contrastive loss.
  - IRM/GroupDRO/VREx/adversarial/reconstruction objectives define all gradients and weights.
  - Training-only modules and inference modules are separated.

## 6. Theoretical Analysis / Proposition

- Purpose: State what can be theoretically supported and what remains empirical.
- Required inputs: assumptions, proposition/theorem, proof sketch, relation to objective.
- Required equations: proposition-specific; include risk, bound, convergence, or invariance statement.
- Allowed claims: assumption-bound guarantees, convergence under specified conditions, complexity order.
- Forbidden claims: empirical superiority derived from theorem alone; theorem without assumptions.
- Validation checklist:
  - Assumptions match the experimental protocol.
  - The proof boundary is explicit.
  - If no theorem exists, section is renamed "Mechanism Analysis" and framed as intuition.

## 7. Experiments

- Purpose: Test each claim under a reproducible protocol.
- Required inputs: datasets, preprocessing, splits, baselines, metrics, seeds/folds, checkpoint rule.
- Required equations: metrics if nonstandard; complexity formulas if claimed.
- Allowed claims: performance under named protocol and metrics.
- Forbidden claims: best-only reporting, target leakage, unclear validation, unfair baselines.
- Validation checklist:
  - Baselines cover classical, plain deep, DG/contrastive, recent specialized, and internal ablations as applicable.
  - OOD protocol matches the central claim.
  - Mean/std or statistical tests are planned when comparing methods.

## 8. Ablation and Sensitivity

- Purpose: Prove that each proposed object buys its claimed role.
- Required inputs: module/loss list, removal tests, replacement tests, hyperparameter ranges.
- Required equations: identify the removed term from `L_total`.
- Allowed claims: component-level support when the correct split and metric show the expected effect.
- Forbidden claims: "effective" without isolating the component; hiding negative stage-wise results.
- Validation checklist:
  - Each loss/module has a remove or replace test.
  - Sensitivity is included for temperatures, weights, perturbation ratios, sparsity penalties, or stage lengths.
  - Negative/mixed results have bounded interpretation.

## 9. Visualization

- Purpose: Qualitatively support, not prove, the quantitative evidence.
- Required inputs: feature source, samples, labels/domains/colors, projection seed, paired metric.
- Required equations: importance-score or projection preprocessing if nonstandard.
- Allowed claims: visible compactness, separation, source-target overlap, or signal morphology consistency.
- Forbidden claims: proof of invariance, robustness, or causality from t-SNE/PCA/topographic maps alone.
- Validation checklist:
  - Visualization is linked to a table, metric, ablation, or statistical test.
  - Low-dimensional projection limitations are stated.

## 10. Complexity and Deployment

- Purpose: Justify the cost of the method.
- Required inputs: parameters, FLOPs/asymptotic cost, memory, throughput, latency, or training overhead.
- Required equations/examples:

```text
Training cost = O(E * N * (C_backbone + C_contrastive + C_DG))
Inference cost = O(C_backbone + C_classifier)
```

- Allowed claims: practical deployment only if latency/memory support it.
- Forbidden claims: lightweight or real-time without measured cost.
- Validation checklist:
  - Training-only modules are excluded from inference cost when appropriate.
  - Accuracy-cost tradeoff is compared to a plain backbone or baseline.

## 11. Discussion / Limitations

- Purpose: Interpret mechanism, failures, and boundaries.
- Required inputs: strongest result, weakest result, ablation interpretation, limitations, future protocol.
- Required equations: none required unless discussing theory boundary.
- Allowed claims: why evidence supports the central mechanism under tested conditions.
- Forbidden claims: restating tables; hiding protocol limitations; claiming universality.
- Validation checklist:
  - Limitations are specific: dataset, OOD variable, labels, sensors, cost, theorem assumptions.
  - Future work follows from an observed boundary.
