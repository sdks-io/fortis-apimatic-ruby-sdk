
# Line Item 20

*This model accepts additional fields of type Object.*

## Structure

`LineItem20`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `description` | `String` | Required | Description of the item.<br><br>**Constraints**: *Maximum Length*: `26` |
| `commodity_code` | `String` | Required | An international description code of the individual good or service being supplied.<br><br>**Constraints**: *Maximum Length*: `12` |
| `discount_amount` | `Integer` | Optional | Total discount amount applied against the line item total ,Can accept Two (2) decimal places.<br><br>**Constraints**: `<= 99999999999900` |
| `other_tax_amount` | `Integer` | Optional | Used if city or multiple county taxes need to be broken out separately ,Can accept Two (2) decimal places.<br><br>**Constraints**: `<= 99999999999900` |
| `product_code` | `String` | Required | Merchant-defined description code of the item.<br><br>**Constraints**: *Maximum Length*: `12` |
| `quantity` | `Integer` | Optional | Quantity of the item, can accept Four (4) decimal places.<br><br>**Constraints**: `<= 99999` |
| `tax_amount` | `Integer` | Optional | Amount of any value added taxes, can accept Two (2) decimal places.<br><br>**Constraints**: `>= 0`, `<= 99999999999` |
| `tax_rate` | `Integer` | Optional | Tax rate used to calculate the sales tax amount, can accept 2 decimal places.<br><br>**Constraints**: `<= 999900` |
| `unit_code` | `String` | Required | Units of measurement as used in international trade. (See Codes for Units of Measurement below for unit code abbreviations)<br><br>**Constraints**: *Maximum Length*: `3` |
| `unit_cost` | `Integer` | Required | Unit cost of the item ,Can accept Four (4) decimal places.<br><br>**Constraints**: `<= 99999999999900` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "description": "cool drink",
  "commodity_code": "cc123456",
  "discount_amount": 0,
  "other_tax_amount": 0,
  "product_code": "fanta123456",
  "quantity": 12,
  "tax_amount": 4,
  "tax_rate": 0,
  "unit_code": "gll",
  "unit_cost": 3,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

