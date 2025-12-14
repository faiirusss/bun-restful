# USER API Spec

## Register User

Endpoint : POST /api/user/login

Request Body :

```json
{
  "username": "John Doe",
  "password": "password",
  "name": "johndoe"
}
```

Response Body (Success):

```json
{
  "data": {
    "username": "john doe",
    "name": "johndoe"
  }
}
```

Response Body (Failed):

```json
{
  "error": "username must not blank, ..."
}
```

## LoginUser

Endpoint : POST /api/user/login

Request Body :

```json
{
  "username": "john doe",
  "password": "password"
}
```

Response Body (Success):

```json
{
  "data": {
    "username": "john doe",
    "name": "johndoe",
    "token": "token"
  }
}
```

## Get User

Endpoint : GET /api/user/current

Request Header:

- Authorization : token

Response Body (Success):

```json
{
  "data": {
    "username": "fairus salimi",
    "name": "fairus"
  }
}
```

## Update User

Endpoint : PATCH /api/user/current

Request Header:

- Authorization : token

Request Body

```json
{
  "username": "optional",
  "password": "optional"
}
```

Response Body (Success):

```json
{
  "data": {
    "username": "fairus salimi",
    "name": "fairus"
  }
}
```

## Logout User

Endpoint : DELETE /api/user/current

Request Header:

- Authorization : token

Response Body (Success):

```json
{
  "data": true
}
```
