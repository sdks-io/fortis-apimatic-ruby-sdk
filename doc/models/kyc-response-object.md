
# Kyc Response Object

Array of KYC response objects.

*This model accepts additional fields of type Object.*

## Structure

`KycResponseObject`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `value` | `String` | Required | KYC object value. |
| `type` | `String` | Required | KYC oject type.<br><br>**Constraints**: *Maximum Length*: `32` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "value": "KYC value.",
  "type": "KYC type",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

