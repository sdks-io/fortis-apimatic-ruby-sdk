# 3 DS Transactions

```ruby
m3_ds_transactions_controller = client.m3_ds_transactions
```

## Class Name

`M3DSTransactionsController`


# 3 DS Transactions Request

For getting results of successful 3DS authentication attempts

```ruby
def m3_ds_transactions_request(three_ds_server_trans_id,
                               product_transaction_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `three_ds_server_trans_id` | `String` | Template, Required | Universally unique transaction identifier assigned by the 3DS Server to identify a single transaction. |
| `product_transaction_id` | `String` | Query, Required | Product Transaction ID associated with this 3DS request<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Response Type

[`ResponseThreeDSTransaction`](../../doc/models/response-three-ds-transaction.md)

## Example Usage

```ruby
three_ds_server_trans_id = '516ef0bf-e510-4895-b0a8-c889f2eaf471'

product_transaction_id = '11e95f8ec39de8fbdb0a4f1a'

result = m3_ds_transactions_controller.m3_ds_transactions_request(
  three_ds_server_trans_id,
  product_transaction_id
)
puts result
```

## Example Response *(as JSON)*

```json
{
  "type": "ThreeDSTransaction",
  "data": {
    "three_ds_server_trans_id": "516ef0bf-e510-4895-b0a8-c889f2eaf471",
    "transaction_status": "Y",
    "ds_trans_id": "f25084f0-5b16-4c0a-ae5d-b24808a95e4b",
    "acs_trans_id": "d7c1ee99-9478-44a6-b1f2-391e29c6b340",
    "message_version": "2.2.0",
    "authentication_value": "MTIzNDU2Nzg5MDA5ODc2NTQzMjE=",
    "eci": "05"
  }
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401tokenException`](../../doc/models/response-401-token-exception.md) |

