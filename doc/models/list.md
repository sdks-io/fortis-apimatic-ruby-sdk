
# List

*This model accepts additional fields of type Object.*

## Structure

`List`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | Batch ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `product_transaction_id` | `String` | Optional | Product Transaction Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `processing_status_id` | `Integer` | Optional | Processing Status Id<br><br>**Constraints**: `>= 1`, `<= 5` |
| `batch_num` | `Integer` | Optional | Batch Number |
| `is_open` | `Float` | Optional | 1 = Batch is_open, 0 = Batch is closed. Only 1 open batch per product_transaction_id.<br><br>**Constraints**: `>= 0`, `<= 1` |
| `settlement_file_name` | `String` | Optional | Settlement File Name |
| `batch_close_ts` | `Float` | Optional | Batch Close Ts in unix |
| `batch_close_detail` | `String` | Optional | Batch Close Detail |
| `total_sale_amount` | `Integer` | Optional | Total Sale Amount |
| `total_sale_count` | `Integer` | Optional | Total Sale Count |
| `total_refund_amount` | `Integer` | Optional | Total Refund Amount |
| `total_refund_count` | `Integer` | Optional | Total Refund Count |
| `total_void_amount` | `Integer` | Optional | Total Void Amount |
| `total_void_count` | `Integer` | Optional | Total Void Count |
| `total_blind_refund_amount` | `Integer` | Optional | Total Blind Refund Amount |
| `total_blind_refund_count` | `Integer` | Optional | Total Blind Refund Count |
| `changelogs` | [`Array[Changelog]`](../../doc/models/changelog.md) | Optional | Changelog Information on `expand` |
| `postback_logs` | [`Array[PostbackLog]`](../../doc/models/postback-log.md) | Optional | Postback Log Information on `expand` |
| `product_transaction` | [`ProductTransaction1`](../../doc/models/product-transaction-1.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "processing_status_id": 2,
  "batch_num": 4,
  "is_open": 0,
  "settlement_file_name": "settement_file.txt",
  "batch_close_ts": 1531423693,
  "batch_close_detail": "BATCH_MISMATCH",
  "total_sale_amount": 2342,
  "total_sale_count": 21,
  "total_refund_amount": 2342,
  "total_refund_count": 18,
  "total_void_amount": 2342,
  "total_void_count": 17,
  "total_blind_refund_amount": 2342,
  "total_blind_refund_count": 16,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

