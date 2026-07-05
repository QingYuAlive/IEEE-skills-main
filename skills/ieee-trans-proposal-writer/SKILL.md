---
name: ieee-trans-proposal-writer
description: >-
  Build rigorous IEEE Transactions-style research proposals and paper blueprints for TCYB, THMS, and TNNLS, especially for domain generalization, contrastive learning, signal/time-series deep learning, sEMG/EEG/IMU, CNN/RNN/Transformer, two-stage training, and experimental design. Use when the user asks for proposal writing, paper planning, innovation framing, argument maps, notation tables, research route design, experiment matrices, or Chinese requests such as 论文方案, 开题, 创新点设计, IEEE论文框架, 方法命名, 实验设计, or 论证链.
---

# IEEE Transactions Proposal Writer

Use this skill to convert a research idea into a defensible IEEE Transactions paper proposal.

## Mandatory First Read

Before doing any proposal work, read `../_shared/ieee-trans-guidelines.md`. Apply it as the controlling source for notation, equation-first method planning, experiment defense, visual evidence, and forbidden claim upgrades.

## Operating Stance

- Treat a proposal as a pre-submission engineering object, not a motivational essay.
- Build the argument before writing paragraphs.
- Require mathematical notation and a claim-evidence map before drafting polished text.
- Be strict about missing evidence, but keep the user moving by producing a bounded next version.
- Do not invent datasets, numerical results, citations, p-values, or final claims.

## Intake Protocol

Classify the request in one line:

- `idea-only`: topic or vague method direction.
- `method-known`: modules and training logic are available, results incomplete.
- `results-known`: experiments exist and need paper framing.
- `revision`: an existing proposal needs repair.

Then extract:

- Target venue: TCYB, THMS, TNNLS, or generic IEEE Transactions.
- Task: classification, regression, generation, diagnosis, representation learning, or multimodal fusion.
- Data regime: subject/session/force/domain split, labels, target availability.
- Proposed mechanism: invariance, contrastive alignment, perturbation, uncertainty, sparsity, reconstruction, adversarial training, two-stage reference learning.
- Evidence available: datasets, baselines, ablations, visualizations, complexity.

Ask questions only when the answer changes the proposal structure. Otherwise proceed with clearly marked assumptions.

## Blocking Gate: Notation and Argument Map

Do not write a polished proposal narrative until these are present in your answer:

1. A notation table covering data, domains, representations, modules, losses, and protocol.
2. An argument map connecting each claimed gap to a method mechanism and each mechanism to an experiment.
3. A risk table identifying claims that are not yet supportable.

If the user refuses or lacks information, produce a minimal notation draft and a missing-input list instead of skipping the gate.

Load `references/notation-and-argument-map.md` when building or repairing these tables.

## Proposal Construction Workflow

1. **Scope**: State the target task, target venue, and paper type.
2. **Problem formulation**: Define domains, data, target condition, and learning objective.
3. **Gap diagnosis**: Identify the technical gap as a failure of existing formal assumptions, pair construction, feature representation, or evaluation protocol.
4. **Core hypothesis**: State one mechanism-level hypothesis, not a list of modules.
5. **Method blueprint**: Define modules and losses in equation order.
6. **Training plan**: Specify stages, frozen/reference modules, update order, and inference path.
7. **Experiment matrix**: Main comparison, ablations, sensitivity, visualization, complexity, and statistical test.
8. **Claim calibration**: Label claims as ready, conditional, or not yet supported.
9. **Deliverable**: Provide a proposal skeleton or full proposal depending on user request.

Load `references/proposal-qa-rubric.md` before finalizing a proposal or when the user asks whether the idea is strong enough.

## Output Contract

Default output:

```text
Proposal Setup
- Target venue:
- Task and data regime:
- Current maturity:
- Main risk:

Notation Table
| Symbol | Meaning | Where used | Status |

Argument Map
| Gap | Mechanism | Formal object | Evidence needed | Claim strength |

Method Blueprint
1. Problem formulation
2. Architecture and representations
3. Objective functions
4. Training and inference

Experiment Defense Matrix
| Claim | Dataset/split | Baseline | Ablation | Metric | Visualization | Risk |

Draft Proposal
[Only after the notation and argument map are established.]

Next Evidence To Collect
```

## Red Lines

- Do not describe a network only as a sequence of layers.
- Do not call a module novel because it combines known modules; identify the new constraint, pair logic, objective, or protocol.
- Do not claim domain generalization without an unseen-domain split.
- Do not claim robustness without perturbation, noise, cross-condition, or sensitivity evidence.
- Do not propose an ablation that fails to isolate the mechanism.
- Do not hide a negative or mixed ablation; use it to refine the claim.

## Related References

| File | Open when |
|---|---|
| `references/notation-and-argument-map.md` | Creating the mandatory notation table, claim map, or loss/module map |
| `references/proposal-qa-rubric.md` | Final proposal audit, novelty-risk check, or experiment-defense scoring |
