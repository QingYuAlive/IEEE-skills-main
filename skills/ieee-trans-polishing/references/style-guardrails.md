# IEEE Transactions Style Guardrails

Use this file for mechanical, stylistic, notation, and claim-defense checks after the main technical diagnosis. These rules refine prose without weakening mathematical precision.

## Absolute Style Ban

Remove subjective, hyped, story-like, or editorial adjectives and adverbs unless they are part of a quoted title:

| Banned wording | IEEE replacement strategy |
|---|---|
| `amazing`, `remarkable`, `excellent` | Replace with a measured result, metric, or leave unstated. |
| `huge`, `massive`, `dramatic` | Use `large` only with a number, confidence interval, or baseline delta. |
| `unprecedented`, `groundbreaking`, `revolutionary` | Use a bounded novelty statement tied to the compared literature. |
| `interestingly`, `surprisingly`, `notably`, `importantly` | Use only when the sentence identifies a concrete technical contrast; otherwise delete. |
| `powerful`, `promising`, `effective` | Specify the protocol, metric, and baseline. |
| `robust`, `generalizable`, `invariant` | Use only with an explicit OOD protocol, invariant criterion, or target-domain evidence. |
| `significant` | Use only with a statistical test or clearly stated practical significance criterion. |

Do not replace banned words with softer hype. Replace them with evidence, protocol, or limitation.

## Terminology And Notation Consistency

The Notation Ledger governs the polish.

- If a domain is defined as `$\mathcal{E}$`, write `domain $\mathcal{E}$`, not `the dataset`, `the environment`, or `the condition`.
- If the unseen target is `$\mathcal{T}$`, keep `target domain $\mathcal{T}$` throughout.
- If the encoder is `$G_\theta$`, do not alternate with `feature extractor`, `backbone`, or `network` unless the ledger defines those as aliases.
- If a loss is `$\mathcal{L}_{\mathrm{con}}$`, do not switch to `contrastive objective`, `alignment loss`, and `regularizer` interchangeably without defining the relation.
- Distinguish dataset, domain, split, distribution, subject, session, trial, force level, and class. Do not collapse them into a generic `dataset`.
- Keep metric names stable: use either macro-F1, balanced accuracy, accuracy, AUC, RMSE, or another defined metric consistently.

## LaTeX Math Integration

Use math notation smoothly and consistently:

- Enclose inline variables, functions, spaces, sets, and losses in `$...$`, for example `$x_i$`, `$\mathcal{X}$`, `$G_\theta$`, `$\mathcal{L}_{\mathrm{cls}}$`.
- Use display equations for objectives, multi-term losses, optimization problems, theorem statements, and algorithms that cannot be read as inline text.
- Define every symbol before or immediately after first use.
- Do not introduce Greek coefficients without a role and tuning policy: write `$ \lambda_{\mathrm{con}} $ weights the contrastive term and is selected on the validation split`.
- Do not mix plain text and math for the same object. Use `source domain $\mathcal{E}_s$`, not `source domain Es`.
- Use roman subscripts for descriptive labels: `$\mathcal{L}_{\mathrm{cls}}$`, `$\lambda_{\mathrm{con}}$`, `$\tau_{\mathrm{temp}}$`.
- Keep punctuation outside display equations unless the manuscript style requires sentence punctuation inside equation lines.
- Avoid unexplained equation references. Write `the objective in (3)` only if equation numbering exists.

## Sentence-Level IEEE Register

- Prefer dense, objective, technical prose.
- Use active voice when it clarifies the actor: `We evaluate...`, `The ablation removes...`.
- Use passive voice when the procedure matters more than the actor: `The target domain was held out during training`.
- Keep one main technical proposition per sentence.
- Do not split a formal definition across too many short sentences; definitions often need controlled density.
- Do not simplify technical nouns for readability if the simplification breaks meaning.

## Claim-Strength Guardrails

| Claim wording | Required support |
|---|---|
| `outperforms` | Metric, baseline, split, and comparable protocol |
| `robust` | Perturbation or OOD protocol and metric |
| `generalizes` | Held-out target domain or leave-one-domain-out evaluation |
| `invariant` | Formal invariant criterion or loss plus representation evidence |
| `necessary` | Removal or replacement ablation |
| `efficient` | Parameters, FLOPs, memory, latency, throughput, or asymptotic complexity |
| `converges` | Theorem, proof sketch, or empirically measured convergence protocol |

When support is missing, change the sentence to a bounded observation or return a formalization flag.

## Examples

Weak:

```text
Our amazing network learns robust features from different datasets.
```

IEEE repair:

```text
Under the leave-one-force-level-out protocol, the encoder $G_\theta$ reduces target-domain error relative to the ERM baseline, supporting the role of $\mathcal{L}_{\mathrm{con}}$ in cross-force feature alignment.
```

Weak:

```text
The signal is passed through several CNN layers and then classified.
```

Formalization flag:

```json
{
  "status": "needs_formalization",
  "reason": "The sentence describes architecture qualitatively without the mapping, tensor shapes, or classifier equation.",
  "required_input": "Define $X_i \\in \\mathbb{R}^{C \\times T}$, $h_i = G_\\theta(X_i)$, and $p_i = C_\\phi(h_i)$ before polishing."
}
```
