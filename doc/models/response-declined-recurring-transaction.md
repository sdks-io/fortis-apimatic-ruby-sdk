
# Response Declined Recurring Transaction

*This model accepts additional fields of type Object.*

## Structure

`ResponseDeclinedRecurringTransaction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type15`](../../doc/models/type-15.md) | Optional | - |
| `data` | [`Data3`](../../doc/models/data-3.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "DeclinedRecurringTransaction",
  "data": {
    "id": "id0",
    "declined_transaction_id": "declined_transaction_id6",
    "payment_transaction_id": "payment_transaction_id4",
    "status": "paid",
    "recurring_id": "recurring_id4",
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

