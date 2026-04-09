
# Response User Verifications Collection

## Structure

`ResponseUserVerificationsCollection`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type124Enum`](../../doc/models/type-124-enum.md) | Optional | Resource Type<br><br>**Default**: `Type124Enum::USERVERIFICATIONSCOLLECTION` |
| `list` | [`Array[List19]`](../../doc/models/list-19.md) | Optional | Resource Members |
| `links` | [`Links`](../../doc/models/links.md) | Optional | Pagination page links |
| `pagination` | [`Pagination`](../../doc/models/pagination.md) | Optional | Pagination info |
| `sort` | [`Sort`](../../doc/models/sort.md) | Optional | Sort information used on the results |

## Example (as JSON)

```json
{
  "type": "UserVerificationsCollection",
  "list": [
    {
      "id": "id2",
      "user_id": "user_id0",
      "hash": "hash8",
      "created_ts": 56
    },
    {
      "id": "id2",
      "user_id": "user_id0",
      "hash": "hash8",
      "created_ts": 56
    },
    {
      "id": "id2",
      "user_id": "user_id0",
      "hash": "hash8",
      "created_ts": 56
    }
  ],
  "links": {
    "type": "Links",
    "first": "first0",
    "previous": "previous2",
    "next": "next2",
    "last": "last4"
  },
  "pagination": {
    "type": "Pagination",
    "total_count": 100,
    "page_count": 212,
    "page_number": 28,
    "page_size": 6
  },
  "sort": {
    "type": "Sorting",
    "fields": [
      {
        "field": "field2",
        "order": "asc"
      },
      {
        "field": "field2",
        "order": "asc"
      },
      {
        "field": "field2",
        "order": "asc"
      }
    ]
  }
}
```

