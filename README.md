# WeatherTrip – Smart Travel Planner

A full-stack travel assistant that provides **real-time weather**, **nearby attractions**, and an intelligent **best-time-to-visit** recommendation for any city.

## Features

- 🌦️ Live weather data (OpenWeatherMap API)
- 📍 Nearby tourist attractions (Geoapify Places API)
- 🔐 JWT-based secure login & protected APIs
- 🧭 Trip recommendation based on weather patterns
- 💻 Responsive UI (HTML, CSS, JavaScript)
- ⚙️ REST API backend with Spring Boot

## Tech Stack

| Layer | Technologies |
|-------|-------------|
| **Backend** | Java, Spring Boot, Spring Security, JWT |
| **Frontend** | HTML, CSS, JavaScript (Fetch API) |
| **APIs** | OpenWeatherMap, Geoapify Places |
| **Tools** | Maven, Postman, GitHub |

## API Overview

| Method | Endpoint | Description |
|--------|----------|-------------|
| `GET`  | `/api/weather/{city}` | Fetch current weather |
| `GET`  | `/api/attractions/{city}` | Nearby places |
| `POST` | `/api/auth/register` | Register a user |
| `POST` | `/api/auth/login` | Login (returns JWT) |

## Project Structure

```
WeatherTrip-Smart-Travel-Planner-main/
├── backend/                 # Spring Boot REST API
│   ├── src/main/java/com/weathertrip/backend/
│   │   ├── controller/      # weather, attractions, auth, trip, user
│   │   ├── service/         # WeatherService, AttractionService, TripService
│   │   ├── security/        # JWT auth filter & util
│   │   ├── model/ repository/ dto/ config/
│   │   └── resources/       # application.properties, attractions.json
│   └── pom.xml
└── frontend/                # index.html, style.css, app.js
```

## Getting Started

### Prerequisites
- Java 17+, Maven 3.9+
- PostgreSQL
- API keys: [OpenWeatherMap](https://openweathermap.org/api) and [Geoapify](https://www.geoapify.com/)

### 1. Configure
Set your database and API keys via environment variables (see `application.properties`):

| Variable | Description |
|----------|-------------|
| `DB_URL` / `DB_USERNAME` / `DB_PASSWORD` | PostgreSQL connection |
| `GEOAPIFY_API_KEY` | Geoapify Places API key |
| `OPENWEATHER_API_KEY` | OpenWeatherMap API key |
| `JWT_SECRET` | Secret used to sign JWT tokens |

### 2. Run the backend
```bash
cd WeatherTrip-Smart-Travel-Planner-main/backend
mvn spring-boot:run
```

### 3. Open the frontend
Open `WeatherTrip-Smart-Travel-Planner-main/frontend/index.html` in your browser
(or serve it with any static server).

## Author

Prabhu Patil
