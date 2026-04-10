
# Location Billing Account

*This model accepts additional fields of type Object.*

## Structure

`LocationBillingAccount`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `title` | `String` | Optional | Title<br><br>**Constraints**: *Maximum Length*: `64` |
| `location_id` | `String` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `location_api_id` | `String` | Optional | Location Api Id |
| `ach_sec_code` | `String` | Optional | Ach Sec Code |
| `account_number` | `String` | Optional | Account number |
| `routing` | `String` | Optional | Routing |
| `exp_date` | `String` | Optional | Exp Date |
| `billing_zip` | `String` | Optional | Billing Zip<br><br>**Constraints**: *Minimum Length*: `3`, *Maximum Length*: `10`, *Pattern*: `^[a-zA-Z0-9\-\s]+$` |
| `account_type` | `String` | Optional | Account Type |
| `account_holder_name` | `String` | Optional | Account Holder Name |
| `id` | `String` | Optional | Location Billing Account Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `created_user_id` | `String` | Optional | Created User Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `modified_user_id` | `String` | Optional | Modified User Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `billing_descriptor` | `String` | Optional | Billing Descriptor |
| `payment_method` | `String` | Optional | Billing Descriptor |
| `portfolio_id` | `String` | Optional | Portfolio Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "title": "Billing Acccount Title",
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "exp_date": "0722",
  "billing_zip": "48375",
  "account_holder_name": "John Smith",
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "modified_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "portfolio_id": "11e95f8ec39de8fbdb0a4f1a",
  "location_api_id": "location_api_id4",
  "ach_sec_code": "ach_sec_code6",
  "account_number": "account_number4",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

