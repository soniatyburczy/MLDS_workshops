# Machine Learning and Data Science Workshops

## Overview

This repository houses a collection of hands-on data science and machine learning workshops for **Baruch College's Machine Learning and Data Science Club**, designed to help participants build foundational and advanced skills in data analysis, visualization, and modeling using Python and popular data science libraries.

---

## About This Fork

This repo is a continuation of the workshop series originally created by **Yahia Taraf** ([@YTaraf](https://github.com/YTaraf)), the club's previous Workshop Director. His original repository is available [here](https://github.com/YTaraf/Work_Shops).

---

## Workshop Structure

Each workshop folder contains:
- **Workshop Notebook (`.ipynb`)**: A Jupyter Notebook with explanations, code, and exercises.
- **Workshop Solutions Notebook (`.ipynb`)**: A Jupyter Notebook with solutions to exercises.
- **Datasets (`.csv` or other formats)**: Sample data used for hands-on learning.
- **Resources & Readings**: Additional materials to reinforce learning.

### Topics Covered
Key topics across the workshops include:
- **Python Fundamentals**: Types, syntax, functions, loops, and core data structures.
- **Data Visualization**: Creating and customizing charts using Matplotlib and Seaborn.
- **Data Wrangling**: Cleaning and manipulating data using Pandas.
- **Exploratory Data Analysis (EDA)**: Identifying trends and insights in datasets.
- **Machine Learning**: Implementing models with Scikit-Learn.

---

## Running the Workshops in Google Colab

All workshops are designed to run in **[Google Colab](https://colab.google/)** for easy accessibility.

To get started:
1. Open **Google Colab** and upload the workshop notebook (`.ipynb`).
2. If the workshop requires a dataset, upload the CSV file and load it using:
```python
   from google.colab import files
   uploaded = files.upload()
```

