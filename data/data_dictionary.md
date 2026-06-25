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

## Processed Dataset: cdc_places_health_predictors_2020_clean.csv

This dataset contains selected county-level health behavior and chronic disease predictors from CDC PLACES 2020.

| Column | Description |
|---|---|
| county_fips | Five-digit county FIPS code |
| state | Two-letter state abbreviation |
| state_name | Full state name |
| county_name_places | County name from CDC PLACES |
| places_total_population_2020 | County population from CDC PLACES |
| uninsured_rate | Estimated percent of adults without health insurance |
| smoking_rate | Estimated percent of adults who currently smoke |
| obesity_rate | Estimated percent of adults with obesity |
| physical_inactivity_rate | Estimated percent of adults reporting no leisure-time physical activity |
| diabetes_rate | Estimated percent of adults with diabetes |
| high_blood_pressure_rate | Estimated percent of adults with high blood pressure |
| poor_physical_health_rate | Estimated percent of adults reporting poor physical health |
| poor_mental_health_rate | Estimated percent of adults reporting poor mental health |
| insufficient_sleep_rate | Estimated percent of adults reporting insufficient sleep |
| copd_rate | Estimated percent of adults with COPD |
| coronary_heart_disease_rate | Estimated percent of adults with coronary heart disease |
| stroke_rate | Estimated percent of adults with stroke |

## Processed Dataset: mortality_places_merged_2015_2020.csv

This dataset merges the 2015–2019 CDC WONDER premature mortality baseline with selected 2020 CDC PLACES health predictors by county FIPS.

## County FIPS Crosswalk Notes

Two counties required manual FIPS updates because of county name/FIPS changes between the mortality baseline period and the CDC PLACES 2020 file:

| Original FIPS | Original County Name | Updated FIPS | Updated County Name |
|---|---|---|---|
| 02270 | Wade Hampton Census Area, AK | 02158 | Kusilvak, AK |
| 46113 | Shannon County, SD | 46102 | Oglala Lakota, SD |

The merged mortality + PLACES dataset contains 3,132 rows and 0 missing CDC PLACES matches after applying this crosswalk.
