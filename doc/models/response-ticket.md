
# Response Ticket

## Structure

`ResponseTicket`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `type` | [`Type87Enum`](../../doc/models/type-87-enum.md) | Optional | Resource Type<br><br>**Default**: `Type87Enum::TICKET` |
| `data` | [`Data24`](../../doc/models/data-24.md) | Optional | - |

## Example (as JSON)

```json
{
  "type": "Ticket",
  "data": {
    "account_holder_name": "account_holder_name0",
    "exp_date": "exp_date8",
    "cvv": "cvv8",
    "account_number": "account_number0",
    "billing_address": {
      "postal_code": "postal_code0",
      "street": "street8"
    }
  }
}
```

