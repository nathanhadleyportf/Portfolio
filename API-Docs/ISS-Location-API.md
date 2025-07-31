*Note:  This is an original writing sample based on the public Open Notify API. All content was independently written and structured to reflect professional API documentation standards.*

---

## Endpoint

`GET http://api.open-notify.org/iss-now.json`

<br>

## Description

Returns real-time latitude and longitude coordinates of the ISS.

<br>

## Authentication

No authentication is required – this is a public API.

<br>

## Request Parameters

_None_

<br>

## Example Request

```json
{
  "message": "success",
  "timestamp": 1750789753,
  "iss_position": {
    "longitude": "-112.0920",
    "latitude": "13.6829"
  }
}
```

<br>

## Response Fields

| Field        | Type    | Description                                                    |
|--------------|---------|----------------------------------------------------------------|
| `message`    | string  | Status of the response (e.g. “success” or “failure”)           |
| `timestamp`  | int     | Time the data was retrieved (UNIX epoch format)                |
| `iss_position` | object | Object containing latitude and longitude fields                |
| `latitude`   | string  | Latitude of the ISS                                            |
| `longitude`  | string  | Longitude of the ISS                                           |
