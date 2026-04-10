
# Location 5

The Location.

*This model accepts additional fields of type Object.*

## Structure

`Location5`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `address_line_1` | `String` | Optional | Merchant's business address line 1.<br><br>**Constraints**: *Maximum Length*: `100` |
| `address_line_2` | `String` | Optional | Merchant's business address line 2.<br><br>**Constraints**: *Maximum Length*: `20` |
| `city` | `String` | Optional | Merchant's business city.<br><br>**Constraints**: *Maximum Length*: `50` |
| `state_province` | `String` | Optional | Merchant's business two-digit state or province code.<br><br>**Constraints**: *Maximum Length*: `2` |
| `postal_code` | `String` | Optional | Merchant's business postal code.<br><br>**Constraints**: *Maximum Length*: `10` |
| `phone_number` | `String` | Optional | Merchant's business phone number.<br><br>**Constraints**: *Maximum Length*: `20` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "address_line_1": "1200 West Hartford Pkwy",
  "address_line_2": "Suite 2000",
  "city": "Dover",
  "state_province": "DE",
  "postal_code": "55022",
  "phone_number": "555-555-1212",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

