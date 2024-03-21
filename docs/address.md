# Address API Spec

## Create Address API

Endpoint : POST /api/contacts/:contactId/addresses

Headers :
- Authorization : token

Request Body :

```json
{
    "street" : "Jln Kartini",
    "city" : "Jember",
    "province" : "East Jawa",
    "country" : "Indonesia",
    "postal_code" : "68177"
}
```

Response Body Success :

```json
{
    "data" : {
        "id" : 1,
        "street" : "Jln Kartini",
        "city" : "Jember",
        "province" : "East Jawa",
        "country" : "Indonesia",
        "postal_code" : "68177"
    }
}
```

Response Body Error :

```json
{
    "errors" : "Country is required"
}
```

## Update Address API

Endpoint : PUT /api/contacts/:contactId/addresses/:addressId

Headers :
- Authorization : token

Request Body :

```json
{
    "street" : "Jln Kartini",
    "city" : "Jember",
    "province" : "East Jawa",
    "country" : "Indonesia",
    "postal_code" : "68177"
}
```

Response Body Success :

```json
{
    "data" : {
        "id" : 1,
        "street" : "Jln Kartini",
        "city" : "Jember",
        "province" : "East Jawa",
        "country" : "Indonesia",
        "postal_code" : "68177"
    }
}
```

Response Body Error :

```json
{
    "errors" : "Country is required"
}
```

## Get Address API

Endpoint : GET /api/contacts/:contactId/address/:addressId

Headers :
- Authorization : token

Response Body Success :

```json
{
    "data" : {
        "id" : 1,
        "street" : "Jln Kartini",
        "city" : "Jember",
        "province" : "East Jawa",
        "country" : "Indonesia",
        "postal_code" : "68177"
    }
}
```

Response Body Error :

```json
{
    "errors" : "Contact is not found"
}
```

## List Addresses API

Endpoint : GET /api/contacts/:contactId/adresses

Headers :
- Authorization : token

Response Body Success :

```json
{
    "data" : [
        {
            "id" : 1,
            "street" : "Jln Kartini",
            "city" : "Jember",
            "province" : "East Jawa",
            "country" : "Indonesia",
            "postal_code" : "68177"
        },
        {
            "id" : 1,
            "street" : "Jln Kartini",
            "city" : "Jember",
            "province" : "East Jawa",
            "country" : "Indonesia",
            "postal_code" : "68177"
        }
    ],
    "paging" : {
        "page" : 1,
        "total_page" : 3,
        "total_item" : 30
    }
}
```

Response Body Error :

```json
{
    "errors" : "Contact is not found"
}
```

## Remove Address API

Endpoint : DELETE /api/contacts/:contactId/addresses/:addressId

Headers :
- Authorization : token

Response Body Success :

```json
{
    "data" : "OK"
}
```

Response Body Error :

```json
{
    "errors" : "Address is not found"
}
```