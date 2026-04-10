
# Billing Address 5

Billing Address Object

*This model accepts additional fields of type Object.*

## Structure

`BillingAddress5`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `postal_code` | `String` | Optional | The Zip or 'Postal Code' portion of the address associated with the Credit Card.<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `10`, *Pattern*: `^[a-zA-Z0-9\-\s]+$` |
| `street` | `String` | Optional | The Street portion of the address associated with the Credit Card.<br><br>**Constraints**: *Maximum Length*: `32`, *Pattern*: `^[\w\#\,\.\-\'\&\s\/]+$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "postal_code": "48375",
  "street": "street4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

