# IEEE Reviewer Workflow

## Execution Order

1. Identify the input package:
   - full manuscript;
   - selected section;
   - abstract only;
   - method and experiment notes;
   - result tables or figure captions.
2. Build the manuscript fact base:
   - task;
   - claimed contribution;
   - formal notation;
   - equations and objectives;
   - assumptions, theorem claims, and complexity claims;
   - datasets, splits, baselines, metrics, ablations, and limitations.
3. Mark assessment boundaries:
   - what is visible;
   - what is missing;
   - what is not assessable from the provided material.
4. Apply `review-axes.md`.
5. Apply `domain-specific-review-gates.md` where relevant.
6. Classify issues by severity:
   - fatal flaw;
   - major concern;
   - minor concern.
7. Write the report using `report-structure.md`.
8. Run `qa-checklist.md`.

## Fact-Base Extraction Checklist

Extract:

- formal task and target venue;
- source domains and target domains;
- input/output spaces and predictor;
- network mappings and tensor shapes;
- loss terms, coefficients, and total objective;
- training stages and inference path;
- theorem, bound, convergence, or complexity claims;
- datasets and split policy;
- baselines and recency;
- ablations and sensitivity analyses;
- claim words requiring calibration;
- limitations stated by the authors.

## Severity Rules

Classify as `fatal flaw` when the issue invalidates the central claim:

- missing formal objective for a proposed method;
- invalid OOD protocol for a DG claim;
- target leakage;
- no ablation for the central proposed mechanism;
- theory claim without theorem, proof, or assumptions;
- results based only on weak or irrelevant baselines.

Classify as `major concern` when the claim may be salvageable but requires substantial new work:

- missing sensitivity analysis;
- incomplete baseline family;
- unclear checkpoint rule;
- missing complexity for a deployment claim;
- weak but not invalid representation analysis.

Classify as `minor concern` only when the issue is local:

- notation inconsistency;
- unclear acronym;
- missing citation for background;
- table caption ambiguity;
- grammar that affects technical clarity.

## Failure-Safe Behavior

If evidence is absent, state that the claim is not established from the supplied material. Do not fill the gap with assumptions.

If the input is very thin, produce a bounded risk audit rather than a full review.
