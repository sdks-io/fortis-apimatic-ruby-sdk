
# Data 1

*This model accepts additional fields of type Object.*

## Structure

`Data1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `async` | [`Async2`](../../doc/models/async-2.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "async": {
    "code": "00000038-0000-0000-0000-000000000000",
    "link": "link8",
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

