# IEEE Introduction Reference Guide

Use this guide when building or repairing the Introduction for TCYB, THMS, TNNLS, or generic IEEE Transactions papers.

## Paragraph-Level Contract

| Part | Required lead | Required exit |
|---|---|---|
| Formal Task | Define the task using input, output, domains, and target metric. | End with the engineering obstacle that makes the task nontrivial. |
| OOD Failure | Define source-target mismatch and why ERM or standard regularization is insufficient. | End with the missing mechanism needed to control target-domain risk. |
| Technical Weapon | Introduce the proposed operator, objective, pair relation, invariant penalty, or training schedule. | End by linking the mechanism to a testable hypothesis. |
| Contributions | State three or four categorized contributions. | End with an evidence-facing summary, not a promise of impact. |

## Prior-Work Synthesis

Group prior work by obstacle:

1. Signal or time-series representation.
2. Domain generalization, adaptation, or robustness.
3. Contrastive, invariant, adversarial, or distributionally robust learning.
4. Deployment cost, latency, interpretability, or human-machine constraints.

Each prior-work paragraph must end with a technical reason why existing methods do not solve the paper's formal target setting.

## Contribution Wording

Use category labels directly:

- **Formalization/Theoretical Insights:** formal problem statement, assumption, bound, convergence argument, invariant condition, or objective decomposition.
- **Architectural/Algorithmic Innovation:** operator design, pair construction, stage coupling, reference-guided update, objective weighting, or inference simplification.
- **Extensive Empirical Validation:** OOD protocol, baseline tiers, ablation map, sensitivity analysis, visualization metrics, statistical test, and complexity report.

## Input JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["task_definition", "prior_work_obstacles", "proposed_mechanism", "contributions"],
  "properties": {
    "task_definition": {"type": "object"},
    "prior_work_obstacles": {"type": "array", "items": {"type": "string"}},
    "proposed_mechanism": {"type": "object"},
    "contributions": {"type": "array", "items": {"type": "object"}}
  }
}
```

## Output JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["introduction", "paragraph_roles", "contribution_table", "unsupported_edges"],
  "properties": {
    "introduction": {"type": "string"},
    "paragraph_roles": {"type": "array", "items": {"type": "object"}},
    "contribution_table": {"type": "array", "items": {"type": "object"}},
    "unsupported_edges": {"type": "array", "items": {"type": "string"}}
  }
}
```

## Repair Checklist

- The first sentence names the technical task.
- Each limitation has a technical cause, not only a performance complaint.
- The method appears only after the gap is defined.
- Contribution bullets map to method equations and experiment evidence.
- OOD, robustness, and invariance claims are protocol-bound.
