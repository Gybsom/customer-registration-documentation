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

**Condition** : All required fields are filled and there is no account created for this customer.

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

Go to [Create Bank Account endpoint](/api-reference/POST-create-bank-account.md)

Or go back to [Introduction](/api-reference/introduction.md)