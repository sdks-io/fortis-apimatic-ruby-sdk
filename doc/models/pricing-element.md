
# Pricing Element

Array of pricing items from template to be changed.

*This model accepts additional fields of type Object.*

## Structure

`PricingElement`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `item_id` | `Integer` | Required | Item ID.<br><br>**Constraints**: `>= 0` |
| `item_value` | `Float` | Required | Item value.<br><br>**Constraints**: `>= 0` |
| `item_term` | `Integer` | Required | Item term.<br><br>**Constraints**: `>= 0` |
| `item_description` | `String` | Optional | Item desciption.<br><br>**Constraints**: *Maximum Length*: `100` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "item_id": 5,
  "item_value": 1.5,
  "item_term": 2,
  "item_description": "AVS fee.",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

