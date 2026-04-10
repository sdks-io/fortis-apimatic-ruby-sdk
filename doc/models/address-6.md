
# Address 6

*This model accepts additional fields of type Object.*

## Structure

`Address6`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `city` | `String` | Optional | City name<br><br>**Constraints**: *Maximum Length*: `36`, *Pattern*: `^[\w\#\,\.\-\'\&\s\/]+$` |
| `state` | `String` | Optional | State name<br><br>**Constraints**: *Minimum Length*: `2`, *Maximum Length*: `2` |
| `postal_code` | `String` | Optional | Postal code<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `10`, *Pattern*: `^[a-zA-Z0-9\-\s]+$` |
| `country` | `Object` | Optional | - |
| `street` | `String` | Optional | Street<br><br>**Constraints**: *Maximum Length*: `32`, *Pattern*: `^[\w\#\,\.\-\'\&\s\/]+$` |
| `street_2` | `String` | Optional | Street 2<br><br>**Constraints**: *Maximum Length*: `32`, *Pattern*: `^[\w\#\,\.\-\'\&\s\/]+$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "city": "Novi",
  "state": "MI",
  "postal_code": "48375",
  "country": {
    "key1": "val1",
    "key2": "val2"
  },
  "street": "street0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

