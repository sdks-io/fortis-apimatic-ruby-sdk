
# Response Declined Recurring Transaction Payment

*This model accepts additional fields of type Object.*

## Structure

`ResponseDeclinedRecurringTransactionPayment`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type20`](../../doc/models/type-20.md) | Optional | - |
| `data` | [`Data4`](../../doc/models/data-4.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "DeclinedRecurringTransactionPayment",
  "data": {
    "declined_recurring_transaction_id": "declined_recurring_transaction_id6",
    "account_number": "account_number0",
    "account_holder_name": "account_holder_name0",
    "exp_date": "exp_date8",
    "transaction_amount": 88,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

