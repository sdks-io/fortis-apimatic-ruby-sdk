
# Response Onboarding

*This model accepts additional fields of type Object.*

## Structure

`ResponseOnboarding`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type52`](../../doc/models/type-52.md) | Optional | - |
| `data` | [`Data15`](../../doc/models/data-15.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "type": "Onboarding",
  "data": {
    "parent_id": "parent_id6",
    "primary_principal": {
      "first_name": "first_name6",
      "last_name": "last_name4",
      "middle_name": "middle_name6",
      "title": "title2",
      "date_of_birth": "date_of_birth2",
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    "template_code": "template_code0",
    "email": "email6",
    "dba_name": "dba_name8",
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

