# 🚴 Cyclistic NYC Bike Usage Case Study

## 📘 Project Overview
This project analyzes NYC Citi Bike usage trends from 2014–2015, focusing on user behavior, trip durations, and the impact of weather conditions. The analysis is done using BigQuery SQL and visualized in Tableau. The project was developed as part of the Google Business Intelligence Certificate.

## 🧾 Datasets Used
- **`citibike_trips`**: Public dataset containing NYC Citi Bike trip data from 2014–2015, available in Google BigQuery.
- **`gsod20*` (NOAA Weather Data)**: Provides daily weather measurements (temperature, wind speed, precipitation) from NYC’s Central Park station.
- **`geo_us_boundaries.zip_codes`**: Used to determine the ZIP codes for start and end stations via geospatial joins.
- **`Cyclistic_NYC.zipcode`**: Uploaded CSV file mapping ZIP codes to boroughs and neighborhoods.

## 🛠️ Tools & Skills Applied
- BigQuery SQL (JOINs, aggregations, date/time functions, filtering)
- Geospatial data handling with `ST_WITHIN`
- Outlier removal using ChatGPT (filtered trips longer than 180 minutes)
- Weather data integration
- Tableau (for visual storytelling and dashboards) Vizz available on https://public.tableau.com/app/profile/antoine.nassaux/viz/CyclisticNYC_17467880265840/TripCount
- Analytical thinking and data transformation

## 🧮 Key SQL Query Summary
One of the core queries enriches Citi Bike trip data by joining weather and ZIP code information. It:
- Aggregates trip durations into 10-minute bins
- Adds temperature, wind speed, and precipitation for the day of each trip
- Maps trip start/end coordinates to neighborhoods using geospatial joins
- Adjusts trip dates by +5 years for dashboard recency



A second query isolates **summer trips only**, adding weather context to analyze seasonal trends.

## 🧠 Challenges & Learnings
- Tableau's aggregation behavior inflated average trip durations (~25 min vs. 10–15 min in SQL), which may misrepresent reality. The Google course accepts this result, so I’ve aligned with their dataset for consistency.
- Used ChatGPT to revise SQL logic for better filtering and clarity.

