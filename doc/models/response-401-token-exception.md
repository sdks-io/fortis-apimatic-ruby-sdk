
# Response 401 Token Exception

*This model accepts additional fields of type Object.*

## Structure

`Response401TokenException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status_code` | `Integer` | Optional | Response code |
| `error` | `String` | Optional | Unauthorized |
| `message` | `String` | Optional | Invalid token |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "statusCode": 401,
  "error": "Unauthorized",
  "message": "Invalid token",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

