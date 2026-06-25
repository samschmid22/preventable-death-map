# Data Dictionary

## Processed Dataset: baseline_premature_mortality_2015_2019_clean.csv

This dataset contains county-level premature mortality data from CDC WONDER for the 2015–2019 pre-COVID baseline period.

| Column | Description |
|---|---|
| county_fips | Five-digit county FIPS code used to merge county-level datasets |
| county | County name and state abbreviation |
| state | Two-letter state abbreviation |
| premature_deaths_2015_2019 | Number of deaths under age 75 from 2015–2019 |
| population_2015_2019 | Population denominator for the selected under-75 age groups across 2015–2019 |
| premature_mortality_crude_rate_2015_2019 | Crude premature mortality rate per 100,000 residents |
| crude_rate_unreliable_2015_2019 | TRUE if CDC WONDER marked the crude rate as unreliable |
| premature_mortality_age_adjusted_rate_2015_2019 | Age-adjusted premature mortality rate per 100,000 residents |
| age_adjusted_rate_unreliable_2015_2019 | TRUE if CDC WONDER marked the age-adjusted rate as unreliable |

## Notes

- The primary project outcome will likely use the age-adjusted premature mortality rate.
- Counties with unreliable rates are retained but flagged.
- Missing rate values correspond to counties where CDC WONDER marked the rate as unreliable.
- The dataset contains 3,132 county rows after removing non-county/footer rows from the raw CDC WONDER export.
