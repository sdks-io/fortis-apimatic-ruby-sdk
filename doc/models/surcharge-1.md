
# Surcharge 1

*This model accepts additional fields of type Object.*

## Structure

`Surcharge1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `surcharge_fee` | `Integer` | Optional | Surcharge Fee |
| `surcharge_rate` | `Integer` | Optional | Surcharge Rate |
| `max_transaction_amount` | `Integer` | Optional | Max Transaction Amount |
| `min_fee_amount` | `Integer` | Optional | Min Fee Amount |
| `max_fee_amount` | `Integer` | Optional | Max Fee Amount |
| `surcharge_on_recurring` | `TrueClass \| FalseClass` | Optional | Surcharge On Recurring |
| `refund_surcharges` | `TrueClass \| FalseClass` | Optional | Refund Surcharges |
| `blind_refund_surcharges` | `TrueClass \| FalseClass` | Optional | Blind Refund Surcharges |
| `product_transaction_id` | `String` | Optional | Product Transaction Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `run_as_separate_transaction` | `TrueClass \| FalseClass` | Optional | Run As Separate Transaction |
| `apply_to_user_type_id` | `String` | Optional | Apply To User Type Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `title` | `String` | Optional | Title<br><br>**Constraints**: *Maximum Length*: `256` |
| `surcharge_label` | `String` | Optional | Surcharge Label<br><br>**Constraints**: *Maximum Length*: `64` |
| `surcharge_transaction_product_id` | `String` | Optional | Surcharge Transaction Product Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `state_exception_check` | `TrueClass \| FalseClass` | Optional | State Exception Check |
| `compliant` | `TrueClass \| FalseClass` | Optional | Compliant |
| `id` | `String` | Optional | Surcharge Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `created_user_id` | `String` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `modified_user_id` | `String` | Optional | Last User ID that updated the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "surcharge_fee": 10,
  "surcharge_rate": 1,
  "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "apply_to_user_type_id": "11e95f8ec39de8fbdb0a4f1a",
  "surcharge_transaction_product_id": "11e95f8ec39de8fbdb0a4f1a",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "max_transaction_amount": 82,
  "min_fee_amount": 28,
  "max_fee_amount": 2,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

