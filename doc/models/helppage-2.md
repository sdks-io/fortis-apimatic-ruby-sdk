
# Helppage 2

Helppage Information on `expand`

*This model accepts additional fields of type Object.*

## Structure

`Helppage2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `user_type_code` | [`UserTypeCode`](../../doc/models/user-type-code.md) | Optional | - |
| `body` | `String` | Optional | Body<br><br>**Constraints**: *Maximum Length*: `65000` |
| `title` | `String` | Optional | Title<br><br>**Constraints**: *Maximum Length*: `255` |
| `id` | `String` | Optional | Help Page ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `created_user_id` | `String` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `modified_user_id` | `String` | Optional | Last User ID that updated the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "body": "Sample Body",
  "title": "Sample Title",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "user_type_code": 250,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

