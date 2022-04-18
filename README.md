# openweather_api_php

### This repository is to get weather data using city name or country name.

### Initial Setup
- Install **Apache server with PHP 8.0** or later
   - In windows
     - https://www.apachefriends.org/download.html


   - In Linux
     - https://www.apachefriends.org/download.html


- Copy project folder into /var/www/html 
  - it is just the default root folder of the web server

#HTML Code to Show Weather Forecasts

HTML code is used to display the weather forecast by decoding the JSON object response. In this section, we access the location, weather description, icon, min-max ranges of the temperature, humidity and wind speed.

#POSTMAN Setup
postman_collection file is included for import

    postman_collection.json

# Development environment set up

###Build from root
```bash
docker-compose -f docker-compose.yml build
```
###Run the container
```bash
docker-compose -f docker-compose.yml up -d
```
Weather API will be available at http://localhost:8800/

## Execution
###SET YOUR API KEY HERE
   
    function getWeatherReport($city){
        $api_key = "SET YOUR API KEY HERE";
    }
- Access GUI application through following link
  - http://localhost:8800/index.php?city={CityName}


## Goals

### What?
- PHP application to display weather forecast information using an API. I have used OpenWeatherMap service to implement this with PHP. We will just grab the weather information provided by the API and display it in the application.
### Why?
- This is one of the best API service that provides weather forecast. It provides tremendous volume of weather data regularly. It is a free service with limited access. For basic usage, it should be sufficient.
### How?
- The following three steps are used for the integration.
  - Get API key
  - Locate city id
  - Request weather forecast by sending API key and city id

##Get OpenWeatherMap API key
- To get the API key, we need to register with OpenWeatherMap. After signing up, it will redirect us to the profile settings.
  - http://openweathermap.org/
- Above the profile settings form, there is a top menu containing several tabs. Click the API keys tab and copy the API key. This will be later used to request API for the weather forecasts.