
# Joi 19

*This model accepts additional fields of type Object.*

## Structure

`Joi19`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `conditions` | [Conditions18](../../doc/models/conditions-18.md) \| [Conditions191](../../doc/models/conditions-191.md) \| [Conditions4](../../doc/models/conditions-4.md) \| [Conditions41](../../doc/models/conditions-41.md) \| [Conditions42](../../doc/models/conditions-42.md) \| [Conditions43](../../doc/models/conditions-43.md) \| nil | Optional | This is a container for any-of cases. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "conditions": {
    "method": "xor",
    "values": "account_number",
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

