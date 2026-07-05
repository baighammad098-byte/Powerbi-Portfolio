# Weather & Air Quality Dashboard — Power BI

A single-page Power BI dashboard displaying live-style current weather conditions, a multi-day forecast, and detailed air quality metrics for a selected location.

## 📊 Overview

This dashboard is built on weather API–style data (structured like WeatherAPI.com's JSON response) and presents current conditions, a short-term forecast, and a full air quality breakdown in one visually rich, icon-driven layout.

## 🗂️ Data Model

| Table | Role |
|---|---|
| `current` | Current weather snapshot — temperature, humidity, wind, UV, pressure, visibility, precipitation, condition text/icon, and nested air quality readings |
| `Forcast_day` | Multi-day forecast data (average temperature, day name) |
| `Locations` | Location metadata (name) used for filtering |
| `Measuress` | Dedicated measures table for DAX calculations |

## 📐 Key Fields & Measures

**Current conditions**
- `Curr_Temp_C`, `Wind_Speed`, `LAST_UPDATED_DATE_CURR`
- `current.humidity`, `current.uv`, `current.pressure_in`, `current.precip_in`, `current.vis_km`, `current.chance_of_rain`
- `current.condition.text` / `current.condition.icon`
- `Sunrise_data`, `Sunset_data`

**Forecast**
- `For_Temp_C`, `Day_name`, `forecast.forecastday.day.avgtemp_c`

**Air Quality Index (AQI) components**
- `current.air_quality.co` (Carbon Monoxide)
- `current.air_quality.no2` (Nitrogen Dioxide)
- `current.air_quality.o3` (Ozone)
- `current.air_quality.so2` (Sulfur Dioxide)
- `current.air_quality.pm2_5` / `current.air_quality.pm10` (Particulate Matter)
- `current.air_quality.us-epa-index` (overall EPA air quality index)

## 📈 Visuals

- KPI cards with custom icons for Humidity, Wind Speed, UV Index, Pressure, Precipitation, and Visibility
- Line chart for forecast temperature trend across days
- 100% stacked bar chart and donut chart for air quality composition
- Advanced slicers for filtering by location and forecast day
- Sunrise/sunset indicators and current condition iconography

## 🛠️ Tools Used

- **Power BI Desktop** — data modeling, DAX, report design
- Weather API–style JSON data source (current conditions, forecast, air quality)

## 🚀 How to Use

1. Download `weather.pbix` and open it in Power BI Desktop.
2. Refresh the data source or connect it to your own weather API data feed.
3. Use the location and day slicers to filter the dashboard.

## 👤 Author

Built by **Hammad** as part of a data analytics portfolio, exploring API-style JSON data modeling and icon-driven dashboard design in Power BI.
