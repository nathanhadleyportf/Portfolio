*Note: This is an original writing sample based on the public NASA API.  All content was independently written and structured to reflect professional API documentation standards.*

---

## Endpoint:
`GET https://api.nasa.gov/planetary/apod`  <br><br>

## Description:
Returns NASA’s Astronomy Photo of the Day (APOD) and accompanying metadata.<br><br>

## Authentication:
The DEMO_KEY is provided by NASA for public testing.  However, an API key is provided for free to public users.<br><br>


## Required Query Parameters:
| Name    | Type   | Description                                      |
|---------|--------|--------------------------------------------------|
| api_key | string | Your NASA API key. Alternatively, use `DEMO_KEY` for public access |

<br>

## Optional Query Parameters
| Name   | Type    | Description                                                  |
|--------|---------|--------------------------------------------------------------|
| date   | string  | Retrieve the APOD for a specific date (YYYY-MM-DD)          |
| hd     | boolean | Return high‑resolution image URL if available (true/false)   |
| thumbs | boolean | Return thumbnail if the media is a video (true/false)       |

<br>

## Request Headers

| Header      | Required | Description                             | Example              |
|-------------|----------|-----------------------------------------|----------------------|
| Accept      | No       | Desired response format (usually JSON)  | application/json     |
| User-Agent  | No       | Client identifier (optional)            | MyApp/1.0            |

<br>

## Important Response Headers

| Header              | Description                               | Example Value        |
|---------------------|-------------------------------------------|----------------------|
| Content-Type        | Format of the response                    | application/json     |
| X-RateLimit-Remaining | Remaining API calls in quota (if present) | 45                   |
| Cache-Control       | Caching policy                            | public, max-age=30   |

<br>

## Example Response:
```json
{
  "date": "2025-06-24",
  "explanation": "Is there a spiral galaxy in the center of this spiral galaxy…",
  "hdurl": "https://apod.nasa.gov/apod/image/2506/M61_HubbleEsoGendler_2753.jpg",
  "media_type": "image",
  "service_version": "v1",
  "title": "In the Center of Spiral Galaxy M61",
  "url": "https://apod.nasa.gov/apod/image/2506/M61_HubbleEsoGendler_960.jpg"
}
```
<br>

## Response Fields

| Field       | Type    | Description                                               |
|-------------|---------|-----------------------------------------------------------|
| copyright   | string  | Returns the owner of the copyright
| date        | string  | Date of the content (YYYY‑MM‑DD)                         |
| explanation | string  | Detailed description of the media                         |
| media_type  | string  | Indicates image or video                                  |
| title       | string  | Title of the APOD                                          |
| url         | string  | URL of the standard‑resolution media                      |
| hdurl       | string  | URL to the high‑resolution version (if available)         |

<br>

## Possible Errors

| Code | Message             | Cause                                           |
|------|---------------------|-------------------------------------------------|
| 400  | INVALID_DATE        | Malformed or out‑of‑range date.                 |
| 403  | API_KEY_INVALID     | Missing, expired, or mistyped API key.          |
| 429  | RATE_LIMIT_EXCEEDED | Exceeded the DEMO_KEY usage quota.              |

<br>

## Notes
- The DEMO_KEY is rate-limited to 30 requests/hour and 50 requests/day
- This endpoint supports educational and demo use.  For higher limits, get a free API key at api.nasa.gov
- When using thumbs=true, a thumbnail URL will be provided for video content
