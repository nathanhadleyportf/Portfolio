
# Update a Post (JSONPlaceholder)
> **Note:** This is an original writing sample based on a public API. All content was independently written and structured to reflect professional API documentation standards.
---
## Endpoint

`PUT https://jsonplaceholder.typicode.com/posts/{id}`

<br>

## Description

This endpoint allows you to simulate a full update of an existing post. A PUT request will replace all properties of a post with the new values of the request body.

<br>

## Authentication

No authentication required. This is a publicly available testing API.

<br>

## Required Path Parameters

| Name | Type   | Description                     |
|------|--------|---------------------------------|
| id   | number | The ID of the post to update.   |

<br>

## Headers

| Header        | Value            | Description                             |
|---------------|------------------|-----------------------------------------|
| Content-Type  | application/json | Specifies JSON format for request       |

<br>

## Required Request Body Parameters (JSON)

| Name    | Type   | Description                           |
|---------|--------|---------------------------------------|
| id      | number | The ID of the post to update          |
| title   | string | Updated title of the post             |
| body    | string | Updated content of the post           |
| userID  | number | ID of the user who owns the post      |

<br>

## Example Request

```http
PUT https://jsonplaceholder.typicode.com/posts/5
Content-Type: application/json
```
<br>

## Request Body

```json
{
  "id": 5,
  "title": "Updated REST Documentation Guide",
  "body": "This PUT request fully replaces the content of the post with ID 5.",
  "userId": 7
}

<br>

## Example Response
```
{
  "id": 5,
  "title": "Updated REST Documentation Guide",
  "body": "This PUT request fully replaces the content of the post with ID 5.",
  "userId": 7
}
```
<br>

## Successful Response

| Code | Message | Description                             |
|------|---------|-----------------------------------------|
| 200  | OK      | Post successfully updated with new data |

<br>

## Possible Errors

| Code | Message            | Cause                                                        |
|------|--------------------|-------------------------------------------------------------|
| 400  | Bad Request        | Required field(s) are missing or JSON body is malformed     |
| 404  | Not Found          | No post exists with the provided `id`                       |
| 415  | Unsupported Media  | Content-type is not `application/json`                      |

<br>

## Notes
- This is intended to simulate a PUT call that replaces an entire resource.  To do so, all fields must be provided, even if unchanged.

