
# Detail

## Structure

`Detail`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `message` | `String` | Optional | - |
| `path` | `Array[String]` | Optional | - |
| `type` | `String` | Optional | - |
| `context` | [`Context`](../../doc/models/context.md) | Optional | - |

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
    "label": "label2"
  }
}
```

