# applied_statistics_2025
Repository for the 2025 Semester 2 module in Applied Statistics - HDIP in Computer Science: Data Analytics

By Emmet Devaney (G00438866@atu.ie)

---

# Introduction

This repository contains a single Jupyter notebook that solves **Problems 1–4** using a mix of **exact probability**, **simulation**, and **classical statistical tests**. 

---

## Required Imports

The notebook uses:

- `numpy`
- `scipy`
- `matplotlib`
- `pandas`


---

## Main file

- **`problems.ipynb`**  
  The complete assessment notebook (Problems 1–4) with:
  - clear structure per problem
  - code + outputs + plots
  - references section at the end of the notebook

---

## Content

### Problem 1 — Extending the Lady Tasting Tea
- Computes an exact probability using combinations.
- Validates the exact result using a Monte Carlo simulation.
- Visualises the distribution of outcomes (histogram).

### Problem 2 — Normal distribution
- Simulates samples from Normal(0,1).
- Compares standard deviation estimates for small vs large sample sizes.
- Uses and explains `ddof=0` vs `ddof=1`.
- Visualises distributions using histograms.

### Problem 3 — t-tests
- Simulates two independent groups:
  - Group A ~ Normal(0,1)
  - Group B ~ Normal(d,1)
- Runs repeated two-sample t-tests for effect sizes \(d\).
- Estimates:
  - **Type II error (β)** as fail-to-reject frequency
  - **Power (1−β)** as reject frequency
- Plots β and power curves.

### Problem 4 — ANOVA
- Generates 3 groups with different means.
- Runs:
  - one-way ANOVA (global test of mean equality)
  - pairwise independent t-tests
- Explains why ANOVA is preferred before multiple pairwise tests.
- Includes references for ANOVA and the t-test.

---

## References (Problems 1–4)

### Problem 1 — Lady Tasting Tea extension (exact probability + simulation)
- Fisher, R. A. (1935). *The Design of Experiments*.
  https://tankona.free.fr/fisher1935.pdf  
  - Primary source for the original “Lady Tasting Tea” experiment and using exact probability under a null hypothesis.

- Python Documentation — `math.comb` (combinations / binomial coefficients).
  https://docs.python.org/3/library/math.html#math.comb  
  - Used to compute exact probabilities via combinations \(\binom{n}{k}\).

- NumPy Documentation — Random number generation (`default_rng`).
  https://numpy.org/doc/stable/reference/random/generator.html  
  - Used for Monte Carlo simulation with the recommended modern RNG interface.

- Matplotlib Documentation — `pyplot.hist` (histograms).
  https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.hist.html  
  - Used to visualise simulation outcomes (distribution of correct guesses).

---

### Problem 2 — Normal distribution, SD, and `ddof`
- NumPy Documentation — `numpy.std` and `ddof`.
  https://numpy.org/doc/stable/reference/generated/numpy.std.html  
  - Directly supports `ddof=0` vs `ddof=1`.

- NIST/SEMATECH e-Handbook — Normal Distribution (overview).
  https://www.itl.nist.gov/div898/handbook/eda/section3/eda3661.htm  
  - Conceptual reference for the Normal distribution and interpreting mean/SD estimates.

- Matplotlib Documentation — `pyplot.hist` (histograms).
  https://matplotlib.org/stable/api/_as_gen/matplotlib.pyplot.hist.html  
  - Used to plot the sampling distribution of SD estimates.

---

### Problem 3 — Two-sample t-test, Type II error, and power
- SciPy Documentation — `scipy.stats.ttest_ind` (two-sample t-test).
  https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.ttest_ind.html  
  - Exact function used to perform the hypothesis tests in the simulation.

- NIST/SEMATECH e-Handbook — Comparing two means / t-tests.
  https://www.itl.nist.gov/div898/handbook/prc/section2/prc22.htm  
  - Explains the purpose, assumptions, and interpretation of the two-sample t-test.

- NIST/SEMATECH e-Handbook — Type I error, Type II error, and power.
  https://www.itl.nist.gov/div898/handbook/prc/section2/prc23.htm  
  - Supports definitions and interpretation of Type II error (β) and power (1−β).

---

### Problem 4 — One-way ANOVA and multiple comparisons
- SciPy Documentation — `scipy.stats.f_oneway` (one-way ANOVA).
  https://docs.scipy.org/doc/scipy/reference/generated/scipy.stats.f_oneway.html  
  - Core function used for the one-way ANOVA global test across 3 groups.

- NIST/SEMATECH e-Handbook — One-way ANOVA (overview).
  https://www.itl.nist.gov/div898/handbook/prc/section4/prc431.htm  
  - Explains ANOVA logic (between-group vs within-group variation) and interpretation of the F-test.

- NIST/SEMATECH e-Handbook — Multiple comparisons / Bonferroni method.
  https://www.itl.nist.gov/div898/handbook/prc/section4/prc473.htm  
  - Supports the explanation of why multiple pairwise tests inflate false positives and how corrections control family-wise error.


