# IMDb-Analysis-Hypothesis-PowerBi

# IMDb Movie Analytics & Hypothesis Testing Dashboard

## Project Overview
This project analyzes IMDb movie data to evaluate whether production budget and director gender significantly influence audience ratings. Using Python for data preprocessing and statistical analysis, followed by Power BI for visualization, the project applies hypothesis-driven analytics to uncover meaningful insights from real-world movie datasets.

The dashboard presents key performance indicators, correlation analysis, and hypothesis testing results in a single interactive Power BI report.

## Objectives
Analyze the relationship between movie budget and IMDb ratings
Evaluate whether director gender impacts audience ratings
Perform hypothesis testing to validate analytical assumptions
Build an interactive Power BI dashboard to communicate findings visually

## Datasets
Two datasets were used:

Movies Table
id
title
budget
revenue
popularity
vote_average (renamed to IMDB_rating)
vote_count
director_id
year, month, day

Directors Table
id
director_name
gender

The datasets were connected using:

**movies.director_id → directors.id**

forming a fact–dimension model.

## 🛠 Tools & Technologies

Python (Pandas, NumPy, SciPy, Matplotlib, Seaborn)

Google Colab

Power BI

GitHub

## Data Preparation

Converted numeric fields (budget, ratings) to proper data types
Removed missing and inconsistent values
Renamed columns for clarity
Created clean CSV files for Power BI
Modeled data using a fact (movies) and dimension (directors) structure

## 📊 Exploratory Data Analysis

Initial EDA included:
IMDb rating distribution
Scatter plot of budget vs IMDb rating
Correlation analysis
Gender-wise rating comparison
These steps helped identify patterns and guided hypothesis formulation.

# Hypothesis Testing

## Hypothesis 1: Does higher budget lead to higher IMDb ratings?

**Null Hypothesis (H₀):**
There is no relationship between movie budget and IMDb rating.

**Alternative Hypothesis (H₁):**
Higher-budget movies tend to have higher IMDb ratings.

Method Used:
**Pearson correlation**

Result:
Correlation ≈ **–0.05 (near zero)**

**Conclusion:**
Movie budget shows virtually no relationship with IMDb ratings. Higher budgets do not guarantee better audience ratings.

## Hypothesis 2: Does director gender influence IMDb ratings?

**Null Hypothesis (H₀):**
There is no significant difference in IMDb ratings between male and female directors.

A**lternative Hypothesis (H₁):**
There is a significant difference in IMDb ratings between male and female directors.

Method Used:
**Independent two-sample t-test**

Result:
**p-value > 0.05**

Conclusion:
There is no statistically significant difference in IMDb ratings based on director gender.

## 📈 Power BI Dashboard

A one-page interactive dashboard was created featuring:

KPI Cards

Total Movies

Average IMDb Rating

Average Budget

Total Directors

Visuals

Scatter Plot: Budget vs IMDb Rating

Bar Chart: Director Gender vs Average IMDb Rating

Bar Chart: Director Gender vs Movie Count

Director Name Slicer

Key Insights

Budget and IMDb ratings show near-zero correlation

Male and female directors receive similar average ratings

Dataset contains significantly more male-directed movies

✅ Final Conclusion

Analysis reveals that neither production budget nor director gender significantly influences IMDb ratings. Audience reception appears to be driven more by storytelling and execution than by financial investment or demographic attributes.
