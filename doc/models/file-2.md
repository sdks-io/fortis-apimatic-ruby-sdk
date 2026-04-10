
# File 2

*This model accepts additional fields of type Object.*

## Structure

`File2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `file_name` | `String` | Optional | The file name including the extension |
| `content` | `String` | Optional | File contents as a base64 encoded string |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "file_name": "file_name6",
  "content": "content6",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

