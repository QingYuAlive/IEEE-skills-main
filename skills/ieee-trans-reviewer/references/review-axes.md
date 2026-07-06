# IEEE Transactions Review Axes

Use these axes to generate a harsh technical review. Do not evaluate broad appeal, narrative quality, or general-audience accessibility. The manuscript survives only if the mathematical object, theoretical support, empirical protocol, and claim scope are defensible.

## Axis 1: Math And Theory

### Fatal questions

- Is the problem setting formalized with input space `$\mathcal{X}$`, output or label space `$\mathcal{Y}$`, source domains, target domains, and predictor?
- Are all variables in equations defined before or immediately after use?
- Does the same symbol ever refer to a dataset, domain, distribution, split, or metric?
- Do the equations match the described network architecture, training schedule, and inference path?
- Is the total objective explicitly stated, including all coefficients and tuning policy?
- Are positive pairs, negative sets, projection spaces, temperatures, margins, and masks defined before contrastive losses?
- If the paper claims IRM, GroupDRO, invariant learning, adversarial alignment, or robustness, is the constraint written as a formal optimization term?
- Is there a theorem, proposition, convergence result, or generalization bound when the paper claims theoretical support?
- Are theorem assumptions stated and consistent with the experimental setting?
- Is there asymptotic time and memory complexity for the proposed algorithm, especially pairwise contrastive terms, attention blocks, graph modules, adversarial training, or two-stage reference encoders?

### Major-revision triggers

- Architecture prose cannot be reconstructed into equations.
- A loss term appears in experiments but not in the objective.
- The proof studies a simplified objective different from the implemented method.
- The inference path is ambiguous or includes training-only modules without disclosure.
- Complexity is absent despite deployment, real-time, or efficiency claims.

## Axis 2: Empirical Defense

### Protocol attack

- If the manuscript claims domain generalization, is there strict LODO, LOSO, leave-one-force, leave-one-session, leave-one-subject, or held-out target evaluation?
- Is the target domain unavailable during training, tuning, normalization statistics, early stopping, checkpoint selection, and hyperparameter search?
- Are seeds, folds, split construction, checkpoint rule, and evaluation metrics specified?
- Are preprocessing steps reported, including filtering, normalization, windowing, overlap, sampling, channels, trial handling, and rest-class handling when relevant?

### Baseline attack

- Are baselines current, including strong methods from the last three years where available?
- Are baseline inputs, backbones, model capacity, training budget, augmentations, and tuning budgets comparable?
- Does the paper compare against DG, contrastive, invariant, adversarial, or robust baselines matching the claimed contribution?
- Are classical or handcrafted baselines used as the only evidence for a deep learning contribution?

### Ablation attack

- Does every proposed module, loss, stage, pair-construction rule, reference model, augmentation, and weighting scheme have a removal or replacement ablation?
- For contrastive learning, are temperature `$\tau$`, positive-pair count, negative sampling, projection head, augmentation policy, and class/domain masks ablated?
- For IRM or GroupDRO-style claims, are penalty strength, group construction, and worst-domain performance analyzed?
- For two-stage methods, are reference source, frozen versus trainable components, stage budget, and checkpoint choice ablated?
- Are sensitivity curves provided for critical hyperparameters such as `$\lambda$`, `$\tau$`, margin, perturbation ratio, sparsity weight, or mix coefficient?

### Visualization attack

- Are t-SNE, PCA, confusion matrices, spectra, or saliency maps paired with quantitative metrics?
- Does the text treat visualization as diagnostic evidence rather than proof?
- Are representation metrics such as intra-class variance, inter-class margin, MMD, A-distance, silhouette score, or source-target discrepancy reported when alignment is claimed?

## Axis 3: Claim Calibration

Flag any sentence that overclaims relative to evidence.

### Fatal overclaims

- `Our method completely solves the robustness problem.`
- `The learned representation is domain-invariant` without a formal invariant criterion and OOD protocol.
- `The method generalizes to unseen domains` without target-held-out evaluation.
- `The proposed loss is necessary` without a removal or replacement ablation.
- `The theorem proves superior empirical performance` when the theorem only states a conditional bound.
- `State of the art` without broad, recent, fair, protocol-matched baselines.

### Required replacements

| Overclaim | Reviewer demand |
|---|---|
| `robust` | Define perturbation or unseen-domain protocol and report metric. |
| `generalizable` | Define source domains, held-out target, and checkpoint rule. |
| `invariant` | Define invariant criterion, objective, and representation metric. |
| `necessary` | Provide removal or replacement ablation. |
| `significant` | Provide statistical test or practical significance criterion. |
| `efficient` | Provide parameters, FLOPs, memory, latency, throughput, or Big-O analysis. |

## Axis 4: Reproducibility And Reporting

- Can another group reproduce data preprocessing, training, validation, and testing?
- Are hyperparameters, optimizer, learning rate schedule, batch size, epochs, seeds, hardware, and implementation details specified?
- Is code availability or pseudo-code sufficient for the algorithm?
- Are statistical tests and multiple-comparison handling stated where claims depend on significance?
- Are limitations specific, or ceremonial?

## Severity Classification

Use this severity scale:

- `Fatal flaw`: invalidates the central claim or would likely trigger rejection.
- `Major concern`: blocks acceptance without substantial new analysis, experiments, proof, or rewriting.
- `Minor concern`: local notation, clarity, citation, or reporting problem that does not invalidate the central claim.

Do not classify missing core ablations, invalid OOD protocols, or undefined objectives as minor.
