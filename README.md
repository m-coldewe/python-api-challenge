# python-api-challenge
Python requests, APIs, and JSON traversals to answer a fundamental question: "What is the weather like as we approach the equator?"
Contains two projects: WeatherPy and VacatioinPy

# WeatherPy

## Overview

This project aims to visualize the weather of over 500 cities of varying distances from the equator. Utilizes matplotlib, pandas, numpy, scipy.stats, and citypy.

## Purpose

In order to learn more about the weather approaching the equator, I:
- generated a list of random cities
- used a for loop to query the OpenWeather API and pull key data for each city in the list
- created scatterplots to visualize the relationship between Latitude and Temperature, Latitude and Humidity, Latitude and Cloudiness, and Latitude and Wind Speed
- created scatterplots for the ssame relationships with the cities divided between northern and southern hemispheres
- defined a function to calculate the linear regressions and r-values to help clarify the above relationships

Tutor Geromino helped me troubleshoot my for loop, and also helped me flesh out my function. The date used represents the current weather data at the time the query was made.

## Result

### Latitude vs. Max Temp

![Lat_vs_Max_Temp_North](https://github.com/m-coldewe/python-api-challenge/assets/152045367/6546b88f-3e59-4a4b-bd49-67dd07495733)
![Lat_vs_Max_Temp_South](https://github.com/m-coldewe/python-api-challenge/assets/152045367/2eeae7c2-e159-482f-ad5c-19c225d8d81d)

- the northern hemisphere has a negative linear relationship while the southern hemisphere has a positive relationship, however, both have higher max temps as the latitude approaches 0.
- the relationship between max temp and latitude is stronger in the northern hemisphere, where the r-value is .8, compared to the southern hemisphere, where it's .6.

### Latitude vs. Humidity

![Lat_vs_Humidity_North](https://github.com/m-coldewe/python-api-challenge/assets/152045367/bb639076-1f8c-4080-ba2e-b5e675cda59c)
![Lat_vs_Humidity_South](https://github.com/m-coldewe/python-api-challenge/assets/152045367/bebdfa55-2f88-4306-afbf-72b9286c0e2e)


- both northern and southern linear regressions show a positive relationship, which means that humidity goes up the further a city is from the equator in the northern hemisphere, and goes down the futher a city is from the equartor in the southern hemisphere.
- neither the northern hemisphere nor the southern hemisphere, however, demonstrates a strong relationship between Latitude and Humidity with r-values of about .4 and .3, respectively.
- again, the correlation is stronger in the northern hemisphere than in the southern hemisphere.

### Latitude vs. Cloudiness

![Lat_vs_Cloudiness_North](https://github.com/m-coldewe/python-api-challenge/assets/152045367/b8b5ff93-473b-427e-8668-d00ee81aeff8)
![Lat_vs_Cloudiness_South](https://github.com/m-coldewe/python-api-challenge/assets/152045367/c1172c02-b3a5-46a7-822a-96feba7ef18e)


- both northern and southern hemisphere linear regressions again show a positive relationship, meaning that while cloudiness increases in the northern hemisphere the further a city is from the equator, in the southern hemisphere cloudiness increases in cities closer to the equator.
- neither the northern hemisphere nor the southern hemisphere demonstrates a strong relationship with r-values at approximately .25 and .24, respectively.

### Latitude vs. Wind Speed

![Lat_vs_Wind_Speed_North](https://github.com/m-coldewe/python-api-challenge/assets/152045367/510ad07d-d475-4ac5-b41b-d082d62c8195)
![Lat_vs_Wind_Speed_South](https://github.com/m-coldewe/python-api-challenge/assets/152045367/be213f4d-ad6f-48f1-b5b4-325a409dd53f)

- the majority of the cities in the northern hemisphere have wind speeds under 10 m/s in the northern hemisphere regardless of how far or near they are to the equator, with fairly even distribution, leading to a mostly flat linear regression.
- in the sourthern hemisphere, however, the linear regression shows a negative relationship where wind speed is lessens for cities as the latitude approaches the equator.
- the r-value for the northern hemisphere is .08 compared to the southern hemisphere of .37 shows that location in the southern hemisphere has a bigger impact on wind speed below the equator than it does for the northern hemisphere.

## Summary

With the except of Max Temperature, the weather around the equator does not appear to differ significantly from from other locations around the world at varying latitudes. Further analysis, using cumulative weather data for previous months or years, could yield different results, as it might allow the emergence of trends related to various seasons.  


# VacationPy

## Overview

The aim of this project is to aid in the planning of future vacations by selecting cities that meet preferred weather criteria. Utilizes hvplot, pandaas, requests.

## Purpose

- mapped city information gathered in WeatherPy from csv by humidity
- defined ideal weather conditions to narrow down the potential cities
- queried Geoapify API to find the closest hotel within 10,000 meters of the city's coordinates
- added the hotel name and country to the hover message for each location

## Result

Provide examples of the finished analysis such as graph.
Explain the results of the analysis.


## Summary
Conclusions of analysis and final words.

