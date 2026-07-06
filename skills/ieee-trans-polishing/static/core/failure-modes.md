# Diagnose Failure Mode Before Editing

Before rewriting, classify the main failure. Fix failures in this order:

```text
notation -> mathematical object -> objective -> protocol -> evidence -> paragraph logic -> sentence polish
```

## IEEE Polishing Failure Modes

| Failure mode | Symptom | Required response |
|---|---|---|
| Missing notation | Prose says "feature", "domain", or "loss" without symbols. | Request or restore the Notation Ledger and use the canonical symbol. |
| Plain-English method | Network or algorithm is described as a workflow only. | Flag for equation or algorithm replacement. |
| Objective gap | A component is said to improve robustness without a loss term or penalty. | Request objective, coefficient, and role. |
| Protocol gap | Results claim OOD or generalization without target-domain definition. | Bind wording to the available protocol or flag missing protocol. |
| Evidence inflation | Visualization, intuition, or single result is written as proof. | Downgrade verb and request quantitative evidence or ablation. |
| Ablation gap | A module is called necessary without removal or replacement evidence. | Replace with a bounded design rationale or flag missing ablation. |
| Complexity gap | A practical or deployable claim lacks parameters, FLOPs, memory, latency, or throughput. | Request measured or asymptotic cost. |
| Sentence clutter | Logic is correct but overloaded. | Split, tighten, and clarify. |

## Do Not Beautify These Sentences

- Sentences that hide missing equations behind fluent mechanism prose.
- Sentences that say a model is robust without an unseen-domain protocol.
- Sentences that say a method outperforms without naming metric, baseline, and split.
- Sentences that use `significant` without statistical or practical criterion.
- Sentences that vary terminology for style and break the Notation Ledger.

Return a formalization flag before polishing when these failures appear.
