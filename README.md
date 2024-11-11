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
Enter the city name: London
```

#### Output:
```yaml
Welcome to the Weather Checker!
-------------------------------------------
This program shows you the current weather in any city.

Temperature: 12.34 °C
It feels like: 11.56 °C
Minimum Temperature: 10.00 °C
Maximum Temperature: 14.50 °C

Pressure: 1012 mBar
Humidity: 82%
Weather Condition: overcast clouds
Wind Speed: 3.45 kph

Sunrise: 06:30:00
Sunset: 18:15:00
Country Code: GB
```
## Note
To use this program, replace "e6d43eafcf69f246c6180b997c652ea7" with your own OpenWeatherMap API key.

## Contributing
Feel free to reach out or contribute to this project! Contributions, issues, and feature requests are welcome.
