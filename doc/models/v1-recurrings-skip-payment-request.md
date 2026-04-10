
# V1 Recurrings Skip Payment Request

*This model accepts additional fields of type Object.*

## Structure

`V1RecurringsSkipPaymentRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `skip_count` | `Integer` | Required | Skip Count<br><br>**Constraints**: `>= 1`, `<= 99` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "skip_count": 7,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

