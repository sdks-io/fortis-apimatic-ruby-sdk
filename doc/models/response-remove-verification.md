
# Response Remove Verification

## Structure

`ResponseRemoveVerification`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type134Enum`](../../doc/models/type-134-enum.md) | Optional | Resource Type<br><br>**Default**: `Type134Enum::REMOVEVERIFICATION` |
| `data` | [`Data32`](../../doc/models/data-32.md) | Optional | - |

## Example (as JSON)

```json
{
  "type": "RemoveVerification",
  "data": {
    "id": "id0",
    "user_id": "user_id8",
    "hash": "hash6",
    "created_ts": 114
  }
}
```

