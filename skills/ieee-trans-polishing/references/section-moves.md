# IEEE Section Moves

Use this file only after the main section logic has been decided in `SKILL.md`. The goal is to polish section-level movement into reviewer-defensible technical order.

## Abstract

Move order:

1. technical task and baseline limitation;
2. proposed mechanism or objective;
3. algorithmic role of the mechanism;
4. protocol-bound evidence and metric gain;
5. bounded implication.

Polishing checks:

- Remove broad motivation.
- Bind results to protocol.
- Avoid equations in the abstract, but preserve formal nouns already defined elsewhere.

## Introduction

Move order:

1. formal task and engineering setting;
2. source-target, subject, session, force, modality, or operating-condition shift;
3. failure of ERM, standard regularization, or existing alignment strategies;
4. proposed mechanism and theoretical intuition;
5. categorized contributions with evidence hooks.

Useful moves:

- `This paper studies ... as ...`
- `The challenge is that ... changes across domains while ... remains shared.`
- `This mismatch makes ERM insufficient because ...`
- `The proposed objective addresses this issue by ...`

Avoid opening with field-scale motivation before defining the task.

## Methods

Move order:

1. notation and problem setting;
2. input processing;
3. encoder, projector, classifier, and inference path;
4. objective terms and optimization constraints;
5. training stages or update algorithm;
6. complexity and implementation details.

Useful moves:

- `Let $X_i\in\mathbb{R}^{C\times T}$ denote...`
- `The encoder maps each input to...`
- `The total objective is...`
- `At inference, ... is discarded and predictions are computed by...`

Avoid component lists without equations.

## Results

Move order:

1. protocol and evaluation setting;
2. comparison group;
3. measured effect;
4. ablation or mechanism interpretation;
5. claim boundary.

Useful moves:

- `Under the held-out target-domain protocol, ...`
- `Compared with the matched ERM baseline, ...`
- `Removing $\mathcal{L}_{\mathrm{con}}$ reduces ..., indicating ...`
- `This claim is restricted to ...`

Avoid passive table narration.

## Discussion

Move order:

1. central mechanism interpretation;
2. evidence that supports the interpretation;
3. alternative explanations or weak domains;
4. limitation;
5. future work grounded in the limitation.

Useful moves:

- `The ablation results support the interpretation that...`
- `A remaining explanation is...`
- `The evidence does not establish...`

Avoid restating all results.

## Conclusion

Move order:

1. bounded contribution;
2. strongest protocol-bound evidence;
3. mechanism-supported interpretation;
4. limitation or deployment boundary.

Avoid new data, new theory, or untested deployment claims.

## Title

Move order:

1. method or mechanism;
2. task;
3. target condition or domain.

Useful patterns:

- `Contrastive Alignment for Cross-Force sEMG Gesture Recognition`
- `Invariant Risk Penalization for Source-Only Time-Series Generalization`
- `Reference-Guided Representation Learning Under Held-Out Operating Conditions`

Avoid empty novelty words and rhetorical hooks.
