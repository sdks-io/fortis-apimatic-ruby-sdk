
# Response Merchant Deposit

*This model accepts additional fields of type Object.*

## Structure

`ResponseMerchantDeposit`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type47`](../../doc/models/type-47.md) | Optional | - |
| `data` | [`Data14`](../../doc/models/data-14.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "MerchantDeposit",
  "data": {
    "id": "id0",
    "company_id": "company_id6",
    "merchant_id": "merchant_id0",
    "service": "service0",
    "deposit_types": [
      "deposit",
      "adjustment",
      "fee"
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

