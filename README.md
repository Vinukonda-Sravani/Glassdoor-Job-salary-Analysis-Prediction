# Glassdoor Job Salary Analysis & Prediction

## 🌍 Overview

This project analyzes job salary data from Glassdoor to uncover key trends and build a machine learning model to predict salary ranges. It is aimed at helping job seekers, recruiters, and employers make data-driven decisions regarding compensation.

## 🏢 Dataset

* **Source**: glassdoor_jobs.csv
* **Size**: ~1000 job listings
* **Features**: Job Title, Company Info, Location, Rating, Industry, Salary Estimate, etc.

## ✅ Project Phases

### ✏️ Phase 1: Data Cleaning

* Removed rows with missing or invalid salary estimates
* Extracted numerical values from `Salary Estimate` to create `min_salary`, `max_salary`, and `avg_salary`
* Cleaned and standardized categorical columns (Job Title, Company Name, Location)
* One-hot encoded all categorical features

### 📊 Phase 2: Exploratory Data Analysis (EDA)

* Salary distribution visualized using histograms and boxplots
* Compared salary by:
  * Job Title (top-paying roles)
  * Location (top cities)
  * Company Size
  * Company Rating
* Found trends such as:
  * Data scientists earn among the highest salaries
  * Jobs in California and New York offer higher pay
  * Company rating has weak correlation with salary

### 🤖 Phase 3: Machine Learning Modeling

* Target: `avg_salary`
* Models built:
  * Linear Regression (baseline)
  * XGBoost Regressor (tuned using GridSearchCV)
* Performance metrics:
  * RMSE (Root Mean Squared Error)
  * R² Score

### 👁️ Feature Importance

* Identified top predictors using XGBoost feature importance:
  * Job Title
  * Location
  * Rating
  * Size
  * Industry

## 🚀 Results

| Model             | RMSE   | R² Score |
| ----------------- | ------ | -------- |
| Linear Regression | 11,000 | 0.29     |
| XGBoost (tuned)   | 9,827  | 0.41     |

## 📆 Final Deliverables

* `glassdoor_salaray_prediction`: ML model
* `glassdoor_jobs.csv`: dataset
* `README.md` or `Report.pdf`: Summary report for HR/internship submission



