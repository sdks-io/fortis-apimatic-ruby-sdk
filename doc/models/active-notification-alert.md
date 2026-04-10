
# Active Notification Alert

*This model accepts additional fields of type Object.*

## Structure

`ActiveNotificationAlert`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location_id` | `String` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `location_api_id` | `String` | Optional | Location Api ID |
| `date_start` | `String` | Optional | Date Start<br><br>**Constraints**: *Maximum Length*: `19`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}\s[\d]{2}:[\d]{2}:[\d]{2}$` |
| `date_end` | `String` | Optional | Date End<br><br>**Constraints**: *Maximum Length*: `19`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}\s[\d]{2}:[\d]{2}:[\d]{2}$` |
| `user_location` | `TrueClass \| FalseClass` | Optional | User Location |
| `user_contact` | `TrueClass \| FalseClass` | Optional | User Contact |
| `include_children` | `TrueClass \| FalseClass` | Optional | Include Children |
| `alert_type` | `Object` | Optional | - |
| `alert_type_id` | `Object` | Optional | - |
| `description` | `String` | Optional | Description<br><br>**Constraints**: *Maximum Length*: `32` |
| `alert_message` | `String` | Optional | Alert Message |
| `id` | `String` | Optional | Notification Alert ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `created_user_id` | `String` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `modified_user_id` | `String` | Optional | Last User ID that updated the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "date_start": "2021-12-01 10:10:00",
  "date_end": "2021-12-01 10:10:00",
  "user_location": true,
  "user_contact": true,
  "include_children": true,
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "location_api_id": "location_api_id4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

