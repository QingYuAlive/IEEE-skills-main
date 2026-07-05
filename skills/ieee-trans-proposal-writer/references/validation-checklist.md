# IEEE Validation Checklist

Run this checklist before any proposal prose is delivered or exported.

## Gate 0: Math Gate

- [ ] Input space `\mathcal{X}` is defined.
- [ ] Label space `\mathcal{Y}` is defined.
- [ ] Source domains/environments are defined.
- [ ] Target or OOD domains are defined.
- [ ] Target availability and validation policy are explicit.
- [ ] Predictor mappings are formalized, e.g. `h=G_\theta(x)`, `z=P_\psi(h)`, `\hat{y}=C_\phi(z)`.
- [ ] Empirical risk is written.
- [ ] Total objective is written.
- [ ] Each loss weight, schedule, or uncertainty parameter is defined.
- [ ] Training and inference paths are separated.

If any item fails, stop drafting and return `Blocked Math Gate`.

## Gate 1: OOD / Empirical Defense

- [ ] OOD variable is named: subject/session/force/load/dataset/machine condition/modality/label noise.
- [ ] Held-out protocol is defined.
- [ ] Validation and checkpoint selection do not leak target information.
- [ ] Seeds, folds, repeats, and metrics are specified.
- [ ] Baseline tiers are justified.
- [ ] Every proposed module/loss has a removal or replacement ablation.
- [ ] Sensitivity is planned for key weights, temperatures, perturbation ratios, or stage lengths.
- [ ] Statistical test or variance reporting is planned for repeated experiments.

If any generalization or robustness claim lacks this gate, mark it forbidden.

## Gate 2: Theory / Mechanism

- [ ] Theorem/proposition claims have assumptions.
- [ ] Proof sketch or convergence/bound statement is present.
- [ ] Theory boundary is explicit.
- [ ] If no theorem exists, the section is called mechanism analysis, not proof.
- [ ] The theorem or mechanism maps to an experiment.

## Gate 3: Visualization

- [ ] t-SNE/PCA/UMAP feature source is specified.
- [ ] Projection seed/sample policy is specified.
- [ ] Confusion matrices state normalization.
- [ ] Signal/spectrum plots state units, preprocessing, and scale.
- [ ] Topographic/importance maps state how importance is computed.
- [ ] Every visualization is linked to quantitative evidence.
- [ ] No visualization is described as proof.

## Gate 4: Complexity

- [ ] Parameter count or model size is planned.
- [ ] FLOPs/asymptotic cost or throughput/latency is planned.
- [ ] Training-only modules are excluded from inference cost when appropriate.
- [ ] Accuracy-cost tradeoff is compared to a baseline.

## Gate 5: Claim Calibration

- [ ] "Robust", "invariant", "generalizable", "significant", and "state of the art" are used only when supported.
- [ ] Abstract and contributions do not exceed the evidence table.
- [ ] Limitations are specific to data, protocol, assumptions, or cost.
- [ ] No invented citations, p-values, baselines, datasets, or results.
