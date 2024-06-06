# Tsunami Data Analysis
## Dataset Source
The NCEI/WDS Global Historical Tsunami Database, containing tsunami source information and runup data. This dataset includes information on locations where tsunami effects were observed.

## Dataset Columns
1. Year: The year the tsunami occurred.
2. Month: The month the tsunami occurred.
3. Tsunami Event Validity: Validity of the actual tsunami occurrence, rated from -1 (erroneous) to 4 (definite).
4. Tsunami Cause Code: The source of the tsunami, from 0 (unknown) to 11 (astronomical tide).
5. Deposits: Criteria commonly used to identify tsunami deposits.
6. Country: Country name where the tsunami occurred.
7. Location Name: The area along the coastline.
8. Number of Runups: Total number of locations along the coastline where the tsunami wave reached a maximum height above the normal sea level.
9. Earthquake Magnitude: Size or strength of the earthquake (Richter Scale).
10. Latitude and Longitude: The location where the tsunami originated.
11. Maximum Water Height: Maximum elevation above the normal sea level that a tsunami wave reached at a specific location.
12. Tsunami Intensity: Potential impact of a tsunami event, calculated using runups height.
13. Total Damage Description: Ranges from 0 (none) to 4 (extreme).
14. After 1900: A binary column indicating if the year is before (0) or after (1) 1900.

## Data Cleaning
The original dataset had 1433 rows and 47 columns, with many NaN values. After cleaning, the dataset was reduced to 280 rows and 15 columns.

## Statistical Analysis
1. Multiple Linear Regression: Examined the relationship between all variables (excluding Year, Month, Latitude, Longitude, and After 1900) and Tsunami Intensity. The model was significant with an R² of 18.65%, and significant variables were Deposits, Earthquake Magnitude, Maximum Water Height, and Total Damage Description.
2. Factor Analysis: Reduced data into factors:
 - Factor 1: Effects of Tsunami (Deposits, Number of Runups)
 - Factor 2: Timeline (Year, After 1900)
 - Factor 3: Tsunami Cause Code
 - Factor 4: Month, Tsunami Event Validity
 - Factor 5: Location (Latitude and Longitude)
The dataset was saved as Tsunami_Factors with 280 rows and 20 columns.
3. Multiple Linear Regression with Factors: Significant model with an R² of 55.42%. All factors had a significant impact on Tsunami Intensity except Maximum Water Height and Earthquake Magnitude, with Factor 1 having the highest impact.
4. Independent Sample t-test: Compared average Tsunami Intensity before and after 1900. The result showed no significant difference, implying no impact of climate change on tsunami intensity.

## How to open ctk file
Download SAS Studio to open the ctk files and view the analysis done on the dataset with selected options or code.
