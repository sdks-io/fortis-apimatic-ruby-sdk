
# Item List 5

*This model accepts additional fields of type Object.*

## Structure

`ItemList5`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Optional | Item's Name, must be unique on the list<br><br>**Constraints**: *Maximum Length*: `100` |
| `amount` | `Integer` | Optional | Item's Amount<br><br>**Constraints**: `>= -999999999`, `<= 999999999` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "name": "Bread",
  "amount": 2015,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

