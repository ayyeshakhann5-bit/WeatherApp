# 🌦️ Weather App using Python and PyQt5

A simple desktop Weather App built using **Python, PyQt5, and the OpenWeatherMap API**. This application allows users to enter a city name and retrieve its current weather information, including temperature, weather description, and a corresponding weather emoji.

## ✨ Features

- **City-Based Weather Search:** Enter a city name to get its current weather information.
- **Temperature Display:** Displays the temperature in Fahrenheit (°F).
- **Weather Description:** Shows a description of the current weather conditions.
- **Weather Emojis:** Displays emojis based on weather conditions, such as sunny, cloudy, rainy, snowy, and stormy.
- **Error Handling:** Handles common HTTP errors, connection errors, timeouts, and request exceptions.
- **Graphical User Interface:** Provides a simple and user-friendly desktop interface built with PyQt5.
- **Custom Styling:** Uses Qt Style Sheets (QSS) to customize fonts, text sizes, alignment, and input borders.

## 🛠️ Technologies Used

- **Python** — Core programming language.
- **PyQt5** — Desktop graphical user interface.
- **Requests** — Sends HTTP requests to the weather API.
- **OpenWeatherMap API** — Retrieves current weather data.
- **Qt Style Sheets (QSS)** — Styles the application interface.

## 📋 Prerequisites

Before running the application, ensure you have:

- Python 3.10 or later recommended.
- An active internet connection.
- An OpenWeatherMap API key.
- PyQt5 and Requests installed.

## ⚙️ Installation and Setup

### 1. Clone the repository

```bash
git clone <your-github-repository-url>
```

Navigate to the project directory:

```bash
cd <your-project-folder>
```

### 2. Create a virtual environment (optional but recommended)

```bash
python3 -m venv venv
```

Activate it on macOS or Linux:

```bash
source venv/bin/activate
```

### 3. Install dependencies

```bash
pip install PyQt5 requests
```

### 4. Configure your API key

1. Create an account on [OpenWeatherMap](https://openweathermap.org/api).
2. Generate an API key from your account.
3. Store your API key securely rather than hardcoding it in your source code.

For example, set an environment variable on macOS or Linux:

```bash
export OPENWEATHER_API_KEY="your_api_key_here"
```

Update your Python code to retrieve the key:

```python
import os

api = os.getenv("OPENWEATHER_API_KEY")
```

Use this value when constructing your API request.

**Important:** Never upload your real API key to GitHub. If the key in your current code is real, revoke or regenerate it before publishing your repository.

### 5. Run the application

Save your Python code as `weather_app.py` and run:

```bash
python weather_app.py
```

The Weather App window will open, allowing you to enter a city name and retrieve its weather information.

## 🖥️ How to Use

1. Launch the application.
2. Enter a city name in the input field.
3. Click the **Get Weather** button.
4. View the temperature, weather description, and corresponding emoji.
5. If the request fails, the application displays an appropriate error message.

## 🌤️ Weather Emoji Mapping

| Weather Condition | Emoji |
|---|---|
| Thunderstorm | ⛈️ |
| Drizzle | 🌦️ |
| Rain | 🌧️ |
| Snow | ❄️ |
| Atmosphere / Fog | 🌫️ |
| Clear Sky | ☀️ |
| Few Clouds | 🌤️ |
| Scattered Clouds | ⛅ |
| Broken Clouds | 🌥️ |
| Overcast Clouds | ☁️ |

## 🧩 Error Handling

The application handles several types of errors:

- **400 — Bad Request:** Checks the user input.
- **401 — Unauthorized:** Indicates an invalid or unauthorized API key.
- **403 — Forbidden:** Indicates access is denied.
- **404 — Not Found:** Indicates the requested city could not be found.
- **500 — Internal Server Error:** Indicates a server-side problem.
- **502, 503, 504:** Handles gateway and service availability issues.
- **Connection Error:** Indicates a possible internet connectivity problem.
- **Timeout Error:** Indicates the request took too long.
- **Request Error:** Handles other request-related exceptions.

## 📁 Project Structure

```text
Weather-App/
│
├── weather_app.py
├── README.md
└── .gitignore
```

## 📚 Concepts Learned

Building this project helped me practice:

- Creating desktop applications with PyQt5.
- Using widgets such as `QLabel`, `QLineEdit`, and `QPushButton`.
- Organizing widgets with `QVBoxLayout`.
- Connecting button clicks to functions using signals and slots.
- Fetching API data using the Requests library.
- Working with JSON responses and dictionaries.
- Handling HTTP errors and network exceptions.
- Applying conditional logic to map weather codes to emojis.
- Styling GUI components using Qt Style Sheets.

## 🚀 Future Improvements

- Display temperatures in Celsius and Fahrenheit.
- Show humidity, wind speed, and feels-like temperature.
- Add weather forecasts for upcoming days.
- Improve the interface with weather-based backgrounds.
- Add input validation and a loading indicator.
- Store API keys securely using environment variables.

## 👩‍💻 Author

**Ayesha Khan**

Python beginner project developed to practice GUI development, API integration, and exception handling.

---

⭐ If you find this project useful, consider giving the repository a star!
