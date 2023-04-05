# [POST] Create Bank Account

Used to create a new bank account, linked to a customer.

**URL** : `/bank_accounts`

**Method** : `POST`

**Auth required** : NO

**Body parameters**

```json
{
    "id": "[UUID - required]",
    "iban": "[string - required]",
    "bic": "[string]",
    "name": "[string - required]",
    "customer_id": "[string - required]"
}
```

**Data example**

```json
{
    "id": "df82cf4f-bfa1-45db-ad12-dbb1e5b29acf",
    "iban": "BR6092702067124540003214324C1",
    "bic": "ITAUBRSPXXX",
    "name": "Example Account",
    "customer_id": "c9a6acf9-6c2f-4dcd-b711-b926b32bbd1a"
}
```

## Success Response

**Condition** : All required fields are filled.

**Code** : `201 CREATED`

**Content example**

```json
{
    "id": "df82cf4f-bfa1-45db-ad12-dbb1e5b29acf",
    "iban": "BR6092702067124540003214324C1",
    "bic": "ITAUBRSPXXX",
    "name": "Example Account",
    "customer_id": "c9a6acf9-6c2f-4dcd-b711-b926b32bbd1a"
}
```

## Error Responses

**Condition** : Required fields missing.

**Code** : `400 BAD REQUEST`

**Content example**

```json
{
    "iban": [
        "This field is required."
    ]
}
```