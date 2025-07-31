>*Note:  This is an original writing sample based on the public Open Notify API. All content was independently written and structured to reflect professional API documentation standards.*

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
```http
GET  http://api.open-notify.org/iss-now.json
```
<br>

## Example Reponse

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

<br>

## Possible Errors
| Code | Message  | Description|
|--------|--------|-----------|
|400 | Not found | Invalid endpoint or mistyped URL |
|500 | Internal Server Error | Temporary issue with the Open Notify server

<br>

## Notes
- The ISS location is only updated once every second.  A single client should keep polling to about once every 5 seconds to reduce strain to the servers.

- Latitude and longitude return strings rather than floats.

