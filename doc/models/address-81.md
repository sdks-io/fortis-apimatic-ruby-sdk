
# Address 81

Array of merchant addresses.

## Structure

`Address81`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `address_line_1` | `String` | Required | Line 1 of address.<br><br>**Constraints**: *Maximum Length*: `100` |
| `address_line_2` | `String` | Optional | Line 2 of address.<br><br>**Constraints**: *Maximum Length*: `20` |
| `city` | `String` | Required | City of address.<br><br>**Constraints**: *Maximum Length*: `50` |
| `state_province` | `String` | Required | State or province of address.<br><br>**Constraints**: *Maximum Length*: `2` |
| `postal_code` | `String` | Required | Postal code of address.<br><br>**Constraints**: *Maximum Length*: `10` |
| `country_code` | `String` | Required | Country of address.<br><br>**Constraints**: *Maximum Length*: `2` |
| `address_type` | [`AddressTypeEnum`](../../doc/models/address-type-enum.md) | Required | Address type of address.<br><br>**Constraints**: *Maximum Length*: `20` |

## Example (as JSON)

```json
{
  "address_line_1": "121 E Main",
  "address_line_2": "Apt 707",
  "city": "Dallas",
  "state_province": "TX",
  "postal_code": "75087",
  "country_code": "US",
  "address_type": "location"
}
```

