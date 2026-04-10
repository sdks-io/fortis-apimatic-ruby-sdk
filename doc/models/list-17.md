
# List 17

*This model accepts additional fields of type Object.*

## Structure

`List17`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `rejected_transaction_id` | `String` | Optional | Rejected Transaction ID.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `return_fee` | `Integer` | Optional | Return Fee.<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `id` | `String` | Optional | Transaction ACH Retry ID.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `retry_transaction_id` | `String` | Optional | Retry Transaction ID.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `return_fee_transaction_id` | `String` | Optional | Return Fee Transaction ID.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `created_user_id` | `String` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `rejected_transaction` | [`Transaction`](../../doc/models/transaction.md) | Optional | - |
| `retry_transaction` | [`Transaction`](../../doc/models/transaction.md) | Optional | - |
| `return_fee_transaction` | [`Transaction`](../../doc/models/transaction.md) | Optional | - |
| `created_user` | [`User9`](../../doc/models/user-9.md) | Optional | - |
| `changelogs` | [`Array[Changelog]`](../../doc/models/changelog.md) | Optional | Changelog Information on `expand` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "rejected_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "retry_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "return_fee_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "return_fee": 230,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

