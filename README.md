# Weather Checker

A command-line C program that retrieves and displays comprehensive weather information for any city worldwide using the OpenWeatherMap API.

## 🌟 Features

- **Temperature Information**: Current temperature, feels-like temperature, minimum and maximum temperatures (in Celsius)
- **Atmospheric Data**: Air pressure (mBar) and humidity percentage
- **Weather Conditions**: Detailed weather description (e.g., clear sky, light rain, mist)
- **Wind Information**: Current wind speed in km/h
- **Sun Events**: Sunrise and sunset times (automatically adjusted for local timezone)
- **Location Details**: Country code identification
- **User-Friendly Interface**: Clean command-line interface with formatted output
- **Error Handling**: Validates city names and handles API errors gracefully

## 📋 Requirements

### Dependencies
- **C Compiler**: GCC or any standard C compiler
- **libcurl**: For making HTTP requests to the OpenWeatherMap API
- **cJSON**: For parsing JSON responses from the API

### Installation of Dependencies

#### Ubuntu/Debian:
```bash
sudo apt-get update
sudo apt-get install libcurl4-openssl-dev libcjson-dev
```

#### CentOS/RHEL/Fedora:
```bash
# For CentOS/RHEL
sudo yum install libcurl-devel cjson-devel

# For Fedora
sudo dnf install libcurl-devel cjson-devel
```

#### macOS (using Homebrew):
```bash
brew install curl cjson
```

## 🚀 Installation & Setup

1. **Clone the repository:**
```bash
git clone https://github.com/yourusername/weather-checker.git
cd weather-checker
```

2. **Get your OpenWeatherMap API Key:**
   - Visit [OpenWeatherMap](https://openweathermap.org/api)
   - Sign up for a free account
   - Generate your API key

3. **Update the API Key:**
   - Open `Weather.c` in your preferred text editor
   - Replace `YOUR_API_KEY` with your actual API key on line 128
   
4. **Compile the program:**
```bash
gcc -o weather Weather.c -lcurl -lcjson
```

## 💻 Usage

Run the compiled program:
```bash
./weather
```

Enter the city name when prompted:
```
Enter the city name: Delhi
```

## 📊 Example Output

```
             Welcome to the Weather Checker! 
------------------------------------------------------------
This program shows you the current weather in any city.

Enter the city name: Delhi

Temperature: 20.05 °C
It feels like: 20.41 °C
Minimum Temperature: 20.05 °C
Maximum Temperature: 20.05 °C

Pressure: 1014 mBar
Humidity: 88 %
Weather Condition: mist
Wind Speed: 2.57 kph

Sunrise: 06:41:40
Sunset: 17:29:05

Country Code: IN
```

## 🏗️ Code Structure

### Key Functions:
- `print_intro()`: Displays welcome message and program description
- `convertUnixTimestamp()`: Converts UNIX timestamps to readable time format with timezone adjustment
- `handle_data()`: Parses JSON response and extracts weather information
- `write_callback()`: Handles HTTP response data and validates city input

### API Integration:
- Uses OpenWeatherMap API v2.5
- Metric units for temperature and wind speed
- Automatic timezone adjustment for sunrise/sunset times

## 🔧 Troubleshooting

### Common Issues:

1. **"City Not Found" Error:**
   - Check spelling of the city name
   - Try entering just the city name without country/state
   - Some cities may require country code (e.g., "London,UK")

2. **Compilation Errors:**
   - Ensure libcurl and cjson libraries are installed
   - Check if pkg-config is available: `pkg-config --libs libcurl cjson`

3. **API Key Issues:**
   - Verify your API key is active (may take a few minutes after generation)
   - Ensure the API key is correctly placed in the code
   - Check API key usage limits

4. **Network Issues:**
   - Verify internet connectivity
   - Check if firewall is blocking HTTP requests

## 🌐 API Information

This program uses the OpenWeatherMap Current Weather Data API:
- **Endpoint**: `http://api.openweathermap.org/data/2.5/weather`
- **Rate Limit**: 1000 calls/day (free tier)
- **Data Update Frequency**: Every 10 minutes
- **Documentation**: [OpenWeatherMap API Docs](https://openweathermap.org/current)

## 🤝 Contributing

Contributions are welcome! Here's how you can help:

1. Fork the repository
2. Create a feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

### Ideas for Contributions:
- Add support for multiple cities at once
- Implement weather forecast (5-day forecast)
- Add support for different units (Fahrenheit, Imperial)
- Create a GUI version
- Add weather history functionality

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 Author

**Vatsal Jaiswal**
- GitHub: [@Vatsalj17](https://github.com/Vatsalj17)

## 🙏 Acknowledgments

- [OpenWeatherMap](https://openweathermap.org/) for providing the weather API
- [libcurl](https://curl.se/libcurl/) for HTTP client functionality
- [cJSON](https://github.com/DaveGamble/cJSON) for JSON parsing capabilities

---

⭐ If you found this project helpful, please give it a star!
