
# Response Terminal

*This model accepts additional fields of type Object.*

## Structure

`ResponseTerminal`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type82`](../../doc/models/type-82.md) | Optional | - |
| `data` | [`Data23`](../../doc/models/data-23.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "Terminal",
  "data": {
    "location_id": "location_id4",
    "default_product_transaction_id": "default_product_transaction_id6",
    "terminal_application_id": "terminal_application_id0",
    "terminal_cvm_id": "terminal_cvm_id0",
    "terminal_manufacturer_code": "1",
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

