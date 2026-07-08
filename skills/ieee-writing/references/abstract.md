# IEEE Abstract Reference Guide

Use this guide when the abstract needs deeper diagnosis than the section fragment provides. The abstract must be short, unstructured, citation-free, and evidence-bound.

## Four-Block Diagnostic Matrix

| Block | Diagnostic question | Failure mode to repair |
|---|---|---|
| Problem Context And Baseline Limitation | Does the first sentence define the exact technical task and what current learning practice fails to handle? | The opening is motivational, social, or too broad for TCYB, THMS, or TNNLS. |
| Proposed Mathematical Mechanism | Does the abstract name the objective-level mechanism that distinguishes the method? | The method is introduced as an architecture name without a loss, constraint, alignment rule, or operator role. |
| Core Algorithmic Innovation | Does the abstract explain how the mechanism changes representation, optimization, or inference behavior? | The abstract lists modules without explaining why they affect OOD risk or target-domain behavior. |
| Defensive Empirical Proof | Does each performance claim include the evaluation setting and provided metrics? | The abstract says the method is robust or generalizable without the target-domain protocol. |

## Compression Rules

- Merge task and baseline limitation into one sentence when the target venue is strict on abstract length.
- Merge mechanism and algorithmic innovation only when the mechanism is self-explanatory from the objective.
- Keep only the strongest verified metric, strongest OOD protocol, and strongest ablation cue.
- Delete implementation details that do not explain the core mathematical mechanism.

## Claim Calibration

| Draft claim | Required support |
|---|---|
| improves accuracy | Metric, dataset, split, and baseline |
| improves robustness | Perturbation or unseen-domain protocol |
| improves generalization | Source-target split with unavailable target during training |
| learns invariant features | Defined invariant objective plus representation evidence |
| reduces complexity | Parameters, FLOPs, memory, latency, throughput, or asymptotic cost |

## Input JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["technical_task", "baseline_failure", "mechanism", "algorithmic_effect", "empirical_proof"],
  "properties": {
    "technical_task": {"type": "string"},
    "baseline_failure": {"type": "string"},
    "mechanism": {"type": "string"},
    "algorithmic_effect": {"type": "string"},
    "empirical_proof": {
      "type": "object",
      "required": ["protocol", "metric_statements", "ablation_statement"],
      "properties": {
        "protocol": {"type": "string"},
        "metric_statements": {"type": "array", "items": {"type": "string"}},
        "ablation_statement": {"type": "string"}
      }
    }
  }
}
```

## Output JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["abstract", "diagnostic_matrix", "claims_to_verify"],
  "properties": {
    "abstract": {"type": "string"},
    "diagnostic_matrix": {"type": "array", "items": {"type": "object"}},
    "claims_to_verify": {"type": "array", "items": {"type": "string"}}
  }
}
```
