# Result Analysis Tightening

Use this reference for polishing experiment and discussion text.

## Table Analysis

A tight result paragraph should name:

- Dataset or split.
- Metric.
- Best and relevant second-best comparison.
- Mechanism-level interpretation.
- Evidence boundary.

Do not narrate every number.

## Ablation Analysis

Write ablation analysis as:

```text
Removing [component] changes [metric] on [split], indicating that [component] mainly contributes to [mechanism]. The smaller/larger effect on [other split] suggests [boundary].
```

If an ablation is negative, do not bury it. Explain whether the module helps only after stage coupling, only under severe shift, or only for certain classes/domains.

## t-SNE/PCA Analysis

Use this safe form:

```text
The projection provides qualitative support for the quantitative results: features learned by [method] form more compact class-wise clusters and show less visible domain separation than [baseline]. Since low-dimensional projection can distort distances, this visualization is interpreted together with [metric/table].
```

## Confusion Matrix Analysis

Mention:

- Which classes improve.
- Which classes remain confused.
- Whether errors correspond to signal similarity, force level, or label ambiguity.
- Whether macro-F1 supports the claim.

## Sensitivity Analysis

Use:

```text
The method remains stable when [parameter] lies in [range], while performance decreases at [extreme] because [mechanism]. We therefore use [default] in all main experiments.
```

Do not select a single best point without reporting the tested range.

## Discussion Tightening

A strong Discussion does not repeat the Results section. It explains:

- Why the objective affects the target shift.
- Which ablation confirms the mechanism.
- Why some splits/classes remain difficult.
- What added cost the method introduces.
- What future experiment would test the remaining boundary.
