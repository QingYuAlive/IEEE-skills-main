# Structural Repair

Use this reference when prose is grammatically acceptable but logically weak.

## Paragraph Diagnostic

Check whether the paragraph has:

1. A topic sentence with a technical role.
2. Defined objects or section context.
3. Evidence or equation support.
4. Mechanism explanation.
5. Boundary or transition.

If two or more are missing, restructure before line editing.

## Method Paragraph Repair

Bad pattern:

```text
First, we use a CNN to extract features. Then, we use a contrastive module. Finally, we use a classifier.
```

Repair pattern:

```text
Given an input window X_i, the encoder G_theta extracts a representation h_i that preserves gesture-discriminative temporal and channel-wise patterns. The contrastive module then constrains h_i by defining positive samples across the target variation, while the classifier C_phi optimizes the supervised decision boundary.
```

## Results Paragraph Repair

Bad pattern:

```text
Table II shows the results. Our method is the best. This proves effectiveness.
```

Repair pattern:

```text
Table II evaluates whether the proposed alignment improves recognition under the held-out target condition. The proposed method achieves the highest mean accuracy and macro-F1 among the compared methods. The gain is most pronounced on the target split, which supports the role of the alignment term in reducing condition-specific feature bias.
```

## Chinese-to-English Repair

Common Chinese draft issue:

- Starts with broad background and delays the technical subject.
- Uses repeated "in order to" chains.
- Says "this paper" too often.
- Uses "obviously", "greatly", or "fully" without evidence.

Repair rules:

- Put the technical object early.
- Convert purpose chains into mechanism clauses.
- Replace "this paper proposes" repetition with module names.
- Convert broad claims into protocol-bound claims.

## Sentence Order for IEEE

Use:

1. Technical object.
2. Operation or constraint.
3. Why it matters.
4. Evidence or downstream effect.

Avoid:

1. Generic importance.
2. Long motivation.
3. Method name.
4. Delayed object.
