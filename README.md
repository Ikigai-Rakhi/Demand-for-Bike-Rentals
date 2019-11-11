# Demand-for-Bike-Rentals
Objective
This repo predicts the demand for rental bikes in the Washington DC area using Linear Regression and Random Forests in Python.

Background
Bike sharing systems are new generation of traditional bike rentals where whole process from membership, rental and return 
back has become automatic. Through these systems, user is able to easily rent a bike from a particular position and return 
back at another position. They are not only environment friendly but also play an important role in decongesting traffic and keeping healthy.
Bike-sharing rental process is highly correlated to the environmental and seasonal settings. For instance, weather conditions,
precipitation, day of week, season, hour of the day, etc. can affect the rental behaviors.
Therefore, it becomes important for cities to be able to predict demand for such bikes.

About the Dataset
The dataset is called 'bikesharing dataset' and has been acquired from UCI Machine Learning website.
It has two files:
  -hour.csv : bike sharing counts aggregated on hourly basis. Records: 17379 hours
	-day.csv - bike sharing counts aggregated on daily basis. Records: 731 days
  
 Attribute Information 
 Both hour.csv and day.csv have the following fields, except hr which is not available in day.csv
	- instant: record index
	- dteday : date
	- season : season (1:springer, 2:summer, 3:fall, 4:winter)
	- yr : year (0: 2011, 1:2012)
	- mnth : month ( 1 to 12)
	- hr : hour (0 to 23)
	- holiday : weather day is holiday or not (extracted from http://dchr.dc.gov/page/holiday-schedule)
	- weekday : day of the week
	- workingday : if day is neither weekend nor holiday is 1, otherwise is 0.
	+ weathersit : 
		- 1: Clear, Few clouds, Partly cloudy, Partly cloudy
		- 2: Mist + Cloudy, Mist + Broken clouds, Mist + Few clouds, Mist
		- 3: Light Snow, Light Rain + Thunderstorm + Scattered clouds, Light Rain + Scattered clouds
		- 4: Heavy Rain + Ice Pallets + Thunderstorm + Mist, Snow + Fog
	- temp : Normalized temperature in Celsius. The values are divided to 41 (max)
	- atemp: Normalized feeling temperature in Celsius. The values are divided to 50 (max)
	- hum: Normalized humidity. The values are divided to 100 (max)
	- windspeed: Normalized wind speed. The values are divided to 67 (max)
	- casual: count of casual users
	- registered: count of registered users
	- cnt: count of total rental bikes including both casual and registered

Methodology
In order to predict the demand, a linear regression would be used. The following approach was used:
1. Basic exploration and visualization of the dataset- check for normality, skewness, variable distribution and their relationship with each other.
2. Check for assumptions of regression
3. Test and remove outliers
4. Train with a basic linear regression
5. Run a linear regression using cross validation
6. Train the model using Ridge Regression for regularization
7. Train the model using Random Forest

Use different techniques to check which one performs best.
