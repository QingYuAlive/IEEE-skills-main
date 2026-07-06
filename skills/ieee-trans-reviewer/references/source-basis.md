# IEEE Review Source Basis

## Authoritative Local Source

The primary local source is `../_shared/ieee-trans-guidelines.md`. This reviewer skill applies those guidelines as adversarial review criteria.

## Derived Review Standards

The manuscript must satisfy these standards when making technical claims:

- formal problem setting before architecture;
- notation table with all symbols defined;
- representation pipeline expressed as mappings;
- core constraint written as a loss, penalty, bound, or algorithm;
- total objective with coefficients and tuning policy;
- optimization and inference paths described;
- OOD or DG protocols defined before robustness or generalization claims;
- baselines broad, recent, fair, and protocol-matched;
- ablations aligned to every proposed component;
- visualization paired with quantitative evidence;
- complexity, memory, latency, or throughput reported when relevant.

## Local Implementation Choices

- The default output is one integrated red-team report, not multiple simulated reviewers.
- The report is organized around fatal flaws, major concerns, minor concerns, claim calibration, and actionable directives.
- The skill uses `not assessable from provided material` instead of inventing missing manuscript content.
- The review emphasizes TCYB, THMS, and TNNLS expectations for mathematical rigor, empirical defense, and claim calibration.

## Limits

- The skill cannot verify unpublished baselines, hidden supplementary experiments, or code not supplied by the user.
- The skill cannot assert a final editorial decision.
- The skill cannot determine recency of baselines without a supplied citation list or browsing request; it can still flag that baseline recency is not demonstrated.
