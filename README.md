# World Weather Analysis

## Overview

PlanMyTrip, a top travel technology company, uses data to recommend ideal hotels anywhere in the world based on clients' weather preferences. To this end, Jack, the head of the analyses for a user-interface team, wants to collect and present data to beta testers based on their prefered travel criteria. The beta testers will then use input statements to filter the data to get recommendations on potential travel destinations and nearby hotels. 

## Resources

- Data sources:
    - WeatherPy_Database.csv
    - WeatherPy_vacation.csv
    
- Software:
    - Python 3.9.7
    - Jupyter Notebook 6.4.5
    - Pandas, citipy, Scipy, requests, gmaps, and numpy libraries and dependencies
    - OpenWeatheMap API and Directions API

## Purpose

1. Create a dataframe with 500 or more unique cities of the world and their weather data in real time by using OpenWeatherMap API. The JSON file from the API requests will then be parsed to create a dataframe with following information:

 - City and country
 - Latitude and longitude
 - Maximum temperature
 - Humidity
 - Cloudiness
 - Wind speed
 - Current weather description

2. Identify potential travel destinations and nearby hotels for each city and show these on a marker layer map with pop-up markers based on customers' weather preferences.

3. Finally, using the Google Maps Directions API, a travel itinerary between four nearby cities as well as a marker layer map has to be generated.

## Outputs

### Retrieve the Weather Data

Using OpenWeatherMap API, 747 unique cities were determined from 2000 randomly selected latitudes and longitudes. Then a dataframe was created based on the weather preferences retrieved for each city.

![City_weather_dataframe]()


### Create a Customer Travel Destinations Map

To get the preferred cities, a new dataframe was created with two input criteria - minimum and maximum temperature selected by customers. That dataframe was then cleaned by dropping the empty rows and null hotel entries. Marker layers map with pop-up markers were created for the remainder of the hotels.

Dataframe:

![Hotels_df]()

Travel destinations map:

![WeatherPy_vacation_map]()


### Create a Travel Itinerary Map

A travel itinerary map showing the route between four cities in a given country was created by using Directions API from the customer’s preffered travel destinations. Then, a marker layers map with a pop-up markers for each city on the itinerary was generated.

Travel itinerary map:

![WeatherPy_travel_map]()

Travel dstination map with markers:

![WeatherPy_travel_map_markers]()
