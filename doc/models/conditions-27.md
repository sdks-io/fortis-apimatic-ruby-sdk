
# Conditions 27

*This model accepts additional fields of type Object.*

## Structure

`Conditions27`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `method` | [`Method`](../../doc/models/method.md) | Optional | - |
| `values` | [`Values99`](../../doc/models/values-99.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "method": "xor",
  "values": "previous_transaction_id",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

