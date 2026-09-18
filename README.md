# Robust Linear Regression Under Outliers

[[Towards Data Science](https://shields.io)](https://towardsdatascience.com)
[[License: MIT](https://shields.io)](https://opensource.org)

Reproducible code and experiments accompanying the **Towards Data Science** article: 
📖 [**“How to Make Linear Regression Survive Outliers: Comparing Classical and Modern Robust Estimators Through Theory, Code, and Experiments”**](https://towardsdatascience.com).

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

---

## Repository contents

- `robust_linear_regression_outliers.ipynb` — complete reproducible notebook
- `figures/` — the nine retained article figures
- `requirements.txt` — Python dependencies
- `.gitignore` — standard Python/Jupyter exclusions

Running the notebook also exports numerical CSV files, article tables,
and a figure manifest into `figures/`.

---

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

---

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

---

## Disclosure

### Methodology & Attribution
**Aamir Hussain Chughtai, PhD** was the primary designer of **ASOR**, originally introduced in the study *“Bayesian Heuristics for Robust Spatial Perception”* (**IEEE Transactions on Instrumentation and Measurement**, 2024). 

To ensure a transparent comparison, all estimators in this benchmark suite are evaluated on the identical **Monte Carlo realizations** using the fixed and documented algorithmic schedules detailed in the article.

#### **BibTeX**
```bibtex
@article{chughtai2024asor,
  author={Chughtai, Aamir Hussain and Tahir, Muhammad and Uppal, Mubeen},
  journal={IEEE Transactions on Instrumentation and Measurement}, 
  title={Bayesian Heuristics for Robust Spatial Perception}, 
  year={2024},
  volume={73},
  pages={1--12}
}
```

#### **APA 7th Edition**
```text
Chughtai, A. H., Tahir, M., & Uppal, M. (2024). Bayesian Heuristics for Robust Spatial Perception. IEEE Transactions on Instrumentation and Measurement, 73, 1-12.
```

---

## License

The source code, notebook, and generated figures in this repository are
released under the MIT License.

Copyright © 2026 Aamir Hussain Chughtai. See the `LICENSE` file for details.
