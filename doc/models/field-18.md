
# Field 18

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
  "visible": true
}
```

