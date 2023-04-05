# Quick Start

To register your customers, create their bank accounts and activate them on the platform, execute the following steps.

## Create a Customer Account

The first step is to create an Customer Account, using the *Create Customer* endpoint.

```cURL
curl --location --request POST 'https://api.example.com/customers' \
--header 'Content-Type: application/json' \
--data-raw '{ 
    "id": "c9a6acf9-6c2f-4dcd-b711-b926b32bbd1a",
    "name": "John Doe",
    "email": "john@example.com",  
    "status": "blocked"
}'
```

To access a detailed version of the endpoint, [click here](/api-reference/POST-create-customer.md).

### IMPORTANT

Customer accounts are always created in a `blocked` state. After creating the Bank Account, do not forget to activate it using the [Activate Customer](/api-reference/POST-activate-customer.md) endpoint.

## Create a Bank Account

After creating the customer account, the next step is to create the Bank Account. For this, we will use the *Create Bank Account* endpoint.

```cURL
curl --location --request POST 'https://api.example.com/bank_accounts' \
--header 'Content-Type: application/json' \
--data-raw '{ 
    "id": "df82cf4f-bfa1-45db-ad12-dbb1e5b29acf",
    "iban": "BR6092702067124540003214324C1",
    "bic": "ITAUBRSPXXX",  
    "name": "Example Account",
    "customer_id": "c9a6acf9-6c2f-4dcd-b711-b926b32bbd1a"
}'
```

For more details about this endpoint, [click here](/api-reference/POST-create-customer.md).

## Activate your Customer

With the customer account and bank account created, we need to activate the customer account. For this, we will use the *Activate Customer* endpoint.

```cURL
curl --location --request POST 'https://api.example.com/customers/c9a6acf9-6c2f-4dcd-b711-b926b32bbd1a/set_as_active/' \
--header 'Content-Type: application/json' \
--data-raw '{ 
    "status": "active",
}'
```

To explore this endpoint, [click here](/api-reference/POST-activate-customer.md).

## Final Considerations

At the end of the steps, your client will be active and ready to transact on our platform. If you have any questions or problems with this integration, please [contact us](mailto:support@example.com).

Go to [API Reference section](/api-reference/introduction.md)

Or go back to [home](/README.md)