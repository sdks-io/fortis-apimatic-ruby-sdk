
# Filter By

*This model accepts additional fields of type Object.*

## Structure

`FilterBy`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `key` | `String` | Required | Resource key to filter by |
| `operator` | [Operator1](../../doc/models/operator-1.md) | Required | This is a container for one-of cases. |
| `value` | Float \| String \| TrueClass \| FalseClass | Required | This is a container for one-of cases. |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "key": "first_name",
  "operator": "<=",
  "value": "Fred",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

