# ieee-polishing

`ieee-polishing` polishes and audits academic prose for IEEE Transactions manuscripts, especially TCYB, THMS, and TNNLS papers in neural networks, machine learning, human-machine systems, bio-signal learning, time-series classification, contrastive learning, and domain generalization.

## Core Purpose

The skill improves language only when the edit strengthens:

- mathematical clarity;
- notation and terminology consistency;
- protocol-bound empirical claims;
- ablation and mechanism defense;
- reviewer-facing risk control.

It does not make underformalized or unsupported claims sound polished. If a sentence needs an equation, objective, OOD protocol, ablation, or complexity metric, the skill flags the missing formal object before polishing.

## Active Files

```text
ieee-polishing/
  SKILL.md
  manifest.yaml
  references/
    phrasebank-playbook.md
    style-guardrails.md
    published-article-patterns.md
    section-moves.md
    writing-strategy.md
    latex-layout.md
  static/
    core/
      stance.md
      failure-modes.md
      output-format.md
    fragments/
      journal/
      language/
      paper_type/
      section/
```

## Polishing Standard

Every major edit should answer one reviewer-facing question:

- Is the symbol defined?
- Is the domain, split, or protocol explicit?
- Is the claim supported by the stated evidence?
- Is the verb calibrated to the evidence strength?
- Is the ablation or limitation visible?
- Is the equation or algorithm integrated into prose correctly?

## Typical Use

- Polish an abstract while binding each claim to a metric and protocol.
- Repair a method paragraph that describes architecture without equations.
- Convert Chinese technical notes into IEEE-style English while preserving notation.
- Tighten result paragraphs so ablation, OOD protocol, and limitation are explicit.
- Reduce rejection risk by downgrading unsupported robustness, invariance, or generalization claims.
- Fix IEEE LaTeX layout and notation presentation when the user asks for typesetting support.
