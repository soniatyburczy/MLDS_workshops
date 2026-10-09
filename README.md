# Machine Learning and Data Science Workshops

## Overview

This repository houses hands-on data science and machine learning workshops for **Baruch College's Machine Learning and Data Science Club**, designed to help participants build foundational and advanced skills in data analysis, visualization, and modeling using Python and popular data science libraries.

---

## About This Repository

All workshops in this repository were created by **Sonia Tyburczy**, the club's current Workshop Director, with contributions from the club's workshop coordinators.

The repository began as a fork of the workshop series by **Yahia Taraf** ([@YTaraf](https://github.com/YTaraf)), the club's previous Workshop Director, whose original repository is available [here](https://github.com/YTaraf/Work_Shops). Some workshops cover similar topics to his series, but the materials here have been rebuilt from scratch, and several workshops are entirely new.

---

## Workshop Structure

Each workshop folder contains:
- **Presentation Slides** (`pdf`): The slideshow used to present the workshop.
- **Workshop Notebook (`.ipynb`)**: A Jupyter Notebook with explanations, code, and exercises.
- **Solutions Notebook (`.ipynb`)**: Worked solutions to the exercises.
- **Datasets (`.csv`)**: Sample data used for hands-on learning.
- **Resources & Readings**: Additional materials to reinforce learning.

### Topics Covered
- **Python Fundamentals**: Types, syntax, functions, loops, and core data structures.
- **Data Visualization**: Creating and customizing charts with Matplotlib and Seaborn.
- **Data Wrangling**: Cleaning and manipulating data with Pandas.
- **Exploratory Data Analysis (EDA)**: Identifying trends and insights in datasets.
- **Machine Learning**: Building models with Scikit-Learn.

---

## Running the Workshops in Google Colab

All workshops are designed to run in **[Google Colab](https://colab.google/)**.

1. Open **Google Colab** and upload the workshop notebook (`.ipynb`).
2. If the workshop uses a dataset, upload the file and load it with:

```python
    from google.colab import files
    uploaded = files.upload()
```

---

## AI Transparency Statement

Generative AI tools ([e.g., Claude, ChatGPT, GitHub Copilot]) were used in developing some of the materials in this repository. AI assistance was used for:
- [Drafting or refining explanatory text in notebooks and slides]
- [Generating or debugging example code]
- [Creating or cleaning sample datasets]

All AI-assisted content was reviewed, edited, and tested by the workshop team, who take full responsibility for its accuracy. Workshop design, topic selection, and teaching decisions are our own.

If you find an error, please [open an issue / contact us].