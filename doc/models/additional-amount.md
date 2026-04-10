
# Additional Amount

*This model accepts additional fields of type Object.*

## Structure

`AdditionalAmount`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | `Object` | Optional | - |
| `amount` | `Integer` | Optional | The amount of additional amount. |
| `account_type` | `Object` | Optional | - |
| `currency` | `Float` | Optional | Currency Code |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "amount": 10,
  "currency": 840.0,
  "type": {
    "key1": "val1",
    "key2": "val2"
  },
  "account_type": {
    "key1": "val1",
    "key2": "val2"
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

