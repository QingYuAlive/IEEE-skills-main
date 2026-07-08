# IEEE Transactions Shared Guidelines

These guidelines are derived from the local IEEE corpus in `IEEE-skills-main/ieee_corpus/`: recent TCYB, THMS, and TNNLS papers on sEMG/EEG signal learning, time-series classification, contrastive learning, domain generalization, invariant risk minimization, and industrial diagnosis. Use them as execution rules, not as background flavor.

## Non-Negotiable Stance

1. Do not draft from intuition alone. Convert the user material into symbols, assumptions, objectives, algorithms, and experiment claims before prose.
2. Do not make descriptive network walkthroughs the main method. IEEE Transactions method sections should expose the computational object first: input, mapping, representation, loss, training, inference.
3. Do not upgrade evidence. "Shows", "indicates", "suggests", "supports", and "validates under this protocol" have different strength.
4. Do not treat visualizations as proof. t-SNE, PCA, confusion matrices, spectra, and topographic maps support interpretation only when paired with quantitative metrics or controlled ablations.
5. Do not call a method state of the art unless baselines are broad, current, fairly implemented, and evaluated under identical splits or a clearly disclosed protocol.

## Corpus-Derived Writing Order

Use this order for methods, proposal cores, and major technical paragraphs.

1. **Problem setting**: Define domains, subjects, sessions, forces, labels, views, modalities, and target/unseen conditions.
2. **Notation table**: Declare every symbol before or immediately after first use.
3. **Representation pipeline**: Define input transformation, encoder, projector, classifier, discriminator, generator, or decoder with equations.
4. **Core constraint**: State the invariant, contrastive, adversarial, reconstruction, sparsity, perturbation, or uncertainty principle as a mathematical loss.
5. **Total objective**: Combine terms with weights or learned uncertainty parameters; define how each term maps to a design claim.
6. **Optimization algorithm**: Give training order, update schedule, frozen/reference networks, gradient reversal, two-stage training, or alternating updates.
7. **Inference path**: State which modules remain at test time and what is discarded.
8. **Cost and deployment**: Report parameters, FLOPs or throughput, memory, latency, or complexity when relevant.

This sequence reflects the corpus pattern: SCIRM/EIRM formalize assumptions and objectives before experiments; CDSRN, MS-DSN, DGNSU, CRT, U-TFSCL, and Learning Motor Cues expose losses and algorithms; sEMG WBHP and MMCANet explicitly connect architecture choices to signal structure and deployment constraints.

## Required Notation Table

For a technical IEEE paper, the notation table must include at least these categories when applicable:

- Data: `x`, `X`, `y`, `i`, `n`, batch size, window length, channel count, sampling rate.
- Domain: source domain `e` or `k`, unseen target `t`, force level, subject, session, dataset split.
- Representations: encoder `G` or `f`, feature `h` or `r`, projected latent `z`, classifier `C`, predictor `q`.
- Losses: task loss, contrastive loss, invariance penalty, adversarial loss, reconstruction loss, sparsity/uncertainty/regularization terms.
- Weights: fixed coefficients, adaptive weights, uncertainty parameters, temperature, margin, perturbation ratio.
- Protocol: folds, seeds, source/target split, checkpoint selection, evaluation metric.

Do not use the same symbol for a domain, dataset, and distribution. Do not introduce Greek weights in prose without defining their role and tuning policy.

## Math Formalization Patterns

### CNN, RNN, Transformer, and sEMG Signals

Use a signal-first definition:

```text
X_i in R^{C x T} or R^{C x W}, y_i in {1,...,K}
h_i = G_theta(X_i)
p_i = C_phi(h_i)
L_cls = CE(p_i, y_i)
```

Then connect architecture to signal facts. For sEMG/EEG/IMU papers, justify window length, overlap, kernel size, dilation, temporal branch, frequency branch, or channel layout by the signal morphology. The WBHP paper models raw sEMG windows as two-dimensional channel-by-window inputs; the MMCANet paper separates modality feature extraction and fusion; U-TFSCL defines time and frequency views before losses.

### Contrastive Learning

State positive-pair construction before writing the loss. The corpus uses multiple pair logics:

- EEG-EMG pairs from the same trial for cross-modal motor cues.
- Original and augmented time/frequency views for time-series representation.
- Same-class positive sets for supervised contrastive learning.
- Domain/fault proxies for domain-specific or domain-invariant spaces.

Minimum formal chain:

```text
h_i^D = G_D(x_i^D), z_i^D = P_D(h_i^D)
P(i) = {p: y_p = y_i, p != i}
L_con = contrast(anchor i, positives P(i), negatives A(i)\P(i), tau)
```

Then state why the pair relation matches the claim. If the claim is cross-force invariance, positives must reflect force variation. If the claim is time-frequency consistency, positives must link time and frequency views of the same sample or same class.

### Domain Generalization

Define source domains and the unseen target before any architecture:

```text
S = {D_1,...,D_m}, D_k = {(x_i^k, y_i^k)}
T is unavailable during training.
Goal: minimize expected target risk under no target labels.
```

Then define the invariance mechanism: IRM-style penalty, risk extrapolation, domain-private/shared separation, domain adversarial loss, perturbation-generated domains, or proxy contrastive alignment. State the category-shift assumption if classes are shared, and state what changes across domains: force, subject, session, machine condition, label noise, style statistics, or operating load.

### Two-Stage or Reference-Guided Methods

If a method has stages, write them as separate optimization problems. The corpus repeatedly separates representation pretraining from downstream training, or reference encoder construction from consistency learning.

Required fields:

- Stage 1 objective and modules trained.
- Stage 1 checkpoint selection.
- Stage 2 objective and which Stage 1 components are frozen or reused.
- Inference modules.
- Ablation comparing the stage choices, not only final accuracy.

### Generative and Reconstruction Models

For GAN, reconstruction, or cross-modal generation, define:

- Conditional input and generated output.
- Discriminator or reconstruction target.
- Auxiliary task preserving semantics.
- Quality metrics beyond visual similarity.

Learning Motor Cues combines cross-modal contrastive representation, WGAN-GP-style generation, classifier guidance, reconstruction, TRTS/TSTR, distribution metrics, PCA, waveform, spectrum, and topographic perturbation analysis. Use this as a defense pattern: generation quality needs task, distribution, temporal, and spectral evidence.

## Experiment Defense Framework

Every result section should answer five reviewer questions.

1. **Protocol**: What data, split, target domain, seed, fold, and checkpoint are used?
2. **Fairness**: Are baselines current, relevant, and run with comparable input, architecture capacity, and training budget?
3. **Coverage**: Does evaluation include cross-subject, cross-session, cross-force, leave-one-domain-out, LOSO, or unseen-condition settings when claiming generalization?
4. **Mechanism**: Does each proposed component have an ablation aligned to its claimed role?
5. **Cost**: Does the added module justify its complexity, memory, latency, or training burden?

Preferred reporting:

- Mean and standard deviation over repeated runs or folds.
- Accuracy plus F1 or task-appropriate metrics; RMSE/score for regression; MMD/DTW/TRTS/TSTR for generation.
- Statistical tests when comparing multiple methods or settings, as seen in WBHP and CDSRN/SCIRM.
- Sensitivity curves for critical hyperparameters such as contrastive temperature, uncertainty weights, perturbation ratios, sparsity weights, or mix coefficients.

## Baseline Justification

Use tiers:

1. Classical feature or machine-learning baselines when the field still uses them.
2. Plain deep baselines sharing input modality and backbone family.
3. Domain-generalization or contrastive baselines matching the claim type.
4. Recent specialized methods from the same signal or industrial condition.
5. Ablated internal variants isolating every proposed mechanism.

Do not compare only against weak or unrelated methods. Do not use handcrafted-feature baselines as the sole evidence for a deep learning contribution.

## Ablation Logic

A good ablation table is a claim map:

- Remove the proposed module.
- Replace it with a simple alternative.
- Vary the component's governing hyperparameter.
- Report the same metric and split as the main table.
- Interpret negative or mixed results without overclaiming.

Examples from the corpus:

- U-TFSCL isolates time-domain contrastive loss, frequency-domain contrastive loss, time-frequency consistency, label ratio, positive-pair count, augmentation strategy, and uncertainty weighting.
- DGNSU isolates perturbation strategies and reports small cost increase.
- Learning Motor Cues removes the classifier, EMG contrastive branch, and multiscale CNN.
- SCIRM/EIRM compare ERM, IRM variants, and robustness under label noise or domain shift.

## Visualization Interpretation

Use visual evidence as a structured paragraph:

1. State what is plotted and what each color/marker/domain means.
2. Describe visible pattern without causal overreach.
3. Link pattern to a quantitative metric or ablation.
4. State the limitation of the visualization.

Common interpretations:

- t-SNE/PCA: interclass separation, intraclass compactness, source-target overlap, or domain-specific/private separation.
- Confusion matrix: which classes remain confused and whether errors match signal similarity.
- Spectrum/waveform: whether generated or augmented signals preserve temporal and frequency morphology.
- Topographic/importance map: whether perturbation-based importance matches known motor regions or sensor physiology.
- Sensitivity curve: stability range, not a single lucky point.

## Section-Level Gates

### Abstract

No equations or citations. Include problem, gap, method, key evidence, and significance. Quantify only results actually present in the paper.

### Introduction

Move from application/domain shift to technical gap to design principle. Avoid a generic "deep learning is powerful" opening. Contributions should map to method modules and experiment evidence.

### Related Work

Group by technical obstacle, not by author chronology: signal representation, contrastive learning, domain generalization, robust training, multimodal fusion, generative modeling.

### Method

Equation-first. Each subsection should have a purpose, symbols, mapping, loss/objective, and training/inference note.

### Experiments

Report data, preprocessing, splits, baselines, implementation, metrics, main comparison, ablation, sensitivity, visualization, and complexity.

### Discussion

Explain why the mechanism helps, where it fails, and what future work follows from evidence. Do not restate tables.

## Forbidden Unsupported Moves

- Do not claim "force-invariant", "domain-invariant", "robust", or "generalizable" without an unseen-domain protocol.
- Do not claim a module is necessary without a removal or replacement ablation.
- Do not claim theory proves empirical dominance. Theorems support conditions; experiments test practice.
- Do not hide a weak Stage 1 result if the final method relies on stage coupling. Explain the coupling carefully.
- Do not use "significant" for numeric improvement unless a statistical test or clear context supports it.
- Do not omit raw preprocessing choices for signals: filtering, normalization, windowing, overlap, sampling, channels, trial handling.
- Do not report only best checkpoint unless selection rule is explicit.
- Do not let figures carry claims absent from text or metrics.

## Final QA Checklist

Before delivering IEEE-style text or files, check:

- All symbols used in equations are defined.
- Every module has a mathematical role and a claimed role.
- Every claimed role has an experiment or ablation.
- Every comparison has a matching protocol.
- Every visualization has a bounded interpretation.
- Limitations are specific, not ceremonial.
- The output does not invent data, citations, p-values, or unseen experiments.
