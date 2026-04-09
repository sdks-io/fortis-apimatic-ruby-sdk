
# List 9

## Structure

`List9`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `location_id` | `String` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `cc_product_transaction_id` | `String` | Optional | cc_product_transaction_id that has paylinks enabled in the service settings.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `email` | `String` | Optional | Optional. An email address that should be used as the "To" address when sending a Paylink Notification email.<br><br>**Constraints**: *Maximum Length*: `128` |
| `amount_due` | `Integer` | Optional | This is the amount that need to be paid (automatically calculated by system). amount_due= sum of items in item_list<br><br>**Constraints**: `>= 1`, `<= 999999999` |
| `location_api_id` | `String` | Optional | Location Api Id. System id |
| `contact_id` | `String` | Optional | Include the Contact_id that the Paylink will belong to. This will allow you to query the List All Paylinks and filter_by Contact_id to see the status of all the contacts Paylinks.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `contact_api_id` | `String` | Optional | Integrator provided unique id that was provided during the contact creation for the Fortis Contact. Include the Contact_id that the Paylink will belong to. This will allow you to query the List All Paylinks and filter_by Contact_id to see the status of all the contacts Paylinks. |
| `paylink_api_id` | `String` | Optional | Integrator provided id that prevents duplicate Paylinke Api Id's per location.<br><br>**Constraints**: *Maximum Length*: `64` |
| `ach_product_transaction_id` | `String` | Optional | ACH product transaction on which Paylink is created. This field is optional and will default to default_ach product if not supplied at all. Either this or cc_product_transaction_id must be supplied. Changes are allowed on PUT if payments have not been made against Paylink.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `expire_date` | `String` | Optional | Expire Date of Paylink. Optional<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `display_product_transaction_receipt_details` | `TrueClass \| FalseClass` | Optional | Display Product Transaction Receipt Details. Show the receipt details after the successful payment |
| `display_billing_fields` | `TrueClass \| FalseClass` | Optional | Display Billing Fields to show the billing field inputs in the paylink form |
| `delivery_method` | [`DeliveryMethodEnum`](../../doc/models/delivery-method-enum.md) | Optional | Delivery Method<br><br>> 0 - Do not send, use the expand parameter of payment_url in the create paylink request to obtain the payment_url to embed into your messaging system.<br>> <br>> 1 - Email. Will send an email to the provided address in the email field.<br>> <br>> 2 - SMS. Text message the Paylink. Check with sales rep for cost.<br>> <br>> 3 - Both |
| `cell_phone` | `String` | Optional | Required if delivery_method is set to 2[SMS], 3[Both email and sms], this will be the recipient of the SMS<br><br>**Constraints**: *Minimum Length*: `10`, *Maximum Length*: `10`, *Pattern*: `^\d{1,10}$` |
| `description` | `String` | Optional | Add a Description for reporting purposes<br><br>**Constraints**: *Maximum Length*: `64` |
| `store_token` | `TrueClass \| FalseClass` | Optional | Store Token to create a token_id(account_vault_id) to be used for future payment types(CC Sale Tokenized, ACH Debit Tokenized) |
| `store_token_title` | `String` | Optional | Store Token Title can be used to set the name of the token, sucha John Smith<br><br>**Constraints**: *Maximum Length*: `16` |
| `paylink_action` | [`PaylinkActionEnum`](../../doc/models/paylink-action-enum.md) | Optional | the action that will be used by the form when making the payment possible values: sale, auth-only |
| `bank_funded_only_override` | `TrueClass \| FalseClass` | Optional | Bank Funded Only Override |
| `tags` | `Array[String]` | Optional | Used to apply tags to a paylink. |
| `redirect_url_delay` | `Float` | Optional | Redirect URL Delay in seconds<br><br>**Default**: `15`<br><br>**Constraints**: `<= 15` |
| `redirect_url_on_approve` | `String` | Optional | Redirect URL On Approved transactions |
| `redirect_url_on_decline` | `String` | Optional | Redirect URL On Declined transactions |
| `id` | `String` | Optional | System generatedPaylink Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `status_id` | `TrueClass \| FalseClass` | Optional | (DEPRECATED) Status Id |
| `status_code` | [`StatusCode12Enum`](../../doc/models/status-code-12-enum.md) | Optional | The various statuses of the paylink.  0=Unpaid \| 1=Paid |
| `active` | `TrueClass \| FalseClass` | Optional | Paylink is still Active |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `created_user_id` | `String` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `modified_user_id` | `String` | Optional | Last User ID that updated the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |

## Example (as JSON)

```json
{
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "cc_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "email": "email@domain.com",
  "amount_due": 1,
  "contact_id": "11e95f8ec39de8fbdb0a4f1a",
  "ach_product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "expire_date": "2021-12-01",
  "display_product_transaction_receipt_details": true,
  "display_billing_fields": true,
  "delivery_method": 0,
  "cell_phone": "3339998822",
  "description": "Description",
  "store_token": false,
  "store_token_title": "John Account",
  "bank_funded_only_override": false,
  "redirect_url_delay": 15,
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "status_id": true,
  "status_code": 1,
  "active": true,
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "location_api_id": "location_api_id8"
}
```

