
# Postback Log

*This model accepts additional fields of type Object.*

## Structure

`PostbackLog`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `postback_status_id` | `Object` | Optional | - |
| `id` | `String` | Optional | Postback Log Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `postback_config_id` | `String` | Optional | Postback Config Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `changelog_id` | `String` | Optional | Changelog Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `http_verb` | `String` | Optional | Http Verb |
| `next_run_ts` | `Integer` | Optional | Next Run |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `model` | `String` | Optional | MOdel |
| `model_id` | `String` | Optional | Model Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
  "changelog_id": "11e95f8ec39de8fbdb0a4f1a",
  "next_run_ts": 1422040992,
  "created_ts": 1422040992,
  "model_id": "11e95f8ec39de8fbdb0a4f1a",
  "postback_status_id": {
    "key1": "val1",
    "key2": "val2"
  },
  "http_verb": "http_verb8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

