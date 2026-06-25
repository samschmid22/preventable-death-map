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
