# TraderJoe-Tract-Stat
Profiling Census Tracts of all the Trader Joe locations

## Data Sourcing and Wrangling
- https://www.traderjoes.com/pdf/locations/all-llocations.pdf
- Copy Pasta Text from PDF to Excel
- TextWrangler
   - Remove Trading Hours
   - Remove Alcohol
   - Find `\n\n` ; Replace with `\n`
   - Find `-([0-9][0-9][0-9][0-9])\n` ; Replace with `-\1\n~~`
   - Find `\n` ; Replace with `|`
   - Find `~~` . ; Replace with `\n`
   - Find `|` ; Replace with `\t`
- You should get a file with `CityName,Address`

- Use [Geocodio](https://geocod.io) and append `Census Features` to retrieve Census Tracts from Trader Joe (TJ) location addresses. [This file is here](https://github.com/vr00n/TraderJoe-Tract-Stat/blob/master/TJ_ALL_LOCS_ADDRESSES.csv)

Append Census Features to append Census geographies to your location data.
![image](https://user-images.githubusercontent.com/4397663/49687579-1227d580-fac2-11e8-9014-4b618946840b.png)


### Social Explorer
- Construct a [Social Explorer Report](https://www.socialexplorer.com/tables/ACS2016_5yr/R11954660) to gather census variables from Census. In this case I sourced from ACS 2016 (5-year estimates)
- The report will need to be pruned to preserve relevant columns.

### Merge Geocodio and Social Explorer
- Identify TJ census tracts in the Social explorer file by doing a vlookup

### [Final Data File](https://github.com/vr00n/TraderJoe-Tract-Stat/blob/master/SOCIAL_EXPLORER_CTs.csv.zip)

Use this File in your analysis.


## Links
- [Google Sheet](https://docs.google.com/spreadsheets/d/1Vwu_58574o6hsB2EnlQQTMPLKRllOOk-guxGMiRM9wA/edit?usp=sharing)
- [Twitter](https://twitter.com/vr00n/status/1071153899107684352)

## Measures used:
- % Total Population: White Alone
- % Total Population: Under 5 Years
- % Total Population: Two or More Races
- % Total Population: Some Other Race Alone
- % Total Population: Native Hawaiian and Other Pacific Islander Alone
- % Total Population: Male
- % Total Population: Female
- % Total Population: Black or African American Alone
- % Total Population: Asian Alone
- % Total Population: American Indian and Alaska Native Alone
- % Total Population: 85 Years and Over
- % Total Population: 75 to 84 Years
- % Total Population: 65 to 74 Years
- % Total Population: 55 to 64 Years
- % Total Population: 5 to 9 Years
- % Total Population: 45 to 54 Years
- % Total Population: 35 to 44 Years
- % Total Population: 25 to 34 Years
- % Total Population: 18 to 24 Years
- % Total Population: 15 to 17 Years
- % Total Population: 10 to 14 Years
- % Renter-Occupied Housing Units: Not Computed
- % Renter-Occupied Housing Units: Less than 10 Percent
- % Renter-Occupied Housing Units: 50 Percent or More
- % Renter-Occupied Housing Units: 30 to 49 Percent
- % Renter-Occupied Housing Units: 10 to 29 Percent
- % Population 25 Years and Over: Some College
- % Population 25 Years and Over: Professional School Degree
- % Population 25 Years and Over: Master's Degree
- % Population 25 Years and Over: Less than High School
- % Population 25 Years and Over: High School Graduate (Includes Equivalency)
- % Population 25 Years and Over: Doctorate Degree
- % Population 25 Years and Over: Bachelor's Degree
- % Households: Nonfamily Households: Female Householder
- % Households: Family Households: Other Family: Male Householder, No Wife Present
- % Households: Family Households: Other Family: Female Householder, No Husband Present
- % Households: Family Households: Other Family
- % Households: Family Households: Married-Couple Family
- % Households: Family Households
- % Civilian Population 18 Years and Over: Veteran: 65 Years and Over
- % Civilian Population 18 Years and Over: Veteran: 18 to 64 Years
- % Civilian Population 18 Years and Over: Veteran
- % Civilian Population 18 Years and Over: Nonveteran: 65 Years and Over
- % Civilian Population 18 Years and Over: Nonveteran: 18 to 64 Years
- % Civilian Population 18 Years and Over: Nonveteran
- % Households: Nonfamily Households: Male Householder
- % Households: Nonfamily Households
- % Total Population: White Alone
- % Total Population: Under 5 Years
- % Total Population: Two or More Races
- % Total Population: Some Other Race Alone
- % Total Population: Native Hawaiian and Other Pacific Islander Alone
- % Total Population: Male
- % Total Population: Female
- % Total Population: Black or African American Alone
- % Total Population: Asian Alone
- % Total Population: American Indian and Alaska Native Alone
- % Total Population: 85 Years and Over
- % Total Population: 75 to 84 Years
- % Total Population: 65 to 74 Years
- % Total Population: 55 to 64 Years
- % Total Population: 5 to 9 Years
- % Total Population: 45 to 54 Years
- % Total Population: 35 to 44 Years
- % Total Population: 25 to 34 Years
- % Total Population: 18 to 24 Years
- % Total Population: 15 to 17 Years
- % Total Population: 10 to 14 Years
- % Renter-Occupied Housing Units: Not Computed
- % Renter-Occupied Housing Units: Less than 10 Percent
- % Renter-Occupied Housing Units: 50 Percent or More
- % Renter-Occupied Housing Units: 30 to 49 Percent
- % Renter-Occupied Housing Units: 10 to 29 Percent
- % Population 25 Years and Over: Some College
- % Population 25 Years and Over: Professional School Degree
- % Population 25 Years and Over: Master's Degree
- % Population 25 Years and Over: Less than High School
- % Population 25 Years and Over: High School Graduate (Includes Equivalency)
- % Population 25 Years and Over: Doctorate Degree
- % Population 25 Years and Over: Bachelor's Degree
- % Households: Nonfamily Households: Female Householder
- % Households: Family Households: Other Family: Male Householder, No Wife Present
- % Households: Family Households: Other Family: Female Householder, No Husband Present
- % Households: Family Households: Other Family
- % Households: Family Households: Married-Couple Family
- % Households: Family Households
- % Civilian Population 18 Years and Over: Veteran: 65 Years and Over
- % Civilian Population 18 Years and Over: Veteran: 18 to 64 Years
- % Civilian Population 18 Years and Over: Veteran
- % Civilian Population 18 Years and Over: Nonveteran: 65 Years and Over
- % Civilian Population 18 Years and Over: Nonveteran: 18 to 64 Years
- % Civilian Population 18 Years and Over: Nonveteran
- % Households: Nonfamily Households: Male Householder
- % Households: Nonfamily Households

## Likely next Trader Joes locations


|  FIPS| Census Link |
|--|--|
| 14000US48453001602 | https://censusreporter.org/profiles/14000US48453001602-census-tract-1602-travis-tx/ | 
| 14000US53033004301 | https://censusreporter.org/profiles/14000US53033004301-census-tract-4301-king-wa/ | 
| 14000US25025010104 | https://censusreporter.org/profiles/14000US25025010104-census-tract-10104-suffolk-ma/ | 
| 14000US06059062610 | https://censusreporter.org/profiles/14000US06059062610-census-tract-62610-orange-ca/ | 
| 14000US36081071303 | https://censusreporter.org/profiles/14000US36081071303-census-tract-71303-queens-ny/ | 
| 14000US36081076901 | https://censusreporter.org/profiles/14000US36081076901-census-tract-76901-queens-ny/ | 
| 14000US42003140800 | https://censusreporter.org/profiles/14000US42003140800-census-tract-1408-allegheny-pa/ | 
| 14000US09009141900 | https://censusreporter.org/profiles/14000US09009141900-census-tract-1419-new-haven-ct/ | 
| 14000US26125197701 | https://censusreporter.org/profiles/14000US26125197701-census-tract-197701-oakland-mi/ | 
| 14000US06037214501 | https://censusreporter.org/profiles/14000US06037214501-census-tract-214501-los-angeles-ca/ |  | 
| 14000US06037264301 | https://censusreporter.org/profiles/14000US06037264301-census-tract-264301-los-angeles-ca/ | 
| 14000US06037267200 | https://censusreporter.org/profiles/14000US06037267200-census-tract-2672-los-angeles-ca/ | 
| 14000US06037267402 | https://censusreporter.org/profiles/14000US06037267402-census-tract-267402-los-angeles-ca/ | 
| 14000US06037275302 | https://censusreporter.org/profiles/14000US06037275302-census-tract-275302-los-angeles-ca/ | 
| 14000US17031281900 | https://censusreporter.org/profiles/14000US17031281900-census-tract-2819-cook-il/ | 
| 14000US06013338203 | https://censusreporter.org/profiles/14000US06013338203-census-tract-338203-contra-costa-ca/ | 
| 14000US25017353700 | https://censusreporter.org/profiles/14000US25017353700-census-tract-3537-middlesex-ma/ | 
| 14000US25017353800 | https://censusreporter.org/profiles/14000US25017353800-census-tract-3538-middlesex-ma/ | 
| 14000US25017382601 | https://censusreporter.org/profiles/14000US25017382601-census-tract-382601-middlesex-ma/ | 
| 14000US48201411502 | https://censusreporter.org/profiles/14000US48201411502-census-tract-411502-harris-tx/ | 
| 14000US06001421700 | https://censusreporter.org/profiles/14000US06001421700-census-tract-4217-alameda-ca/ | 
| 14000US06001421900 | https://censusreporter.org/profiles/14000US06001421900-census-tract-4219-alameda-ca/ | 
| 14000US48201431501 | https://censusreporter.org/profiles/14000US48201431501-census-tract-431501-harris-tx/ | 
| 14000US51059480202 | https://censusreporter.org/profiles/16000US5126496-fairfax-va/ | 
| 14000US17031810000 | https://censusreporter.org/profiles/14000US17031810000-census-tract-8100-cook-il/ | 
| 14000US17031832900 | https://censusreporter.org/profiles/14000US17031832900-census-tract-8329-cook-il/ |
