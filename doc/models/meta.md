
# Meta

*This model accepts additional fields of type Object.*

## Structure

`Meta`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `details` | [`Array[Detail]`](../../doc/models/detail.md) | Optional | Error detail |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "details": [
    {
      "message": "message0",
      "path": [
        "path6"
      ],
      "type": "type0",
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
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

