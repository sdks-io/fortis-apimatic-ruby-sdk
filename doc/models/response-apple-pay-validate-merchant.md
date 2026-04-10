
# Response Apple Pay Validate Merchant

*This model accepts additional fields of type Object.*

## Structure

`ResponseApplePayValidateMerchant`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type136`](../../doc/models/type-136.md) | Optional | - |
| `data` | [`Data37`](../../doc/models/data-37.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "ApplePayValidateMerchant",
  "data": {
    "merchantSession": "merchantSession0",
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

