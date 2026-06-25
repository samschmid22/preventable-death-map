# Power BI Dashboard Build Plan

## Dashboard Title

Preventable Death Map: County-Level Risk Patterns in Premature Mortality

## Dataset

Use:

`dashboard/power_bi_county_mortality_dataset.csv`

## Page 1: National Overview

### Purpose

Show the overall county-level premature mortality pattern across the United States.

### Visuals

1. Filled map or shape map
   - Location: County FIPS
   - Color saturation: Premature Mortality Age-Adjusted Rate
   - Tooltip: County, State, Premature Mortality Age-Adjusted Rate, Poverty Rate, Smoking Rate, Poor Mental Health Rate

2. KPI cards
   - Counties analyzed
   - Average Premature Mortality Age-Adjusted Rate
   - Highest-risk county
   - Median Poverty Rate

3. State slicer
   - Field: State

4. County ranking table
   - County
   - State
   - Premature Mortality Age-Adjusted Rate
   - Poverty Rate
   - Smoking Rate
   - Poor Mental Health Rate

## Page 2: Actionable Risk Factors

### Purpose

Show which non-disease indicators are most associated with premature mortality.

### Visuals

1. Bar chart
   - Use actionable predictor correlations
   - Highlight: Poor Mental Health, Poor Physical Health, Physical Inactivity, Smoking, Poverty

2. Scatterplot
   - X-axis: Smoking Rate
   - Y-axis: Premature Mortality Age-Adjusted Rate
   - Tooltip: County, State, Poverty Rate, Poor Mental Health Rate

3. Scatterplot
   - X-axis: Poverty Rate
   - Y-axis: Premature Mortality Age-Adjusted Rate
   - Tooltip: County, State, Smoking Rate, Median Household Income

4. Slicers
   - State
   - Age-Adjusted Rate Unreliable

## Page 3: Socioeconomic Conditions

### Purpose

Show how poverty, income, education, and unemployment relate to premature mortality.

### Visuals

1. Bar chart
   - Poverty Rate
   - Unemployment Rate
   - Bachelor's Degree or Higher Rate
   - Median Household Income

2. Scatterplot
   - X-axis: Median Household Income
   - Y-axis: Premature Mortality Age-Adjusted Rate

3. County ranking table
   - County
   - State
   - Premature Mortality Age-Adjusted Rate
   - Poverty Rate
   - Median Household Income
   - Bachelor's Degree or Higher Rate
   - Unemployment Rate

## Page 4: Modeling Summary

### Purpose

Show that non-disease indicators can predict county-level premature mortality.

### Visuals

1. Model performance cards
   - Linear Regression Test R²: 0.66
   - Random Forest Test R²: 0.72
   - Random Forest Test MAE: 42.01
   - Random Forest Test RMSE: 56.54

2. Feature importance bar chart
   - Poor Mental Health
   - Physical Inactivity
   - Uninsured
   - Poverty
   - Bachelor's Degree or Higher
   - Smoking
   - Median Household Income

3. Text box
   - “Poor mental health was the strongest non-disease warning signal in the model, but this does not prove causation. The broader pattern combines mental health, inactivity, healthcare access, poverty, education, smoking, and income.”

## Design Notes

- Keep the dashboard clean and serious.
- Use clear page titles.
- Avoid overclaiming causation.
- Label disease-burden indicators as context, not the main causal story.
- Prioritize readability over too many visuals.

## Final Portfolio Deliverables

- GitHub repository
- README with findings and charts
- Power BI-ready CSV
- Power BI dashboard file once built
- Optional screenshots exported from Power BI for GitHub
