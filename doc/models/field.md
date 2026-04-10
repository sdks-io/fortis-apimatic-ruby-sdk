
# Field

*This model accepts additional fields of type Object.*

## Structure

`Field`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `field` | `String` | Optional | Field name used on the sort |
| `order` | [`Order`](../../doc/models/order.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "field": "last_name",
  "order": "asc",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

