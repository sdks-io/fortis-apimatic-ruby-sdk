
# Response Merchant Details

*This model accepts additional fields of type Object.*

## Structure

`ResponseMerchantDetails`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type137`](../../doc/models/type-137.md) | Optional | - |
| `data` | [`Data38`](../../doc/models/data-38.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "MerchantDetails",
  "data": {
    "resultCode": false,
    "merchantID": "merchantID8",
    "applePay": false,
    "googlePay": false,
    "applePayDomains": [
      {
        "key1": "val1",
        "key2": "val2"
      }
    ],
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

