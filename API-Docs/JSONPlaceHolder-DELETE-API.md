# Delete a Post (JSONPlaceholder)

>*Note:  This is an original writing sample based on a public API.  All content was independently written and structured to reflect professional API documentation standards.*

<br>

## Endpoint
`DELETE https://jsonplaceholder.typicode.com/posts/{id}`

<br>

## Description
This endpoint simulates the deletion of a post based on a given post ID. While the JSONPlaceholder API does not actually remove data on the server, it returns a successful response code (200 OK) to indicate that the request was received and accepted.

<br>

## Authentication

No authentication required.  This is a publicly available testing API.

<br>

## Required Path Parameters

| Name | Type | Description|
|------|-------|-----------|
| id | number | The ID of the post to delete.|

<br>

## Headers

| Header | Value  | Description|
|--------|--------|-----------|
|Content-Type | application/json | Typically included, even if no body is sent |

<br>

## Example Request
```http
DELETE https://jsonplaceholder.typicode.com/posts/10
Content-Type: application/json
```

<br>

## Example Response
{}

<br>

## Successful Response
| Code | Message  | Description|
|--------|--------|-----------|
|200 | OK | The post was deleted successfully.  JSONPlaceholder returns an empty body. |

<br>

## Possible Errors
| Code | Message  | Description|
|--------|--------|-----------|
|404 | Not Found | No post found with the provided id |
|400 | Bad request | Invalid id format (e.g. string instead of number) |

<br>
## Notes
- This is intended to simulate deletion; the post is not actually removed
