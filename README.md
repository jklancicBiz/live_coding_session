# Weather Application

## Overview
Creating a simple BE service for the live coding session.

### Task
The goal of the application is a simple REST API integration. You have 2 tasks. The first task is to create an API that 
allows to store the weather location. Once you have this, your next task is to store hourly readings of temperatures for 
the chosen location. You are going to use the H2 in memory DB, which is already set up. As a requirement you need to save:
- the location
  - city/town name
  - country
  - latitude and longitude
- the creation date and time
- the temperature in Celsius and Fahrenheit
- the wind speed in km/h and mph
- the humidity in %

The application uses the OpenWeatherMap API to retrieve the weather data. The key can already be found in the `application.properties` file.
For testing purposes, you can use the following endpoint:
```
https://www.weatherapi.com/api-explorer.aspx
```

This should allow you to understand the weather API; how to use it and which information to pick. With that you should be 
able to tailor the service to the given requirements.

## Prerequisites
- Java 11 or higher
- Maven 3.6.0 or higher

## Configuration
The application requires an API key for accessing weather data. This key should be set in the `application.properties` file.

Example `application.properties`:
```
spring.application.name=weather
server.port=8080
weather.api.key=YOUR_API_KEY_HERE
```

## Running the Application

To run the application, execute the following command:

```
mvn spring-boot:run
```