
# Pagination 1

*This model accepts additional fields of type Object.*

## Structure

`Pagination1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type3`](../../doc/models/type-3.md) | Optional | - |
| `total_count` | `Integer` | Optional | Total records count |
| `page_count` | `Integer` | Optional | Total page count |
| `page_number` | `Integer` | Optional | Current page |
| `page_size` | `Integer` | Optional | Page size |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "total_count": 423,
  "page_count": 42,
  "page_number": 6,
  "page_size": 10,
  "type": "Pagination",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

