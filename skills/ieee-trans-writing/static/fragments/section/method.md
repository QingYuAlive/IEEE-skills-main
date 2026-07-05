# Section: Method

## Equation-First Mapping Engine

Organize the Method section by mathematical operators, not by a narrative walkthrough of software modules. Plain text may explain the intuition behind operators, but it must not replace equations, objectives, or algorithm steps.

## Required Subsection Order

| Subsection | Mathematical contract | Reviewer question answered |
|---|---|---|
| Problem Setting And Notation | Define `\mathcal{X}`, `\mathcal{Y}`, domains, samples, labels, representations, losses, weights, and protocol variables. | What is being optimized and under which training-test split? |
| Input Space Processing | Define windowing, normalization, augmentation, view construction, frequency transform, or modality mapping as operators. | How does raw data become a mathematical input object? |
| Latent Space Projection | Define encoder, projector, classifier, reference encoder, discriminator, generator, or fusion mapping with tensor shapes. | What representation is learned and what module remains at inference? |
| Optimization Constraints | Define empirical risk, contrastive loss, invariant penalty, GroupDRO objective, IRM penalty, reconstruction loss, or uncertainty weighting. | Which loss term enforces each claimed property? |
| Training And Inference Algorithm | State stages, update order, frozen modules, checkpoint selection, inference path, and discarded training-only components. | How can the method be implemented and reproduced? |
| Complexity And Deployment Cost | Report asymptotic complexity or measured parameters, FLOPs, memory, latency, and throughput. | Is the added mechanism justified by cost? |

## Equation Patterns

Use these patterns when applicable. Adapt symbols only if the Notation Ledger already defines them.

### Empirical Risk

```text
R_e(theta, phi) = (1 / n_e) sum_{i=1}^{n_e} CE(C_phi(G_theta(x_i^e)), y_i^e)
```

### IRM-Style Penalty

```text
L_IRM = sum_{e in S} || grad_{w | w = 1} R_e(w * C_phi(G_theta(x))) ||_2^2
```

### GroupDRO Objective

```text
min_{theta, phi} max_{q in Delta_m} sum_{e=1}^{m} q_e R_e(theta, phi)
```

### Supervised Contrastive Alignment

```text
P(i) = {p: y_p = y_i, d_p != d_i}
L_con = - sum_i (1 / |P(i)|) sum_{p in P(i)}
        log exp(sim(z_i, z_p) / tau) /
        sum_{a != i} exp(sim(z_i, z_a) / tau)
```

### Total Objective

```text
L_total = L_cls + lambda_con L_con + lambda_inv L_inv + lambda_reg L_reg
```

After each equation, add one sentence that maps the term to its claimed role and one sentence that names the ablation required to test the role.

## Architecture Writing Rule

Invalid style:

```text
The signal passes through three convolutional layers followed by normalization and a classifier.
```

Valid style:

```text
The encoder maps each window `X_i in R^{C x T}` to `h_i = G_theta(X_i) in R^d`; the projector produces `z_i = P_psi(h_i)` for alignment loss, while the classifier computes `p_i = softmax(W h_i + b)` for task risk. The projector is discarded during inference, so the test-time path is `C_phi(G_theta(X_i))`.
```

## Algorithm Complexity Example

When the method adds contrastive pairs, report the governing cost:

```text
For batch size B and embedding dimension d, the pairwise similarity matrix requires O(B^2 d) operations and O(B^2) memory before masking. If positives are capped at K per anchor, positive aggregation is O(B K d) after similarity construction.
```

Tie this cost to measured memory, throughput, or training-time overhead when the user provides numbers.

## Input JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["notation", "input_operators", "latent_mappings", "losses", "training_algorithm", "inference_path", "complexity"],
  "properties": {
    "notation": {"type": "array", "items": {"type": "object"}},
    "input_operators": {"type": "array", "items": {"type": "string"}},
    "latent_mappings": {"type": "array", "items": {"type": "string"}},
    "losses": {
      "type": "array",
      "items": {
        "type": "object",
        "required": ["name", "equation", "role", "ablation"],
        "properties": {
          "name": {"type": "string"},
          "equation": {"type": "string"},
          "role": {"type": "string"},
          "ablation": {"type": "string"}
        }
      }
    },
    "training_algorithm": {"type": "array", "items": {"type": "string"}},
    "inference_path": {"type": "string"},
    "complexity": {"type": "array", "items": {"type": "string"}}
  }
}
```

## Output JSON Schema

```json
{
  "$schema": "https://json-schema.org/draft/2020-12/schema",
  "type": "object",
  "required": ["method_section", "subsection_map", "equation_role_map", "algorithm_steps", "complexity_notes", "missing_formal_objects"],
  "properties": {
    "method_section": {"type": "string"},
    "subsection_map": {"type": "array", "items": {"type": "object"}},
    "equation_role_map": {"type": "array", "items": {"type": "object"}},
    "algorithm_steps": {"type": "array", "items": {"type": "string"}},
    "complexity_notes": {"type": "array", "items": {"type": "string"}},
    "missing_formal_objects": {"type": "array", "items": {"type": "string"}}
  }
}
```

## Quality Gate

- Every module has a mathematical mapping and a stated inference role.
- Every loss term has a coefficient, role, and ablation.
- Positive-pair construction is defined before contrastive loss.
- Domain sets are defined before domain-generalization claims.
- Stage-wise methods are written as separate optimization problems.
- Complexity is reported for any added alignment, adversarial, generative, or reference-guided mechanism.
