
# V1 Recurrings Request 1

*This model accepts additional fields of type Object.*

## Structure

`V1RecurringsRequest1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `next_run_date` | `String` | Optional | Next Run Date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `account_vault_id` | `String` | Optional | Token ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `token_id` | `String` | Optional | Token ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `active` | `TrueClass \| FalseClass` | Optional | Active |
| `description` | `String` | Optional | Description<br><br>**Constraints**: *Maximum Length*: `36` |
| `end_date` | `String` | Optional | End date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `installment_total_count` | `Integer` | Optional | Installment Total Count<br><br>**Constraints**: `>= 1`, `<= 999` |
| `interval` | `Integer` | Optional | Interval<br><br>**Constraints**: `>= 0`, `<= 365` |
| `interval_type` | `Object` | Optional | - |
| `location_id` | `String` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `notification_days` | `Integer` | Optional | Notification Days<br><br>**Constraints**: `>= 0`, `<= 365` |
| `payment_method` | `Object` | Optional | - |
| `product_transaction_id` | `String` | Optional | Product Transaction ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `recurring_id` | `String` | Optional | Recurring ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `recurring_api_id` | `String` | Optional | Recurring Api ID<br><br>**Constraints**: *Maximum Length*: `64` |
| `start_date` | `String` | Optional | Start date<br><br>**Constraints**: *Maximum Length*: `10`, *Pattern*: `^[\d]{4}-[\d]{2}-[\d]{2}$` |
| `status` | `Object` | Optional | - |
| `transaction_amount` | `Integer` | Optional | Transaction amount |
| `terms_agree` | `TrueClass \| FalseClass` | Optional | Terms Agree |
| `terms_agree_ip` | `String` | Optional | Terms Agree Ip |
| `recurring_c_1` | `String` | Optional | Custom field used for integrations<br><br>**Constraints**: *Maximum Length*: `128` |
| `recurring_c_2` | `String` | Optional | Custom field used for integrations<br><br>**Constraints**: *Maximum Length*: `128` |
| `recurring_c_3` | `String` | Optional | Custom field used for integrations<br><br>**Constraints**: *Maximum Length*: `128` |
| `send_to_proc_as_recur` | `TrueClass \| FalseClass` | Optional | Send To Proc As Recur |
| `tags` | `Array[String]` | Optional | Tags |
| `secondary_amount` | `Integer` | Optional | Retained Amount |
| `contact_id` | `String` | Optional | Contact ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "next_run_date": "2021-12-01",
  "account_vault_id": "11e95f8ec39de8fbdb0a4f1a",
  "token_id": "11e95f8ec39de8fbdb0a4f1a",
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
  "contact_id": "11e95f8ec39de8fbdb0a4f1a",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

