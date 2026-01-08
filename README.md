# Bias, Variance & Regularization — FAANG-Level Hands-On (Breast Cancer)

**Goal:** Build interview-grade intuition for under/overfitting, bias/variance tradeoffs, and regularization (L1/L2, early stopping), grounded in experiments.

**Outcome:** Students can:
- diagnose bias vs variance from learning curves,
- choose regularization knobs and justify them,
- explain L1 vs L2 and their effects on weights/features,
- reason about model capacity and data size.

---

# How to Start

1. **Fork** this repository.  
2. Open `biasvar_student_lab.ipynb` in **Google Colab**.  
3. Complete all **TODO** sections.  
4. **Restart runtime → Run All** cells.  
5. Push changes and submit a **Pull Request**.  

⚠️ **Do NOT edit notebooks directly on GitHub.**

---

## Lab Rules (FAANG Style)

- ✅ Always compare models by controlled capacity changes
- ✅ Don’t tune on the test set
- ✅ Explain *why* a knob affects bias/variance
- ✅ Prefer simple models unless complexity is justified

---

# Dataset

Primary: `sklearn.datasets.load_breast_cancer` (real dataset, no download).  
Fallback: none needed.

---

## Section 1 — Setup + Baseline

### Task 1.1: Logistic regression baseline

**Checkpoint Questions:**

- Why is logistic regression a “high bias / low variance” baseline?

---

## Section 2 — Capacity Sweep (Under/Overfitting)

### Task 2.1: Decision tree depth sweep

- Vary `max_depth` and plot train vs validation accuracy

**Checkpoint Questions:**

- What pattern indicates high variance?
- What pattern indicates high bias?

---

## Section 3 — Regularization (L2 vs L1)

### Task 3.1: Sweep C for LogisticRegression (L2)

### Task 3.2: Compare L1 vs L2 sparsity

**FAANG Gotcha:**

- L1 can zero out correlated features arbitrarily.

---

## Section 4 — Learning Curves (Data Size)

### Task 4.1: Learning curve by subsampling

**Interview Angle:**

- How do you know whether to get more data vs regularize more?

---

## Submission Expectations

- Plots/tables for depth sweep and C sweep
- Written bias/variance diagnosis for at least 2 settings
- Short explanation: L1 vs L2 tradeoffs

---

## FAANG Interview Evaluation Rubric

| Skill                         | Evaluated |
|------------------------------|-----------|
| Bias/variance diagnosis       | ✅        |
| Experimental discipline       | ✅        |
| Regularization intuition      | ✅        |
| Communication clarity         | ✅        |
| Correct sklearn usage         | ✅        |

---

## Stretch Problems (Optional)

- Add `SGDClassifier` with early stopping and compare to L2 logistic regression
- Compute calibration (ECE) across regularization settings
