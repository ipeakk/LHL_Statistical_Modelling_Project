# Final-Project-Statistical-Modelling-with-Python

## Project/Goals

The objective of this project was to integrate bike station data with nearby POI data to explore potential relationships between bike availability and business characteristics.

### Bike Station Data:

Latitude and Longitude

Number of free bikes

Number of empty slots

### Business Information Data:

Distance from the bike station

Business names

Category

Ratings

Number of reviews

### Data was collected from the following sources:

CityBikes API for bike station data

Foursquare and Yelp APIs for business information

The purpose of combining these datasets was to analyze potential relationships between bike station usage and the characteristics of nearby businesses, such as business ratings, category, and popularity.

## Process
### Data Collection:

Selected Vancouver as the study area, given its dense network of bike stations and diverse business landscape.

Queried the CityBikes API to obtain data on bike station locations, the number of free bikes, and empty slots.

### Data Extraction from APIs:

Foursquare and Yelp APIs were used to extract business data based on the bike station coordinates.

Queried business data included name, category, rating, review count, and distance from bike stations.

### Data Consolidation:

The data obtained from the Foursquare and Yelp APIs was merged based on coordinates and business names.

The data was then merged with the bike station dataset based on latitude and longitude.

### Data Cleaning and Standardization:

Duplicates were removed based on coordinates and business names.

Missing values were addressed using mean imputation for numerical columns (e.g., ratings) and 'Unknown' for categorical columns.

Distance values were normalized for consistency.


### Data Visualization:

Data distribution was explored using boxplots, histograms, and scatter plots.

Visualizations helped in identifying potential relationships between business ratings, distances from bike stations, and bike availability.

### Model Building:

A simple linear regression model was built to analyze the relationship between business rating and bike availability (free bikes and empty slots).

A multivariate regression model was developed to examine the influence of business characteristics (rating, review count, category) on bike availability.

Model Evaluation and Interpretation:

The linear regression model showed a weak relationship between business ratings and bike availability, with an R-squared value of 0.004.

Including additional predictors such as business category and review count slightly improved the model, but the R-squared value remained low.

## Results

The data obtained from Foursquare and Yelp provided diverse business categories, but the overlap between both datasets was limited.

Distance from the bike station showed a weak correlation with business rating and review count.

The regression analysis revealed that business ratings had a statistically significant but weak negative relationship with empty slots.

Multivariate regression including distance, rating, popularity, and review count did not significantly improve the model's explanatory power.

## Challenges 
Data collection was constrained by API call limits, leading to incomplete data for some bike stations.

Combining data from multiple APIs required extensive data cleaning and standardization due to differences in category classifications.

Multicollinearity among features was observed, affecting the model's stability.

## Future Goals
Enhance data collection to cover more bike stations and reduce missing values.

Investigate the impact of other POI categories such as public transit and parks.


