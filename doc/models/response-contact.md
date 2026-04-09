
# Response Contact

## Structure

`ResponseContact`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type10Enum`](../../doc/models/type-10-enum.md) | Optional | Resource Type<br><br>**Default**: `Type10Enum::CONTACT` |
| `data` | [`Data2`](../../doc/models/data-2.md) | Optional | - |

## Example (as JSON)

```json
{
  "type": "Contact",
  "data": {
    "location_id": "location_id4",
    "account_number": "account_number0",
    "contact_api_id": "contact_api_id4",
    "first_name": "first_name0",
    "last_name": "last_name8"
  }
}
```

