
# Data 4

*This model accepts additional fields of type Object.*

## Structure

`Data4`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `declined_recurring_transaction_id` | `String` | Optional | Declined Recurring Transaction Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `account_number` | `String` | Optional | Account Number<br><br>**Constraints**: *Minimum Length*: `13`, *Maximum Length*: `19` |
| `account_holder_name` | `String` | Optional | Account Holder Name |
| `exp_date` | `String` | Optional | Exp Date<br><br>**Constraints**: *Maximum Length*: `4` |
| `transaction_amount` | `Integer` | Optional | Transaction Amount<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `description` | `String` | Optional | Description<br><br>**Constraints**: *Maximum Length*: `255` |
| `billing_address` | [`BillingAddress7`](../../doc/models/billing-address-7.md) | Optional | - |
| `tags` | `Array[String]` | Optional | Tags |
| `id` | `String` | Optional | Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `first_six` | `String` | Optional | First Six<br><br>**Constraints**: *Maximum Length*: `6` |
| `last_four` | `String` | Optional | Last Four<br><br>**Constraints**: *Maximum Length*: `4` |
| `routing` | `String` | Optional | Routing |
| `status_id` | `Float` | Optional | Status Id |
| `reason_code_id` | `Object` | Optional | - |
| `type_id` | `Float` | Optional | Type Id |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `created_user_id` | `String` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "declined_recurring_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "account_number": "5454545454545454",
  "account_holder_name": "John Doe",
  "exp_date": "0722",
  "transaction_amount": 0,
  "description": "Description",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "first_six": "700953",
  "last_four": "3657",
  "created_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

