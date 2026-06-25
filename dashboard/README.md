# Power BI Dashboard Dataset

## File

`power_bi_county_mortality_dataset.csv`

## Purpose

This file is the dashboard-ready dataset for the Preventable Death Map project. It combines county-level premature mortality, health behavior/status indicators, disease burden indicators, and socioeconomic predictors.

## Dashboard Goal

The Power BI dashboard will help users explore which county-level indicators are most associated with premature mortality across U.S. counties.

## Recommended Dashboard Pages

### 1. National Overview

- U.S. county map of age-adjusted premature mortality
- KPI cards for average premature mortality, highest-risk county, and number of counties analyzed
- State filter

### 2. Actionable Risk Factors

- Correlation chart for non-disease indicators
- Smoking vs. premature mortality scatterplot
- Poverty vs. premature mortality scatterplot
- Filters for state and county

### 3. Socioeconomic Conditions

- Poverty, income, education, and unemployment visuals
- County ranking table
- Comparison of high-poverty vs. low-poverty counties

### 4. Disease Burden Context

- Disease burden indicators such as coronary heart disease, stroke, COPD, diabetes, and high blood pressure
- Clearly labeled as outcome-adjacent context rather than the main causal story

## Key Dashboard Fields

### Geography

- County FIPS
- Original County FIPS
- County
- State

### Mortality Outcome

- Premature Deaths 2015-2019
- Population 2015-2019
- Premature Mortality Crude Rate
- Premature Mortality Age-Adjusted Rate
- Age-Adjusted Rate Unreliable

### Health Behavior / Status

- Smoking Rate
- Physical Inactivity Rate
- Poor Physical Health Rate
- Poor Mental Health Rate
- Insufficient Sleep Rate
- Obesity Rate
- Uninsured Rate

### Disease Burden

- Diabetes Rate
- High Blood Pressure Rate
- COPD Rate
- Coronary Heart Disease Rate
- Stroke Rate

### Socioeconomic

- Median Household Income
- Poverty Rate
- Bachelor's Degree or Higher Rate
- Unemployment Rate

## Interpretation Note

This dashboard shows county-level associations, not proof of individual-level causation. The strongest portfolio story should focus on actionable health, behavior, and socioeconomic indicators rather than only disease burden indicators.
