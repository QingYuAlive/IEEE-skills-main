# IEEE Transactions Phrasebank Playbook

Use this file after the paragraph role, notation, objective, and evidence boundary are clear. These formulas support precise IEEE-style transitions; they do not replace technical content.

## Definition And Formalization Language

Use these formulas to introduce symbols, tasks, domains, and mappings:

- `Formally, we define the input space as $\mathcal{X}$ and the label space as $\mathcal{Y}$.`
- `Let $\mathcal{E}=\{\mathcal{E}_1,\ldots,\mathcal{E}_m\}$ denote the set of source domains available during training.`
- `For each sample $(x_i^e,y_i^e)\in\mathcal{E}_e$, the encoder maps $x_i^e$ to $h_i^e=G_\theta(x_i^e)$.`
- `The prediction function is given by $p_i=C_\phi(G_\theta(x_i))$, where $C_\phi$ denotes the classifier.`
- `The target domain $\mathcal{T}$ is unavailable during training and is used only for evaluation.`
- `The total objective combines the task risk and alignment penalty as $\mathcal{L}_{\mathrm{total}}=\mathcal{L}_{\mathrm{cls}}+\lambda_{\mathrm{con}}\mathcal{L}_{\mathrm{con}}$.`

## Theorem, Proposition, And Bound Language

Use these formulas only when the manuscript supplies the theorem or condition:

- `Under Assumption 1, Proposition 1 bounds the discrepancy between the source risk and the target risk by...`
- `The result does not imply empirical dominance; it specifies the condition under which the penalty controls the domain discrepancy.`
- `The proof follows by decomposing the target risk into the source risk and a representation discrepancy term.`
- `This bound motivates the design of $\mathcal{L}_{\mathrm{inv}}$, while the empirical section tests whether the condition is useful in practice.`
- `The convergence statement applies to the stated update rule and does not cover alternative optimizers or adaptive schedules.`

## Method Transition Formulas

- `Given this notation, we next define the representation mapping used by the proposed objective.`
- `The role of $\mathcal{L}_{\mathrm{con}}$ is to align positive pairs across domains while retaining class discrimination.`
- `Unlike a descriptive module stack, this formulation separates the encoder used at inference from the projector used only during training.`
- `The positive set $P(i)$ is constructed before the contrastive objective is evaluated, ensuring that the loss matches the claimed invariance relation.`
- `At inference, the training-only projector is discarded, and predictions are computed by $C_\phi(G_\theta(x))$.`

## Ablation Defense Language

Use these formulas to make ablation logic explicit:

- `To isolate the contribution of $\mathcal{L}_{\mathrm{con}}$, we remove the contrastive term while keeping the encoder, classifier, training budget, and split unchanged.`
- `Removal of this module yields a degradation of the reported metric under the same OOD protocol, indicating that the gain is not solely due to model capacity.`
- `Replacing the cross-domain positive-pair rule with random pairing reduces performance, supporting the necessity of domain-aware pair construction.`
- `The sensitivity curve shows that the method remains stable for $\tau$ within the tested range, rather than depending on a single tuned value.`
- `The ablation is interpreted as evidence for the module's role under this protocol, not as proof of universal necessity.`

## Distribution Shift And OOD Language

- `The training set contains source domains $\mathcal{E}$, whereas the target domain $\mathcal{T}$ is held out until evaluation.`
- `The shift arises from changes in force level, subject identity, recording session, or operating condition, while the label space remains shared.`
- `This protocol evaluates domain generalization because no target-domain samples or labels are used for optimization.`
- `The claim is therefore restricted to the specified source-target split and checkpoint-selection rule.`
- `When the target domain differs in both marginal signal statistics and class-conditioned structure, the present evidence does not isolate which factor dominates the error.`

## Generalization-Bound And Limitation Language

- `These results support generalization under the tested leave-one-domain-out protocol.`
- `The evidence does not establish robustness to unseen domains outside the reported source-target family.`
- `The observed improvement is bounded by the tested subjects, sessions, force levels, and preprocessing pipeline.`
- `Because the target labels are not used during training, the improvement reflects source-only generalization under the stated protocol.`
- `The remaining failure cases indicate that class overlap persists when the target-domain signal morphology differs substantially from the source domains.`

## Results And Comparison Language

- `Under the same split and checkpoint rule, the proposed objective improves macro-F1 relative to the ERM baseline.`
- `The improvement is most pronounced in the worst-performing target domain, which is consistent with the distributional-robustness claim.`
- `The comparison remains inconclusive without matched training budgets and identical preprocessing.`
- `The table supports the claim only for the reported datasets and metrics.`
- `The result should be interpreted as a protocol-bound empirical gain rather than a general statement of state-of-the-art performance.`

## Visualization Language

- `The t-SNE plot is consistent with tighter class-wise clustering, but the claim is supported by the accompanying reduction in intra-class variance.`
- `The confusion matrix identifies residual class pairs whose errors remain high under the target-domain split.`
- `The visualization is used as diagnostic evidence and does not by itself establish invariance.`
- `The spectral plot supports signal-preservation analysis only when paired with the reported frequency-domain metric.`

## Claim Calibration Replacements

| Avoid | Use when supported |
|---|---|
| `proves` | `supports`, `is consistent with`, `validates under the stated protocol` |
| `huge improvement` | `an improvement of the reported magnitude` |
| `generalizes well` | `improves target-domain performance under the held-out protocol` |
| `learns robust features` | `reduces target-domain error under the perturbation or OOD protocol` |
| `the module is necessary` | `the removal ablation indicates that the module contributes to the reported gain` |
| `the figure shows invariance` | `the visualization is consistent with the quantitative discrepancy metric` |
