# IEEE Argument Map

This file replaces broad storytelling with an IEEE Transactions theorem-proof and ablation-defense structure. Do not draft prose from this file until every required formal object is filled or explicitly marked as missing.

## 0. Math Gate Status

- Gate status: `pass / blocked`
- Missing formal objects:
- Missing OOD protocol:
- Missing objective terms:
- Missing ablation or complexity evidence:

## 1. Formal Problem Statement

- Input space `\mathcal{X}`:
- Sample shape, e.g. `X_i in R^{C x W}` or `X_i in R^{C x T}`:
- Label space `\mathcal{Y}`:
- Source domains `\mathcal{E}_{tr} = {e_1,...,e_M}`:
- Target/OOD domains `\mathcal{E}_{te}`:
- Training set per domain `D_e = {(x_i^e, y_i^e)}_{i=1}^{n_e}`:
- Target availability rule:
- Task risk:

```text
R_e(\theta,\phi) =
```

## 2. Central Technical Tension

| Item | IEEE formulation |
|---|---|
| Known method class | |
| Failure mode under OOD/domain/signal shift | |
| Why existing objective is insufficient | |
| Specific variable or distribution that shifts | |
| What must remain invariant or discriminative | |

## 3. Central Thesis

One sentence, equation-aware:

```text
By [formal constraint/objective], the proposed method encourages [representation property] under [OOD protocol], while preserving [task-discriminative property] measured by [metrics].
```

## 4. Predictor and Objective Stack

### 4.1 Representation Pipeline

```text
h_i = G_\theta(x_i)
z_i = P_\psi(h_i)
\hat{y}_i = C_\phi(z_i)
```

- Encoder role:
- Projector role:
- Classifier/predictor role:
- Training-only modules:
- Inference modules:

### 4.2 Primary Empirical Risk

```text
\min_{\theta,\phi} \sum_{e in \mathcal{E}_{tr}} R_e(\theta,\phi)
```

- Loss function:
- Class imbalance or regression treatment:
- Checkpoint selection rule:

### 4.3 Robustness / DG / Contrastive Constraint

Choose and fill the relevant block.

#### IRM-style block

```text
\min_{\theta,\phi} \sum_e R_e(\theta,\phi)
  + \lambda \sum_e \|\nabla_{w|w=1} R_e(w \circ C_\phi \circ G_\theta)\|^2
```

- Invariance claim:
- Assumption:
- Known limitation:

#### GroupDRO-style block

```text
\min_{\theta,\phi} \max_{e in \mathcal{E}_{tr}} R_e(\theta,\phi)
```

- Worst-group definition:
- Group weighting/update rule:
- OOD target relation:

#### Supervised contrastive / domain contrastive block

```text
P(i) = {p: y_p = y_i, d_p != d_i}
L_con = - \sum_i \frac{1}{|P(i)|} \sum_{p in P(i)}
  log \frac{\exp(sim(z_i,z_p)/\tau)}
  {\sum_{a in A(i)} \exp(sim(z_i,z_a)/\tau)}
```

- Positive-pair rule:
- Negative-pair rule:
- Why the pair rule matches the claimed invariance:
- Failure if the pair rule is wrong:

#### Uncertainty / multi-task weighting block

```text
L_total = \sum_m exp(-s_m) L_m + \alpha_m s_m
```

- Task losses:
- Learned uncertainty parameters:
- Evidence that automatic weighting helps:

### 4.4 Total Objective

```text
L_total =
```

- Weight policy:
- Hyperparameter search or learned schedule:
- Optimization algorithm:
- Complexity implication:

## 5. Theorem-Proof Claim Map

Use "theorem" broadly: formal proposition, lemma, assumption-bound guarantee, or mechanistic claim. If no theorem exists, write a proof-sketch boundary instead of pretending.

| ID | Proposition / claim | Assumptions | Formal object | Proof sketch or mechanism | Boundary |
|---|---|---|---|---|---|
| T1 | | | | | |
| T2 | | | | | |
| T3 | | | | | |

Example:

| ID | Proposition / claim | Assumptions | Formal object | Proof sketch or mechanism | Boundary |
|---|---|---|---|---|---|
| T1 | Cross-force positives reduce force-specific feature bias. | Same gesture label is preserved across force levels; target force is not used in training. | `P(i) = {p: y_p=y_i, f_p != f_i}` and `L_con`. | Pulling same-class cross-force embeddings together penalizes force-specific directions in `z`. | Does not prove invariance without held-out-force evaluation and ablation. |

## 6. Ablation-Defense Map

Each method claim must have a matching removal/replacement test.

| Module or loss | Claimed role | Remove test | Replacement test | OOD split | Metric | Expected failure if claim is true |
|---|---|---|---|---|---|---|
| `L_cls` | Preserve task discrimination | train without CE | CE-only baseline | source and target | Acc/F1 | contrastive features lose class decision quality |
| `L_con` | Align same-class OOD variation | remove contrastive term | random pairs or within-domain pairs | held-out force/session/subject | Acc/F1, t-SNE bounded | target split drops more than source split |
| `L_IRM` or `L_DRO` | Stabilize predictor across environments | ERM-only | VREx/GroupDRO/IRM alternative | leave-one-domain-out | mean/std per target | higher variance or weaker worst-domain score |
| complexity module | Improve accuracy-cost tradeoff | remove module | larger backbone | same protocol | params/FLOPs/latency + Acc/F1 | similar accuracy but unacceptable cost or vice versa |

## 7. Baseline Defense

| Baseline tier | Required examples | Why needed | Included? |
|---|---|---|---|
| Classical feature / ML | LDA, SVM, KNN, handcrafted TD features when field-relevant | tests value over legacy signal pipelines | |
| Plain deep model | CNN, RNN/LSTM, Transformer, ResNet/FCN | tests backbone capacity | |
| DG / robust learning | ERM, IRM, GroupDRO, VREx, Mixup, CORAL/DANN if relevant | tests generalization mechanism | |
| Contrastive / SSL | SupCon, SimCLR-style, TS-TCC/TS2Vec-like when relevant | tests representation mechanism | |
| Internal ablations | remove each proposed term/module | tests causal contribution | |

## 8. OOD Protocol Contract

- OOD variable: subject / session / force / load / machine condition / dataset / modality:
- Held-out protocol:
- Validation rule:
- Number of seeds/folds:
- Metrics:
- Statistical test:
- Visualization and its boundary:

## 9. Complexity and Deployment Claim

- Parameter count target:
- FLOPs or asymptotic complexity:
- Memory:
- Throughput or latency:
- Training overhead:
- Which modules are discarded at inference:
- Accuracy-cost tradeoff claim:

## 10. Final Proposal Move

Allowed final move only after Sections 1-9 are complete:

- Contribution 1:
- Contribution 2:
- Contribution 3:
- Claims not yet allowed:
