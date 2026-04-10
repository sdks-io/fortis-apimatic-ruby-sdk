
# Response 417 Filter Channels

*This model accepts additional fields of type Object.*

## Structure

`Response417FilterChannels`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status_code` | `Integer` | Optional | Response code |
| `error` | `String` | Optional | Expectation Failed |
| `message` | `String` | Optional | Channel filters are not set for this project |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "statusCode": 417,
  "error": "Expectation Failed",
  "message": "Channel filters are not set for this project",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

