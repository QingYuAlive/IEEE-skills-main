# IEEE Polishing Strategy

Use this file when the user asks for more than grammar cleanup. It governs paragraph and section repair for IEEE Transactions manuscripts.

## Core Stance

Polishing is a technical review act. A fluent paragraph that hides missing notation, objective, protocol, ablation, or limitation is a failed edit.

## Technical Argument Chain

Strong IEEE writing follows this chain:

```text
formal task -> notation -> mechanism -> objective -> protocol -> evidence -> limitation
```

When the draft jumps from motivation to results without this chain, rebuild the paragraph order before sentence polishing.

## Claim, Evidence, Boundary

Every major statement needs:

1. `claim`: the exact technical assertion;
2. `evidence`: metric, protocol, ablation, theorem, or complexity result;
3. `boundary`: domains, assumptions, datasets, subjects, force levels, sessions, or operating conditions where the claim applies.

Typical failures:

- claim without metric or protocol;
- method description without equation;
- visualization presented as proof;
- theory language used to imply empirical dominance;
- ablation omitted while necessity is claimed.

## Section Responsibilities

### Introduction

Define the task, the shift or failure mode, and the technical mechanism. Contributions must map to method components and experiment evidence.

### Methods

Expose computational objects first: input, mapping, representation, loss, training, inference, and complexity. Flag qualitative architecture prose that lacks equations.

### Results

Report protocol, comparison, metric, ablation, and boundary. Do not substitute table labels for claims.

### Discussion

Explain why the mechanism may help under the reported evidence, where it fails, and what remains untested. This is where bounded interpretation belongs.

### Conclusion

Restate the contribution, decisive evidence, and scope boundary. Do not add new claims.

### Abstract

Compress problem, limitation, mechanism, algorithmic innovation, and evidence. Quantify only supplied results.

## Citation And Baseline Fairness

Citation and baseline language must disclose:

- whether the baseline uses the same input;
- whether the architecture capacity and training budget are comparable;
- whether the split and checkpoint rule are matched;
- whether cited work is a direct method, an adapted protocol, or contextual motivation.

## Overclaim Control

Flag and repair:

- `prove`, unless a theorem proves the stated mathematical claim;
- `state of the art`, unless baselines are broad, current, fair, and protocol-matched;
- `robust`, unless stress or OOD evidence is supplied;
- `generalizable`, unless target-domain evaluation is explicit;
- `necessary`, unless an ablation isolates the component.
