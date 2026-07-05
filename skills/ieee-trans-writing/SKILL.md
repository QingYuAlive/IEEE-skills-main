---
name: ieee-trans-writing
description: >-
  Draft, restructure, or plan IEEE Transactions manuscript sections for TCYB, THMS, and TNNLS from author claims, methods, equations, figures, results, Chinese notes, or rough drafts. Use for abstract, introduction, related work, method, experiments, results, discussion, conclusion, title, full manuscript argument, equation-first method writing, and Chinese requests such as IEEE论文写作, 写摘要, 写引言, 写方法, 写实验分析, 写discussion, or 搭论文框架.
---

# IEEE Transactions Writing

Use this skill to draft or rebuild IEEE Transactions-style manuscript content.

## Mandatory First Read

Read `../_shared/ieee-trans-guidelines.md` before drafting. It controls the equation-first order, notation discipline, experiment defense, visualization interpretation, and claim boundaries.

## Request Routing

Detect these axes and state them in one short line before drafting:

- `section`: abstract, introduction, related-work, method, experiments/results, discussion, conclusion, title, full-outline.
- `paper_type`: signal-learning, domain-generalization, contrastive-learning, multimodal/generative, general algorithmic.
- `source_language`: English, Chinese, mixed Chinese-English.
- `maturity`: idea, method, results, existing draft.

Load references as needed:

- Method or algorithm writing: `references/equation-first-methods.md`.
- Experiments/results/discussion: `references/bulletproof-results.md`.
- Section structure or full outline: `references/section-patterns.md`.

Do not load all references by default if the request is narrow.

## Drafting Workflow

1. Extract the one-sentence thesis.
2. Build the claim inventory: what the user wants to prove and what evidence is available.
3. Build the minimum formal skeleton: symbols, modules, losses, training/inference, or experiment matrix.
4. Identify unsupported claims and either remove them or mark them under `Assumptions or missing inputs`.
5. Draft the requested section in IEEE style.
6. Add a short `Claim boundary` note when the draft includes inferred or conditional wording.

## IEEE Style Priorities

- Prefer precise technical verbs: formulate, derive, optimize, constrain, align, regularize, perturb, reconstruct, evaluate.
- Use numbered contributions only when each contribution maps to a method object and evidence.
- Write method paragraphs around equations, not around implementation chronology.
- Write experiment paragraphs around claims, not around tables in order.
- Keep limitations specific and technical.
- Preserve the user's actual result direction, including mixed or negative observations.

## Section-Specific Rules

- **Abstract**: Problem, gap, method, evidence, implication. No citations. No unverified superlatives.
- **Introduction**: Application pressure -> technical limitation -> mechanism -> contributions -> evidence.
- **Related work**: Cluster by technical bottleneck; end each cluster with the unresolved issue your method targets.
- **Method**: Formal problem first, then architecture, losses, algorithm, inference, and complexity.
- **Experiments**: Protocol before numbers; baselines and ablations before visualization interpretation.
- **Discussion**: Explain mechanism and failure modes; do not repeat the main table.

## Output Contract

For substantial requests, return:

```text
Detected route:
Thesis:
Formal / evidence skeleton:
Draft:
Assumptions or missing inputs:
Claim boundary:
```

For small rewrite requests, provide the revised text first, then a compact note on any claim or evidence issue.

## Red Lines

- Do not invent equations, results, baselines, datasets, or citations.
- Do not replace precise but modest claims with grander language.
- Do not write "the proposed method effectively solves" unless the evidence supports that breadth.
- Do not bury missing protocol details such as seeds, folds, target domains, or checkpoint selection.
- Do not use t-SNE, PCA, or confusion matrices as standalone proof.
- Do not write a method as "first we use module A, then module B" without defining the computational object and objective.
