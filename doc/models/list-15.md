
# List 15

*This model accepts additional fields of type Object.*

## Structure

`List15`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account_holder_name` | `String` | Optional | Account holder name<br><br>> The Name as it appears on Card.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `32` |
| `exp_date` | `String` | Optional | The Expiration Date for the credit card. |
| `cvv` | `String` | Optional | CVV<br><br>**Constraints**: *Maximum Length*: `4` |
| `account_number` | `String` | Optional | Account number<br><br>> A credit card number. Length 13-19.<br><br>**Constraints**: *Minimum Length*: `4`, *Maximum Length*: `19`, *Pattern*: `^[\d]+$` |
| `billing_address` | [`BillingAddress9`](../../doc/models/billing-address-9.md) | Optional | - |
| `contact_id` | `String` | Optional | Used to associate the Ticket with a Contact.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `contact_api_id` | `String` | Optional | Used to associate the Ticket with a Contact. |
| `location_id` | String \| nil | Optional | This is a container for any-of cases. |
| `location_api_id` | `String` | Optional | Location Api Id |
| `id` | `String` | Optional | A unique, system-generated identifier for the Ticket.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `created_user_id` | `String` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "account_holder_name": "John Smith",
  "exp_date": "0722",
  "account_number": "545454545454545",
  "contact_id": "11e95f8ec39de8fbdb0a4f1a",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "cvv": "cvv6",
  "billing_address": {
    "postal_code": "postal_code0",
    "street": "street8",
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

