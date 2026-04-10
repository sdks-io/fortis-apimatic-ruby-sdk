
# Links 1

*This model accepts additional fields of type Object.*

## Structure

`Links1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type2`](../../doc/models/type-2.md) | Optional | - |
| `first` | `String` | Optional | Link to the first page |
| `previous` | `String` | Optional | Link to the previous page |
| `mnext` | `String` | Optional | Link to the next page |
| `last` | `String` | Optional | Link to the last page |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "first": "/v1/endpoint?page[size]=10&page[number]=1",
  "previous": "/v1/endpoint?page[size]=10&page[number]=5",
  "next": "/v1/endpoint?page[size]=10&page[number]=7",
  "last": "/v1/endpoint?page[size]=10&page[number]=42",
  "type": "Links",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

