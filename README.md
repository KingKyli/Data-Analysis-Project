# Exploratory Data Analysis of the Instagram Reach Dataset

> **EDA, feature engineering, and interpretable classification for high-engagement Instagram posts**

**Author:** Sotiris Kylintireas (Student ID: 3220098) | **Date:** March 2026 | **Language:** R (R Markdown)

---

## Project Overview

This project analyzes a dataset of 100 Instagram posts to identify variables associated with high engagement and evaluate a classification model for predicting high-engagement posts. The analysis combines exploratory data analysis, feature engineering, and logistic regression modeling, with evaluation on a held-out test set.

**Highlights:**
- Cleaned and transformed raw social media data
- Engineered categorical engagement variables from numeric features
- Built a full visual EDA pipeline
- Trained and evaluated a logistic regression classifier
- Assessed performance under class imbalance using multiple metrics (accuracy, recall, F1, AUC)
- Compared model against a majority-class baseline

---

## Objective

Determine which variables most influence whether an Instagram post achieves high engagement, and build an interpretable binary classifier to predict high-engagement posts from minimal features.

---

## Dataset

| Property | Detail |
|---|---|
| Observations | 100 posts |
| Variables (after cleaning) | 6 |
| Numeric variables | `Followers`, `Hours.since.posted`, `Likes` |
| Categorical variables | `USERNAME`, `time`, `like`, `high_like` |

> The dataset file (`instagram_reach.txt`) is not tracked in this repository. Place it in the `data/` directory before knitting. See [`data/README.md`](data/README.md) for details.

---

## Methods

1. **Data Inspection** — structural validation, type assignment, index removal
2. **Feature Engineering** — quartile-based `like` tier variable; time-category `time`; binary target `high_like`
3. **Descriptive Statistics** — mean, standard deviation, min/median/max for numeric variables
4. **Distribution Analysis** — histogram with KDE, Q-Q plot for normality assessment
5. **Time-Based Engagement Analysis** — bar chart, boxplot by time category
6. **Correlation and Bivariate Analysis** — Pearson correlation matrix, colored scatterplot
7. **Categorical Association Analysis** — contingency table, grouped bar chart
8. **Logistic Regression Modeling** — trained on 70-post training split
9. **Model Evaluation** — confusion matrix, accuracy, precision, recall, F1, AUC, baseline comparison on 30-post test set

---

## Key Findings

- `Hours.since.posted` is the most statistically significant predictor of high engagement in this dataset — posting age outperforms follower count as a predictor.
- `Followers` is strongly right-skewed; a small number of high-follower accounts distort the mean.
- Posts in the highest time category (4+ hours) show a noticeably higher proportion of high-like outcomes.
- A moderate positive correlation (r ≈ 0.61) exists between `Hours.since.posted` and `Likes`.

---

## Model Performance

| Metric | Value |
|---|---|
| Accuracy (test set) | ~83% |
| Baseline accuracy (majority class) | ~77% |
| AUC | ~0.76 |
| Recall (high-engagement class) | Moderate — limited by class imbalance |

*Exact values are computed at knit time and displayed in the report.*

---

## Files in This Repository

```
Data-Analysis-Project/
│
├── README.md                          # Project overview
├── instagram_analysis.Rmd             # Reproducible analysis source
├── instagram_analysis.html            # Rendered report (clean, no code)
├── report/
│   └── Exploratory_Data_Analysis_Instagram_Reach.pdf
├── data/
│   └── README.md                      # Dataset placement instructions
├── figures/                           # Exported plot files (optional)
└── .gitignore
```

---

## How to Reproduce

1. Clone the repository.
2. Obtain `instagram_reach.txt` and place it in the `data/` directory.
3. Open `instagram_analysis.Rmd` in RStudio.
4. Knit to HTML: `Knit → Knit to HTML`.

---

## Tools Used

| Tool | Purpose |
|---|---|
| R / R Markdown | Analysis and reproducible report generation |
| ggplot2 | Data visualization |
| knitr + kableExtra | Tables and report formatting |
| dplyr + scales | Data manipulation and axis labels |
| pROC | ROC curve and AUC computation |

---

## Why This Project Is Relevant

Social media engagement analysis is a practical and widely applicable domain in data analytics. This project demonstrates a complete analytics workflow — from raw data to a model with proper out-of-sample evaluation — using interpretable methods on a small, real-world dataset. The explicit treatment of class imbalance and the baseline comparison reflect the kind of critical thinking expected in applied analytics roles.

---

## Skills Demonstrated

- Data cleaning and transformation
- Feature engineering from domain context
- Exploratory data analysis
- Statistical interpretation
- Binary classification modeling
- Performance evaluation under class imbalance
- Reproducible reporting with R Markdown

---

**Author:** Sotiris Kylintireas | GitHub: [@KingKyli](https://github.com/KingKyli)
