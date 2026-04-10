
# Tip Percents 1

*This model accepts additional fields of type Object.*

## Structure

`TipPercents1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `percent_1` | `Integer` | Optional | field can only contain a value from 0 to 99, if 1 field is NULL, all fields must be null.<br><br>**Constraints**: `>= 0`, `<= 99` |
| `percent_2` | `Integer` | Optional | field can only contain a value from 0 to 99, if 1 field is NULL, all fields must be null.<br><br>**Constraints**: `>= 0`, `<= 99` |
| `percent_3` | `Integer` | Optional | field can only contain a value from 0 to 99, if 1 field is NULL, all fields must be null.<br><br>**Constraints**: `>= 0`, `<= 99` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "percent_1": 0,
  "percent_2": 2,
  "percent_3": 99,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

