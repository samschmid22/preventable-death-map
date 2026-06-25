# Initial Findings

## Project Question

Which county-level health, behavioral, and socioeconomic indicators are most associated with premature mortality across U.S. counties?

## Data Used

This analysis combines:

- CDC WONDER 2015–2019 premature mortality data
- CDC PLACES 2020 health behavior and chronic disease estimates
- ACS 2019 county-level socioeconomic indicators

The main outcome variable is age-adjusted premature mortality rate for deaths under age 75.

## Key Finding 1: Health behavior and health-status indicators are strongly associated with premature mortality

The strongest non-disease health indicators were:

| Indicator | Correlation with Premature Mortality |
|---|---:|
| Poor Physical Health | 0.79 |
| Poor Mental Health | 0.78 |
| Physical Inactivity | 0.74 |
| Smoking | 0.74 |
| Insufficient Sleep | 0.64 |
| Obesity | 0.61 |

These results suggest that counties with worse reported health, higher smoking, and higher physical inactivity tend to have higher premature mortality.

## Key Finding 2: Socioeconomic disadvantage is strongly associated with premature mortality

The strongest socioeconomic relationships were:

| Indicator | Correlation with Premature Mortality |
|---|---:|
| Poverty Rate | 0.70 |
| Median Household Income | -0.68 |
| Bachelor's Degree or Higher | -0.60 |
| Unemployment Rate | 0.55 |

Counties with higher poverty and unemployment tend to have higher premature mortality. Counties with higher income and higher educational attainment tend to have lower premature mortality.

## Key Finding 3: Smoking and poverty both show strong county-level patterns

Smoking rate and poverty rate each show strong positive relationships with premature mortality across counties.

- Smoking vs. premature mortality correlation: 0.74
- Poverty vs. premature mortality correlation: 0.70

## Important Interpretation Note

This analysis shows county-level associations, not proof of individual-level causation.

Disease-burden indicators such as coronary heart disease, stroke, COPD, diabetes, and high blood pressure are strongly associated with premature mortality, but they are outcome-adjacent. For that reason, the main project story focuses more on actionable health behavior, health-status, and socioeconomic indicators.

## Current Conclusion

Premature mortality in U.S. counties appears strongly patterned by both health conditions and socioeconomic disadvantage. The strongest non-disease signals include poor physical health, poor mental health, physical inactivity, smoking, poverty, lower income, and lower educational attainment.

## Key Finding 4: Non-disease indicators can predict county premature mortality

A predictive modeling step tested whether non-disease indicators could estimate county-level premature mortality.

The model excluded disease-burden indicators such as coronary heart disease, stroke, COPD, diabetes, and high blood pressure to avoid an overly circular result.

| Model | Test R² | Test MAE | Test RMSE |
|---|---:|---:|---:|
| Linear Regression | 0.66 | 46.08 | 62.44 |
| Random Forest | 0.72 | 42.01 | 56.54 |

The Random Forest model performed better, explaining about 72% of test-set variation in county-level premature mortality.

## Key Finding 5: Poor mental health was the strongest non-disease model signal

In the Random Forest model, the strongest non-disease predictors were:

| Predictor | Random Forest Permutation Importance |
|---|---:|
| Poor Mental Health | 0.204 |
| Physical Inactivity | 0.054 |
| Uninsured | 0.036 |
| Poverty | 0.022 |
| Bachelor's Degree or Higher | 0.020 |
| Smoking | 0.019 |
| Median Household Income | 0.019 |

This suggests that premature mortality is tied to a broader county-level risk profile involving mental health, physical inactivity, healthcare access, poverty, education, smoking, and income.

## Modeling Interpretation Note

Feature importance does not prove causation. Poor mental health should be interpreted as the strongest non-disease warning signal in the model, not as proof that mental health alone causes premature mortality.
