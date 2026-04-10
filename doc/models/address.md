
# Address

Address of contact

*This model accepts additional fields of type Object.*

## Structure

`Address`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `city` | `String` | Optional | City of contact<br><br>**Constraints**: *Maximum Length*: `36`, *Pattern*: `^[\w\#\,\.\-\'\&\s\/]+$` |
| `state` | `String` | Optional | State of contact<br><br>**Constraints**: *Maximum Length*: `24` |
| `postal_code` | `String` | Optional | Postal code of contact<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `10`, *Pattern*: `^[a-zA-Z0-9\-\s]+$` |
| `country` | `String` | Optional | The alpha 2 or alpha 3 format country code. If alpha 3 is provided, it will be converted to alpha 2. |
| `street` | `String` | Optional | Street of contact<br><br>**Constraints**: *Maximum Length*: `32`, *Pattern*: `^[\w\#\,\.\-\'\&\s\/]+$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "city": "Novi",
  "state": "Michigan",
  "postal_code": "48375",
  "country": "USA",
  "street": "street8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

