
# Payment Recurring Notification

Payment Recurring Notification Information on `expand`

*This model accepts additional fields of type Object.*

## Structure

`PaymentRecurringNotification`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `declined_transaction_id` | `String` | Optional | Declined Transaction ID |
| `payment_transaction_id` | `String` | Optional | Payment Transaction ID |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `created_user_id` | `String` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `modified_user_id` | `String` | Optional | Last User ID that updated the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_ts": 1422040992,
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "declined_transaction_id": "declined_transaction_id0",
  "payment_transaction_id": "payment_transaction_id8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

