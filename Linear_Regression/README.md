# Linear Regression Workshop
## Predicting Store Revenue

In this workshop, you'll predict how much a store will sell on a given day using **linear regression**, trained on more than two years of real daily sales data from 1,115 Rossmann drug stores in Germany. Along the way, you'll see why most of modeling is actually understanding your data. Everything runs **directly in your browser** using [Google Colab](https://colab.research.google.com/).

---

## Topics Covered

1. **Loading & Exploring Data**
   - Reading a CSV into a DataFrame with `pd.read_csv()`
   - Summary statistics with `.describe()`
   - Correlation matrices and heatmaps

2. **Cleaning the Data**
   - Dropping closed-store days
   - Fixing mixed data types (`StateHoliday`)

3. **Train/Test Split for Time Data**

4. **Simple Linear Regression**
   - Fitting `LinearRegression()` with one feature: **Sales = b₀ + b₁x**
   - Reading the intercept and slope

5. **Evaluating a Regression Model**
   - Errors and residuals
   - MAE, MSE, RMSE, and R²

6. **Target Leakage**

7. **Looking at the Features**

8. **Multiple Linear Regression**
   - One-hot encoding categories with `pd.get_dummies()`
   - Target encoding store IDs (computed from training data only)
   - Comparing models against a simple baseline

9. **Checking the Model**

---

## Workshop Format

- **Live Coding in Google Colab**: no installation required.
- **✏️ cells** where you write the code yourself.
- **💬 cells** where you stop and discuss.
-**👀 cells** for notes.
- **Solutions notebook** provided so you can check your work after the workshop.

---

## Files

| File | What it is |
|---|---|
| `linear_regression.ipynb` | The workshop notebook (student version) |
| `linear_regression_solutions.ipynb` | Completed notebook with solutions |
| `train.csv` | The dataset |
| `store.csv` | Additional store information |

---

## Getting Started with Google Colab

1. Open **Google Colab**: [https://colab.research.google.com/](https://colab.research.google.com/)
2. Sign in with your Google account.
3. Click **File → Upload notebook** and select `linear_regression.ipynb`.
4. Click the **folder icon** in the left sidebar, then the **upload icon**, and upload `train.csv`.
5. Click into a code cell and press **Shift + Enter** to run it.

> **Note:** Files uploaded to Colab are deleted when the session ends, so you'll need to re-upload `train.csv` if you come back later.

---

## About the Dataset

`train.csv` is from the [Rossmann Store Sales](https://www.kaggle.com/competitions/rossmann-store-sales) Kaggle competition. Each row is one store on one day (January 2013 – July 2015), with that day's sales, customer count, and whether the store was open, running a promo, or on a holiday.

---

## After the Workshop

By the end of this workshop, you will:
- Be able to fit and evaluate simple and multiple linear regression models.
- Know why exploring your data comes before modeling.

