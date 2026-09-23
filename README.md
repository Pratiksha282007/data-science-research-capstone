# Data Science Research Capstone — Predictive Analytics for Daily Demand

## Project Overview

This project presents a complete data science research workflow for predicting daily demand using historical demand patterns, marketing events, holidays, and calendar-based characteristics.

The project was developed as part of an internship capstone and includes exploratory data analysis, statistical hypothesis testing, feature engineering, predictive modeling, model evaluation, and business interpretation.

## Research Question

**Can historical demand patterns, marketing events, holidays, and calendar-based characteristics be used to predict daily demand accurately?**

## Objectives

* Analyze daily demand patterns over time.
* Examine the relationship between demand, marketing events, and holidays.
* Engineer useful calendar-based predictive features.
* Develop machine learning models for daily demand prediction.
* Compare model performance using MAE, RMSE, and R².
* Translate analytical findings into practical business implications.

## Dataset

The dataset contains 30 daily observations with the following variables:

* `date` — observation date
* `demand` — daily demand value
* `marketing_event` — indicator for marketing-event days
* `holiday` — indicator for holiday days

The dataset was checked for missing values and duplicate records before analysis.

## Methodology

The analysis followed these major stages:

1. Data loading and inspection
2. Data quality assessment
3. Date conversion and chronological sorting
4. Exploratory data analysis
5. Calendar-based feature engineering
6. Statistical hypothesis testing
7. Chronological train-test split
8. Predictive model development
9. Model evaluation
10. Business interpretation
11. Limitations and future research

## Exploratory Data Analysis

The analysis included:

* Daily demand trend visualization
* Demand distribution analysis
* Demand comparison across marketing-event days
* Demand comparison across holidays
* Correlation analysis
* Grouped statistical summaries

## Statistical Analysis

An independent two-sample t-test was conducted to compare demand between marketing-event and non-marketing-event days.

### Result

* t-statistic: **4.2128**
* p-value: **0.0014**
* Significance level: **0.05**

Since the p-value is below 0.05, the analysis found a statistically significant difference in mean demand between the two groups in this sample.

This result indicates an association in the observed data and should not be interpreted as proof that marketing events directly caused the difference.

## Predictive Modeling

Two regression models were developed:

### 1. Linear Regression

Performance:

* MAE: **2.8155**
* RMSE: **3.1495**
* R²: **0.9143**

### 2. Random Forest Regressor

Parameters:

* `n_estimators = 200`
* `random_state = 42`

Performance:

* MAE: **5.4508**
* RMSE: **6.2210**
* R²: **0.6658**

The evaluation used a chronological 80/20 train-test split, with 24 observations used for training and 6 observations used for testing.

The results are specific to this dataset and test period. Because the dataset is small, the model performance should be interpreted cautiously.

## Key Findings

* Daily demand showed measurable variation across the observation period.
* Marketing-event days and non-event days showed a statistically significant difference in mean demand in the sample.
* Calendar-based variables provided useful predictive information for the models.
* Linear Regression achieved lower MAE and RMSE and a higher R² than Random Forest on the selected test period.
* The small dataset limits the reliability of broad generalizations.

## Business Implications

The analysis demonstrates how organizations can use historical demand and event-related information to support demand planning.

Potential applications include:

* Inventory planning
* Staff scheduling
* Marketing-event planning
* Short-term demand forecasting
* Resource allocation

Marketing events and holidays may be incorporated as explanatory variables when developing demand-planning systems.

## Limitations

The main limitations are:

* The dataset contains only 30 observations.
* The test set contains only 6 observations.
* The available variables are limited.
* The analysis does not establish causal relationships.
* Model performance may change with a larger and more diverse dataset.

## Future Research

Future work could include:

* Collecting a larger historical dataset.
* Adding price and promotion information.
* Including weather and seasonal variables.
* Testing time-series forecasting models such as ARIMA or Prophet.
* Applying cross-validation designed for time-series data.
* Comparing additional machine learning models.
* Monitoring model performance on future observations.

## Repository Structure

```text
data-science-research-capstone/
│
├── Data_Science_Research_Capstone.ipynb
├── marketing_sales.csv.csv
├── Data_Science_Research_Capstone_Report.pdf
└── README.md
```

## How to Run the Project

The notebook can be opened and executed using Google Colab or Jupyter Notebook.

### Google Colab

1. Open the `.ipynb` file in Google Colab.
2. Upload `marketing_sales.csv.csv` when required.
3. Run the notebook cells from top to bottom.
4. Review the exploratory analysis, statistical tests, model results, and conclusions.

## Technologies Used

* Python
* Pandas
* NumPy
* Matplotlib
* Seaborn
* SciPy
* Scikit-learn
* Google Colab
* Jupyter Notebook

## Deliverables

This repository contains:

* Complete research notebook
* Dataset used for analysis
* Formal research report / whitepaper in PDF format
* Project documentation

## Author

**Pratiksha**

Data Science Research Capstone — 2026
