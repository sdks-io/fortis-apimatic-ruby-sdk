
# Response Payment Card Reader Token

*This model accepts additional fields of type Object.*

## Structure

`ResponsePaymentCardReaderToken`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type58`](../../doc/models/type-58.md) | Optional | - |
| `data` | [`Data17`](../../doc/models/data-17.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "PaymentCardReaderToken",
  "data": {
    "token": "token4",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

