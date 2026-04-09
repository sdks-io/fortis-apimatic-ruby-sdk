
# Product Transaction

Product Transaction Information on `expand`

## Structure

`ProductTransaction`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `processor_version` | `String` | Optional | Processor Version |
| `industry_type` | [`IndustryTypeEnum`](../../doc/models/industry-type-enum.md) | Optional | Industry Type<br><br>**Constraints**: *Maximum Length*: `45` |
| `title` | `String` | Optional | Title<br><br>**Constraints**: *Maximum Length*: `64` |
| `payment_method` | [`PaymentMethodEnum`](../../doc/models/payment-method-enum.md) | Optional | Payment method |
| `processor` | [`ProcessorEnum`](../../doc/models/processor-enum.md) | Optional | Processor |
| `mcc` | `String` | Optional | MCC<br><br>**Constraints**: *Maximum Length*: `4`, *Pattern*: `^\d+$` |
| `tax_surcharge_config` | [`TaxSurchargeConfigEnum`](../../doc/models/tax-surcharge-config-enum.md) | Optional | Tax Surcharge Config<br><br>**Default**: `TaxSurchargeConfigEnum::ENUM_2` |
| `terminal_id` | `String` | Optional | Terminal ID<br><br>**Constraints**: *Maximum Length*: `24` |
| `partner` | [`PartnerEnum`](../../doc/models/partner-enum.md) | Optional | Partner<br><br>**Constraints**: *Maximum Length*: `24` |
| `product_ach_pv_store_id` | `String` | Optional | Product Ach Pv Store ID |
| `invoice_adjustment_title` | `String` | Optional | Invoice Adjustment Title |
| `location_id` | `String` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `location_api_id` | `String` | Optional | Location Api ID |
| `billing_location_api_id` | `String` | Optional | Billing Location API ID |
| `portfolio_id` | `String` | Optional | Portfolio ID |
| `portfolio_validation_rule` | `String` | Optional | Product Validation Rule |
| `sub_processor` | `String` | Optional | Sub Processor<br><br>**Constraints**: *Maximum Length*: `48` |
| `surcharge` | `Object` | Optional | Surcharge |
| `processor_data` | `Object` | Optional | - |
| `vt_clerk_number` | `TrueClass \| FalseClass` | Optional | Vt Clerk Number |
| `vt_billing_phone` | `TrueClass \| FalseClass` | Optional | Card Type JCB |
| `vt_enable_tip` | `TrueClass \| FalseClass` | Optional | VT Enable Tip |
| `ach_allow_debit` | `TrueClass \| FalseClass` | Optional | Ach Allow Debit |
| `ach_allow_credit` | `TrueClass \| FalseClass` | Optional | Ach Allow Credit |
| `ach_allow_refund` | `TrueClass \| FalseClass` | Optional | Ach Allow Refund |
| `vt_cvv` | `TrueClass \| FalseClass` | Optional | VT CVV |
| `vt_street` | `TrueClass \| FalseClass` | Optional | VT Street |
| `vt_zip` | `TrueClass \| FalseClass` | Optional | VT Zip |
| `vt_order_num` | `TrueClass \| FalseClass` | Optional | VT Order Num |
| `vt_enable` | `TrueClass \| FalseClass` | Optional | VT Enable |
| `receipt_show_contact_name` | `TrueClass \| FalseClass` | Optional | Receipt Show Contact Name |
| `display_avs` | `TrueClass \| FalseClass` | Optional | Display Avs |
| `card_type_visa` | `TrueClass \| FalseClass` | Optional | Card Type Visa |
| `card_type_mc` | `TrueClass \| FalseClass` | Optional | Card Type Mc |
| `card_type_disc` | `TrueClass \| FalseClass` | Optional | Card Type Disc |
| `card_type_amex` | `TrueClass \| FalseClass` | Optional | Card Type Amex |
| `card_type_diners` | `TrueClass \| FalseClass` | Optional | Card Type Dinners |
| `card_type_jcb` | `TrueClass \| FalseClass` | Optional | - |
| `card_type_ebt` | `TrueClass \| FalseClass` | Optional | Card Type EBT |
| `allow_ebt_cash_benefit` | `TrueClass \| FalseClass` | Optional | Allow EBT Cash Benefit |
| `allow_ebt_food_stamp` | `TrueClass \| FalseClass` | Optional | Allow EBT Food Stamp |
| `invoice_location` | `TrueClass \| FalseClass` | Optional | Invoice Location |
| `allow_partial_authorization` | `TrueClass \| FalseClass` | Optional | Allow Partial Authorization |
| `allow_recurring_partial_authorization` | `TrueClass \| FalseClass` | Optional | Allow Recurring Partial Authorization |
| `auto_decline_cvv` | `TrueClass \| FalseClass` | Optional | Auto Decline Cvv |
| `auto_decline_street` | `TrueClass \| FalseClass` | Optional | Auto Decline Street |
| `auto_decline_zip` | `TrueClass \| FalseClass` | Optional | Auto Decline ZIP |
| `split_payments_allow` | `TrueClass \| FalseClass` | Optional | Split Payments Allow |
| `vt_show_custom_fields` | `TrueClass \| FalseClass` | Optional | Vt Show Custom Fields |
| `receipt_show_custom_fields` | `TrueClass \| FalseClass` | Optional | Receipt Show Custom Fields |
| `vt_override_sales_tax_allowed` | `TrueClass \| FalseClass` | Optional | Vt Override Sales Tax Allowed |
| `vt_enable_sales_tax` | `TrueClass \| FalseClass` | Optional | Vt Enable Sales Tax |
| `vt_require_zip` | `TrueClass \| FalseClass` | Optional | Vt Require ZIP |
| `vt_require_street` | `TrueClass \| FalseClass` | Optional | Vt Require Street |
| `auto_decline_cavv` | `TrueClass \| FalseClass` | Optional | Auto Decline Cavv |
| `merchant_id` | `String` | Optional | Merchant ID<br><br>**Constraints**: *Maximum Length*: `24` |
| `receipt_header` | `String` | Optional | Receipt Header<br><br>**Constraints**: *Maximum Length*: `255` |
| `receipt_footer` | `String` | Optional | Receipt Footer<br><br>**Constraints**: *Maximum Length*: `255` |
| `receipt_add_account_above_signature` | `String` | Optional | Receipt Add Account Above Signature<br><br>**Constraints**: *Maximum Length*: `1032` |
| `receipt_add_recurring_above_signature` | `String` | Optional | Receipt Add Recurring Above Signature<br><br>**Constraints**: *Maximum Length*: `1032` |
| `receipt_vt_above_signature` | `String` | Optional | Receipt VT Above Signature<br><br>**Constraints**: *Maximum Length*: `1032` |
| `default_transaction_type` | [`DefaultTransactionTypeEnum`](../../doc/models/default-transaction-type-enum.md) | Optional | Default Transaction Type |
| `username` | `String` | Optional | Username<br><br>**Constraints**: *Maximum Length*: `512` |
| `password` | `String` | Optional | Passowrd<br><br>**Constraints**: *Maximum Length*: `512` |
| `current_batch` | `Float` | Optional | Current Batch<br><br>**Default**: `1`<br><br>**Constraints**: `>= 1`, `<= 9999` |
| `dup_check_per_batch` | `String` | Optional | Dup Check Per Batch<br><br>**Constraints**: *Maximum Length*: `500` |
| `agent_code` | `String` | Optional | Agent Code<br><br>**Constraints**: *Maximum Length*: `16`, *Pattern*: `^[\w\-]+$` |
| `paylink_allow` | `TrueClass \| FalseClass` | Optional | Paylink Allow |
| `quick_invoice_allow` | `TrueClass \| FalseClass` | Optional | Quick Invoice Allow |
| `level_3_allow` | `TrueClass \| FalseClass` | Optional | Level3 Allow |
| `payfac_enable` | `TrueClass \| FalseClass` | Optional | Payfac Enable |
| `enable_3_ds` | `TrueClass \| FalseClass` | Optional | Enable 3DS |
| `sales_office_id` | `String` | Optional | Sales Office ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `hosted_payment_page_max_allowed` | `Float` | Optional | Hosted Payment Page Max Allowed<br><br>**Default**: `5`<br><br>**Constraints**: `>= 1`, `<= 999` |
| `hosted_payment_page_allow` | `TrueClass \| FalseClass` | Optional | Hosted Payment Page Allow |
| `surcharge_id` | `String` | Optional | Surcharge ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `allow_big_commerce` | `TrueClass \| FalseClass` | Optional | Allow Big Commerce |
| `level_3_default` | [`Level3Default`](../../doc/models/level-3-default.md) | Optional | Level3 Default |
| `cau_subscribe_type_id` | [`CauSubscribeTypeIdEnum`](../../doc/models/cau-subscribe-type-id-enum.md) | Optional | Cau Subscribe Type ID |
| `cau_account_number` | `String` | Optional | Cau Account Number<br><br>**Constraints**: *Minimum Length*: `32`, *Maximum Length*: `32`, *Pattern*: `^[a-zA-Z0-9\-]+$` |
| `location_billing_account_id` | `String` | Optional | Location Billing Account ID |
| `product_billing_group_id` | `String` | Optional | Product Billing Group ID |
| `account_number` | `String` | Optional | Account number<br><br>**Constraints**: *Maximum Length*: `32`, *Pattern*: `^[a-zA-Z0-9\-_]+$` |
| `run_avs_on_accountvault_create` | `TrueClass \| FalseClass` | Optional | Run Avs On Accountvault Create |
| `accountvault_expire_notification_email_enable` | `TrueClass \| FalseClass` | Optional | Accountvault Expire Notification Email Enable |
| `debit_allow_void` | `TrueClass \| FalseClass` | Optional | Debit Allow Void |
| `quick_invoice_text_to_pay` | `TrueClass \| FalseClass` | Optional | Quick Invoice Text To Pay |
| `authentication_code` | `String` | Optional | Authentication Code |
| `sms_enable` | `TrueClass \| FalseClass` | Optional | SMS Enable |
| `vt_show_currency` | `TrueClass \| FalseClass` | Optional | Vt Show Currency |
| `receipt_show_currency` | `TrueClass \| FalseClass` | Optional | Receipt Show Currency |
| `allow_blind_refund` | `TrueClass \| FalseClass` | Optional | Allow Blind Refund |
| `vt_show_company_name` | `TrueClass \| FalseClass` | Optional | Vt Show Company Name |
| `receipt_show_company_name` | `TrueClass \| FalseClass` | Optional | Receipt Show Company Name |
| `bank_funded_only` | `TrueClass \| FalseClass` | Optional | Bank Funded Only |
| `require_cvv_on_keyed_cnp` | `TrueClass \| FalseClass` | Optional | Require CVV on keyed CNP |
| `require_cvv_on_tokenized_cnp` | `TrueClass \| FalseClass` | Optional | Require CVV on tokenized CNP |
| `show_secondary_amount` | `TrueClass \| FalseClass` | Optional | Show Retained Amount |
| `allow_secondary_amount` | `TrueClass \| FalseClass` | Optional | Allow Retained Amount |
| `show_google_pay` | `TrueClass \| FalseClass` | Optional | Vt Require Street |
| `show_apple_pay` | `TrueClass \| FalseClass` | Optional | Vt Require Street |
| `batch_risk_config` | [`BatchRiskConfig`](../../doc/models/batch-risk-config.md) | Optional | Batch Risk Config |
| `currency_code` | `Float` | Optional | Currency Code |
| `enable_ach_validation` | `TrueClass \| FalseClass` | Optional | Enable ACH Validation |
| `enable_ach_retry` | `TrueClass \| FalseClass` | Optional | Enable ACH Retry |
| `allow_softpos` | `TrueClass \| FalseClass` | Optional | Allow Soft POS |
| `id` | `String` | Optional | User Reports ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `receipt_logo` | `String` | Optional | Receipt Logo |
| `active` | `TrueClass \| FalseClass` | Optional | Active |
| `tz` | `String` | Optional | TZ |
| `current_stan` | `Float` | Optional | Current Stan<br><br>**Default**: `1` |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `created_user_id` | `String` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `modified_user_id` | `String` | Optional | Last User ID that updated the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `product_transaction_api_id` | `String` | Optional | Product Transaction API ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `transaction_amount_notification_threshold` | `Integer` | Optional | Transaction Amount Notification Treshold |
| `is_secondary_amount_allowed` | `TrueClass \| FalseClass` | Optional | Allow Retained Amount |
| `fortis_id` | `String` | Optional | - |
| `product_billing_group_code` | `String` | Optional | Product Billing Group Code |
| `cau_subscribe_type_code` | [`CauSubscribeTypeCodeEnum`](../../doc/models/cau-subscribe-type-code-enum.md) | Optional | Cau Subscribe Type Code |
| `merchant_code` | `String` | Optional | Merchant Code<br><br>**Constraints**: *Maximum Length*: `24` |

## Example (as JSON)

```json
{
  "processor_version": "1_0_0",
  "title": "My terminal",
  "payment_method": "cc",
  "processor": "zgate",
  "mcc": "1111",
  "tax_surcharge_config": 2,
  "partner": "standalone",
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "vt_clerk_number": true,
  "vt_billing_phone": true,
  "vt_enable_tip": true,
  "ach_allow_debit": true,
  "ach_allow_credit": true,
  "ach_allow_refund": true,
  "vt_cvv": true,
  "vt_street": true,
  "vt_zip": true,
  "vt_order_num": true,
  "vt_enable": true,
  "receipt_show_contact_name": true,
  "display_avs": true,
  "card_type_visa": true,
  "card_type_mc": true,
  "card_type_disc": true,
  "card_type_amex": true,
  "card_type_diners": true,
  "card_type_jcb": true,
  "card_type_ebt": true,
  "allow_ebt_cash_benefit": true,
  "allow_ebt_food_stamp": true,
  "invoice_location": true,
  "allow_partial_authorization": true,
  "allow_recurring_partial_authorization": true,
  "auto_decline_cvv": true,
  "auto_decline_street": true,
  "auto_decline_zip": true,
  "split_payments_allow": true,
  "vt_show_custom_fields": true,
  "receipt_show_custom_fields": true,
  "vt_override_sales_tax_allowed": true,
  "vt_enable_sales_tax": true,
  "vt_require_zip": true,
  "vt_require_street": true,
  "auto_decline_cavv": true,
  "current_batch": 34,
  "paylink_allow": false,
  "quick_invoice_allow": false,
  "level3_allow": false,
  "payfac_enable": false,
  "enable_3ds": false,
  "sales_office_id": "11e95f8ec39de8fbdb0a4f1a",
  "hosted_payment_page_max_allowed": 5,
  "hosted_payment_page_allow": false,
  "surcharge_id": "11e95f8ec39de8fbdb0a4f1a",
  "allow_big_commerce": false,
  "cau_subscribe_type_id": 0,
  "location_billing_account_id": "11eb88b873980c64a21e5fd2",
  "product_billing_group_id": "nofees",
  "account_number": "12345678",
  "run_avs_on_accountvault_create": false,
  "accountvault_expire_notification_email_enable": false,
  "debit_allow_void": false,
  "quick_invoice_text_to_pay": false,
  "sms_enable": false,
  "vt_show_currency": true,
  "receipt_show_currency": false,
  "allow_blind_refund": false,
  "vt_show_company_name": false,
  "receipt_show_company_name": false,
  "bank_funded_only": false,
  "require_cvv_on_keyed_cnp": true,
  "require_cvv_on_tokenized_cnp": true,
  "show_secondary_amount": false,
  "allow_secondary_amount": false,
  "show_google_pay": true,
  "show_apple_pay": true,
  "currency_code": 840,
  "enable_ach_validation": false,
  "enable_ach_retry": false,
  "allow_softpos": false,
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "active": true,
  "current_stan": 1,
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "product_transaction_api_id": "11e95f8ec39de8fbdb0a4f1a",
  "is_secondary_amount_allowed": false,
  "fortis_id": "8149742",
  "product_billing_group_code": "nofees",
  "cau_subscribe_type_code": 0,
  "industry_type": "retail"
}
```

