# IEEE Transactions Article Patterns

Use this file when polishing should improve the technical argument, not just English. The patterns reflect IEEE-style machine-learning, neural-network, bio-signal, time-series, and domain-generalization manuscripts.

## Full-Manuscript Pattern

```text
formal task -> source-target or operating-condition challenge -> mathematical mechanism -> algorithmic implementation -> protocol-bound evidence -> ablation defense -> complexity and limitation
```

Do not polish around a missing link. Flag the missing formal object.

## Abstract Pattern

IEEE abstracts should compress four functions:

1. technical problem and baseline limitation;
2. proposed mathematical or algorithmic mechanism;
3. representation, alignment, optimization, or inference innovation;
4. protocol-bound empirical evidence and metric gain.

Polishing rule: remove broad opening motivation and replace it with the formal task. Quantify only results supplied by the user.

## Introduction Pattern

Strong introductions move in this order:

1. define the formal task and engineering setting;
2. explain the source-target, subject, session, force, modality, or operating-condition shift;
3. identify why ERM, standard regularization, or existing alignment methods are insufficient;
4. introduce the technical mechanism and its intuition;
5. list categorized contributions with evidence hooks.

Polishing rule: do not improve flow by adding broad motivation. Improve flow by making the technical dependency chain explicit.

## Method Pattern

Method polishing follows this order:

1. notation and problem setting;
2. input-space processing;
3. latent mapping and inference path;
4. objective terms and constraints;
5. training schedule or algorithm;
6. complexity and deployment cost.

Polishing rule: when a method paragraph is mostly component prose, flag it for equation-level repair.

## Results Pattern

Results paragraphs should follow:

```text
protocol -> comparison -> measured effect -> mechanism interpretation -> boundary
```

Polishing rule: do not write `Table I shows...` as the main claim. State the reviewer-relevant comparison and use the table as support.

## Discussion Pattern

Discussion should explain:

- why the mechanism plausibly improves the observed metric;
- which ablations support that interpretation;
- which domains, subjects, sessions, or operating conditions remain difficult;
- what future work follows from the limitation.

Do not restate the result table. Do not imply that theory proves empirical dominance.

## Conclusion Pattern

Conclusions should be compact:

1. bounded contribution;
2. strongest protocol-bound evidence;
3. mechanism-supported interpretation;
4. limitation or deployment boundary.

Do not introduce new claims, new citations, or new experiments.

## Title Pattern

Strong IEEE titles are searchable and technical:

```text
mechanism or model family + task + target setting
```

Avoid empty prestige words. Prefer terms that identify the method, task, and domain condition.
