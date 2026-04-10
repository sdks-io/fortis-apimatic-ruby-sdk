
# List 18

*This model accepts additional fields of type Object.*

## Structure

`List18`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `additional_amounts` | [`Array[AdditionalAmount]`](../../doc/models/additional-amount.md) | Optional | Additional amounts |
| `billing_address` | [`BillingAddress2`](../../doc/models/billing-address-2.md) | Optional | - |
| `checkin_date` | `String` | Optional | Checkin Date - The time difference between checkin_date and checkout_date must be less than or equal to 99 days. NOTE: if checkin_date is in the future, set the advance_deposit to 1<br><br>> Required if merchant industry type is lodging.<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `checkout_date` | `String` | Optional | Checkout Date - The time difference between checkin_date and checkout_date must be less than or equal to 99 days.<br><br>> Required if merchant industry type is lodging.<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `clerk_number` | `String` | Optional | Clerk or Employee Identifier<br><br>**Constraints**: *Maximum Length*: `16` |
| `contact_api_id` | `String` | Optional | This can be supplied in place of contact_id if you would like to use a contact for the transaction and are using your own custom api_id's to track contacts in the system.<br><br>**Constraints**: *Maximum Length*: `36` |
| `contact_id` | `String` | Optional | If contact_id is provided, ensure it belongs to the same location as the transaction. You cannot move transaction across locations.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `custom_data` | `Object` | Optional | A field that allows custom JSON to be entered to store extra data. |
| `customer_id` | `String` | Optional | Can be used by Merchants to identify Contacts in our system by an ID from another system.<br><br>**Constraints**: *Maximum Length*: `64` |
| `description` | `String` | Optional | Description<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `64` |
| `iias_ind` | `Object` | Optional | - |
| `image_front` | `String` | Optional | A base64 encoded string for the image.  Used with Check21 ACH transactions. |
| `image_back` | `String` | Optional | A base64 encoded string for the image.  Used with Check21 ACH transactions. |
| `installment` | `TrueClass \| FalseClass` | Optional | Flag that is allowed to be passed on card not present industries to signify the transaction is a fixed installment plan transaction. |
| `installment_number` | `Integer` | Optional | If this is a fixed installment plan and installment field is being passed as 1, then this field must have a vlue of 1-999 specifying the current installment number that is running.<br><br>**Constraints**: `>= 1`, `<= 999` |
| `installment_count` | `Integer` | Optional | If this is a fixed installment plan and installment field is being passed as 1, then this field must have a vlue of 1-999 specifying the total number of installments on the plan. This number must be grater than or equal to installment_number.<br><br>**Constraints**: `>= 1`, `<= 999` |
| `recurring_flag` | `Object` | Optional | - |
| `installment_counter` | `Integer` | Optional | Installment Counter<br><br>**Constraints**: `>= 1`, `<= 999` |
| `installment_total` | `Integer` | Optional | Installment Total<br><br>**Constraints**: `>= 1`, `<= 999` |
| `subscription` | `TrueClass \| FalseClass` | Optional | Subscription |
| `standing_order` | `TrueClass \| FalseClass` | Optional | Standing Order |
| `location_api_id` | `String` | Optional | This can be supplied in place of location_id for the transaction if you are using your own custom api_id's for your locations.<br><br>**Constraints**: *Maximum Length*: `36` |
| `location_id` | `String` | Optional | A valid Location Id to associate the transaction with.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `product_transaction_id` | `String` | Optional | The Product's method (cc/ach) has to match the action. If not provided, the API will use the default configured for the Location.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `advance_deposit` | `TrueClass \| FalseClass` | Optional | Advance Deposit |
| `no_show` | `TrueClass \| FalseClass` | Optional | Used in Lodging |
| `notification_email_address` | `String` | Optional | If email is supplied then receipt will be emailed |
| `order_number` | `String` | Optional | Required for CC transactions , if merchant's deposit account's duplicate check per batch has 'order_number' field<br><br>**Constraints**: *Maximum Length*: `32` |
| `po_number` | `String` | Optional | Purchase Order number<br><br>**Constraints**: *Maximum Length*: `64` |
| `quick_invoice_id` | `String` | Optional | Can be used to associate a transaction to a Quick Invoice.  Quick Invoice transactions will have a value for this field automatically.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `recurring` | [`Recurring`](../../doc/models/recurring.md) | Optional | - |
| `recurring_number` | `Integer` | Optional | If this is an ongoing recurring and recurring field is being passed as 1, then this field must have a vlue of 1-999 specifying the current recurring number that is running.<br><br>**Constraints**: `>= 1`, `<= 999` |
| `room_num` | `String` | Optional | Used in Lodging<br><br>**Constraints**: *Maximum Length*: `12` |
| `room_rate` | `Integer` | Optional | Required if merchant industry type is lodging. |
| `save_account` | `TrueClass \| FalseClass` | Optional | Specifies to save account to contacts profile if account_number/track_data is present with either contact_id or contact_api_id in params. |
| `save_account_title` | `String` | Optional | If saving token while running a transaction, this will be the title of the token.<br><br>**Constraints**: *Maximum Length*: `16` |
| `subtotal_amount` | `Integer` | Optional | This field is allowed and required for transactions that have a product where surcharge is configured. Use only integer numbers, so $10.99 will be 1099.<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `surcharge_amount` | `Integer` | Optional | This field is allowed and required for transactions that have a product where surcharge is configured. Use only integer numbers, so $10.99 will be 1099.<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `tags` | [`Array[Tag]`](../../doc/models/tag.md) | Optional | Tag Information on `expand` |
| `tax` | `Integer` | Optional | Amount of Sales tax - If supplied, this amount should be included in the total transaction_amount field. Use only integer numbers, so $10.99 will be 1099.<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `tip_amount` | `Integer` | Optional | Optional tip amount. Tip is not supported for lodging and ecommerce merchants. Use only integer numbers, so $10.99 will be 1099.<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `transaction_amount` | `Integer` | Optional | Amount of the transaction. This should always be the desired settle amount of the transaction. Use only integer numbers, so $10.99 will be 1099.<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `secondary_amount` | `Integer` | Optional | Retained Amount of the transaction. This should always be less than transaction amount. Use only integer numbers, so $10.99 will be 1099<br><br>**Constraints**: `>= 0`, `<= 999999999` |
| `transaction_api_id` | `String` | Optional | See api_id page for more details<br><br>**Constraints**: *Maximum Length*: `64` |
| `transaction_c_1` | `String` | Optional | Custom field 1 for api users to store custom data<br><br>**Constraints**: *Maximum Length*: `128` |
| `transaction_c_2` | `String` | Optional | Custom field 2 for api users to store custom data<br><br>**Constraints**: *Maximum Length*: `128` |
| `transaction_c_3` | `String` | Optional | Custom field 3 for api users to store custom data<br><br>**Constraints**: *Maximum Length*: `128` |
| `bank_funded_only_override` | `TrueClass \| FalseClass` | Optional | Bank Funded Only Override |
| `allow_partial_authorization_override` | `TrueClass \| FalseClass` | Optional | Allow Partial Authorization Override |
| `auto_decline_cvv_override` | `TrueClass \| FalseClass` | Optional | Auto Decline CVV Override |
| `auto_decline_street_override` | `TrueClass \| FalseClass` | Optional | Auto Decline Street Override |
| `auto_decline_zip_override` | `TrueClass \| FalseClass` | Optional | Auto Decline Zip Override |
| `ebt_type` | `Object` | Optional | - |
| `id` | `String` | Optional | Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `terminal_id` | `String` | Optional | Terminal ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `account_holder_name` | `String` | Optional | For CC, this is the 'Name (as it appears) on Card'. For ACH, this is the 'Name on Account'.<br><br>> Required for ACH transactions if account_vault_id is not provided. For CC transactions that are run through a terminal, this field may be overwritten by data acquired from the credit card track data.<br><br>**Constraints**: *Maximum Length*: `32` |
| `account_type` | `String` | Optional | Required for ACH transactions if account_vault_id is not provided.<br><br>> For ACH, allowed values are 'checking' or 'savings'. For CC, this field is read only. The system will identify card type and generate a value for this field automatically. possible values are: visa, mc, disc, amex, jcb, diners, and debit.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `32` |
| `token_api_id` | `String` | Optional | This can be supplied in place of account_vault_id if you would like to use an token for the transaction and are using your own custom api_id's to track accountvaults in the system.<br><br>**Constraints**: *Maximum Length*: `36` |
| `token_id` | `String` | Optional | Required if account_number,  track_data, micr_data is not provided.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `ach_identifier` | `String` | Optional | Required for ACH transactions in certain scenarios.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1` |
| `ach_sec_code` | `Object` | Optional | - |
| `auth_amount` | `Integer` | Optional | Authorization Amount<br><br>**Constraints**: `<= 999999999` |
| `auth_code` | `String` | Optional | Required on force transactions and EBT voucher clear sale/refund. Ignored for all other actions.<br><br>**Constraints**: *Minimum Length*: `6`, *Maximum Length*: `6` |
| `avs` | `Object` | Optional | - |
| `avs_enhanced` | `String` | Optional | AVS Enhanced<br><br>**Constraints**: *Minimum Length*: `1` |
| `cardholder_present` | `TrueClass \| FalseClass` | Optional | If the cardholder is present at the point of service |
| `card_present` | `TrueClass \| FalseClass` | Optional | A POST only field to specify whether or not the card is present.<br><br>> This field will be defaulted to '1' for all card present industries (retail, lodging, restaurant) and '0' for card not present industries (MOTO/e-commerce).<br>> For lodging, if the no_show flag is set to '1', this field will automatically be set to '0'.<br>> For transactions where account_vault_id is used, this filed will be set to '0'. |
| `check_number` | `String` | Optional | Required for transactions using TEL SEC code.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `15` |
| `customer_ip` | `String` | Optional | Can be used to store customer IP Address |
| `cvv_response` | `String` | Optional | Obfuscated CVV<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `1` |
| `entry_mode_id` | `Object` | Optional | - |
| `emv_receipt_data` | `Object` | Optional | - |
| `first_six` | `String` | Optional | First six numbers of account_number.  Automatically generated by system.<br><br>**Constraints**: *Minimum Length*: `6`, *Maximum Length*: `6` |
| `last_four` | `String` | Optional | Last four numbers of account_number.  Automatically generated by the system.<br><br>**Constraints**: *Minimum Length*: `4`, *Maximum Length*: `4` |
| `payment_method` | [`PaymentMethod9`](../../doc/models/payment-method-9.md) | Optional | - |
| `terminal_serial_number` | `String` | Optional | If transaction was processed using a terminal, this field would contain the terminal's serial number<br><br>**Constraints**: *Maximum Length*: `36`, *Pattern*: `^[a-zA-Z0-9]*$` |
| `transaction_settlement_status` | `String` | Optional | (Deprecated field)<br><br>**Constraints**: *Maximum Length*: `32` |
| `charge_back_date` | `String` | Optional | Charge Back Date (ACH Trxs)<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `is_recurring` | `TrueClass \| FalseClass` | Optional | Flag that is allowed to be passed on card not present industries to signify the transaction is a fixed installment plan transaction. |
| `notification_email_sent` | `TrueClass \| FalseClass` | Optional | Indicates if email receipt has been sent |
| `par` | `String` | Optional | A field usually returned form the processor to uniquely identifier a specific cardholder's credit card.<br><br>**Constraints**: *Maximum Length*: `36` |
| `reason_code_id` | `Object` | Optional | - |
| `recurring_id` | `String` | Optional | A unique identifer used to associate a transaction with a Recurring.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `settle_date` | `String` | Optional | Settle date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `status_code` | `Object` | Optional | - |
| `transaction_batch_id` | `String` | Optional | For cc transactions, this is the id of the batch the transaction belongs to (not to be confused with batch number). This will be null for transactions that do not settle (void and authonly).<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `type_id` | `Object` | Optional | - |
| `verbiage` | `String` | Optional | Verbiage -Do not use verbiage to see if the transaction was approved, use status_id |
| `voucher_number` | `String` | Optional | Voucher Number |
| `void_date` | `String` | Optional | void date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `batch` | `String` | Optional | Batch |
| `terms_agree` | `TrueClass \| FalseClass` | Optional | Terms Agreement |
| `response_message` | `String` | Optional | Response Message<br><br>**Constraints**: *Maximum Length*: `255` |
| `return_date` | `String` | Optional | Return Date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `trx_source_id` | `Object` | Optional | - |
| `routing_number` | `String` | Optional | This field is read only for ach on transactions. Must be supplied if account_vault_id is not provided. |
| `trx_source_code` | `Object` | Optional | - |
| `paylink_id` | `String` | Optional | Paylink Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `currency_code` | `Float` | Optional | Currency Code<br><br>**Default**: `840` |
| `is_accountvault` | `TrueClass \| FalseClass` | Optional | Is Token Transaction |
| `created_user_id` | `String` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `modified_user_id` | `String` | Optional | Last User ID that updated the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `transaction_code` | `String` | Optional | Transaction Code |
| `effective_date` | `String` | Optional | For ACH only, this is optional and defaults to current day.<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `notification_phone` | `String` | Optional | Notification Phone. Country code not included |
| `cavv_result` | `String` | Optional | Cavv Result |
| `is_token` | `TrueClass \| FalseClass` | Optional | Is Token Transaction |
| `account_vault_id` | `String` | Optional | Token ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `hosted_payment_page_id` | `String` | Optional | Hosted Payment Page Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `stan` | `String` | Optional | - |
| `currency` | `String` | Optional | Currency |
| `card_bin` | `String` | Optional | Card Bin |
| `wallet_type` | `String` | Optional | This value provides information from where the transaction was initialized (Such as In-App provider) |
| `account_vault` | [`AccountVault1`](../../doc/models/account-vault-1.md) | Optional | - |
| `quick_invoice` | [`QuickInvoice1`](../../doc/models/quick-invoice-1.md) | Optional | - |
| `log_emails` | [`Array[LogEmail]`](../../doc/models/log-email.md) | Optional | Log Email Information on `expand` |
| `is_voidable` | `TrueClass \| FalseClass` | Optional | Is Voidable Information on `expand` |
| `is_reversible` | `TrueClass \| FalseClass` | Optional | Is Reversible Information on `expand` |
| `is_refundable` | `TrueClass \| FalseClass` | Optional | Is Refundable Information on `expand` |
| `is_completable` | `TrueClass \| FalseClass` | Optional | Is Competable Information on `expand` |
| `is_settled` | `TrueClass \| FalseClass` | Optional | Is Settled Information on `expand` |
| `created_user` | [`User9`](../../doc/models/user-9.md) | Optional | - |
| `location` | [`Location18`](../../doc/models/location-18.md) | Optional | - |
| `contact` | [`Contact3`](../../doc/models/contact-3.md) | Optional | - |
| `changelogs` | [`Array[Changelog]`](../../doc/models/changelog.md) | Optional | Changelog Information on `expand` |
| `product_transaction` | [`ProductTransaction1`](../../doc/models/product-transaction-1.md) | Optional | - |
| `all_tags` | [`Array[AllTag]`](../../doc/models/all-tag.md) | Optional | All Tag Information on `expand` |
| `tag_transactions` | [`Array[TagTransaction]`](../../doc/models/tag-transaction.md) | Optional | TagTransaction Information on `expand` |
| `declined_recurring_notification` | [`DeclinedRecurringNotification1`](../../doc/models/declined-recurring-notification-1.md) | Optional | - |
| `payment_recurring_notification` | [`PaymentRecurringNotification1`](../../doc/models/payment-recurring-notification-1.md) | Optional | - |
| `developer_company` | [`DeveloperCompany1`](../../doc/models/developer-company-1.md) | Optional | - |
| `terminal` | [`Terminal2`](../../doc/models/terminal-2.md) | Optional | - |
| `hosted_payment_page` | [`HostedPaymentPage1`](../../doc/models/hosted-payment-page-1.md) | Optional | - |
| `transaction_level_3` | [`Data29`](../../doc/models/data-29.md) | Optional | - |
| `developer_company_id` | `String` | Optional | Developer Company Id Information on `expand` |
| `transaction_histories` | [`Array[TransactionHistory]`](../../doc/models/transaction-history.md) | Optional | Transaction History Information on `expand` |
| `surcharge_transaction` | [`SurchargeTransaction1`](../../doc/models/surcharge-transaction-1.md) | Optional | - |
| `surcharge` | [`Surcharge1`](../../doc/models/surcharge-1.md) | Optional | - |
| `signature` | [`Signature1`](../../doc/models/signature-1.md) | Optional | - |
| `reason_code` | [`ReasonCode1`](../../doc/models/reason-code-1.md) | Optional | - |
| `type` | [`Type7`](../../doc/models/type-7.md) | Optional | - |
| `status` | [`Status7`](../../doc/models/status-7.md) | Optional | - |
| `transaction_batch` | [`TransactionBatch1`](../../doc/models/transaction-batch-1.md) | Optional | - |
| `transaction_splits` | [`Array[TransactionSplit]`](../../doc/models/transaction-split.md) | Optional | Transaction Split Information on `expand` |
| `postback_logs` | [`Array[PostbackLog]`](../../doc/models/postback-log.md) | Optional | Postback Log Information on `expand` |
| `currency_type` | [`CurrencyType1`](../../doc/models/currency-type-1.md) | Optional | - |
| `transaction_references` | [`Array[TransactionReference]`](../../doc/models/transaction-reference.md) | Optional | Transaction Reference Information on `expand` |
| `rejected_transaction_ach_retries` | [`Array[RejectedTransactionAchRetry]`](../../doc/models/rejected-transaction-ach-retry.md) | Optional | [object Object] |
| `return_fee_transaction_ach_retry` | [`RejectedTransactionAchRetry`](../../doc/models/rejected-transaction-ach-retry.md) | Optional | - |
| `retry_transaction_ach_retry` | [`RejectedTransactionAchRetry`](../../doc/models/rejected-transaction-ach-retry.md) | Optional | - |
| `is_retriable` | `TrueClass \| FalseClass` | Optional | [object Object] |
| `saved_account` | [`SavedAccount1`](../../doc/models/saved-account-1.md) | Optional | - |
| `balances` | [`Array[Balance]`](../../doc/models/balance.md) | Optional | Additional amounts |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "checkin_date": "2021-12-01",
  "checkout_date": "2021-12-01",
  "clerk_number": "AE1234",
  "contact_id": "11e95f8ec39de8fbdb0a4f1a",
  "custom_data": {
    "data1": "custom1",
    "data2": "custom2"
  },
  "customer_id": "customerid",
  "description": "some description",
  "image_front": "U29tZVN0cmluZ09idmlvdXNseU5vdEJhc2U2NEVuY29kZWQ=",
  "image_back": "U29tZVN0cmluZ09idmlvdXNseU5vdEJhc2U2NEVuY29kZWQ=",
  "installment": true,
  "installment_number": 1,
  "installment_count": 1,
  "installment_counter": 1,
  "installment_total": 1,
  "subscription": false,
  "standing_order": false,
  "location_api_id": "location-api-id-florida-2",
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "advance_deposit": false,
  "no_show": false,
  "notification_email_address": "johnsmith@smiths.com",
  "order_number": "433659378839",
  "po_number": "555555553123",
  "quick_invoice_id": "11e95f8ec39de8fbdb0a4f1a",
  "recurring_number": 1,
  "room_num": "303",
  "room_rate": 95,
  "save_account": false,
  "save_account_title": "John Account",
  "subtotal_amount": 599,
  "surcharge_amount": 100,
  "tax": 0,
  "tip_amount": 0,
  "transaction_amount": 0,
  "secondary_amount": 0,
  "transaction_api_id": "transaction-payment-abcd123",
  "transaction_c1": "custom-data-1",
  "transaction_c2": "custom-data-2",
  "transaction_c3": "custom-data-3",
  "bank_funded_only_override": false,
  "allow_partial_authorization_override": false,
  "auto_decline_cvv_override": false,
  "auto_decline_street_override": false,
  "auto_decline_zip_override": false,
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "terminal_id": "11e95f8ec39de8fbdb0a4f1a",
  "account_holder_name": "smith",
  "account_type": "checking",
  "token_id": "11e95f8ec39de8fbdb0a4f1a",
  "ach_identifier": "P",
  "auth_amount": 1,
  "auth_code": "BR349K",
  "avs_enhanced": "N",
  "cardholder_present": true,
  "card_present": true,
  "check_number": "8520748520963",
  "customer_ip": "192.168.0.10",
  "cvv_response": "N",
  "first_six": "545454",
  "last_four": "5454",
  "terminal_serial_number": "1234567890",
  "charge_back_date": "2021-12-01",
  "is_recurring": true,
  "notification_email_sent": true,
  "par": "Q1J4Z28RKA1EBL470G9XYG90R5D3E",
  "recurring_id": "11e95f8ec39de8fbdb0a4f1a",
  "settle_date": "2021-12-01",
  "transaction_batch_id": "11e95f8ec39de8fbdb0a4f1a",
  "verbiage": "APPROVED",
  "voucher_number": "1234",
  "void_date": "2021-12-01",
  "batch": "2",
  "terms_agree": true,
  "return_date": "2021-12-01",
  "routing_number": "051904524",
  "paylink_id": "11e95f8ec39de8fbdb0a4f1a",
  "currency_code": 840,
  "is_accountvault": true,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "effective_date": "2021-12-01",
  "is_token": true,
  "account_vault_id": "11e95f8ec39de8fbdb0a4f1a",
  "hosted_payment_page_id": "11e95f8ec39de8fbdb0a4f1a",
  "is_voidable": true,
  "is_reversible": true,
  "is_refundable": true,
  "is_completable": true,
  "is_settled": true,
  "developer_company_id": "Sample Developer Company ID",
  "additional_amounts": [
    {
      "type": {
        "key1": "val1",
        "key2": "val2"
      },
      "amount": 6,
      "account_type": {
        "key1": "val1",
        "key2": "val2"
      },
      "currency": 154.64,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "type": {
        "key1": "val1",
        "key2": "val2"
      },
      "amount": 6,
      "account_type": {
        "key1": "val1",
        "key2": "val2"
      },
      "currency": 154.64,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    },
    {
      "type": {
        "key1": "val1",
        "key2": "val2"
      },
      "amount": 6,
      "account_type": {
        "key1": "val1",
        "key2": "val2"
      },
      "currency": 154.64,
      "exampleAdditionalProperty": {
        "key1": "val1",
        "key2": "val2"
      }
    }
  ],
  "billing_address": {
    "city": "city2",
    "state": "state6",
    "postal_code": "postal_code0",
    "street": "street8",
    "phone": "phone2",
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

