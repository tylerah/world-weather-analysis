# Analysis of Weather Data Retrieved From OpenWeatherMap API
Click here to view the jupyter notebooks used to retrieve data from OpenWeatherMap: https://github.com/tylerah/world-weather-analysis/blob/main/WeatherPy.ipynb | https://github.com/tylerah/world-weather-analysis/blob/main/VacationPy.ipynb

## Purpose
The purpose of this project was to retrieve information from the OpenWeatherMap and Google Maps APIs in order to provide a simple weather summary of potential vacation destinations. Information pertaining to the weather of various locations was retrieved from the OpenWeatherMap API. This included data such as: latitude, longitude, maximim temperature, % humidity, % cloudiness, and wind speed. Information pertaining to hotels located near each destination was retrieved from Google APIs such as Google Maps and Google Places. The python scripts used to generate the weather information DataFrames and maps created in this project provide a framework for which the client can create a user facing app that can generate vacation suggestions based on the user's weather preferences. 

## Overview

### Analysis of Weather Data
Utilizing jupyter notebooks and pandas functionality, an API request was made to OpenWeatherMap in order to retrieve a basic summary of the weather at 2,000 random locations. The random locations were obtained by generating a list of random latitudes and longitudes which were then matched up to the nearest city using citipy funcitons. These cities were then used as part of the parameters in the API request.

The following is an example of the initial weather information DataFrame containing information retrieved from OpenWeatherMap:

![DataFrame screenshot](https://user-images.githubusercontent.com/104606662/174228761-64504c9a-74ba-46ed-bd77-69d44cf8b02a.png)

## Hotel Information

After this data was successfully retrieved, a request was made to the Google API in order to retrieve information on the nearest hotel to each city in the original DataFrame. The hotel name was added to the DataFrame.

The following is an example of the DataFrame after retriving information on hotels from Google:

![deliverable 2 dataframe](https://user-images.githubusercontent.com/104606662/174228983-b2e00b3a-a8c9-40df-9dce-40f6c8411d4a.png)

Using the information from these hotels, an example vacation itinerary was created using gmaps capabilities. A label was generated for all of the hotels in the previous DataFrame and placed in a marker layer to help visualize the hotel name and the city in which it was located alongside a basic description of the current weather. Another marker layer was created using directions retrieved from the Google API.

The following is an example of the marker layer:

![WeatherPy_travel_map_markers_1](https://user-images.githubusercontent.com/104606662/174229317-86226207-966f-4a23-9dbe-3b968de4eb09.png)

The following is an example of the travel layer:

![WeatherPy_travel_map](https://user-images.githubusercontent.com/104606662/174229309-5dafcade-0e2d-4aa1-93fe-70e12bfb4b77.png)
