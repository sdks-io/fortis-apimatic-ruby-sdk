
# V1 Recurrings Defer Payment Request

*This model accepts additional fields of type Object.*

## Structure

`V1RecurringsDeferPaymentRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `defer_count` | `Integer` | Required | Defer Count<br><br>**Constraints**: `>= 1`, `<= 99` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "defer_count": 5,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

