# Address API Spec

## Create Address

Endpoint : POST /api/contacts/{idContact}/addresses

Request Header :

- Authorization : token

Request Body :

```json
{
  "street": "street",
  "city": "city",
  "province": "province",
  "country": "country",
  "postal_code": "postal_code"
}
```

Response Body :

```json
{
  "data": {
    "id": 1,
    "street": "street",
    "city": "city",
    "province": "province",
    "country": "country",
    "postal_code": "postal_code"
  }
}
```

## Get Address

Endpoint : GET /api/contacts/{idContact}/addresses/{idAddress}

Request Header :

- Authorization : token

Response Body :

```json
{
  "data": {
    "id": 1,
    "street": "street",
    "city": "city",
    "province": "province",
    "country": "country",
    "postal_code": "postal_code"
  }
}
```

## Update Address

Endpoint : PUT /api/contact/{idContact}/addresses/{idAddress}

Request Header :

- Authorization : token

Request Body :

```json
{
  "street": "street",
  "city": "city",
  "province": "province",
  "country": "country",
  "postal_code": "postal_code"
}
```

Response Body :

```json
{
  "data": {
    "id": 1,
    "street": "street",
    "city": "city",
    "province": "province",
    "country": "country",
    "postal_code": "postal_code"
  }
}
```

## Remove Address

Endpoint : DELETE /api/contact/{idContact}/addresses/{idAddress}

Request Header :

- Authorization : token

Response Body :

```json
{
  "data": true
}
```

## List Address

Endpoint : DELETE /api/contact/{idContact}/addresses

Request Header :

- Authorization : token

Response Body :

```json
{
  "data": [
    {
      "id": 1,
      "street": "street",
      "city": "city",
      "province": "province",
      "country": "country",
      "postal_code": "postal_code"
    },
    {
      "id": 2,
      "street": "street",
      "city": "city",
      "province": "province",
      "country": "country",
      "postal_code": "postal_code"
    }
  ]
}
```
