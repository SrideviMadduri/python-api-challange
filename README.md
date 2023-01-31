# python-api-challange
This project  was to investigate and analyze different weather factors for 500+ cities around the world, and create varying visualizations, including maps, scatter plots and linear regressions. To perform this analysis, the following resources were used:

OpenweatherMap API - Used to collect weather data for cities around the world 

CitiPy - used to generate list of cities to be analyzed in this challenge

Google Places API - used for humidty map visualizations and finding nearest hotels to specified coordinates

# WeatherPy

First, a list of 500+ cities was generated using CitiPy. Next, weatherdata was collected using OpenWeatherMap's API. A print log of each city as it's being processed with the city number and city name can be seen in the jupyter notebook output. The list of cities used was exported to a csv and can be found in the output folder under WeatherPy.

# Visualizations
Scatter plots were generated to show the following relationships:

Temperature (F) vs. Latitude
Humidity (%) vs. Latitude
Cloudiness (%) vs. Latitude
Wind Speed (mph) vs. Latitude
These visualizations were exported and saved in the Output folder under WeatherPy.

From there, linear regression was run on each relationship, separating the data into Northern and Southern Hemispheres:

Northern Hemisphere - Temperature (F) vs. Latitude
Southern Hemisphere - Temperature (F) vs. Latitude
Northern Hemisphere - Humidity (%) vs. Latitude
Southern Hemisphere - Humidity (%) vs. Latitude
Northern Hemisphere - Cloudiness (%) vs. Latitude
Southern Hemisphere - Cloudiness (%) vs. Latitude
Northern Hemisphere - Wind Speed (mph) vs. Latitude
Southern Hemisphere - Wind Speed (mph) vs. Latitude
To create these linear regressions more efficiently, a function (linregress_func) was created.

Observations of trends are shown after each plot.

#VacationPy

First, a heat map was created that displays the humidity for every city from the WeatherPy challenge.

Next, the data from WeatherPy was filtered to include locations ideal for a vacation, specifically:

A max temperature lower than 80 degrees but higher than 70.
Wind speed less than 10 mph
Zero cloudiness
Humidity less than 80%
From this filtered data, the Google Places API was used to locate the first hotel for each city located within 5000m of the filtered data coordinates.

Finally, the hotels were plotted on the humidity heatmap with a pin, which contains the hotel name, city, and country.


API keys
In order to access OpenWeatherMap API and Google Places API, API keys were required. These were not uploaded to this repository, to keep them private. To run this code, the user would need to create a file entitled api_keys.py with the following format:

weather_api_key = "Your OpenWeatherMap API key here"

g_key = "Your Google Places API key here"
