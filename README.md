# Final Project Statistical Modelling with Python
This project is the Statistical Modeling Project for Lighthouse Labs Data Analytics Course. 

## Project/Goals
For this project, there were 4 main tasks.
- Connection to the City Bikes API to retrieve bike stations for a specific city.
- Connection to Foursquare and Yelp APIs to retrieve points of interests (POIs) around each bike station.
- Data Parsing, Joining and Exploration of the data retrieved via APIs to gain insights to aid in model building and prediction.
-  Model Building – creating a regression model that demonstrates a relationship between the number of bikes or bike usage and the POI characteristics for the location.

## Process
### City Selection: 
The City of Philadelphia was selected as my location of interest and API calls were made to request information about the bike stations - *Indego, Philly's official bike share program. Since the API call gives the bike station information for only a point in time, the data cannot give a robust picture of bike usage. To mitigate this in a small way, I checked for peak traffic times in Philly and used a random clock generator to select the time for the API call. Information was received for 233 bike stations.

### Points of Interest: 
A function was created and utilized to request for POI information from Yelp and Foursquare. POIs selected were the **distances of the nearest colleges/universities and fitness centers**. The Yelp request had to be made on separate days because of the daily call limits.

### Data Parsing & Exploration: 
Data obtained was parsed into DataFrames, cleaned and explored. Most of the variables were weakly correlated with the dependent variable – percentage usage; a heat map and pair plot were generated for visualization.

### Model Building: 
Linear and Logistic regression models were used to explore relationships, possibly predictive between the predictor/independent variables and the dependent variables – percent usage and usage category (high/low).

## Results
- The comparison between the APIs showed that the Yelp API had more complete data and more business-related data points including review counts, ratings, types of service etc.
- Regarding the regression models, while the models showed that fitness centers have some statistical significance in relation to bike usage, the independent variables accounted for only about 2% of the overall variability in bike usage, lending little credibility to the predictive strength of the models. For business decisions regarding new bike station openings, other variables and stronger models should be explored to determine POIs that could potentially increase bike usage.


## Challenges/Limitations 
- Daily limit of the Yelp APIS lengthened the processing of obtaining the needed information on POIs.
- Point in Time – The citybikes API only provides a data on bike usage for one point in time, it is in no way a robust picture of the actual bike usage at each station. Studying the trends in bike usage over different time periods (perhaps randomly selected or consistently monitored) would yield more accurate data from which predictions could be achieved.
- Unfamiliar Terrain – Having better knowledge of the city of Philadelphia would have enabled exploration of further insights such as comparison of high vs low socio-economic areas, school districts etc.
- Limited Time


## Future Goals
If I had more time, I would:
- Change approaches: retrieving data for the number of the POIs as well as the proximity to the bike stations.
- Explore other POIs such as senior centres/elder care facilities and their relationship to bike usage as well as the presence of parks around bike stations.
- Create a Time series exploring seasonality in bike usage.

