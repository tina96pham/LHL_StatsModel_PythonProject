# Final-Project-Statistical-Modelling-with-Python

## Project/Goals
City of Montreal is the largest city in Quebec province of Canada. Montreal has been named as one of the most bike friendly city in North America by Copenhagen Index, with bike paths to encourage economical and ecological transportation. Bixi is the popular public self service bicycle sharing system in Montreal with station across the city. The purpose of the project is to explore data from the bike sharing system and examine their possible impact as a mean of transportation to support local lifestyles in Montreal. In the project the distribution of bike station across the city across different point of interests (POI) will be examined.
The technical for this project is to explore and utilize API get request extract data from different websites. Using Pandas to perform data 
## Process
### 1. Extract data
Data obtain by sending get request to citybik.es for bike station information, Foursquare for restaurant and bar data and Yelp for landmarks and recreation data.
a. citbik.es data provided the cordinate to retrieve POI information from Foursquare and YELP
b. Created a new dataframe with " Station Name, Number of bikes vailable, Latittude, Longitude" for analysis
### 2. Transform data
The data is loaded into Jupyter notebook and cleane. Json data from the for loop need to be parsed through a for loop. Json normalize is used to turn data into a dataframe with ```pandas```
The data is then merged together to create a new dataframe
### 3. Load data
Data is clean and load into an SQL database use SQL lite extension from Jyputer notebook.
A database of bike share was created with the table of station inside using ```sqlite3``` engine.
### 4. Analysis
Using seaborn and statsmodel libraries in python to then analyzed the data using descriptive statistics and visualizations.

## Results
There are 762 bike stations across the city of Montreal which more bike available around restaurant and bar than landmark and outdoor. 

## Challenges 
1. The bug in the for loop of the api request, for a beginner, this might be hard to catch since the request will return a sucessful response and it can still be transformed into a dataframe. There is a direpancies in the data for the bike stations and POI, 762 bike stations vs total 50 restaurants surrounded each bike stations across Montreal. If any data loading and transformation outside of the for loop, it only return the data from the most recent get request which yield the smaller amount of POI. A possible solution is to loop the transformation and paste it to a list.
2. Be careful when using a for loop, syntax and indentation matters. Create a QA code and test out the sucessful run of different components of the for loop before executing the for loop itself. 
2. There are limited API get request from Fourshares and YELP. A dictionary was created using latitude_longitude as a key to store each get request as a .json. The .json file can then be loaded into Jupyter notebook for dta cleaning and transformation.
3. The data is not cleaned with missing value which make it challenging to come up with a strategy to merge all three dataframes form Citybike, FOURSQUARES and YELP together.
4. Organization is the key in any project but it is a challenge to keep tab of the work as the project move along. It is very crucial to keep all the code organize. One of the common mistake is the utilization generic variables in the get request which can prompt a sucessfull request message but it could have belong to previous sucessfull request. Always remember, python only return the recent query of the variable and with all the generic naming can cause a problem debugging especially in Jupyter Notebook. A way to manage this challenge is add number at the end of each variable for each cell of Jupyter notebook to order and organize the code.
5. Debugging waste a large amount of time. Documentation is tedious and never fun however it is important for debugging. Include a short statement in each cell of the Jupyter Notebook will help to recall the logic behind the code and help when other debugging the code. 
## Future Goals
There is a limited of time available for this project and with the challenge of limited daily API request from YeLP API causing delay and lost of time in the project. 
1. With more time, more insights data can be produce with detailed parsing from Foursquare and Yelp to including latititude and longitude from each bike stations that the POI belong to from the get request. With Yelp provided rating for the location, corellation between location rating and bike available can help understand how the people of Montreal make use of Bixi. Structure data from foursquare and yelp with more data cleaning 
2. More time can be use on how to structure and organize data into the database. Information about food services avaible surrounding each ike station and tourist attraction area can be loaded into data with longitude and latitude of the bike station they belong to from the API can be utilize as the primary key to join with the station table.
3. Yelp data of restaurant and bar within 1000m fromm each bike station can be pull from the API and compare with data from Foursquare API. Data from Yelp provided with price which can help analyze the relationship of bike availability in area with high cost.
4. Better visualization will better deliver the insights from the data. Python library from Geopandas and folium can help create geographical visual to show the distribution of bike across the city.
The future foal for this project is to continue organize the data and produce insights from data. The possibilities to collect and implement historical data regarding the usage of the bike share system into the stats model will help to gain actionable insight to help improve bike share structure and create a model to promote biking as public transportation in other cities across Canada.


