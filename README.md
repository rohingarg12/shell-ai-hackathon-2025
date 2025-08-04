

# Shell.ai Hackathon 2025 — Fuel Blend Properties Prediction Challenge

**Max. score: 100**
*This competition is no longer open for practice.
Repository by rohingarg12

---

## 🏆 Introduction

Welcome to our submission for the sixth edition of the Shell.ai Hackathon for Sustainable and Affordable Energy. This global hackathon brings together AI and data enthusiasts to tackle real energy challenges and accelerate the energy transition.

This year’s theme: **Blend Properties Estimation for Sustainable Fuel.**
Our goal: **Predict the final properties of complex fuel blends based on their constituent components and proportions.**

---

## 🚩 Challenge Overview

Sustainable Aviation Fuels (SAFs) and other innovative blends are key to a greener future, but finding optimal fuel combinations is a sophisticated challenge. Blending various sustainable and conventional fuels must:

* Meet strict safety & performance requirements
* Maximize sustainability & economic viability

The relationships between blend composition and final properties are **highly complex** — both linear and non-linear, with hidden interactions.

**Your challenge:**
Develop machine learning models that can **accurately predict the final properties of fuel blends** given their composition and component properties.

---

## 📈 Problem Statement

In the fuel industry, blending is both an art and a science. Given the non-linear and synergistic effects of mixing diverse components, **predicting blend properties is a high-dimensional challenge**.

Your task:
Build models that, based on the proportions and properties of fuel components, **precisely estimate the final blend properties**—guiding real-world decisions on safety, performance, and sustainability.

Key goals for this challenge:

* **Evaluate** thousands of blend combinations rapidly
* **Identify** optimal sustainable recipes
* **Accelerate** development of new fuel formulations
* **Enable** real-time blend optimization

---

## 🗃️ Data Description

* **train.csv** — 65 columns per row:

  * 5: Blend composition (volume % of each base component)
  * 50: Component properties (real-world batch COA values)
  * 10: Final blend properties (**targets**)
* **test.csv** — Same as above, but only the 55 input columns (no targets)
* **sample\_submission.csv** — Required format for submissions (ID + 10 target columns)

Example column groupings:

```
Blend1, Blend2, Blend3, Blend4, Blend5, Component1_Property1, ..., BlendProperty1, ..., BlendProperty10
```

---

## 🏗️ Our Solution

This repository contains a **Google Colab notebook** documenting the **full modeling journey**, including:

* Exploratory data analysis (EDA)
* Data preprocessing and feature engineering
* Multiple ML models:

  * CatBoost
  * LightGBM
  * XGBoost
  * SVR
  * (Stacked ensemble approaches)
* **Optuna hyperparameter tuning**
* Advanced validation strategies
* **Real errors and debugging steps included** for transparency and reproducibility

The process is documented **start to finish**:
You’ll see not only the working code, but also the mistakes, errors, and how each was solved.

---

## 📂 Submission Files

This repo includes all final CSV files submitted for leaderboard evaluation:

| File Name                        | Description                                        |
| -------------------------------- | -------------------------------------------------- |
| `submission_90plus_PRO.csv`      | Highest scoring/pro ensemble model (final version) |
| `submission_90plus_blended.csv`  | Ensemble/blended model submission                  |
| `submission_90plus_seed1337.csv` | Model trained with random seed 1337                |
| `submission_90plus_seed2024.csv` | Model trained with random seed 2024                |
| `submission_90plus_seed42.csv`   | Model trained with random seed 42                  |


Each file follows the required Shell.ai submission format:
`ID, BlendProperty1, BlendProperty2, ..., BlendProperty10`

Use these files as references for submission formatting, result comparison, or to reproduce leaderboard results.

---

## 🚀 How to Use

1. **Open the notebook** (`ShellAI2025_FuelBlend_Ensemble.ipynb`) in Google Colab (recommended).
2. Follow through each step—explore EDA, model development, hyperparameter tuning, error handling, and final prediction.
3. Try editing or running cells to adapt to your data or extend the solution.

*No special installation is required for Colab notebooks (dependencies installed in-code).*

---

## 🏅 Results

* **Final public leaderboard score:** XX.XX (replace with your score)
* Achieved with stacked ensemble and advanced feature engineering

---

## 📊 Evaluation Metric

* **Mean Absolute Percentage Error (MAPE)** is used for leaderboard ranking
  (as implemented in scikit-learn).

* There are **two leaderboard rounds**:

  * Public: First 250 test samples
  * Private: Remaining 250 test samples (final score)

---

## 🤝 Credits

Developed by **\[Your Name / Team Name]**

Inspired by the drive for **sustainable energy solutions** through data science.

---

## 📎 References

* [Shell.ai Hackathon](https://www.shell.com/ai-hackathon) *(update link if needed)*
* [scikit-learn MAPE metric](https://scikit-learn.org/stable/modules/generated/sklearn.metrics.mean_absolute_percentage_error.html)

---

**Feel free to fork, adapt, and use this repository as a template for future ML competitions!**

