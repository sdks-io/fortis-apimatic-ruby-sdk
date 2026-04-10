
# Field 18

*This model accepts additional fields of type Object.*

## Structure

`Field18`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | id |
| `label` | `String` | Optional | Label |
| `field_type` | `String` | Optional | Field Type |
| `position` | `Array[String]` | Optional | Position<br><br>**Constraints**: *Minimum Items*: `1` |
| `required` | `TrueClass \| FalseClass` | Optional | Required |
| `readonly` | `TrueClass \| FalseClass` | Optional | Read Only |
| `visible` | `TrueClass \| FalseClass` | Optional | Visible |
| `value` | `String` | Optional | Value |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "id": "transaction_amount",
  "label": "Header",
  "field_type": "heading",
  "position": [
    "1",
    "0",
    "1",
    "1"
  ],
  "required": true,
  "readonly": true,
  "visible": true,
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

