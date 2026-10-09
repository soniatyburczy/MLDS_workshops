# Phishing URL Detection Workshop (MLDS × ISACA)

In this workshop, you'll turn the red flags security teams look for into numbers a model can learn from, then train a **logistic regression** model that estimates the probability a URL is a phishing link. Everything runs **directly in your browser** using [Google Colab](https://colab.research.google.com/).

---

## Topics Covered

1. **Loading & Inspecting Data**
   - Reading a CSV into a DataFrame with `pd.read_csv()`
   - Checking class balance with `.value_counts()`
   - Sampling and reading real phishing vs. legitimate URLs

2. **Feature Engineering**
   - Turning phishing red flags into numeric features
   - pandas string methods: `.str.len()`, `.str.count()`, `.str.contains()`
   - Building a reusable `make_features()` function
   - Features like URL length, digits, hyphens, `@` symbols, raw IP addresses, subdomains, and suspicious TLDs

3. **Exploring the Features**
   - Comparing class averages with `groupby()`
   - Visualizing differences with box plots

4. **Training a Logistic Regression Model**
   - Train/test split with `train_test_split` (and why `random_state` matters)
   - Scaling features with `StandardScaler`
   - Fitting `LogisticRegression()`

5. **Interpreting the Model**
   - Reading the weights: **z = w₁x₁ + w₂x₂ + … + b**
   - Which features push a URL toward *phishing* vs. *legit*

6. **Evaluating the Model**
   - Accuracy vs. a baseline
   - Confusion matrix
   - Precision and recall, and which mistake is worse

7. **Choosing a Threshold**
   - `predict` vs. `predict_proba`
   - Trading off precision and recall by moving the cutoff

8. **Error Analysis**
   - Looking at the phishing URLs the model missed
   - 🏆 Challenge: write URLs that fool the model

---

## Workshop Format

- **Live Coding in Google Colab**: no installation required.
- **✏️ cells** throughout where you write the code yourself.
- **💬 cells** where you stop and think or talk with the people next to you.
- **Fool-the-model challenge** at the end.
- **Solutions notebook** provided so you can check your work after the workshop.

---

## Files

| File | What it is |
|---|---|
| `phishing_detection.ipynb` | The workshop notebook (student version) |
| `phishing_detection_solutions.ipynb` | Completed notebook with solutions |
| `logistic_regression_guide.ipynb` | Beginner's guide to logistic regression, built from scratch (sigmoid, log loss, weights, metrics, thresholds) |
| `phishing_urls.csv` | The dataset (20,000 labeled URLs) |
| `Cheat_Sheets/` | pandas, scikit-learn, and Matplotlib cheat sheets |

---

## Getting Started with Google Colab

1. Open **Google Colab**: [https://colab.research.google.com/](https://colab.research.google.com/)
2. Sign in with your Google account.
3. Click **File → Upload notebook** and select `phishing_detection.ipynb`.
4. Click the **folder icon** in the left sidebar, then the **upload icon**, and upload `phishing_urls.csv`.
5. Click into a code cell and press **Shift + Enter** to run it.

> **Note:** Files uploaded to Colab are deleted when the session ends, so you'll need to re-upload `phishing_urls.csv` if you come back later.

---

## Requirements

- A Google account.
- Internet access.
- Basic Python knowledge (variables, functions, loops).
- Some pandas experience helps, but isn't required.
- No prior machine learning experience needed!

---

## About the Dataset

`phishing_urls.csv` is a sample of the [PhiUSIIL Phishing URL dataset](https://www.kaggle.com/datasets/kaggleprollc/phishing-url-websites-dataset-phiusiil). It has two columns:
- `URL`: the link
- `label`: **1 = phishing**, **0 = legitimate**

How the original dataset became `phishing_urls.csv`:
- Sampled 237k rows down to 20k (random sampling, `random_state=64`).
- Dropped all columns except `URL` and `label`.
- Reversed the label column. The original dataset uses `1` for legitimate and `0` for phishing; we flipped it so `1` = phishing, the class we're trying to catch.

---

## After the Workshop

By the end of this workshop, you will:
- Understand how to turn raw text (URLs) into numeric features a model can use.
- Be able to train and interpret a logistic regression classifier.
- Know why accuracy alone can be misleading, and how to use precision, recall, and the confusion matrix instead.
- Understand that the decision threshold is a choice with real trade-offs.
- See how a simple model fits into a real phishing defense, and why attackers adapting means detectors need constant updating.

---

## Resource Credits

- Dataset: [PhiUSIIL Phishing URL Dataset (Kaggle)](https://www.kaggle.com/datasets/kaggleprollc/phishing-url-websites-dataset-phiusiil)
- Pandas Cheat Sheet: https://pandas.pydata.org/Pandas_Cheat_Sheet.pdf
- Scikit-learn Cheat Sheet: https://s3.amazonaws.com/assets.datacamp.com/blog_assets/Scikit_Learn_Cheat_Sheet_Python.pdf
