# Users

## The user object

```json
{
  "id": 112,
  "name": "Juliet Burke",
  "emails": [
    "juliet.burke@example.com",
     "other.woman@example.com"
  ],
  "disabled": false,
  "site_admin": true
}
```

| Attribute | Description |
|-----------|-------------|
| id | The user's unique identifier |

## List users

```shell
curl 'https://harvest.greenhouse.io/v1/users' \
-H "Authorization: Basic MGQwMzFkODIyN2VhZmE2MWRjMzc1YTZjMmUwNjdlMjQ6"
```

```json
[
  {
    "id": 112,
    "name": "Juliet Burke",
    "emails": [
      "juliet.burke@example.com",
       "other.woman@example.com"
    ],
    "disabled": false,
    "site_admin": true
  },
  {
    "id": 712,
    "name": "Mr. Eko",
    "emails": [
      "mr.eko@example.com"
    ],
    "disabled": true,
    "site_admin": false
  }
]
```

List all of an organization's Greenhouse users.

### HTTP Request

`GET https://harvest.greenhouse.io/v1/users`

### Optional querystring parameters

| Parameter | Description |
|-----------|-------------|
| per_page | Return up to this number of objects per response.  Must be an integer between 1 and 100.  Defaults to 100.
| page | A cursor for use in pagination.  Returns the n-th chunk of `per_page` objects.

## Retrieve a user 

```shell
curl 'https://harvest.greenhouse.io/v1/users/{id}' \
-H "Authorization: Basic MGQwMzFkODIyN2VhZmE2MWRjMzc1YTZjMmUwNjdlMjQ6"
```

```json
{
  "id": 112,
  "name": "Juliet Burke",
  "emails": [
    "juliet.burke@example.com",
     "other.woman@example.com"
  ],
  "disabled": false,
  "site_admin": true
}
```

### HTTP Request

`GET https://harvest.greenhouse.io/v1/users/{id}`

### URL Parameters

Parameter | Description
--------- | -----------
id | The ID of the user to retrieve