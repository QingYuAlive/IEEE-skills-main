# IEEE Proposal QA Rubric

Use this rubric before drafting prose, before exporting a proposal, and whenever the user asks whether an IEEE Transactions idea is ready. Score hard gates first. A high prose score cannot compensate for missing formalization or missing OOD evidence.

## Hard Fail Gates

Any one of these blocks polished writing:

1. No formal input space `\mathcal{X}` or label space `\mathcal{Y}`.
2. No source-domain and target/OOD-domain definition.
3. Neural network described only in plain English without mappings such as `h = G_\theta(x)` and `\hat{y}=C_\phi(h)`.
4. No empirical risk or total objective.
5. Robustness/generalization/invariance claimed without a named OOD test protocol.
6. Contrastive learning claimed without positive/negative pair definitions.
7. IRM/GroupDRO/VREx/DRO claimed without environment risks and the exact penalty or constraint.
8. No ablation plan for each proposed loss/module.
9. No complexity, latency, parameter, FLOP, or training-overhead plan when adding modules.
10. Theoretical guarantee claimed without assumptions, statement, proof sketch, and boundary.

If any hard fail is present, return `Blocked Math Gate` or `Blocked Evidence Gate`; do not draft abstract, introduction, contribution bullets, or polished method prose.

## Scoring Scale

Score each dimension from 0 to 3.

| Score | Meaning |
|---|---|
| 0 | Missing or contradicted |
| 1 | Present only as vague prose |
| 2 | Mostly formalized but incomplete or weakly defended |
| 3 | IEEE-ready: formal, testable, and evidence-linked |

## Dimensions

### 1. Formal Problem Definition

- 0: Task is described narratively only.
- 1: Dataset/task named but no `\mathcal{X}`, `\mathcal{Y}`, domains, or target rule.
- 2: Spaces and domains present but target availability or category-shift assumption is unclear.
- 3: Input/label spaces, domains, target/OOD rule, data tensors, and assumptions are explicit.

### 2. Network as Equations

- 0: Plain-English layer walkthrough only.
- 1: Module names listed but no formal mappings.
- 2: Encoder/classifier mappings present but shapes, projectors, or training-only modules are unclear.
- 3: Every module has input, output, parameters, role, and inference/training status.

Penalty trigger: subtract 1 if the proposal says "we first use CNN/LSTM/Transformer..." without defining the computational object.

### 3. Objective Stack

- 0: No objective.
- 1: Cross-entropy or task loss only, with unsupported robustness claims.
- 2: DG/contrastive/regularization terms present but weights, gradients, or pair sets are incomplete.
- 3: Empirical risk, auxiliary objectives, total loss, weights/schedules, and optimization order are fully specified.

### 4. OOD and Domain-Generalization Protocol

- 0: Random split only while claiming generalization.
- 1: OOD variable implied but not formalized.
- 2: Held-out protocol stated but validation/checkpoint or seeds/folds missing.
- 3: Source/target domains, held-out protocol, validation rule, metrics, seeds/folds, and leakage prevention are explicit.

Penalty trigger: any claim of "robust", "domain-invariant", "force-invariant", or "generalizable" without this section is P0.

### 5. Theoretical Support

- 0: Theory claimed but absent.
- 1: Intuition written as if it were proof.
- 2: Assumptions/proposition present but proof boundary or experiment relation is weak.
- 3: Assumptions, theorem/proposition, proof sketch, complexity or convergence analysis, and boundary are explicit.

Penalty trigger: if no theorem is available, the proposal must say "mechanism analysis" instead of "proof".

### 6. Ablation-Defense Matrix

- 0: No ablation plan.
- 1: Only "w/o module" list, not mapped to claims.
- 2: Removal tests exist but replacement tests, hyperparameter sensitivity, or OOD split are missing.
- 3: Each module/loss has remove, replace, sensitivity, expected failure mode, metric, and OOD split.

### 7. Baseline Fairness

- 0: No baselines or only weak baselines.
- 1: Baselines listed without fairness policy.
- 2: Several relevant baselines but missing DG/contrastive/recent specialized tier.
- 3: Classical, plain deep, mechanism-specific, recent specialized, and internal ablations are justified with equal protocol.

### 8. Visualization Discipline

- 0: Visualization used as proof.
- 1: t-SNE/PCA/confusion/spectrum planned without metric link.
- 2: Visualizations linked to metrics but feature source, seed, or sample policy missing.
- 3: Visualization has source, seed/sample policy, metric/ablation linkage, and explicit limitation.

### 9. Complexity and Deployment

- 0: Added module has no cost discussion.
- 1: Vague "lightweight/efficient" claim.
- 2: Parameter or FLOP estimate present but no baseline comparison or inference path.
- 3: Parameters, FLOPs/asymptotic cost, memory/latency/throughput where relevant, training overhead, and inference modules are clear.

### 10. Claim Calibration

- 0: Claims exceed evidence.
- 1: Some hedging but unsupported novelty or robustness remains.
- 2: Most claims are protocol-bound; a few broad phrases remain.
- 3: Every claim maps to objective, evidence, ablation, protocol, and boundary.

## Readiness Bands

```text
Any hard fail     Blocked: do not draft prose
0-14             Not paper-shaped; formalize first
15-22            Internal method sketch; build objectives and protocols
23-27            Proposal draftable after targeted repairs
28-30            IEEE-ready proposal foundation
```

## QA Output Format

```text
Gate Result
- Math gate:
- Evidence gate:
- Theory gate:

Scores
| Dimension | Score | Reason | Required repair |

P0/P1 Issues
1.

Allowed Next Action
- formalize only / design experiments / draft bounded proposal / polish
```
