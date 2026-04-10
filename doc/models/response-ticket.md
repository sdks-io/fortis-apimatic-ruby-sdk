
# Response Ticket

*This model accepts additional fields of type Object.*

## Structure

`ResponseTicket`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type87`](../../doc/models/type-87.md) | Optional | - |
| `data` | [`Data24`](../../doc/models/data-24.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "Ticket",
  "data": {
    "account_holder_name": "account_holder_name0",
    "exp_date": "exp_date8",
    "cvv": "cvv8",
    "account_number": "account_number0",
    "billing_address": {
      "postal_code": "postal_code0",
      "street": "street8",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
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

