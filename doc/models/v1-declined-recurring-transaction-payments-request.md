
# V1 Declined Recurring Transaction Payments Request

*This model accepts additional fields of type Object.*

## Structure

`V1DeclinedRecurringTransactionPaymentsRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `declined_recurring_transaction_id` | `String` | Required | Declined Recurring Transaction Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `account_number` | `String` | Required | Account Number<br><br>**Constraints**: *Minimum Length*: `13`, *Maximum Length*: `19` |
| `account_holder_name` | `String` | Optional | Account Holder Name |
| `exp_date` | `String` | Required | Exp Date<br><br>**Constraints**: *Maximum Length*: `4` |
| `transaction_amount` | `Integer` | Required | Transaction Amount<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `description` | `String` | Optional | Description<br><br>**Constraints**: *Maximum Length*: `255` |
| `billing_address` | [`BillingAddress7`](../../doc/models/billing-address-7.md) | Optional | - |
| `tags` | `Array[String]` | Optional | Tags |
| `replace_account_vault` | `TrueClass \| FalseClass` | Optional | Replace AccountVault |
| `save_account` | `TrueClass \| FalseClass` | Optional | Specifies to save account to contacts profile if account_number/track_data is present with either contact_id or contact_api_id in params. |
| `save_account_title` | `String` | Optional | If saving token while running a transaction, this will be the title of the token.<br><br>**Constraints**: *Maximum Length*: `16` |
| `subtotal_amount` | `Integer` | Optional | Subtotal Amount<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `surcharge_amount` | `Integer` | Optional | Surcharge Amount<br><br>**Constraints**: `>= 0`, `<= 999999999` |
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
  "save_account_title": "John Account",
  "subtotal_amount": 599,
  "surcharge_amount": 599,
  "billing_address": {
    "postal_code": "postal_code0",
    "street": "street8",
    "city": "city2",
    "state": "state6",
    "phone": "phone2",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "tags": [
    "tags3",
    "tags4"
  ],
  "replace_account_vault": false,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

