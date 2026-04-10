
# Response Quick Invoice

*This model accepts additional fields of type Object.*

## Structure

`ResponseQuickInvoice`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type59`](../../doc/models/type-59.md) | Optional | - |
| `data` | [`Data18`](../../doc/models/data-18.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "QuickInvoice",
  "data": {
    "location_id": "location_id4",
    "title": "title6",
    "cc_product_transaction_id": "cc_product_transaction_id2",
    "ach_product_transaction_id": "ach_product_transaction_id2",
    "due_date": "due_date8",
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

