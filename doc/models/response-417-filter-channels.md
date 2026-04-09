
# Response 417 Filter Channels

## Structure

`Response417filterChannels`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status_code` | `Integer` | Optional | Response code |
| `error` | `String` | Optional | Expectation Failed |
| `message` | `String` | Optional | Channel filters are not set for this project |

## Example (as JSON)

```json
{
  "statusCode": 417,
  "error": "Expectation Failed",
  "message": "Channel filters are not set for this project"
}
```

