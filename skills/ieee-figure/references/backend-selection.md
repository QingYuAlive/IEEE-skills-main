# Backend Selection

The active backend is fixed: generate Python code using Matplotlib and Seaborn.

Do not ask the user to choose a backend. Do not generate non-Python plotting code in this skill. If the user requests another plotting environment, state that `ieee-figure` is Python-only and offer to provide a Python equivalent.

Required Python stack:

- `matplotlib`
- `seaborn`
- `numpy`
- `pandas`
- `scipy` for statistical tests when needed
- `scikit-learn` for PCA, t-SNE, and embedding diagnostics

All generated scripts must be runnable from a terminal and must not rely on notebook state.
