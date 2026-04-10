
# Home Phone 2

*This model accepts additional fields of type Object.*

## Structure

`HomePhone2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cc` | `String` | Optional | Country Code of the phone<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `3` |
| `subscriber` | `String` | Optional | Subscriber section of the number<br><br>**Constraints**: *Maximum Length*: `15` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "cc": "cc2",
  "subscriber": "subscriber4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

