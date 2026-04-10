
# Response 416 Date Range

*This model accepts additional fields of type Object.*

## Structure

`Response416DateRange`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `status_code` | `Integer` | Optional | Response code |
| `error` | `String` | Optional | Requested Range Not Satisfiable |
| `message` | `String` | Optional | The "fieldDate" should be less or equal to "ISODate". |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "statusCode": 416,
  "error": "Requested Range Not Satisfiable",
  "message": "The \"startDate\" should be less or equal \"2019-08-20T03:00:00.000Z\".",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

