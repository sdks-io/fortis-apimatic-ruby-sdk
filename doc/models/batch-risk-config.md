
# Batch Risk Config

Batch Risk Config

*This model accepts additional fields of type Object.*

## Structure

`BatchRiskConfig`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `blind_refund_total_count` | `Integer` | Optional | Blind Refund Total Count<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `blind_refund_max_amount` | `Integer` | Optional | Blind Refund Max Amount<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "blind_refund_total_count": 110,
  "blind_refund_max_amount": 172,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

