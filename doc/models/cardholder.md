
# Cardholder

Contains information for the Cardholder. This field is required unless market or regional mandate restricts sending this information.

*This model accepts additional fields of type Object.*

## Structure

`Cardholder`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `address_match` | [`AddressMatch`](../../doc/models/address-match.md) | Optional | - |
| `billing_address` | [`BillingAddress13`](../../doc/models/billing-address-13.md) | Optional | - |
| `email` | `String` | Optional | The email address associated with the account that is either entered by the Cardholder, or is on file with the 3DS Requestor. This field shall meet requirements of Section 3.4 of IETF RFC 5322.<br><br>This field is required unless market or regional mandate restricts sending this information.<br><br>**Constraints**: *Maximum Length*: `256` |
| `home_phone` | [`HomePhone2`](../../doc/models/home-phone-2.md) | Optional | - |
| `mobile_phone` | [`MobilePhone2`](../../doc/models/mobile-phone-2.md) | Optional | - |
| `work_phone` | [`WorkPhone2`](../../doc/models/work-phone-2.md) | Optional | - |
| `cardholder_name` | `String` | Optional | Name of the Cardholder.<br><br>This field is required unless market or regional mandate restricts sending this information.<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `45` |
| `shipping_address` | [`ShippingAddress2`](../../doc/models/shipping-address-2.md) | Optional | - |
| `tax_id` | `String` | Optional | Tax ID is the Cardholder's tax identification.<br><br>This field is required depending on the rules provided by the Directory Server.<br>Available for supporting EMV 3DS 2.3.1 and later versions.<br><br>**Constraints**: *Maximum Length*: `45` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "email": "fortis@example.com",
  "cardholder_name": "John Doe",
  "address_match": "Y",
  "billing_address": {
    "city": "city2",
    "country_code": "country_code8",
    "address_line_1": "address_line_12",
    "address_line_2": "address_line_28",
    "address_line_3": "address_line_34",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "home_phone": {
    "cc": "cc8",
    "subscriber": "subscriber0",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "mobile_phone": {
    "cc": "cc8",
    "subscriber": "subscriber0",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

