
# Response Error Exception

## Structure

`ResponseErrorException`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | `String` | Optional | Message type |
| `id` | `String` | Optional | Unique identifier for this API call |
| `status_code` | `Integer` | Optional | HTTP status code |
| `title` | `String` | Optional | Error title |
| `detail` | [`Detail1`](../../doc/models/detail-1.md) | Optional | Error details |
| `meta` | `Object` | Optional | Object with additional error details |

## Example (as JSON)

```json
{
  "type": "Error",
  "id": "c7f03d44-c966-4578-93ff-295f3ef6a467",
  "statusCode": 400,
  "title": "Bad Request",
  "detail": {
    "three_ds_server_trans_id": "three_ds_server_trans_id6",
    "acs_trans_id": "acs_trans_id8",
    "ds_trans_id": "ds_trans_id4",
    "error_code": "error_code4",
    "error_component": "error_component2"
  }
}
```

