
# User 4

*This model accepts additional fields of type Object.*

## Structure

`User4`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `username` | `String` | Optional | Username |
| `first_name` | `String` | Optional | First Name |
| `last_name` | `String` | Optional | Last Name |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "username": "email@domain.com",
  "first_name": "Bob",
  "last_name": "Fairview",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

