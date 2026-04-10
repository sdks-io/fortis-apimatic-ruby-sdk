
# Header 2

*This model accepts additional fields of type Object.*

## Structure

`Header2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `settings` | [`Settings`](../../doc/models/settings.md) | Optional | - |
| `fields` | [`Array[Field18]`](../../doc/models/field-18.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "settings": {
    "enabled": false,
    "columns": 202.28,
    "rows": 235.78,
    "exampleAdditionalProperty": {
      "key1": "val1",
      "key2": "val2"
    }
  },
  "fields": [
    {
      "id": "id8",
      "label": "label8",
      "field_type": "field_type4",
      "position": [
        "position7",
        "position8",
        "position9"
      ],
      "required": false,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

