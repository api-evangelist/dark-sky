# Dark Sky

Dark Sky was a hyperlocal weather forecast REST API that provided
minute-by-minute precipitation forecasts, hourly weather conditions,
and multi-day outlooks powered by machine-learning models.

The API delivered real-time and historical weather data for any
latitude and longitude worldwide, including current conditions,
60-minute minutely precipitation intensity, 48-hour hourly forecasts,
and 7-day daily summaries. Apple acquired Dark Sky in March 2020;
new developer signups closed immediately, and the API was permanently
shut down on March 31, 2023.

Apple's [WeatherKit](https://developer.apple.com/weatherkit/) REST API
is the successor service.

## Base URL

```
https://api.darksky.net/forecast/{api_key}/{latitude},{longitude}
```

## Key Endpoints

| Endpoint | Description |
|---|---|
| `GET /forecast/{key}/{lat},{lng}` | Current and forecast weather for a location |
| `GET /forecast/{key}/{lat},{lng},{time}` | Time Machine — historical or future conditions |

## Response Data Blocks

- **currently** — Present conditions at the requested location
- **minutely** — Minute-by-minute precipitation for the next 60 minutes
- **hourly** — Hourly weather data for the next 48 hours
- **daily** — Day-by-day summaries for the next 7 days
- **alerts** — Severe weather alerts from official sources
- **flags** — Metadata about the request

## Authentication

API key passed as a path segment: `/forecast/{api_key}/...`

## Links

- Developer docs: https://darksky.net/dev/docs
- GitHub org: https://github.com/darkskyapp
- Successor API: https://developer.apple.com/weatherkit/

## APIs.json

This repository contains an [APIs.json 0.19](https://apisjson.org) profile
describing the Dark Sky API for cataloging and discovery purposes.
