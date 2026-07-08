# Default Stance For IEEE Transactions Writing

## Governing Principle

Write from formal objects outward: notation, assumptions, operators, objectives, algorithms, protocols, evidence, and only then prose. The writing target is a skeptical TCYB, THMS, or TNNLS reviewer who checks whether every sentence can be traced to a definition, equation, experiment, ablation, or limitation.

## Required Gate Before Drafting

Before drafting any section, verify that the user has supplied a passed proposal-writer package or equivalent material:

| Intake object | Drafting requirement |
|---|---|
| Notation Ledger | Every symbol used in prose or equations has a single meaning and scope. |
| Formal task | `\mathcal{X}`, `\mathcal{Y}`, source domains, target domains, predictor, and training-test separation are defined. |
| Objective | Empirical risk, total loss, auxiliary penalties, and loss weights are explicit. |
| Protocol | OOD split, target-domain definition, seeds or folds, checkpoint rule, metrics, and statistical policy are explicit. |
| Evidence | Baselines, ablations, sensitivity tests, visualization metrics, complexity numbers, and limitations are mapped to claims. |

If the gate fails, stop and return the blocked-gate report from `SKILL.md`. Do not draft around missing mathematics.

## Claim Discipline

- Use strong verbs only for directly supported findings.
- Use `under the specified OOD protocol` when claims depend on source-target splits.
- Use `supports`, `is consistent with`, or `indicates` for visualization-backed interpretations.
- Delete universal claims unless the protocol covers the universal setting.
- Mark any theorem, bound, or convergence statement with its assumptions and scope.

## Architecture Discipline

Do not describe a neural network as a sequence of components unless each component has a mathematical role. Define mappings such as

```text
X_i in R^{C x T}, h_i = G_theta(X_i), z_i = P_psi(h_i), p_i = C_phi(z_i).
```

Then explain why each operator exists: signal transformation, domain alignment, class separation, uncertainty weighting, invariant penalty, or deployment reduction.

## Evidence Discipline

Each major claim must map to one of these evidence types:

| Claim type | Minimum evidence |
|---|---|
| Accuracy or classification gain | Same split, same metric, strong baselines, mean and deviation where available |
| Robustness or generalization | Explicit unseen-domain, cross-subject, cross-session, cross-force, or leave-one-domain-out protocol |
| Module necessity | Remove, replace, or sensitivity ablation with the same evaluation protocol |
| Representation alignment | Quantitative compactness, separation, discrepancy, or target-risk metric plus bounded visualization |
| Efficiency | Parameters, FLOPs, memory, latency, throughput, or asymptotic complexity |
| Theory | Assumptions, statement, proof sketch or reference, and empirical test boundary |

## Intake JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["notation_ledger", "formal_task", "objective", "protocol", "evidence"],
  "properties": {
    "notation_ledger": {"type": "array", "items": {"type": "object"}},
    "formal_task": {"type": "object"},
    "objective": {"type": "object"},
    "protocol": {"type": "object"},
    "evidence": {"type": "array", "items": {"type": "object"}}
  }
}
```
