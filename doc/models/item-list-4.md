
# Item List 4

## Structure

`ItemList4`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `name` | `String` | Required | Item's Name, must be unique on the list<br><br>**Constraints**: *Maximum Length*: `100` |
| `amount` | `Integer` | Required | Item's Amount<br><br>**Constraints**: `>= -999999999`, `<= 999999999` |

## Example (as JSON)

```json
{
  "name": "Bread",
  "amount": 2015
}
```

