# Payment Card Reader Token

```ruby
payment_card_reader_token_controller = client.payment_card_reader_token
```

## Class Name

`PaymentCardReaderTokenController`


# Payment Card Reader Token Request

For initializing iPhone card readers for Apple Tap to Pay transactions

```ruby
def payment_card_reader_token_request(product_transaction_id)
```

## Parameters

| Parameter | Type | Tags | Description |
|  --- | --- | --- | --- |
| `product_transaction_id` | `String` | Query, Required | Product Transaction ID to be used to initialize the card reader<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Response Type

[`ResponsePaymentCardReaderToken`](../../doc/models/response-payment-card-reader-token.md)

## Example Usage

```ruby
product_transaction_id = '11e95f8ec39de8fbdb0a4f1a'

result = payment_card_reader_token_controller.payment_card_reader_token_request(product_transaction_id)
puts result
```

## Example Response *(as JSON)*

```json
{
  "type": "PaymentCardReaderToken",
  "data": {}
}
```

## Errors

| HTTP Status Code | Error Description | Exception Class |
|  --- | --- | --- |
| 401 | Unauthorized | [`Response401tokenException`](../../doc/models/response-401-token-exception.md) |

