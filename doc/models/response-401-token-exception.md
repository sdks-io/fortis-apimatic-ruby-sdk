
# Response 401 Token Exception

## Structure

`Response401tokenException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status_code` | `Integer` | Optional | Response code |
| `error` | `String` | Optional | Unauthorized |
| `message` | `String` | Optional | Invalid token |

## Example (as JSON)

```json
{
  "statusCode": 401,
  "error": "Unauthorized",
  "message": "Invalid token"
}
```

