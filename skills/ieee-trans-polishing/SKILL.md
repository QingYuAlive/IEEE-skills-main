---
name: ieee-trans-polishing
description: >-
  Polish, translate, tighten, or structurally repair IEEE Transactions manuscript prose for TCYB, THMS, and TNNLS while preserving evidence boundaries. Use for English polishing, Chinese-to-English academic rewriting, abstract/introduction/method/results/discussion refinement, claim calibration, AI-like prose reduction, and Chinese requests such as IEEE论文润色, 英文论文润色, 学术英语, 降低AI味, 改写discussion, 结果分析润色, or 中译英论文.
---

# IEEE Transactions Polishing

Use this skill to polish IEEE-style manuscript prose without weakening technical precision or exaggerating claims.

## Mandatory First Read

Read `../_shared/ieee-trans-guidelines.md` before polishing. It defines the evidence boundary, equation-first expectations, experiment defense rules, and forbidden claim upgrades.

## Polishing Stance

- Preserve the user's scientific meaning, result direction, and uncertainty.
- Improve structure before sentence fluency when the paragraph is logically weak.
- Do not turn a conditional observation into a universal conclusion.
- Do not add citations, numbers, datasets, baselines, or equations unless the user supplied them.
- Keep IEEE tone: precise, compact, technical, and evidence-bound.

## Route Detection

State the route in one line:

- `language polish`: grammar, concision, register.
- `zh-to-en`: Chinese or mixed notes into IEEE English.
- `claim calibration`: overclaiming, unsupported novelty, weak hedging.
- `structural repair`: paragraph order or method/result logic.
- `result tightening`: tables, ablations, t-SNE/PCA/confusion/sensitivity.

Load references:

- `references/claim-calibration.md` for claim strength, verbs, hedging, and overclaim repair.
- `references/structural-repair.md` for paragraph order, Chinese-to-English logic, and method/result flow.
- `references/result-analysis-tightening.md` for evidence analysis, ablation, visualization, and discussion.

## Workflow

1. Identify section type and claim level.
2. Extract claims and evidence from the input.
3. Diagnose the main failure mode: vague claim, missing subject, unsupported comparison, layer-by-layer method prose, table narration, or overclaim.
4. Rewrite the text.
5. Provide a compact edit note explaining technical changes and any remaining risk.

## Output Contract

Default:

```text
Polished Version
[revised text]

Technical Edits
- [claim/structure/wording change]

Remaining Risks
- [only if relevant]
```

If the text is severely under-specified, output:

```text
Repair Needed Before Polishing
- Missing evidence:
- Ambiguous claim:
- Suggested minimal rewrite:
```

## IEEE Language Rules

- Prefer "is designed to", "encourages", "penalizes", "aligns", "reduces", "improves under", "suggests" over broad certainty.
- Use "outperforms" only with named baselines, metric, and protocol.
- Use "significant" only for statistical significance or clearly defined practical significance.
- Avoid empty intensifiers: very, highly, greatly, remarkable, revolutionary, excellent.
- Avoid vague nouns: performance, robustness, effectiveness, superiority, feasibility without metric context.
- Avoid layer listing when a formal mapping would be clearer.

## Red Lines

- Do not add stronger novelty than the draft supports.
- Do not erase limitations because they sound negative.
- Do not hide conflicting ablation results.
- Do not imply unseen-domain generalization from random train/test splits.
- Do not treat smoother English as stronger science.
