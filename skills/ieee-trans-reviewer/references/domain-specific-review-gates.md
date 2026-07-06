# IEEE Domain-Specific Review Gates

Use this file after building the manuscript fact base. Apply only the gates relevant to the manuscript. Convert diagnostics into the final report; do not expose this file's internal routing.

## Shared Gate Pattern

For each central claim, identify:

1. exact claim and scope;
2. mathematical object or assumption needed;
3. objective, algorithm, or theorem supporting it;
4. experiment required to test it;
5. ablation required to isolate it;
6. failure mode if the claim is overstated.

## Domain Generalization And OOD Learning

Fatal checks:

- Are source domains `$\mathcal{E}=\{\mathcal{E}_1,\ldots,\mathcal{E}_m\}$` and target domain `$\mathcal{T}$` formally defined?
- Is `$\mathcal{T}$` unavailable during training, tuning, normalization, model selection, and checkpoint selection?
- Is the protocol strict LODO, LOSO, leave-one-force, leave-one-session, leave-one-subject, or held-out operating condition?
- Are class sets shared or is label shift addressed?
- Is target risk reported separately from averaged source performance?

Reviewer attack:

- Flag any domain generalization claim evaluated only on random train/test splits.
- Flag target leakage through normalization statistics, subject windows, trial segments, or hyperparameter tuning.
- Require worst-domain metrics, not only average accuracy.

## Contrastive Learning

Fatal checks:

- Is the positive pair set `$P(i)$` formally defined before the loss?
- Are negatives, anchor set, temperature `$\tau$`, similarity function, projection head, and masking rule defined?
- Does the pair relation match the claim? Cross-force invariance requires cross-force positives; time-frequency consistency requires matched views; supervised contrast requires label-defined positives.
- Are false positives or false negatives discussed for class/domain pair construction?

Required ablations:

- remove `$\mathcal{L}_{\mathrm{con}}$`;
- vary `$\tau$`;
- vary positive-pair count;
- replace positive-pair construction;
- remove projection head;
- alter negative sampling or masking.

## IRM, GroupDRO, And Robust Optimization

Fatal checks:

- Is the risk per domain `$R_e$` defined?
- Is the IRM penalty or GroupDRO max-risk objective written explicitly?
- Are groups meaningful, balanced, and available at training time?
- Does the method report worst-domain or target-domain performance?

Required ablations:

- penalty coefficient sensitivity;
- group definition sensitivity;
- ERM comparison with matched backbone;
- comparison to at least one recent robust or DG baseline.

## sEMG, EEG, IMU, And Human-Machine Signals

Fatal checks:

- Are sampling rate, channels, window length, overlap, filtering, normalization, trial segmentation, subject IDs, and session or force levels reported?
- Are subject-level, trial-level, and window-level splits leakage-free?
- Is rest class handling reported when relevant?
- Are cross-subject, cross-session, cross-force, or unseen-user claims evaluated with held-out protocols?

Reviewer attack:

- Flag window leakage when adjacent windows from the same trial appear in both train and test.
- Flag normalization leakage when trial or subject statistics use target data.
- Require accuracy plus macro-F1 or balanced metrics when classes are imbalanced.
- Require latency or throughput if real-time control is claimed.

## Time-Series And Industrial Diagnosis

Fatal checks:

- Are operating conditions, loads, fault types, sensors, sampling rates, and temporal splits defined?
- Are train/test splits chronological or condition-held-out when forecasting or generalization is claimed?
- Are augmentations physically plausible?
- Are baselines matched for input length and sampling rate?

Required analyses:

- sensitivity to window length and overlap;
- per-condition or per-fault performance;
- robustness to sensor noise or operating load changes when claimed;
- complexity or inference-time analysis for deployment.

## Neural Architecture Claims

Fatal checks:

- Are tensors and mappings defined, for example `$X_i\in\mathbb{R}^{C\times T}$`, `$h_i=G_\theta(X_i)$`, and `$p_i=C_\phi(h_i)$`?
- Are architectural choices justified by signal morphology, objective terms, or complexity constraints?
- Is parameter count or FLOPs reported when a new architecture is proposed?

Reviewer attack:

- Flag qualitative architecture descriptions as unacceptable when equations and tensor shapes are absent.
- Require ablations for branch count, kernel size, projection dimension, attention heads, dilation, fusion rule, or stage design when central to novelty.

## Generative, Reconstruction, And Cross-Modal Models

Fatal checks:

- Are generated outputs, conditioning variables, discriminators, reconstruction targets, and auxiliary semantic losses defined?
- Are generation metrics task-relevant, not only visual?
- Are TRTS/TSTR, distribution metrics, waveform, spectrum, or downstream classification tests provided when generation quality matters?

Reviewer attack:

- Flag visual-only generation claims.
- Require semantic preservation evidence and downstream utility.

## Deployment, Efficiency, And Real-Time Claims

Fatal checks:

- Are parameters, FLOPs, memory, latency, throughput, and hardware reported?
- Is test-time computation separated from training-only modules?
- Is Big-O time and memory complexity stated for pairwise, attention, graph, or adversarial components?

Reviewer attack:

- Flag `lightweight`, `efficient`, `real-time`, or `deployable` without measured or asymptotic cost.
