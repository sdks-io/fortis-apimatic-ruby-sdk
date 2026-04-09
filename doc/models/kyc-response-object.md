
# Kyc Response Object

Array of KYC response objects.

## Structure

`KycResponseObject`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `value` | `String` | Required | KYC object value. |
| `type` | `String` | Required | KYC oject type.<br><br>**Constraints**: *Maximum Length*: `32` |

## Example (as JSON)

```json
{
  "value": "KYC value.",
  "type": "KYC type"
}
```

