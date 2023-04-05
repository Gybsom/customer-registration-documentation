# [POST] Activate Customer

Used to activate a new customer account.

**URL** : `/customers/{customer_id}/set_as_active`

**Method** : `POST`

**Auth required** : NO

**Path parameters**

```json
{
    "customer_id": "[UUID - required]",
}
```

**Body parameters**

```json
{
    "status": "[string - required - default active]",
}
```

**Data example**

```json
{
    "status": "active"
}
```

## Success Response

**Condition** : If everything is OK and an Account didn't exist for this Customer.

**Code** : `200 OK`

**Content example**

```json
{
    "id": "c9a6acf9-6c2f-4dcd-b711-b926b32bbd1a",
    "name": "John Doe",
    "email": "john@example.com",
    "status": "active"
}
```

## Error Responses

**Condition** : Invalid *customer_id*.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "message": [
        "The provided customer_id is invalid."
    ]
}
```