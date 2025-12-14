# Contatt API Spec

## Create Contact

Endpoint : POST /api/contacts

Request Header :

- Authorization : token

Request Body :

```json
{
  "first_name": "John",
  "last_name": "Doe",
  "email": "text@example.test",
  "phone": "08123456789"
}
```

Response Body :

```json
{
  "data": {
    "id": 1,
    "first_name": "john",
    "last_name": "doe",
    "email": "text@example.test",
    "phone": "08123456789"
  }
}
```

## Get Contact

Endpoint : GET /api/contacts/{idContact}

Request Header :

- Authorization : token

Response Body :

```json
{
  "data": {
    "id": 1,
    "first_name": "john",
    "last_name": "doe",
    "email": "text@example.test",
    "phone": "08123456789"
  }
}
```

## Update Contact

Endpoint : PUT /api/contacts/{idContact}

Request Header :

- Authorization : token

Request Body :

```json
{
  "data": {
    "first_name": "john",
    "last_name": "doe",
    "email": "text@example.test",
    "phone": "08123456789"
  }
}
```

Response Body :

```json
{
  "data": {
    "id": 1,
    "first_name": "john",
    "last_name": "doe",
    "email": "text@example.test",
    "phone": "08123456789"
  }
}
```

## Remove Contact

Endpoint : DELETE /api/contacts/{idContact}

Request Header :

- Authorization : token

Response Body :

```json
{
  "data": true
}
```

## Search Contact

Endpoint : GET /api/contacts

Request Header :

- Authorization : token

Query Parameter :

- name : string, search first name & last name
- email : string, search email
- phone : string, search phone number
- page : number, default 1
- size : number, default 10

Response Body

```json
{
  "data": [
    {
      "id": 1,
      "first_name": "john",
      "last_name": "doe",
      "email": "text@example.test",
      "phone": "08123456789"
    },
    {
      "id": 2,
      "first_name": "samuel",
      "last_name": "doe",
      "email": "text2@example.test",
      "phone": "08123456789"
    }
  ],
  "paging": {
    "current_page": 1,
    "total_page": 10,
    "size": 10
  }
}
```
