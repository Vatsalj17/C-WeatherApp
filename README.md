# Weather Checker
A simple C program that retrieves and displays the current weather information for a specified city using the OpenWeatherMap API.

## Features
  - Shows current temperature, feels-like temperature, minimum and maximum temperatures, pressure, and humidity.
  - Displays the general weather condition and wind speed.
  - Shows sunrise and sunset times (adjusted for local timezone) and the country code.

## Requirements
  - C Compiler (e.g., GCC)
  - libcurl for making HTTP requests
  - cJSON library for parsing JSON responses

## Usage
  - Enter the name of the city for which you want to check the weather.\

## Example
```bash
Enter the city name: Delhi
```

#### Output:
```yaml
Welcome to the Weather Checker!
-------------------------------------------
This program shows you the current weather in any city.

Temperature: 20.05 °C
It feels like: 20.41 °C
Minimum Tempreature: 20.05 °C
Maximum Tempreature: 20.05 °C

Pressure: 1014 mBar
Humidity: 88 %
Weather Condition: mist
Wind Speed: 2.57 kph

Sunrise: 06:41:40
Sunset: 17:29:05

Country Code: IN
```
## Note
To use this program, replace "e6d43eafcf69f246c6180b997c652ea7" with your own OpenWeatherMap API key.

## Contributing
Feel free to reach out or contribute to this project! Contributions, issues, and feature requests are welcome.
