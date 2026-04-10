
# Contact 13

*This model accepts additional fields of type Object.*

## Structure

`Contact13`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `first_name` | `String` | Optional | Contact's first name.<br><br>**Constraints**: *Maximum Length*: `20` |
| `last_name` | `String` | Optional | Contact's last name.<br><br>**Constraints**: *Maximum Length*: `20` |
| `email` | `String` | Optional | Contact's email address.<br><br>**Constraints**: *Maximum Length*: `100` |
| `phone_number` | `String` | Required | Contact's phone.<br><br>**Constraints**: *Maximum Length*: `20` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "first_name": "Jeffery",
  "last_name": "Todd",
  "email": "jtodd@example.com",
  "phone_number": "555-555-3456",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

