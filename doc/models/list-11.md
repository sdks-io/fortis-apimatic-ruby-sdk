
# List 11

*This model accepts additional fields of type Object.*

## Structure

`List11`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account_vault_id` | `String` | Optional | Token ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `token_id` | `String` | Optional | Token ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `contact_id` | `String` | Optional | Contact ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `account_vault_api_id` | `String` | Optional | Token API ID<br><br>**Constraints**: *Maximum Length*: `64` |
| `token_api_id` | `String` | Optional | Token API ID<br><br>**Constraints**: *Maximum Length*: `64` |
| `joi` | [`Joi`](../../doc/models/joi.md) | Optional | - |
| `active` | `TrueClass \| FalseClass` | Optional | Active |
| `description` | `String` | Optional | Description<br><br>**Constraints**: *Maximum Length*: `36` |
| `end_date` | `String` | Optional | End date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `installment_total_count` | `Integer` | Optional | Installment Total Count<br><br>**Constraints**: `>= 1`, `<= 999` |
| `interval` | `Integer` | Optional | Interval<br><br>**Constraints**: `>= 0`, `<= 365` |
| `interval_type` | [`IntervalType`](../../doc/models/interval-type.md) | Optional | - |
| `location_id` | `String` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `notification_days` | `Integer` | Optional | Notification Days<br><br>**Constraints**: `>= 0`, `<= 365` |
| `payment_method` | [`PaymentMethod1`](../../doc/models/payment-method-1.md) | Optional | - |
| `product_transaction_id` | `String` | Optional | Product Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `recurring_id` | `String` | Optional | Recurring ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `recurring_api_id` | `String` | Optional | Recurring Api ID<br><br>**Constraints**: *Maximum Length*: `64` |
| `start_date` | `String` | Optional | Start date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `status` | [`Status`](../../doc/models/status.md) | Optional | - |
| `transaction_amount` | `Integer` | Optional | Transaction amount |
| `terms_agree` | `TrueClass \| FalseClass` | Optional | Terms Agree |
| `terms_agree_ip` | `String` | Optional | Terms Agree Ip |
| `recurring_c_1` | `String` | Optional | Custom field used for integrations<br><br>**Constraints**: *Maximum Length*: `128` |
| `recurring_c_2` | `String` | Optional | Custom field used for integrations<br><br>**Constraints**: *Maximum Length*: `128` |
| `recurring_c_3` | `String` | Optional | Custom field used for integrations<br><br>**Constraints**: *Maximum Length*: `128` |
| `send_to_proc_as_recur` | `TrueClass \| FalseClass` | Optional | Send To Proc As Recur |
| `tags` | [`Array[Tag]`](../../doc/models/tag.md) | Optional | Tag Information on `expand` |
| `secondary_amount` | `Integer` | Optional | Retained Amount |
| `currency` | `String` | Optional | - |
| `id` | `String` | Optional | Recurring ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `next_run_date` | `String` | Optional | Next Run Date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `recurring_type_id` | [`RecurringTypeId`](../../doc/models/recurring-type-id.md) | Optional | - |
| `installment_amount_total` | `Integer` | Optional | Installment Amount Total |
| `created_user_id` | `String` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `log_emails` | [`Array[LogEmail]`](../../doc/models/log-email.md) | Optional | Log Email Information on `expand` |
| `contact` | [`Contact3`](../../doc/models/contact-3.md) | Optional | - |
| `account_vault` | [`AccountVault1`](../../doc/models/account-vault-1.md) | Optional | - |
| `created_user` | [`User9`](../../doc/models/user-9.md) | Optional | - |
| `signature` | [`Signature1`](../../doc/models/signature-1.md) | Optional | - |
| `payment_schedule` | `Array[String]` | Optional | Payment Schedule Information on `expand`<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `location` | [`Location18`](../../doc/models/location-18.md) | Optional | - |
| `product_transaction` | [`ProductTransaction1`](../../doc/models/product-transaction-1.md) | Optional | - |
| `next_run_date_min` | `String` | Optional | Next Run Date Min Information on `expand`<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `next_run_date_max` | `String` | Optional | Next Run Date Max Information on `expand`<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `all_tags` | [`Array[AllTag]`](../../doc/models/all-tag.md) | Optional | All Tag Information on `expand` |
| `changelogs` | [`Array[Changelog]`](../../doc/models/changelog.md) | Optional | Changelog Information on `expand` |
| `forecast` | [`Forecast1`](../../doc/models/forecast-1.md) | Optional | - |
| `recurring_splits` | [`Array[RecurringSplit]`](../../doc/models/recurring-split.md) | Optional | Recurring Split Information on `expand` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "account_vault_id": "11e95f8ec39de8fbdb0a4f1a",
  "token_id": "11e95f8ec39de8fbdb0a4f1a",
  "contact_id": "11e95f8ec39de8fbdb0a4f1a",
  "account_vault_api_id": "token1234abcd",
  "token_api_id": "token1234abcd",
  "active": true,
  "description": "Description",
  "end_date": "2021-12-01",
  "installment_total_count": 20,
  "interval": 1,
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "notification_days": 2,
  "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "recurring_id": "11e95f8ec39de8fbdb0a4f1a",
  "recurring_api_id": "recurring1234abcd",
  "start_date": "2021-12-01",
  "transaction_amount": 300,
  "terms_agree": true,
  "terms_agree_ip": "192.168.0.10",
  "recurring_c1": "recurring custom data 1",
  "recurring_c2": "recurring custom data 2",
  "recurring_c3": "recurring custom data 3",
  "send_to_proc_as_recur": true,
  "secondary_amount": 100,
  "currency": "USD",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "next_run_date": "2021-12-01",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "installment_amount_total": 99999999,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "next_run_date_min": "2021-12-01",
  "next_run_date_max": "2021-12-01",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

