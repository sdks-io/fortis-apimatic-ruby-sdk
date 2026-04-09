
# Response Send Verification

## Structure

`ResponseSendVerification`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type135Enum`](../../doc/models/type-135-enum.md) | Optional | Resource Type<br><br>**Default**: `Type135Enum::SENDVERIFICATION` |
| `data` | [`Data32`](../../doc/models/data-32.md) | Optional | - |

## Example (as JSON)

```json
{
  "type": "SendVerification",
  "data": {
    "id": "id0",
    "user_id": "user_id8",
    "hash": "hash6",
    "created_ts": 114
  }
}
```

