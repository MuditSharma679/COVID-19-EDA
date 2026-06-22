# COVID-19 Patient Data Analysis (EDA)

## Project Overview

In this project, I performed an end-to-end Exploratory Data Analysis
(EDA) on a COVID-19 patient dataset to identify factors influencing
patient outcomes, especially mortality patterns.

The objective was to understand how demographic factors, medical
conditions, treatment-related variables, and severity indicators impact
COVID-19 patient survival and death outcomes.

------------------------------------------------------------------------

## Dataset Overview

The dataset contains COVID-19 patient records with information related
to:

-   Patient demographics (Age, Sex, Pregnancy)
-   Medical conditions (Diabetes, Hypertension, Obesity, COPD, Asthma,
    Pneumonia, etc.)
-   Treatment details (ICU admission, Intubation, Patient Type)
-   COVID status
-   Death information

The dataset contained encoded categorical values:

-   1 → Yes
-   2 → No
-   97, 98, 99 → Missing / Unknown values

These values were cleaned and transformed into meaningful categories
before analysis.

------------------------------------------------------------------------

# Data Cleaning & Preprocessing

Performed:

-   Dataset structure and column analysis
-   Data type validation
-   Duplicate checking
-   Missing value analysis
-   Handling encoded missing values
-   Conversion of categorical variables into readable formats

Missing values were handled by replacing unavailable information with
"Unknown" to preserve records and avoid unnecessary data loss.

The missing values did not significantly affect the overall distribution
and major patterns observed during analysis.

------------------------------------------------------------------------

# Feature Engineering

Created analytical features:

## Death Status

Created target variable:

-   Died
-   Survived

using the DATE_DIED column.

## Date Features

Extracted:

-   Death Year
-   Death Month
-   Month-Year trend

for time-series mortality analysis.

## Age Group

Created age categories to analyze mortality patterns across different
age segments.

## Severity Analysis

Created severity-related insights using:

-   ICU admission
-   Intubation requirement

to identify critical cases.

## Total Disease Count

Created a feature counting the number of underlying diseases:

-   Diabetes
-   Hypertension
-   Pneumonia
-   Obesity
-   COPD
-   Asthma
-   Cardiovascular disease
-   Renal disease
-   Immunosuppression
-   Other diseases

------------------------------------------------------------------------

# Exploratory Data Analysis

## Univariate Analysis

Analyzed:

-   Age distribution
-   Gender distribution
-   Patient type distribution
-   COVID status
-   Disease distribution
-   Death vs Survival ratio

## Bivariate Analysis

Studied relationships between:

-   Diseases and death outcomes
-   Age and mortality
-   Severity and patient outcomes

## Multivariate Analysis

Performed analysis using:

-   Age Group + Disease + Death Status
-   ICU + COVID Status + Death Status
-   Intubation + COVID Status + Death Status
-   Patient Type + Age Group + Death Status

Used:

-   Crosstab analysis
-   Heatmaps
-   Interactive Plotly visualizations

------------------------------------------------------------------------

# Time Series Analysis

Analyzed COVID mortality trends using death date information.

Created:

-   Year-wise death analysis
-   Month-wise death trends
-   Month-Year mortality trends

This helped identify changes in mortality patterns throughout the
pandemic.

------------------------------------------------------------------------

# Visualization Tools Used

Libraries:

-   Pandas
-   NumPy
-   Matplotlib
-   Seaborn
-   Plotly

Visualizations:

-   Count plots
-   Bar charts
-   Pie charts
-   Box plots
-   Heatmaps
-   Line charts
-   Interactive charts

------------------------------------------------------------------------

# Key Insights

-   Age is one of the major factors associated with COVID mortality.
-   Older age groups showed higher death proportions.
-   Patients with multiple diseases showed higher mortality patterns.
        The highest mortality was observed among patients having 5–6 diseases, where death rates were approximately 44%, indicating that patients with multiple comorbidities had a much higher risk of severe outcomes.
-   ICU admission and intubation were associated with severe cases.
-   Medical conditions such as diabetes, hypertension, pneumonia, and
    obesity showed relationships with patient outcomes.
-   Time-series analysis helped understand mortality changes over the
    pandemic period.

------------------------------------------------------------------------

# Conclusion

This project demonstrates a complete healthcare data analytics workflow
including:

-   Data cleaning
-   Feature engineering
-   Exploratory data analysis
-   Visualization
-   Insight generation

The analysis highlights important factors affecting COVID-19 patient
outcomes and demonstrates how data analytics can support healthcare
decision-making.
