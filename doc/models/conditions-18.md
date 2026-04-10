
# Conditions 18

*This model accepts additional fields of type Object.*

## Structure

`Conditions18`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `method` | [`Method`](../../doc/models/method.md) | Optional | - |
| `values` | [`Values50`](../../doc/models/values-50.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "method": "xor",
  "values": "account_number",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

