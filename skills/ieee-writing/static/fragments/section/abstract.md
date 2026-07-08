# Section: Abstract

## IEEE Four-Block Contract

Draft the abstract as one dense paragraph with four functional blocks in this order:

| Block | Required function | Content rule |
|---|---|---|
| 1. Problem Context And Baseline Limitation | Define the technical task and the failure mode of existing training or modeling practice. | Name the task, domain shift, nonstationarity, label condition, or deployment constraint. |
| 2. Proposed Mathematical Mechanism | State the proposed mechanism as an objective-level or operator-level contribution. | Mention the loss, invariant penalty, contrastive relation, reference encoder, uncertainty weight, or optimization constraint. |
| 3. Core Algorithmic Innovation | Explain how the mechanism aligns representations, controls generalization, or improves deployment. | Connect the mechanism to source-target, class-wise, time-frequency, cross-force, or cross-subject behavior. |
| 4. Defensive Empirical Proof And Metric Gains | Report the strongest verified evidence under the named protocol. | Include only provided metrics, deltas, datasets, OOD splits, ablations, and cost values. |

Do not use a five-sentence editorial summary pattern. Do not open with broad societal motivation. Do not include equations, citations, or unverified claims in the abstract, but every technical noun must be backed by equations and evidence elsewhere in the manuscript package.

## Required Inputs

- Formal task statement with `\mathcal{X}`, `\mathcal{Y}`, source domains, target domains, and predictor.
- One-sentence baseline limitation tied to ERM, standard regularization, domain-adversarial learning, contrastive learning, or task-specific prior methods.
- Total objective and the exact term that carries the main contribution.
- OOD protocol, metrics, baselines, ablation deltas, and complexity evidence.
- Boundary condition for claims that depend on dataset, subject, session, force level, operating condition, or modality.

## Drafting Rules

1. Use the first sentence to define the task and bottleneck, not the application hype.
2. Use the second functional block to name the mathematical mechanism, not to describe network wiring.
3. Use metric gains only when the user provided numbers and protocol details.
4. Use `under` phrases to bind claims to protocols, such as `under leave-one-force-level-out evaluation`.
5. End with a bounded contribution statement, not a promise of broad impact.

## Input JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["task", "baseline_limitation", "mechanism", "algorithmic_innovation", "empirical_evidence", "boundary"],
  "properties": {
    "task": {"type": "string"},
    "baseline_limitation": {"type": "string"},
    "mechanism": {"type": "string"},
    "algorithmic_innovation": {"type": "string"},
    "empirical_evidence": {
      "type": "object",
      "required": ["protocol", "metrics", "baselines", "ablations"],
      "properties": {
        "protocol": {"type": "string"},
        "metrics": {"type": "array", "items": {"type": "string"}},
        "baselines": {"type": "array", "items": {"type": "string"}},
        "ablations": {"type": "array", "items": {"type": "string"}}
      }
    },
    "boundary": {"type": "string"}
  }
}
```

## Output JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["abstract", "block_map", "claim_evidence_map", "unsupported_claims"],
  "properties": {
    "abstract": {"type": "string"},
    "block_map": {
      "type": "array",
      "items": {
        "type": "object",
        "required": ["block", "sentence_role"],
        "properties": {
          "block": {"type": "string"},
          "sentence_role": {"type": "string"}
        }
      }
    },
    "claim_evidence_map": {"type": "array", "items": {"type": "object"}},
    "unsupported_claims": {"type": "array", "items": {"type": "string"}}
  }
}
```

## Quality Gate

- The abstract contains all four blocks in order.
- No sentence claims robustness or generalization without a protocol phrase.
- No result appears without a metric and evaluation setting.
- No neural component is described without a mechanism-level term.
- The final sentence remains bounded to the tested domain and evidence.
