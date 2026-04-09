
# Surcharge Transaction

Surcharge Transaction Information on `expand`

## Structure

`SurchargeTransaction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `model_name` | `String` | Optional | Model Name |
| `transaction_id` | `String` | Optional | Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `surcharge_fee` | `Integer` | Optional | Surcharge Fee<br><br>**Constraints**: `>= 0` |
| `surcharge_rate` | `Integer` | Optional | Surcharge Rate<br><br>**Constraints**: `>= 0` |
| `surcharge_amount` | `Integer` | Optional | Surcharge Amount<br><br>**Constraints**: `>= 0` |
| `surcharge_transaction_min` | `Integer` | Optional | Surcharge Transaction Minimum<br><br>**Constraints**: `>= 0` |
| `surcharge_transaction_max` | `Integer` | Optional | Surcharge Transaction Maximum<br><br>**Constraints**: `>= 0` |
| `created` | `Integer` | Optional | Created |
| `modified` | `Integer` | Optional | Modified |
| `created_user_id` | `String` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `modified_user_id` | `String` | Optional | Last User ID that updated the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Example (as JSON)

```json
{
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "model_name": "Model Name",
  "transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "surcharge_fee": 0,
  "surcharge_rate": 0,
  "created": 1422040992,
  "modified": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a"
}
```

