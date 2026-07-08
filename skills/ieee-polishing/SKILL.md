---
name: ieee-polishing
description: Polish, restructure, audit, or translate academic prose for IEEE Transactions venues, especially TCYB, THMS, TNNLS, and adjacent machine-learning, neural-network, bio-signal, time-series, domain-generalization, and contrastive-learning papers. Use when the user asks for publication-quality English, technical copyediting, reviewer-risk reduction, LaTeX notation repair, claim calibration, mathematical clarity, ablation-defense wording, OOD/generalization wording, or Chinese-to-English academic polishing for IEEE-style manuscripts.
---

# IEEE Transactions Polishing Router

This skill edits language only when the edit improves mathematical clarity, logical defense, and reviewer-facing precision. Polishing must not make an underformalized, unsupported, or scientifically weak sentence merely sound fluent.

## Non-Negotiable Philosophy

Language optimization must serve mathematical clarity and logical defense.

For TCYB, THMS, and TNNLS, a polished sentence is successful only if it helps reviewers see:

1. the formal object being discussed;
2. the equation, algorithm, assumption, or protocol behind the claim;
3. the evidence strength and scope boundary;
4. the relation between terminology, notation, and empirical result.

## Required Reading Order

1. Read `../_shared/ieee-guidelines.md` before polishing.
2. Read `manifest.yaml`.
3. Read every path listed under `always_load`.
4. Detect the request axes and load only the selected fragments.
5. Load references on demand from the manifest, especially:
   - `references/style-guardrails.md` for terminology, notation, math, and style checks.
   - `references/phrasebank-playbook.md` for IEEE transition formulas and defense wording.

Do not apply polishing rules from memory. Use the loaded fragments.

## Formality Gate

Actively detect plain-English descriptions of neural networks, algorithms, losses, domains, or protocols. Flag them before polishing.

Refuse to simply beautify prose when the sentence has one of these defects:

- A neural module is described without a mapping, tensor shape, or equation.
- An algorithm is described as a sequence of vague operations without update rules or objectives.
- A loss or penalty is named without its mathematical role, coefficient, or ablation.
- Robustness, invariance, generalization, or OOD performance is claimed without a source-target protocol.
- A visualization is used as proof without quantitative support.
- A result is described as significant without a statistical test or explicit practical criterion.

When the gate fails, return this schema and stop short of polished prose:

```json
{
  "status": "blocked_by_formality_gate",
  "reason": "The sentence would become fluent but remain scientifically underformalized.",
  "required_author_action": [
    "Provide the formal notation, equation, objective, or protocol behind the claim.",
    "Define the relevant variables in LaTeX notation.",
    "State the evidence, ablation, or OOD split that supports the claim."
  ],
  "rewrite_allowed": false
}
```

If the user explicitly asks for a diagnostic-only pass, give a repair plan instead of polished prose.

## Routing Protocol

1. **Load active rules.** Read shared guidelines, manifest, and always-load fragments.
2. **Detect axes.**
   - `paper_type`: `algorithmic` by default for learning systems; otherwise infer from the draft.
   - `section`: abstract, intro, results, discussion, conclusion, title, or methods.
   - `language`: `zh-to-en` for Chinese or Chinese-influenced English; otherwise `en`.
   - `journal`: `tcyb`, `thms`, `tnnls`, or `generic-ieee`.
3. **State the route.** Report one concise line with detected axes and whether the formality gate passed.
4. **Diagnose before editing.** Identify whether the main issue is notation, objective, protocol, evidence, paragraph logic, or sentence-level wording.
5. **Polish with defense.** Provide revised text plus a reviewer-defense rationale for every major structural edit.

## Editing Priorities

Apply these priorities in order:

1. Fix terminology and notation consistency.
2. Convert vague mechanism prose into equation-aware prose.
3. Bind claims to protocols, metrics, ablations, or limitations.
4. Calibrate verbs to evidence strength.
5. Improve paragraph order and sentence clarity.
6. Perform grammar, article, tense, and punctuation cleanup.

Sentence-level elegance never outranks correctness.

## Required Output

Use `static/core/output-format.md`.

For substantive edits, return:

- polished text;
- before-and-after table or diff when useful;
- reviewer-defense rationale;
- formalization flags;
- notation and terminology changes;
- unresolved author inputs.

## Red Lines

- Do not add equations, numbers, citations, p-values, datasets, or theorem assumptions not supplied by the user.
- Do not replace precise notation with informal synonyms.
- Do not vary terms for style. If the ledger defines domain `\mathcal{E}`, keep using domain `\mathcal{E}`.
- Do not weaken mathematical prose into popular-science explanation.
- Do not upgrade results from `indicate` to `demonstrate` unless the evidence directly supports it.
- Do not call a method robust, invariant, generalizable, superior, or state of the art without the required protocol and comparison.
- Do not polish a sentence that should instead be replaced by a formal equation or algorithm statement.

## Input Schema For Polishing

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["text", "section", "target_journal", "notation_ledger", "evidence_context"],
  "properties": {
    "text": {"type": "string"},
    "section": {
      "type": "string",
      "enum": ["abstract", "intro", "results", "discussion", "conclusion", "title", "methods", "standalone"]
    },
    "target_journal": {
      "type": "string",
      "enum": ["TCYB", "THMS", "TNNLS", "generic-ieee"]
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
    "evidence_context": {
      "type": "object",
      "properties": {
        "protocol": {"type": "string"},
        "metrics": {"type": "array", "items": {"type": "string"}},
        "baselines": {"type": "array", "items": {"type": "string"}},
        "ablations": {"type": "array", "items": {"type": "string"}},
        "limitations": {"type": "array", "items": {"type": "string"}}
      }
    }
  }
}
```

## Output Schema For Successful Polishing

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": [
    "route",
    "polished_text",
    "before_after_edits",
    "reviewer_defense_rationale",
    "notation_and_terminology_changes",
    "formalization_flags",
    "unresolved_author_inputs"
  ],
  "properties": {
    "route": {"type": "string"},
    "polished_text": {"type": "string"},
    "before_after_edits": {"type": "array", "items": {"type": "object"}},
    "reviewer_defense_rationale": {"type": "array", "items": {"type": "object"}},
    "notation_and_terminology_changes": {"type": "array", "items": {"type": "string"}},
    "formalization_flags": {"type": "array", "items": {"type": "string"}},
    "unresolved_author_inputs": {"type": "array", "items": {"type": "string"}}
  }
}
```
