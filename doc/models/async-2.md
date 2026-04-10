
# Async 2

*This model accepts additional fields of type Object.*

## Structure

`Async2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `code` | `UUID \| String` | Optional | A [UUID v4](https://datatracker.ietf.org/doc/html/rfc4122) that's unique for the Async Request |
| `link` | `String` | Optional | Link to the status check endpoint |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "code": "406c66c3-21cb-47fb-80fc-843bc42507fb",
  "link": "/v1/async/status/406c66c3-21cb-47fb-80fc-843bc42507fb",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

