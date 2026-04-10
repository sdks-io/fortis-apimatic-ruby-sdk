
# Home Phone

The home phone provided by the Cardholder. Refer to ITU-E.164 for additional information on format and length.

This field is required if available, unless market or regional mandate restricts sending this information.

*This model accepts additional fields of type Object.*

## Structure

`HomePhone`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `cc` | `String` | Optional | Country Code of the phone<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `3` |
| `subscriber` | `String` | Optional | Subscriber section of the number<br><br>**Constraints**: *Maximum Length*: `15` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "cc": "cc6",
  "subscriber": "subscriber8",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

