
# Detail 2

## Structure

`Detail2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `processor_batch_number` | `String` | Optional | Processor Batch Number |
| `product_code` | `String` | Optional | Product Code |
| `deposit_detail_type` | `String` | Optional | Deposit Detail Type |
| `amount` | `Float` | Optional | Amount |
| `memo` | `String` | Optional | Memo |
| `reported_date` | `String` | Optional | Reported Date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `settled_date` | `String` | Optional | Settled Date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `mid` | `String` | Optional | Merchant ID |

## Example (as JSON)

```json
{
  "amount": 2487.24,
  "reported_date": "2021-12-01",
  "settled_date": "2021-12-01",
  "processor_batch_number": "processor_batch_number6",
  "product_code": "product_code8",
  "deposit_detail_type": "deposit_detail_type6",
  "memo": "memo6"
}
```

