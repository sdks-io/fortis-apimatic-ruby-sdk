
# Response Tags Collection

*This model accepts additional fields of type Object.*

## Structure

`ResponseTagsCollection`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type78`](../../doc/models/type-78.md) | Optional | - |
| `list` | [`Array[List13]`](../../doc/models/list-13.md) | Optional | Resource Members |
| `links` | [`Links1`](../../doc/models/links-1.md) | Optional | - |
| `pagination` | [`Pagination1`](../../doc/models/pagination-1.md) | Optional | - |
| `sort` | [`Sort1`](../../doc/models/sort-1.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "TagsCollection",
  "list": [
    {
      "location_id": "location_id6",
      "title": "title8",
      "id": "id2",
      "created_ts": 56,
      "modified_ts": 124,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "location_id": "location_id6",
      "title": "title8",
      "id": "id2",
      "created_ts": 56,
      "modified_ts": 124,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "links": {
    "type": "Links",
    "first": "first0",
    "previous": "previous2",
    "next": "next2",
    "last": "last4",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "pagination": {
    "type": "Pagination",
    "total_count": 100,
    "page_count": 212,
    "page_number": 28,
    "page_size": 6,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "sort": {
    "type": "Sorting",
    "fields": [
      {
        "field": "field2",
        "order": "asc",
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      {
        "field": "field2",
        "order": "asc",
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      },
      {
        "field": "field2",
        "order": "asc",
        "exampleAdditionalProperty": {
          "key1": "val1",
          "key2": "val2"
        }
      }
    ],
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

