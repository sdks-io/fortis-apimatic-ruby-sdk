
# Contact 11

The Contact.

## Structure

`Contact11`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `first_name` | `String` | Optional | Contact's first name.<br><br>**Constraints**: *Maximum Length*: `20` |
| `last_name` | `String` | Optional | Contact's last name.<br><br>**Constraints**: *Maximum Length*: `20` |
| `email` | `String` | Optional | Contact's email address.<br><br>**Constraints**: *Maximum Length*: `100` |
| `phone_number` | `String` | Required | Contact's phone.<br><br>**Constraints**: *Maximum Length*: `20` |

## Example (as JSON)

```json
{
  "first_name": "Jeffery",
  "last_name": "Todd",
  "email": "jtodd@example.com",
  "phone_number": "555-555-3456"
}
```

