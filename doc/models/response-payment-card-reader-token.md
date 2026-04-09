
# Response Payment Card Reader Token

## Structure

`ResponsePaymentCardReaderToken`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type58Enum`](../../doc/models/type-58-enum.md) | Optional | Resource Type<br><br>**Default**: `Type58Enum::PAYMENTCARDREADERTOKEN` |
| `data` | [`Data17`](../../doc/models/data-17.md) | Optional | - |

## Example (as JSON)

```json
{
  "type": "PaymentCardReaderToken",
  "data": {
    "token": "token4"
  }
}
```

