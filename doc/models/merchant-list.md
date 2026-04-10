
# Merchant List

*This model accepts additional fields of type Object.*

## Structure

`MerchantList`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `merchant_name_listed` | `String` | Required | Name of the listed merchant as used in the authorization message as defined in ISO 8583.<br><br>**Constraints**: *Maximum Length*: `40` |
| `acquirer_merchant_id_listed` | `String` | Optional | Acquirer-assigned Merchant Listed Identifier.<br>This may be the same value that is used in authorisation requests sent on behalf of the 3DS Requestor and is represented in ISO 8583 formatting requirements.<br><br>**Constraints**: *Maximum Length*: `15` |
| `merchant_amount` | `String` | Optional | Purchase amount for the merchant in minor units of currency with all punctuation removed.<br>When used in conjunction with the Purchase Currency Exponent field, proper punctuation can be calculated.<br><br>**Constraints**: *Maximum Length*: `48` |
| `merchant_currency` | `String` | Optional | Currency Code in which purchase Merchant Amount is expressed. Must be provided as ISO 4217 three-digit currency code except values 955-964 and 999.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `3` |
| `merchant_exponent` | `String` | Optional | Minor units of Merchant Currency as specified in the ISO 4217 currency exponent.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "merchant_name_listed": "merchant_name_listed4",
  "acquirer_merchant_id_listed": "acquirer_merchant_id_listed4",
  "merchant_amount": "merchant_amount2",
  "merchant_currency": "merchant_currency0",
  "merchant_exponent": "merchant_exponent4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

