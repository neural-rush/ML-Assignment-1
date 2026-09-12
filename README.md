# ML Assignment 1 — CS26S510

**Course:** ML_CS519L_CS303L
**Due:** 13 Sept 2026, 11:59 PM

Solutions to Assignment 1: parameter estimation for linear models, regularization
(Ridge/Lasso), and one-vs-rest logistic regression on IRIS.

## Structure

```
ml_a1_CS26S510/
├── derivations/
│   └── partAB_derivation_normaleq_ridge_lasso_CS26S510.md
├── notebooks/
│   ├── partC1_regression_normaleq_gd_illconditioning_CS26S510.ipynb
│   ├── partC2_polyfit_ridge_lasso_CS26S510.ipynb
│   └── partC3_logreg_ovr_iris_CS26S510.ipynb
├── figures/
│   ├── c1_regression_diagnostics/
│   ├── c2_polynomial_regularization/
│   └── c3_logistic_iris/
├── data/
│   ├── raw/          # untouched downloads (e.g. IRIS csv)
│   └── processed/    # anything cleaned/split myself
├── requirements.txt
├── .gitignore
└── README.md
```

Every notebook and derivation file is suffixed with my roll number (`CS26S510`) so the
repo is unambiguously mine — filenames also encode the part + topic keywords
(e.g. `partC1_regression_normaleq_gd_illconditioning`) so contents are clear without
opening the file.

## Setup

```bash
python -m venv venv
source venv/bin/activate        # Windows: venv\Scripts\activate
pip install -r requirements.txt
```

Open notebooks in VS Code / Jupyter Lab and select the `venv` interpreter as the kernel.

## Status

| Part | Topic | Status |
|------|-------|--------|
| A1(a) | Normal equation derivation + 2nd-order check | ⬜ |
| A1(b) | Hand computation, n=4 | ⬜ |
| A1(c) | MLE ⟺ least squares | ⬜ |
| B1 | Perturbation sensitivity of OLS | ⬜ |
| B2 | Ridge/Lasso derivations | ⬜ |
| C1(a) | Normal equation from scratch | ⬜ |
| C1(b) | Condition number + perturbation | ⬜ |
| C1(c) | Gradient descent, 3 learning rates | ⬜ |
| C1(d) | Ridge normal equation + sensitivity | ⬜ |
| C2(a) | Polynomial fits p ∈ {1,3,9,15} | ⬜ |
| C2(b) | Ridge vs Lasso across λ | ⬜ |
| C2(c) | Coefficient sparsity comparison | ⬜ |
| C3(a) | Logistic regression from scratch | ⬜ |
| C3(b) | PyTorch logistic regression | ⬜ |

## Generating the final submission PDF

```bash
jupyter nbconvert --to pdf ml_a1_CS26S510_solutions.ipynb
```

Requires a LaTeX distribution (e.g. TeX Live) installed locally.

## Notes

- Random seeds are fixed as given in the assignment — not changed.
- From-scratch parts (C1, polynomial fitting in C2a) use only `numpy`/`matplotlib`;
  `scikit-learn` is used only where the assignment explicitly calls for it
  (Ridge/Lasso in C2b/C2c).
