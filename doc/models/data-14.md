
# Data 14

## Structure

`Data14`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | Deposit Id |
| `company_id` | `String` | Optional | Company Id |
| `merchant_id` | `String` | Optional | Merchant Id |
| `service` | `String` | Optional | Service |
| `deposit_types` | [`Array[DepositTypeEnum]`](../../doc/models/deposit-type-enum.md) | Optional | - |
| `deposit_amount` | `Float` | Optional | Deposit Amount |
| `batch_amount` | `Float` | Optional | Batch Amount |
| `adjustment_amount` | `Float` | Optional | Adjustment Amount |
| `retained_amount` | `Float` | Optional | Retained Amount |
| `conveyed_amount` | `Float` | Optional | Conveyed Amount |
| `fee_amount` | `Float` | Optional | Fee Amount |
| `reference_number` | `String` | Optional | Reference Number |
| `trace_number` | `String` | Optional | - |
| `currency` | `String` | Optional | Currency |
| `created_ts` | `Integer` | Optional | Created Timestamp |
| `reported_date` | `String` | Optional | Reported Date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `transaction_date` | `String` | Optional | Transaction Date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `deposit_account` | `String` | Optional | Deposit Account |
| `details` | [`Array[Detail2]`](../../doc/models/detail-2.md) | Optional | - |

## Example (as JSON)

```json
{
  "company_id": "8410111",
  "merchant_id": "88441",
  "deposit_amount": 2487.24,
  "batch_amount": 2487.24,
  "adjustment_amount": 2487.24,
  "retained_amount": 2487.24,
  "conveyed_amount": 2487.24,
  "fee_amount": 2487.24,
  "reference_number": "400000",
  "trace_number": "400000",
  "currency": "USD",
  "created_ts": 1422040992,
  "reported_date": "2021-12-01",
  "transaction_date": "2021-12-01",
  "id": "id0",
  "service": "service0",
  "deposit_types": [
    "deposit",
    "adjustment",
    "fee"
  ]
}
```

