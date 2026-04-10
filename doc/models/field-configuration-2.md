
# Field Configuration 2

*This model accepts additional fields of type Object.*

## Structure

`FieldConfiguration2`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `css_mini` | `TrueClass \| FalseClass` | Optional | CSS Mini |
| `stack` | [`Stack`](../../doc/models/stack.md) | Optional | - |
| `header` | [`Header2`](../../doc/models/header-2.md) | Optional | - |
| `body` | [`Body2`](../../doc/models/body-2.md) | Optional | - |
| `footer` | [`Footer2`](../../doc/models/footer-2.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "css_mini": true,
  "stack": "horizontal",
  "header": {
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
  },
  "body": {
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
      },
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
      },
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
  },
  "footer": {
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
      },
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
  },
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

