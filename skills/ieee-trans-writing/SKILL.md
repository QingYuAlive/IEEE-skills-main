---
name: ieee-trans-writing
description: Draft, restructure, or audit IEEE Transactions-style manuscript sections for TCYB, THMS, TNNLS, and adjacent machine-learning, neural-network, bio-signal, time-series, domain-generalization, and contrastive-learning papers. Use when the user wants mathematically grounded academic writing for abstracts, introductions, related work, methods, experiments, discussion, conclusions, titles, or full manuscript argument plans, especially when claims require notation ledgers, formal objectives, OOD protocols, ablations, complexity analysis, or reviewer-facing empirical defense.
---

# IEEE Transactions Writing Router

This skill drafts IEEE Transactions manuscript prose only after the paper has passed a mathematical intake gate. Treat TCYB, THMS, and TNNLS reviewers as technically adversarial: every claim must be tied to notation, an objective, a protocol, an ablation, a bound, or a stated limitation.

## Required Reading Order

1. Read `../_shared/ieee-trans-guidelines.md` before using any local fragment.
2. Read the corpus analysis only when the task asks for venue-specific justification, section design, or reviewer defense:
   - `../../analysis/corpus_evidence.md`
   - `../../analysis/key_reading_pack.md`
   - `../../analysis/corpus_manifest.tsv`
3. Read `manifest.yaml`.
4. Read every file listed in `always_load`.
5. Detect request axes from the manifest and read only the mapped fragments needed for the requested section, paper type, language, and journal.

## Mathematical Intake Gate

Do not draft prose until the user has already passed the `ieee-trans-proposal-writer` math gate or has supplied equivalent material in the current request.

The gate is passed only when all required objects are available:

| Gate item | Required content |
|---|---|
| Notation Ledger | Symbols for data, domains, representations, losses, weights, metrics, and protocol variables |
| Task formalization | Input space `\mathcal{X}`, label or output space `\mathcal{Y}`, source domains, unavailable target domains, and prediction function |
| Objective | Empirical risk and total training objective with every loss weight defined |
| Generalization protocol | Explicit OOD split, target-domain definition, checkpoint rule, seed or fold policy, and metrics |
| Mechanism map | Each claimed mechanism mapped to an equation, algorithm step, ablation, or theoretical condition |
| Evidence ledger | Main comparisons, ablations, sensitivity tests, visualization metrics, complexity evidence, and known limitations |

If any gate item is missing, refuse to draft the section and return a gate report using this schema:

```json
{
  "status": "blocked_by_math_gate",
  "missing_gate_items": [
    "notation_ledger",
    "task_formalization",
    "objective",
    "generalization_protocol",
    "mechanism_map",
    "evidence_ledger"
  ],
  "minimum_user_inputs_needed": {
    "notation_ledger": "A table defining data, domains, mappings, losses, weights, metrics, and protocol variables.",
    "task_formalization": "A formal statement of input space, output space, source domains, target domains, and prediction function.",
    "objective": "The empirical risk and total objective with all auxiliary losses and coefficients.",
    "generalization_protocol": "The OOD split, target-domain construction, metrics, seeds or folds, and checkpoint rule.",
    "mechanism_map": "A mapping from each claimed contribution to equations, algorithm steps, ablations, or theoretical conditions.",
    "evidence_ledger": "Tables, figures, metric deltas, ablations, sensitivity tests, complexity numbers, and limitations."
  },
  "draft_allowed": false
}
```

Do not replace missing gate items with assumptions. A scaffold may be returned only if the user explicitly asks for a scaffold, and the scaffold must not contain invented symbols, numbers, citations, or experimental claims.

## Routing Protocol

1. **Load the active layers.** Use the required reading order above.
2. **Detect axes.** Decide `paper_type`, `section`, `language`, and `journal` from `manifest.yaml`. Default to `algorithmic`, `en`, and `generic-ieee` when unspecified.
3. **State the route.** Before drafting, report one concise line containing detected axes and gate status.
4. **Apply fragments in priority order.**
   1. Shared IEEE guidelines.
   2. Local core stance, workflow, and output format.
   3. Paper-type fragment.
   4. Section fragment.
   5. Journal fragment.
   6. Language fragment.
5. **Open references only on demand.** Use `references.on_demand` from the manifest. Prefer IEEE-specific reference guides and avoid loading inactive legacy files unless the user explicitly requests conversion from an old draft.

## Red Lines

- Never write an abstract using the broad-journal five-sentence editorial formula. Use the IEEE four-block abstract contract from `static/fragments/section/abstract.md`.
- Never open an Introduction with broad societal hype. The first paragraph must define the technical task and engineering challenge.
- Never describe a neural architecture qualitatively without immediate equation backing. A sentence such as "the signal passes through three normalized CNN blocks" is invalid unless the mapping, tensor shapes, and operator role are defined.
- Never claim robustness, invariance, domain generalization, or OOD performance without an explicit target-domain protocol.
- Never treat t-SNE, PCA, confusion matrices, spectra, or saliency maps as proof without quantitative support.
- Never call a component necessary unless a removal, replacement, or sensitivity ablation isolates it.
- Never use theorem language to imply empirical dominance. State the theorem condition and the experimental test separately.

## Input Schema For Drafting

Use this schema to decide whether the request is draftable:

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": [
    "target_journal",
    "section",
    "notation_ledger",
    "task_formalization",
    "objective",
    "generalization_protocol",
    "mechanism_map",
    "evidence_ledger",
    "draft_request"
  ],
  "properties": {
    "target_journal": {
      "type": "string",
      "enum": ["TCYB", "THMS", "TNNLS", "generic-ieee"]
    },
    "section": {
      "type": "array",
      "items": {
        "type": "string",
        "enum": ["abstract", "intro", "related-work", "method", "experiments", "discussion", "conclusion", "title"]
      },
      "minItems": 1,
      "uniqueItems": true
    },
    "notation_ledger": {
      "type": "array",
      "items": {
        "type": "object",
        "required": ["symbol", "meaning", "scope"],
        "properties": {
          "symbol": {"type": "string"},
          "meaning": {"type": "string"},
          "scope": {"type": "string"}
        }
      }
    },
    "task_formalization": {
      "type": "object",
      "required": ["input_space", "output_space", "source_domains", "target_domains", "predictor"],
      "properties": {
        "input_space": {"type": "string"},
        "output_space": {"type": "string"},
        "source_domains": {"type": "array", "items": {"type": "string"}},
        "target_domains": {"type": "array", "items": {"type": "string"}},
        "predictor": {"type": "string"}
      }
    },
    "objective": {
      "type": "object",
      "required": ["empirical_risk", "total_objective", "loss_terms"],
      "properties": {
        "empirical_risk": {"type": "string"},
        "total_objective": {"type": "string"},
        "loss_terms": {"type": "array", "items": {"type": "string"}}
      }
    },
    "generalization_protocol": {
      "type": "object",
      "required": ["ood_split", "metrics", "checkpoint_rule", "seeds_or_folds"],
      "properties": {
        "ood_split": {"type": "string"},
        "metrics": {"type": "array", "items": {"type": "string"}},
        "checkpoint_rule": {"type": "string"},
        "seeds_or_folds": {"type": "string"}
      }
    },
    "mechanism_map": {
      "type": "array",
      "items": {
        "type": "object",
        "required": ["claim", "equation_or_algorithm", "validation"],
        "properties": {
          "claim": {"type": "string"},
          "equation_or_algorithm": {"type": "string"},
          "validation": {"type": "string"}
        }
      }
    },
    "evidence_ledger": {
      "type": "array",
      "items": {
        "type": "object",
        "required": ["evidence_type", "protocol", "result", "claim_supported"],
        "properties": {
          "evidence_type": {"type": "string"},
          "protocol": {"type": "string"},
          "result": {"type": "string"},
          "claim_supported": {"type": "string"}
        }
      }
    },
    "draft_request": {
      "type": "string"
    }
  }
}
```

## Output Schema For Successful Drafts

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": [
    "route",
    "gate_status",
    "draft",
    "section_outline",
    "notation_used",
    "claim_evidence_map",
    "reviewer_defense_notes",
    "missing_inputs"
  ],
  "properties": {
    "route": {"type": "string"},
    "gate_status": {"type": "string", "enum": ["passed"]},
    "draft": {"type": "string"},
    "section_outline": {"type": "array", "items": {"type": "string"}},
    "notation_used": {"type": "array", "items": {"type": "string"}},
    "claim_evidence_map": {
      "type": "array",
      "items": {
        "type": "object",
        "required": ["claim", "evidence", "status"],
        "properties": {
          "claim": {"type": "string"},
          "evidence": {"type": "string"},
          "status": {"type": "string", "enum": ["supported", "bounded", "needs_evidence"]}
        }
      }
    },
    "reviewer_defense_notes": {"type": "array", "items": {"type": "string"}},
    "missing_inputs": {"type": "array", "items": {"type": "string"}}
  }
}
```

## Reference Use

Use IEEE references only when they answer a concrete drafting problem:

- Section structure or reviewer defense: `references/article-architecture.md`
- Abstract drafting: `references/abstract.md`
- Introduction drafting: `references/introduction.md`
- Method equations and algorithm mapping: `references/method.md`
- Experiment defense and ablation planning: `references/experiments.md`
- Paragraph-level flow repair: `references/paragraph-flow.md`
- Final rejection-risk audit: `references/paper-review.md`

When a legacy reference conflicts with the shared IEEE guidelines, follow the shared IEEE guidelines.
