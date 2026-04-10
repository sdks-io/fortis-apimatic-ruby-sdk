
# Primary Location

Primary Location Information on `expand`

*This model accepts additional fields of type Object.*

## Structure

`PrimaryLocation`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `id` | `String` | Optional | Location ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `created_ts` | `Integer` | Optional | Created Time Stamp |
| `modified_ts` | `Integer` | Optional | Modified Time Stamp |
| `account_number` | `String` | Optional | Account number<br><br>**Constraints**: *Maximum Length*: `32`, *Pattern*: `^[a-zA-Z0-9\-_]+$` |
| `address` | [`Address6`](../../doc/models/address-6.md) | Optional | - |
| `branding_domain_id` | `String` | Optional | GUID for Branding Domain<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `contact_email_trx_receipt_default` | `TrueClass \| FalseClass` | Optional | If true, will email contact receipt for any transaction |
| `default_ach` | `String` | Optional | GUID for Location's default ACH Product Transaction<br><br>**Constraints**: *Minimum Length*: `24`, *Maximum Length*: `36` |
| `default_cc` | `String` | Optional | GUID for Location's default CC Product Transaction<br><br>**Constraints**: *Minimum Length*: `24`, *Maximum Length*: `36` |
| `email_reply_to` | `String` | Optional | Used as from email address when sending various notifications<br><br>**Constraints**: *Maximum Length*: `64` |
| `fax` | `String` | Optional | Fax number<br><br>**Constraints**: *Minimum Length*: `10`, *Maximum Length*: `10`, *Pattern*: `^\d{10}$` |
| `location_api_id` | `String` | Optional | Location api ID<br><br>**Constraints**: *Maximum Length*: `36` |
| `location_api_key` | `String` | Optional | Location api key<br><br>**Constraints**: *Maximum Length*: `36` |
| `location_c_1` | `String` | Optional | Can be used to store custom information for location.<br><br>**Constraints**: *Maximum Length*: `128` |
| `location_c_2` | `String` | Optional | Can be used to store custom information for location.<br><br>**Constraints**: *Maximum Length*: `128` |
| `location_c_3` | `String` | Optional | Can be used to store custom information for location.<br><br>**Constraints**: *Maximum Length*: `128` |
| `name` | `String` | Optional | Name of the company<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `64` |
| `office_phone` | `String` | Optional | Office phone number<br><br>**Constraints**: *Minimum Length*: `10`, *Maximum Length*: `10` |
| `office_ext_phone` | `String` | Optional | Office phone extension number<br><br>**Constraints**: *Maximum Length*: `10` |
| `tz` | `String` | Optional | Time zone<br><br>**Constraints**: *Maximum Length*: `30` |
| `parent_id` | `String` | Optional | Location GUID of the parent location<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `show_contact_notes` | `TrueClass \| FalseClass` | Optional | If set to true will show 'Notes' tab on Contact |
| `show_contact_files` | `TrueClass \| FalseClass` | Optional | If set to true will show 'Files' tab on Contact |
| `created_user_id` | `String` | Optional | User ID Created the register<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `location_type` | `Object` | Optional | - |
| `parent_name` | `String` | Optional | Name of the parent location |
| `ticket_hash_key` | `String` | Optional | Ticket Hash Key<br><br>**Constraints**: *Maximum Length*: `36` |
| `additional_access` | [`AdditionalAccess`](../../doc/models/additional-access.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "id": "11e95f8ec39de8fbdb0a4f1a",
  "created_ts": 1422040992,
  "modified_ts": 1422040992,
  "account_number": "5454545454545454",
  "branding_domain_id": "11e95f8ec39de8fbdb0a4f1a",
  "contact_email_trx_receipt_default": true,
  "default_ach": "11e608a7d515f1e093242bb2",
  "default_cc": "11e608a442a5f1e092242dda",
  "email_reply_to": "email@domain.com",
  "fax": "3339998822",
  "location_api_id": "location-111111",
  "location_api_key": "AE34BBCAADF4AE34BBCAADF4",
  "location_c1": "custom 1",
  "location_c2": "custom 2",
  "location_c3": "custom data 3",
  "name": "Sample Company Headquarters",
  "office_phone": "2481234567",
  "office_ext_phone": "1021021209",
  "tz": "America/New_York",
  "parent_id": "11e95f8ec39de8fbdb0a4f1a",
  "show_contact_notes": true,
  "show_contact_files": true,
  "created_user_id": "11e95f8ec39de8fbdb0a4f1a",
  "ticket_hash_key": "A5F443CADF4AE34BBCAADF4",
  "address": {
    "city": "city6",
    "state": "state2",
    "postal_code": "postal_code8",
    "country": {
      "key1": "val1",
      "key2": "val2"
    },
    "street": "street6",
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

