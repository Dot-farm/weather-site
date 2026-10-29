# SkyCast Weather App

SkyCast is a static, browser-based weather dashboard. Its JavaScript is written to look up a city with the Open-Meteo geocoding API and request current conditions and a five-day forecast from the Open-Meteo forecast API. The page is designed to show temperature, apparent temperature, humidity, wind, pressure, condition icons, and daily high/low temperatures; it loads Lagos as the default city.

## Project files

- `index.html` — dashboard markup and initial sample content.
- `style.css` — responsive layout, visual styling, and animations.
- `script.js` — city lookup, API requests, weather-code labels, and forecast rendering.

The project uses plain HTML, CSS, and browser JavaScript; there is no package manifest, build configuration, or test suite in the repository. No install or build step is defined. Weather lookups require an internet connection to reach Open-Meteo.

## Current source limitation

The interactive behavior is not currently wired up successfully: `index.html` loads `script.js` synchronously in the document `<head>`, while the script immediately queries elements in the body. In addition, several selectors in `script.js` do not match the markup (including the search form and weather description fields). As a result, the search handler and initial weather load do not reliably run. Resolve these source mismatches before relying on the weather features.
