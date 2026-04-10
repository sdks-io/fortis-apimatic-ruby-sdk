
# Detail

*This model accepts additional fields of type Object.*

## Structure

`Detail`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message` | `String` | Optional | - |
| `path` | `Array[String]` | Optional | - |
| `type` | `String` | Optional | - |
| `context` | [`Context`](../../doc/models/context.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "message": "\"fieldName\" is required",
  "type": "any.required",
  "path": [
    "path8",
    "path9"
  ],
  "context": {
    "key": "key2",
    "label": "label2",
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

