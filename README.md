# Robust Linear Regression Under Outliers

Reproducible code and experiments accompanying the Towards Data Science
article **“How to Make Linear Regression Survive Outliers.”**

The notebook compares:

- Ordinary Least Squares (OLS)
- Huber regression
- RANSAC
- GNC-GM
- GNC-TLS
- Adaptive Selective Outlier Rejecting (ASOR)

It evaluates zero-mean Gaussian, biased Gaussian, biased uniform, and
coherent competing-line contamination, together with sample-size,
noise-scale, accuracy, and runtime experiments.

## Repository contents

- `robust_linear_regression_outliers.ipynb` — complete reproducible notebook
- `figures/` — the nine retained article figures
- `requirements.txt` — Python dependencies
- `.gitignore` — standard Python/Jupyter exclusions

Running the notebook also exports numerical CSV files, article tables,
and a figure manifest into `figures/`.

## Quick start

Python 3.10 or newer is recommended.

```bash
python -m venv .venv
```

On Windows PowerShell:

```powershell
.\.venv\Scripts\Activate.ps1
```

On macOS or Linux:

```bash
source .venv/bin/activate
```

Install the dependencies and start Jupyter:

```bash
python -m pip install --upgrade pip
python -m pip install -r requirements.txt
jupyter lab
```

Open `robust_linear_regression_outliers.ipynb`, then use **Restart Kernel
and Run All Cells**.

## Reproducibility notes

- Monte Carlo datasets use deterministic seeds.
- Every estimator receives the same dataset within each realization.
- Prediction-error results are deterministic under the supplied settings.
- Runtime values depend on hardware, power mode, operating-system
  scheduling, Python packages, and the BLAS implementation.
- The reported benchmark system was an HP ProBook 455 G10 with an AMD
  Ryzen 7 7730U processor, 32 GB RAM, and Microsoft Windows 11 Pro.
- The introductory alternative line uses slope 9; the structured
  quantitative benchmark uses slope 15.
- The GNC chi-square coverage probability of 0.99 is a benchmark
  calibration choice rather than a prescribed value from the original
  GNC formulation.

## Generated outputs

The notebook generates these retained figures:

1. clean observations;
2. introductory contaminated observations;
3. zero-mean Gaussian prediction error;
4. biased Gaussian prediction error;
5. biased uniform prediction error;
6. coherent competing-line prediction error;
7. biased Gaussian runtime;
8. sample-size prediction-error scaling;
9. sample-size runtime scaling.

## Disclosure

Aamir Hussain Chughtai, PhD was the primary designer of ASOR in the original
study cited in the accompanying article. All estimators are evaluated on
the same Monte Carlo realizations using fixed and documented settings.

## License

## License

The source code, notebook, and generated figures in this repository are
released under the MIT License.

Copyright © 2026 Aamir Hussain Chughtai. See the `LICENSE` file for details.
