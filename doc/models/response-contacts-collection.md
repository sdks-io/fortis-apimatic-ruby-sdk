
# Response Contacts Collection

*This model accepts additional fields of type Object.*

## Structure

`ResponseContactsCollection`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type11`](../../doc/models/type-11.md) | Optional | - |
| `list` | [`Array[List1]`](../../doc/models/list-1.md) | Optional | Resource Members |
| `links` | [`Links1`](../../doc/models/links-1.md) | Optional | - |
| `pagination` | [`Pagination1`](../../doc/models/pagination-1.md) | Optional | - |
| `sort` | [`Sort1`](../../doc/models/sort-1.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "ContactsCollection",
  "list": [
    {
      "location_id": "location_id6",
      "account_number": "account_number2",
      "contact_api_id": "contact_api_id2",
      "first_name": "first_name2",
      "last_name": "last_name0",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "location_id": "location_id6",
      "account_number": "account_number2",
      "contact_api_id": "contact_api_id2",
      "first_name": "first_name2",
      "last_name": "last_name0",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "location_id": "location_id6",
      "account_number": "account_number2",
      "contact_api_id": "contact_api_id2",
      "first_name": "first_name2",
      "last_name": "last_name0",
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

