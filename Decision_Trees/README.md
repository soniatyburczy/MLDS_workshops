# Decision Trees Workshop
## Predicting Hotel Cancellations

In this workshop, you'll predict whether a hotel booking will be canceled using a **decision tree**, trained on 119,390 real bookings from two hotels in Portugal (a City Hotel in Lisbon and a Resort Hotel in the Algarve). Along the way, you'll see how a tree builds its own yes/no rules, why deeper isn't always better, and why a model that looks great in a notebook can still be fooling you. Everything runs **directly in your browser** using [Google Colab](https://colab.research.google.com/).

---

## Topics Covered

1. **Exploring the Data**
   - Loading a CSV from a URL with `pd.read_csv()`
   - Summary statistics with `.describe()` for numeric and text columns
   - Counting categories with `.value_counts()`
   - Finding the **baseline** (always guessing "not canceled")
   - Quick charts with `groupby()`: does the cancellation rate change with this feature?

2. **When a Pattern Looks Backwards**
   - Investigating why ~99% of "non-refundable" bookings were canceled
   - Spotting duplicate rows with `.duplicated()`

3. **Cleaning the Data**
   - **Target leakage**: dropping columns you wouldn't know at booking time
   - Dropping columns that won't carry over to new bookings
   - Filling missing values with `.fillna()`

4. **Encoding Categories**
   - One-hot encoding with `pd.get_dummies()`
   - Why trees don't need scaling or `drop_first`

5. **Stratified Train/Test Split**

6. **Fitting a Decision Tree**
   - Fitting `DecisionTreeClassifier()` with a small `max_depth`
   - Drawing and reading the tree with `plot_tree()`: questions, Gini impurity, samples, values, and leaves

7. **Choosing the Depth**
   - Looping over `max_depth` and comparing train vs. test accuracy
   - Underfitting vs. **overfitting**

8. **Evaluating a Classifier**
   - Accuracy compared to the baseline
   - The confusion matrix: false alarms vs. missed cancellations
   - Precision and recall

9. **What the Tree Leans On**
   - Feature importances with `feature_importances_`
   - How duplicates can make a model look better than it is

---

## Workshop Format

- **Live Coding in Google Colab**: no installation required.
- **✏️ cells** where you write the code yourself.
- **💬 cells** where you stop and discuss.
- **👀 cells** for notes.
- **Challenges** at the end if you want to keep going.
- **Solutions notebook** provided so you can check your work after the workshop.

---

## Files

| File | What it is |
|---|---|
| `decision_trees.ipynb` | The workshop notebook (student version) |
| `decision_trees_solutions.ipynb` | Completed notebook with solutions |

> The dataset loads directly from a URL inside the notebook, so there's no CSV to upload.

---

## Getting Started with Google Colab

1. Open **Google Colab**: [https://colab.research.google.com/](https://colab.research.google.com/)
2. Sign in with your Google account.
3. Click **File → Upload notebook** and select `decision_trees.ipynb`.
4. Click into the first code cell and press **Shift + Enter** to run it. Keep running cells **in order** as you go.

> **Note:** Colab needs an internet connection to download the data. If you come back later, re-run the cells from the top, since variables are cleared when the session ends.

---

## About the Dataset

The **Hotel Booking Demand** data comes from [TidyTuesday](https://github.com/rfordatascience/tidytuesday/tree/main/data/2020/2020-02-11). Each row is one booking (arrivals from July 2015 to August 2017), with details like how far ahead it was booked, the length of the stay, the meal plan, how it was booked, the deposit type, the price per night, and any special requests. The target is `is_canceled` (1 = canceled, 0 = not).

---

## After the Workshop

By the end of this workshop, you will:
- Be able to fit, draw, and read a decision tree classifier.
- Know how to pick a tree depth by watching for overfitting.
- Be able to evaluate a classifier with a baseline, a confusion matrix, precision, and recall.
- Know how to spot leakage and suspicious patterns before trusting a model.
