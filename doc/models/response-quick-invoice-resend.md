
# Response Quick Invoice Resend

## Structure

`ResponseQuickInvoiceResend`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type61Enum`](../../doc/models/type-61-enum.md) | Optional | Resource Type<br><br>**Default**: `Type61Enum::QUICKINVOICERESEND` |
| `data` | [`Data19`](../../doc/models/data-19.md) | Optional | - |

## Example (as JSON)

```json
{
  "type": "QuickInvoiceResend",
  "data": {
    "id": "id0",
    "email_log_id": "email_log_id2",
    "sms_log_id": "sms_log_id4",
    "success": false,
    "sms_success": false
  }
}
```

