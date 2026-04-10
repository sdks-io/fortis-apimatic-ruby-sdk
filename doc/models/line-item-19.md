
# Line Item 19

*This model accepts additional fields of type Object.*

## Structure

`LineItem19`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `alternate_tax_id` | `String` | Optional | Tax identification number of the merchant that reported the alternate tax amount.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `15` |
| `debit_credit` | `Object` | Optional | - |
| `description` | `String` | Required | Description of the item.<br><br>**Constraints**: *Maximum Length*: `26` |
| `discount_amount` | `Integer` | Optional | Total discount amount applied against the line item total ,Can accept Two (2) decimal places.<br><br>**Constraints**: `<= 99999999999900` |
| `discount_rate` | `Integer` | Optional | Discount rate for the line item ,Can accept Two (2) decimal places.<br><br>**Constraints**: `<= 9999900` |
| `product_code` | `String` | Required | Merchant-defined description code of the item.<br><br>**Constraints**: *Maximum Length*: `12` |
| `quantity` | `Integer` | Optional | Quantity of the item, can accept Four (4) decimal places.<br><br>**Constraints**: `<= 99999` |
| `tax_amount` | `Integer` | Optional | Amount of any value added taxes, can accept Two (2) decimal places.<br><br>**Constraints**: `>= 0`, `<= 99999999999` |
| `tax_rate` | `Integer` | Optional | Tax rate used to calculate the sales tax amount, can accept 2 decimal places.<br><br>**Constraints**: `<= 999900` |
| `tax_type_applied` | `String` | Optional | Type of value-added taxes that are being used (Conditional If tax amount is supplied)<br><br>> This field is only required when Merchant is directed to include by Mastercard.<br><br>**Constraints**: *Maximum Length*: `4` |
| `tax_type_id` | `String` | Optional | Indicates the type of tax collected in relationship to a specific tax amount (Conditional If tax amount is supplied)<br><br>**Constraints**: *Maximum Length*: `2` |
| `unit_code` | `String` | Required | Units of measurement as used in international trade. (See Codes for Units of Measurement below for unit code abbreviations)<br><br>**Constraints**: *Maximum Length*: `3` |
| `unit_cost` | `Integer` | Required | Unit cost of the item ,Can accept Four (4) decimal places.<br><br>**Constraints**: `<= 99999999999900` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "alternate_tax_id": "1234",
  "description": "cool drink",
  "discount_amount": 10,
  "discount_rate": 11,
  "product_code": "coke12345678",
  "quantity": 5,
  "tax_amount": 3,
  "tax_rate": 0,
  "tax_type_applied": "22",
  "tax_type_id": "a1",
  "unit_code": "gll",
  "unit_cost": 10,
  "debit_credit": {
    "key1": "val1",
    "key2": "val2"
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

