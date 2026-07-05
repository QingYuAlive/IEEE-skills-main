# Theory and Formalization Loophole Checklist

Use this when reviewing methods, equations, assumptions, and theoretical claims.

## Notation

Flag:

- Symbols used before definition.
- Same symbol reused for different objects.
- Domain variable undefined.
- Loss weights introduced without tuning or learning policy.
- Shape of signal tensors missing.
- Pair sets missing for contrastive losses.

## Problem Setting

Check:

- Are source and target domains formally defined?
- Is category shift absent or handled?
- Are labels available in all source domains?
- Is the target domain used in model selection?
- Are subject/session/force conditions confused with random splits?

## Objective

Check:

- Does each objective term have a defined input?
- Does each term optimize the claimed representation?
- Are weights fixed, searched, scheduled, or learned?
- Are gradients applied to the intended modules?
- Is the total objective consistent with the algorithm?

## Algorithm

Check:

- Sampling rule.
- Update order.
- Frozen versus trainable modules.
- Stage boundary.
- Reference/teacher/EMA distinction.
- Inference path.

## Theory Claims

Flag:

- Theorem assumptions not satisfied by experiments.
- Flatness/invariance/sparsity claims without empirical proxy.
- Proof of optimization property used as proof of accuracy.
- Risk formulation that does not match the evaluated metric.
- Domain-invariant language without multiple environments.

## Repair Suggestions

- Add an assumptions paragraph before the objective.
- Move notation before equations.
- Add a total objective after individual losses.
- Add an algorithm block.
- Add a paragraph connecting theorem assumptions to experimental protocol.
- Calibrate theory wording: theorem supports a property under conditions; experiments evaluate utility.
