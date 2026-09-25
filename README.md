# Weather App  

>> live working link ( https://whether-app-one-cyan.vercel.app/ )


A mobile-first weather app built with plain HTML, CSS and JavaScript. Search any city, or use your location, to see current conditions, an hourly outlook and a 7-day forecast. It has no build step, no dependencies and needs no API key.

**Live demo:** `https://USERNAME.github.io/weather-app/` (replace `USERNAME` with your GitHub username after enabling GitHub Pages)

## Features

- **City search** with suggestions as you type
- **Current location** weather with one tap
- **Current conditions:** temperature, feels-like, humidity, wind, pressure, UV index, sunrise and sunset
- **Next 24 hours** in a scrollable hourly strip
- **7-day forecast** with highs, lows and chance of rain
- **°C / °F toggle**
- **Themes:** Auto (follows the weather and time of day), Day, and Night (dark mode)
- **Phone-app layout:** fills the screen on mobile and appears as a phone-sized window on desktop
- **Installable:** can be added to your home screen when served over HTTP(S)
- **Remembers** your last city, unit and theme
- **Clear error messages** for unknown cities, denied location access and network problems

## Tech stack

- HTML5, CSS3 (custom properties, flexbox, grid)
- Vanilla JavaScript (ES6+, `fetch`, `async/await`)
- [Open-Meteo](https://open-meteo.com/) Forecast and Geocoding APIs (free, no API key)

## Getting started

 
### Install on your phone

- **Android (Chrome):** open the live link, then tap ⋮ → **Install app** or **Add to Home screen**.
- **iPhone (Safari):** open the live link, tap **Share**, then **Add to Home Screen**.

## How it works

| Function | What it does |
| --- | --- |
| `search()` | Finds cities using the Open-Meteo Geocoding API |
| `load()` | Fetches current, hourly and daily weather for a location |
| `render()` | Builds the page from the weather data |
| `applyTheme()` | Sets the Auto, Day or Night look and the status bar colour |

Weather codes returned by the API (WMO codes) are mapped to a description, an icon and a background theme in the `WMO` object at the top of the script.

## Project structure

```
weather-app/
├── index.html   # markup, styles and JavaScript in a single file
└── README.md
```

## Data source

Weather data is provided by [Open-Meteo](https://open-meteo.com/) under the CC BY 4.0 license. Open-Meteo's free tier is intended for non-commercial use.
