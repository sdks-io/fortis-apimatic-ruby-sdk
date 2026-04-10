
# Balance

*This model accepts additional fields of type Object.*

## Structure

`Balance`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `amount_type` | `String` | Optional | The type of amount balance |
| `account_type` | `String` | Optional | The type of account balance |
| `amount` | `Integer` | Optional | The amount of balance |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "amount": 1000,
  "amount_type": "amount_type4",
  "account_type": "account_type6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

