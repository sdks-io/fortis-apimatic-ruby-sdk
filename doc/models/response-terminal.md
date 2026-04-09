
# Response Terminal

## Structure

`ResponseTerminal`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type82Enum`](../../doc/models/type-82-enum.md) | Optional | Resource Type<br><br>**Default**: `Type82Enum::TERMINAL` |
| `data` | [`Data23`](../../doc/models/data-23.md) | Optional | - |

## Example (as JSON)

```json
{
  "type": "Terminal",
  "data": {
    "location_id": "location_id4",
    "default_product_transaction_id": "default_product_transaction_id6",
    "terminal_application_id": "terminal_application_id0",
    "terminal_cvm_id": "terminal_cvm_id0",
    "terminal_manufacturer_code": "1"
  }
}
```

