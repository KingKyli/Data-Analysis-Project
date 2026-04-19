# Exploratory Data Analysis of the Instagram Reach Dataset

**Author:** Sotiris Kylintireas (Student ID: 3220098)
**Date:** March 2026
**Language:** R (R Markdown)

## Overview

This project presents an exploratory data analysis of the *Instagram Reach* dataset, which includes 100 posts and their core engagement characteristics.

The report follows a clear workflow: data inspection and preparation, variable engineering, descriptive and visual analysis, and a final logistic regression model for predicting high-engagement posts.

## Dataset

| Property | Detail |
|---|---|
| Observations | 100 posts |
| Variables (after cleaning) | 6 |
| Main numeric variables | `Followers`, `Hours.since.posted`, `Likes` |
| Main categorical variables | `USERNAME`, `time`, `like`, `high_like` |

> **Important:** Place `instagram_reach.txt` in your R working directory before knitting the report.

## Main Findings

- There is a **moderate positive relationship** (r ≈ 0.61) between `Hours.since.posted` and `Likes`, indicating that older posts generally collect more likes.
- The `Followers` distribution is **strongly right-skewed**, with several high-value outliers.
- The engineered `time` categories are meaningfully associated with engagement outcomes.
- In logistic regression, `Hours.since.posted` is the most influential predictor for high engagement, and the model reaches about **77% classification accuracy**.

## Tools and Libraries

| Tool | Purpose |
|---|---|
| R / R Markdown | Analysis and report generation |
| ggplot2 | Data visualization |
| knitr + kableExtra | Tables and report formatting |
| dplyr + scales | Data manipulation and labels |
| pROC | ROC curve and AUC evaluation |

## How to Run

1. Clone the repository.
2. Place `instagram_reach.txt` in your R working directory.
3. Open `instagram_analysis.Rmd` in RStudio.
4. Knit the file to HTML (`Knit → Knit to HTML`).

## Project Structure

```
├── instagram_analysis.Rmd   # Main analysis report
├── instagram_analysis.html  # Rendered output
├── instagram_reach.txt      # Input dataset (local placement required)
└── README.md                # Project overview and usage
```

## Author

Sotiris Kylintireas
Student ID: 3220098
GitHub: [@KingKyli](https://github.com/KingKyli)
