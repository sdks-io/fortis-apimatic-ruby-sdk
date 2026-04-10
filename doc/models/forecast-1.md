
# Forecast 1

*This model accepts additional fields of type Object.*

## Structure

`Forecast1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `recurring_id` | `String` | Optional | Recurring ID |
| `recurring_type` | `Float` | Optional | Recurring Type |
| `amount` | `Float` | Optional | Amount |
| `month` | `String` | Optional | Month |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "recurring_id": "Recurring ID",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "recurring_type": 113.38,
  "amount": 2.42,
  "month": "month0",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

