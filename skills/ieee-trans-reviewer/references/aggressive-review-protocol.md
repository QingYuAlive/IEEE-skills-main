# Aggressive Review Protocol

Use this reference to produce a strict IEEE Transactions pre-submission review.

## First-Pass Extraction

Extract:

- Central claim.
- Claimed novelty.
- Formal problem setting.
- Method mechanism.
- Main evidence.
- Strongest missing evidence.
- Most likely reviewer attack.

If any of these cannot be extracted, that is itself a major concern.

## Major Concern Patterns

### Novelty Is Only a Module Combination

Attack:

```text
The manuscript combines known modules without identifying a new constraint, objective, or protocol.
```

Repair:

- Define the new mathematical relation.
- Show why existing objectives fail.
- Add ablations that separate the new relation from known components.

### Domain Generalization Claim Without Unseen Domain

Attack:

```text
The evaluation does not isolate an unseen target condition, so the generalization claim is unsupported.
```

Repair:

- Add leave-one-domain/subject/session/force/load-out splits.
- Report per-target results and variance.
- Compare DG-specific baselines.

### Contrastive Pair Logic Is Unjustified

Attack:

```text
The positive and negative pairs do not match the invariance claim.
```

Repair:

- Define pair sets mathematically.
- Explain why pair membership preserves class semantics.
- Ablate pair construction.

### Weak Baseline Set

Attack:

```text
The baselines do not test the claimed mechanism or are not current enough for the venue.
```

Repair:

- Add classical, deep, DG/contrastive, and recent signal-specific baselines as relevant.
- State implementation fairness.

### Missing Complexity Analysis

Attack:

```text
The proposed module adds training or inference cost without reporting parameters, memory, throughput, latency, or complexity.
```

Repair:

- Add a cost table.
- State which modules are training-only.
- Compare cost to accuracy/generalization gain.

## Review Tone

Be concise and specific. Avoid generic "needs more experiments" unless naming the exact missing experiment.
