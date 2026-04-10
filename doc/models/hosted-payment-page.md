
# Hosted Payment Page

Hosted Payment Page Information on `expand`

*This model accepts additional fields of type Object.*

## Structure

`HostedPaymentPage`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `user_id` | `String` | Optional | User ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `location_id` | `String` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `location_api_id` | `String` | Optional | Location Api Id |
| `product_transaction_id` | `String` | Optional | Product Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `title` | `String` | Optional | Title<br><br>**Constraints**: *Maximum Length*: `64` |
| `redirect_url_delay` | `Float` | Optional | Redirect Url Delay<br><br>**Default**: `15`<br><br>**Constraints**: `<= 15` |
| `min_payment_amount` | `Integer` | Optional | Min Payment Amount<br><br>**Constraints**: `>= 0` |
| `max_payment_amount` | `Integer` | Optional | Max Payment Amount<br><br>**Default**: `9999999999`<br><br>**Constraints**: `<= 9999999999` |
| `redirect_url_on_approve` | `String` | Optional | Redirect Url On Approval |
| `redirect_url_on_decline` | `String` | Optional | Redirect Url On Decline |
| `field_configuration` | [`FieldConfiguration2`](../../doc/models/field-configuration-2.md) | Optional | - |
| `encryption_key` | `String` | Optional | Encryption Key<br><br>**Constraints**: *Minimum Length*: `32`, *Maximum Length*: `32` |
| `stylesheet_url` | `String` | Optional | Stylesheet Url |
| `parent_send_message` | `TrueClass \| FalseClass` | Optional | Parent Send Message |
| `hide_optional_fields` | `TrueClass \| FalseClass` | Optional | Hide Optional Fields |
| `id` | `String` | Optional | Hosted Payment Page Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `created_user_id` | `String` | Optional | System generated id for user who created record<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `modified_user_id` | `String` | Optional | System generated id for user who created record<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "user_id": "11e95f8ec39de8fbdb0a4f1a",
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "title": "Sample title",
  "redirect_url_delay": 15,
  "min_payment_amount": 0,
  "max_payment_amount": 9999999999,
  "parent_send_message": true,
  "hide_optional_fields": true,
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "location_api_id": "location_api_id2",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

