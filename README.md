# Dark Sky

<!-- API-EVANGELIST-PROVENANCE:BEGIN -->
> ### About this repository
>
> **This is not our API.** This repository is an independent, third-party profile of a company's
> **publicly available** API surface, maintained by [API Evangelist](https://apievangelist.com).
> API Evangelist does not operate, host, resell, or support this company's APIs, and is not
> affiliated with or endorsed by the company unless stated on the profile.
>
> **Where the information came from.** Everything here is assembled from material a member of the
> public can reach with a browser and no credentials — the company's own website, developer portal
> and documentation, the specifications it publishes for public use (OpenAPI, AsyncAPI, JSON Schema,
> `apis.json`, `llms.txt` and similar), its public repositories, and its public status, pricing and
> changelog pages. **Nothing here is obtained by breaching a system, defeating an access control, or
> using credentials of any kind.**
>
> **The rating is an independent assessment.** The Kin Score and Agent Readiness rating are
> independently calculated scores of a company's *public* API artifacts, produced by API Evangelist
> against a published rubric. They are not certifications, endorsements, security assessments, or
> audits, and they score published artifacts — not the quality, safety, or security of the software.
>
> **Corrections, re-scores, and removal are free.** No partnership, contract, or purchase is
> required, and you do not need to justify the request.
>
> - **Something wrong?** Open an issue on this repository, or email
>   [info@apievangelist.com](mailto:info@apievangelist.com).
> - **Published something new?** Ask for a re-score and we will re-run the rating.
> - **Want the listing taken down?** Say so and we will honor it. The profile is reduced to your
>   company name, a factual description, and a link to your own site, and the company is recorded as
>   **unrated** — never scored zero for having asked.
>
> **Response times.** Acknowledgement within **one business day**; removal or restriction within
> **two business days**; corrections and re-scores within **five business days**.
>
> **On a security or compliance team?** Email
> [info@apievangelist.com](mailto:info@apievangelist.com) with *security* in the subject line and
> you will get a person, not a form. We will tell you exactly which public URLs this profile was
> built from so your team can see the same surface we did, and we will take the listing down on
> request while you work through it.
>
> Full detail: **[Where this data comes from](https://apievangelist.com/about/where-our-data-comes-from)**
<!-- API-EVANGELIST-PROVENANCE:END -->

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
