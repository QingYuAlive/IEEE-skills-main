# IEEE Section Patterns

Use this reference when drafting full sections or restructuring a manuscript.

## Abstract Pattern

1. Application or task pressure.
2. Technical limitation of existing methods.
3. Proposed mechanism and name.
4. Evaluation protocol and key result.
5. Engineering or scientific implication.

No citations. Avoid unexplained acronyms unless standard in the field.

## Introduction Pattern

Paragraph 1: Application setting and why the task matters.

Paragraph 2: Existing technical route and why it is insufficient under the target condition.

Paragraph 3: Core insight. Name the phenomenon your method exploits, such as class-preserving cross-force perturbation, time-frequency consistency, or reference-guided contrastive alignment.

Paragraph 4: Proposed framework. Mention modules only after the insight.

Paragraph 5: Contributions. Each contribution should include a method object and evidence object.

## Related Work Pattern

Use problem-centered clusters:

- Signal representation and neural architectures.
- Domain generalization and invariant learning.
- Contrastive/self-supervised/supervised contrastive learning.
- Multimodal or generative modeling when applicable.
- Robustness, uncertainty, or label noise when applicable.

End each cluster with the remaining gap.

## Method Pattern

Each subsection should have:

- Technical purpose.
- Symbols.
- Equation.
- Design rationale.
- Optimization or inference role.

## Experiments Pattern

1. Datasets and preprocessing.
2. Splits and protocol.
3. Baselines.
4. Implementation details.
5. Metrics and statistical tests.
6. Main comparison.
7. Ablation.
8. Sensitivity.
9. Visualization.
10. Complexity.

## Discussion Pattern

Discuss:

- Why the mechanism helps under the target shift.
- Which ablation supports this mechanism.
- Where performance is weak.
- Whether cost or training complexity limits use.
- What future experiment would test the next boundary.
