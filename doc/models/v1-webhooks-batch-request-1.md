
# V1 Webhooks Batch Request 1

## Structure

`V1WebhooksBatchRequest1`

## Fields

| Name | Type | Tags | Description |
|  --- | --- | --- | --- |
| `attempt_interval` | `Integer` | Optional | Number of seconds before another retry is submitted<br><br>**Default**: `300`<br><br>**Constraints**: `>= 300`, `<= 86400` |
| `basic_auth_username` | `String` | Optional | The Basic authorization username for the URL, if not supplied, the postback will be submitted without Basic authorization headers<br><br>> This is only expandable for response but settable in the POST/PUT request<br><br>**Constraints**: *Maximum Length*: `512` |
| `basic_auth_password` | `String` | Optional | The basic authorization password<br><br>> This is only expandable for response but settable in the POST/PUT request<br><br>**Constraints**: *Maximum Length*: `512` |
| `expands` | `String` | Optional | An option list of expanded data to send with base data. (i.e. set this field to “contact,account_vault” to get the contact an accountvault used to run a transaction.)<br><br>**Constraints**: *Maximum Length*: `512` |
| `format` | [`FormatEnum`](../../doc/models/format-enum.md) | Optional | Options include: api-default |
| `is_active` | `TrueClass \| FalseClass` | Optional | Flag to indicate whether configuration is active (in effect). |
| `location_id` | `String` | Optional | The location identifier of the resource you want to recieve postbacks from.<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `location_api_id` | `String` | Optional | Location Api ID |
| `on_create` | `TrueClass \| FalseClass` | Optional | To receive postbacks on the creation of a resource |
| `on_update` | `TrueClass \| FalseClass` | Optional | To receive postbacks on the updating of a resource |
| `on_delete` | `TrueClass \| FalseClass` | Optional | To receive postbacks when the record is deleted |
| `legacy` | `TrueClass \| FalseClass` | Optional | Prefer the legacy api format.<br><br>**Default**: `true` |
| `postback_config_id` | `String` | Optional | Postback Config ID<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `product_transaction_id` | `String` | Optional | Required when using 'transaction' or 'transactionbatch' resource<br><br>**Constraints**: *Pattern*: `^(([0-9a-fA-F\-]{24,36})\|(([0-9a-fA-F]{8})-(([0-9a-fA-F]{4}\-){3})([0-9a-fA-F]{12})))$` |
| `resource` | [`Resource12Enum`](../../doc/models/resource-12-enum.md) | Optional | The resource you want to subscribe the postbacks to.<br><br>> Possible values include: 'contact', 'transaction', 'transactionbatch'<br><br>**Constraints**: *Maximum Length*: `128` |
| `number_of_attempts` | `Integer` | Optional | Maximum number of attempts on failure<br><br>**Constraints**: `>= 1`, `<= 5` |
| `url` | `String` | Optional | The URL where the postback will be submitted<br><br>**Constraints**: *Maximum Length*: `512` |

## Example (as JSON)

```json
{
  "attempt_interval": 300,
  "basic_auth_username": "tester",
  "basic_auth_password": "Test@522",
  "expands": "changelogs,tags",
  "format": "api-default",
  "is_active": true,
  "location_id": "11e95f8ec39de8fbdb0a4f1a",
  "on_create": true,
  "on_update": true,
  "on_delete": true,
  "legacy": true,
  "postback_config_id": "11e95f8ec39de8fbdb0a4f1a",
  "product_transaction_id": "11e95f8ec39de8fbdb0a4f1a",
  "resource": "contact",
  "number_of_attempts": 1,
  "url": "https://127.0.0.1/receiver"
}
```

