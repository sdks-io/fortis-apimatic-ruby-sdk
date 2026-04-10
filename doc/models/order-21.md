
# Order 21

*This model accepts additional fields of type Object.*

## Structure

`Order21`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `key` | `String` | Required | Resource key to order by. |
| `operator` | [`Operator`](../../doc/models/operator.md) | Required | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "key": "first_name",
  "operator": "asc",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

