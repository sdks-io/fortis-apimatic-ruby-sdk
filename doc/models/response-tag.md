
# Response Tag

*This model accepts additional fields of type Object.*

## Structure

`ResponseTag`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type77`](../../doc/models/type-77.md) | Optional | - |
| `data` | [`Data22`](../../doc/models/data-22.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "Tag",
  "data": {
    "location_id": "location_id4",
    "title": "title6",
    "id": "id0",
    "created_ts": 114,
    "modified_ts": 190,
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

