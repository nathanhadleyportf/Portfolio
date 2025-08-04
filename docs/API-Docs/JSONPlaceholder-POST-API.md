# Create a New Post (JSONPlaceholder)

> *Note: This is an original writing sample based on a public API. All content was independently written and structured to reflect professional API documentation standards.*

---

## Endpoint

`POST https://jsonplaceholder.typicode.com/posts`

<br>

## Description

This is a simulated endpoint that allows users to simulate the creation of a new blog post.

<br>

## Authentication

No authentication required. This is a publicly available testing API.

<br>

## Headers

| Header        | Value              | Description                              |
|---------------|--------------------|------------------------------------------|
| Content-Type  | application/json   | Specifies that the request body is JSON-formatted |

<br>

## Required Request Body Parameters (JSON)

| Name    | Type    | Description                    |
|---------|---------|--------------------------------|
| title   | string  | Title of the blog post         |
| body    | string  | The content of the post        |
| userID  | number  | The ID of the post’s author    |

<br>

## Example Request

```http
POST https://jsonplaceholder.typicode.com/posts
Content-Type: application/json
```

<br>

## Request Body
```
{
  "title": "Example of a POST endpoint",
  "body": "This example demonstrates how to create a post using a POST request.",
  "userId": 7,
  "id": 101
}
```

<br>

## Example Response

```
{
  "title": "Example of a POST endpoint",
  "body": "This example demonstrates how to create a post using a POST request.",
  "userId": 7,
  "id": 101
}
```

<br>

## Successful Response

| Code | Message | Description                                                   |
|------|---------|---------------------------------------------------------------|
| 201  | Created | The post was successfully created. A fictitious id:101 is returned. |

<br>

## Possible Errors

| Code | Message            | Description                                        |
|------|--------------------|----------------------------------------------------|
| 400  | Bad Request        | JSON body is missing required fields or is malformed |
| 415  | Unsupported Media  | Content-type is not set to application/json          |

<br>

## **Notes**
* This is a mock API, and no post is actually created
* The returned id is always 101, regardless of the input
