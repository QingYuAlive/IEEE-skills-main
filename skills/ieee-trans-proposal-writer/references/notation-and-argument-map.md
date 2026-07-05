# Notation and Argument Map

Use this reference when a proposal lacks mathematical discipline or when the user wants to design the method from an idea.

## Notation Table Template

| Category | Symbol | Meaning | Required Detail |
|---|---|---|---|
| Data | `x_i`, `X_i` | sample or window | shape, modality, sampling/window rule |
| Label | `y_i` | class/regression target | class set or units |
| Domain | `d`, `e`, `k` | source condition | subject/session/force/load/device |
| Target | `t` | unseen condition | unavailable labels or held-out domain |
| Encoder | `G`, `f_theta` | feature extractor | CNN/RNN/Transformer branch, input view |
| Feature | `h_i`, `r_i` | representation | before projection/classifier |
| Projector | `P` | latent mapping | contrastive or shared space |
| Classifier | `C`, `q_phi` | predictor | logits/probabilities |
| Loss | `L_cls`, `L_con`, `L_inv` | objective term | exact pair/risk/penalty definition |
| Weight | `lambda`, `beta`, `tau`, `sigma` | tradeoff or temperature | fixed, searched, or learned |
| Protocol | `K`, `S`, `F` | fold/seed/domain count | split and checkpoint rule |

## Argument Map Template

| Layer | Question | Answer Pattern |
|---|---|---|
| Application gap | What fails in practice? | Cross-force/session/subject shift causes a classifier to learn condition-specific features. |
| Technical gap | Which formal assumption is missing? | Current pair construction or risk objective does not constrain class-preserving variation across domains. |
| Mechanism | What is the proposed constraint? | Align same-class cross-domain representations while regularizing logits or risk sensitivity. |
| Formal object | Where does the mechanism live? | Positive-pair set, invariant penalty, perturbation distribution, reference encoder, or uncertainty-weighted loss. |
| Evidence | How will this be tested? | Leave-one-domain-out, component removal, sensitivity, t-SNE with quantitative metrics, complexity. |
| Boundary | What is not claimed? | No claim of universal invariance beyond observed domains and target protocol. |

## Loss-to-Claim Mapping

Each loss term must buy one claim.

| Loss Term | Legitimate Claim | Required Evidence |
|---|---|---|
| Cross-entropy | Discriminative task learning | Accuracy/F1 and confusion matrix |
| Supervised contrastive | Intraclass compactness and interclass separability | Ablation, embedding plot, class metrics |
| Cross-domain contrastive | Domain/force/session alignment | Unseen-domain split, source-target feature plot |
| IRM/risk penalty | Stable predictor across environments | Multi-environment training and DG baselines |
| Spectral/logit regularization | Reduced overconfidence or smoother logits | Ablation and calibration or robustness metric |
| Reconstruction | Preserved signal information | Reconstruction metric and downstream metric |
| Adversarial domain loss | Reduced domain-specific leakage | Domain classifier or feature-separation evidence |
| Uncertainty weighting | Adaptive balance of tasks | Manual-weight ablation and sensitivity |

## Proposal Repair Moves

- If the method has too many modules, merge them under one mechanism-level hypothesis.
- If the contribution is only architectural, add signal-specific motivation and complexity justification.
- If the experiment matrix is broad but not diagnostic, add ablations that remove exactly one mechanism at a time.
- If the proposal claims robustness, define the perturbation or held-out condition explicitly.
- If the proposal depends on a stage-1 model, require stage-specific and full-pipeline ablations.
