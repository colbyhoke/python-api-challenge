# python-api-challenge

### Setup:
    * Each folder should have a config.py file
    * For WeatherPy, the config file should have a key for openweathermap API, set as: weather_api_key
    * For VacationPy, the config file should have a key for google places API, set as: g_key
## 2 parts:
1. WeatherPy
    * This Jupyter Notebook generates random latitude and longitude points, finds the nearest city to those points, then gather weather dat on those cities.
    * Data includes: max temperatures, humidity, cloudiness, and wind speed.
    * It then plots linear regression lines for each of those as they relate to latitude (northern vs southern hemisphere)
1. VacationPy
    * This Jupyter Notebook takes the cleaned CSV of citied from WeatherPy, 
<br>--------------------------------------------------------------------------------------------

## OBSERVATIONS

### WeatherPy
1. Caveat: Observations are based on the data pulled in the jupyter notebook on 7/15/20
1. Latitude vs. Temperature Plot:
    * This clearly shows that the temperatures increase, overall, the closer you get to the equator / 20 deg lat.
1. Latitude vs. Humidity Plot
    * It seems that, right now, humidity levels are high, no matter the latitude, with most of the cities at >60% humidity (as of 7/15/20).
    * Latitude seems to play a role in humidity levels, as you see them dip the further as they move away from the equator.
    * I believe those levels would be most impacted by other factors, like rainfall, latitude, and proximity to large bodies of water, perhaps.
1. Latitude vs. Cloudiness Plot
    * Latitude doens't seem to play much of a role at all in regrards to cloud cover.
1. Latitude vs. Wind Speed Plot
    * Latitude doesn't seem to play a role in regards to wind speed.
    * There is an outlier (as of 7/15/20) that could be tied to some weather events (storms)
1. Northern & Southern Hemisphere - Max Temp vs. Latitude Linear Regression
    * This shows a clear correlation between temp and latitude.
    * The closer you get to the equator the higher the temps.
1. Northern & Southern Hemisphere - Humidity (%) vs. Latitude Linear Regression
    * The data is somewhat grouped, though loosely, and shows some signs of humidity increasing the closer you are to the equator.
    * That is most likely impacted by # of datapoints/cities that are closer to the equator as well.
1. Northern & Southern Hemisphere - Cloudiness (%) vs. Latitude Linear Regression
    * With the linear regression, I'm not seeing much correlation between latitude and cloud cover when broken out to hemispheres.
    * The line for the northern hemisphere indicates theres some evidence that cloud cover increases a bit as you approach the equator, but the data is all over the place.
1. Northern & Southern Hemisphere - Wind Speed (mph) vs. Latitude Linear Regression
    * Seems that wind speeds increase more in the southern hemisphere as you approach the equator.
    * Wind speeds don't seem to be affected by latitude in the norther hemisphere.

### VacationPy
1. I set ideal conditions for city weather as:
    * A max temperature <= 85 degrees, but >= 70.
    * Humidity less <= 70%.
    * Less than 10% cloud cover.
    * Drop any rows that don't contain all three conditions. You want to be sure the weather is ideal.