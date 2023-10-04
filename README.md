# python-api-challenge
module 6 assignment

# Weather Analysis
Within the WeatherPy directory, you'll find two Jupyter source files: WeatherPy.ipynb and VacationPy.ipynb. These files retrieve pertinent data from two API providers, namely OpenWeatherMap and Geoapify, for over 500 cities specified by desired coordinates. Additionally, there's a repository called "output_data," housing the images generated from WeatherPy.ipynb.


In these Jupyter source files, the Pandas library is employed to construct DataFrames for each dataset. Matplotlib is imported to generate a series of scatter plots based on various variables. The inclusion of Scipy and linregress facilitates statistical computations and the creation of linear regression lines for the data points. Furthermore, Citipy is imported to generate a list of cities along with their coordinates. The utilization of hvplot allows for interactive data visualization, while geoviews is imported to explore and visualize the data geographically.

# WeatherPy

## Temperature vs. Latitude

There is a fairly strong negative correlation between temperature and latitude with a correlation coefficient of -0.808964459543422 on Northern Hemisphere.


There is a relatively strong positive correlation between temperature and latitude with a correlation coefficient of 0.8101142957604677 on Southern Hemisphere.

## Humidity vs. Latitude

There is a relatively week positive correlation between humidity and latitude with a correlation coefficient of  0.10192241908390481 on Northern Hemisphere.

There is a relatively week positive correlation correlation between humidity and latitude with a correlation coefficient of 0.05210863473698021 on Southern Hemisphere.


## Cloudiness vs. Latitude

There is a weak positive correlation between cloudiness and latitude with a correlation coefficient of  0.07036916335427049 on Northern Hemisphere.

There is a relatively week positive correlation between cloudiness and latitude with a correlation coefficient of 0.05801508072658086 on Southern Hemisphere.

## Wind Speed vs. Latitude

There is a week coorrelation between wind speed and latitude with a correlation coefficient of 0.09750635616709692 on Northern Hemisphere.

There is a weak negative correlation between wind speed and latitude with a correlation coefficient of -0.05966272065711817 on Southern Hemisphere.


# VacationPy

Generate a city map showcasing a point for each city present in the city_data_df DataFrame, utilizing information from the output_data/cities.csv file. The size of each point corresponds to the humidity level of the respective city.

Filter cities based on specific criteria, eliminating any entries with null values. The criteria are as follows:

Maximum temperature lower than 27 degrees but higher than 21.
Cloudiness less than 3.
Wind speed less than 4.5 m/s.
Subsequently, generate a new DataFrame named hotel_df, comprising the columns: City, Country, Lat, Lng, Humidity, and Hotel Name. Utilize the Geoapify API to identify the initial hotel within a 10,000-meter radius of each city, appending the results to the hotel_df in a column labeled Hotel Name for each corresponding city.

Include the hotel name and the country as supplementary details in the hover message for each city on the hotel map.