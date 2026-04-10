
# Response 412 Exception

*This model accepts additional fields of type Object.*

## Structure

`Response412Exception`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | `String` | Optional | - |
| `id` | `String` | Optional | - |
| `status_code` | `Integer` | Optional | Response code |
| `title` | `String` | Optional | Error description |
| `detail` | `String` | Optional | Error details |
| `meta` | [`Meta`](../../doc/models/meta.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "clj4ge1234004t9ptdoz34567",
  "id": "clj4ge1234004t9ptdoz34567",
  "statusCode": 412,
  "title": "Precondition Failed",
  "detail": "\"fieldName\" is required",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

