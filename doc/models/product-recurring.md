
# Product Recurring

Product recurring array

## Structure

`ProductRecurring`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `title` | `String` | Optional | Title<br><br>**Constraints**: *Maximum Length*: `64` |
| `location_id` | `String` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `location_api_id` | `String` | Optional | Location Api ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `send_declined_notifications` | `TrueClass \| FalseClass` | Optional | Send Declined Notifications |
| `require_full_payment` | `TrueClass \| FalseClass` | Optional | Require Full Payment |
| `expire_notification_email_enable` | `TrueClass \| FalseClass` | Optional | Expire Notification Email Enable |
| `expire_notification_sms_enable` | `TrueClass \| FalseClass` | Optional | Expire Notification SMS Enable |
| `notification_days_default` | `Integer` | Optional | Notification Days Default<br><br>**Constraints**: `>= 0`, `<= 365` |
| `id` | `String` | Optional | Product Recurring Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `created_user_id` | `String` | Optional | Created User Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `modified_user_id` | `String` | Optional | Modified User Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Example (as JSON)

```json
{
  "title": "Fortispay RbYN6y",
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "location_api_id": "11e95f8ec39de8fbdb0a4f1a",
  "send_declined_notifications": true,
  "require_full_payment": true,
  "expire_notification_email_enable": true,
  "expire_notification_sms_enable": true,
  "notification_days_default": 1,
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a"
}
```

