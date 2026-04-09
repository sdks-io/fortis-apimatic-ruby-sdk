
# Response Transaction Ach Retry

## Structure

`ResponseTransactionAchRetry`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type99Enum`](../../doc/models/type-99-enum.md) | Optional | Resource Type<br><br>**Default**: `Type99Enum::TRANSACTIONACHRETRY` |
| `data` | [`Data26`](../../doc/models/data-26.md) | Optional | - |

## Example (as JSON)

```json
{
  "type": "TransactionAchRetry",
  "data": {
    "rejected_transaction_id": "rejected_transaction_id4",
    "return_fee": 208,
    "id": "id0",
    "retry_transaction_id": "retry_transaction_id6",
    "return_fee_transaction_id": "return_fee_transaction_id4"
  }
}
```

