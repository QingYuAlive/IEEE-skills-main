# IEEE Stopping Rules

Stop rather than continue drafting or polishing when any condition holds.

## Hard Stops

```text
math gate failed
OOD protocol missing for a robustness/generalization claim
objective function missing or inconsistent with claimed mechanism
contrastive pair sets undefined
IRM/GroupDRO/DRO penalty or constraint undefined
ablation cannot isolate the proposed module
theory claimed without assumptions/proof boundary
complexity claim made without cost evidence
target leakage cannot be ruled out
```

When a hard stop occurs, output:

1. Current gate status.
2. The missing formal object or evidence.
3. Why drafting would be misleading.
4. The minimum next input needed.
5. A safe scaffold that does not overclaim.

## Soft Stops

```text
max 3 revision rounds reached
two consecutive QA score improvements < 0.5
all allowed claims are already contract-bound
user's current deliverable has been reached
```

Soft stops may end the current loop, but must preserve unresolved risks.

## Never Do This

- Do not hide a failed gate with smoother English.
- Do not write a polished abstract while the objective is missing.
- Do not call a visualization proof.
- Do not convert a mechanism intuition into a theorem.
- Do not use "future work" to cover a missing core experiment.
