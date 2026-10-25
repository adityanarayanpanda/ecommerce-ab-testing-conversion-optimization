
# 📊 Dataset — E-Commerce A/B Testing & Conversion Rate Optimization

## 📌 Overview

This folder contains the datasets used in the **E-Commerce A/B Testing & Conversion Rate Optimization** project.

The datasets are used to compare the conversion performance of the existing landing page (Control Group) against the redesigned landing page (Treatment Group).

## 📁 Dataset Files

### 1. `ab_data.csv`

The primary dataset containing user-level A/B testing information.

| Column | Description |
|---|---|
| `user_id` | Unique identifier assigned to each user |
| `timestamp` | Date and time of the experiment record |
| `group` | Experiment group: `control` or `treatment` |
| `landing_page` | Landing page assigned: `old_page` or `new_page` |
| `converted` | Conversion outcome: `1` = converted, `0` = not converted |

### 2. `countries.csv`

The supplementary dataset used for country-level conversion analysis.

| Column | Description |
|---|---|
| `user_id` | User identifier used to join the datasets |
| `country` | Country associated with the user |

## 🧹 Data Preparation

The following data preparation steps were performed using Python:

- Inspected dataset structure and data types.
- Checked for missing values and duplicate user IDs.
- Validated experiment group and landing-page assignments.
- Removed records with inconsistent group and landing-page assignments.
- Removed the remaining duplicate user record.
- Prepared date values for daily conversion analysis.
- Combined country information with the cleaned experiment dataset.

**Final cleaned dataset:** 290,584 unique users.

## 🎯 Analysis Objectives

The datasets support the following analyses:

- Control vs. treatment conversion-rate comparison.
- Absolute conversion difference and relative conversion lift.
- Statistical hypothesis testing using a two-proportion Z-test.
- 95% confidence interval estimation.
- Daily conversion-rate trend analysis.
- Country-level conversion-rate analysis.

## 🛠️ Tools Used

- **Python:** Pandas, NumPy, SciPy, Statsmodels, Matplotlib
- **Power BI:** KPI cards, interactive charts, and slicers
- **Statistics:** Hypothesis testing, p-values, and confidence intervals

## 📈 Key Results

| Metric | Result |
|---|---:|
| Total Users | 290,584 |
| Total Conversions | 34,753 |
| Control Conversion Rate | 12.04% |
| Treatment Conversion Rate | 11.88% |
| Conversion Difference | -0.16 percentage points |
| Relative Conversion Change | -1.31% |
| One-Sided Z-Test P-Value | 0.905 |

## 💡 Important Note

The experiment did not provide statistically significant evidence that the new landing page improves conversion at the 5% significance level.

These findings apply to the supplied dataset and should not automatically be generalized to all e-commerce businesses.

## 👤 Project Information

**Project:** E-Commerce A/B Testing & Conversion Rate Optimization  
**Author:** Aditya Narayan Panda  
**Purpose:** Data analytics portfolio project

