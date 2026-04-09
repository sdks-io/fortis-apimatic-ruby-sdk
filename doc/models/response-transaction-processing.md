
# Response Transaction Processing

## Structure

`ResponseTransactionProcessing`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type5Enum`](../../doc/models/type-5-enum.md) | Optional | Resource Type<br><br>**Default**: `Type5Enum::TRANSACTIONPROCESSING` |
| `data` | [`Data1`](../../doc/models/data-1.md) | Optional | - |

## Example (as JSON)

```json
{
  "type": "TransactionProcessing",
  "data": {
    "async": {
      "code": "00000038-0000-0000-0000-000000000000",
      "link": "link8"
    }
  }
}
```

