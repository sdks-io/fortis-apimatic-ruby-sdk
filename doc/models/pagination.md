
# Pagination

Pagination info

## Structure

`Pagination`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type3Enum`](../../doc/models/type-3-enum.md) | Optional | Object type |
| `total_count` | `Integer` | Optional | Total records count |
| `page_count` | `Integer` | Optional | Total page count |
| `page_number` | `Integer` | Optional | Current page |
| `page_size` | `Integer` | Optional | Page size |

## Example (as JSON)

```json
{
  "type": "Pagination",
  "total_count": 423,
  "page_count": 42,
  "page_number": 6,
  "page_size": 10
}
```

