# [POST] Create Customer

Used to create a new customer account.

**URL** : `/customers`

**Method** : `POST`

**Auth required** : NO

**Body parameters**

```json
{
    "id": "[UUID - required]",
    "name": "[string - required]",
    "email": "[string]",
    "status": "[string - required - default blocked]"
}
```

**Data example**

```json
{
    "id": "c9a6acf9-6c2f-4dcd-b711-b926b32bbd1a",
    "name": "John Doe",
    "email": "john@example.com",
    "status": "blocked"
}
```

## Success Response

**Condition** : If everything is OK and an Account didn't exist for this Customer.

**Code** : `201 CREATED`

**Content example**

```json
{
    "id": "c9a6acf9-6c2f-4dcd-b711-b926b32bbd1a",
    "name": "John Doe",
    "email": "john@example.com",
    "status": "blocked"
}
```

## Error Responses

**Condition** : Required fields missing.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "name": [
        "This field is required."
    ]
}
```