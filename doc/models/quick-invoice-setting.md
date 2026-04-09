
# Quick Invoice Setting

Quick Invoice Setting Information on `expand`

## Structure

`QuickInvoiceSetting`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location_api_id` | `String` | Optional | Location API ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `location_id` | `String` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `quick_invoice_template` | `String` | Optional | Quick Invoice Template<br><br>**Constraints**: *Maximum Length*: `5000` |
| `default_allow_partial_pay` | `TrueClass \| FalseClass` | Optional | Default Quick Invoice Allow Partial Pay |
| `default_notification_on_due_date` | `TrueClass \| FalseClass` | Optional | Default Quick Invoice Notification On Due Date |
| `default_notification_days_after_due_date` | `Float` | Optional | Default Quick Invoice Notification Days After Due Date<br><br>**Constraints**: `>= 0`, `<= 60` |
| `default_notification_days_before_due_date` | `Float` | Optional | Default Quick Invoice Notification Days Before Due Date<br><br>**Constraints**: `>= 0`, `<= 60` |
| `show_custom_fields` | `TrueClass \| FalseClass` | Optional | Show Custom Fields |
| `id` | `String` | Optional | Quick Invoice Settings ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Example (as JSON)

```json
{
  "location_api_id": "11e95f8ec39de8fbdb0a4f1a",
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "quick_invoice_template": "<html>Template<html>",
  "default_allow_partial_pay": true,
  "default_notification_on_due_date": true,
  "default_notification_days_after_due_date": 7,
  "default_notification_days_before_due_date": 3,
  "show_custom_fields": false,
  "id": "11e95f8ec39de8fbdb0a4f1a"
}
```

