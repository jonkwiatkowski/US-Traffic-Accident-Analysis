# Project 1 - Group 9
## Group 9

### Brandon Groenewold
### Jon Kwiatkowski
### Martin Vazquez
### Kim Price
 
Topic: **Accidents in the USA**

## Overview
Our project is to uncover patterns in traffic accidents across the US. We'll examine relationships between location and volume and severity of accidents; impact of disruptions to traffic flow to accident severity; effects of weather on traffic safety; and related questions, as the data admits. 

## Dataset: [US-Accidents: A Countrywide Traffic Accident Dataset](https://smoosavi.org/datasets/us_accidents)
### Size: 1.15 GB (282 MB when zipped)
    - Dataset originally contains 47 columns from 5 years of data
> Size restriction for GitHub uploads. A lot of potentially interesting data needed to be cut out of the study.

![Column breakdown1](/Resources/column_breakdown1.JPG)
![Column breakdown2](/Resources/column_breakdown2.JPG)

## Fields to pull from full dataset:
- Start Time - to grab year, in order to reduce to 2021
- Severity
- Latitude
- Longitude
- State
- Visibility
- Sunrise_Sunset
- Traffic Signal
- Crossing
- Stop
- Roundabout

## Data Analysis
> Alaska and Hawaii didn't report any traffic accident data for the year of 2021.
>
> Traffic volume wasn't included in the data set.
- Number and severity of accidents by location
    - Stacked (severity) Bar graph by state
    - Scatter Plot of accidents - makes shape of US
    - Heatmap
- Visibility
    - Scatter plot of Visibility vs # of accidents
    - Linear Regression
 > Visibility varied widely in terms of how it was reported.  In order to standardize, we eliminated 10 mi and above from the analysis as no impact.  Adjusted visibility values were calculated by rounding values under 1 mi up to the nearest quarter mile.
- Day vs night
    - Pie chart of # of accidents (or Bar Chart)
- Anomalies/disruptions to traffic flow
    - **Hypothesis:**  Traffic obstructions help to reduce the number of accidents
    - **Null Hypothesis:** Traffic obstructions have no effect on the number of accidents
    - Hypothesis Tests:
        - Stop
        - Roundabouts
        - Crossings
        - Bumps
        - Pie Chart of # of Accidents per disruption - (w/no disruption as 'None')
        - Stacked (Day/Night) Bar chart of # of accidents per disruption (w/no disruptions as 'None')

## Findings
- There were about 1.5 Million accidents reported in the US in 2021
- The three states with the highest recorded number of reported accidents were California, Florida, and Texas.
- The three states with the lowest recorded number of reported accidents were Maine, Vermont, and South Dakota.
- 64.62% of accidents happened during the day and only 35.38% happened at night. Although night driving is thought to be more dangerous, there is much more traffic during the day.
- 83.4% of all traffic accidents in 2021 were not near a traffic obstruction (signal, stop sign, roundabout, or crosswalk)
- Only 0.006% of accidents happened at a roundabout, 2% at a stopsign, 7.2% at a crosswalk, and 7.4% at a traffic signal.
- Using a Chi-squared hypothesis test, we were able to determine that fewer accidents occur near traffic obstruction, p-value near 0.
- The number of accidents vs visibility yielded a positive relationship. We have $r^2 \approx 0.5940$ which corresponds to a moderate fit.

## References
 - Moosavi, Sobhan, Mohammad Hossein Samavatian, Srinivasan Parthasarathy, and Rajiv Ramnath. “A Countrywide Traffic Accident Dataset.”, arXiv preprint arXiv:1906.05409 (2019).
 - Moosavi, Sobhan, Mohammad Hossein Samavatian, Srinivasan Parthasarathy, Radu Teodorescu, and Rajiv Ramnath. “Accident Risk Prediction based on Heterogeneous Sparse Data: New Dataset and Insights.” In proceedings of the 27th ACM SIGSPATIAL International Conference on Advances in Geographic Information Systems, ACM, 2019.
 - https://seaborn.pydata.org/index.html
 - https://libraries.io/pypi/gmaps
 - https://stackoverflow.com/questions/12897374/get-unique-values-from-a-list-in-python
 - https://pandas.pydata.org/docs/user_guide/index.html#user-guide
 - Dom LaBella
 - Nick Buller
 - Chris Howard
 - Colin Barquist

## Repository Files

### 1. ReadMe file
- Description and link to original datafile

### 2. _Reduced Dataset Notebook:_ 
- Shrink original dataset to around 90mb so it fits to GitHub by reducing to the columns needed for our analysis (see field list in DataSet section) and only data from 2021, as well as Data Cleaning

### 3. _Analysis Notebook:_  
- Data Analysis to answer questions
    - Statistical analysis
    - Graph creation
    - Heat Map/API
    
### 4. Final Written Analysis
- Key findings
- Data limitations and assumptions