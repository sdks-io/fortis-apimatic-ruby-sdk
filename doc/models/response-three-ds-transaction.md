
# Response Three DS Transaction

## Structure

`ResponseThreeDSTransaction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type46Enum`](../../doc/models/type-46-enum.md) | Optional | Resource Type<br><br>**Default**: `Type46Enum::THREEDSTRANSACTION` |
| `data` | [`Data13`](../../doc/models/data-13.md) | Optional | - |

## Example (as JSON)

```json
{
  "type": "ThreeDSTransaction",
  "data": {
    "three_ds_server_trans_id": "three_ds_server_trans_id0",
    "transaction_status": "transaction_status0",
    "ds_trans_id": "ds_trans_id8",
    "acs_trans_id": "acs_trans_id2",
    "message_version": "message_version0"
  }
}
```

