# Section: Introduction

## Mandatory IEEE Paragraph Flow

Write a four-part Introduction. Each part may be one or more paragraphs, but the functional order must not change.

| Part | Paragraph job | Required content |
|---|---|---|
| 1. Formal Task | Define the technical task and engineering setting. | Specify input, output, domain variables, signal or time-series properties, and evaluation target. |
| 2. OOD Failure | Explain the distribution shift and why ERM or standard regularization fails. | Name the changing factor, source-target mismatch, violated assumption, and failure mode. |
| 3. Technical Weapon | Introduce the proposed mechanism and its theoretical intuition. | Link contrastive alignment, invariant penalty, reference guidance, GroupDRO, IRM, or uncertainty weighting to the failure in Part 2. |
| 4. Contributions | List three or four contributions by category. | Use the categories Formalization/Theoretical Insights, Architectural/Algorithmic Innovation, and Extensive Empirical Validation. |

The first paragraph must open with the task, not broad societal motivation. A valid opening defines the recognition, prediction, adaptation, diagnosis, or control problem in technical terms.

## Contribution Taxonomy

Use this contribution structure:

1. **Formalization/Theoretical Insights:** state the formal problem, assumption, theorem, bound, invariant condition, or loss alignment.
2. **Architectural/Algorithmic Innovation:** state the operator, training schedule, pair construction, reference encoder, objective coupling, or complexity-aware design.
3. **Extensive Empirical Validation:** state the OOD protocol family, baselines, ablations, sensitivity tests, visualization metrics, statistical tests, and complexity analysis.
4. **Deployment Or Boundary Insight:** include only when the paper has measured cost, latency, memory, throughput, robustness limits, or failure-mode evidence.

## Prohibited Openings And Moves

- Do not begin with generic claims about artificial intelligence, healthcare, industrial automation, human-machine interaction, or neural networks.
- Do not claim ERM failure without defining the source and target distributions.
- Do not introduce the method name before the technical failure it addresses is explicit.
- Do not describe architecture as a component list unless equations or operators are introduced immediately.
- Do not list related work chronologically. Group prior work by technical obstacle.

## Input JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["formal_task", "ood_failure", "technical_weapon", "contributions", "evidence_scope"],
  "properties": {
    "formal_task": {
      "type": "object",
      "required": ["input", "output", "domains", "evaluation_target"],
      "properties": {
        "input": {"type": "string"},
        "output": {"type": "string"},
        "domains": {"type": "string"},
        "evaluation_target": {"type": "string"}
      }
    },
    "ood_failure": {
      "type": "object",
      "required": ["shift_factor", "erm_limitation", "standard_regularization_limitation"],
      "properties": {
        "shift_factor": {"type": "string"},
        "erm_limitation": {"type": "string"},
        "standard_regularization_limitation": {"type": "string"}
      }
    },
    "technical_weapon": {
      "type": "object",
      "required": ["mechanism", "equation_link", "theoretical_intuition"],
      "properties": {
        "mechanism": {"type": "string"},
        "equation_link": {"type": "string"},
        "theoretical_intuition": {"type": "string"}
      }
    },
    "contributions": {
      "type": "array",
      "minItems": 3,
      "maxItems": 4,
      "items": {
        "type": "object",
        "required": ["category", "claim", "support"],
        "properties": {
          "category": {"type": "string"},
          "claim": {"type": "string"},
          "support": {"type": "string"}
        }
      }
    },
    "evidence_scope": {"type": "string"}
  }
}
```

## Output JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["introduction", "paragraph_map", "contribution_map", "risk_flags"],
  "properties": {
    "introduction": {"type": "string"},
    "paragraph_map": {
      "type": "array",
      "items": {
        "type": "object",
        "required": ["part", "job", "main_claim"],
        "properties": {
          "part": {"type": "string"},
          "job": {"type": "string"},
          "main_claim": {"type": "string"}
        }
      }
    },
    "contribution_map": {"type": "array", "items": {"type": "object"}},
    "risk_flags": {"type": "array", "items": {"type": "string"}}
  }
}
```

## Reviewer Defense Checks

- The first paragraph defines the formal task before motivation.
- The OOD challenge names the shift factor and the unavailable target setting.
- The proposed mechanism is linked to a loss, operator, bound, or algorithmic update.
- Contributions are categorized, evidence-facing, and not marketing claims.
- The Introduction does not preview unsupported metric gains.
