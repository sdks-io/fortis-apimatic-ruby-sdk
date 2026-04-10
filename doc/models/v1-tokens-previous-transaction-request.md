
# V1 Tokens Previous Transaction Request

*This model accepts additional fields of type Object.*

## Structure

`V1TokensPreviousTransactionRequest`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `account_holder_name` | `String` | Optional | Account holder name<br><br>> For CC, this is the 'Name (as it appears) on Card'. For ACH, this is the 'Name on Account'.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `32` |
| `account_vault_api_id` | `String` | Optional | This field can be used to correlate Tokens in our system to data within an outside software integration<br><br>> Must be unique per location. When running a transaction and using a stored token, this field can be used in place of account_vault_id.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `64` |
| `token_api_id` | `String` | Optional | This field can be used to correlate Tokens in our system to data within an outside software integration<br><br>> Must be unique per location. When running a transaction and using a stored token, this field can be used in place of token_id.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `64` |
| `accountvault_c_1` | `String` | Optional | DEPRECATED (Use token_c1 instead)<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `accountvault_c_2` | `String` | Optional | DEPRECATED (Use token_c2 instead)<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `accountvault_c_3` | `String` | Optional | DEPRECATED (Use token_c3 instead)<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `token_c_1` | `String` | Optional | Custom field 1 for API users to store custom data<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `token_c_2` | `String` | Optional | Custom field 2 for API users to store custom data<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `token_c_3` | `String` | Optional | Custom field 3 for API users to store custom data<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `128` |
| `ach_sec_code` | `Object` | Optional | - |
| `billing_address` | [`BillingAddress7`](../../doc/models/billing-address-7.md) | Optional | - |
| `contact_id` | `String` | Optional | Used to associate the Token with a Contact.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `customer_id` | `String` | Optional | Used to store a customer identification number.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `50` |
| `identity_verification` | [`IdentityVerification5`](../../doc/models/identity-verification-5.md) | Optional | - |
| `location_id` | `String` | Required | A valid Location Id associated with the Contact for this Token<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `previous_account_vault_api_id` | `String` | Optional | Can be used to pull payment info from a previous token api id.<br><br>**Constraints**: *Maximum Length*: `64` |
| `previous_token_api_id` | `String` | Optional | Can be used to pull payment info from a previous token api id.<br><br>**Constraints**: *Maximum Length*: `64` |
| `previous_account_vault_id` | `String` | Optional | Can be used to pull payment info from a previous token.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `previous_token_id` | `String` | Optional | Can be used to pull payment info from a previous token.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `previous_transaction_id` | `String` | Required | Can be used to pull payment info from a previous transaction.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `account_number` | `String` | Optional | Account number<br><br>> For CC transactions, a credit card number. For ACH transactions, a bank account number. String lengths are conditional, CC should be 13-19 and ACH should be 4-19.<br><br>**Constraints**: *Minimum Length*: `4`, *Maximum Length*: `19`, *Pattern*: `^[\d]+$` |
| `terms_agree` | `TrueClass \| FalseClass` | Optional | Terms agreement. |
| `terms_agree_ip` | `String` | Optional | The ip address of the client that agreed to terms. |
| `title` | `String` | Optional | Used to describe the Token for easier identification within our UI.<br><br>**Constraints**: *Minimum Length*: `1`, *Maximum Length*: `16` |
| `token_import_id` | `String` | Optional | Token Import Id<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `secure_directory_server_transaction_id` | `String` | Optional | (ECOMM) Directory Server Transaction ID (Such as XID, TAVV) |
| `secure_protocol_version` | `Integer` | Optional | (ECOMM)  Secure Program Protocol Version |
| `secure_auth_data` | `String` | Optional | (ECOMM) The token authentication value associated with 3D secure transactions (Such as CAVV, UCAF auth data) |
| `secure_collection_indicator` | `Integer` | Optional | (ECOMM) Used for UCAF collection indicator or Discover Autentication type |
| `three_ds_server_trans_id` | `String` | Optional | 3DS Server Transaction ID.  If this field is sent and 3DS authentication was done with Fortis, the 3DS fields secure_directory_server_transaction_id, secure_protocol_version, and secure_collection_indicator will be pre-populated. |
| `acs_transaction_id` | `String` | Optional | ACS Transaction ID<br><br>**Constraints**: *Maximum Length*: `36` |
| `joi` | [`Joi4`](../../doc/models/joi-4.md) | Optional | - |
| `additional_properties` | `Hash[String, Object]` | Optional | - |

## Example (as JSON)

```json
{
  "account_holder_name": "John Smith",
  "account_vault_api_id": "accountvaultabcd",
  "token_api_id": "tokenabcd",
  "accountvault_c1": "accountvault custom 1",
  "accountvault_c2": "accountvault custom 2",
  "accountvault_c3": "accountvault custom 3",
  "token_c1": "token custom 1",
  "token_c2": "token custom 2",
  "token_c3": "token custom 3",
  "contact_id": "11e95f8ec39de8fbdb0a4f1a",
  "customer_id": "123456",
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "previous_account_vault_api_id": "previousaccountvault123456",
  "previous_token_api_id": "previousaccountvault123456",
  "previous_account_vault_id": "11e95f8ec39de8fbdb0a4f1a",
  "previous_token_id": "11e95f8ec39de8fbdb0a4f1a",
  "previous_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "account_number": "545454545454545",
  "terms_agree": true,
  "terms_agree_ip": "192.168.0.10",
  "title": "Test CC Account",
  "token_import_id": "11e95f8ec39de8fbdb0a4f1a",
  "secure_directory_server_transaction_id": "d65e93c3-35ab-41ba-b307-767bfc19eae",
  "secure_protocol_version": 2,
  "secure_auth_data": "vVwL7UNHCf8W8M2LAfvRChNHN7c%3D",
  "three_ds_server_trans_id": "d65e93c3-35ab-41ba-b307-767bfc19eae",
  "acs_transaction_id": "13c701a3-5a88-4c45-89e9-ef65e50a8bf9",
  "exampleAdditionalProperty": {
    "key1": "val1",
    "key2": "val2"
  }
}
```

