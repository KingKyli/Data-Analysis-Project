# Exploratory Data Analysis of the Instagram Reach Dataset

**Author:** Sotiris Kylintireas | Student ID: 3220098
**Date:** March 2026
**Language:** R (R Markdown)

---

## Overview

This project presents a structured **Exploratory Data Analysis (EDA)** of the *Instagram Reach* dataset, a collection of 100 Instagram posts with engagement metrics including follower counts, post age, and likes received.

The analysis spans descriptive statistics, distributional assessment, bivariate and categorical relationships, and a logistic regression model for predicting high-engagement posts.

---

## Dataset

| Property | Detail |
|---|---|
| Observations | 100 posts |
| Variables (after cleaning) | 6 |
| Key numeric variables | `Followers`, `Hours.since.posted`, `Likes` |
| Key categorical variables | `USERNAME`, `time`, `like`, `high_like` |

> **To run this project:** Place `instagram_reach.txt` in your R working directory before knitting.

---

## Key Findings

- 📈 **Moderate positive correlation** (r ≈ 0.61) between `Hours.since.posted` and `Likes` — older posts accumulate more engagement.
- 📊 **Followers distribution is right-skewed** and non-normal, with notable outliers among high-follower accounts.
- 🏷️ **Posting recency (`time`) predicts engagement level** — posts in category `time = 4` show the highest rate of high likes.
- 🤖 **Logistic regression model** using `Followers` and `Hours.since.posted` achieves ~77% accuracy; `Hours.since.posted` is the statistically significant predictor (p < 0.01).

---

## Technologies

| Tool | Purpose |
|---|---|
| R / R Markdown | Analysis and report generation |
| ggplot2 | All data visualizations |
| knitr + kableExtra | Report formatting and tables |
| pROC | ROC curve and AUC computation |
| dplyr + scales | Data wrangling and formatting |

---

## How to Run

1. Clone this repository
2. Place `instagram_reach.txt` in your R working directory
3. Open `instagram_analysis.Rmd` in RStudio
4. Click **Knit → Knit to HTML**

---

## Project Structure

```
├── instagram_analysis.Rmd   # Main analysis report
├── instagram_analysis.html  # Rendered HTML output
├── instagram_reach.txt      # Dataset (place in working directory)
└── README.md                # This file
```

---

## Author

**Sotiris Kylintireas**
Student ID: 3220098
GitHub: <a href="https://github.com/KingKyli">@KingKyli</a>
