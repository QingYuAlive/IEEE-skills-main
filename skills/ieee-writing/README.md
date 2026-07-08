# ieee-writing

`ieee-writing` drafts and audits mathematically grounded manuscript sections for IEEE Transactions venues such as TCYB, THMS, and TNNLS.

## Scope

Use this skill for:

- abstract drafting with problem, limitation, mechanism, and evidence blocks
- introduction drafting with formal task, OOD failure, technical mechanism, and categorized contributions
- equation-first method sections
- experiments and results sections with protocol, baseline, ablation, visualization, and complexity defense
- claim-evidence audits for robustness, generalization, invariance, convergence, and deployment claims
- Chinese or mixed Chinese-English author notes that must become rigorous IEEE-style English prose

## Core Rule

The skill does not draft full prose until the user supplies a passed mathematical intake package: Notation Ledger, formal task, objective, OOD protocol, mechanism map, and evidence ledger.

## Active Structure

```text
ieee-writing/
  SKILL.md
  manifest.yaml
  agents/
    openai.yaml
  static/
    core/
      stance.md
      workflow.md
      output-format.md
    fragments/
      section/
      journal/
      language/
      paper_type/
  references/
    abstract.md
    article-architecture.md
    chinese-author-workflow.md
    conclusion.md
    experiments.md
    introduction.md
    method.md
    paper-review.md
    paragraph-flow.md
    related-work.md
```

## Review Standard

Every major claim must map to at least one of:

- a defined symbol or assumption
- an equation or algorithm step
- an OOD protocol
- a baseline comparison
- an ablation or sensitivity study
- a theorem condition, convergence statement, or bound
- a complexity, latency, memory, or throughput measurement
- a specific limitation
