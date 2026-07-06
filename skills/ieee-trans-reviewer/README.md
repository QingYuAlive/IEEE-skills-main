# ieee-trans-reviewer

`ieee-trans-reviewer` performs harsh pre-submission red-team reviews for IEEE Transactions manuscripts, especially TCYB, THMS, and TNNLS papers involving neural networks, time-series learning, sEMG/EEG, contrastive learning, domain generalization, invariant learning, and robust empirical evaluation.

## Purpose

The skill is designed to find rejection-level flaws before submission:

- missing mathematical formulation;
- undefined variables and inconsistent notation;
- equations that do not match the architecture;
- absent theoretical bounds or convergence analysis;
- weak or outdated baselines;
- missing ablations and sensitivity tests;
- invalid OOD or LODO protocols;
- overclaimed robustness, invariance, or generalization;
- missing complexity or deployment evidence.

## Output

The default report is a single integrated IEEE red-team review:

```text
Review Verdict
Fatal Flaws / Major Concerns
Minor Concerns
Claim-Calibration Audit
Actionable Directives
Submission Readiness Gate
```

The report does not praise writing style, prose polish, accessibility, or venue fit. It prioritizes theoretical loopholes, empirical defense gaps, and required author actions.

## Reference Files

```text
ieee-trans-reviewer/
  SKILL.md
  README.md
  references/
    reviewer-workflow.md
    review-axes.md
    domain-specific-review-gates.md
    report-structure.md
    qa-checklist.md
    role-boundaries.md
    source-basis.md
    editorial criteria and processes.md
```
