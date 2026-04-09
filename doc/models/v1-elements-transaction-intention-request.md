
# V1 Elements Transaction Intention Request

## Structure

`V1ElementsTransactionIntentionRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `action` | [`ActionEnum`](../../doc/models/action-enum.md) | Optional | The transaction action to be performed with the transaction intention. `sale`, `auth-only`, `avs-only`, `tokenization`.<br><br>**Default**: `ActionEnum::SALE` |
| `digital_wallets_only` | `TrueClass \| FalseClass` | Optional | **Default**: `false` |
| `methods` | [`Array[Method50]`](../../doc/models/method-50.md) | Optional | By default the system will try to offer all the availables payment methods from your account. However, if you need to display only cc or ach only use the corresponding product transaction id.<br><br>**Constraints**: *Minimum Items*: `1`, *Unique Items Required* |
| `amount` | `Integer` | Optional | The total transaction amount to be charged with the transaction intention. Allowed on the actions: `sale`, `auth-only`, `refund`<br><br>**Constraints**: `>= 1`, `<= 999999999` |
| `tax_amount` | Integer \| nil | Optional | This is a container for any-of cases.<br><br>**Constraints**: `>= 1`, `<= 999999999` |
| `secondary_amount` | Integer \| nil | Optional | This is a container for any-of cases.<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `location_id` | `String` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `contact_id` | `String` | Optional | Contact ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `save_account` | TrueClass \| FalseClass \| nil | Optional | This is a container for any-of cases. |
| `save_account_title` | String \| nil | Optional | This is a container for any-of cases.<br><br>**Constraints**: *Maximum Length*: `16` |
| `title` | String \| nil | Optional | This is a container for any-of cases.<br><br>**Constraints**: *Maximum Length*: `16` |
| `ach_sec_code` | [`AchSecCodeEnum`](../../doc/models/ach-sec-code-enum.md) | Optional | SEC code for the transaction if it's an ACH transaction.<br><br>**Default**: `AchSecCodeEnum::WEB` |
| `bank_funded_only_override` | TrueClass \| FalseClass \| nil | Optional | This is a container for any-of cases. |
| `allow_partial_authorization_override` | TrueClass \| FalseClass \| nil | Optional | This is a container for any-of cases. |
| `auto_decline_cvv_override` | TrueClass \| FalseClass \| nil | Optional | This is a container for any-of cases. |
| `auto_decline_street_override` | TrueClass \| FalseClass \| nil | Optional | This is a container for any-of cases. |
| `auto_decline_zip_override` | TrueClass \| FalseClass \| nil | Optional | This is a container for any-of cases. |
| `message` | `String` | Optional | A custom text message that displays after the payment is processed.<br><br>**Constraints**: *Maximum Length*: `120` |

## Example (as JSON)

```json
{
  "action": "sale",
  "digitalWalletsOnly": false,
  "amount": 1099,
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "contact_id": "11e95f8ec39de8fbdb0a4f1a",
  "ach_sec_code": "WEB",
  "methods": [
    {
      "type": "ach",
      "product_transaction_id": "product_transaction_id4"
    }
  ],
  "tax_amount": 50
}
```

