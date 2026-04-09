
# Filter By

## Structure

`FilterBy`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `key` | `String` | Required | Resource key to filter by |
| `operator` | [Operator1](../../doc/models/operator-1-enum.md) | Required | This is a container for one-of cases. |
| `value` | Float \| String \| TrueClass \| FalseClass | Required | This is a container for one-of cases. |

## Example (as JSON)

```json
{
  "key": "first_name",
  "operator": "<=",
  "value": "Fred"
}
```

