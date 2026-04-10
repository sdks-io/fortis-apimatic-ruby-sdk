
# Response Transaction Processing

*This model accepts additional fields of type Object.*

## Structure

`ResponseTransactionProcessing`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type5`](../../doc/models/type-5.md) | Optional | - |
| `data` | [`Data1`](../../doc/models/data-1.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "TransactionProcessing",
  "data": {
    "async": {
      "code": "00000038-0000-0000-0000-000000000000",
      "link": "link8",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
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

