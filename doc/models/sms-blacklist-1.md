
# Sms Blacklist 1

*This model accepts additional fields of type Object.*

## Structure

`SmsBlacklist1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | Blacklist ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `is_blacklisted` | `TrueClass \| FalseClass` | Optional | isBlacklisted |
| `detail` | `TrueClass \| FalseClass` | Optional | Contact Id |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "isBlacklisted": true,
  "detail": true,
  "created_ts": 1422040992,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

